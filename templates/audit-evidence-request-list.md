# Template: Audit Evidence Request List (PBC List)

> **What this is:** The list an auditor sends the company asking for the documents that prove ITGC operated. In practice it's often called the **PBC list** ("Prepared By Client"). Use it to know what to gather *before* the audit and to track what's been provided. See [chapter 09](../docs/09-how-controls-are-tested.md).

## How to use it

For each item, fill in who owns it, the due date, and the status. Attach the actual evidence and note where it's stored. Good evidence is **dated**, **attributable to a person**, and hard to alter after the fact.

- **Audit period:** ____________  **Requested by (auditor):** ____________  **Date requested:** __________

## General / entity-level

| # | Evidence requested | Owner | Due | Status | Notes |
|---|--------------------|-------|-----|--------|-------|
| G-1 | List of in-scope systems/applications for financial reporting | | | ☐ Open | |
| G-2 | IT policies (security, change, access) | | | ☐ Open | |
| G-3 | IT organization chart | | | ☐ Open | |
| G-4 | Third-party assurance reports (e.g., SOC reports) for hosted/cloud systems | | | ☐ Open | |

## Access to programs and data

| # | Evidence requested | Owner | Due | Status | Notes |
|---|--------------------|-------|-----|--------|-------|
| A-1 | Complete list of users with access (per in-scope system) + how completeness was verified | | | ☐ Open | population |
| A-2 | Sample of new-user access requests with approvals | | | ☐ Open | |
| A-3 | List of terminations in the period + evidence access was removed timely | | | ☐ Open | |
| A-4 | List of privileged/admin users + justification and monitoring evidence | | | ☐ Open | |
| A-5 | Completed periodic user access review(s) with sign-off and revocation tickets | | | ☐ Open | |
| A-6 | Password policy configuration and MFA settings (screenshots) | | | ☐ Open | |

## Change management

| # | Evidence requested | Owner | Due | Status | Notes |
|---|--------------------|-------|-----|--------|-------|
| C-1 | Complete list of production changes in the period + how completeness was verified | | | ☐ Open | population |
| C-2 | Sample of changes with approval, test evidence, and deploy approval | | | ☐ Open | |
| C-3 | Deployment logs showing developer vs deployer (SoD) | | | ☐ Open | |
| C-4 | List of emergency changes + retroactive approvals and post-reviews | | | ☐ Open | |

## System development (SDLC)

| # | Evidence requested | Owner | Due | Status | Notes |
|---|--------------------|-------|-----|--------|-------|
| S-1 | List of systems implemented/major upgrades in the period | | | ☐ Open | |
| S-2 | Approved requirements + UAT sign-off | | | ☐ Open | |
| S-3 | Data migration reconciliation (counts/totals before vs after) | | | ☐ Open | |
| S-4 | Go-live / go-no-go approval | | | ☐ Open | |

## Computer operations

| # | Evidence requested | Owner | Due | Status | Notes |
|---|--------------------|-------|-----|--------|-------|
| O-1 | Batch job schedule + evidence of monitoring and failure resolution | | | ☐ Open | |
| O-2 | Backup schedule/logs + a documented test-restore result | | | ☐ Open | |
| O-3 | Sample of incident tickets with resolution | | | ☐ Open | |
| O-4 | Physical/environmental controls evidence (badge logs) or cloud SOC report | | | ☐ Open | |

*Status legend: ☐ Open · ◐ In progress · ☑ Provided · ✗ N/A. Tip: agree the population items (A-1, C-1) first — everything else samples from them.*

## Related

- Concept: [09 — How controls are tested](../docs/09-how-controls-are-tested.md)
- Roles: [10 — Roles and responsibilities](../docs/10-roles-and-responsibilities.md)
- Glossary: [Evidence](../glossary.md), [Population](../glossary.md)
