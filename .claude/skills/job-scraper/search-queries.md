# Search Queries for Job Scraper

<!-- SETUP: Customized for Hiramis Castillo Barraza — procurement, purchasing, supply chain, logistics/customs. Default locations pending confirmation (St. Augustine / Jacksonville FL + US remote). -->

## Search Sites

Primary (US market):
- **linkedin.com/jobs** - LinkedIn job listings (filter: St. Augustine / Jacksonville, Florida / Remote)
- **freehire.dev** - Tech-focused aggregator; low yield for procurement, use only for broad sweeps

Secondary (optional / market-specific):
- Danish portal CLIs (Jobindex, Jobbank, Jobdanmark, Jobnet) — **skip for this candidate** (US market)
- Company career pages via Google `site:` searches for target employers (e.g. Jacksonville-area distribution, port/JAXPORT logistics, construction firms)

## Query Categories

Queries are grouped by priority. Combine with location terms (St. Augustine, Jacksonville FL, Remote) where the site supports it.

### Priority 1: Procurement / Purchasing

Strongest direction: procure-to-pay ownership, vendor negotiation, cost reduction.

```
site:linkedin.com/jobs "Purchasing Agent" OR "Buyer" Jacksonville Florida
site:linkedin.com/jobs "Procurement Specialist" Florida
site:linkedin.com/jobs "Purchaser" OR "Procurement Coordinator" Jacksonville
```

CLI translations:
- linkedin-search: `-q "Procurement Specialist" -l "Jacksonville, Florida, United States" --jobage 14`
- linkedin-search: `-q "Purchasing Agent" -l "Jacksonville, Florida, United States" --jobage 14`
- linkedin-search: `-q "Buyer" -l "St. Augustine, Florida, United States" --jobage 14`
- linkedin-search: `-q "Procurement Specialist" -l "Remote" --jobage 14`

### Priority 2: Import/Export, Logistics & Trade Compliance

Domain strengths: customs compliance, HTS classification, international logistics, bilingual Spanish.

```
site:linkedin.com/jobs "Import Coordinator" OR "Export Coordinator" Florida
site:linkedin.com/jobs "Logistics Coordinator" Jacksonville
site:linkedin.com/jobs "Trade Compliance" OR "Customs Compliance" Florida
```

CLI translations:
- linkedin-search: `-q "Import Coordinator" -l "Florida, United States" --jobage 14`
- linkedin-search: `-q "Logistics Coordinator" -l "Jacksonville, Florida, United States" --jobage 14`
- linkedin-search: `-q "Trade Compliance" -l "Florida, United States" --jobage 14`

### Priority 3: Invoice / Freight Audit & Supply Chain Analysis

Adjacent roles using invoice auditing, reconciliation, and cost analysis.

```
site:linkedin.com/jobs "Freight Audit" OR "Invoice Audit" Remote
site:linkedin.com/jobs "Supply Chain Analyst" Jacksonville
site:linkedin.com/jobs "Accounts Payable" Bilingual Spanish Jacksonville
```

CLI translations:
- linkedin-search: `-q "Freight Audit" -l "Remote" --jobage 14`
- linkedin-search: `-q "Supply Chain Analyst" -l "Jacksonville, Florida, United States" --jobage 14`
- linkedin-search: `-q "Demand Planner" -l "Jacksonville, Florida, United States" --jobage 14`

### Priority 4: Broader Operations (Bilingual)

Wider net: operations and supply chain roles where Spanish/English is an advantage.

```
site:linkedin.com/jobs "Supply Chain Coordinator" Bilingual Spanish Florida
site:linkedin.com/jobs "Operations Coordinator" Jacksonville
site:linkedin.com/jobs "Vendor Manager" OR "Sourcing Specialist" Remote
```

CLI translations:
- linkedin-search: `-q "Supply Chain Coordinator" -l "Florida, United States" --jobage 14`
- linkedin-search: `-q "Operations Coordinator" -l "Jacksonville, Florida, United States" --jobage 14`
- linkedin-search: `-q "Sourcing Specialist" -l "Remote" --jobage 14`

## Location Filter

When evaluating results, verify the job location fits (default — confirm with candidate):
- St. Augustine, FL and St. Johns County (ideal)
- Jacksonville, FL metro / Palm Coast (ideal for on-site or hybrid)
- US remote (acceptable)
- Elsewhere in Florida, hybrid (borderline — discuss)
- Mandatory relocation outside Florida (too far unless candidate says otherwise)

## Date Filter

Only include jobs posted within the last 14 days, or with an application deadline that has not yet passed. If a posting date cannot be determined, include it but flag as "date unknown".

## Adapting Queries

If the user specifies a focus area, select queries from the matching category and also generate 2-3 custom queries for that focus. For example:
- "/scrape procurement" -> Priority 1 + custom buyer/sourcing queries
- "/scrape logistics" -> Priority 2 + custom import/export queries
- "/scrape broad" -> all four priority categories
