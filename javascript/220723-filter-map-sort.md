# 오늘 한 일

- 진상현 강사님 JavaScript 강의 퀴즈 복습

<strong>JavaScript</strong>

- freeCodeCamp JavaScript Algorithms and Data Structures  
  <b>Basic JavaScript</b> 완료✅ 113/113  
  <b>ES6</b> 진행중 ➡️ 9/29  
  <b>Debugging</b> 진행중 ➡️ 10/12

- 김민태의 프론트엔드 아카데미: 제 1강 JavaScript & TypeScript Essential 잠시 멈춤 ■■□□□□□

-> 퀴즈 복습에 7시간이 걸렸다...

# 오늘의 코드

map 메소드의 활용법을 더 많이 익혀야겠다.

```js
const arr = [
  {
    name: 'kim',
    age: 10,
  },
  {
    name: 'choi',
    age: 13,
  },
  {
    name: 'jin',
    age: 20,
  },
  {
    name: 'woo',
    age: 50,
  },
  {
    name: 'woo',
    age: 20,
  },
  {
    name: 'woo',
    age: 30,
  },
];

const findAge = (name) => {
  const trimmedName = name.trim().toLowerCase();
  const foundAge = arr
    .filter((item) => trimmedName === item.name)
    /*
    (3) [{…}, {…}, {…}]
      0: {name: 'woo', age: 50}
      1: {name: 'woo', age: 20}
      2: {name: 'woo', age: 30}
      length: 3
      [[Prototype]]: Array(0)
    */
    .map(({ age }) => age)
    /*
    (3) [50, 20, 30]
      0: 50
      1: 20
      2: 30
      length: 3
      [[Prototype]]: Array(0)
    */
    .sort((a, b) => b - a);

  return foundAge;
};
console.log(findAge(' WoO '));

/*
(3) [50, 30, 20]
0: 50
1: 30
2: 20
length: 3 
[[Prototype]]: Array(0)
*/
```

.sort((a, b) => b - a); 내림차순이 되는 이유

```js
let someNumberArray = [5, 4, 3, 2, 1];
someNumberArray.sort((next, prev) => (prev > next ? -1 : 0)); // return [1, 2, 3, 4, 5]
// 이전 엘리먼트가 이후 엘리먼트보다 크면 순서를 바꾸기 때문에 결국 오름차순으로 정렬됩니다.
```

```
만일, 오름차순으로 정렬하고 싶다면

arr.sort((a, b) => a - b)와 같이 작성하면 됩니다. b 가 더 클 때만 a - b의 결과로 음수가 나옵니다. 그러면 b 즉, 앞에 있는 값이 더 클 때 변경이 일어나니까 뒤에 있는 큰 값이 다 앞으로 오게 돼서 오름차순 정렬이 됩니다.

만일, 내림차순으로 정렬하고 싶다면

arr.sort((a, b) => b-a)와 같이 작성하면 됩니다. a (뒤에 있는 값을 의미)가 더 클 때만 b - a 의 결과로 음수가 나오겠죠? 그러면 결국 뒤에 있는 값이 클 때 변경이 일어나기 때문에, 큰 값은 뒤로 가게 되고 작은 값은 앞으로 오게 돼서 내림차순 정렬이 됩니다.
```

[sort 참고 블로그](https://velog.io/@jakeseo_me/Javascript-Sort%ED%95%A8%EC%88%98%EC%97%90-%EB%8C%80%ED%95%9C-%EC%9E%A1%EC%A7%80%EC%8B%9D)

# 내일 할 일

- HTML CSS JavaScript 정리
  - 김준태 강사님 자료 정리
  - [바닐라 JS로 크롬 앱 만들기](https://nomadcoders.co/javascript-for-beginners)

