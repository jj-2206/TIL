# Done

- 리액트를 다루는 기술 ~ch11  
  useReducer
- 노마드코더 챌린지
  - 재귀
  - [모듈 내보내고 가져오기](https://ko.javascript.info/import-export)

```
// index.html
<script defer src="./js/weather.js" type="module"></script>

// apikey.js
export const API_KEY = '123456789';

// weather.js
import { API_KEY } from './apikey.js';
const url = https://api.openweathermap.org/data/2.5/weather?lat=${lat}&lon=${lon}&appid=${API_KEY}&units=metric;
```

# Today's code

useReducer

```js
const todoReducer = (todos, action) => {
  switch (action.type) {
    case 'INSERT':
      return todos.concat(action.todo);
    case 'REMOVE':
      return todos.filter((todo) => todo.id !== action.id);
    case 'TOGGLE':
      return todos.map((todo) =>
        todo.id === action.id ? { ...todo, checked: !todo.checked } : todo,
      );
    default:
      return todos;
  }
};

const App = () => {
  const [todos, dispatch] = useReducer(todoReducer, undefined, createBulkTodos);
  // const [state, dispatch] = useReducer(reducer, initialArg, init);

    const onInsert = useCallback((text) => {
    const todo = {
      id: nextId.current,
      text,
      checked: false,
    };

    dispatch({ type: 'INSERT', todo });
    nextId.current += 1; // nextId 1씩 더하기
  }, []);

  const onRemove = useCallback((id) => {
    dispatch({ type: 'REMOVE', id });
  }, []);

  const onToggle = useCallback((id) => {
    dispatch({ type: 'TOGGLE', id });
  }, []);

```

# To do

- 생활코딩
  - React 2022
  - React Redux
- freeCodeCamp
  - Functional Programming
