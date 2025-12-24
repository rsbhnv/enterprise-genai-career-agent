# 🤖 GenAI Career Agent – Architecture & Conversation Design

## Overview
This repository describes the architecture and conversation design of an
**enterprise-grade GenAI career agent** that assists candidates in discovering
relevant job opportunities, validating basic eligibility, and navigating
the application process.

The solution is designed to reduce irrelevant inquiries, improve candidate
experience, and support workforce planning by combining deterministic decision
logic with GenAI-powered free-text conversations.

All descriptions are intentionally generic and sanitized to preserve
organizational confidentiality.

---

## My Role
- Architecture and conversation design at the solution level
- Definition of agent responsibilities and interaction modes
- Design of eligibility filtering logic
- Integration of structured data sources with GenAI capabilities
- Hands-on technical coordination across conversational and data layers


---

## High-Level Flow

```
Main Job Menu
↓
User Selects Interaction Mode
↓
Structured Domain Flow ←→ Free-Text Conversation
↓
Job Recommendation
↓
Redirect to Career Portal
```

---

## Architecture Overview
The solution is orchestrated through **Microsoft Copilot Studio**, which serves
as the primary interaction layer and user entry point.

Within this experience, two specialized agents are integrated, each responsible
for a distinct interaction pattern and powered by different AI capabilities.

---

## Agent Design & Responsibilities

### 1️⃣ Structured Domain Agent (Copilot Studio)
This agent is implemented directly within **Copilot Studio** and is responsible
for structured, deterministic job matching based on predefined domains.

The agent is **data-driven** and relies on managed tables stored in **Dataverse**
to evaluate eligibility and return precise job recommendations.

Responsibilities:
- Presenting a domain-based job selection menu
- Guiding users through eligibility and filtering questions
- Applying rule-based logic driven by Dataverse-managed data
- Returning accurate job recommendations based on user responses

This agent ensures accuracy, consistency, and full control over eligibility logic,
while allowing business users to maintain and update job data independently.


---

### 2️⃣ Free-Text GenAI Agent (Azure AI Foundry)
This agent is implemented using **Azure AI Foundry** and handles open-ended,
natural language conversations.

Key capabilities:
- Free-text conversational interaction
- Semantic retrieval using **AI Search** over curated knowledge sources
- Answering general questions about roles, requirements, and career paths
- Redirecting users back to the structured flow when precise matching is required

This agent complements the structured flow by providing flexibility and a more
natural conversational experience.

---

## Knowledge & Data Sources
The solution relies on a combination of structured and unstructured knowledge sources:

- **Dataverse tables** used by the Structured Domain Agent to store job attributes,
  eligibility criteria, and matching rules
- Job description files organized by domain
- Planned roles and future training information

The Free-Text GenAI Agent uses **AI Search** to retrieve relevant information from
curated knowledge sources while maintaining control over authoritative content.

Knowledge and data sources are maintained outside the conversational layer,
allowing independent updates without changes to conversation logic.


---

## Conversation Logic & Behavior

### Interaction Modes
Users can explicitly choose between:
- A **structured, domain-based job matching flow**
- A **free-text conversational flow**

Both modes are accessible within the same Copilot Studio experience, allowing
seamless transitions between guided selection and open-ended inquiry.

### Structured Flow Rules
- Users select a job domain at the beginning of the structured flow
- Eligibility questions are asked only once, unless the user explicitly requests
  to modify previous answers
- Once a match is identified, the agent recommends a relevant role and provides
  a link to the career portal

### Free-Text Handling
- Users may ask general questions in natural language
- When a precise job match is required, the agent can redirect the user back to
  the structured domain flow

### Unavailable or Future Roles
- If a requested role is not currently available, the agent checks for future
  availability indicators
- When applicable, users are informed that the role may open in the future and
  are advised to return at a later time

### Knowledge Gaps and Out-of-Scope Questions
- If a question cannot be answered using available knowledge sources, users are
  redirected to the career portal for additional information
- Questions unrelated to career or job topics are gently redirected back to
  relevant conversation paths

---

## Strengths of the Solution
- Clear separation between deterministic logic and GenAI capabilities
- Controlled and auditable eligibility decision-making
- Flexible conversational experience for candidates
- Scalable architecture suitable for future expansion
- Reduced operational load through automated pre-screening

---

