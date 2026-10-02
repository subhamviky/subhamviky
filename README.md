# Hi, I'm Subham Gupta 👋

**Staff Architect · I make AI agents safe to write to financial systems of record.**
13+ years building ledger-grade distributed systems at SAP scale.
Now applying the same core invariants — idempotency, sagas, transactional outbox, scoped credentials,
and evaluation gates — to agentic AI.

**Start here**
- 📄 **Whitepaper:** [Frontier AI concept → distributed-systems pattern → cloud service → control plane](https://github.com/subhamviky/e2a-framework/blob/main/docs/e2a_architecture_framework_whitepaper.md)
- 🗺️ **Pattern map:** [E2A — Harmonizing the Frontier](https://github.com/subhamviky/e2a-framework/blob/main/docs/enterprise_architecture_ai_pattern_mapping_matrix.md)
- ✍️ **Core Thesis:** [Why agentic AI makes application modernization mandatory](https://www.linkedin.com/pulse/why-agentic-ai-makes-application-modernization-mandatory-subham-gupta-rahne/)
- 🧪 **Eval Rig:** [Context Harness & Evals: What AI SDLC Can Borrow from Automotive HIL/SIL Testing](https://www.linkedin.com/pulse/context-harness-evals-what-ai-assisted-sdlc-can-borrow-subham-gupta-fplfc/)

> **Thesis.** An LLM cannot safely navigate tightly coupled legacy state machines. It requires clean,
> deterministic boundaries — so agentic AI makes application-level modernization structurally mandatory.
> E2A, A2C, P0, and G2C enforce those boundaries in code, not in prompts.

## The Mental Model
*Same pattern set, different runtime.* OData → FastAPI · BDEF → `BaseAgent` · CDS entity → `AgentState`.

![SAP RAP to Python agentic stack](https://raw.githubusercontent.com/subhamviky/order-to-cash-agentic-ai/main/docs/images/sap-to-agentic-mental-model.svg)

## Correct by Design
Financial integrity at enterprise scale stems from making invalid states architecturally impossible,
not from defensive prompt engineering. Idempotency, lineage, and reconciliation are business features.

| Enterprise Mechanism | What It Enforces | Cloud-Native / Agentic Equivalent |
|---|---|---|
| Deterministic charge-to-settlement key | Revisions are updates, never duplicates | Redis `SETNX` fast path + DB unique constraint · DynamoDB conditional write |
| "Completely invoiced" business gate | No ledger posting before status confirmed | `SettlementState.COMPLETED` as the only pre-condition for a ledger write |
| Dispute workflow | Charge-delta mediation as a business process | Policy-grounded reasoning agent + critic groundedness gate |
| Write-once finance ledger | Immutable source of truth | Double-entry unique index; reversal-only corrections |

## The Framework Family
A cohesive architectural methodology designed to translate high-level enterprise governance, security, and NFRs into deterministic code boundaries.

| Framework | Architecture Scope | Core Invariant Enforced | Repository |
| :--- | :--- | :--- | :--- |
| **E2A** (Enterprise-to-Agentic) | Runtime Governance | Invariant lifecycle execution via single entry point; pre-compute validation gates | [e2a-framework](https://github.com/subhamviky/e2a-framework) |
| **A2C** (Architecture-to-Code) | Modernization Engine | Injects operational NFRs, schemas, and CI/CD policies directly at code generation | [a2c-framework](https://github.com/subhamviky/a2c-framework) |
| **P0** (Phase Zero) | Ingress & Scaffolding | Zero-drift workspace bootstrap with pre-wired telemetry, auth, and contract harnesses | in [a2c-framework](https://github.com/subhamviky/a2c-framework) |
| **G2C** (Generate-to-Class) | Model Compiler | Compiles declarative architecture specifications into typed, contract-bound classes | in [a2c-framework](https://github.com/subhamviky/a2c-framework) |

## Reference Implementations
Concrete runtimes proving the framework's deterministic boundaries and enterprise invariants across heterogeneous stacks:

* **[order-to-cash-agentic-ai](https://github.com/subhamviky/order-to-cash-agentic-ai):** Multi-agent coordination (Python, LangGraph, Bedrock, OpenSearch) featuring 5-agent bounded context isolation, hybrid RAG retrieval, and critic faithfulness verification.
* **[aws-reconciliation-engine](https://github.com/subhamviky/aws-reconciliation-engine):** Serverless reconciliation system (Python, Lambda, DynamoDB, SQS) enforcing two-layer idempotency gates, atomic state updates, and dead-letter queue escalation.
* **[financial-settlement-platform](https://github.com/subhamviky/financial-settlement-platform):** Distributed settlement engine (Java 21, Spring Boot 3, Kafka, PostgreSQL) validating Saga orchestration with reverse compensation, transactional outbox CDC, and double-entry immutable ledgers.

*Framework abstractions are cloud-agnostic by design. Reference implementations demonstrate distributed patterns across serverless and open-source stacks, with Azure and GCP landing-zone equivalents documented in the pattern map.*

## Landing-Zone Isomorphism
| Framework Concept | Cloud Equivalent | Enforced By |
|---|---|---|
| Abstract class | Landing-zone account / VPC | Control Tower account factory / Azure Landing Zone |
| `_apply_policy()` | SCP + policy gate | Runs before business logic execution |
| `@abstractmethod` NFR | Required NFR contract | Container task definition fails without `/health` |
| CriticAgent | Evaluation gate in CI/CD + SLO alarm | Deployment or completion blocked below threshold |
| Public entry point | API Gateway + ALB | Single ingress boundary |
→ [Full reference](https://github.com/subhamviky/e2a-framework/blob/main/docs/CLOUD_LANDING_ZONE.md)

## What I've Delivered at Enterprise Scale
- **35 → 7 min** month-end batch runtime (≈80% reduction) across 10,000+ daily freight documents with zero business disruption.
- **Ledger-Grade Integrity:** Designed exactly-once posting invariants and automated reconciliation engines across high-volume financial settlement batches.
- **Mission-Critical Production Ownership:** Lead escalation architect for complex enterprise incidents, resolving tier-1 production blockers across global deployments.

## Open To
Principal / Staff platform-architecture roles in agentic AI infrastructure & strategic customer workloads — Microsoft Azure, Google Cloud, AWS.

[LinkedIn](https://www.linkedin.com/in/subham-gupta-0a05a058) · [Email](mailto:subhamviky@gmail.com)

---
*Trademarks: AWS, GCP, Azure, Meta Llama, SAP belong to their owners; used for architectural reference only. Third-party technologies named here (LangGraph, Pinecone, Lakera) are non-affiliated open-source or commercial products.*
