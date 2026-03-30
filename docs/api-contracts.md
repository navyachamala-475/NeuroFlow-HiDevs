# API Contracts

## POST /ingest
Request:
{
  "type": "file | url",
  "source": "path_or_url"
}

Response:
{
  "ingest_id": "uuid",
  "status": "processing"
}

---

## POST /query
Request:
{
  "query": "What is AI?",
  "pipeline_id": "default"
}

Response:
{
  "query_id": "uuid",
  "status": "started"
}

---

## GET /query/{id}/stream
Response (SSE):
data: token1
data: token2

---

## GET /evaluations
Response:
{
  "results": [],
  "page": 1
}

---

## GET /evaluations/aggregate
Response:
{
  "avg_faithfulness": 0.9
}

---

## POST /pipelines
Request:
{
  "name": "default",
  "model": "gpt-4"
}

---

## GET /pipelines/{id}/runs
Response:
{
  "runs": []
}

---

## POST /finetune/jobs
Request:
{
  "dataset_id": "123"
}

---

## GET /finetune/jobs/{id}
Response:
{
  "status": "running"
}

---

## GET /health
{
  "status": "ok"
}