# Workers' Compensation — Deep Dive — Workday County HR Reference

## Overview

Workers' compensation (WC) is a no-fault insurance system that provides medical benefits and
wage replacement for employees injured in the course and scope of employment. County government
HR plays a central coordination role — between the injured employee, department supervisor,
WC carrier or self-insurance pool, and return-to-work programs. Workday tracks the absence
and leave side; WC is managed externally.

> ⚠️ LEGAL NOTE: Workers' compensation claims are governed by Missouri RSMo Chapter 287 and
  administered by the Missouri Division of Workers' Compensation. All decisions about claim
  acceptance, medical causation, and benefits are made by the WC carrier or self-insured
  administrator — not HR. HR's role is coordination and documentation.

---

## Missouri Workers' Compensation — Key Rules

### Coverage

- All county employees are covered (full-time, part-time, seasonal, temporary)
- Volunteer firefighters and EMS: covered under Missouri WC if receiving some compensation
- Elected officials: coverage depends on whether they are "employees" under RSMo 287

### Employer Options

County governments typically use one of:
- **Self-insurance pool** (most common): Missouri Association of Counties (MAC) risk pool or similar
- **Commercial insurance**: traditional WC carrier
- **Individual self-insurance**: very large counties only; requires DWC approval

### Statute of Limitations

- Report an accident to the WC carrier within **30 days** of injury
- Employee must file a WC claim with the Division within **2 years** of injury (3 years for occupational disease)

---

## Injury Response Protocol

### Immediate Response (Day of Injury)

**Supervisor responsibilities:**
1. Ensure employee receives immediate medical attention (send to ER if serious; urgent care for non-emergency)
2. Notify HR same day
3. Complete First Report of Injury form (FROI) — Missouri Form WC-2
4. Preserve the scene; document what happened

**HR responsibilities:**
1. Notify WC carrier or self-insurance administrator within **24 hours** (carriers prefer same-day)
2. Provide employee with panel of physicians (list of approved treating doctors)
3. Determine whether FMLA runs concurrently (if serious health condition — see FMLA note below)
4. Notify employee of WC rights in writing

### Panel of Physicians

Missouri law (RSMo § 287.140) allows the employer to direct initial medical care by providing
a panel of at least one physician (some jurisdictions require a panel of 3+). If the county
does not provide a panel, the employee may choose their own treating physician and the county
loses control of treatment.

**Maintain a current panel of physicians** and provide it to every injured employee.

### First Report of Injury (FROI)

Missouri Form WC-2 must be filed with the Division of Workers' Compensation within **5 days**
of notice of a work-related injury or death.

Fields required:
- Employee name, DOB, SSN, hire date
- Date, time, and location of injury
- Description of how injury occurred
- Body part injured
- Medical treatment provided
- Employer information

> File via the Missouri Division of Workers' Compensation online portal or designated fax number.

---

## Workday — WC Leave Tracking

Workday does not manage WC claims, but HR uses Workday to track the absence.

### How to Process in Workday

1. **Create a Leave of Absence**: Absence > Leave of Absence > Create
   - Leave Type: Workers' Compensation Leave
   - Enter anticipated end date (update as treatment progresses)

2. **Run FMLA concurrently** (if qualifying serious health condition):
   - Create a second leave record: FMLA Leave (concurrently with WC)
   - Notify employee in writing that FMLA is running

3. **Track pay during WC leave**:
   - WC pays wage replacement (typically 66.67% of average weekly wage in Missouri)
   - County policy may allow employee to supplement WC pay with accrued sick/vacation
   - Configure time rules accordingly

4. **Process return to work** in Workday when employee returns:
   - Absence > Return from Leave
   - Note any work restrictions in worker profile

---

## Missouri WC Benefits

### Medical Benefits

- All necessary and reasonable medical treatment is covered
- No copays or deductibles for the employee
- Mileage reimbursement for medical travel (current IRS mileage rate)
- Prescription drugs covered
- Durable medical equipment covered

### Wage Replacement (Temporary Total Disability — TTD)

- Rate: **66.67% of employee's average weekly wage (AWW)**
- AWW calculated from last 13 weeks of earnings before injury
- TTD begins on the 4th day of disability (3-day waiting period); if disability exceeds 14 days, the first 3 days are also paid retroactively
- TTD maximum rate is set by DWC annually

### Permanent Partial Disability (PPD)

When the employee reaches maximum medical improvement (MMI) but has a permanent impairment:
- Rated by treating physician as a % impairment
- PPD benefits calculated by impairment rating × body part schedule in RSMo 287

### Permanent Total Disability (PTD)

If the employee is unable to perform any work:
- Weekly benefits for life (or until able to return to work)
- Second Injury Fund may contribute

### Death Benefits

- Burial expenses up to $5,000
- Weekly benefits to surviving spouse and dependent children

---

## Return to Work (RTW) Program

A strong RTW program reduces WC costs and supports employee recovery.

### Why RTW Matters

- Every day an employee is off work increases claim cost
- Modified/light duty can return an employee to productivity while they recover
- Employees who return to work sooner have better outcomes than those who remain off work

### County RTW Protocol

**Step 1: Medical clearance**
- When treating physician authorizes return (full or modified duty), notify HR same day
- Get written work restrictions from physician

**Step 2: Assess modified duty availability**
- HR and department determine if restrictions can be accommodated
- Modified duty examples: desk assignment for a field worker; no lifting for a maintenance worker; seated work for someone with foot injury

**Step 3: Document in Workday**
- Update leave of absence end date
- Add note to worker profile with work restrictions and duration
- Set a calendar reminder for restriction review date (typically 30-day intervals)

**Step 4: Ongoing monitoring**
- Regular check-ins with employee and supervisor
- HR coordinates with WC carrier on treatment progress
- Schedule medical re-evaluation as restrictions approach expiration

**Step 5: Full return**
- Physician releases employee without restrictions
- Update Workday leave return date
- Close WC claim coordination

### When Modified Duty Isn't Available

If no modified duty is available:
- Employee remains on WC leave with TTD benefits
- County should document good-faith efforts to accommodate
- If no modified duty for 6+ months, evaluate long-term disability or disability retirement

---

## OSHA Recordkeeping (County Government)

Most county government employers are covered by OSHA (or state equivalent).

### Missouri OSHA Coverage

Missouri is a **Federal OSHA state** (no state plan). Federal OSHA standards apply to county government in Missouri.

### Recordable Injuries (OSHA 300 Log)

A work-related injury is OSHA recordable if it results in:
- Days away from work
- Restricted work or job transfer
- Medical treatment beyond first aid
- Loss of consciousness
- Diagnosis of a significant condition by a healthcare professional

### OSHA 300, 300A, and 301

| Form | Purpose | Retention |
|---|---|---|
| OSHA 300 | Log of work-related injuries and illnesses | 5 years |
| OSHA 300A | Summary posted Feb 1 – Apr 30 annually | 5 years |
| OSHA 301 | Incident report for each recordable injury | 5 years |

HR maintains these records; WC carrier often provides the data.

### Severe Injury Reporting

**Fatality**: Report to OSHA within **8 hours**
**Inpatient hospitalization, amputation, eye loss**: Report within **24 hours**

Contact OSHA via 1-800-321-OSHA.

---

## Fraud Prevention

WC fraud costs county governments significant money. HR's role:

- Review patterns: same employee, repeated claims; same supervisor's department has high claim rate
- Coordinate with WC carrier on surveillance or investigation if fraud suspected
- Never confront employee directly — route through WC carrier and county counsel
- Document all return-to-work violations (employee observed doing restricted activities)

---

## WC KPIs

| KPI | Target | Source |
|---|---|---|
| FROI filed within 5 days | 100% | WC carrier log |
| OSHA recordable rate (per 100 FTEs) | <3.0 | OSHA 300 log |
| Lost time injury rate (per 100 FTEs) | <1.5 | WC carrier report |
| Average days away per lost-time claim | Track trend | WC carrier report |
| WC cost per $100 of payroll | Track trend | WC carrier report |
| Modified duty program utilization | >80% of eligible claims | WC carrier + HR tracking |
| Return-to-work within 30 days | >70% of claims | WC carrier report |
| OSHA recordables with accurate OSHA 300 log | 100% | Annual OSHA 300 audit |
| Severe injury OSHA reporting compliance | 100% | HR log |
