# Recruiting & Position Management — Workday County HR Reference

## Overview

County recruiting starts before the job posting: the position has to exist, be approved by
the board or commission, and be funded in the budget. After that, civil service rules often
govern how the job is posted, who is eligible, how candidates are scored and ranked, and who
may be selected. Workday supports the requisition, posting, candidate pipeline and offer.

> ⚠️ LEGAL NOTE: Educational information only, not legal advice. Selection procedures,
  veterans' preference, background checks and pre-employment questions carry legal limits.
  Check with your state labor agency or an employment attorney — for a county, usually the
  county counselor — before changing a selection process.

---

## Position Control First

| Check | Where |
|---|---|
| Position exists and is approved | Workday position record; board minutes |
| Position is funded for the fiscal year | Finance budget / position control list |
| Position is vacant (or approved to overfill) | Workday position status |
| Job profile is correct (FLSA status, EEO-4 category, pay grade) | Workday job profile — see references/job-classification.md |

**Watch out:** recruiting into a position that Finance shows as unfunded is the most common
county hiring error. Reconcile Workday positions to Finance position control at least quarterly.

Create a position: Staffing > Create Position.

---

## Requisition to Offer

| Step | Workday | Notes |
|---|---|---|
| 1. Create requisition | Recruiting > Create Job Requisition | Link to the approved position |
| 2. Approvals | Business process routing | Department head, HR, Finance as configured |
| 3. Posting | Career site, plus required external sites | Posting period per civil service rules |
| 4. Screen minimum qualifications | Candidate grid | Apply the posted minimums the same way to everyone |
| 5. Exam or structured scoring (if civil service) | Assessment or scoring step | Keep scoring records with the requisition |
| 6. Eligibility list / referral | Per civil service rules | Rule of three, rule of the list, or banding |
| 7. Interviews | Interview scheduling | Same core questions for every candidate |
| 8. Selection | Disposition all candidates with an accurate reason | Dispositions feed EEO and audit records |
| 9. Offer | Offer business process | Contingencies; pay within approved range |
| 10. Hire | Staffing > Hire | Hand off to references/onboarding.md |

> Navigation based on standard Workday HCM. Tenant customization varies — verify in your environment.

---

## Structured Interviews

- Write questions from the job description's essential functions
- Ask every candidate the same core questions in the same order
- Use a rating scale with behavior anchors (for example, 1 = no example; 3 = relevant example with result; 5 = strong example with measurable result)
- Panel members rate independently before discussing
- Keep notes and score sheets with the requisition record

### Questions to Avoid

Do not ask about age, race, religion, national origin, marital or family status, pregnancy,
disability or medical history, genetic information, or plans to have children. Ask whether
the candidate can perform the essential functions, with or without reasonable accommodation.

---

## Accommodations in the Hiring Process

- Offer accommodation for applications, tests and interviews in every posting
- An applicant may ask in plain language; that starts the interactive process (EEOC ADA guidance)
- Medical exams and disability-related questions only after a conditional offer `[VERIFY: 29 CFR 1630.13–1630.14 pre-offer limits]`

---

## Veterans' Preference

Some counties apply veterans' preference by ordinance or civil service rule.
`[VERIFY: whether a Missouri statute requires veterans' preference for county employment, and its terms]`
Apply the preference exactly as written and document how it was applied on each list.

---

## Background Checks

- Use a consumer reporting agency and follow FCRA notice and consent steps `[VERIFY: FCRA employer steps at ftc.gov]`
- Law enforcement and positions with access to criminal justice information have additional requirements — see references/public-safety-hr.md
- Consider job-relatedness, time since the offense, and the nature of the job for criminal history
- Local "ban the box" ordinances may apply in some Missouri cities `[VERIFY: applicable local ordinances for your county's cities]`

---

## Records and EEO

- Applicant data and selection records: retain per references/records-management.md `[VERIFY: 2-year retention for state and local governments, 29 CFR 1602.31]`
- Voluntary self-identification data stays separate from the hiring manager's view
- Candidate dispositions with accurate reasons support EEO-4 reporting and adverse impact review

### Adverse Impact Check

After a high-volume recruitment, compare selection rates by group at each step (screen, exam,
interview, offer). A common rule of thumb is the "four-fifths rule" in the Uniform Guidelines
`[VERIFY: 29 CFR 1607.4(D)]`. A large gap is a signal to review the step with counsel, not a
finding of discrimination.

---

## Recruiting KPIs

| KPI | Target | Source |
|---|---|---|
| Time to fill (requisition approved to offer accepted) | Track by job family; set local target | Workday recruiting report |
| Requisitions linked to funded positions | 100% | Position control reconciliation |
| Offer acceptance rate | >85% | Workday offer report |
| Candidates dispositioned with a reason | 100% | Workday candidate report |
| Applicants per posting | Track by job family | Workday recruiting report |
| First-year turnover of new hires | Track trend | Workday turnover report |

---

## Sources

Checked 2026-10-23.

- EEOC, Enforcement Guidance on Reasonable Accommodation and Undue Hardship under the ADA: https://www.eeoc.gov/laws/guidance/enforcement-guidance-reasonable-accommodation-and-undue-hardship-under-ada
- EEOC, EEO Data Collections (EEO-4): https://www.eeoc.gov/data/eeo-data-collections
