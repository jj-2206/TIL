# 오늘 한 일

- 토이 프로젝트
- React 실시간 강의  
   `useRef`  
   useRef를 사용하여 ref를 설정하면 useRef를 통해 만든 객체 안의 current 값이 실제 엘리먼트(DOM)를 가리킵니다.

  - ref는 dom을 담을 때만 쓸 수 있다? -> X
  - ref는 값이 바뀌어도 컴포넌트가 re-render 되지 않는다? -> O
  - react에 의한 re-render가 아닌,
    실제 document에 존재하는 element를 직접 접근하여 수정
  - react state로는 관리할 수 없는 경우에만 사용하는 것이 적절

  `useEffect`  
   side effect를 다룰 때 사용하는 hooks.  
   리액트 컴포넌트가 렌더링될 때마다 특정 작업을 수행하도록 설정할 수 있는 hook입니다.

  - 첫번째 인자로 실행할 콜백함수를 넘겨준다.
  - App 함수컴포넌트가 다시 실행(렌더)되더라도,
    콜백함수는 첫번째 render이후에만 실행
  - useEffect 함수의 두번째 인자: dependency array
  - 최초 render이후 1회 실행
    그 다음부턴 dependency array에 넣은 값이 바뀌면, callback함수 재실행

useEffect 다시 공부해야겠다,,,

# 오늘의 코드

controlled input

```js
import React, { useState, useRef } from 'react';

export default function App() {
  const [id, setId] = useState('');
  const [pw, setPw] = useState('');

  const idRef = useRef(null);
  const pwRef = useRef(null);

  const idError = '유효하지 않은 id입니다.';
  const pwError = '유효하지 않은 password입니다.';

  const idCheck = id.length >= 6 && id.length <= 20;
  const pwCheck = pw.length >= 12 && pw.length <= 20;

  const handleIdChange = (event) => {
    if (event.target.name === 'id') {
      setId(event.target.value);
    }
  };

  const handlePwChange = (event) => {
    if (event.target.name === 'pw') {
      setPw(event.target.value);
    }
  };

  const handleClick = () => {
    if (!idCheck) {
      alert(idError);
      setId('');
      idRef.current.focus();
    } else if (!pwCheck) {
      alert(pwError);
      setPw('');
      pwRef.current.focus();
    } else alert('회원가입 성공!');
  };

  return (
    <div>
      <div>
        <input
          type="text"
          name="id"
          placeholder="6글자 이상 20글자 이하"
          ref={idRef}
          value={id}
          onChange={handleIdChange}
        />
      </div>
      {idCheck ? null : idError}
      <div>
        <input
          type="text"
          name="pw"
          placeholder="12글자 이상 20글자 이하"
          ref={pwRef}
          value={pw}
          onChange={handlePwChange}
        />
      </div>
      {pwCheck ? null : pwError}

      <div>
        <button type="button" onClick={handleClick} disabled={id || pw ? false : true}>
          회원가입
        </button>
      </div>
    </div>
  );
}
```

이렇게도 가능!

```
disabled={!(id || pw)}
```

# 내일 할 일

- 토이 프로젝트 제출 ~17:00
- 토이 프로젝트 코드 해설,,,

<strong>JavaScript</strong>

- freeCodeCamp JavaScript Algorithms and Data Structures  
  잠시 멈춤,,, ■□□□□□□□□□

- 김민태의 프론트엔드 아카데미: 제 1강 JavaScript & TypeScript Essential  
  잠시 멈춤,,, ■■□□□□□
