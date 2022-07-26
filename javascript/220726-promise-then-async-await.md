# 오늘 한 일

- JavaScript 실시간 강의
- 노마드코더 바닐라JS로 크롬 앱 만들기 진행 중 ➡️ ■■■■■■□□

<strong>JavaScript</strong>

- freeCodeCamp JavaScript Algorithms and Data Structures  
  잠시 멈춤 ■□□□□□□□□□

- 김민태의 프론트엔드 아카데미: 제 1강 JavaScript & TypeScript Essential  
  잠시 멈춤 ■■□□□□□

어렵지만 재밌다...

# 오늘의 코드

비동기 `promise` `then` `async` `await`

```js
const callbackFunctionForPromise = (resolve) => {
  const someFunction = () => {
    console.log('hello world!');
    resolve();
  };
  setTimeout(someFunction, 5000);
};

const helloPromise = new Promise(callbackFunctionForPromise);
const afterFunction = () => {
  console.log('완료!');
};
helloPromise.then(afterFunction);

const startAsyncFunction = async function () {
  const helloPromise = new Promise(callbackFunctionForPromise);
  await helloPromise;
  console.log('완료!');
};
startAsyncFunction();
```

# 내일 할 일

- 토이 프로젝트
- 리액트 필수 강의...

