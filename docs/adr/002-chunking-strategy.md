# ADR 002: Chunking Strategy

## Context
Need to split text into chunks.

## Decision
Use hybrid chunking:
- Semantic (default)
- Fixed-size (fallback)

## Consequences
- Better accuracy
- Slightly slower processing