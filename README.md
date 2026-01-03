# 🏦 Banking API

A **FastAPI-based internal banking API** that simulates essential financial operations such as customer onboarding, account management, balance checks, and money transfers.

This project is implemented as a **production-oriented prototype**, following clean architecture principles, Python best practices, **enforced Role-Based Access Control (RBAC)**, and a clearly documented path to production.

---

## 📌 Key Highlights

- JWT-based authentication
- **Role-Based Access Control (RBAC) enforced**
- Atomic money transfers
- Clean, maintainable architecture
- Dockerized setup (runs out of the box)
- Docker Compose orchestration
- GitLab CI/CD integration
- Clear production-readiness roadmap

---

## ✨ Features

- Customer registration & login
- JWT authentication
- Role-based authorization:
  - **Admin** – full access
  - **Employee** – manage accounts & transfers
  - **Customer** – access own accounts only
- Account creation with initial deposits
- Balance retrieval
- Secure money transfers
- Transfer history per account
- Automatic database initialization
- Default admin & customer seeding
- Interactive Swagger (OpenAPI) documentation

---

## 🛠 Tech Stack

| Layer | Technology |
|------|------------|
| Language | Python 3.9 |
| API Framework | FastAPI |
| ASGI Server | Uvicorn |
| ORM | SQLAlchemy |
| Database | SQLite (development only) |
| Authentication | JWT |
| Authorization | RBAC |
| Containers | Docker |
| Orchestration | Docker Compose |
| CI/CD | GitLab CI/CD |
| Testing | Pytest |

---

## 🚀 Getting Started (Development)

Prerequisites

- Docker

- Docker Compose

1. Clone the Repository
git clone <repository-url>
cd <project-directory>

2. Build & Run the Application
docker compose up --build

3. API Access

The API will be available at:

http://localhost:8000/docs

4. Stop the Application
docker compose down

## 🔑 Authentication & Authorization

- Authentication via JWT

- Authorization enforced using RBAC

- All protected endpoints validate:

- Token validity

- User role

- Resource ownership

Example request header
Authorization: Bearer <access_token>

## 🧩 System Design (High Level)

The application follows a layered architecture for clarity and maintainability:

Client
  ↓
API Routes (FastAPI)
  ↓
Service Layer (Business Logic)
  ↓
Data Access Layer (SQLAlchemy ORM)
  ↓
Database (SQLite)


Business rules are handled in the service layer, while routes remain thin and focused on request/response handling.

## 🧪 Running Tests
pytest -q


Tests cover authentication, RBAC enforcement, account operations, and transfer edge cases.

## 📚 API Documentation

Interactive API documentation is available via Swagger UI:

http://localhost:8000/docs

