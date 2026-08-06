# 11 — Common deficiencies

> **In plain English:** These are the problems auditors find over and over. For each one, know the *risk* it creates and the *fix* (remediation) — and understand how bad a deficiency has to be before it becomes a big deal.

A **deficiency** is simply a control that's missing or not working as intended. Most are ordinary and fixable. This chapter shows the greatest hits and how severity is rated.

## A real-world analogy

A building inspector finds the same issues again and again: a fire exit that's blocked, a smoke detector with no battery, a door that should auto-lock but doesn't. None of these mean the building will burn down — but each raises the *risk*, and the inspector rates how serious each is. ITGC deficiencies work the same way.

## The classic findings

### 1. Terminated user still has active access

- **What it is:** An employee left the company weeks or months ago, but their account still works.
- **Risk:** A former insider (or anyone who compromises the dormant account) could access or alter financial data unnoticed. It's an access-control failure with direct fraud potential.
- **Remediation:** Tighten deprovisioning so terminations trigger prompt access removal (ideally automated from the HR feed); run a clean-up to disable the orphaned accounts; add a periodic reconciliation of active accounts to active employees.

### 2. Developer with production access

- **What it is:** A developer can push their own code (or edit data) directly in production.
- **Risk:** Breaks **segregation of duties** — the developer could deploy untested, unapproved, or malicious changes with no independent check, including changes that disable an automated financial control.
- **Remediation:** Remove standing developer access to production; require a separate deployer; where emergency developer access is truly needed, make it temporary, logged, and reviewed after the fact.

### 3. Missing change approval

- **What it is:** A change reached production but there's no evidence it was approved (or tested) beforehand.
- **Risk:** Uncontrolled changes can break functionality or silently alter automated controls, undermining reliance on the affected application.
- **Remediation:** Enforce approval gates in the change tool so a change *cannot* be deployed without recorded approval and test evidence; investigate the unapproved change; retrain the team.

### 4. No evidence of an access review

- **What it is:** The company says it does quarterly access reviews, but can't produce the completed, dated, signed review for the period.
- **Risk:** Without the review, inappropriate access (from role changes, missed terminations) accumulates undetected. And from the auditor's view: *if it isn't evidenced, it didn't happen.*
- **Remediation:** Re-perform the review and retain the completed artifact; formalize the process so each review produces dated, attributable evidence going forward.

## How severity is rated

Not every deficiency is equal. In SOX terms, they escalate on a three-step ladder based on the *magnitude* of a potential misstatement and the *likelihood* it wouldn't be caught:

| Level | Rough meaning | Consequence |
|-------|---------------|-------------|
| **Deficiency** | A control is missing or not operating, but the potential impact is limited. | Fix it; usually no external disclosure. |
| **Significant deficiency** | Serious enough to deserve the attention of those charged with governance (e.g., the audit committee), but less severe than a material weakness. | Reported to the audit committee; tracked to remediation. |
| **Material weakness** | A reasonable possibility that a *material* misstatement wouldn't be prevented or caught in time. | Must be **publicly disclosed**; can hit stock price and credibility. |

A helpful way to think about it: the same finding (say, a developer with production access) might be a minor deficiency in a small, low-risk system, but a material weakness if that system directly produces the financial statements and there are no [compensating controls](../glossary.md). **Severity depends on impact and likelihood, not just the label of the finding.**

## Why an auditor cares

Auditors are required to evaluate and communicate the severity of every deficiency, because severity drives the audit opinion and what management must disclose. They also look for **compensating controls** — an alternative control that reduces the risk of a deficiency (e.g., if developers have production access but *every* change is independently logged and reviewed, the risk is partly mitigated). Remediation isn't done until the fix is proven to operate, which usually means re-testing in a later period.

## Concrete remediation examples

- **Automated deprovisioning:** Wire access removal to the HR termination feed and reconcile monthly.
- **Enforced gates:** Configure the deployment pipeline to block releases without recorded approval and test evidence.
- **Independent deploy:** Route all production releases through a release manager who is not the author.
- **Evidenced reviews:** Generate a dated, signed access-review report each quarter and store it centrally.

## Key terms

- **[Deficiency](../glossary.md)** — a control missing or not working.
- **[Significant deficiency](../glossary.md)** — serious enough to merit governance attention.
- **[Material weakness](../glossary.md)** — reasonable chance a material misstatement is missed; disclosed publicly.
- **[Compensating control](../glossary.md)** — an alternative control that offsets a weakness.
- **[Remediation](../glossary.md)** — fixing a deficiency and proving the fix works.

Next up: **[12 — Glossary and next steps](12-glossary-and-next-steps.md)**
