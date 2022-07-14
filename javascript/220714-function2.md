# 오늘 한 일

- JavaScript
  - 첫술에 배 부르랴  
    강의 한 번 봤다고 퀴즈를 술술 풀 수 있길 바라는 게 도둑놈 심보겠지만, 계속 퀴즈를 풀지 못하면 슬퍼진다...  
    어제 웹으로 JavaScript 배우기를 검색을 하다가 `freecodecamp.org`를 발견했는데 오늘 강사님이 강의하시다가 좋은 곳이라고 소개해주셔서 확신을 가졌다. 할 수 있는 방법을 총동원해서... JavaScript를 많이 접해야겠다.

# 오늘의 코드

- `callback`  
  매개변수로 함수를 넘겨받아 호출하는 패턴.  
  이 때, 넘겨받은 함수를 `callback` 함수라고 부른다.  
  여기에서는 func1과 func2가 `callback` 함수겠다.

```js
function checkBoolean(bool, func1, func2) {
  if (bool) {
    func1();
  } else {
    func2();
  }
}
```

# 내일 할 일

- JavaScript 필수 강의 - part.4 Ch.3 완강
