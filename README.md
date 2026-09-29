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
