# Worked example: a user access review, end to end

> **What this shows:** How the abstract "periodic user access review" control from [chapter 05](../docs/05-access-to-programs-and-data.md) actually plays out — including one problem it catches. Names and company are fictional.

## The setup

**Company:** Northwind Retail (fictional). **System:** *LedgerPro*, the accounting application that feeds the financial statements. **Control (from the RCM, ID AC-02):** *Every quarter, each manager reviews and certifies that their team's LedgerPro access is still appropriate; anything inappropriate is revoked.*

**Cast:** Priya (IAM Lead, runs the review), Marcus (Finance Manager, certifies his team), and — importantly — Dana, an analyst who transferred out of Finance two months ago.

## Step 1 — Priya pulls a complete population

On April 1, Priya exports the full list of everyone with LedgerPro access: **48 accounts**. Crucially, she doesn't stop there. She reconciles the export to LedgerPro's admin console total to prove it's **complete** (all 48, including 3 privileged admins and 2 service accounts), and saves the export with a timestamp and her name. *Why it matters: if the list were missing people, the whole review would be meaningless — see [population completeness](../docs/09-how-controls-are-tested.md).*

## Step 2 — Managers review their people

Priya sends each manager only their team's slice. Marcus receives his list of 11 Finance users and goes line by line, checking each against two questions: *is this person still on my team, and is their access level right for their current job?*

Most are fine — he certifies them. But he hits a snag on one line: **Dana**.

## Step 3 — The review catches a problem

Dana transferred from Finance to Marketing two months ago. Her new role has nothing to do with the accounting system, yet she **still has LedgerPro access** — a classic case of "access creep" that provisioning/deprovisioning missed during her role change. This breaks **least privilege**: she can see and potentially post to a financial system she no longer has any business reason to touch.

Marcus marks Dana's line **"Revoke."**

## Step 4 — Action the revocation

Priya raises a ticket (CHG-Access-2291) to remove Dana's LedgerPro access. The next day she confirms in LedgerPro that the account is disabled — and saves that confirmation. *The key point: the review isn't "done" when Marcus says "revoke"; it's done when the access is actually gone and there's proof.*

## Step 5 — Sign-off and evidence

Every manager signs and dates their certification. Priya assembles the evidence package:

- the timestamped population export (48 accounts) + the completeness reconciliation,
- each manager's signed certification,
- the revocation ticket CHG-Access-2291 and the screenshot showing Dana's account disabled,
- a short summary noting one exception (Dana) and its resolution.

She stores it all in the controls repository for the Q1 review.

## Step 6 — What the auditor does later

At audit time, the external auditor tests this control:

1. **Completeness:** They re-reconcile the 48-account population to an independent source. It ties out. Good.
2. **Design:** They confirm the review covered *all* account types, including the privileged and service accounts. It did.
3. **Operating effectiveness:** They pick a sample of users and confirm each was genuinely certified, and they specifically check that Dana's revocation was completed on time. The evidence holds.

Conclusion: the control operated effectively. Because access is controlled, the auditor gains comfort to **rely** on LedgerPro's automated controls.

## The lessons

- A UAR is a **detective** safety net — it caught the access creep that slipped through when Dana changed roles.
- **Completeness first.** The review is only as good as the population it started from.
- **Evidence, not intention.** "Marcus reviewed it" means nothing without the signed certification and the proof the revocation completed.
- **Follow-through matters.** The control isn't finished until the access is actually removed.

## Try it yourself

Run this against a system you know using the [access-review checklist](../templates/access-review-checklist.md), and add a row for it in the [control matrix](../templates/control-matrix.md).

## Related

- Concept: [05 — Access to programs and data](../docs/05-access-to-programs-and-data.md)
- Testing: [09 — How controls are tested](../docs/09-how-controls-are-tested.md)
- Deficiencies: [11 — Common deficiencies](../docs/11-common-deficiencies.md)
