# V2-5 컴포넌트 스펙 결과물

피그마 실존 컴포넌트 8개 / 구현 코드 없음 / V2 토큰 참조

---

## 1. Button — full-width (`button/next`)

피그마 ID: `151:6436`

| 항목 | 값 |
|---|---|
| Variants | `default` (button=on), `disabled` (button=off) |
| Width | 100% (full) |
| Height | `54px` |
| Radius | `radius-full` (9999px) |
| Padding X | `space-5` (20px) |
| Font | `size-title` / `weight-medium` (18px / 500) |
| Text color | `text-on-brand` (#FFFFFF) |
| BG — default | `brand` (#0077CE) |
| BG — disabled | `disabled` (#BBBBBB) |

---

## 2. Button — circle (`button/o` / `button/x`)

피그마 ID: `151:6473` (O), `151:6476` (X)

| 항목 | 값 |
|---|---|
| Variants | `default` (button=on), `disabled` (button=off) |
| Size | `120 × 120px` |
| Radius | `radius-full` (9999px) |
| BG — default | `brand` (#0077CE) |
| BG — disabled | `disabled` (#BBBBBB) |
| 차이 | O버튼 / X버튼 — 내부 아이콘만 다름, 구조 동일 |

---

## 3. Card

홈 화면에서 3가지 형태로 사용됨.

### 3-1. Card — default (흰 카드)

| 항목 | 값 |
|---|---|
| Variants | 없음 (단일) |
| BG | `bg-card` (#FFFFFF) |
| Radius | `radius-lg` (12px) |
| Shadow | `0px 0px 16px rgba(0,0,0,0.08)` |
| Padding X | `space-5` (20px) |
| Padding Y | `space-4` (16px) |

### 3-2. Card — action-brand (버디 보내기 카드)

| 항목 | 값 |
|---|---|
| Variants | 없음 (단일) |
| BG | `gradient: brand-light → brand` (`#43A6EF → #0077CE`, 144.86deg) |
| Radius | `radius-md` (10px) |
| Shadow | `0px 0px 8px rgba(120,144,238,0.42)` (glow) |
| Border | `rgba(136,197,242,0.2)` |
| Height | `120px` |
| Text color | `text-on-brand` (#FFFFFF) |

### 3-3. Card — action-surface (AI 챗봇 카드)

| 항목 | 값 |
|---|---|
| Variants | 없음 (단일) |
| BG | `gradient: #FFFFFF → #DFE2E5` (144.86deg) |
| Radius | `radius-md` (10px) |
| Shadow | `0px 0px 8px rgba(0,0,0,0.08)` |
| Border | `border-card` (#FFFFFF) |
| Height | `120px` |
| Text color | `brand` (#0077CE) |

---

## 4. ProgressBar

피그마: 레벨 진행바 (홈화면 미션 카드 내부)

| 항목 | 값 |
|---|---|
| Variants | 없음 (단일) |
| Track BG | `bg-track` (#EDEDED) |
| Fill | `brand` (#0077CE) |
| Height | `12px` |
| Radius | `radius-full` (9999px) |
| 레벨 라벨 | `caption` textStyle / `brand` color (Lv.02, Lv.03) |

---

## 5. Checkbox

피그마 ID: `53:2537`

| 항목 | 값 |
|---|---|
| Variants | `on` (Property 1=On), `off` (Property 1=Off) |
| Size | `20 × 20px` |
| 아이콘 내부 | 피그마 SVG 에셋 사용 |

---

## 6. Navigation — bottom

피그마 ID: `151:3797`

| 항목 | 값 |
|---|---|
| Variants | `home`, `report`, `my` (활성 탭 기준) |
| BG | `bg-card` (#FFFFFF) |
| Shadow | `0px 0px 8px rgba(0,0,0,0.08)` |
| Padding top | `space-3` (12px) |
| Padding bottom | `34px` — iOS safe area 하단 여백 (디바이스 환경 고정값, spacing 토큰 외) |
| Padding X | `space-4` (16px) |
| Active color | `brand` (#0077CE) |
| Inactive color | `text-inactive` (#BBBBBB) |
| Label | `label` textStyle (11px / Medium) |
| Icon size | `24 × 24px` |
| 탭 항목 | HOME, REPORT, MY |

---

## 7. TopBar

피그마 ID: `87:3487`

| 항목 | 값 |
|---|---|
| Variants | 없음 (단일) |
| BG | 투명 (페이지 배경 `bg-page` 그대로) |
| Width | `393px` (디바이스 너비) |
| Height | `48px` |
| Padding top | `space-2` (8px) |
| Padding bottom | `space-4` (16px) |
| Padding X | `space-4` (16px) |
| 좌측 | Logo 컴포넌트 |
| 우측 | icon/notification + icon/settings (`24 × 24px`) |
| Logo 텍스트 | "Working Buddy" / 16px / **Bold(700)** / `brand` (#0077CE) |

> ⚠️ **토큰 불일치 발견**: TopBar의 로고 텍스트가 Bold(700)을 사용하지만 V2 타이포그래피 토큰에서 Bold를 제외했음. V3에서 처리 방향 결정 필요 — (A) `weight-bold` 토큰 추가 / (B) SemiBold(600)로 근사.

---

## 8. Logo

피그마 ID: `132:3446`

| 항목 | 값 |
|---|---|
| Variants | Default, gray, White, text_white, text_blue, logo7, Point, gray_point, Black (9종) |
| 아이콘 단독 크기 | `24 × 24px` |
| 텍스트+아이콘 크기 | `147 × 24px` |
| 텍스트 | "Working Buddy" |

---

## 미결 사항 (V3 검토 필요)

| 항목 | 내용 |
|---|---|
| Shadow 토큰 | 세 가지 shadow값이 토큰화되지 않음 → V3에서 elevation 정의 필요 |
| TopBar Bold | `weight-bold(700)` 추가 여부 결정 필요 |
| Nav padding-bottom 34px | spacing 토큰 범위 밖 고정값 — 처리 방식 결정 필요 |
