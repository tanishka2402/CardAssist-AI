# 📚 CardAssist-AI — Retrieval-Augmented Generation (RAG) Subsystem

> **Document Processing, Vector Storage, and Semantic Context Retrieval Engine.**

---

## 📋 Overview
The `rag` module powers CardAssist-AI's knowledge base. It ingests credit card policy PDFs, terms of service agreements, and fee schedules, converts them into embeddings, and provides semantic search context to AI agents for accurate response generation.

---

## 📂 Directory Structure

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

## ⚙️ Data Ingestion Pipeline

1. **Upload & Extract:** Place raw card policy PDFs into `rag/documents/` and run `pdf_ingestion.py`.
2. **Chunking:** Documents are split into semantic chunks with overlap to retain context.
3. **Embeddings:** Chunks are vectorized using high-dimensional embedding models.
4. **Indexing:** Vectors and metadata are stored in the vector database via `vector_store.py`.
5. **Retrieval:** Agents call `retriever.py` to obtain grounded context for cardholder queries.

---

## 🛠️ Technology Stack
- **PDF Parser:** PyPDF / PDFPlumber / Unstructured
- **Embeddings:** OpenAI text-embedding-3 / Sentence Transformers
- **Vector DB:** ChromaDB / Qdrant / Pinecone
- **Reranker:** Cohere Rerank / Cross-Encoder

---

## 🚀 Running Ingestion
```bash
python rag/pdf_ingestion.py
```
