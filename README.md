# 📝 ReactProject Mini-Blog

![React](https://img.shields.io/badge/Framework-React-blue?logo=react)
![Language](https://img.shields.io/badge/Language-JavaScript-yellow?logo=javascript)
![UI](https://img.shields.io/badge/UI-Custom%20Component-lightgrey)
![Date](https://img.shields.io/badge/Last%20Update-2025.06.19-brightgreen)

---

## 📌 프로젝트 개요

> 사용자 중심 기능을 확장한 **React 기반 미니 블로그 웹앱**

이 프로젝트는 기존 블로그 프로젝트를 기반으로 **검색, 카테고리 필터, 다크모드, 댓글 기능 등 실사용 기능을 강화**한 개선형 React 실습 프로젝트입니다. 컴포넌트 분리와 상태 관리, 테마 기능 등 실제 서비스 구현에 가까운 구조로 설계되었습니다.

- 📍 **제작자**: 권법진 (동의과학대학교 컴퓨터소프트웨어과)
- 📧 **이메일**: gwonbubjin@gmail.com

---

## 🧩 주요 기능

| 기능 | 설명 |
|------|------|
| 🔍 게시글 검색 | 제목/본문/작성자 기준 실시간 검색 필터링 |
| 📂 카테고리 필터 | 선택된 카테고리에 해당하는 글만 필터링 |
| 🌗 다크모드 지원 | 테마 토글 버튼으로 다크/라이트 전환 |
| 📝 게시글 CRUD | 글 작성, 목록 보기, 상세 보기, 댓글 작성 |
| 🔝 UX 기능 추가 | 뒤로가기 버튼, 스크롤 상단 이동 버튼 등 |

---

## 🔧 변경 및 확장 사항

### ✅ 변경된 부분
- **라우팅 구조 개선**: `App.js`에서 전체 앱 라우팅 구조 정비
- **UI 개편**: `MainPage.jsx`에 주요 기능 UI 배치 (검색창, 필터, 토글 등)
- **데이터 구조 보강**: `data.json`에 작성자, 썸네일, 좋아요 등 필드 추가

### ➕ 추가된 컴포넌트
- `SearchInput.jsx`: 실시간 검색 필터링 기능
- `CategoryFilter.jsx`: 카테고리 기반 필터링 버튼
- `ThemeToggle.jsx`: 다크모드 전환 버튼
- `ScrollTopButton.jsx`: 상단 이동 버튼
- `BackButton.jsx`: 뒤로가기 버튼

---

## 🖼️ 실행 화면

| 메인화면 (Light/Dark) | 글 작성 화면 | 상세 보기 |
|---------------------|-------------|----------|
| 검색/필터/테마 토글 | 제목/내용/이미지 등록 | 댓글 포함 상세 조회 |

---

## 📁 폴더 구조


```bash
src/
├── components/
│   ├── common/            # SearchInput, ThemeToggle 등 공통 기능
│   ├── list/              # PostList, CommentList 등 목록 출력
│   ├── page/              # MainPage, PostViewPage, PostWritePage
│   ├── plus/              # ScrollTopButton, BackButton 등 UX 향상
│   └── ui/                # UI 관련 스타일 또는 보조 요소
├── data/
│   └── data.json          # 게시글 및 댓글 데이터 구조
└── App.js                 # 전체 앱의 라우팅 및 테마 관리

🧠 핵심 코드 설명
App.js
테마 전환 로직 (다크/라이트 모드)

React Router를 이용한 /, /write, /post/:id 페이지 이동 구현

MainPage.jsx
게시글 리스트 필터링 (카테고리, 검색어)

useMemo, useEffect 활용한 최적화 및 렌더링 제어

PostWritePage.jsx
useState 기반 입력폼 구성

카테고리, 제목, 이미지 URL, 본문 입력 후 등록

PostViewPage.jsx
URL 파라미터(postId) 기반 글 상세 보기

댓글 작성 및 목록 출력 (댓글은 comments[] 배열 기반)

data.json
{
  "id": 1,
  "title": "제목",
  "content": "본문",
  "imageUrl": "https://...",
  "author": "작성자",
  "category": "카테고리",
  "likes": 0,
  "comments": [
    {
      "id": 1,
      "author": "댓글작성자",
      "content": "댓글 내용"
    }
  ]
}

🚀 실행 방법

# 1. 프로젝트 클론
git clone https://github.com/your-id/react-mini-blog.git
cd react-mini-blog

# 2. 패키지 설치
npm install

# 3. 개발 서버 실행
npm start

💬 마무리 소감
기존 프로젝트의 구조를 분석하고, 기능별로 분리/확장하는 과정을 통해 실전 감각을 높일 수 있었던 프로젝트입니다.

테마 관리, 검색 필터, 데이터 구조 확장 등 실제 웹앱 서비스 구현에 필요한 핵심 요소들을 직접 적용하며 개발자로 한걸음 성장할 수 있는 계기가 되었습니다.

🎉 만든 사람: 권법진 (202229016) / 📧 gwonbubjin@gmail.com
