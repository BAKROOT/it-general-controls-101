# 03 — Frameworks (COSO, COBIT, ITIL, NIST)

> **In plain English:** ITGC isn't a single rulebook you buy off the shelf. It's *implemented using* well-known frameworks — COSO, COBIT, ITIL, and NIST — each of which contributes a different piece of the puzzle.

## Why frameworks exist

Left to itself, "good IT control" is vague. Frameworks turn vague good intentions into organized, comparable practices, so that different companies and auditors share a common language. A helpful way to remember the big four:

| Framework | Nickname | Answers the question |
|-----------|----------|----------------------|
| **COSO** | The *why & what* of internal control | "What does good internal control even mean?" |
| **COBIT** | IT governance map | "How do we govern and control IT specifically?" |
| **ITIL** | Operations playbook | "How do we run IT services day to day?" |
| **NIST CSF** | Security framework | "How do we protect against cyber threats?" |

**Key point:** ITGC draws on all of these but *is not any single one of them*. ITGC is the set of controls; the frameworks are the reference libraries you use to design and organize those controls.

## A real-world analogy

Building a safe, well-run house needs several codebooks: a building code (structure), an electrical code (wiring), a plumbing code (water), and a fire code (safety). No single code builds the house, and a good builder consults all of them. ITGC is the finished, livable house; COSO, COBIT, ITIL, and NIST are the codebooks the builder followed.

## COSO — the foundation of internal control

**COSO** (the *Committee of Sponsoring Organizations of the Treadway Commission*) publishes the most widely used *Internal Control — Integrated Framework*. It defines internal control through five components: control environment, risk assessment, control activities, information & communication, and monitoring.

COSO is the "why and what." It's the framework auditors map ICFR to under SOX. It doesn't tell you the technical details of an IT control — it tells you what a healthy control system looks like overall. ITGC lives inside COSO's "control activities" (and touches the others).

## COBIT — governing and controlling IT

**COBIT** (*Control Objectives for Information and Related Technologies*, from ISACA) narrows the focus to IT. It provides governance and management objectives that map neatly onto ITGC domains — access, change, development, and operations. If COSO says "you need control activities," COBIT says "here specifically are the IT objectives and practices to achieve them." Many IT auditors use COBIT as the backbone for organizing an ITGC program.

## ITIL — running IT services well

**ITIL** (*Information Technology Infrastructure Library*) is a set of best practices for **IT service management** — the operational side. It shapes how organizations handle things like change enablement, incident management, and problem management. You'll see ITIL's fingerprints all over [change management](06-change-management.md) and [computer operations](08-computer-operations.md), because those domains are fundamentally about running services reliably.

## NIST CSF — the security lens

The **NIST Cybersecurity Framework** (from the U.S. National Institute of Standards and Technology) organizes security around five functions: **Identify, Protect, Detect, Respond, Recover**. It's the go-to reference for the security side of ITGC, especially [access to programs and data](05-access-to-programs-and-data.md). Where COBIT gives the governance view, NIST CSF gives the threat-and-defense view.

## How they fit together

```
COSO      → the overall meaning of "good internal control"
  COBIT   → IT-specific control objectives (access, change, ops, dev)
  ITIL    → how to run IT services (operations & change practices)
  NIST CSF→ how to secure the environment (access & protection)
= ITGC    → the actual controls you implement, informed by all of the above
```

## Why an auditor cares

Auditors need a recognized basis for saying a control set is complete and reasonable. Mapping ITGC to COSO (for SOX) and COBIT (for IT specifics) lets them demonstrate coverage: every important IT risk has an objective, and every objective has a control. Frameworks also make findings comparable across companies and years.

## Concrete examples

- A company documents its ITGC program with **COBIT** objective references so auditors can trace risk → objective → control.
- The security team measures itself against the **NIST CSF** five functions to show access controls are comprehensive.
- The operations team follows **ITIL** incident-management practices, producing the tickets that later serve as audit evidence.
- Management maps all of this up to **COSO** to support its SOX 404 assertion.

## Key terms

- **[COSO](../glossary.md)** — framework defining what internal control is.
- **[COBIT](../glossary.md)** — IT governance and control objectives.
- **[ITIL](../glossary.md)** — IT service-management best practices.
- **[NIST CSF](../glossary.md)** — cybersecurity framework (Identify, Protect, Detect, Respond, Recover).

Next up: **[04 — The four domains](04-the-four-domains.md)**
