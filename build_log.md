# 빌드 로그 — 코드 너머의 직업들 v1.0.0

## 빌드 1 (2026-05-12)

### 입력

- 원고: `beyond-code-jobs/04_manuscript.md` (288,703 bytes / 152,685 자 / 3,485 줄)
- 표지: `beyond-code-jobs/cover.png` (133,634 bytes, 1600×2560)
- 매니페스트: `beyond-code-jobs/book_manifest.json` (2,337 bytes)

### 빌드 명령

```bash
bash .claude/skills/epub-build/scripts/build_epub.sh beyond-code-jobs
```

내부적으로 pandoc 3.9.0.2가 EPUB 3 표준으로 변환.

### 결과

- **파일:** `코드-너머의-직업들-v1.0.0.epub` (프로젝트 루트)
- **크기:** 261,615 bytes (약 256KB)
- **압축 풀린 내부 총합:** 575,570 bytes
- **내부 파일 수:** 36개 (XHTML 26 + 메타·CSS·이미지 등)
- **Pandoc exit code:** 0 (성공)

### 내부 구조 요약

```
EPUB/text/ch001.xhtml ~ ch026.xhtml   본문 26 챕터 분할
EPUB/text/cover.xhtml                  표지 페이지
EPUB/content.opf                       매니페스트
EPUB/toc.ncx                           구식 NCX (호환성)
EPUB/nav.xhtml                         EPUB 3 Nav 문서
EPUB/images/cover.png                  임베드된 표지
EPUB/styles/stylesheet.css             pandoc 기본 CSS
```

### 검증

- ✅ EPUB 파일 생성됨
- ✅ 파일 크기 ≥ 50KB (요구) — 실제 256KB
- ✅ `unzip -l`로 내부 구조 확인 가능 (36 파일)
- ✅ 26 챕터가 정상 분할 (ch001 ~ ch026)
- ⚠️ `epubcheck` 미설치로 외부 표준 검증은 미수행. 필요 시 `brew install epubcheck && epubcheck 코드-너머의-직업들-v1.0.0.epub`로 재검증 가능.

### 메타데이터

| 필드 | 값 |
|---|---|
| title | 코드 너머의 직업들 |
| subtitle | GPU 위에서 일하는 사람들 |
| author | 김상기 |
| language | ko |
| version | 1.0.0 |
| series | 코드 너머의 (시리즈 II) |
| 전작 | 코드 너머의 시대 |

### 시리즈 비교

| 책 | 파일 크기 | 분량 비고 |
|---|---|---|
| 코드 너머의 시대 (전작) | 123,974 bytes | 9장, 약 220쪽 |
| **코드 너머의 직업들 (본서)** | **261,615 bytes** | 14장 + 막간 + 부록, 약 254쪽 (본문 152,685 자) |

본서가 전작의 약 2.1배 분량. 본론 5개 직업 도감(7~11장)이 무게중심.

### 빌드 파이프라인 요약

1. **Phase 1 — 리서치:** web/paper/community 세 갈래 병렬 리서치 → `research/*.md` (총 ~125KB)
2. **Phase 2 — 통합 레퍼런스:** `01_reference.md` (41KB / 604 줄, 챕터별 매핑)
3. **Phase 3 — 저술 계획:** `02_plan.md` (Rev 1 → Rev 2 by review)
4. **Phase 4 — 계획 리뷰:** `03_review.md` (Critical 5 + Should 8 + Nice 4 — 모두 반영)
5. **Phase 5 — 챕터 저술:** `chapters/*.md` 19개 파일 (프롤로그·14장·막간·에필로그·부록 + front matter·PART intro·bibliography)
6. **Phase 6 — 합본:** `04_manuscript.md` (셸 cat으로 26개 파일 통합)
7. **Phase 7 — 표지:** `cover.png` (ImageMagick typography 폴백, 1600×2560)
8. **Phase 8 — EPUB 빌드:** 본 파일

### 다음 단계 (선택)

- **epubcheck 검증:** `brew install epubcheck && epubcheck 코드-너머의-직업들-v1.0.0.epub`
- **eBook 리더 시각 확인:** Apple Books, Calibre, Kindle Previewer
- **표지 디자이너 리디자인:** 한빛미디어 출간 단계의 정식 표지 작업
- **버전 증가 규칙:** 오탈자 패치 1.0.1 / 챕터 개정 1.1.0 / 구조 재편 2.0.0
