# 컴포넌트 스펙 (최종)

최종 확정 (V3) — 상세 과정: [process/v3-result.md](../process/v3-result.md)

---

## 1. Button — full-width

최종 확정 (V3)

피그마 ID: `151:6436` (`button/next`)

| 항목 | 값 |
|---|---|
| Variants | `default` (on), `disabled` (off) |
| Width | 100% (full) |
| Height | `54px` |
| Radius | `radius-full` |
| Padding X | `space-5` |
| Font | `size-title` / `weight-medium` |
| Text color | `text-on-brand` |
| BG — default | `brand` |
| BG — disabled | `disabled` |

---

## 2. Button — circle

최종 확정 (V3)

피그마 ID: `151:6473` (O), `151:6476` (X)

| 항목 | 값 |
|---|---|
| Variants | `default` (on), `disabled` (off) |
| Size | `120 × 120px` |
| Radius | `radius-full` |
| BG — default | `brand` |
| BG — disabled | `disabled` |
| 비고 | O / X — 내부 아이콘만 다름, 구조 동일 |

---

## 3. Card — default

최종 확정 (V3)

| 항목 | 값 |
|---|---|
| Variants | 없음 (단일) |
| BG | `bg-card` |
| Radius | `radius-lg` |
| Shadow | `shadow-card` |
| Padding X | `space-5` |
| Padding Y | `space-4` |

---

## 4. Card — action-brand

최종 확정 (V3)

(버디 보내기 카드)

| 항목 | 값 |
|---|---|
| Variants | 없음 (단일) |
| BG | gradient `brand-light → brand` (`#43A6EF → #0077CE`, 144.86deg) |
| Radius | `radius-md` |
| Shadow | `shadow-glow` |
| Border | `rgba(136,197,242,0.2)` |
| Height | `120px` |
| Text color | `text-on-brand` |

---

## 5. Card — action-surface

최종 확정 (V3)

(AI 챗봇 카드)

| 항목 | 값 |
|---|---|
| Variants | 없음 (단일) |
| BG | gradient `#FFFFFF → #DFE2E5` (144.86deg) |
| Radius | `radius-md` |
| Shadow | `shadow-card` |
| Border | `border-card` |
| Height | `120px` |
| Text color | `brand` |

---

## 6. ProgressBar

최종 확정 (V3)

| 항목 | 값 |
|---|---|
| Variants | 없음 (단일) |
| Track BG | `bg-track` |
| Fill | `brand` |
| Height | `12px` |
| Radius | `radius-full` |
| 레벨 라벨 | `caption` textStyle / `brand` color |

---

## 7. Checkbox

최종 확정 (V3)

피그마 ID: `53:2537`

| 항목 | 값 |
|---|---|
| Variants | `on`, `off` |
| Size | `20 × 20px` |
| 아이콘 | 피그마 SVG 에셋 사용 |

---

## 8. Navigation — bottom

최종 확정 (V3)

피그마 ID: `151:3797`

| 항목 | 값 |
|---|---|
| Variants | `home`, `report`, `my` (활성 탭 기준) |
| BG | `bg-card` |
| Shadow | `shadow-nav` |
| Padding top | `space-3` |
| Padding bottom | `34px` (iOS safe area 고정값, 토큰 외) |
| Padding X | `space-4` |
| Active color | `brand` |
| Inactive color | `text-inactive` |
| Label | `label` textStyle |
| Icon size | `24 × 24px` |
| 탭 항목 | HOME, REPORT, MY |

---

## 9. TopBar

최종 확정 (V3)

피그마 ID: `87:3487`

| 항목 | 값 |
|---|---|
| Variants | 없음 (단일) |
| BG | 투명 (`bg-page` 그대로) |
| Height | `48px` |
| Padding top | `space-2` |
| Padding bottom | `space-4` |
| Padding X | `space-4` |
| 좌측 | Logo 컴포넌트 |
| 우측 | icon/notification + icon/settings (`24 × 24px`) |
| Logo 텍스트 | `size-subtitle` / `weight-semibold` / `brand` |

---

## 10. Logo

최종 확정 (V3)

피그마 ID: `132:3446`

| 항목 | 값 |
|---|---|
| Variants | Default, gray, White, text_white, text_blue, logo7, Point, gray_point, Black (9종) |
| 아이콘 단독 | `24 × 24px` |
| 텍스트+아이콘 | `147 × 24px` |
| 텍스트 | "Working Buddy" |

---

## 컴포넌트 총계

| 구분 | 수량 |
|---|---|
| 컴포넌트 (Card 3종 포함) | 10개 스펙 |
| 피그마 Variants 총합 | 17종 |
