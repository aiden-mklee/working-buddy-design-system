# V3-1 Shadow 토큰 프롬프트

## 요청 원문

> 아래 조건으로 워킹버디 shadow 토큰을 정의해줘.
>
> [피그마에서 확인된 실제 shadow값 - 이것만]
> - card shadow: 0px 0px 16px rgba(0,0,0,0.08)
> - nav shadow: 0px 0px 8px rgba(0,0,0,0.08)
> - glow-brand: 0px 0px 8px rgba(120,144,238,0.42)
>
> [절대 원칙]
> - 위 3개만 토큰화
> - 단계 확장 없음 (elevation-1~8 같은 시스템 X)
>
> [출력] 토큰명 / 값 / 사용 컴포넌트

---

## V1 대비 달라진 점

| 항목 | V1 | V3 |
|---|---|---|
| 토큰 수 | 8단계 (elevation 0~5 + glow 2종) | **3개** |
| 확장 방식 | Material Design 엘리베이션 시스템 참조 | 없음 |
| 미사용 포함 | elevation 0~2, 5 (피그마에 없음) | **없음** |
