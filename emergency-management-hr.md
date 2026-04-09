# Emergency Management & Disaster HR — Workday County HR Reference

## Overview

County governments are first responders to natural disasters, public health emergencies, and
critical infrastructure failures. HR plays a critical operational role: activating emergency
staffing, managing disaster leave, coordinating FEMA documentation, handling hazard pay and
overtime, and supporting employee mental health post-disaster. Workday must be configured in
advance — not during the emergency.

---

## HR's Role in Emergency Operations

### Emergency Operations Center (EOC) Integration

In most counties, the EOC is activated during declared emergencies. HR's EOC functions:
- **Staffing management**: track who is deployed, where, and for how long
- **Pay and overtime authorization**: approve emergency overtime pay
- **Leave administration**: manage emergency leave policy
- **Personnel accountability**: confirm all employees are safe and accounted for
- **Documentation**: maintain FEMA-compliant time records for reimbursement
- **Employee support**: coordinate EAP, crisis counseling, welfare checks

### NIMS/ICS Requirements

Most county HR directors and key HR staff should complete:
- ICS-100: Introduction to Incident Command System
- ICS-200: Basic Incident Command System
- ICS-700: National Incident Management System (NIMS)
- ICS-800: National Response Framework

These are free online at training.fema.gov and typically take 1–2 hours each.

---

## Pre-Disaster HR Preparation

### Emergency Staffing Plan (Update Annually)

Maintain a document (outside Workday) that identifies:
- Essential positions by department (cannot be suspended during emergency)
- Emergency response assignments (who activates to EOC; who remains in department)
- Backup/alternate for each essential position
- Contact information for all employees (home, cell, emergency contact) — pull from Workday

### Workday Emergency Roster Export

Before hurricane/tornado season, flood risk periods, or during hazard warnings:

1. Navigate: Reports > Headcount by Organization
2. Export: Name, Department, Supervisor, Personal Cell, Emergency Contact
3. Save to a secure offline location (Google Drive, OneDrive, or printed)
4. This roster allows HR to account for all employees if Workday is inaccessible during the event

> ⚠️ This report contains PII. Restrict access to HR Director, EOC staff, and department heads.
  Do not email broadly.

### Essential Function Designations in Workday

Add a custom field to Position:
- Field name: "Essential Function Designation"
- Values: Essential (Tier 1) / Important (Tier 2) / Non-Essential (Tier 3)

This enables rapid reporting of who must report during an emergency.

---

## Emergency Leave Policy

Ensure your employee handbook and MOU(s) address:

### Administrative Leave

When the county closes or restricts operations:
- Non-essential employees: administrative leave (paid); count toward work time
- Essential employees who work: regular pay + any applicable hazard or overtime premium
- Configure in Workday as a separate leave type: "Emergency Administrative Leave"

### Disaster Leave (If Offered)

Some counties allow employees affected by the disaster (home damage, family care) additional paid leave:
- Typically 1–5 days authorized by CAO or board action
- Configure in Workday as a one-time leave event triggered by an emergency declaration

### Voluntary Emergency Response Leave

Missouri RSMo § 44.250 et seq. governs state emergency response. Some provisions may apply to employees who are licensed emergency responders (firefighters, EMTs, medical professionals) volunteering during a disaster.

---

## Hazard Pay and Emergency Overtime

### Hazard Pay

Hazard pay is additional compensation for work performed in hazardous conditions. Not required by FLSA but may be required by MOU or authorized by county policy during emergency.

Common hazard pay structures:
- Flat dollar amount per hour worked in hazardous conditions (e.g., +$5/hr)
- Percentage premium on base pay (e.g., +25% for specific assignments)

#### Workday Configuration

Create a hazard pay allowance plan:
- Navigate: Compensation > Allowance Plans > Create
- Set as a temporary allowance (time-limited)
- Assign to employees working in the hazardous assignment
- Remove when assignment ends

#### Activating Mid-Emergency

If hazard pay is authorized during the emergency:
1. CAO or board issues emergency authorization
2. HR documents authorization in writing
3. HR activates allowance plan for affected employees
4. Payroll processes in next available cycle (or off-cycle if immediate)

### Emergency Overtime

During disasters, overtime is frequently unavoidable. Key rules:

- Non-exempt employees: FLSA overtime applies regardless of emergency
- Public safety employees: FLSA § 7(k) thresholds apply
- No FLSA exception for emergency conditions — overtime must be paid

#### Workday Time Tracking During Emergency

During an emergency, normal time-entry workflows may be disrupted. Options:

1. **Continue normal Workday time entry** if system is accessible
2. **Paper timesheets** (designate a backup form pre-disaster) → enter into Workday when system restored
3. **Supervisor batch entry** (supervisor enters for entire team if employees can't access)

> Maintain all paper timesheets for FEMA reimbursement documentation.

---

## FEMA Public Assistance — HR Documentation Requirements

If the county receives FEMA Public Assistance grants after a federally declared disaster,
FEMA requires extremely detailed documentation of labor costs.

### What FEMA Requires

For every employee who worked on the disaster:
- **Name and title**
- **Regular pay rate and OT pay rate**
- **Hours worked on disaster-related activities** (by date, by project)
- **Work performed** (description linked to the FEMA project number)
- **Signed timesheets or equivalent**

### Workday FEMA Documentation Setup

During the emergency:
1. Create a **FEMA Cost Code** (coordinate with Finance — they typically set up project tracking)
2. Train supervisors to code hours in Workday against the FEMA project code
3. For employees splitting time between disaster and regular duties: split timesheets by activity

### Common FEMA Documentation Errors

| Error | Impact | Prevention |
|---|---|---|
| Missing supervisor signature on timesheet | Ineligible for reimbursement | Require all timesheets to have supervisor sign-off |
| Hours not attributed to specific FEMA project | FEMA disallows the cost | Establish project codes before work begins |
| Including unrelated work in FEMA claim | Audit finding; repayment | Train supervisors on what qualifies |
| No description of work performed | Disallowed | Require brief description on all FEMA-coded time |
| Overtime calculated incorrectly | Disallowed or underclaimed | Workday calculates; verify against FEMA requirements |

> FEMA audit risk is significant. Engage your county emergency management office and FEMA
  public assistance coordinator before submitting any FEMA labor cost claim.

---

## Employee Welfare During Disasters

### Personnel Accountability

During an active emergency:
- HR activates the emergency roster (see above)
- Department heads account for all employees (on duty, evacuated, off duty and safe, unaccounted)
- Unaccounted employees: escalate to EOC immediately

### Welfare Checks

If an employee's home or family is affected by the disaster:
- HR coordinates with department head to allow flexible reporting during the immediate recovery phase
- Refer employee to EAP for disaster mental health support
- Coordinate with county's emergency assistance programs or community organizations for housing/financial assistance referrals

### Disaster Mental Health

Following a major disaster (especially one involving employee deaths, community casualties, or traumatic response):
- Activate CISM (Critical Incident Stress Management) team
- Schedule group debriefing within 24–72 hours
- Notify EAP of elevated need
- Provide information about ongoing counseling resources
- Track employee leave during recovery period — spikes in sick leave post-disaster are a sign of need

---

## Continuity of HR Operations

### What HR Must Be Able to Do During/After a Disaster

| Function | Normal System | Backup Method |
|---|---|---|
| Process payroll | Workday + payroll system | Manual calculation + paper checks |
| Access employee contact info | Workday | Pre-exported roster (offline) |
| Track time worked | Workday | Paper timesheets → manual entry later |
| Process emergency leave | Workday | Paper form → Workday when restored |
| Issue emergency pay (advance) | Workday + payroll | Manual check + reconcile later |
| Communicate with employees | Email/intranet | Phone tree; supervisor cascade; text alert system |

### HR Continuity Checklist (Maintain Annually)

- [ ] Emergency contact roster exported and stored offline
- [ ] Paper timesheet template ready (printed and stored)
- [ ] Paper leave request form ready
- [ ] HR Director and backup have mobile access to Workday (mobile app)
- [ ] Payroll Director and HR Director have each other's personal cell numbers
- [ ] FEMA project code setup procedure documented
- [ ] IT has offline backup of Workday data (part of Workday's SLA — verify)
- [ ] Employee emergency alert system (text/phone) configured and tested

---

## Emergency Management HR KPIs

| KPI | Target | Source |
|---|---|---|
| NIMS training completion (HR staff) | 100% | Learning management records |
| Emergency roster exported within 6 months | Yes | HR operations log |
| FEMA documentation completeness (post-disaster) | 100% eligible costs documented | FEMA PA coordinator |
| Employee welfare accountability (all employees) | 100% accounted for within 24 hrs | EOC records |
| EAP activation within 72 hours of major event | Yes | HR/EAP log |
| Hazard pay activation within 24 hours of authorization | Yes | Workday compensation records |
