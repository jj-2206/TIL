# 오늘 한 일

- 리액트를 다루는 기술 ~ch04
- 리액트 강의 styled-component, 전역 상태 관리  
  `전역 상태 관리` 단어부터 어려운 느낌이라 예습을 할 수 있는만큼 하고 수업 들어야겠다.
- 조별 회고 1등 했다,,, 항항항,,, 스타벅스 가야지,,,  
  조별 회고 시간이 마지막이어서 아쉬웠지만 JS 보충을 할 수 있는 시간이 늘어서 좋기도 하다.

# 오늘의 코드

keyframes  
props의 이동을 잘 이해하고 싶다!ㅜ0ㅜ

```js
const boxAnimation = (color) => keyframes`
  0% {
    background-color: black;
  }
  50% {
    background-color: ${color};
  }
  100% {
    background-color: red;
  }
`;

const Box = styled.div`
  width: 100px;
  height: 100px;
  background-color: black;
  animation-name: ${(props) => boxAnimation(props.color)};
  animation-duration: 3s;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
`;

const HelloTitle = styled.div`
  color: ${({ color: { me } }) => me};
`;

const Hello = ({ list, setList }) => {
  const [value, setValue] = useState('');
  const handleChange = (e) => {
    setValue(e.target.value);
  };
  const handleClick = () => {
    setList(list.concat([value]));
    setValue('');
  };
  console.log({ list });
  return (
    <>
      <Box color={value} />
      <h1>this is Hello Component</h1>
      <HelloTitle color={{ me: 'green' }}>글쓰기 화면</HelloTitle>
      <br />
      <input value={value} type="text" onChange={handleChange} />
      <button onClick={handleClick}>등록</button>
      <br />
      <p>----글 리스트----</p>
      {list.map((item, i) => (
        <Link key={i} to={`/post/${i}`}>
          <div>{item}</div>
        </Link>
      ))}
      <p>-------------------</p>
      <div>
        <Link to="/">return to form</Link>
      </div>
    </>
  );
};
```

# 내일 일정

- 08:00 ~ 09:00 노마드코더 바닐라 JS 챌린지
- 09:00 ~ 12:30 리액트를 다루는 기술, 리액트 복습
- 13:00 ~ 14:00 알고리즘 day1 복습
- 14:00 ~ 17:00 알고리즘 강의
- 19:00 ~ 22:00 리액트 강의
