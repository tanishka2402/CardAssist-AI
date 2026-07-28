# ⚡ CardAssist-AI — Backend Development Branch (`backend`)

> **Domain Branch for FastAPI Core Engine, REST Endpoints, Database Models, and Middleware.**

---

## 📌 Branch Focus: Backend Subsystem

This branch (`backend`) is dedicated to building and maintaining the core backend API service of CardAssist-AI. Developers working on this branch focus on API routes, authentication logic, database schema integrations, Pydantic schemas, and middleware services.

---

## 📂 Backend Subsystem Map (`backend/`)

```
backend/
├── main.py       # FastAPI application entrypoint & server setup
├── api/          # API versioning & router aggregators
├── auth/         # JWT authentication, password hashing, & permission guards
├── routes/       # Endpoint handlers (cards, support tickets, transactions, agent triggers)
├── models/       # Database ORM entity models (SQLAlchemy / Tortoise)
├── schemas/      # Pydantic data schemas for request validation & response serialization
├── services/     # Business logic layer isolating API routes from DB access
├── database/     # DB connection pooling, session lifecycle, and ORM setup
├── middleware/   # Custom HTTP middlewares (CORS, rate limiting, logging)
├── utils/        # Shared backend utilities, formatters, and encryption helpers
└── config/       # Environment variable settings, app configurations, & constants
```

---

## 🚀 Quick Start for Backend Developers

1. **Navigate to the backend directory:**
   ```bash
   cd backend
   ```
2. **Create and activate virtual environment:**
   ```bash
   python -m venv .venv
   # Windows: .venv\Scripts\activate
   # Linux/macOS: source .venv/bin/activate
   ```
3. **Install backend dependencies:**
   ```bash
   pip install -r ../requirements.txt
   ```
4. **Start the API server:**
   ```bash
   uvicorn main:app --reload --port 8000
   ```
   Open `http://localhost:8000/docs` for interactive Swagger UI documentation.

5. **Detailed Backend Documentation:**
   See [backend/README.md](file:///c:/Users/svija/Downloads/CardAssist-AI/backend/README.md) for full architecture specifications.

---

## 🌿 Git Workflow Rules for `backend`
- Always pull the latest changes from `develop` before starting work on API features:
  ```bash
  git pull origin develop
  ```
- Push backend updates to `backend` and open a Pull Request to merge into `develop`.
