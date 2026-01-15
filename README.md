# 🏡 Real Estate Research Tool (RAG)

A Retrieval-Augmented Generation (RAG) based research assistant that ingests real-world, JavaScript-heavy financial news and answers questions with **source-grounded accuracy**.

Built specifically to analyze **mortgage rates, Federal Reserve policy, and real-estate market trends**.

---

## 🚀 Key Features

- 🌐 **Browser-based ingestion with Playwright**
  - Reliably scrapes JS-heavy sites like CNBC, Bloomberg, Forbes
- 🧠 **RAG Architecture**
  - Chunking → Embeddings → Vector Search → LLM Answering
- 📚 **Source-grounded answers**
  - Every answer is backed by retrieved documents
- ⚡ **Fast semantic search**
  - Uses Chroma vector database
- 🧩 **Modular & extensible**
  - Easy to add new sources, models, or UIs

---

## 🧠 Why Playwright Instead of Standard Document Loaders?

Most real-world news sites:
- Render content via JavaScript
- Block bots and static HTTP requests

Traditional loaders often ingest:
- “Enable JavaScript” pages
- Access denied HTML
- Navigation noise instead of real content

**Playwright solves this by behaving like a real browser**, ensuring high-quality data ingestion — which directly improves retrieval and answer accuracy.

---

## 🏗️ Architecture Overview

