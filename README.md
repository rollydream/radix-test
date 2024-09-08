# 기본설치
```c
npm install yarn
yarn install
yarn create vite
yarn add react-router-dom
yarn add -D tailwindcss postcss autoprefixer
yarn tailwind init -p
yarn add axios
```
# msw 설치
```c
yarn add msw --dev
```
서비스 워커 생성 : Browser 환경에서 API 요청을 가로채기 위해 반드시 필요한 파일
```c
npx msw init public/ --save
```

# Radix 설치
```c
yarn add @radix-ui/react
```
# storybook 설치
```c
npx storybook@latest init
yarn add --dev @storybook/builder-vite
```
# storybook addon-a11y 설치(접근성)
```c
yarn add --dev @storybook/addon-a11y
```
main.js 수정 필요
```c
 addons: [
	"@storybook/addon-a11y", // 추가 필요
 ]
```

# 기타
## 404 에러
react-router-dom Refresh 시 404 에러 발생

클라이언트 측의 라우팅을 처리하는 경우, 서버는 해당 경로에 대한 파일을 찾을 수 없다 


## 해결 방법
nginx의 nginx.conf 파일 try_files 설정 (개발 요청)

React Router의 basename 설정(BrowserRouter의 basename을 nginx의 서브 디렉토리를 같게 설정)

정적 리소스(파일)을 가져오는 경로 올바르게 맞춰주기 


