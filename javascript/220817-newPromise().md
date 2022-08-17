# Done

- 자바스크립트 보강
  - 생성자 함수, 인스턴스
  - static `클래스의 정적 메서드`
  - prototype

제대로 아는 게 하나도 없다,,,  
this, new Upper(), 인스턴스(생성자 함수로 만든 객체,,,?) 공부하자!

# Today's code

`정적 메서드`는 클래스의 `인스턴스` 없이 호출이 가능하며 클래스가 인스턴스화되면 호출할 수 없다.

```js
class People {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
  getAge() {
    return this.age;
  }
  static getLegs() {
    return 2;
  }
}

const jj = new People('JJ', 100);
// jj는 인스턴스!
const loopy = new People('Loopy', 10);
// loopy는 인스턴스!

console.log(jj.getAge()); // 100
console.log(People.getLegs()); // 2
console.log(jj.getLegs()); // Uncaught TypeError: jj.getLegs is not a function
```

사실 자바스크립트는 `prototype 기반 상속`이기 때문에 아래와 같이 동작하는 것이다.

```js
function People(name, age) {
  this.name = name;
  this.age = age;
}
People.prototype.getAge = function () {
  return this.age;
};
People.getLegs = function () {
  return 2;
};
const jj = new People('JJ', 100);
const loopy = new People('Loopy', 10);

console.log(jj.getAge()); // 100
console.log(loopy.getAge()); // 10
console.log(People.getLegs()); // 2
console.log(jj.getLegs()); // Uncaught TypeError: jj.getLegs is not a function
```

```
People.getLegs = function () {
  return 2;
};
```

이렇게 작동되는 거라고 이해했는데,,, 강사님께 질문해봐야겠다.

# To do

- React로 To do list 만들기
- 생활코딩 redux, react-redux
- 김민태의 프론트엔드 아카데미 제 1강 JavaScript & TypeScript Essential
