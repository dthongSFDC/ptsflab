# Phase 0 — Discovery Resolution And Delivery Readiness (PTSFLab)

> **Phase orchestration — what's in/out of phase, dependencies, starting state.** Read this first to orient. Per-capability buildable specs live in `11-intents-0.md` (when present) — that's what you actually build against, one intent at a time.
> Phase duration: **2 weeks (per user commitment)**.

## Intent

- **For:** Delivery leadership and architecture governance team
- **Outcome:** Resolve policy and dependency decisions that would otherwise block implementation throughput in later phases.
- **Measured by:** All load-bearing open questions have a named owner, decision date, and accepted default.
- **Must not:** Must not start feature build work before policy-critical assumptions are explicitly accepted.

## Pre-decided (do not re-litigate)
- Use a formal readiness phase because 41 open gaps exceed the threshold for safe accelerated delivery.
- Keep social sign-in deferred unless policy owners explicitly approve it.
- Keep tokenized eligibility evidence as the interim pattern for internal assessors.

## Plan-mode questions (resolve before switching to Build mode)
- [ ] Confirm final identity policy for patient login options by launch and by post-launch phase.
- [ ] Confirm regional data residency constraints for APAC, EMEA, and AMER with security owners.
- [ ] Confirm channel architecture for external collaboration and internal assessor routing.

## Build-mode questions (ask only if the situation arises)
- Finalized assumptions package approved?
- Named owners for every unresolved gap assigned?

## Epics in scope for this phase

The phase brief is authoritative. Epics below are listed for cross-reference only — when an automation cites `(E04)`, this is what it refers to. For deeper epic narrative, see `90-epics-context.md`.

_(no epics tied to this phase)_

## Build targets — orchestration summary

These sections orient the build agent on the shape of the phase. Per-capability buildable detail (Outcome, Build target, Guardrails, Out of scope, Acceptance, Open questions) lives in `11-intents-0.md` per intent. When a section below cites `INT-NNN`, look up the intent there.

### Data model
No net-new production data model is expected in this phase. Focus is metadata for decision tracking and a documented assumptions register that later phases consume.

### Automation
No customer-facing automation is built in this phase. The only automation expected is internal tracking for decision readiness and escalation of unresolved blockers.

### UI & navigation
No end-user interface delivery in this phase. Any workspace views are internal-only for readiness governance.

### Security & access
Define baseline security constraints that later phases must follow, especially around clinical-data visibility and region-specific access boundaries.

### Reports & dashboards
Produce a readiness dashboard showing blocker count, owner assignment coverage, and decision closure status by phase dependency.

### Sample data
Use anonymized sample records only if needed to validate decision-tracking flows.

### Data sources

| Source | Use |
| --- | --- |
| discovery-notes and gaps baseline | decision and blocker traceability |

## Acceptance — user-outcome checks (phase-level)

Phase-level user-outcome claims a stakeholder would walk through to feel "Phase 0 is done." Run them in conversation with the user; mark `- [x]` only when the user agrees. Per-intent acceptance walkthroughs live in `11-intents-0.md`.

- [ ] Solution Architect can show that every blocker has an owner and next action.
- [ ] Delivery lead can approve transition to Phase 1 with no unresolved hard blockers.

## Acceptance — metadata-shaped checks (phase-level)

Phase-level metadata-shaped checks — queries the build agent runs against the target org without human help. Run via the Metadata skill (describe / tooling / SOQL). Per-intent acceptance is in `11-intents-0.md`.

- [ ] Assumption register exists and links to impacted epics.
- [ ] Readiness report is generated and reviewable.

## Out of scope for Phase 0

If you find yourself needing to build any of these, stop and surface it — it belongs to a later phase or is explicitly excluded.

_(none surfaced in gaps.json — confirm with user during plan-mode review)_

## Dependencies and risks

**Dependencies:** Inputs from discovery and requirements baseline

**Risks:** Decision latency on policy-heavy questions can delay start of build phases.

## Story citations covered in this phase

_(no user-story backlog captured for this phase)_

## Recipe boundary

When this phase is accepted, ask the user: *"Save this run as a recipe so we can repeat for Phase 1?"* The recipe should capture: the data-model decisions made above, the naming patterns confirmed in `03-glossary-and-naming.md`, and any Build-mode question resolutions that emerged.
