# Hi, I'm Subham Gupta 👋

**Staff Architect & AI Architect** at SAP Labs India
13+ years governing $350M+ in financial transaction volumes — now building production AI systems on AWS.

![AWS](https://img.shields.io/badge/AWS-Bedrock_Lambda_SQS_DynamoDB-FF9900?style=flat&logo=amazonaws&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat&logo=python&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-Multi--Agent-FF6B35?style=flat)
![Terraform](https://img.shields.io/badge/Terraform-IaC-7B42BC?style=flat&logo=terraform&logoColor=white)

## What I Build

My core mental model maps enterprise distributed systems patterns directly to AI-native components:

Agent        =  microservice (reasoning unit)
RAG          =  CQRS knowledge retrieval layer
MCP Tool     =  idempotency-aware API action
Orchestrator =  saga-compensating control plane

## Active Portfolio

### 1. Order-to-Cash Agentic AI Platform
Phase 2

> 5-agent LangGraph system with Amazon Bedrock RAG, hybrid OpenSearch retrieval, MCP-style tool
> microservices, Terraform IaC, and RAGAS CI/CD evaluation gate.

**Stack:** Python · FastAPI · LangGraph · Amazon Bedrock · OpenSearch · Terraform · ECS Fargate

**Key patterns:** Two-layer DynamoDB idempotency · Circuit breakers · BM25+KNN hybrid RAG ·
Policy-as-code governance · Async SQS FIFO + DLQ

**View Repository → https://github.com/subhamviky/order-to-cash-agentic-ai **

---

### 2. Cloud-Native Payment Reconciliation Engine
Phase 1
Phase 2

> Production payment reconciliation engine on AWS, directly mirroring $350M SAP TM financial
> settlement architecture on cloud-native infrastructure.

**Stack:** Python · FastAPI · Lambda · SQS + DLQ · DynamoDB · CloudWatch · Amazon Bedrock

**Key patterns:** Async POST → PENDING → RECONCILED pipeline · DLQ escalation with backoff ·
LangGraph agent routing · Bedrock Titan RAG over financial audit logs

**View Repository → https://github.com/subhamviky/aws-reconciliation-engine **

---
## What I've Proven at Enterprise Scale

At SAP Labs, working on $350M+ financial settlement systems:

- **80% runtime reduction** — Re-engineered synchronous invoicing engine to async pipeline (35 min → 7 min) for 10,000+ daily freight orders
- **Zero audit failures** — Designed idempotency + exactly-once processing for $350M+ in distributed financial postings across 150+ global vendors
- **99.9% stability** — Primary Incident Commander for 300+ mission-critical escalations annually

---

## Tech Across Both Portfolios

FastAPI
LangChain
DynamoDB
SQS
OpenSearch
Terraform
GitHub Actions

---
## Connect

LinkedIn -> https://www.linkedin.com/in/subham-gupta-0a05a058
Email -> subhamviky@gmail.com

*Open to conversations about Agentic AI platform design, RAG at scale, and cloud-native financial systems.*
