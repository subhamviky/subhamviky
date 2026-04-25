# Hi, I'm Subham Gupta 👋

**Staff Architect & AI Architect** at SAP Labs India
13+ years governing $350M+ in financial transaction volumes — now building production AI systems on AWS.

![AWS](https://img.shields.io/badge/AWS-Bedrock_Lambda_SQS_DynamoDB-FF9900?style=flat&logo=amazonaws&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat&logo=python&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-Multi--Agent-FF6B35?style=flat)
![Terraform](https://img.shields.io/badge/Terraform-IaC-7B42BC?style=flat&logo=terraform&logoColor=white)

---

## What I Build

My core mental model maps 13+ years of enterprise distributed systems
patterns directly to AI-native components:

![SAP RAP to Python Agentic Stack mental model](https://raw.githubusercontent.com/subhamviky/order-to-cash-agentic-ai/main/docs/images/sap-to-agentic-mental-model.svg)

> The diagram above is not a translation — it is the same pattern set, different runtime.
> OData = FastAPI. BDEF = BaseAgent. CDS Entity = AgentState. The framework changed. The thinking didn't.

---

## Active Portfolio

### 1. Order-to-Cash Agentic AI Platform
![Phase 2](https://img.shields.io/badge/Phase_2-In_Progress-blue?style=flat)

> 5-agent LangGraph system with Amazon Bedrock RAG, hybrid OpenSearch retrieval, MCP-style tool
> microservices, Terraform IaC, and RAGAS CI/CD evaluation gate.

**Stack:** Python · FastAPI · LangGraph · Amazon Bedrock · OpenSearch · Terraform · ECS Fargate

**Key patterns:** Two-layer DynamoDB idempotency · Circuit breakers · BM25+KNN hybrid RAG ·
Policy-as-code governance · Async SQS FIFO + DLQ

**[View Repository →](https://github.com/subhamviky/order-to-cash-agentic-ai)**

---

### 2. Cloud-Native Payment Reconciliation Engine
![Phase 1](https://img.shields.io/badge/Phase_1-Live_on_AWS-brightgreen?style=flat)
![Phase 2](https://img.shields.io/badge/Phase_2-Q2_2026-blue?style=flat)

> Production payment reconciliation engine on AWS, directly mirroring $350M SAP TM financial
> settlement architecture on cloud-native infrastructure.

**Stack:** Python · FastAPI · Lambda · SQS + DLQ · DynamoDB · CloudWatch · Amazon Bedrock

**Key patterns:** Async POST → PENDING → RECONCILED pipeline · DLQ escalation with backoff ·
LangGraph agent routing · Bedrock Titan RAG over financial audit logs

**[View Repository →](https://github.com/subhamviky/aws-reconciliation-engine)**

---
📐 **[E2A Framework](https://github.com/subhamviky/e2a-framework)** — Enterprise-to-Agentic
Architecture: formal mapping of SAP RAP / Spring Boot / Oracle patterns to LangGraph agent systems.

## What I've Proven at Enterprise Scale

At SAP Labs, working on $350M+ financial settlement systems:

- **80% runtime reduction** — Re-engineered synchronous invoicing engine to async pipeline (35 min → 7 min) for 10,000+ daily freight orders
- **Zero audit failures** — Designed idempotency + exactly-once processing for $350M+ in distributed financial postings across 150+ global vendors
- **99.9% stability** — Primary Incident Commander for 300+ mission-critical escalations annually

---

## 🏛️ Architectural Philosophy — Correct by Design
 
> *Idempotency and Reconciliation are **business features**, and not just technical safeguards.*
 
At SAP TM scale, financial integrity was achieved not by adding defensive code, but by making incorrect states architecturally impossible:
 
| SAP TM Mechanism | What It Enforces | Cloud-Native Equivalent |
|---|---|---|
| Line-Element Key | Deterministic 1:1 charge-to-settlement mapping — revised amounts route as valid updates, never duplicates | Redis `SETNX` idempotency key · DynamoDB conditional write |
| "Completely Invoiced" business gate | Ledger posting blocked until business status confirmed — immutable by contract, not by code | `SettlementState.COMPLETED` as the only valid pre-condition for ledger write |
| Dispute Management workflow | Charge delta mediation as a first-class business process — unblocks final posting without bypassing integrity | RAG-powered reasoning agent references policy docs to resolve discrepancies; CriticAgent groundedness gate |
| SAP FI posting rules | Finance Ledger is a write-once source of truth | Double-entry `UNIQUE` index on `(settlement_id, direction, entry_type)` · reversal-only corrections |
 
**The result:** every transaction is *Correct by Design* — the system governs financial integrity
at the architectural level, not at the exception-handling level.
 
This is the mental model carried from $350M+ SAP TM delivery into:
- `@Idempotent` AOP (Redis SETNX) in the Financial Settlement Platform
- Two-layer DynamoDB idempotency in the Payment Reconciliation Engine
- CriticAgent SLO gate (groundedness ≥ 0.85) in the Order-to-Cash platform

## Expertise Framework

<p align="center">
  <img src="expertise_framework_cloud_native.svg" width="520" alt="Expertise Differentiator Framework"/>
</p>

## Tech Across Both Portfolios

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-LangGraph-1C3C3C?style=flat)
![DynamoDB](https://img.shields.io/badge/DynamoDB-4053D6?style=flat&logo=amazondynamodb&logoColor=white)
![SQS](https://img.shields.io/badge/SQS_+_DLQ-FF9900?style=flat&logo=amazonaws&logoColor=white)
![OpenSearch](https://img.shields.io/badge/OpenSearch-005EB8?style=flat&logo=opensearch&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat&logo=terraform&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)

---

## Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Subham_Gupta-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/subham-gupta-0a05a058)
[![Email](https://img.shields.io/badge/Email-subhamviky@gmail.com-D14836?style=flat&logo=gmail&logoColor=white)](mailto:subhamviky@gmail.com)

*Open to conversations about Agentic AI platform design, RAG at scale, and cloud-native financial systems.*
