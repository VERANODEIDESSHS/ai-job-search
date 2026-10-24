# Job Evaluation Framework

<!-- SETUP: Skill match areas and career goals personalized for Hiramis Castillo Barraza (career goals and constraints pending confirmation) -->

## Scoring Dimensions

Evaluate each job posting against these five dimensions:

### 1. Technical Skills Match (0-100)
How well do the required/preferred skills align with the candidate's capabilities?

| Score | Meaning |
|-------|---------|
| 80-100 | Core requirements are primary skills |
| 60-79 | Most requirements match, 1-2 gaps that are learnable |
| 40-59 | Partial match, significant upskilling needed |
| 0-39 | Fundamental mismatch |

**Strong match areas:** End-to-end procurement / procure-to-pay, vendor and supplier negotiation, cost reduction and rate/spend analysis, invoice auditing and reconciliation, international logistics and customs compliance, bilingual Spanish/English
**Moderate match areas:** Contract and PO management, supplier performance management, Harmonized Tariff Schedule classification, demand planning and transport operations (certificates), Microsoft Excel reporting, Microsoft Project
**Weak match areas:** Named ERP systems (SAP, Oracle, NetSuite) unless confirmed, licensed US customs brokerage, US-specific regulations (FAR/government procurement), advanced analytics (SQL, Power BI, Python), people management of large teams

### 2. Experience Match (0-100)
Does work history align with what they're looking for?

| Score | Meaning |
|-------|---------|
| 80-100 | Direct experience in the same domain and role type |
| 60-79 | Related experience, transferable skills clear |
| 40-59 | Adjacent experience, would need to make the case |
| 0-39 | Unrelated experience |

**Strong:** Purchasing / procurement on high-value construction projects, import coordination, logistics coordination, invoice and freight audit
**Moderate:** Supply chain analysis, demand planning (certificate-level), operations coordination across finance/logistics
**Entry-level / gap:** US-market experience (all roles in Panamá), roles requiring specific US ERP tenure, senior strategic sourcing leadership

### 3. Behavioral/Culture Fit (0-100)
Does the role and company culture match the behavioral profile?

| Score | Meaning |
|-------|---------|
| 80-100 | Culture strongly matches behavioral preferences |
| 60-79 | Mixed signals but mostly compatible |
| 40-59 | Some friction areas |
| 0-39 | Significant culture mismatch |

**Red flags to research:** Department disorganization, work dominated by maintenance over development, poor chemistry with leadership, culture mismatches. Check reviews, media coverage, LinkedIn connections, and network contacts for insider perspective.

### 4. Location & Logistics (Pass/Fail + Notes)
- St. Augustine FL / St. Johns County / Jacksonville metro on-site or hybrid: PASS
- US remote: PASS
- Elsewhere in Florida (hybrid, longer commute): FLAG (confirm with user)
- Requires relocation outside Florida: FLAG (default FAIL unless user confirms openness)
- Requires US work authorization / no sponsorship: PASS (green card holder)
- ITAR / EAR "U.S. person" requirement: PASS (lawful permanent resident qualifies)
- Posting explicitly states "U.S. citizenship required" (common for security clearances and some Public Trust roles): FAIL until naturalization completes; note as "revisit after citizenship"
- Federal contractor or Public Trust **without** an explicit citizenship statement: PASS, but flag for the user to confirm eligibility (many accept lawful permanent residents)

### 5. Career Alignment & Motivation (0-100)
Does this role advance career goals and contain tasks that energize?

| Score | Meaning |
|-------|---------|
| 80-100 | Strongly aligned with career direction, clear growth path |
| 60-79 | Good role but only partially aligned with long-term goals |
| 40-59 | Decent job but doesn't build toward career goals |
| 0-39 | Dead end or backwards step |

**Career goals:** *(inferred from resume — confirm with user)*
- Re-establish a procurement / purchasing career in the US (Northeast Florida or remote)
- Grow toward senior buyer / procurement specialist, supported by CPSM certification
- Leverage bilingual Spanish/English and Latin America trade experience

**Motivation filter:** Evaluate not just whether you *can* do the tasks, but whether the tasks will *energize* you. Consider:
- Tasks that energize (inferred): negotiating savings, vendor management, cost analysis, making processes audit-ready
- Tasks that drain (inferred): pure data entry with no ownership; quota-driven sales
- Non-task factors: leadership style, department culture, company values, degree of autonomy

**Life situation alignment:** Consider personal constraints:
- **Re-entry**: No listed role since 04/2023; prefer roles that value international experience
- **Location**: Based in St. Augustine, FL; local on-site/hybrid or remote preferred
- **Professional development**: CPSM in progress; employer certification support is a plus

### 6. Salary Benchmark (Optional)

If the salary lookup tool is configured (`salary_data.json` exists), look up the company:
```
python salary_lookup.py "<Company Name>" --json
```

If a city is known from the posting, add `--city "<City>"` to narrow results.

Present findings as:
```
### Salary Benchmark
| Metric | Value |
|--------|-------|
| [Category] index | XX.X (+/-X.X% vs baseline) |
| Overall index | XX.X (+/-X.X% vs baseline) |
```

Interpret results relative to the baseline defined in the data file's metadata. For index-based data, higher typically means above-market compensation.

If the salary tool is not configured, skip this section.

## Output Format

Present the evaluation as:

```
## Job Fit Evaluation: [Role] at [Company]

| Dimension | Score | Notes |
|-----------|-------|-------|
| Technical Skills | XX/100 | [brief note] |
| Experience Match | XX/100 | [brief note] |
| Behavioral Fit | XX/100 | [brief note] |
| Location | PASS/FAIL | [brief note] |
| Career Alignment | XX/100 | [brief note] |

**Overall Score: XX/100** (weighted average of scored dimensions)

### Verdict: [Strong Fit / Good Fit / Moderate Fit / Weak Fit / Poor Fit]

### Key Strengths for This Role
- [bullet points]

### Gaps to Address
- [bullet points]

### Recommendation
[1-2 sentences: apply/skip/apply with caveats]

### Company Research Checklist
- [ ] Checked company website (mission, values, recent news)
- [ ] Checked review sites (Glassdoor, Jobindex, etc.)
- [ ] Checked LinkedIn for team size, recent hires, connections
- [ ] Checked media for restructuring, growth, or workplace issues
- [ ] Identified network contacts who may know the team/manager
```

## Weighting
- Technical Skills: 30%
- Experience Match: 25%
- Behavioral Fit: 15%
- Career Alignment: 30%

(Location is pass/fail, not weighted)

## Thresholds
- **Strong Fit** (75+): Definitely apply, tailor everything
- **Good Fit** (60-74): Apply, address gaps in cover letter
- **Moderate Fit** (45-59): Consider carefully, discuss with user
- **Weak Fit** (30-44): Probably skip unless strategic reasons
- **Poor Fit** (<30): Skip

## Pre-Application: Call the Employer (Best Practice)

Before writing the application, consider whether the candidate should call the contact person listed in the posting. **Only call if there are substantive questions** - never call just to "be remembered."

### When to Suggest Calling
- The posting has unclear or ambiguous requirements
- It's unclear which competencies are essential vs. nice-to-have
- The role description is vague about day-to-day tasks
- There's a named contact person who invites questions

### Good Questions to Ask
- "What are the primary challenges in this role?"
- "How is time typically divided across the listed responsibilities?"
- "Which competencies are most critical for success in this position?"
- "What does success look like in the first 6-12 months?"

### Rules for the Call
- Prepare a 30-second "elevator pitch" about your background in case they ask
- The call's purpose is **gathering information**, not delivering a pitch
- Take notes - use what you learn to tailor the application
- Reference the conversation naturally in the cover letter ("After speaking with [name], I was especially drawn to...")
