# 🤖 RAG System (AI Assistant)

## 📘 Project Overview

RAG System is a Retrieval Augmented Generation (RAG) application that enables intelligent question answering over custom knowledge sources including PDF documents and web URLs.

It combines LangChain, ChromaDB, HuggingFace Embeddings, and Mistral AI to build an end to end AI pipeline that converts unstructured data into searchable vector knowledge and generates context-aware responses using an LLM.

---

## ✨ Key Features

### 📚 Multi Source Ingestion
- PDF document processing
- Web URL content extraction
- Unified preprocessing pipeline

### 🔍 Semantic Search Engine
- ChromaDB vector database
- HuggingFace embeddings (all-MiniLM-L6-v2)
- MMR-based retrieval for better context diversity

### 🤖 AI-Powered Answer Generation
- Mistral LLM integration
- Retrieval grounded responses
- Reduced hallucination through context enforcement

### 💬 Conversation Memory
- Chat history support
- Follow up question handling
- Context-aware responses

---

## 🧰 Tech Stack

- **Framework:** LangChain  
- **LLM:** Mistral AI  
- **Vector DB:** ChromaDB  
- **Embeddings:** HuggingFace Sentence Transformers  
- **Data Processing:** PyPDF, BeautifulSoup, Requests  
- **Environment:** python-dotenv  

---

## ⚙️ Installation

```bash
python -m venv venv
venv\Scripts\activate   # Windows
source venv/bin/activate  # Mac/Linux

pip install -r requirements.txt
```

---

## 🔑 Environment Setup

Create a `.env` file:

```env
MISTRAL_API_KEY=your_api_key_here
```

---

## ▶️ Run Application

```bash
python app.py
```

---

## 🧪 Workflow

1. Load PDF or URL  
2. Extract & clean text  
3. Split into chunks  
4. Generate embeddings  
5. Store in ChromaDB  
6. User asks question  
7. Retrieve relevant context  
8. Mistral generates final answer  

---

## 🧠 Architecture

```
User Query
   ↓
Embedding Model (HuggingFace)
   ↓
ChromaDB Vector Search
   ↓
Context Retrieval
   ↓
Mistral LLM
   ↓
Final Answer
```

---

## ⚠️ Notes

- Do not upload `chroma_db/` to GitHub  
- First run may download embedding models  
- Internet required for URL ingestion  
- Ensure `.env` is not committed  

---

## 📌 Project Goal

This project demonstrates a complete modern RAG pipeline, combining semantic search and LLM reasoning to build an AI system capable of answering questions from external documents and web sources.

---

## 🚀 Future Improvements

- FastAPI backend for production deployment  
- Streamlit / React UI interface  
- Hybrid search (BM25 + Vector search)  
- Reranking model integration  
- Multi-user memory isolation  
```
