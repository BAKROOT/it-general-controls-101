# 01 — What is ITGC?

> **In plain English:** IT General Controls are the "house rules" for the technology environment — controlling who gets in, how software changes, how new systems are built, and how the machines are run — so the applications sitting on top can be trusted.

## The definition

**IT General Controls (ITGC)** are controls that apply broadly across an organization's IT systems and infrastructure rather than to one specific transaction. They create a stable, secure, well-run environment. When ITGC is strong, the individual business applications running in that environment can be relied upon to process data correctly.

ITGC traditionally covers four domains, which you'll meet in [chapter 04](04-the-four-domains.md): access to programs and data, change management, system development (SDLC), and computer operations.

## A real-world analogy

Think of a commercial kitchen in a restaurant. **Application controls** are the recipes — precise steps that make each individual dish come out right. But recipes only produce safe, consistent food if the *kitchen itself* is well run: only trained staff have keys (access), any change to a recipe is reviewed before it goes on the menu (change management), new kitchen stations are built to code (development), and the fridges, timers, and cleaning schedules all work (operations).

ITGC is that well-run kitchen. Nobody orders "the ITGC" off the menu, but without it you can't trust any dish that comes out.

## ITGC vs application controls vs entity-level controls

These three layers are easy to mix up. Here's the distinction:

| Layer | Scope | Example |
|-------|-------|---------|
| **Entity-level controls** | Whole organization; tone and governance | A board-approved information security policy; "tone at the top." |
| **IT General Controls (ITGC)** | The IT environment broadly | Terminated employees lose access within 24 hours; every code change is approved and tested before deployment. |
| **Application controls (ITAC)** | One transaction inside one app | A **3-way match**: the system won't pay an invoice unless it matches a purchase order *and* a goods-received note. |

Notice the relationship: entity-level controls set the environment, ITGC keeps the systems trustworthy, and application controls keep each transaction clean.

## The layered model (the key idea)

Auditors think in layers:

```
Entity-level controls   ── governance & environment ──┐
                                                        │ supports
IT General Controls     ── trustworthy IT environment ─┤
                                                        │ supports
Application controls    ── correct transactions ───────┤
                                                        │ supports
Financial statements    ── numbers the world relies on ┘
```

**ITGC supports application controls, which support the financial statements.** This is the single most important sentence in IT audit. If ITGC is weak, an auditor cannot trust that an application control (like the 3-way match) worked *every* time — because maybe someone with unauthorized access changed the rule, or an untested code change quietly broke it.

## Why an auditor cares

An auditor wants to rely on automated application controls, because relying on the computer is far more efficient than manually re-checking thousands of transactions. But they can only rely on those automated controls **if ITGC is effective**. Weak ITGC means the auditor loses that reliance and has to do much more manual work — or conclude the numbers can't be fully trusted. So ITGC is the gatekeeper for the entire audit's efficiency and conclusion.

## Concrete control examples

- **Access:** A new hire only receives system access after their manager approves a request specifying their role.
- **Change:** A developer's code change cannot reach production until a separate person approves and deploys it.
- **Operations:** Nightly backups run automatically and are test-restored periodically.
- **Development:** A new payroll system must pass user acceptance testing and get sign-off before go-live.

## Key terms

- **[ITGC](../glossary.md)** — broad controls over the IT environment.
- **[Application control (ITAC)](../glossary.md)** — a control inside one app for one transaction type.
- **[Entity-level control](../glossary.md)** — organization-wide governance control.
- **[3-way match](../glossary.md)** — invoice matched to a purchase order and receipt before payment.

Next up: **[02 — Why it matters](02-why-it-matters.md)**
