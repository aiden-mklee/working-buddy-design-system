# V2 결과물 통합

V2-1 컬러 ~ V2-5 컴포넌트 전 단계 확정 내용 통합  
각 상세 내용 → process/v2-{색션}-result.md 참조

---

## 컬러 토큰

### Primitive (7개)

| 토큰명 | 값 |
|---|---|
| `blue` | `#0077CE` |
| `blue-light` | `#43A6EF` |
| `white` | `#FFFFFF` |
| `gray-100` | `#F4F4F4` |
| `gray-200` | `#EDEDED` |
| `gray-500` | `#BBBBBB` |
| `gray-900` | `#222222` |

### Semantic (10개)

| 토큰명 | 참조 | 용도 |
|---|---|---|
| `bg-page` | `gray-100` | 전체 화면 배경 |
| `bg-card` | `white` | 카드·패널 표면 |
| `bg-track` | `gray-200` | 프로그레스바 트랙 |
| `text-primary` | `gray-900` | 기본 텍스트 |
| `text-inactive` | `gray-500` | 비활성 라벨·아이콘 |
| `text-on-brand` | `white` | 브랜드 배경 위 텍스트 |
| `brand` | `blue` | CTA 버튼, 진행바, 강조 |
| `brand-light` | `blue-light` | 그라디언트 시작점 |
| `border-card` | `white` | 카드 외곽선 |
| `disabled` | `gray-500` | 비활성 버튼 배경 |

---

## 타이포그래피 토큰

### 폰트
`'Pretendard Variable', Pretendard, -apple-system, sans-serif`

### 사이즈 (6단계)

| 토큰명 | 값 |
|---|---|
| `size-label`    | `11px` |
| `size-caption`  | `12px` |
| `size-body`     | `14px` |
| `size-subtitle` | `16px` |
| `size-title`    | `18px` |
| `size-display`  | `72px` |

### 굵기 (3단계)

| 토큰명 | 값 |
|---|---|
| `weight-regular`  | `400` |
| `weight-medium`   | `500` |
| `weight-semibold` | `600` |

### 공통 규칙
- Line-height: `1.4` (전 스타일 공통)
- Letter-spacing: `-0.025em` (전 사이즈 공통)

### textStyles (7종)

| textStyle | size | weight | line-height | letter-spacing |
|---|---|---|---|---|
| `display`     | 72px | semibold | 1.4 | -0.025em |
| `title`       | 18px | regular  | 1.4 | -0.025em |
| `subtitle`    | 16px | semibold | 1.4 | -0.025em |
| `body-strong` | 14px | semibold | 1.4 | -0.025em |
| `body`        | 14px | regular  | 1.4 | -0.025em |
| `caption`     | 12px | regular  | 1.4 | -0.025em |
| `label`       | 11px | medium   | 1.4 | -0.025em |

---

## 스페이싱 토큰 (4개 · 4px 그리드)

| 토큰명 | 값 | 주요 용도 |
|---|---|---|
| `space-2` | `8px`  | 아이템 row 여백, 아이콘↔텍스트 간격 |
| `space-3` | `12px` | 섹션 래퍼 vertical, 내비 상단, gap |
| `space-4` | `16px` | 카드 vertical padding, 화면 edge |
| `space-5` | `20px` | 화면/카드 horizontal padding |

---

## 보더 레디어스 토큰 (3개)

| 토큰명 | 값 | 사용 컴포넌트 |
|---|---|---|
| `radius-md`   | `10px`   | 퀵액션 카드 (버디 보내기, AI 챗봇) |
| `radius-lg`   | `12px`   | 메인 카드, 미션 카드 |
| `radius-full` | `9999px` | 버튼, 프로그레스바 |

---

## 컴포넌트 목록 (8개)

| 컴포넌트 | Variants | 핵심 토큰 |
|---|---|---|
| Button (full-width) | default, disabled | `brand` / `disabled` / `radius-full` / `size-title` / `weight-medium` |
| Button (circle) | default, disabled | `brand` / `disabled` / `radius-full` |
| Card (default) | — | `bg-card` / `radius-lg` / `space-5×space-4` |
| Card (action-brand) | — | gradient `brand-light→brand` / `radius-md` |
| Card (action-surface) | — | gradient white→#DFE2E5 / `radius-md` |
| ProgressBar | — | `bg-track` / `brand` / `radius-full` / 12px height |
| Checkbox | on, off | 24×24px |
| Navigation (bottom) | home, report, my | `bg-card` / `brand` / `text-inactive` / `label` |
| TopBar | — | `bg-page` 투명 / `space-4` padding |
| Logo | 9 variants | 24×24px (아이콘) / 147×24px (텍스트+아이콘) |

---

## V2 미결 사항 (V3 검토 필요)

| # | 항목 | 내용 |
|---|---|---|
| 1 | Shadow 토큰 미정의 | card `0 0 16px rgba(0,0,0,0.08)`, nav `0 0 8px`, glow `0 0 8px rgba(120,144,238,0.42)` — 아직 토큰화 안 됨 |
| 2 | TopBar Bold(700) | 로고 텍스트가 Bold 사용 — `weight-bold` 추가 or SemiBold 근사 결정 필요 |
| 3 | Nav bottom padding 34px | spacing 토큰 범위 밖 고정값 — 처리 방식 결정 필요 |

---

## V1 → V2 수치 비교

| 토큰 | V1 | V2 | 감소율 |
|---|---|---|---|
| 컬러 | 46개 | 17개 | -63% |
| 타이포 사이즈 | 11단계 | 6단계 | -45% |
| textStyles | 13종 | 7종 | -46% |
| 스페이싱 | 16단계 | 4개 | -75% |
| 보더 레디어스 | 8단계 | 3개 | -63% |
| 컴포넌트 | 4개 구현 | 8개 스펙 | +100% (누락 없음) |
