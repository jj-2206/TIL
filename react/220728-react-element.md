# 오늘 한 일

- React 필수강의
- React 실시간 강의  
  `CRA` React 프로젝트를 위한 bolierplate (빵틀🥖)  
  `React Element` = render하기 위한 정보를 담아둔 객체  
  `React Component` = React Element를 return 하는 함수  
  `JSX` = React Element를 생성하기 위해 사용하는 문법적 sugar
  - React Component에서의 `props`  
    `Props` = Component 라는 함수를 호출할 때 넘기는 인자

# 오늘의 코드

알쏭달쏭

MyComponent의 props로 buttonText(html 속성주듯)  
buttonText는 getButtonText함수를 실행한 리턴 값이므로  
버튼에 hello가 출력된다.

```js
function getButtonText() {
  return 'hello';
}

function MyComponent(someParam) {
  return <button>{someParam.buttonText}</button>;
}

function App() {
  return (
    <div className="App">
      <MyComponent buttonText={getButtonText()} />
    </div>
  );
}
export default App;
```

# 내일 할 일

- 토이 프로젝트...!
- 리액트

<strong>JavaScript</strong>

- freeCodeCamp JavaScript Algorithms and Data Structures  
  잠시 멈춤,,, ■□□□□□□□□□

- 김민태의 프론트엔드 아카데미: 제 1강 JavaScript & TypeScript Essential  
  잠시 멈춤,,, ■■□□□□□

