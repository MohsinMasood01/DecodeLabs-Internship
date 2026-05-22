# Task : 

---

# Task 3: The Knowledge Analyst
**RAG-Based Legal Document Intelligence Tool**

A Generative AI project simulating Retrieval-Augmented Generation (RAG) for legal document intelligence, built using Claude Projects with zero code.

### Overview

This project delivers a working simulation of a RAG workflow that enables users to query a large, complex legal document using natural language and receive precise, cited answers with zero hallucination.

The tool was built entirely using Generative AI (Claude Projects by Anthropic). No backend, no vector database, no code, only prompt engineering and document intelligence.

### The Scenario

 *A law firm has 500-page contracts that take hours to read manually. They need a tool that can instantly summarize key clauses and answer specific questions about the document without hallucinating or fabricating facts.*

### Tool Capabilities

| Feature | Description |
|---|---|
| Citation-Enforced Q&A | Every answer includes `[Chapter X, Page Y]` citations |
| Hallucination Guard | Refuses to answer anything not present in the document |
| Document Exclusivity | Cannot use outside knowledge, only the uploaded document |
| Summary Dashboard | Auto-extracts Risks, Dates, and Stakeholders on command |
| Visual Dashboard | HTML artifact rendering the dashboard in a professional UI |
| User-Driven Queries | All questions provided by the user, nothing hardcoded |

### Knowledge Base Document

**The 9/11 Commission Report**: 585 pages

Selected for its density, complexity, and rich content across all three dashboard categories (Risks, Dates, Stakeholders). The document was compressed and split into chunks for upload into Claude Projects.

### Repository Contents

| File | Description |
|---|---|
| `system_prompt.txt` | The engineered system prompt |
| `TheKnowledgeAnalyst_ProjectReport.pdf` | Full project report |

---

# Task : 

