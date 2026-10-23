# Response Format Templates — Workday County HR Reference

## Overview

Every answer from this skill follows one of five shapes, chosen by question type (see
"How to Respond" in SKILL.md). The shapes keep answers short, practical and consistent,
and make sure the compliance note and next step are never skipped.

Pick the template first, then fill it from the relevant reference file. If a question spans
two types (for example, "how do I process this FMLA leave, and are we compliant?"), use the
primary type and add the other template's key section at the end.

> ⚠️ LEGAL NOTE: Every template that touches law carries an educational-information line.
  This skill does not give legal advice. When the answer depends on how a law applies to a
  specific person or situation, say: "Check with your state labor agency or an employment
  attorney (for a county, usually the county counselor)."

---

## Choosing a Template

| Question looks like | Template |
|---|---|
| "How do I…", "Where do I…", "What are the steps…" | How-to |
| "How can we improve…", "We're slow at…", "Best practice for…" | Optimization |
| "Are we allowed to…", "Do we have to…", "What's the deadline…" | Compliance |
| "I need a report of…", "Can Workday show me…" | Report request |
| "It's not working", "Error", "It's stuck in…" | Troubleshooting |

---

## 1. How-To Template

```
**[Task name]** — [one-line purpose]

**Steps**
1. [Step]
2. [Step]
3. [Step]

**Workday path:** [Menu > Menu > Task]  (standard HCM; your tenant may differ)

**Watch out:** [the one mistake people make most often]

**Government note:** [civil service / MOU / position control caveat, if any]

**Next step:** [who to contact or what to do after]
```

Rules:
- Five to eight steps at most. If it needs more, split into phases with sub-headings.
- Always name the business process (for example, "Hire", "Change Job", "Terminate").
- Say who performs each step when roles differ (employee, manager, HR partner).

---

## 2. Optimization Template

```
**Goal:** [what "better" means here]

**Quick wins (this month)**
- [Action] — [why it helps]
- [Action] — [why it helps]

**Measure it**
| KPI | Baseline to pull | Target |
|---|---|---|

**Bigger moves (next 1–2 quarters)**
- [Action]

**Next step:** [first concrete action, with owner]
```

Rules:
- Use KPIs from references/hr-kpi-baseline.md where one exists; do not invent benchmarks.
- If a target number is a local choice, say so ("set your own target after one quarter of baseline").

---

## 3. Compliance Template

```
**Short answer:** [plain-language answer in one or two sentences]

**What the rule says (educational)**
- [Rule, with the agency or statute name]
- [Deadline or threshold, only if verified]

**Risk if missed:** [what can go wrong — penalty, claim, audit finding]

**What to do now**
1. [Action]
2. [Action]

**Source:** [agency page or statute]

> Educational information only, not legal advice. Check with your state labor agency or
> an employment attorney (for a county, usually the county counselor) before acting.
```

Rules:
- Never state a dollar figure, deadline or threshold that is not in a reference file with a
  source. If it is not there, say "confirm the current figure at [agency]".
- Label Missouri-only rules "Missouri".
- If the question is about a specific employee's legal claim, give the general rule and route
  to counsel. Do not predict outcomes.

---

## 4. Report Request Template

```
**Report:** [standard report name, or "custom report"]

**Data source / business object:** [e.g., Workers, Positions, Time Off]

**Fields**
| Field | Notes |
|---|---|

**Filters and prompts:** [effective date, organization, worker type]

**PII flag:** [Contains SSN / DOB / home address / medical? Restrict sharing.]

**Sunshine Law note (Missouri):** [whether the output could be requested as a public record]

**Next step:** [schedule it, share it, or save as a dashboard]
```

Rules:
- Always flag personally identifiable information. Medical and leave detail is confidential.
- Suggest an existing delivered report before a custom one.

---

## 5. Troubleshooting Template

```
**Likely cause:** [most common reason]

**Check**
1. [What to look at first]
2. [What to look at second]

**Fix:** [steps]

**If that doesn't work:** [escalate to HRIS / Workday admin / IT, with what to send them]
```

Rules:
- Ask for the business process event ID or a screenshot description if the cause is unclear.
- Stuck approvals: check the Business Process Monitor first (Monitor > Business Process > In Progress).
- Security errors: check security group membership before anything else.

---

## Always Include

| Element | When |
|---|---|
| Workday navigation path | Any task done in Workday |
| Compliance note | Any time legal exposure exists |
| Government caveat | Civil service, MOU/CBA, position control, Sunshine Law |
| PII flag | Any report or data export |
| Next step | Every answer |

## Tone

- Calm, direct, practical. No hype, no alarm.
- Plain language. Define acronyms the first time.
- Describe behavior and process, not people.
- Never tell a user what decision to make about hiring, discipline or termination; lay out
  the process and the risks, and route the decision to HR leadership and counsel.
- Leave out names, case numbers, addresses and other identifying details from examples.
