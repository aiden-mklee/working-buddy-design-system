# 토큰 정의 — V4 반응형 확장

> V3 토큰은 **변경 없음** — 추가만. 원본: [docs/tokens.md](tokens.md)

V3는 모바일(393px) 단일 환경 기준으로 설계됐다. V4는 tablet·desktop 레이아웃을 지원하기 위한 토큰을 추가한다.

---

## Breakpoints ← V4 신규

| 토큰명 | 값 | 적용 범위 |
|---|---|---|
| `bp-tablet`  | `640px`  | tablet 시작점 |
| `bp-desktop` | `1024px` | desktop 시작점 |

> mobile(0~639px)은 별도 토큰 없음 — "기본값"이 곧 mobile.

---

## Spacing 추가 ← V4 신규 [tablet+]

V3 스페이싱(space-2~5, 8~20px)은 모바일 밀도 기준. tablet 이상에서는 더 넓은 여백이 필요.

| 토큰명 | 값 | 주요 용도 |
|---|---|---|
| `space-6`  | `24px` | 카드 내부 padding, topbar 수평 여백 |
| `space-8`  | `32px` | 섹션 간 여백, 주요 vertical padding |
| `space-10` | `40px` | 페이지 좌우 여백 (desktop) |
| `space-12` | `48px` | 페이지 최상단·최하단 여백 |

> 4px 그리드 유지. space-7·space-9는 실제 웹 레이아웃 패턴에서 수요가 없어 생략.

---

## Typography 추가 ← V4 신규

V3 7종 textStyle은 전 breakpoint에서 기본값으로 유지.

### 신규 textStyle

| textStyle | size | weight | breakpoint | 근거 |
|---|---|---|---|---|
| `heading` | `24px` | semibold | [tablet+] | 웹 섹션 제목용. 모바일 title(18px)과 display(72px) 사이 단계 필요 |

### display 재정의

| textStyle | size | breakpoint | 근거 |
|---|---|---|---|
| `display` | `48px` | [desktop] | 72px는 모바일 전면 배너 스케일. 1100px 콘텐츠 폭에서는 48px로 충분 |

> display는 mobile/tablet에서 V3 72px 그대로. desktop에서만 48px로 override.
> 공통 규칙(line-height 1.4 / letter-spacing -0.025em)은 신규 스타일에도 동일 적용.

---

## Layout 토큰 ← V4 신규 [desktop]

웹 전용 구조값. mobile/tablet에 적용하지 않음.

| 토큰명 | 값 | 용도 |
|---|---|---|
| `sidebar-width`     | `240px`   | 좌측 사이드바 고정 폭 |
| `content-max-width` | `1100px`  | 본문 최대 폭 (중앙 정렬 컨테이너) |
| `topbar-height`     | `60px`    | 상단 고정 바 높이 |
| `grid-gap`          | `space-5` | 그리드 컬럼 간격 (space-5 참조, 독립 토큰으로 레이아웃 맥락 명시) |

---

## 보더 레디어스 추가 ← V4 신규 [tablet+]

| 토큰명 | 값 | 근거 |
|---|---|---|
| `radius-xl` | `16px` | 웹 카드는 화면 밀도가 낮아 더 넉넉한 곡률이 자연스러움. radius-lg(12px)에서 4px 스텝 증가 |

---

## 토큰 총계

| 영역 | V3 | V4 추가 |
|---|---|---|
| Breakpoints | — | 2개 |
| Spacing | 4개 | 4개 |
| textStyles (신규) | 7종 | 1종 |
| textStyles (재정의) | — | 1건 |
| Layout | — | 4개 |
| 레디어스 | 3개 | 1개 |
| 컬러 / Shadow | 20개 | — |
| 타이포 size·weight | 9개 | — |
| **합계** | **43개** | **+13개 = 56개** |
