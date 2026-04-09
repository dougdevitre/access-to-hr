# Records Management & Audit Readiness — Workday County HR Reference

## Overview

County government HR records are subject to Missouri Sunshine Law (public disclosure),
federal employment law retention requirements, civil service appeal rights, union grievance
discovery, and EEOC/litigation hold obligations. Workday stores transactional data, but
HR must also manage documents outside Workday — and ensure both are defensible in any audit
or legal proceeding.

---

## Records Retention Schedule — County HR

### Federal Minimum Requirements

| Record Type | Retention Period | Authority |
|---|---|---|
| Personnel files (general) | 3 years after separation | Various |
| Payroll records (time, pay) | 3 years | FLSA |
| Payroll records (FMLA) | 3 years | FMLA regulations |
| I-9 forms | Longer of: 3 years from hire OR 1 year after separation | IRCA |
| EEO records / applicant data | 1 year from creation or action date | Title VII / EEOC |
| OSHA 300/300A/301 | 5 years | OSHA |
| ACA records | 6 years recommended | IRS / ACA |
| Benefit plan documents | 6 years | ERISA |
| COBRA notices | 6 years | COBRA |
| Workers' comp records | 10 years (recommended) | State DWC + litigation risk |
| Pension / retirement records | Permanent or life of plan + 6 years | ERISA / plan documents |
| Union grievance records | 6 years | Best practice |
| Investigation records | 5 years after resolution | Best practice |

> ⚠️ Missouri Sunshine Law may impose longer retention for some public records. County charter
  or ordinance may have additional requirements. Consult county counselor and records management officer.

### Missouri-Specific Retention

Missouri State Records Retention Schedule (Secretary of State) provides guidance for local
governments. HR records typically fall under Series HR-xxx in the state retention schedule.
Verify the current schedule at sos.mo.gov.

---

## Workday as a Records System

### What Workday Stores

Workday maintains:
- **Worker history**: all job actions, pay changes, status changes (permanent; no deletion)
- **Time and payroll**: all approved timesheets and payroll runs
- **Benefits**: enrollment elections and coverage history
- **Leave**: all leave requests and approvals
- **Performance**: completed review cycles, goals, ratings
- **Documents**: HR-attached PDFs (disciplinary letters, offer letters, certifications)
- **Audit trail**: every transaction with user ID, timestamp, and reason code

### What Workday Does NOT Store

- I-9 forms (unless Workday's I-9 module is specifically configured)
- OSHA 300 log (external document)
- Workers' comp claim files (managed by carrier)
- Grievance files (maintain separately)
- Investigation case files (maintain in restricted folder; attach summary to Workday)
- Personnel files (Workday stores data; the formal personnel file may be physical or separate DMS)

---

## Document Management in Workday

### Document Categories Setup

Navigate: Documents > Document Categories > Create/Edit

Establish these categories with appropriate security:

| Category | Who Can View | Contents |
|---|---|---|
| General HR | HR Partners + Manager (limited) | Offer letters, performance reviews, general correspondence |
| Confidential — Medical | HR Director + Legal only | Medical certifications, accommodation documentation |
| Confidential — Investigation | HR Director + Legal only | Investigation reports, Skelly notices, IA findings |
| Disciplinary | HR Partner + Manager (limited) | Written warnings, suspension notices |
| Recruiting | Recruiting team | Application, interview notes, background check summary |
| Benefits | Benefits Admin + Employee | Benefits enrollment confirmations |
| Certifications | HR + Manager | Professional licenses, POST certs, training records |
| Payroll | Payroll team | Tax documents, direct deposit authorizations |

### Document Upload Best Practices

1. Use descriptive file names: `[LastName]_[FirstName]_[DocType]_[YYYYMMDD].pdf`
   - Example: `Smith_John_WrittenWarning_20250315.pdf`
2. Always upload as PDF (not Word — PDFs can't be edited)
3. Add a note to the document record with date, type, and brief description
4. Select the correct security category (don't put medical records in General HR)
5. Never upload a document that contains SSN, DOB, or financial account numbers unless in a restricted-access category

---

## Personnel File Management

### What Goes in the Personnel File

| Included | Not Included |
|---|---|
| Job application | I-9 (keep separate) |
| Offer letter | Medical records / doctor's notes (keep separate) |
| Performance reviews | Workers' comp claim files |
| Disciplinary letters | Background check investigative report |
| Commendations / awards | Payroll deduction records |
| Training records | EEOC charge and investigation records |
| Classification / reclassification notices | Union grievance files |
| Separation documentation | Polygraph records (if applicable) |

### Physical vs. Electronic Personnel Files

Many counties maintain both:
- **Workday**: transactional data + attached PDFs (primary system)
- **Physical file**: original signed documents, I-9 (required to be available for inspection)

Best practice: move to electronic-only where legally permissible. Missouri does not require
physical personnel files — electronic is acceptable if:
- Originals are scanned to PDF
- System has access controls and audit trail
- Records can be produced on demand

---

## I-9 Compliance and Audit Readiness

### I-9 Storage Requirements

I-9 forms must be:
- Completed by Day 3 (employer Section 2)
- Retained for: 3 years from hire date OR 1 year after separation (whichever is later)
- Available for inspection by ICE, DHS, or DOL within **3 business days** of a request
- Kept **separate from the personnel file** (ICE inspectors see I-9s only — not the rest of the personnel file)

### I-9 Storage Options

| Method | Notes |
|---|---|
| Paper binder (alphabetical or by date) | Simple; hard to search; risk of physical loss |
| Electronic I-9 system (e.g., I9Advantage, Tracker I-9) | Best practice; audit trail; expiration alerts |
| Workday I-9 module (if configured) | Integrated; available in some Workday configurations |
| E-Verify (supplements but doesn't replace I-9) | Required for federal contractors; voluntary for others |

### I-9 Self-Audit

Conduct annually or before any anticipated inspection:

1. Pull complete list of active employees (Workday headcount report)
2. Match against I-9 file — every active employee must have an I-9
3. Review each I-9 for:
   - Section 1 completed by employee (signed and dated on or before Day 1)
   - Section 2 completed by employer within 3 days
   - Documents are acceptable per List A/B/C
   - Reverification dates are tracked for temporary work authorization
4. Correct technical errors using proper correction procedures (strike-through + initials)
5. Never backdate or white out — this is a federal offense

### Common I-9 Errors

| Error | Risk | Fix |
|---|---|---|
| Section 2 not completed within 3 days | Violation; penalty per form | Train HR; automate Day 3 reminder |
| Unacceptable documents accepted | Violation | Retrain on acceptable document lists |
| Reverification missed | Violation; employee may not be work-authorized | Set expiration alerts |
| Missing I-9 entirely | Violation | Conduct self-audit; complete I-9 if employee still active (cannot backdate) |
| White-out used | Willful violation | Never use white-out; use strike-through and initials |

---

## Audit Response Playbook

When a government agency (EEOC, DOL, ICE, DWC, IRS) contacts the county:

### Step 1: Receipt and Routing (Day 1)
- All audit/investigative correspondence goes to HR Director AND county counselor immediately
- Do not respond without county counselor involvement
- Note the response deadline on the cover letter

### Step 2: Litigation Hold (If Investigation or Lawsuit)
- County counselor issues a legal hold notice
- HR freezes deletion of all relevant Workday records
- Notify IT: no routine data purging of affected records
- Preserve: emails, Workday data, physical files, relevant to the matter

### Step 3: Records Pull from Workday
- Work with IT/HRIS to pull requested data
- Common EEOC records request: all personnel records for charging party + comparators in same job classification
- Common DOL records request: payroll, timesheets, FMLA records for 3 years
- Common ICE I-9 inspection: all I-9 forms for current employees + terminated employees within retention window

### Step 4: Review Before Producing
- County counselor reviews all records before producing to the agency
- Remove any attorney-client privileged communications
- Verify no over-production (producing records outside the scope of the request)

### Step 5: Document Your Response
- Keep a log of everything produced: date, to whom, what records, quantity
- Confirm receipt from the agency

---

## Workday Audit Trail Features

Workday maintains a complete transaction history that is valuable in audits and litigation:

### Accessing the Audit Trail

**Worker History**: Worker Profile > Actions > Worker History
- Shows every job action, pay change, leave, with date, time, and user who made the change
- Cannot be altered or deleted

**Business Process History**: Monitor > Business Process > All Business Processes
- Shows all transactions, approvals, and who approved what and when

**Audit Report**: Reports > System > Audit Trail
- Searchable by user, date range, and type of action
- Shows login history, data access, and changes

> In litigation, Workday's audit trail has been used to prove that a termination decision was
  made before (or after) an employee's protected activity. Preserve this data carefully.

---

## Records Management KPIs

| KPI | Target | Source |
|---|---|---|
| I-9 completion rate (active employees) | 100% | I-9 self-audit |
| I-9 accuracy rate (no uncorrected errors) | >98% | I-9 self-audit |
| Documents uploaded with correct security category | 100% (spot check quarterly) | Workday document audit |
| Records retention schedule reviewed | Annually | HR admin log |
| Response to EEOC charge within deadline | 100% | HR/Legal log |
| Litigation hold compliance | 100% when issued | Legal hold log |
| Personnel file completeness (required documents present) | >98% | Annual file audit |
