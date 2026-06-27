# 🤖 RAG System (AI Assistant)

## 📘 Project Overview

RAG System is a Retrieval Augmented Generation (RAG) application that enables intelligent question answering over custom knowledge sources such as PDF documents and web URLs. It combines LangChain, ChromaDB, HuggingFace Embeddings, Mistral AI, and Streamlit to build an end to end AI pipeline that converts unstructured data into searchable vector knowledge and generates accurate, context aware responses.

Unlike traditional RAG systems, this assistant also functions as a general AI chatbot. If no relevant document or URL context is available, it automatically responds using the LLM's own knowledge, providing a seamless conversational experience.

---

# ✨ Key Features

### 📚 Multi Source Knowledge Ingestion
- PDF document processing
- Web URL content extraction
- Automatic text cleaning and preprocessing

### 🔍 Semantic Search Engine
- ChromaDB persistent vector database
- HuggingFace Sentence Transformers (`all-MiniLM-L6-v2`)
- MMR based retrieval for diverse and relevant context

### 🤖 AI Powered Answer Generation
- Mistral AI integration
- Context aware response generation
- Automatic fallback to LLM knowledge when no relevant context exists

### 💬 Conversation Memory
- Chat history support
- Follow up question handling
- Context aware multi turn conversations

### 🖥️ Interactive Interface
- Streamlit based frontend
- Upload PDFs or add web URLs
- Ask questions through a clean web interface

---

# 🧰 Tech Stack

### AI Framework
- LangChain

### Large Language Model
- Mistral AI

### Vector Database
- ChromaDB

### Embeddings
- HuggingFace Sentence Transformers (`all-MiniLM-L6-v2`)

### Data Processing
- PyPDF
- BeautifulSoup
- Requests

### Frontend
- Streamlit

### Environment Management
- python-dotenv

---

# ⚙️ Installation
## Create Virtual Environment

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### macOS / Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 🔑 Environment Setup

Create a `.env` file in the project root.

```env
MISTRAL_API_KEY=your_api_key_here
```

---

# ▶️ Run the Application

### Streamlit Frontend

```bash
streamlit run streamlit_app.py
```

### Command Line Version

```bash
python app.py
```

---

# 🧪 Workflow

1. Upload a PDF or enter a website URL.
2. Extract and clean the content.
3. Split text into manageable chunks.
4. Generate vector embeddings.
5. Store embeddings in ChromaDB.
6. User asks a question.
7. Retrieve the most relevant context.
8. Generate an answer using Mistral AI.
9. If no relevant context is found, respond using the LLM's general knowledge.

---

# 🧠 System Architecture

```text
                   +----------------------+
                   |      User Input      |
                   | (Question / Upload)  |
                   +----------+-----------+
                              |
               +--------------+--------------+
               |                             |
      Upload PDF                     Enter Website URL
               |                             |
        Text Extraction               Web Scraping
               |                             |
               +--------------+--------------+
                              |
                   Text Cleaning & Processing
                              |
               Recursive Text Chunking
                              |
         HuggingFace Embedding Generation
                              |
                     ChromaDB Vector Store
                              |
                     User Question Received
                              |
                 Semantic Similarity Search
                              |
                 Relevant Context Retrieved
                              |
              +---------------+---------------+
              |                               |
      Context Available?               No Context Found
              |                               |
              v                               v
      Context + Prompt              User Question Only
              |                               |
              +---------------+---------------+
                              |
                         Mistral AI
                              |
                      Final AI Response
                              |
                    Display in Streamlit UI
```

---

# 📂 Project Structure

```text
RAG/
│
├── app.py                 # CLI application
├── streamlit_app.py       # Streamlit frontend
├── chroma_db_multi/       # ChromaDB persistent storage
├── requirements.txt
├── .env
└── README.md
```


# 📌 Project Goal

This project demonstrates a complete Retrieval Augmented Generation (RAG) pipeline by combining document processing, semantic search, vector databases, and Large Language Models. It showcases how external knowledge sources can be integrated with AI to build an intelligent assistant capable of answering both document-based and general purpose questions.

