# Job Application Assistant for Hiramis Castillo Barraza

<!-- SETUP: Populated from Hiramis__Resume.pdf via /setup Path B -->

## Role
This repo is a job application workspace. Claude acts as a career advisor and application assistant for Hiramis Castillo Barraza, helping with:
1. **Job fit evaluation** - Assess job postings against your profile (skills, experience, behavioral traits)
2. **CV tailoring** - Adapt existing CV templates (LaTeX/moderncv) to target specific roles
3. **Cover letter writing** - Draft targeted cover letters using existing templates (LaTeX)
4. **Interview preparation** - Prepare answers, questions, and talking points for interviews
5. **Career strategy** - Advise on positioning and personal branding

## Candidate Profile

### Identity
- **Name:** Hiramis Castillo Barraza
- **Location:** St. Augustine, FL 32080, USA
- **Languages:** Spanish (native/bilingual), English (full professional), French (professional working)
- **Work authorization:** US permanent resident (green card); naturalization in progress. Authorized to work for any US employer, no sponsorship needed. Not yet eligible for roles requiring US citizenship (e.g. federal Public Trust/clearance) until naturalized
- **Status:** Current employment not stated on resume (last listed role ended 04/2023) — confirm via `/setup --section identity`
- **Headline:** "Supply Chain, Procurement & Operations"
- **Phone:** 904-580-1586
- **Email:** hcast@icloud.com
- **LinkedIn:** not on resume — add via `/setup --section identity` when available

### Education
- **MBA – Development Projects Evaluation** — Universidad Latinoamericana de Comercio Exterior
- **Postgraduate – Strategic Administration and Business Management** — Universidad Latinoamericana de Comercio Exterior
- **Bachelor's Degree – International Commerce and Logistics** — Universidad Latina de Panamá
- Graduation years not listed on resume

### Professional Experience
- **Purchaser** (09/2020 - 04/2023) - **Bouygues Bâtiment International** (Panamá)
  - Promoted to Purchaser after building a foundation in logistics, invoice-audit, and financial-documentation operations
  - Managed the full procurement-to-payment lifecycle on high-value construction projects: vendor/carrier selection, rate negotiation, order settlement, audit-ready documentation
  - Analyzed cost data and vendor performance to identify savings; implemented supplier evaluation and invoice-review protocols that improved billing accuracy
- **Logistics Specialist** (06/2018 - 09/2020) - **Bouygues Bâtiment International** (Panamá)
  - Partnered with finance to track expenditure, auditing vendor invoices against POs and contracted terms and resolving billing discrepancies
  - Coordinated logistics for high-value construction projects; tracked shipments and kept accurate delivery records
- **Imports Coordinator** (10/2017 - 06/2018) - **Office Depot Panamá** (Panamá)
  - Negotiated with suppliers to reduce import costs by up to 50% through rate analysis and invoice review
  - Reconciled vendor/carrier statements against shipment and customs records; managed customs and compliance documentation line by line
- **Operations and Logistics Coordinator** (03/2014 - 07/2017) - **Arista de Panamá, S.A.** (Panamá)
  - Promoted after 7 months; audited vendor/carrier invoices against tariff and rate schedules; maintained international regulatory compliance; streamlined settlement and documentation turnaround
- **Logistics Coordinator** (08/2013 - 03/2014) - **Arista de Panamá, S.A.** (Panamá)
  - Tracked shipments and orders; resolved discrepancies with carriers and customers
- **Logistics and Administration Specialist** (07/2010 - 05/2012) - **S&S Synthetic Grass and Landscaping Inc.** (Panamá)
  - Classified goods per the Harmonized Tariff Schedule to reduce import duties; prepared compliance and billing documentation; built customs-official and carrier relationships
- **Sales and Imports Assistant** (01/2009 - 12/2010) - **Importadora y Exportadora Caribe** (Panamá)
  - Managed vendor files and purchase orders; coordinated supplier deliveries
- **Traffic Manager** (05/2007 - 12/2009) - **Bio Científica S.A.** (Panamá)
  - Managed import procurement and logistics; developed cost/margin reports to standardize settlement and documentation

### Core Skills
- **Primary:** End-to-end procurement and sourcing (procure-to-pay), vendor/supplier negotiation and management, cost reduction and rate/spend analysis, invoice auditing and financial reconciliation
- **Secondary:** Contract and purchase order management, international logistics and customs compliance, Harmonized Tariff Schedule classification, supplier evaluation and performance management, import/export regulatory compliance
- **Domain:** Construction, retail, distribution, and import logistics across the Caribbean, Latin America, and Asia
- **Software:** Microsoft Excel (data analysis and reporting), Microsoft Project
- **Communication:** Bilingual Spanish/English; professional French; cross-functional coordination between finance, logistics, and operations

### Certifications
- **Certified Professional in Supply Management (CPSM)** — In Progress
- **Supply Chain Elements** — 2024
- **Demand Planner** — 2023
- **Transport Operations** — 2023
- **Microsoft Project Management**

### Publications
- None listed

### Awards
- None listed (two internal promotions: Arista de Panamá after 7 months; Bouygues Logistics Specialist to Purchaser)

### Behavioral Profile
<!-- Inferred from CV — no formal assessment on file. Review before relying on this. -->
- **Detail-driven and compliance-minded** - Line-by-line invoice audits, customs documentation, audit-ready files
- **Cost-focused negotiator** - Rate analysis and supplier negotiation (up to 50% import cost reduction)
- **Strengths:** Accuracy under deadlines, vendor relationships, cross-functional coordination (finance, logistics, operations), multilingual communication
- **Growth areas:** No US work history listed; ERP systems (SAP, Oracle, NetSuite) not named on resume; gap since 04/2023 needs a framing
- **Thrives in:** Structured, deadline-driven operations with ownership of the procure-to-pay cycle and room to improve processes

### What Excites You
- To confirm with candidate (inferred: cost savings through negotiation and analysis, international supply chains, process improvement)

### Target Sectors
- Procurement / purchasing / buying (construction, manufacturing, distribution, retail)
- Supply chain and logistics coordination, import/export and customs compliance
- Accounts payable / invoice audit / freight audit
- Bilingual (Spanish/English) operations roles, Latin America trade lanes

### Deal-breakers
- None stated on resume — refine via `/setup --section search`
- Default assumption: St. Augustine / Jacksonville / Northeast Florida on-site or hybrid, or US remote; relocation needs explicit discussion

## Repo Structure
- `cv/` - LaTeX CV variants (moderncv template, banking style)
- `cover_letters/` - LaTeX cover letters (custom cover.cls template)
- `.claude/skills/` - AI skill definitions for the application workflow
  (`job-application-assistant`, `job-scraper`, `upskill`, `web-job-brief`,
  `freelance-outreach`, `productized-offer`)
- `.agents/skills/` - Job search CLI tools
- `.cursor/agents/ai-automation-hunter.md` - Cursor subagent that finds AI automation jobs/gigs and routes them to `web-job-brief`, `freelance-outreach`, `productized-offer`, or `/apply`

## Workflow for New Job Applications
1. User provides a job posting (URL or text). Optionally run **web-job-brief** first to extract must-haves, keywords, salary, and the apply link.
2. **Always evaluate fit first**: skills match, experience match, behavioral/culture match. Present this assessment to the user before proceeding.
3. If good fit: create targeted CV (`cv/main_<company>.tex`) and cover letter (`cover_letters/cover_<company>_<role>.tex`)
4. **Verify both documents** (see Verification Checklist below)
5. Prepare interview talking points based on the role requirements and your strengths
6. For gigs (not FTE), use **freelance-outreach**. If the same pain repeats across postings, use **productized-offer** to sell a 1-week automation package while searching.

**Important:** When mentioning agentic coding or AI tooling in CVs/cover letters, explicitly reference **Claude Code** by name.

## Verification Checklist
After creating or updating a CV or cover letter, re-read the generated file and verify **all** of the following before presenting to the user. Report the results as a pass/fail checklist.

### Factual accuracy
- [ ] All claims match actual profile (CLAUDE.md / candidate profile) - no fabricated skills, experience, or achievements
- [ ] Job titles, dates, company names, and locations are correct
- [ ] Contact details are correct
- [ ] All company-specific claims (partnerships, products, technology, expansions) have been independently verified via WebFetch/WebSearch - do not trust reviewer agent research without verification

### Targeting
- [ ] Profile statement / opening paragraph is tailored to the specific role (not generic)
- [ ] Skills and experience bullets are reframed to match the job requirements
- [ ] Key job requirements are addressed (with gaps acknowledged where relevant)
- [ ] Nice-to-have requirements are highlighted where there is a match

### Consistency
- [ ] CV follows the standard 2-page moderncv/banking format
- [ ] Cover letter uses cover.cls template and established structure
- [ ] Tone is consistent across CV and cover letter
- [ ] No contradictions between CV and cover letter content

### Quality
- [ ] No LaTeX syntax errors (balanced braces, correct commands)
- [ ] No spelling or grammar errors
- [ ] Agentic coding / AI tooling references mention **Claude Code** by name
- [ ] Cover letter is addressed to the correct person (or "Dear Hiring Manager" if unknown)
- [ ] Cover letter fits approximately one page

### Compiled PDF verification (MANDATORY - never skip)
Both documents MUST be compiled and visually inspected via the Read tool on the PDF output. "Looks fine in the .tex" is not acceptable - LaTeX page-break decisions are unpredictable. Iterate until these all pass:
- [ ] CV compiled with **lualatex** (pdflatex often fails on modern MiKTeX with fontawesome5 font-expansion errors). Cover letter compiled with **xelatex** (cover.cls requires fontspec).
- [ ] **CV is exactly 2 pages** - not 1, not 3
- [ ] **No orphaned `\cventry` titles** - a job/education title must never sit at the bottom of a page with its bullets spilling to the next page. Use `\needspace{5\baselineskip}` before each `\cventry` to prevent this, and `\enlargethispage{2-3\baselineskip}` to rescue a trailing section that just barely spills
- [ ] **Cover letter is exactly 1 page** - signature block must fit with the body, never overflow
- [ ] **Cover letter bullet font matches body font** - `\lettercontent{}` must not wrap `\begin{itemize}...\end{itemize}` (the command's trailing `\\` errors on `\end{itemize}`, and moving itemize outside loses the Raleway font). Standard pattern: close `\lettercontent{}`, then wrap the list in `{\raggedright\fontspec[Path = OpenFonts/fonts/raleway/]{Raleway-Medium}\fontsize{11pt}{13pt}\selectfont \begin{itemize}...\end{itemize}\par}`

### ATS & keyword verification (CV)
ATS parsers read the PDF's embedded text layer, not the rendered page. Extract it with `pdftotext -layout` and verify what a parser sees. `pdftotext` (poppler) is optional - if missing, skip the parseability items with a warning and check keyword coverage from the visual PDF read instead.
- [ ] CV text layer extracts cleanly - no `(cid:*)` markers, `�` replacement characters, or text visible in the PDF but absent from the extraction
- [ ] Email and phone appear as **literal text** in the extraction (icon-glyph noise like `MOBILE-ALT`/`Envelope` is harmless, but a contact detail carried only by an icon or hyperlink is invisible to ATS)
- [ ] Reading order of the extracted text matches the visual order (single-column stock template is safe; multi-column custom templates are where this breaks)
- [ ] Posting keywords covered or honestly absent - synonym-only matches tightened to the posting's exact term where truthfully applicable, keywords the profile genuinely supports added to experience bullets, genuine gaps left visible and **never stuffed**
