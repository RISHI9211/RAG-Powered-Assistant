# RAG-Powered-Assistant
A mini chatboat assistant that can answers question based on given documents..

Automobile Domain Mini RAG-Powered Assistant

This repository contains a Mini Retrieval-Augmented Generation (RAG) Assistant designed for the automobile domain. The system enables intelligent question-answering over automobile-related documents such as vehicle owner manuals and diagnostic trouble codes (DTCs) using Hugging Face embeddings and FAISS vector search.



# Project Overview

The assistant processes automobile documents, converts them into vector embeddings, stores them in a vector database, and retrieves relevant information to answer user queries accurately.

# Example Queries
- What is the fuel type for a specific vehicle?
- What is the engine oil service interval?
- What type of car insurance is required or recommended?
- What does a specific diagnostic trouble code (DTC) mean?



# System Architecture




#  Tech Stack

- Programming Language: Python  
- Embeddings: Hugging Face Sentence Transformers  
- Vector Database: FAISS  
- LLM: Open-source / API-based LLM (configurable)  
- Document Formats: PDF, DOCX, TXT  
- Cloud Deployment: Azure



#  Project Structure



# Workflow
graph TD
    %% Phase 1: Ingestion
    subgraph Ingestion_Phase [1. Document Ingestion]
        A[📄 Documents Upload] --> B[🧹 Text Extraction & Cleaning]
        B --> C[✂️ Chunking <br/> 500-800 chars]
        C --> D[🔢 HuggingFace Embeddings]
        D --> E[(📚 FAISS Vector Database)]
    end

    %% Phase 2: Retrieval
    subgraph Query_Phase [2. Query & Generation]
        F[❓ User Query] --> G[🔢 Query Embedding]
        G --> H{🔍 Similarity Search}
        E -.->|Search Index| H
        H --> I[🔗 Context + Prompt Construction]
        I --> J[🧠 LLM GPT Generation]
        J --> K[✨ Final Answer + Citations]
    end

    %% Styling
    style E fill:#f9f,stroke:#333,stroke-width:2px
    style J fill:#bbf,stroke:#333,stroke-width:2px
    style K fill:#bfb,stroke:#333,stroke-width:2px
# Document Ingestion
- Upload automobile-related documents:
  Vehicle owner manuals
  Diagnostic Trouble Code (DTC) references
- Supported formats: PDF, DOCX, TXT

# Text Preprocessing
- Text cleaning (remove noise, headers, symbols)
- Chunking documents into smaller semantic units

# Embedding Generation
- Generate dense vector embeddings using Hugging Face models
- Example model:


# Vector Storage
- Store embeddings in FAISS for efficient similarity search

# Query Handling
- User query is embedded
- Relevant chunks retrieved from FAISS
- Context passed to LLM for response generation

#  Response Generation
- Context-aware answers generated using RAG



# Deployment

- Deployable on: Azure App Service






