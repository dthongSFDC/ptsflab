## INTENT FOR
Patients and security-conscious operations stakeholders

## INTENT OUTCOME
Stand up patient onboarding and launch-safe access controls so subsidy intake can begin on a secure foundation.

## INTENT MEASURED BY
New patients can complete onboarding end-to-end and internal teams can operate without violating data-visibility policy.

## INTENT MUST NOT
Must not expose subsidy workflow entry until onboarding and baseline access controls are complete.

## PRE-DECIDED
- Email and password registration is in-scope for launch.
- Social sign-in remains deferred unless policy owners reverse the decision.
- Internal users do not get raw medical-history visibility.

## PLAN-MODE QUESTIONS
- [ ] What fields are mandatory at onboarding vs deferred?
- [ ] Are there region-specific onboarding content or consent differences at launch?
- [ ] What is the exact approval path to revisit social sign-in later?

## BUILD-MODE QUESTIONS
- Which email domain and templates are approved for go-live welcome communication?
- What default failure behavior should happen when onboarding prepopulation services are delayed?

## DATA MODEL
Create patient onboarding entities and fields needed for profile completion, insurance attributes, and readiness gating. Keep the model minimal and extensible to reduce migration friction later.

## AUTOMATION
See INT-001 and INT-002. Automate onboarding completion checks and role-safe access defaults so downstream lifecycle processing starts from a validated patient profile.

## UI
Implement the onboarding flow and registration experience with clear completion states and explicit next-step messaging once the patient is ready to start a subsidy request.

## SECURITY
Define permission sets for patient and internal assessor personas, enforce least-privilege defaults, and preserve strict boundaries around sensitive medical-history details.

## REPORTS
Create onboarding completion and exception reports so operations can identify stuck registrations and policy-related access issues early.

## SAMPLE DATA
Seed a small patient cohort with varied onboarding completeness to verify gate behavior and security boundaries.

## DATA SOURCES
| Source | Use |
| --- | --- |
| patient registration input | account and profile creation |
| insurance prepopulation service | onboarding enrichment and validation |

## ACCEPTANCE USER
- [ ] A patient completes registration and reaches a confirmed onboarding-complete state.
- [ ] An internal assessor can see eligibility evidence status without viewing restricted clinical details.

## ACCEPTANCE METADATA
- [ ] Permission sets for core personas are created and assigned in test users.
- [ ] Onboarding gate prevents subsidy entry for incomplete profiles.
