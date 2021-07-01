# 딥러닝 실시간 전력수요 예측모니터링 웹시스템

# 목적: 실시간으로 발생하는 전력데이터를 대상으로 분석 및 예측 구조를 개발하여, 사용자에게 실시간으로 유의미한 예측정보를 제공하는 딥러닝을 이용한 실시간 전력수요예측 및 가시화 시스템을 구축

# 역할: 클라이언트(가시화)
   화면설계, 구글맵 인터페이스, 그래프(차트) 설계 및 구현 (스크립트)
   UI설계 및 배치, GoogleMap API(NaverMapAPI), D3, Chart js
   
• 구글맵 기반 위치정보 페이지
• 지역별 실시간 전력사용량 그래프
• 지역별 실시간 전력수요예측 그래프
• 지역별 전력사용량과 수요예측 통계정보 그래프

![스크린샷(235)](https://user-images.githubusercontent.com/62291578/124079785-8d887280-da84-11eb-8422-a7996b711626.png)

### 설치할 모듈


    1. kakaodev 사이트에서 javascript app key를 받아온다. 
    2. 리액트 프로젝트를 생성한다. $ yarn create react-app hooks-tutorial (cd C:\Users\name\React.js\Medium\hooks-tutorial )
    3. node.js 설치 / git bash 터미널 사용/ visual studio code 편집기 사용
    4. yarn add @material-ui/core, yarn add @material-ui/icons 설치하기 (네비게이션 바의 툴을 만들기 위함)
  


### 실행 과정


    1. public 폴더에 index.html 수정
    2. src 폴더에 components 와 page 폴더 생성
    3. src 폴더에 data 폴더 생성 후 에 markderdata.js 파일 생성


### 함수 및 파일 설명


> public : 가상 DOM이 들어갈 빈 껍데기 html이 필요한데, 그 html 이 존재하는 폴더입니다.
> > index.html: html 파일로 위에서 받아온 javascript app  key 를 적어줍니다.

> src : 리액트 개발이 이루어지는 메인 폴더
> > components 폴더 -map 폴더 - map.js : 지도 생성 함수( mapscript) , 마커 표시 함수 
> > components 폴더 -map 폴더 - kakaomap.js : 실제로 카카오맵이 담길 컴포넌트 

### 10.29 


    1.지도 컨트롤 줌인 , 줌아웃 이벤트 등록하기
    2.커스텀 마커 생성하기 
    3.키워드로 장소 검색하고 마커 표시하기
    4.네비게이션 바, 화면 분할 방법에 대해 알아봄

### 11.12


    
    1. 리액트 네비바 
       :네비바를 부트스트랩을 이용해서 띄웠는데 검색창이 나오면서 사라지는 문제점이 있었음. 검색코드가 index.html에 있으면 안되는 거 같음, 사이드바 네비바를 연습해봐야함 .. (복잡)
    2. d3 를 react 화면에 띄우기 
    3. 리액트 사이드바 참고 문서 https://gaemi606.tistory.com/139
    4. 리액트 강의 수강 
    (1)reactjs 개념, jsx특징, props, state, 컴포넌트 매핑 알아보기 
    (2)작업환경 설정하기 ( -> react project 만드는 도중 webpack  오류 발생.ㅠ , )
    (3)contract 검색기능 구현(input, sort , filter) , contact 선택기능)
    (4)handleclick, change, remove, update 기능 구현
    (5)component lifecycle api
    종류 
    *constructor: 컴포넌트가 처음 만들어질때 실행된다. 기본 state를 설정할 수 있다.
    constructor(props){
        super(props);
        console.log('constructor');
     }
     *componentWillMount: 컴포넌트가 dom위에 만들어지기 전에 실행되어 여기엔 dom처리를 할 수없다.
     *componentDidMount: 첫 렌더링 마치고 실행된다. 이 안에서 다른 자바스크립트 프레임워크 연동 및              setTimeout, setInterval 및 AJAX 사용
     *componentWillReceiveProps: props를 받을 때 실행된다. props 에 따라 state를 업데이트 할 때 사용하면
     유용하다.  이 안에서 setstate를 해도 좋다.
     *shouldComponentUpdate: props/state가 변경되었을 때 리 렌더링을 할지말지 정한다. 실제로 사용할 떈 필요
     한 비교를 하고 값을 반환한다.
     *componentWillUpdate: 컴포넌트 업데이트 전 실행된다 . 여기서 setstate절대 사용하지 말것
     *componentDidUpdate: 컴포넌트가 리렌더링을 마친 후 실행된다. 여기서 setstate 사용하지 말것
     *componentWillUnmount: 컴포넌트가 dom에서 사라진 후 실행된다.
     (6) redux 배경지식 mvc, flux
     redux가 있으면 store에 반영해서 빨라짐 
     특징 1. single source of truth (어플리케이션의 state를 위해 단 한개의 store를 사용한다.
     특징2 . state is read only store의 state를 직접 변경할 수 없다. 변경하기 위해선 무조건 action이 dispatch 되야한다.
     특징3. changes are made with pure functions: 객체를 처리하는 함수를 reducer라고 한다. reducer는 정보를 받아 상태를 어떻게 업데이트 할지 정한다. 
     상태객체가 직접 변경되지않고 조각들이 새로운 복사본에 합쳐져 만들어진다.
     (7) redux action: 
     redux reducer: 변화를 일으켜야하고 비동기작업x, 인수변경x, 동일한 인수=동일한 결과, 기존상태를 복사하고 변환을 준 다음 반환한다. 
     
     redux store: action을 reducer에게 보낸다. redecer가 새 상태를 주면 갈아끼운다. 
     
     redux:react-redux
     
    
