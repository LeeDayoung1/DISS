# DISS

**대학생을 위한 학습·커뮤니티 웹 서비스**

<div align="center">
  <img src="./introduce.gif" width="600"/>
</div>

## 프로젝트 배경 및 목적

기존 대학생 커뮤니티 플랫폼에서 발견한 문제를 해결하기 위해 시작한 프로젝트입니다.

- **무응답 및 정보 소멸**: 질문글에 무응답이 잦고, 답변을 받은 후 글을 삭제해 다른 사용자가 동일한 정보를 얻지 못하는 구조적 문제
- **유해 콘텐츠**: 비속어·욕설·비하 발언 등 공격적인 댓글에 대한 필터링 미흡
- **정보 품질 저하**: 홍보글 범람으로 인한 플랫폼 가치 하락

위 문제를 해결하고 질 높은 학습·커뮤니티 환경을 제공하는 것을 목표로 했습니다.

---

## 관련 문서
 
| 제목 | 링크 |
|------|------|
| Microsoft Azure를 활용한 통합 교육 웹 플랫폼 DISS 개발 | [📄 PDF](./DISS_paper.pdf) |
 
---

## 학습 목표

- Azure Cloud 서비스 실습 (Azure Translator, Speech SDK, OpenAI Studio, QnA Maker 등)
- 클라우드 환경에서의 백엔드 설계 및 DB 구축 경험
- 실제 서비스 배포 프로세스 이해

---

## 팀 구성 및 담당 역할

**개발 기간**: 2024.03 ~ 2024.07 (5개월) | **팀원**: 4명

| GitHub | 역할 |
|--------|------|
| LeeDayoung1 (본인) | 기획, 디자인, 백엔드, 프론트엔드 |
| [@gaeun-jay](https://github.com/gaeun-jay) | 기획, 디자인, 백엔드, 프론트엔드 |
| [@yeonnnnni](https://github.com/yeonnnnni) | 기획, 백엔드, 프론트엔드 |
| [@chaewon0401](https://github.com/chaewon0401) | 기획, 백엔드, 프론트엔드 |

### 제가 담당한 주요 작업은 다음과 같습니다

| 구분  |  내용 |
|-------|-------|
| **Frontend** |  메인 광고 배너 구현<br> Q&A Public 화면 구현 (질문 등록, 답변 등록, 좋아요 기능)<br> My Page 화면 구현 (개인정보 수정, 시간표, 언어 변경, 로그아웃)<br> 동영상 강의 화면 구현 (정렬 기능, 음성 서비스, 동영상 삽입)<br> 자료실 화면 구현 (정렬 기능)<br> 수비니아 화면 구현 (정렬 기능) |
| **Backend** |  Azure AI Translator 연동 (다국어 번역 기능)<br> Azure AI 음성 연동 (음성 지원) |
| **Design** |  Figma를 활용한 UI/UX 디자인 |
 
---

## 주요 기능

### 메인 · 회원

- 메인 홈: 배너 슬라이드, 키워드 검색
- 로그인 / 회원가입: PHP API와 JSON 연동

### 질의응답(QnA)

- **1:1 질의응답**: 멘토 카드 목록, ID·별명 검색
- **공개 질문**: 게시형 질문 목록, 좋아요, 상세·작성 화면

### 동영상 강의

- 카테고리(전체, 전공별, 자격증, 기타), 정렬, 검색
- Microsoft Translator 기반 다국어 전환

### 자료실

- DB에서 자료 메타데이터 조회
- 카테고리 필터, 조회순·날짜순·평점순 정렬

### 대학원

- 분야·지역 선택 UI 및 대학원 정보 조회

### 수비니아(마켓)

- 카테고리·검색·목록 UI

### 프로필

- 채팅방, 파일 관리, 시간표, 개인정보 수정

---

## 기술 스택

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)
![Azure](https://img.shields.io/badge/Microsoft_Azure-0089D6?style=for-the-badge&logo=microsoft-azure&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)
![Notion](https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white)

| 구분         | 사용 기술                          |
| ------------ | ---------------------------------- |
| 프론트엔드   | HTML5, CSS3, JavaScript (Vanilla)  |
| 백엔드       | PHP 7.x (sqlsrv 확장)              |
| 데이터베이스 | Microsoft SQL Server               |
| 클라우드     | Azure Translator, Azure Speech SDK |
| 협업 도구    | Notion, Figma                      |

---

## 미구현 기능

아래 Azure 모듈을 학습하고 개발하였으나, 보안 정책 및 기타 오류 등의 문제로 배포 단계까지 구현하지 못했습니다.

- **Azure OpenAI Studio / GPT**: AI 기반 답변 서비스
- **Azure Cognitive Services (QnA Maker)**: 자주 묻는 질문 자동 응답
- **Azure Notification Hubs**: 알림 서비스
- **Azure Blob Storage**: 파일 저장 및 관리
- **Azure Machine Learning**: 콘텐츠 추천 서비스

---

## 프로젝트 구조

```
DISS-main/
├── Home.html                      # 메인
├── Login.html / register.html
├── login.php / register.php       # 회원 JSON API
├── search.php                     # 검색
├── file.php                       # 자료실 데이터
├── QnA_private_home.html          # 1:1 QnA
├── QnA-public_main.html           # 공개 QnA
├── video.html / video_detail.html # 동영상 강의
├── profile.html / profile-*.html  # 프로필
├── speech.js                      # Azure TTS
├── translator.js                  # Azure 번역
└── styles.css / st_*.css          # 스타일시트
```

---

## 설치 및 실행

### 사전 요구사항

- PHP 7.x 이상 (`sqlsrv` 확장)
- Microsoft SQL Server
- Apache 또는 Nginx (또는 PHP 내장 서버)

### 실행 방법

```bash
git clone <repository-url>
cd DISS-main
php -S localhost:8080
```

브라우저에서 `http://localhost:8080/Home.html` 접속

> DB 및 Azure API 설정이 맞지 않으면 로그인·검색·자료실 등 일부 기능이 동작하지 않을 수 있습니다.

### 환경 설정

1. `login.php`, `register.php`, `search.php` 등에서 DB 서버명·계정 수정
2. `Home.html` 등의 `fetch` URL을 배포된 PHP 엔드포인트로 변경
3. `translator.js`, `speech.js`에 Azure 구독 키·리전 입력
