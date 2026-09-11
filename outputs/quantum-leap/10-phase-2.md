# Phase 2 — Application Lifecycle And Eligibility Automation (PTSFLab)

> **Phase orchestration — what's in/out of phase, dependencies, starting state.** Read this first to orient. Per-capability buildable specs live in `11-intents-2.md` (when present) — that's what you actually build against, one intent at a time.
> Phase duration: **3 weeks (per user commitment)**.

## Intent

- **For:** Patients, assessors, and policy owners who depend on consistent eligibility decisions
- **Outcome:** Deliver a reliable subsidy application lifecycle with automated eligibility checks and safe fallback paths.
- **Measured by:** Applications progress through a standardized state model with clear resolution when checker latency or failure occurs.
- **Must not:** Must not allow silent checker failures to produce hidden delays or wrongful auto-rejections.

## Pre-decided (do not re-litigate)
- Lifecycle states are standardized across regions.
- Tokenized verification evidence remains the internal assessor visibility pattern.
- Manual triage is required when external checker retries fail.

## Starting state (from Identity And Onboarding Foundation)

You should find these already deployed in the sandbox:
- **Identity And Onboarding Foundation outcome:** Patients can register and complete onboarding; baseline controls for regional security and migration planning are implemented and testable.

## Plan-mode questions (resolve before switching to Build mode)
- [ ] What exact threshold defines insurance coverage-based rejection?
- [ ] Which activity and evidence artifacts are required for compliance audit?
- [ ] What SLA defines checker timeout before manual intervention?

## Build-mode questions (ask only if the situation arises)
- How many retries and backoff intervals should the checker integration use?
- Which queue receives unresolved eligibility checks by default?

## Epics in scope for this phase

The phase brief is authoritative. Epics below are listed for cross-reference only — when an automation cites `(E04)`, this is what it refers to. For deeper epic narrative, see `90-epics-context.md`.

- **E02: Subsidy Application Lifecycle And Eligibility Decisions** — Implement end-to-end subsidy application capture for treatment type, reason, and medical history verification. Orchestrate health insurance entitlement checks with automated rejection logic where coverage exists and standardize application states across regions.
- **E05: Migration, Security, And Regional Operating Model** — Plan and deliver migration of patients, subsidy applications, and assessments while enforcing data-access constraints around sensitive medical history. Integrate internal identity with regional Active Directory patterns and define transition controls for in-flight applications that remain in legacy processing.

## Build targets — orchestration summary

These sections orient the build agent on the shape of the phase. Per-capability buildable detail (Outcome, Build target, Guardrails, Out of scope, Acceptance, Open questions) lives in `11-intents-2.md` per intent. When a section below cites `INT-NNN`, look up the intent there.

### Data model
Introduce core subsidy application and eligibility tracking fields with auditable status transitions, external check outcomes, and intervention reason codes.

### Automation
See INT-003 and INT-004. Implement state-machine transitions, checker invocation and retry logic, and manual fallback routing when external services fail or delay.

### UI & navigation
Expose clear lifecycle and verification status to patients and assessors, including pending-check guidance and next-step messaging for manual review cases.

### Security & access
Maintain policy-safe evidence exposure while granting assessors enough context to resolve pending or failed eligibility checks.

### Reports & dashboards
Provide operational views for lifecycle throughput, checker latency/failure trends, and manual fallback volume by region.

### Sample data
Use representative applications covering approved, rejected, pending verification, and manual triage outcomes.

### Data sources

| Source | Use |
| --- | --- |
| subsidy application submissions | lifecycle creation and status tracking |
| health insurance checker API | eligibility decisions and fallback routing |

## Acceptance — user-outcome checks (phase-level)

Phase-level user-outcome claims a stakeholder would walk through to feel "Phase 2 is done." Run them in conversation with the user; mark `- [x]` only when the user agrees. Per-intent acceptance walkthroughs live in `11-intents-2.md`.

- [ ] A patient-submitted application follows the expected lifecycle transitions.
- [ ] An assessor can resolve a checker-failure case through manual triage without policy breach.

## Acceptance — metadata-shaped checks (phase-level)

Phase-level metadata-shaped checks — queries the build agent runs against the target org without human help. Run via the Metadata skill (describe / tooling / SOQL). Per-intent acceptance is in `11-intents-2.md`.

- [ ] Lifecycle status transitions are auditable and timestamped.
- [ ] Integration retries and fallback queue routing are verifiable in logs and records.

## Out of scope for Phase 2

If you find yourself needing to build any of these, stop and surface it — it belongs to a later phase or is explicitly excluded.

_(none surfaced in gaps.json — confirm with user during plan-mode review)_

## Dependencies and risks

**Dependencies:** depends on: E01

**Risks:** External checker latency and unresolved verification evidence model can reduce automation quality and increase manual triage.

## Story citations covered in this phase

_(no user-story backlog captured for this phase)_

## Recipe boundary

When this phase is accepted, ask the user: *"Save this run as a recipe so we can repeat for Phase 3?"* The recipe should capture: the data-model decisions made above, the naming patterns confirmed in `03-glossary-and-naming.md`, and any Build-mode question resolutions that emerged.
