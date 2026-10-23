# Compliance Calendar, EEO, I-9 & OSHA — Workday County HR Reference

## Overview

County HR compliance is mostly a calendar problem: a known set of filings, postings, notices
and audits that come due on fixed dates or on fixed counts of days after an event. This file
lists the recurring items and the event-driven deadlines, with the Workday report that
supports each one.

> ⚠️ LEGAL NOTE: Educational information only, not legal advice. Deadlines change and some
  depend on facts. Confirm each date with the agency named, and check with your state labor
  agency or an employment attorney — for a county, usually the county counselor — when an
  item is missed or disputed.

---

## Annual Compliance Calendar

| When | Item | Source / Notes |
|---|---|---|
| January | Update pay rates for the new Missouri minimum wage, if changed ($15.00 for 2026) | MO DOLIR |
| By January 31 | Furnish Forms W-2 to employees and file W-2/W-3 with SSA | IRS |
| Early in year | Furnish and file ACA Forms 1095-C / 1094-C | `[VERIFY: current-year due dates at irs.gov]` |
| Annually | Review required federal and Missouri workplace posters | MO DOLIR posters page via labor.mo.gov/new-employer |
| Biennially (2025 cycle current) | EEO-4 report — state and local governments with 100+ employees | EEOC |
| Annually | FLSA exempt status audit | references/time-tracking-payroll.md |
| Annually | Accrual plan audit against MOUs | references/leave-absence.md |
| Annually | I-9 self-audit | references/records-management.md |
| Annually | Pay equity analysis | references/dei-pay-equity.md |
| Annually | Records retention review | references/records-management.md |
| Each plan year | Open enrollment, COBRA vendor review | references/benefits.md |
| Each new MOU | Leave, pay and scheduling configuration audit | references/labor-relations.md |

## Event-Driven Deadlines

| Event | Deadline | Source |
|---|---|---|
| New hire — Form I-9 Section 2 | Within 3 business days of the first day of employment (first day, if the job lasts less than 3 business days) | USCIS M-274 |
| New hire — Form I-9 Section 1 | `[VERIFY: no later than the first day of employment — USCIS M-274 section 3]` | — |
| New hire — Missouri new hire report | Within 20 calendar days of hire | Missouri DSS |
| I-9 inspection notice | Produce forms within 3 business days of the request | USCIS |
| FMLA leave request — eligibility notice | Within 5 business days | DOL Fact Sheet #28D |
| FMLA — designation notice | Within 5 business days of having enough information | DOL Fact Sheet #28D |
| COBRA — employer to plan administrator | Within 30 days of the qualifying event | CMS |
| COBRA — administrator to beneficiaries | Within 14 days of receiving notice | CMS |
| Missouri Sunshine Law request | Respond by end of 3rd business day after receipt (or explain delay) | RSMo 610.023.3 |
| EEOC charge filed against county | Respond by date on the notice | EEOC notice |
| Employee's deadline to file EEOC charge | 180 days; 300 days where a state agency enforces a similar law | EEOC |
| Employee's deadline to file with MCHR (Missouri) | 180 days | MCHR |

---

## EEO Coverage Thresholds

| Law | Coverage | Source |
|---|---|---|
| Title VII, ADA, GINA (race, color, religion, sex, national origin, disability, genetic information) | 15 or more employees for 20+ calendar weeks (this year or last) | EEOC coverage page |
| ADEA (age 40+) | For private employers, 20 or more employees; for states and political subdivisions, the 20-employee threshold does not apply | EEOC coverage page; *Mount Lemmon Fire District v. Guido* (2018) |
| Equal Pay Act | Virtually all employers | EEOC coverage page |
| PWFA | 15 or more employees, including state and local governments | EEOC |
| Missouri Human Rights Act | `[VERIFY: 6+ employees, RSMo 213.010]` | — |

---

## EEO-4 Report

- Required of state and local governments with 100 or more employees; a mandatory biennial
  data collection (EEOC)
- Data: full-time, part-time and new hires by job category, salary band, sex and race/ethnicity
  `[VERIFY: current EEO-4 data elements and snapshot date in the EEOC instruction booklet]`
- Workday: Reports > Equal Employment Opportunity; job category mapping must be set on every
  job profile
- Self-identification is voluntary for employees; never guess race or ethnicity in Workday

### Before Filing

1. Report job profiles missing an EEO-4 job category
2. Confirm full-time / part-time flags
3. Compare totals to payroll headcount for the snapshot period
4. Keep a copy of the filed report with the records retention schedule

---

## Form I-9 and E-Verify

- Form I-9 is required for every new hire, including temporary, seasonal and part-time employees
- Section 2 deadline: within 3 business days of the first day of employment (USCIS)
- Store I-9s separately from personnel files so they can be produced on inspection without
  the rest of the file
- Retention: keep until the date calculated on the form's retention line `[VERIFY: 3 years after hire or 1 year after separation, whichever is later — USCIS M-274 section 10]`
- **Missouri:** public employers are required to participate in a federal work authorization
  program `[VERIFY: RSMo 285.530 scope for counties]`. E-Verify supplements the I-9; it does
  not replace it.

Full self-audit steps: references/records-management.md.

---

## OSHA

- Per OSHA, in states without an OSHA-approved State Plan, "State and local government workers
  are not covered by federal OSHA." **Missouri** has no State Plan.
- Many Missouri counties still keep OSHA-style injury logs and safety programs as a best
  practice and for insurance and WC pool requirements. Confirm your county's obligations with
  county counsel and your WC carrier or pool.
- Detail: references/workers-compensation.md.

---

## Posters and Notices

- Federal and Missouri posters change; review annually and when laws change
- Post where employees actually see them, and electronically for remote staff
- FMLA general notice must be posted and given to new hires if there is no handbook (DOL)
- Missouri minimum wage summary posting is required (RSMo 290.522, per MO DOLIR)

---

## Compliance KPIs

| KPI | Target | Source |
|---|---|---|
| I-9 Section 2 completed within 3 business days | 100% | I-9 system report |
| Missouri new hire reports within 20 days | 100% | State reporting integration log |
| EEO-4 filed on time | Each cycle | HR admin log |
| Job profiles with EEO-4 category | 100% | Workday job profile report |
| Sunshine requests answered within 3 business days | 100% | Records request log |
| Compliance calendar items completed on time | 100% | HR compliance tracker |

---

## Sources

Checked 2026-10-23.

- USCIS, M-274 section 4.0, Completing Section 2: https://uscis.gov/i-9-central/form-i-9-resources/handbook-for-employers-m-274/40-completing-section-2-employer-review-and-verification
- USCIS, I-9 Retention and Storage: https://uscis.gov/node/41388
- Missouri DSS, New Hire Reporting: https://missouriemployer.dss.mo.gov/NewHireInfo.aspx
- EEOC, EEO Data Collections (EEO-4): https://www.eeoc.gov/data/eeo-data-collections
- EEOC, Coverage — Business/Private Employers: https://www.eeoc.gov/coverage-businessprivate-employers
- *Mount Lemmon Fire District v. Guido*, No. 17-587 (U.S. Nov. 6, 2018): https://www.supremecourt.gov/opinions/18pdf/17-587_n7ip.pdf
- EEOC, What You Should Know About the PWFA: https://www.eeoc.gov/wysk/what-you-should-know-about-pregnant-workers-fairness-act
- EEOC, Time Limits for Filing a Charge: https://www.eeoc.gov/time-limits-filing-charge
- Missouri Commission on Human Rights, File a Complaint: https://labor.mo.gov/mohumanrights/file-complaint
- DOL, Fact Sheet #28D: https://www.dol.gov/agencies/whd/fact-sheets/28d-fmla-employer%20notification
- CMS, COBRA fact sheet: https://www.cms.gov/cciio/programs-and-initiatives/other-insurance-protections/cobra_fact_sheet
- OSHA, State Plans: https://www.osha.gov/stateplans
- IRS, January 31 wage statement deadline: https://www.irs.gov/newsroom/january-31-wage-statement-deadline-reminder-for-employers
- Missouri Attorney General, Sunshine Law booklet: https://oa.mo.gov/sites/default/files/missourisunshinelaw2020.pdf
- MO DOLIR, 2026 Minimum Wage: https://labor.mo.gov/node/21616
- MO DOLIR, Quick Guide for New Employers: https://labor.mo.gov/new-employer
