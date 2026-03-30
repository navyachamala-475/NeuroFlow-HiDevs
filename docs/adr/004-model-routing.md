# ADR 004: Model Routing

## Context
NeuroFlow must handle different types of queries such as simple questions, complex reasoning, coding tasks, and domain-specific queries. Using a single model for all queries can increase cost and reduce efficiency.

---

## Decision
We will implement a model routing system based on:
- Cost
- Latency
- Capability (complexity of query)
- Domain specificity

---

## Routing Strategy

| Query Type        | Model Used        | Reason |
|------------------|------------------|--------|
| Simple Q&A       | Low-cost model   | Fast and cheap |
| Complex reasoning| High-capability model | Better accuracy |
| Coding queries   | Strong LLM       | Handles logic well |
| Domain-specific  | Fine-tuned model | Specialized knowledge |

---

## Consequences

### Positive
- Reduced operational cost
- Improved response quality
- Efficient resource utilization

### Negative
- Slight increase in system complexity
- Need for routing logic maintenance