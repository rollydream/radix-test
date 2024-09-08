# radix-test기본설치
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
