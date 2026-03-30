# NeuroFlow 🚀

NeuroFlow is a modular Retrieval-Augmented Generation (RAG) system designed to process, retrieve, and generate intelligent responses from multiple data sources.

---

## 🔥 Features

- Multi-format data ingestion (PDF, DOCX, Images, URLs)
- Hybrid retrieval (Vector + Keyword search)
- Reranking using advanced models
- LLM-based response generation
- Automated evaluation (LLM-as-judge)
- Fine-tuning pipeline for continuous improvement
- Model routing for cost and performance optimization

---

## 🏗️ System Architecture

NeuroFlow consists of 5 core subsystems:

1. **Ingestion**  
   Handles data upload, parsing, chunking, and embedding.

2. **Retrieval**  
   Uses hybrid search (vector + keyword) and reranking to fetch relevant context.

3. **Generation**  
   Builds prompts and generates responses using LLMs.

4. **Evaluation**  
   Scores responses using metrics like faithfulness and relevance.

5. **Fine-Tuning**  
   Improves model performance using high-quality training data.

---

## 🛠️ Tech Stack

- Backend: Python (FastAPI)
- Database: PostgreSQL (pgvector)
- Frontend: React (planned)
- Evaluation: LLM-as-judge
- Tracking: MLflow

- NeuroFlow-HiDevs/ ├── backend/ ├── frontend/ ├── pipelines/ ├── evaluation/ ├── infra/ ├── docs/ │   ├── architecture.md │   ├── api-contracts.md │   ├── data-models.md │   └── adr/

---

## 🚀 Getting Started

1. Clone the repository
2. Set up environment
3. Run backend services

---

## 📌 Future Work

- Full pipeline implementation
- UI development
- Advanced evaluation metrics
- Deployment

---

## 👩‍💻 Author

Navya

---

## 📂 Project Structure
