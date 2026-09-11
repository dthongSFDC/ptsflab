## INTENT FOR
Cutover, security, and hypercare teams responsible for go-live stability

## INTENT OUTCOME
Complete migration and stabilization with reconciled data, hardened access controls, and controlled transition to steady state.

## INTENT MEASURED BY
Cutover completes with reconciliation evidence, high-priority defects are triaged quickly, and access controls pass post-cutover checks.

## INTENT MUST NOT
Must not complete cutover without explicit reconciliation checkpoints and security verification.

## PRE-DECIDED
- In-flight legacy applications require controlled transition handling.
- Final access posture must preserve time-bound practitioner visibility controls.
- Hypercare is mandatory for defect stabilization immediately after cutover.

## PLAN-MODE QUESTIONS
- [ ] What exact freeze window and rollback thresholds apply for final migration?
- [ ] Which reconciliation tolerances are acceptable before go-live sign-off?
- [ ] Who approves security exceptions discovered during hypercare?

## BUILD-MODE QUESTIONS
- Which defects are P1 and must block business-as-usual handoff?
- What trigger ends hypercare and transitions to operations support?

## DATA MODEL
No broad new model expected. Focus is migration completeness markers, reconciliation evidence fields, and cutover control records.

## AUTOMATION
See INT-008. Execute migration control automation, exception routing, and post-cutover access revocation checks to ensure stable and compliant operations.

## UI
Provide operational cutover and hypercare views for defect triage, exception ownership, and readiness-to-close tracking.

## SECURITY
Run final access-hardening checks and remove temporary elevated permissions used during migration activities.

## REPORTS
Deliver cutover reconciliation and hypercare status reports showing exceptions, defect aging, and closure readiness.

## SAMPLE DATA
Use migrated and preexisting sample cohorts to validate reconciliation and access behavior after cutover.

## DATA SOURCES
| Source | Use |
| --- | --- |
| legacy export package | final migration and reconciliation |
| production readiness checklist | cutover and hypercare acceptance evidence |

## ACCEPTANCE USER
- [ ] Delivery lead can confirm reconciled migration outcomes and approve stabilization completion.
- [ ] Security owner can verify final access posture and sign off on go-live controls.

## ACCEPTANCE METADATA
- [ ] Reconciliation report exists with exception counts and dispositions.
- [ ] Temporary migration-era elevated access has been revoked and verified.
