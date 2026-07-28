# 🤖 CardAssist-AI — Multi-Agent AI Development Branch (`ai-agents`)

> **Domain Branch for Autonomous Multi-Agent Workflows, Intent Parsing, Policy Checking, Fraud Detection, and Decision Engines.**

---

## 📌 Branch Focus: AI Multi-Agent System

This branch (`ai-agents`) is dedicated to building, tuning, and evaluating the autonomous Multi-Agent AI architecture of CardAssist-AI. Developers working on this branch focus on agent graph orchestration, specialized agent logic, prompt engineering, and risk assessment models.

---

## 📂 Agents Subsystem Map (`agents/`)

```
agents/
├── orchestrator.py    # Master workflow graph controller & task router
├── intent/            # Natural Language Understanding & intent classification
├── verification/      # User identity, card status, & security challenge validation
├── policy/            # Credit card agreement & policy compliance checking
├── fraud/             # Real-time transaction risk scoring & anomaly detection
├── decision/          # Automated approval / conditional approval / rejection engine
├── execution/         # Executes card actions (block card, reissue, limit adjustment)
├── audit/             # Structured audit logging for agent actions & decisions
├── blockchain/        # On-chain cryptographic proof generation & contract interaction
├── notification/      # Customer alert dispatch (SMS / Email / Push)
└── escalation/        # Handoff controller for transferring complex queries to humans
```

---

## 🚀 Quick Start for AI Agent Developers

1. **Activate virtual environment:**
   ```bash
   # Windows: .venv\Scripts\activate
   # Linux/macOS: source .venv/bin/activate
   ```
2. **Install agent dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
3. **Run Agent Test Suite:**
   ```bash
   pytest tests/test_agents.py
   ```

4. **Detailed Multi-Agent Architecture Documentation:**
   See [agents/README.md](file:///c:/Users/svija/Downloads/CardAssist-AI/agents/README.md) for full workflow and agent communication details.

---

## 🌿 Git Workflow Rules for `ai-agents`
- Always pull the latest changes from `develop` before starting work on agent workflows:
  ```bash
  git pull origin develop
  ```
- Push agent updates to `ai-agents` and open a Pull Request to merge into `develop`.
