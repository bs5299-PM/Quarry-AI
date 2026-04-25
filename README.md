# Quarry AI — AI Competitive Intelligence Agent

> **RAG + Multi-Agent System  |  AI PM Portfolio Project**

## The Problem

Product teams spend **6–10 hours per week** manually tracking competitors.
Signals arrive days late. Decisions get made on stale data.
A competitor can launch a major feature on Monday — and the team finds out Friday.

## The Solution

Quarry AI is an always-on AI analyst that **mines competitor intelligence**
from websites, job boards, news, and reviews — then delivers cited,
grounded answers in **under 5 seconds**.

---

## System Architecture

System Architecture Daigram.png

---

## System Flow

System Flow Daigram.png

---

## Product UI

UI Design.png

---

## Key PM Decisions

| Decision | Why |
|---|---|
| Hybrid retrieval (BM25 + vector) | Pure vector search misses exact product names like "Notion AI" — BM25 fixes this |
| text-embedding-3-small not -large | 5x cheaper ($0.002 vs $0.013 per 1M tokens) with no quality loss for this use case |
| Task Success Rate as north star | A correct answer a PM cannot act on has failed — product outcome, not model metric |
| HITL with automatic triggers | Faithfulness < 0.85 routes to human review with 2-hour SLA before delivery |
| GPT-4o only for synthesis | GPT-4o-mini handles cheap steps; GPT-4o reserved for final answer quality |

---

## Tech Stack

`GPT-4o`   `GPT-4o-mini`   `text-embedding-3-small`   `Pinecone`   `Cohere Rerank`   `DistilBERT`   `LangGraph`

---

## Evaluation Framework

| Tier | Metric | Target |
|---|---|---|
| Retrieval | Context Precision | > 80% |
| Retrieval | Context Recall | > 75% |
| Generation | Faithfulness | > 90% |
| Generation | Hallucination Rate | < 5% |
| Product | Task Success Rate | > 80% |
| Business | Cost per query | < $0.03 |

---

## Full PRD

📄 QuarryAI_PRD.pdf

---

*Built by Bindu Singh ·  AI Product Manager*
https://www.linkedin.com/in/bindu-singh-pmp-csm/ 
After pasting, click the green "Commit changes" button at the bottom of the GitHub editor. Your README will go live immediately.
QuarryAI_PRD.pdf must match upload
Make sure your PDF filename matches exactly — GitHub links are case sensitive
