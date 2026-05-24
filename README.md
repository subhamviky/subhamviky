# Hi, I'm Subham Gupta 👋

**Staff Architect & AI Architecture Framework Author | Enterprise-to-Cloud Advisory** *Translating 13+ Years of Enterprise Transaction Integrity into Governed Cloud-Native & Agentic AI Architectures*

![AWS](https://img.shields.io/badge/AWS-Bedrock_Lambda_SQS_DynamoDB-FF9900?style=flat&logo=amazonaws&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=flat&logo=python&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-Multi--Agent-FF6B35?style=flat)
![Terraform](https://img.shields.io/badge/Terraform-IaC-7B42BC?style=flat&logo=terraform&logoColor=white)
![Java](https://img.shields.io/badge/Java_21-Spring_Boot_3.x-ED8B00?style=flat&logo=spring&logoColor=white)

---

## Architectural Mental Model — Enterprise to Cloud-Native

My core mental model maps 13+ years of enterprise distributed systems patterns directly to AI-native components:

![SAP RAP to Python Agentic Stack mental model](https://raw.githubusercontent.com/subhamviky/order-to-cash-agentic-ai/main/docs/images/sap-to-agentic-mental-model.svg)

> The diagram above is not a translation — it is the same pattern set, different runtime.  
> OData = FastAPI. BDEF = BaseAgent. CDS Entity = AgentState. The framework changed. The thinking didn't.

---

## Framework Authorship — Core Architectural IP

These frameworks represent formalized architectural standards designed to bridge traditional enterprise systems integrity with next-generation agentic workflows.

### 1. E2A Framework (Enterprise-to-Agentic)
**[github.com/subhamviky/e2a-framework](https://github.com/subhamviky/e2a-framework)** A formal, multi-cloud architectural standard mapping legacy transaction patterns (SAP RAP / Spring Boot / Oracle) to LangGraph agent systems.
* **Decoupled Orchestration:** Standardizes base abstract class contracts (`BaseWorkflow`, `BaseAgent`, `BaseRAGPipeline`), isolating enterprise business logic from changing foundational model SDKs.
* **Multi-Cloud Vendor Portability:** Designed to execute the exact same agent subclass across **AWS Bedrock, GCP Vertex AI, Azure AI Foundry, or standalone Meta Llama** runtimes via metadata configuration switches — requiring **zero code changes** at the execution layer.
* **Runtime Vendor Arbitrage:** Includes native, programmatic FinOps cost-routing engines to dynamically shift token workloads based on real-time margin requirements.

### 2. A2C Framework (Architecture-to-Code) — The Meta-Framework
**[github.com/subhamviky/a2c-framework](https://github.com/subhamviky/a2c-framework)** An AI-governed developer platform framework designed to enforce Non-Functional Requirements (NFRs) at generation time.
* **Correct-by-Design Generation:** Uses E2A-governed agents to programmatically generate enterprise-grade microservices, IaC, and CI/CD pipelines — addressing "NFR Amnesia" by moving constraints from loose prompt engineering into strict base-class compiler policies.
* **Automated Quality Gates:** Programmatically injects idempotency annotations, circuit breakers, structured JSON logging, and validation boundaries into generated artifacts *by construction*, validating outputs via `CodeCriticAgent` (RAGAS threshold >= 0.75).

### 3. P0 Framework (Project Bootstrap) — Phase Zero
**[github.com/subhamviky/a2c-framework](https://github.com/subhamviky/a2c-framework)** Phase Zero scaffolding that generates the complete project foundation before A2C's code generation begins.
* **Single bootstrap() entry point:** Generates pyproject.toml/pom.xml/go.mod, full directory tree, .gitignore, .env.example, application.yml, README scaffold, LICENSE, multi-stage Dockerfile, .dockerignore, and Makefile — in one call, under 10 seconds.
* **Runtime and platform independent:** `ProjectBootstrapperFactory` resolves the correct subclass from a `ScaffoldRequest`; supports Python/Poetry, Python/pip, Java/Maven, Java/Gradle, Node/npm, Go; platform: AWS, GCP, Azure, standalone.
* **Composable with A2C via `BootstrapAndGenerateWorkflow`:** A single scaffold-config.json with `scaffold` and `a2c` sections runs the full pipeline — P0 scaffolds the project, then A2C generates the business logic, IaC, and CI/CD in sequence.

---

## 📦 Architectural Spikes & Reference Runtimes (In Progress)
*Purpose-built reference runtimes validating the E2A, A2C, and P0 Frameworks — proving that the same Clean Architecture principles and financial integrity controls proven at $350M+ SAP TM scale apply across Java Spring Boot, Python FastAPI, and serverless runtimes. Active refactoring to full E2A/A2C/P0 base-class inheritance is underway.*

* **[Order-to-Cash Agentic AI Platform](https://github.com/subhamviky/order-to-cash-agentic-ai):** ![Phase 2](https://img.shields.io/badge/Phase_2-In_Progress-blue?style=flat)  
  E2A Primary Reference Implementation using Python, LangGraph, Amazon Bedrock, hybrid OpenSearch retrieval, and full automated Terraform IaC. Serves as the principal testing ground for E2A's multi-agent coordination; active work focuses on refactoring the custom orchestrator to inherit directly from the formalized E2A base-class state contract.  
  *Stack:* Python · FastAPI · LangGraph · Amazon Bedrock · OpenSearch · Terraform · ECS Fargate  
  *Key patterns:* Two-layer DynamoDB idempotency · Circuit breakers · BM25+KNN hybrid RAG · Policy-as-code governance · Async SQS FIFO + DLQ

* **[Cloud-Native Financial Settlement Platform](https://github.com/subhamviky/financial-settlement-platform):** ![Phase 2](https://img.shields.io/badge/Phase_2-In_Progress-blue?style=flat)  
  Java E2A Reference Runtime implementing transactional saga orchestration with automatic reverse-order compensation and Redis-backed AOP idempotency over Kafka. Validates clean core extensibility principles over distributed message brokers.  
  *Stack:* Java 21 · Spring Boot 3.x · Spring AI · Apache Kafka · Redis · PostgreSQL · Docker

* **[Cloud-Native Payment Reconciliation Engine](https://github.com/subhamviky/aws-reconciliation-engine):** ![Phase 1 Live](https://img.shields.io/badge/Phase_1-Live_on_AWS-brightgreen?style=flat)
![Phase 2](https://img.shields.io/badge/Phase_2-In_Progress-blue?style=flat)
  Serverless E2A Spike validating two-layer idempotency (FastAPI, AWS Lambda, SQS FIFO, and DynamoDB conditional writes) in production. Phase 1 validated serverless database locking; Phase 2 focuses on decoupling reconciliation rules out of procedural handlers and wrapping them in E2A-compliant tool execution blocks.  
  *Stack:* Python · FastAPI · Lambda · SQS + DLQ · DynamoDB · CloudWatch · Amazon Bedrock  
  *Key patterns:* Async POST → PENDING → RECONCILED pipeline · DLQ escalation with backoff · LangGraph agent routing · Bedrock Titan RAG over financial audit logs

---

## What I've Proven at Enterprise Scale

At SAP Labs, working on $350M+ financial settlement systems:

- **80% runtime reduction** — Re-engineered synchronous invoicing engine to async pipeline (35 min → 7 min) for 10,000+ daily freight orders
- **Zero audit failures** — Designed idempotency + exactly-once processing for $350M+ in distributed financial postings across 150+ global vendors
- **99.9% stability** — Primary Incident Commander for 300+ mission-critical escalations annually governing $350M+ in annual financial volumes across 150+ global vendors

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

---

## Expertise Framework

<p align="center">
  <img src="https://raw.githubusercontent.com/subhamviky/subhamviky/main/expertise_framework_cloud_native.svg" width="520" alt="Expertise Differentiator Framework"/>
</p>

---

## Tech Stack

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

*Open to: Cloud Solution Architect · Customer Engineer · Advisory Architect roles across Microsoft · Google Cloud · Amazon.
Topics: Agentic AI platform design · Enterprise-to-Cloud migration · RAG at scale · Cloud-native financial systems.*

---

<sub style="font-size: 0.8em; color: gray;">
<b>Structural Attribution:</b> The 6-pillar organizational structure utilized in this framework (Responsible AI, Data Management, Model Hub, Orchestration, Observability, and GenAI Ops) is a structural mapping inspired by the AWS AI Ecosystem visualization by Prashant Rathi.  
<b>Legal Disclaimer:</b> All trademarks, service marks, and logos (AWS, GCP, Azure, Meta Llama, SAP) are the property of their respective owners. Their use is for educational and architectural reference purposes only and does not imply official endorsement by the trademark holders.  
<b>Ecosystem Note:</b> Certain components referenced (e.g., Pinecone, LangGraph, Lakera) are third-party partner technologies and are not native managed services of AWS, Google Cloud, or Microsoft Azure.
</sub>
