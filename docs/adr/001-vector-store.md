# ADR 001: Vector Store

## Context
Need a vector database for storing embeddings.

## Decision
Use PostgreSQL with pgvector.

## Consequences
- Easy setup
- No extra cost
- Slightly less scalable than Pinecone