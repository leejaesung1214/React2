# 2026.09.09 - Next.js 2주차

## 프로젝트 생성

Next.js 프로젝트는 직접 필요한 파일과 패키지를 구성할 수도 있지만, 보통 `create-next-app`을 이용하면 편리하게 생성할 수 있다.

```bash
pnpm create next-app@latest
```

자동 생성 방식을 사용하면 TypeScript, ESLint, App Router, Tailwind CSS, import alias 등의 설정을 프로젝트 생성 과정에서 선택할 수 있다.

## 기본 실행 명령어

`package.json`에 등록된 스크립트를 이용해 프로젝트를 실행하거나 빌드할 수 있다.

```bash
pnpm dev      # 개발 서버 실행
pnpm build    # 배포용 빌드
pnpm start    # 빌드된 프로젝트 실행
```

개발 서버를 실행한 뒤 브라우저에서 `localhost:3000`으로 접속하면 결과를 확인할 수 있다.

## 프로젝트 구조

Next.js의 App Router는 폴더와 파일 구조를 기준으로 URL 경로를 구성한다.

* `app/page.tsx` : 기본 페이지
* `app/layout.tsx` : 공통 레이아웃
* `public/` : 이미지 등의 정적 파일
* `package.json` : 패키지와 실행 스크립트 관리
* `tsconfig.json` : TypeScript 설정
* `eslint.config.mjs` : ESLint 설정

## 동적 라우팅

폴더 이름에 대괄호를 사용하면 URL의 일부를 동적으로 처리할 수 있다.

```text
[slug]       → 하나의 경로 처리
[...slug]    → 여러 단계의 하위 경로 처리
[[...slug]]  → 기본 경로를 포함한 여러 하위 경로 처리
```

예를 들어 `app/posts/[slug]/page.tsx`가 있다면 `/posts/1`, `/posts/react`처럼 값이 달라지는 주소를 하나의 페이지에서 처리할 수 있다.

## 기타 정리

`dependencies`에는 실제 프로그램 실행에 필요한 패키지를, `devDependencies`에는 TypeScript나 ESLint처럼 개발 과정에서 필요한 패키지를 주로 등록한다.

또한 최신 프로젝트에서는 import 경로를 간단하게 작성하기 위해 `tsconfig.json`의 `paths`를 이용해 `@/*`와 같은 별칭을 설정할 수 있다.


---


# 3주차 Next.js

## Folder & File Conventions

- `(folder)` : URL에 영향 없이 파일 정리
- `_folder` : 라우팅에서 제외되는 비공개 폴더
- `page.js` : 실제 페이지로 접근하기 위해 필요

---

## Routing

- `@folder` : 여러 UI를 동시에 보여주는 슬롯
- **Intercepting Route** : 현재 화면에서 다른 경로를 모달처럼 표시

---

## 주요 파일

- `layout.js` : 공통 레이아웃
- `template.js` : 이동 시 새로 생성
- `loading.js` : 로딩 화면
- `error.js` : 에러 화면
- `not-found.js` : 404 화면

---

## Open Graph

SNS에 링크를 공유할 때  
제목, 이미지 등의 **미리보기**를 보여주는 프로토콜.

---

# 4주차 Next.js

- `Link` 컴포넌트의 `href`를 사용하여 페이지 이동
- 폴더 구조를 이용해 중첩된 라우트 구성 가능
- `[slug]`를 이용하여 게시글 같은 동적 라우팅 구현
- `params`를 통해 동적 URL의 값을 가져올 수 있음
- `searchParams`를 사용하여 검색, 필터 등의 URL 값 처리


-----------

# 5주차 Next.js

- React와 Next.js의 라우팅 방식 차이 학습
- `App Router`를 이용한 파일 기반 라우팅 구조 이해
- `Server Rendering`과 `Prefetching`을 통한 페이지 로딩 최적화
- `Streaming`으로 준비된 콘텐츠부터 빠르게 표시
- `<Link>`와 `loading.tsx`를 활용한 자연스러운 페이지 전환
