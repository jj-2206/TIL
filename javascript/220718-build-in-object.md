# 오늘 한 일

- JavaScript console에 다시 풀어보기

<strong>JavaScript</strong>

- freeCampCode JavaScript Algorithms and Data Structures <b>Basic JavaScript</b> 진행중 ➡️ 40/113
- 김민태의 프론트엔드 아카데미: 제 1강 JavaScript & TypeScript Essential 잠시 멈춤 ■■□□□□□

# 오늘의 코드

array 내장객체 퀴즈..  
find()와 `콜백함수` 정확히 이해하기

```js
arr.find(findAge('jin')).age; // 20
arr.find(findAge('woo')).age; // 30
```

```js
const arr = [
  {
    name: 'kim',
    age: 10,
  },
  {
    name: 'park',
    age: 15,
  },
  {
    name: 'lee',
    age: 12,
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
    age: 30,
  },
];

// quiz.1
function findAge(a) {
  console.log('findAge호출', a);
  return function (item) {
    console.log('findAge가 리턴한 함수 호출', item);
    if (item.name === a) return true;
  };
}

console.log(arr.find(findAge('jin')).age);
```

# 내일 할 일

- JavaScript 복습!!!!!!!!!!
- JavaScript 라이브 강의 출석

