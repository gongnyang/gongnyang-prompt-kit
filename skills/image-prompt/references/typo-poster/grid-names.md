# 포스터 그리드 이름 24 — 판 나누기 · 놓는 법 · 글자 놓기 (grid-names)

> 포스터를 "세련되게"로 시키면 요소가 위에서 아래로 쌓이거나 가운데에 모입니다. **판을 어떻게 나누고(그리드 10), 칸 위에 어떻게 앉히고(놓는 법 8), 제목과 정보를 어떻게 놓을지(글자 놓기 6)를 이름과 칸 수로 박습니다.** TP·P·C3 포스터 어느 패턴과도 겹쳐 쓰는 **판 짜기 레이어**이며, 패턴 문법(질감·팔레트)은 각 패턴 파일이 정합니다.
>
> 출처: 기팅 @giting.kr 「GRID RACK 24 TYPES」(Threads, 2026-11) · `hanmariyang/giting-skills` grid-menu v0.1.0(MIT). 한글·영문 이름과 「평소 하는 말」은 원문 그대로이고, 정의는 줄였으며, EN 토큰은 공냥 철칙(긍정형·수치)에 맞춰 새로 썼습니다.

## 쓰는 법

1. 레시피 표에서 포스터 종류를 고르거나, 그리드 1 + 놓는 법 1–2 + 글자 놓기 1–2를 직접 고릅니다.
2. 아래 **프롬프트 칸**을 Scene 맨 앞 문장에 채웁니다. 이름(EN) + **칸 수** + **여백 %** + **각 요소가 차지할 칸**을 함께 써야 효과가 납니다. 이름만 쓰면 효과가 약합니다.
3. 레이아웃 그리드는 **보이지 않는 판**이므로 `invisible`로 씁니다. 철칙 #6(한 캔버스 멀티패널 금지)은 컷을 여러 개 나누는 것을 막는 규칙이고, 한 컷 안의 판 짜기와는 무관합니다.

## 프롬프트 칸 (Scene 첫 문장)

```
Layout on an invisible [GRID_EN] of [N columns x M rows], outer margin and gutter both [4]% of width;
[ELEMENT] spanning [cols x rows] modules at the [position]; headline as a [TITLE_EN] in the [cols x rows] modules [position];
date and venue as a small [INFO] in the [position] module; every edge on a module line, asymmetric flush-left composition.
```

슬롯(`[…]`)은 작성 전용입니다. 출력에 남으면 `E-SLOT-LEAK`입니다.

## ① 그리드 종류 (판 나누기) 10

| # | 한글 | EN | 평소 하는 말 | 한 줄 정의 | EN 토큰 |
|---|---|---|---|---|---|
| 01 | 원고 그리드 | Manuscript Grid | 가운데 큰 글 상자 하나 | 여백 안쪽에 큰 사각 영역 하나만 둔다 | `manuscript grid: one large text block inside 8% top and bottom, 10% side margins` |
| 02 | 단 그리드 | Column Grid | 세로로 몇 줄 나눠서 | 세로 단 여러 개, 제목은 단을 걸치고 글은 한 단씩 | `3-column grid, headline spanning all 3 columns, body text flowing column by column` |
| 03 | 모듈 그리드 | Modular Grid | 바둑판 칸 | 가로세로 같은 칸에 사진·글을 칸 단위로 놓는다 | `invisible modular grid of 4 columns x 6 rows, margin and gutter both 4% of width, every element snapped to module edges` |
| 04 | 계층 그리드 | Hierarchical Grid | 중요한 거 크게 나머지 작게 | 칸 크기를 중요도로 정한다 | `hierarchical grid: photo field half the canvas, headline field a quarter, remaining fields share the rest, edges aligned` |
| 05 | 기준선 그리드 | Baseline Grid | 글줄 높이 맞추기 | 모든 글줄을 같은 간격 가로선 위에 앉힌다 | `all text lines sitting on one shared baseline rhythm, lines level across columns` |
| 06 | 겹친 그리드 | Compound Grid | 두 그리드 섞기 | 단 수가 다른 그리드 둘을 겹친다 | `compound grid: 2-column structure in the upper half, 3-column structure in the lower half, on a shared 6-column base` |
| 07 | 3분할 그리드 | Rule of Thirds Grid | 삼등분 선 | 3등분 선 4개와 교차점 4개로 놓는다 | `rule-of-thirds layout: subject on the upper-right intersection, headline starting at the lower-left intersection` |
| 08 | 사선 그리드 | Oblique Grid | 삐딱하게 기울여서 | 그리드 전체를 한 각도로 기울인다 | `oblique grid: the whole 4-column grid rotated -30 degrees, all text set on the tilted columns, one single angle` |
| 09 | 방사 그리드 | Radial Grid | 한 점에서 뻗어 나가게 | 한 점에서 뻗는 선을 따라 놓는다 | `radial grid: rays fanning from the bottom-left corner every 15 degrees, headline words set along the rays` |
| 10 | 동심원 그리드 | Concentric Grid | 과녁처럼 원 여러 개 | 중심을 둘러싼 원 여러 개를 칸 대신 쓴다 | `concentric grid: 4 evenly spaced rings around the center, headline running along the outer ring, one image inside the inner ring` |

## ② 놓는 법 (칸 위에 앉히기) 8

| # | 한글 | EN | 평소 하는 말 | 한 줄 정의 | EN 토큰 |
|---|---|---|---|---|---|
| 11 | 칸 묶기 | Spanning Modules | 여러 칸 합쳐서 크게 | 요소 하나가 여러 칸을 묶어 차지, 칸 선은 지킨다 | `photo spanning the top 4x3 modules, all four edges on module lines` |
| 12 | 가장자리 붙이기 | Edge Hugging | 모서리에 딱 붙여서 | 요소를 가장자리 여백선에 붙이고 가운데를 비운다 | `headline hugging the top-left margin, info hugging the bottom-right margin, open empty center` |
| 13 | 초점 고립 | Focal Point Isolation | 하나만 덩그러니 | 넓은 빈 공간에 요소 하나, 나머지는 아주 작게 | `one red circle at 8% of canvas area, 40% from the top, all other text tiny along the bottom margin` |
| 14 | 긴장 배치 | Visual Tension | 닿을 듯 말 듯 | 요소 둘을 닿기 직전까지 붙이거나 판 끝에 걸친다 | `circle almost touching the last letter of the headline, one third of it cropped by the right edge` |
| 15 | 그리드 깨기 | Breaking the Grid | 하나만 칸 밖으로 | 하나만 칸 선을 넘고 나머지는 칸을 지킨다 | `everything locked to the grid except the photo, which crosses its module line by half a module` |
| 16 | 크기 대비 | Scale Contrast | 엄청 크게랑 엄청 작게 | 최대·최소 크기 차이를 크게 벌린다 | `headline at 90% of canvas width, info text tiny, only these two type sizes` |
| 17 | 여백 남기기 | Active White Space | 비워 두기 | 칸 일부를 일부러 비운다. 빈 칸도 한 칸 | `more than half of the 4x6 modules left as calm empty field, content only in the top two rows and the bottom row` |
| 18 | 축 정렬 | Axis Alignment | 선 하나에 다 맞추기 | 제목·사진·정보의 한쪽 가장자리를 보이지 않는 선 하나에 맞춘다 | `headline, photo and info all flush-left on one invisible vertical axis at one third from the left` |

## ③ 글자 놓기 (제목과 정보) 6

| # | 한글 | EN | 평소 하는 말 | 한 줄 정의 | EN 토큰 |
|---|---|---|---|---|---|
| 19 | 세로 제목 | Vertical Title | 제목 세워서 | 제목을 90도 돌려 한 단 높이를 따라 세운다 | `headline rotated 90 degrees, filling the full height of the left column, reading bottom to top` |
| 20 | 사선 제목 | Angled Title | 제목만 비스듬히 | 제목 한 줄만 기울여 판을 가로지른다 | `headline alone tilted -35 degrees, crossing from top-left to bottom-right at full canvas width` |
| 21 | 쌓은 제목 | Stacked Title | 단어 하나씩 줄 바꿔서 | 단어마다 줄을 바꿔 쌓고 줄마다 같은 폭으로 꽉 채운다 | `stacked headline, one word per line, each line enlarged in font size to the full 4-column width, tight 0.9 leading, letters set solid at normal spacing` |
| 22 | 쪼갠 제목 | Split Word | 단어 중간에서 끊어서 | 한 단어를 칸 폭에 맞춰 중간에서 끊어 여러 줄로 | `single word broken mid-word into clean 3-letter lines, flush to the left column line` |
| 23 | 정보 블록 | Info Block | 날짜 장소 작게 모아서 | 날짜·시간·장소·주최를 작은 글 한 덩어리로 한 칸에 | `date and venue as one small flush-left info block in the bottom-right module, one item per line` |
| 24 | 잘린 큰 글자 | Cropped Type | 글자가 판 밖으로 잘리게 | 글자를 판보다 키워 일부가 판 밖으로 잘린다 | `headline 40% of canvas height, its bottom third cropped by the bottom edge, first letter fully visible` |

헷갈리는 쌍: 단↔모듈(가로로도 나뉘면 모듈) · 모듈↔계층(칸 크기가 같으면 모듈) · 방사↔동심원(선이면 방사, 원이면 동심원) · 사선 그리드↔사선 제목(판 전체가 기울면 그리드) · 칸 묶기↔그리드 깨기(칸 선을 넘으면 깨기) · 쌓은↔쪼갠 제목(단어 단위면 쌓은) · 잘린 큰 글자↔쌓은 제목(판 밖으로 잘리면 잘린).

## 레시피 4

| 포스터 | 조합 | 공냥 패턴 짝 |
|---|---|---|
| 전시 | 모듈 그리드 + 칸 묶기 + 가장자리 붙이기 + 쌓은 제목 + 정보 블록 | TP6·P9 |
| 공연·파티 | 사선 그리드 + 사선 제목 + 긴장 배치 + 정보 블록 | TP11·P7 |
| 강연·모임 | 단 그리드 + 기준선 그리드 + 축 정렬 + 세로 제목 + 정보 블록 | TP17·C3 |
| 공지·오픈 | 원고 그리드 + 초점 고립 + 잘린 큰 글자 + 여백 남기기 + 정보 블록 | P10·C3 |

## 완성 예 (전시 레시피, 포맷 A)

```
Scene: an exhibition poster laid out on an invisible modular grid of 4 columns x 6 rows, outer
margin and gutter both 4% of width; a calm grey seascape photograph spanning the top 4x3 modules,
all four edges on module lines; the two-word stacked headline in the 4x2 modules below, one word
per line, each line enlarged in font size to the full 4-column width, tight 0.9 leading, letters
set solid at normal spacing; date and venue as one small flush-left info block hugging the
bottom-right margin; asymmetric flush-left composition, open warm-white field around the blocks.
Camera: flat frontal print composition, poster seen straight on.
Lighting: even diffuse light, flat printed surface.
Color grading: muted cool greys, warm paper white #F2F1EE, ink black #151515, slate #5D6063.
Texture/Medium: offset-printed matte poster paper, crisp ink edges.
Text-in-image: headline "느린 바다" in heavy bold sans-serif; info "2026.12.05 – 2027.01.18" and
"부산 영도 전시실" in small medium sans-serif. All text appears once, perfectly legible — no duplicate text, no extra words, no invented glyphs, no watermark.
AR 4:5
```

## 실측 메모 (HTML 프록시, 2026-11-08)

같은 전시 포스터를 HTML로 그리게 하고 헤드리스 렌더 DOM을 판정했습니다(유료 이미지 API는 쓰지 않았습니다).

- 기본 지시 A: 4×6 모듈에 맞춘 판 0/6, 제목이 폭을 채운 판 0/6. 키트의 기존 영역 문법 C(bottom-left·caption 등): 0/6, 0/6.
- 이름 지시 B: 4×6 모듈 6/6, 제목 폭 채움 6/6. 하지만 5/6에서 쌓은 제목을 **자간·양끝 정렬로 벌려** 채웠습니다(「느 … 린」).
- 보정 B2(`enlarged in font size … letters set solid at normal spacing`): 3/3 모두 글자 크기로 채웠습니다. 위 토큰 #21이 이 보정을 반영한 것입니다.
- 쌓은 제목은 **줄마다 글자 수가 비슷할 때**만 씁니다. 「임플란트 / 상담 / 주간」처럼 4자와 2자를 같은 폭에 맞추면 짧은 줄이 가로로 늘어나 납작해지고 줄끼리 격칩니다. `임플란트 / 상담 주간`처럼 글자 수를 맞춰 끊으세요.
- 가운데 정렬 자체는 A에서도 0/6이었습니다(최신 모델은 기본이 좌측 정렬). 이 레이어의 효과는 **칸을 지키는 것과 제목 스케일**에서 나옵니다.
- gpt-image-2에서 칸을 얼마나 지키는지는 아직 확인하지 않았습니다. 첫 생성 때 칸 위치를 눈으로 확인하세요.
