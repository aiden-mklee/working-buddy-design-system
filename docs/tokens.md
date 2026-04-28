# 토큰 정의 (최종)

최종 확정 (V3) — 상세 과정: [process/v3-result.md](../process/v3-result.md)

---

## 컬러

최종 확정 (V3)

### Primitive (7개)

| 토큰명 | 값 |
|---|---|
| `blue`       | `#0077CE` |
| `blue-light` | `#43A6EF` |
| `white`      | `#FFFFFF` |
| `gray-100`   | `#F4F4F4` |
| `gray-200`   | `#EDEDED` |
| `gray-500`   | `#BBBBBB` |
| `gray-900`   | `#222222` |

### Semantic (10개)

| 토큰명 | 참조 | 용도 |
|---|---|---|
| `bg-page`       | `gray-100`   | 전체 화면 배경 |
| `bg-card`       | `white`      | 카드·패널 표면 |
| `bg-track`      | `gray-200`   | 프로그레스바 트랙 |
| `text-primary`  | `gray-900`   | 기본 텍스트 |
| `text-inactive` | `gray-500`   | 비활성 라벨·아이콘 |
| `text-on-brand` | `white`      | 브랜드 배경 위 텍스트 |
| `brand`         | `blue`       | CTA 버튼, 진행바, 강조 |
| `brand-light`   | `blue-light` | 그라디언트 시작점 |
| `border-card`   | `white`      | 카드 외곽선 |
| `disabled`      | `gray-500`   | 비활성 버튼 배경 |

---

## 타이포그래피

최종 확정 (V3)

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

## 스페이싱

최종 확정 (V3)

4px 그리드 기반 / 예외 고정값 1건 별도 명시

| 토큰명 | 값 | 주요 용도 |
|---|---|---|
| `space-2` | `8px`  | 아이템 row 여백, 아이콘↔텍스트 간격 |
| `space-3` | `12px` | 섹션 래퍼 vertical, 내비 상단, gap |
| `space-4` | `16px` | 카드 vertical padding, 화면 edge |
| `space-5` | `20px` | 화면/카드 horizontal padding |

> **예외 고정값**: Navigation `padding-bottom: 34px` = iOS safe area 하단 여백 (디바이스 환경값, 토큰 외)

---

## 보더 레디어스

최종 확정 (V3)

| 토큰명 | 값 | 사용 컴포넌트 |
|---|---|---|
| `radius-md`   | `10px`   | 퀵액션 카드 (버디 보내기, AI 챗봇) |
| `radius-lg`   | `12px`   | 메인 카드, 미션 카드 |
| `radius-full` | `9999px` | 버튼, 프로그레스바 |

---

## Shadow

최종 확정 (V3)

| 토큰명 | 값 | 사용 컴포넌트 |
|---|---|---|
| `shadow-card` | `0px 0px 16px rgba(0,0,0,0.08)`      | Card (default), Card (action-surface) |
| `shadow-nav`  | `0px 0px 8px rgba(0,0,0,0.08)`       | Navigation (bottom) |
| `shadow-glow` | `0px 0px 8px rgba(120,144,238,0.42)` | Card (action-brand) |

---

## 토큰 총계

| 영역 | 수량 |
|---|---|
| 컬러 Primitive | 7개 |
| 컬러 Semantic | 10개 |
| 타이포 사이즈 | 6개 |
| 타이포 굵기 | 3개 |
| textStyles | 7종 |
| 스페이싱 | 4개 |
| 레디어스 | 3개 |
| Shadow | 3개 |
| **합계** | **43개** |
