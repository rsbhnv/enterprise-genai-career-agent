# Conversation Model

This document describes the **conversation design model**
used in the GenAI Career Agent.

The solution combines **structured, deterministic flows**
with **free-text GenAI conversations**, allowing candidates
to navigate between precision and flexibility.

---

## Dual Interaction Model
The conversational experience supports two complementary modes:

- **Structured Domain Flow**
- **Free-Text Conversational Flow**

Both modes are accessible within the same Copilot Studio agent
and can redirect users between each other when appropriate.

---

## Structured Domain Flow
The structured flow is designed for **accuracy and control**.

Characteristics:
- Domain-based entry points
- Deterministic eligibility questions
- Rule-driven decision logic
- Predictable and auditable outcomes

This flow is used when precise job matching
and eligibility validation are required.

![copilot_studio](screenshots/copilot_studio_blocks.png)
---

## Free-Text Conversational Flow
The free-text flow supports **natural language interaction**.

Characteristics:
- Open-ended user questions
- Semantic understanding
- Informational responses
- Context-aware redirection to structured flow when needed

This flow improves user experience while maintaining
control over authoritative answers.

---

## Conversation State Management
Conversation state is managed explicitly to ensure:
- Questions are not repeated unnecessarily
- User intent is preserved across turns
- Transitions between flows are predictable

State handling prevents confusion and ensures
a coherent user experience.

---

## Out-of-Scope and Fallback Handling
The conversation model includes explicit handling for:
- Questions outside supported domains
- Requests for unavailable roles
- Incomplete or ambiguous user input

Users are guided back to relevant flows
or redirected to external resources when required.

---

## Summary
The conversation model emphasizes:
- Clear separation between deterministic and GenAI interactions
- Controlled transitions between interaction modes
- Predictable behavior with flexible user experience

This approach ensures both usability and enterprise reliability.
