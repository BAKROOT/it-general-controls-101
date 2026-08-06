# 00 — Start here

> **In plain English:** ITGC is the trust foundation under every financial system. If the plumbing is sound, the numbers coming out can be relied on.

Welcome. This chapter tells you how to use this knowledge base and gives you a mental model you can hold in your head for the whole journey.

## How to use this repo

Read the chapters in order, 00 through 12. Each one is short and builds on the last. Every chapter follows the same shape so you always know what you're looking at:

1. **In plain English** — a one-line summary.
2. **A real-world analogy** — the idea in everyday terms.
3. **Why an auditor cares** — the reason this matters for trust and money.
4. **Concrete control examples** — a few real controls you'd actually see.
5. **Key terms** — a quick recap linking to the [glossary](../glossary.md).

When you meet an unfamiliar word, click through to the glossary rather than pushing past it. The vocabulary *is* half the battle in IT audit.

## A five-minute mental model

Imagine a modern company. Money moves through software: orders, invoices, payroll, the general ledger. At the end of the year, leadership publishes financial statements, and investors, lenders, and regulators rely on those numbers being right.

Now ask a simple question: **how do we know the numbers are right?**

Part of the answer is *application controls* — checks inside each app that keep individual transactions clean (for example, refusing to pay an invoice that doesn't match a purchase order and a receiving record). But application controls only work if the systems around them are trustworthy: the right people have access, changes to the software are controlled, new systems are built carefully, and the machines keep running and backing up data.

That surrounding trustworthiness is **IT General Controls (ITGC)**. Think of it as the plumbing and foundation of a house. You don't admire plumbing at a dinner party, but if it leaks, everything above it is at risk. ITGC is the quiet foundation that lets everyone trust the visible results.

## The one picture to remember

```
        Financial statements   <- what the world relies on
                 ^
        Application controls   <- keep each transaction correct
                 ^
        IT General Controls    <- keep the systems themselves trustworthy
```

Read this stack from the bottom up: strong ITGC makes application controls dependable, and dependable application controls support reliable financial statements. Weaken the bottom layer and everything above it wobbles.

## What you'll be able to do after reading

- Explain what ITGC is and how it differs from application and entity-level controls.
- Name the four ITGC domains and give examples in each.
- Describe how an auditor tests a control and what "evidence" means.
- Recognize the most common findings and how they get fixed.

## Key terms

- **[ITGC](../glossary.md)** — the foundational controls over IT.
- **[Application control (ITAC)](../glossary.md)** — checks inside a specific app.
- **[Reliance](../glossary.md)** — trusting a control enough to test it less.

Next up: **[01 — What is ITGC?](01-what-is-itgc.md)**
