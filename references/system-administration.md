# Workday System Administration & Security — Workday County HR Reference

## Overview

Workday administration in a county covers security (who can see and do what), business
process configuration (who approves what), integrations (payroll, retirement, benefits
carriers, Active Directory, state reporting), and tenant maintenance (releases, sandbox
testing, data quality). Because so much HR data is confidential — and some is public under
the Missouri Sunshine Law — security mistakes are compliance mistakes.

> Configuration requiring Workday Professional Services or Workday Studio integration
  development is out of scope for this skill. Refer to IT/IS or your Workday partner.

---

## Security Model Basics

| Concept | What it means |
|---|---|
| Security group | A set of users who share permissions (role-based, user-based, job-based, intersection) |
| Domain security policy | Which groups can view/modify a type of data (e.g., Worker Data: Compensation) |
| Business process security policy | Which groups can initiate, approve or view a business process |
| Role assignment | A person assigned to a role on an organization (e.g., HR Partner for Public Works) |
| Segmented security | Restricting access to subsets (e.g., confidential document categories) |

**Principle:** least privilege. Give each role only what the job requires, and prefer
role-based groups (which follow the organization) over user-based groups (which follow a person).

---

## Monthly Security Audit

1. **Terminated users with active accounts:** Reports > Security > Security Group Assignments, filtered to terminated workers — target 0
2. **User-based security groups:** list every member; confirm each still needs access
3. **Admin-level groups:** list members; confirm with HR Director and IT
4. **Role assignments for vacant positions:** reassign or remove
5. **Proxy access:** confirm proxy is disabled in production or restricted to named admins
6. **Confidential document categories:** confirm only intended groups can view Medical and Investigation categories
7. Record the audit date, findings and fixes

> Navigation based on standard Workday HCM. Tenant customization varies — verify in your environment.

### Sensitive Data to Restrict

| Data | Who should see it |
|---|---|
| SSN, date of birth, home address | HR, payroll, benefits admins as required |
| Medical, leave reason, accommodation details | HR leave/ADA staff only |
| Investigation records | HR Director, assigned investigator, counsel |
| Self-identified race/ethnicity, disability, veteran status | HR analytics and EEO reporting only |
| Compensation | HR, payroll, managers for their own teams |
| Bank account (direct deposit) | Payroll only |

**Missouri:** names, positions, salaries and lengths of service are open records; most other
personnel records may be closed (RSMo 610.021(13)). Security should match: broad visibility
for open fields is not a privacy problem, but closable fields need protection.

---

## Business Process Configuration

| Check | Why |
|---|---|
| Every approval step has an assigned role with a person in it | Prevents stuck transactions |
| Delegation is set for approvers on leave | Prevents stuck transactions |
| HR review step on leave of absence requests | FMLA notice deadlines — see references/leave-absence.md |
| Finance step on hires and position changes | Position control |
| Counsel or HR Director step on involuntary terminations (if desired) | Due process review |
| Notifications go to roles, not named people | Survives turnover |

Business Process Monitor: Monitor > Business Process > In Progress. Review weekly for items
older than the service level.

---

## Integrations

| Integration | Direction | Monitor |
|---|---|---|
| Payroll (if external) | Outbound | Each pay period |
| Retirement plan (e.g., LAGERS) | Outbound | Each reporting period |
| Benefits carriers | Outbound | Weekly during OE; monthly otherwise |
| Active Directory / identity | Outbound | Daily — drives account creation and removal |
| State new hire reporting | Outbound | Each file — **Missouri** requires reporting within 20 calendar days of hire |
| Time clocks | Inbound | Daily |
| Background check / I-9 vendor | Bidirectional | Weekly |

### Integration Error Routine

1. Check integration events daily (Integrations > Integration Events)
2. Log each error: date, integration, record, cause, fix
3. Fix the source data in Workday, not in the vendor file
4. Re-run and confirm success
5. Review recurring errors monthly with the vendor

---

## Releases and Sandbox

- Workday releases major updates twice a year `[VERIFY: current Workday release schedule]`
- Review release notes for HR, absence, time, payroll and security changes
- Test top business processes in the sandbox before the release reaches production
- Test every integration after the release
- Keep a regression test script (hire, change job, terminate, leave, time off, merit)

---

## Data Quality Checks (Monthly)

| Check | Fix owner |
|---|---|
| Job profiles missing FLSA status or EEO-4 category | HR comp/classification |
| Workers missing a supervisory organization | HRIS |
| Positions with no budget/fund assignment | HRIS + Finance |
| Terminations with no reason code | HR partners |
| Workers with expired certifications still assigned to the job | Departments + HR |
| Duplicate worker records | HRIS |

---

## System Administration KPIs

| KPI | Target | Source |
|---|---|---|
| Terminated users with active access | 0 | Monthly security audit |
| Security audit completed | Monthly | Audit log |
| Integration errors unresolved after 5 business days | 0 | Integration error log |
| Business processes stuck past SLA | Track; aim for 0 | BP monitor |
| Release regression tests completed before production | 100% | Release checklist |
| Data quality exceptions | Falling | Monthly data quality report |

---

## Sources

Checked 2026-10-23.

- Missouri Attorney General, Sunshine Law booklet: https://oa.mo.gov/sites/default/files/missourisunshinelaw2020.pdf
- Missouri DSS, New Hire Reporting: https://missouriemployer.dss.mo.gov/NewHireInfo.aspx
