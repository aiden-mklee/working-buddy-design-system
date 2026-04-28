# V2-2 타이포그래피 결과물

피그마 실사용 기반 / 확장 없음

---

## 폰트 패밀리

| 토큰명 | 값 | 비고 |
|---|---|---|
| `font-sans` | `'Pretendard Variable', Pretendard, -apple-system, sans-serif` | 피그마 전체 공통 |

---

## 폰트 사이즈 (6단계)

피그마 확인 사이즈만. 번호 없이 역할명 기반으로 명명.

| 토큰명 | 값 | 피그마 확인 위치 |
|---|---|---|
| `size-label`   | `11px` | 내비게이션 탭 라벨 (HOME, REPORT, MY) |
| `size-caption` | `12px` | 보조 텍스트 ("오늘 획득한 버디", 레벨 표기) |
| `size-body`    | `14px` | 미션 항목, 핵심 본문 |
| `size-subtitle`| `16px` | 카드 제목 ("버디 보내기", "AI 챗봇") |
| `size-title`   | `18px` | 인사 텍스트, 강조 문구 |
| `size-display` | `72px` | 대형 수치 (오늘 획득한 버디 수) |

---

## 폰트 굵기 (3단계)

| 토큰명 | 값 | 피그마 확인 위치 |
|---|---|---|
| `weight-regular`  | `400` | body, caption, title(인사 텍스트) |
| `weight-medium`   | `500` | label(탭 라벨), button(컴포넌트 레벨) |
| `weight-semibold` | `600` | subtitle, body-strong, display |

> Bold(700)는 피그마 전체 화면에서 확인되지 않아 미포함.

---

## 자간 (letter-spacing)

피그마에서 추출한 절댓값. 모든 사이즈가 동일 비율(-0.025em)로 적용되어 있음.

| 사이즈 | 피그마 절댓값 | em 환산 |
|---|---|---|
| 11px | `-0.275px` | `-0.025em` |
| 12px | `-0.3px`   | `-0.025em` |
| 14px | `-0.35px`  | `-0.025em` |
| 16px | `-0.4px`   | `-0.025em` |
| 18px | `-0.45px`  | `-0.025em` |
| 72px | `-1.8px`   | `-0.025em` |

→ 전 사이즈 공통 규칙: `-0.025em`

---

## textStyles (7종)

line-height: 7종 모두 `1.4` — 피그마 `leading-[1.4]` 로 전 텍스트 확인됨.

| textStyle | size | weight | line-height | letter-spacing | 피그마 용도 |
|---|---|---|---|---|---|
| `display`      | 72px | SemiBold(600) | 1.4 | -1.8px | 오늘 획득한 버디 수 (대형 숫자) |
| `title`        | 18px | Regular(400)  | 1.4 | -0.45px | 인사 문구, 강조 멀티라인 텍스트 |
| `subtitle`     | 16px | SemiBold(600) | 1.4 | -0.4px | 카드 제목, 섹션 헤더 |
| `body-strong`  | 14px | SemiBold(600) | 1.4 | -0.35px | 미션 항목, 인용 문구 |
| `body`         | 14px | Regular(400)  | 1.4 | -0.35px | 일반 본문 |
| `caption`      | 12px | Regular(400)  | 1.4 | -0.3px | 보조 정보, 레벨 수치 |
| `label`        | 11px | Medium(500)   | 1.4 | -0.275px | 내비게이션 탭 라벨 |

---

## 주석: 버튼 텍스트 처리

| 항목 | 값 | 처리 방식 |
|---|---|---|
| 버튼 텍스트 | 18px / Medium(500) / leading-17px | textStyle 미포함 → 컴포넌트 토큰에서 별도 정의 |

버튼 "다음" 텍스트의 line-height가 피그마에서 `17px`(고정값)로 확인됨.  
이는 텍스트 스타일이 아닌 버튼 컴포넌트 내부 레이아웃 처리이므로 textStyles에서 분리.

---

## 요약

| 항목 | V1 | V2 |
|---|---|---|
| 사이즈 단계 | 11 | **6** |
| textStyles 수 | 13 | **7** |
| 굵기 종류 | 4 (+ Bold) | **3** |
| line-height 종류 | 5 | **1 (1.4 고정)** |
