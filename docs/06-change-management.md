# 06 — Change management

> **In plain English:** When you change software that's already running, you follow a controlled path — request, approve, test, approve again, and have *someone other than the developer* put it live — so nothing breaks or sneaks in unapproved.

Change management covers changes to *existing* systems: bug fixes, configuration tweaks, updates, and enhancements. (Building brand-new systems is [SDLC](07-sdlc.md), the next chapter.)

## A real-world analogy

Imagine editing a published cookbook that restaurants worldwide are cooking from. You can't just scribble in a new ingredient. You submit the proposed change, an editor approves it, a test kitchen cooks the revised recipe to confirm it works, a second editor signs off, and finally a *different* person than the recipe author publishes the update. That separation stops a rogue or careless edit from reaching every kitchen unchecked. Software change management works exactly the same way.

## The standard change flow

A well-controlled change moves through clear stages, each leaving evidence:

```
Request → Approval → Development → Testing → Approval to deploy → Migration to production
                                                                     (by someone other
                                                                      than the developer)
```

1. **Request.** Someone raises a change ticket describing what and why.
2. **Approval.** An authorized person approves the change *before* work starts.
3. **Development.** A developer builds the change in a non-production environment.
4. **Testing.** The change is tested (functionally, and often via user acceptance testing) to confirm it works and doesn't break anything.
5. **Approval to deploy.** A final go/no-go sign-off.
6. **Migration to production.** The change is moved live — critically, **by someone other than the developer**.

## Why the developer shouldn't deploy their own code

This is **segregation of duties (SoD)** applied to change. If the same person can write code *and* push it to production unchecked, they could deploy an untested, unapproved, or malicious change and no independent eye would ever see it. Separating the developer from the deployer means at least two people are involved, dramatically reducing the risk of accidents and fraud. See it in action in the [change-ticket walkthrough](../examples/walkthrough-change-ticket.md).

## Emergency changes

Sometimes production is broken *now* and there's no time for the full process. **Emergency changes** are allowed — but with a catch: the approvals and testing evidence are documented immediately *after* the fix, and the change is reviewed retroactively. Auditors specifically check that emergency changes weren't used as a loophole to skip controls, and that each one was genuinely urgent and properly documented after the fact.

## Traceability

A strong change process is **traceable**: from the ticket you can find the approval, the test results, the deploy approval, and who moved it to production — and vice versa. If an auditor picks any production change, they should be able to reconstruct its whole story from the records. If a change appears in production with no matching ticket, that's a serious red flag (an "unauthorized change").

## Why an auditor cares

Automated application controls (like our 3-way match) live in code and configuration. An uncontrolled change could silently disable or alter them. Change management is the assurance that *nothing reached production without being approved, tested, and deployed by an independent person*. Without it, the auditor can't trust that the control they tested in January is the same control that ran in December.

## Concrete control examples

- **Approval before work:** No change ticket moves to development without a documented approval.
- **Test evidence:** Each change has attached test results (and UAT sign-off for significant changes).
- **Developer/deployer separation:** The deployment log shows the person who released the change differs from the person who wrote it.
- **No orphan changes:** A periodic comparison confirms every production change maps to an approved ticket.

## Key terms

- **[Change management](../glossary.md)** — controlled process for changing existing systems.
- **[Segregation of duties (SoD)](../glossary.md)** — developer ≠ deployer.
- **[Emergency change](../glossary.md)** — urgent fix documented after the fact.
- **[Evidence](../glossary.md)** — tickets, approvals, and test results proving the process ran.

Next up: **[07 — SDLC](07-sdlc.md)**
