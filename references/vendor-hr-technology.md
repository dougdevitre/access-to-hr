# Vendor & HR Technology Management — Workday County HR Reference

## Overview

County HR departments manage a portfolio of HR technology vendors beyond Workday: background
check vendors, benefits brokers, COBRA administrators, EAP providers, LMS platforms, applicant
tracking supplements, assessment vendors, and more. This guide covers vendor management,
technology stack optimization, and how to evaluate new HR tech — including AI tools.

---

## HR Technology Stack Map

### Typical County HR Technology Portfolio

| Category | Common Vendors | Workday Integration |
|---|---|---|
| Core HCM | Workday (primary) | — |
| Background Check | HireRight, Sterling, Checkr | Bidirectional via Workday integration |
| COBRA Administration | WEX, Benefitfocus, DirectPay | Outbound qualifying event data |
| Benefits Broker Platform | bswift, Businessolver, Benefitsolver | 834 file to carriers |
| EAP | Optum, ComPsych, Magellan Health | No integration; referral tracking only |
| LMS (if external) | Cornerstone, Bridge, TalentLMS | Bidirectional: employees + completions |
| I-9 / E-Verify | I9Advantage, Tracker I-9, WorkBright | May integrate with Workday onboarding |
| Applicant Tracking (supplement) | NeoGov (most common in govt), Governmentjobs.com | Bidirectional or replace with Workday Recruiting |
| Compensation Benchmarking | Mercer, Willis Towers Watson, SUTA/public salary surveys | Manual data pull |
| Payroll (if separate) | Tyler Munis, SAP, Oracle | Bidirectional payroll feed |
| Time Clock Hardware | Kronos (UKG), Swipeclock, ADP | Integration with Workday Time |
| Survey / Engagement | Qualtrics, Culture Amp, Gallup | Manual or API integration |
| HR Case Management | ServiceNow, Salesforce, Zendesk | Usually standalone |
| Document Management | SharePoint, Laserfiche, DocuWare | Manual or integration |

---

## Vendor Management Framework

### Vendor Inventory

Maintain a vendor registry spreadsheet or in your procurement system:

| Field | Description |
|---|---|
| Vendor Name | Company providing the service |
| Service | What they provide |
| Contract Start | Agreement start date |
| Contract End | Renewal/expiration date |
| Auto-Renew | Yes/No; if yes, notice period to cancel |
| Annual Cost | Total annual spend |
| Contract Owner | HR person responsible for the relationship |
| Integration Status | How data flows between vendor and Workday |
| SLA / Uptime | Key performance guarantees |
| Data Classification | What county data the vendor holds (PHI, PII, financial) |
| BAA Required | Business Associate Agreement (if PHI involved) |
| Security Certification | SOC 2 Type II, ISO 27001, etc. |

### Annual Vendor Review

For each significant HR vendor:
1. **Performance review**: Did they meet SLAs? Any service failures?
2. **Cost review**: Are we getting value? Benchmark against alternatives?
3. **Contract review**: Is this the right term? Any auto-renew traps?
4. **Security review**: Have they had any data breaches? Current certifications?
5. **Integration health**: Are integrations running cleanly? Any data errors?

---

## NeoGov / GovernmentJobs.com

NeoGov is the most widely used applicant tracking and NEOGOV system in government. Many counties
use it for recruiting because it integrates with state civil service systems and is familiar to
government job seekers.

### NeoGov + Workday Integration

If your county uses both:
- NeoGov manages the recruiting and civil service testing process
- When a hire is made in NeoGov, data should feed to Workday to initiate the hire action
- Integration options: NeoGov has a published Workday integration; IT must configure
- Without integration: HR manually re-enters candidate data in Workday = double data entry + error risk

### Decision: NeoGov vs. Workday Recruiting

| Factor | NeoGov Advantage | Workday Recruiting Advantage |
|---|---|---|
| Civil service / eligibility list management | Strong | Limited |
| Integration with state testing systems | Yes | No |
| Job seeker familiarity (govt) | High | Low |
| Cost | Additional license | Included in Workday |
| Single platform (no double entry) | No | Yes |
| Reporting and analytics | Limited | Strong |

**Recommendation**: Counties with active civil service testing and eligibility lists → keep NeoGov.
Counties without civil service testing → consider migrating to Workday Recruiting.

---

## Background Check Vendor Management

### Key Compliance Requirements

Background check vendors are regulated by the **Fair Credit Reporting Act (FCRA)**:
- Require signed authorization from applicant before ordering check
- Provide pre-adverse action notice if planning to deny based on results
- Provide adverse action notice if denying (with copy of report + Summary of Rights)
- Allow applicant time to dispute inaccuracies (typically 5 business days minimum)

### Workday Integration with Background Check Vendor

Most major vendors (HireRight, Sterling) have Workday integrations:
- Recruiter initiates background check from within Workday candidate record
- Vendor sends candidate a consent/authorization link
- Results returned to Workday (pass / review / adverse)
- HR reviews adverse results before any adverse action

### Turnaround Time SLAs

Negotiate SLAs with your vendor:
- Standard check (criminal, employment verification): 3–5 business days
- Law enforcement (with psychological eval): 30–45 days total
- Credit check (if applicable): 1–2 days

---

## EAP (Employee Assistance Program) Management

### What to Look for in an EAP Contract

| Feature | Standard | Better |
|---|---|---|
| Sessions per issue | 3 sessions | 6–8 sessions |
| Available 24/7 | Yes | Yes |
| In-person + telehealth | Yes | Yes + app-based |
| Manager consultation | Included | Yes |
| Critical incident response | Yes | On-site debriefing included |
| Financial counseling | Basic | Full (budgeting, debt, legal) |
| Legal consultation | Basic | Full access |
| Work-life services | Basic | Child care referrals, elder care |
| Reporting | Basic utilization | Department-level (anonymous) |
| Cost (PEPM) | $1.50–$3.00/employee/month | $3.00–$6.00 |

### EAP Utilization Reports

Request quarterly from your EAP:
- Total utilization rate (number of employees using services / total eligible)
- Anonymous utilization by department (if 10+ users — anonymity threshold)
- Issues categories (work stress, family, financial, substance use) — no names
- Critical incident activations and responses

> Use EAP utilization data to identify departments or periods of elevated stress. A department
  with 3x normal EAP utilization may have a management or workload problem.

---

## AI Tools in County HR

AI is rapidly entering HR practice. County HR leaders need to evaluate these tools carefully.

### Current AI Applications in HR

| Application | Vendors | Considerations |
|---|---|---|
| Resume screening | Workday AI, HireVue, Eightfold | Bias risk; EEOC guidance on AI screening; require human review |
| Job description writing | Workday AI, Textio, ChatGPT | Review for exclusionary language; ensure ADA-compliant |
| Chatbot / HR self-service | Various | Good for routine FAQs; must not give inaccurate policy guidance |
| Predictive attrition | Workday Illuminate, Qualtrics | Privacy concerns; use to guide retention — not punish employees |
| Interview question generation | AI assistants | Ensure questions are legal (no protected class topics) |
| Performance review drafting | AI assistants | Manager must review; cannot fully delegate accountability |
| Pay equity analysis | Workday, Syndio, Trusaic | Useful tool; results must be reviewed by HR + legal |
| Scheduling optimization | Various | Good for complex shift scheduling; verify FLSA compliance |
| Benefits recommendation | AI chatbots | Must not give advice that constitutes insurance advice |

### AI Procurement Checklist for County HR

Before adopting any AI HR tool:

- [ ] **Bias audit**: Has the vendor conducted a bias audit? Can they provide results?
- [ ] **EEOC compliance**: Does the tool comply with current EEOC guidance on AI in employment decisions?
- [ ] **Data privacy**: What employee data does the tool ingest? Is it stored in the US? Is it used to train the vendor's model?
- [ ] **County data ownership**: County owns its data; vendor cannot use county employee data for model training
- [ ] **Transparency**: Can the tool explain its recommendations? (Explainability requirement for adverse employment decisions)
- [ ] **Human review requirement**: AI should augment human decisions, not replace them — especially for adverse actions
- [ ] **IT security**: Vendor must meet county cybersecurity standards; SOC 2 Type II minimum
- [ ] **Legal review**: County counselor should review AI vendor terms before contract

### Workday Illuminate (Workday's AI)

Workday has integrated AI (Workday Illuminate) across the platform. Features include:
- Manager copilot: draft performance review comments; summarize employee history
- Recruiting AI: job description optimization; candidate matching
- Analytics: predictive attrition signals; anomaly detection
- Time: schedule optimization suggestions

As Workday Illuminate matures, features are added with each release. Review release notes
specifically for Illuminate features; some require opt-in activation.

---

## Technology Governance for HR

### HR Technology Committee

For counties with multiple HR tech systems, establish a governance committee:
- Members: HR Director, IT Director or HRIS lead, Finance (if payroll is included), Payroll Director
- Meets: Quarterly
- Responsibilities: approve new HR technology purchases, manage vendor performance, oversee integration health, review data privacy

### Technology Decision Framework

Before purchasing any new HR technology:

1. **Problem definition**: What specific problem are we solving? (Don't buy tech looking for a problem)
2. **Build vs. buy vs. configure**: Can Workday already do this? Can we configure our existing system?
3. **Total cost of ownership**: License + implementation + training + ongoing support + integration
4. **Integration requirements**: How does this connect to Workday? What does the integration cost?
5. **Security and privacy**: See AI checklist above (applies to all tech)
6. **Change management**: How will we drive adoption? What training is needed?
7. **ROI**: What is the measurable return? How will we know if it's working?

---

## HR Technology KPIs

| KPI | Target | Source |
|---|---|---|
| Vendor SLA compliance | >99% uptime for critical systems | IT monitoring |
| Integration error rate (weekly) | <1% per integration run | Integration monitoring log |
| Background check turnaround time | <5 days (standard) | Vendor SLA report |
| EAP utilization rate | >5% (indicates access; not stigma) | EAP quarterly report |
| HR technology spend as % of HR budget | Track trend; 10–20% of HR budget | Finance + HR budget |
| Contracts auto-renewing without review | 0 | Vendor registry |
| Vendors without current SOC 2 | 0 (for vendors holding PII) | Security review |
