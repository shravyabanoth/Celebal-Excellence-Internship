# Assignment 7 – Document Question Answering System (RAG)

This project implements a complete Retrieval-Augmented Generation (RAG) pipeline for answering questions from user-provided documents.

## Features

- Document ingestion (PDF/TXT)
- Text extraction
- Text chunking
- Sentence embeddings using MiniLM
- FAISS vector database
- Semantic retrieval
- Answer generation using FLAN-T5

## Tech Stack

- Python
- Google Colab
- Sentence Transformers
- FAISS
- Hugging Face Transformers
- PyPDF

## Model Used

- Embedding Model: all-MiniLM-L6-v2
- Language Model: google/flan-t5-base
- Vector Store: FAISS

## Project Workflow

1. Environment Setup
2. Import Libraries
3. Upload Documents
4. Extract Text
5. Create Chunks
6. Generate Embeddings
7. Build FAISS Index
8. Load FLAN-T5
9. Retrieve Relevant Context
10. Generate Answers
11. Evaluate Results

---
**Author:** Sravya Banoth
