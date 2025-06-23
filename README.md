# 💰 Finance RAG Assistant – Gen‑AI App

A powerful Retrieval‑Augmented Generation (RAG) assistant tailored for **financial document intelligence**. This app allows users to securely upload financial data files (PDFs, Excel, CSV) and interact with them using natural language queries. It uses **vector embeddings**, **LangChain**, and **LLMs** like LLaMA3 (via Ollama) to provide accurate, context-aware insights from financial documents — all through a clean **Streamlit UI**.

---

## 🚀 Key Features

- 📄 Upload **PDF, Excel, CSV** financial documents securely  
- 🧠 **Semantic retrieval** using **ChromaDB** vector store  
- 🔗 Built with **LangChain** for structured prompt chaining  
- 💬 Query with **natural language**, get smart answers from your data  
- 🧾 Summarizes **balance sheets**, **P&L statements**, and more  
- 🔒 Designed to run **offline** for privacy and data security  
- ⚡ Fast responses using **local LLMs** (e.g. LLaMA3)

---

## 🛠️ Tech Stack

| Component     | Tool / Library        |
|---------------|------------------------|
| LLM           | LLaMA3 via Ollama       |
| Embeddings    | `nomic-embed-text`     |
| Vector Store  | ChromaDB               |
| Framework     | LangChain              |
| UI            | Streamlit              |
| Language      | Python ≥ 3.10          |

---

## 📁 Project Structure

```bash
├── app.py                  # Streamlit frontend interface
├── generator.py            # LLM prompt controller using LangChain
├── utils/                  # Utilities: loaders, chunkers, retrievers
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation

## clone the repository
git clone https://github.com/NKsCODES/Finance-RAG-Assistant-Gen-AI-App.git
cd Finance-RAG-Assistant-Gen-AI-App

## Install Dependencies
pip install -r requirements.txt

## Pull Required Models via Ollama
ollama pull nomic-embed-text
ollama pull llama3

## Set Environment Variables
EMBED_MODEL=nomic-embed-text
LLM_MODEL=llama3
DB_DIR=./chroma_db
CHUNK_SIZE=500
CHUNK_OVERLAP=50
