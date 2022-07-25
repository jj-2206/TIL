# 오늘 한 일

- 진상현 강사님 퀴즈 복습
- JavaScript 실시간 강의
- 노마드코더 바닐라JS로 크롬 앱 만들기 진행 중 ➡️ ■■■□□□□□

<strong>JavaScript</strong>

- freeCodeCamp JavaScript Algorithms and Data Structures  
  잠시 멈춤 ■□□□□□□□□□

- 김민태의 프론트엔드 아카데미: 제 1강 JavaScript & TypeScript Essential  
  잠시 멈춤 ■■□□□□□

내장 함수들...😭 map, reduce... 계속 보기...

# 오늘의 코드

콜백...😭
계속 보고 해보는 수밖에 없다.

```js
<html>
  <body>
    <input type="number" />
    <button>시작</button>
    <div></div>
  </body>
  <script>
    const [startBtn, endBtn] = document.querySelectorAll('button');
    // querySelectorAll 사용하는 방법!
    const inputEl = document.querySelector('input');
    const divEl = document.querySelector('div');

    let num = 3;
    let timerId;
    function consoleLog() {
      num = num - 1;
      divEl.innerText = num;
      if (num === 0) {
        window.clearInterval(timerId);
        console.log(inputEl.value);
      } // num이 0이 되면 타이머 종료
    }
    startBtn.addEventListener('click', () => {
      divEl.innerText = num;
      timerId = window.setInterval(consoleLog, 1000);
    }); // 1초마다 num을 div에 출력
  </script>
</html>
```

# 내일 할 일

- JavaScript 강의 퀴즈 복습
- 토이 프로젝트 고민 하기
