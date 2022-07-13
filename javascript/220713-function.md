# 오늘 한 일

- 함수
  - 화살표 함수, 호이스팅, 콜백
- 생성자 함수, prototype, this, extends, super

자바스크립트는 명령형, 함수형, `prototype` 기반 객체지향 프로그래밍을 지원하는 멀티 패러다임 프로그래밍 언어다.

아직 콜백 함수가 헷갈린다.

```js
function timeout(callback) {
  setTimeout(() => {
    console.log('happy!'); // happy!
    callback();
  }, 3000);
}
timeout(() => {
  console.log('done!'); // done!
});
```

여기에서의 콜백 함수는... setTimeout()과 timeout()인지, timeout()만 해당하는건지...  
모양은 (()=>{}) 같아보이는데... 😵‍💫

# 오늘의 코드

- 별 찍기 과정, $와 변수 i,j,k 출력

```js
let lineCount = 5;
let result = '';

for (let i = 1; i < lineCount * 2; i += 2) {
  for (let j = 1; j < (lineCount * 2 - i) / 2; j++) {
    console.log(`${i}`, `${j}`);
    result += '$';
  }
  for (let k = 1; k <= i; k++) {
    console.log(`${k}`);
    result += '*';
  }
  result += '\n';
}
console.log(result);
```

# 내일 할 일

- JavaScript 이론 정리

