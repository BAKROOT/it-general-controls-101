# Template: Change Request Form

> **What this is:** A fill-in form that captures a change to an existing system through the controlled flow: request → approval → test → deploy, with the developer and deployer kept separate. See [chapter 06](../docs/06-change-management.md) and the [worked example](../examples/walkthrough-change-ticket.md).

Copy this per change. The completed form (with its approvals and test evidence) *is* the audit evidence.

## 1. Request details

- **Change ID / ticket #:** _______________________
- **Title:** _______________________
- **Requested by:** ____________  **Date requested:** __________
- **System / application affected:** _______________________
- **Change type:** [ ] Standard  [ ] Normal  [ ] Emergency
- **Priority:** [ ] Low  [ ] Medium  [ ] High  [ ] Critical
- **Description of the change (what and why):**
  _______________________________________________
- **Business justification:**
  _______________________________________________
- **Risk / impact if we make it (and if we don't):**
  _______________________________________________
- **Rollback plan (how to undo it if it fails):**
  _______________________________________________

## 2. Approval (before work starts)

- **Approver name / role:** _______________________
- **Approval decision:** [ ] Approved  [ ] Rejected  [ ] More info needed
- **Approval date:** __________
- **Comments:** _______________________

> The approver must be different from the requester/developer where possible.

## 3. Development

- **Developer:** _______________________
- **Environment built in:** (Dev / non-production) __________
- **Date completed:** __________

## 4. Testing

- **Tested by:** _______________________
- **Test type:** [ ] Functional  [ ] Regression  [ ] User Acceptance Testing (UAT)
- **Test result:** [ ] Pass  [ ] Fail (fix and re-test)
- **Test evidence attached:** [ ] Yes  (screenshots / results / UAT sign-off)
- **Date tested:** __________

## 5. Approval to deploy (go/no-go)

- **Approved to deploy by:** _______________________
- **Decision:** [ ] Go  [ ] No-go
- **Date:** __________

## 6. Deployment to production

- **Deployed by:** _______________________  ← must be **someone other than the developer**
- **Date/time deployed:** __________
- **Post-deployment verification:** [ ] Confirmed working  [ ] Issue (see rollback)
- **Deployment log reference (evidence):** _______________________

## 7. Emergency changes only

- **Reason it could not follow the normal process:** _______________________
- **Retroactive approval obtained by:** ____________  **Date:** __________
- **Post-implementation review completed:** [ ] Yes  **Date:** __________

## Segregation-of-duties check

- [ ] The **developer** (section 3) and the **deployer** (section 6) are **different people**.
- [ ] Approval (section 2) came from someone independent of the developer.

## Related

- Concept: [06 — Change management](../docs/06-change-management.md)
- Example: [Change-ticket walkthrough](../examples/walkthrough-change-ticket.md)
- Glossary: [Change management](../glossary.md), [SoD](../glossary.md), [Emergency change](../glossary.md)
