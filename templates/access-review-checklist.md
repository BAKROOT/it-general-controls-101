# Template: User Access Review (UAR) Checklist

> **What this is:** A ready-to-use checklist for running a periodic user access review — the control that catches inappropriate access that slipped through. See [chapter 05](../docs/05-access-to-programs-and-data.md) and the [worked example](../examples/walkthrough-access-review.md).

Fill in the blanks. Anything not evidenced is treated by an auditor as not done, so keep the completed, dated, signed result.

## Header

- **System / application reviewed:** _______________________
- **Review period:** ____________  **Review frequency:** (e.g., Quarterly) __________
- **Reviewer(s) / certifier(s):** _______________________
- **Prepared by:** ____________  **Date started:** __________  **Date completed:** __________

## Step 1 — Establish a complete population

- [ ] Exported the **complete** list of all users with access as of the review date.
- [ ] Confirmed completeness (reconciled the export to an independent source, e.g., the directory or an admin count).
- [ ] Included **all** account types: standard users, **privileged/admin** accounts, **service/system** accounts, and third parties/vendors.
- [ ] Recorded the date, source system, and who generated the export (evidence).

## Step 2 — Review each user's access

For every user, confirm:

- [ ] The person is still **employed / engaged** (cross-check the HR/active-employee list).
- [ ] Their access matches their **current role** (role changes = old access removed — least privilege).
- [ ] No **segregation-of-duties (SoD)** conflicts (no toxic combinations of permissions).
- [ ] **Privileged access** is still justified and limited to those who genuinely need it.
- [ ] **Service accounts** have a documented owner and purpose.

## Step 3 — Decide and record

For each line item, mark one:

- [ ] **Certify** (access remains appropriate), or
- [ ] **Revoke / modify** (access should be removed or reduced).

Record the decision, the reviewer, and the date.

## Step 4 — Action revocations

- [ ] Raised a **ticket** for every revocation/modification.
- [ ] Confirmed each change was **actually made** in the system (not just requested).
- [ ] Tracked all revocations **to completion** and retained the closure evidence.

## Step 5 — Sign-off and retain evidence

- [ ] The reviewer/certifier **signed and dated** the completed review.
- [ ] Stored the population export, the annotated review, and the revocation tickets together.
- [ ] Noted any **exceptions** and how they were resolved.

**Certifier signature:** _______________________  **Date:** __________

## Common pitfalls to avoid

- Reviewing only *active* users and missing terminated ones still enabled.
- Forgetting **privileged** and **service** accounts.
- "Rubber-stamping" — certifying everything without genuine review.
- No proof the revocations were actually completed.

## Related

- Concept: [05 — Access to programs and data](../docs/05-access-to-programs-and-data.md)
- Example: [Access-review walkthrough](../examples/walkthrough-access-review.md)
- Glossary: [UAR](../glossary.md), [Least privilege](../glossary.md), [Privileged access](../glossary.md), [SoD](../glossary.md)
