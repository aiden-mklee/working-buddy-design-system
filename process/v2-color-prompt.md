# V2-1 컬러 프롬프트

## 요청 원문

> 아래 조건으로 워킹버디 Figma 파일의 컬러 토큰만 다시 정의해줘.
>
> [절대 원칙]
> - 피그마 화면에 실제로 등장한 컬러값만 포함한다
> - 피그마에 없는 컬러는 추가하지 않는다
> - Material Design 등 외부 시스템 기준으로 확장하지 않는다
>
> [피그마에서 확인된 실제 사용 컬러 - 이것만 사용]
> - #0077CE (primary blue)
> - #43A6EF (primary blue light)
> - #FFFFFF (white)
> - #F4F4F4 (background)
> - #EDEDED (gray light)
> - #BBBBBB (gray inactive)
> - #222222 (black text)
>
> [구조]
> Primitive 먼저:
> - 위 7개 컬러를 이름 붙여서 나열 (확장 없이 7개만)
>
> Semantic 다음:
> - Primitive를 참조해서 용도 기반으로 명명
> - 실제 UI 패턴에 존재하는 용도만: bg, text, brand, border, disabled
> - "있을 법한" 케이스 예상해서 추가하지 말 것
>
> [출력 형식]
> 마크다운 테이블로 토큰명 / 값 / 용도 설명

---

## V1 대비 달라진 점

| 항목 | V1 | V2 |
|---|---|---|
| 컬러 수 | 32개 (primitive 확장) | 7개 (실사용만) |
| 확장 기준 | Material Design scale | 없음 |
| Semantic 범위 | 14개 (예상 케이스 포함) | 실제 UI 패턴만 |
| 상태색 (error/success) | 포함 | 미포함 (피그마에 없음) |
