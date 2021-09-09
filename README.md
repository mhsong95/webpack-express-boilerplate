# Webpack + Express Boilerplate
Webpack 프론트엔드, Express 백엔드를 사용하여 개발할 때 Express 서버를 devServer로 사용할 수 있도록 해주는 Boilerplate 코드입니다. Babel, Sass 트랜스파일링을 포함합니다. 

# 디렉토리 구조
## Express
- `public/` Express의 static 미들웨어가 사용하며, `index.html` 파일을 포함합니다. 
- `bin/`
- `routes/`
- `app.js`

## Webpack
- `public/assets/` Webpack 번들링 결과를 출력합니다. 
- `configs/` Webpack configuration을 정의합니다. 
- `src/` 프론트엔드 소스를 포함합니다. 

# 스크립트
- `npm run build`  
Webpack 빌드를 실행하여 `public/assets/` 디렉토리에 결과를 출력합니다. 

- `npm start` / `npm run server`  
미리 빌드된 결과를 가지고 Express 서버를 NODE_ENV=production 환경변수와 함께 실행합니다. 

- `npm run devServer`  
NODE_ENV 환경변수를 설정하지 않고 Express 서버를 실행합니다. 이 경우 Express 서버는 `webpack-dev-middleware`를 사용하여 프론트엔드 개발서버devServer로도 동작합니다. `src/` 아래 파일에 변화가 있을 때마다 webpack 빌드가 메모리에 hot-reloading되고, 서버에 접속하면 메모리에 있는 빌드를 가지고 응답합니다. 

- `npm run devServer-mon` / `npm run server-mon`  
Express 서버를 nodemon으로 실행합니다. 서버 로직에 변화가 있을때마다 서버를 재시작합니다. 
