# Cover Design Log — 코드 너머의 직업들

## Version 1 (2026-05-12)

- **콘셉트:** C (타이포그래피 중심, 미니멀 + 시리즈 정체성)
- **도구:** ImageMagick 7.1.2-18 (typography fallback)
- **사이즈:** 1600 × 2560 (portrait, 1.6:1)

### 디자인 의도

- *코드 너머의* 시리즈 두 번째 책으로서 시리즈 정체성 유지 (전작 *코드 너머의 시대*와 같은 색감 계열)
- 핵심 단어 "직업들"을 시안(#5fb4ff)으로 강조해 본서가 *직업 도감*임을 시각적으로 드러냄
- 중앙의 가는 라인 + 점이 *인프라가 깔린 풍경*과 *그 위의 자리*를 분리하는 미니멀 모티프
- AI 인프라의 차분한 톤(딥 네이비)에 일렉트릭 블루 액센트

### 색상 팔레트

- 배경 그라데이션: `#0a0e27` (top) → `#1a2444` (bottom) — 짙은 네이비
- 시리즈 라벨: `#e8edf5` (밝은 화이트)
- 핵심 단어: `#5fb4ff` (일렉트릭 블루)
- 부제: `#a8b8d8` (소프트 그레이)
- 시리즈 표기: `#6a7da0` (디스플레이용 다크 그레이)
- 저자: `#c8d8f0` (페일 블루)
- 액센트 라인/점: `#5fb4ff` / `#7fc4ff`

### ImageMagick 명령

```bash
magick -size 1600x2560 gradient:'#0a0e27-#1a2444' \
  -fill '#5fb4ff' -draw "rectangle 200,1280 1400,1284" \
  -fill '#7fc4ff' -draw "circle 800,1280 820,1280" \
  -gravity center \
  -font '.Apple-SD-Gothic-NeoI-Bold' -pointsize 130 -fill '#e8edf5' \
  -annotate +0-680 "코드 너머의" \
  -font '.Apple-SD-Gothic-NeoI-Heavy' -pointsize 200 -fill '#5fb4ff' \
  -annotate +0-440 "직업들" \
  -font '.Apple-SD-Gothic-NeoI-Medium' -pointsize 64 -fill '#a8b8d8' \
  -annotate +0+90 "GPU 위에서" \
  -annotate +0+180 "일하는 사람들" \
  -font '.Apple-SD-Gothic-NeoI-Light' -pointsize 42 -fill '#6a7da0' \
  -annotate +0+600 "—  코드 너머의 시리즈 II  —" \
  -font '.Apple-SD-Gothic-NeoI-Medium' -pointsize 56 -fill '#c8d8f0' \
  -annotate +0+1080 "김상기" \
  /Users/1112022/source/github/book-writer/beyond-code-jobs/cover.png
```

### 결과

- **파일:** `cover.png` (134KB)
- **해상도:** 1600 × 2560 ✓
- **포맷:** PNG, 16-bit sRGB
- **썸네일 검증:** 200×320 축소해도 제목 "직업들" 가독.
- **저자 표기:** "김상기" 중앙 하단.

### Notes

- ImageMagick typography-only 폴백. 이미지 생성 모델로 회로 패턴이나 데이터센터 모티프를 더하면 더 풍부해질 수 있음.
- 시리즈 라벨 *"코드 너머의 시리즈 II"*가 표지 정면에 명시되어 전작 독자가 즉시 인지 가능.
- 한빛미디어 출간 단계에서 표지 디자이너의 리디자인을 받기 좋은 *베이스 디자인*. EPUB 전자책의 *내장 표지*로는 충분히 작동.
