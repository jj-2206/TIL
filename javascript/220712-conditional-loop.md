# 오늘 한 일

- JavaScript
  - switch 문
  - for 문 
    - 중첩 for 문, 삼각형 만들기  

# 오늘의 코드

 - 틀린 코드 
```js
let browser = '';
if (browser === 'Edge') {
  console.log('Edge를 사용하고 계시네요!');
} else if (browser === 'Chrome' || 'Firefox' || 'Safari' || 'Opera') {
  console.log('저희 서비스가 지원하는 브라우저를 사용하고 계시네요.');

} else {
  console.log('현재 페이지가 괜찮아 보이길 바랍니다!');
}
// 저희 서비스가 지원하는 브라우저를 사용하고 계시네요.
```
browser === 'Chrome' 을 비교한 뒤에 'Firefox'와 비교하게 되는 연산이 된다.  
false || 'Firefox' 의 비교가 되어 'Firefox'를 결과값으로 인식하기 때문에  
콘솔에 '저희 서비스가 지원하는 브라우저를 사용하고 계시네요.' 가 출력된다.  
무엇과 비교하는지 정확하게 작성해야한다.  
  
 - 옳은 코드

```js
let browser = '';
if (browser == 'Edge') {
  console.log('Edge를 사용하고 계시네요!');
} else if (browser == 'Chrome' || browser == 'Firefox' || browser == 'Safari' || browser == 'Opera') {
  console.log('저희 서비스가 지원하는 브라우저를 사용하고 계시네요.');
} else {
  console.log('현재 페이지가 괜찮아 보이길 바랍니다!');
}
// 현재 페이지가 괜찮아 보이길 바랍니다!
```
# 내일 할 일

- JavaScript 강의 듣기 4-1 까지 목표.
- 실강 자료 퀴즈 복습
