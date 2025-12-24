# Dataverse Design

This document describes the **Dataverse data model**
used by the Structured Domain Agent within the GenAI Career Agent solution.

The design supports deterministic eligibility logic
and business-managed job data.

![Dataverse tables used by the agent (anonymized)](screenshots/copilot_studio_dataverse.png)

---

## Purpose of Dataverse

Dataverse serves as the authoritative data store for
structured, decision-driving information.

It is used to store:
- Job roles and domains
- Eligibility attributes
- Matching and filtering criteria
- Status and availability indicators

This structured data enables consistent
and auditable decision logic during conversations.

---

## Design Characteristics

Key characteristics of the Dataverse model include:

- Strongly typed fields to prevent invalid input
- Choice columns for controlled, enumerated values
- Business-friendly schema for non-technical maintenance
- Read-only access during conversation runtime

This design minimizes ambiguity
and ensures predictable agent behavior.

---

## Data Access Pattern

During runtime:
- The conversational agent reads from Dataverse
- No direct data modification occurs as part of conversations
- All eligibility decisions are driven by stored attributes

This pattern preserves data integrity
and supports safe conversational execution.

---

## Business Ownership

Job and eligibility data can be maintained
by authorized business users through Dataverse
without requiring changes to conversation logic.

This separation:
- Improves agility
- Reduces dependency on development cycles
- Preserves technical control over agent behavior

---

## Summary

The Dataverse design provides:
- Deterministic decision support
- Clear separation of data and logic
- Business-manageable configuration
- Enterprise-grade reliability
