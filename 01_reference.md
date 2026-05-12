# 코드 너머의 직업들 — 통합 레퍼런스

> 본 문서는 web·paper·community 세 갈래 리서치를 챕터 단위로 재조직한 *본문 저술용 1차 자료집*이다.
> 전체 풀버전은 `research/web.md`, `research/papers.md`, `research/community.md`에 있다. 이 문서는 *어떤 자료를 어느 챕터의 어느 자리에 어떻게 쓸지*에 집중한다.
>
> 작성일: 2026-05-10. 수집 기준 시점: 2026 Q2.
> 산출 구조: ① 책 가설과 자료의 정합 ② 챕터별 사용 매핑(프롤로그~14장+에필로그) ③ 5개 직업 deep dive ④ 한국 시장 자료 ⑤ 균형 점검(반론) ⑥ Epigraph 모음 ⑦ 검증 필요 항목 ⑧ 한계.

---

## 0. 책의 핵심 가설과 자료가 어떻게 뒷받침하는가

**가설:** *PC·인터넷·모바일이 그랬듯, AI 인프라 다음에 새로운 소프트웨어 회사와 새로운 직업이 자란다. 그리고 그 사람들은 우리가 알던 직업과는 다른 모양을 하고 있다.*

이 가설은 세 갈래로 검증된다.

| 가설 구성요소 | 강력한 자료 | 균형/반론 자료 |
|---|---|---|
| **인프라가 깔리면 시차를 두고 응용이 자란다** | Carlota Perez 2002 (Installation→Deployment), Bresnahan-Trajtenberg 1995 (GPT 보완재 이론), Paul David 1990 (40년 전기화 시차) | Acemoglu 2024 (10년 TFP ≤0.66%) |
| **시차는 매번 짧아져 왔다 (PC 14년 → 모바일 5~6년 → AI ?년)** | web 자료 1-A~1-L (PC/Internet/Mobile timeline 좌표), Brynjolfsson-Li-Raymond 2023 (콜센터 +14%, 신입 +34%) | Anthropic Economic Index 5차 (22~25세 신입 채용 -14%) |
| **새 직업이 등장한다** | Autor 외 2024 (2018 직업의 60%+가 1940년에 부재), LinkedIn (AI Engineer +143.2%), 5개 직업의 실무자 발화·채용 데이터 | Acemoglu-Restrepo 2019 (지난 40년 reinstatement effect 약화), Cemri 외 2025 (다중 에이전트 41~87% 실패) |

이 표가 책 전체의 *지렛점*이다. 13장 결론에서 균형 자료를 정직하게 다루는 것이 책의 신뢰성 차별점이 된다.

---

## 1. 챕터별 사용 매핑

> 각 챕터마다 ① 도입(epigraph/풍경) ② 핵심 데이터 ③ 학술 백킹 ④ 한국 자료 ⑤ 균형 자료를 명시한다.
> 깊은 원문은 `research/web.md` §1-A 식의 좌표로 표기.

---

### 프롤로그 — 풍경이 닮아 있다

**도입 풍경(2010 모바일 ↔ 2025 AI 평행):**
- 2010년: Qualcomm/ARM이 끌고, 모바일 소프트웨어는 보이지 않던 시기 → 2014~15 Uber·Airbnb·Instagram·WhatsApp 폭발 (`web §1-J`)
- 2025년: Nvidia 시총 $5.23T (`web §2-A`), SaaS 멀티플 평균 회귀 (`web §2-B`)

**Epigraph 후보:** Steve Jobs 2007년 1월 키노트 *"An iPod, a phone, and an Internet communicator. These are not three separate devices. This is one device."* (`web §1-H`)

**한 줄 요약 핵심 인용:** Satya Nadella, BG2 팟캐스트 2024-12-12 — *"SaaS is dead."* (`web §2-D`)

---

### 1장. 반도체는 늘 먼저 갔다 — PC·인터넷·모바일의 같은 순서

**핵심 데이터(시차 정리표 — 책의 시각화 자산):**
| 시대 | 인프라 깔린 시점 | 시장 지배자 등극 | 시차 |
|---|---|---|---|
| **PC** | 1981 (IBM PC + Intel 8088, $1,565) | 1993 (MS > IBM 시총) ~ 1995 (Windows 95 첫해 4,000만 카피) | **12~14년** |
| **Internet** | 1995~96 (Cisco/Sun 폭증, Netscape IPO) | 2004 (Google IPO $85) ~ 2006 (AWS S3) | **9~11년** |
| **Mobile** | 2007 (iPhone) ~ 2008 (App Store, 첫 주말 1,000만 다운로드) | 2012~13 (스마트폰 보급률 50%, FB 모바일 광고 50%) | **5~6년** |
| **AI** | 2022 (ChatGPT) ~ 2024 (1M context, capex $200B+) | 2027~2030? | (예측) |

원좌표: `web §1-A ~ §1-L`, `web §X-B`.

**학술 백킹:**
- Carlota Perez 2002, *Technological Revolutions and Financial Capital*: Installation phase(약 20년: Irruption + Frenzy) → Turning Point → Deployment golden age(약 30년). AI는 지금 Installation 후반(Frenzy). [PDF](http://pombo.free.fr/carlota2002.pdf) (`papers §논문 1`)
- Bresnahan & Trajtenberg 1995, *General Purpose Technologies*: GPT 가치는 보완재에서 발생. NBER W4148. (`papers §논문 2`)
- Paul David 1990, *The Dynamo and the Computer*: 1881 발전기 → 1920년대 공장 생산성 폭증, 약 40년 시차. AER 80(2). (`papers §논문 3`)
- Autor 외 2024, *New Frontiers* QJE 139(3): **2018년 미국 직업의 60%+가 1940년에 존재하지 않음.** 새 직업의 역사적 패턴. (`papers §논문 10`)

**Epigraph 후보:** Perez 2002 — *"It is during the Deployment Period — after the major financial collapse — that the full social and economic potential of the new technologies can be realized."*

**책의 핵심 메시지(이 장):** "한 번이면 우연, 두 번이면 패턴, 세 번이면 법칙. AI는 네 번째다."

---

### 2장. 시차는 점점 짧아진다 — 그리고 AI는 더 빠르다

**핵심 데이터:**
- 미국 스마트폰 보급률 50% 돌파: 2012~13년 사이 (Pew Research, `web §1-K`)
- Facebook 모바일 광고 비중 분기별: 2012 초 0% → Q3 14% → Q4 23% → 2013 Q1 30% → Q2 41% → 2013 말 ~50% (`web §1-L`)
- iPhone 2007/01 → Uber 2009 등록, Airbnb 2008/08 창업, Instagram 2010/10 출시, WhatsApp 2009/01 (`web §1-J`)

**시차 단축 메커니즘 학술:**
- Brynjolfsson, Rock & Syverson 2021, *The Productivity J-Curve*: 무형자본 보정 시 TFP 수준 +15.9%. AEJ:Macro 13(1). 시차의 정량 메커니즘. (`papers §논문 4`)
- Brian Arthur 1989, *Lock-In*: 채택률이 표준을 만든다. EJ 99. (`papers §논문 5`)
- Geoffrey Moore 1991/2014, *Crossing the Chasm*: early adopters → early majority의 골. (`papers §논문 6`)

**AI 시차 가속 정량:**
- Brynjolfsson, Li & Raymond 2023, *Generative AI at Work* NBER W31161: 5,179명 콜센터 RCT. **+14% 평균, 신입 +34%.** 신입의 숙련자 따라잡는 시간 압축. (`papers §논문 7`)
- Dell'Acqua 외 2023, *Navigating the Jagged Technological Frontier* HBS WP 24-013: 758 BCG 컨설턴트 RCT. Frontier 안 +12.2% 완료 / +25.1% 속도 / +40% 품질, 바깥 -19%p. (`papers §논문 9`)

**균형/반론:** Acemoglu 2024 — TFP 10년 ≤0.66%, 거시 효과는 미미. 거시 낙관에 베팅하지 말 것. (`papers §논문 8`)

---

### 3장. 우리는 지금 어디쯤 와 있나 — Nvidia 신고가, SaaS 회귀, 채용 시장의 신호

**핵심 데이터(2025~26 시장 신호 패키지):**
- **Nvidia 시총:** 2024/06 $3T → 2025/07 $4T → **2025/10 세계 최초 $5T** → 2026/05 약 $5.23T. 데이터센터 칩 매출 점유율 81% (IDC). (`web §2-A`)
- **SaaS 멀티플 압축 (BVP Cloud Index):** 공개 SaaS 평균 EV/Revenue 7.5~8x. Cloud 100 사모 평균 26x → 23x → 20x (3년 연속 하락). 2021 정점 대비 41% ↓. (`web §2-B`)
- **"AI Wrappers" 멀티플 붕괴**, 리텐션 무너짐 (BVP). 상위 25%만 NRR 강한 40%+ 성장. (`web §2-B`)
- **2025년 가격 모델 전환:**
  - HubSpot — Breeze Prospecting Agent: "qualified lead 1건당 $1"로 전환
  - ServiceNow — AI add-on 폐지, 3-tier로 단순화 (AI 무료 번들)
  - Salesforce — Enterprise/Unlimited 6% 인상 (Agentforce 가치)
  - Atlassian — Rovo AI 무료 번들 (`web §2-C`)
- **"SaaS is dead":** Satya Nadella, BG2 팟캐스트 2024-12-12. JPMorgan: *"Software Collapse Broadens with Nowhere to Hide"*. Jefferies 신조어: *"SaaSmageddon"*. (`web §2-D`)

**채용 시장 신호:**
- LinkedIn (Stanford AI Index 2025 ch.4): 2024 GenAI 명시 채용 16,000 → 66,000건(4배+). LLM 5,000 → 20,000, prompt eng 1,400 → 6,300. (`papers §논문 15`)
- LinkedIn Future of Work: AI Engineer 채용 +143.2%(3년), Prompt Engineer +135.8%. 2030년까지 핵심 스킬 70% 변화. (`papers §논문 22`)
- WEF Future of Jobs 2025: 2030까지 순 +7,800만 일자리, AI 직군 신규 +1,100만 / 대체 +900만. (`papers §논문 14`)

**균형/반론:** 
- Cisco 닷컴 정점 시총 $569B (2000/03/27) → 90% 손실 → **25년 만에 2025/12에야 회복.** (`web §1-F`) → "지난 시대의 인프라 챔피언이 영원하지 않았다"는 톤 환기. NVIDIA와의 비교 분석은 본문에 반드시 한 번 언급.
- Anthropic Economic Index 5차(2026-03): 22~25세 노출 직업 진입 신입 구직률 -14%. (`papers §논문 12`)
- ILO 2025 WP140: 전 세계 노동자 25%가 어느 정도 GenAI 노출, 그러나 **transformation > replacement**. 고소득국 34% vs 저소득국 11%. (`papers §논문 13`)

---

### 4장. GPU와 데이터센터가 가능하게 한 것들 — 길이·속도·비용

**길이 (컨텍스트 윈도우):**
| 시점 | 모델 | 컨텍스트 |
|---|---|---|
| 2022/11 ChatGPT 출시 | GPT-3.5 | 4K |
| 2023/03 | GPT-4 | 8K~32K |
| 2023/11 | Claude 2.1 | 200K |
| 2024 초 | Gemini 1.5 Pro | **1M** (최초 GA) |
| 2026 초 | Claude Opus 4.6/Sonnet 4.6, GPT-5.4 | 1M GA |

3년 만에 4K → 1M = **250배.** (`web §3-B`)

**속도(throughput):**
- Cerebras CS-3 wafer-scale: Llama 3.1 8B ~1,800 tok/s, 70B ~450 tok/s, **405B 969 tok/s** (frontier 규모로는 처음). GPU 대비 약 20배 (Artificial Analysis 독립 벤치마크). (`web §3-D`)
- Groq LPU: Llama 2 70B 241 tok/s, TTFT 강점 (deterministic 컴파일러).

**비용:**
- GPT-4 출시 가격(2023/03): $30/$60 per 1M tokens.
- "GPT-4 수준 능력"의 가격: 2023 초 ~$30/1M → 현재 **$1 미만/1M.**
- Epoch AI 분석: 성능 마일스톤별 가격 하락 9~900배/년. **중앙값 연 50배 → 2024년 1월 이후 가속 200배.** (`web §3-C`)
- Cisco-Cerebras 인용: *"The fastest trends (e.g. 900x per year) start after January 2024."*

**capex 규모:**
- 4대 하이퍼스케일러(MS+Meta+Google+Amazon) 합산:
  - 2024: ~$200~210B
  - 2025: ~$410B (전년 대비 ~2배)
  - **2026: $725B 예상** (+77%)
- Microsoft FY2026 capex $190B. Q4 단독 $40B+. Azure 연 매출 $75B 돌파, 34% 성장. 70개 리전, 400+ 데이터센터. (`web §3-A`)

**Epigraph 후보:** Fortune 표제 — *"Big Tech is about to spend $700 billion on AI this year. No one knows where the buildout ends."*

**책에서의 사용:** 4장은 *기술 카탈로그가 아니라 일감의 원료*로 본다. "길이가 만든 일 = 5장 에이전트, 비용이 만든 일 = 11장 Eval"의 다리 놓기.

---

### 5장. 에이전트가 일을 한다는 것 — 도구가 아니라 동료에 가까운

**학술 표준어:**
- Wang 외 2023, *A Survey on LLM-based Autonomous Agents* arXiv:2308.11432: 4모듈 프레임워크 — **Profile / Memory / Planning / Action.** (`papers §논문 16`)
- Huang 외 2024, *Understanding the Planning of LLM Agents* arXiv:2402.02716: 5개 분류(Task Decomposition, Plan Selection, External Module, Reflection, Memory). (`papers §논문 17`)

**현실 데이터(반드시 같이):**
- Cemri 외 2025, *Why Do Multi-Agent LLM Systems Fail?* arXiv:2503.13657 (UC Berkeley): 7개 SOTA 오픈소스 MAS의 **41~86.7% 실패율.** 14개 실패 모드 / 3개 카테고리(MASFT). 인터-어노테이터 카파 0.88. (`papers §논문 18`)

**책의 메시지:** "에이전트는 *도구→어시스턴트→동료에 가까운 존재*로 올라왔다. 그러나 80% 망가져 있다. 그래서 *옆에 운영하는 사람*이 직업이 된다(10장)."

**Epigraph 후보:** Galileo AI — *"Hallucinations are not just a model problem. In production, they are a system design problem."* (`community §1-4`)

---

### 6장. 새로운 비즈니스 모델 — 시트당 과금에서 결과물 과금까지

**결과물 과금 사례 (book 본문에 직접 인용 가능 데이터):**
- **Intercom Fin:** $0.99 per outcome. 한 대화에서 여러 질문 답해도 1회만 과금. *"You only pay when Fin delivers value."* (`web §4-A`)
- **Zendesk Resolution Platform** (2024/08, CX 업계 최초 outcome-based):
  - 1~100건 $1.50/건
  - 101~1,000건 $1.30
  - 1,001~5,000건 $1.10
  - 5,001건+ $1.00
  - pay-as-you-go $2.00. AI가 사람에 에스컬레이션하면 무과금. (`web §4-B`)
- **Sierra (Bret Taylor 공동창업):** 2024/02 출시 → 2025/11 ARR $100M → 2026/02 ARR $150M+ → **2026/05 valuation $15.8B (raise $950M).** Outcome 단위 과금: 해결, 해지 만회, 업셀 완료. (`web §4-C`)
- **Klarna AI(2024/02 OpenAI 협업):** 첫 1개월 230만 건 = CS 2/3 = **풀타임 700명분 일감.** 평균 해결 11분 → 2분 미만(82%↓). 2024 이익 +$40M. **단, 2025 후반 사람 CS 재채용:** *"We focused too much on efficiency and cost. The result was lower quality."* (`web §4-E`)

**시장 데이터:**
- Bessemer 2026 AI Pricing Playbook(200+ AI 벤더): 하이브리드 가격 채택률 27% → 41%. 순수 시트 모델 21% → 15%. (`web §4-D`)
- Battery Ventures: *"Software shifts from aiding human productivity to autonomously completing work."* (`web §X-A`)
- 시트 고수 AI 회사 = gross margin 40%↓, churn 2.3배↑ (`web §X-A`)

**AI 회사 매출 구조 일람:**
- **OpenAI:** 2026/04 월 $2B = 연 $24B. 엔터프라이즈 30% (2025) → 40%+ (2026).
- **Anthropic:** 2025말 $9B → 2026/03 $19B → 현재 ~$30B (검증 필요). 컨슈머 거의 없음, 엔터프라이즈+클라우드 파트너십.
- **Cursor (Anysphere):** 2025/01 $100M → 2026/02 $2B (3년 만에 0→$2B, B2B 사상 최단). 2026/04 valuation $50B 협상.
- **Perplexity:** 2025 $200M → 2026 목표 $650M. (`web §4-F`)

**책에서의 사용:** 6장은 *직업의 KPI*가 어떻게 바뀌는지의 토대. "기능 출시 수"에서 "결과물 단가 절감"으로의 이동을 7장(AI PM)·11장(Eval)이 직접 받는다.

---

### 7장. AI Product Manager — 모델을 제품으로 만드는 사람

**일과 묘사 (community §1-1):**
- "전통 PM이 백로그를 관리하면, AI PM은 **모델 학습 사이클·평가 프레임워크·AI 안전 프로토콜**을 관리한다." (Aakash Gupta)
- PRD → **evals(평가셋)이 사양서**. 분기 로드맵 → continuous experimentation. 결정론 → 확률적.

**비교표 (커뮤니티 합의):**
| 항목 | 전통 PM | AI PM |
|---|---|---|
| 사양 | PRD | Evals |
| 사이클 | 분기 로드맵 | 연속 실험 |
| 시스템 | 결정론적 | 확률적 |
| 책임 | 기능 출시 | + 모델 안전·드리프트 |
| 메트릭 | DAU·전환율 | + hallucination rate, factuality |

**Epigraph 후보 (강도 순):**
- Hamel Husain — *"Evals replace traditional PRDs for AI products."*
- Aakash Gupta — *"AI PMs are making $300K+ while regular PMs get laid off."*
- Marily Nika (Lenny's Newsletter) — *"Every PM will be an AI PM. This is not a separate role — it is the new default."*

**학술 백킹:**
- Vu & Oppenlaender 2025, *Prompt Engineer Skill Requirements* arXiv:2506.00058: 채용 공고에서 AI 지식 22.8%, 프롬프트 디자인 18.7%, 커뮤니케이션 21.9%, 창의적 문제해결 15.8%. (`papers §논문 23`)

**한국 매핑:** 명시적 'AI PM' 타이틀은 아직 드묾. 토스·당근 PM 직무에 AI 활용이 통합되는 형태. 카카오스타일 PM 이미준 분석: 미국 데이터에서 AI PM 폭증, 일반 PM 정체. *별도 직군화는 1~2년 후 예상*. (`community §3-B-1`)

**논쟁점:** "AI PM은 별도 직군인가, PM의 새 표준인가" — 본문에서 양쪽 입장 모두 반영. (`community §논쟁 A`)

---

### 8장. Forward Deployed Engineer — 고객 현장에서 모델을 다듬는 사람

**Bloomberry 1,000건 채용 분석 (`community §1-2`):**
- 고객과 직접 협업 **55%** (1순위)
- AI/ML 시스템 빌드/배포 37% (2순위)
- 시스템·API 통합 32% (3순위)
- **매출 책임 명시 0%** — 영업 직무가 아니라는 강력한 신호
- 채용 공고 **+1,165% YoY**

**원조 (Palantir):**
- 2011년 Palantir가 solutions engineer + integration engineer를 묶어 새 타이틀 **Forward Deployed Engineer** 부여. 'Deltas'(Delta Force) 별명.
- a16z — *"The hottest job in startups."*

**보상:**
- 일반 시장 중앙값 $173,816 (`community §2`)
- OpenAI/Anthropic mid-senior **$350K~$550K**
- Palantir staff급 $630K+

**그림자 면 (균형):**
- Palantir Glassdoor: 워라밸 2.5/5, 보상 4.2/5. 익명 후기 — *"Burnout happens eventually to all FDEs."* / *"FDE에서 SWE로 전환한다는 약속? 거짓말이었다."*
- HN 11647103: "engineering mill/sweatshop" (검증 필요, 다수 추천)

**Epigraph 후보:**
- a16z — *"We took our solutions engineers and called them Deltas — like Delta Force. It sounded ridiculous, and it worked brilliantly."*
- Bloomberry — *"Forward deployed engineer jobs exploded by 1,165% year-over-year."*

**한국 매핑:** 정확한 'FDE' 타이틀은 거의 없음. **SI 빅3가 "AI 컨설턴트 + 솔루션 아키텍트" 형태로 분리·재조합 중.** LG CNS — AI Tech 컨설턴트, AI Service Design 컨설턴트, AI 솔루션 아키텍트, AI 어플리케이션 개발자 등 11개 직무. **연말까지 1,000명 확보 목표.** 삼성SDS — AI 컨설팅 직군. 업스테이지 — AI Customer Engineer, AI Solution Architect. (`community §3-B-2`)

**논쟁점:** "FDE는 진짜 엔지니어인가, 컨설턴트인가" → 본문은 **"코드를 쓰는 컨설턴트, 사업을 이해하는 엔지니어"** 하이브리드 정체성으로 정리. (`community §논쟁 B`)

---

### 9장. Applied AI Engineer — 백엔드·풀스택 개발자의 자연스러운 다음 자리

**원조 인용 (Swyx, Latent Space 2023, 지금도 가장 자주 인용됨):**
> *"5년 걸리던 AI 작업이 API 문서와 한가한 오후 한 번이면 가능해졌다. Andrej Karpathy도 동의했다. 수학적으로, AI Engineer는 ML Engineer보다 10배 많아질 것이다."*
> https://www.latent.space/p/ai-engineer

**비교 (드라이 정리):**
> "Data Scientists answer questions. ML Engineers build systems. **AI Engineers ship products.**" — Drew Breunig 2025

| 항목 | ML Engineer | Applied AI Engineer |
|---|---|---|
| 초점 | 모델 레이어 | 애플리케이션 레이어 |
| 일상 | 학습 파이프라인·feature store | RAG·prompt·evals·orchestration |
| 산출물 | 모델 가중치 | 작동하는 제품 |
| 출신 | 통계·박사 다수 | 시니어 풀스택 다수 |

**채용 신호:**
- LinkedIn: **AI Engineer 채용 +74% YoY vs ML Engineer +33%** (Howdy 분석)
- 미국 base 평균 $145K~$190K, frontier lab 시니어 $600K~$1M+ (Levels.fyi)
- 한국 키워드 패턴: **RAG + LangChain + LLMOps + 평가**가 거의 모든 공고에 등장

**한국 매핑 (가장 활발):** 카카오 ML Engineer (LLM/Search), 네이버 AI Challenge, 토스 ML Engineer, 당근 2026 ML 직군 (피드 품질·광고추천·LLM 개인화), 업스테이지 AI Research Engineer (LLM Evaluation), LG AI Research EXAONE Lab, 뤼튼 17개 분야(합격 보너스 2,000만원). (`community §3-B-3`)

**Epigraph 후보:**
- Swyx — *"5년 걸리던 작업이 API 문서와 한가한 오후로 가능해졌다."*
- Drew Breunig — *"Data Scientists answer questions. ML Engineers build systems. AI Engineers ship products."*

---

### 10장. Agent 운영자 / AgentOps — 책의 시그니처

**용어 정착 신호:**
- IBM Think (2025): *"AgentOps — agent operations — is an emerging set of practices focused on the lifecycle management of autonomous AI agents, bringing together principles from DevOps and MLOps."*
- 학술: arXiv:2411.05285 *"AgentOps: Enabling Observability of LLM Agents"* (2024/11). **용어가 산업·학술 양쪽에서 동시 등장.**
- IBM 추정 시장: 2024 $5B → 2030 $50B.

**도구 생태계 (10장 시그니처 보강):**
| 도구 | 라이선스 | 핵심 차별화 | 도입 패턴 |
|---|---|---|---|
| LangSmith | 상용 SaaS | LangChain 통합, 오버헤드 미미 | 빠른 도입 |
| **Langfuse** | OSS (MIT) + Cloud | 셀프호스팅, 프롬프트 관리 | **데이터 주권 중시 (한국에서 가장 활발)** |
| Helicone | 상용 + OSS | URL 한 줄 변경 (proxy) | 스타트업 |
| Arize Phoenix | OSS + Enterprise | SOC 2/HIPAA, eval rigor | 엔터프라이즈 |
| W&B Weave | 상용 | 기존 W&B 통합 | 전통 ML 팀 |
| Braintrust | 상용 | eval-first | 평가 중심 |
| AgentOps(도구) | 상용 | 시간여행 디버깅, 멀티에이전트 시각화 | 복잡한 agent 시스템 |

핵심 시장 신호: **Langfuse가 2026/01 ClickHouse에 인수.** OSS는 그대로 유지.

**책 가설을 뒷받침하는 결정적 학술:**
- Cemri 외 2025 (위 5장 자료 재활용): SOTA 다중 에이전트 41~86.7% 실패. 14개 실패 모드. **이 직업이 왜 필요한지의 학술 토대.**
- Zheng 외 2023, *LLM-as-a-Judge* NeurIPS 2023 (arXiv:2306.05685): GPT-4 judge ↔ 인간 80%+ 일치. 단 4대 편향(position, verbosity, self-enhancement, 제한된 추론). (`papers §논문 19`)

**Epigraph 후보:**
- Galileo AI — *"Hallucinations are not just a model problem. In production, they are a system design problem."*
- 영주.dev (한국) — *"프롬프트는 더 이상 코드 안에 하드코딩되지 않는다. 대시보드에서 비개발자가 수정한다."*

**한국 매핑:** 'AgentOps Engineer' 정확한 타이틀 거의 없음. SK Devocean 에이닷 운영팀(프롬프트 엔지니어링·운영체계 50% 감축, 발화 작업량 3배). LangSmith — SKT 강의(sudormrf.run 후기). Langfuse — 한국어 공식 문서, 셀프호스팅 활발. PyTorch KR 토론. 영주.dev "한국 LLM 모니터링 도구 비교"가 종합 출처. (`community §3-B-4`, §4)

**검증 필요한 가설:** AgentOps는 MLOps가 그랬던 것처럼 1~2년 안에 정식 직군화. 지금은 LLMOps·AI Platform Engineer로 분산.

**책의 톤:** 10장은 분량(30쪽)·핵심성·신선함에서 책의 무게중심. 한국 독자가 가장 적게 알지만 가장 빨리 자라는 자리.

---

### 11장. Eval Engineer · AI Reliability — 품질을 측정하고 책임지는 사람

**Anthropic 채용 공고 직접 인용 (`community §1-5`):**
- "evaluation 플랫폼 설계·구현"
- "novel evaluation methodologies — reasoning, safety, helpfulness, harmlessness"
- "high-throughput evaluation pipelines that run during production training"
- "evaluation results를 분석해 failure mode 식별, training 결정에 영향"
- 요구: ML 평가 시스템 + distributed computing
- 출처: https://job-boards.greenhouse.io/anthropic/jobs/4990535008

**Hamel Husain & Shreya Shankar (Maven AI Evals 4,500+명 수료):**
> *"We spent 60-80% of our development time on error analysis and evaluation. Most effort goes toward understanding failures rather than building automated checks."*
> *"Teams jump straight to building LLM judges or dashboards without knowing what they're measuring. Error analysis is not optional — it's the foundation. Skip it and everything else is built on sand."*

**기존 직무 비교:**
- vs QA Engineer: 결정론적 테스트 → 확률적·통계적 measurement
- vs ML Researcher: 새 모델을 만들지 않고 *측정*만 한다
- vs Test Engineer: 정답이 없는 문제 — *"정답"을 정의하는 것 자체가 일*

**학술 토대 (책의 차별점):**
- Zheng 외 2023, LLM-as-Judge: GPT-4 ↔ 인간 80%+ 일치, 4대 편향. (`papers §논문 19`)
- Deng 외 2024, *Investigating Data Contamination* NAACL/arXiv:2311.09783: GPT-4 MMLU 정확히 맞춤(메모리화 추정) **57%**, ChatGPT 52%. *"general reasoning이 아닌 암기"*. (`papers §논문 20`)
- Liang 외 HELM, TMLR 2023 (arXiv:2211.09110): 16 시나리오 × 7 메트릭. 단일 점수 한계 폭로. (`papers §논문 21`)
- Cemri 외 2025 (재활용): 다중 에이전트 41~87% 실패.

**Epigraph 후보:**
- Hamel Husain — *"Error analysis is not optional. Skip it and everything else is built on sand."*
- Husain & Shankar — *"We spent 60-80% of our development time on error analysis and evaluation."*
- Lenny's Newsletter 제목 — *"Evals are the hottest new skill for product builders."*

**한국 매핑:** **거의 없음.** 가장 늦게 들어올 직군. 가까운 형태: 업스테이지 "AI Research Engineer (LLM Evaluation)" — 영문 표기로만 등장. 카카오·네이버는 ML Engineer 직무에 평가 책임이 포함됨. → 11장은 *글로벌 자료 + 부분 한국 사례*에 의존. (`community §3-B-5`)

---

### 12장. 한국 시장에서 이 흐름은 어떻게 다른가

**인력난의 명백한 신호 (한국어 헤드라인급):**
- 고용노동부·한국직업능력연구원: **2023~2027 AI 분야 12,800명 부족** (클라우드 추가 18,800명)
- 국내 AI 기업 2,354곳 중 **81.9%가 인력 부족 호소**
- 스탠퍼드 AI Index 2025: 한국 AI 인재 순유출 -0.36/만명, **OECD 38개국 중 35위 (최하위권)**
- KMJournal: *"수백억 원 인프라를 깔아놨지만 LLM 고도화 수석 엔지니어를 수개월째 못 구한다."*

**Epigraph 후보 (헤드라인급 한국어):**
- KMJournal — **"GPU는 쌓였는데 사람이 없다."** (12장 도입 결정적)
- 네이트 뉴스 (2026/01/05) — **"다룰 사람이 없다 — 텅 빈 한국 AI 두뇌."**
- 영주.dev — **"AI 시대의 SI 엔지니어는 '코더'에서 'AI 오케스트레이터'로 변화한다."**

**한국 SI 산업의 AI 전환 (12장의 가장 풍부한 자산):**
- 영주.dev "SI 산업의 AI 대전환" (2026/03/23) — Gartner: 2028까지 SI 프로젝트 80%의 코딩 작업이 AI 자동화.
- 삼성SDS 풀스택 AI 아키텍처(인프라→플랫폼→앱→컨설팅), AI 관련 SI 비중 2026 40%+ 전망
- **SI 엔지니어 진화 로드맵 (영주.dev 정리):**
  - 2020-2024: **코더**
  - 2025-2027: **AI 활용 개발자**
  - 2028-2030: **AI 오케스트레이터**
- ZDNet Korea (2025/12): "삼성SDS·LG CNS·SK C&C, 인사 키워드는 'AX'… 전략은 '동상이몽'"
- ZDNet Korea (2025/12/08): "2026 채용 트렌드: 4~7년차 경력직 + AI 활용 인재 더 뽑는다."

**5개 직군의 한국 매핑 — 한 표:**

| 직군 | 한국에서의 모습 | 정확한 타이틀 등장 정도 | 주요 회사 |
|---|---|---|---|
| AI PM (7장) | PM 직무에 AI 활용이 통합되는 형태 | 거의 없음 (1~2년 후 예상) | 토스, 당근, 카카오스타일 |
| FDE (8장) | "AI 컨설턴트 + 솔루션 아키텍트"로 분리·재조합 | 정확한 타이틀 거의 없음, SI 빅3에서 빠르게 자람 | LG CNS(11개 직무), 삼성SDS, 업스테이지(AI Customer Engineer) |
| Applied AI Eng (9장) | **가장 활발**, 다양한 타이틀 | "ML Engineer (LLM)" / "AI 엔지니어" / "AI 응용 엔지니어" | 카카오, 네이버, 토스, 당근, 업스테이지, LG AI Research, 뤼튼 |
| AgentOps (10장) | 별도 직군 거의 없음, 운영팀이 사실상 수행 | 정확한 타이틀 거의 없음 | SK 에이닷, Langfuse 셀프호스팅 사례 다수 |
| Eval Eng (11장) | **거의 없음**, 가장 늦게 들어올 직군 | 영문 표기로만 등장 (업스테이지) | 업스테이지, 카카오·네이버는 ML Engineer 책임 통합 |

**왜 한국 자료가 적은가 (5가지 진단, 본문에 인용):**
1. 직군이 1~2년 늦게 정착
2. 영문 표기 차이 (같은 일을 다른 이름으로 부름)
3. 회사 블로그 위주, 익명 커뮤니티 토론 양 적음
4. 인재 유출 (스탠퍼드 OECD 35위) — 실력자가 글을 안 씀
5. SI 빅3가 'AI 컨설턴트' 형태로 만들고 있으나 명칭 미정착

**12장 결론 가설:** "frontier 경쟁이 아니라 application·SI·도메인 특화에서 한국 기회 있다." SI 빅3의 AI 전환이 핵심 사례. (`community §3-C, §논쟁 D`)

---

### 13장. 어디서 어디로 — 백엔드·프론트·PM·SI 컨설턴트별 전환 경로

**현직 → 새 직군 매핑 (책 전체에서 가장 자주 들춰볼 페이지):**
| 현직 | 가장 가까운 새 직군 | 두 번째 후보 | 학습 갭 |
|---|---|---|---|
| 백엔드/풀스택 | **Applied AI Eng** | Agent 운영자 / FDE | 비결정성·evals·비용 모니터링 |
| 프론트엔드 | AI PM | Applied AI Eng (UI 영역) | 모델 사고·실험 사이클 |
| PM/기획자 | **AI PM** | FDE (도메인이 강하면) | evals·통계·실험 |
| SI 컨설턴트/SA | **FDE** | AI PM | 직접 코드, RAG·LangChain |
| QA/플랫폼/SRE | **Eval Eng / Agent 운영자** | Applied AI Eng | 통계적 측정·LLM-as-judge |
| 데이터 엔지니어/분석가 | Eval Eng | AI PM | LLM·distributed |

**자가진단 체크리스트 (15문항)** — 본문 작성 시 직접 작성. 자료의 적합도 항목들이 토양:
- "비결정성을 다룬다" / "고객 사무실에 6개월 살 수 있다" / "통계적 직관 강하다" / "패턴 추적 끈기" / "야간 알림에 침착하다" 등.

**전환 사례 (인터뷰 후보):** 영주.dev SI 엔지니어 (한국), Eugene Yan (Amazon Senior Applied), Hamel Husain (Parlance Labs), Marily Nika (Lenny's Newsletter PM 대담).

**책 가설을 *반박*하는 자료(13장 결론 정직성용):**
| 반박 포인트 | 출처 |
|---|---|
| AI 거시 효과 미미 (TFP 10년 ≤0.66%) | Acemoglu 2024 |
| 신직무는 변형 < 변형 (transformation 우세) | ILO 2025 WP140 |
| 신입 진입 -14% | Anthropic Economic Index 5차 |
| Reinstatement effect 지난 40년 약화 | Acemoglu·Restrepo 2019 |
| AI는 frontier 바깥 -19%p | Dell'Acqua 2023 |
| 다중 에이전트 41~87% 실패 | Cemri 2025 |
| LLM 평가 50%+ 메모리화 | Deng 2024 |

이 7가지를 13장에서 정직하게 다뤄야 책이 *현실주의 가이드*가 된다.

---

### 14장. 다음 5년을 준비하는 90일 플랜

**자료 토양 (휴리스틱 5가지, `community §휴리스틱`):**
1. *측정할 수 없으면 만들지 마라* (Hamel Husain) — error analysis 60-80% 시간
2. *AI 도입 4단계*: 트레이싱 → 비용 → 자동평가 → 프롬프트 관리 (영주.dev)
3. *FDE 채용에 매출 책임 있으면 영업이다* (Bloomberry)
4. *RAG + LangChain + 평가는 한국 응용 엔지니어 표준 공통분모*
5. *오픈소스 셀프호스팅이 한국 엔터프라이즈 기본 입찰* (Langfuse 활성도)

**한국 커뮤니티 진입 자원 (네트워킹 트랙):**
- 영주.dev (SI 전환·LLM 모니터링 종합)
- SK Devocean (실무 사례)
- velog/qlgks1, dkvlg, imkkuk, yaza
- OKKY 5선 (위 community §3-D)
- AI Engineer World's Fair (Swyx)
- Latent Space 팟캐스트
- PyTorch KR 디스코드

**90일 일정표 골격(본문 작성 시 직접 채울 것):** 학습·만들기·쓰기·네트워킹의 4트랙 × 30/60/90일.

---

### 에필로그 — 다음 단계는 곧 도착한다

**한 줄 회수:** "반도체는 먼저 갔고, 사람은 따라간다. 그리고 사람의 자리는 새로 만들어진다."

**Epigraph 후보:** Autor 외 2024 — *"More than 60 percent of employment in 2018 is found in job titles that did not exist in 1940."*

---

## 2. 5개 직업 deep dive 비교표 (본론 7~11장 통일 포맷의 자료원)

| 직군 | 시그니처 인용 | 채용 데이터 | 학술 백킹 | 한국 자리 |
|---|---|---|---|---|
| **AI PM (7장)** | "Evals replace traditional PRDs" — Husain | LinkedIn AI PM 폭증 / $300K+ trajectory | Vu & Oppenlaender 2025 (skill 분석) | 토스·당근, 별도 직군화 1~2년 후 |
| **FDE (8장)** | "Forward deployed jobs +1,165% YoY" — Bloomberry | OpenAI/Anthropic mid-senior $350~550K, FDE 일반 $174K | Dell'Acqua "jagged frontier" 능력 | LG CNS 1,000명 / 삼성SDS / 업스테이지 |
| **Applied AI (9장)** | "AI Engineers ship products" — Breunig / "5년→한 오후" — Swyx | LinkedIn AI Eng +143.2% (3년) | Brynjolfsson 2023 (+14% 생산성) | 카카오·네이버·토스·당근·업스테이지·뤼튼 |
| **Agent 운영자 (10장)** | "Hallucinations are a system design problem" — Galileo | 정식 직군화 진행 중, $5B → $50B 시장 | Cemri 2025 (41~87% 실패), Wang Agent Survey | SK 에이닷, Langfuse 한국어 공식 문서 |
| **Eval Eng (11장)** | "Error analysis is not optional" — Husain / "60-80% 시간을 evals에" | Anthropic Research Engineer (Model Evaluations) JD | Zheng LLM-as-judge, Deng MMLU 메모리화 57%, HELM | 거의 없음 (업스테이지 부분), 가장 늦게 |

---

## 3. 한국 시장 자료 별도 모음 (12장이 자료 부족으로 약해지지 않도록)

이 섹션의 모든 자료는 12장에서 직접 인용하고, 7~11장 한국 매핑에서도 활용한다.

### 3-A. 정량/뉴스
- KMJournal (2026): "GPU는 쌓였는데 사람이 없다" — https://www.kmjournal.net/news/articleView.html?idxno=7040
- 네이트 뉴스 (2026/01/05): "다룰 사람이 없다 — 텅 빈 한국 AI 두뇌"
- 스탠퍼드 AI Index 2025: 한국 OECD 35위 (인재 순유출)
- ZDNet Korea (2025/12/05): SI 빅3 AX 인사 전략 — https://zdnet.co.kr/view/?no=20251205105935
- ZDNet Korea (2025/12/08): 2026 채용 트렌드 — https://zdnet.co.kr/view/?no=20251208160526

### 3-B. 회사 채용 (빅컴퍼니 + 스타트업)
- 카카오: https://careers.kakao.com/jobs (ML Engineer LLM/Search, 경력 LLM)
- 네이버: 2026 NAVER AI CHALLENGE
- 토스: https://toss.im/career/jobs
- 당근: 2026 ML 직군 (피드 품질·광고추천·LLM 개인화)
- LG AI Research: https://kr.linkedin.com/company/lgairesearch/jobs (EXAONE Lab, Data Intelligence, STT/TTS)
- 업스테이지: https://careers.upstage.ai/ (AI Research Engineer LLM Eval, AI Solution Architect 등 30개)
- 뤼튼: 17개 분야 + 합격 보너스 2,000만원 — https://www.aitimes.com/news/articleView.html?idxno=169900
- LG CNS: 11개 AI 직무, 1,000명 목표 — https://www.smartfn.co.kr/news/articleView.html?idxno=110739

### 3-C. 회사 기술 블로그·실무 사례
- 영주.dev "SI 산업의 AI 대전환" (가장 종합적): https://www.youngju.dev/blog/culture/2026-03-23-si-industry-ai-transformation-career-guide
- 영주.dev LLM 모니터링 도구 비교: https://www.youngju.dev/blog/ai-platform/2026-03-09-ai-platform-llm-monitoring-langsmith-langfuse-arize
- SK Devocean (에이닷 LLM 운영 사례 다수): https://devocean.sk.com/blog/techBoardDetail.do?ID=166281
- LBox AI 개발기: https://medium.com/lbox-team/llm-...
- 당근 "AI 툴 개발은 처음이라" Medium
- 카카오스타일 PM 이미준의 AI PM 분석

### 3-D. 익명 커뮤니티 (OKKY 5선, velog 5선) — `community §3-D` 참조

### 3-E. 한국 도구 도입 신호
- Langfuse 한국어 공식 문서: https://langfuse.com/kr (셀프호스팅 활발)
- LangSmith — SKT 강의 진행(sudormrf.run)
- PyTorch KR 디스코드 토론

### 3-F. 분석/매체
- jmhong2020 Threads 분석: 한국 대기업 AI 에이전트 채용 트렌드 — https://www.threads.com/@jmhong2020/post/DQSPetlEufT
- 잡코리아 PMPO Day: AI 활용 PM론

---

## 4. Epigraph 모음 (챕터 도입 활용)

**1순위 (강도 최고):**
1. Swyx 2023 — *"5년 걸리던 AI 작업이 API 문서와 한가한 오후 한 번이면 가능해졌다."* → 9장
2. Drew Breunig 2025 — *"Data Scientists answer questions. ML Engineers build systems. AI Engineers ship products."* → 9장
3. Bloomberry 2025 — *"Forward deployed engineer jobs exploded by 1,165% year-over-year."* → 8장
4. a16z (Palantir) — *"We took our solutions engineers and called them Deltas — like Delta Force. It worked brilliantly."* → 8장
5. Hamel Husain — *"Evals replace traditional PRDs for AI products."* → 7장
6. Hamel Husain — *"Error analysis is not optional. Skip it and everything else is built on sand."* → 11장
7. Galileo AI — *"Hallucinations are not just a model problem. In production, they are a system design problem."* → 10장

**한국어 헤드라인 (12장 본문):**
8. KMJournal — *"GPU는 쌓였는데 사람이 없다."* (12장 도입 결정적)
9. 네이트 — *"다룰 사람이 없다 — 텅 빈 한국 AI 두뇌."*
10. 영주.dev — *"AI 시대의 SI 엔지니어는 '코더'에서 'AI 오케스트레이터'로 변화한다."*

**역사·학술 (1·2장):**
11. Steve Jobs 2007 — *"An iPod, a phone, and an Internet communicator. These are not three separate devices. This is one device."* → 프롤로그/2장
12. Carlota Perez 2002 — *"It is during the Deployment Period — after the major financial collapse — that the full social and economic potential of the new technologies can be realized."* → 1장
13. Autor 외 2024 — *"More than 60 percent of employment in 2018 is found in job titles that did not exist in 1940."* → 에필로그
14. Satya Nadella 2024 — *"SaaS is dead."* → 3장 도입
15. Fortune 2026 — *"Big Tech is about to spend $700 billion on AI this year. No one knows where the buildout ends."* → 4장

**중간 삽입용:**
16. Marily Nika — *"Every PM will be an AI PM. This is not a separate role — it is the new default."* → 7장
17. Husain & Shankar — *"We spent 60-80% of our development time on error analysis."* → 11장
18. Aakash Gupta — *"AI PMs are making $300K+ while regular PMs get laid off."* → 7장
19. Battery Ventures — *"Software shifts from aiding human productivity to autonomously completing work."* → 6장
20. Bret Taylor — *"Outcome-based pricing aligns the vendor's incentive with the customer's business outcome."* → 6장

---

## 5. 균형 점검 — 책 가설을 반박/완화하는 자료

13장 결론에서 정직하게 다뤄야 한다.

| # | 반박/완화 포인트 | 출처 | 책의 응답 방향 |
|---|---|---|---|
| 1 | AI 거시 효과 미미 (TFP 10년 ≤0.66%) | Acemoglu 2024 NBER w32487 | "거시는 천천히, 미시는 빠르게. 이 책은 미시(개인) 기회에 베팅한다." |
| 2 | 신직무는 *변형*이 우세, *대체*는 작다 | ILO 2025 WP140 | "변형의 옆에 서 있는 사람이 새 직업이 된다." |
| 3 | 22~25세 신입 진입 -14% | Anthropic Economic Index 5차(2026-03) | "AI를 *쓰는* 신입은 빨리 큰다(B+L+R 2023), AI에 *대체되는* 위치 신입은 진입이 막힌다." 두 데이터의 모순이 12장 핵심 긴장. |
| 4 | Reinstatement effect 지난 40년 약화 | Acemoglu·Restrepo 2019 JEP | "그래서 *가만히 있으면* 잃는다. 이동하는 사람만 새 reinstatement에 자리 잡는다." |
| 5 | AI는 frontier 바깥 -19%p | Dell'Acqua 2023 HBS | "Jagged frontier 매핑 능력 자체가 새 직업 역량." |
| 6 | 다중 에이전트 41~87% 실패 | Cemri 2025 arXiv:2503.13657 | "그래서 10장 Agent 운영자 직업이 진짜다." |
| 7 | LLM 평가 50%+ 메모리화 가능 | Deng 2024 NAACL | "그래서 11장 Eval Engineer가 측정의 표준을 다시 짠다." |
| 8 | 닷컴 인프라 챔피언 Cisco는 90% 손실, 25년 만에 회복 | CNBC 2025/12/10, Harding Loevner | "인프라 단계에 베팅하는 사람과 응용 단계에 베팅하는 사람의 위험은 다르다." → 3장 톤 환기. |
| 9 | Klarna 사람 CS 재채용 | Customer Experience Dive 2025 | "결과 과금에도 한계가 있다. 균형이 책의 정직성." → 6장 |

---

## 6. 검증 필요 항목 (본문 인용 시 신중)

1. **Anthropic ARR $30B (2026/05 시점):** SaaStr 보도 인용. 발표 출처가 회사 공식 IR이 아니라 매체 인용이므로 본문에서 *"보도 기준"* 표기.
2. **Cursor ARR $6B (2026 말 예상):** Anysphere 자체 가이던스 명시.
3. **Klarna "700명":** OpenAI 보도자료의 700은 *"AI가 대체한 풀타임 일감"*이며 실제 인원 5,527→3,422 감소는 같은 기간 다른 요인 포함. 본문에서 *"700 FTE 일감 ≠ 700명 해고"* 정확히 구분.
4. **Microsoft 1993년 IBM 시총 추월의 정확한 월:** "Early 1993"으로만 확인. 더 정확한 일자가 필요하면 추가 조사.
5. **Palantir Glassdoor / HN 익명 후기:** 모두 "익명 후기" 또는 "검증 필요"로 표기.
6. **Cisco 정점 시총 $569B:** CNBC와 Wikipedia 일치, *확정 사용 가능.*
7. **'AgentOps Engineer' 정식 직군화:** 검증 필요 가설로 명시 ("1~2년 안에 정식 직군화 가능성").

---

## 7. 리서치 한계

1. **영문 자료 중심:** 학술 자료는 영문 기반. 한국 KESS·한국고용정보원 통계를 본문 작성 단계에서 추가 보강 필요.
2. **Reddit 직접 검색 일부 실패:** 일부 Reddit 토론은 2차 출처(Pragmatic Engineer, a16z)에 의존.
3. **익명 커뮤니티 토론 (한국):** OKKY는 검색되지만 미국 Reddit에 비해 깊이 부족. 회사 기술 블로그가 보완.
4. **Eval Engineer 한국 자료 거의 전무:** 11장은 글로벌 자료 + 부분 사례에 의존.
5. **Anthropic Economic Index 후속 데이터:** 5차(2026-03) 이후 발표 시 갱신 필요.
6. **Bessemer Cloud Index 분기 갱신:** 2026 Q2~Q3 데이터로 본문 작성 직전 재확인.
7. **5개 직군의 LinkedIn 공고 키워드 빈도:** 본문 작성 시점에 한 번 더 스냅샷 떠서 *"X년 N월 기준"*으로 명시.

---

## 8. 원본 자료 위치

본 통합 레퍼런스는 다음 세 자료의 *재조직본*이다. 깊은 인용은 원본을 직접 참조.

| 원본 | 경로 | 용량 | 주요 자산 |
|---|---|---|---|
| 웹 리서치 | `research/web.md` | 33KB / 424줄 | 시대 패턴 timeline·시장 신호·인프라 데이터·BM 사례 (80개 출처) |
| 논문 리서치 | `research/papers.md` | 43KB / 489줄 | 24편 + 추가 5편 (Perez·David·Brynjolfsson·Acemoglu·Autor·Cemri·Zheng) |
| 커뮤니티 리서치 | `research/community.md` | 47KB / 784줄 | 5개 직업 실무자 발화·채용 공고·연봉·한국 시장·도구 비교 (131개 URL) |

본문 저술자는 챕터 시작 시 본 문서의 *해당 챕터 섹션*을 펼치고, 깊은 인용이 필요하면 원본으로 들어간다.

---

*작성: research-coordination 스킬 (책 "코드 너머의 직업들" 1차 자료집)*
*리서처: web-researcher / paper-researcher / community-researcher (병렬, 모두 opus)*
*작성일: 2026-05-10*
