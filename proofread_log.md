# Proofread Log — 코드 너머의 직업들

## 문체 점검 — v1.1.2 (2026-11-01)

- 기준: writing-deslop 11패턴 + 한국어 표현 지침(K-1~K-5), 「에이전트 성적표」 계획서 §C(처음부터 피할 문체) 목록. 외부 전송 없이 원천 장 파일을 직접 통독하고 로컬 정규식으로 후보를 찾았다.
- 범위: `chapters/`의 본문·부 도입·막간·에필로그(앞·뒷부속 포함). 표·인용 블록·참고문헌 목록·부록 A 카탈로그 항목은 문형 판정에서 뺐다(부록 A는 확정 건 없음).
- 목소리: 이 책의 원래 합니다체를 유지했다. 평어체로 바꾸지 않았다.
- 전 장을 통독하며 후보를 표시했고, 확정·수정은 169건이다. 오탐·그대로 둔 후보는 따로 세지 않았다(대표 예는 아래).

### 패턴별 확정 건수

| 패턴 | 건수 |
|---|---|
| C-4 글의 자기 설명("~부터 보겠습니다", "이 데이터가 무엇을 말하는지는 분명합니다", "다음 페이지는 ~") | 50 |
| P2 "X가 아니다. Y다." / "단순히 A가 아니라 B" | 23 |
| P7 예고형 반전("한 가지 있습니다. ~입니다.") | 20 |
| P4 원룸 문장·조각 나열("작은 화면. 느린 속도. 답답한 입력.") | 19 |
| K-4 마지막 재요약·같은 말 반복 | 14 |
| C-17 격언형·대구형 결말 | 8 |
| 질문 직후 자답 | 8 |
| P8 평가형 수식("정확히 짚었습니다", "진실입니다") | 7 |
| P6 세 겹 나열 | 3 |
| C-3 독자 훈계(작업 메모 노출 1건 포함) | 3 |
| C-15 근거 과장("학술적으로 증명합니다" → "뒷받침합니다") | 3 |
| C-2 추상 연결어 / C-6 반복 안전 종결 | 4 |
| P5 가짜 심오한 반전 | 2 |
| 기타(C-1 한계 고지 반복, C-5 감정 대리, 비문, 중복 결말, 교차 참조 오류) | 5 |

장별: 프롤로그 3, 1장 12, 2장 9, 3장 8, 4장 9, 5장 12, 6장 9, PART 3 도입 4, 7장 11, 8장 10, 9장 7, 10장 15, 11장 20, 막간 11, 12장 12, 13장 3, 14장 6, 에필로그 8.

### 예시 (전 → 후)

| 장 | 패턴 | 전 | 후 |
|---|---|---|---|
| 1 | P2 | Cisco도, Sun도, IBM도, Yahoo도 아니었습니다. Google. Amazon. | Cisco, Sun, IBM, Yahoo 대신 Google과 Amazon이었습니다. |
| 2 | C-4 + P5 | 이 결과가 무엇을 말하는지를 다시 정리해 보면, 시차의 메커니즘이 좀 더 분명해집니다. *AI는 평균을 끌어올리는 게 아니라, 신입을 빠르게 숙련자로 만든다.* | *AI는 신입을 빠르게 숙련자로 만듭니다.* 새 인프라 위에서 일하는 방식을 *모두가 학습하는 시간*이 짧아지고, 그래서 시차가 짧아집니다. |
| 5 | P4·대구 3연속 | SRE는 … 추적합니다. AgentOps는 … 추적합니다. (한 문장 문단 3개 반복) | SRE는 …를 추적하고, …를 보며, …합니다. AgentOps는 …를 추적하고, …를 보며, …를 짭니다. (두 문장) |
| 6 | C-3 작업 메모 노출 | 본문에서 인용할 때 이 구분을 정확히 해 두는 것이 좋습니다. | 삭제(앞 문장이 구분을 이미 적음) |
| 7 | P2 | 퇴근 전, GitHub PR 두 개를 리뷰합니다. 코드 PR이 아닙니다. *프롬프트 PR*입니다. | 퇴근 전, GitHub에서 *프롬프트 PR* 두 개를 리뷰합니다. |
| 10 | P7 | 가장 큰 차이가 한 가지 있습니다. *측정의 대상이 결정론적이지 않습니다.* | 가장 큰 차이는 *측정의 대상이 결정론적이지 않다*는 점입니다. |
| 막간 | P8 + P4 | 이 9가지가 모두 옳을 가능성. 일부만 옳을 가능성. 전부 틀릴 가능성. 어느 경우든, …않다는 게 진실입니다. | 이 9가지가 모두 옳을 수도, 일부만 옳을 수도, 전부 틀릴 수도 있습니다. 어느 경우든 … 않습니다. |
| 12 | K-4 | 이 모순을 직시하는 것이 12장의 가장 큰 메시지입니다. *한국은 진입은 좁고, …시장입니다.* 90일 플랜이 …이유가 여기 있습니다. | 그래서 90일 플랜은 *진입 가능성을 높이는 90일*이 되어야 합니다. (같은 가설이 바로 앞 인용 박스에 있음) |

### 오탐·그대로 둔 것 (대표)

- 인용 안의 문형: Nadella "SaaS is dead", Husain "Error analysis is not optional", Marily Nika "별도 직군이 아니라 PM의 새로운 표준" 등은 화자의 말이라 두었다.
- 인용 바로 뒤의 우리말 풀이("~라는 것."): 영어 인용을 독자에게 옮기는 기능이라 두었다(재진술이 두 번 겹친 4장 1건만 삭제).
- 정의를 가르는 대조: 9장 "ML engineers focus on the model…" 풀이, 10장 "서비스가 죽은 게 아니라 에이전트가 이상하게 행동한 경우", 막간 8 "Nvidia 주식에 베팅하는 게 아니라 …직업에 베팅".
- 부 도입·5칸 포맷 안내, 각 장 끝 "다음 장에서는 ~" 예고 한 문장: 책 구조 안내라 두었다(조각 나열형만 문장으로 합침).
- 엠대시(K-1): 장 제목·인용 출처·목록 표기의 "—"는 이 책 전체의 편집 관례라 일괄 치환하지 않았다.
- 추상 은유 "축"(K-2): "길이·속도·비용의 세 축"이 책의 틀을 이루는 용어라 두었다.

### 불변식 검사 (통합 원고 전후 비교, 스크립트)

- 따옴표(“”, "", 「」, 『』) 안 문자열 177개: 전후 동일.
- URL 64개: 전후 동일.
- 표 행 191행: 전후 셀 값까지 동일.
- 숫자 토큰 2,702 → 2,685. 사라진 토큰은 모두 지운 자기 설명 문장 안의 장·부 번호("5장의 마지막 한 절은, 10장으로…", "12장의 클라이맥스", "(4장)…(5장)…(6장)" 등), 바로 앞 문장이 이미 말한 수("7시간", "2024년 이후", "9가지", "1·1·1 원칙", "90일")다. 추가된 토큰은 판본 표기(1.1.2, 2026-11-01, 169)와 3장 교차 참조 수정 "1장" 하나다.

### 사실 관련 수정 1건 (편집 교정)

- 3장 박스: "지난 장에서 잠깐 언급한 Cisco의 차트" → "1장에서 잠깐 언급한 Cisco의 차트". Cisco 차트는 2장이 아니라 1장에 있다.

### 남은 문제 (내용 사안이라 고치지 않음, 저자 확인 필요)

- 10장 하루의 풍경: "트레이싱 셋업. 비용 모니터링. 알람 채널. 실패 모드 카탈로그. 다섯 가지 단계를" — 항목은 넷인데 "다섯"이라 적혀 있다.
- 10장: 도입 4단계 인용을 "velog에 올라온 한 한국 실무자"의 글로 소개한 뒤 다음 문단은 "영주.dev의 한 글에서 정리한"이라 적는다(14장 휴리스틱 2도 영주.dev로 적음). 출처 귀속이 엇갈린다.
- 14장 끝: "13장의 4명의 사례 중 3명이 90일 안에 첫 공개 자산을 만들었습니다"와 13장 "네 명 모두 GitHub 또는 블로그에 공개된 자산"이 어긋난다.
- 막간 3: "두 데이터의 모순이 이 책의 12장 핵심 긴장입니다" — 3장에서 먼저 다루고 12장 클라이맥스 절에서 다시 다룬다. 의도된 참조인지 확인 필요.
- 8장 그림자 면: "워라밸 2.5/5는 한 회사의 데이터지만, FDE라는 직군의 평균 풍경에 가깝습니다"는 한 회사 자료의 일반화(C-8)다. 주장 자체라 두었다.

### 빌드

- 통합 원고: `chapters/`를 이전과 같은 순서·구분자(파일 사이 빈 줄 하나, 끝 빈 줄 둘)로 이어 `04_manuscript.md`를 다시 만들었다. 이전 v1.1.1 원고를 같은 방식으로 재조립해 차이가 앞부속 버전·발행일 두 줄(원천이 1.0.0으로 남아 있던 부분)뿐임을 확인했고, 이번에 원천 `000_frontmatter.md`도 1.1.2로 맞췄다.
- EPUB: 하네스 `build_epub.sh`(book-writer 1.11.0)로 `docs/epub/코드-너머의-직업들-v1.1.2.epub` 생성, epubcheck 0 오류·0 경고.
- 웹: `docs/index.html`의 TOC~본문 구간을 pandoc(`--toc --toc-depth=2`, html5)으로 다시 만들어 교체했다. 같은 방식으로 v1.1.1 원고를 변환하면 기존 구간과 바이트 단위로 같음을 먼저 확인했다. 머리(hero·오프닝 영상 블록)와 꼬리(맨 위로 버튼 스크립트)는 그대로 두고, hero의 판본 표기만 v1.1.2로 바꿨다. 목차(TOC) 구간은 전후 동일.

## 내용 정합성 정리 — v1.1.3 (2026-11-01)

v1.1.2 점검에서 남긴 문제 가운데 저자가 승인한 다섯 건을 고쳤다. 에이닷 운영팀 사례는 저자 지시대로 그대로 두었다.

| # | 위치 | 판단 근거 | 전 | 후 |
|---|---|---|---|---|
| a | 10장 하루의 풍경 | 나열 항목은 넷이다. 이 장면은 가상 인물의 하루라 research/·01_reference.md에 다섯 번째 단계의 출처가 없다. 그래서 복원하지 않고 수를 맞췄다. | 다섯 가지 단계를 | 네 가지 단계를 |
| b | 14장 끝 | 13장 사례 넷의 "첫 90일에 한 것"이 모두 공개 자산을 적는다. 민호는 RAG 프로토타입 GitHub 공개, 수진은 eval 데이터셋 GitHub 공개, 지수는 비용 측정 블로그, 재현은 실패 모드 보고서 블로그다. 사례는 재구성이라 research/에 따로 근거가 없어 본문 사례를 기준으로 했다. | 4명의 사례 중 *3명이* … 나머지 1명도 … *학습의 결정적 진전* | 13장의 4명은 모두 *90일 안에 첫 공개 자산*을 만들었습니다. |
| c | 10장 도입 4단계 인용 | research/community.md 232행: 인용문 출처가 "영주.dev 블로그 정리"다(youngju.dev LLM 모니터링 비교 글, 2026-03-09). velog 귀속은 틀렸다. 14장 휴리스틱 2, 01_reference.md 434행도 영주.dev로 적는다. | velog에 올라온 한 한국 실무자는 … / 영주.dev의 한 글에서 정리한 … | 영주.dev의 LLM 모니터링 도구 비교 글은 … / 이 글이 정리한 … |
| d | 막간 3 | 이 모순은 3장 "반대 신호" 절에서 처음 나오고 12장 클라이맥스 절에서 다시 다룬다. | 이 책의 12장 핵심 긴장입니다 | 3장에서 처음 짚고 12장에서 다시 다루는 이 책의 핵심 긴장입니다 |
| e | 8장 그림자 면 | 근거는 Palantir 한 회사의 Glassdoor 후기다. | 한 회사의 데이터지만, *FDE라는 직군의 평균 풍경*에 가깝습니다. | 다만 … Palantir 한 회사의 Glassdoor 후기라서, *FDE 직군 전체의 평균*으로 읽을 수는 없습니다. |

- 불변식 검사(v1.1.2 대비): 따옴표 안 문자열 177·URL 64·표 191행 동일. 숫자 토큰 변화는 판 이력 줄(1.1.3, 10·13·14장, 8장), 막간의 "3장"(같은 문장에서 "3명"이 빠져 '3' 토큰은 같은 수), 14장에서 지운 "나머지 1명", 되풀이된 "90일"뿐이다.
- 빌드: 같은 파이프라인. EPUB `docs/epub/코드-너머의-직업들-v1.1.3.epub`, epubcheck 0 오류·0 경고. 웹 본문은 pandoc으로 다시 만들었다. v1.1.2 원고를 같은 방식으로 변환한 구간이 기존 페이지와 일치함을 확인한 뒤 교체했다. TOC는 전후 동일하고 오프닝 영상 블록도 그대로다.

## v1.1.4 패치 (2026-11-02)

### 1. 인물 '수진'의 회사 소재 정합

수진은 7장(하루의 풍경)과 13장(사례 2)에 나온다. 두 곳 모두 전직 "카카오 PM 4년", 현직 "시리즈 B AI 스타트업 1년 차"로 같은 인물이고, 13장 끝 공통점 1·2와 14장 끝도 같은 수진을 가리킨다. 소재만 7장 "미국", 13장 "한국"으로 갈렸다.

| 위치 | 전 | 후 |
|---|---|---|
| 7장 하루의 풍경 첫 문단 | 미국의 한 시리즈 B AI 스타트업에서 AI Product Manager로 일하고 있습니다. | 한국의 한 시리즈 B AI 스타트업에서 AI Product Manager로 일하고 있습니다. |

- 정전 판단: 처음 소개되는 곳은 7장이지만, 13장을 정전으로 삼았다. 02_plan.md 13장 설계가 이 사례를 "PM → AI PM (Marily Nika 또는 한국 PM)"으로 잡았고 사례들은 "가능하면 한국 실명/익명"이다. 13장 사례 2는 제목("한국 PM → AI Product Manager (한국 잔류)"), 현직, 옮긴 동기("별도 직군이 한국에 거의 없으니"), 회고 한 줄("한국 AI 네이티브 회사에 가니 모든 PM이 AI PM")까지 한국 소재 위에 서 있다. 7장은 소재를 한 단어로만 적고 나머지 장면에는 소재에 기대는 서술이 없다. 그래서 7장 한 단어를 고치는 쪽이 최소 수정이다. research/·01_reference.md에는 수진에 관한 서술이 없다(가상 인물).
- 덱(docs/presentation, deck/slides.py): 수진은 7장 슬라이드 각주에 "가상 인물 수진의 PRD"로만 나오고 소재 서술이 없어 고치지 않았다.
- 남긴 것: 7장 오전 11시의 가격 예시($50·$80)는 소재와 무관한 숫자 예시라 그대로 두었다. 13장은 "PM 타이틀, 실질적 AI PM"이라 적고 7장은 "AI Product Manager로 일하고"라 적는 직함 표기 차이도 있으나, 13장이 실질 직무를 AI PM으로 보므로 모순으로 보지 않고 두었다. 에이닷 운영팀 사례는 저자 지시로 건드리지 않았다.

### 2. 웹 책 표 가로 넘침

- 진단(Playwright, 390px): 문서 폭 565px. 넘친 요소는 본문 표 24개(셀 최소 폭 44px까지 눌림)와 참고문헌의 Threads URL 한 줄(`span.citation`, pandoc이 `@jmhong2020/...`을 인용 표기로 읽은 것, 이전부터 있던 표기).
- 수정: pandoc 본문 구간의 `<table>` 24개를 모두 `<div class="table-wrap">`(overflow-x:auto)로 감쌌다. 표 칸 `th,td`에 `overflow-wrap:break-word; min-width:6.5em`. 긴 URL은 `main p, main li { overflow-wrap:break-word }`로 줄을 넘긴다. 코드 블록 `pre`는 이미 overflow-x:auto였다(본문에 pre 0개).
- 결과: 390·768·1440 세 폭에서 문서 폭 = 화면 폭, 넘침 요소 0. 표 셀 최소 폭 390에서 105px, 1440에서 137px. 1440·390 표 캡처(deck/shots/table_widest_*.png)로 칸이 한 글자씩 쪼개지지 않음을 눈으로 확인했다. 390에서는 표가 감싸개 안에서 옆으로 스크롤된다. 오프닝 영상 블록, 발표 자료 링크, 목차 링크 183개 유지.

### 빌드
- 통합 원고: 같은 순서·구분자로 `chapters/`를 재조립. 재조립 스크립트가 v1.1.3 원고와 바이트 단위로 같음을 먼저 확인했다. 차이는 앞부속 버전·개정일·판 이력 줄과 7장 한 단어.
- EPUB: 하네스 `build_epub.sh`(book-writer 1.11.0)로 `docs/epub/코드-너머의-직업들-v1.1.4.epub`, epubcheck 0 오류·0 경고.
- 웹: 같은 pandoc 설정(`--toc --toc-depth=2`, html5)으로 v1.1.3 원고를 변환하면 기존 구간과 같음을 확인한 뒤, v1.1.4 원고로 다시 만들어 교체했다. 표 감싸개는 변환 뒤 후처리로 넣었다. hero 판본 표기 v1.1.4.

## 문체 2차 점검 — v1.1.5 (2026-11-07)

- 기준: writing-deslop 한국어 표현 지침(K-1~K-5) 중심, 11패턴 재점검. 외부 전송 없이 원천 장 파일·덱 원천·README를 직접 읽고 로컬 정규식으로 후보를 뽑아 문맥을 보고 고쳤다. 합니다체 유지.
- 범위: `chapters/` 전체(앞·뒷부속, 부 도입, 막간, 부록 A, 참고문헌), `deck/slides.py`, `README.md`, `book_manifest.json`의 장 제목 목록·rights 문구. 영상은 건드리지 않았다.
- 원고 정리 248곳(장 파일 기준 치환 수), 덱 64곳, README 19곳.
- 저자 결정 대기 줄(12장 "SK C&C / SK텔레콤" 줄, 에이닷 사례가 든 줄)은 엠대시까지 포함해 손대지 않았다.

### 규칙별 건수 (원고)

| 규칙 | 건수 | 내용 |
|---|---|---|
| K-1 엠대시 | 228자 제거 (245 → 17) | 장·절 제목 103, 인용 출처 줄 17(괄호로), 서명 3, 표 셀 18(빈 칸 표시 8은 `-`), 목록·본문·판 이력 나머지 |
| K-2 축 | 12 | 4장·PART 2 도입·5·9·14장·에필로그의 "세 축/3축"을 "세 지표", "세 가지(변화)"로. 커리어 분류 용어가 아니라 길이·속도·비용(9장은 정확도·지연·비용)을 가리키는 은유였다 |
| K-3 영어 직역 | 6 | "~하지 않고" → "~하는 대신" 3, "남겼습니다" → "썼습니다" 1, "남깁니다" → "올립니다" 1, "곧 회사의 매출입니다" → "회사의 매출을 좌우합니다" 1 |
| K-4 대조 틀·맺음 | 10 | 같은 장에 이어 나온 "X가 아니라 Y" 9(막간 2, 5·7·7·9·10·10·11장), "결국" 맺음 1(8장) |
| 11패턴 | 14 | P7 예고형 2(3장 공통점, 7장 면접 질문), C-4 자기 설명 1(3장 "한 줄로 정리하면"), P4 조각 나열 11(직업 이름 다섯 개를 마침표로 끊은 나열 5곳, PART 2 도입·에필로그 요약 문단 5곳, 5장 네 모듈 문단 1) |

엠대시와 다른 규칙이 한 문장에서 겹친 곳은 한 번으로 셌다.

### 남긴 엠대시 17자 (원고)

- 직접 인용문 안 11자: 1장·에필로그 Perez 인용(2+2), 5장·10장 Cemri 인용(1+1), 10장 AgentOps 정의 인용(2), 11장 Zheng 인용(1), 11장 Husain 인용(1), 8장 Palantir 인용(1).
- 11장 Anthropic 채용 공고 책임 목록의 원문 구절(*novel evaluation methodologies — …*) 1자.
- 기사 원제 3자: 12장 본문 네이트 뉴스 헤드라인, 12장 ZDNet Korea 기사 제목, 참고문헌의 네이트 뉴스.
- 참고문헌 원제 1자: Bloomberry 글 제목.
- 저자 결정 대기 줄 1자: PART 3 도입 표의 10장 행("운영팀 형태 — SK 에이닷 등…"). 덱의 같은 행도 그대로 두었다.
- 엔대시(–) 8자는 전후 같다(새로 쓰지 않았다).
- 웹 `docs/index.html`의 CSS 주석 1자는 코드라 두었다. 덱 HTML `<title>`의 "— 1시간 발표 자료"는 하네스 deck.py 엔진이 붙이는 문구라 이 책에서 고치지 않았다(쪽 아래 책 이름 표시는 `D.setup(book=…)`로 엠대시 없이 넘겼다).

### 용어로 유지한 단어

- 칸: "다섯 칸 포맷", "한국 칸", "5칸 × 3문항". PART 3 도입에 "## 다섯 칸 포맷" 절이 있고 7~11장의 다섯 절 구성을 가리키는 책의 형식 용어다.
- 축: 9장 비교 표의 머리 "최적화 축"과 셀 "응답 시간·토큰 비용·결과 정확도 3축", 덱의 같은 표. 표 값은 바꾸지 않는다는 규칙으로 두었다.
- 따라온다: PART 1 제목 "인프라가 먼저 가고, 사람이 따라온다". 성과가 따라온다는 직역 뜻이 아니라 순서(뒤에 온다)를 말하는 제목이고, 책 전체의 문장 "반도체는 먼저 갔고, 사람은 따라간다"와 짝이라 두었다.
- 곧: 에필로그 제목 "다음 단계는 곧 도착한다"는 '머지않아' 뜻이라 두었다.
- 답: 앞부속 "질문이 명확해지자 답도 분명해졌습니다"처럼 질문에 대한 대답 뜻만 남아 있다.
- 1차에서 둔 "끝의 풍경이 아니라 다음을 기다리는 풍경"(프롤로그 절 제목·책을 펴내며·에필로그)과 5장 제목 "도구가 아니라 동료에 가까운"은 책의 모티프라 그대로 두었다.

### 예시 (전 → 후)

| 장 | 규칙 | 전 | 후 |
|---|---|---|---|
| 2 | K-1 장 제목 | 2장. 시차는 점점 짧아진다 — 그리고 AI는 더 빠르다 | 2장. 시차는 점점 짧아진다, 그리고 AI는 더 빠르다 |
| 1 | K-1 인용 출처 | > — Carlota Perez, *Technological Revolutions and Financial Capital* (2002) | > (Carlota Perez, *Technological Revolutions and Financial Capital*, 2002) |
| 4 | K-2 | 그 안에 *세 가지 축*이 움직이고 있습니다. | 그 안에서는 *세 가지 지표*가 움직이고 있습니다. |
| PART 2 도입 | K-1 + K-2 + P4 | 4장은 AI 인프라의 세 축 — 길이·속도·비용 — 을 정리합니다. 컨텍스트 윈도우 250배. 토큰당 비용 연 50~200배 하락. | 4장은 AI 인프라에서 함께 움직인 길이·속도·비용을 정리합니다. 컨텍스트 윈도우는 250배 길어졌고, 토큰당 비용은 해마다 50~200배씩 떨어졌습니다. |
| 8 | K-3 곧 | *모델을 어떻게 고객 환경에 맞춰 배포할지*가 곧 회사의 매출입니다. | …가 회사의 매출을 좌우합니다. |
| 14 | K-3 | 모든 단계를 동시에 시작하지 않고, *한 단계씩* 채웁니다. | 모든 단계를 동시에 시작하는 대신, *한 단계씩* 채웁니다. |
| 막간 | K-4 | 이 책은 *국가 GDP*에 베팅하는 게 아니라 *개인 커리어*에 베팅합니다. | 이 책이 베팅하는 대상은 *국가 GDP*보다 *개인 커리어*입니다. |
| 3 | P7 + C-4 | 공통점이 한 가지 있습니다. *시트당(seat) 과금*이 무너지고 있습니다. … 한 줄로 정리하면, 그 변화의 본질은 | 공통점은 *시트당(seat) 과금*이 무너지고 있다는 것입니다. … 그 변화의 본질은 |
| 에필로그 | P4 | 막간에서 직시한 9가지 반박을 떠올려 봅니다. AI 거시 효과 미미. 신직무는 변형이 우세. 신입 진입 -14%. … Klarna 재채용. | 막간에서는 9가지 반박을 직시했습니다. AI의 거시 효과는 미미하고, 신직무는 변형이 우세하며, 신입 진입은 -14%였습니다. … Klarna는 다시 사람을 뽑았습니다. |
| 11 | K-1 표 셀 | "Evals replace PRDs" — Husain | "Evals replace PRDs" (Husain) |

### 불변식 검사 (통합 원고 v1.1.4 → v1.1.5, 스크립트)

- URL 64개: 전후 동일.
- 따옴표 안 문자열 177개: 수 동일. 바뀐 것 1개는 14장 가상 글 제목 예시 "RAG retrieval 단계의 청크 크기 실험 — 4가지 크기 비교"의 엠대시를 쌍점으로 바꾼 것뿐이다(실존 인용이 아니라 독자에게 주는 제목 예시).
- 표 191행: 행 수 동일. 셀 값이 바뀐 18행은 모두 엠대시 차이뿐이다. PART 3 도입 표 4행(단계명 뒤 "—" → ":"), 11장 QA 비교 표 1행, 11장 다섯 직업 요약 표 5행(인용 뒤 "— 이름" → "(이름)"), 13장 매핑 표 8행(빈 칸 표시 "—" → "-"). 나머지 문자는 같다.
- 숫자 토큰 2,691 → 2,692. 빠진 것: "3축" 두 곳의 3(→ "세 가지"), 판본 1.1.4, 개정일 02. 더한 것: 판본 1.1.5(2), 개정일 07, 판 이력 줄의 "2차"·"248".
- 덱 원천: 숫자 토큰은 판 표기 1.1.3 → 1.1.5 세 곳만 바뀌었고 URL은 같다. README: 판 이력 한 줄과 EPUB 파일 이름 판 표기만 숫자가 바뀌었다.

### 빌드

- 통합 원고: 이전과 같은 순서·구분자로 `chapters/`를 재조립. 재조립 스크립트가 v1.1.4 원고와 바이트 단위로 같음을 먼저 확인했다.
- 장 제목을 바꾼 만큼 앞부속 목차, `book_manifest.json`의 chapters, README 목차 표, 덱의 장 제목도 같은 문구로 맞췄다. 매니페스트에 `rights`("© 2026 김상기, Licensed under CC BY-NC-SA 4.0")를 넣어 하네스 기본 rights 문구의 엠대시를 뺐다.
- EPUB: 하네스 `build_epub.sh`(book-writer 1.11.0)로 `docs/epub/코드-너머의-직업들-v1.1.5.epub`, epubcheck 0 오류·0 경고. (이 기기의 JAVA_HOME이 없는 JDK를 가리켜, 실행할 때만 Homebrew openjdk를 지정했다.)
- 웹: 같은 pandoc 설정(`--toc --toc-depth=2`, html5)과 표 감싸개 후처리로 v1.1.4 원고를 변환하면 기존 구간과 같음을 확인한 뒤, v1.1.5 원고로 교체했다. hero 판본 v1.1.5. 목차 링크 183개 모두 본문 id와 맞고, 오프닝 영상 블록·발표 자료 링크 유지.
- 덱: 하네스 deck.py 엔진으로 `docs/presentation/index.html` 재생성(44장). 끝 장 판 표기도 v1.1.5로 맞췄다.
- Playwright(390·1440): 웹과 덱 모두 문서 폭 = 화면 폭, 넘침 요소 0.

## 참고문헌 링크 패치 — v1.1.6 (2026-11-07)

- 문제: 참고문헌의 Threads 글 주소가 웹과 EPUB에서 링크가 아니었다. pandoc이 주소 안의 `@jmhong2020/...`을 인용 표기(`span.citation`)로 읽었다. 주소는 살아 있다(응답 200, 글 제목 일치).
- 수정: `chapters/zz_bibliography.md`와 통합 원고의 그 한 줄만 주소를 `<https://...>` 자동 링크로 감쌌다. 본문(9장·14장)의 jmhong2020 언급은 링크가 아니라 그대로 두었다.
- 판 표기: 앞부속 버전 1.1.6, 판 이력 한 줄, README 판 이력·EPUB 링크, 매니페스트 version. 내용·수치 변경 없음.
- EPUB: 하네스 `build_epub.sh`(book-writer 1.11.0)로 `docs/epub/코드-너머의-직업들-v1.1.6.epub`, epubcheck 0 오류·0 경고. EPUB 안에 해당 `<a href>` 1개, 인용 표기 0개.
- 웹: 같은 pandoc 설정으로 v1.1.5·v1.1.6 원고를 변환해 나온 차이(앞부속 버전·판 이력, 참고문헌 한 줄)만 `docs/index.html`에 옮기고 hero 판본을 v1.1.6으로 바꿨다. 덱은 건드리지 않았다.
- Playwright(390·1440): 웹·덱 문서 폭 = 화면 폭, 넘침 0. 웹에 해당 a 태그 1개, `span.citation` 0개, 목차 링크 183개 모두 본문 id와 맞음, 오프닝 영상·발표 자료 링크 유지.

## 참고문헌 주소 링크·접근 확인 — v1.1.7 (2026-11-07)

- 범위: 원고의 주소 64개 전부(참고문헌 63개, 11장 본문 출처 1개). v1.1.6에서 감싼 Threads 주소도 다시 확인했다.
- 방법: curl `-sIL`(실패하면 GET), 브라우저 User-Agent, 타임아웃 20초. 200이 아니거나 리다이렉트가 수상한 주소는 Playwright(showreel 스킬의 playwright-core, Chromium 1248)로 다시 열어 응답·쪽 제목을 확인했다. 결과가 404이거나 도메인이 사라진 주소는 같은 출처의 옮긴 주소를 찾고, 없으면 Wayback Machine 보관본을 찾았다.
- 결과: 열림 60개(주소 그대로 `<URL>`로 감쌈), 보관본으로 교체 3개, 못 찾음 1개. 같은 출처의 새 주소로 옮긴 경우는 없었다.
- Cloudflare 사람 확인 화면이 뜨는 4개(OUP DOI 3개, SSRN 1개)는 Playwright(헤드리스·창 띄움 둘 다)로도 넘지 못했다. DOI는 Crossref 메타데이터 제목이 서지와 같고 출판사 논문 쪽으로 해석되며, SSRN은 Wayback에 2026-10-24 정상 보관본이 있어 열림으로 판단했다.

### 주소 갱신 (전 → 후)

| 위치 | 전 | 후 | 근거 |
|---|---|---|---|
| 참고문헌 1절 Perez 2002 | http://pombo.free.fr/carlota2002.pdf | https://web.archive.org/web/20240801135259/http://pombo.free.fr/carlota2002.pdf | 404. 보관본 PDF 첫 쪽이 같은 책(Edward Elgar) |
| 참고문헌 7절 영주.dev (LLM 모니터링) | https://www.youngju.dev/blog/ai-platform/2026-03-09-ai-platform-llm-monitoring-langsmith-langfuse-arize | https://web.archive.org/web/20260509200439/https://www.youngju.dev/blog/ai-platform/2026-03-09-ai-platform-llm-monitoring-langsmith-langfuse-arize | 도메인 만료(주차 페이지). 보관본 제목·날짜 2026-03-09 일치 |
| 11장 본문 출처 (Anthropic 채용 공고) | https://job-boards.greenhouse.io/anthropic/jobs/4990535008 | https://web.archive.org/web/20260213181053/https://job-boards.greenhouse.io/anthropic/jobs/4990535008 | 공고 마감(목록 오류 화면으로 이동). 보관본 제목 "[Expression of Interest] Research Engineer, Model Evaluations" |

### 못 찾음 (링크로 감싸지 않고 그대로 둠, 저자 결정)

- 참고문헌 7절 영주.dev. "SI 산업의 AI 대전환." 2026-03-23. https://www.youngju.dev/blog/culture/2026-03-23-si-industry-ai-transformation-career-guide : 도메인 만료(GoDaddy 주차 페이지). 검색에 나온 같은 도메인의 /split/·/transcribe/ 주소도 같은 상태이고, Wayback에는 세 주소 모두 보관본이 없다.

### 확인 표

| # | URL | curl | 브라우저(Playwright) | 판단 |
|---|---|---|---|---|
| 1 | http://pombo.free.fr/carlota2002.pdf | 404→GET 404 | 404 404 Not Found | 안 열림(404, 같은 사이트에 옮긴 곳 없음). Wayback 보관본(2024-08-01, 같은 책 PDF 확인)으로 교체 |
| 2 | https://doi.org/10.1093/cje/bep051 | 403→GET 403 | 403 Just a moment... | 열림으로 판단. 출판사(OUP) Cloudflare 사람 확인 화면. DOI가 해당 논문 쪽으로 해석되고 Crossref 제목 일치 |
| 3 | https://www.nber.org/papers/w4148 | 200 | 200 General Purpose Technologies "Engines of Growth?" | 열림 |
| 4 | http://digamo.free.fr/david90.pdf | 200 | 200 | 열림 |
| 5 | https://doi.org/10.2307/2234208 | 403→GET 403 | 403 Just a moment... | 열림으로 판단. OUP Cloudflare 사람 확인 화면. Crossref 제목 일치 |
| 6 | https://doi.org/10.1257/mac.20180386 | 403→GET 403 | 200 The Productivity J-Curve: How Intangibles Compleme | 열림. curl 봇 차단, 브라우저 200·제목 일치 |
| 7 | https://www.nber.org/papers/w31161 | 200 | 200 Generative AI at Work / NBER | 열림 |
| 8 | https://www.nber.org/papers/w32487 | 200 | 200 The Simple Macroeconomics of AI / NBER | 열림 |
| 9 | https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4573321 | 403→GET 403 | 403 Just a moment... | 열림으로 판단. SSRN Cloudflare 사람 확인 화면. Wayback에 2026-10-24 정상 보관(200) |
| 10 | https://doi.org/10.1093/qje/qjae008 | 403→GET 403 | 403 Just a moment... | 열림으로 판단. OUP Cloudflare 사람 확인 화면. Crossref 제목 일치 |
| 11 | https://doi.org/10.1257/jep.33.2.3 | 403→GET 403 | 200 Automation and New Tasks: How Technology Displaces | 열림. curl 봇 차단, 브라우저 200·제목 일치 |
| 12 | https://www.anthropic.com/economic-index | 200 | 200 The Anthropic Economic Index \ Anthropic | 열림 |
| 13 | https://www.ilo.org/sites/default/files/2025-05/WP140_web.pdf | 200 | 200 | 열림 |
| 14 | https://www.weforum.org/publications/the-future-of-jobs-report-2025/ | 403→GET 403 | 200 The Future of Jobs Report 2025 / World Economic Fo | 열림. curl 봇 차단, 브라우저 200·제목 일치 |
| 15 | https://hai.stanford.edu/ai-index/2025-ai-index-report | 200 | 200 The 2025 AI Index Report / Stanford HAI | 열림 |
| 16 | https://arxiv.org/abs/2308.11432 | 200 | 200 [2308.11432] A Survey on Large Language Model base | 열림 |
| 17 | https://arxiv.org/abs/2402.02716 | 200 | 200 [2402.02716] Understanding the planning of LLM age | 열림 |
| 18 | https://arxiv.org/abs/2503.13657 | 200 | 200 [2503.13657] Why Do Multi-Agent LLM Systems Fail? | 열림 |
| 19 | https://arxiv.org/abs/2306.05685 | 200 | 200 [2306.05685] Judging LLM-as-a-Judge with MT-Bench | 열림 |
| 20 | https://arxiv.org/abs/2311.09783 | 200 | 200 [2311.09783] Investigating Data Contamination in M | 열림 |
| 21 | https://arxiv.org/abs/2211.09110 | 200 | 200 [2211.09110] Holistic Evaluation of Language Model | 열림 |
| 22 | https://economicgraph.linkedin.com/research/future-of-work-report-ai | 404→GET 200 | 200 Future of Work Report: AI at Work | 열림. pulse.linkedin.com 같은 보고서로 리다이렉트, 제목 일치. 주소는 그대로 |
| 23 | https://www.onetcenter.org/dataUpdates.html | 200 | 200 O*NET® Occupation Update Summary at O*NET Resource | 열림 |
| 24 | https://bloomberry.com/blog/i-analyzed-1000-forward-deployed-engineer-jobs-what-i-learned/ | 200 | 200 What I learned analyzing 1K forward deployed engin | 열림 |
| 25 | https://www.pewresearch.org/internet/2012/03/01/nearly-half-of-american-adults-are-smartphone-owners/ | 200 | 200 Nearly half of American adults are smartphone owne | 열림 |
| 26 | https://www.pewresearch.org/internet/2013/06/05/smartphone-ownership-2013/ | 200 | 200 Smartphone Ownership 2013 / Pew Research Center | 열림 |
| 27 | https://cloudindex.bvp.com/ | 200 | 200 404: This page could not be found | 열림. 첫 로드 때 404 문구가 잠깐 보였으나 재확인에서 Overview 지수 화면 |
| 28 | https://www.bvp.com/atlas/the-cloud-100-benchmarks-report | 200 | 200 The Cloud 100 Benchmarks Report 2025 / Bessemer Ve | 열림 |
| 29 | https://epoch.ai/data-insights/llm-inference-price-trends | 200 | 200 LLM inference prices have fallen rapidly but unequ | 열림 |
| 30 | https://artificialanalysis.ai/ | 200 | 200 AI Model & API Providers Analysis / Artificial Ana | 열림 |
| 31 | https://fin.ai/pricing | 200 | 200 Fin AI Agent Pricing / Free 14-day Trial | 열림 |
| 32 | https://www.zendesk.com/newsroom/articles/zendesk-outcome-based-pricing/ | 200 | 200 Zendesk First in CX Industry to offer Outcome-Base | 열림 |
| 33 | https://techcrunch.com/2025/11/21/bret-taylors-sierra-reaches-100m-arr-in-under-two-years/ | 200 | 200 Bret Taylor's Sierra reaches $100M ARR in under tw | 열림 |
| 34 | https://www.customerexperiencedive.com/news/klarna-reinvests-human-talent-customer-service-AI-chatbot/747586/ | 200 | 200 Klarna changes its AI tune and again recruits huma | 열림 |
| 35 | https://openai.com/index/klarna/ | 403→GET 403 | 200 Klarna's AI assistant does the work of 700 full-ti | 열림. curl 봇 차단, 브라우저 200·제목 일치 |
| 36 | https://www.saastr.com/ | 200 | 403 SaaStrAI / B2B + AI Community, Events, Leads | 열림. 브라우저 응답 403이지만 화면은 정상 표시(curl 200) |
| 37 | https://www.latent.space/p/ai-engineer | 200 | 200 The Rise of the AI Engineer — Latent Space | 열림 |
| 38 | https://hamel.dev/blog/posts/evals-faq/ | 200 | 200 AI Evals: Everything You Need to Know – Hamel’s Bl | 열림 |
| 39 | https://maven.com/ | 200 | 200 Maven / Unlock your career growth | 열림 |
| 40 | https://aakashgupta.medium.com/i-interviewed-100-ai-product-managers-heres-what-they-actually-do-9e55d393a287 | 403→GET 403 | 200 I Interviewed 100+ AI Product Managers. Here’s Wha | 열림. curl 봇 차단, 브라우저 200·제목 일치 |
| 41 | https://www.lennysnewsletter.com/p/ai-and-product-management-marily | 200 | 200 AI and product management / Marily Nika (Meta, Goo | 열림 |
| 42 | https://a16z.com/services-led-growth/ | 200 | 200 Trading Margin for Moat: Why the Forward Deployed | 열림 |
| 43 | https://www.dbreunig.com/2025/08/21/a-guide-to-ai-titles.html | 200 | 200 Making Sense of AI Job Titles | 열림 |
| 44 | https://www.ibm.com/think/topics/agentops | 200 | 200 What is AgentOps? / IBM | 열림 |
| 45 | https://galileo.ai/blog/best-llm-reliability-solutions | 200 | 200 8 Best LLM Reliability Solutions for Production / | 열림 |
| 46 | https://www.youngju.dev/blog/culture/2026-03-23-si-industry-ai-transformation-career-guide | 200 | 200 | 도메인 만료(주차 페이지 /lander). 옮긴 주소·Wayback 보관본 모두 없음. 링크로 감싸지 않고 둠(저자 결정) |
| 47 | https://www.youngju.dev/blog/ai-platform/2026-03-09-ai-platform-llm-monitoring-langsmith-langfuse-arize | 200 | 200 | 도메인 만료(주차 페이지 /lander). Wayback 보관본(2026-05-09, 같은 제목·날짜 확인)으로 교체 |
| 48 | https://www.kmjournal.net/news/articleView.html?idxno=7040 | 404→GET 200 | 200 GPU는 쌓였는데 사람이 없다… 한국 AI 발목 잡는 인력난 < AI·XR < 뉴스 < 뉴 | 열림. HEAD만 404, GET·브라우저 200, 기사 제목 일치 |
| 49 | https://devocean.sk.com/ | 200 | 200 데보션 (DEVOCEAN) 기술 블로그 & 커뮤니티 | 열림 |
| 50 | https://medium.com/lbox-team/ | 403→GET 403 | 200 LBOX Team | 열림. curl 봇 차단, 브라우저 200·제목 일치 |
| 51 | https://medium.com/daangn/ | 403→GET 403 | 200 당근 기술 블로그 | 열림. curl 봇 차단, 브라우저 200·제목 일치 |
| 52 | https://www.smartfn.co.kr/news/articleView.html?idxno=110739 | 404→GET 200 | 200 LG CNS, AI 인재 확보 위해 경력직 전문가 모집 < 컴퓨팅 < IT·과학 < 기사본 | 열림. smartbizn.com 같은 기사 번호로 리다이렉트, 본문에 "11개 직무"·"1000명" 확인. 주소는 그대로 |
| 53 | https://careers.upstage.ai/ | 200 | 200 Upstage 채용 | 열림 |
| 54 | https://www.jobkorea.co.kr/goodjob/tip/view?News_No=22472 | 200 | 200 잡코리아 / 퇴근 후 밋업 PMPO DAY 생생한 현장 스케치 후기 | 열림 |
| 55 | https://okky.kr/ | 200 | 200 OKKY - All That Developer | 열림 |
| 56 | https://velog.io/ | 200 | 200 velog | 열림 |
| 57 | https://www.threads.com/@jmhong2020/post/DQSPetlEufT | 200 | 200 "AI 에이전트" 관련 대기업 채용 트렌드 분석 결과 1. 연구자🧑‍🔬 < 응용 엔지니어🧑 | 열림 |
| 58 | https://sudormrf.run/2024/08/17/langsmith_review/ | 200 | 200 LangSmith, 사용 후기 | 열림 |
| 59 | https://langfuse.com/kr | 200 | 200 Langfuse - 한국어 개요 - Langfuse | 열림 |
| 60 | https://www.levels.fyi/companies/anthropic/salaries/software-engineer | 405→GET 405 | 200 Anthropic Software Engineer Salary / $483K-$1.41M+ | 열림. curl 봇 차단, 브라우저 200·제목 일치 |
| 61 | https://www.levels.fyi/companies/openai/salaries/software-engineer | 405→GET 405 | 200 OpenAI Software Engineer Salary / $249K-$1.89M+ / | 열림. curl 봇 차단, 브라우저 200·제목 일치 |
| 62 | https://www.teamblind.com/ | 200 | 200 Blind - Anonymous and Professional Community | 열림 |
| 63 | https://www.sundeepteki.org/forward-deployed-engineer.html | 200 | 200 Forward Deployed Engineer Coaching / FDE Career Pr | 열림 |
| 64 | https://job-boards.greenhouse.io/anthropic/jobs/4990535008 | 200 | 200 Jobs at Anthropic | (11장 본문 출처) 공고 마감, 채용 목록 오류 화면으로 이동. Wayback 보관본(2026-02-13, 제목 "Research Engineer, Model Evaluations" 확인)으로 교체 |

### 빌드·검증

- 서지 정보(저자·제목·연도)는 바꾸지 않았다. 주소를 뺀 원고 텍스트는 v1.1.6과 앞부속 버전·판 이력 줄만 다르다(스크립트 대조).
- 통합 원고: 같은 순서·구분자로 `chapters/`를 재조립.
- EPUB: 하네스 `build_epub.sh`(book-writer 1.11.0)로 `docs/epub/코드-너머의-직업들-v1.1.7.epub`, epubcheck 0 오류·0 경고. EPUB 안 외부 `<a href>` 63개, 인용 표기 0개.
- 웹: 같은 pandoc 설정(`--toc --toc-depth=2`, html5)과 표 감싸개 후처리로 v1.1.6 원고를 변환한 구간이 기존 `docs/index.html`과 같음을 확인한 뒤 v1.1.7 원고로 교체했다. hero 판본 v1.1.7.
- Playwright(390·1440): 문서 폭 = 화면 폭, 넘침 0, 본문 주소 링크(a.uri) 63개 중 화면 밖으로 나가는 것 0(기존 `main p, main li { overflow-wrap:break-word }`로 줄바꿈). 페이지 a 태그 185 → 247개. 목차 링크 183개 모두 본문 id와 맞음, 오프닝 영상·발표 자료 링크 유지. 덱은 건드리지 않았다.

## 참고문헌 한 항목 삭제 — v1.1.8 (2026-11-07)

- 저자 결정: v1.1.7에서 주소를 찾지 못한 참고문헌 7절 영주.dev. "SI 산업의 AI 대전환." 2026-03-23 한 줄을 뺐다(도메인 만료, 옮긴 주소·Wayback 보관본 없음). 본문의 영주.dev 언급, 12장 박스, 머리말은 그대로 두었다. Perez 2002 보관본 주소도 그대로다.
- 원고 차이: 앞부속 버전·판 이력 한 줄, 참고문헌 한 줄뿐이다.
- EPUB: 하네스 `build_epub.sh`(book-writer 1.11.0)로 `docs/epub/코드-너머의-직업들-v1.1.8.epub`, epubcheck 0 오류·0 경고, 외부 `<a href>` 63개.
- 웹: 같은 pandoc 설정과 표 감싸개로 v1.1.7 원고를 변환한 구간이 기존 `docs/index.html`과 같음을 확인한 뒤 v1.1.8 원고로 교체, hero 판본 v1.1.8.
- Playwright(390·1440): 문서 폭 = 화면 폭, 넘침 0, 주소 링크 63개 넘침 0, a 태그 247개(뺀 항목은 링크가 없었음), 목차 링크 183개 모두 맞음, 오프닝 영상·발표 자료 링크 유지.

## 전작 표기·감사 문장 정정 — v1.1.9 (2026-11-07)

- 저자 확인 사실: 전작 「코드 너머의 시대」는 하네스로 쓴 웹 공개 책이고 한빛미디어 책이 아니다. 정식 출판된 책은 2025년 공저 「코드너머, 회사보다 오래 남을 개발자」뿐이다.
- 앞부속: 「**전작:** 코드 너머의 시대 (한빛미디어)」 → 「**전작:** 코드 너머의 시대 (웹 공개, <https://ksangki.github.io/beyond-code-era/>)」. 주소 응답 200 확인.
- 머리말 감사의 말: 저자 결정으로 「특히 한국 시장 분석에 영주.dev, DEVOCEAN, 카카오스타일 PM 이미준, 한빛미디어 편집팀이 도움을 주셨습니다. 한국 SI 산업의 진화 로드맵은 영주.dev의 분석에 빚지고 있습니다.」 두 문장(한 문단)을 뺐다. 앞뒤 문단은 그대로 이어져 연결 문장을 보태지 않았다. 본문의 영주.dev 인용·12장 박스는 그대로다.
- 원고 차이: 앞부속 전작·버전·판 이력 줄, 머리말 한 문단뿐이다. 발표 자료(deck/slides.py, docs/presentation/)와 README에는 같은 감사 문장·한빛 표기가 없어 덱은 다시 만들지 않았다. 내부 기획 문서(02_plan.md, 03_review.md, cover_prompt.md, book_manifest.json의 expected_length.format)에 남은 「한빛」 언급은 독자 지면에 나오지 않아 두었다.
- EPUB: 하네스 `build_epub.sh`(book-writer 1.11.0)로 `docs/epub/코드-너머의-직업들-v1.1.9.epub`, epubcheck 0 오류·0 경고, EPUB 안 「한빛」 0건.
- 웹: 같은 pandoc 설정과 표 감싸개로 v1.1.8 원고를 변환한 구간이 기존 `docs/index.html`과 같음을 확인한 뒤 v1.1.9 원고로 교체, hero 판본 v1.1.9. 페이지 「한빛」 0건.
- Playwright(390·1440): 문서 폭 = 화면 폭, 넘침 0, 주소 링크 64개(전작 주소 1개 추가), a 태그 247 → 248, 목차 링크 183개 모두 맞음, 오프닝 영상·발표 자료 링크 유지.
