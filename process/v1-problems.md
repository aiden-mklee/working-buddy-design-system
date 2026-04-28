# V1 결과물의 문제점

---

## 컬러

### 문제 1: 실제 화면에서 사용하지 않는 컬러 과잉 생성
피그마 홈화면에서 실제 사용된 컬러는 7개 수준이나, 총 32개의 Primitive를 생성했다.

| 구분 | 생성 수 | 실제 사용 수 | 미사용 |
|---|---|---|---|
| Blue | 11단계 | 2개 (400, 600) | 9개 |
| Gray | 12단계 | 5개 (0, 100, 200, 500, 900) | 7개 |
| Red/Green/Yellow | 9개 | 0개 | 9개 |

→ 전체 32개 중 실제로 화면에 등장한 컬러는 7개.
→ 상태색(red/green/yellow)은 피그마 어디에도 존재하지 않았음.

### 문제 2: Semantic 토큰 이름 일부가 실제 용도와 불일치
- `fg-subtle`, `fg-muted` 등 두 단계의 보조 텍스트 색이 생성되었으나, 피그마에는 텍스트 색이 `#222(primary)`와 `#BBB(inactive)` 두 가지뿐임.
- `border-strong`, `border-brand` 등 피그마에서 사용하지 않는 보더 변형이 포함됨.

---

## 타이포그래피

### 문제 1: 실제 쓰인 스케일보다 많은 단계 생성
피그마 홈화면에서 실제 사용된 폰트 사이즈: 6단계 (11, 12, 14, 16, 18, 72px)  
생성된 스케일: 11단계

미사용 사이즈: `10px, 20px, 24px, 32px, 48px` → 5개 불필요

### 문제 2: 합성 textStyles 12종 중 실제 매핑 가능한 것은 소수
생성된 textStyles: display, h1, h2, h3, title, subtitle, body-lg, body, body-strong, caption, label, button-lg, button (13종)

피그마 화면에서 확인 가능한 스타일: `display(72px)`, `title(18px)`, `subtitle(16px)`, `body-strong(14px/SemiBold)`, `body(14px/Regular)`, `caption(12px)`, `label(11px)` → 7종

미사용 스타일: `h1, h2, h3, body-lg, button-lg` → 5종 과잉

### 문제 3: Bold(700) 굵기가 피그마에서 미사용
피그마에 등장한 굵기: Regular, Medium, SemiBold  
생성된 굵기: Regular, Medium, SemiBold, **Bold** → Bold는 피그마 어디에도 없음.

---

## 스페이싱

### 문제 1: 일부 단계가 근거 없이 추가됨
피그마에서 확인된 실제 여백값: 8px, 10px, 12px, 13px, 16px, 20px, 22px 등  
생성된 스케일이 4px 그리드 기반이지만 `10px, 22px` 같은 중간값은 표현 불가.  
→ 화면에서 실제 쓰인 여백과 토큰 간의 불일치 발생.

---

## 보더 레디어스

### 문제 1: 피그마 미사용 단계 포함
피그마에서 확인된 radius: `10px(small card)`, `12px(card)`, `9999px(pill/button)` → 3가지  
생성된 단계: none, xs(4px), sm(8px), md(10px), lg(12px), xl(16px), 2xl(24px), full → 8단계  
미사용: `none, xs, sm, xl, 2xl` → 5단계 불필요

---

## 컴포넌트

### 문제 1: 피그마에 없는 컴포넌트가 구현됨
| 컴포넌트 | 피그마 존재 여부 | 비고 |
|---|---|---|
| Button (full-width) | ✅ | button/next |
| Button (circle) | ✅ | button/o, button/x |
| Card | ✅ | 홈화면 카드들 |
| ProgressBar | ✅ | 레벨 진행바 |
| Navigation (bottom) | ✅ | 하단 탭바 |
| Checkbox | ✅ | 미션 체크박스 |
| **Badge** | ❌ | **피그마에 없음** |
| **Input** | ❌ | **피그마에 없음 (토큰만 존재)** |

### 문제 2: 피그마에 있는 컴포넌트가 구현 안 됨
| 컴포넌트 | 상태 |
|---|---|
| Checkbox | 토큰만 있고 구현체 없음 |
| Navigation (bottom) | 미구현 |
| TopBar | 미구현 |
| Logo | 미구현 |

---

## 종합 학습

### 핵심 인식
> 전체 위임(AI에게 재정립 권한 부여) 방식은 피그마 원본보다 훨씬 크고 추상적인 결과물을 만든다.  
> 디자인 시스템은 "완전한 스펙"이 아니라 "현재 제품에 필요한 최소 계약"이어야 한다.

### 다음 버전에서 바꿀 것
1. **화면 단위로 토큰 추출** → 각 화면에서 실제 사용된 값만 수집, 그 교집합으로 시스템 정의
2. **컴포넌트는 피그마 컴포넌트 섹션 기준** → 없는 것은 만들지 않는다
3. **타이포 스케일은 피그마 실사용 사이즈 기반** → 범용 스케일 X
4. **Semantic 토큰은 실제 UI 패턴 기반** → "있을 법한" 케이스 예상 X
5. **단계별 승인** → Foundation → Typography → Component 순서로 확인 후 진행
