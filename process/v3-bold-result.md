# V3-2 Bold(700) 처리 결과물

결정: **옵션 B — SemiBold(600) 근사**

---

## 변경 내용

| 항목 | 변경 전 (피그마 원본) | 변경 후 (V3 확정) |
|---|---|---|
| TopBar 로고 텍스트 weight | Bold(700) | `weight-semibold` (600) |

---

## 적용 위치

| 컴포넌트 | 항목 | 확정값 |
|---|---|---|
| TopBar | Logo 텍스트 "Working Buddy" | `size-subtitle` / `weight-semibold` (16px / 600) / `brand` |

---

## 결정 근거

- Bold(700)는 TopBar 로고 외 피그마 전체 화면에서 사용되지 않음
- 예외 하나를 위해 타이포그래피 토큰 체계를 확장하는 것은 V2의 핵심 원칙("실사용값만")에 역행
- 시각적 차이(Bold vs SemiBold)가 미미하여 사용자 경험에 영향 없음
- 타이포그래피 토큰은 V2 확정 그대로 유지 (`weight-regular` / `weight-medium` / `weight-semibold`)
