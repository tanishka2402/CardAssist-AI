# 📚 CardAssist-AI — RAG Subsystem Development Branch (`rag`)

> **Domain Branch for Retrieval-Augmented Generation, Document Ingestion Pipelines, Vector Stores, and Hybrid Context Retrievers.**

---

## 📌 Branch Focus: RAG Knowledge Subsystem

This branch (`rag`) is dedicated to building, refining, and evaluating the RAG pipeline of CardAssist-AI. Developers working on this branch focus on PDF document extraction, text chunking strategies, vector embeddings, indexing, vector database wrappers, and hybrid retrievers.

---

## 📂 RAG Subsystem Map (`rag/`)

```
rag/
├── pdf_ingestion.py   # PDF text, table, and metadata extraction pipeline
├── chunking.py        # Semantic text splitting & chunking strategies
├── embeddings.py      # Vector embeddings generation wrapper
├── vector_store.py    # Vector DB interface (ChromaDB / Qdrant / Pinecone)
├── retriever.py       # Hybrid semantic + keyword context retriever
├── documents/         # Raw storage directory for card policy PDFs & manuals
└── prompts/           # System prompt templates for context-guided generation
```

---

## 🚀 Quick Start for RAG Developers

1. **Activate virtual environment:**
   ```bash
   # Windows: .venv\Scripts\activate
   # Linux/macOS: source .venv/bin/activate
   ```
2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
3. **Run Document Ingestion Pipeline:**
   ```bash
   python rag/pdf_ingestion.py
   ```

4. **Detailed RAG Architecture Documentation:**
   See [rag/README.md](file:///c:/Users/svija/Downloads/CardAssist-AI/rag/README.md) for full pipeline specifications.

---

## 🌿 Git Workflow Rules for `rag`
- Always pull the latest changes from `develop` before starting work on ingestion or retrieval algorithms:
  ```bash
  git pull origin develop
  ```
- Push RAG updates to `rag` and open a Pull Request to merge into `develop`.
