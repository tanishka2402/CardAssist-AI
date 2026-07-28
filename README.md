# 💳 CardAssist-AI

> **Production-Ready Monorepo for AI-Powered Credit Card Assistance, Intelligent Multi-Agent Orchestration, RAG Knowledge Base, and Blockchain Audit Verification.**

---

## 📌 Executive Summary

**CardAssist-AI** is an enterprise-grade platform designed to streamline cardholder support, fraud detection, policy verification, and transaction processing using an autonomous Multi-Agent AI system. By combining Retrieval-Augmented Generation (RAG) for policy & document analysis with Blockchain smart contracts for immutable audit trails, CardAssist-AI ensures secure, transparent, and intelligent card assistance workflows.

---

## 🏗️ High-Level System Architecture

```
                                    +-----------------------+
                                    |     Frontend UI       |
                                    | (React / Next.js Web) |
                                    +-----------+-----------+
                                                |
                                                v
                                    +-----------------------+
                                    |     Backend API       |
                                    |   (FastAPI / Python)  |
                                    +-----------+-----------+
                                                |
       +----------------------------------------+----------------------------------------+
       |                                        |                                        |
       v                                        v                                        v
+--------------+                       +------------------+                    +------------------+
|  AI Agents   |<--------------------->|   RAG Engine     |                    |    Blockchain    |
| Orchestration|                       | (Vector & Docs)  |                    | (Solidity/EVM)   |
+--------------+                       +------------------+                    +------------------+
```

---

## 📂 Comprehensive Directory & Subsystem Map

The repository is structured as a monorepo containing modular, independent subsystems. Below is the detailed breakdown of every directory and its purpose:

```
CardAssist-AI/
├── frontend/             # User Interface Subsystem
├── backend/              # Core API & Service Layer
├── agents/               # Autonomous Multi-Agent AI Engine
├── rag/                  # Retrieval-Augmented Generation Subsystem
├── blockchain/           # Smart Contracts & On-Chain Audit Log
├── database/             # Relational Database Schemas & Migrations
├── docs/                 # Developer Documentation & Architecture Specifications
├── tests/                # System Integration & End-to-End Test Suites
├── docker/               # Containerization Definitions & Configurations
├── scripts/              # Automation & Operational Management Scripts
└── .github/workflows/    # CI/CD Automated Pipelines
```

---

### 1. 🎨 `frontend/` — Web Application Layer
Provides the user-facing portal for cardholders and admin dashboards for customer support agents.
- `app/`: Next.js / React application routes, pages, and layout definitions.
- `components/`: Reusable UI components (buttons, modals, card displays, chat widgets).
- `hooks/`: Custom React hooks for state management, authentication, and WebSocket/API hooks.
- `lib/`: Shared utility functions, formatters, and client-side helpers.
- `services/`: API client modules for interacting with the `backend/` services.
- `public/`: Static assets including images, icons, fonts, and manifest files.
- `styles/`: Global styling, CSS modules, design tokens, and theme configurations.

---

### 2. ⚡ `backend/` — FastAPI Service Engine
Powers the core REST APIs, user authentication, request routing, and database integrations.
- `main.py`: Main entry point for starting the FastAPI backend application server.
- `api/`: API versioning and top-level router aggregators.
- `auth/`: Authentication logic (JWT validation, OAuth2 integrations, password hashing).
- `routes/`: Specific endpoint route modules (e.g., card management, support tickets, agent triggers).
- `models/`: Database ORM models (e.g., SQLAlchemy / Tortoise data definitions).
- `schemas/`: Request and response validation schemas (Pydantic data models).
- `services/`: Business logic handlers separating raw API requests from data storage.
- `database/`: Database connection pooling, session creation, and ORM setup.
- `middleware/`: Custom HTTP middlewares (CORS handling, request logging, rate limiting).
- `utils/`: Common backend utilities (helpers, date formatters, encryption utils).
- `config/`: Application settings, environment variable loaders, and constants.

---

### 3. 🤖 `agents/` — Multi-Agent AI System
Housing autonomous agents coordinate via `orchestrator.py` to handle complex cardholder requests safely.
- `orchestrator.py`: Master workflow controller routing tasks between specialized agents.
- `intent/`: Recognizes and categorizes user requests (e.g., limit increase, fraud report, lost card).
- `verification/`: Validates user identity, card status, and security challenges.
- `policy/`: Checks credit card terms, conditions, limits, and eligibility guidelines.
- `fraud/`: Real-time anomaly detection, risk scoring, and suspicious activity analysis.
- `decision/`: Automated approval, conditional approval, or rejection decision logic.
- `execution/`: Executes approved card operations (e.g., blocking card, issuing replacement).
- `audit/`: Generates structured audit records for all agent decisions and actions.
- `blockchain/`: Interfaces agent action logs directly with smart contracts for immutable proof.
- `notification/`: Triggers customer communications via SMS, Email, or Push notifications.
- `escalation/`: Routes high-risk or ambiguous requests to human support representatives.

---

### 4. 📚 `rag/` — Knowledge & RAG Subsystem
Processes documentation, PDF policy guides, and terms to answer user queries with precise context.
- `pdf_ingestion.py`: Extracts raw text, tables, and metadata from card policy PDFs and manuals.
- `chunking.py`: Splits large documents into semantic chunks optimized for retrieval.
- `embeddings.py`: Generates vector embeddings for document chunks using AI embedding models.
- `vector_store.py`: Interface wrapper for vector database operations (ChromaDB / Qdrant / Pinecone).
- `retriever.py`: Hybrid search retriever combining vector similarity search with keyword search.
- `documents/`: Storage directory for raw card agreements, policy PDFs, and knowledge files.
- `prompts/`: System prompt templates for context-augmented agent responses.

---

### 5. ⛓️ `blockchain/` — On-Chain Audit & Verification Layer
Ensures zero-tamper audit logs for financial card operations using Ethereum/EVM smart contracts.
- `hardhat.config.js`: Configuration for Hardhat development environment, networks, and compilers.
- `package.json`: Node dependencies for contract compilation, testing, and deployment.
- `contracts/`: Solidity smart contracts (e.g., AuditLogger.sol, VerificationRegistry.sol).
- `scripts/`: Deployment scripts for local testnets, test networks (Sepolia), and mainnet.
- `test/`: Automated test suite for verifying smart contract logic and edge cases.
- `abi/`: Generated JSON Application Binary Interfaces (ABIs) for backend/agent consumption.
- `ignition/`: Hardhat Ignition deployment and module definitions.

---

### 6. 🗄️ `database/` — Data Persistence Layer
Manages relational database structures, migration scripts, and seed datasets.
- `schema.sql`: Core DDL SQL file containing tables, indices, and foreign key relationships.
- `seed.sql`: Initial seed data for local development (sample users, test cards, policies).
- `migrations/`: Alembic / SQL versioned migration files for schema evolution.

---

### 7. 🛠️ Top-Level Support Directories
- `docs/`: System architectural diagrams, API specifications, and operational playbooks.
- `tests/`: End-to-end (E2E) integration tests covering cross-subsystem workflows.
- `docker/`: Custom Dockerfiles for microservices (backend, frontend, rag service).
- `scripts/`: Development utility scripts (scaffolding, database resets, data sync).
- `.github/workflows/`: GitHub Actions workflows for continuous integration (CI) and deployment (CD).

---

## 🌿 Monorepo Branching Strategy

To maintain high code quality and isolate feature development, the repository follows a strict multi-branch model:

| Branch Name | Primary Scope / Responsibility |
| :--- | :--- |
| `main` | Production-ready stable release code |
| `develop` | Primary integration branch for feature pull requests |
| `frontend` | User interface and web portal development |
| `backend` | Core API, backend services, and database integration |
| `ai-agents` | Multi-agent orchestrator and specialized agent workflows |
| `rag` | Document ingestion, vector storage, and retriever logic |
| `blockchain` | Smart contract development, hardhat scripts, and ABIs |

### Branch Workflow Rules:
1. Always base feature development off `develop`.
2. Push domain-specific changes to your feature/domain branch (e.g., `ai-agents`, `frontend`).
3. Open a Pull Request targeting `develop` for peer review before merging into `main`.

---

## 🚀 Getting Started for Developers

### Prerequisites
- **Python**: 3.10+
- **Node.js**: v18+ (pnpm / npm)
- **Docker**: Desktop / Engine v20+ with Docker Compose
- **Git**: 2.30+

### Environment Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/tanishka2402/CardAssist-AI.git
   cd CardAssist-AI
   ```

2. **Configure Environment Variables:**
   ```bash
   cp .env.example .env
   ```
   Edit `.env` to configure database connections, secret keys, AI API keys, and blockchain RPC URLs.

3. **Backend & Agent Setup (Python):**
   ```bash
   python -m venv .venv
   # Windows:
   .venv\Scripts\activate
   # Linux/macOS:
   source .venv/bin/activate

   pip install -r requirements.txt
   ```

4. **Blockchain Setup (Node.js & Hardhat):**
   ```bash
   cd blockchain
   npm install
   npx hardhat compile
   cd ..
   ```

5. **Running Local Services via Docker Compose:**
   ```bash
   docker-compose up --build
   ```

---

## 🧪 Testing & Verification

Run tests across subsystems to ensure system integrity:

- **Backend & Agent Tests:**
  ```bash
  pytest tests/
  ```
- **Smart Contract Tests:**
  ```bash
  cd blockchain
  npx hardhat test
  ```

---

## 🛡️ Security & Best Practices

- **Never commit `.env` files** or secret keys to version control.
- **Audit smart contracts** thoroughly before deploying to public testnets or mainnet.
- **Enforce strict validation** on all agent execution outputs before calling external APIs or contract methods.

---

## 📄 License
This repository is maintained for **CardAssist-AI**. See `LICENSE` for licensing terms.
