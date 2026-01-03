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

## 📁 Project Structure

```text
project/
├── app/
│   ├── main.py
│   ├── models/
│   ├── schemas/
│   ├── services/
│   ├── routes/
│   └── auth/
├── db/
│   └── dev.db            # auto-created
├── Dockerfile.dev
├── docker-compose.yml
├── requirements.txt
├── .gitignore
└── .gitlab-ci.yml

## 🚀 Getting Started (Development)
Prerequisites :

Docker

Docker Compose

** Clone the Repository
git clone <repository-url>
cd <project-directory>

Build & Run the Application
docker compose up --build


The API will be available at:

http://localhost:8000/docs

Stop the Application
docker compose down

## 🔑 Authentication & Authorization

- Authentication via JWT

- Authorization enforced using RBAC

- All protected endpoints validate:

- Token validity

- User role

- Resource ownership

**Example request header:**

Authorization: Bearer <access_token>
