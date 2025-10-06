# 🧠 Retrieval-Augmented Generation (RAG) Implementation from Scratch

### 🔍 Overview
This project demonstrates a **from-scratch implementation of a Retrieval-Augmented Generation (RAG)** pipeline — built entirely using **Python** and **LLaMA2** (served locally via **Ollama**).  
The goal is to show how retrieval and generation can be seamlessly combined **without relying on external frameworks** (like LangChain) or external vector databases.

This implementation focuses on understanding the **core mechanics of RAG**:
- How to **retrieve relevant information** from a corpus of documents.
- How to **augment LLM prompts** with retrieved context.
- How to generate **accurate and grounded responses** using an open-source LLM (LLaMA2).

---

## 🎯 Objectives
- Implement a **complete RAG system from scratch**.
- Use **locally running LLaMA2 via Ollama** for generation.
- Build a **simple, lightweight retriever** using a custom text corpus.
- Eliminate dependency on external vector databases (FAISS, Pinecone, etc.).
- Understand how **context grounding** improves response quality.

---

## 🧩 Architecture

```mermaid
graph LR
A[📄 Document Corpus] --> B[🧹 Preprocessing & Chunking]
B --> C[🔍 Retriever (TF-IDF / Semantic Similarity)]
E[💬 User Query] --> F[🧠 Query Preprocessing]
F --> C
C --> G[📄 Retrieve Top-K Relevant Chunks]
G --> H[🤖 LLaMA2 (via Ollama)]
H --> I[🧠 Context-Augmented Response]

### 📈 Key Features

- ✅ No external vector database — pure Python-based retrieval.
- ✅ Uses LLaMA2 model locally via Ollama, ensuring privacy & offline capability.
- ✅ Step-by-step RAG pipeline built from scratch (no LangChain).
- ✅ Modular design — each stage (retrieval, augmentation, generation) can be replaced or improved.
- ✅ Lightweight and reproducible — runs entirely on a personal machine.

### 🔮 Future Enhancements

- 🧩 Integrate semantic embeddings (e.g., SentenceTransformers).
- 🗂️ Add a vector store (FAISS / ChromaDB) for scalable retrieval.
- 🧠 Use reranking models to improve context selection.
- 💬 Create an interactive Streamlit chatbot for real-time querying.
- 🚀 Dockerize and deploy the RAG pipeline locally or on cloud.
