# Avatars 과제

## 링크

> https://minqyu.github.io/homework/avatars/avatars.html

## 수행과정

- 초기 파일, 이미지 파일, svg 파일 세팅
- index 파일에서 avatars 파일 마크업
- 코드 작성. 컨테이너 - 아바타랩 - 아바타 객체 구조
- 클래스 네이밍
- CSS 작성

## 과제 수행중 특이사항

- 하드코딩된 아바타 객체들의 태그와 속성값을 멀티 커서로 수정하다가 div 요소가 하나 더 생겨서 배치가 망가졌는데, 이 문제를 CSS로 찾다가 시간을 많이 허비했습니다. JSX를 사용하면 깔끔하게 코딩할 수 있는데, 참 불편하다는 생각이 들었습니다.
- 파일을 따로 분리하지 않고 클래스 이름을 바꾸고 CSS 셀렉터를 활용해 float와 flex 배치를 구현했습니다.
- float을 이용한 배치는 자동정렬을 사용하지 않고, figma에서 여백과 크기값을 확인해 마진과 패딩만을 사용했습니다. 여백 계산을 쉽게 하기 위해 box-sizing: border-box; 값을 주었습니다.
- flex를 이용한 배치는 justify-content와 align-content를 이용해 자동정렬을 이용했습니다.
