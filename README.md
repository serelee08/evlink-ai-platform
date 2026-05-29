# ⚡ EVLink: AI 기반 전기차 충전 공유 플랫폼
> **Portfolio:** 🌐 [이지애의 AI 백엔드 엔지니어 포트폴리오 사이트](https://serelee08.github.io/PortfolioSL/)
> 
> **Spring Boot & Django 마이크로서비스 아키텍처 기반의 스마트 충전 솔루션**

---

## 🚀 Key Highlights
* **보안 인증 시스템**: **Passwordless (X1280)** 및 **Spring Security + JWT** 기반의 Stateless 인증 구조 설계
* **AI 모델 최적화**: **RNN/LSTM** 기반 감성 분석 및 **Gemini AI** 연동 대화형 추천 서비스 구현
* **데이터 엔지니어링**: 공공데이터 API 기반 **20만 건 대용량 데이터** 처리 및 MyBatis SQL 최적화
* **클라우드 인프라**: **AWS EC2** 리눅스 환경에서 AI 모델 및 백엔드 서비스 배포/연동

---

## 🛠 Tech Stack
- **Backend**: Java (Spring Boot, Security, JWT), Python (Django)
- **AI/ML**: LSTM, RNN, KoBERT, Gemini API
- **Frontend**: React (TypeScript), Tailwind CSS, Recharts
- **Infra**: AWS EC2, Oracle DB, Redis

---

## 📐 System Architecture
### 1. Authentication Flow (Passwordless)
* 패스워드 없는 로그인 방식을 도입하여 보안성과 사용자 경험(UX)을 동시 개선했습니다.
* 📐 [시스템 아키텍처 전체 구조 보기](./docs/architecture.md)

### 2. AI Sentiment Analysis
* 커뮤니티 게시글 텍스트를 분석하여 긍/부정 대시보드 형태로 시각화합니다.

---

## 📎 문서
* 📡 [API Endpoints](./docs/api-endpoints.md)
* 📋 [API Specification](./docs/api-specification.md)
* 📐 [System Architecture](./docs/architecture.md)

---

## 👤 담당 역할 (이지애)
* **인증 시스템**: Spring Security 기반 OAuth2 SNS 로그인 및 JWT 인증 흐름 구현
* **AI 연동**: Django 기반 Gemini API 챗봇 서비스 개발
* **감성 분석**: LSTM 모델 활용 사용자 리뷰 긍·부정 감성 분석 기능 구현
* **데이터 처리**: 공공데이터 API 기반 20만 건 충전소 데이터 처리 및 MyBatis 쿼리 최적화

---

## 🗄️ DB 설계
* Oracle 기반 충전소 / 예약 / 리뷰 / 회원 테이블 설계
* 서비스 요구사항 기반 스키마 설계 및 MyBatis 연동

---

## 🔧 트러블슈팅
* **문제**: Spring Boot 백엔드와 Django AI 서버 간 API 응답 키 이름이 달라 프론트엔드 연동 오류 반복 발생
* **원인**: 팀원 간 응답 형식 사전 합의 없이 개발 진행
* **해결**: Postman으로 API 명세 작성 후 팀 공유 및 응답 구조 통일
* **결과**: 연동 오류 감소 및 팀 전체 개발 속도 향상

---

## 🏆 Accomplishments
* **한국 ICT 인재개발원 프로젝트 우수상** 수상
* **클라우드 기반 AI 서비스 풀스택 개발 과정** 수료 (2025.03 - 2025.09)
* **IBM AI Engineering Professional Certificate (2025.12 - Present)**

---

## 👤 Author: 이지애 (AI Backend)
* **Email**: serelee08@gmail.com
* **Portfolio**: [https://serelee08.github.io/PortfolioSL/](https://serelee08.github.io/PortfolioSL/)
* **Detailed API Spec**: [API-Endpoints.md](https://github.com/serelee08/evlink-ai-platform/blob/main/api-endpoints.md)
