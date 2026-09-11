# Epics — Context Only — PTSFLab

> Reference role: **background**, not load-bearing. The phase briefs are authoritative. This file dereferences epic IDs cited in phase briefs (e.g. `(E01)`) and provides scoping-stage context for trade-off reasoning.
>
> Do not plan against epics. Plan against `10-phase-N.md`.

## E01: Patient Identity And Onboarding Experience
Deliver patient-facing registration and authentication with email/password and social sign-in, plus an onboarding wizard that captures profile, language, and insurance details. Include address validation, onboarding completion gating, and multilingual welcome communications to establish a complete patient profile before subsidy requests.

_Confidence: Confirmed_
**KB sources:** [KB:experience_cloud_4-2-2026.md:2153-2324], [KB:experience_cloud_4-2-2026.md:13346-13549]

## E02: Subsidy Application Lifecycle And Eligibility Decisions
Implement end-to-end subsidy application capture for treatment type, reason, and medical history verification. Orchestrate health insurance entitlement checks with automated rejection logic where coverage exists and standardize application states across regions.

_Confidence: Confirmed_
**KB sources:** [KB:sales_einstein_implementation_guide.md:28-77], [extends: workflow-driven case/application lifecycle using standard platform automation patterns]

## E03: Practitioner Assignment And Assessment Operations
Automate practitioner assignment by treatment type and nearest-practice criteria, with SLA-driven acceptance tracking, reassignment logic, and escalation for overdue assessments. Support multi-practitioner and specialist assessment flows where additional expertise is required.

_Confidence: Assumed_
**KB sources:** [KB:service_cloud_3-27-2026.md:1-18775], [assumption: confirm geospatial matching and reassignment strategy in solution design]

## E04: Assessor Work Management And Collaboration Support
Provide internal assessor workflows for application handling, subsidy review support, and manager escalation visibility. Enable patient and practitioner collaboration with assessor teams through digital support channels and support-request deflection for common questions.

_Confidence: Assumed_
**KB sources:** [KB:experience_cloud_4-2-2026.md:23656-23687], [KB:experience_cloud_4-2-2026.md:23793-23812], [assumption: confirm channel architecture for external chat and internal routing]

## E05: Migration, Security, And Regional Operating Model
Plan and deliver migration of patients, subsidy applications, and assessments while enforcing data-access constraints around sensitive medical history. Integrate internal identity with regional Active Directory patterns and define transition controls for in-flight applications that remain in legacy processing.

_Confidence: Confirmed_
**KB sources:** [KB:service_cloud_3-27-2026.md:1-18775], [KB:experience_cloud_4-2-2026.md:13864-13980]

---

## Estimates and complexity drivers

These T-shirt sizes are scoping-stage planning estimates. They are **not** build instructions — the build agent should plan against the per-phase briefs, not against epic size. Sizes are included here for context only.

_(no estimates captured — run the `design` skill to populate `estimates.json`)_
