# DEI, Pay Equity Analysis & EEO-4 — Workday County HR Reference

## Overview

For a county, equal employment opportunity work is grounded in law and in public trust:
Title VII, the ADA, the ADEA, the Equal Pay Act, the Pregnant Workers Fairness Act and the
Missouri Human Rights Act set the rules, and the EEO-4 report shows the public who the
county employs. This file covers the practical work — pay equity analysis, workforce
representation review and EEO-4 data quality — using Workday data.

Keep the work focused on fair process and equal opportunity for every applicant and
employee. Program design choices (for example, any preference based on a protected
characteristic) carry legal risk and need counsel review before adoption.

> ⚠️ LEGAL NOTE: Educational information only, not legal advice. Pay equity analyses can be
  discoverable. Many counties run them at the direction of counsel. Check with your state
  labor agency or an employment attorney — for a county, usually the county counselor —
  before starting an analysis, and before any pay adjustment based on its results.

---

## Who Is Covered

| Law | Threshold | Source |
|---|---|---|
| Title VII, ADA, GINA | 15+ employees for 20+ calendar weeks | EEOC coverage page |
| ADEA | 20-employee threshold does not apply to states and political subdivisions | *Mount Lemmon Fire District v. Guido* (2018) |
| Equal Pay Act | Virtually all employers | EEOC coverage page |
| PWFA | 15+ employees, including state and local governments | EEOC |
| EEO-4 report | State and local governments with 100+ employees; biennial | EEOC |
| **Missouri** Human Rights Act | `[VERIFY: 6+ employees, RSMo 213.010]` | — |

---

## Pay Equity Analysis — Method

### Step 1: Scope and Privilege

- Decide with county counsel whether the analysis is done under attorney-client privilege
- Define the question: equal pay for substantially equal work (EPA) and/or unexplained pay
  differences across groups in similar jobs (Title VII)

### Step 2: Pull the Data (Workday)

Compensation > Pay Equity Analysis, or a custom report with:

| Field | Purpose |
|---|---|
| Job profile, grade, step | Group similar work |
| Base pay (annualized) | Outcome |
| Hire date, time in job, time in grade | Legitimate factors |
| Prior relevant experience (if recorded consistently) | Legitimate factor |
| Performance rating (if merit pay) | Legitimate factor |
| FTE, union unit | Normalization and contract rules |
| Sex, race/ethnicity (self-identified) | Comparison groups |

**PII flag:** restrict this report to the analysis team. Never circulate employee-level
demographic pay data.

### Step 3: Group Similar Work

- Start with the same job profile; combine job profiles only when the work is substantially similar
- Separate bargaining units if pay is set by different MOUs

### Step 4: Analyze

- Small groups (under ~10): compare individuals directly; explain every gap with documented factors
- Larger groups: regression on pay with legitimate factors, then test the group variable
- Look at starting pay separately; most gaps start at hire

### Step 5: Explain or Fix

| Finding | Response |
|---|---|
| Gap explained by documented, job-related factors | Record the explanation |
| Gap explained by an undocumented exception | Fix the record or the pay |
| Unexplained gap | Pay adjustment plan with counsel; budget it |
| Root cause in placement rules | Change the rule — see references/compensation.md |

### Step 6: Prevent

- Apply written placement rules at hire and promotion
- Review every above-minimum offer
- Re-run the analysis annually and after each merit cycle

---

## EEO-4 Data Quality

The EEO-4 report is only as good as the job category on each job profile and the
self-identification data on each worker.

| Check | Workday report |
|---|---|
| Every job profile has an EEO-4 job category | Job profiles missing EEO category |
| Every job profile has the correct function code for the department | EEO function mapping |
| Workers with no self-identification on file | Worker demographics completeness |
| Full-time / part-time flags match actual schedules | Worker time type |

- Self-identification is voluntary; invite employees to complete or update it
- Do not assign race or ethnicity based on observation in Workday
- Current EEO-4 data elements and snapshot date: `[VERIFY: EEO-4 instruction booklet for the current cycle]`

---

## Workforce Representation Review

Compare the county workforce to the relevant labor market by job category:

1. Workday headcount by EEO-4 job category and group
2. Applicant flow and selection rates by step — see "Adverse Impact Check" in references/recruiting.md
3. Promotion and separation rates by group
4. Discipline rates by group

Use the results to find process problems (a test, a posting practice, an interview step).
Report aggregate results only, with minimum group sizes to protect individuals.

---

## Inclusive Workplace Practices (Process-Based)

- Post every vacancy, including internal promotions, with clear minimum qualifications
- Use structured interviews and diverse interview panels
- Offer accommodation at every stage of hiring
- Provide harassment-prevention and bystander training — see references/learning-development.md
- Translate key employee communications where the workforce needs it
- Track accommodation request turnaround — see references/employee-relations.md

---

## DEI & Pay Equity KPIs

| KPI | Target | Source |
|---|---|---|
| Pay equity analysis completed | Annually | HR/legal log |
| Unexplained pay gaps remaining after review | 0 | Pay equity analysis |
| Job profiles with EEO-4 category | 100% | Workday job profile report |
| Workers with self-ID on file | Track; invite annually | Workday demographics report |
| Selection rate review after high-volume hiring | 100% of large recruitments | Recruiting log |
| EEO-4 filed on time | Each cycle | HR admin log |

---

## Sources

Checked 2026-10-23.

- EEOC, Coverage — Business/Private Employers: https://www.eeoc.gov/coverage-businessprivate-employers
- *Mount Lemmon Fire District v. Guido*, No. 17-587 (U.S. Nov. 6, 2018): https://www.supremecourt.gov/opinions/18pdf/17-587_n7ip.pdf
- EEOC, What You Should Know About the PWFA: https://www.eeoc.gov/wysk/what-you-should-know-about-pregnant-workers-fairness-act
- EEOC, EEO Data Collections (EEO-4): https://www.eeoc.gov/data/eeo-data-collections
- EEOC, Time Limits for Filing a Charge: https://www.eeoc.gov/time-limits-filing-charge
