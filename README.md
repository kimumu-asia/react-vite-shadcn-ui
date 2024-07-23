# 1. Structure

### Vite

- [ESBuild](https://esbuild.github.io/)를 베이스로 한 빌드 툴

### React

- [단일 페이지 애플리케이션 (SPA)](https://poiemaweb.com/js-spa) 방식

### UI framework

- [shadcn/ui](https://github.com/shadcn-ui/ui)

- [icon: Lucide](https://lucide.dev/icons/)

### Linter

- [eslint](https://www.google.com/search?q=eslint&oq=eslint&gs_lcrp=EgZjaHJvbWUyBggAEEUYOTIMCAEQIxgnGIAEGIoFMgwIAhAjGCcYgAQYigUyCQgDEAAYBBiABDIHCAQQABiABDIHCAUQABiABDIGCAYQRRg8MgYIBxBFGD3SAQgxMzYzajBqNKgCALACAA&sourceid=chrome&ie=UTF-8), [prettier](https://prettier.io/)


# 2. Installation

1. 패키지 인스톨

```
$ yarn install
or
$ npm run install
```

2. server 실행

```
$ yarn dev
or
$ npm run dev
```

3. `http://localhost:portNumber/` 으로 액세스 (default 5173)

# 3. Style Guide

1. 새로운 컴포넌트 요소 추가 시 [shadcn/UI](https://ui.shadcn.com/) 를 활용

   - 패키지를 설치해서 import해서 사용하는 방식이 아닌, 직접 아래의 커맨드로 필요한 요소를 설치하면 리포지토리 소스 코드 내에 생성되는 방식을 채용하고 있음
   - src/components/ui

   ```
   npx shadcn-ui@latest add
   or
   npx shadcn-ui@latest add button
   ```

2. 클래스 작성 시 [TailwindCSS](https://tailwindcss.com/docs/installation) 를 활용
   1. 기본적으로 CSS를 적용할 때는 tailwindcss에서 제공하는 유틸리티(클래스)를 **우선적으로** 적용한다.
   2. 만약 tailwindcss로 커버하기 어려운 예외적인 경우에 커스텀 스타일을 작성한다.
   3. 필요한 커스텀이 있다면 tailwind.config.js에서 설정 추가/변경
   4. 사용 예
      1. 너비 5rem의 플렉스 타입의 노란색 배경을 가진 요소 작성 시 아래 코드 처럼 적용
      2. `<section className='w-20 flex bg-yellow' />`
