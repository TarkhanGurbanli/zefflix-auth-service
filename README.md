# zefflix-auth-service
Authentication and Authorization microservice for Zefflix — handles user registration, login, JWT token management, and secure session handling.

# Zefflix Auth Service

🔐 Authentication and Authorization microservice for **Zefflix**, a distributed media discovery platform.  
This service is responsible for:

- User registration and login
- Secure password encryption (BCrypt)
- JWT access & refresh token management
- Redis-based session storage
- Stateless authentication flow
- Event publishing upon successful registration (`UserRegisteredEvent`)

---

## 🧱 Tech Stack

- Java 17
- Spring Boot
- Spring Security
- JWT (Access + Refresh)
- Redis
- RabbitMQ / Kafka(for event-driven architecture)
- Docker

---

## 📦 API Endpoints

| Method | Endpoint         | Description            |
|--------|------------------|------------------------|
| POST   | `/auth/register` | Register new user      |
| POST   | `/auth/login`    | Authenticate user      |
| POST   | `/auth/refresh`  | Refresh access token   |
| POST   | `/auth/logout`   | Revoke refresh token   |
| POST   | `/auth/logoutAll`   | Revoke refresh token   |

---

## 📡 Events

| Event Name           | Triggered When           |
|----------------------|--------------------------|
| `UserRegisteredEvent`| Upon successful register |

---

## 📁 Folder Structure

```bash
zefflix-auth-service/
├── controller/
├── model/
|  |──────/dto
|         |──────/request
|         |──────/response
├── config/
├── security/
├── repository/
├── service/
└── util/
