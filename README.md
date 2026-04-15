# 🛒 Microservices-based E-commerce Backend

A production-style e-commerce backend built with **Java, Spring Boot, and Spring Cloud**, following distributed system architecture principles. Features event-driven communication, centralized authentication, full observability, and containerized deployment.

---

<img width="1328" height="672" alt="architecture-design" src="https://github.com/user-attachments/assets/57ef9104-6d83-4134-8c19-09e754db1476" />
---

## 🔧 Services

| Service | Description | Database |
|---|---|---|
| **API Gateway** | Centralized routing via Spring Cloud Gateway MVC | — |
| **Product Service** | Manages product catalog and listings | MongoDB |
| **Order Service** | Handles order creation and processing | MySQL |
| **Inventory Service** | Tracks product stock and availability | MySQL |
| **Notification Service** | Sends async notifications triggered via Kafka | — |
| **Shop Frontend** | User-facing UI built with Angular 18 | — |

---

## 💻 Tech Stack

### Backend
- **Java** — Core language
- **Spring Boot** — Microservice framework
- **Spring Cloud Gateway MVC** — API Gateway and routing
- **Apache Kafka** — Asynchronous event-driven communication
- **Keycloak** — JWT-based authentication and Role-Based Access Control (RBAC)

### Frontend
- **Angular 18**

### Databases
- **MongoDB** — Product Service
- **MySQL** — Order and Inventory Services

### Testing
- **Testcontainers** — Integration testing with real containerized dependencies
- **WireMock** — HTTP service mocking for isolated testing

### Observability & Monitoring
- **Prometheus** — Metrics collection
- **Grafana** — Metrics visualization and dashboards
- **Loki** — Log aggregation
- **Tempo** — Distributed tracing

### DevOps
- **Docker + Docker Compose** — Containerization and local orchestration

---

## ✨ Key Features

- **Event-driven architecture** — Services communicate asynchronously via Apache Kafka, ensuring loose coupling and fault tolerance
- **Centralized authentication** — Keycloak handles JWT issuance and RBAC enforcement across all microservices
- **Full observability stack** — End-to-end visibility with metrics (Prometheus + Grafana), logs (Loki), and distributed traces (Tempo)
- **Production-grade testing** — Integration tests with Testcontainers spin up real dependencies; WireMock handles external service mocking
- **Containerized deployment** — All services orchestrated locally via Docker Compose

---

## 🚀 How to Run

### Prerequisites
- Java 21+
- Docker + Docker Compose

### Steps

**1. Clone the repository**
```bash
git clone https://github.com/ganeshakkimardi/spring-boot-microservice.git
cd spring-boot-microservice
```

**2. Start all services**
```bash
docker-compose up -d
```

**3. Access the application**

| Service | URL |
|---|---|
| Shop Frontend | http://localhost:4200 |
| API Gateway | http://localhost:8080 |
| Keycloak (Auth) | http://localhost:8181 |
| Grafana Dashboard | http://localhost:3000 |
| Prometheus | http://localhost:9090 |

---
