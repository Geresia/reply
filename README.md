# 미니 게시판 (Vanilla JS · 단일 HTML · 로컬 상태)

![Vanilla JS](https://img.shields.io/badge/Vanilla_JS-Yes-2F6DF6?style=flat)
![Single HTML](https://img.shields.io/badge/Single_File-index.html-22C55E?style=flat)
![No Build](https://img.shields.io/badge/Build-None-64748B?style=flat)
![In‑Memory](https://img.shields.io/badge/Storage-In_Memory-EF4444?style=flat)

> **부트/톰캣 없이** 브라우저만으로 동작하는 가벼운 게시판 데모입니다. 데이터는 메모리에만 저장되며 새로고침 시 초기화됩니다.

---

## 컬러 팔레트 (README 표시용)

![Accent](https://img.shields.io/badge/Accent-2F6DF6?style=flat\&labelColor=2F6DF6\&color=2F6DF6)
![Accent‑2](https://img.shields.io/badge/Accent%E2%80%912-22C55E?style=flat\&labelColor=22C55E\&color=22C55E)
![Danger](https://img.shields.io/badge/Danger-EF4444?style=flat\&labelColor=EF4444\&color=EF4444)
![Text](https://img.shields.io/badge/Text-1B1C1F?style=flat\&labelColor=1B1C1F\&color=1B1C1F)
![Border](https://img.shields.io/badge/Border-E5E7EB?style=flat\&labelColor=E5E7EB\&color=E5E7EB)

> README는 사용자 CSS가 불가하므로 색상은 **배지**로 표현합니다. 실제 페이지 색상은 `index.html`의 CSS 변수(`:root`)가 적용됩니다.

---

## 실행 방법

* 이 저장소를 클론/다운로드 후 **`index.html` 더블클릭** 또는 아무 정적 서버로 열기
* 추가 설치/빌드 과정 없음

```bash
# 선택: 간단 서버로 실행 (임의)
python -m http.server 5173
# 또는
npx serve .
```
---

## 주요 기능 (기능 중심 요약)

### 1) 게시글 목록

* 최신순 카드 목록
* **제목 / 작성자 / 작성일 / 댓글 수** 표기
* **“자세히 보기” → 상세 보기**

### 2) 글 작성

* 상단 **“작성하기”** 버튼으로 작성 모달 열기
* 필수: **제목, 내용** / 선택: 작성자
* 단축키: **Ctrl/Cmd + Enter** 등록, **Esc** 닫기
* 등록 시 즉시 목록 반영

### 3) 게시글 상세

* 제목/작성자/작성일/본문 표시
* 바깥 영역 클릭 또는 **Esc**로 닫기

### 4) 댓글 & 대댓글

* 댓글 작성(내용 필수, 작성자 선택)
* **대댓글** 지원: 각 댓글의 **“답글/닫기”** 토글
* 댓글 수는 **대댓글 포함 총 개수**로 표시
* 입력 후 모달 재오픈으로 최신 상태 표시

---

## 데이터/상태 (메모리 전용)

* 새로고침 시 **초기화**됨 (DB/로컬스토리지 없음)
---

## 단축키

* **Ctrl/Cmd + Enter**: 작성 모달에서 등록
* **Esc**: 작성/상세 모달 닫기

## 구조

```
.
├── index.html   # 단일 파일 (모든 기능 포함)
└── README.md    # 이 문서
```
