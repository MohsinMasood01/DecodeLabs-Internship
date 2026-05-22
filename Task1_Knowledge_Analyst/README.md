# The Knowledge Analyst
### RAG-Based Legal Document Intelligence Tool

> A Generative AI project simulating Retrieval-Augmented Generation (RAG) for legal document intelligence — built using Claude Projects with zero code.

---

## Overview

This project delivers a working simulation of a RAG workflow that enables users to query a large, complex legal document using natural language and receive precise, cited answers — with zero hallucination.

The tool was built entirely using Generative AI (Claude Projects by Anthropic). No backend, no vector database, no code — only prompt engineering and document intelligence.

---

## The Scenario

> *A law firm has 500-page contracts that take hours to read manually. They need a tool that can instantly summarize key clauses and answer specific questions about the document — without hallucinating or fabricating facts.*

---

## What is RAG?

Retrieval-Augmented Generation (RAG) is an AI architecture that combines:

- **Retrieval** — locating the most relevant content from a large knowledge base in response to a query
- **Generation** — producing a coherent, human-readable answer using only that retrieved content

This project simulates the same behavior without infrastructure — using Claude Projects as the AI backbone, with prompt engineering enforcing document-exclusive, citation-grounded responses.

---

## Tool Capabilities

| Feature | Description |
|---|---|
| Citation-Enforced Q&A | Every answer includes `[Chapter X, Page Y]` citations |
| Hallucination Guard | Refuses to answer anything not present in the document |
| Document Exclusivity | Cannot use outside knowledge — only the uploaded document |
| Summary Dashboard | Auto-extracts Risks, Dates, and Stakeholders on command |
| Visual Dashboard | HTML artifact rendering the dashboard in a professional UI |
| User-Driven Queries | All questions provided by the user — nothing hardcoded |

---

## Knowledge Base Document

**The 9/11 Commission Report** — 585 pages

Selected for its density, complexity, and rich content across all three dashboard categories (Risks, Dates, Stakeholders). The document was compressed and split into chunks for upload into Claude Projects.

---

## System Prompt

The following system prompt was deployed as the Project Instructions in Claude Projects. It governs every conversation within the project:

```
You are a Legal Document Intelligence Assistant. Your sole knowledge base
is the document(s) uploaded to this project. You have no other knowledge
source.

STRICT RULES — FOLLOW WITHOUT EXCEPTION:

1. ONLY answer from the uploaded documents. Never use outside knowledge,
   assumptions, or general information under any circumstances.

2. CITATIONS ARE MANDATORY. Every statement you make must end with:
   [Chapter X, Page Y] or [Section Title, Page Y]
   If you cannot cite it, do not say it.

3. IF THE ANSWER IS NOT IN THE DOCUMENT, respond with exactly:
   "This information is not found in the uploaded document."
   Never guess or approximate.

4. NEVER summarize from memory. Treat every question as a fresh lookup
   from the uploaded documents only.

5. DASHBOARD COMMAND — When the user types "ANALYZE DOCUMENT", respond
   ONLY in this exact structured format:

   DOCUMENT ANALYSIS DASHBOARD
   RISKS IDENTIFIED: [list at least 8 risks with citations]
   KEY DATES & TIMELINE: [list at least 10 dates with citations]
   KEY STAKEHOLDERS: [list at least 10 stakeholders with citations]

6. Keep answers concise and direct. No opinions or commentary beyond
   what the document states.

7. If a question spans multiple sections, cite all relevant sections
   separately.
```

---

## Sample Outputs

### Q&A with Citations

**Query:** What were the primary failures of U.S. intelligence agencies that allowed the 9/11 attacks to occur?

**Response (excerpt):**
```
The CIA did not share with the FBI critical information about two known
al Qaeda operatives — Nawaf al Hazmi and Khalid al Mihdhar — who had
entered the United States, despite knowing this as early as January 2000.
[Chapter 8, Page 269]

There was no government-wide collection of intelligence about potential
domestic threats from al Qaeda in the period before 9/11.
[Chapter 8, Page 265]

The report concludes there was a failure of policy, capabilities, and
management — not merely individual mistakes — across multiple agencies
simultaneously. [Chapter 11, Page 339]
```

---

### Hallucination Guard Test

**Query:** What recommendations did the Commission make regarding the role of Pakistan's ISI in funding the hijackers?

*(This is a deliberate trick question — no such recommendations exist in the report)*

**Response (excerpt):**
```
The Commission did not make specific recommendations targeting Pakistan's
ISI as a funding source for the hijackers, because the report did not
establish that the ISI directly funded the 9/11 operation.

"To date, the U.S. government has not been able to determine the origin
of the money used for the 9/11 attacks." [Chapter 5, Page 172]

This information is not found in the uploaded document.
```

✅ Hallucination guard held — the system refused to fabricate findings that do not exist.

---

### Summary Dashboard

Triggered by typing `ANALYZE DOCUMENT` in the chat:

```
DOCUMENT ANALYSIS DASHBOARD
═══════════════════════════════════════════════════════════

RISKS IDENTIFIED:
- Lack of domestic intelligence capability [Chapter 8, Page 265]
- Failure to watchlist known terrorists [Chapter 8, Page 269]
- The "Wall" between law enforcement and intelligence [Chapter 8, Page 271]
- Vulnerability of U.S. aviation security [Chapter 1, Page 2]
- Al Qaeda's global financial network [Chapter 5, Page 169]
- Insufficient counterterrorism resources [Chapter 4, Page 93]
- Failure of imagination [Chapter 11, Page 344]
- Lack of unity of command in counterterrorism [Chapter 11, Page 353]
- Visa and border security vulnerabilities [Chapter 7, Page 215]
- Taliban sanctuary for al Qaeda in Afghanistan [Chapter 2, Page 65]
- Inadequate response to USS Cole attack [Chapter 6, Page 190]
- Over-reliance on covert action without strategic policy [Chapter 4, Page 132]

KEY DATES & TIMELINE:
- 1988 — al Qaeda established [Chapter 2, Page 56]
- Feb 26, 1993 — First WTC bombing [Chapter 3, Page 71]
- Aug 7, 1998 — Embassy bombings in Kenya and Tanzania [Chapter 4, Page 115]
- Aug 20, 1998 — U.S. cruise missile strikes [Chapter 4, Page 117]
- Jan 2000 — CIA identifies Hazmi and Mihdhar [Chapter 6, Page 181]
- Jun 3, 2000 — Atta arrives in United States [Chapter 7, Page 224]
- Oct 12, 2000 — USS Cole bombing [Chapter 6, Page 190]
- Aug 6, 2001 — Presidential Daily Brief issued [Chapter 8, Page 261]
- Aug 15, 2001 — Moussaoui concerns raised, not acted on [Chapter 8, Page 273]
- Sep 11, 2001 8:46AM — Flight 11 strikes North Tower [Chapter 1, Page 7]
- Sep 11, 2001 9:03AM — Flight 175 strikes South Tower [Chapter 1, Page 8]
- Sep 11, 2001 9:37AM — Flight 77 strikes Pentagon [Chapter 1, Page 10]
- Sep 11, 2001 10:03AM — Flight 93 crashes, Shanksville [Chapter 1, Page 14]

KEY STAKEHOLDERS:
- Osama bin Laden — al Qaeda founder and attack director [Chapter 2, Page 55]
- Khalid Sheikh Mohammed — 9/11 operational mastermind [Chapter 5, Page 153]
- Mohamed Atta — Lead hijacker, piloted Flight 11 [Chapter 7, Page 215]
- Nawaf al Hazmi — Senior operative, not watchlisted [Chapter 8, Page 269]
- Khalid al Mihdhar — Senior operative, identified too late [Chapter 6, Page 181]
- George Tenet — CIA Director [Chapter 6, Page 197]
- Richard Clarke — National Coordinator for Counterterrorism [Chapter 6, Page 188]
- Condoleezza Rice — National Security Advisor [Chapter 8, Page 260]
- Louis Freeh — FBI Director [Chapter 3, Page 76]
- Ayman al Zawahiri — al Qaeda Deputy [Chapter 2, Page 57]
- The Taliban — Provided sanctuary to al Qaeda [Chapter 2, Page 65]
- FAA — Aviation security failures [Chapter 11, Page 345]
- NORAD — Air defense command [Chapter 1, Page 17]
═══════════════════════════════════════════════════════════
```

---

## Repository Contents

| File | Description |
|---|---|
| `README.md` | Project documentation |
| `system_prompt.txt` | The engineered system prompt |
| `dashboard.html` | Visual HTML dashboard (open in any browser) |
| `TheKnowledgeAnalyst_ProjectReport.docx` | Full project report |

---

## Tools Used

| Tool | Purpose |
|---|---|
| Claude Projects (Anthropic) | AI engine — document intelligence and prompt deployment |
| ilovepdf.com | PDF compression and splitting |
| HTML Artifact | Claude-generated visual dashboard |

---
