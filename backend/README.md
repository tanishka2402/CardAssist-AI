# ⚡ CardAssist-AI — Backend API Service

> **FastAPI Core REST API, Authentication, and Business Logic Engine.**

---

## 📋 Overview
The `backend` module serves as the primary gateway for all CardAssist-AI services. It handles request authentication, API routing, database ORM models, Pydantic validation schemas, and coordinates calls to the AI Agent framework, RAG engine, and Blockchain network.

---

## 📂 Directory Structure

```
backend/
├── main.py       # FastAPI application entrypoint & server initialization
├── api/          # API versioning & top-level router aggregators
├── auth/         # JWT authentication, password hashing, & permission guards
├── routes/       # Endpoint handlers (cards, support, transactions, agents)
├── models/       # Database ORM entity models (SQLAlchemy / Tortoise)
├── schemas/      # Pydantic data schemas for request validation & response serialization
├── services/     # Business logic layer isolating API routes from DB access
├── database/     # DB connection pooling, session lifecycle, and ORM setup
├── middleware/   # Custom HTTP middlewares (CORS, rate limiting, logging)
├── utils/        # Shared backend utilities, formatters, and encryption helpers
└── config/       # Environment variable settings, app configurations, & constants
```

---

## 🛠️ Technology Stack
- **Framework:** FastAPI (Python 3.10+)
- **Data Validation:** Pydantic v2
- **ORM & DB:** SQLAlchemy / Alembic / PostgreSQL
- **Security:** OAuth2 with Password Bearer + JWT Tokens
- **Server:** Uvicorn / Gunicorn

---

## 🚀 Getting Started

### Setup Environment
```bash
cd backend
python -m venv .venv

# Activate virtual environment:
# Windows: .venv\Scripts\activate
# Linux/macOS: source .venv/bin/activate

pip install -r ../requirements.txt
```

### Running Local API Server
```bash
uvicorn main:app --reload --port 8000
```
Interactive API docs available at `http://localhost:8000/docs`.

---

## 🧪 Testing
```bash
pytest ../tests/test_backend.py
```
