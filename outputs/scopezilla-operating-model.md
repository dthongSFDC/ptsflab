# Scopezilla Operating Model: Roles, Handoffs and Speed

**Internal — for discussion** · 9 September 2026

---

## Executive summary

Scopezilla removed the old division of labour without replacing it. The solution used to sit with the Delivery Leader (DL); proposal creation and negotiation sat with the Services Solution Sales Lead (SSSL). The DL approves the estimates and is accountable for follow-on delivery. The new tool lets either role run the entire or parts of the flow, and no one has agreed who should.

Two consequences have surfaced from the DLs. **Work is being done twice** — an SSSL scopes a deal and the architect re-runs it before approving. And **there is sometimes no confidence in the output** — the approver cannot see which claims were confirmed, which were assumed, and how the load-bearing decisions were reached, so re-deriving the scope is cheaper than auditing it. The duplication is not carelessness. It is the rational response to an artefact you cannot inspect and also the fact the DLs are fully accountable for subsequent delivery of the deal.

**Proposal, in two parts.**

- **Two speeds, routed on risk and complexity.** On a higher-risk or more complex deal the DL is present when the shape of the solution is decided on the parts where implementation judgement is critical. On a lower-risk deal the SSSL runs it and the DL reviews the output. The DL makes the call at intake.
- **A standardised review that makes the scope inspectable** — and that leads with whether the scope declares its own uncertainty honestly. This is what ends the re-run, and it is the only build item in the plan.

**Ask:** agreement on the two speeds, the ownership split, and sponsorship for the actions below, all achievable inside a month.

**What this is not.** It removes duplicated senior effort and makes the delivery approval mean something. It does not add capacity. With 10 full-time SSSLs and 24 DLs who each lead a delivery team and accountable for delivery, if demand exceeds what this recovers, the queue returns — and that is a demand and headcount conversation above this paper.

---

## What is happening today

| Pattern | What it costs |
|---|---|
| DL runs the whole flow, hands to SSSL for SOW and Org62 | Pulls the DL away from a delivery team of fifteen. Sustainable on a few deals, not as a default. |
| SSSL runs the whole flow, architect re-runs it | The expensive one, and the source of the complaint that Scopezilla costs a DL *more* time than before: they used to scope a deal once, and now they review someone else's scoping and re-do it anyway. |
| Both work the deal simultaneously | Ownership collision. Scopezilla is git-backed, so concurrent editing of the same step produces conflicts, not collaboration. |

## Root cause

**The approval has no audit surface.** The DL is asked to approve a conclusion — a scope, a size, a set of assumptions — without visibility of the premises it rests on. Everything needed is already captured in the project repository and has never been surfaced as a review. Until it is, re-running the work is the cheaper option, and the duplication will continue no matter who owns which step.

**No named owner per step.** A Scopezilla step has one author by construction. Shared ownership of a step is not a collaboration model, it is a merge conflict.

**Neither is a tooling gap.** Both are decisions we have not made.

---

## The model: two speeds

The speeds differ in **where the DL's time sits**, not whether the DL is involved. Both end at the same delivery approval.

**Speed A — DL-SSSL paired.** The DL is present through the front end, where implementation judgment does its work: discovery, the epic skeleton (epic boundaries, scope stubs, double-counting), the architecture skeleton (the load-bearing forks and the relative sizing everything downstream inherits), and the scope stress-test that follows. After that the deal hands to the SSSL for roadmap, pricing, narrative and SOW. One contiguous sitting, not a full run.

**Speed B — SSSL-led.** The SSSL runs the whole flow, front to back. The DL reviews the output based on tooling signals and signs the estimate.

**Speed A means the DL is in the room for the front end** — discovery, the epic skeleton, the architecture skeleton, and the scope stress-test that follows them. Everything downstream is derivation and commercial work, and it is the SSSL's in both speeds. The only step the DL runs outright in either speed is the formal risk review, because the recommended rating carries their name at the gate.

**Routing is the DL's call at intake, on risk and complexity.** The SSSL completes a one-screen deal shape and proposes a speed; the DL confirms or overrides within a stated turnaround, or the bottleneck simply moves to the routing decision. Judgment, not a scorecard — but informed by a consistent set of factors:

- Clouds in scope, and whether we have delivered them locally
- Single-cloud or multi-cloud
- Net-new integration surface
- Greenfield or brownfield
- Configuration-shaped or build-shaped, particularly on industry clouds where the platform ships capability that can be mis-scoped as a build
- Fixed, regulatory or immovable date
- Regulated environment, data residency or sovereignty constraints
- Data migration volume
- Client governance maturity and decision velocity

**Default is Speed B**, and Speed A requires a stated reason. That puts the burden of proof on the more expensive option rather than the cheaper one, which is the mechanism that makes the default hold under pressure.

**The AP has no vote.** Their incentive runs one way — architect coverage de-risks their deal at no cost to them, so left open they will request it every time, entirely rationally. Speed is an internal resourcing decision, not a deal-team decision, and "the AP asked" is not a stated reason for Speed A.

**The speed is revisable.** A call made at intake rests on very little; discovery is what reveals whether a deal is hard. After the epics land, the SSSL flags anything that changed the shape and the DL can move it to Speed A. This is the insurance against discovering a bad routing call at final review, which is the re-run we are trying to eliminate.

**Handoffs are pull requests.** Each phase runs on its own branch in the deal repository, so the handoff is a reviewable diff rather than a document drop. This is what makes Speed B auditable and is the most direct fix for the duplication.

## The review, and the return leg

The DL approves the **delivery** of the deal, across all of it and not only its architecture: scope, governance, assumptions and risk. The commercials — rate, price, margin, commercial terms — are the SSSL's/APs/Services Leadership and are explicitly **not** in this review. Leverage the existing `/deal-review` skill or enhance it to suit.

### It leads with whether the scope declares its own uncertainty

This is the part that does the real work, and it is cheap to compute because Scopezilla already records all of it. **On a real deal, declared uncertainty is a sign of competent scoping; its absence is the warning.** A scope that arrives tidy, fully confirmed and gap-free has usually not been interrogated. So the page opens with:

- Items marked confirmed with no basis recorded against them
- A gap count implausibly low for the volume of requirements
- Architecture decisions carrying no grounding
- Named clouds, integrations or personas with nothing buildable behind them
- Sizes with no complexity rationale
- Assumptions absent on a deal with thin discovery

None of that judges the author. It reads the artifact, it reads the same way on every deal, and it points the reviewer straight at what to test.

### Then the premises

Against a fixed question set and a time box:

- Confirmed / assumed / unknown split, particularly on the epics driving the size
- Every load-bearing architecture decision and how it was grounded
- Whether the roadmap is achievable, not merely sequenced
- Sponsorship, and the customer obligations the deal assumes the client can meet
- The governance and delivery-management load the shape implies
- Open gaps and source conflicts, and what the scope deliberately excludes

The failure mode is not the model, it is an approver signing quickly under volume. A fixed question set and a time box keep it a check rather than a signature.

**The review is one standardised page**, generated from the deal's own data rather than written by hand. Same layout every deal, so any two are comparable and the DL is never reading a bespoke document. It reports; the DL decides.

**Findings return to the SSSL as review comments on the pull request.** No separate rework process: the diff is already the handoff, so objections attach to it, resolution is tracked, and approval is the merge. This also produces a durable record of every objection raised.

**Findings are triaged into three kinds,** because they need different work to close, and naming them stops the return leg reproducing the same ambiguity in reverse:

| Finding | What it means | How it closes |
|---|---|---|
| Wrong | A decision resolved incorrectly, or an epic mis-sized | `revise` — recomputes the downstream impact and re-runs what it touches |
| Unproven | Stated as confirmed with no basis, or a capability named with nothing behind it | `grill-me-on-scope` — resolves it, or demotes it to a recorded gap |
| Missing | An implied activity nobody surfaced, typically change, testing or release management | `requirements` — back to scope definition |

---

## Actions — all inside a month

| # | Action | Owner | By |
|---|---|---|---|
| 1 | Publish the step ownership map (appendix), one named owner per step, with a stated turnaround on anything crossing roles | DL lead + SSSL lead | Week 2 |
| 2 | Agree the routing factors and the intake shape. Default Speed B; Speed A requires a stated reason | DL lead + SSSL lead | Week 1 |
| 3 | No scoping starts without a completed intake | SSSL lead | Week 1 |
| 4 | Build the review artifact and end the re-run: the standardised page, leading with the uncertainty signals, plus the triaged return of findings. A report over data we already hold, built as a skill on Scopezilla | DL lead, with a named DL building it | Week 4 |
| 5 | Adopt branch-per-phase handoffs so every handoff is a reviewable diff | DL lead | Week 3 |
| 6 | Record the speed proposed, the speed decided, and one line of rationale on every deal | SSSL lead | Week 1 |

Items 1, 2, 3 and 6 are conventions we can publish this week at no cost. Item 4 is the only build, and it is load-bearing for the rest: if the page is not good enough to read instead of re-derive, DLs will keep re-running and nothing else here matters. Its acceptance test is simple — can a DL clear a Speed B deal without opening the repository.

**Item 4 sits with delivery because the approver has to own the acceptance test**; nobody else can say when the page is sufficient to review from rather than re-derive. It needs a named individual rather than a lead, or it will not land inside the month. Two conditions on it: the uncertainty signals are **agreed with the SSSL lead before first use**, so it is a shared standard rather than an instrument aimed at their team and so the signals are not relitigated deal by deal; and it reports only — it never scores a person, and the record it produces is for coaching, not comparison.

Action 6 matters most over time. We are designing from anecdote because we have no data. Twenty recorded decisions turn the routing judgment into an observable pattern, and the escalation criteria then write themselves from real calls rather than being invented up front.

## What this does not solve

**Routing on the deal does not screen the scoping.** Risk and complexity are the right signal for deciding where an architect's time is best spent, but they only correlate with where a scope goes wrong. A thin or over-confident scope on a straightforward deal will route to Speed B untouched. That is precisely why the review leads with the uncertainty signals — the review is what catches it, and it is the reason Action 4 is not optional.

**The review verifies process, not correctness.** It can confirm the gates were run and the decisions grounded. It cannot confirm they were resolved correctly. A confirmed tag attests that someone stood behind a claim, not that they were right.

**It does not create capacity.** It removes duplicated senior effort. With both roles saturated, if Account Partner demand exceeds what that recovers, the queue returns. Managing that demand, or funding the capacity, sits above this paper.

**Tooling is not a lever this quarter.** SolutionIQ is the next-generation app being built on the Scopezilla engine, and it brings scope, estimate, risk and approval into one workflow. Its published roadmap does not cover Public Sector, Health or Nonprofit, and multi-cloud scoping arrives in the October release. Scopezilla remains required until SolutionIQ reaches global availability. Because SolutionIQ is a fork of the same engine, the review artifact in Action 4 is reusable — and worth submitting to the CoE while their Deal Review and Approval Process design is still open.

---

# Appendix — Draft step ownership map

Draft for agreement under Action 1. Roles: **DL** Delivery Leader / Architect, **SSSL** Services Solution Sales Lead.

Three principles behind the assignments:

1. **One named owner per step.** Not one per deal. Shared ownership of a step is a merge conflict.
2. **Hang the model on the stops the tool already has.** Scopezilla already halts for a human at four places: the epic skeleton in `requirements`, the architecture skeleton in `design`, the Solution Lead sign-off in `estimate`, and rate validation in `commercials`. We do not need to invent gates; we need to say who stands at the existing ones.
3. **Judgment is not all delivery judgment.** Rate validation and deal shaping are the SSSL's expertise, not an architect's, and should not route to a DL.

## A1. Deterministic — no approval, whoever holds the deal runs it

Output is produced by a script or a render. There is no judgment call and therefore no handoff. Some current delay is people queueing for a human on these.

| Step | What it does |
|---|---|
| `setup`, `collaborate` | Creates the project and the shared repository |
| `validate` | Runs the data consistency checker |
| `export` | Produces the workbook and packages deliverables |
| `deal-review`, `capability-map` | Renders internal views from existing data; report-only, mutates nothing |
| `share`, `slides` | Publishes a deliverable or builds a deck |
| `org62` | Derives the load file from an already-approved roster |
| `cleanup`, `wrapup` | Housekeeping |

## A2. Implementation judgment — the DL's

Only the front-end rows change between speeds. Everything below them is the SSSL's in both, with the DL reviewing and signing rather than running.

| Step | What the judgment is | Who runs it | DL involvement |
|---|---|---|---|
| `discover` | Extraction audit, gaps and assumptions | **Speed A: DL · Speed B: SSSL** | Speed A: runs the gap interview. Speed B: read at the review. The SSSL prepares the document ingest either way |
| **`requirements`** | **Epic boundaries, scope stubs, double-counting, gap register** | **Speed A: DL · Speed B: SSSL** | **Speed A: approves the skeleton live. Speed B: at the review** |
| **`design`** | **Architecture forks, grounding, T-shirt sizing** | **Speed A: DL · Speed B: SSSL** | **Speed A: approves the skeleton live. Speed B: at the review** |
| `roadmap` | Phasing, dependencies, duration basis | SSSL | Reviews the duration basis and the Phase 0 call |
| `efficiency` | AI delivery bands, which set the AI-native lane | SSSL | Confirms the band — an AI-native compression is a delivery claim we will be held to |
| **`estimate`** | **Named roster with justified counts; Solution Lead sign-off** | **SSSL drafts the roster** | **Signs — this is the delivery approval** |
| `grill-me-on-scope` | Over- and under-sizing, confidence resolution | **Speed A: DL · Speed B: SSSL** | **Speed A: runs it in the same sitting as the design gate** — not a separate handoff. Speed B: directs it through the review findings |
| `risk-review` | Overall risk rating and its basis | DL | Owns outright — the recommended rating carries the DL's name at the risk gate |
| `revise` | Blast radius of an approved change | Step owner | Re-approves what it touches |

## A3. Commercial judgment — the SSSL's, in both speeds

| Step | Note |
|---|---|
| `strategy` | Business case and value framing. AP contributes; not a DL step |
| **`commercials`** | **Rate validation and indicative pricing. The tool requires a rate the human supplies and validates — the SSSL's expertise, not an architect's. Not reviewed by the DL** |
| `commercials` (deal-strategy mode) | Shaping the deal commercially: levers beyond rate, value anchoring |
| `rfp` | Bid decision, win strategy, compliance matrix. Fit and gap classification is delegated to `requirements`, so that part is a DL input |
| `sow-scope` | DL reviews exclusions and assumptions, which are delivery commitments |
| `narratives` | DL reviews technical sections |
| `seller-essentials`, `packaged-offerings` | Pre-scoping. Produces no price, ROM or committed timeline by design |

## Notes on the contested points

**The `estimate` sign-off is the delivery approval, and the tool's own boundary matches ours.** Scopezilla keeps rates out of `estimate` entirely — roster, effort and duration live there, and rates exist only in `commercials`. So the sign-off it already stops for is a delivery sign-off, not a commercial one, which is exactly the line we are drawing. Running that sign-off and a separate delivery approval as two distinct gates is duplicated latency, and a candidate cause of the slowness we are trying to explain. Merge them.

**Roadmap, sponsorship and customer obligations are DL-owned** because the DL owns delivery governance and the delivery managers. They are not commercial steps.

**A ROM is a priced ±30% estimate.** It runs the same chain as any other estimate — the tool will not manufacture a number from a short one — and the only thing it omits is the SOW. Speed is therefore about where the architect's time sits, not about producing a cheaper artifact.

**Post-award steps are out of this map.** `quantum-leap` (build handoff) and `backlog` (user stories for a delivery team) belong to the delivery operating model.

**Where the split is genuinely arguable:** `roadmap` (delivery judgment, but the SSSL can draft the sequencing once sizes exist) and `efficiency` (the bands set the AI-native lane and therefore the price, so we have placed them with the DL). Both are worth a decision rather than a default.
