# AI 업무 자동화 정규강의 — 2회차 덱

`regular_lecture_deck_web_week_1`과 동일한 발표 UX·디자인 언어를 사용하는 2회차 강의 덱입니다.

현재 구성: 오프닝 1장 → 1회차 Recap 13장(디바이더 포함 · 파트별 요약 + 이메일 자동화 케이스 5장 + 실습 환경(ChatGPT 앱·모드 구분) 2장) → 지난 시간 질문 답변 6장(디바이더 포함 · 실제 수강생 질문 3건 기반) → 사전 설문 정리 3장(설문 응답 8건 · 공통 구조 4단계 · AI Agent 적합성) → 2회차 컨셉(실습 위주 케이스 중심) 1장 → Claude Cowork 전환 준비 6장(ChatGPT Work ↔ Claude Cowork 기능/용어 비교 2장 · Notion·Slack·Google Drive 설치 안내 3장 · 전환 선언 1장) → 실습 케이스 1 · 이메일 자동화(Cowork 복붙 원문 2 · 스킬·예약 작업 만들기 1) 3장 → 실습 케이스 2 · 회의록→업무보고(개요 1 · Step 1~4 4장 · 입력 2갈래·재사용 등록·실행 위치 3장 · 복붙 원문 1 · 스킬 만들기 1 · 예약 작업 만들기 1 · 확장 가능성 1) 12장 → Claude Code 전환(디바이더 1 · 개념 1 · 루프 예시 1 · 사전 지식 7장(터미널·Git·Git과 GitHub·CLAUDE.md 개념·CLAUDE.md 예시·대화 관리와 권한 모드·확장 구조) · 설치 1 · 비교 1 · 배울 이유 1 · 참고 링크 1) 14장 → 목표 프로젝트 도구 분류(판별 기준 1 · 설문 분류표 1) 2장 → Claude Code 실습 · 회의록→업무보고 재현(개요 1 · 준비 1 · 흐름 1 · MCP 연결 1 · 복붙 원문 1 · 서브에이전트 1 · 스킬 1 · 예약 작업(Routine) 1) 8장 → Q&A 1장 — 총 70장.

## 구조

```text
regular_lecture_deck_web_week_2/
├─ index.html
├─ src/
│  ├─ main.jsx
│  ├─ App.jsx
│  └─ index.css
├─ public/
│  ├─ deck.html
│  ├─ instructor.png
│  └─ assets/
├─ vite.config.js
└─ package.json
```

React 앱은 `public/deck.html`을 전체화면 iframe으로 로드합니다. 슬라이드 디자인, 키보드 이동, 진행률, 발표자 노트, 전체화면 전환은 `deck.html` 내부에서 동작합니다.

## 로컬 실행

```bash
npm install
npm run dev
npm run build
```

## 편집 방식

- 강의 자료는 `public/deck.html`의 `<section class="slide">` 단위로 추가합니다.
- 무료 강의 덱에서 가져온 핵심 UI 블록: `kicker`, `numlist`, `steps`, `sheet`, `versus`, `toolgrid`, `media`, `vslot`, `timer`, `note`.
- 발표자 노트는 각 슬라이드 끝의 `<aside class="note">`에 작성합니다.
- 데모 영상은 `public/assets/videos/`, 캡처 이미지는 `public/assets/images/`에 넣고 슬라이드에서 상대 경로로 참조합니다.
