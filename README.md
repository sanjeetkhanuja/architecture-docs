# architecture-docs

Architecture and design documentation for enterprise AI and data platforms I have architected and delivered. 

## Projects

| Project | What it is | Highlights |
|---|---|---|
| [**Conversational Insights**](Conversational_Insights/) | An AI agent platform that lets data scientists ask questions in natural language and get answers from complex subsurface data. | Multi-agent design on LangGraph, every agent and data source exposed through MCP, hybrid retrieval (SQL, vector search and logs), guardrails on input and output, and budget-bounded self-correction. |
| [**Data Ingestion and Enrichment Pipelines**](Ingestion_Enrichment_Pipelines/) | A cloud-native framework and portal that ingests Exploration and Production (E&P) data and turns it into standardized Well-Known Entities. | Delivered on both **Google Cloud and Microsoft Azure**. Event-driven, validated and idempotent, with separate paths for structured data and for documents (OCR, embeddings and vector search). |
| [**Agentic CI/CD Pipeline Automation**](Agentic_CI_CD_Pipeline_Automation/) | An autonomous, AI-driven CI/CD framework where specialised agents author, deliver and repair pipelines end to end across GitHub and GitLab, replacing manual, engineer-driven processes with an auditable, agent-orchestrated flow. | Independently deployable **CI and CD agents** on one shared harness and system of record, a **security remediation agent** (triage, auto-fix PRs), blue/green delivery with health, DAST and Playwright gates and automated rollback, and a human-approved PR / MR for every change (agents never self-merge). |

## Patents

The ingestion framework and its workflows are covered by two patents:

- [Geologic Formation Operations Framework](https://patents.google.com/patent/US20210026030A1/en)
- [Geologic Formation Operations Relational Framework](https://patents.google.com/patent/US20210019351/en)

## Themes across the work

- **Multi-cloud delivery:** the same architecture implemented on GCP and Azure.
- **Agentic AI and RAG:** LangGraph orchestration, Model Context Protocol, and LLM gateways routing across hosted and self-hosted models.
- **Agentic DevSecOps:** CI/CD pipelines authored, delivered and repaired by agents, with security gates, auto-remediation, human-in-the-loop approval and a full audit trail.
- **Data platform engineering:** event-driven ingestion, data quality, enrichment, and vector, relational and analytical stores.

## Repository layout

```
architecture-docs/
├── Conversational_Insights/             # AI agent platform
├── Ingestion_Enrichment_Pipelines/      # Ingestion and enrichment (GCP and Azure)
└── Agentic_CI_CD_Pipeline_Automation/   # Agentic CI/CD and security remediation
```

Each folder contains a `README.md`, PNG diagrams for viewing, and `.drawio` sources for editing.
