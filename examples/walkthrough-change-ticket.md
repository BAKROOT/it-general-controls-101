# Worked example: a change ticket, end to end

> **What this shows:** How the change-management control from [chapter 06](../docs/06-change-management.md) works for one real change — with special attention to why the **developer doesn't deploy their own code**. Names and company are fictional.

## The setup

**Company:** Northwind Retail (fictional). **System:** *LedgerPro*, the accounting application. **The change:** the tax-rate lookup used when posting invoices needs updating because a state changed its sales-tax rate. **Control (from the RCM, IDs CM-01 and CM-02):** *changes are approved and tested before deployment, and are deployed by someone other than the developer.*

**Cast:** Sofia (developer), Ken (change approver / Finance systems owner), Ravi (QA tester), and Lena (release manager who deploys). Notice that's four different people — that separation is the whole point.

## Step 1 — Request

Sofia opens change ticket **CHG-4471**. She writes what's changing (the tax-rate table for one state), why (the state's rate changed effective next month), the risk if it's wrong (invoices would compute the wrong tax → revenue and liabilities misstated), and a **rollback plan** (revert to the previous tax-table version). Nothing gets built yet.

## Step 2 — Approval (before any work)

Ken reviews CHG-4471. Because this change touches how money is calculated, he checks the effective date and the source for the new rate, then marks the ticket **Approved** and dates it. *Key point: approval comes **before** development, and Ken is not the person writing the code.*

## Step 3 — Development (in a safe environment)

Only now does Sofia make the change — in a **non-production (dev) environment**, never directly in production. She updates the tax-rate configuration and links her work to CHG-4471.

## Step 4 — Testing

Ravi (QA) tests the change: he posts sample invoices for the affected state and confirms the new rate is applied correctly, and that invoices for *other* states are unaffected (a quick regression check). He attaches the test results to the ticket and marks it **Pass**. For a change like this, Finance also does a brief **UAT** to confirm the numbers look right.

## Step 5 — Approval to deploy (go/no-go)

With passing tests attached, Ken gives the final **"Go"** to deploy and dates it. The ticket now contains: the request, the pre-work approval, the test evidence, and the deploy approval — a complete story.

## Step 6 — Deployment by someone other than the developer

Here's the crucial control. **Lena**, the release manager, deploys the change to production — **not Sofia**, who wrote it. Lena confirms the ticket has approval and passing tests, deploys during the change window, and records the deployment in the release log (which captures that the **author was Sofia and the deployer was Lena**).

### Why not just let Sofia deploy her own change?

Because that would collapse two duties into one person. If a developer can both write *and* release code unchecked, they could push something untested, unapproved, or malicious — for example, quietly widening a tax rule in their own favor — and no independent person would ever see it before it hit real transactions. Keeping the **developer separate from the deployer** guarantees at least two sets of eyes and a second point of accountability. This is **segregation of duties (SoD)** in its most common ITGC form.

## Step 7 — Post-deployment verification

After go-live, Lena and Sofia confirm invoices for the affected state now compute the correct tax, and that nothing else broke. If it had failed, the rollback plan from Step 1 would kick in. CHG-4471 is closed with the verification noted.

## Step 8 — What the auditor does later

At audit time, the auditor:

1. Establishes the **complete population** of production changes in the period and reconciles it to the deployment tool (so no change is hidden).
2. **Samples** changes — and CHG-4471 is picked.
3. For CHG-4471, confirms: approval existed *before* work, test evidence is attached, deploy was approved, and — checking the release log — the **deployer (Lena) differs from the developer (Sofia)**.

Everything ties out, so the control is operating effectively, and the auditor can trust that LedgerPro's tax calculation wasn't changed without control.

## The lessons

- The controlled flow (**request → approve → test → approve → deploy**) leaves a trail that *is* the evidence.
- **Approval comes before work**, not after.
- **Developer ≠ deployer.** This single separation prevents a huge class of accidents and fraud.
- **Population completeness** protects the whole test — a change with no ticket ("orphan change") is a serious red flag.

## Try it yourself

Document a change you know using the [change-request form](../templates/change-request-form.md), and add the control as a row in the [control matrix](../templates/control-matrix.md).

## Related

- Concept: [06 — Change management](../docs/06-change-management.md)
- Testing: [09 — How controls are tested](../docs/09-how-controls-are-tested.md)
- Deficiencies: [11 — Common deficiencies](../docs/11-common-deficiencies.md)
