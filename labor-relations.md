# Labor Relations & Collective Bargaining — Workday County HR Reference

## Overview

Labor relations is the most legally sensitive area of county government HR. Union contracts
(MOUs/CBAs) govern wages, hours, and working conditions for represented employees. Workday
must be configured to reflect the current MOU — not HR's preference, not past practice, not
a prior MOU. Labor relations missteps trigger grievances, unfair labor practice (ULP) charges,
and arbitration.

> ⚠️ LEGAL NOTE: Collective bargaining is governed by Missouri public sector labor law
  (RSMo § 105.500–105.530), federal law where applicable, and the specific MOU language.
  All bargaining strategy and ULP responses must involve the county counselor or labor counsel.
  This guide covers the operational/Workday dimensions — not bargaining strategy.

---

## Missouri Public Sector Labor Law

### Governing Statute
**RSMo § 105.500–105.530** — Missouri Public Sector Labor Relations Act

### Key Provisions

| Provision | Summary |
|---|---|
| Right to organize | Public employees may form and join labor organizations |
| Duty to bargain | County must bargain in good faith over wages, hours, and conditions |
| No strike | Public employees prohibited from striking |
| Impasse resolution | Mediation through State Board of Mediation; no binding arbitration mandate in MO |
| ULP process | Unfair labor practice charges filed with State Board of Mediation |
| Recognition | Union certified as exclusive representative through election or card check |

### What Must Be Bargained ("Mandatory Subjects")

- Wages and salary schedules
- Hours of work (schedules, shifts, overtime rules)
- Vacation, sick leave, and other leave
- Grievance procedures
- Health and retirement benefits (in many cases)
- Disciplinary procedures
- Layoff and recall procedures

### What is Reserved to Management ("Management Rights")

Most MOUs include a management rights clause preserving the county's right to:
- Direct the workforce
- Determine services to be provided
- Establish work standards and performance expectations
- Hire, promote, transfer, and assign employees
- Discipline for just cause

> Management rights are not unlimited — exercise of rights that affects wages, hours, or
  conditions may trigger the duty to bargain before implementation (i.e., notice and meet-and-confer).

---

## Contract Administration — Workday Implications

### MOU Compliance Audit (Do This When a New MOU Is Signed)

Every time an MOU is negotiated or renewed, HR must audit Workday to ensure configuration matches:

**Leave and Absence**
- [ ] Sick leave accrual rate matches new MOU
- [ ] Vacation accrual rate and schedule matches
- [ ] Vacation accrual cap matches new MOU (common negotiation point)
- [ ] Bereavement leave duration and eligible relatives match
- [ ] Comp time accrual and cap match
- [ ] Holiday list matches MOU Exhibit

**Compensation**
- [ ] Pay grade minimums, steps, and maximums match new salary schedule
- [ ] Step advancement rules (automatic vs. merit) match MOU
- [ ] Shift differential rates match MOU
- [ ] Standby/callback pay minimums match MOU
- [ ] Longevity pay (if any) correctly configured

**Scheduling and Time**
- [ ] FLSA work period matches MOU
- [ ] Overtime threshold matches FLSA + MOU
- [ ] Shift bidding rules accommodated in schedule management

**Benefits**
- [ ] Health insurance contribution split (employer/employee) matches MOU
- [ ] Benefits eligibility (waiting period for new hires) matches MOU
- [ ] Retirement contribution rates match MOU

**Discipline**
- [ ] Discipline procedure steps reflected in HR policy (Workday doesn't enforce, but HR must)
- [ ] Just cause standard documented and understood by all managers

> After each MOU audit, produce a written summary of all Workday configuration changes made.
  This creates an audit trail and helps defend against grievances alleging contract violations.

---

## Grievance Tracking System

Workday does not have a native grievance management module. HR needs a separate system.
At minimum, maintain a grievance log with:

| Field | Description |
|---|---|
| Grievance Number | Sequential; e.g., GR-2025-001 |
| Date Filed | Date grievant submitted grievance |
| Grievant Name | Employee filing the grievance |
| Bargaining Unit | Which union |
| Issue | Brief description of alleged contract violation |
| Contract Article | Specific MOU section alleged violated |
| Step | Current grievance step (1, 2, 3, Arbitration) |
| Step Due Date | Deadline for county response at current step |
| County Response Date | When county responded |
| Outcome | Sustained / Denied / Settled / Withdrawn |
| Arbitration | Yes/No; arbitrator name if yes |
| Arbitration Outcome | County won / Lost / Split |
| Cost | Legal fees + settlement amount |

### Grievance Log Tools

- At minimum: shared Excel spreadsheet or Google Sheet accessible to HR Director and legal
- Better: a case management system (Salesforce, ServiceNow, or even Airtable)
- Never: tracking in Workday worker profile notes (creates discovery risk if file is pulled)

### Statute of Limitations for Grievances

Most MOUs require the grievance to be filed within **5–10 calendar days** of the incident or
when the employee should have known about it. HR must know and enforce this timeline — late
grievances may be dismissed.

---

## Unfair Labor Practice (ULP) Prevention

### Common County Government ULPs

| Action | ULP Risk | Prevention |
|---|---|---|
| Making a change to wages/hours without bargaining | Failure to bargain — most common ULP | Trigger notice + meet-and-confer before any policy change affecting represented employees |
| Threatening employees who engage in protected activity | Interference with organizing rights | Manager training; zero tolerance |
| Bypassing the union to deal directly with employees on bargaining topics | Surface bargaining / bypass | All communication on mandatory subjects goes through the union table |
| Denying Weingarten rights (union rep at investigative interview) | ULP | Train all supervisors on Weingarten |
| Retaliating against a union steward for their representation activities | Discrimination | Document all actions; consult legal before any discipline of a steward |
| Unilaterally changing past practice | Failure to bargain | Before changing any longstanding practice affecting represented employees, notice union and meet-and-confer |

### The "Notice and Meet-and-Confer" Protocol

Before implementing any policy that could affect wages, hours, or conditions for represented employees:

1. Provide written notice to the union (typically 30 days)
2. Offer to meet and confer (discuss, but not necessarily agree)
3. If union requests bargaining, you must bargain before implementing
4. Document all communications in the labor relations file

---

## Negotiation Support — Workday Data

When preparing for contract negotiations, Workday provides critical data:

### Costing a Union Proposal

When the union proposes a wage increase, Workday data enables accurate costing:

1. Pull **Compensation by Employee** report (filter to bargaining unit)
2. Export: Name, classification, current salary, step, FTE
3. Apply proposed increase: % increase or step advancement
4. Calculate total cost increase (salary + benefits load)
5. Identify secondary effects (step advancement could push employees above grade max)

### Workday Reports for Negotiations

| Report | Use in Negotiations |
|---|---|
| Compensation Summary by Org | Cost current proposals |
| Turnover by Reason | Quantify retention problem driving wage demands |
| Leave Balance Report | Value accrued leave liability (leave payout proposals) |
| Overtime Report | Cost overtime vs. hiring proposals |
| Headcount Trend | Document staffing levels over contract period |
| Time to Fill | Demonstrate recruiting difficulty (market pay arguments) |
| Absence Rate | Counter union claims about workload/staffing |

---

## Multi-Unit Environments

Most county governments have multiple bargaining units. Common structure:

| Unit | Union | Key Issues |
|---|---|---|
| Law enforcement (sworn) | FOP, Teamsters, MCPOA | Pension, OT, discipline, body cam policy |
| Detention officers | AFSCME, Teamsters | Safety staffing ratios, OT, use of force |
| Public works / maintenance | AFSCME, Laborers | Wages, safety, prevailing wage |
| Clerical / administrative | AFSCME | Wages, reclassification, remote work |
| Social services / case management | AFSCME, SEIU | Caseload, wages, supervision |

### Workday Configuration for Multiple Units

- Create a custom field on Position: **Bargaining Unit** (dropdown with each unit + "Unrepresented")
- This enables filtering of all compensation and workforce reports by unit
- Ensures MOU-specific leave plans are assigned to the correct employee population

---

## Weingarten Rights — Supervisor Quick Reference Card

> Print this and include in manager onboarding.

**What they are:** Union employees have the right to have a union representative present at any investigative interview they reasonably believe could result in discipline.

**When they apply:** Any interview conducted by a supervisor or HR where the employee could reasonably believe discipline might result.

**Trigger:** Employee must request the representative — the employer does not have to offer proactively (though best practice is to advise the employee of the right).

**What happens when requested:**
- Allow the employee to contact their union rep
- Give the rep a brief explanation of the subject matter
- Allow the rep to clarify questions and assist the employee
- The rep cannot answer questions for the employee or obstruct the interview

**What happens if you deny the request:**
- Employee can refuse to answer without their rep
- County commits a ULP
- Investigation results may be unusable in discipline proceedings

**What Weingarten does NOT require:**
- A rep present at a witness interview (non-investigative)
- A rep at a termination notification (decision already made)
- A rep at a performance review (not an investigation)

---

## Labor Relations Calendar

| Timing | Event | Action |
|---|---|---|
| 90 days before MOU expiration | Begin preparation for negotiations | Pull costing data from Workday; identify county priorities |
| 60 days before expiration | Open negotiations (or per MOU notice requirement) | First bargaining session |
| MOU expiration | If no agreement: status quo or impasse | Notify State Board of Mediation if impasse |
| MOU ratification | New contract signed | Immediate Workday config audit (see above) |
| Annually (January) | Review all grievance outcomes | Update training; identify patterns |
| Annually (March) | Update manager Weingarten training | Incorporate any new case law |

---

## Labor Relations KPIs

| KPI | Target | Source |
|---|---|---|
| ULP charges filed | 0 per year | State Board of Mediation records |
| Grievances filed per 100 represented employees | <5/year | Grievance log |
| Grievances resolved at Step 1 or 2 | >70% | Grievance log |
| Arbitrations lost | <30% of cases that go to arbitration | Grievance log |
| Workday config updated within 30 days of MOU ratification | 100% | HR project log |
| Manager Weingarten training completion | 100% of supervisors annually | Learning campaign report |
| MOU compliance audit completed within 60 days of ratification | Yes/No | HR project log |
