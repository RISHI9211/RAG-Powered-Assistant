# RAG-Powered-Assistant
A mini chatboat assistant that can answers question based on given documents..

Automobile Domain Mini RAG-Powered Assistant

This repository contains a Mini Retrieval-Augmented Generation (RAG) Assistant designed for the automobile domain. The system enables intelligent question-answering over automobile-related documents such as "vehicle owner manuals" and "diagnostic trouble codes (DTCs)" using Hugging Face embeddings and FAISS vector search.



# Project Overview

The assistant processes automobile documents, converts them into vector embeddings, stores them in a vector database, and retrieves relevant information to answer user queries accurately.

# Example Queries
- What is the fuel type for a specific vehicle?
- What is the engine oil service interval?
- What type of car insurance is required or recommended?
- What does a specific diagnostic trouble code (DTC) mean?



#  Tech Stack

- Programming Language: Python  
- Embeddings: Hugging Face Sentence Transformers  
- Vector Database: FAISS  
- LLM: Open-source / API-based LLM (configurable)  
- Document Formats: PDF, DOCX, TXT  
- Cloud Deployment: Azure



#  Project Structure
<invoke name="artifacts">
<parameter name="command">update</parameter>
<parameter name="id">auto_rag_readme</parameter>
<parameter name="old_str">├── app.py                      # Flask application
├── main.py                     # FastAPI application
├── requirements.txt            # Python dependencies
├── Dockerfile                </parameter>
<parameter name="new_str">├── app.py                      # Flask application
├── main.py                     # FastAPI application
├── requirements.txt            # Python dependencies
├── Dockerfile                  # Container configuration
├── .env                        # Environment variables (not in git)
├── .gitignore                  # Git ignore file
├── README.md                   # This file
│
├── src/                        # Source code
│   ├── __init__.py
│   ├── embeddings.py          # HuggingFace embedding generation
│   ├── vectorstore.py         # FAISS vector database operations
│   ├── chunking.py            # Document chunking logic
│   ├── llm.py                 # LLM integration (OpenAI/Llama)
│   ├── preprocessing.py       # PDF/text extraction & cleaning
│   └── utils.py               # Utility functions
│
├── scripts/                    # Utility scripts
│   ├── index_documents.py     # Process and index documents
│   ├── test_queries.py        # Test query examples
│   └── clear_index.py         # Clear FAISS index
│
├── data/                       # Data directory
│   ├── documents/             # Raw automobile documents
│   │   ├── manuals/           # Owner manuals
│   │   ├── dtc_codes/         # Diagnostic trouble codes
│   │   └── service/           # Service schedules
│   ├── processed/             # Processed chunks
│   └── faiss_index/           # FAISS vector index files
│
├── api/                        # API routes
│   ├── __init__.py
│   ├── query.py               # Query endpoint
│   ├── upload.py              # Upload endpoint
│   └── stats.py               # Statistics endpoint
│
├── models/                     # Model definitions
│   ├── __init__.py
│   ├── query_model.py         # Query request/response models
│   └── document_model.py      # Document metadata models
│
├── config/                     # Configuration files
│   ├── __init__.py
│   ├── settings.py            # App settings
│   └── prompts.py             # LLM prompts
│
├── tests/                      # Unit tests
│   ├── test_embeddings.py
│   ├── test_vectorstore.py
│   ├── test_chunking.py
│   └── test_api.py
│
├── deployment/                 # Deployment configs
│   ├── docker-compose.yml     # Local Docker setup
│   ├── kubernetes/            # K8s manifests
│   │   ├── deployment.yaml
│   │   └── service.yaml
│   └── terraform/             # Infrastructure as Code
│       ├── main.tf
│       └── variables.tf
│
├── frontend/                   # Optional React frontend
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   │   ├── QueryInput.jsx
│   │   │   ├── AnswerDisplay.jsx
│   │   │   └── DocumentUpload.jsx
│   │   ├── App.jsx
│   │   └── index.js
│   └── package.json
│
├── docs/                       # Documentation
│   ├── architecture.md        # Detailed architecture
│   ├── api_guide.md           # API documentation
│   └── deployment_guide.md    # Deployment instructions
│
└── logs/                       # Application logs
    └── app.log
```</parameter>
# Workflow
mini-rag-automobile-assistant

- Data
raw_docs # Owner manuals, DTC documents
processed_docs # Cleaned & chunked text

- Embeddings
embedder.py # Hugging Face embedding logic

- Vector_store
faiss_index # Stored FAISS index
faiss_utils.py

- Retriever
retriever.py # Similarity search logic

- Rag_pipeline
rag_chain.py # End-to-end RAG pipeline

- App
api.py # Query interface (FastAPI/Flask)

- Deployment

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






