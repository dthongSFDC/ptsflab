# Intent Statements — Phase 1 (PTSFLab)

> Reference role: the **load-bearing build target** for Phase 1. Each intent below is one capability — one firing trigger or user action, one outcome, one walkthrough. Build one at a time. The phase brief (`10-phase-1.md`) is orchestration; this file is what to build.
>
> **For architects:** walk these with the customer to assign priority and answer open questions. Edit `data/intents.json` (canonical) or this file directly — the next quantum-leap run re-renders from JSON.

## INT-001 — Patient account registration and profile gate

epic `E01` · priority _(unassigned)_ · confidence _Confirmed_ · surface `experience-cloud`

### 1. Outcome

Patients can create an account, verify identity, and reach a complete profile before starting subsidy requests.

### 2. Build target

- Create Experience Cloud registration and login flow with email and password
- Capture required onboarding fields: language, insurance details, and contact profile
- Enforce profile-complete gate before subsidy application entry point is visible
- Persist onboarding completion status for downstream lifecycle automation

### 3. Guardrails

- Must not enable social sign-in in this phase.
- Must not expose subsidy request forms before onboarding completion.
- Must not store unrestricted clinical notes in onboarding fields.

### 4. Out of scope

- Must not migrate legacy patient records in this intent (handled by INT-008).
- Must not implement multilingual content governance workflow (handled in later operations).

### 5. Acceptance

A patient creates a new account, completes onboarding fields, and only then sees the subsidy application start action; an incomplete profile keeps that action hidden.

### Open questions

- [ ] **Q-001** — Which exact fields are mandatory at onboarding versus deferred to first application? (Resolver: Product owner + Solution Architect)

---

## INT-002 — Identity policy baseline and access controls

epic `E05` · priority _(unassigned)_ · confidence _Assumed_ · surface `security`

### 1. Outcome

Internal and external access model is consistent with launch policy and ready for downstream role-based work.

### 2. Build target

- Define baseline permission sets for patient users and internal assessor users
- Configure access boundaries so internal users cannot view raw medical-history content
- Capture launch policy markers in metadata for deferred social sign-in decision

### 3. Guardrails

- Must not deploy direct production access changes without explicit confirmation.
- Must not grant internal users unrestricted patient clinical visibility.

### 4. Out of scope

- Must not implement AD federation topology in this intent (handled by INT-008).

### 5. Acceptance

An assessor can view eligibility evidence status but cannot open sensitive medical-history payload details.

### Open questions

- [ ] **Q-002** — Is social sign-in still deferred after Phase 1 go-live preparation? (Resolver: Security governance lead)

