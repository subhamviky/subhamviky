# Hi, I'm Subham Gupta 👋

**Principal Engineer, Systems Architect & AI Architecture Framework Author | Enterprise-to-Cloud & Agentic AI Architecture**

*Translating enterprise transaction integrity, distributed-systems discipline, and cloud-native architecture into governed agentic AI systems.*

> **Status:** Solo-authored architecture R&D, actively evolving. The reference runtimes below exercise framework patterns against real, non-production workloads unless explicitly stated otherwise.

## Core Thesis

Enterprise modernization and agentic AI are connected engineering problems.

The runtime may change from deterministic application services to probabilistic reasoning systems, but enterprise architecture still needs explicit contracts for identity, tenancy, state, reliability, auditability, cost, security, and physical side effects.

My framework family explores a simple principle:

> **Probabilistic intelligence may propose an action. Deterministic enterprise controls must authorize, execute, and confirm material outcomes.**

This is the bridge between the systems I have spent my career engineering and the agentic systems I am now exploring.

---

## Framework Family

The frameworks are designed as different lifecycle and control layers of one architecture rather than isolated projects.

```text
Enterprise Intent
      |
      v
  P0  ->  G2C  ->  E2A  ->  A2C
 foundation   contracts   runtime   artifacts
                  \          /
                   \        /
                    AI-DLC
              evaluation & assurance

Deterministic CQRS / transactional patterns protect material state changes
where business correctness requires deterministic guarantees.
```

| Framework / Profile | Primary responsibility | Intended outcome |
|---|---|---|
| **E2A** | Governed runtime for agents, RAG, tools, enterprise integration and execution context | Auditable agentic execution |
| **A2C** | NFR-aware generation of code, tests, configuration, IaC and delivery artifacts | Consistent engineering artifacts |
| **P0** | Project, runtime, configuration and platform scaffolding | Repeatable foundation |
| **G2C** | Governed contract synthesis; Generate-to-Class is the initial concrete realization | Implementation-ready contracts and class structures |
| **AI-DLC** | Evaluation and assurance across generated artifacts and runtime behavior | Evidence of quality, safety and fitness |
| **Deterministic CQRS Profile** | Commands, queries, idempotency, outbox, concurrency and compensation | Safe state mutation and scalable reads |

### How the layers relate

**P0 prepares the foundation.**  
**G2C turns architectural intent into explicit contracts.**  
**E2A governs runtime execution.**  
**A2C turns those contracts and policies into consistent engineering artifacts.**  
**AI-DLC evaluates whether the artifacts and runtime behavior satisfy the intended requirements.**

The deterministic CQRS profile is applied where enterprise state transitions require stronger consistency, idempotency, audit and recovery guarantees.

---

## E2A — Enterprise-to-Agentic

🔗 [github.com/subhamviky/e2a-framework](https://github.com/subhamviky/e2a-framework)

E2A is the runtime and governance core of the framework family. It formalizes familiar enterprise architecture responsibilities for an agentic runtime:

- Stable public lifecycle entry points
- Bounded specialization through protected extension hooks
- Governed internal mechanics
- Explicit, request-scoped execution context
- RAG and knowledge boundaries
- Governed REST/MCP tool execution
- Evaluation before release
- Observability and cost controls
- Deterministic confirmation for material physical side effects

### Architectural continuity

The framework grew from comparing recurring layers across enterprise and AI runtimes: data models, interface contracts, business services, callable operations, quality gates, exposure layers, events, observability, governance and deployment.

The goal is not to claim that SAP RAP, Spring Boot, FastAPI and LangGraph are identical. The goal is to make the recurring architectural responsibilities explicit so that proven engineering reasoning can transfer across runtimes.

### Multi-cloud model

E2A is designed around vendor-neutral contracts and provider adapters.

Agent implementations written exclusively against common E2A contracts can remain largely provider-independent. Provider adapters, deployment configuration, model capabilities and cloud-specific infrastructure may still require platform-specific implementation.

Reference mappings currently consider **AWS**, **Google Cloud**, **Microsoft Azure**, and standalone/open-model runtimes.

---

## A2C — Architecture-to-Code

🔗 [github.com/subhamviky/a2c-framework](https://github.com/subhamviky/a2c-framework)

A2C explores governed artifact generation with architectural policy applied before code reaches review.

The central idea is **Correct-by-Design generation**: engineering requirements such as idempotency, observability, retry behavior, circuit breaking, health checks, graceful shutdown, security and domain-specific policies should be represented as executable generation constraints rather than left entirely to prompt wording or late review.

A2C is intended to generate and validate artifacts such as:

- Application and service code
- Tests
- Configuration
- Infrastructure as Code
- CI/CD definitions
- Policy-aware templates

Generated artifacts remain reviewable engineering outputs, not an independent source of architectural truth.

---

## P0 — Project Bootstrap / Phase Zero

P0 is the scaffolding layer that prepares the project before application generation begins.

Current concepts include:

- Build and dependency metadata
- Repository and directory structure
- Environment examples and application configuration
- README and license scaffolding
- Container build artifacts
- Developer task automation
- Runtime and platform selection
- Baseline quality and security integration points

P0 exists because architecture starts before business logic. Repository structure, configuration precedence, identity, deployment assumptions and quality gates are architectural decisions too.

---

## G2C — Governed Contract Synthesis / Generate-to-Class

G2C translates architectural intent into implementation-ready contracts.

**Generate-to-Class** is its initial concrete realization: E2A-governed generator agents produce framework and domain class structures while remaining subject to the same architectural controls they generate.

The broader architectural direction includes synthesis of:

- Class and interface contracts
- Workflow contracts
- Data contracts
- API and event contracts
- NFR and test contracts

This creates a deliberate boundary between **what the architecture requires** and **how an implementation realizes it**.

---

## AI-DLC — Evaluation & Assurance Lifecycle

AI-DLC is best understood as a lifecycle spanning G2C, A2C and E2A rather than as a disconnected generator framework.

It focuses on evidence that architecture and AI behavior meet their intended contracts:

- Static contract and policy validation
- Deterministic unit/component verification
- Groundedness, safety, schema and task evaluation
- Integration testing across RAG, tools and systems of record
- Operational evaluation of latency, reliability and cost
- Business-outcome feedback

The objective is to shift evaluation left while keeping runtime evaluation and telemetry part of the production control loop.

---

## Architectural Philosophy — Correct by Design

The strongest lesson I carry from enterprise transactional systems is that important correctness properties should be architectural invariants, not merely error-handling conventions.

### Deterministic and probabilistic boundaries

| Deterministic responsibilities | Probabilistic responsibilities |
|---|---|
| Identity and authorization | Intent classification |
| Contract validation | Reasoning and planning |
| Concurrency and consistency | Retrieval and summarization |
| Idempotency | Tool recommendation |
| Transactional state mutation | Response generation |
| Event publication | Self-critique / evaluation signals |
| Audit and physical confirmation | Adaptive decision support |

A model may reason about what should happen. The enterprise control boundary determines whether it is allowed to happen and whether it actually happened.

### Financial-integrity calibration

Financial integrity controls belong at the business layer when domain complexity justifies them. Three useful questions are:

1. Can the input legitimately mutate mid-flight?
2. Can identical values carry different business meaning?
3. What is the audit or financial exposure of an incorrect posting?

High ambiguity and exposure justify domain-level controls such as explicit idempotency, sagas, reconciliation and ledger invariants. Lower-risk flows may be adequately protected by simpler infrastructure controls.

---

## NFR-First Engineering

The framework family treats non-functional requirements as executable architecture.

A representative delivery sequence is:

1. **Scaffold** — establish project structure and engineering standards
2. **Infrastructure** — make the execution environment reproducible
3. **Observability** — make behavior measurable before complexity grows
4. **CI/CD** — enforce automated delivery gates
5. **NFR controls** — reliability, security, policy and cost constraints
6. **Business logic** — build domain capability on the governed foundation

This sequence is not mandatory for every project. It expresses the principle that production controls should not be postponed until after application logic is complete.

---

## Framework Invariant vs Implementation Evidence

To keep the architecture honest, I distinguish these categories:

| Classification | Meaning |
|---|---|
| **Framework invariant** | A rule the architecture intends to enforce |
| **Implemented capability** | Present in a concrete code implementation |
| **Reference implementation** | A realization used to exercise a framework pattern |
| **Recommended production pattern** | Guidance that requires contextual validation |
| **Directional design** | An architectural extension or hypothesis still being explored |

This distinction is especially important when discussing multi-cloud portability, reliability targets and reference runtimes.

---

## Architectural Spikes & Reference Runtimes

These repositories are purpose-built engineering references used to exercise parts of the framework thinking. Active refactoring and alignment with the formal framework contracts may continue over time.

### Order-to-Cash Agentic AI Platform

🔗 [order-to-cash-agentic-ai](https://github.com/subhamviky/order-to-cash-agentic-ai)

Python / FastAPI / LangGraph / Amazon Bedrock / OpenSearch / Terraform / ECS-oriented reference implementation exploring multi-agent orchestration, RAG, policy controls, asynchronous processing, idempotency and failure handling.

### Cloud-Native Financial Settlement Platform

🔗 [financial-settlement-platform](https://github.com/subhamviky/financial-settlement-platform)

Java / Spring Boot / Spring AI / Kafka / Redis / PostgreSQL reference runtime exploring saga orchestration, idempotency and distributed financial-processing patterns.

### Cloud-Native Payment Reconciliation Engine

🔗 [aws-reconciliation-engine](https://github.com/subhamviky/aws-reconciliation-engine)

Python / FastAPI / AWS serverless-oriented spike exploring asynchronous reconciliation, idempotency, DLQ handling and agent routing.

> These projects demonstrate architectural feasibility and implementation patterns. They should not be interpreted as production validation unless a specific project explicitly provides that evidence.

---

## From Frameworks to Platform

My longer-term architectural interest is the productization of recurring enterprise AI engineering friction into reusable platform capabilities:

| Recurring need | Framework response | Potential reusable capability |
|---|---|---|
| Governed agent runtime | E2A | Agent execution control plane |
| NFR-aware artifact generation | A2C | Developer productivity / paved path |
| Consistent project foundation | P0 | Project bootstrap platform |
| Contract synthesis | G2C | Architecture productivity tooling |
| Evaluation and assurance | AI-DLC | Continuous AI quality and release gating |

The objective is not framework complexity for its own sake. The platform layer is justified when multiple domains repeatedly need the same guardrails, contracts and operational controls.

---

## Why Not Simpler?

A core design question is always: **does this use case need the framework capability?**

- If deterministic application logic solves the problem, use it.
- If a bounded retrieval assistant is sufficient, do not introduce transactional orchestration.
- If a managed cloud capability directly satisfies the requirement, prefer the managed capability over unnecessary abstraction.
- Introduce E2A-level controls when probabilistic reasoning interacts with enterprise data, tools, material business actions, regulated boundaries or systems of record.

---

## Documentation

- [E2A Framework repository](https://github.com/subhamviky/e2a-framework)
- [A2C Framework repository](https://github.com/subhamviky/a2c-framework)
- [E2A Framework document](https://github.com/subhamviky/e2a-framework/blob/main/docs/Subham_Gupta_E2A_Enterprise_Agentic_Framework.pdf)
- [G2C Phase Trigger Decision Reference](https://github.com/subhamviky/a2c-framework/raw/main/docs/G2C_Phase_Trigger_Decision_Reference.pdf)

---

## Areas of Focus

- Enterprise and agentic AI architecture
- Distributed systems and transactional correctness
- RAG and enterprise knowledge systems
- Agent orchestration and tool integration
- Multi-cloud architecture
- Developer platforms and paved paths
- Evaluation, observability and AI production readiness
- Cloud-native modernization

---

## Design Principle

> **Same enterprise principles. New runtime. Explicit boundaries. Measurable outcomes.**

The goal of this work is to connect the reliability discipline of enterprise systems with the flexibility of probabilistic AI without confusing one correctness model for the other.

---

### Attribution and trademarks

All trademarks, service marks and logos referenced in architecture examples remain the property of their respective owners. References to AWS, Google Cloud, Microsoft Azure, SAP, Meta, LangGraph and other technologies are for educational and architectural comparison and do not imply endorsement.
