# Time Tracking, FLSA, Comp Time & Payroll — Workday County HR Reference

## Overview

Wage-and-hour errors are the most common source of back-pay liability for counties, and they
are usually configuration errors, not bad intent: the wrong FLSA status on a job profile, a
comp time cap missing from a time-off plan, or a 7(k) work period set up as a 7-day week.
Workday calculates what it is told to calculate. HR's job is to make sure it is told the
right thing.

> ⚠️ LEGAL NOTE: Educational information only, not legal advice. FLSA status and overtime
  questions depend on actual duties and pay. Check with your state labor agency or an
  employment attorney — for a county, usually the county counselor — before reclassifying
  a position as exempt or changing overtime practice.

---

## FLSA Basics for Counties

| Item | Rule | Source |
|---|---|---|
| Coverage | FLSA covers state and local government employees | DOL Fact Sheet #7 |
| Overtime | 1.5× regular rate for hours over 40 in a workweek (non-exempt), unless a 7(k) work period applies | DOL Fact Sheet #7, #8 |
| White-collar exemption salary level | $684 per week ($35,568 per year) | DOL Salary Levels page |
| Highly compensated employee level | $107,432 per year, including at least $684 per week | DOL Salary Levels page |
| Duties test | Salary alone is not enough; the job must meet an executive, administrative or professional duties test | DOL Fact Sheet #17A |
| Federal minimum wage | Applies with the higher state rate | DOL |

**Missouri:** the state minimum wage is $15.00 per hour for 2026, and public employers are
now subject to it. See references/missouri-specific.md.

---

## Compensatory Time (Public Agencies Only)

Per DOL Fact Sheet #7, public agencies may give comp time instead of cash overtime under
certain conditions:

| Rule | Detail |
|---|---|
| Rate | At least 1.5 hours of comp time per overtime hour worked |
| Cap — public safety, emergency response, seasonal | Up to 480 hours |
| Cap — all other employees | Up to 240 hours |
| Use | Employees must be allowed to use comp time on the date requested unless the agency's exception applies |
| Agreement | Comp time must be agreed to in advance `[VERIFY: agreement/MOU requirement in 29 CFR 553.23]` |
| Payout at separation | `[VERIFY: payout rate at separation under 29 CFR 553.27]` |

### Workday Configuration

- Build a Comp Time Earned time code that credits 1.5 hours per OT hour
- Set the plan maximum to 240 or 480 by eligibility group, and stop accrual (pay cash) once at cap
- Report: comp time balances by employee, monthly, flagged at 90% of cap
- Map each comp time group to the MOU that authorizes it

---

## FLSA § 7(k) — Law Enforcement and Fire

Per DOL Fact Sheet #8:
- A work period may be 7 to 28 consecutive days
- 28-day thresholds: **212 hours** (fire protection), **171 hours** (law enforcement)
- Shorter periods are prorated — for example, 14 days = **106 hours** (fire) or **86 hours** (law enforcement)
- Agencies with fewer than 5 employees in law enforcement or fire protection activities are exempt from overtime for those employees (Section 13(b)(20))

Full configuration guidance: references/public-safety-hr.md.

---

## Hours Worked — Common County Problem Areas

| Situation | Risk | Practice |
|---|---|---|
| Unpaid pre-shift briefings, equipment checks | Unpaid hours worked | Pay it; build a shift start that includes it |
| Mandatory training outside shift | Unpaid hours worked | Code as hours worked |
| On-call with tight response restrictions | May be hours worked | Review restrictions with counsel |
| Employees "volunteering" in their own job | Not a valid volunteer arrangement | Pay as hours worked `[VERIFY: 29 CFR 553.102 rule]` |
| Meal breaks interrupted by calls | Break may be compensable | Track interruptions in Workday |
| Exempt employee docked for partial day | May lose exemption | Review salary-basis rules before any deduction |

---

## Payroll Calendar Essentials

| Task | Timing | Source |
|---|---|---|
| Form W-2 to employees | By January 31 | IRS |
| Form W-2/W-3 to SSA | By January 31; extension requires Form 8809 and is not automatic | IRS |
| Missouri new hire report | Within 20 calendar days of hire | Missouri DSS |
| ACA Forms 1094-C/1095-C | Annual | `[VERIFY: current-year furnishing and filing due dates at irs.gov]` |
| FLSA payroll records retention | At least 3 years | DOL Fact Sheet #21 |
| Time cards and wage-rate tables retention | 2 years | DOL Fact Sheet #21 |

> Payroll tax calculation and actual payroll processing are out of scope for this skill.
  Route to the payroll lead or Finance.

---

## Timesheet Approval in Workday

1. Employee submits time: Me > Time > Enter Time
2. Manager approves: Team > My Team > Time > Review
3. Payroll locks the period after the approval deadline
4. Late changes go through a time correction with a reason code

**Watch-outs:**
- Approvers on leave: set up delegation so approvals do not stall
- Retroactive time changes after payroll: generate a correction, never edit the paid record
- Mixed exempt/non-exempt departments: confirm each job profile's FLSA status flag

---

## FLSA Status Audit (Annually)

1. Report all job profiles with FLSA status = Exempt
2. Confirm each salary is at or above $684/week
3. Spot-check duties against the job description and actual work
4. Flag any exempt employee whose pay was reduced for partial-day absences
5. Document findings and corrections; review with county counsel

---

## Time & Payroll KPIs

| KPI | Target | Source |
|---|---|---|
| Timesheets approved by deadline | >98% | Workday time report |
| Payroll corrections per pay period | Track trend; aim downward | Payroll log |
| Exempt job profiles audited | 100% annually | FLSA audit log |
| Comp time balances over 90% of cap | 0 without a plan | Workday absence report |
| Retroactive time corrections | Track trend | Workday audit report |

---

## Sources

Checked 2026-10-23.

- DOL, Fact Sheet #7, State and Local Governments under the FLSA: https://www.dol.gov/agencies/whd/fact-sheets/7-flsa-state-local-government
- DOL, Fact Sheet #8, Law Enforcement and Fire Protection under the FLSA: https://www.dol.gov/agencies/whd/fact-sheets/8-flsa-police-firefighters
- DOL, Overtime Salary Levels: https://www.dol.gov/agencies/whd/overtime/salary-levels
- DOL, Fact Sheet #17A, Exemptions for Executive, Administrative and Professional Employees: https://dol.gov/agencies/whd/fact-sheets/17a-overtime
- DOL, Fact Sheet #21, Recordkeeping under the FLSA: https://www.dol.gov/agencies/whd/fact-sheets/21-flsa-recordkeeping?lang=en
- IRS, January 31 wage statement deadline reminder: https://www.irs.gov/newsroom/january-31-wage-statement-deadline-reminder-for-employers
- Missouri DSS, New Hire Reporting: https://missouriemployer.dss.mo.gov/NewHireInfo.aspx
- MO DOLIR, "Minimum Wage Increases to $15.00 per Hour for 2026": https://labor.mo.gov/news/press-releases/minimum-wage-increases-1500-hour-2026
