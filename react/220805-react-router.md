# 오늘 한 일

- 온라인 강의 - 리액트
  - useState, useEffect, Hook 만들기
- 리액트
  - (useMemo, useCallback), react-router, useParams
- 자바스크립트
  - 노마드코더 챌린지 Assignment 5

# 오늘의 코드

wildcard와 Navgiate

```js
import React from 'react';
import { BrowserRouter, Navigate, Route, Routes, Link } from 'react-router-dom';

const Hi = () => {
  return <>Hi 뒤로 가기 눌러도 안될 겁니당,,, </>;
};

const Main = () => {
  return (
    <>
      This is Main Component <br />
      <Link to="/abc"> 클릭하면 영원한 Hi에 갇히게 됩니다,,, </Link>
    </>
  );
};

const App = () => {
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<Main />} />
        <Route path="/hi" element={<Hi />} />
        <Route path="*" element={<Navigate to="/hi" replace={false} />} />
        {/* abc라고 지정된 path가 없어서 * path로 들어가게 됩니다. */}
        {/* replace = replace={true}  props.replace는 browser history에 영향을 끼칩니다. */}
      </Routes>
    </BrowserRouter>
  );
};

export default App;
```

# 내일 할 일

- 밀린 온라인 강의 수강

  1. React (React 공식문서로 디테일잡기)
  2. 김민태의 프론트엔드 아카데미 : 제 1강 JavaScript & TypeScript Essential
  3. type script

- toy project 다른 분들 코드, 강사님 코드 읽기
