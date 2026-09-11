# Intent Statements — Phase 4 (PTSFLab)

> Reference role: the **load-bearing build target** for Phase 4. Each intent below is one capability — one firing trigger or user action, one outcome, one walkthrough. Build one at a time. The phase brief (`10-phase-4.md`) is orchestration; this file is what to build.
>
> **For architects:** walk these with the customer to assign priority and answer open questions. Edit `data/intents.json` (canonical) or this file directly — the next quantum-leap run re-renders from JSON.

## INT-008 — Migration cutover and security hardening

epic `E05` · priority _(unassigned)_ · confidence _Assumed_ · surface `devops`

### 1. Outcome

Cutover from legacy processing is controlled, reconciled, and secure for steady-state operations.

### 2. Build target

- Execute final migration load for in-scope patients, applications, and assessments
- Reconcile migrated records and flag exceptions for manual remediation
- Enforce final access controls and revocation rules for practitioner time-bound visibility
- Run hypercare triage workflow for high-priority defects

### 3. Guardrails

- Must not migrate records without reconciliation checkpoints.
- Must not leave temporary elevated access permissions active after cutover.

### 4. Out of scope

- Must not redesign upstream legacy-system data quality processes.

### 5. Acceptance

Cutover completes with reconciled record counts, unresolved exceptions tracked, and security controls validated before business-as-usual handoff.

### 6. Dependencies

- **Internal (build first):** INT-003, INT-005, INT-006
- **External:** Legacy platform — Final export and in-flight application freeze window _(owner: Legacy platform team)_

### Open questions

_(no open questions captured)_

