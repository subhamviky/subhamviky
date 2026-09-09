# Hi, I'm Subham Gupta 👋

**Principal Enterprise Architect & Systems Engineering Leader**  
*Enterprise Cloud Modernization & Customer Advisory • AI-Assisted SDLC Platforms • Core Distributed Systems ($350M+ Scale)*

Bengaluru, India | [LinkedIn](https://www.linkedin.com/in/subham-gupta-0a05a058) | [Email](mailto:subhamviky@gmail.com)

---

### 🏛️ The Core Thesis: Modernization & Agentic AI Are Structurally Inseparable

Enterprise cloud modernization and agentic AI are not parallel initiatives — **agentic AI makes clean-core modernization mandatory**. 

An LLM or autonomous agent cannot safely navigate tightly coupled legacy monoliths or inconsistent state machines without catastrophic hallucination and reasoning drift. Autonomous workflows demand deterministic API boundaries, strict idempotency, and contract-first isolation. The **E2A / A2C / P0 / G2C** stack was engineered specifically to enforce those architectural boundaries. 

→ **[Read the Full Architectural Argument on LinkedIn Pulse](https://www.linkedin.com/pulse/why-agentic-ai-makes-application-modernization-mandatory-subham-gupta-rahne/)**

![AWS](https://img.shields.io/badge/AWS-Bedrock_Lambda_SQS_DynamoDB-FF9900?style=flat&logo=amazonaws&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-Vertex_AI_Cloud_Run-4285F4?style=flat&logo=googlecloud&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-AI_Foundry-0078D4?style=flat&logo=microsoftazure&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=flat&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java_21-Spring_Boot_3.x-ED8B00?style=flat&logo=spring&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-IaC-7B42BC?style=flat&logo=terraform&logoColor=white)

---

## 🧭 Three Interlocking Architectural Personas

My work operates across three complementary dimensions of modern enterprise systems engineering:
```text
┌─────────────────────────────────────────────────────────────────────────────┐
│ 1. CUSTOMER ADVISORY & CLOUD MODERNIZATION                                  │
│    • 150+ Enterprise Accounts: Net-new discovery & clean-core migration     │
│    • Incident Command: 300+ critical escalations de-escalated (99.9% SLO)   │
│    • Financial De-risking: $350M+ transactional volume safeguarded          │
└──────────────────────────────────────┬──────────────────────────────────────┘
                                       │
                    Informs & Validates│Directs Governance
                                       ▼
┌─────────────────────────────────────────────────────────────────────────────┐
│ 2. AI-ASSISTED SDLC & DEVEX PLATFORMS                                       │
│    • P0: Zero-day project bootstrap & standardized workspace scaffolding    │
│    • G2C: Spec-driven generate-to-class meta-generation (zero boilerplate)  │
│    • E2A / A2C: Model Context Protocol (MCP) multi-agent governance         │
└──────────────────────────────────────┬──────────────────────────────────────┘
                                       │
                          Enforces Invariants
                                       ▼
┌─────────────────────────────────────────────────────────────────────────────┐
│ 3. CORE DISTRIBUTED SYSTEMS & PLATFORM INTEGRITY                            │
│    • High-throughput calculation engines (10+ year production lifecycle)    │
│    • 80% runtime reduction (35m → 7m) via asynchronous event pipelines     │
│    • Correct-by-Design: Distributed idempotency, Sagas & outbox guarantees  │
└─────────────────────────────────────────────────────────────────────────────┘
```


---

## ⚙️ How I Work: Architectural Orchestration & Shift-Left Invariants

I specialize in **systemic thinking and shift-left design**: auditing existing and target-state enterprise landscapes to surface latent bottlenecks, model trade-offs, and codify invariants into paved paths that squads can build upon with confidence.

* **At the HLD Layer:** Defining target topology, cloud interconnects, domain boundaries, NFR governance, and cost-to-serve boundaries.
* **At the LLD Layer:** Establishing contract-first schemas, class contracts, deterministic state transitions, encapsulation boundaries, and single-entry-point invariants before engineering execution begins.
* **In Collaborative Delivery:** Partnering with cross-functional engineering teams, domain specialists, and AI tooling inside clearly bounded interface contracts. I maintain end-to-end technical accountability for the delivered outcome — personally authoring core base abstractions, conducting deep architecture reviews, and validating runtime behavior against production invariants.

---

## 🏛️ What I've Proven at Enterprise Scale (SAP Labs India)

* **80% Runtime Compression:** Re-engineered synchronous monolithic invoice-calculation engines into decoupled, asynchronous event-driven pipelines (35 min → 7 min) across 10,000+ daily freight documents with zero business disruption.
* **$350M+ Financial Volume De-risked:** Architected distributed idempotency keys, transactional outbox commits, and reverse-compensation Saga orchestrators across 150+ global enterprise accounts, eliminating double-spend and ledger drift.
* **Crisis Command & 99.9% Availability:** Served as Lead Technical Authority and Incident Commander for 300+ mission-critical customer escalations annually; translating outages into transparent post-mortems and actionable SRE error-budget policies.
* **Clean-Core Modernization Precedent:** Directed incremental modernization of legacy ERP/settlement cores to modular microservices (SAP RAP) with REST/OData V4 APIs, maintaining 100% operational continuity.

---

## 🧩 Framework Authorship — Paved Paths for the AI-Assisted SDLC

The framework stack represents a formalized architectural standard bridging mission-critical systems reliability with AI-assisted software delivery:

### 1. E2A Framework (Enterprise-to-Agentic Governance)
**[github.com/subhamviky/e2a-framework](https://github.com/subhamviky/e2a-framework)**  
A multi-cloud architectural standard mapping legacy transaction-integrity patterns to agentic systems.
* **Decoupled Orchestration:** Standardizes abstract base class contracts (`BaseWorkflow`, `BaseAgent`, `BaseRAGPipeline`), isolating enterprise logic from changing model SDKs.
* **Multi-Cloud Vendor Portability:** Executes the identical agent subclass across **AWS Bedrock, GCP Vertex AI, and Azure AI Foundry** via configuration switches — requiring zero execution-layer code changes.
* **Deterministic Write Guarantees:** Enforces exactly-once write semantics via deterministic outbox patterns, generalizing ledger posting guarantees to distributed AI agent tool calls.

### 2. A2C Framework (Architecture-to-Code)
**[github.com/subhamviky/a2c-framework](https://github.com/subhamviky/a2c-framework)**  
An AI-governed developer platform framework enforcing non-functional requirements (NFRs) at code generation time.
* **Correct-by-Design Generation:** Mitigates "NFR Amnesia" by moving constraints from loose prompts into strict base-class compiler policies and automated AST validation.
* **Quality & Faithfulness Gates:** Injects idempotency annotations, circuit breakers, and structured JSON logging by construction, validating outputs via `CodeCriticAgent` (RAGAS threshold ≥ 0.85).

### 3. P0 Framework (Phase-Zero Developer Bootstrap)
**Module within [github.com/subhamviky/a2c-framework](https://github.com/subhamviky/a2c-framework)**  
Automates workspace blueprints and greenfield repository scaffolding before feature implementation begins.
* **Single `bootstrap()` Entry Point:** Generates project dependencies (`pyproject.toml`, `pom.xml`), Dockerfiles, CI/CD pipelines, and configuration trees in under 10 seconds.
* **Enforced Consistency:** Bakes architectural invariants into repository scaffolding so developer squads onboard instantly into a secure, pre-configured paved path.

### 4. G2C Framework (Generate-to-Class Meta-Generation)
**Module within [github.com/subhamviky/a2c-framework](https://github.com/subhamviky/a2c-framework)**  
Spec-driven meta-generation substrate compiling OpenAPI/OData schemas into type-safe, production-ready backend microservices (FastAPI / Spring Boot).
* Eliminates repetitive CRUD boilerplate, automated boundary validation, and schema synchronization friction across squads.

---

## 📦 Architectural Reference Runtimes & Spikes

Validated reference implementations stress-testing framework invariants against realistic workloads:

* **[Order-to-Cash Agentic Platform](https://github.com/subhamviky/order-to-cash-agentic-ai):** 5-agent orchestration prototype (Python, FastAPI, LangGraph, Bedrock/Vertex AI, Terraform) featuring dynamic intent routing and codebase RAG; benchmarked with RAGAS faithfulness thresholds (≥ 0.85).
* **[Cloud-Native Financial Settlement Platform](https://github.com/subhamviky/financial-settlement-platform):** High-concurrency Java 21 / Spring Boot 3.x / Kafka runtime with a 7-state reverse-compensation Saga orchestrator and Redis-backed idempotency under split-brain simulations.
* **[Serverless Payment Reconciliation Engine](https://github.com/subhamviky/aws-reconciliation-engine):** Event-driven serverless pipeline on AWS Lambda, SQS FIFO, and DynamoDB conditional writes validating two-layer distributed idempotency.

---

## 🏛️ Architectural Philosophy: Correct by Design

> *Idempotency, reconciliation, and auditability are **business capabilities**, not after-the-fact defensive patches.*

| Enterprise ERP Mechanism | Distributed Cloud Equivalent | Architectural Invariant Enforced |
|---|---|---|
| **Line-Element Key** | Redis `SETNX` / DynamoDB Conditional Write | Exactly-once distributed write semantics; eliminates double-execution |
| **"Completely Invoiced" Gate** | `SettlementState.COMPLETED` Pre-condition | Ledger posting blocked until business contract verified |
| **Dispute Management** | Agentic Reasoning & Reconciliation Loop | Discrepancy mediation as an asynchronous, audited first-class workflow |
| **FI Posting Immutability** | Write-once append-only transactional log | Reversal-only correction patterns; zero destructive updates |

---

## ☁️ Framework-to-Cloud Landing Zone Mapping

The E2A/A2C class hierarchy maps isomorphically onto cloud-native infrastructure concepts:

| Framework Concept | Cloud-Native Equivalent | Enforcement Mechanism |
|---|---|---|
| **Abstract Base Class** | Landing Zone Account / VPC Blueprint | AWS Control Tower / GCP Landing Zone factory |
| **Class Inheritance** | Environment Promotion (DEV → STAGING → PROD) | Root Terraform module parameterized per environment |
| **`_apply_policy()`** | Service Control Policy (SCP) / OPA Gate | Blocks non-compliant resource provisioning before deployment |
| **`@abstractmethod`** | Required NFR Contract (Health / Metrics) | Container orchestration checks; container rejected without contract |
| **CriticAgent** | CI/CD Quality Gate & SLO Budget | Automated deployment blocked if evaluation score drops below threshold |

---

## Connect & Explore

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Subham_Gupta-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/subham-gupta-0a05a058)
[![Email](https://img.shields.io/badge/Email-subhamviky@gmail.com-D14836?style=flat&logo=gmail&logoColor=white)](mailto:subhamviky@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-subhamviky-181717?style=flat&logo=github&logoColor=white)](https://github.com/subhamviky)

*Targeting Principal Customer Solutions Architect, AI-Assisted SDLC Platform Architect, and Staff/Principal Distributed Systems roles at hyperscale technology organizations.*
