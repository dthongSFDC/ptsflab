# Scopezilla Operating Model: Roles, Handoffs and Speed

**Internal — for discussion** · 9 September 2026

---

## Executive summary

Scopezilla removed the old division of labour without replacing it. Solution scoping and estimation used to sit with the Delivery Leader (DL); SOW creation and negotiation sat with the Services Solution Sales Lead (SSSL). The tool now lets either role run the entire flow, and no one has said who should. The result is three patterns, all of them slower than the model they replaced, and none of them agreed.

**The constraint is capacity, in both roles.** We have 10 full-time SSSLs who also carry SOW writing and negotiation, and 24 DLs who each lead a delivery team of around fifteen people and pick up presales alongside sponsorship and escalations. Moving scoping between two saturated pools decides who queues. It does not create capacity. Any plan that reallocates work between the DL and the SSSL is therefore not a plan.

**Proposal: two depths, not two lanes.** The only lever available to us in the near term is to do less per deal. Most deals need a rough order of magnitude, not a due-diligence estimate, and today many of them get the full treatment anyway. Setting the required depth at intake, defaulting to the shorter one, is the single largest reduction in scoping load available — and it needs no new role, no retraining, and no new tooling. Alongside it, one named owner per step removes the collision, and a real review gate removes the architect re-run, which is duplicated senior time on every deal.

**Ask:** agreement on the two depths and the ownership rule, and sponsorship for the five actions below, all achievable inside a month.

**What this is not.** It recovers duplicated effort and reduces work per deal. It does not add capacity. If demand exceeds what these five items recover, the queue returns, and that is a demand and headcount conversation above this paper.

---

## What is happening today

| Pattern | What it costs |
|---|---|
| DL runs the whole flow, hands to SSSL for SOW and Org62 | Pulls the DL away from a delivery team of fifteen. Sustainable on a few deals, not as a default. |
| SSSL runs the whole flow, architect re-runs it | The expensive one. Senior time spent twice on the same deal, and the approval is still made on an output whose inputs the approver cannot see. |
| Both work the deal simultaneously | Ownership collision. Scopezilla is git-backed, so concurrent editing of the same step produces conflicts, not collaboration. |

## Root cause

**Every deal runs at full depth regardless of the confidence it needs.** An early-stage qualification and a deal we are about to commit to receive the same treatment. This is the largest single source of avoidable work, and nothing in the tool prevents it — depth is a decision we have never made explicitly.

**No named owner per step.** A Scopezilla step has one author by construction. Shared ownership of a step is not a collaboration model, it is a merge conflict.

**The approval has no audit surface.** The DL is asked to approve a conclusion without visibility of the premises it rests on. Re-deriving the scope is cheaper than reading it, so that is what happens. Everything needed is already captured in the project repository; it has never been surfaced as a review.

---

## The model: two depths, one process

**ROM depth — the default.** Discovery, epics and gaps, relative sizing. Stop there. No phase durations, no roster, no commercial model, no priced estimate. The output is explicitly low-confidence and disclosed as such. This is enough to qualify a deal, shape it, and decide whether to invest further.

**Committed depth.** The full chain through to the estimate sign-off, because a number anyone will be held to needs the confidence behind it.

**Depth is set at intake and defaults to ROM.** Committed depth requires a stated reason. That puts the burden of proof on the expensive option rather than the cheap one, which is the mechanism that makes the default hold under pressure.

**A deal can be promoted from ROM to committed** when it firms up. That is the normal path, not an exception — most deals should reach committed depth only once there is a reason to believe they will close.

**Who does what does not vary by depth.** Whoever holds the deal runs the deterministic steps. The DL makes the judgment calls at the four points the tool already stops for a human. The SSSL owns everything commercial. The appendix sets this out step by step.

**No scoping starts without a completed intake.** A one-screen deal shape: clouds in scope, integration surface, greenfield or brownfield, fixed date or not, configuration-shaped or build-shaped, client and buying pattern, and the depth required. A deal that arrives as a verbal ask does not enter the queue. This is the cheapest rework prevention available.

**Handoffs are pull requests.** Each phase runs on its own branch in the deal repository, so the handoff is a reviewable diff rather than a document drop. This is what makes the review possible and is the most direct fix for the re-run.

## The review, and the return leg

The DL is accountable for end-to-end deal approval, not only its architecture. So the review is on the **premises, not the conclusions**, and it covers both halves of that accountability, against a fixed question set and a time box:

- Confirmed / assumed / unknown split, particularly on the epics driving the size
- Every load-bearing architecture decision and how it was grounded
- Whether the roadmap is achievable, not merely sequenced
- Sponsorship, and the customer obligations the deal assumes the client can meet
- The governance and delivery-management load the shape implies
- Open gaps and source conflicts, and what the scope deliberately excludes

The failure mode is not the model, it is an approver signing quickly under volume. A fixed question set and a time box keep it a check rather than a signature.

**The review is surfaced as one standardised page**, generated from the deal's own data rather than written by hand. Same layout every deal, so any two are comparable and the DL is never reading a bespoke document. It reports; the DL decides.

**Findings return to the SSSL as review comments on the pull request.** No separate rework process: the diff is already the handoff, so objections attach to it, resolution is tracked, and approval is the merge.

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
| 1 | Set depth at intake, defaulting to ROM. Committed depth requires a stated reason | DL lead + SSSL lead | Week 1 |
| 2 | Publish the step ownership map (appendix), one named owner per step, with a stated turnaround on anything crossing roles | DL lead + SSSL lead | Week 2 |
| 3 | No scoping starts without a completed intake | SSSL lead | Week 1 |
| 4 | Build the review artifact and kill the re-run: the standardised page the DL reads, and the triaged return of findings. A report over data we already hold, built as a skill on Scopezilla | | Week 4 |
| 5 | Record the depth chosen and one line of rationale on every deal | SSSL lead | Week 1 |

Items 1, 2, 3 and 5 are conventions we can publish this week at no cost. Item 4 is the only build, and it is the one that returns duplicated senior time.

Action 5 matters most over time. We are designing from anecdote because we have no data. Twenty recorded decisions tell us whether the ROM default is holding, and where the depth calls are really being made.

## What this does not solve

**It does not create capacity.** It recovers duplicated effort and reduces work per deal. With both roles saturated, if Account Partner demand exceeds what these items recover, the queue returns. Managing that demand, or funding the capacity, sits above this paper.

**The review verifies process, not correctness.** It can confirm the gates were run and the decisions grounded. It cannot confirm they were resolved correctly. A confirmed tag attests that someone stood behind a claim, not that they were right.

**ROM depth is a disclosed trade.** A short chain produces a wider, less certain answer. That is the point, and it has to be stated on the output rather than discovered later by whoever quotes it.

**Tooling is not a lever this quarter.** SolutionIQ is the next-generation app being built on the Scopezilla engine, and it brings scope, estimate, risk and approval into one workflow. Its published roadmap does not cover Public Sector, Health or Nonprofit, and multi-cloud scoping arrives in the October release. Scopezilla remains required until SolutionIQ reaches global availability. Because SolutionIQ is a fork of the same engine, the review artifact in Action 4 is reusable — and worth submitting to the CoE while their approval process design is still open.

---

# Appendix — Draft step ownership map

Draft for agreement under Action 2. Roles: **DL** Delivery Leader / Architect, **SSSL** Services Solution Sales Lead.

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

The **ROM** column is the work reduction: at ROM depth, only the steps marked yes are run.

| Step | What the judgment is | Runs at ROM | DL involvement |
|---|---|---|---|
| `discover` | Extraction audit, gaps and assumptions | Yes | Reviews at the gate; SSSL prepares the document ingest |
| **`requirements`** | **Epic boundaries, scope stubs, double-counting, gap register** | **Yes** | **Approves the skeleton** |
| **`design`** | **Architecture forks, grounding, T-shirt sizing** | **Sizing only — forks flagged, not resolved** | **Approves the skeleton** |
| `roadmap` | Phasing, dependencies, duration basis | No — sequence only, no durations | Reviews the duration basis and the Phase 0 call |
| `efficiency` | AI delivery bands, which set the AI-native lane | No | Owns |
| **`estimate`** | **Named roster with justified counts; Solution Lead sign-off** | **No** | **Signs — this is the delivery approval** |
| `grill-me-on-scope` | Over- and under-sizing, confidence resolution | No | Owns |
| `risk-review` | Overall risk rating and its basis | No — risks noted, not rated | Owns |
| `revise` | Blast radius of an approved change | As needed | Re-approves what it touches |

## A3. Commercial judgment — the SSSL's

Nothing in this table runs at ROM depth. A ROM produces no price, no committed timeline and no SOW.

| Step | Note |
|---|---|
| `strategy` | Business case and value framing. AP contributes; not a DL step |
| **`commercials`** | **Rate validation and indicative pricing. The tool requires a rate the human supplies and validates — the SSSL's expertise, not an architect's** |
| `commercials` (deal-strategy mode) | Shaping the deal commercially: levers beyond rate, value anchoring |
| `rfp` | Bid decision, win strategy, compliance matrix. Fit and gap classification is delegated to `requirements`, so that part is a DL input |
| `sow-scope` | DL reviews exclusions and assumptions, which are delivery commitments |
| `narratives` | DL reviews technical sections |
| `seller-essentials`, `packaged-offerings` | Pre-scoping. Produces no price, ROM or committed timeline by design |

## Notes on the contested points

**The `estimate` sign-off is the delivery approval.** The tool already stops and asks for one name there. Running the sign-off and a separate delivery approval as two distinct gates is duplicated latency, and a candidate cause of the slowness we are trying to explain. Merge them.

**Roadmap, sponsorship and customer obligations are DL-owned** because the DL owns delivery governance and the delivery managers. They are not commercial steps.

**The AP has no vote in depth or routing.** Their incentive runs one way — more scoping coverage de-risks their deal at no cost to them. Depth is an internal capacity decision, not a deal-team decision, and "the AP asked" is not a stated reason for committed depth.

**Post-award steps are out of this map.** `quantum-leap` (build handoff) and `backlog` (user stories for a delivery team) belong to the delivery operating model.

**Where the split is genuinely arguable:** `roadmap` (delivery judgment, but the SSSL can draft the sequencing once sizes exist) and `efficiency` (the bands set the AI-native lane and therefore the price, so we have placed them with the DL). Both are worth a decision rather than a default.
