# Integration Patterns

This document outlines the **integration patterns**
used by Copilot Studio within the GenAI Career Agent solution.

The focus is on **interaction boundaries and responsibilities**,
not on low-level configuration.

---

## Integration with Dataverse
Dataverse serves as the **system of record**
for structured job and eligibility data.

Integration characteristics:
- Read-only access during conversation runtime
- Rule evaluation based on managed tables
- Business-owned data updates without conversation changes

This ensures data accuracy and operational independence.

---

## Integration with GenAI Services
Copilot Studio integrates with external GenAI capabilities
to support free-text interactions.

Key principles:
- GenAI is used for informational and exploratory conversations
- Deterministic logic is never delegated to LLMs
- Authoritative decisions remain rule-based

This prevents hallucinations from affecting eligibility outcomes.

---

## Redirection Between Interaction Modes
Integration patterns support controlled redirection:
- From structured flow to GenAI for general questions
- From GenAI back to structured flow for precise matching

Transitions are intentional and governed
by conversation state and user intent.

---

## External System Boundaries
Copilot Studio does not:
- Own business logic
- Store sensitive data
- Perform eligibility calculations independently

It acts as an orchestration and interaction layer,
delegating responsibility to appropriate systems.

---

## Summary
The integration patterns ensure:
- Clear system boundaries
- Controlled use of GenAI
- Predictable and auditable behavior
- Enterprise-ready conversational workflows
