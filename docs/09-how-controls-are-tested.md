# 09 — How controls are tested

> **In plain English:** Auditors don't just ask "do you have a control?" They check two things: is it *designed* to work, and did it *actually work* every time over the whole period — proven with real evidence.

Now that you know the four domains, here's how an auditor actually evaluates them.

## Two questions: design vs operating effectiveness

Every control test answers two separate questions:

1. **Design effectiveness** — *If this control operates as intended, would it actually prevent or detect the problem it's meant to?* A control can be well-intentioned but poorly designed (e.g., an access review that only looks at active users would miss terminated ones).
2. **Operating effectiveness** — *Did the control actually operate, consistently, throughout the whole period?* A well-designed control that got skipped in three of twelve months is not operating effectively.

Both must hold. A beautifully designed control that nobody runs is worthless; a diligently run control that checks the wrong thing is also worthless.

## A real-world analogy

Think of a smoke detector. **Design effectiveness** asks: is it the right kind of detector, placed in the right spot, wired to alarm? **Operating effectiveness** asks: over the past year, did it actually have working batteries and would it have gone off every single time? You test the first by inspecting it; you test the second by checking the maintenance log and pressing the button.

## The main testing techniques

### Walkthroughs

A **walkthrough** follows a single transaction from start to finish to confirm the control works the way people say it does. It's how auditors first understand and confirm the *design*. The two [worked examples](../examples/) in this repo are essentially walkthroughs.

### Sampling

Because it's impossible to re-check thousands of items, auditors test a **sample** — a subset chosen from the full population. The sample size depends on how often the control runs (a daily control needs a bigger sample than an annual one). If the sample is clean, the auditor infers the whole population is likely fine; if the sample has exceptions, they dig deeper.

### Population completeness

Sampling only means something if you're sampling from the **complete** population. If an auditor tests "10 of the year's changes" but the list of changes was itself incomplete, the test proves little. So a crucial, often-overlooked step is establishing **population completeness** — proving the list of all changes, all users, or all jobs is truly whole (for example, by reconciling it to an independent source). Beginners frequently underestimate this; auditors do not.

## What "evidence" looks like

Auditors don't take anyone's word for it — they want **evidence** that a control operated. Typical evidence includes:

- **Tickets** (change requests, incidents, access requests)
- **Approvals** (emails, workflow sign-offs, signatures)
- **Screenshots** (a configuration setting, a system status)
- **Logs** (access logs, deployment logs, job-run logs)
- **Reports** (a completed access review, a backup-restore result)

Good evidence is dated, attributable to a person, and hard to fake after the fact. "We always do it" is not evidence; the signed approval ticket is.

## The Risk-Control Matrix (RCM)

The **Risk-Control Matrix** is the master table that ties everything together. Each row typically captures: the **risk**, the **control** that addresses it, the **domain**, whether it's **preventive or detective**, how often it runs (**frequency**), and how it's **tested** (with what evidence). The RCM is the auditor's map of the whole ITGC program — see the fill-in [control-matrix template](../templates/control-matrix.md) with example rows.

## Why an auditor cares

Design vs operating effectiveness, sampling, and population completeness are the auditor's core method. They're how a small team can give assurance over a year of activity without checking every single item — *provided* the population is complete and the evidence is solid. Sloppiness here is where audits go wrong.

## Concrete testing examples

- **Design:** The auditor reviews the access-review procedure and confirms it covers *all* users, including privileged and service accounts.
- **Operating (sample):** From the complete list of 240 changes, the auditor selects 25 and verifies each had approval, testing, and independent deployment.
- **Completeness:** The change list is reconciled to the deployment tool's records to prove no changes are missing before sampling.
- **Evidence:** For each sampled item, the auditor retains the ticket, approval, and deployment log.

## Key terms

- **[Design effectiveness](../glossary.md)** — would the control work if it operated as intended?
- **[Operating effectiveness](../glossary.md)** — did it actually operate consistently all period?
- **[Walkthrough](../glossary.md)** — following one transaction end to end.
- **[Population](../glossary.md)** — the complete set the control applies to.
- **[Evidence](../glossary.md)** — proof a control ran.
- **[RCM](../glossary.md)** — risk-control matrix.

Next up: **[10 — Roles and responsibilities](10-roles-and-responsibilities.md)**
