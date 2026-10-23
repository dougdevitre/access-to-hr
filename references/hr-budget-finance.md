# HR Budget, Turnover Cost & Finance Partnership — Workday County HR Reference

## Overview

Personnel costs are usually the largest part of a county's operating budget. That makes HR
and Finance partners: HR owns the position, pay and benefits data; Finance owns the budget,
position control and the fund structure. Most budget surprises come from the gap between the
two — a position funded at the wrong step, a benefit rate that changed mid-year, or overtime
that nobody forecast.

---

## The Personnel Budget Build

| Component | Data source | Notes |
|---|---|---|
| Base pay by position | Workday positions + current pay; vacant positions at budgeted step | Reconcile to Finance position control |
| Scheduled increases | Step increases, MOU increases, merit pool | Effective dates matter — partial-year cost |
| Overtime | Prior 3 years by department, adjusted for vacancies and events | Separate public safety |
| Employer taxes | Social Security/Medicare where applicable, unemployment | `[VERIFY: whether your county participates in Social Security (Section 218 agreement)]` |
| Retirement | LAGERS (**Missouri**) or other plan employer rate × covered payroll | Rates set by the plan; confirm each year |
| Health and other benefits | Employer premium share × enrolled tiers | Use renewal rates; plan for mid-year changes |
| Workers' compensation | Pool or carrier premium | See references/workers-compensation.md |
| Leave payouts | Retirements and separations expected | Large one-time costs; estimate from eligibility |
| Vacancy factor | Expected savings from turnover | Use historical vacancy rate by department |

---

## Position Control Reconciliation

Run at least quarterly, and before every budget submission.

1. Export Workday positions (filled and vacant) with department, fund, job profile and FTE
2. Export Finance's authorized position list
3. Match by position ID
4. Investigate: in Workday not Finance; in Finance not Workday; FTE or fund mismatches
5. Correct the system of record; document board actions for any change

**Watch out:** grant-funded positions often have end dates and split funding. Track the
funding source and end date on the position record.

---

## Cost of Turnover

Use a simple, explainable model. Show assumptions; do not claim precision.

| Cost element | How to estimate |
|---|---|
| Separation | HR and payroll time to process; leave payout |
| Vacancy | Overtime or temporary staff to cover; lost service |
| Recruiting | Advertising, testing, background checks, staff time |
| Onboarding and training | Training hours × wage; equipment; certification |
| Lost productivity | Months to full productivity × percentage below full |

Present as a range per job family (for example, a patrol officer vs. a clerk) built from your
own data. Avoid quoting a generic "percentage of salary" benchmark unless you can cite its
source and year.

---

## Overtime Management

| Step | Detail |
|---|---|
| Measure | OT hours and dollars by department, job and person, monthly |
| Find drivers | Vacancies, leave, events, minimum staffing rules, scheduling |
| Act | Fill vacancies, adjust schedules, approve OT in advance, cross-train |
| Watch | Individual OT outliers (fatigue, safety, and pension-spiking risk where the plan counts OT) |

Workday: payroll results by earning code; time reports by department.

---

## Costing Changes for the Board

For any proposal (pay adjustment, new position, reclassification, MOU change):

| Item | Show |
|---|---|
| Annual cost | Base pay + benefits + taxes + retirement |
| First-year cost | Prorated from effective date |
| Multi-year cost | 3–5 years with scheduled increases |
| Fund | General fund vs. special revenue vs. grant |
| Offsets | Overtime reduction, vacancy savings, grant revenue |
| Risk of not acting | Turnover, overtime, service impact |

Labor proposal costing: see references/labor-relations.md.

---

## HR Department Budget

| Line | Typical items |
|---|---|
| Personnel | HR staff pay and benefits |
| Systems | Workday subscription, integrations, add-on modules — see references/vendor-hr-technology.md |
| Recruiting | Job boards, testing, background checks |
| Training | Required training, supervisor program, tuition assistance |
| Legal and investigations | Outside investigators, employment counsel (if budgeted in HR) |
| Employee programs | EAP, recognition, wellness |
| Compliance | Posters, I-9/E-Verify tools, ACA reporting vendor |

---

## Finance Partnership Rhythm

| Frequency | Meeting / output |
|---|---|
| Monthly | Personnel spend vs. budget by department; OT report; vacancy report |
| Quarterly | Position control reconciliation; forecast update |
| Budget season | Personnel budget build; costing of requests |
| Mid-year | Benefits rate changes; MOU settlements; reforecast |
| Year-end | Leave liability; accrued payroll; W-2 and ACA readiness |

---

## Budget & Finance KPIs

| KPI | Target | Source |
|---|---|---|
| Personnel spend vs. budget | Within ±2% | Finance |
| Position control mismatches | 0 after reconciliation | Reconciliation log |
| Overtime as % of payroll by department | Track trend; set local target | Payroll results |
| Turnover cost estimate updated | Annually | HR analytics |
| Board requests with full multi-year costing | 100% | Board packet review |
| Accrued leave liability | Track trend | Finance year-end |
