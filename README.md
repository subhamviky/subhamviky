# Hi, I'm Subham Gupta 👋

**Staff Architect & AI Architecture Framework Author | Enterprise-to-Cloud & Agentic AI Architecture**

*Translating 13+ years of enterprise transaction integrity, distributed-systems discipline, and cloud-native architecture into governed Agentic AI systems.*

> **Status:** Solo-authored architecture R&D, actively evolving. Architectural spikes and reference runtimes below exercise the framework ideas against real, non-production workloads unless a repository explicitly states otherwise.

## Core Thesis

Enterprise modernization and Agentic AI are connected engineering problems.

Agentic AI increases the architectural pressure for clean application contracts, deterministic transactional boundaries, explicit state, governed tools, observable execution paths, and reliable recovery. The runtime can change substantially while many of the core engineering invariants remain recognizable.

> **Same enterprise engineering invariants. Different runtime. New implementation mechanisms.**

A second principle follows from this:

> **Probabilistic intelligence may propose an action. Deterministic enterprise controls must authorize, execute, and confirm material outcomes.**

---

## How the Framework Family Emerged

The framework family did not begin as a top-down attempt to invent abstractions for Agentic AI.

It emerged through **architectural spikes** I built to explore and validate how enterprise-grade reliability, transaction integrity, integration, observability, and failure-management principles translate into cloud-native and Agentic AI runtimes.

Those spikes repeatedly exposed structural correspondence across runtime generations. The implementation technologies changed, but responsibilities such as contracts, idempotency, execution context, policy, observability, reconciliation, failure isolation, and deterministic systems of record remained important.

### Evolution of the architecture R&D

```text
Enterprise Transactional & Distributed-Systems Experience
                         |
                         v
              Architectural Spikes
                         |
                         v
       Discovery: stable engineering invariants
          across changing runtime models
                         |
                         v
                        E2A
            Enterprise-to-Agentic runtime
                         |
              +----------+----------+
              |                     |
              v                     v
             A2C                   P0
    governed generation     foundation/scaffolding
              |                     |
              +----------+----------+
                         |
                         v
                        G2C
             contract/class synthesis
                         |
                         v
               Further E2A evolution
                    /           \
                   v             v
        Deterministic CQRS     AI-DLC
             Profile        Assurance Lifecycle
```

Chronology and runtime composition are deliberately different views. **E2A emerged first historically**, while **P0 and G2C can execute earlier in a solution lifecycle** because they prepare foundations and contracts before runtime execution.

The architectural spikes therefore have two roles:

- **Discovery spikes** helped reveal and test the cross-runtime invariants that led to E2A.
- **Reference runtimes** exercise, challenge, and refine formalized framework patterns after those patterns exist.

---

## Architectural Mental Model — Structural Correspondence Across Runtimes

My core mental model comes from comparing recurring architectural responsibilities across enterprise applications, cloud-native distributed systems, and Agentic AI.

The important claim is **not literal technology equivalence**. An OData service is not a FastAPI router, and a Behavior Definition is not literally a `BaseAgent`. The useful observation is that they can occupy comparable architectural responsibilities: contract definition, exposure, execution, policy, observability, and lifecycle control.

```text
Enterprise Runtime        Cloud-Native Runtime       Agentic Runtime
------------------        --------------------       ---------------
Domain contract       ->  API/service contract   ->  Agent/tool contract
Business operation    ->  Service/command        ->  Governed tool/action
Request context       ->  Trace/request state    ->  Workflow/agent state
Validation            ->  Policy/validator       ->  Evaluation + policy gate
Recovery              ->  Retry/saga/outbox      ->  Retry/fallback/compensation
Observability         ->  Logs/metrics/traces    ->  + tokens/evals/tool traces
System authority      ->  Database / SoR         ->  Deterministic SoR remains authoritative
```

This cross-runtime correspondence became the conceptual basis for **E2A structural isomorphism**.

---

## Architecture R&D — Framework Family

The frameworks are different lifecycle and control layers of one evolving architecture, not six independent abstractions.

### Current architectural composition

```text
BUSINESS / ARCHITECTURE INTENT
             |
             v
            P0
     Context + Scaffolding
             |
             v
            G2C
       Contract Synthesis
             |
       +-----+-----+
       |           |
       v           v
      A2C         E2A
 Generation   Runtime Execution
       |           |
       +-----+-----+
             |
             v
           AI-DLC
    Evaluation / Assurance

Deterministic CQRS applies where transactional
semantics require stronger correctness guarantees.
```

| Framework / profile | Primary responsibility | Intended outcome |
|---|---|---|
| **E2A** | Governed runtime for agents, RAG, tools, enterprise integration, and execution context | Auditable Agentic AI execution |
| **A2C** | NFR-aware generation of code, tests, configuration, IaC, and delivery artifacts | Consistent engineering artifacts |
| **P0** | Project, runtime, configuration, and platform scaffolding | Repeatable foundation |
| **G2C** | Governed contract synthesis; Generate-to-Class is the initial concrete realization | Implementation-ready contracts and class structures |
| **AI-DLC** | Evaluation and assurance across generated artifacts and runtime behavior | Evidence of quality, safety, and fitness |
| **Deterministic CQRS Profile** | Commands, queries, idempotency, outbox, concurrency, and compensation | Safe state mutation and scalable reads |

### E2A — Enterprise-to-Agentic

🔗 [github.com/subhamviky/e2a-framework](https://github.com/subhamviky/e2a-framework)

E2A is the runtime and governance core of the family. It explores:

- Stable public lifecycle entry points
- Protected extension hooks for bounded specialization
- Explicit request-scoped execution context
- Governed RAG and knowledge boundaries
- Governed REST/MCP tool execution
- Evaluation before trust
- Reliability, observability, and cost controls
- Deterministic confirmation before material side effects are declared successful

**Multi-cloud portability:** E2A is designed around stable contracts and provider adapters. Agent implementations written exclusively against supported common contracts can remain largely provider-independent, while provider adapters, configuration, model capabilities, and cloud-specific infrastructure remain intentionally isolated.

### A2C — Architecture-to-Code

🔗 [github.com/subhamviky/a2c-framework](https://github.com/subhamviky/a2c-framework)

A2C explores **Correct-by-Design generation**: moving architectural and NFR constraints from loose prompt instructions into governed generation policies.

Representative generated artifacts include application code, tests, configuration, Infrastructure as Code, CI/CD definitions, and policy-aware templates.

### P0 — Project Bootstrap / Phase Zero

P0 separates project and platform foundation from later business-code generation.

Current concepts include build/dependency metadata, directory structure, environment configuration, README/license scaffolding, container artifacts, developer automation, runtime/platform selection, and baseline quality/security integration points.

### G2C — Governed Contract Synthesis / Generate-to-Class

G2C translates architectural intent into implementation-ready contracts. **Generate-to-Class** is the initial concrete realization, where E2A-governed generator agents produce framework and domain class structures.

The broader direction includes class/interface, workflow, data, API/event, NFR, and test contracts.

### AI-DLC — Evaluation & Assurance Lifecycle

AI-DLC is a cross-cutting lifecycle spanning contract synthesis, generation, runtime execution, and production feedback. It covers static policy checks, deterministic tests, AI evaluations, integration verification, runtime reliability/cost evaluation, and business-outcome feedback.

### Deterministic CQRS Profile

The CQRS profile extends E2A where Agentic workflows interact with material transactional state. It keeps command correctness, scalable reads, idempotency, concurrency, transactional outbox behavior, events, and compensation inside deterministic control boundaries.

---

## 🎯 Vision — From Field Patterns to Reusable Platform Capabilities

The long-term direction is to turn recurring enterprise AI engineering friction into reusable platform capabilities.

| Recurring need | Framework response | Potential productization form |
|---|---|---|
| Governed Agentic AI runtime | E2A | Agent execution / governance control plane |
| NFR-aware artifact generation | A2C | Developer productivity / paved-path tooling |
| Repeatable project foundation | P0 | Project bootstrap tooling |
| Architecture-to-contract synthesis | G2C | Architect productivity tooling |
| Continuous evaluation and assurance | AI-DLC | AI quality and release-gating platform |
| Deterministic enterprise mutation paths | CQRS profile | Transactional integration patterns |

The objective is not abstraction for its own sake. A reusable platform is justified when multiple domains repeatedly need the same contracts, guardrails, observability, and operational controls.

The framework family is vendor-neutral by design. Reference mappings span **AWS Bedrock, Google Cloud / Vertex AI, Microsoft Azure AI, and standalone/open-model runtimes**, with provider-specific capabilities isolated behind adapters rather than assumed to be equivalent.

---

## 🌐 Live Reference Landscape — Finance Investigation on Google Cloud (free tier)

🔗 [enterprise-finance-genai-assistant](https://github.com/subhamviky/enterprise-finance-genai-assistant)

The three reference runtimes below, plus a new GenAI application, run together as one landscape on **real Google Cloud, inside the free tier** (Cloud Run scaled to zero, Firestore, Pub/Sub, a PostgreSQL ledger on an Always Free VM, Gemini's free tier). The assistant investigates why a payment is unmatched or a settlement is flagged, **proposes** a write-off within policy, and the ledger posts it **only after a second person approves**, exactly once. That is the second principle above, running against real infrastructure.

| System | Repository |
|---|---|
| GenAI assistant (investigate, propose, four-eyes approval) | [enterprise-finance-genai-assistant](https://github.com/subhamviky/enterprise-finance-genai-assistant) |
| Settlement ledger and audit service | [financial-settlement-platform](https://github.com/subhamviky/financial-settlement-platform) |
| Bank-line reconciliation | [payment-reconciliation-engine](https://github.com/subhamviky/payment-reconciliation-engine) |
| Order-to-cash assistant | [order-to-cash-agentic-ai](https://github.com/subhamviky/order-to-cash-agentic-ai) |

**What was measured (25 November 2026, synthetic data, one author):**

- An end-to-end scenario across the five deployed services passed in about 125 seconds: order, event, audit flag, short payment, cited explanation, proposal, refusal of the requester, approval by a second person, one posting to a balanced ledger, replays with no second posting, an injection refused, another tenant reading nothing. Billing for the project stayed at 0.00.
- Against the live model (`gemini-3.5-flash-lite`, free tier) the 53 golden cases scored **0.943** (mean), up from 0.855 after two fixes that only the live run could find, and all nine red-team cases passed. The report states what that score does not show.
- The first deployment found real problems that the emulator-based tests had not (a password newline between PostgreSQL and Cloud Run, an identity-token issuer spelled two ways, JSON wrapped in a markdown fence ending a workflow, a reworded model reason that could have made a second postable proposal, and others). Each has a cause, a fix and a test in the repositories.

> **Evidence discipline:** a free-tier reference landscape with synthetic data. It shows the architecture running and being measured; it is not a production claim.

---

## 📦 Architectural Spikes & Reference Runtimes

These projects are architecture R&D evidence. Some contributed to discovering the framework principles; later/evolved implementations are used to exercise and refine formal contracts.

### Order-to-Cash Agentic AI Platform

🔗 [order-to-cash-agentic-ai](https://github.com/subhamviky/order-to-cash-agentic-ai)

Python · FastAPI · E2A · Cloud Run · Firestore · Pub/Sub · Terraform (the original LangGraph, Bedrock and OpenSearch spike is kept on a branch)

**Patterns explored:** governed multi-agent workflow with human approval, hybrid retrieval, policy controls, asynchronous events, idempotency and crash recovery, calls to real systems of record with typed outcomes. Runs on the Google Cloud free tier in the live landscape above.

### Cloud-Native Financial Settlement Platform

🔗 [financial-settlement-platform](https://github.com/subhamviky/financial-settlement-platform)

Java 21 · Spring Boot · PostgreSQL · transactional outbox · a Python E2A audit service · Azure and Google Cloud (the original Kafka, Redis and Spring AI spike is kept on a branch)

**Patterns explored:** transactional saga orchestration, compensation, idempotent commands, an event feed with a checked contract, ledger adjustments posted once, and financial-integrity controls. Runs on the Google Cloud free tier in the live landscape above.

### Cloud-Native Payment Reconciliation Engine

🔗 [payment-reconciliation-engine](https://github.com/subhamviky/payment-reconciliation-engine) (renamed from `aws-reconciliation-engine`; old links redirect)

Python · FastAPI · E2A · DSA · AWS Lambda, SQS and DynamoDB, or Cloud Run, Pub/Sub and Firestore · Terraform

**Patterns explored:** asynchronous reconciliation, one transaction per match, duplicate and ambiguity handling, dead-letter replay, an agent that proposes while rules decide. The same service runs on AWS or on the Google Cloud free tier by configuration.

### Capability-Oriented DSA (Enterprise Lens)

🔗 [capability-oriented-dsa](https://github.com/subhamviky/capability-oriented-dsa)

Python · zero runtime dependencies · mypy strict · GitHub Actions

**Patterns explored:** one governed entry point, declared operations instead of branching, ordered configuration resolution, request identifiers (`correlation_id`, `tenant_id`, `idempotency_key`) and honest structured results, applied to classical data structures and algorithms as a bridge for enterprise developers.

> **Evidence discipline:** Reference implementations demonstrate architectural feasibility and implementation patterns. They are not presented as production validation unless a specific repository provides explicit production evidence.

---

## Enterprise Production Engineering — Where the Invariants Came From

My framework thinking is grounded in enterprise transactional and distributed-systems work, particularly financial settlement and transportation-management domains.

The important connection is not that cloud and Agentic AI systems should copy SAP implementations. It is that production experience with transactional consistency, zero-loss processing, idempotency, integration boundaries, auditability, failure recovery, and major NFRs provides a strong set of invariants to test against new runtime models.

This is what the architectural spikes were intended to challenge: **which principles survive when the runtime changes?**

The answer became the foundation of E2A.

---

## 🏛️ Architectural Philosophy — Correct by Design

**Idempotency and reconciliation can be business features, not merely technical safeguards.**

For financial and settlement-oriented workflows, the correct control layer depends on the domain.

A useful calibration asks:

1. **Input mutability** — can amounts or quantities legitimately change mid-flight?
2. **Output ambiguity** — can identical values represent different business meaning?
3. **Audit exposure** — what is the consequence of an incorrect posting?

Higher ambiguity and exposure justify stronger business-layer controls such as explicit idempotency, sagas, reconciliation, and ledger invariants. Lower-risk flows may be adequately protected by simpler infrastructure controls.

The broader principle is:

> **Make invalid business states difficult or impossible by architecture before relying on exception handling.**

---

## NFR-First Engineering

A representative production-oriented sequence used across the framework thinking is:

1. **Scaffold** — establish structure and engineering standards
2. **Infrastructure** — establish a reproducible execution substrate
3. **Observability** — make behavior measurable
4. **CI/CD** — automate engineering gates
5. **NFR controls** — reliability, security, policy, cost, and recovery
6. **Business logic** — build domain capability on the governed foundation

This is a reference sequence, not a requirement that every use case implement every layer. **Why not simpler?** remains an explicit architectural test.

---

## Claim & Evidence Discipline

I distinguish these categories across the repositories:

| Classification | Meaning |
|---|---|
| **Framework invariant** | Architectural rule the framework intends to enforce |
| **Implemented capability** | Present in concrete code |
| **Architectural spike** | Experiment used to discover or challenge an architectural hypothesis |
| **Reference runtime** | Implementation used to exercise formalized framework patterns |
| **Recommended production pattern** | Guidance requiring contextual validation |
| **Directional design** | Extension or hypothesis still under architectural exploration |

This distinction is especially important for portability, reliability targets, multi-cloud mappings, and production-readiness claims.

---

## Why Not Simpler?

A framework is useful only when the problem justifies it.

- If conventional deterministic application logic solves the problem, use it.
- If a bounded RAG assistant is sufficient, do not introduce transactional orchestration.
- If a managed cloud capability directly satisfies a requirement, prefer it over unnecessary custom abstraction.
- Introduce E2A-level controls when probabilistic reasoning interacts with enterprise data, tools, regulated boundaries, material business actions, or systems of record.

---

## 📐 Framework Documentation

- [E2A Framework](https://github.com/subhamviky/e2a-framework)
- [A2C Framework](https://github.com/subhamviky/a2c-framework)
- [E2A Framework document](https://github.com/subhamviky/e2a-framework/blob/main/docs/Subham_Gupta_E2A_Enterprise_Agentic_Framework.pdf)
- [G2C Phase Trigger Decision Reference](https://github.com/subhamviky/a2c-framework/raw/main/docs/G2C_Phase_Trigger_Decision_Reference.pdf)

---

## Areas of Focus

- Enterprise and Agentic AI architecture
- Distributed systems and transactional correctness
- RAG and enterprise knowledge systems
- Agent orchestration and tool integration
- Multi-cloud architecture
- Developer platforms and paved paths
- Evaluation, observability, and AI production readiness
- Cloud-native modernization

---

## Design Principle

> **Same enterprise principles. Different runtime. Explicit boundaries. Measurable outcomes.**

---

### Attribution and trademarks

All trademarks, service marks, and logos referenced in architecture examples remain the property of their respective owners. References to AWS, Google Cloud, Microsoft Azure, SAP, Meta, LangGraph, and other technologies are for educational and architectural comparison and do not imply endorsement.
