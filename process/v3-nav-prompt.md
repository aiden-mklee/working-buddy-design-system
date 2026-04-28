# V3-3 Nav Bottom 34px 처리 프롬프트

## 배경

V2 spacing 토큰 최대값: `space-5` (20px)  
Navigation bottom의 `padding-bottom: 34px` → 토큰 범위 밖 고정값

## 결정 옵션

| 옵션 | 내용 |
|---|---|
| A | 예외 고정값으로 명시 — spacing 토큰 외 처리 |
| B | `space-8`(32px) 또는 `space-9`(36px) 토큰 추가 — 그리드 편입 |

## 결정: 옵션 A — 예외 고정값으로 명시

> 이유: 34px는 iOS safe area 하단 여백으로,
> 디자인 의도가 아닌 디바이스 환경 대응값.
> spacing 시스템에 포함시키는 것이 오히려 부자연스러움.
