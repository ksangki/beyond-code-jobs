# 11장. Eval Engineer · AI Reliability — 품질을 측정하고 책임지는 사람

> *"Error analysis is not optional. Skip it and everything else is built on sand."*
> — Hamel Husain, hamel.dev (2026)

본론 5개 직업의 마지막 자리입니다. 그리고 *한국 시장에 가장 늦게 들어올* 자리이기도 합니다.

이 자리에 대해 미리 짚어 둘 한 가지가 있습니다. 다른 본론 챕터들과 달리, 11장은 *글로벌 자료의 비중이 더 큽니다*. 한국 자료가 부족해서가 아니라, *직군의 한국 도착이 가장 늦었기 때문*입니다. 비중을 70:30으로 잡았습니다. 그리고 이 비중의 차이 자체를, 11장 한 절에서 *데이터로 다루겠습니다*. 부재가 신호가 됩니다.

먼저 이 자리가 어떻게 일하는지부터 봅니다.

---

## Anthropic의 채용 공고를 그대로 읽어 봅니다

Anthropic이 자기 회사 *Research Engineer, Model Evaluations* 자리의 채용 공고에 적어 둔 책임을 그대로 옮기면 다음과 같습니다.

- *evaluation 플랫폼의 설계와 구현*
- *novel evaluation methodologies — reasoning, safety, helpfulness, harmlessness*
- *high-throughput evaluation pipelines that run during production training*
- *evaluation results를 분석해 failure mode를 식별하고, training 의사결정에 영향을 준다*

요구 사항:
- *ML 모델, 특히 LLM의 evaluation system 설계 경험*
- *distributed computing 경험*

(출처: https://job-boards.greenhouse.io/anthropic/jobs/4990535008)

이 채용 공고를 한 문장으로 옮기면, *모델의 품질을 측정하는 시스템 자체를 만드는 사람*입니다. 모델을 만드는 사람도 아니고, 모델을 응용하는 사람도 아닙니다. *그 사이에서, 측정의 기준을 짜는 사람*입니다.

여기서 한 가지 미묘한 차이가 있습니다. Anthropic의 자리가 *Eval Engineer*의 한 극단 — *frontier lab에서 모델 자체를 평가*하는 자리입니다. 같은 직군이 응용 회사로 내려오면 *제품 evals를 책임지는 자리*가 됩니다. Hamel Husain, Eugene Yan, Shreya Shankar 같은 인플루언서들이 가르치는 *AI Evals* 커리큘럼이 그쪽입니다. 두 가지가 같은 직군의 두 극단이라고 보면 됩니다.

이 책에서는 *응용 회사의 Eval Engineer*에 무게를 두고 다룹니다. 한국 독자가 들어갈 자리에 가장 가까운 극단이기 때문입니다.

---

## 하루의 풍경 — 어느 Eval Engineer의 9시부터 6시까지

가상의 인물입니다. 이름은 **수민**. 미국의 한 시리즈 B AI 회사에서 *AI Reliability Engineer*로 일하고 있습니다. 회사 안에서는 그냥 *Eval Engineer*. 전직은 한국 카카오에서 QA 엔지니어 5년, 그 뒤에 데이터 엔지니어 2년. 9개월 전에 이 회사로 옮겼습니다.

**오전 9시.** 야간 eval 파이프라인 결과 확인. 어제 새 모델 v3.1 후보가 *50개 카테고리의 evals*에서 어떻게 점수를 받았는지 한 표로 정리되어 있습니다. 5개 카테고리에서 *유의미한 회귀*가 잡혔습니다.

수민이 회귀가 잡힌 5개 카테고리를 *수동으로* 들여다봅니다. 한 카테고리에서, 모델이 *결제 정보를 잘못 표시*하는 사례가 12% 늘었습니다. 자동 점수는 *문제 없음*으로 표시되었지만, 수동으로 보니 *작은 숫자 차이*가 결제 금액에서 일어나고 있었습니다.

LLM-as-judge가 이 차이를 잡지 못했다는 게 발견됩니다. *Judge prompt에서 숫자 정확도 항목이 약하다*는 것이 진단입니다.

**오전 10시.** Judge prompt를 개선하는 작업. 숫자 정확도 항목을 더 엄격하게 잡도록 *예시*를 늘립니다. 새 judge로 같은 12% 사례를 다시 돌립니다. 이번에는 잡힙니다. 점수가 *문제 있음*으로 정확히 표시됩니다.

여기서 11장 자리의 가장 큰 일감이 드러납니다. *측정 도구 자체*를 평가하고 개선하는 일. *LLM-as-judge*가 신뢰할 만한지를 *또 다른 평가*로 확인하는 일.

**오전 11시.** 사내 ML 팀과의 회의. *v3.1을 배포할 것인가*에 대한 결정. 수민이 결정의 핵심 데이터를 가져갑니다.

- 50개 카테고리 중 *45개에서 동등 이상*
- *5개에서 회귀*. 그 중 2개가 *결제 관련*. 이 2개가 deal breaker
- *Judge prompt 개선 후 회귀가 정확히 잡혔다는 증거*

결정은 미뤄집니다. 결제 관련 회귀를 잡고 다시 측정한 뒤에 배포. ML 팀이 시스템 프롬프트를 다시 손봅니다.

**오후 12시.** 점심. Hamel Husain이 매주 보내는 *evals 뉴스레터*를 후딱 읽습니다. 이번 호의 핵심 발언이 마음에 박힙니다.

> *"60-80%의 개발 시간을 error analysis에 씁니다. 대부분의 노력은 *자동 체크*를 만드는 게 아니라 *실패를 이해하는* 데 들어갑니다."*

자기 시간 분배도 거의 같습니다. 자동화된 evals보다, *그 evals가 잡지 못한 사례를 손으로 들여다보는 시간*이 더 깁니다.

**오후 1시 30분.** 새 도메인의 evals 작성. 회사가 새로 들어가는 산업이 *법률*입니다. 법률 도메인의 eval 셋이 아직 없습니다. 수민이 *법률 전문가 한 명을 사내 컨설턴트로 섭외*해서 50개 사례를 같이 만듭니다. 각 사례에 *기대하는 답*과 *측정 기준*을 적습니다.

eval 데이터셋을 만드는 일이 *데이터 큐레이션*에 가깝다는 점이 드러납니다. 코드를 짜는 게 아닙니다. *어떤 사례가 모델 품질을 잡는 데 중요한지*를 도메인 전문가와 함께 정의하는 일.

**오후 4시.** 회귀 분석 도구. 자기가 직접 짠 *eval trend 대시보드*. 모델 버전별로, 카테고리별로, eval 점수가 어떻게 변해 왔는지 시각화. 새 데이터를 추가하고, 회사 전체에 공개되는 *주간 evals 보고서*에 한 페이지 추가.

**오후 5시 30분.** 다른 회사의 새 모델 출시 추적. Anthropic이 새 Claude를 출시했습니다. 자기 회사 evals를 *그 새 모델에 한 번 돌려*보는 작업을 자동화에 추가. 결과는 내일 아침에. 만약 다른 회사 모델이 *우리 회사 자체 모델*보다 더 잘 한다면, 그 자체가 *전략 결정의 입력*이 됩니다.

**오후 6시 30분.** 퇴근 전에, 다음 주에 진행할 *eval 워크숍 자료*를 다듬습니다. 회사 안에서 *모든 PM과 엔지니어가 evals를 직접 짤 수 있도록* 가르치는 워크숍. 수민의 일이 *측정 시스템을 운영*하는 것뿐 아니라, *조직 전체의 측정 능력*을 키우는 것까지 포함됩니다.

---

## QA와 무엇이 다른가 — 결정적인 경계선

수민이 QA 5년의 경험을 가지고 들어왔지만, Eval Engineer와 QA는 *비슷한 듯 다른* 자리입니다. 한 표로 정리하겠습니다.

| 항목 | QA Engineer | Eval Engineer |
|---|---|---|
| 측정 단위 | **패스 / 페일** | **분포·점수** |
| 정답의 정의 | 명확 (테스트 케이스에 적힘) | **모호 — 정답을 정의하는 게 일의 일부** |
| 시스템 | 결정적 | **확률적** |
| 회귀의 의미 | 명확한 픽스 가능 | **기준점의 이동, 픽스가 항상 가능하지 않음** |
| 측정 도구 | 단위 테스트, 통합 테스트, E2E | **eval 데이터셋, LLM-as-judge, HELM** |
| 자동화의 한계 | 거의 모든 검증 자동화 가능 | **자동 점수가 인간 판단과 일치하는지를 또 평가해야 함** |
| 책임의 범위 | 출시 전 품질 보장 | **출시 전 + 출시 후 지속 측정** |
| 산출물 | 테스트 코드, 버그 리포트 | **eval 데이터셋, 측정 기준 문서, judge prompt** |

가장 큰 차이가 *정답의 정의*입니다. QA에서는 *맞는 답*이 미리 정해져 있습니다. Eval Engineer에서는 *맞는 답이 무엇인지*를 먼저 정의해야 합니다.

이 차이가 결정적인 이유는, *측정 자체가 새로운 종류의 일감*이 되기 때문입니다. 단순히 *검증을 자동화*하는 게 아니라, *측정 가능한 영역과 측정 어려운 영역의 경계*를 매번 다시 그어야 합니다. Dell'Acqua의 *Jagged Frontier*가 여기에도 적용됩니다. Eval Engineer는 *그 frontier의 지도를 그리는 사람*입니다.

ML Researcher와의 차이도 짚어 두면 좋겠습니다.

| 항목 | ML Researcher | Eval Engineer |
|---|---|---|
| 일의 중심 | **새 모델 만들기** | **만든 모델을 측정하기** |
| 산출물 | 논문, 새 학습 방법, 새 아키텍처 | **평가 시스템, 데이터셋, 측정 기준** |
| 통계 깊이 | 매우 깊음 | 중급 (실험 설계에 충분한 수준) |
| 코드 작성 | 학습 파이프라인 | 평가 파이프라인, 데이터 처리 |

ML Researcher가 *새 모델*을 만든다면, Eval Engineer는 *측정의 기준*을 만듭니다. 같이 일하지만 *역할이 분리*되어 있습니다.

---

## 학술 토대 — 측정 자체가 정말 어렵다는 증거 네 편

이 자리가 *진지한 직군*이 된 이유 중 하나는, *측정 자체가 정말 어렵다*는 게 학술적으로 증명되었기 때문입니다. 네 편의 핵심 논문을 한 번에 정리하겠습니다.

**1. Zheng 외 2023, *Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena*** (NeurIPS 2023, arXiv:2306.05685, 피인용 3,500+).

LLM을 평가자로 쓰는 방법의 기준점이 된 논문. GPT-4 같은 강한 모델이 *통제·크라우드 인간 선호와 80% 이상 일치*한다는 발견. 인간 사이 일치도와 거의 같음. 그러나 4가지 편향이 있음.

- *Position bias.* 앞에 나온 답을 선호.
- *Verbosity bias.* 긴 답을 선호.
- *Self-enhancement bias.* 자기 가족 모델(GPT-4가 GPT 출력을)을 선호. 자기 모델에 +10%p 보너스.
- *제한된 추론.* 깊은 수학·논리 문제에서 흔들림.

> *"Strong LLM judges like GPT-4 can match both controlled and crowdsourced human preferences well, achieving over 80% agreement — yet they exhibit position, verbosity, and self-enhancement biases."*

수민의 하루에서 *judge prompt를 개선*하던 작업이, 이 논문이 짚은 *4가지 편향을 잡는 작업*과 같은 종류입니다. Eval Engineer는 매일 이 편향과 싸웁니다.

**2. Deng 외 2024, *Investigating Data Contamination in Modern Benchmarks for Large Language Models*** (NAACL 2024, arXiv:2311.09783).

LLM 벤치마크가 *학습 데이터에 오염되어 있는지*를 검증한 논문. TS-Guessing(Testset Slot Guessing) 기법으로 객관식 답안의 한 옵션을 마스킹하고 모델에 채우게 시켜 *메모리화 정도*를 측정. 결과:

- ChatGPT의 MMLU 정확히 맞춤(메모리화 추정): **52%**
- GPT-4의 MMLU 정확히 맞춤: **57%**

> *"The high exact-match rates for GPT-4 and ChatGPT on the original MMLU test are indicative of memorization rather than general reasoning ability."*

이 데이터가 무엇을 말하는지가 분명합니다. *AI가 시험을 잘 본다고 일을 잘하는 게 아닙니다.* 시험지를 미리 봤을 가능성이 50%가 넘습니다. *평가를 새로 짜는 사람*이 직업이 되는 이유가 이 논문에 있습니다.

**3. Liang 외, *HELM — Holistic Evaluation of Language Models*** (TMLR 2023, arXiv:2211.09110).

Stanford CRFM의 평가 프레임워크. *16개 시나리오 × 7개 메트릭*(정확도·견고성·공정성·편향·독성·효율 등)을 *동시에* 측정. 단일 점수 대신 *trade-off 노출*이 핵심 가치.

> *"Holistic evaluation surfaces trade-offs that single-number leaderboards systematically obscure."*

단일 점수 leaderboard가 *체계적으로 가리는 trade-off*를 노출시킨다는 것. Eval Engineer가 회사 안에서 *단일 점수 보고를 거부하는* 자리가 되는 학술적 정당성입니다.

**4. Cemri 외 2025, *Why Do Multi-Agent LLM Systems Fail?*** (arXiv:2503.13657, 10장 자료 재활용).

7개 SOTA 다중 에이전트 시스템의 41~86.7% 실패율. 14가지 실패 모드(MASFT). Eval Engineer가 *측정해야 할 카테고리*의 학술적 기반입니다.

이 네 편이 *측정이 왜 어려운지*에 대한 표준 답을 학술에서 정리한 자료들입니다. Eval Engineer 면접에서 *이 네 편 중 어느 것이라도 깊이 토론할 수 있는 후보*가 곧바로 차별화됩니다.

---

## 어떤 사람이 잘 맞나 — 적합도 자가진단 5문항

1. **데이터 감각이 강한가.** 1만 개의 사례를 *분포로* 보는 게 자연스러운가. *몇 개의 outlier*가 무엇을 의미하는지 짚을 수 있는가.

2. **통계적 직관이 있는가.** 통계학을 깊이 공부했을 필요는 없지만, *실험 설계의 기본*(샘플 크기, 통계적 유의성, 신뢰 구간)을 *대화에서 자연스럽게 다룰 수 있는가*.

3. **정성과 정량을 오가는 글쓰기.** 평가 결과를 보고할 때 *숫자만이 아니라 사례*로 풀어 설명할 수 있는가. *왜 이 회귀가 중요한지*를 문장으로 정리할 수 있는가.

4. **합의를 끌어내는 보고가 가능한가.** *모델 배포 여부*를 결정하는 회의에서, *데이터로 결정을 끌어내는* 글쓰기와 말하기가 가능한가. 정치적이지 않은 영역에서, 데이터가 결정을 만들도록 돕는 자리.

5. **측정 자체에 대한 회의가 즐거운가.** *내가 만든 측정 기준이 잘못되었을 가능성*을 매일 의심하는 게 자연스러운가. *측정 자체의 메타 평가*가 일의 본질입니다.

다섯 문항 중 *세 개 이상*에 그렇다고 답할 수 있다면, Eval Engineer가 가까운 자리입니다. 특히 QA, 플랫폼 엔지니어, 데이터 엔지니어, 데이터 분석가 출신이 적합도가 높습니다.

---

## 한국에서의 채용 신호 — 가장 늦게 도착한 자리

도입부 표에서 11장이 ★(가장 적은 별)으로 분류된 이유를 정리해 보겠습니다. 한국 채용 시장에서 *Eval Engineer*라는 정확한 타이틀이 *거의 없습니다*. 가장 가까운 사례 두 가지만 짚을 수 있습니다.

**업스테이지.** *AI Research Engineer (LLM Evaluation)*라는 영문 타이틀로 모집 중. 한국 회사 중에서 가장 명시적으로 *evals*를 직군 이름에 넣은 사례. 다만 *별도 직군*이라기보다 *AI Research Engineer 안의 한 트랙*에 가깝습니다.

**카카오·네이버.** ML Engineer 직무 안에 *평가 책임이 통합*되어 있습니다. *별도 직군이 없음*이라는 표현이 정확합니다. 한 사람이 모델을 만들고, *그 모델의 평가도 자기가 함*. 그래서 *측정에 대한 깊이*가 글로벌 frontier lab보다 얕은 경우가 많습니다.

이 풍경이 한국 시장의 *현재 상태*입니다. 그러나 *부재 자체가 신호*입니다. 다음 한 절에서 풀어 보겠습니다.

---

## 메타 절 — 왜 한국에 가장 늦게 들어오는가

11장의 한국 칸을 *글로벌 자료로 채우지 않는다*는 점이 이 책에서 의도된 선택입니다. 부재 자체를 *데이터*로 다루겠습니다.

**한국에 늦은 다섯 가지 이유:**

**1. 한국 AI 시장이 응용 단계에서 출발했습니다.** Frontier lab(자체 모델 개발)이 글로벌만큼 많지 않습니다. LG AI Research의 EXAONE이 있지만, OpenAI·Anthropic 같은 규모의 *모델 평가 팀*이 한국에는 거의 없습니다. *Frontier lab이 만드는 Eval Engineer 일감*이 한국에는 자리가 적습니다.

**2. 응용 회사에서 평가가 ML Engineer 책임에 통합됩니다.** 카카오·네이버·토스 같은 응용 회사들이 *별도 Eval Engineer*를 채용하지 않습니다. 같은 사람이 모델을 응용하고 평가하는 모델로 굴러갑니다. *역할 분리*가 일어나지 않은 상태입니다.

**3. 한국어 evals의 비표준성.** 영어로 만들어진 표준 벤치마크(MMLU, HELM 등)와 비교 가능한 *한국어 표준 벤치마크*가 아직 정착되지 않았습니다. 각 회사가 *자체 한국어 evals*를 만들지만, *비교 가능성*이 낮아서 직군 표준화가 더딥니다.

**4. 통계·실험 설계 인력의 시장 분리.** 한국에서 *데이터 사이언티스트*와 *ML Engineer*는 분명하게 분리되어 있지만, *Eval Engineer*가 둘 사이의 한 자리로 자리잡는 데 시간이 걸리고 있습니다.

**5. AgentOps와 묶여 들어옴.** 한국에서 *evals를 누가 책임지는가*에 대한 답이, 지난 1~2년 동안 *AgentOps 운영팀*에 통합된 형태로 진행되고 있습니다. SK 에이닷 운영팀이 *프롬프트와 평가를 같이* 다루는 풍경. 별도 *Eval Engineer 직군*이 자리잡지 않은 채, *AgentOps 직군 안에 평가 책임이 통합*되는 형태입니다.

**한국 도착 timeline 가설:** Eval Engineer가 한국에서 *별도 직군*으로 본격 자리잡는 시점은 *2028~2030년*으로 예상합니다. 다른 4개 직군보다 1~2년 더 늦을 가능성이 높습니다.

**그래서 이 자리가 흥미롭습니다.** 한국에서 가장 늦게 들어올 자리라는 것은 *직군이 정해지기 전 가장 큰 자리를 잡을 기회*가 가장 큰 자리이기도 합니다. 지금 한국에서 *Eval Engineer*에 가까운 일을 자처하는 사람이라면, 2~3년 뒤 직군이 표준화될 때 *가장 앞자리*에 있을 수 있습니다.

---

## Husain & Shankar의 표준 — 60-80% 시간을 evals에

Hamel Husain과 Shreya Shankar가 운영하는 *Maven AI Evals* 코스가 4,500명 이상을 졸업시켰습니다. 미국에서 *Eval Engineer 진입의 표준 커리큘럼*에 가까운 위치입니다.

이 코스에서 두 사람이 가장 자주 인용되는 발언이 한 줄입니다.

> *"We spent 60-80% of our development time on error analysis and evaluation. Most effort goes toward understanding failures rather than building automated checks."*

개발 시간의 60~80%를 *error analysis*에 쓴다는 것. 그리고 그 노력의 대부분은 *자동 체크 만들기*가 아니라 *실패 이해*에 들어간다는 것.

같은 글에서 두 사람이 자주 짚는 진단도 인용해 두겠습니다.

> *"Teams jump straight to building LLM judges or dashboards without knowing what they're measuring. They build judges for generic things like 'helpfulness' or 'conciseness' that don't catch real problems. Error analysis is not optional — it's the foundation. Skip it and everything else is built on sand."*

대부분의 팀이 *무엇을 측정하는지 모른 채로* LLM judge나 대시보드 만들기에 직행한다는 것. *Helpfulness*나 *conciseness* 같은 generic 항목으로 judge를 만들지만, *진짜 문제*를 잡지 못한다는 것. *Error analysis*는 선택이 아니라 *토대*. 건너뛰면 모든 것이 *모래 위에 짓는 것*이 됩니다.

이 진단이 Eval Engineer 일의 본질을 짚었습니다. *측정 도구를 만드는 일*보다, *측정해야 할 것을 정의하는 일*이 더 크고 더 어렵습니다.

같은 시리즈에서 Lenny's Newsletter가 한 호의 제목을 *"Evals are the hottest new skill for product builders"*로 정한 적이 있습니다. 직군 이름은 아직 안 정해졌지만, *evals라는 능력 자체*가 가장 뜨거운 스킬이 되어 가고 있다는 시장 진단입니다.

---

## RAG Evals의 6가지 — Jason Liu의 프레임워크

Eval Engineer가 특정 시스템에서 *어떻게 평가를 짜는지*의 구체 예로, Jason Liu가 정리한 *RAG Evals 6 framework*를 짚어 두면 유용합니다.

RAG(Retrieval-Augmented Generation) 시스템의 평가는 6가지 층으로 나뉩니다.

- **Tier 1 (3개):** 전통 정보 검색 메트릭. Retrieval Precision, Retrieval Recall, Retrieval Ranking.
- **Tier 2 (2개):** Question/Context/Answer 관계 평가. Context Relevance, Answer Faithfulness.
- **Tier 3 (1개):** 사용자 만족도. End-to-end User Satisfaction.

이 6가지를 *서로 다른 도구로* 측정합니다. Tier 1은 기존 IR 도구로 측정 가능. Tier 2는 *LLM-as-judge*가 필요. Tier 3는 *실제 사용자 데이터*가 필요.

Eval Engineer가 *어떤 tier를 누가 책임지는지*를 명시적으로 정의하는 게 일의 한 부분입니다. 그리고 *각 tier 측정 방법의 신뢰도*를 또 평가하는 게 한 부분입니다. 메타 평가가 매번 동반됩니다.

---

## 90일 안에 시도해 볼 수 있는 것

한국 QA·플랫폼·데이터 엔지니어가 Eval Engineer로 옮겨가려고 할 때, 90일 동안 해 볼 만한 행동입니다.

**1. 공개 벤치마크의 한계 분석 글.** MMLU, HellaSwag, HumanEval 중 한 가지를 골라서, *어떤 한계*가 있는지 분석한 글을 씁니다. Deng 외 *데이터 오염* 논문을 인용. 자기 도메인에서 *이 벤치마크가 잡지 못하는 것*을 구체 사례로 제시. 한 편의 글이 60일 안에 가능합니다.

**2. 자기 도메인 eval 셋 공개.** 자기 도메인에서 *100개 사례의 eval 셋*을 만들어 GitHub에 공개. 각 사례마다 *기대 답*, *측정 기준*, *왜 이 사례가 중요한지*를 적습니다. 90일 안에 *공개된 eval 셋 한 개*가 자산이 됩니다.

**3. LLM-as-judge 실험 보고서.** Zheng 외 *LLM-as-Judge* 논문에서 짚은 4가지 편향을, 자기 도메인에서 *실제로 재현*해 보는 실험을 합니다. position bias, verbosity bias, self-enhancement bias, 제한된 추론. 어떤 편향이 어떤 사례에서 발생하는지를 보고서로 정리. 30~45일 안에 가능합니다.

**4. Husain & Shankar의 AI Evals 코스 수강.** Maven 플랫폼에서 진행되는 *AI Evals* 코스를 수강합니다. 약 4주 과정. 글로벌 표준 커리큘럼이라, 졸업증이 *진지한 후보임을 보여 주는 신호*가 됩니다. 한국에서는 이 자격이 *희소한 차별점*이 됩니다.

**5. 한국 도메인 한국어 eval 시도.** 한국어 도메인에서 *영어 벤치마크와 비교 가능한* eval 셋을 만들어 보는 시도. 예를 들어 *한국어 법률 질문 100개에 대한 fact-check eval*. 한국 회사 면접에서 *바로 도움이 되는 자산*이 됩니다.

다섯 가지 중 *세 가지*를 끝낸 사람이라면, 한국 빅컴퍼니의 *AI Research Engineer (Evaluation)* 자리에 진지하게 검토되는 후보가 됩니다. 동시에 *글로벌 회사 원격*도 가능한 자산이 됩니다.

---

## 측정의 표준을 다시 짜는 사람

본론 5개 직업의 마지막 자리입니다. *측정의 표준*을 만드는 사람.

이 자리가 다른 4개와 다른 점이 한 가지 있습니다. *Eval Engineer는 본론의 다른 모든 직업과 짝을 이룹니다*. AI PM은 *eval로 PRD를 대체*하고, FDE는 *고객 현장에서 evals를 만들고*, Applied AI는 *eval로 회귀를 잡고*, AgentOps는 *eval 결과로 알람을 짭니다*. 다섯 자리가 *측정의 기준* 위에서 함께 돌아갑니다.

그래서 Eval Engineer는 *조용한 핵심*입니다. 화려한 자리는 아닙니다. 그러나 *이 자리 없이는 다른 직업들이 작동하지 않습니다*.

한국에서 가장 늦게 들어올 자리이고, 가장 적은 자료가 있는 자리지만, *그래서* 지금 들어가는 사람에게 가장 큰 자리가 될 수 있습니다.

---

## 본론 5개 직업을 한 번 더 정렬해 봅니다

5개 직업의 비교를 도입부에서 한 번 했고, 본론에서 한 챕터씩 들여다봤습니다. 막간으로 넘어가기 전, 한 표로 다시 정리하겠습니다.

| 직업 | 시그니처 인용 | 한국 도착 | 가장 가까운 현직 |
|---|---|---|---|
| **7장 AI PM** | "Evals replace PRDs" — Husain | 도구화 단계 ★★★ | PM/기획자 |
| **8장 FDE** | "+1,165% YoY" — Bloomberry | 재편 중 ★★★★ | SI 컨설턴트, 솔루션 아키텍트 |
| **9장 Applied AI Engineer** | "5년 → 한 오후" — Swyx | 성숙 ★★★★★ | 백엔드, 풀스택 |
| **10장 Agent 운영자** | "환각은 시스템 설계 문제" — Galileo | 운영팀 형태 ★★ | SRE, 플랫폼, 시니어 백엔드 |
| **11장 Eval Engineer** | "Error analysis is not optional" — Husain | 가장 늦음 ★ | QA, 플랫폼, 데이터 엔지니어 |

이 다섯 자리가 본론 도감이었습니다. 다섯 자리 모두 *Jagged Frontier 매핑*이라는 공통 능력 위에 서 있고, *KPI가 결과 단위로 옮겨가는 시대*의 짝을 이루는 자리들입니다.

본론을 닫기 전에, 책의 가설이 *틀릴 수 있는 9가지*를 한 자리에 모아 직시하는 짧은 막간으로 들어가겠습니다. 다음 페이지가 그 막간입니다.
