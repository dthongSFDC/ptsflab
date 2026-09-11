# Intent Statements — Phase 3 (PTSFLab)

> Reference role: the **load-bearing build target** for Phase 3. Each intent below is one capability — one firing trigger or user action, one outcome, one walkthrough. Build one at a time. The phase brief (`10-phase-3.md`) is orchestration; this file is what to build.
>
> **For architects:** walk these with the customer to assign priority and answer open questions. Edit `data/intents.json` (canonical) or this file directly — the next quantum-leap run re-renders from JSON.

## INT-005 — Practitioner assignment and reassignment engine

epic `E03` · priority _(unassigned)_ · confidence _Assumed_ · surface `automation`

### 1. Outcome

Eligible applications are assigned to the right practitioner quickly, with deterministic reassignment and escalation rules.

### 2. Build target

- Implement assignment logic by treatment type and proximity input
- Start practitioner acceptance SLA timer at assignment
- Reassign on decline or timeout using ordered fallback rules
- Escalate overdue cases to managers and track escalation outcomes

### 3. Guardrails

- Must not create infinite reassignment loops.
- Must not assign outside policy-eligible practitioner pools.

### 4. Out of scope

- Must not implement full geospatial optimization engine in this intent (external service may be required).

### 5. Acceptance

A new eligible application is assigned, reassigned when declined, and escalated to a manager when SLA limits are breached.

### Open questions

- [ ] **Q-003** — What is the definitive geospatial matching method and tie-break order? (Resolver: Operations lead + Technical Architect)

---

## INT-006 — Assessor collaboration and support routing

epic `E04` · priority _(unassigned)_ · confidence _Assumed_ · surface `console`

### 1. Outcome

Assessors can manage inbound collaboration requests with consistent routing and traceable handoffs.

### 2. Build target

- Configure collaboration intake channel to create or update trackable work records
- Route conversations to assessor queues based on language, region, and request type
- Provide escalation actions and status visibility inside assessor workspace
- Capture transcript and disposition metadata for quality and governance

### 3. Guardrails

- Must not allow collaboration records to bypass case/application traceability.
- Must not expose restricted medical-history content in support channels.

### 4. Out of scope

- Must not commit to 24x7 staffing model in platform configuration (operating model decision).

### 5. Acceptance

A patient support interaction is routed to the right assessor queue, linked to the underlying application record, and escalated through manager workflow when thresholds are exceeded.

### Open questions

_(no open questions captured)_

---

## INT-007 — Operational reporting and escalation visibility

epic `E04` · priority _(unassigned)_ · confidence _Confirmed_ · surface `reports`

### 1. Outcome

Leads can monitor queue health, SLA performance, and escalation load by region.

### 2. Build target

- Build dashboards for application lifecycle throughput, pending verification backlog, and overdue assessments
- Add manager-facing escalation report with aging and ownership views
- Include regional slices for APAC, EMEA, and AMER operations

### 3. Guardrails

- Must not expose personally sensitive fields in manager summary reports.

### 4. Out of scope

- Must not deliver predictive analytics in this phase.

### 5. Acceptance

An operations manager can open a dashboard and identify overdue assessments, current escalation owners, and regional queue pressure in one view.

### Open questions

_(no open questions captured)_

