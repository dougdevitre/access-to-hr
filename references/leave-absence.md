# Leave Management, FMLA & Accruals — Workday County HR Reference

## Overview

Leave is where county HR most often meets legal exposure: FMLA, ADA accommodation, the
Pregnant Workers Fairness Act, workers' compensation, military leave and MOU leave terms can
all apply to one absence at once. Workday tracks the leave and the accruals; HR owns the
eligibility decision, the notices and the paper trail.

> ⚠️ LEGAL NOTE: Educational information only, not legal advice. Leave decisions turn on
  facts. Check with your state labor agency or an employment attorney — for a county, usually
  the county counselor — before denying leave, counting an absence against an employee, or
  ending employment during or after leave.

---

## FMLA — Core Rules

| Item | Rule | Source |
|---|---|---|
| Covered employers | "FMLA applies to all public agencies" — every county, regardless of size | DOL FMLA page |
| Employee eligibility | Worked for the employer at least 12 months; at least 1,250 hours in the past 12 months; at a location with 50+ employees within 75 miles | DOL FMLA page |
| Leave amount | Up to 12 weeks of unpaid, job-protected leave per year | DOL FMLA page |
| Military caregiver leave | Up to 26 workweeks in a single 12-month period to care for a covered servicemember | DOL Military Family Leave guide |
| Qualifying exigency | Up to 12 workweeks | DOL Military Family Leave guide |
| Health coverage | Group health benefits must be maintained during leave | DOL FMLA page |

> **Government note:** a county is a covered employer at any size, but an individual employee
> still has to meet the 50-employees-within-75-miles test. Small counties can be covered
> employers with employees who are not eligible. Check each request.

### FMLA Notice Deadlines

| Notice | When | Source |
|---|---|---|
| General notice | Posted for all employees; given to each new hire if there is no handbook | DOL Fact Sheet #28D |
| Eligibility notice | Within **5 business days** of the initial request for leave | DOL Fact Sheet #28D |
| Rights and responsibilities notice | Each time an eligibility notice is given | DOL Fact Sheet #28D |
| Designation notice | Within **5 business days** of having enough information to decide, absent extenuating circumstances | DOL Fact Sheet #28D |
| Medical certification | Employee's time to return it | `[VERIFY: 15 calendar days under 29 CFR 825.305(b)]` |

**Most common county failure:** leave is approved by a supervisor, nobody sends the
designation notice, and the time is never counted as FMLA. Make the Workday leave request
route to HR before approval.

---

## FMLA in Workday

1. **Create the leave:** Absence > Leave of Absence > Create
   - Leave type: FMLA (Continuous) or FMLA (Intermittent)
   - Enter first day of leave and estimated last day
2. **Attach notices:** Worker Profile > Documents > Add Document (Confidential — Medical category)
3. **Track intermittent time:** employees record FMLA time against the FMLA time-off type so
   the 12-week balance draws down accurately
4. **Run concurrently** with paid leave, WC or disability where policy and the MOU allow;
   create both records so balances are right
5. **Return:** Absence > Leave of Absence > Return Worker; collect fitness-for-duty
   certification if policy requires it and the employee was notified in advance

> Navigation based on standard Workday HCM. Tenant customization varies — verify in your environment.

### Leave Year Method

Choose one method and apply it to everyone: calendar year, fixed year, rolling forward from
first use, or rolling backward. Rolling backward is hardest to game and hardest to explain;
configure it in Workday rather than tracking it by hand. Changing methods requires notice to
employees `[VERIFY: 60-day notice requirement under 29 CFR 825.200]`.

---

## Leave Laws That Run Alongside FMLA

| Law | When it applies | Key point |
|---|---|---|
| ADA | Employee with a disability needs leave or a schedule change | Leave can be a reasonable accommodation even after FMLA is exhausted; start the interactive process. See references/employee-relations.md |
| Pregnant Workers Fairness Act (PWFA) | Known limitations related to pregnancy, childbirth or related conditions; employers with 15+ employees, including state and local governments; effective June 27, 2023 | Employer may not require leave if another reasonable accommodation would let the employee keep working |
| PUMP Act (FLSA) | Nursing employees, for one year after the child's birth | Reasonable break time and a private space that is not a bathroom; covers state and local government employees |
| Workers' compensation | Work-related injury | Run FMLA concurrently if qualifying; see references/workers-compensation.md |
| USERRA | Military service | Reemployment rights; see Missouri military leave in references/missouri-specific.md |

---

## Accrual Plans

County accruals are usually set by ordinance, personnel policy and each MOU. Workday must
mirror all three.

### Accrual Audit (Annually, and After Every New MOU)

1. Pull each Time Off Plan: Absence > Leave Plans > [select]
2. List accrual rate, cap, carryover, waiting period and payout rule
3. Compare line by line to the current policy and every MOU
4. Test three sample employees per plan (new hire, mid-tenure, at cap)
5. Fix the plan in a sandbox first; document the change and effective date

### Common Accrual Errors

| Error | Effect | Fix |
|---|---|---|
| MOU raised accrual rate; Workday plan not updated | Underpayment of leave; grievance | Accrual audit on every MOU signing |
| Cap applied at wrong point (per pay period vs. annual) | Lost hours | Confirm cap rule wording with labor relations |
| Part-time proration missing | Over-accrual | Use FTE-based eligibility rules |
| Leave payout rule not configured | Final pay errors | Align with references/offboarding-separation.md |

---

## Missouri — Leave Notes

- **Paid sick time:** the Missouri earned paid sick time requirement ended August 28, 2025
  (HB 567). County policy and MOUs now control.
- **Military, jury and voting leave:** see references/missouri-specific.md — several items
  there are still marked `[VERIFY]`.

---

## Leave KPIs

| KPI | Target | Source |
|---|---|---|
| Eligibility notice sent within 5 business days | 100% | HR leave log |
| Designation notice sent within 5 business days of sufficient information | 100% | HR leave log |
| Leave requests routed to HR before approval | 100% | Workday business process audit |
| Accrual plans audited against MOUs | Annually + each new MOU | HR admin log |
| Open leaves past expected return date with no update | 0 | Workday leave report |
| Intermittent FMLA balances reconciled | Quarterly | Workday absence report |

---

## Sources

Checked 2026-10-23.

- DOL, Family and Medical Leave (FMLA): https://www.dol.gov/general/topic/benefits-leave/fmla
- DOL, Fact Sheet #28 (FMLA): https://www.dol.gov/agencies/whd/fact-sheets/28-fmla
- DOL, Fact Sheet #28D, Employer Notification Requirements: https://www.dol.gov/agencies/whd/fact-sheets/28d-fmla-employer%20notification
- DOL, Military Family Leave under the FMLA: https://www.dol.gov/sites/dolgov/files/WHD/flsa/FMLA-Military-092225-public.pdf
- EEOC, What You Should Know About the Pregnant Workers Fairness Act: https://www.eeoc.gov/wysk/what-you-should-know-about-pregnant-workers-fairness-act
- DOL, Fact Sheet #73, FLSA Protections to Pump at Work: https://www.dol.gov/agencies/whd/fact-sheets/73-flsa-break-time-nursing-mothers
- MO DOLIR, Wages, Hours & Dismissal Rights FAQ: https://labor.mo.gov/wages-hours-dismissal-rights
