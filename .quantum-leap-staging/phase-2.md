## INTENT FOR
Patients, assessors, and policy owners who depend on consistent eligibility decisions

## INTENT OUTCOME
Deliver a reliable subsidy application lifecycle with automated eligibility checks and safe fallback paths.

## INTENT MEASURED BY
Applications progress through a standardized state model with clear resolution when checker latency or failure occurs.

## INTENT MUST NOT
Must not allow silent checker failures to produce hidden delays or wrongful auto-rejections.

## PRE-DECIDED
- Lifecycle states are standardized across regions.
- Tokenized verification evidence remains the internal assessor visibility pattern.
- Manual triage is required when external checker retries fail.

## PLAN-MODE QUESTIONS
- [ ] What exact threshold defines insurance coverage-based rejection?
- [ ] Which activity and evidence artifacts are required for compliance audit?
- [ ] What SLA defines checker timeout before manual intervention?

## BUILD-MODE QUESTIONS
- How many retries and backoff intervals should the checker integration use?
- Which queue receives unresolved eligibility checks by default?

## DATA MODEL
Introduce core subsidy application and eligibility tracking fields with auditable status transitions, external check outcomes, and intervention reason codes.

## AUTOMATION
See INT-003 and INT-004. Implement state-machine transitions, checker invocation and retry logic, and manual fallback routing when external services fail or delay.

## UI
Expose clear lifecycle and verification status to patients and assessors, including pending-check guidance and next-step messaging for manual review cases.

## SECURITY
Maintain policy-safe evidence exposure while granting assessors enough context to resolve pending or failed eligibility checks.

## REPORTS
Provide operational views for lifecycle throughput, checker latency/failure trends, and manual fallback volume by region.

## SAMPLE DATA
Use representative applications covering approved, rejected, pending verification, and manual triage outcomes.

## DATA SOURCES
| Source | Use |
| --- | --- |
| subsidy application submissions | lifecycle creation and status tracking |
| health insurance checker API | eligibility decisions and fallback routing |

## ACCEPTANCE USER
- [ ] A patient-submitted application follows the expected lifecycle transitions.
- [ ] An assessor can resolve a checker-failure case through manual triage without policy breach.

## ACCEPTANCE METADATA
- [ ] Lifecycle status transitions are auditable and timestamped.
- [ ] Integration retries and fallback queue routing are verifiable in logs and records.
