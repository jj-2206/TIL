# 오늘 한 일

- JavaScript 문법 복습

<strong>JavaScript</strong>

- freeCodeCamp JavaScript Algorithms and Data Structures <b>Basic JavaScript</b> 진행중 ➡️ 103/113
- 김민태의 프론트엔드 아카데미: 제 1강 JavaScript & TypeScript Essential 잠시 멈춤 ■■□□□□□

# 오늘의 코드
freeCodeCamp  
- Replace Loops using Recursion

```js
  function sum(arr, n) {
    if (n <= 0) {
      return 0;
    } else {
      return sum(arr, n-1) + arr[n-1];
    }
  }
console.log(sum([2, 3, 4, 5], 3)); // 9
console.log(sum([1], 0)); // 0
console.log(sum([2, 3, 4], 1)); // 2
```
배열과 인덱스를 생각하는 문제였다.

# 내일 할 일

- JavaScript 문법 익히기

