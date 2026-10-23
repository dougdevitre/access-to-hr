# Missouri-Specific Law & Rules — Workday County HR Reference

## Overview

This file collects the Missouri rules that most often change the answer for a Missouri
county. Federal law sets the floor; Missouri law, county ordinance, civil service rules and
MOUs/CBAs can add to it. When two rules apply, follow the one that gives the employee more.

Everything in this file is labeled **Missouri**. Figures marked `[VERIFY: ...]` could not be
confirmed against an official source when this file was drafted; confirm them before relying
on them.

> ⚠️ LEGAL NOTE: Educational information only, not legal advice. Missouri statutes change
  most years (new laws usually take effect August 28). Check with your state labor agency
  (Missouri Department of Labor and Industrial Relations) or an employment attorney — for a
  county, usually the county counselor — before acting on any rule here.

---

## Missouri — Minimum Wage

| Item | Rule | Source |
|---|---|---|
| 2026 minimum wage | $15.00 per hour, effective January 1, 2026 | MO DOLIR press release |
| Annual CPI adjustment | Ended — HB 567 (2025) removed the annual Consumer Price Index adjustment | MO DOLIR press release |
| Public employers | "Public employers previously exempted are now subject to the Missouri minimum wage law" | MO DOLIR press release |
| Tipped employees | At least half the minimum wage ($7.50/hour) plus tips; employer makes up any shortfall to $15.00 | MO DOLIR 2026 minimum wage page |
| Retail/service exemption | Retail or service businesses with annual gross income under $500,000 are not required to pay the state minimum | MO DOLIR 2026 minimum wage page |

**What this means for a county:** pay rates for seasonal, part-time, election-worker,
youth and temporary positions must meet $15.00 per hour. Audit every pay grade step and hourly
rate in Workday (Compensation > Compensation Plans) against the current rate each January.

> Federal minimum wage still applies too. Where Missouri's rate is higher, pay the higher rate.

---

## Missouri — Earned Paid Sick Time (Repealed)

- Proposition A (2024) created a state earned paid sick time requirement.
- HB 567 (2025) repealed it. Per MO DOLIR: employers "are no longer required to do so beginning
  Aug. 28, 2025," and "may continue to offer employees earned paid sick time."
- **County action:** sick leave now follows county policy, ordinance and MOUs. If your county
  built a separate Prop A accrual plan in Workday, decide (with counsel and any unions) whether
  to keep, merge or retire it, and document the decision.

---

## Missouri — Final Pay

Statute: `[VERIFY: section number — commonly cited as RSMo 290.110; MO DOLIR's page does not cite it]`

Per MO DOLIR:
- **Discharge:** "Wages are due at the time of termination."
- If not paid, the former employee may send a written request by certified mail; the employer
  then has **seven days** to respond. An employer that does not pay can be liable for
  additional wages for up to **60 days**.
- **Resignation:** Missouri law has no specific deadline; wages not paid by the next regular
  payday can be pursued through legal action.
- The state does not collect wages for individuals; claims go through private action
  (small claims under $5,000).

**Public employers:** MO DOLIR's final-wage page does not say whether RSMo 290.110 reaches
counties. `[VERIFY: whether the final-pay statute applies to Missouri counties — ask county counselor]`
Best practice either way: pay final wages on or before the next regular payday, and pay on
the separation date for involuntary terminations when payroll timing allows.

See references/offboarding-separation.md for the Workday steps.

---

## Missouri — Service Letter (RSMo 290.140)

Per MO DOLIR, an employee who worked **more than 90 days** for a **corporation** with **seven
or more employees** may request, by certified mail, a letter stating the type of work, length
of employment and the true reason for discharge.

- The statute is written for corporations. Whether it reaches a county is
  `[VERIFY: RSMo 290.140 application to counties]`.
- If a request arrives, route it to HR Director and county counselor the same day; the
  response is time-limited `[VERIFY: response deadline under RSMo 290.140]`.

---

## Missouri — Human Rights Act (MHRA, RSMo Chapter 213)

| Item | Rule | Status |
|---|---|---|
| Deadline to file with the Missouri Commission on Human Rights (MCHR) | 180 days from the alleged discrimination | Verified (MCHR) |
| Federal comparison | 300 days to file with EEOC where a state agency enforces a similar law | Verified (EEOC) |
| Employer size | 6 or more employees in Missouri | `[VERIFY: RSMo 213.010 employer definition]` |
| Damage caps by employer size (2017 amendments) | Caps on actual + punitive damages, scaled by headcount | `[VERIFY: RSMo 213.111.4 cap amounts]` |
| Civil action timing after right-to-sue | Time limits apply | `[VERIFY: RSMo 213.111.1 deadlines]` |

**HR actions:**
- Any MCHR or EEOC charge goes to HR Director and county counselor the day it arrives.
- Issue a litigation hold (see references/records-management.md).
- Calendar the position-statement deadline on the notice.

---

## Missouri — Sunshine Law (RSMo Chapter 610)

From the Missouri Attorney General's Sunshine Law booklet (text of Chapter 610):

| Rule | What it says |
|---|---|
| § 610.021(13) | Individually identifiable personnel records, performance ratings and records pertaining to employees and applicants **may be closed** — but **not** the names, positions, salaries and lengths of service of officers and employees |
| § 610.021(3) | Meetings may be closed for hiring, firing, disciplining or promoting particular employees when personal information is discussed; any final vote must be made public within **72 hours** with how each member voted |
| § 610.023.3 | Respond as soon as possible, no later than the **end of the third business day** after the custodian receives the request; if not immediate, explain the delay and give the earliest available date and time |

**HR checklist for a records request:**
1. Log date and time received; identify the custodian of record.
2. Pull only what was requested.
3. Separate open fields (name, position, salary, length of service) from closable records.
4. Redact SSN, medical information and other information closed by law.
5. Have county counselor review closures before release.
6. Respond (or explain the delay) by end of the third business day.

Workday report outputs (headcount, salary lists) are often requested. Build a "Sunshine
salary list" report that contains only the open fields, so staff never export extra data by
accident.

---

## Missouri — New Hire Reporting

- Report newly hired employees **within 20 calendar days** of the hire date (Missouri DSS
  employer site, citing RSMo 285.300–285.308 and 42 U.S.C. 653a).
- Anyone who completes a W-4 must be reported.
- Most Workday tenants send this through a payroll or state-reporting integration. Check the
  integration's error log monthly.

---

## Missouri — Leave Laws to Confirm

These Missouri leave rules commonly affect counties. Each needs confirmation of the current
statute text before it is used in policy or an answer.

| Leave | Status |
|---|---|
| Military leave for public employees | `[VERIFY: statute (believed RSMo 105.270), hours per year and pay status]` |
| Jury service — protection from discipline | `[VERIFY: statute (believed RSMo 494.460), protections and remedies]` |
| Time off to vote | `[VERIFY: statute (believed RSMo 115.639), hours and conditions]` |
| Crime victim / witness leave | `[VERIFY: whether a Missouri statute applies to counties]` |
| Domestic violence leave (Missouri VESSA) | `[VERIFY: statute section, employer size thresholds and leave amounts]` |

Until these are confirmed, answer leave questions in these areas with the county's written
policy and MOU, and route statutory questions to county counsel.

---

## Missouri — Workers' Compensation

Covered in detail in references/workers-compensation.md (RSMo Chapter 287). Missouri has no
OSHA-approved State Plan; per OSHA, "State and local government workers are not covered by
federal OSHA" in Missouri.

---

## Missouri — Retirement (LAGERS)

Many Missouri counties participate in the Missouri Local Government Employees Retirement
System (LAGERS). Contribution rates, vesting and eligibility depend on the benefit program the
county elected.

- Treat LAGERS plan documents and LAGERS staff as the authority; do not restate benefit
  formulas from memory.
- Workday tasks: correct eligibility flags on hire, accurate reporting of covered wages, and a
  monitored integration. See references/benefits.md.
- `[VERIFY: current LAGERS minimum service hours for membership eligibility]`

---

## Missouri — E-Verify for Public Employers

Missouri law requires public employers to enroll and participate in a federal work
authorization program `[VERIFY: RSMo 285.530 requirement and scope for counties]`. E-Verify
supplements Form I-9; it does not replace it. See references/compliance.md.

---

## Missouri — Peace Officers (POST)

Missouri POST licensing and continuing education are covered in references/public-safety-hr.md.

---

## Quick Reference — Missouri vs. Federal

| Topic | Federal | Missouri |
|---|---|---|
| Minimum wage | FLSA floor | $15.00/hour (2026); public employers now covered |
| Discrimination charge deadline | 180 days, extended to 300 with a state agency (EEOC) | 180 days to MCHR |
| Paid sick leave | None required | State requirement repealed Aug. 28, 2025 |
| New hire report | 20 days (federal floor) | 20 calendar days |
| Public records | — | Sunshine Law; 3 business days |
| OSHA for county employees | Not covered in non-State-Plan states | No State Plan |

---

## Sources

Checked 2026-10-23.

- MO DOLIR, "Minimum Wage Increases to $15.00 per Hour for 2026": https://labor.mo.gov/news/press-releases/minimum-wage-increases-1500-hour-2026
- MO DOLIR, 2026 Minimum Wage: https://labor.mo.gov/node/21616
- MO DOLIR, Termination / Final Wages: https://labor.mo.gov/dls/general/termination-final-wages
- MO DOLIR, Wages, Hours & Dismissal Rights FAQ (HB 567 sick time; service letter): https://labor.mo.gov/wages-hours-dismissal-rights
- Missouri Commission on Human Rights, File a Complaint: https://labor.mo.gov/mohumanrights/file-complaint
- EEOC, Time Limits for Filing a Charge: https://www.eeoc.gov/time-limits-filing-charge
- Missouri Attorney General, Sunshine Law booklet (Chapter 610 text): https://oa.mo.gov/sites/default/files/missourisunshinelaw2020.pdf
- Missouri DSS, New Hire Reporting: https://missouriemployer.dss.mo.gov/NewHireInfo.aspx
- OSHA, State Plans: https://www.osha.gov/stateplans
