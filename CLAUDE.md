# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 프로젝트 개요

Sandbox Network 파트너십팀의 **디스코드 온보딩 SOP(표준 운영 절차) 가이드** 웹페이지. PM과 크리에이터가 디스코드를 처음 사용할 때 필요한 단계별 안내를 제공한다.

## 기술 스택 및 구조

- **빌드 도구 없음** — 프레임워크, 번들러, 패키지 매니저 없이 순수 HTML/CSS/JS 단일 파일(`index.html`)로 구성
- 로컬 개발: `index.html`을 브라우저에서 직접 열거나 `python3 -m http.server` 등 간이 서버 사용
- 배포: `main` 브랜치 push 시 GitHub Actions → GitHub Pages 자동 배포

## 아키텍처 (index.html 단일 SPA)

`index.html` 하나에 스타일, 마크업, 스크립트가 모두 포함된 SPA 구조:

- **상단 탭 바**: PM 모드 / 크리에이터 모드 / 채널 가이드 3개 탭 (`switchMode()`, `switchToChannelGuide()`)
- **사이드바 + 메인 영역**: 단계(step) 네비게이션. `STEPS` 객체에 모드별 단계 정의, `goToPage()`로 `data-page` 속성 기반 페이지 전환
- **채널 가이드 탭**: 디스코드 서버 구조를 모방한 인터랙티브 목업. `DM_MARKERS` 배열 기반 마커/툴팁 시스템으로 UI 영역과 채널 설명 제공
- **모드별 조건부 표시**: `data-pm-only` / `data-creator-only` 속성으로 모드에 따라 콘텐츠 표시/숨김

### CSS 변수 (디자인 토큰)

`:root`에 정의된 컬러 시스템 — `--red (#E9004B)`, `--yellow (#FFD03E)`, `--cyan (#00C1DE)` 가 브랜드 컬러. 변경 시 여기만 수정.

## 주의사항

- `index.html`이 이미 2500줄 이상. 콘텐츠 추가 시 파일 크기에 유의
- `images/`, `videos/` 디렉토리의 미디어 파일은 각 단계 페이지에서 참조됨
- `noindex, nofollow` 메타 태그 설정됨 — 내부 전용 가이드
- Obsidian 프로젝트 노트: `~/Documents/ObsidianVault/프로젝트/discord-sop.md`
