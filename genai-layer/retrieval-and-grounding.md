# Retrieval & Grounding Strategy

This document describes the **retrieval and grounding approach**
used to support GenAI interactions in the Career Agent solution.

The goal is to provide helpful, accurate answers
while minimizing hallucinations and uncontrolled outputs.

---

## Retrieval-Augmented Generation (RAG)
Free-text responses are grounded using
retrieval-based techniques rather than relying solely on model knowledge.

Key characteristics:
- Responses are based on curated knowledge sources
- Retrieval is scoped to relevant career and role information
- Authoritative content is maintained outside the conversational layer

---

## Knowledge Sources
Typical knowledge sources include:
- Job descriptions organized by domain
- Role requirements and general career information
- Training paths and future role planning content

Knowledge sources are curated and updated independently
from conversation logic.

---

## Grounding Principles
The grounding strategy follows these principles:
- Prefer retrieved content over model assumptions
- Avoid speculative or unsupported answers
- Redirect users when information is incomplete or unavailable
- Maintain consistency across responses

This ensures predictable and trustworthy behavior.

---

## Handling Ambiguity and Knowledge Gaps
When a question cannot be confidently answered:
- The agent avoids speculative responses
- Users are guided to structured flows or external resources
- Clear boundaries are maintained between known and unknown information

---

## Summary
The retrieval and grounding approach enables:
- Safer GenAI usage
- Reduced hallucinations
- Clear separation between knowledge and conversation logic
- Enterprise-ready conversational reliability
