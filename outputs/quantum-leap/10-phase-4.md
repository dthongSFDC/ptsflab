# Phase 4 — Cutover, Stabilization, And Hypercare (PTSFLab)

> **Phase orchestration — what's in/out of phase, dependencies, starting state.** Read this first to orient. Per-capability buildable specs live in `11-intents-4.md` (when present) — that's what you actually build against, one intent at a time.
> Phase duration: **1 weeks (per user commitment)**.

## Intent

- **For:** Cutover, security, and hypercare teams responsible for go-live stability
- **Outcome:** Complete migration and stabilization with reconciled data, hardened access controls, and controlled transition to steady state.
- **Measured by:** Cutover completes with reconciliation evidence, high-priority defects are triaged quickly, and access controls pass post-cutover checks.
- **Must not:** Must not complete cutover without explicit reconciliation checkpoints and security verification.

## Pre-decided (do not re-litigate)
- In-flight legacy applications require controlled transition handling.
- Final access posture must preserve time-bound practitioner visibility controls.
- Hypercare is mandatory for defect stabilization immediately after cutover.

## Starting state (from Operations, Assignment, And Collaboration)

You should find these already deployed in the sandbox:
- **Operations, Assignment, And Collaboration outcome:** Assignment and escalation flows run against agreed rules; assessor work queues and collaboration channels are operational with traceable routing.

## Plan-mode questions (resolve before switching to Build mode)
- [ ] What exact freeze window and rollback thresholds apply for final migration?
- [ ] Which reconciliation tolerances are acceptable before go-live sign-off?
- [ ] Who approves security exceptions discovered during hypercare?

## Build-mode questions (ask only if the situation arises)
- Which defects are P1 and must block business-as-usual handoff?
- What trigger ends hypercare and transitions to operations support?

## Epics in scope for this phase

The phase brief is authoritative. Epics below are listed for cross-reference only — when an automation cites `(E04)`, this is what it refers to. For deeper epic narrative, see `90-epics-context.md`.

- **E05: Migration, Security, And Regional Operating Model** — Plan and deliver migration of patients, subsidy applications, and assessments while enforcing data-access constraints around sensitive medical history. Integrate internal identity with regional Active Directory patterns and define transition controls for in-flight applications that remain in legacy processing.

## Build targets — orchestration summary

These sections orient the build agent on the shape of the phase. Per-capability buildable detail (Outcome, Build target, Guardrails, Out of scope, Acceptance, Open questions) lives in `11-intents-4.md` per intent. When a section below cites `INT-NNN`, look up the intent there.

### Data model
No broad new model expected. Focus is migration completeness markers, reconciliation evidence fields, and cutover control records.

### Automation
See INT-008. Execute migration control automation, exception routing, and post-cutover access revocation checks to ensure stable and compliant operations.

### UI & navigation
Provide operational cutover and hypercare views for defect triage, exception ownership, and readiness-to-close tracking.

### Security & access
Run final access-hardening checks and remove temporary elevated permissions used during migration activities.

### Reports & dashboards
Deliver cutover reconciliation and hypercare status reports showing exceptions, defect aging, and closure readiness.

### Sample data
Use migrated and preexisting sample cohorts to validate reconciliation and access behavior after cutover.

### Data sources

| Source | Use |
| --- | --- |
| legacy export package | final migration and reconciliation |
| production readiness checklist | cutover and hypercare acceptance evidence |

## Acceptance — user-outcome checks (phase-level)

Phase-level user-outcome claims a stakeholder would walk through to feel "Phase 4 is done." Run them in conversation with the user; mark `- [x]` only when the user agrees. Per-intent acceptance walkthroughs live in `11-intents-4.md`.

- [ ] Delivery lead can confirm reconciled migration outcomes and approve stabilization completion.
- [ ] Security owner can verify final access posture and sign off on go-live controls.

## Acceptance — metadata-shaped checks (phase-level)

Phase-level metadata-shaped checks — queries the build agent runs against the target org without human help. Run via the Metadata skill (describe / tooling / SOQL). Per-intent acceptance is in `11-intents-4.md`.

- [ ] Reconciliation report exists with exception counts and dispositions.
- [ ] Temporary migration-era elevated access has been revoked and verified.

## Out of scope for Phase 4

If you find yourself needing to build any of these, stop and surface it — it belongs to a later phase or is explicitly excluded.

_(none surfaced in gaps.json — confirm with user during plan-mode review)_

## Dependencies and risks

**Dependencies:** depends on: E03,E04,E05

**Risks:** Late discovery of migration data quality issues or unresolved policy items can extend stabilization.

## Story citations covered in this phase

_(no user-story backlog captured for this phase)_

## Recipe boundary

When this phase is accepted, ask the user: *"Save this run as a recipe so we can repeat for Phase —?"* The recipe should capture: the data-model decisions made above, the naming patterns confirmed in `03-glossary-and-naming.md`, and any Build-mode question resolutions that emerged.
