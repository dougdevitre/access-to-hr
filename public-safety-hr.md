# Public Safety HR — Law Enforcement & Fire — Workday County HR Reference

## Overview

Public safety HR is the most specialized area of county government HR. Law enforcement and
fire departments operate under distinct FLSA rules, POST certification requirements, pension
systems, use-of-force documentation obligations, and mental health considerations that require
dedicated Workday configuration and HR practices.

> ⚠️ LEGAL NOTE: Public safety discipline, terminations, and use-of-force investigations
  involve significant legal exposure and civil service protections. Always partner with county
  counsel and the department's legal advisor on any adverse action.

---

## FLSA § 7(k) — Public Safety Overtime

Public safety employers may use a **work period** (7–28 days) instead of a standard 40-hour
workweek for overtime calculation. This is one of the most consequential Workday configurations
for law enforcement and fire.

### Overtime Thresholds by Work Period

| Work Period | Law Enforcement OT Threshold | Fire OT Threshold |
|---|---|---|
| 7 days | 43 hours | 53 hours |
| 14 days | 86 hours | 106 hours |
| 21 days | 128 hours | 159 hours |
| 28 days | 171 hours | 212 hours |

### Adopting § 7(k)

Requirements:
- Formal adoption — must be reflected in MOU or written policy
- Consistent application — cannot switch work periods to avoid overtime
- Documentation — county must maintain records of work period start dates

### Configuring in Workday

1. Navigate: Time & Attendance > Time Calculation Rules > FLSA Work Period
2. Set work period length (14 or 28 days most common)
3. Set OT threshold matching the work period and employee type
4. Apply to the correct pay group (Law Enforcement, Fire — separately)
5. Test against a sample pay period before going live

> ⚠️ CRITICAL: Misconfiguring FLSA § 7(k) means employees are either underpaid (litigation
  risk) or overpaid (budget impact). Have Payroll and legal review the configuration before
  activating.

---

## POST Certification Management

Peace Officer Standards and Training (POST) certification is required for all sworn law
enforcement officers in Missouri (and most states).

### Missouri POST Requirements

- Initial certification: complete a POST-approved academy + pass written/physical exam
- Continuing education: 48 hours per 3-year cycle (Missouri)
- Specialized certifications: taser, firearms instructor, K-9, accident reconstruction, etc.
- Decertification: felony conviction, dishonesty findings, certain terminations trigger POST
  to revoke certification — county HR must report qualifying events to Missouri POST

### Tracking in Workday

Navigate: Worker Profile > Skills & Experience > Certifications

For each officer, track:
- POST basic certification number and date
- Academy completion date
- Firearms qualification dates (typically annual)
- Continuing education hours completed / remaining in cycle
- Specialized certifications with expiration dates

Build a custom report:
- Business object: Worker
- Filter: Job Profile = [sworn law enforcement profiles]
- Fields: Name, Certification Name, Certification Number, Expiration Date, Hours Completed
- Schedule: Quarterly, to HR and Police Chief

> ⚠️ A lapsed POST certification means the officer cannot legally function as a peace officer.
  An officer working without valid certification creates enormous liability. Track this obsessively.

---

## Firefighter Certification Management

### National/State Certifications

| Certification | Issuing Body | Renewal |
|---|---|---|
| Firefighter I / II | IFSAC or ProBoard / state fire academy | Varies by state |
| EMT / Paramedic | State EMS office | 2–3 year recertification |
| Hazmat Operations / Technician | State fire marshal | Renewal training required |
| NFPA 1582 Physical | Physician | Annual (NFPA recommendation) |
| Incident Command (ICS 100/200/300/400) | FEMA/NIMS | No expiration but update if NIMS changes |
| Driver/Operator | State or department | Annual driver evaluation |

### Annual Physical Requirements

Many fire departments require annual physicals per NFPA 1582. HR should:
- Track due dates in Workday certifications
- Coordinate with department for scheduling
- Flag any officer who fails the physical — triggers accommodation / light duty / disability retirement review

---

## Law Enforcement Staffing Models in Workday

### Position Types

| Type | Description | Configuration |
|---|---|---|
| Sworn Officer (full-time) | Budgeted, classified position | Full position in position management |
| Reserve / Part-Time Officer | Variable hours; may be POST certified | Part-time position; track certification separately |
| Detention Officer | Often non-sworn but specialized | Separate job profile; check if POST required |
| Civilian Support | Dispatch, records, evidence | Standard HCM position |
| School Resource Officer (SRO) | Full-time assignment to school district | Track interagency agreement; may be funded by school |

### Patrol Schedule Configurations

Law enforcement runs complex rotating schedules. Common patterns:

| Schedule | Description | FLSA Period |
|---|---|---|
| 5/8 (traditional) | 5 days × 8 hours | 7-day; OT at 43 hrs |
| 4/10 | 4 days × 10 hours | 7-day; OT at 43 hrs |
| 3/12 (compressed) | 3 days × 12 hours | 14-day; OT at 86 hrs |
| Pitman (rotating) | 2–3 day cycles rotating | 14-day; configure carefully |
| Southern rotation | 4 on / 2 off / 4 on / 2 off | 28-day; OT at 171 hrs |

Configure each schedule as a separate Workday work schedule and assign to the correct
officers during shift bidding season.

---

## Fire Department Scheduling

Fire departments typically use 24-hour shift schedules:

| Pattern | Description | Common Usage |
|---|---|---|
| 24/48 | 24 hours on, 48 hours off | Most common; Kelly day variations |
| 24/72 | 24 hours on, 72 hours off (4-platoon) | Larger departments |
| 48/96 | 2 days on, 4 days off | Less common |
| 10/14 | 10-hr day / 14-hr night shifts | Smaller departments |

### Kelly Days

Many fire MOUs include "Kelly days" — scheduled days off that reduce the average work week
below the 212-hour/28-day FLSA threshold. Configure Kelly days as:
- Scheduled days off in the work schedule, or
- Automatically-generated comp time offsets

> Get payroll and legal to verify Kelly day configuration before going live — errors here
  affect every firefighter's pay every cycle.

---

## Use-of-Force Documentation

County HR is not the primary owner of use-of-force reports, but HR must:

- Ensure use-of-force incidents that result in injury, complaint, or investigation are
  documented in the employee's Workday worker profile (as a confidential note or attachment)
- Track any administrative leave or light duty tied to an ongoing investigation
- Know that a substantiated use-of-force finding may trigger discipline workflow in Workday

### Workday Documentation

- Attach investigation outcomes (from law enforcement IA unit) to worker profile: Worker Profile > Documents > Confidential — Investigation
- Log any discipline resulting from the investigation per the standard discipline workflow
- Coordinate with the department — HR should not receive raw investigation materials directly

---

## Law Enforcement Background & Pre-Employment

Sworn officers require the most extensive pre-employment screening of any county role:

| Check | Requirement | Notes |
|---|---|---|
| Criminal history | Felony disqualifier; misdemeanor review | Missouri POST standards + county policy |
| Psychological evaluation | Required by most POST standards | Licensed psychologist; confidential |
| Polygraph | Optional; many departments use | Not admissible in court but usable for employment |
| Physical fitness test | Required at hire | POPAT or department-specific |
| Medical examination | Required | NFPA 1582 or department physical standards |
| Background investigation | 10-year employment/residential history | Investigator interviews; weeks-long process |
| Drug testing | Required; random ongoing | DOT-standard for some positions |
| Credit check | Optional; some departments | FCRA compliance required |

### Workday Process

- Track each pre-employment step in the candidate record
- Do not initiate a hire action until all clearances are received
- Store psychological and medical results in a restricted document folder (not general personnel file)
- Background investigation results: attach summary only; retain full report per county records retention policy

---

## Law Enforcement Mental Health & Wellness

County HR has a growing role in supporting officer mental health:

### Critical Incident Stress Management (CISM)

Following a traumatic incident (officer-involved shooting, line-of-duty death, mass casualty):
- HR coordinates with CISM team or EAP for debriefing
- Officers should not be required to return to duty before clearance
- Document administrative leave or modified duty in Workday (neutral leave type — not disciplinary)

### Peer Support Programs

- Many MOUs now recognize peer support programs
- Track peer support coordinator role in Workday (if assigned as a secondary role or duty)
- Peer support contacts are confidential — HR does not receive the content of peer support conversations

### EAP Referrals

- HR can refer officers to EAP; EAP sessions are confidential
- HR tracks only whether the referral was made and whether mandatory EAP (post-incident or fitness-for-duty) was completed
- Do not document EAP utilization content in Workday

---

## Disability Retirement — Public Safety

Law enforcement officers and firefighters injured on duty or who develop qualifying disabilities
may be eligible for disability retirement through LAGERS or the county pension system.

### HR Process

1. Employee or supervisor notifies HR of disability/injury claim
2. HR coordinates with Workers' Comp and pension system
3. HR initiates FMLA concurrently if injury qualifies
4. Pension system initiates disability retirement application process
5. HR processes Workday leave while application is pending
6. Upon approval: process retirement in Workday (reason: Disability Retirement)
7. Coordinate COBRA notification + any service-connected health benefits

> Public safety disability retirements are governed by the pension plan documents, not just
  HR policy. Engage LAGERS (or applicable pension) early.

---

## Public Safety HR KPIs

| KPI | Target | Source |
|---|---|---|
| POST certification compliance | 100% of sworn officers current | Custom certification report |
| Firearms qualification compliance | 100% annually | Custom certification report |
| Vacancy rate (sworn positions) | <8% | Position Fill Report (sworn filter) |
| Academy pipeline (recruits in training) | Track against projected vacancy | HR + Academy records |
| Overtime as % of total hours | <15% (flag if higher) | Time & Attendance Reports |
| Workers' comp incidents per 100 officers | Track and trend | WC carrier data |
| Turnover — sworn officers | <8% annually | Turnover Report (sworn filter) |
| Psychological clearance turnaround | <30 days from conditional offer | HR case tracking |
| Use-of-force incidents requiring discipline | Track per department policy | IA + HR records |
| EAP utilization rate | Track (no target; trend matters) | EAP vendor report |
