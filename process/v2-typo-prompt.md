# V2-2 타이포그래피 프롬프트

## 요청 원문

> 아래 조건으로 워킹버디 타이포그래피 토큰만 다시 정의해줘.
>
> [절대 원칙]
> - 피그마 화면에서 실제로 사용된 텍스트 스타일만 포함한다
> - 피그마에 없는 스케일은 추가하지 않는다
>
> [피그마에서 확인된 실제 사용값 - 이것만 사용]
> 사이즈: 11px, 12px, 14px, 16px, 18px, 72px (6단계)
> 굵기: Regular(400), Medium(500), SemiBold(600) (3가지, Bold 없음)
> 폰트: Pretendard
>
> [구성해야 할 textStyles - 7종만]
> - display: 72px
> - title: 18px
> - subtitle: 16px
> - body-strong: 14px / SemiBold
> - body: 14px / Regular
> - caption: 12px
> - label: 11px
>
> [출력 형식]
> 각 textStyle마다: size / weight / line-height / 용도 설명
> line-height는 피그마에서 확인된 값으로, 없으면 추측하지 말고 "-"로 표기

---

## V1 대비 달라진 점

| 항목 | V1 | V2 |
|---|---|---|
| 폰트 사이즈 단계 | 11단계 (10~72px) | 6단계 (11, 12, 14, 16, 18, 72px) |
| textStyles 수 | 13종 | 7종 |
| Bold(700) 포함 여부 | 포함 | 미포함 (피그마에 없음) |
| line-height 종류 | 5가지 (tight~loose) | 피그마 확인값만 |
| 합성 스타일 (h1~h3 등) | 포함 | 미포함 (피그마에 없음) |
