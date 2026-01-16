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
Web Articles (CNBC, etc.)
↓
Playwright (Headless Browser)
↓
Clean Text Extraction
↓
Text Chunking
↓
Embeddings (HuggingFace)
↓
Chroma Vector Database
↓
Retriever
↓
LLM (Groq)
↓
Grounded Answer + Sources


---

## 🛠️ Tech Stack

- **Python 3.12**
- **LangChain 1.2.x**
- **Playwright (Async)**
- **ChromaDB**
- **HuggingFace Embeddings**
- **Groq LLMs**
- **Streamlit (UI layer)**

---

## 📂 Project Structure

Real_Estate_Project/
├── main.py # Streamlit UI
├── rag.py # RAG pipeline (ingestion + retrieval + QA)
├── resources/ # Vector store persistence (ignored in git)
├── .gitignore
└── README.md



---

## ▶️ How to Run

### 1️⃣ Install dependencies
```bash
pip install -r requirements.txt
playwright install
2️⃣ Set environment variables

Create a .env file:

GROQ_API_KEY=your_api_key_here

3️⃣ Run the app
streamlit run main.py


🧪 Example Questions

Why did mortgage rates rise despite a Fed rate cut?

What was the 30-year fixed mortgage rate mentioned in the articles?

How does Federal Reserve policy impact mortgage rates?

Summarize key mortgage-related data points.

🔒 Best Practices Followed

No secrets committed (.gitignore enforced)

Browser-based ingestion for reliability

Context-bounded answers (no hallucination)

Clean separation of ingestion, storage, and querying

📌 Future Improvements

Auto-suggest questions from ingested documents

Streaming responses

Multi-source filtering

Document freshness scoring

Production deployment



👤 Author
Rudy Montoo
Building production-grade AI systems with strong data foundations.

⭐ If you find this useful
Star ⭐ the repository and feel free to fork or contribute.

---

If you want, next I can:
- add **screenshots** section
- write a **requirements.txt**
- add **architecture diagram image**
- tailor README for **recruiters vs engineers**

Just say 👍

