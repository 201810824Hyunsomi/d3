# REACT로 KAKAOMAP!

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
    4. 리액트 강의 수강 reactjs 개념, jsx특징, props, state, 컴포넌트 매핑 알아보기 
    작업환경 설정하기 ( -> react project 만드는 도중 webpack  오류 발생.ㅠ , )
    contract 검색기능 구현(input, sort , filter) , contact 선택기능)
