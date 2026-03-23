# 디스코드 온보딩 가이드 — Sandbox Network

디스코드를 처음 사용하는 PM과 크리에이터를 위한 단계별 온보딩 가이드 웹페이지입니다.

## 개요

Sandbox Network 파트너십팀에서 디스코드 기반 캠페인을 운영할 때 필요한 SOP(표준 운영 절차)를 인터랙티브 웹 가이드로 제공합니다.

### 가이드 구성

**공통 단계** (PM / 크리에이터 모두)
- 디스코드 앱 설치하기
- 회원가입하기
- 프로필 설정하기
- 서버에 입장하기

**PM 운영 가이드**
- 서버 개설 신청하기
- 크리에이터에게 초대 링크 전달하기
- 크리에이터 입장 확인 및 역할 부여하기
- 캠페인 채널 만들기
- 캠페인 채널 첫 메시지 작성하기
- 캠페인 상태에 따라 채널 이동하기

## 기술 스택

- HTML / CSS / JavaScript (단일 파일, 프레임워크 없음)
- [Pretendard](https://github.com/orioncactus/pretendard) 웹폰트
- GitHub Pages 자동 배포

## 배포

`main` 브랜치에 push하면 GitHub Actions를 통해 GitHub Pages로 자동 배포됩니다.

## 프로젝트 구조

```
├── index.html          # 메인 페이지 (SPA)
├── images/             # 스크린샷 이미지
├── videos/             # 단계별 안내 영상
└── .github/workflows/  # GitHub Pages 배포 워크플로우
```
