# Offboarding, Separation & Final Pay — Workday County HR Reference

## Overview

A separation touches payroll, benefits, retirement, security access, county property and
public records at once. In county government it can also trigger civil service appeal
rights or a grievance. A clean separation is a checklist, run the same way every time, with
the reason documented accurately.

> ⚠️ LEGAL NOTE: Educational information only, not legal advice. Involuntary separations of
  classified or union-represented employees carry due process and contract obligations.
  Check with your state labor agency or an employment attorney — for a county, usually the
  county counselor — before any involuntary termination, and before signing any separation
  or release agreement.

---

## Separation Types

| Type | Key questions before processing |
|---|---|
| Voluntary resignation | Written notice received? Last day confirmed? Rehire-eligible? |
| Retirement | LAGERS (or other plan) application timing coordinated? Leave payout rules? |
| Involuntary — performance or conduct | Civil service and MOU steps complete? Pre-termination notice and opportunity to respond given? Counsel reviewed? |
| Layoff / reduction in force | Board action? Seniority and bumping rules in MOU or civil service rules? Recall list? |
| End of temporary or seasonal appointment | End date in Workday? Any ACA measurement implications? See references/seasonal-temp-workforce.md |
| Death of employee | Final pay to estate or beneficiary per policy; life insurance and retirement notifications; COBRA for dependents |
| Job abandonment | Policy definition met? Written notice attempts documented? |

> **Government note:** in *Cleveland Board of Education v. Loudermill*, 470 U.S. 532 (1985),
  the Supreme Court held that a tenured public employee "is entitled to oral or written notice
  of the charges against him, an explanation of the employer's evidence, and an opportunity to
  present his side of the story" before termination. Whether a particular employee has that
  property interest depends on civil service rules, ordinance and contract — ask counsel.
  Skipping steps is a common reason a county loses a termination appeal.

---

## Separation Checklist

### Before the Last Day

1. Confirm separation type, last day worked and effective termination date
2. Involuntary: confirm counsel review and that every civil service/MOU step is documented
3. Notify payroll of the date and any leave payout
4. Notify benefits administration (COBRA, retirement, life insurance)
5. Schedule return of county property (keys, badge, laptop, phone, vehicle, uniforms, weapons)
6. Schedule access removal with IT for the end of the last shift

### On the Last Day

1. Collect property; document what was returned
2. IT disables network, email, building and Workday access
3. Deliver final pay or the date it will be paid
4. Provide benefits continuation information
5. Exit interview (voluntary separations) — see "Exit Interviews" below

### After the Last Day

1. Process termination in Workday (below)
2. Confirm final paycheck and leave payout were correct
3. Confirm COBRA notice was issued on time (see references/benefits.md)
4. Report the separation to LAGERS or other retirement plan as required
5. File separation documents in the personnel file
6. Remove from security groups (see references/system-administration.md)

---

## Workday — Terminate Employee

**Path:** Worker Profile > Actions > Terminate

| Field | Guidance |
|---|---|
| Termination date | Day after last day worked, or last day worked, per your tenant's convention — be consistent |
| Last day of work | The actual last day the person worked |
| Primary reason | Use a reason code that is accurate and defensible; it may be read in an unemployment hearing, a lawsuit or a public records request |
| Regrettable | Used for turnover analytics; set honestly |
| Eligible for rehire | Set per policy; document the reason when "No" |
| Pay through date | Confirm with payroll |
| Close position | Usually **No** — keep the position for backfill unless the board eliminated it |

> Navigation based on standard Workday HCM. Tenant customization varies — verify in your environment.

**Watch out:** the termination business process often triggers benefits end dates and COBRA
events automatically. Check the subprocess steps completed.

---

## Final Pay

### Missouri

Per MO DOLIR:
- **Discharge:** wages are due at the time of termination. If not paid, the former employee
  can send a written request by certified mail; the employer has **seven days** to respond, and
  can be liable for additional wages for up to **60 days**.
- **Resignation:** no specific Missouri deadline; wages unpaid by the next regular payday can
  be pursued through legal action.
- Whether the final-pay statute reaches counties is
  `[VERIFY: application of Missouri's final-pay statute to counties]` — see references/missouri-specific.md.

### Leave Payout

There is no federal requirement to pay out accrued leave. Payout follows county policy,
ordinance and each MOU. Check:
- Which plans pay out (vacation often does; sick leave often does not, or only at retirement)
- Caps on payout hours
- Comp time balances (public agencies) `[VERIFY: comp time payout rate at separation, 29 CFR 553.27]`

---

## Unemployment

- Separated employees may apply for unemployment. Respond to Missouri Division of Employment
  Security notices by the deadline on the notice.
- The termination reason code and supporting documents are the record the county will rely on.
- Separation notice to employees: `[VERIFY: whether Missouri requires employers to give separating employees a written notice of unemployment insurance availability, and the form number]`

---

## Separation and Release Agreements

- Draft only with county counsel.
- For employees 40 and older, a release of age discrimination claims has specific timing and
  disclosure requirements `[VERIFY: OWBPA consideration and revocation periods, 29 U.S.C. 626(f)]`.
- Board approval may be required for any payment; check county rules.
- Agreements may be public records under the Missouri Sunshine Law.

---

## Exit Interviews

- Offer to every voluntary separation; online survey plus optional conversation
- Ask: reason for leaving, what would have kept you, supervisor relationship, pay, workload
- Report themes quarterly by department (minimum group size of 5 to protect confidentiality)
- Feed into references/workforce-planning.md and references/hr-kpi-baseline.md

---

## Security and Access Removal

| System | Owner | Timing |
|---|---|---|
| Workday account | HRIS | Effective at termination; confirm daily report of terminated users with active accounts |
| Email / network | IT | End of last shift |
| Building badges, keys | Facilities | Last day |
| Criminal justice systems (law enforcement) | Agency terminal coordinator | Immediately |
| Purchasing cards, fuel cards | Finance | Last day |

See references/system-administration.md for the terminated-user security audit.

---

## Offboarding KPIs

| KPI | Target | Source |
|---|---|---|
| Workday termination processed within 1 business day of last day | >95% | Workday BP report |
| Terminated users with active system access | 0 | Security audit report |
| Final pay errors | 0 | Payroll correction log |
| COBRA notices issued on time | 100% | Benefits vendor report |
| Exit survey response rate (voluntary) | >50% | Survey tool |
| County property recovered | 100% | Offboarding checklist |

---

## Sources

Checked 2026-10-23.

- *Cleveland Board of Education v. Loudermill*, 470 U.S. 532 (1985): https://law.cornell.edu/supremecourt/text/470/532
- MO DOLIR, Termination / Final Wages: https://labor.mo.gov/dls/general/termination-final-wages
- MO DOLIR, Wages, Hours & Dismissal Rights FAQ: https://labor.mo.gov/wages-hours-dismissal-rights
- CMS, COBRA Continuation Coverage fact sheet (state and local government plans): https://www.cms.gov/cciio/programs-and-initiatives/other-insurance-protections/cobra_fact_sheet
- MO DOLIR, Quick Guide for New Employers (unemployment insurance): https://labor.mo.gov/new-employer
