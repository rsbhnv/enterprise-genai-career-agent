# Agent Design

This document describes the **multi-agent design**
used in the GenAI Career Agent solution.

The architecture intentionally separates
deterministic logic from GenAI-driven interaction
to ensure reliability and auditability.

---

## Agent Roles Overview
The solution consists of two complementary agents:

1. **Structured Domain Agent**
2. **Free-Text GenAI Agent**

Each agent has clearly defined responsibilities
and operates within strict boundaries.

---

## Structured Domain Agent
The Structured Domain Agent is responsible for:
- Guided, domain-based job discovery
- Eligibility and filtering questions
- Rule-based job matching
- Deterministic and auditable outcomes

This agent prioritizes accuracy and consistency
and is used whenever precise decision-making is required.

---

## Free-Text GenAI Agent
The Free-Text GenAI Agent supports:
- Open-ended user questions
- Informational and exploratory interaction
- Contextual explanations of roles and career paths

This agent never performs eligibility decisions
and redirects users to the structured flow
when authoritative outcomes are needed.

---

## Agent Collaboration
The two agents operate within a single conversational experience
and can redirect users between each other
based on intent and context.

This collaboration ensures:
- Flexibility without loss of control
- Clear ownership of decisions
- Predictable conversational behavior

---

## Summary
The agent design balances:
- Deterministic control
- Conversational flexibility
- Enterprise governance

This approach avoids over-reliance on GenAI
while delivering a natural user experience.
