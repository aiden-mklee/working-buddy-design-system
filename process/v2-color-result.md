# V2-1 컬러 결과물

피그마 실사용 색상 7개 기반 / 확장 없음

---

## Layer 1 — Primitive (7개)

순수 값만 나열. 의미 없는 이름, 위치 기반 네이밍.

| 토큰명 | 값 | 피그마 출처 |
|---|---|---|
| `blue` | `#0077CE` | 버튼, 브랜드, 프로그레스 fill, 텍스트 강조 |
| `blue-light` | `#43A6EF` | 그라디언트 시작점 (버디 보내기 카드) |
| `white` | `#FFFFFF` | 카드 배경, 흰 텍스트 |
| `gray-100` | `#F4F4F4` | 전체 페이지 배경 |
| `gray-200` | `#EDEDED` | 프로그레스 트랙, 구분 영역 |
| `gray-500` | `#BBBBBB` | 비활성 아이콘·라벨, 비활성 버튼 |
| `gray-900` | `#222222` | 기본 텍스트 |

> gray 숫자는 scale 위치 표기 (100=연함, 900=진함). 중간값 생략 — 실제로 없으므로.

---

## Layer 2 — Semantic (10개)

Primitive를 참조. 실제 UI 패턴에 존재하는 용도만.

### bg (배경)

| 토큰명 | 참조 | 값 | 용도 |
|---|---|---|---|
| `bg-page` | `gray-100` | `#F4F4F4` | 전체 화면 배경 |
| `bg-card` | `white` | `#FFFFFF` | 카드, 패널 표면 |
| `bg-track` | `gray-200` | `#EDEDED` | 프로그레스바 트랙, 비활성 영역 채우기 |

### text (텍스트)

| 토큰명 | 참조 | 값 | 용도 |
|---|---|---|---|
| `text-primary` | `gray-900` | `#222222` | 본문, 제목 등 기본 텍스트 |
| `text-inactive` | `gray-500` | `#BBBBBB` | 내비게이션 비활성 라벨, 보조 텍스트 |
| `text-on-brand` | `white` | `#FFFFFF` | 파란 배경 위 텍스트 |

### brand (브랜드)

| 토큰명 | 참조 | 값 | 용도 |
|---|---|---|---|
| `brand` | `blue` | `#0077CE` | CTA 버튼, 진행바 fill, 강조 텍스트, 아이콘 active |
| `brand-light` | `blue-light` | `#43A6EF` | 그라디언트 시작 (`brand-light → brand`) |

### border (테두리)

| 토큰명 | 참조 | 값 | 용도 |
|---|---|---|---|
| `border-card` | `white` | `#FFFFFF` | AI챗봇 카드 외곽선 (흰 배경에 흰 border, 그림자로 구분) |

### disabled (비활성)

| 토큰명 | 참조 | 값 | 용도 |
|---|---|---|---|
| `disabled` | `gray-500` | `#BBBBBB` | 비활성 버튼 배경 (button/next off 상태) |

---

## 요약

| 계층 | 수량 |
|---|---|
| Primitive | 7개 |
| Semantic | 10개 |
| **합계** | **17개** |

V1(32개 primitive + 14개 semantic = 46개) 대비 **63% 감소**

---

## 미포함 항목 및 이유

| 항목 | 미포함 이유 |
|---|---|
| 상태색 (success/warning/error) | 피그마 어떤 화면에도 존재하지 않음 |
| `rgba(136,197,242,0.2)` (버디카드 border) | 7개 primitive에서 파생된 투명도값 — 직접 토큰화 대상 아님 |
| blue-50~400 중간 단계 | 피그마에 `blue(600)`, `blue-light(400)` 외 등장 없음 |
| hover / pressed 상태색 | 피그마에 인터랙션 상태 정의 없음 |
