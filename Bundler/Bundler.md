# Bundler란?

---

## 만들어진 배경

---

웹 페이지의 규모가 커지게 됨에 따라, 자연스럽게 쓰여지는 라이브러리나 프레임워크의 수도 증가하게 되었고,
웹 애플리케이션을 구성하는 파일의 양이 늘어나게 되었다.
이로 인해 발생되는 큰 두가지 문제가 있었는데,

### 1. 중복된 이름으로 인한 에러

두개 이상의 스크립트 파일에서 동일한 변수명을 선언할 경우, 그 변수를 참조할 때에 문제가 생길 수 있다.
파일이 적다면 변수명을 나눠서 사용하는 등의 방법이 있겠지만, 현대의 웹 애플리케이션은 수많은 개발자가
수많은 코드를 작성하기 때문에 이를 미연에 방지하기란 불가능에 가깝다.

### 2. 파일 전송 문제

유저가 브라우저에 URI를 입력하면, URI에 해당하는 파일을 서버로부터 가져오게 되는데, 만약 파일이 많다면
요청을 처리하는 시간이 증가하게 된다. 하나의 스크립트에 모든 것을 작성하면 해결할 수 있겠지만, 유지보수 측면에서도
코드 가독성 면에서도 좋은 방법이 아니다.

## 번들러의 탄생

---

위의 이유로 인해 여러개의 파일(React, vue, svelte, sass 등등등... )을 HTML, CSS, Javascript, jpg, png 등의
정적(static)인 파일로 묶어주는 번들러가 탄생하게 되었다.
반드시 자바스크립트 파일 뿐만 아니라, 애플리케이션에 필요한 모든 종류의 파일들을 모듈 단위로 나누어 최소한의 파일 묶음(번들)로
만들어낸다.
대표적으로, Parcel, Webpack, rollup등이 있다.

### 번들러는 모든 것들을 알아서 변환해주는가?

번들러가 변환을 할 때, 번들러가 스스로 변환을 시키는 것이 아니라 번들러에서 변환이 가능하게 하도록 할 수 있는 패키지를 설치해야 한다.
예를 들면, Sass에서 CSS 파일로 변환을 할 때 sass라는 외부 패키지를 설치해서 변환을 해 주는 것이다.

## Parcel과 Webpack

---

### Parcel

- 구성 없는 단순한 자동 번들링
- 소/중형 프로젝트에 적합

### Webpack

- 매우 꼼꼼한 구성
- 중/대형 프로젝트에 적합