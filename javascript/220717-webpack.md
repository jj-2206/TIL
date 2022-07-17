# 오늘 한 일

- 5조 오프라인 모임＼(^0^)／ @강남역 
- 온라인 필수 강의 Webpack  
  `webpack`은 `모던 JavaScript` 애플리케이션을 위한 `정적 모듈 번들러` 입니다. webpack이 애플리케이션을 처리할 때, 내부적으로는 `프로젝트에 필요한 모든 모듈을 매핑`하고 하나 이상의 `번들을 생성`하는 디펜던시 그래프를 만듭니다.

  파일을 읽어들이는 진입점이 `entry: './js/main.js',` 자바스크립트라는 것이 생소하고 신기했다!

<strong>JavaScript</strong>

- freeCampCode JavaScript Algorithms and Data Structures <b>Basic JavaScript</b> 진행중 ➡️ 30/113
- 김민태의 프론트엔드 아카데미: 제 1강 JavaScript & TypeScript Essential 진행중 ➡️ ■□□□□□□

# 오늘의 코드

webpack.config.js

```js
//node.js에서 동작합니다.
const path = require('path');
const HtmlPlugin = require('html-webpack-plugin');
const CopyPlugin = require('copy-webpack-plugin');

module.exports = {
  // 파일을 읽어들이기 시작하는 진입점 설정
  entry: './js/main.js',

  // 결과물(번들)을 반환하는 설정
  output: {
    // path: path.resolve(__dirname, 'dist'),
    // filename: 'main.js',
    // 이상 기본 설정
    clean: true,
  },

  module: {
    rules: [
      {
        test: /\.s?css$/,
        use: ['style-loader', 'css-loader', 'postcss-loader', 'sass-loader'],
      },
      {
        test: /\.js$/,
        use: ['babel-loader'],
      },
    ],
  },

  // 번들링 후 결과물의 처리 방식 등 다양한 플러그인들을 설정
  plugins: [
    new HtmlPlugin({
      template: './index.html',
    }),
    new CopyPlugin({
      patterns: [{ from: 'static' }],
    }),
  ],
};
```

package.json

```
"scripts": {
    "dev": "webpack-dev-server --mode development",
    "build": "webpack --mode production"
  },
```

`$ npm run dev`  
`$ npm run build`

# 내일 할 일

- JavaScript 복습!!!!!!!!!!
- JavaScript 라이브 강의 출석

