# GenAI Layer – Azure AI Foundry Overview

This document describes the role of **Azure AI Foundry**
within the Enterprise GenAI Career Agent solution.

Azure AI Foundry provides the **foundation for GenAI capabilities**
used in free-text conversational interactions,
while maintaining enterprise governance, security,
and clear responsibility boundaries.

---

## Purpose of the GenAI Layer

The GenAI layer is responsible for:
- Handling open-ended, natural language questions
- Providing informational and exploratory responses
- Supporting semantic understanding and retrieval
- Complementing structured, deterministic conversation flows

GenAI capabilities are intentionally scoped
to enhance user experience without influencing
authoritative or eligibility-based decisions.

---

## Why Azure AI Foundry

Azure AI Foundry was selected to:
- Centralize and govern GenAI model usage
- Enforce enterprise security and compliance controls
- Integrate safely with curated knowledge sources
- Support retrieval-augmented generation (RAG) patterns

This enables controlled use of GenAI
within regulated enterprise environments,
without exposing internal logic or sensitive data.

---

## Responsibilities and Boundaries

The GenAI layer is designed with explicit boundaries.

### The GenAI layer:
- Answers general career-related questions
- Provides contextual explanations and guidance
- Supports exploratory interaction and discovery
- Redirects users back to structured flows when precision is required

### The GenAI layer does **not**:
- Perform eligibility or matching decisions
- Replace deterministic business logic
- Act as a system of record
- Modify enterprise data

This separation ensures predictability,
auditability, and trust in decision outcomes.

---

## Integration with Copilot Studio

Azure AI Foundry operates as a **capability layer**
invoked from Copilot Studio during free-text interactions.

Copilot Studio retains responsibility for:
- Conversation orchestration
- State management
- Flow control and redirection
- Decision boundaries

This integration model preserves a single
authoritative interaction controller
while extending conversational flexibility.

---

## Summary

The GenAI layer enhances the conversational experience
by enabling natural language interaction
and semantic understanding.

Clear responsibility boundaries ensure that:
- GenAI remains supportive rather than authoritative
- Deterministic logic stays auditable and controlled
- Enterprise governance and reliability are preserved
