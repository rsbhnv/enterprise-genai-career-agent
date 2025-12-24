# Dataverse Design

This document describes the **Dataverse data model**
used by the Structured Domain Agent.

The design supports deterministic eligibility logic
and business-managed job data.
![Power Platform](screenshots/copilot_studio_datavers.png)
---

## Purpose of Dataverse
Dataverse is used to store:
- Job roles and domains
- Eligibility attributes
- Matching criteria
- Status and availability indicators

It acts as the authoritative source
for structured decision data.

---

## Design Characteristics
- Strongly typed fields
- Choice columns for controlled values
- Business-friendly data management
- Read-only access during conversation runtime

This design enables reliable decision logic
and minimizes runtime ambiguity.

---

## Business Ownership
Job data can be maintained by business users
without requiring changes to conversation logic.

This separation improves agility
while preserving technical control.

---

## Summary
The Dataverse design provides:
- Deterministic decision support
- Clean separation of data and logic
- Enterprise-grade reliability
