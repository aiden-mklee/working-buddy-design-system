# V1 결과물 전체 기록

생성 일자: 2026-04-28  
피그마 소스: 워킹버디 페이지 (홈화면 + 컴포넌트 섹션)

---

## 파일 구조

```
src/
├── app/
│   ├── globals.css          CSS 토큰 (@theme 블록, :root semantic)
│   └── layout.tsx           Pretendard CDN 연결
├── styles/
│   ├── index.ts             barrel export
│   └── tokens/
│       ├── colors.ts        Primitive palette + Semantic aliases
│       ├── typography.ts    Font scale, weights, textStyles
│       ├── spacing.ts       4px grid spacing scale
│       ├── radius.ts        Border radius scale
│       ├── elevation.ts     Shadow / elevation system
│       ├── components.ts    Component-level tokens
│       └── index.ts         barrel export
└── components/ui/
    ├── Button.tsx
    ├── Card.tsx
    ├── ProgressBar.tsx
    ├── Badge.tsx
    └── index.ts
```

---

## 컬러 토큰

### Primitive: Blue (11단계)
| 토큰 | 값 |
|---|---|
| blue-50  | #EFF8FF |
| blue-100 | #DBEFFE |
| blue-200 | #B8DFFD |
| blue-300 | #7AC4FB |
| blue-400 | #43A6EF ← Figma primary-light |
| blue-500 | #1A90E0 |
| blue-600 | #0077CE ← Figma primary |
| blue-700 | #0063AF |
| blue-800 | #004F8C |
| blue-900 | #003D6B |
| blue-950 | #002847 |

### Primitive: Gray (12단계)
| 토큰 | 값 |
|---|---|
| gray-0   | #FFFFFF |
| gray-50  | #F9F9F9 |
| gray-100 | #F4F4F4 ← Figma bg |
| gray-200 | #EDEDED ← Figma gray-light |
| gray-300 | #E0E0E0 |
| gray-400 | #CCCCCC |
| gray-500 | #BBBBBB ← Figma gray (inactive) |
| gray-600 | #999999 |
| gray-700 | #666666 |
| gray-800 | #444444 |
| gray-900 | #222222 ← Figma black (text) |
| gray-950 | #111111 |

### Primitive: Status (9단계)
red-400/500/600, green-400/500/600, yellow-400/500/600

### Semantic (14개)
bg-base, bg-surface, bg-sunken,
fg-default, fg-subtle, fg-muted, fg-inverted,
brand, brand-light, brand-subtle, brand-fg, brand-hover,
disabled, success, warning, danger,
border, border-strong, border-brand

---

## 타이포그래피

### 폰트
- Pretendard Variable (CDN, dynamic subset)

### 사이즈 스케일 (11단계)
| 토큰 | 값 | 피그마 매핑 |
|---|---|---|
| 2xs | 10px | - |
| xs  | 11px | label (nav) |
| sm  | 12px | caption |
| base| 14px | body |
| md  | 16px | heading |
| lg  | 18px | title / button |
| xl  | 20px | - |
| 2xl | 24px | - |
| 3xl | 32px | - |
| 4xl | 48px | - |
| display | 72px | hero number |

### 굵기
regular(400), medium(500), semibold(600), bold(700)

### 행간
tight(1.2), snug(1.3), normal(1.4), relaxed(1.6), loose(1.8)

### 자간
tighter(-0.05em), tight(-0.025em), normal(0), wide(0.025em)

### 합성 textStyles (12종)
display, h1, h2, h3, title, subtitle, body-lg, body, body-strong, caption, label, button-lg, button

---

## 스페이싱 (4px 그리드, 16단계)
0, 0.5(2px), 1(4px), 1.5(6px), 2(8px), 3(12px), 4(16px), 5(20px),
6(24px), 7(28px), 8(32px), 10(40px), 12(48px), 16(64px), 20(80px), 24(96px)

---

## 보더 레디어스 (8단계)
none(0), xs(4px), sm(8px), md(10px), lg(12px), xl(16px), 2xl(24px), full(9999px)

---

## 엘리베이션 / 섀도 (8단계)
| 토큰 | 값 |
|---|---|
| 0 | none |
| 1 | 0 1px 2px rgba(0,0,0,0.05) |
| 2 | 0 2px 4px + 0 1px 2px |
| 3 | 0 0 16px rgba(0,0,0,0.08) ← Figma card |
| 4 | 0 0 8px rgba(0,0,0,0.08) ← Figma nav |
| 5 | 0 20px 25px + 0 8px 10px |
| glow-brand | 0 0 8px rgba(120,144,238,0.42) ← Figma blue card |
| glow-sm | 0 0 4px rgba(120,144,238,0.42) |

---

## 컴포넌트 토큰 (components.ts)
button.primary, button.ghost, button.circle, button.sm,
card.default, card.sm, card.brand,
input,
progressBar,
checkbox,
badge,
navBar,
topBar

---

## UI 컴포넌트 (구현체)
- Button: variant(primary/ghost/disabled) × size(full/circle/sm)
- Card: variant(default/sm/brand)
- ProgressBar: value(0-100) + minLabel/maxLabel
- Badge: variant(brand/success/warning/danger/neutral)
