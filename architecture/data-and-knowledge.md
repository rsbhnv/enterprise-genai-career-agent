# Data & Knowledge Architecture

This document describes how **data and knowledge**
are managed and consumed by the GenAI Career Agent.

The solution separates structured decision data
from unstructured informational content.

---

## Structured Data
Structured data is used for:
- Job definitions
- Eligibility criteria
- Domain classification
- Deterministic matching logic

This data is managed centrally
and treated as the system of record.

---

## Unstructured Knowledge
Unstructured knowledge supports:
- General career questions
- Role explanations
- Informational guidance

Knowledge sources are curated
and consumed through retrieval mechanisms
rather than embedded directly in conversation logic.

---

## Data Ownership and Updates
Data and knowledge are maintained outside the conversational layer,
allowing updates without changes to agent logic.

This separation improves:
- Maintainability
- Governance
- Business ownership of content

---

## Summary
The data and knowledge design ensures:
- Accurate decision-making
- Controlled GenAI grounding
- Independent lifecycle management
