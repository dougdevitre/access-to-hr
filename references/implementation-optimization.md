# Workday Optimization & Quick Wins — Workday County HR Reference

## Overview

Most counties use a fraction of what their Workday tenant can do. Optimization is the
steady work of finding manual steps, workarounds and unused features, and fixing them in
order of value. It is not a re-implementation. Start with the diagnostic in SKILL.md, pick a
few quick wins, measure the result, and repeat each quarter.

---

## Finding the Opportunities

### Sources of Optimization Ideas

| Source | What to look for |
|---|---|
| HR and payroll staff | Paper forms, spreadsheets, re-keying, email approvals |
| Managers | Steps that feel slow; approvals they don't understand |
| Business Process Monitor | Steps that routinely sit for days |
| Help desk tickets | Repeated questions on the same task |
| Integration error log | Recurring errors from the same source data |
| Audit findings | Controls done manually that Workday could enforce |

### Score Each Opportunity

| Factor | Score 1–3 |
|---|---|
| Hours saved per year | 1 = low, 3 = high |
| Compliance or error risk reduced | 1 = low, 3 = high |
| Employees affected | 1 = few, 3 = all |
| Effort (reverse: 3 = easy) | 1 = hard, 3 = easy |

Do the highest totals first. Anything scoring high on risk goes first regardless of effort.

---

## Quick Wins (Usually Under 30 Days)

| Quick win | Why | Related file |
|---|---|---|
| Remove Workday access for separated employees and run the audit monthly | Security and audit risk | references/system-administration.md |
| Schedule the top 5 monthly reports to run automatically | Saves staff time; consistent data | references/hr-kpi-baseline.md |
| Enable and promote the mobile app | Faster approvals; field staff access | references/change-management-adoption.md |
| Turn on approval delegation reminders | Fewer stuck transactions | references/system-administration.md |
| Route leave requests through an HR step | FMLA notice deadlines | references/leave-absence.md |
| Add an HR review of termination reason codes | Defensible records | references/offboarding-separation.md |
| Build a "Sunshine salary list" report with only open fields | Faster, safer **Missouri** records responses | references/missouri-specific.md |
| Certification expiration report, monthly | Prevents lapsed licenses | references/learning-development.md |
| Comp time balance report flagged at 90% of cap | FLSA cap compliance | references/time-tracking-payroll.md |

## Medium Projects (One Quarter)

| Project | Value |
|---|---|
| Accrual plan audit against every MOU | Pay accuracy; fewer grievances |
| Position control reconciliation process with Finance | Budget accuracy; no unfunded hires |
| Retire remaining paper forms in scope | Self-service rate up |
| Onboarding business process with full task list | Faster, compliant Day 1 |
| Manager dashboard (team headcount, time off, OT, open requisitions) | Fewer HR requests |
| Structured interview guides attached to requisitions | Consistent, defensible hiring |

## Larger Improvements (Two Quarters or More)

| Improvement | Notes |
|---|---|
| Workday Learning for required training | If licensed; replaces spreadsheets |
| Succession planning module | If licensed; critical positions first |
| Time tracking for all hourly staff (replacing paper or legacy clocks) | Needs union notice where scheduling or timekeeping changes affect working conditions |
| Pay equity analysis built as a repeatable report | With counsel |
| Integrations with retirement plan and carriers fully automated | Fewer manual files |

---

## Measuring the Result

For each change, record before and after:

| Measure | Example |
|---|---|
| Cycle time | Hire request to Day 1: 41 days → 30 days |
| Touches | HR data entry per hire: 6 → 2 |
| Error rate | Payroll corrections per period |
| Self-service rate | % of transactions started by employees and managers |
| Satisfaction | Manager pulse survey score |

The example numbers are illustrations only, not benchmarks. Use your own baseline.

---

## Common Reasons Optimization Stalls

| Reason | Response |
|---|---|
| No owner | Name one owner per project |
| Waiting for "the perfect design" | Ship a working version; iterate |
| Department exceptions | Configure real differences; standardize the rest |
| Fear of breaking payroll | Test in sandbox; schedule changes away from payroll close |
| No measurement | Pull a baseline before starting |

---

## Quarterly Optimization Rhythm

1. Review the opportunity list and scores
2. Close finished items and record results
3. Pick the next 3–5 items with owners and dates
4. Report progress to the HR Director (and board quarterly report, if relevant)

---

## Optimization KPIs

| KPI | Target | Source |
|---|---|---|
| Quick wins completed per quarter | 3–5 | Optimization log |
| Self-service rate | Up each quarter | Business process report |
| Manual workarounds remaining | Falling | Workaround inventory |
| Average business process cycle time (top 5 processes) | Falling | BP report |
| Payroll corrections per pay period | Falling | Payroll log |
