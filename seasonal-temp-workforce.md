# Seasonal, Temporary & Contract Workforce — Workday County HR Reference

## Overview

County governments employ significant numbers of seasonal, temporary, and contract workers —
summer parks staff, election workers, seasonal road crews, interns, temporary administrative
support, and contracted service workers. This population creates distinct HR, benefits, FLSA,
and Workday configuration challenges that are often handled inconsistently or incorrectly.

---

## Workforce Categories

| Category | Definition | Typical County Uses |
|---|---|---|
| **Seasonal** | Hired for a specific season or time-limited program; may return year over year | Parks/rec staff, seasonal road crew, lifeguards, summer youth workers |
| **Temporary** | Limited-duration hire to fill a vacancy or backlog | Maternity leave coverage, vacancy coverage pending recruitment |
| **Intermittent / As-Needed** | Works irregular hours with no guaranteed schedule | Election workers, jury summons escorts, event staff |
| **Intern** | Student or recent grad; educational component | County internship programs; sometimes paid, sometimes unpaid |
| **Contracted (Staffing Agency)** | Placed by a staffing agency; agency is the employer of record | IT temp, administrative temp, professional temp |
| **Independent Contractor** | Self-employed; 1099 relationship; not a county employee | Consultants, specialists, certain professional services |

> ⚠️ CRITICAL DISTINCTION: Contracted (staffing agency) workers and independent contractors
  are NOT county employees. Do not process them through Workday as workers. Do not issue
  them county benefits. Misclassifying contractors as employees (or vice versa) creates
  significant tax and liability exposure. Consult county counsel before engaging contractors.

---

## Workday Configuration for Temp/Seasonal

### Employment Types in Workday

Configure distinct employment types:

| Workday Employment Type | Who It Applies To |
|---|---|
| Regular | Full-time and part-time permanent employees |
| Temporary | Temp and seasonal employees |
| Intern | County interns |
| On Leave | Employees on extended leave |

Temporary/seasonal employees should be hired into:
- A **temporary position** (or evergreen position for recurring seasonal roles)
- The correct employment type (Temporary)
- With an **expected end date** (set at hire; visible in Workday)

### Setting End Dates

Navigate: Worker Profile > Actions > Change Job > Update Expected End Date

Benefits of tracking end dates:
- Run a report of workers with end dates in the next 30/60/90 days
- Plan for extensions or replacements
- Ensure automatic benefits eligibility review at ACA measurement period
- Prevent workers from continuing on payroll past their intended end date

---

## ACA and the Temporary/Seasonal Workforce

This is the most complex compliance issue for temp/seasonal workers.

### ACA Employer Mandate (Applicable Large Employers)

Counties with 50+ FTEs must offer minimum essential coverage to full-time employees
(those averaging ≥30 hours/week). This applies to temp and seasonal workers too.

### Measurement Periods for Variable-Hour Employees

Because temp/seasonal hours vary, the ACA allows employers to use **measurement periods**
to determine full-time status:

| Period | Definition |
|---|---|
| Standard Measurement Period | 3–12 months to measure average hours |
| Administrative Period | Up to 90 days after measurement period; determine eligibility; enroll |
| Stability Period | Period during which employee is offered coverage (regardless of hours during this period) |

**Most common setup:** 12-month standard measurement period with 90-day administrative period
and 12-month stability period.

### Workday ACA Configuration for Seasonal/Temp

1. Assign seasonal/temp employees to a variable-hour ACA measurement group
2. Navigate: Benefits > ACA > Manage ACA Measurement Periods
3. Track hours during the measurement period
4. Run ACA Eligibility Report at end of each measurement period
5. Offer coverage to any seasonal employee who averaged ≥30 hours/week

> ⚠️ Many counties miss ACA obligations for seasonal workers. A seasonal employee who works
  full-time for 6 months may trigger ACA eligibility in the following year's stability period.
  Get your benefits broker involved in the configuration.

### Seasonal Worker ACA Exception

The ACA provides a **seasonal worker exception**: if your workforce exceeds 50 FTEs for
no more than 120 days and the excess is attributable to seasonal workers, those workers
are excluded from the ALE calculation. Document this if applicable.

---

## FLSA and Seasonal/Temp Workers

### Minimum Wage and Overtime

Seasonal, temp, and intermittent workers are fully covered by FLSA:
- Minimum wage applies
- Overtime (>40 hours/week) must be paid at 1.5x for non-exempt workers
- No exception for seasonal workers under FLSA

### Youth Employment (Under 18)

For summer youth programs and parks/rec:

| Age | Work Hours | Restrictions |
|---|---|---|
| 14–15 | Max 8 hrs/day; 40 hrs/week when school not in session | No hazardous occupations |
| 16–17 | No hour restrictions | No hazardous occupations (FLSA Hazardous Occupation Orders) |
| Under 14 | Very limited; effectively not employed in most county roles | Agricultural exceptions only |

Missouri child labor law (RSMo Chapter 294) may impose additional restrictions.
Work permits may be required for 14–15 year olds.

### Subminimum Wage Certificate Programs

Some counties operate work programs for individuals with disabilities under FLSA § 14(c)
subminimum wage certificates. This is specialized and controversial — consult county counsel
and the Missouri Division of Developmental Disabilities before establishing.

---

## Summer Youth Programs

Many counties run summer employment programs for youth (ages 14–21), often funded through
WIOA Youth Formula funds or county general fund.

### HR Processing in Workday

1. Create seasonal positions for the program (can be evergreen or individual)
2. Hire participants as temporary workers
3. Assign to youth-specific employment type
4. Configure youth labor law restrictions (no hazardous work; hour limits)
5. Set position end dates at program end
6. Process all terminations at program conclusion

### Payroll Considerations

- Youth workers are employees — full payroll processing, W-2 issuance
- FICA applies (unless a specific exception applies — consult payroll/tax advisor)
- Workers' comp applies — youth workers are covered

---

## Internship Programs

### Paid vs. Unpaid Internships

Under FLSA, unpaid internships in the private sector are very restricted. For government:
- Public agency internships can be unpaid if the intern receives academic credit and the arrangement is primarily for the intern's benefit
- However, unpaid internships at government agencies are scrutinized more than at nonprofits
- **Best practice**: Pay interns at least minimum wage; it eliminates legal risk and improves candidate quality

### Workday Processing for Interns

- Hire as temporary workers (employment type: Intern)
- Assign to an internship position (can be evergreen if recurring)
- Track department, supervisor, and program dates
- Process termination at internship end

### Intern Benefits Eligibility

- Paid interns working <30 hours/week: typically not ACA-eligible
- Interns in MOU-covered positions: check union contract for applicability
- Retirement: typically excluded from LAGERS for temporary workers — verify with LAGERS

---

## Election Workers

### Special FLSA Status

Election workers (poll workers, precinct election judges) are subject to a special FLSA
exemption: election workers paid less than $2,000/year (indexed) are not subject to
Social Security and Medicare (FICA) taxes. Some states have additional exemptions.

### IRS Reporting

- If election worker earns ≥$600: issue 1099-MISC
- Social Security / Medicare: consult county tax advisor and IRS Publication 963
- Missouri: verify state withholding requirements for election workers

### Workday Options for Election Workers

Given the special tax treatment and low volume, many counties process election workers
outside Workday:
- Process through Accounts Payable as contract payments (if true independent contractor status applies)
- Or hire as temporary workers in Workday with special tax designation

> Get explicit guidance from your county auditor/tax advisor on election worker classification
  before processing in Workday.

---

## Independent Contractor vs. Employee Test

### IRS 20-Factor Test (Key Factors)

| Factor | Indicates Employee | Indicates IC |
|---|---|---|
| Instructions | County controls HOW work is done | Worker controls their own methods |
| Training | County trains the worker | Worker uses their own methods |
| Integration | Work is integral to county operations | Work is separate/specialized |
| Hours | County sets hours | Worker sets their own hours |
| Location | Works at county facility | Works from their own location |
| Tools | County provides equipment | Worker provides own tools |
| Multiple clients | Works only for county | Works for multiple clients |
| Termination | Can be terminated at will | Termination may require breach |

### DOL Economic Reality Test (FLSA)

The DOL uses a multi-factor "economic reality" test focused on economic dependence:
- Is the work integral to the business?
- Does the worker invest in their own equipment/facilities?
- Can the worker profit or lose money?
- Is the relationship permanent?
- Does the employer exercise control?

> ⚠️ County governments have been subject to significant IC misclassification audits. The
  default should be: if in doubt, it's an employee. Consult county counsel before engaging
  any long-term IC arrangement.

---

## Contractor / Staffing Agency Management

### What HR Tracks

When using a staffing agency:
- The agency worker is NOT in Workday (they are not a county employee)
- HR maintains a **contractor roster** (spreadsheet or vendor management tool) showing:
  - Worker name and agency
  - Department and supervisor
  - Assignment start and end dates
  - Hourly bill rate
  - Position or project they're filling

### Workday Touchpoints

- If a contract worker is later converted to a regular employee: standard new hire process in Workday
- Track the vendor contract in Finance (not HR)
- Ensure county liability insurance covers contract workers in county facilities

---

## Temp/Seasonal Workforce KPIs

| KPI | Target | Source |
|---|---|---|
| ACA compliance rate for variable-hour employees | 100% measured and offered if eligible | ACA Eligibility Report |
| Workers with end dates tracked in Workday | 100% | End Date Report |
| Youth workers in hazardous occupations | 0 | Supervisor compliance; HR spot check |
| Seasonal workers rehired year-over-year | Track (high % = program quality) | Year-over-year hire report |
| Contractor conversion rate (temp-to-perm) | Track | HR tracking |
| IC misclassification findings | 0 | Legal / audit |
| Election worker tax compliance issues | 0 | Auditor / tax advisor report |
