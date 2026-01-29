# EVLink API Endpoints

EVLink의 REST API 설계 문서입니다. 실제 구현된 기능을 중심으로 프론트엔드와 백엔드 간의 데이터 규격을 정의합니다.

---

## 🌐 1. Base URL
- **Local:** `http://localhost:8080/api`
- **Prod:** `http://<server-ip>:8080/api`

## 🔐 2. Authentication
- **Mechanism:** JWT 기반 Bearer 인증
- **Header:** `Authorization: Bearer {access_token}`
- **Notice:** 인증이 필요한 API는 헤더에 유효한 JWT 토큰을 포함해야 합니다.

---

## 🚀 3. Core Endpoints

### 3.1 Auth (인증)
| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/auth/login/passwordless` | 패스워드리스 인증 및 JWT 발급 |
| `GET` | `/auth/session` | 현재 로그인된 사용자 정보 확인 |

### 3.2 AI Service (챗봇)
| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/ai/chat` | Gemini 기반 주변 충전소 정보 추천 서비스 |

**[POST] /ai/chat 상세**
- **Request Body:**
```json
{
  "message": "파주 근처 맛집 추천해줘"
}
```  <-- 이 닫는 기호(```)를 추가하세요!

- **Success Response (200 OK):**
```json
{
  "success": true,
  "data": {
    "answer": "해당 충전소 근처 500m 이내에 'XX 식당'이 있습니다."
  },
  "message": "OK"
}
```



