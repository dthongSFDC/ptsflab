# Phase 1 — Identity And Onboarding Foundation (PTSFLab)

> **Phase orchestration — what's in/out of phase, dependencies, starting state.** Read this first to orient. Per-capability buildable specs live in `11-intents-1.md` (when present) — that's what you actually build against, one intent at a time.
> Phase duration: **3 weeks (per user commitment)**.

## Intent

- **For:** Patients and security-conscious operations stakeholders
- **Outcome:** Stand up patient onboarding and launch-safe access controls so subsidy intake can begin on a secure foundation.
- **Measured by:** New patients can complete onboarding end-to-end and internal teams can operate without violating data-visibility policy.
- **Must not:** Must not expose subsidy workflow entry until onboarding and baseline access controls are complete.

## Pre-decided (do not re-litigate)
- Email and password registration is in-scope for launch.
- Social sign-in remains deferred unless policy owners reverse the decision.
- Internal users do not get raw medical-history visibility.

## Plan-mode questions (resolve before switching to Build mode)
- [ ] What fields are mandatory at onboarding vs deferred?
- [ ] Are there region-specific onboarding content or consent differences at launch?
- [ ] What is the exact approval path to revisit social sign-in later?

## Build-mode questions (ask only if the situation arises)
- Which email domain and templates are approved for go-live welcome communication?
- What default failure behavior should happen when onboarding prepopulation services are delayed?

## Epics in scope for this phase

The phase brief is authoritative. Epics below are listed for cross-reference only — when an automation cites `(E04)`, this is what it refers to. For deeper epic narrative, see `90-epics-context.md`.

- **E01: Patient Identity And Onboarding Experience** — Deliver patient-facing registration and authentication with email/password and social sign-in, plus an onboarding wizard that captures profile, language, and insurance details. Include address validation, onboarding completion gating, and multilingual welcome communications to establish a complete patient profile before subsidy requests.
- **E05: Migration, Security, And Regional Operating Model** — Plan and deliver migration of patients, subsidy applications, and assessments while enforcing data-access constraints around sensitive medical history. Integrate internal identity with regional Active Directory patterns and define transition controls for in-flight applications that remain in legacy processing.

## Build targets — orchestration summary

These sections orient the build agent on the shape of the phase. Per-capability buildable detail (Outcome, Build target, Guardrails, Out of scope, Acceptance, Open questions) lives in `11-intents-1.md` per intent. When a section below cites `INT-NNN`, look up the intent there.

### Data model
Create patient onboarding entities and fields needed for profile completion, insurance attributes, and readiness gating. Keep the model minimal and extensible to reduce migration friction later.

### Automation
See INT-001 and INT-002. Automate onboarding completion checks and role-safe access defaults so downstream lifecycle processing starts from a validated patient profile.

### UI & navigation
Implement the onboarding flow and registration experience with clear completion states and explicit next-step messaging once the patient is ready to start a subsidy request.

### Security & access
Define permission sets for patient and internal assessor personas, enforce least-privilege defaults, and preserve strict boundaries around sensitive medical-history details.

### Reports & dashboards
Create onboarding completion and exception reports so operations can identify stuck registrations and policy-related access issues early.

### Sample data
Seed a small patient cohort with varied onboarding completeness to verify gate behavior and security boundaries.

### Data sources

| Source | Use |
| --- | --- |
| patient registration input | account and profile creation |
| insurance prepopulation service | onboarding enrichment and validation |

## Acceptance — user-outcome checks (phase-level)

Phase-level user-outcome claims a stakeholder would walk through to feel "Phase 1 is done." Run them in conversation with the user; mark `- [x]` only when the user agrees. Per-intent acceptance walkthroughs live in `11-intents-1.md`.

- [ ] A patient completes registration and reaches a confirmed onboarding-complete state.
- [ ] An internal assessor can see eligibility evidence status without viewing restricted clinical details.

## Acceptance — metadata-shaped checks (phase-level)

Phase-level metadata-shaped checks — queries the build agent runs against the target org without human help. Run via the Metadata skill (describe / tooling / SOQL). Per-intent acceptance is in `11-intents-1.md`.

- [ ] Permission sets for core personas are created and assigned in test users.
- [ ] Onboarding gate prevents subsidy entry for incomplete profiles.

## Out of scope for Phase 1

If you find yourself needing to build any of these, stop and surface it — it belongs to a later phase or is explicitly excluded.

_(none surfaced in gaps.json — confirm with user during plan-mode review)_

## Dependencies and risks

**Dependencies:** None

**Risks:** Identity-policy drift or unresolved onboarding edge cases can cascade into downstream lifecycle and migration scope.

## Story citations covered in this phase

_(no user-story backlog captured for this phase)_

## Recipe boundary

When this phase is accepted, ask the user: *"Save this run as a recipe so we can repeat for Phase 2?"* The recipe should capture: the data-model decisions made above, the naming patterns confirmed in `03-glossary-and-naming.md`, and any Build-mode question resolutions that emerged.
