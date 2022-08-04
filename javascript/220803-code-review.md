# 오늘 한 일

- 김민태의 프론트엔드 아카데미 수강
- JS 토이프로젝트 코드 리뷰
  - [innerHTML vs appendChild()](https://marian-caikovski.medium.com/innerhtml-vs-appendchild-e74c763846df)
  - github 상에 올린 코드에는 console.log가 적혀있지 않는 것이 좋다.
  - CSS visibility hidden vs display none의 차이
  - HTML rel="noopener noreferrer"
  - 고차함수 (클로저)

다음 토이프로젝트는 완성해서 제출할 수 있도록!!! 화이팅 얍얍.

---

# 오늘의 코드

고차함수... 클로저... closure  
클로저는 외부 변수를 기억하고 이 외부 변수에 접근할 수 있는 함수를 의미합니다.

```js
function init() {
  var name = 'Mozilla'; // name은 init에 의해 생성된 지역 변수이다.
  function displayName() {
    // displayName() 은 내부 함수이며, 클로저다.
    alert(name); // 부모 함수에서 선언된 변수를 사용한다.
  }
  displayName();
}
init();
```

```js
function add(baseNumber) {
  function returnedFunction(secondNumber) {
    // returnedFunction(secondNumber) 클로저
    return baseNumber + secondNumber;
  }
  return returnedFunction;
}
```

실행시

```js
add(1)(5)
// 6

add(1)
// f returnedFunction(secondNumber) {
//  return baseNumber + secondNumber
// }
```

고차함수: return값이 함수이거나 인자로 콜백함수를 전달받는 함수  
콜백함수: 다른 함수(고차함수)의 인자로 들어가는 함수

```js
function introduce(lastName, firstName, callback) {
  const fullName = lastName + firstName;
  callback(fullName); // 클로저?
}
function say_hello(name) {
  console.log('안녕하세요 제 이름은 ' + name + '입니다'); // 클로저?
}
function say_bye(name) {
  console.log('지금까지 ' + name + '이었습니다. 안녕히 계세요'); // 클로저?
}

introduce('홍', '길동', say_hello);
// 안녕하세요 제 이름은 홍길동입니다
introduce('우', '영우', say_bye);
// 지금까지 우영우이었습니다. 안녕히 계세요
```

function introduce는 고차함수  
function say_hello와 say_bye는 콜백함수

---

# 내일 할 일

- 알고리즘 강의 수강
- 리액트 강의 수강 useEffet

<strong>JavaScript</strong>

- freeCodeCamp JavaScript Algorithms and Data Structures
- 김민태의 프론트엔드 아카데미: 제 1강 JavaScript & TypeScript Essential  
  진행 중➡️
