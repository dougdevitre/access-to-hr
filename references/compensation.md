# Compensation, Merit & Pay Equity — Workday County HR Reference

## Overview

County pay is set by a pay plan the board or commission adopts, modified by MOUs for
bargaining units, and limited by the budget. HR's job is to keep the pay plan current and
competitive, apply it consistently, and make sure Workday pays what the plan says. Most pay
disputes come from inconsistent placement at hire, out-of-date pay ranges, or merit increases
applied outside the rules.

> ⚠️ LEGAL NOTE: Educational information only, not legal advice. Pay decisions are subject
  to the Equal Pay Act, Title VII, FLSA, the MOU and the adopted pay plan. Check with your
  state labor agency or an employment attorney — for a county, usually the county counselor —
  before adopting a new pay practice or resolving a pay equity complaint.

---

## Pay Plan Structure

| Element | Description | Workday |
|---|---|---|
| Pay grade / range | Minimum, midpoint, maximum for each grade | Compensation > Compensation Plans / Grades |
| Steps (if step system) | Fixed increments within the grade | Grade profiles with steps |
| Job profile → grade | Each job profile maps to one grade | Job profile compensation |
| Pay rules | Placement at hire, promotion, demotion, reclassification | Policy + business process rules |
| Differentials | Shift, hazard, certification, bilingual, on-call | Allowance or one-time payment plans |

Step vs. broadband: see references/job-classification.md.

**Missouri:** every hourly rate in the plan must be at least the Missouri minimum wage
($15.00 per hour for 2026; public employers are now covered).

---

## Placement Rules (Write Them Down)

| Action | Common rule | Watch out |
|---|---|---|
| New hire | Minimum of range, or up to a set step for documented qualifications | Inconsistent above-minimum hires create equity gaps |
| Promotion | Greater of range minimum or a set percentage increase | Make sure the result is within the new range |
| Reclassification upward | Treated as promotion, or placed at nearest step with an increase | Follow the reclass rule in references/job-classification.md |
| Demotion | Within new range; red-circle rules if pay exceeds max | Board policy may decide |
| Lateral transfer | No change, unless range differs | |

Document the reason for any exception in the compensation business process comment.

---

## Merit / Annual Increase Cycle

1. **Budget:** confirm the approved increase pool with Finance (percentage of covered payroll)
2. **Rules:** eligibility (hire date cutoff, rating minimum, at-max employees), lump sum vs. base
3. **Bargaining units:** apply MOU increases separately; they may not be merit-based
4. **Configure:** Compensation > Merit > Create Merit Process
5. **Manager worksheets:** guidelines by rating; caps and floors
6. **Review:** HR checks outliers, budget totals and equity by group before approval
7. **Approve and load:** effective date aligned with a pay period start
8. **Audit first paycheck:** spot-check 10–20 employees

> Navigation based on standard Workday HCM. Tenant customization varies — verify in your environment.

---

## Market Review

- Choose a peer group (similar counties by population and budget, nearby cities, regional employers for hard-to-fill jobs)
- Use benchmark jobs with clear matches; avoid matching by title alone
- Compare range midpoints to market median; set a policy line (for example, 100% of market median)
- Review every 3–5 years in full; annually for hard-to-fill job families
- Present to the board with cost by fiscal year — see references/hr-budget-finance.md

---

## Compression and Inversion

| Problem | Signal | Response |
|---|---|---|
| Compression | Long-tenure employees paid near new hires | Tenure-based adjustment; review starting-pay rule |
| Inversion | Supervisor paid less than a subordinate | Review supervisor differential; check OT effects |
| Range penetration skew | Most employees at range minimum or maximum | Range is out of market or step progression is stalled |

Workday report: compa-ratio and range penetration by job profile and by tenure band.

---

## Equal Pay

- The Equal Pay Act covers virtually all employers; it prohibits sex-based pay differences
  for substantially equal work, with defenses for seniority, merit, quantity/quality of
  production, or a factor other than sex `[VERIFY: EPA defenses at eeoc.gov]`
- Filing deadline under the EPA: two years from the last discriminatory paycheck, three years
  for willful violations; no EEOC charge is required (EEOC)
- **Missouri** has its own pay equity statute `[VERIFY: Missouri pay discrimination statute section and remedies]`

Full analysis method: references/dei-pay-equity.md.

---

## Pay Transparency and Records

- **Missouri:** names, positions, salaries and lengths of service of county employees are open
  records under the Sunshine Law (RSMo 610.021(13)). Assume pay data can be requested.
- Posting pay ranges in job announcements is standard practice for counties and supports equity
- Keep the adopted pay plan and every amendment with the board action that approved it

---

## Compensation KPIs

| KPI | Target | Source |
|---|---|---|
| Ranges reviewed against market | Every 3–5 years full; annually for hard-to-fill | Comp study log |
| Average compa-ratio by job family | Near policy line (e.g., 0.95–1.05) | Workday compensation report |
| Employees below range minimum | 0 | Workday compensation report |
| Exceptions to placement rules, with documented reason | 100% documented | Comp BP audit |
| Merit cycle within approved budget | 100% | Finance reconciliation |
| Hourly rates at or above Missouri minimum wage | 100% | Annual January audit |

---

## Sources

Checked 2026-10-23.

- EEOC, Time Limits for Filing a Charge (Equal Pay Act timing): https://www.eeoc.gov/time-limits-filing-charge
- EEOC, Coverage — Business/Private Employers (EPA coverage): https://www.eeoc.gov/coverage-businessprivate-employers
- MO DOLIR, "Minimum Wage Increases to $15.00 per Hour for 2026": https://labor.mo.gov/news/press-releases/minimum-wage-increases-1500-hour-2026
- Missouri Attorney General, Sunshine Law booklet: https://oa.mo.gov/sites/default/files/missourisunshinelaw2020.pdf
