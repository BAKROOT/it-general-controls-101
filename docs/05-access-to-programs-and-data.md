# 05 — Access to programs and data

> **In plain English:** Only the right people should be able to get into a system, and only to the parts they actually need. This domain is about controlling and proving that.

This is the largest and most heavily tested ITGC domain, because organizations have huge numbers of users and access changes every single day. Sometimes called **logical access** or **security**, it answers one question: *who can do what, and should they?*

## A real-world analogy

Think of a bank branch. Not everyone gets the same keys. Tellers can open their own drawer but not the vault. The vault needs two managers together (segregation of duties). New employees get keys only after HR confirms they're hired and their supervisor signs off. When someone leaves, security collects their keys *that day*. Periodically, the branch manager reviews the key list to make sure it still matches who works there. Every one of those practices has a direct ITGC equivalent.

## The core controls in this domain

### 1. Provisioning and deprovisioning

- **Provisioning** = granting access. Good practice: access is requested, tied to a job role, and approved by the right manager *before* it's granted.
- **Deprovisioning** = removing access when someone leaves or changes roles. This should happen promptly — ideally same-day for terminations. A former employee (or a mover who kept old rights) is one of the most common and dangerous findings.

### 2. Least privilege

**Least privilege** means giving each person only the access they need to do their job — nothing more. A junior analyst doesn't need the ability to delete accounts. Over-provisioning quietly accumulates ("access creep") and is a frequent audit issue, especially after people change roles but keep old rights.

### 3. Segregation of duties (SoD)

**Segregation of duties** splits conflicting responsibilities so no single person can both commit and conceal an error or fraud. Classic example: the person who *creates* a vendor should not also *approve payments* to vendors. In access terms, no single user should hold that toxic combination of permissions.

### 4. Privileged access

**Privileged access** is the powerful "admin/superuser" access that can change configurations, grant other people rights, or edit data directly. Because it's so powerful, it needs extra control: limited to a few named people, logged, monitored, and often granted only temporarily ("just-in-time"). A developer with standing admin rights in production is a textbook red flag.

### 5. Periodic user access reviews (UAR)

A **User Access Review** is a scheduled check (often quarterly) where managers or system owners look at everyone with access and confirm it's still appropriate — revoking anything that isn't. This is the safety net that catches access that slipped through provisioning/deprovisioning. See the worked [access-review example](../examples/walkthrough-access-review.md) and the [checklist template](../templates/access-review-checklist.md).

### 6. Authentication (MFA and password policy)

**Authentication** is proving you are who you claim to be. Controls here include a strong **password policy** (length, complexity, rotation where appropriate) and **Multi-Factor Authentication (MFA)** — requiring a second factor like a phone code, so a stolen password alone isn't enough to get in. Many organizations also use **Role-Based Access Control (RBAC)**, granting access by job role rather than person by person, which makes provisioning and reviews far cleaner.

## Why an auditor cares

Access is the front door to every financial system. If access is loose, none of the other controls can be trusted — someone could bypass the 3-way match, post fake entries, or alter data. Auditors test this domain hard: they check that new access was approved, that terminated users were removed promptly, that privileged access is limited and monitored, and that access reviews actually happened *with evidence*. Because access changes constantly, this is also where **sampling** and **population completeness** (see [chapter 09](09-how-controls-are-tested.md)) matter most.

## Concrete control examples

- **Joiners:** A new hire receives access only after a ticket with manager approval specifying their role (RBAC).
- **Leavers:** HR's termination feed automatically triggers access removal within 24 hours, and the auditor tests a sample of terminations for timely removal.
- **Privileged access:** Only three named engineers have production admin rights; their actions are logged and reviewed monthly.
- **UAR:** Every quarter, department heads certify their team's access to the ERP; revocations are ticketed and tracked to completion.

## Key terms

- **[Provisioning](../glossary.md)** / **[Deprovisioning](../glossary.md)** — granting / removing access.
- **[Least privilege](../glossary.md)** — only the access needed, nothing more.
- **[Segregation of duties (SoD)](../glossary.md)** — splitting conflicting duties.
- **[Privileged access](../glossary.md)** — powerful admin/superuser access.
- **[UAR](../glossary.md)** — periodic user access review.
- **[MFA](../glossary.md)** — multi-factor authentication.
- **[RBAC](../glossary.md)** — role-based access control.

Next up: **[06 — Change management](06-change-management.md)**
