# Benefits, COBRA, ACA & Open Enrollment — Workday County HR Reference

## Overview

County benefits usually combine a group health plan (insured, self-funded or a pool), a
defined benefit retirement plan (in Missouri, often LAGERS), an optional deferred
compensation plan, and life and disability coverage. Workday holds eligibility and elections
and feeds carriers through integrations. Most benefits errors are eligibility errors or
integration errors.

> ⚠️ LEGAL NOTE: Educational information only, not legal advice. Plan documents control
  benefits. Government plans follow different federal rules than private plans in some areas
  (for example, COBRA for state and local government plans is administered by CMS, not DOL).
  Check with your benefits counsel, your state labor agency or an employment attorney — for a
  county, usually the county counselor — on any eligibility dispute.

---

## Government Plans — What Is Different

| Topic | Private employer | County government |
|---|---|---|
| ERISA | Usually applies | Governmental plans are generally exempt `[VERIFY: ERISA governmental plan exemption, 29 U.S.C. 1003(b)(1)]` |
| COBRA | DOL / ERISA | Public Health Service Act; CMS has jurisdiction for state and local government employers |
| Retirement | 401(k) common | Defined benefit plan (e.g., LAGERS) plus 457(b) deferred comp common |
| Plan changes | Employer decision | Often needs board or commission approval and budget action |
| Union contracts | Sometimes | Premium share and plan design may be bargained |

---

## COBRA (State and Local Government Plans)

Per the CMS COBRA fact sheet:

| Item | Rule |
|---|---|
| Covered employers | Group health plans of employers with 20 or more employees in the prior year; CMS administers COBRA for state and local government employers |
| Initial qualifying event | Covered employee's termination or reduction of hours |
| Other qualifying events | Death, divorce or legal separation, Medicare entitlement, dependent child losing eligibility |
| Duration | Usually up to 18 months; up to 29 months with a qualifying disability; up to 36 months after a second qualifying event |
| Premium | Up to 102% of plan cost; up to 150% during the disability extension months |
| Employer → plan administrator notice | Within 30 days of the qualifying event (for example, employee's death) |
| Administrator → beneficiaries | Within 14 days after the administrator receives notice |
| Beneficiary notice of divorce or similar event | Within 60 days |
| First premium | Within 45 days after the COBRA election |
| Election period | `[VERIFY: 60-day election period — not stated on the CMS fact sheet]` |

### COBRA in Workday

- The termination or reduction-in-hours event should start the COBRA event in Workday or in
  the COBRA vendor feed. Check the integration log weekly.
- When the county is both employer and plan administrator, the combined notice timeline is
  `[VERIFY: 44-day combined deadline when employer is plan administrator]`.
- Keep proof of mailing for every COBRA notice.

---

## ACA Employer Requirements

| Item | Rule | Source |
|---|---|---|
| Applicable large employer (ALE) | At least 50 full-time employees, including full-time equivalents, on average in the prior year | IRS ALE Information Center |
| Full-time employee | `[VERIFY: 30 hours/week or 130 hours/month, 26 CFR 54.4980H-1]` | — |
| Reporting | Form 1094-C (transmittal) and Form 1095-C (per employee) | IRS ALE Information Center |
| Due dates | `[VERIFY: current-year furnishing and filing deadlines at irs.gov]` | — |
| Affordability percentage | `[VERIFY: 2026 affordability percentage — IRS Revenue Procedure for 2026]` | — |

Variable-hour, seasonal and temporary employees: see references/seasonal-temp-workforce.md
for measurement periods.

### Workday ACA Setup Checks

- Every worker has an ACA status (full-time, variable-hour, seasonal)
- Measurement, administrative and stability periods match the county's written method
- 1095-C codes reconcile to actual offers of coverage before forms go out
- Run a test 1095-C file before year-end

---

## Open Enrollment

### Timeline (Typical)

| Weeks before OE | Task |
|---|---|
| 16–12 | Renewal from carriers; board approval of rates and plan changes |
| 10–8 | Configure new plan year in Workday (sandbox first); update rates and eligibility rules |
| 6 | Test elections for sample employees in each eligibility group |
| 4 | Communications launch (see references/hr-communications.md) |
| 0 | OE opens: Benefits > Open Enrollment event |
| +2–3 | OE closes; non-completers default per plan rules |
| +4 | Send carrier files; reconcile; confirm deductions for first pay period of new plan year |

### Common OE Errors

| Error | Effect | Prevention |
|---|---|---|
| Rates entered for wrong coverage tier | Wrong deductions | Two-person rate review |
| Eligibility rule excludes a bargaining unit | Employees can't enroll | Test one employee per unit |
| Dependent verification not required | Ineligible dependents on plan | Require documents for new dependents |
| Carrier file sent before corrections | Coverage mismatches | Reconcile before first file |

---

## Life Events

Common events: marriage, divorce, birth or adoption, loss of other coverage, change in
employment status. Employees request changes in Workday (Me > Benefits > Change Benefits).

- Enforce the plan's life-event window `[VERIFY: window length in your Section 125 plan document — commonly 30 days]`
- Require documentation (marriage certificate, birth certificate)
- Divorce: ex-spouse loses eligibility and is a COBRA qualified beneficiary

---

## Retirement Plans

### Missouri — LAGERS

- Coordinate eligibility on hire: positions that meet the county's LAGERS membership rule must
  be flagged in Workday `[VERIFY: current LAGERS membership hours threshold]`
- Report covered wages accurately each period; check the LAGERS integration for errors
- Do not quote benefit estimates; refer employees to LAGERS
- Retirement timing affects final pay and leave payout — see references/offboarding-separation.md

### Deferred Compensation (457(b))

- Annual contribution limits change each year `[VERIFY: current-year 457(b) limits at irs.gov]`
- Vendor handles investments; HR handles payroll deduction setup and eligibility

---

## Benefits Data Privacy

- Health plan enrollment and dependent information is confidential
- Self-funded health plans may bring HIPAA privacy obligations for the plan `[VERIFY: county plan's HIPAA status with benefits counsel]`
- **Missouri:** personnel records may be closed under the Sunshine Law (RSMo 610.021(13));
  coordinate any request for benefits data with county counsel

---

## Benefits KPIs

| KPI | Target | Source |
|---|---|---|
| OE completion rate | >95% active elections | Workday OE report |
| Carrier file errors per cycle | 0 unresolved after 5 days | Integration log |
| COBRA notices issued on time | 100% | COBRA vendor report |
| New hire benefits enrollment within window | >98% | Workday benefits report |
| 1095-C corrections after furnishing | Track trend; aim for 0 | ACA vendor log |
| Benefits cost per employee | Track trend | Finance |

---

## Sources

Checked 2026-10-23.

- CMS, COBRA Continuation Coverage fact sheet: https://www.cms.gov/cciio/programs-and-initiatives/other-insurance-protections/cobra_fact_sheet
- IRS, ACA Information Center for Applicable Large Employers: https://www.irs.gov/affordable-care-act/employers/aca-information-center-for-applicable-large-employers-ales
- Missouri Attorney General, Sunshine Law booklet: https://oa.mo.gov/sites/default/files/missourisunshinelaw2020.pdf
