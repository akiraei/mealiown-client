# MEALIOWN-client

> - Mealiown은 식사 점수 기록 앱입니다. 식사 시간, 식사 종류, 3가지의 식사 점수를 기록합니다.
> - meal-i-own과 million의 뜻을 가지고 있습니다. '나의 식사'를 기록합니다. 한 기록당 최고점은 1000점이고 1000끼(하루 3끼 기준 333일, 약 1년)를 기록하면 총 '천만(million)'을 달성할 수 있습니다. 1000끼가 기준입니다.
> - 프로젝트는 https://mealiown.netlify.com/ 에서 확인해보실 수 있습니다.

## 프로젝트 목표


- 로그인, 로그아웃, 사인업
- 식사 점수 기록: , 정보확인, 단계확인
- 대쉬보드: 기간, 시간, 식사종류, 점수종류에 대한 필터링

## 서비스 기능

### 1. 로그인/회원가입

- 사용자는 이름/패스워드를 등록해 계정을 생성할 수 있다.
- 회원가입시 중복 아이디일 경우 안내 메시지를 제공한다.
- 로그인시 이름이나 패스워드가 틀렸을 경우 안내 메시지를 제공한다.


### 2. 기록

- 사용자는 식사에 대한 점수를 기록할 수 있다.
- faze_1에서 일자와 시각, 식사종류를 고른다.
- faze_2에서 3 단계 점수를 정한다. 요소 당 10단계가 있으며 1단계 당 점수는 2의 지수로 올라간다. 요소 당 최고점은 1000점이고 총 점은 요소의 점수의 합이다. 총 점의 최고점은 1000점이다. 
- faze_3는 faze_1과 faze_2의 정보를 확인할 수 있다.
- footer에는 현재 faze의 상태를 나타낸다.
- faze는 스크롤으로 변경 할 수 있다.

### 3. 대쉬보드

- 사용자는 대쉬보드에서 기록의 통계를 확인 할 수 있다.
- 데이터가 완전히 불러오기 전에는 loading 사인이 보인다. 
- 첫 화면은 기록 전체에 대한 정보를 보여준다.
- footer의 필터 팝업을 열면 필터 조건을 정할 수 있다.
- 조건으로는 기간, 시각, 식사종류, 점수종류를 고를 수 있다.
- 필터 조건을 정하고 submit을 클릭하면 조건에 맞는 통계를 확인 할 수 있다.
- 조건에 대한 정보를 화면 좌측 상단에서 확인 할 수 있다.

## 개발 기간

18.08.04 ~ 

## 기술 스택 & 툴
### Front-end

- UI libraries
  - react (create-react-app)
  - react-router
  - moment
  - classnames
  - [Ant design](https://ant.design/)
- Network
  - apollo-boost
  - graphql
  - react-apollo
- version control
  - git flow
- convention
  - eslint-plugin-prettier
  - prettier

### Back-end

- Server
  - [mealiown-server](https://github.com/akiraei/mealiown)
    - graphql, apollo-boost, mongoose
- Database
  - mongoDB
    - mlab
### 환경

- create-react-app 환경 빌드
- [glitch](https://even-friction.glitch.me/graphql) 를 통한 웹 서버 배포
- mlab을 통한 데이터 베이스 활용
- [netlify](https://mealiown.netlify.com/) 를 통한 웹사이트 배포