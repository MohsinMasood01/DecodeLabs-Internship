# Task 2: The Creative Visionary

### Brand Identity

**Company:** NexCore Technologies

**Aesthetic:** Cyberpunk-Corporate

**Color Palette:** Dark navy background, neon blue and purple

**Tagline:** Redefining the Grid

### Assets Generated

| File |	Description |
|---|---|
01_logo.png	| Company logo (hexagon with N monogram)
02_hero.png	| Website hero banner (server room with cityscape)
03_icons_set1.png |	Security, Network, Cloud icons
04_icons_set2.png |	AI, Analytics, Automation icons
05_icons_set3.png | Connectivity, Blockchain, Identity icons

### Tool Selection
The task permitted Midjourney, DALL-E 3, or Stable Diffusion. Midjourney was excluded as it no longer offers a free tier and requires a paid subscription. To compare the remaining options, the same logo prompt was tested on both DALL-E 3 and Leonardo.ai (Stable Diffusion). DALL-E 3 produced superior results, sharper neon glow effects, better prompt adherence, and a more distinctive output, and was selected for all final assets.

### Prompting Strategy
- Negative prompts used on every image to eliminate unwanted elements
- Aspect ratios specified per use case (1:1 for logo, 16:9 for banners and icons)
- Lighting style consistent across all assets (neon glow, dark background)
- Brand consistency maintained by repeating identical style parameters across all prompts
- Tool: *DALL-E 3 via ChatGPT*

### Brand Consistency Approach
Since DALL-E 3 does not support direct image-to-image translation, brand consistency was maintained through systematic prompt engineering, repeating the same color palette, lighting style, and aesthetic descriptors across every asset to ensure a cohesive visual identity.

### Key Design Decision
Cyberpunk-Corporate was chosen to balance futuristic innovation with professional credibility, neon aesthetics signal cutting-edge technology while geometric precision maintains corporate trustworthiness.

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

