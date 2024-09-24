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
# msw 설치 : api 요청을 모킹
```c
yarn add msw --dev
```
서비스 워커 생성 : Browser 환경에서 API 요청을 가로채기 위해 반드시 필요한 파일
```c
npx msw init public/ --save
```
# react-query 설치 : 데이터 패칭 관리
```c
yarn add @tanstack/react-query @tanstack/react-query-devtools
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
# vite-bundle-visualizer 설치 (vite bundle 용량 분석) 
```c
yarn add --dev vite-bundle-visualizer
```

--output : 파일 저장 경로 설정
```c
yarn vite-bundle-visualizer --sourcemap --output output/my-stats.html
```

# 기타
## 404 에러
react-router-dom Refresh 시 404 에러 발생

클라이언트 측의 라우팅을 처리하는 경우, 서버는 해당 경로에 대한 파일을 찾을 수 없다 


## 해결 방법
nginx의 nginx.conf 파일 try_files 설정 (개발 요청)

React Router의 basename 설정(BrowserRouter의 basename을 nginx의 서브 디렉토리를 같게 설정)

정적 리소스(파일)을 가져오는 경로 올바르게 맞춰주기 

## VSCode 확장 프로그램 
Tailwind CSS IntelliSense : 자동 완성

## 크롬 확장 프로그램
lighthouse : 성능 측정
