# Job Classification & Reclassification — Workday County HR Reference

## Overview

Job classification is the backbone of county government HR. Every position is assigned a
classification (job title + specification) that defines duties, required qualifications,
and pay grade. Getting classifications right affects pay equity, civil service eligibility,
FLSA status, union jurisdiction, and budget. Workday manages the classification structure
through Job Profiles linked to Compensation Grades.

---

## Classification System Architecture

### How Classification Maps to Workday

```
Civil Service Classification Spec
    → Workday Job Profile
        → Workday Job Family (grouping)
            → Compensation Grade (pay range)
                → Position (specific authorized slot)
                    → Worker (the person in that position)
```

Every change at the classification spec level should be reflected in the Workday Job Profile.

### Classification Components

| Component | Definition | Workday Field |
|---|---|---|
| Classification title | Official job title | Job Profile Name |
| Class code | Numeric identifier | Job Profile Code |
| Class specification | Duties, quals, examples of work | Job Profile Description or attachment |
| Pay grade | Compensation range assigned | Compensation Grade |
| FLSA status | Exempt / Non-Exempt | FLSA Designation on Job Profile |
| EEO category | EEO-4 job category | EEO Job Category on Job Profile |
| Bargaining unit | Union affiliation (if any) | Custom field or Position Management |
| Civil service status | Classified / Unclassified | Custom field on Job Profile or Position |

---

## Classification Audit Process

### When to Audit

- **Annually** — review all job profiles against actual duties being performed
- **When MOU changes** — new pay grades or title changes must be reflected in Workday
- **When reorganizing** — mergers, splits, or restructuring require classification review
- **When new work emerges** — technology change creating new duties → possible new classification

### Audit Steps

1. Pull **Job Profile List** from Workday (Reports > Staffing > All Job Profiles)
2. Compare each profile to the official classification specification (HR or Civil Service Commission maintains these)
3. Flag discrepancies:
   - Workday pay grade ≠ board-approved pay grade
   - FLSA status not set or incorrect
   - EEO category blank or wrong
   - Duties in spec significantly different from what employees actually do
4. Correct discrepancies in Workday (change Job Profile fields)
5. Document changes made

---

## Reclassification Process

A reclassification occurs when:
- An employee's duties have expanded beyond their current classification ("upward reclassification")
- An employee's duties have contracted ("downward reclassification" — rare but occurs in RIFs)
- A classification title/spec is being revised for all incumbents ("reclass of the class")

### Reclassification Request Workflow

**Step 1: Request initiated**
- Employee or supervisor submits reclassification request with:
  - Current classification and duties
  - Description of new/changed duties (using Position Description Questionnaire, PDQ)
  - Justification for why current class no longer fits
  - Supervisor signature

**Step 2: HR desk audit**
- HR Analyst reviews PDQ
- Compares to current class spec and candidate classes
- May conduct interview with employee and supervisor
- Determines: justified / not justified / needs more information

**Step 3: Civil service or classification review** (if applicable)
- In counties with a Civil Service Commission or Classification Review Committee:
  submit recommendation for formal approval

**Step 4: Implement in Workday** (if approved)
- Navigate: Staffing > Change Job
- Select: Change Job Reason = Reclassification
- Update: Job Profile, Compensation Grade, FLSA status
- Effective date: typically first day of next pay period

**Step 5: Pay adjustment**
- Determine new pay rate within new grade (usually step 1 of new grade, or maintain current pay if already above)
- Process via Compensation > Request Compensation Change

**Step 6: Civil service notification** (if applicable)
- Some civil service systems require employee to take a new exam or be placed on an eligibility list for the new classification

### Workday Change Job — Required Fields for Reclassification

| Field | What to Enter |
|---|---|
| Effective Date | First day of next pay period |
| Reason | Reclassification (use standardized reason code) |
| Job Profile | New classification |
| Business Title | Update if different from job profile name |
| Compensation Grade | New grade tied to new classification |
| FLSA Status | Verify — may change (e.g., non-exempt promoted to exempt manager) |
| Default Weekly Hours | Verify — should match new classification |

---

## Position Description Questionnaire (PDQ)

The PDQ is the foundation of classification analysis. HR should maintain a standard county PDQ form. Key sections:

**Section 1 — Basic Information**
- Position title, department, supervisor, date

**Section 2 — Position Summary**
- 2–3 sentences describing the primary purpose of the position

**Section 3 — Essential Functions**
- List each major duty with estimated % of time
- Each duty should be specific enough that a stranger could understand what is done
- ADA NOTE: these are the essential functions for reasonable accommodation analysis

**Section 4 — Minimum Qualifications**
- Education, experience, licensure, certifications required to perform the job
- Distinguish "required" from "preferred" — "required" must be applied consistently

**Section 5 — Working Conditions**
- Physical demands, environment, equipment used
- ADA NOTE: these form the basis of physical requirement analysis for accommodations

**Section 6 — Supervision**
- Who does this position report to?
- Does this position supervise others? How many? What type of supervision?

**Section 7 — Signatures**
- Employee, supervisor, department head, HR

---

## New Classification Creation

When no existing classification fits a new role:

1. Write a draft class specification:
   - Title (follow county naming conventions)
   - General definition (1–2 sentences)
   - Distinguishing characteristics (how is this different from similar classes?)
   - Examples of duties (not exhaustive — use "such as" and "including but not limited to")
   - Minimum qualifications
   - Knowledge, skills, and abilities (KSAs)

2. Assign a pay grade:
   - Compare to similar positions in the county (internal equity)
   - Survey market data for the role (external competitiveness)
   - Determine exempt/non-exempt status under FLSA

3. Get approval:
   - Civil service commission or classification review board
   - Finance (budget authority for the pay grade)
   - Board (if new classification requires board action per charter)

4. Create in Workday:
   - Navigate: Staffing > Job Profiles > Create Job Profile
   - Complete all fields including EEO category and FLSA status
   - Assign to correct job family
   - Link to compensation grade

---

## Broadband vs. Step Classification Systems

### Step System (Most Common in County Government)

- Each grade has defined steps (e.g., Steps 1–10)
- Employee starts at Step 1 (or as specified by MOU for lateral transfers)
- Advances one step per year (merit or automatic per MOU)
- Pay within a step is the same for all incumbents at that step → no manager discretion
- Transparent and defensible; limited pay flexibility

#### Workday Configuration
- Create a Salary Plan with defined step amounts per grade
- Configure step advancement rules (automatic or merit-based)
- Workday auto-calculates step increase dates based on hire/last-advance date

### Broadband System (Less Common)

- Each grade has min/mid/max only; no defined steps
- Manager has discretion to pay anywhere within the band
- More flexible for recruiting and retention; harder to defend for pay equity

#### Workday Configuration
- Configure as a standard Compensation Grade with min/mid/max
- Enable Workday Pay Range Guideline (optional; provides recommended pay within range based on performance/tenure)

---

## Classification and FLSA — Critical Intersection

### Common FLSA Misclassification in County Government

| Role | Common Error | Correct Analysis |
|---|---|---|
| "Senior Clerk" | Classified exempt based on title | Non-exempt unless duties + salary test met |
| Department admin assistant to director | Treated as exempt | Non-exempt unless performing exempt-level work |
| Working supervisor (supervisor who also does frontline work) | Exempt assumed | May be non-exempt if management is not primary duty |
| IT analyst | Often misclassified non-exempt | Likely exempt under computer professional exemption if salary threshold met |
| Social worker / case manager | Varies | Learned professional exemption applies if advanced degree required for the work |
| Engineer | Exempt | Professional exemption — verify degree requirement in class spec |

> When in doubt on FLSA status, consult county counsel. Misclassifying a non-exempt employee
  as exempt means unpaid overtime claims going back 2–3 years under FLSA.

---

## Classification KPIs

| KPI | Target | Source |
|---|---|---|
| Job profiles with EEO category assigned | 100% | Job Profile audit report |
| Job profiles with FLSA status assigned | 100% | Job Profile audit report |
| Reclassification requests processed within 60 days | >90% | HR case tracking |
| Classification specs last reviewed | Within 3 years for all specs | Classification spec log |
| Positions where job profile doesn't match actual duties | 0 (ongoing audit) | Annual desk audit results |
| FLSA reclassification liability identified | $0 (resolved) | FLSA audit |
