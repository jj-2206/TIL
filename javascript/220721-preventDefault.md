# 오늘 한 일

- JavaScript 문법 복습
- 실시간 강의

<strong>JavaScript</strong>

- freeCodeCamp JavaScript Algorithms and Data Structures  
  <b>Basic JavaScript</b> 완료✅ 113/113  
  <b>ES6</b> 예정 ➡️ /29
- 김민태의 프론트엔드 아카데미: 제 1강 JavaScript & TypeScript Essential 잠시 멈춤 ■■□□□□□

오늘은 멘토링이 있었다.  
문법 공부만 하다보니까 머릿속에 입력이 되고 있는건지, 이 공부? 익히는 방법이 맞는지 답답해서 말씀드렸더니 클론 코딩이라도 [일단 듣고 - 따라 치고 - 지우고 (이해) - 내가 만들어보기] 식으로 익히는 게 좋을 것 같다는 결론에 도달했다.  
물론 문법도 문법대로 계속 공부해야겠지만 직접 화면을 작성해보기로!!!

# 오늘의 코드

input

```html
<html>
  <body>
    <form>
      <input id="input" type="text" placeholder="값을 입력하고 enter" />
    </form>
    <div>div 내 text가 변경됩니다</div>
  </body>
  <script>
    const input = document.getElementById('input');
    input.addEventListener('keypress', (e) => {
      // console.log(e.key);
      event.preventDefault();
      // input에서 enter를 눌렀을 때의 기본 동작인,
      // [form 엘리먼트의 submit 이벤트를 발생시킨다]
      // 위 동작을 preventDefault로 막아준 것입니다.
      if (e.key === 'Enter') {
        const div = document.querySelector('div');
        div.innerText = e.target.value;
      }
    });
  </script>
</html>
```

```html
<html>
  <head>
    <style>
      .some-div {
        width: 100px;
        height: 100px;
        margin: 10px;
      }
    </style>
  </head>
  <body>
    <input id="input" type="text" placeholder="값을 입력하고 enter" />
  </body>
  <script>
    const input = document.getElementById('input');
    input.addEventListener('keypress', (e) => {
      if (e.key === 'Enter') {
        console.log(e.target.value);
        const newDiv = document.createElement('div');
        newDiv.className = 'some-div';
        newDiv.style.backgroundColor = input.value;
        input.value = '';
        document.body.appendChild(newDiv);
      }
    });
  </script>
</html>
```

# 내일 할 일

- JavaScript! JavaScript!

