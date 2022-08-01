# 오늘 한 일

- 토이 프로젝트,,,  
  어려워보이는 것들만 남았다,,, API로 검색 구현하는 것도 나에게는 매우 어려웠지만 ㅠ0ㅠ  
  시간이 없다,,,  
  페이지를 어떻게 넘기는 거지,,, 빙글뱅글 @\_@,,, 넘기고 싶다,,,!

# 오늘의 코드

Intersection Observer API? scroll?

```js
const numSteps = 20.0;

let boxElement;
let prevRatio = 0.0;
let increasingColor = 'rgba(40, 40, 190, ratio)';
let decreasingColor = 'rgba(190, 40, 40, ratio)';

// Set things up
window.addEventListener(
  'load',
  (event) => {
    boxElement = document.querySelector('#box');

    createObserver();
  },
  false
);
```

```js
let last_known_scroll_position = 0;
let ticking = false;

function doSomething(scroll_pos) {
  // scroll 위치에 대한 작업을 하세요
}

window.addEventListener('scroll', function (e) {
  last_known_scroll_position = window.scrollY;

  if (!ticking) {
    window.requestAnimationFrame(function () {
      doSomething(last_known_scroll_position);
      ticking = false;
    });

    ticking = true;
  }
});
```

# 내일 할 일

- 토이 프로젝트
- 실시간 리액트 강의

<strong>JavaScript</strong>

- freeCodeCamp JavaScript Algorithms and Data Structures  
  잠시 멈춤 ■□□□□□□□□□

- 김민태의 프론트엔드 아카데미: 제 1강 JavaScript & TypeScript Essential  
  잠시 멈춤 ■■□□□□□
