# apple 제품 카드

## 링크

> https://minqyu.github.io/homework/apple/apple.html

## 구현 결과
![애플과제](https://github.com/user-attachments/assets/0f90d4e0-7bcd-4408-9670-9993ab1ea6a2)

## 요구사항 해결과정

### 카드 컴포넌트 구현
- 커스텀 프로퍼티를 활용해 inline-size가 1024px을 넘어가면 변수만 재지정 하도록 구현
- dark-style, bright-style로 나누어 제작

### CSS Grid를 이용해 반응형으로 구현
- 카드 컴포넌트를 구현한 뒤, 2열로 배치가 변하는 요소들만 container-grid로 묶음
- grid-template-columns 값을 repeat(1, 1fr) -> repeat(2, 1fr)로 바꾸는 방식으로 구현
- subtitle은 flex를 이용해 가로로 펴지도록 구현

### img 태그가 아닌 background 속성을 활용해 구현
- 각 컴포넌트마다 개별 class를 부여하고 background-image를 지정
- 이미지를 바꿔야 하는 경우, @container를 이용해 카드가 들어있는 요소의 inline-size가 1024px이 넘어가면 background-image를 교체

### 디바이스의 픽셀 밀도별로 배율 이미지 반영
- 미구현

## 과제 수행중 특이사항
- 처음에 커스텀 프로퍼티를 재할당을 안하고 theme.css 그대로 사용하다가, 재할당을 하면 크기 변환이 필요할 때 손쉽게 할 수 있다는 것을 깨닫고 고쳤습니다.
- card 컴포넌트별 폰트 색상과 버튼 색상이 두 가지인 것에 착안해 bright-style과 dark-style로 나누어 css를 꾸몄는데, 클래스를 따로 부여하지 않고 순서로 선택해도 가능했을 것 같습니다.
- theme.css에 색상 프로퍼티가 네 가지나 있어서 의문이었는데, 애플 공식 홈페이지에서 기본 버튼 색상 두 종류에 hover시 색상, active이 있는 것을 확인해 (dark-style)파란색 버튼에만 구현해 보았습니다.
- 중복 코드는 최대한 없애보려 했으나, 우선순위 규칙때문에 @container (inline-size >= 1024px)를 두 번 사용하는 등, 깔끔한 코드를 짜지 못한것이 아쉽습니다.
- 생각보다 카드 컴포넌트에 시간을 너무 많이 사용했는데, 배율 이미지 반영을 잊고 구현을 못했습니다.
