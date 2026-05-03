# V4 작업 기록

V3(모바일 단일, 43토큰)을 반응형 웹 환경으로 확장한 과정.

---

## V4-1. 토큰 확장

### 프롬프트 원문

> V3까지 정의한 워킹버디 디자인 시스템을 반응형 웹 환경으로 확장하려고 해.
>
> [V4에서 추가할 것]
> 1. Breakpoints 토큰 — mobile: 0~639px / tablet: 640~1023px / desktop: 1024px+
> 2. Spacing 확장 — space-6(24) / space-8(32) / space-10(40) / space-12(48px)
> 3. Typography 확장 — display desktop 72→48px / heading 추가 24px semibold
> 4. Layout 토큰 — sidebar-width(240) / content-max-width(1100) / topbar-height(60) / grid-gap(space-5)
> 5. Radius 추가 — radius-xl 16px
>
> [절대 원칙]
> - V3 토큰은 변경하지 않고 추가만 한다
> - 각 토큰에 어느 breakpoint에서 사용되는지 명시
> - 근거 없는 추가 금지 — 실제 웹 UI 패턴에서 필요한 것만
>
> 출력 형식: docs/v4-tokens.md

### 핵심 조건 (V3 대비 달라진 점)

| 항목 | V3 | V4 |
|---|---|---|
| 환경 | mobile(393px) 단일 | mobile / tablet / desktop 3단계 |
| Breakpoints | 없음 | bp-tablet(640) / bp-desktop(1024) |
| Spacing 범위 | space-2~5 (8~20px) | space-6~12 추가 (24~48px) |
| display 크기 | 72px (전 환경) | mobile/tablet 72px / desktop 48px override |
| heading textStyle | 없음 | 24px semibold [tablet+] 추가 |
| Layout 토큰 | 없음 | sidebar / content / topbar / grid-gap |
| Radius 최대값 | radius-lg 12px | radius-xl 16px [tablet+] 추가 |

### 결과에서 달라진 점

- **mobile 토큰 무변경**: V3 43개 토큰을 그대로 유지하고 V4는 순수 추가
- **display override 방식**: display를 새 토큰으로 만들지 않고 같은 토큰명을 desktop breakpoint에서 override — 토큰 수를 줄이고 "display는 큰 텍스트" 의미를 유지
- **grid-gap의 독립 토큰화**: space-5(20px)의 값 별칭이지만 레이아웃 맥락에서 명시적으로 쓰기 위해 분리
- **space-7·space-9 생략**: 4px 그리드이나 28px·36px 여백은 실제 웹 패턴에서 수요 없음

---

## V4-2. HTML 구현

### 프롬프트 원문

> V4 토큰을 기반으로 워킹버디 홈 화면을 반응형 HTML로 구현해줘.
>
> [반응형 3단계 요구사항]
> - mobile: 기존 V3 모바일 디자인 그대로 / 하단 네비게이션 / 단일 컬럼
> - tablet: 상단 네비게이션으로 변경 / 2컬럼 그리드 / space-6·space-8 적용
> - desktop: 좌측 사이드바(240px, 다크 네이비) / 우측 콘텐츠(1100px) / 3컬럼 그리드 / TopBar
>
> [기술 요구사항]
> - 단일 HTML 파일 (CSS, JS 포함)
> - CSS Variables로 V4 토큰 전부 적용
> - 구글 폰트 Noto Sans KR (Pretendard 대체)
> - 브라우저 창 크기 조절 시 실시간 레이아웃 변경
> - 우하단 breakpoint 뱃지 (MOBILE / TABLET / DESKTOP)
> - 모든 색상은 CSS Variables 참조, 하드코딩 금지
> - 각 컴포넌트에 사용 토큰 주석 표기
>
> 파일명: v4-home.html

### 핵심 조건 (V3 대비 달라진 점)

| 항목 | V3 (모바일) | V4 (반응형) |
|---|---|---|
| 네비게이션 | 하단 Bottom Nav (fixed) | mobile: Bottom Nav / tablet+: TopBar 수평 링크 / desktop: 좌측 사이드바 |
| 카드 레이아웃 | 단일 컬럼 | tablet: 2컬럼 / desktop: 3컬럼 |
| 카드 radius | radius-lg (12px) | tablet+: radius-xl (16px) [V4] |
| TopBar 높이 | 48px (V3) | tablet+: topbar-height 60px [V4] |
| 여백 | space-4/space-5 | tablet: space-6/space-8 / desktop: space-8/space-10 [V4] |
| 추가 콘텐츠 | 없음 | 주간 활동 Stats 카드 (tablet+에서 3번째 컬럼) |
| display 텍스트 | 72px | desktop: 48px override [V4] |
| 폰트 | Pretendard Variable | Noto Sans KR (CDN 대체) |

### 구현 결정 사항

**Bottom Nav → TopBar 전환 (tablet)**
- 640px에서 하단 네비게이션 완전 숨김, 상단 수평 링크로 교체
- 이유: 마우스 환경에서 하단 탭은 접근성 저하. 상단 네비가 표준 웹 패턴

**Desktop 사이드바 다크 네이비**
- 색상 `#0B2D4E` — V4 토큰 스펙 외 구현 결정값
- 이유: brand blue(#0077CE)의 어두운 보완색. 사이드바에 brand 원색 쓰면 콘텐츠와 충돌

**Stats 카드 (tablet+ 전용)**
- 모바일에서는 숨김, tablet 2컬럼 레이아웃부터 등장
- 이유: 모바일 단일 컬럼에서는 정보 밀도 과부하. tablet 3번째 카드로 자연스럽게 추가

**`display` textStyle 적용 대상**
- 주간 달성률 숫자 "94%"에 적용
- mobile/tablet: size-title(18px) → desktop: 48px (display override [V4])
- 홈 화면에서 72px 원본이 쓰일 콘텍스트가 없어, 달성률 강조 수치가 가장 적합한 대상

**그리드 흐름 (desktop 3컬럼)**
- Level Card / Mission Card / Stats Card — 좌→우 자연 흐름
- tablet에서는 Level Card가 full-width span, 하단 2컬럼에 Mission + Stats
