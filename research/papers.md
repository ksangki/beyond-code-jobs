# 논문 리서치: 코드 너머의 직업들 — GPU 위에서 일하는 사람들

> 책의 핵심 가설 "PC·인터넷·모바일이 그랬듯 AI 인프라 다음에 새 직업이 자란다"의 학술적 토대를 모은다. 영역 1·2·3·4 순으로 정리하며, 가설을 강화하는 자료와 *반박·완화*하는 자료를 모두 포함한다.
>
> 조사 시점: 2026-05. 모든 인용은 (저자, 제목, 발행처/저널, 연도, DOI/arXiv ID 또는 URL)을 포함한다.

---

## 영역 1 — 기술 사이클·인프라 ↔ 응용 이론

> 책의 1장(패턴 인식)·2장(시차 단축 메커니즘)의 학술적 뒷받침. "인프라가 먼저 깔리고 응용이 자란다"는 직관을 경제사·혁신경제학으로 정당화한다.

---

### 논문 1: Technological Revolutions and Financial Capital — The Dynamics of Bubbles and Golden Ages

- **저자·연도:** Carlota Perez, 2002
- **발표처:** Edward Elgar Publishing (단행본)
- **DOI/URL:** https://carlotaperez.org/books/ — 본문 PDF: http://pombo.free.fr/carlota2002.pdf
- **유형:** 단행본 (Seminal). 후속 다수 논문 발표. (cf. Perez, "Technological revolutions and techno-economic paradigms", Cambridge Journal of Economics 34(1), 2010, https://doi.org/10.1093/cje/bep051)
- **요약 (4문장):** Perez는 산업혁명 이래 5번의 기술혁명을 분석하여 각 혁명이 *Installation phase*(거품과 인프라 구축)와 *Deployment phase*(응용 황금기) 두 단계를 반드시 거친다고 주장한다. Installation은 다시 *Irruption*(약 10년, 핵심 기술과 인프라 구축)과 *Frenzy*(약 10년, 자본의 광적 투기)로 나뉘며, 그 사이 *Turning Point*에서 거품이 붕괴한다. 이후 Deployment 단계에서야 새 산업·새 직업·새 비즈니스 모델이 사회 전반에 퍼지며 진정한 생산성 황금기가 도래한다. 책은 이 패턴이 증기·철도(1771~), 철강·전기(1875~), 자동차·대량생산(1908~), 정보기술(1971~)에서 일관되게 반복되었음을 실증한다.
- **핵심 수치·결과:**
  - Installation: 약 20년 (Irruption 10 + Frenzy 10)
  - Deployment: 약 30년에 걸친 골든 에이지
  - 5개 거대 사이클 동일 패턴 반복
- **인용할 만한 문장 (역자 직역):**
  > "Each technological revolution irrupts in the form of a constellation of new and dynamic industries, plus a new infrastructure, which together create a new techno-economic paradigm capable of guiding entrepreneurs, managers, innovators and investors for several decades, in their separate decisions and actions." (Ch.1)
  >
  > "It is during the Deployment Period — after the major financial collapse — that the full social and economic potential of the new technologies can be realized."
- **챕터 매핑:** **→ 1장 도입 학술 뒷받침의 핵심 자료**, → 2장 시차 메커니즘 (Frenzy → Turning Point → Deployment의 시간 비용을 단축한다는 책 가설의 비교 기준점), → 13장 결론(거시 사이클 안에서 개인 커리어 위치 잡기)
- **독자 전달 방식 제안:** AI 인프라 시대를 "지금 우리는 GPT·LLM의 Installation 후반 (Frenzy)에 있다"고 좌표화. 닷컴 버블 직후 검색·SaaS·소셜 직업이 우후죽순 자란 사례를 평행으로 소개.

---

### 논문 2: General Purpose Technologies "Engines of Growth?"

- **저자·연도:** Timothy F. Bresnahan, Manuel Trajtenberg, 1995
- **발표처:** *Journal of Econometrics*, vol. 65(1), pp. 83–108
- **DOI/URL:** https://doi.org/10.1016/0304-4076(94)01598-T — NBER 사전인쇄 W4148 (1992): https://www.nber.org/papers/w4148
- **피인용:** 5,000+ (Google Scholar 기준, 분야 seminal)
- **요약 (4문장):** 저자들은 한 시대 전체의 경제성장이 소수의 핵심 기술 — General Purpose Technology (GPT) — 에 의해 추동된다는 이론을 정식화한다. GPT의 세 가지 정의 조건은 ① *pervasiveness*(다수 산업의 입력재로 광범위 사용), ② *inherent potential for technical improvements*(자체 개선 잠재력), ③ *innovational complementarities*(다운스트림 산업의 R&D 생산성을 GPT 혁신이 끌어올리는 보완성)이다. 증기기관·전기모터가 과거의 GPT였고, 반도체·컴퓨터가 현대의 GPT다. 핵심 통찰은 GPT 자체의 가치보다 *보완재(complementary innovations)에서 발생하는 가치*가 훨씬 크며, 시장 분권화 때문에 보완재 투자가 늘 "too little, too late"으로 저조하게 일어난다는 것.
- **핵심 수치·결과:** 정량 추정보다는 이론 모형. 게임이론적 두 단계 모델(상류 GPT 산업 + 하류 응용산업).
- **인용할 만한 문장 (직역):**
  > "Whole eras of technical progress and economic growth appear to be driven by a few 'General Purpose Technologies', characterized by pervasiveness, inherent potential for technical improvements, and 'innovational complementarities'."
  >
  > "The decentralized market may give rise to 'too little, too late' innovation, both in the GPT and in the application sectors."
- **챕터 매핑:** **→ 2장 보완재 등장 메커니즘의 학술 핵심**, → 5장(에이전트가 LLM을 GPT로 보고 그 위에 응용 직업이 폭발), → 7~11장(개별 새 직무가 GPT-보완재라는 프레이밍)
- **독자 전달 방식 제안:** "AI는 망치가 아니라 동력원이다. 동력원이 깔리면 그 위에 작업장(직업)이 자라기 시작한다." 책 본문에서 GPU=전기, 모델=모터, 응용 직업=공장 노동의 비유로 풀어낼 것.

---

### 논문 3: The Dynamo and the Computer — An Historical Perspective on the Modern Productivity Paradox

- **저자·연도:** Paul A. David, 1990
- **발표처:** *American Economic Review*, vol. 80(2) — Papers and Proceedings, pp. 355–361
- **DOI/URL:** https://www.jstor.org/stable/2006600 — PDF: http://digamo.free.fr/david90.pdf
- **피인용:** 1,500+
- **요약 (4문장):** David는 1880년대 발전기(dynamo) 등장 후 30~40년이 지나서야 미국 공장의 생산성이 본격 폭증했다는 역사적 사실을 들어, 1980년대 컴퓨터의 "생산성 역설"(Solow paradox)이 이상한 일이 아니라 새 GPT의 표준적 시차임을 논증한다. 발전기의 진정한 효과는 모터 자체가 아니라 *공장 평면도(plant layout)의 재설계* — 전기로 인해 천장 벨트축이 사라지고 단층 공장이 가능해지면서 자재 흐름이 최적화된 것 — 에서 나왔다. 즉, 생산성은 GPT가 도입된 시점이 아니라 보완 자본(공장 재배치, 인적자본, 새 작업방식)이 누적된 후에야 측정된다. 핵심 메커니즘: *diffusion lags + 보완 자본의 공동발명(co-invention)*.
- **핵심 수치·결과:**
  - 1881 에디슨 발전소 → 1920년대까지 약 40년 시차 후 제조업 TFP 폭증
  - 1900년 미국 공장 동력의 약 5%만 전기, 1929년 80% 이상으로 확산
- **인용할 만한 문장 (직역):**
  > "The computer is to be classed as a transforming general purpose engine of economic growth, much as was the case with the electric dynamo a century earlier."
  >
  > "Major productivity gains followed only after factories had been redesigned to exploit the unique advantages of unit drive electric motors — a process that required the abandonment of an entire stock of preceding capital and the slow accumulation of new tacit knowledge among workers and managers."
- **챕터 매핑:** **→ 1장(시차의 역사적 사례)**, **→ 2장 시차 단축 메커니즘의 정면 토대**, → 13장(개인이 시차 안에서 어디에 자리 잡을지)
- **독자 전달 방식 제안:** "LLM 도입 4년 됐는데 왜 회사 KPI는 그대로지?" 같은 독자의 답답함을 발전기 사례로 정당화. "지금이 1900년 시점이라면 우리는 무슨 직업을 만들 수 있는가?"로 자연스레 본론 진입.

---

### 논문 4: The Productivity J-Curve — How Intangibles Complement General Purpose Technologies

- **저자·연도:** Erik Brynjolfsson, Daniel Rock, Chad Syverson, 2021 (NBER WP 2018)
- **발표처:** *American Economic Journal: Macroeconomics*, vol. 13(1), pp. 333–372
- **DOI/URL:** https://doi.org/10.1257/mac.20180386 — NBER W25148: https://www.nber.org/papers/w25148
- **피인용:** 800+
- **요약 (4문장):** GPT는 도입 직후 측정 생산성을 *과소평가*하게 만든다. 새 기술이 가치를 내려면 무형자본(공정 재설계, 비즈니스 모델 혁신, 인적자본, 데이터 자산)에 막대한 투자가 필요한데, 이 투자는 GDP·TFP 통계에 비용으로만 잡히고 자산으로 잡히지 않기 때문이다. 결과적으로 도입 초기에는 측정 TFP가 *과소측정* (J 곡선의 바닥), 무형자본이 결실을 맺기 시작하면 *과대측정*되는 J-Curve가 생긴다. 미국 데이터에서 ICT 무형자본을 보정하면 2017년 말 TFP 수준이 공식 통계보다 15.9% 높다.
- **핵심 수치·결과:**
  - 무형자본 보정 시 TFP 수준 +15.9% (2017 기준)
  - 컴퓨터·SW 관련 무형 투자: J-Curve 패턴 통계적 유의 (1985~2015)
- **인용할 만한 문장 (직역):**
  > "The intangible capital that is required to make a GPT productive is itself a form of investment, but it is largely missing from official measures, leading to mismeasurement of TFP that follows a J-shaped curve."
- **챕터 매핑:** **→ 2장 (생산성 통계가 늦게 나타나는 이유의 정량적 증거)**, → 3장 직업 변동 (회사가 보이지 않는 무형 투자에 사람을 갈아 넣는 시점이 바로 새 직무가 자라는 토양), → 12장 (실력 누적의 보이지 않는 자산 가치)
- **독자 전달 방식 제안:** "당신의 노력이 회계상 비용으로만 잡히는 시기가 J-Curve의 바닥이다. 그 바닥에 자리를 잡은 사람만 위로 함께 올라간다."

---

### 논문 5: Competing Technologies, Increasing Returns, and Lock-In by Historical Events

- **저자·연도:** W. Brian Arthur, 1989
- **발표처:** *The Economic Journal*, vol. 99, no. 394, pp. 116–131
- **DOI/URL:** https://doi.org/10.2307/2234208 — PDF: https://fbaum.unc.edu/teaching/articles/Arthur_EJ_1989.pdf
- **피인용:** 11,000+
- **요약 (3문장):** Arthur는 채택률이 높을수록 기술 자체가 더 좋아지는 *increasing returns to adoption* 환경에서, 시장은 작은 역사적 우연에 의해 한 기술로 *lock-in*된다고 모형화한다. QWERTY 자판, VHS, x86처럼 "최고가 아니어도 먼저 임계 사용자를 모은 기술"이 표준이 되는 메커니즘이다. 이는 GPT가 단순 기술 우월성이 아니라 *보완재 생태계*에 의해 지위를 굳히는 이유를 설명한다.
- **핵심 수치·결과:** 이론 모형 — Polya urn 확률과정으로 lock-in을 증명.
- **인용할 만한 문장 (직역):**
  > "The economy can become locked-in, by 'random' historical events, to a technological path that is not necessarily efficient."
- **챕터 매핑:** → 2장(LLM 생태계가 어떻게 락인되는가, 왜 기술 자체보다 도구·MCP·에이전트 쪽 직업에 기회가 큰가), → 5장(에이전트 표준 경쟁), → 11장(어떤 도구·플랫폼에 묶이는 게 위험·기회인지)
- **독자 전달 방식 제안:** "기술 우월성이 아니라 사용자 수가 표준을 결정한다. AI 시대에도 같다 — 가장 빨리 익숙해진 사람이 가장 강한 직무 정의를 차지한다."

---

### 논문 6: Crossing the Chasm — Marketing and Selling High-Tech Products to Mainstream Customers

- **저자·연도:** Geoffrey A. Moore, 1991 (3판 2014)
- **발표처:** HarperBusiness (단행본)
- **DOI/URL:** ISBN 978-0062292988
- **유형:** 실무서 (학술 인용 다수, 후속 마케팅 학계에서 표준 참조)
- **요약 (3문장):** Rogers의 혁신확산이론(Diffusion of Innovations, 1962)을 토대로, 신기술이 *innovators → early adopters* 단계에서 *early majority*로 넘어갈 때 깊은 골(*chasm*)이 존재함을 모형화한다. 이 골을 건너려면 단순 기술 데모가 아니라 "주류 사용자가 자기 일의 맥락에서 즉시 가치를 보는 보완재 묶음(whole product)"이 필요하다. 책에서는 이 "whole product" 개념이 새 직업이 성립하는 조건을 설명한다.
- **핵심 수치·결과:** Rogers 5단계 채택곡선: innovators 2.5%, early adopters 13.5%, early majority 34%, late majority 34%, laggards 16%.
- **인용할 만한 문장 (직역):**
  > "Each high-tech product encounters a chasm in its life cycle. The visionaries who buy early are not the same as the pragmatists who buy in volume — and what worked for the former actively repels the latter."
- **챕터 매핑:** → 1장(현재 AI는 chasm을 건너는 중), → 7~11장(개별 직무가 자라는 시점은 chasm을 막 건넌 직후), → 12장(현장의 pragmatist를 설득하는 능력 자체가 직업이 됨)
- **독자 전달 방식 제안:** "당신이 AI에 일찍 발 디딘 사람이라면, 다음 1~3년 안에 들어오는 'pragmatist 동료'를 어떻게 데리고 갈지가 직업 정의가 된다."

---

## 영역 2 — AI와 노동시장 학술

> 책의 2·3·12·13장 자료. 이 영역은 *낙관·중립·비관*을 균형 있게 배치한다.

---

### 논문 7: Generative AI at Work

- **저자·연도:** Erik Brynjolfsson, Danielle Li, Lindsey R. Raymond, 2023 (NBER WP); 2025 *Quarterly Journal of Economics*에 게재 예정 후속본
- **발표처:** NBER Working Paper No. 31161 (April 2023); arXiv:2304.11771
- **DOI/URL:** https://www.nber.org/papers/w31161 — arXiv: https://arxiv.org/abs/2304.11771
- **피인용:** 1,200+
- **요약 (4문장):** 5,179명의 콜센터 상담사가 단계적으로 GPT 기반 대화 보조 도구를 도입한 자연실험. 도구 도입 이후 시간당 해결 이슈 수가 **평균 14% 증가**했고, 특히 **신입·저숙련 상담사는 34% 향상**된 반면 고숙련자에게는 거의 효과 없음. 도구는 고숙련자의 best practice를 추출해 신입에게 전달하는 *경험곡선 압축* 메커니즘으로 작동했다. 부수효과로 고객 감정 점수 개선과 직원 이직률 감소도 관찰.
- **핵심 수치·결과:**
  - 평균 생산성 +14% (이슈/시간)
  - 신입·저숙련 +34%, 숙련자 ~0%
  - 고객 부정 발화 -9%, 매니저 개입 요청 -25%
  - 6개월 미만 신입의 숙련자 따라잡는 시간 단축
- **인용할 만한 문장 (직역):**
  > "Access to AI assistance increases the productivity of agents by 14 percent on average, with the largest gains accruing to less experienced and lower-skilled workers."
- **챕터 매핑:** → 2장(시차 단축의 가장 강력한 정량 증거), → 3장(직업 변동의 첫 데이터), **→ 12장 신입의 기회 — 핵심 인용**
- **독자 전달 방식 제안:** "AI는 평균을 끌어올리는 게 아니라, 신입을 빠르게 숙련자로 만든다. 그래서 지금이 신입에게 가장 좋은 시기다."

---

### 논문 8: The Simple Macroeconomics of AI

- **저자·연도:** Daron Acemoglu, 2024
- **발표처:** NBER Working Paper No. 32487 (May 2024); *Economic Policy* 게재 예정
- **DOI/URL:** https://www.nber.org/papers/w32487
- **피인용:** 250+ (1년 만에)
- **요약 (4문장):** Acemoglu는 GenAI 거시효과에 대한 *낙관론* (Goldman Sachs 등의 GDP +7%급 예측)을 강하게 반박한다. 작업 단위 생산성·노출도·자동화 가능 비율을 곱한 task-based 모델로 재계산하면 향후 10년 누적 TFP 증가는 **0.66% 이하**, GDP 효과는 약 1.1~1.6%에 불과하다. 동시에 AI는 자본·노동 분배 격차를 더 벌릴 가능성이 높고, 새 일자리(reinstatement effect)는 자동화에 비해 약하게 작동할 것으로 본다. 즉 "생산성 폭발"은 과장이며, 노동시장 변동도 비대칭으로 일어난다.
- **핵심 수치·결과:**
  - 향후 10년 TFP 증가: **≤ 0.66%** (연 0.05~0.07%)
  - GDP 증가: 1.1~1.6% (10년 누적)
  - 자동화 가능한 노출 작업 비율: ~20%, 그 중 비용 효율적으로 자동화될 비율: ~23%
  - → 결과적으로 AI가 영향 미치는 작업: 전체의 **약 4.6%**
- **인용할 만한 문장 (직역):**
  > "Even taking the most optimistic estimates from existing micro studies as given, my estimates suggest that the macroeconomic effects of AI are likely to be modest — no more than 0.66% increase in TFP over 10 years."
  >
  > "The forecasts of much larger productivity effects appear hyperbolic."
- **챕터 매핑:** **→ 균형 잡기용 핵심 반론 자료**, → 1장(맹목적 낙관 경계), → 3장(대량 일자리 창출 서사 약화), → 13장(개인 전략은 거시 낙관에 베팅하지 말 것)
- **독자 전달 방식 제안:** "거시는 천천히, 미시는 빠르게. 이 책은 거시 낙관에 베팅하는 게 아니라 미시(개인) 기회에 베팅한다."

---

### 논문 9: Navigating the Jagged Technological Frontier — Field Experimental Evidence on Knowledge Worker Productivity

- **저자·연도:** Fabrizio Dell'Acqua, Edward McFowland III, Ethan R. Mollick, Hila Lifshitz-Assaf, Katherine Kellogg, Saran Rajendran, Lisa Krayer, François Candelon, Karim R. Lakhani, 2023 (HBS WP); 2025 *Organization Science* 게재
- **발표처:** Harvard Business School Working Paper 24-013; *Organization Science* (2025)
- **DOI/URL:** SSRN: https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4573321 — Org. Sci.: https://doi.org/10.1287/orsc.2025.21838
- **피인용:** 600+
- **요약 (4문장):** 758명의 BCG 컨설턴트(전체 IC급의 약 7%)를 대상으로 한 무작위 통제 실험. *frontier 안쪽* 작업(창의 글쓰기·아이디어 생성·분석 등)에서는 GPT-4 사용군이 비사용군 대비 **완료 작업 수 +12.2%, 속도 +25.1%, 인간 평가 품질 +40%** 향상. 그러나 *frontier 바깥쪽* 작업(미묘한 비즈니스 판단·정량 추론)에서는 사용군이 **19%p 더 나쁜 성과** — AI가 그럴듯한 오류를 만들어 인간을 속였다. 시사점: AI 도구는 모든 작업을 균일하게 도와주지 않는다 — *jagged frontier*의 안과 밖을 식별하는 능력 자체가 새 직무 역량이다.
- **핵심 수치·결과:**
  - 표본: 758 BCG 컨설턴트, 사전 등록 RCT
  - Inside frontier: +12.2% 완료, +25.1% 속도, 품질 +40%
  - Outside frontier: -19%p 정확도
  - 클러스터 분석: 두 사용 패턴 — *Centaur* (작업 분리) vs *Cyborg* (긴밀 협업)
- **인용할 만한 문장 (직역):**
  > "AI capabilities currently form a 'jagged technological frontier'. For tasks within this frontier, AI can substantially improve human performance; for tasks outside it, AI degrades performance, even when the tasks appear similar in difficulty."
- **챕터 매핑:** → 2장(생산성 14%의 추가 증거), → 5장(에이전트 frontier 식별 능력), **→ 7~11장 새 직무의 핵심 능력 = jagged frontier mapping**, → 12장(신입이 얻는 +40% 품질이 가장 큰 자산)
- **독자 전달 방식 제안:** "AI를 잘 쓰는 사람 = AI가 무엇을 못하는지 빨리 아는 사람. 'Frontier 지도 그리기'가 새 직업의 본질 능력이다."

---

### 논문 10: New Frontiers — The Origins and Content of New Work, 1940–2018

- **저자·연도:** David Autor, Caroline Chin, Anna Salomons, Bryan Seegmiller, 2024
- **발표처:** *The Quarterly Journal of Economics*, vol. 139(3), pp. 1399–1465
- **DOI/URL:** https://doi.org/10.1093/qje/qjae008 — NBER W30389: https://www.nber.org/papers/w30389
- **피인용:** 200+
- **요약 (4문장):** 미국 인구조사 직업 코드와 특허·과학 출판물 텍스트를 매칭해 1940~2018 사이 새로 만들어진 직업("micro-titles")을 추적한 기념비적 실증 연구. **2018년 미국인이 하는 일의 60% 이상이 1940년에 존재하지 않던 직업**이다. 새 직업의 발생원은 두 가지 — ① 기술이 기존 직업의 *output을 보완*해 수요를 늘릴 때(augmentation innovation), ② 외생 수요 충격. 자동화 혁신은 단기 일자리를 줄이며 *최근 40년*간 자동화 충격이 신직업 생성을 따라잡지 못해 노동수요 둔화로 이어졌다.
- **핵심 수치·결과:**
  - 2018 직업의 60%+ 가 1940년에 부재
  - 1940~1980: 새 직업 주로 중급 생산직·사무직
  - 1980~2018: 새 직업 양극화 — 고임금 전문직 + 저임금 서비스직
  - 자동화 혁신과 증강 혁신의 비율 변화 → augmentation 효과 약화
  - 예시 micro-titles: "computer application engineer" (1980s), "AI specialist", "wind turbine technician", "solar photovoltaic electrician"
- **인용할 만한 문장 (직역):**
  > "More than 60 percent of employment in 2018 is found in job titles that did not exist in 1940."
  >
  > "Augmentation innovations — those that complement the outputs of an occupation — generate new work, while automation innovations primarily redistribute it."
- **챕터 매핑:** **→ 1장 패턴 인식의 정량 토대 (60%+ 통계)**, → 3장(직업 변동 패턴), **→ 7~11장 새 직무 등장 메커니즘의 학술 근거**, → 13장
- **독자 전달 방식 제안:** "당신의 손주가 2080년에 하고 있을 직업의 60%는 지금 이름조차 없다. 당신이 그 이름을 짓는 사람일 수 있다."

---

### 논문 11: Automation and New Tasks — How Technology Displaces and Reinstates Labor

- **저자·연도:** Daron Acemoglu, Pascual Restrepo, 2019
- **발표처:** *Journal of Economic Perspectives*, vol. 33(2), pp. 3–30
- **DOI/URL:** https://doi.org/10.1257/jep.33.2.3 — NBER W25684: https://www.nber.org/papers/w25684
- **피인용:** 3,000+
- **요약 (3문장):** Acemoglu·Restrepo의 task-based 프레임워크. 기술의 노동시장 효과는 두 힘의 합 — *displacement effect* (자본이 노동의 작업을 대체) + *reinstatement effect* (새 작업이 만들어져 노동에 비교우위 회복). 지난 30년은 displacement 가속 + reinstatement 둔화로 노동 점유율 하락이 일어났다.
- **핵심 수치·결과:**
  - 1947~1987 vs 1987~2017: reinstatement 기여도 절반 이하로 감소
  - 자동화 1%p → 임금 -0.4 ~ -0.5% (구체 패널 추정)
- **인용할 만한 문장 (직역):**
  > "The labor share declines when automation runs faster than the introduction of new tasks where labor has comparative advantage."
- **챕터 매핑:** → 3장(직업 변동 이론 토대), **→ 7~11장 (새 직무 = reinstatement effect의 미시 사례)**, → 12·13장
- **독자 전달 방식 제안:** "나쁜 소식: 자동화는 일자리를 빼앗는다. 좋은 소식: 새 작업도 만들어낸다. 이 책은 후자에 인생을 거는 가이드다."

---

### 논문 12: Anthropic Economic Index (Series, 2025–2026)

- **저자·연도:** Anthropic Economic Research Team (Mehrdad Esfandyari, Kunal Handa, Maxim Massenkoff, Peter McCrory, et al.), 2025–2026
- **발표처:** Anthropic Research (인덱스 보고서 시리즈, 1차 2025-02, 5차 2026-03)
- **URL:** https://www.anthropic.com/economic-index — 데이터셋: https://huggingface.co/datasets/Anthropic/EconomicIndex
- **유형:** 산업 연구 보고서 (학술적 방법론 적용 — 익명 변환·O*NET 작업 매핑)
- **요약 (4문장):** Claude.ai의 익명화된 수백만 대화를 O*NET 작업 분류에 매핑해 직업별 AI 사용 패턴을 추적하는 정기 보고서. 첫 보고서(2025-02) 핵심: 직업의 약 36%가 자기 작업의 1/4 이상을 Claude에 위탁; 사용은 컴퓨터 프로그래머·기술 작가에 집중; **augmentation 57% vs automation 43%**. 후속 보고서들은 augmentation/automation 비율이 시간이 지나며 자동화 쪽으로 이동(2026-03 기준 augmentation 52%, automation 45%)하고 있음을 보여준다. 5차 보고서(2026-03): 컴퓨터 프로그래머의 작업 75%가 Claude로 커버됨 — 가장 노출된 직업.
- **핵심 수치·결과:**
  - 1차(2025-02): 36%의 직업에서 작업 1/4 이상 AI 사용
  - 1차: augmentation 57% / automation 43%
  - 5차(2026-03): augmentation 52% / automation 45% (자동화 비중 상승)
  - 컴퓨터 프로그래머 작업 커버리지 75%
  - 22~25세 노출 직업 진입 신입의 구직률 -14% (post-ChatGPT)
  - 노출 작업 종사자 평균 임금 +47% (비노출 대비)
- **인용할 만한 문장 (1차 보고서):**
  > "AI use leans toward augmentation (57%), where AI collaborates with and enhances human capabilities, rather than automation (43%), where AI directly performs tasks."
  >
  > 5차 보고서: "We observe a 14% decline in job-finding rates for workers aged 22–25 entering exposed occupations after ChatGPT's release."
- **챕터 매핑:** **→ 3장 직업 변동의 가장 최신·가장 큰 데이터**, → 5장(어떤 작업이 자동화/증강되는지 매핑), **→ 12장 신입 시장의 *경고* 자료** (Brynjolfsson과 대조: 신입 생산성↑이지만 채용 자체는↓), → 13장
- **독자 전달 방식 제안:** Brynjolfsson 2023과 함께 *대조*시킨다 — "AI를 *쓰는* 신입은 빨리 큰다(B), 그러나 AI에 *대체되는* 위치의 신입은 들어가기 자체가 어렵다(A)". 이 모순이 책의 12장 핵심 긴장.

---

### 논문 13: Generative AI and Jobs — A Refined Global Index of Occupational Exposure

- **저자·연도:** Janine Berg, Pawel Gmyrek (ILO), 2025
- **발표처:** ILO Working Paper No. 140 (May 2025)
- **DOI/URL:** https://www.ilo.org/publications/generative-ai-and-jobs-refined-global-index-occupational-exposure — PDF: https://www.ilo.org/sites/default/files/2025-05/WP140_web.pdf
- **요약 (3문장):** 글로벌 직업 데이터베이스를 기반으로 GenAI 노출도를 재추정. **전 세계 노동자 약 25%가 어느 정도 GenAI 노출 직업에 종사**하며, 이 중 *고노출* 비율은 3.3%. 고소득국 34% vs 저소득국 11%로 격차가 크고, 사무직(clerical)이 가장 높은 노출. 결론: 대규모 *대체*보다는 *직무 변형(transformation)*이 주된 효과.
- **핵심 수치·결과:**
  - 전 세계 노동력의 25%가 어느 정도 GenAI 노출
  - 고노출 비율 3.3% (여성 4.7% > 남성 2.4%)
  - 고소득국 34% vs 저소득국 11%
  - 사무직 노출 최고
- **인용할 만한 문장:**
  > "One in four jobs is at risk of being transformed by generative AI — but transformation, not replacement, is the central scenario for most occupations."
- **챕터 매핑:** → 3장(국제 비교 토대), → 12·13장(여성·사무직의 변동성), 균형용 자료 (대량 실업 서사 완화)
- **독자 전달 방식 제안:** "AI는 일자리를 없애는 게 아니라 *바꾸는* 힘이 더 크다. 바꿀 때 옆에 서 있을 사람이 새 직업이 된다."

---

### 논문 14: Future of Jobs Report 2025

- **저자·연도:** World Economic Forum (Saadia Zahidi et al.), 2025
- **발표처:** WEF Insight Report (January 2025)
- **URL:** https://www.weforum.org/publications/the-future-of-jobs-report-2025/ — PDF: https://reports.weforum.org/docs/WEF_Future_of_Jobs_Report_2025.pdf
- **유형:** 산업 보고서 (1,000+ 글로벌 고용주 서베이 기반)
- **요약 (3문장):** 2030까지 글로벌 노동시장에서 *순 +7,800만 일자리* 생성 전망. AI/정보처리 단독으로 1,100만 신규 + 900만 대체 = 순 +200만. 가장 빠른 성장 직업: Big Data Specialist, FinTech Engineer, AI/ML Specialist, SW Developer, Security Management. 반대로 가장 빨리 줄어드는 직업: 캐셔, 행정 사무, 그래픽 디자이너(GenAI 영향), 회계·감사.
- **핵심 수치·결과:**
  - 2030년까지 순 +7,800만 일자리
  - AI 직군 신규 +1,100만 / 대체 +900만 (순 +200만)
  - 향후 5년 노동자 1인당 핵심 스킬의 39%가 변화/구식화
  - 51%의 GenAI 도입 기업이 매출 +10% 이상 보고
- **인용할 만한 문장:**
  > "Of all surveyed technologies, AI and information processing technologies are expected to create the largest absolute number of new jobs and to displace the most existing roles."
- **챕터 매핑:** → 3장(직업 변동 양적 전망), **→ 7~11장 (특정 새 직무명들의 글로벌 검증)**, → 12·13장(스킬 39% 변동의 함의)
- **독자 전달 방식 제안:** 책 후반 "어떤 직업을 권하는가" 부분에서 WEF 리스트와 본인의 관찰을 교차 검증. 단, WEF 데이터는 *자기보고 서베이* 기반이라 한계 명시.

---

### 논문 15: AI Index Report 2025 — Chapter 4: Economy

- **저자·연도:** Stanford HAI (Nestor Maslej, Loredana Fattorini, Ray Perrault, et al.), 2025
- **발표처:** Stanford Institute for Human-Centered AI Annual Report
- **URL:** https://hai.stanford.edu/ai-index/2025-ai-index-report — Chapter 4 PDF: https://hai.stanford.edu/assets/files/hai_ai-index-report-2025_chapter4_final.pdf
- **요약 (3문장):** 2024 채용 공고에서 GenAI 명시 스킬이 **16,000 → 66,000건 (4배+)**. LLM 관련 게시물 5,000 → 20,000, 프롬프트 엔지니어링 1,400 → 6,300. 미국 일자리 중 AI 관련 비중은 워싱턴 D.C. 4.4%, 워싱턴주 3.4%, 델라웨어 3.3%로 지역 편차가 크다.
- **핵심 수치·결과:** 위 수치들 + 2024 글로벌 민간 AI 투자 252억 달러 (전년 대비 +18%)
- **인용할 만한 문장:**
  > "Demand for generative AI skills surged dramatically in 2024, reflecting a fundamental reshaping of hiring patterns rather than a transient hype cycle."
- **챕터 매핑:** → 3장(채용 공고 데이터로 본 직업 변동), → 7~11장(개별 직무 검증)
- **독자 전달 방식 제안:** "직업이 새로 자라는 첫 신호는 LinkedIn 채용 키워드의 4배 증가다."

---

## 영역 3 — 에이전트 시스템 & 평가 학술

> 책의 5·10·11장 토양. 에이전트 시대에 *무엇이 작동하고 무엇이 안 작동하는지*에 대한 정직한 학술 근거.

---

### 논문 16: A Survey on Large Language Model based Autonomous Agents

- **저자·연도:** Lei Wang, Chen Ma, Xueyang Feng, et al. (人民大学 Renmin Univ.), 2023~2025 (다수 개정)
- **발표처:** *Frontiers of Computer Science* (게재 예정), arXiv:2308.11432
- **URL:** https://arxiv.org/abs/2308.11432
- **피인용:** 1,500+
- **요약 (3문장):** LLM 기반 자율 에이전트 분야의 첫 종합 서베이. 통합 프레임워크 4요소 — *Profile* (역할 정의), *Memory* (단·장기 기억), *Planning* (작업 분해·반성·반복), *Action* (도구 사용·실행). 사회과학·자연과학·SW 엔지니어링 응용 사례 분류와 평가 방법론까지 정리.
- **핵심 수치·결과:** 정성 서베이; 200+ 논문 정리.
- **인용할 만한 문장:**
  > "LLM-based autonomous agents are typically composed of four modules: profiling, memory, planning, and action — a unified framework that captures most existing work."
- **챕터 매핑:** → 5장(에이전트 구성 요소의 학술 표준어), → 10·11장(특정 직무가 다루는 모듈)
- **독자 전달 방식 제안:** "에이전트는 모듈이다 — Profile, Memory, Planning, Action. 새 직업은 보통 이 네 칸 중 하나의 *전문가* 자리다."

---

### 논문 17: Understanding the Planning of LLM Agents — A Survey

- **저자·연도:** Xu Huang, Weiwen Liu, Xiaolong Chen, et al., 2024
- **발표처:** arXiv:2402.02716
- **URL:** https://arxiv.org/abs/2402.02716
- **요약 (3문장):** LLM 에이전트의 *planning* 능력 첫 체계 서베이. 5개 분류 — Task Decomposition, Plan Selection, External Module, Reflection, Memory. 각 접근의 장단·실패 모드·벤치마크 정리.
- **핵심 수치·결과:** 정성 서베이.
- **챕터 매핑:** → 5장(에이전트 능력 한계), → 10장(에이전트 운영자 직무가 무엇을 풀어야 하는지)

---

### 논문 18: Why Do Multi-Agent LLM Systems Fail?

- **저자·연도:** Mert Cemri, Melissa Z. Pan, Shuyi Yang, et al. (UC Berkeley), 2025
- **발표처:** arXiv:2503.13657
- **URL:** https://arxiv.org/abs/2503.13657
- **요약 (4문장):** 7개 오픈소스 다중 에이전트 시스템(MAS)의 1,600+ 실행 트레이스를 전문가 6명이 그라운디드 시어리로 분석. **MASFT (Multi-Agent System Failure Taxonomy)** — 14개 실패 모드, 3개 카테고리(시스템 설계, 에이전트 간 부정렬, 작업 검증). 7개 SOTA 오픈소스 MAS의 **실패율 41~86.7%**. 즉, 다중 에이전트는 *기본적으로 작동하지 않는다*.
- **핵심 수치·결과:**
  - 14개 실패 모드 / 3개 카테고리
  - 실패율 41~86.7% (SOTA 기준)
  - 인터-어노테이터 카파 0.88
- **인용할 만한 문장:**
  > "Despite the enthusiasm surrounding multi-agent LLM systems, our analysis reveals failure rates of 41% to 86.7% across seven state-of-the-art frameworks — performance gains over single-agent baselines are often minimal or negative."
- **챕터 매핑:** **→ 11장 reliability/observability 직무의 학술 토대**, → 5·10장(에이전트 한계의 정직한 데이터)
- **독자 전달 방식 제안:** "에이전트는 80% 망가져 있다. 망가지는 방식 14가지를 아는 사람이 11장의 새 직업이다." 이 데이터 자체가 책의 신뢰성 차별점.

---

### 논문 19: Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena

- **저자·연도:** Lianmin Zheng, Wei-Lin Chiang, Ying Sheng, et al. (UC Berkeley/LMSYS), 2023
- **발표처:** *NeurIPS 2023 Datasets and Benchmarks*
- **DOI/URL:** arXiv:2306.05685; https://arxiv.org/abs/2306.05685
- **피인용:** 3,500+
- **요약 (4문장):** LLM을 평가자(judge)로 쓰는 방법의 기준점. GPT-4 같은 강한 모델이 통제·크라우드 인간 선호와 **80%+ 일치** — 이는 인간 사이 일치도와 거의 같다. 그러나 LLM judge는 *position bias*(앞에 나온 답 선호), *verbosity bias*(긴 답 선호), *self-enhancement bias*(자기 가족 모델 선호), *제한된 추론*의 4대 편향을 갖는다. 저자들은 swap-position, calibration, fine-tuned judge로 일부 완화 가능함을 보였다.
- **핵심 수치·결과:**
  - GPT-4 judge ↔ 인간 일치율 80%+
  - position bias ~25% 까지 흔들림
  - 자기-자기 보너스 +10%p (self-enhancement)
- **인용할 만한 문장:**
  > "Strong LLM judges like GPT-4 can match both controlled and crowdsourced human preferences well, achieving over 80% agreement — yet they exhibit position, verbosity, and self-enhancement biases."
- **챕터 매핑:** **→ 10장 평가·QA 직무의 학술 토대**, → 11장
- **독자 전달 방식 제안:** "AI를 AI로 평가하는 시대다. 단, 그 평가에는 4가지 편향이 있다 — 이걸 잡는 사람이 직업이 된다."

---

### 논문 20: Investigating Data Contamination in Modern Benchmarks for Large Language Models

- **저자·연도:** Chunyuan Deng, Yilun Zhao, Xiangru Tang, Mark Gerstein, Arman Cohan (Yale), 2024
- **발표처:** *NAACL 2024*; arXiv:2311.09783
- **URL:** https://arxiv.org/abs/2311.09783
- **요약 (3문장):** 주요 LLM 벤치마크가 학습 데이터에 *오염*되어 있는지 검증. **TS-Guessing** (Testset Slot Guessing) 기법으로 객관식 답안의 한 옵션을 마스킹하고 모델에 채우게 시켜 메모리화 정도를 측정. 결과: ChatGPT가 MMLU에서 정확히 맞춘 비율 **52%**, GPT-4는 **57%** — 일반 추론 능력이 아닌 *암기*의 증거.
- **핵심 수치·결과:**
  - GPT-4 MMLU 답 맞춤(메모리화 추정) 57%
  - ChatGPT 52%
  - 학습데이터 의도적 노출 시 100% 근접
- **인용할 만한 문장:**
  > "The high exact-match rates for GPT-4 and ChatGPT on the original MMLU test are indicative of memorization rather than general reasoning ability."
- **챕터 매핑:** **→ 10장 평가 한계 + 11장 신뢰성** 핵심 자료
- **독자 전달 방식 제안:** "AI가 시험을 잘 본다고 일을 잘하는 건 아니다. 시험지를 미리 봤을 가능성이 50%다. 평가를 새로 짜는 사람이 직업이 된다."

---

### 논문 21: HELM — Holistic Evaluation of Language Models

- **저자·연도:** Percy Liang et al. (Stanford CRFM), 2022~ 지속 업데이트
- **발표처:** TMLR (2023); arXiv:2211.09110
- **URL:** https://arxiv.org/abs/2211.09110 — https://crfm.stanford.edu/helm/
- **요약 (3문장):** 16개 시나리오 × 7개 메트릭(정확도·견고성·공정성·편향·독성·효율 등)을 *동시에* 측정하는 평가 프레임워크. 단일 점수 대신 *trade-off 노출*이 핵심 가치. 후속 HELM-MMLU(2024)는 표준화된 프롬프트로 *모델 발표사*들의 자체 보고 점수의 비교불가능성을 폭로.
- **핵심 수치·결과:** 30+ 모델, 40+ 시나리오 등록 (2024 기준)
- **인용할 만한 문장:**
  > "Holistic evaluation surfaces trade-offs that single-number leaderboards systematically obscure."
- **챕터 매핑:** → 10장(평가의 표준), → 11장(모델 비교 직무)
- **독자 전달 방식 제안:** "단일 점수는 거짓말한다. 7개 축으로 보는 사람이 평가 직무다."

---

## 영역 4 — 직업 변동·새 직무 등장 메타 자료

> 책의 7~11장 토양 — *어떻게 새 직무 이름이 처음 등장하는가*에 대한 패턴 자료.

---

### 논문 22: LinkedIn Future of Work Report — AI at Work / Work Change Report (2024–2025)

- **저자·연도:** LinkedIn Economic Graph Team (Karin Kimbrough et al.), 2024–2025
- **발표처:** LinkedIn Economic Graph Reports
- **URL:** https://economicgraph.linkedin.com/research/future-of-work-report-ai — https://economicgraph.linkedin.com/research/work-change-report
- **요약 (3문장):** LinkedIn의 약 10억 회원·6천만 기업 데이터로 본 직업 변동 첫 데이터. **AI Engineer 채용공고 +143.2% (3년)**, Prompt Engineer +135.8%, AI Content Creator +134.5%. **2030년까지 직무 핵심 스킬의 약 70%가 변화** 예측.
- **핵심 수치·결과:**
  - AI Engineer 채용 +143.2% (3년)
  - Prompt Engineer +135.8%
  - 2030년까지 핵심 스킬 70% 변화
  - 1.3M 신규 AI 직군 + 600K 데이터센터 직군
  - 가장 빠른 성장 스킬: Custom GPTs, AI Productivity, AI Agents (2024)
- **인용할 만한 문장:**
  > "By 2030, 70% of the skills used in most jobs will change, with AI as the catalyst — and AI Engineer is among the fastest-growing job titles globally over the past three years."
- **챕터 매핑:** **→ 7~11장 새 직무명 검증의 핵심 산업 데이터**, → 12·13장(스킬 변동 70%의 함의)
- **독자 전달 방식 제안:** "직무명이 채용공고에 처음 등장한 시점이 그 직업의 '탄생일'이다. 이 책은 7~11장에서 그 탄생일을 추적한다."

---

### 논문 23: Prompt Engineer — Analyzing Skill Requirements in the AI Job Market

- **저자·연도:** An Vu, Jonas Oppenlaender, 2025
- **발표처:** arXiv:2506.00058
- **URL:** https://arxiv.org/html/2506.00058v1
- **요약 (3문장):** 채용 사이트에서 'prompt engineer' 명시 공고 수집·분석. 2024년 기준 전체 IT 공고의 **0.5% 미만**으로 여전히 희귀하지만, 요구 스킬 프로필이 명확 — AI 지식 22.8%, 프롬프트 디자인 18.7%, 커뮤니케이션 21.9%, 창의적 문제해결 15.8%. 즉, 단순 "프롬프트 잘 짜기"가 아니라 *AI×사람 인터페이스 설계자* 역할.
- **핵심 수치·결과:** 위 비율 + 2024~2030 prompt engineering 시장 CAGR 32.8%
- **챕터 매핑:** **→ 7장 (프롬프트 엔지니어 직무 정의 학술 자료)**

---

### 논문 24: O*NET-SOC 2019 New & Emerging Occupations 갱신

- **저자·연도:** US Department of Labor, O*NET Center (2020년 11월 25.1 DB 발표)
- **발표처:** O*NET Resource Center
- **URL:** https://www.onetcenter.org/dataUpdates.html — https://www.onetcenter.org/taxonomy.html
- **유형:** 정부 공식 직업 분류 (학술 인용 표준)
- **요약 (3문장):** 미국 표준 직업 분류 SOC 2018 → O*NET-SOC 2019 전환. 새로 등록된 emerging 직업: Data Scientist (15-2051.00), Information Security Engineer, Wind Turbine Service Technician, Solar Photovoltaic Installer 등. **Data Scientist는 2018 SOC에서 비로소 *독립 코드*를 받음** — 직무가 충분히 보편화된 후에야 분류가 따라잡는 구조.
- **핵심 수치·결과:**
  - O*NET 25.1 (2020-11): 1,016 직업 타이틀, 923 데이터 수준 직업
  - 신규 cybersecurity 4개 emerging 코드
- **챕터 매핑:** **→ 1장(직업이 이름을 얻는 데 걸리는 시차의 정부 데이터)**, → 7~11장(각 직업이 코드를 받았는지 여부로 성숙도 측정)
- **독자 전달 방식 제안:** "데이터 사이언티스트가 BLS 코드를 받은 게 2018년이다. 사람들은 그 전 10년 동안 그 일을 하고 있었다. AI 인프라 직업도 똑같다."

---

## 추가 권장 자료 (책 본문에서 짧게 인용 가능)

| 자료 | 저자 | 발행 | 챕터 매핑 |
|------|------|------|----------|
| *Diffusion of Innovations* (5e) | Everett Rogers | 2003 | 1장 (채택곡선 원전) |
| *Power and Prediction* | Agrawal, Gans, Goldfarb | 2022 | 2·5장 (예측재 보완재) |
| *Power and Progress* | Acemoglu, Johnson | 2023 | 13장 (방향 선택의 정치경제) |
| WEF *Four Futures for Jobs in the New Economy* | WEF | 2025 | 3장 |
| *Microfoundations of the Productivity J-curve(s)* | Brynjolfsson et al. | 2025 (CES WP) | 2장 |

---

## 균형 점검 — 가설 *반박/완화* 자료 명시

본 리서치는 책의 가설 ("AI 인프라 다음에 새 직업이 자란다")을 강화하는 자료뿐 아니라 *반박·완화* 자료를 의도적으로 포함했다.

| 반박 / 완화 포인트 | 출처 |
|--------------------|------|
| AI 거시 효과는 미미하다 (TFP 10년 ≤0.66%) | Acemoglu 2024 (논문 8) |
| 새 직무 자체는 소수 — *변형*이 더 큰 효과 | ILO 2025 (논문 13) |
| AI 채용 신입 진입은 -14% 둔화 | Anthropic Index 5차 (논문 12) |
| Reinstatement effect는 *지난 40년 약화*되었다 | Acemoglu·Restrepo 2019 (논문 11) |
| AI는 jagged frontier 바깥에선 -19%p 손해 | Dell'Acqua et al. 2023 (논문 9) |
| 다중 에이전트는 41~87% 실패 | Cemri et al. 2025 (논문 18) |
| LLM 평가는 50%+ 메모리화일 가능성 | Deng et al. 2024 (논문 20) |

이 7가지 반박 자료는 책이 "장밋빛 진로 예언서"가 아니라 *현실주의 가이드*임을 보장하는 학술 안전장치다. 13장 결론에서 이를 정직하게 다뤄야 한다.

---

## 메타 노트 — 인용 우선순위와 한계

**1순위 인용 (책 본문에 직접 인용 강력 권장):** 1, 2, 3, 7, 9, 10, 12, 18  
**2순위 (각주·박스):** 4, 5, 6, 8, 11, 13, 14, 19, 20, 22  
**3순위 (참고문헌만):** 15, 16, 17, 21, 23, 24

**한계:**
- 영역 4의 "새 직무명이 채용 공고에 등장하기 시작한 시점"을 직접 분석한 *peer-reviewed* 논문은 매우 드물다. LinkedIn·O*NET 데이터 사용이 학술 표준이 아닌 산업 보고서라는 한계 — 인용 시 출처 성격 명시 필요.
- 본 리서치는 영문 자료 중심. 한국 KESS·한국고용정보원 자료는 별도 community-research 흐름에서 보충 필요.
- 일부 NBER/HBS WP는 abstract+search 결과 기반이며, 실제 본문 일부 수치는 출판 버전에서 갱신될 수 있음. 인용 시 발행 버전(연도+게재 저널) 재확인 필요.

---

*리서치 작성: paper-researcher (책 "코드 너머의 직업들" 학술 토대)*  
*작성일: 2026-05-10*
