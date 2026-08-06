# 07 — SDLC (system development)

> **In plain English:** When you build or buy a *brand-new* system (or make a major overhaul), you follow a disciplined project process — with requirements, testing, careful data migration, and a formal go-live sign-off — so the new system is trustworthy from day one.

**SDLC** stands for **System Development Life Cycle**. This domain covers controls over creating new systems and major implementations, as opposed to the routine tweaks handled by [change management](06-change-management.md).

## SDLC vs change management — the key difference

They sound similar, so pin down the distinction:

| | **Change management ([06](06-change-management.md))** | **SDLC (this chapter)** |
|---|---|---|
| **Applies to** | Existing, live systems | New systems or major implementations |
| **Scale** | Small, frequent | Large, occasional (a project) |
| **Example** | Fix a bug in the ERP | Replace the ERP entirely |

A useful rule of thumb: change management is *maintenance* on a house you live in; SDLC is *building or buying a new house*.

## A real-world analogy

Buying or building a home follows a life cycle: figure out what you need (requirements), design it, build or purchase it, inspect it thoroughly, move your belongings in carefully (data migration), and only then get the keys and move in (go-live). Skip the inspection or move in before the wiring is finished, and you've got a dangerous house. SDLC controls make sure a new system isn't "moved into" before it's genuinely ready.

## The core controls in this domain

### 1. Requirements

Define what the system must do *before* building or buying it, with the business stakeholders' agreement. Clear, approved requirements are the yardstick everything else is measured against.

### 2. Testing

The new system is tested against those requirements — including **user acceptance testing (UAT)**, where actual business users confirm it does what they need. Testing evidence (test cases, results, sign-offs) is retained.

### 3. Data conversion / migration

When replacing an old system, existing data must be moved into the new one **completely and accurately**. This is a high-risk step: dropped or corrupted records during migration can misstate balances. Controls include reconciling record counts and key totals before and after migration, and signing off that the converted data is correct.

### 4. Go-live approval

A formal, documented **go-live decision** (sometimes a "go/no-go" or steering-committee sign-off) confirms testing passed, data converted correctly, and the business is ready. Only then does the system go into production.

## Why an auditor cares

A new financial system starts processing real money on day one. If it wasn't tested, or if data migrated incompletely, the very first numbers it produces could be wrong — and no one would have a baseline to catch it. Auditors examine major implementations closely: Were requirements defined and approved? Was there evidence of testing and UAT? Was migrated data reconciled? Was there a formal go-live sign-off? For a system that went live during the audit period, these SDLC controls are often a special area of focus.

## Concrete control examples

- **Requirements sign-off:** Business owners approve documented requirements before configuration begins.
- **UAT:** Users execute test scripts and formally sign off before go-live.
- **Data migration reconciliation:** Record counts and control totals from the legacy system are reconciled to the new system, with any differences investigated and resolved.
- **Go-live approval:** A steering committee documents a go/no-go decision confirming readiness.

## Key terms

- **[SDLC](../glossary.md)** — controlled life cycle for building/implementing new systems.
- **UAT (user acceptance testing)** — business users confirm the system meets their needs. See [glossary](../glossary.md).
- **Data conversion / migration** — moving data from an old system to a new one, completely and accurately.
- **Go-live approval** — formal sign-off that a new system is ready for production.

Next up: **[08 — Computer operations](08-computer-operations.md)**
