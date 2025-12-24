# GenAI Layer – Azure AI Foundry Overview

This document describes the role of **Azure AI Foundry**
within the Enterprise GenAI Career Agent solution.

Azure AI Foundry provides the **foundation for GenAI capabilities**
used in free-text conversational interactions,
while maintaining enterprise governance and control.

---

## Purpose of the GenAI Layer
The GenAI layer is responsible for:
- Handling open-ended, natural language questions
- Providing informational and exploratory responses
- Supporting semantic understanding and retrieval
- Complementing deterministic conversation flows

GenAI capabilities are intentionally scoped
to avoid making authoritative or eligibility-based decisions.

---

## Why Azure AI Foundry
Azure AI Foundry was selected to:
- Centralize GenAI model management
- Enforce governance and usage boundaries
- Integrate securely with enterprise data sources
- Support retrieval-augmented generation (RAG)

This allows GenAI to be used safely
within regulated enterprise environments.

---

## Responsibilities and Boundaries
The GenAI layer:
- Answers general career-related questions
- Provides contextual explanations and guidance
- Redirects users back to structured flows when precision is required

The GenAI layer does **not**:
- Perform eligibility decisions
- Replace deterministic logic
- Act as a system of record

---

## Integration with Copilot Studio
Azure AI Foundry operates as a **capability layer**
invoked from Copilot Studio when free-text interaction is required.

Conversation orchestration, state management,
and decision control remain within Copilot Studio.

---

## Summary
The GenAI layer enhances user experience
by enabling natural language interaction,
while preserving accuracy, auditability,
and enterprise control through clear responsibility boundaries.
