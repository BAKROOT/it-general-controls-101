# 04 — The four domains

> **In plain English:** Almost every ITGC you'll ever meet fits into one of four buckets: who can get in, how software changes, how new systems are built, and how the machines are run.

## The four pillars

IT General Controls are traditionally organized into **four domains**. If you remember these four buckets, you have the skeleton of the entire subject. Everything else hangs off them.

| # | Domain | One-line purpose | Deep-dive chapter |
|---|--------|------------------|-------------------|
| 1 | **Access to Programs and Data** | Make sure only the right people can get into systems and data — and only to the extent they need. | [05](05-access-to-programs-and-data.md) |
| 2 | **Change Management** | Make sure changes to existing systems are requested, approved, tested, and deployed safely. | [06](06-change-management.md) |
| 3 | **System Development (SDLC)** | Make sure *new* systems and major implementations are built or bought carefully and go live only when ready. | [07](07-sdlc.md) |
| 4 | **Computer Operations** | Make sure the systems keep running: jobs, backups, incidents, and the physical/cloud environment. | [08](08-computer-operations.md) |

## A real-world analogy: running an apartment building

Picture yourself managing an apartment building:

- **Access** = who has keys and to which doors. You don't give the new tenant a master key to every apartment.
- **Change management** = how you handle repairs and renovations to *existing* units — a request, an approved plan, a licensed contractor, an inspection before residents move back in.
- **Development (SDLC)** = building a *brand-new* wing — architecture, permits, construction, and a final inspection before anyone lives there.
- **Operations** = the daily running — the boiler, elevators, trash pickup, fire alarms, and a backup generator for outages.

A trustworthy building needs all four. So does a trustworthy IT environment.

## How the domains relate

The domains overlap in one very important idea: **segregation of duties (SoD)** — making sure no single person can both make a change and hide it. You'll see SoD appear in access ("no one should approve their own access"), change ("the developer shouldn't deploy their own code"), and operations. Keep an eye out for it; it's the connective tissue of ITGC.

Access is usually the *largest* domain by volume — most organizations have far more users and access events than code changes or new-system projects. That's why [chapter 05](05-access-to-programs-and-data.md) is the meatiest.

## Why an auditor cares

Auditors use these four domains as their checklist for completeness. If a company can show strong controls in all four, the auditor has confidence that the environment supporting the financial applications is trustworthy. A gap in any single domain can undermine reliance on the automated controls that depend on it.

## Concrete examples, one per domain

- **Access:** Quarterly, each manager reviews and re-confirms which of their staff can access the accounting system.
- **Change:** A bug fix moves through request → approval → testing → an independent person deploying it to production.
- **Development:** A new expense-management platform is configured, tested, and formally signed off before replacing the old one.
- **Operations:** The nightly billing job is monitored; if it fails, an alert creates a ticket that someone must resolve.

## Key terms

- **[Segregation of duties (SoD)](../glossary.md)** — splitting sensitive tasks so no one person can act unchecked.
- **[Change management](../glossary.md)** — controlled process for changing existing systems.
- **[SDLC](../glossary.md)** — controlled process for building/implementing new systems.
- **[Logical access](../glossary.md)** — electronic access to systems and data.

Next up: **[05 — Access to programs and data](05-access-to-programs-and-data.md)**
