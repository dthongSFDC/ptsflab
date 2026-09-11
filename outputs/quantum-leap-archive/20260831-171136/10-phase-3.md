# Phase 3 — Operations, Assignment, And Collaboration (PTSFLab)

> **Phase orchestration — what's in/out of phase, dependencies, starting state.** Read this first to orient. Per-capability buildable specs live in `11-intents-3.md` (when present) — that's what you actually build against, one intent at a time.
> Phase duration: **3 weeks (per user commitment)**.

## Intent

- **For:** Practitioners, assessors, and operations managers running daily assessment operations
- **Outcome:** Operationalize assignment, collaboration, and escalation workflows so assessments move quickly with clear ownership.
- **Measured by:** Assignment and support interactions route correctly, SLA breaches are visible, and managers can act on escalation signals.
- **Must not:** Must not allow collaboration channels or reassignment flows to bypass traceable work records.

## Pre-decided (do not re-litigate)
- Assignment depends on treatment eligibility and proximity input.
- Collaboration routing must bind to formal work records.
- Regional visibility and escalation reporting are required, not optional.

## Starting state (from Application Lifecycle And Eligibility Automation)

You should find these already deployed in the sandbox:
- **Application Lifecycle And Eligibility Automation outcome:** Eligibility flow handles core pathways with auditable decisions; lifecycle states are consistent across regions; migration/security controls are integrated into lifecycle processing.

## Plan-mode questions (resolve before switching to Build mode)
- [ ] What deterministic geospatial method and tie-break order governs assignment?
- [ ] Which channel architecture is final for external collaboration intake?
- [ ] What region-specific operating-hour and language constraints apply to support routing?

## Build-mode questions (ask only if the situation arises)
- How should unresolved reassignment attempts terminate when no suitable practitioner is found?
- What thresholds trigger manager escalation for collaboration backlog?

## Epics in scope for this phase

The phase brief is authoritative. Epics below are listed for cross-reference only — when an automation cites `(E04)`, this is what it refers to. For deeper epic narrative, see `90-epics-context.md`.

- **E03: Practitioner Assignment And Assessment Operations** — Automate practitioner assignment by treatment type and nearest-practice criteria, with SLA-driven acceptance tracking, reassignment logic, and escalation for overdue assessments. Support multi-practitioner and specialist assessment flows where additional expertise is required.
- **E04: Assessor Work Management And Collaboration Support** — Provide internal assessor workflows for application handling, subsidy review support, and manager escalation visibility. Enable patient and practitioner collaboration with assessor teams through digital support channels and support-request deflection for common questions.

## Build targets — orchestration summary

These sections orient the build agent on the shape of the phase. Per-capability buildable detail (Outcome, Build target, Guardrails, Out of scope, Acceptance, Open questions) lives in `11-intents-3.md` per intent. When a section below cites `INT-NNN`, look up the intent there.

### Data model
Add assignment, reassignment, escalation, and collaboration tracking fields that preserve ownership history and support regional operations reporting.

### Automation
See INT-005 and INT-006. Implement practitioner assignment logic, reassignment and escalation automation, and collaboration routing into assessor queues with traceable handoffs.

### UI & navigation
Provide assessor and manager workspaces for queue handling, escalation action, and collaboration context linked directly to the underlying application records.

### Security & access
Enforce role-based access and transcript visibility limits so collaboration data is usable for operations without exposing restricted sensitive details.

### Reports & dashboards
See INT-007. Deliver manager dashboards for overdue assessments, reassignment churn, collaboration backlog, and regional SLA performance.

### Sample data
Load scenarios with multi-practitioner paths, declined assignments, overdue escalations, and multilingual support interactions.

### Data sources

| Source | Use |
| --- | --- |
| practitioner directory and treatment mapping | assignment and reassignment logic |
| collaboration channel events | queue routing and transcript-linked operations |

## Acceptance — user-outcome checks (phase-level)

Phase-level user-outcome claims a stakeholder would walk through to feel "Phase 3 is done." Run them in conversation with the user; mark `- [x]` only when the user agrees. Per-intent acceptance walkthroughs live in `11-intents-3.md`.

- [ ] An eligible case is assigned, reassigned when required, and escalated when SLA conditions are met.
- [ ] An assessor can process a collaboration request tied to the correct application record.

## Acceptance — metadata-shaped checks (phase-level)

Phase-level metadata-shaped checks — queries the build agent runs against the target org without human help. Run via the Metadata skill (describe / tooling / SOQL). Per-intent acceptance is in `11-intents-3.md`.

- [ ] Assignment and escalation automations run deterministically under test scenarios.
- [ ] Manager dashboard surfaces overdue and escalated records with current ownership.

## Out of scope for Phase 3

If you find yourself needing to build any of these, stop and surface it — it belongs to a later phase or is explicitly excluded.

_(none surfaced in gaps.json — confirm with user during plan-mode review)_

## Dependencies and risks

**Dependencies:** depends on: E02

**Risks:** Unconfirmed geospatial-matching approach and channel architecture can force late design changes.

## Story citations covered in this phase

_(no user-story backlog captured for this phase)_

## Recipe boundary

When this phase is accepted, ask the user: *"Save this run as a recipe so we can repeat for Phase 4?"* The recipe should capture: the data-model decisions made above, the naming patterns confirmed in `03-glossary-and-naming.md`, and any Build-mode question resolutions that emerged.
