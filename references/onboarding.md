# Onboarding — Workday County HR Reference

## Overview

Onboarding runs from offer acceptance through the end of probation. In county government it
starts with position control (the position must be approved and funded), includes
compliance steps with hard deadlines (Form I-9, new hire reporting), and ends when the new
employee is productive and knows their rights and obligations.

> ⚠️ LEGAL NOTE: Educational information only, not legal advice. Pre-employment checks
  (background, drug testing, medical exams) carry legal limits. Check with your state labor
  agency or an employment attorney — for a county, usually the county counselor — before
  adding or changing any pre-employment requirement.

---

## Before Day 1

| Step | Owner | Notes |
|---|---|---|
| Confirm position is approved and funded | HR + Finance | Position control — never hire into an unfunded position |
| Offer letter issued and accepted | HR | Contingencies stated (background check, license, drug test if required for the job) |
| Background check | HR | Use FCRA-compliant process with a consumer reporting agency `[VERIFY: FCRA pre-adverse/adverse action steps at ftc.gov or consumerfinance.gov]` |
| Medical exam (if job requires) | HR | Only after a conditional offer, and only if required of everyone in the job category `[VERIFY: ADA post-offer medical exam rule, 29 CFR 1630.14(b)]` |
| Hire business process | HR | Staffing > Hire > Select Position > Hire |
| Onboarding tasks assigned | Workday | Personal data, tax forms, direct deposit, policy acknowledgments |
| IT account and equipment | IT | Request at least 5 business days ahead |
| Workspace, keys, badge | Department | Ready on Day 1 |

> Navigation based on standard Workday HCM. Tenant customization varies — verify in your environment.

---

## Day 1 to Day 3 — Compliance Deadlines

| Item | Deadline | Source |
|---|---|---|
| Form I-9 Section 1 (employee) | `[VERIFY: no later than first day of employment — USCIS M-274]` | — |
| Form I-9 Section 2 (employer) | Within 3 business days of the first day of employment; first day if the job lasts less than 3 business days | USCIS M-274 |
| E-Verify case (if enrolled) | `[VERIFY: E-Verify case creation deadline — no later than 3rd business day]` | — |
| **Missouri** new hire report | Within 20 calendar days of hire | Missouri DSS |
| FMLA general notice | At hire, if not in a handbook | DOL Fact Sheet #28D |
| W-4 and Missouri withholding form | Before first payroll | IRS / Missouri DOR |

**Missouri:** public employers must participate in a federal work authorization program
`[VERIFY: RSMo 285.530 scope for counties]`.

---

## Workday Onboarding Tasks

Configure the onboarding business process to assign:

1. Personal information and emergency contacts
2. Federal W-4 and state withholding
3. Direct deposit
4. Form I-9 Section 1 (if using Workday I-9) or link to the I-9 system
5. Benefits enrollment event (new hire window) — see references/benefits.md
6. Retirement enrollment (LAGERS or other plan) where the position is eligible
7. Policy acknowledgments: handbook, harassment policy, computer use, Sunshine Law awareness, safety
8. Required training assignments — see references/learning-development.md
9. Self-identification forms (voluntary): race/ethnicity, disability, veteran status

**Watch out:** the new hire benefits window is short. Send a reminder at day 10 and day 20.

---

## The First 90 Days

| When | What |
|---|---|
| Day 1 | Welcome, workspace, introductions, safety orientation, systems login |
| Week 1 | Job expectations, schedule, timekeeping (Me > Time > Enter Time), who to ask |
| Day 30 | Manager check-in: what's working, what's unclear |
| Day 60 | Manager check-in; training progress |
| Day 90 | Structured check-in; early performance feedback; HR pulse survey |
| End of probation | Decision documented before the end date — see references/performance.md |

---

## Government-Specific Onboarding Topics

- **Civil service status:** explain probation, permanent status and appeal rights in plain language
- **Union membership:** if the position is in a bargaining unit, give the MOU and union contact information as the MOU requires
- **Public records:** emails and documents on county systems may be public records under the Missouri Sunshine Law
- **Political activity:** county rules may restrict political activity on duty; federally funded positions may be covered by the Hatch Act `[VERIFY: Hatch Act coverage of state and local employees at osc.gov]`
- **Ethics and gifts:** county ethics ordinance and Missouri ethics rules
- **Mandatory reporting:** positions in social services, health, schools or law enforcement may carry reporting duties

---

## Rehires and Transfers

- Rehire: check rehire eligibility on the prior termination record; new I-9 or reverification per USCIS rules `[VERIFY: I-9 rehire rule — within 3 years of original I-9 date]`
- Internal transfer: Change Job business process, not a new hire; check whether the new position changes FLSA status, union unit or LAGERS eligibility

---

## Onboarding KPIs

| KPI | Target | Source |
|---|---|---|
| I-9 Section 2 completed within 3 business days | 100% | I-9 system report |
| Missouri new hire reports within 20 days | 100% | State reporting log |
| Onboarding tasks complete by day 5 | >90% | Workday onboarding report |
| Benefits elections within new hire window | >98% | Workday benefits report |
| 90-day turnover | Track trend | Workday turnover report |
| New hire 90-day survey score | Track trend | Survey tool |

---

## Sources

Checked 2026-10-23.

- USCIS, M-274 section 4.0, Completing Section 2: https://uscis.gov/i-9-central/form-i-9-resources/handbook-for-employers-m-274/40-completing-section-2-employer-review-and-verification
- Missouri DSS, New Hire Reporting: https://missouriemployer.dss.mo.gov/NewHireInfo.aspx
- DOL, Fact Sheet #28D: https://www.dol.gov/agencies/whd/fact-sheets/28d-fmla-employer%20notification
- Missouri Attorney General, Sunshine Law booklet: https://oa.mo.gov/sites/default/files/missourisunshinelaw2020.pdf
