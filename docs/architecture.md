# NeuroFlow Architecture

## Overview
NeuroFlow is a modular RAG (Retrieval-Augmented Generation) system with five subsystems:
- Ingestion
- Retrieval
- Generation
- Evaluation
- Fine-Tuning

---

## 1. Ingestion Subsystem
Flow:
User Upload → Parsing → Chunking → Embedding → Vector Store

Steps:
- Accept files (PDF, DOCX, CSV, Images, URLs)
- Extract text (OCR for images)
- Chunk text (semantic + fixed hybrid)
- Generate embeddings
- Store in pgvector with metadata

---

## 2. Retrieval Subsystem
Flow:
Query → Embedding → Vector Search + Keyword Search + Metadata Filter → RRF → Reranker → Top-K Context

Techniques:
- Hybrid search (vector + keyword)
- Reciprocal Rank Fusion (RRF)
- Cross-encoder reranking

---

## 3. Generation Subsystem
Flow:
Context + Query → Prompt Builder → Model Router → LLM → Streaming Response

Features:
- Model routing (cost, capability)
- Token streaming (SSE)
- Logging inputs and outputs

---

## 4. Evaluation Subsystem
Flow:
Generated Answer → LLM Judge → Scores → Database

Metrics:
- Faithfulness
- Answer relevance
- Context precision
- Context recall

---

## 5. Fine-Tuning Subsystem
Flow:
Evaluation Logs → Filter High Quality → JSONL → Fine-tune → MLflow → Deploy

Condition:
faithfulness > 0.8 AND rating >= 4