# 🤖 CardAssist-AI — Multi-Agent AI System

> **Autonomous Multi-Agent Orchestration Engine for Credit Card Assistance.**

---

## 📋 Overview
The `agents` module contains the multi-agent AI architecture responsible for processing cardholder requests autonomously. Guided by `orchestrator.py`, specialized agents collaborate to analyze user intent, verify identities, check policies, assess fraud risk, make decisions, execute card operations, generate audit trails, submit blockchain proofs, and notify users.

---

## 📂 Directory Structure & Agent Roles

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

## 🔄 Multi-Agent Workflow Execution

```
[User Request] ──> [Orchestrator]
                        │
      ┌─────────────────┼─────────────────┐
      ▼                 ▼                 ▼
[Intent Agent]  [Verification Agent] [Policy Agent]
      │                 │                 │
      └─────────────────┼─────────────────┘
                        ▼
                 [Fraud Agent]
                        │
                        ▼
                [Decision Engine]
                        │
        ┌───────────────┴───────────────┐
        ▼                               ▼
[Execution Agent]               [Escalation Agent]
        │                               │
        ├──> [Audit Agent]               └──> [Human Support]
        │
        ├──> [Blockchain Agent]
        │
        └──> [Notification Agent]
```

---

## 🛠️ Technology Stack
- **Framework:** LangGraph / AutoGen / CrewAI / Custom Graph Orchestrator
- **LLM Models:** OpenAI GPT-4o / Anthropic Claude / Gemini 1.5 Pro
- **Embedding / Memory:** Vector-backed conversational context

---

## 🧪 Testing Agent Workflows
```bash
pytest ../tests/test_agents.py
```
