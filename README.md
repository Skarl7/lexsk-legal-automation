# Lexsk Legal Automation

> AI-powered legal workflow automation for small firms and paralegal practices

[![OpenAI](https://img.shields.io/badge/OpenAI-412991?logo=openai&logoColor=white)](https://openai.com)
[![n8n](https://img.shields.io/badge/n8n-EA4B71?logo=n8n&logoColor=white)](https://n8n.io)
[![Google](https://img.shields.io/badge/Google%20Workspace-4285F4?logo=google&logoColor=white)](https://workspace.google.com)

**Built by** [Skarl7](https://github.com/Skarl7) | [Lexsk Legal Limited](https://lexsk.co.uk)

---

## Overview

Lexsk Legal Automation streamlines paralegal workflows using AI and no-code automation. It handles client intake, document drafting, case research, and compliance tasks — freeing time for high-value legal work.

## Components

| Component | Description | Tech Stack |
|-----------|-------------|------------|
| Client Intake Pipeline | Automated form to CRM with AI triage | Typeform, Google Sheets, OpenAI |
| Contract Drafting Engine | AI-generated NDAs, SLAs, LoEs with human review | Claude API, Google Docs |
| Case Research Summariser | LLM-powered legal research summaries | OpenAI, LangChain |
| Compliance Tracker | GDPR and regulatory deadline monitoring | n8n, Google Calendar |
| Document Assembly | Template-based document generation | Google Docs API, OpenAI |

## Workflows

### Contract Review Workflow
1. Client submits document via secure portal
2. AI analyses document type and jurisdiction
3. Risk flags identified and highlighted
4. Review notes generated for paralegal
5. Client notified via email with timeline

### NDA Drafting Workflow
1. Intake form collects party details and scope
2. Claude generates jurisdiction-appropriate NDA
3. Document saved to Google Drive with metadata
4. DocuSign integration for e-signature
5. Fully executed copy stored in client folder

### Case Research Pipeline
1. Paralegal inputs case facts and jurisdiction
2. RAG engine searches legal precedent database
3. OpenAI summarises relevant authorities
4. Output formatted as paralegal research memo
5. Stored in case management system

## Getting Started

### Prerequisites

- OpenAI or Claude API key
- Google Workspace account with API access
- n8n instance (self-hosted or cloud)
- Typeform or Google Forms account

### Environment Setup

```bash
cp .env.example .env
OPENAI_API_KEY=sk-...
CLAUDE_API_KEY=...
GOOGLE_WORKSPACE_CREDENTIALS=path/to/credentials.json
N8N_WEBHOOK_URL=https://your-n8n/webhook/
```

## File Structure

```
lexsk-legal-automation/
├── workflows/
│   ├── client-intake/
│   ├── contract-drafting/
│   └── case-research/
├── templates/
│   ├── nda-template.docx
│   ├── sla-template.docx
│   └── loe-template.docx
├── scripts/
│   └── document-assembler.py
└── docs/
    └── GDPR-compliance.md
```

## GDPR Compliance

All automation respects GDPR requirements:
- Data minimisation — only necessary client data collected
- Purpose limitation — data used only for stated legal purposes
- Access controls — role-based permissions on all systems
- Audit logging — all data access and modifications logged
- Data retention — automated deletion after statutory periods

See [GDPR Compliance](/docs/GDPR-compliance.md) for details.

## Contributing

Contributions welcome from legal-tech professionals and automation enthusiasts.

## License

Apache 2.0

---
*Lexsk Legal Limited — Regulated paralegal services | lexsk.co.uk*
