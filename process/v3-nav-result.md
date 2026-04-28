# V3-3 Nav Bottom 34px 처리 결과물

결정: **옵션 A — 예외 고정값으로 명시**

---

## 처리 내용

| 항목 | 처리 방식 |
|---|---|
| Navigation `padding-bottom: 34px` | spacing 토큰 미편입 — 고정값 주석으로 명시 |
| spacing 토큰 변경 | 없음 (V2 4개 그대로 유지) |

---

## 결정 근거

- 34px는 iOS Home Indicator safe area 대응값 — 디바이스 환경 제약, 디자인 결정이 아님
- spacing 토큰은 레이아웃 의도를 표현하는 것이 목적 → 환경 대응값 혼입 시 의미 오염
- 향후 Android / 웹 대응 시 플랫폼별로 다르게 처리해야 할 값이므로 토큰화 부적합

---

## spacing 토큰 최종 확정

V2에서 정의한 4개 그대로 유지.

| 토큰명 | 값 |
|---|---|
| `space-2` | `8px` |
| `space-3` | `12px` |
| `space-4` | `16px` |
| `space-5` | `20px` |
