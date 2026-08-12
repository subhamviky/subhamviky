# Hi, I'm Subham Gupta 👋

Systemic Platform Architect · Paved-Path Frameworks & AI DLC Strategy · E2A · A2C · P0 · G2C · AWS · Azure · GCP

Solo-authored architecture R&D, actively in development. Reference runtimes below validate the framework patterns against real (non-production) workloads.

The core thesis: enterprise modernization and agentic AI are not separate initiatives — agentic AI makes application-level modernization structurally mandatory. An LLM cannot safely navigate tightly coupled legacy state machines; it needs clean, deterministic API boundaries to operate without reasoning drift. The E2A/A2C/P0/G2C stack is built specifically to enforce those boundaries. → Full architectural argument: https://www.linkedin.com/pulse/why-agentic-ai-makes-application-modernization-mandatory-subham-gupta-rahne/

![AWS](https://img.shields.io/badge/AWS-Bedrock_Lambda_SQS_DynamoDB-FF9900?style=flat&logo=amazonaws&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=flat&logo=python&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-Multi--Agent-FF6B35?style=flat)
![Terraform](https://img.shields.io/badge/Terraform-IaC-7B42BC?style=flat&logo=terraform&logoColor=white)
![Java](https://img.shields.io/badge/Java_21-Spring_Boot_3.x-ED8B00?style=flat&logo=spring&logoColor=white)
![G2C](https://img.shields.io/badge/G2C-Generate--to--Class-8B2500?style=flat)

---

## Architectural Mental Model — Enterprise to Cloud-Native

My core mental model maps 13+ years of enterprise distributed systems patterns directly to AI-native components:

![SAP RAP to Python Agentic Stack mental model](https://raw.githubusercontent.com/subhamviky/order-to-cash-agentic-ai/main/docs/images/sap-to-agentic-mental-model.svg)

> The diagram above is not a translation — it is the same pattern set, different runtime.  
> OData = FastAPI. BDEF = BaseAgent. CDS Entity = AgentState. The framework changed. The thinking didn't.

---

## ⚙️ How I Work — Architectural Orchestration, Not Deep Execution

I specialize in systemic thinking and shift-left design: auditing current and target-state setups to surface bottlenecks, optimization potential, and common functionality, then codifying the result as abstract patterns — the paved path a team builds on.

That spans both HLD and LLD. At the HLD layer, that means system topology, NFRs, and governance guardrails. At the LLD layer, it means class contracts, method signatures, modularization strategy, strict encapsulation boundaries (public/protected/private), and single entry points — establishing the architectural framework before implementation begins.

Deep vertical execution — tuning retrieval pipelines, model selection, or infrastructure provisioning — is where I collaborate with domain experts and AI tools to implement inside the contracts I've designed. While collaborating closely for domain-specific implementation, I retain 100% technical ownership and responsibility for the final system state: personally authoring core base abstractions (`e2a_base.py`), conducting rigorous code reviews, and verifying runtime behaviour (`multimodal_orchestrator.py`) against production state engines.

The reference runtimes below showcase this exact workflow: I design the HLD/LLD contracts, AI/domain specialists accelerate execution inside those boundaries, and I review, validate, and iterate — demonstrating how this framework stack scales across engineering teams with total architectural governance.

## 🧩 One Framework, Three Use Cases

**E2A is the governance layer, not a single application.** It's a set of
abstract base classes — Template Method pattern — that inject NFRs,
idempotency, and observability at the point of inheritance, so anything
built on top gets compliance by construction instead of by code review.
"Enterprise-to-Agentic" is where the name came from and remains the
flagship use case, but it's one of three the same base classes now govern:

| Use Case | What it is | Where |
| --- | --- | --- |
| **1. Enterprise-to-Agentic** *(origin case)* | SAP RAP / Java EE architecture patterns mapped onto LangGraph and Bedrock agent systems | [e2a-framework](https://github.com/subhamviky/e2a-framework), [order-to-cash-agentic-ai](https://github.com/subhamviky/order-to-cash-agentic-ai) |
| **2. CQRS Cloud-Native Architecture** | The identical base-class contracts applied to standard distributed CQRS systems — no agentic component required | E2A CQRS HLD/LLD & Implementation Playbook (`e2a-framework` docs) |
| **3. AI-Assisted Developer Velocity** | P0 (project bootstrap), A2C (code generation), G2C (self-generating framework classes) — E2A governance applied to the SDLC itself | [a2c-framework](https://github.com/subhamviky/a2c-framework) |

> The letters stand for where the framework started. The governance model
> underneath — abstract base classes enforcing NFRs at the
> class-inheritance level — is what actually generalizes, and use cases 2
> and 3 are proof of that, not exceptions to the name.

---

## Framework Authorship — Core Architectural IP

These frameworks represent formalized architectural standards designed to bridge traditional enterprise systems integrity with next-generation agentic workflows.

### 1. E2A Framework (Enterprise-to-Agentic)
**[github.com/subhamviky/e2a-framework](https://github.com/subhamviky/e2a-framework)** A formal, multi-cloud architectural standard mapping legacy transaction patterns (SAP BOPF/RAP / Spring Boot / Oracle) to LangGraph agent systems.
* **Decoupled Orchestration:** Standardizes base abstract class contracts (`BaseWorkflow`, `BaseAgent`, `BaseRAGPipeline`), isolating enterprise business logic from changing foundational model SDKs.
* **Multi-Cloud Vendor Portability:** Designed to execute the exact same agent subclass across **AWS Bedrock, GCP Vertex AI, Azure AI Foundry, or standalone Meta Llama** runtimes via metadata configuration switches — requiring **zero code changes** at the execution layer.
* **Dual Execution Profiles:** Agentic (`BaseWorkflow`/`BaseAgent`, LangGraph) and Deterministic CQRS (`BaseOrchestrator`/`BaseCommandService`/`BaseQueryService`) — same propagation contract and abstract-class Observability/Governance layer, different Tier 2 routing shape for LLM vs. non-LLM request paths.
* **Deterministic Write Guarantees:** The tool-service base class enforces exactly-once write semantics via a deterministic outbox commit pattern — the same construction-time guarantee SAP TM's Line-Element Key gives ledger postings, generalized to any distributed write.

### 2. A2C Framework (Architecture-to-Code)
**[github.com/subhamviky/a2c-framework](https://github.com/subhamviky/a2c-framework)** An AI-governed developer platform framework designed to enforce Non-Functional Requirements (NFRs) at generation time.
* **Correct-by-Design Generation:** Uses E2A-governed agents to programmatically generate enterprise-grade microservices, IaC, and CI/CD pipelines — addressing "NFR Amnesia" by moving constraints from loose prompt engineering into strict base-class compiler policies.
* **Automated Quality Gates:** Programmatically injects idempotency annotations, circuit breakers, structured JSON logging, and validation boundaries into generated artifacts *by construction*, validating outputs via `CodeCriticAgent` (RAGAS threshold >= 0.75).

### 3. P0 (Project Bootstrap) — Phase Zero module
**Module within [github.com/subhamviky/a2c-framework](https://github.com/subhamviky/a2c-framework)** Phase Zero scaffolding that generates the complete project foundation before A2C's code generation begins.
* **Single bootstrap() entry point:** Generates pyproject.toml/pom.xml/go.mod, full directory tree, .gitignore, .env.example, application.yml, README scaffold, LICENSE, multi-stage Dockerfile, .dockerignore, and Makefile — in one call, under 10 seconds.
* **Runtime and platform independent:** `ProjectBootstrapperFactory` resolves the correct subclass from a `ScaffoldRequest`; supports Python/Poetry, Python/pip, Java/Maven, Java/Gradle, Node/npm, Go; platform: AWS, GCP, Azure, standalone.
* **Composable with A2C via `BootstrapAndGenerateWorkflow`:** A single scaffold-config.json with `scaffold` and `a2c` sections runs the full pipeline — P0 scaffolds the project, then A2C generates the business logic, IaC, and CI/CD in sequence.

### 4. G2C (Generate-to-Class) — Top-of-stack module
**Module within [github.com/subhamviky/a2c-framework](https://github.com/subhamviky/a2c-framework)**
E2A-governed generator classes that produce E2A and A2C abstract classes via LLM.
* **Self-referential design:** G2C generator classes are themselves E2A-governed agents
  inheriting from `BaseGeneratorAgent`. The agent is governed by E2A. The output follows
  E2A. Architecture is enforced at class generation time.
* **One call, complete output:** `DeveloperPlatformWorkflow.generate(request, config)`
  chains E2AAbstractClassGenerator, P0 scaffolding, and inherited class generation
  automatically from a single `generator-config.json`.
---

## 🎯 Vision — Framework-to-Platform Productization

The E2A, A2C, P0, and G2C frameworks are a vendor-neutral productization blueprint for what enterprise cloud AI platforms need most: **governed, NFR-first, enterprise-grade agentic AI developer tooling**.

| Framework | What it solves | Productization form |
|---|---|---|
| **E2A** | Enterprise agentic AI governance — idempotency, SLOs, multi-cloud portability | Governed AI orchestration tooling |
| **A2C** | NFR-first code generation — architecture enforced at generation time, not in review | Developer productivity tooling |
| **P0** | Project scaffolding — complete project foundation in one call, any runtime | Project bootstrap tooling |
| **G2C** | Framework class generation — the stack made self-generating via LLM | Architect productivity tooling |

**The goal:** bring the architectural patterns in this framework stack into a hyperscaler's AI product suite as enterprise-grade developer tooling — this is solo R&D today; the design is built for that destination.

The frameworks are multi-cloud by design. The productization platform is whichever company I get to work with — **AWS Bedrock · Azure AI Foundry · Google Cloud AI**.
---

## 📦 Architectural Spikes & Reference Runtimes (In Progress)
*Purpose-built reference runtimes validating the E2A, A2C, P0 and G2C Frameworks — proving that the same Clean Architecture principles and financial integrity controls proven at $350M+ SAP TM scale apply across Java Spring Boot, Python FastAPI, and serverless runtimes. Built by pairing my HLD/LLD design with AI working out low-level implementation cases under my review — active refactoring to full E2A/A2C/P0 base-class inheritance is underway.*

* **[Order-to-Cash Agentic AI Platform](https://github.com/subhamviky/order-to-cash-agentic-ai):** ![Phase 2](https://img.shields.io/badge/Phase_2-In_Progress-blue?style=flat)  
  E2A Primary Reference Implementation using Python, LangGraph, Amazon Bedrock, hybrid OpenSearch retrieval, and full automated Terraform IaC. Serves as the principal testing ground for E2A's multi-agent coordination; active work focuses on refactoring the custom orchestrator to inherit directly from the formalized E2A base-class state contract.  
  *Stack:* Python · FastAPI · LangGraph · Amazon Bedrock · OpenSearch · Terraform · ECS Fargate  
  *Contracts validated:* Two-layer DynamoDB idempotency · Circuit breakers · Retrieval-groundedness gate (RAGAS ≥ 0.85) · Policy-as-code governance · Async SQS FIFO + DLQ

* **[Cloud-Native Financial Settlement Platform](https://github.com/subhamviky/financial-settlement-platform):** ![Phase 2](https://img.shields.io/badge/Phase_2-In_Progress-blue?style=flat)  
  Java E2A Reference Runtime implementing transactional saga orchestration with automatic reverse-order compensation and Redis-backed AOP idempotency over Kafka. Validates clean core extensibility principles over distributed message brokers.  
  *Stack:* Java 21 · Spring Boot 3.x · Spring AI · Apache Kafka · Redis · PostgreSQL · Docker

* **[Cloud-Native Payment Reconciliation Engine](https://github.com/subhamviky/aws-reconciliation-engine):** ![Phase 1 Live](https://img.shields.io/badge/Phase_1-Live_on_AWS-brightgreen?style=flat)
![Phase 2](https://img.shields.io/badge/Phase_2-In_Progress-blue?style=flat)
  Serverless E2A Spike validating two-layer idempotency (FastAPI, AWS Lambda, SQS FIFO, and DynamoDB conditional writes) in production. Phase 1 validated serverless database locking; Phase 2 focuses on decoupling reconciliation rules out of procedural handlers and wrapping them in E2A-compliant tool execution blocks.  
  *Stack:* Python · FastAPI · Lambda · SQS + DLQ · DynamoDB · CloudWatch · Amazon Bedrock  
  *Contracts validated:* Async POST → PENDING → RECONCILED pipeline · DLQ escalation with backoff · LangGraph agent routing · Retrieval-augmented reasoning gate over financial audit logs (foundation-model agnostic via E2A's interface)

---

## What I've Proven at Enterprise Scale

At SAP Labs, working on $350M+ financial settlement systems:

- **80% runtime reduction** — Re-engineered synchronous invoicing engine to async pipeline (35 min → 7 min) for 10,000+ daily freight orders
- **Zero audit failures** — Designed idempotency + exactly-once processing for $350M+ in distributed financial postings across 150+ global vendors
- **99.9% stability** — Primary Incident Commander for 300+ mission-critical escalations annually governing $350M+ in annual financial volumes across 150+ global vendors
- **10+ years** — Core contributor to SAP's standard TM Charge Calculation Engine, resolving thousands of scenario permutations via BAdI extensibility contracts and single-entry-point execution — the direct precedent for E2A's base-class thesis
- **Monolith-to-microservice precedent** — Directed the BOPF-to-RAP migration of legacy TM/Settlement cores to SAP RAP with OData V4 APIs, 100% operational continuity — the structural transition underpinning E2A's base-class thesis

---

## 🏛️ Architectural Philosophy — Correct by Design
 
> *Idempotency and Reconciliation are **business features**, and not just technical safeguards.*
 
At SAP TM scale, financial integrity was achieved not by adding defensive code, but by making incorrect states architecturally impossible:
 
| SAP TM Mechanism | What It Enforces | Cloud-Native Equivalent |
|---|---|---|
| Line-Element Key | Deterministic 1:1 charge-to-settlement mapping — revised amounts route as valid updates, never duplicates | Redis `SETNX` idempotency key · DynamoDB conditional write · deterministic outbox commit |
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

## ☁️ Framework-to-Cloud Landing Zone — The Structural Isomorphism

The E2A/A2C/P0/G2C abstract class hierarchy maps **directly and completely** onto a cloud-native landing zone. This is not metaphor — the structural relationships are isomorphic. Every framework constraint has a named cloud counterpart enforced at the infrastructure level.

| Framework Concept | Cloud-Native Equivalent | Enforcement Mechanism |
|-------------------|------------------------|-----------------------|
| **Abstract Class** | Landing Zone Account / VPC | AWS Control Tower Account Factory — every account derives from the same base blueprint |
| **Inheritance** | Environment Promotion (DEV → QA → PROD) | Terraform module inheritance — child modules extend root with environment overrides |
| **`_apply_policy()`** | Service Control Policy (SCP) + OPA Policy Gate | Runs before business logic; blocks non-compliant resource creation — same as SCP runs before any AWS API action |
| **`@abstractmethod`** | Required NFR Contract (Health Check, Observability) | ECS task definition enforces `/health` endpoint; deploy fails without it |
| **CriticAgent** | RAGAS CI/CD Gate + CloudWatch SLO Alarm | Deployment blocked if quality score < 0.85; auto-rollback triggered |
| **Private Method** | Private Subnet / Data Tier | Security Group: no ingress from public tier; `__llm_call()` = Bedrock VPC endpoint |
| **Public Entry Point** | API Gateway + ALB (single ingress) | SCP: deny direct VPC access; all traffic via Gateway |

> **The unified principle:** A class IS a landing zone account. A method IS a cloud component. Inheritance IS environment promotion. Abstract enforcement IS Service Control Policy.

> Full reference architecture (10 sections, complete SCP governance matrix, 7-phase provisioning lifecycle): **[Framework-to-Cloud Landing Zone Reference](https://github.com/subhamviky/e2a-framework/blob/main/docs/CLOUD_LANDING_ZONE.md)**
>
> E2A ships two execution profiles on this same isomorphism: **Agentic** (LLM-driven, LangGraph) and **Deterministic CQRS** (no LLM on the request path) — same propagation contract, same abstract-class Observability/Governance layer, different Tier 2 routing shape. CQRS profile reference: **[CQRS Cloud Landing Zone](https://github.com/subhamviky/e2a-framework/blob/main/docs/CQRS_CLOUD_LANDING_ZONE.md)** · **[CQRS Implementation Playbook](https://github.com/subhamviky/e2a-framework/blob/main/docs/CQRS_IMPLEMENTATION_PLAYBOOK.md)**
---

---

## Expertise Framework

<p align="center">
  <img src="https://raw.githubusercontent.com/subhamviky/subhamviky/main/expertise_framework_cloud_native.svg" width="520" alt="Expertise Differentiator Framework"/>
</p>

---
## 📐 Framework Documentation

| Document | Description |
|---|---|
| [G2C Phase Trigger Decision Reference](https://github.com/subhamviky/a2c-framework/blob/main/a2c-framework/docs/G2C_Phase_Trigger_Decision_Reference.pdf) | Phase-trigger matrix for E2A · A2C · P0 · G2C — monorepo & multi-repo scenarios |

## Tech Stack

*The multi-cloud, multi-runtime footprint the framework is designed to target — not a personal tool-by-tool specialization claim.*

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

*Open to: Principal Platform Architect · Principal Systems Engineer · Core AI/Agentic Infrastructure Roles across Microsoft Azure Core · Google Cloud · Amazon Web Services.
Topics: Agentic AI platform design · Enterprise-to-Cloud migration · RAG at scale · Cloud-native financial systems.*

---

<sub style="font-size: 0.8em; color: gray;">
<b>Structural Attribution:</b> The 6-pillar organizational structure utilized in this framework (Responsible AI, Data Management, Model Hub, Orchestration, Observability, and GenAI Ops) is a structural mapping inspired by the AWS AI Ecosystem visualization by Prashant Rathi.  
<b>Legal Disclaimer:</b> All trademarks, service marks, and logos (AWS, GCP, Azure, Meta Llama, SAP) are the property of their respective owners. Their use is for educational and architectural reference purposes only and does not imply official endorsement by the trademark holders.  
<b>Ecosystem Note:</b> Certain components referenced (e.g., Pinecone, LangGraph, Lakera) are third-party partner technologies and are not native managed services of AWS, Google Cloud, or Microsoft Azure.
</sub>
