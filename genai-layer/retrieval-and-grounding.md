# Retrieval & Grounding Strategy

This document describes the **retrieval and grounding approach**
used to support GenAI interactions in the GenAI Career Agent solution.

The primary goal is to provide **helpful, accurate, and consistent answers**
while minimizing hallucinations and preventing uncontrolled or speculative outputs.

---

## Retrieval-Augmented Generation (RAG)

Free-text responses are grounded using
**retrieval-augmented generation (RAG)** techniques,
rather than relying solely on the language model’s internal knowledge.

Key characteristics:
- Responses are based on curated and approved knowledge sources
- Retrieval is scoped to relevant career and role-related content
- Authoritative information is maintained outside the conversational layer

This approach improves accuracy
and ensures that answers remain aligned
with enterprise-approved content.

---

## Knowledge Sources

Typical knowledge sources used for retrieval include:
- Job descriptions organized by domain
- Role requirements and general career information
- Training paths and future role planning content

Knowledge sources are curated, versioned,
and updated independently of conversation logic,
allowing content evolution without redesigning the agent.

---

## Grounding Principles

The grounding strategy follows these core principles:

- Prefer retrieved content over model assumptions
- Avoid speculative or unsupported responses
- Maintain consistent phrasing for authoritative answers
- Redirect users when information is incomplete or unavailable

These principles ensure predictable
and trustworthy conversational behavior.

---

## Handling Ambiguity and Knowledge Gaps

When a user question cannot be confidently answered:
- The agent avoids guessing or fabricating information
- Users are guided back to structured flows when appropriate
- External or authoritative resources may be suggested
- Clear boundaries are maintained between known and unknown information

This behavior preserves user trust
and prevents misleading guidance.

---

## Summary

The retrieval and grounding approach enables:
- Safer and more reliable GenAI usage
- Reduced hallucinations and uncontrolled outputs
- Clear separation between knowledge management and conversation logic
- Enterprise-ready conversational reliability
