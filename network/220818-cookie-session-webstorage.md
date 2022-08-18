# Done

- React로 To do list 만들기  
  따라 만들었는데, 따라 만들면서도 useCallback 사용하는 부분이 아리송했다...
  ```
  컴포넌트의 성능을 아낄 수 있도록 ~ props로 전달해야 할 함수를 만들 때는 useCallback을 사용하여 함수를 감싸는 것을 습관화하세요.
  ```
- 브라우저 저장소

  - cookie
    - 브라우저에 저장되는 데이터의 일종
    - 도메인 단위로 데이터 저장
    - \*자동으로 HTTP Request에 포함된다.
  - session
    - 쿠키에는 서버가 발급해준 id만 저장, 데이터는 서버에 저장
    - 데이터를 서버에 저장하므로 보안상 유리
    - session id 를 서버에 저장하고 있어야하므로 메모리 차지
  - web storage

    - web storage: http request에 포함되지 않으므로 트래픽 절약
    - cookie: 용량 최대 4KB, web storage: 용량 최대 5MB
    - LocalStorage: 직접 삭제하지 않으면, 탭 혹은 브라우저를 종료해도 데이터 유지
    - SessionStorage: 탭 혹은 브라우저를 종료하면 데이터 소멸

    [쿠키와 세션 개념](https://interconnection.tistory.com/74)

# Today's code

```js
document.cookie = 'a=1';
document.cookie = 'b=2';
document.cookie = 'a=3';
document.cookie = 'b=2; max-age=0';
```

```js
localStorage.setItem('a', 1);
localStorage.getItem('a');
localStorage.removeItem('a');
```

# To do

- redux, react-redux, middleware
- 김민태의 프론트엔드 아카데미
