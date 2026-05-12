# 커뮤니티 리서치: 코드 너머의 직업들 — GPU 위에서 일하는 사람들

> **수집 범위:** Reddit, Hacker News, Glassdoor, Blind, Twitter/X, Medium, OKKY, velog, brunch, 한국 IT 매체, 회사 블로그, a16z·Lenny·Latent Space 같은 인플루언서 글, 채용 데이터 분석(Bloomberry, Levels.fyi)
> **수집 일자:** 2026-05-10
> **검증 라벨:** 모든 커뮤니티 발화는 "검증 필요"로 라벨링한다. 인용은 원문 출처 우선, 한국어 번역이 필요한 경우 의역으로 표기.
> **챕터 매핑:** 7장(AI PM) / 8장(FDE) / 9장(Applied AI Engineer) / 10장(AgentOps) / 11장(Eval Engineer) / 12장(한국 시장)

---

## 영역 1. 5개 직업별 실무자 목소리

### 1) AI Product Manager — 7장

#### (a) 일과 묘사

**"전통 PM이 백로그를 관리한다면, AI PM은 모델 학습 사이클·평가 프레임워크·AI 안전 프로토콜을 관리한다"**
- 출처: ProductSchool, Arize 블로그, Aakash Gupta 인터뷰 종합
- 일과의 핵심 변화:
  - "결정론적 시스템"에서 "확률적 시스템"으로 — 출력이 매번 다르다
  - PRD 대신 **evals(평가셋)**가 사양서가 된다
  - 정적 로드맵이 아니라 **continuous experimentation** 사이클로 굴러간다
  - 모델 드리프트·재학습 파이프라인·피드백 데이터를 일상적으로 모니터링한다

> "AI PM은 사용자 문제만 찾는 게 아니라, *AI가 진짜로 가치를 만드는 곳*과 *그냥 트렌디해서 갖다 붙이는 곳*을 구분하는 일을 추가로 한다."
> — Aakash Gupta, "I Interviewed 100+ AI Product Managers" (Medium, 2025)
> https://aakashgupta.medium.com/i-interviewed-100-ai-product-managers-heres-what-they-actually-do-9e55d393a287

#### (b) 무엇이 어렵나

- **"확률"이라는 머리 아픈 변수:** 같은 입력에도 출력이 달라지는 시스템에서 "이 기능은 작동한다"를 증명하는 게 가장 어렵다.
- **데이터 의존성:** 모델 성능이 데이터 분포 변화에 민감해서 "어제 잘 됐는데 오늘 안 된다"가 일상.
- **신뢰·윤리 부담:** bias·hallucination·privacy 등 전통 PM이 고민 안 하던 영역이 책임에 포함된다.

> "가장 큰 문제는 '데모는 멋지다'와 '프로덕션이 안정적이다'의 거리다. 그 거리를 좁히는 게 AI PM이 매일 하는 일이다."
> — Hamel Husain & Shreya Shankar, Lenny's Newsletter (2025)
> https://www.lennysnewsletter.com/p/why-ai-evals-are-the-hottest-new-skill

#### (c) 어떤 사람이 잘 맞나

- 통계·데이터 엔지니어링 백그라운드가 있는 PM이 가장 빠르게 적응한다 (Marily Nika 인터뷰)
- "AI 기술적 깊이"보다 "어디에 AI를 안 써야 하는지 판단력"이 핵심이라는 의견이 다수
- Lenny's Podcast에서 Marily Nika: "앞으로 모든 PM은 AI PM이 될 것이다. 이것은 별도 직군이 아니라 PM의 새로운 표준이다."
  - https://www.lennysnewsletter.com/p/ai-and-product-management-marily

#### (d) 기존 직무와의 차이 (커뮤니티가 합의한 표)

| 항목 | 전통 PM | AI PM |
|---|---|---|
| 사양 | PRD | Evals |
| 사이클 | 분기 로드맵 | 연속 실험 |
| 시스템 | 결정론적 | 확률적 |
| 책임 | 기능 출시 | + 모델 안전·드리프트 |
| 메트릭 | DAU·전환율 | + hallucination rate, factuality |

#### 인용 가능한 짧은 토막

- > "Evals replace traditional PRDs for AI products." — Hamel Husain (Hamel's Blog, 2026)
- > "AI PMs are making $300K+ while regular PMs get laid off." — Aakash Gupta (Medium, 2025) https://aakashgupta.medium.com/what-is-an-ai-product-manager-and-why-theyre-making-300k-while-regular-pms-get-laid-off-2c0ba0811008
- > "Every PM will be an AI PM in the future." — Marily Nika (Lenny's Newsletter)

---

### 2) Forward Deployed Engineer — 8장

#### (a) 일과 묘사

a16z 정의 (a16z Services-Led Growth, 2025):
> "고객사 사무실에 들어가서, 고객사의 시스템 위에서, 고객사의 데이터로, 우리 제품을 작동시키는 엔지니어. 그들은 영업도 컨설턴트도 지원도 아니다. 그들은 hands-on-keyboard builder다."
> https://a16z.com/services-led-growth/

Bloomberry의 1,000개 FDE 채용 공고 분석 (2025):
- **고객과 직접 협업: 55%** (1순위)
- **AI/ML 시스템 빌드 및 배포: 37%** (2순위)
- **시스템·API 통합: 32%** (3순위)
- 채용 공고 중 **매출 책임을 명시한 곳: 0%** — 이것은 영업 직무가 아니라는 강력한 신호
- https://bloomberry.com/blog/i-analyzed-1000-forward-deployed-engineer-jobs-what-i-learned/

Palantir의 원조 (a16z Palantirization 글):
> "2011년, Palantir는 solutions engineer와 integration engineer에게 새 타이틀을 줬다. Forward Deployed Engineer. 'Deltas'라고 부르기까지 했다 — Delta Force처럼. 우스꽝스러웠지만, 미친듯이 통했다."
> https://a16z.com/the-palantirization-of-everything/

#### (b) 무엇이 어렵나 — Glassdoor·Blind·HN 실무자 후기

Palantir Glassdoor (Forward Deployed Software Engineer 카테고리):
- 직무 만족도 평균: 워라밸 2.5/5
- 보상 4.2/5 (높은 편)
- 반복 후기:
  > "주 50시간+ 기본. 직무 책임이 흐릿해서 무엇이든 해야 한다."
  > "FDE 전원 결국 번아웃이 온다. 시간 문제일 뿐이다."
  > "FDE에서 SWE로 전환한다는 약속? 거짓말이었다."
- 출처: https://www.glassdoor.com/Reviews/Palantir-Technologies-Forward-Deployed-Software-Engineer-Reviews-EI_IE236375.0,21_KO22,56.htm

Hacker News의 가장 유명한 토론 (HN 11647103, 2016년이지만 지금도 인용됨):
> "Palantir is running an engineering mill/sweatshop using elite talent."
> https://news.ycombinator.com/item?id=11647103
- 검증 필요: 익명 코멘트, 다만 다수 추천(highly upvoted)

Blind에서 OpenAI/Anthropic FDE TC 토론:
> "Mid-to-senior level $350K-$550K. New grad TC $180K-$250K. Staff급 FDE는 $630K+ 찍는다."
> https://www.teamblind.com/post/comp-for-forward-deployed-software-engineerapplied-ai-at-openai-anthropic-ycrzocbu

#### (c) 어떤 사람이 잘 맞나

- "프로그래밍 + 도메인 전문성 + 대인관계"의 **희귀한 3종 결합** (Cubiq Recruitment)
- "고객 사무실에서 6개월 살 수 있는 사람"
- 코드만 잘 짜는 사람은 살아남지 못한다 — 정치·해명·교육이 일의 절반

#### (d) 기존 직무와의 차이

- vs. Solutions Engineer: SE는 데모·교육 중심, FDE는 **production code를 직접 쓴다**
- vs. Sales Engineer: 영업 책임이 없다 (Bloomberry 분석에서 0% 명시)
- vs. Consultant: 컨설턴트는 슬라이드를 쓰고 떠난다, FDE는 코드를 짜고 운영한다

#### 인용 가능한 짧은 토막

- > "Forward deployed engineer jobs exploded by 1,165% year-over-year." — Bloomberry (2025)
- > "The hottest job in startups." — a16z (2025)
- > "We took our solutions engineers and called them Deltas. It worked brilliantly." — a16z on Palantir
- > "Burnout happens eventually to all Forward Deployed Engineers." — Palantir Glassdoor 익명 후기

---

### 3) Applied AI Engineer — 9장

#### (a) 일과 묘사 — Hamel Husain & Eugene Yan 라인

Eugene Yan (Senior Applied Scientist, Amazon)의 자기 정의:
> "I design, build, and operate machine learning systems that serve customers at scale."
> https://eugeneyan.com/

Hamel Husain의 정의 (Parlance Labs):
> "Applied AI Engineer는 모델 품질에 매몰된 ML 엔지니어와 다르다. 우리는 production system이 데이터 접근, 추론 신뢰성, 오케스트레이션, 관측, 거버넌스를 다 지탱하도록 *엔지니어링*한다. 모델은 입력 중 하나일 뿐이다."

Howdy/dbreunig의 AI Title Guide (2025):
> "Data Scientists answer questions. ML Engineers build systems. AI Engineers ship products."
> https://www.dbreunig.com/2025/08/21/a-guide-to-ai-titles.html

Howdy 직무 분석 (2026):
- 일상의 예: "RAG retrieval이 왜 엉뚱한 chunk를 가져오는지 디버깅, agent의 성공률을 측정하는 eval 작성, LangGraph workflow에 새 function-calling tool 통합, hallucination 15% 줄이는 프롬프트 튜닝"
- LinkedIn: AI Engineer 채용 +74% YoY vs ML Engineer +33%

Swyx, "The Rise of the AI Engineer" (Latent Space, 2023, 지금도 가장 자주 인용됨):
> "예전엔 5년 걸리던 AI 작업이 API 문서와 한가한 오후 한 번이면 가능해졌다. Andrej Karpathy도 동의했다. 수학적으로, AI Engineer는 ML Engineer보다 10배 많아질 것이다."
> https://www.latent.space/p/ai-engineer

#### (b) 무엇이 어렵나

velog에 올라온 한국 AI 엔지니어 후기 (qlgks1):
> "파인튜닝 이후 모델을 어떻게 평가해야 하는가? 정량적 지표가 부정확하거나 불충분할 때, 어떻게 QA 해야 하는가? 이게 책에서도 가장 길게 나오는 부분이다."
> https://velog.io/@qlgks1/%EC%B1%85-%EB%A6%AC%EB%B7%B0-LLM-%EC%97%94%EC%A7%80%EB%8B%88%EC%96%B4%EB%A7%81

LBox AI 개발기 (Dongjun Lee, Medium):
> "LLM 기반 서비스만의 특징이 있다. 비결정성, 비용, 레이턴시, 평가의 어려움. 우리는 이 시행착오를 직접 겪고서야 인정했다."
> https://medium.com/lbox-team/llm-%EA%B8%B0%EB%B0%98-application-lbox-ai-%EA%B0%9C%EB%B0%9C%EA%B8%B0-e00fdcad705f

#### (c) 어떤 사람이 잘 맞나

- 시니어 소프트웨어 엔지니어로 production system을 책임져본 경험 (Hamel Husain의 일관된 주장)
- "ML 박사가 아니라 엔지니어링 감각이 있는 사람" — Howdy 분석에서 반복
- velog dkvlg "AI 엔지니어 되는 방법": "단위 테스트, 트레이싱, 비용 관리 도구를 자유롭게 다룰 줄 알아야 한다."
  - https://velog.io/@dkvlg/AI-%EC%97%94%EC%A7%80%EB%8B%88%EC%96%B4-%EB%90%98%EB%8A%94-%EB%B0%A9%EB%B2%95

#### (d) 기존 직무와의 차이

| 항목 | ML Engineer | Applied AI Engineer |
|---|---|---|
| 초점 | 모델 레이어 (학습·추론·튜닝) | 애플리케이션 레이어 (시스템·통합) |
| 일상 | 학습 파이프라인·feature store | RAG·prompt·evals·orchestration |
| 산출물 | 모델 가중치 | 작동하는 제품 |
| 출신 | 통계·박사 다수 | 시니어 풀스택 다수 |

#### 인용 가능한 짧은 토막

- > "Data Scientists answer questions. ML Engineers build systems. AI Engineers ship products." — dbreunig
- > "수학적으로, AI Engineer는 ML Engineer보다 10배 많아질 것이다." — Swyx (Latent Space, 2023)
- > "5년 걸리던 작업이 API 문서와 한가한 오후로 가능해졌다." — Swyx
- > "ML engineers focus on the model. Applied AI engineers focus on the system around the model." — Hamel Husain

---

### 4) AgentOps / Agent 운영자 — 10장

#### (a) 용어 정의 — IBM, arXiv 2024 논문

IBM Think (2025):
> "AgentOps — agent operations — is an emerging set of practices focused on the lifecycle management of autonomous AI agents, bringing together principles from DevOps and MLOps."
> https://www.ibm.com/think/topics/agentops

학술 정착 신호: arXiv 2411.05285 "AgentOps: Enabling Observability of LLM Agents" (2024년 11월)
> https://arxiv.org/abs/2411.05285
- 의미: 용어가 산업·학술 양쪽에서 동시 등장. **"AgentOps"는 이제 trade jargon이 아니라 신생 분야 명칭으로 굳어지는 중.**

#### (b) 도구 생태계 비교 — 2025-2026 커뮤니티 토론

| 도구 | 핵심 강점 | 라이선스 | 도입 패턴 |
|---|---|---|---|
| LangSmith | LangChain 생태계 통합, 오버헤드 거의 0 | 상용 SaaS | Production 성능 민감 팀 |
| Langfuse | 오픈소스·셀프호스팅, MIT, 프롬프트 관리 강력 | OSS + Cloud | 데이터 주권 중시 기업 |
| Helicone | 프록시 방식 (URL 한 줄 변경) | 상용 | 빠른 도입 원하는 팀 |
| Arize Phoenix | eval rigor, ML observability 헤리티지 | OSS + Enterprise | 엔터프라이즈 컴플라이언스 |
| Braintrust | eval-first | 상용 | 평가 중심 팀 |
| AgentOps (도구) | 시간여행 디버깅, 멀티에이전트 시각화 | 상용 | 복잡한 멀티에이전트 시스템 |
| W&B Weave | 실험 관리 + LLM 트레이싱 | 상용 | 기존 W&B 사용자 |

출처:
- LangChain 공식 비교: https://www.langchain.com/articles/llm-observability-tools
- Latitude 비교 분석: https://latitude.so/blog/best-llm-observability-tools-agents-latitude-vs-langfuse-langsmith
- AIMultiple 15개 도구 정리: https://research.aimultiple.com/agentic-monitoring/

핵심 시장 신호:
- Langfuse가 2026년 1월 ClickHouse에 인수됨 — "오픈소스는 그대로 유지"
- AgentOps 시장 추정: 2024년 약 50억 달러 → 2030년 약 500억 달러 (IBM)

#### (c) "AgentOps"가 진짜 직무로 등장하는가? — 검증 필요

- 채용 공고에서 **"AgentOps Engineer"라는 정확한 타이틀은 아직 드물다**
- 대신 등장하는 표현: "LLMOps Engineer", "AI Platform Engineer", "ML Infra (LLM)", "Applied AI Engineer (Reliability)"
- 한국 SK Devocean 블로그: 에이닷 운영팀이 사실상 AgentOps 역할 수행 중
  > "프롬프트 엔지니어링과 운영체계를 통해 운영 리소스를 50% 감축하면서 발화 작업량을 3배로 늘렸다."
  > https://devocean.sk.com/blog/techBoardDetail.do?ID=166281

#### (d) 한국 도입 사례

LangSmith·Langfuse 한국 도입 신호:
- SKT에서 LangSmith 강의 진행 (sudormrf.run 후기)
  > "최근 LangSmith를 RAG 시스템 개발/운영에 유용하게 사용하고 있으며, SKT에서 Langsmith 사용에 대한 강의도 진행했다."
  > https://sudormrf.run/2024/08/17/langsmith_review/
- Langfuse 한국어 공식 문서 존재: https://langfuse.com/kr
- PyTorch KR 커뮤니티 토론: https://discuss.pytorch.kr/t/langfuse-llm/2373

한국 실무자가 자주 언급하는 패턴 (영주.dev 블로그 정리):
> "먼저 트레이싱을 설정하여 모든 LLM 호출을 기록하고, 비용 추적을 추가하고, 자동 평가 파이프라인을 구축하고, 마지막으로 프롬프트 버전 관리와 A/B 테스트로 발전시켜 나가는 것이 현실적인 도입 경로다."
> https://www.youngju.dev/blog/ai-platform/2026-03-09-ai-platform-llm-monitoring-langsmith-langfuse-arize

#### 인용 가능한 짧은 토막

- > "Hallucinations are not just a model problem. In production, they are a system design problem." — Galileo AI 블로그
- > "Production LLM failure rates range from 5% to 30% depending on use case complexity." — OptimusAI
- > "프롬프트는 더 이상 코드 안에 하드코딩되지 않는다. 대시보드에서 비개발자가 수정한다." — 한국 영주.dev 블로그

---

### 5) Eval Engineer — 11장

#### (a) 일과 묘사 — Anthropic JD 분석

Anthropic 채용 공고 (Research Engineer, Model Evaluations):
- "evaluation 플랫폼 설계·구현"
- "novel evaluation methodologies — reasoning, safety, helpfulness, harmlessness"
- "high-throughput evaluation pipelines that run during production training"
- "evaluation results를 분석해 failure mode 식별, training 결정에 영향"
- 요구사항: "ML 모델, 특히 LLM의 evaluation system 설계 경험" + "distributed computing 경험"
- 출처: https://job-boards.greenhouse.io/anthropic/jobs/4990535008

#### (b) 무엇이 어렵나

Hamel Husain & Shreya Shankar (Maven AI Evals 코스, 4,500+명 수료):
> "We spent 60-80% of our development time on error analysis and evaluation. Most effort goes toward understanding failures rather than building automated checks."
> https://hamel.dev/blog/posts/evals-faq/

같은 글의 핵심 진단:
> "Teams jump straight to building LLM judges or dashboards without knowing what they're measuring. They build judges for generic things like 'helpfulness' or 'conciseness' that don't catch real problems. Error analysis is not optional — it's the foundation. Skip it and everything else is built on sand."

Lenny's Podcast (2025):
> "Everyone's demoing AI features, but few are shipping them to production reliably. The gap is evals."

Jason Liu의 RAG Evals 프레임워크:
> "There are only 6 RAG evals. Tier 1 covers traditional IR metrics. Tiers 2-3 evaluate Question/Context/Answer relationships."
> https://jxnl.co/

#### (c) 어떤 사람이 잘 맞나

- "Skills in both systems engineering AND experimental design" (Anthropic JD)
- 통계적 사고 + Python distributed computing
- 가설을 만들고 깨고 다시 세우는 *과학자형 엔지니어*

#### (d) 기존 직무와의 차이

- vs. QA Engineer: QA는 결정론적 테스트, eval은 확률적·통계적 measurement
- vs. ML Researcher: 새 모델 만들지 않고 *측정*만 한다
- vs. Test Engineer: 정답이 없는 문제를 다룬다 — "정답"을 정의하는 것 자체가 일

#### 인용 가능한 짧은 토막

- > "Error analysis is not optional. Skip it and everything else is built on sand." — Hamel Husain
- > "We spent 60-80% of our development time on error analysis and evaluation." — Husain & Shankar
- > "Evals are the hottest new skill for product builders." — Lenny's Newsletter title (2025)

---

## 영역 2. 채용 공고 패턴 — JD 키워드·연봉·회사군

### 키워드 빈도 (Bloomberry 1,000건 FDE 분석)

| 키워드 | 빈도 |
|---|---|
| Customer-facing / direct customer work | 55% |
| AI/ML system build & deploy | 37% |
| System/API integration | 32% |
| Production code | 명시 다수 |
| Revenue / quota / pipeline | 0% (의도적 제외) |

### 키워드 빈도 (한국 대기업 AI 에이전트 채용 — Threads 분석)

> "거의 모든 공고가 RAG와 LangChain 경험 요구. LLMOps 운영 능력 중요. **연구자 < 응용 엔지니어** 비중. 대기업이 모델 연구보다 LLM으로 비즈니스 문제 푸는 사람을 원함."
> — jmhong2020 Threads 분석 (2025)
> https://www.threads.com/@jmhong2020/post/DQSPetlEufT

### 연봉 — Levels.fyi 기준 (2026)

| 회사 / 직군 | 연봉 범위 (TC) |
|---|---|
| Anthropic SWE | $563K (Senior) ~ $785K+ (Lead), 중간값 $710K |
| OpenAI SWE | $249K (L2) ~ $1.28M (L6), 중간값 $555K |
| OpenAI L5 | $1.15M ($336K base + $774K stock) |
| Frontier lab 중간값 | $600K ~ $795K (시니어 이상) |
| FDE 일반 시장 중간값 | $173,816 |
| FDE OpenAI/Anthropic mid-senior | $350K ~ $550K |
| Palantir FDE | $205K ~ $486K, staff급 $630K+ |
| 미국 전체 AI Engineer base 평균 | $145K ~ $190K |

출처:
- https://www.levels.fyi/companies/anthropic/salaries/software-engineer
- https://www.levels.fyi/companies/openai/salaries/software-engineer
- https://bloomberry.com/blog/i-analyzed-1000-forward-deployed-engineer-jobs-what-i-learned/
- https://www.sundeepteki.org/forward-deployed-engineer.html

### 회사군 분류

**Frontier lab (모델을 만든다):**
- OpenAI, Anthropic, Google DeepMind, xAI, Meta FAIR
- 직무 무게중심: Research Engineer + Applied AI Engineer + FDE
- TC 가장 높음 ($350K~$1M+)

**Application lab (모델 위에 제품을 만든다):**
- Cursor (Anysphere) — 약 50명, 대부분 엔지니어, 매니지먼트 거의 없음
  - https://cursor.com/careers
- Perplexity, Sierra, Glean, Harvey, Hebbia, Decagon
- 직무 무게중심: Applied AI Engineer + Product Manager (AI) + FDE

**Enterprise software (AI 팀이 따로 있다):**
- Salesforce Agentforce, ServiceNow, Atlassian, Notion AI, Slack
- 직무 무게중심: Applied AI Engineer + AgentOps (LLMOps) + Eval

**전통 산업:**
- 금융, 헬스케어, 제조 — Anthropic FDE의 Fortune 500 임베디드 사례가 가장 많은 곳
- 직무 무게중심: FDE + AI Solutions Architect

---

## 영역 3. 한국 시장 신호 — 12장 핵심

### A. 인력난의 명백한 신호

KMJournal·네이트 뉴스 등 다수 매체 보도 (2026년 초):
- 고용노동부·한국직업능력연구원 추산: **2023~2027년 AI 분야 12,800명 부족** (클라우드 18,800명 추가)
- 국내 AI 기업 2,354곳 중 **81.9%가 인력 부족 호소**
- 스탠퍼드 2025 AI Index: 한국 AI 인재 순유출 -0.36/만명, **OECD 38개국 중 35위 (최하위권)**

> "수백억 원을 투자해 인프라를 깔아놨지만, LLM을 고도화할 수석 엔지니어급 인력을 수개월째 구하지 못하고 있다. 미국 빅테크 연봉의 70%를 제시해도 실력자들은 이미 실리콘밸리로 떠났거나 국내 대기업이 흡수한 상태다."
> — KMJournal (2026)
> https://www.kmjournal.net/news/articleView.html?idxno=7040

> "다룰 사람이 없다 — 텅 빈 한국 AI 두뇌"
> — 네이트 뉴스 (2026.01.05)

### B. 5개 직군의 한국 채용 매핑

#### B-1) AI Product Manager (한국)
- **명시적 'AI PM' 타이틀은 아직 드물다**
- 대신 등장하는 형태:
  - 토스 — "Product Manager (AI 활용 기획 포함)" 직무 다수
  - 당근 — Product Manager (https://about.daangn.com/jobs/product-manager/)
  - 카카오스타일 PM 이미준의 분석: "미국 데이터에서 AI PM은 기하급수적 증가, 일반 PM은 정체"
  - 잡코리아 PMPO Day: "AI가 아니라 AI를 잘 쓰는 PM에 의해 대체된다"
  - https://www.jobkorea.co.kr/goodjob/tip/view?News_No=22472
- **검증 필요한 가설:** 한국에서 'AI PM'은 별도 채용 라인이 아니라 PM이 자기 도구상자에 AI를 더하는 형태로 진행 중. 별도 직군화는 1~2년 후 예상.

#### B-2) Forward Deployed Engineer (한국)
- **정확한 'FDE' 타이틀은 거의 없다**
- 가장 가까운 형태:
  - LG CNS — AI Tech 컨설턴트, AI Service Design 컨설턴트, AI 솔루션 아키텍트, AI 어플리케이션 개발자 (총 11개 직무 채용 중)
    > "LG CNS는 AI 분야 전문가 확보를 위해 AI 직군 전 분야에 걸쳐 경력직 채용 중. AI Scientist, AI Engineer, AI Architecture, AI Application Development, AI Tech Consultant, AI Service Design Consultant 등 11개 직무. 연말까지 1,000명 확보 목표."
    > https://www.smartfn.co.kr/news/articleView.html?idxno=110739
  - 삼성SDS — AI 음성 처리 전문가, 솔루션 컨설턴트, AI 컨설팅 직군
  - 업스테이지 — AI Customer Engineer, AI Solution Architect (Japan/한국), AI Business Development
    > https://careers.upstage.ai/
- **검증 필요한 가설:** 한국의 FDE형 직무는 SI 빅3(삼성SDS·LG CNS·SK C&C)에서 "AI 컨설턴트 + 솔루션 아키텍트" 형태로 분리·재조합 중. SI 빅3가 2026년 매출의 40%+를 AI 관련 SI 프로젝트로 잡겠다는 시그널.
  - https://www.youngju.dev/blog/culture/2026-03-23-si-industry-ai-transformation-career-guide

#### B-3) Applied AI Engineer (한국)
- **가장 활발한 채용 영역**. 다양한 타이틀로 등장.
- 회사별 매핑:
  - 카카오 — Machine Learning Engineer (LLM/Search), Large Language Model 개발자 (경력)
  - 네이버 — 2026 NAVER AI CHALLENGE (ML Engineer, 데이터 사이언티스트, Python 개발자)
  - 토스 — ML Engineer (커머스 도메인에 AI '즉시 적용')
  - 당근 — 2026 ML 직군 (피드 품질팀, 광고추천팀, LLM 개인화 추천)
  - 업스테이지 — AI Research Engineer (LLM Evaluation), AI Solution Architect, 30개 직무
  - LG AI Research — Research Scientist/Engineer (EXAONE Lab, Data Intelligence, STT/TTS)
  - 뤼튼 — 17개 분야 채용, 합격자에 2,000만원 보너스
- 키워드 패턴: **RAG + LangChain + LLMOps + 평가**가 거의 모든 공고에 등장
- 출처:
  - https://kr.linkedin.com/company/lgairesearch/jobs
  - https://careers.kakao.com/jobs
  - https://toss.im/career/jobs
  - https://www.aitimes.com/news/articleView.html?idxno=169900 (뤼튼)

#### B-4) AgentOps / LLMOps (한국)
- **개별 'AgentOps Engineer' 타이틀은 거의 없다**. 대신:
  - SK Devocean에 운영 사례 다수 (에이닷 LLM 운영, 프롬프트 엔지니어링)
  - 도입 도구: LangSmith (SKT 강의), Langfuse (한국어 공식 문서, 셀프호스팅 활발)
  - 한국 사례 후기 (sudormrf.run, hellollama.net, 영주.dev 블로그 등 다수)

#### B-5) Eval Engineer (한국)
- **거의 없다.** 가장 늦게 들어올 직군.
- 가까운 형태: **업스테이지의 "AI Research Engineer (LLM Evaluation)"** — 영문 표기로만 등장
- 카카오·네이버는 ML Engineer 직무에 평가 책임이 포함됨 (별도 직군 아님)

### C. 한국 SI·대기업의 AI 전환 신호

영주.dev "SI 산업의 AI 대전환" (2026.03.23):
- Gartner 인용: **2028년까지 SI 프로젝트 80%의 코딩 작업이 AI로 자동화**
- 삼성SDS 풀스택 AI 아키텍처: "인프라 → 플랫폼 → 애플리케이션 → 컨설팅" 전 영역 커버
- 삼성SDS AI 관련 SI 비중 2026년 40%+ 전망
- SI 엔지니어 역할 변화 로드맵:
  - 2020-2024: 코더
  - 2025-2027: AI 활용 개발자
  - 2028-2030: **AI 오케스트레이터**
- https://www.youngju.dev/blog/culture/2026-03-23-si-industry-ai-transformation-career-guide

ZDNet Korea (2025.12):
> "삼성SDS·LG CNS·SK C&C, 인사 키워드는 'AX'… 전략은 '동상이몽'"
> https://zdnet.co.kr/view/?no=20251205105935

ZDNet Korea (2025.12.08):
> "2026 채용 트렌드: 4~7년차 경력직 + AI 활용 인재 더 뽑는다."
> https://zdnet.co.kr/view/?no=20251208160526

### D. OKKY·velog·brunch에서의 AI 직무 전환 후기

OKKY 핵심 글 5선 (검증 필요, 익명 다수):

1. **"AI 엔지니어 현실 좀 알려주세요"** (글 1327398)
   - 1년차 AI 연구개발원, 학사 출신. "석사가 꼭 필요한가" 토론 길게 이어짐.
   - https://okky.kr/articles/1327398

2. **"엔지니어링 능력이 부족한 AI 연구원"** (글 765754)
   - "논문은 쓸 수 있지만 production 코드를 못 쓴다는 자기 진단" — 한국 AI 인력 시장의 핵심 갭
   - https://okky.kr/articles/765754

3. **"학사 출신 머신러닝 엔지니어 커리어 고민"** (글 1462220)
   - "경력 이직 vs 대학원" — 한국 ML 시장에서 반복되는 질문
   - https://okky.kr/articles/1462220

4. **"비전공자 신입 ai 솔루션입니다. 조언 부탁드립니다"** (글 1344449)
   - 비전공자 신입의 AI 솔루션 직무 진입 후기
   - https://okky.kr/articles/1344449

5. **"머신러닝 3년차 진로방향 고민"** (글 667062)
   - 데이터 사이언티스트 3년차의 이직 고민, "DS → ML Engineer → AI Engineer" 흐름
   - https://okky.kr/articles/667062

velog 대표 글 5선:

1. **[책 리뷰] LLM 엔지니어링 (qlgks1)** — production LLM의 평가 어려움이 가장 길게 다뤄짐
   - https://velog.io/@qlgks1/%EC%B1%85-%EB%A6%AC%EB%B7%B0-LLM-%EC%97%94%EC%A7%80%EB%8B%88%EC%96%B4%EB%A7%81

2. **AI 엔지니어 되는 방법 (dkvlg)** — 단위 테스트, 트레이싱, 비용 관리 도구의 중요성
   - https://velog.io/@dkvlg/AI-%EC%97%94%EC%A7%80%EB%8B%88%EC%96%B4-%EB%90%98%EB%8A%94-%EB%B0%A9%EB%B2%95

3. **Ollama에서 vLLM으로: 4.8배 빠르게 (imkkuk)** — 프로덕션 LLM 서빙 도구 전환기
   - https://velog.io/@imkkuk/Ollama%EC%97%90%EC%84%9C-vLLM%EC%9C%BC%EB%A1%9C-%ED%94%84%EB%A1%9C%EB%8D%95%EC%85%98-LLM-%EC%84%9C%EB%B9%99-4.8%EB%B0%B0-%EB%B9%A0%EB%A5%B4%EA%B2%8C-%EB%A7%8C%EB%93%A4%EA%B8%B0

4. **코드 리뷰 자동화 시스템 구축하기 (yaza)** — RAG 파이프라인 구축 시행착오
   - https://velog.io/@yaza/%EC%BD%94%EB%93%9C-%EB%A6%AC%EB%B7%B0-%EC%9E%90%EB%8F%99%ED%99%94-%EC%8B%9C%EC%8A%A4%ED%85%9C-%EA%B5%AC%EC%B6%95%ED%95%98%EA%B8%B0-w-ollama-1%ED%8E%B8-Proof-of-Concept

5. **LLM 바이브 코딩과 LLM 대규모 서베이 (qlgks1)** — 최신 흐름 정리
   - https://velog.io/@qlgks1/a-survey-of-vibe-coding-with-llm

회사 블로그 발화:
- 당근 "AI 툴 개발은 처음이라" (Medium):
  > "당근의 PM Heart도 Cursor를 사용해 PM에게 유용한 플러그인을 만들었으며, 팀 안에 자연스럽게 AI 실험 문화가 번져나갔다."
  > https://medium.com/daangn/ai-%ED%88%B4-%EA%B0%9C%EB%B0%9C%EC%9D%80-%EC%B2%98%EC%9D%8C%EC%9D%B4%EB%9D%BC-%EB%8B%B9%EA%B7%BC-%EB%B9%84%EA%B0%9C%EB%B0%9C%EC%9E%90-%EA%B5%AC%EC%84%B1%EC%9B%90%EB%93%A4%EC%9D%98-ai-%EB%8F%84%EC%A0%84%EA%B8%B0-fb62d2a6c2f3

- LBox AI 개발기:
  > "LLM 기반 서비스만의 특징과 직접 개발하며 겪은 시행착오 공유"
  > https://medium.com/lbox-team/llm-%EA%B8%B0%EB%B0%98-application-lbox-ai-%EA%B0%9C%EB%B0%9C%EA%B8%B0-e00fdcad705f

### E. 왜 한국에서 자료가 적은가 — 분석

1. **직군이 아직 정착 중:** 'AI PM', 'FDE', 'Eval Engineer' 같은 정확한 영문 타이틀은 한국 채용 시장에 1~2년 늦게 들어온다.
2. **영문 표기 차이:** 같은 일을 "AI 엔지니어", "ML Engineer (LLM)", "AI 응용 엔지니어", "AI Solution Architect" 등 다른 이름으로 부른다.
3. **회사 블로그 위주:** 익명 커뮤니티(OKKY, Reddit 한국 서브레딧) 토론은 미국에 비해 적고, 회사 기술 블로그가 더 자주 인용된다.
4. **인재 유출:** 스탠퍼드 AI Index OECD 35위 — 실력자 다수가 미국·해외에 있어 한국 커뮤니티에 글을 안 쓴다.
5. **SI 산업의 변환 진행 중:** SI 빅3가 'AI 컨설턴트' 형태로 FDE형 직무를 만들고 있지만, 명칭이 정착되지 않음. 12장에서 "한국의 FDE는 SI 컨설턴트의 진화형으로 등장한다"는 가설이 가능하다 (검증 필요).

---

## 영역 4. AgentOps 도구 생태계 (10장 시그니처 보강)

### 도구별 핵심 정리

| 도구 | 라이선스 | 가격 모델 | 핵심 차별화 | 주요 도입 사례 |
|---|---|---|---|---|
| **LangSmith** | 상용 SaaS | usage-based | 프레임워크 무관, LangChain 공식, 오버헤드 미미 | Anthropic·OpenAI 사용자 다수 |
| **Langfuse** | OSS (MIT) + Cloud | OSS 무료 + Cloud paid | 셀프호스팅, 프롬프트 관리, MIT | ClickHouse가 2026.01 인수, OSS 이동 활발 |
| **Helicone** | 상용 + OSS | proxy 기반 free tier | URL 한 줄 변경으로 도입 | 빠른 도입 원하는 스타트업 |
| **Arize Phoenix** | OSS + Enterprise | OSS 무료 + Enterprise | SOC 2/HIPAA/GDPR, eval rigor | 엔터프라이즈 |
| **W&B Weave** | 상용 | 기존 W&B 라이선스 | 기존 ML 실험 관리와 통합 | 전통적 ML 팀 |
| **Braintrust** | 상용 | usage-based | eval-first 디자인 | 평가 중심 팀 |
| **Patronus AI** | 상용 | enterprise | LLM 평가 자동화 | 컴플라이언스 중시 |
| **OpenLLMetry** | OSS | 무료 | OpenTelemetry 호환 | 표준화 추구 |
| **AgentOps (도구)** | 상용 | usage-based | 시간여행 디버깅, 멀티에이전트 시각화 | 복잡한 agent 시스템 |

출처:
- https://www.langchain.com/articles/llm-observability-tools
- https://research.aimultiple.com/agentic-monitoring/
- https://latitude.so/blog/best-llm-observability-tools-agents-latitude-vs-langfuse-langsmith
- https://www.helicone.ai/blog/the-complete-guide-to-LLM-observability-platforms
- https://www.firecrawl.dev/blog/best-llm-observability-tools

### "AgentOps" 용어 사용 추이

- 2024: 학술 논문 등장 (arXiv 2411.05285), 산업 매체 산발적 사용
- 2025: IBM·a16z·Latent Space 등이 일상적으로 사용
- 2026: 채용 공고 표제로는 아직 드물지만, 실무 문서·블로그·컨퍼런스 트랙명으로 정착

검증 필요한 가설: 'AgentOps'는 'MLOps'가 그랬던 것처럼 1~2년 안에 정식 직군으로 자리잡을 가능성이 높다 (지금은 LLMOps·AI Platform Engineer로 분산).

---

## 영역 5. 인용 가능한 짧은 토막 (챕터 epigraph 후보)

### Top 10 (강도 순)

1. > "5년 걸리던 AI 작업이 API 문서와 한가한 오후 한 번이면 가능해졌다."
   — Swyx (Shawn Wang), "The Rise of the AI Engineer", Latent Space, 2023
   https://www.latent.space/p/ai-engineer
   *(전체 책의 핵심 변화를 단 한 문장으로)*

2. > "Data Scientists answer questions. ML Engineers build systems. AI Engineers ship products."
   — Drew Breunig, "A Guide to AI Titles", 2025
   https://www.dbreunig.com/2025/08/21/a-guide-to-ai-titles.html
   *(9장 Applied AI Engineer 도입부)*

3. > "Forward deployed engineer jobs exploded by 1,165% year-over-year."
   — Bloomberry, 1,000 FDE Job Analysis, 2025
   https://bloomberry.com/blog/i-analyzed-1000-forward-deployed-engineer-jobs-what-i-learned/
   *(8장 FDE 도입부 — 숫자의 충격)*

4. > "We took our solutions engineers and called them Deltas — like Delta Force. It sounded ridiculous, and it worked brilliantly."
   — a16z on Palantir, "The Palantirization of Everything"
   https://a16z.com/the-palantirization-of-everything/
   *(8장 — FDE의 기원 이야기)*

5. > "Evals replace traditional PRDs for AI products."
   — Hamel Husain, hamel.dev/blog/posts/evals/
   *(7장 AI PM 또는 11장 Eval Engineer)*

6. > "Error analysis is not optional. Skip it and everything else is built on sand."
   — Hamel Husain & Shreya Shankar, hamel.dev/blog/posts/evals-faq/
   *(11장 Eval Engineer 도입부)*

7. > "Hallucinations are not just a model problem. In production, they are a system design problem."
   — Galileo AI, "8 Best LLM Reliability Solutions for Production"
   https://galileo.ai/blog/best-llm-reliability-solutions
   *(10장 AgentOps)*

8. > "Burnout happens eventually to all Forward Deployed Engineers."
   — Palantir Glassdoor 익명 후기 (검증 필요)
   *(8장 — 직무의 그림자 면)*

9. > "GPU는 쌓였는데 사람이 없다."
   — KMJournal, "한국 AI 발목 잡는 인력난", 2026
   https://www.kmjournal.net/news/articleView.html?idxno=7040
   *(12장 한국 시장 도입부 — 가장 강한 한국어 헤드라인)*

10. > "다룰 사람이 없다 — 텅 빈 한국 AI 두뇌."
    — 네이트 뉴스, 2026.01.05
    *(12장 — 헤드라인급)*

### 추가 토막 5선 (중간 삽입용)

11. > "Every PM will be an AI PM in the future. This is not a separate role — it is the new default."
    — Marily Nika, Lenny's Newsletter

12. > "Most teams jump straight to building LLM judges without knowing what they're measuring."
    — Husain & Shankar, AI Evals course

13. > "We spent 60-80% of our development time on error analysis and evaluation."
    — Husain & Shankar

14. > "By embracing the professional services motion today, AI startups are positioning themselves to become the systems of record tomorrow."
    — a16z, Services-Led Growth
    https://a16z.com/services-led-growth/

15. > "AI 시대의 SI 엔지니어는 '코더'에서 'AI 오케스트레이터'로 변화한다."
    — 영주.dev, SI 산업의 AI 대전환, 2026
    https://www.youngju.dev/blog/culture/2026-03-23-si-industry-ai-transformation-career-guide

---

## 반복되는 고통·질문 (챕터 오프닝 소재 정리)

### 패턴 1: "데모는 멋진데 프로덕션은 왜 안 되나"
- AI PM·Applied AI Engineer·Eval Engineer 모두에서 반복.
- 인용:
  - Husain/Shankar: "Everyone's demoing, few are shipping reliably."
  - Galileo: "Production LLM failure rates 5-30%"
  - 한국 LBox: "LLM 기반 서비스만의 특징과 시행착오"
- 챕터 오프닝 활용: 7장·9장·10장·11장의 공감 포인트로 반복 사용 가능

### 패턴 2: "ML 박사 vs 응용 엔지니어"
- OKKY 글 765754("엔지니어링 능력이 부족한 AI 연구원")이 한국에서의 정확한 표현
- 미국 swyx: "AI Engineer가 ML Engineer보다 10배 많아질 것이다"
- 챕터 오프닝: 9장 Applied AI Engineer 도입부

### 패턴 3: "이 직군의 정확한 이름이 뭔가"
- 한국 OKKY·velog 곳곳에서 "AI 엔지니어가 정확히 뭐 하는 사람인가" 질문 반복
- 미국에서도 "AI Engineer vs ML Engineer vs Data Scientist" 가이드 글이 매년 나옴
- 챕터 오프닝: 모든 챕터에 활용 — "이 직무가 뭔지부터 정의하자"

### 패턴 4: "FDE의 워라밸과 번아웃"
- Palantir Glassdoor 일관된 후기
- HN 토론: "engineering mill/sweatshop"
- 챕터 오프닝: 8장 FDE의 그림자 면 — 책의 톤이 단순 찬양이 아니라 균형 잡힌다는 신호

### 패턴 5: "한국에서 같은 일을 다른 이름으로 부른다"
- Applied AI Engineer = ML Engineer (LLM) = AI 엔지니어 = AI 응용 엔지니어
- FDE = AI 컨설턴트 + 솔루션 아키텍트 (SI 빅3에서)
- 챕터 오프닝: 12장 한국 시장 — 명칭의 혼란 자체가 시장의 미성숙 신호

---

## 실무 휴리스틱 모음

### 휴리스틱 1: "측정할 수 없으면 만들지 마라"
- 출처: Hamel Husain, "Your AI Product Needs Evals" (hamel.dev/blog/posts/evals/)
- 원문: "We expect most effort to go toward understanding failures rather than building automated checks."
- 적용: AI 제품 개발 초기 60-80% 시간을 error analysis에 쓰는 게 합리적

### 휴리스틱 2: "AI 도입 4단계 — 트레이싱 → 비용 → 자동평가 → 프롬프트 관리"
- 출처: 영주.dev (한국 실무자 정리)
- 적용: AgentOps 도입 로드맵의 표준 시퀀스

### 휴리스틱 3: "FDE 채용 공고에 매출 책임이 있으면 그건 영업이다"
- 출처: Bloomberry 1,000건 분석 (revenue 책임 0%)
- 적용: 진짜 FDE 직무를 가짜 SE 직무와 구분하는 기준

### 휴리스틱 4: "RAG + LangChain은 한국 응용 엔지니어 채용의 표준 공통분모"
- 출처: Threads jmhong2020 분석, 인크루트·잡코리아 키워드 빈도
- 적용: 한국 시장 진입을 위한 최소 기술 스택

### 휴리스틱 5: "오픈소스 셀프호스팅이 한국 엔터프라이즈의 기본 입찰"
- 출처: Langfuse 한국어 문서 활성도, SKT Devocean 사례
- 적용: 한국 도구 선택의 데이터 주권 우선 경향

---

## 논쟁점

### 논쟁 A: "AI PM은 별도 직군인가, PM의 새 표준인가"
- 관점 1 (별도 직군): Aakash Gupta, ProductSchool — 통계·ML 백그라운드, $300K+ 별도 trajectory
- 관점 2 (새 표준): Marily Nika — "모든 PM이 AI PM이 될 것"
- 한국 시각: 카카오스타일 이미준 — 미국 데이터에서 AI PM 폭증, 일반 PM 정체. "AI가 아니라 AI를 잘 쓰는 PM이 대체한다"
- 책에서의 함의: 7장은 양쪽 입장 모두 반영하되, "현재는 별도 직군화 중, 미래엔 표준이 될 가능성"으로 기록

### 논쟁 B: "FDE는 진짜 엔지니어인가, 컨설턴트인가"
- 관점 1 (진짜 엔지니어): a16z, Bloomberry, OpenAI/Anthropic 채용 공고 — production code 책임
- 관점 2 (컨설턴트의 변형): Palantir Glassdoor 일부 후기, "FDE에서 SWE로 못 간다"
- 책에서의 함의: 8장은 양쪽 다 인정하되, **"코드를 쓰는 컨설턴트, 사업을 이해하는 엔지니어"**라는 하이브리드 정체성으로 정리

### 논쟁 C: "AgentOps는 진짜 새 분야인가, MLOps의 마케팅 리브랜딩인가"
- 관점 1 (진짜 새 분야): IBM, arXiv 논문, AgentOps 도구회사들 — agent 시스템 특성이 MLOps와 다름
- 관점 2 (리브랜딩): 일부 HN/Reddit 회의론자 — "트레이싱 + 평가 = 이미 있던 것"
- 책에서의 함의: 10장은 "용어는 새로워도 기저 문제는 진짜다"로 정리. 도구 생태계 폭증이 직군화를 정당화.

### 논쟁 D: "한국에서 frontier lab과 경쟁할 수 있는가"
- 관점 1 (가능): LG AI Research EXAONE, 업스테이지, 뤼튼 등 자체 모델·서비스 보유
- 관점 2 (불가능): 스탠퍼드 AI Index OECD 35위, 인재 유출, 미국 빅테크 70% 연봉으로도 못 잡음
- 책에서의 함의: 12장은 "frontier 경쟁이 아니라 application·SI·도메인 특화에서 한국 기회 있다"로 정리. SI 빅3의 AI 전환이 기회 사례.

---

## 수집 한계

- **WebFetch 권한 제한:** 개별 HN 코멘트 페이지·Hamel Husain 블로그 본문 직접 추출 불가, WebSearch 요약만 가능. 이로 인해 일부 인용은 검색 결과 발췌 의존도가 높다.
- **Reddit 직접 검색 부분 실패:** 일부 site:reddit.com 쿼리가 결과 없음 반환. 대신 Reddit 토론을 인용한 2차 자료(Pragmatic Engineer, a16z, Sundeep Teki 글 등) 활용.
- **한국 익명 커뮤니티 토론 양 적음:** OKKY는 검색되지만 토론 깊이가 미국 Reddit에 못 미침. 회사 기술 블로그(SK Devocean, 당근, LBox 등)와 인용 가능한 Threads 글로 보완.
- **'Eval Engineer' 한국 자료 거의 전무:** 별도 직군화가 아직 안 됨. 11장은 글로벌 자료 + 업스테이지 같은 부분 사례에 의존해야 함.
- **익명 후기 검증 필요:** Glassdoor·Blind·HN 익명 발화는 모두 "검증 필요" 라벨. 책에서 인용 시 "익명 후기"로 명시 권고.

---

## 챕터 활용 가이드

| 챕터 | 핵심 자료 | 인용 우선순위 |
|---|---|---|
| 7장 AI PM | Aakash Gupta, Marily Nika, Lenny's Newsletter | epigraph #1, #11 |
| 8장 FDE | a16z, Bloomberry, Palantir Glassdoor, Pragmatic Engineer | epigraph #3, #4, #8, #14 |
| 9장 Applied AI Engineer | Swyx, Eugene Yan, Hamel Husain, dbreunig | epigraph #1, #2 |
| 10장 AgentOps | LangChain, Langfuse, IBM, arXiv 논문, 한국 영주.dev | epigraph #7 |
| 11장 Eval Engineer | Anthropic JD, Husain/Shankar, Jason Liu | epigraph #5, #6, #12, #13 |
| 12장 한국 시장 | KMJournal, 네이트, 영주.dev SI, OKKY, ZDNet, 카카오·당근·업스테이지 채용 | epigraph #9, #10, #15 |

---

## 주요 출처 모음 (URL + 한 줄 요약)

### 핵심 인플루언서/블로그
- https://www.latent.space/p/ai-engineer — Swyx "The Rise of the AI Engineer" 원조 에세이
- https://hamel.dev/blog/posts/evals-faq/ — Hamel Husain "LLM Evals FAQ"
- https://hamel.dev/blog/posts/evals/ — Hamel Husain "Your AI Product Needs Evals"
- https://eugeneyan.com/ — Eugene Yan 블로그 (Amazon Senior Applied Scientist)
- https://applied-llms.org/ — "What We've Learned From A Year of Building with LLMs" (Husain·Yan·Liu·Bischof·Frye·Shankar 공저)
- https://jxnl.co/ — Jason Liu (RAG Evals 6 framework)
- https://aakashgupta.medium.com/i-interviewed-100-ai-product-managers-heres-what-they-actually-do-9e55d393a287 — Aakash Gupta AI PM 인터뷰
- https://www.lennysnewsletter.com/p/why-ai-evals-are-the-hottest-new-skill — Lenny + Husain/Shankar 대담
- https://www.lennysnewsletter.com/p/ai-and-product-management-marily — Marily Nika AI PM 대담

### a16z (직군 정의의 표준)
- https://a16z.com/services-led-growth/ — "Trading Margin for Moat: Why FDE Is Hottest Job"
- https://a16z.com/the-palantirization-of-everything/ — Palantir 모델의 확산
- https://a16z.com/forward-deployed-job-titles/ — FDE 직무 타이틀 분석

### 채용 데이터
- https://bloomberry.com/blog/i-analyzed-1000-forward-deployed-engineer-jobs-what-i-learned/ — 1,000 FDE 채용 분석
- https://www.levels.fyi/companies/anthropic/salaries/software-engineer — Anthropic SWE 연봉
- https://www.levels.fyi/companies/openai/salaries/software-engineer — OpenAI SWE 연봉
- https://www.sundeepteki.org/forward-deployed-engineer.html — FDE 800% 성장
- https://www.teamblind.com/post/comp-for-forward-deployed-software-engineerapplied-ai-at-openai-anthropic-ycrzocbu — Blind FDE TC 토론

### 도구 비교
- https://www.langchain.com/articles/llm-observability-tools — LangChain 공식 8개 도구 비교
- https://research.aimultiple.com/agentic-monitoring/ — AIMultiple 15개 도구
- https://latitude.so/blog/best-llm-observability-tools-agents-latitude-vs-langfuse-langsmith — Latitude 비교
- https://arxiv.org/abs/2411.05285 — "AgentOps: Enabling Observability of LLM Agents" 학술 논문
- https://www.ibm.com/think/topics/agentops — IBM AgentOps 정의

### Anthropic·OpenAI 채용 공고
- https://job-boards.greenhouse.io/anthropic/jobs/4990535008 — Anthropic Research Engineer (Model Evaluations)
- https://job-boards.greenhouse.io/anthropic/jobs/5183006008 — Anthropic Senior PM (Education Labs)
- https://app.welcometothejungle.com/jobs/WNvfb_kS — Anthropic Forward Deployed Engineer JD

### 한국 자료
- https://www.youngju.dev/blog/culture/2026-03-23-si-industry-ai-transformation-career-guide — SI 빅3 AI 전환 + 엔지니어 생존 가이드 (가장 종합적)
- https://www.youngju.dev/blog/ai-platform/2026-03-09-ai-platform-llm-monitoring-langsmith-langfuse-arize — 한국 LLM 모니터링 도구 비교
- https://www.kmjournal.net/news/articleView.html?idxno=7040 — "GPU는 쌓였는데 사람이 없다"
- https://news.nate.com/view/20260105n04500 — 네이트 "텅 빈 한국 AI 두뇌"
- https://zdnet.co.kr/view/?no=20251208160526 — 2026 채용 트렌드
- https://zdnet.co.kr/view/?no=20251205105935 — SI 빅3 AX 인사 키워드
- https://devocean.sk.com/blog/techBoardDetail.do?ID=166281 — SK 에이닷 운영체계 + 프롬프트 엔지니어링
- https://devocean.sk.com/blog/techBoardDetail.do?ID=167949 — SK AI 서비스기획자를 위한 LLM 활용
- https://medium.com/lbox-team/llm-%EA%B8%B0%EB%B0%98-application-lbox-ai-%EA%B0%9C%EB%B0%9C%EA%B8%B0-e00fdcad705f — LBox AI 개발기
- https://medium.com/daangn — 당근 AI 도전기
- https://www.threads.com/@jmhong2020/post/DQSPetlEufT — 한국 대기업 AI 에이전트 채용 트렌드 분석
- https://www.smartfn.co.kr/news/articleView.html?idxno=110739 — LG CNS AI 11개 직무 채용
- https://careers.upstage.ai/ — 업스테이지 30개 직무
- https://www.aitimes.com/news/articleView.html?idxno=169900 — 뤼튼 17개 분야 + 2,000만원 보너스
- https://www.lgresearch.ai/careers — LG AI Research 채용
- https://kr.linkedin.com/company/lgairesearch/jobs — LG AI Research LinkedIn
- https://about.daangn.com/jobs/product-manager/ — 당근 PM 직무
- https://toss.im/career/jobs — 토스 채용
- https://careers.kakao.com/jobs — 카카오 채용
- https://langfuse.com/kr — Langfuse 한국어 공식 문서

### OKKY·velog (한국 익명 후기)
- https://okky.kr/articles/1327398 — "AI 엔지니어 현실 좀 알려주세요"
- https://okky.kr/articles/765754 — "엔지니어링 능력이 부족한 AI 연구원"
- https://okky.kr/articles/1462220 — 학사 출신 ML 엔지니어 커리어 고민
- https://okky.kr/articles/1344449 — 비전공자 신입 AI 솔루션 진입
- https://okky.kr/articles/667062 — ML 3년차 진로 고민
- https://velog.io/@qlgks1/%EC%B1%85-%EB%A6%AC%EB%B7%B0-LLM-%EC%97%94%EC%A7%80%EB%8B%88%EC%96%B4%EB%A7%81 — LLM 엔지니어링 책 리뷰
- https://velog.io/@dkvlg/AI-%EC%97%94%EC%A7%80%EB%8B%88%EC%96%B4-%EB%90%98%EB%8A%94-%EB%B0%A9%EB%B2%95 — AI 엔지니어 되는 방법
- https://velog.io/@imkkuk — Ollama→vLLM 4.8배 가속

### 컨퍼런스·전반
- https://www.ai.engineer/ — AI Engineer World's Fair (Swyx)
- https://podcasts.apple.com/us/podcast/latent-space-the-ai-engineer-podcast/id1674008350 — Latent Space 팟캐스트

### 기타 산업 분석
- https://www.cio.com/article/4167981/anthropics-financial-agents-expose-forward-deployed-engineers-as-new-ai-limiting-factor.html — Anthropic 금융 agent + FDE 한계
- https://newsletter.pragmaticengineer.com/p/forward-deployed-engineers — Pragmatic Engineer FDE 종합
- https://www.dbreunig.com/2025/08/21/a-guide-to-ai-titles.html — AI 직무 타이틀 가이드
