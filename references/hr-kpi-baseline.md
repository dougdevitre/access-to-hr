# HR KPIs, Metrics & Dashboards — Workday County HR Reference

## Overview

A KPI is useful only if it is defined the same way every time, pulled from the same source,
and reviewed by someone who can act on it. This file defines the core county HR metrics,
how to calculate each one from Workday, and how to set a baseline before setting a target.

**Benchmarks:** this file does not publish industry benchmark numbers. Public-sector
benchmarks vary by source, year and county size. Set targets from your own baseline (one to
four quarters of data), then compare with peer counties or a published survey you can cite.

---

## Setting a Baseline

1. Pick the metric and write its definition (numerator, denominator, time period, exclusions)
2. Build or select the Workday report; save it with the definition in the description
3. Pull at least 4 quarters of history if available
4. Note anything unusual (a layoff, a hiring freeze, a system change)
5. Set a target only after the baseline is stable; record who approved it

---

## Core Workforce Metrics

| Metric | Formula | Workday source |
|---|---|---|
| Headcount | Active workers on the last day of period | Reports > Headcount by Organization |
| FTE | Sum of FTE for active workers | Headcount report with FTE field |
| Vacancy rate | Vacant funded positions ÷ total funded positions | Position report reconciled to Finance |
| Turnover rate (annual) | Separations in 12 months ÷ average headcount | Terminations report + headcount |
| Voluntary turnover rate | Voluntary separations ÷ average headcount | Terminations report by reason |
| First-year turnover | Separations within 12 months of hire ÷ hires in the period | Terminations by length of service |
| Retirement eligibility (next 5 years) | Workers eligible to retire within 5 years ÷ headcount | Requires retirement eligibility data — see references/workforce-planning.md |
| Average tenure | Mean years of service | Worker report |

## Talent Acquisition Metrics

| Metric | Formula | Workday source |
|---|---|---|
| Time to fill | Requisition approved → offer accepted (days) | Recruiting report |
| Time to hire | Application → offer accepted (days) | Recruiting report |
| Offer acceptance rate | Offers accepted ÷ offers extended | Offer report |
| Applicants per posting | Applications ÷ postings | Recruiting report |
| Hiring manager satisfaction | Survey score | Survey tool |

## Compensation & Benefits Metrics

| Metric | Formula | Workday source |
|---|---|---|
| Average compa-ratio | Pay ÷ range midpoint | Compensation report |
| Range penetration | (Pay − min) ÷ (max − min) | Compensation report |
| Overtime as % of payroll | OT pay ÷ total pay | Payroll results |
| Benefits cost per employee | Total employer benefits cost ÷ headcount | Finance + Workday |
| Open enrollment completion | Active elections ÷ eligible workers | OE report |

## Compliance & Risk Metrics

| Metric | Formula | Workday source |
|---|---|---|
| I-9 timeliness | Section 2 on time ÷ hires | I-9 system |
| FMLA notice timeliness | Notices within 5 business days ÷ requests | HR leave log |
| Terminated users with active access | Count | Security audit report |
| Grievances filed | Count by unit and topic | Labor relations log |
| WC lost-time rate (per 100 FTE) | Lost-time claims × 200,000 ÷ hours worked `[VERIFY: OSHA incidence-rate formula at osha.gov]` | WC carrier report |

## HR Operations Metrics

| Metric | Formula | Workday source |
|---|---|---|
| Self-service rate | Transactions started by employee/manager ÷ all transactions | Business process report by initiator |
| Business processes past due | Count in progress beyond SLA | Monitor > Business Process > In Progress |
| Review completion | Completed reviews ÷ eligible workers | Review cycle report |
| HR staff ratio | HR FTE ÷ county FTE (per 100) | Headcount by org |

---

## Dashboards by Audience

| Audience | Show | Frequency |
|---|---|---|
| Board / commission | Headcount, vacancy rate, turnover, overtime cost, key risks | Quarterly — see references/hr-director-playbook.md |
| Department heads | Their vacancies, time to fill, turnover, overtime, leave usage | Monthly |
| HR Director | All core metrics + compliance metrics + operations metrics | Monthly |
| HR team | Business processes past due, open cases, data errors | Weekly |

### Dashboard Rules

- One page; trend lines over single numbers
- Show the definition under each chart
- Suppress groups under 5 people to protect privacy
- **Missouri:** dashboards shared with the board may become public records; include only aggregate data

---

## Scheduling Reports

Schedule the top monthly reports to run automatically (report > Related Actions > Schedule
Report). Send to a restricted distribution, not to all managers, when a report contains PII.

> Navigation based on standard Workday HCM. Tenant customization varies — verify in your environment.

---

## KPI Governance

| Item | Practice |
|---|---|
| Definitions | One shared KPI dictionary, owned by HR analytics or HRIS |
| Changes | Version the definition; note the date it changed on every chart |
| Data quality | Monthly check of missing job profiles, EEO categories, termination reasons |
| Review | HR Director reviews targets annually |
