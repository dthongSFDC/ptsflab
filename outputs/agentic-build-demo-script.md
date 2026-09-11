# Agentic build demo — 60-minute run-of-show

Internal demo script. Not a client deliverable.

**Audience:** customer stakeholders evaluating agentic Salesforce delivery  
**Length:** 60 minutes  
**Org:** demo sandbox only — no production deploy  
**Off stage:** Scopezilla / pre-sales tooling, Experience Cloud Setup, external APIs

## Shape of the hour

Proof first, craft second.

1. Read a prepared intent (`INT-003`), then plan → build → walk → prove it in the sandbox.
2. Pivot to new scope and author a new intent (practitioner assignment). Do not build it.


| Beat   | Artifact                          | Job                                               |
| ------ | --------------------------------- | ------------------------------------------------- |
| Build  | Prepared `INT-003` slice          | Intent survives plan → sandbox → proof            |
| Author | New assignment intent, draft only | New scope is authored, not stuffed into `INT-003` |




## Constraints

- Build from Intent, not from a prompt pile.
- Human gates: plan approval, Intent ratification. Production deploy would stay human on a real engagement; skip it today.
- Do not live-author `INT-003`. Read it, then build a thin slice.
- Do not open Experience Cloud Setup.



## Pre-bake (day before)

- [ ] Demo sandbox ready; build agent connected to that org
- [ ] Two users: patient-like and assessor
- [ ] Thin `INT-003` slice already green in the org as fallback (object, Path, illegal-transition Flow, record page, perm set)
- [ ] `INT-003` intent file openable in 10 seconds
- [ ] Blank intent template ready for the 42-minute pivot
- [ ] Timer rehearsal once; at minute 32, cut to the pre-baked org if the live build is still spinning



## Thin slice of `INT-003` (what you actually build)

**In**

- Subsidy application object and statuses
- Path on the record page
- One Flow that blocks illegal transitions (for example a list-view jump to Approved)
- Record page and permission set

**Out**

- Regional variants
- Eligibility checker
- Practitioner assignment
- Experience Cloud
- Email
- Dashboards

**Acceptance to prove in the room**

A submitted application moves Submitted → Pending Verification → Approved or Rejected. An illegal jump to Approved fails. A legal transition succeeds.

---



## Script



### 0–3 — Frame

One slide: **Intent → Plan (human) → Build → Prove (sandbox).** Sit down.

**Say:** We build from Intent, not from a prompt pile. When the ask is new scope, we author a new intent — you will see that after something is working.

### 3–8 — Read `INT-003` (do not write it)

Open **INT-003 — Subsidy application orchestration** (thin slice). Sixty seconds on the five sections:


| Section          | What you say                                                                          |
| ---------------- | ------------------------------------------------------------------------------------- |
| **Outcome**      | Applications move through a consistent, auditable lifecycle.                          |
| **Build target** | Object, statuses, Path, one Flow that blocks untracked jumps.                         |
| **Guardrails**   | No untracked status change; no skipping verification before Approved.                 |
| **Out of scope** | Practitioner assignment (later). Eligibility API (later).                             |
| **Acceptance**   | Submit → Submitted → Pending Verification → Approved or Rejected; illegal jump fails. |


**Say:** This file is the scope. The build is not allowed to invent past it.

Point at Out of scope — that is the pivot at minute 42.

### 8–38 — Plan, build, walk `INT-003`

```
PROMPT

We are going to do a demo thin-slice build of INT-003 without the regionalisation. Let's get started?
```

Start Plan mode on this intent only. Read two plan lines aloud. Approve.

Show the design file.

```
PROMPT

Create the unit test scripts
```

Build the thin slice listed above. 

Show the automated unit testing.

Sandbox walkthrough (same as Acceptance):

1. Create an application (pick patient-like or assessor-on-behalf; stick to one).
2. Path moves **Submitted → Pending Verification → Approved**.
3. Fail an illegal jump to Approved.
4. Succeed a legal transition.

**Minute 32 fallback:** stop narrating the spinner; open the pre-baked org; same four clicks.

### 38–42 — Prove (same org)

- Run org-probe (`object-exists`, `flow-active`, Path present).
- Tick the manual Path scene.

**Say:** Production stays a human confirmation; we are not doing that today.

Do not open a deployment-plan file unless someone asks.

### 42–58 — Pivot: new scope, author a new intent

Planted ask, as the customer:

> When it’s Approved, assign it to a practitioner. They accept or decline on the record.

Classify in 30 seconds:

- **Not a refine** — different job than the Path. `INT-003` already put assignment in Out of scope.
- **Not park** — they are asking to commit it.
- **New intent.**

Contrast, do not demo: *A verification checkbox before Approved would refine* `INT-003`*. This isn’t that.*

Author live, blank page. Agent drafts; edit one line out loud.


| Section          | Keep it small                                                                                        |
| ---------------- | ---------------------------------------------------------------------------------------------------- |
| **Outcome**      | An approved application has a practitioner who has accepted or declined.                             |
| **Build target** | Practitioner lookup on the application, Accept / Decline on the record, status updates.              |
| **Guardrails**   | No assignment before Approved; no looping reassign.                                                  |
| **Out of scope** | Geospatial matching, SLA timers, Experience Cloud / portal, eligibility API. `INT-003` stays closed. |
| **Acceptance**   | Assessor assigns on Approved → practitioner accepts on the record; a decline clears ownership.       |


Vet live. Catch one hole: *Who is in the practitioner pool?* → open question. Do not invent a matching engine.

Ratify as **draft**. Do not build it. Do not open Experience Cloud Setup.

### 58–60 — Close

They watched one intent become working software in the sandbox, then watched a new ask become a new Intent instead of a bolt-on to the last build.

**Say:** Plan approval and Intent ratification stay human. On a real engagement, production deploy would too. Week one is this loop: one sandbox, one intent this thin.

---



## Do not show

- Scopezilla or other pre-sales tooling
- A full phase
- Experience Cloud Setup
- An external API
- Social sign-in or medical-history policy debates
- Change sets, `release/*`, or production



## Fallback lines


| If this happens                          | Do this                                                                |
| ---------------------------------------- | ---------------------------------------------------------------------- |
| Live build still spinning at minute 32   | Cut to pre-baked org; keep the four-click walkthrough                  |
| Someone asks to see the portal           | Repeat Out of scope; assignment is internal on the record              |
| Someone asks to deploy to prod           | Human confirmation, not today; sandbox is the proof                    |
| Someone asks to build the new intent now | Offer it as the follow-up session, not this hour                       |
| Authored intent is vague                 | Stop and tighten Acceptance before ratifying; do not build from a hole |


