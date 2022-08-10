# Done

- 노마드 코더 챌린지 - 제출 코드와 정답 코드 비교, 오늘치 코드 제출
- PM 특강

  - Software Development Life Cycle 개발 생명 주기
    - `요구사항 분석` -> 설계 -> 구현 -> 테스트 -> 유지 및 보수
  - Waterfall, Spiral
  - Agile
    - Code-oriented Methodology 코드 중심
    - TDD Test Driven Development 테스트 주도 개발
    - OOP Object Oriented Programming 객체 지향 프로그래밍 (JavaScript...!)
    - eXtreme Programming, Scrum
  - 협업에서의 GitHub 사용
    - Issue & Projects
    - Assignees: 이 이슈에 대한 책임인원  
      Labels: 이슈의 종류  
      Projects: 이슈를 배당할 프로젝트  
      Milestone: 이슈에 해당하는 중요 시점 지정
  - 요구사항의 동사형은 언제나 명령형으로 작성한다.  
    (~해야한다, ~서는 안된다)  
    해석의 여지가 있으면 안된다.
  - 실습
    - 절차: 기획 -> 설계 및 Issue 작성
    - [Wiki](https://github.com/team-5jo/The-Game-of-Pig/wiki)

  요구사항 문서 작성 잘했다고 칭찬 받았다. 헤헤,,,  
   `pigma` 다룰 줄 알아야한다!

# Today's code

useReducer(state값, dispatch함수)  
useState와 비슷한 구조를 가졌다...  
dispatch(action)으로 reducer함수 호출...  
이해가 어렵다...

```js
import { useReducer } from 'react';

function reducer(state, action) {
  // action.type에 따라 다른 작업 수행
  switch (action.type) {
    case 'INCREMENT':
      return { value: state.value + 1 };
    case 'DECREMENT':
      return { value: state.value - 1 };
    default:
      // 아무것도 해당되지 않을 때 기존 상태 반환
      return state;
  }
}

const Counter = () => {
  const [state, dispatch] = useReducer(reducer, { value: 0 });
  return (
    <div>
      <p>
        현재 카운터 값은 <b>{state.value}</b>입니다.
      </p>
      <button onClick={() => dispatch({ type: 'INCREMENT' })}> +1 </button>
      <button onClick={() => dispatch({ type: 'DECREMENT' })}> -1 </button>
    </div>
  );
};

export default Counter;
```

# To do

- 리액트: 리액트를 다루는 기술 ~ch17
- 리액트 강의 복습
- 노마드코더 챌린지
