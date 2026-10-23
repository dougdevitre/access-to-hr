# Performance Management, PIPs & Discipline — Workday County HR Reference

## Overview

Performance management in a county has two jobs: help people do good work, and build the
record that supports a fair decision when they do not. Civil service rules and MOUs usually
define the steps of discipline, who may impose it, and how it can be appealed. Workday holds
the review cycle, goals and the documents; the process itself must follow the rules that
apply to each employee.

> ⚠️ LEGAL NOTE: Educational information only, not legal advice. Discipline of classified
  or union-represented employees must follow civil service rules and the MOU/CBA. Check with
  your state labor agency or an employment attorney — for a county, usually the county
  counselor — before suspension, demotion or termination.

---

## The Performance Cycle

| Phase | Timing (typical) | Workday |
|---|---|---|
| Goal setting | Start of review year | Performance > Goals |
| Check-ins | Quarterly | Performance > Check-Ins (if configured) |
| Mid-year review | Optional | Performance > Manage Review Cycles |
| Annual review | End of review year | Performance > Manage Review Cycles |
| Calibration | Before ratings are final | Calibration (if licensed) |
| Merit link | After reviews close | references/compensation.md |

> Navigation based on standard Workday HCM. Tenant customization varies — verify in your environment.

### Launching a Review Cycle

1. Confirm the review template (ratings scale, competencies, comment fields)
2. Confirm eligibility rules (exclude employees hired after a cutoff date, on leave, or in probation if they have a separate review)
3. Start the cycle: Performance > Manage Review Cycles
4. Communicate deadlines to managers (see references/hr-communications.md)
5. Monitor completion weekly: Monitor > Business Process > In Progress
6. Close the cycle and lock ratings before merit processing

---

## Probationary Periods

- Most county civil service systems and MOUs set an initial probation period for new hires
  and often for promotions
- Track the end date in Workday on the worker record and send the manager a reminder 30 days before
- Probationary employees often have fewer appeal rights — but they are still protected from
  discrimination and retaliation
- Extensions must follow the rule that allows them; document the reason before the end date

---

## Coaching Before Discipline

Most performance problems are fixed by a clear conversation. Coach first unless the conduct
is serious (violence, theft, harassment, safety).

**Coaching conversation:**
1. State the expectation
2. Describe the gap with specific examples (dates, facts)
3. Ask for the employee's view
4. Agree on what changes and by when
5. Write a short note to file (date, topic, agreement)

---

## Performance Improvement Plan (PIP)

Use a PIP when coaching has not worked and the issue is performance, not misconduct.

### PIP Contents

| Section | Content |
|---|---|
| Expectations | The specific standards not being met, tied to the job description |
| Evidence | Examples with dates |
| Goals | Measurable targets |
| Support | Training, tools, check-in schedule |
| Duration | Usually 30, 60 or 90 days; long enough to show change |
| Consequence | What happens if goals are not met, consistent with policy and MOU |
| Signatures | Manager, employee (acknowledging receipt, not agreement), HR |

### Running the PIP

- Weekly or biweekly check-ins, documented
- Adjust support if a barrier appears
- If the employee raises a medical condition or need, pause and start the ADA interactive
  process — see references/employee-relations.md
- If the employee recently complained, took leave or filed a grievance, review timing with HR
  and counsel before starting or ending a PIP (retaliation risk)

---

## Progressive Discipline

A typical sequence (your civil service rules or MOU control):

| Step | Form | Notes |
|---|---|---|
| 1 | Documented verbal warning | Note to file |
| 2 | Written reprimand | Copy to employee and personnel file |
| 3 | Suspension | Unpaid suspensions of exempt employees need FLSA review `[VERIFY: 29 CFR 541.710 public-agency pay system rule]` |
| 4 | Demotion or termination | Pre-disciplinary notice and opportunity to respond for employees with property interest (*Loudermill*) — see references/offboarding-separation.md |

### Just Cause Checklist (Common in Labor Arbitration)

Before discipline, answer:
1. Did the employee know the rule and the consequence?
2. Is the rule reasonable and related to the job?
3. Was the matter investigated before discipline?
4. Was the investigation fair?
5. Is there substantial evidence?
6. Has the rule been applied consistently to others?
7. Is the penalty proportionate, considering the employee's record?

If any answer is "no" or "not sure," stop and talk with HR.

### Union-Represented Employees

- Investigatory interviews: Weingarten rights — see references/labor-relations.md
- Follow the MOU's notice, timeline and grievance steps exactly
- Many MOUs limit how long old discipline can be used; check before citing prior discipline

---

## Documentation in Workday

| Document | Category |
|---|---|
| Coaching note, written reprimand | Disciplinary |
| PIP | Disciplinary |
| Investigation report | Confidential — Investigation |
| Medical documentation | Confidential — Medical |

Path: Worker Profile > Documents > Add Document. Use the naming convention in
references/records-management.md.

**Missouri:** personnel records and performance ratings may be closed under the Sunshine Law
(RSMo 610.021(13)); names, positions, salaries and lengths of service are open.

---

## Performance KPIs

| KPI | Target | Source |
|---|---|---|
| Review completion by deadline | >95% | Workday review cycle report |
| Employees with current-year goals | >90% | Workday goals report |
| Probation end dates acted on before expiry | 100% | Workday probation report |
| PIPs with documented check-ins | 100% | HR case log |
| Discipline overturned on appeal or grievance | Track; aim for 0 | Labor relations log |
| Rating distribution by department | Review for outliers each cycle | Workday calibration report |

---

## Sources

Checked 2026-10-23.

- *Cleveland Board of Education v. Loudermill*, 470 U.S. 532 (1985): https://law.cornell.edu/supremecourt/text/470/532
- Missouri Attorney General, Sunshine Law booklet: https://oa.mo.gov/sites/default/files/missourisunshinelaw2020.pdf
