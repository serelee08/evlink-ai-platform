# 시스템 아키텍처 개요


![EVLink 시스템 아키텍처](./images/architecture.jpg)

위의 다이어그램은 EVLink 프로젝트의 전체 시스템 구성과
각 컴포넌트 간 책임 분리를 나타냅니다.

프론트엔드, 백엔드, AI 서버를 역할 기준으로 분리하고,
인증·데이터·AI 연산 흐름이 어떻게 연결되는지를 시각적으로 표현했습니다.


## 전체 아키텍처 구조

[ Client ]
    ↓
[ Frontend (React) ]
  - UI Rendering
  - API Request
    ↓
[ Spring Boot Backend ]
  - Authentication (OAuth2 + JWT)
  - Business Logic
  - Data Access
    ↓  (REST API)
[ Django AI Server ]
  - Gemini API Integration
  - Sentiment Analysis (RNN / LSTM)
    ↓
[ Gemini API / NLP Model ]

- 프론트엔드는 사용자 인터페이스 렌더링과 API 요청을 담당합니다.
- 백엔드는 인증, 비즈니스 로직 처리 및 데이터 접근을 담당합니다.
- AI 서버는 챗봇 응답 생성 및 감성 분석과 같은 AI 연산을 전담합니다.

## 서버 분리 설계 이유

AI 연산은 응답 시간이 길고 리소스 사용량이 크기 때문에
백엔드 서버와 분리하여 다음과 같은 이점을 얻고자 했습니다.

- 백엔드 API 안정성 확보
- AI 모델 교체 및 확장 용이성
- 장애 발생 시 영향 범위 최소화

## 데이터베이스 모델링 전략

EVLink 프로젝트에서는 MySQL(RDS) 을 단일 데이터베이스로 사용했습니다.

## 아키텍처 설계 핵심

- React 프론트엔드는 모든 요청을 Spring Boot 백엔드로 전달합니다.
- 백엔드는 OAuth2 + JWT 기반 인증 및 핵심 비즈니스 로직을 담당합니다.
- Django AI 서버는 Gemini API 및 감성 분석 모델을 전담 처리합니다.
- AI 서버는 독립 서비스로 구성하여 모델 교체 및 확장을 용이하게 했습니다.
- MySQL(RDS)을 단일 데이터베이스로 사용하여 데이터 일관성을 유지했습니다.

### 정규화 기준

- 중복 데이터 제거
- 변경 가능성이 높은 속성 분리
- 참조 무결성을 고려한 외래 키 설계

이를 통해 데이터 일관성과 유지보수성을 동시에 확보하고자 했습니다.
