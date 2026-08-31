# Delivery Plan

Total program duration: 12 weeks (per user commitment).

Critical path: E01 -> E02 -> E03 -> E04 — these gate the schedule; slippage on any one cascades.

Because `data/estimates.json` is not present yet, this roadmap uses requirement complexity and dependency risk from `epics.json` and `gaps.json` for sequencing.

## Phase 0 - Discovery Resolution And Delivery Readiness (2 weeks)

- Sequence position: 1 of 5
- Objective: Close high-impact assumptions and source conflicts before the main build.
- Epics included: None (cross-cutting readiness phase)
- Dependencies: Inputs from discovery and requirements baseline
- Success criteria: Identity policy, residency rules, and collaboration-channel decisions have named owners and concrete outcomes.
- Key risks: Governance or policy decisions stall and delay downstream implementation.

## Phase 1 - Identity And Onboarding Foundation (3 weeks)

- Sequence position: 2 of 5
- Objective: Launch the patient identity and onboarding foundation.
- Epics included: E01, E05 (foundation controls)
- Dependencies: None
- Success criteria: Patients can register, authenticate, and complete onboarding; baseline migration/security controls are in place.
- Key risks: Identity-policy changes and onboarding edge cases ripple into later lifecycle work.

## Phase 2 - Application Lifecycle And Eligibility Automation (3 weeks)

- Sequence position: 3 of 5
- Objective: Deliver subsidy application lifecycle and eligibility automation.
- Epics included: E02, E05 (continued security/migration controls)
- Dependencies: depends on E01
- Success criteria: Lifecycle states are standardized and eligibility decisions are auditable across regions.
- Key risks: Insurance-check latency and unresolved verification evidence model increase manual work.

## Phase 3 - Operations, Assignment, And Collaboration (3 weeks)

- Sequence position: 4 of 5
- Objective: Complete practitioner assignment, assessor operations, and collaboration support.
- Epics included: E03, E04
- Dependencies: depends on E02
- Success criteria: Assignment and reassignment logic, escalation pathways, and assessor routing are working end to end.
- Key risks: Geospatial assignment and chat architecture assumptions may require design refactoring.

## Phase 4 - Cutover, Stabilization, And Hypercare (1 week)

- Sequence position: 5 of 5
- Objective: Execute cutover and stabilize operations.
- Epics included: E05 (cutover hardening and controls)
- Dependencies: depends on E03, E04, E05
- Success criteria: Data reconciliation, access controls, and high-priority stabilization actions are complete.
- Key risks: Late migration defects or unresolved policy items extend hypercare.

## Standard Processes Across All Build Phases

- Testing and quality gates: Integration, regression, and release-readiness checks run continuously across Phases 1-4.
- Deployment controls: Environment promotions, release governance, and rollback planning are executed per phase.
- Training and enablement: Assessor/practitioner enablement and support playbooks are iterated before each phase release.

## Consolidated Risk Table

| Risk | Where It Bites | Mitigation Focus |
| --- | --- | --- |
| Identity and social sign-in policy drift | Phases 0-2 | Lock decision owners and acceptance criteria in Phase 0. |
| Medical-history visibility contradiction | Phases 0-2 | Confirm tokenized verification evidence and controls before build deepens. |
| Geospatial assignment design uncertainty | Phase 3 | Confirm matching architecture and fallback behavior during Phase 0/1. |
| Collaboration channel architecture ambiguity | Phase 3 | Decide channel pattern and routing model before assessor workflow finalization. |
| Regional residency and federation constraints | Phases 0-4 | Confirm policy boundaries and enforce in migration/cutover design. |

The disciplines and named roster to deliver this — with defensible counts, per lane — come from `estimate`.
