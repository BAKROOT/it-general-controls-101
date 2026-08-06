# 10 — Roles and responsibilities

> **In plain English:** Lots of different people touch ITGC. Knowing who owns a control, who checks it, and who gives the final opinion keeps everyone honest — and it's a form of segregation of duties at the organizational level.

## A real-world analogy

Think of food safety in a restaurant. The **cook** follows hygiene rules (owns the control). The **shift manager** spot-checks that they did (management oversight). The **head office quality team** audits multiple restaurants (internal audit). And an **independent health inspector** shows up to give an official rating the public can trust (external auditor). Each layer is more independent than the last — and that independence is exactly the point.

## The key players

### Control owner

The **control owner** is the person responsible for a specific control actually operating — for example, the IT manager who runs the quarterly access review, or the release manager who ensures developers don't deploy their own code. They're the "cook": closest to the work, accountable for doing it and keeping the evidence.

### IT (operations and security)

The broader **IT function** performs many controls day to day: provisioning access, deploying approved changes, running and monitoring jobs, managing backups and incidents. They generate most of the evidence auditors later examine.

### Internal audit and the three lines of defense

Many organizations use the **three lines of defense** model to organize accountability:

| Line | Who | Role |
|------|-----|------|
| **1st line** | Operations / control owners | *Own and operate* the controls day to day. |
| **2nd line** | Risk & compliance functions | *Oversee and support* — set policy, monitor, challenge. |
| **3rd line** | Internal audit | *Independently assure* — test whether controls really work and report to the board/audit committee. |

**Internal audit** is independent of the day-to-day operations it reviews. It reports findings to leadership and the audit committee, and it's often the group that runs internal ITGC testing before the external auditors arrive.

### External auditor

The **external auditor** is an independent firm that gives the official opinion the outside world relies on. For SOX, they independently test ITGC (and controls generally) and opine on whether internal control over financial reporting is effective. They may *rely on* internal audit's work to a degree, but they reach their own conclusion.

### Management and the assertion

Under [SOX](02-why-it-matters.md), **management** must make a formal **assertion** — a signed statement that internal control over financial reporting is effective. This is not a casual claim; executives are personally accountable for it. Everything below (control owners doing the work, keeping evidence; internal audit testing) exists partly to support management being able to make that assertion honestly.

## Why the separation matters

Notice the increasing independence: the control owner operates it, a separate risk/compliance function oversees it, internal audit independently tests it, and the external auditor independently opines. That layering is **segregation of duties at the organizational level** — no single group both performs a control *and* provides the final independent assurance that it works. It's the same principle as "the developer shouldn't deploy their own code," just scaled up to the whole organization.

## Why an auditor cares

Auditors need to know *who* is responsible for each control so they can request the right evidence from the right person, and assess whether the person reviewing a control is sufficiently independent from the person performing it. If the same person operates and "reviews" a control, that review isn't really independent — a design weakness.

## Concrete examples

- **Control owner:** The IAM (identity and access management) lead owns and evidences the quarterly access review.
- **1st vs 3rd line:** IT operations runs backups (1st line); internal audit independently tests that restores work (3rd line).
- **Management assertion:** The CFO and CEO sign the SOX 404 assertion, supported by the documented control evidence.
- **External reliance:** The external auditor reviews internal audit's ITGC testing, then performs their own independent sample tests.

## Key terms

- **Control owner** — the person accountable for a control operating. See [glossary](../glossary.md).
- **[Three lines of defense](../glossary.md)** — operations, oversight, and independent audit.
- **[Reliance](../glossary.md)** — external auditors leaning on internal audit's work.
- **Management assertion** — leadership's formal statement that controls are effective.

Next up: **[11 — Common deficiencies](11-common-deficiencies.md)**
