# Template: Risk-Control Matrix (RCM)

> **What this is:** The master table that maps each **risk** to the **control** that addresses it, and records how the control works and how it's tested. It's the single most useful artifact in an ITGC program. See [chapter 09](../docs/09-how-controls-are-tested.md) for the concepts.

## How to use it

1. List each meaningful IT risk (one per row).
2. Describe the control that addresses it.
3. Tag the **domain** (Access / Change / SDLC / Operations), the **type** (Preventive or Detective), and the **frequency**.
4. Name the **control owner** and describe the **test procedure** and the **evidence** you'd collect.
5. Keep it current — an out-of-date RCM is worse than none.

Copy the table below and replace the example rows with your own.

## The matrix

| ID | Risk | Control description | Domain | Type (P/D) | Frequency | Control owner | Test procedure | Evidence |
|----|------|---------------------|--------|-----------|-----------|---------------|----------------|----------|
| AC-01 | Terminated users retain access and could misuse it. | Access is removed within 1 business day of termination, triggered by the HR feed. | Access | Preventive | Continuous / per event | IAM Lead | Select a sample of terminations; confirm access removed within SLA. | HR termination record + system access-removal log with timestamps. |
| AC-02 | Inappropriate access accumulates over time. | Quarterly user access review; managers certify or revoke each user's access. | Access | Detective | Quarterly | System Owner | Inspect the completed review for the period; confirm revocations were actioned. | Signed, dated access-review report + revocation tickets. |
| AC-03 | A single user can perform conflicting duties (SoD conflict). | Access is role-based (RBAC); conflicting roles are blocked and reviewed. | Access | Preventive | Continuous | IAM Lead | Review role-to-permission mapping; test that a conflicting combination is prevented. | RBAC configuration + SoD conflict report. |
| CM-01 | An unapproved or untested change reaches production. | Changes require documented approval and test evidence before deployment. | Change | Preventive | Per change | Release Manager | Sample production changes; verify approval + test evidence exist prior to deploy. | Change tickets with approvals and test results. |
| CM-02 | A developer deploys their own code without independent review. | Deployment to production is performed by someone other than the developer. | Change | Preventive | Per change | Release Manager | Sample changes; compare author vs deployer in the pipeline logs. | Deployment log showing author ≠ deployer. |
| OP-01 | A failed batch job means transactions aren't processed. | Critical jobs are monitored; failures raise an alert and a ticket that must be resolved. | Operations | Detective | Daily | Operations Lead | Sample job-failure alerts; confirm each was investigated and resolved. | Job monitoring log + incident tickets. |
| OP-02 | Data loss from a system failure. | Backups run nightly and a test restore is performed periodically. | Operations | Detective | Nightly / quarterly test | Operations Lead | Confirm backup schedule ran; inspect a documented test-restore result. | Backup logs + test-restore report. |
| SD-01 | A new system goes live before it's ready. | Formal go-live approval confirms testing, data migration, and readiness. | SDLC | Preventive | Per implementation | Project Sponsor | For systems implemented in period, inspect go-live sign-off and test/migration evidence. | Go/no-go approval + UAT sign-off + migration reconciliation. |

*P = Preventive (stops the problem), D = Detective (catches it after). Add columns for "Deficiency noted" and "Remediation status" when you use this for a real assessment.*

## Related

- Concept: [09 — How controls are tested](../docs/09-how-controls-are-tested.md)
- Domains: [04 — The four domains](../docs/04-the-four-domains.md)
- Glossary: [RCM](../glossary.md), [Preventive control](../glossary.md), [Detective control](../glossary.md)
