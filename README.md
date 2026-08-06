# IT General Controls 101

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Level: Beginner](https://img.shields.io/badge/level-beginner-brightgreen.svg)
![Topic: IT Audit](https://img.shields.io/badge/topic-IT%20audit%20%26%20GRC-blue.svg)
![Format: Markdown](https://img.shields.io/badge/format-Markdown-lightgrey.svg)

> A beginner-friendly end to end knowledge base built from the ground up on **IT General Controls (ITGC)**: the behind-the-scenes controls that make an organization's technology, and the financial information it produces, trustworthy.

## What is this?

This repository is a self-contained course you can read top to bottom. It explains what IT General Controls are, why auditors and regulators care about them, and how they work in real life — using plain English, everyday analogies, and worked examples. No prior IT-audit experience is required. If you can read a checklist, you can follow this.

By the end you'll understand the four core ITGC domains (access, change management, system development, and computer operations), how controls are tested, who is responsible for what, and what the most common problems (deficiencies) look like and how they get fixed.

## Audience: zero background assumed

This is written for complete beginners — new IT auditors, GRC analysts, software engineers who suddenly have "SOX season," compliance folks, students, and the merely curious. Every acronym is spelled out on first use and collected in the [glossary](glossary.md). If a sentence assumes knowledge you don't have, that's a bug — please open an issue.

## How to read this

Read the `docs/` files in numeric order — they build on each other. Start with **[00-start-here.md](docs/00-start-here.md)** for a five-minute mental model, then keep going. When you hit a term you don't recognize, click through to the [glossary](glossary.md). After the concept chapters, the [templates](templates/) give you fill-in-the-blank artifacts, and the [examples](examples/) walk two real controls end to end so the theory becomes concrete. The full reading order also lives in **[SUMMARY.md](SUMMARY.md)**.

## Table of contents

| # | Chapter | What you'll learn |
|---|---------|-------------------|
| 00 | [Start here](docs/00-start-here.md) | How to use this repo + a 5-minute mental model |
| 01 | [What is ITGC?](docs/01-what-is-itgc.md) | Definition; ITGC vs application vs entity-level controls |
| 02 | [Why it matters](docs/02-why-it-matters.md) | SOX 404, audits, "reliance," and material weakness |
| 03 | [Frameworks](docs/03-frameworks.md) | COSO, COBIT, ITIL, NIST CSF and how they connect |
| 04 | [The four domains](docs/04-the-four-domains.md) | Overview of the four ITGC pillars |
| 05 | [Access to programs & data](docs/05-access-to-programs-and-data.md) | Logical access, least privilege, SoD, MFA, UARs |
| 06 | [Change management](docs/06-change-management.md) | Request → approve → test → deploy, with SoD |
| 07 | [SDLC](docs/07-sdlc.md) | Controls over building/buying new systems |
| 08 | [Computer operations](docs/08-computer-operations.md) | Jobs, backups, incidents, physical & environmental |
| 09 | [How controls are tested](docs/09-how-controls-are-tested.md) | Design vs operating effectiveness, sampling, evidence |
| 10 | [Roles & responsibilities](docs/10-roles-and-responsibilities.md) | Control owner, IT, audit, management assertion |
| 11 | [Common deficiencies](docs/11-common-deficiencies.md) | Typical findings, risks, and remediation |
| 12 | [Glossary & next steps](docs/12-glossary-and-next-steps.md) | Certifications, further reading, careers |

### Supporting material

- **[Glossary](glossary.md)** — one-line, plain-English definitions of every term and acronym.
- **[Templates](templates/)** — [control matrix](templates/control-matrix.md), [access-review checklist](templates/access-review-checklist.md), [change-request form](templates/change-request-form.md), [audit evidence request list](templates/audit-evidence-request-list.md).
- **[Examples](examples/)** — [access-review walkthrough](examples/walkthrough-access-review.md), [change-ticket walkthrough](examples/walkthrough-change-ticket.md).
- **[Contributing](CONTRIBUTING.md)** — how to suggest edits.

## A one-line mental model

> **ITGC is the plumbing under your financial systems.** If the plumbing is sound, the numbers that come out of the taps can be trusted. If it leaks, nobody can be sure what's really flowing.

## License

Released under the [MIT License](LICENSE). Learn freely, share freely.

---

*This is an educational resource. It explains concepts and common practice; it is not professional audit, legal, or accounting advice.*
