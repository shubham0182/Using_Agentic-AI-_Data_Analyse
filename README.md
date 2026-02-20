# 🧠 n8n RAG Pipeline using Pinecone & OpenAI

This project implements a **Retrieval-Augmented Generation (RAG) pipeline** using **n8n**, **Pinecone Vector Store**, and **OpenAI Embeddings**.  
It automatically ingests documents from **Microsoft OneDrive**, splits and embeds them, and stores them in a vector database for intelligent retrieval.

---

## 🚀 Project Overview

**Goal:**  
To build an **Agentic AI–ready document ingestion pipeline** that transforms raw files into searchable vector embeddings.

**Key Capabilities:**
- Automated document ingestion
- Intelligent text splitting
- Vector embedding generation
- Storage in Pinecone for semantic search
- Scalable foundation for AI agents and chatbots

---

## 🧩 Workflow Architecture

```mermaid
flowchart LR

T[Test Trigger] --> O[Microsoft OneDrive<br/>Download File]

O --> L[Default Data Loader<br/>Load Document]

L --> S[Recursive Character<br/>Text Splitter]

S --> E[OpenAI Embeddings]

E --> P[Pinecone Vector Store<br/>Store Vectors]
