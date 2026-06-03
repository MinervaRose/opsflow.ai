# opsflow-ai

Developed by Sabrina Palis

*MSc Artificial Intelligence (First Class Honours)*

AI Systems • Workflow Automation • AI Operations

![Python](https://img.shields.io/badge/Python-3.10+-blue)
![OpenAI](https://img.shields.io/badge/OpenAI-API-green)
![Status](https://img.shields.io/badge/Status-Production--oriented-orange)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

**Multi-Agent AI Client Operations Router with Safety, SLA, and Activation Layer**

AI lead qualification is only part of the story. Real businesses need to process *all* inbound communication — sales, support, billing, partnerships, and more.

This project demonstrates a production-oriented AI system that turns unstructured inbound messages into structured actions, routing decisions, and human-review-ready replies.

---

## Objective

Transform inbound business messages into:

- structured analysis
- prioritized decisions
- routed operational workflows
- automation-ready payloads

While maintaining:

- safety (untrusted input handling)
- deterministic business logic
- human-in-the-loop control

---

## System Overview

```
inbound message
→ safety agent
→ classification agent
→ entity extraction agent
→ priority + SLA assignment
→ routing agent
→ reply drafting agent
→ QA agent
→ activation payload
```

---

## Core Features

###  Multi-Agent Architecture

The system is structured as a set of logical agents:

- Safety Agent (prompt injection detection)
- Intent & Classification Agent
- Entity Extraction Agent
- Routing Agent (deterministic)
- Reply Drafting Agent
- QA / Review Agent

---

### Deterministic Routing Logic

LLM outputs are **not blindly trusted**.

Routing decisions are enforced via rules:

- Sales → CRM
- Support → Ticket
- Technical incident → Urgent escalation
- Billing → Finance
- Low confidence → Manual review
- Suspicious input → Automation blocked

---

###  SLA Assignment

Each message is mapped to an operational SLA:

- High priority → respond within 1 hour
- Medium → 4 business hours
- Low → 2 business days
- Manual review → no automation

---

###  Scoring Layer

Messages are scored (0–100) using deterministic logic:

- priority
- confidence
- category importance
- urgency signals
- tool mentions

This makes decisions **explainable and auditable**.

---

###  Safety Layer

All inbound messages are treated as untrusted input.

Includes:

- prompt injection detection
- message sanitization
- structured output validation
- automation blocking for risky inputs

---

###  QA / Human Review Layer

Before any action:

- replies are reviewed for risk
- unsupported claims are flagged
- human approval is required

---

###  Activation Layer (Simulation)

The system generates automation-ready payloads for:

- CRM (HubSpot, Pipedrive, etc.)
- Support tools (Zendesk, Intercom)
- Slack notifications
- Internal tasks

Example:

```json
{
  "tool": "crm",
  "object": "deal_or_task",
  "company": "CloudNest",
  "priority": "high"
}
```

---

## Example Use Cases

- inbound sales triage
- support ticket routing
- urgent incident escalation
- billing issue handling
- partnership request routing
- customer success workflows

---

##  Business Impact

This system helps companies:

- reduce manual message triage
- respond faster to high-priority issues
- standardize operational decisions
- prevent risky automation
- scale client operations with AI
- maintain human oversight

---

##  Integration (Production)

This architecture can be connected to:

- Make / n8n / Zapier
- OpenAI API
- HubSpot / Pipedrive / Airtable
- Zendesk / Intercom
- Slack / Gmail
- Custom APIs

---

##  Notebook

The full system is implemented in a Google Colab notebook.

👉 Run the notebook to see:

- single message processing
- batch processing
- routing views
- simulated activations

---

##  Positioning

This project is not a prompt demo.

It demonstrates:

- AI system design
- workflow orchestration
- business logic integration
- safety-aware automation
- production-ready thinking

---

##  Related Project

See also:

👉 **leadflow-ai** — AI lead qualification and scoring system

Together:

- leadflow-ai → acquisition layer  
- opsflow-ai → operations layer  

---

##  License

MIT
