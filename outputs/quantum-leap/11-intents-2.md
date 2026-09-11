# Intent Statements — Phase 2 (PTSFLab)

> Reference role: the **load-bearing build target** for Phase 2. Each intent below is one capability — one firing trigger or user action, one outcome, one walkthrough. Build one at a time. The phase brief (`10-phase-2.md`) is orchestration; this file is what to build.
>
> **For architects:** walk these with the customer to assign priority and answer open questions. Edit `data/intents.json` (canonical) or this file directly — the next quantum-leap run re-renders from JSON.

## INT-003 — Subsidy application orchestration and state machine

epic `E02` · priority _(unassigned)_ · confidence _Confirmed_ · surface `automation`

### 1. Outcome

Applications move through a consistent, auditable lifecycle across regions.

### 2. Build target

- Create subsidy application object model and lifecycle statuses
- Implement submission, review, pending-verification, approved, rejected, and closed transitions
- Apply regional state standardization and timestamped audit trail for each transition
- Surface current lifecycle state to patients and internal assessors

### 3. Guardrails

- Must not allow untracked status changes outside the lifecycle engine.
- Must not bypass required verification checks before approval.

### 4. Out of scope

- Must not add practitioner assignment rules in this intent (handled by INT-005).

### 5. Acceptance

An application submitted by a patient moves from Submitted to Pending Verification to Approved or Rejected with a visible and auditable history for each transition.

### Open questions

_(no open questions captured)_

---

## INT-004 — Eligibility checker integration with resilient fallback

epic `E02` · priority _(unassigned)_ · confidence _Assumed_ · surface `integration`

### 1. Outcome

Eligibility checks are automated when available and safely recover when the external checker is slow or unavailable.

### 2. Build target

- Integrate subsidy application flow with health insurance eligibility checker endpoint
- Handle slow response path with pending status and asynchronous retry
- Route unresolved checks to manual assessor queue with reason codes
- Record checker response outcome for compliance and reporting

### 3. Guardrails

- Must not auto-reject when checker response is missing or timed out.
- Must not expose raw external payload fields directly to end users.

### 4. Out of scope

- Must not redesign third-party checker SLA commitments (external owner).

### 5. Acceptance

A delayed checker response places the application in Pending Verification and later resumes automatically, while assessors can manually intervene when retries fail.

### 6. Dependencies

- **Internal (build first):** INT-003
- **External:** Health Insurance Checker API — Stable endpoint, auth credentials, and timeout/retry guidance _(owner: External insurance IT)_

### Open questions

_(no open questions captured)_

