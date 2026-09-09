# Scopezilla Operating Model: Roles, Handoffs and Speed

**Internal — for discussion** · 9 September 2026

---

## Executive summary

Scopezilla removed the old division of labour without replacing it. Solution scoping and estimation used to sit with the Delivery Leader (DL); SOW creation and negotiation sat with the Services Solution Sales Lead (SSSL). The tool now lets either role run the entire flow, and no one has said who should. The result is three patterns, all of them slower than the model they replaced, and none of them agreed.

**The constraint is capacity, in both roles.** We have 10 full-time SSSLs who also carry SOW writing and negotiation, and 24 DLs who each lead a delivery team of around fifteen people and pick up presales alongside sponsorship and escalations. Moving scoping between two saturated pools decides who queues. It does not create capacity. Any plan that reallocates work between the DL and the SSSL is therefore not a plan.

**Proposal: two speeds, set by the confidence the deal needs.** The only lever available to us in the near term is to do less per deal. Most deals need a rough order of magnitude, not a due-diligence estimate, and today many of them get the full treatment anyway.

- **Speed 1 — ROM at ±30%.** One pass through the chain on the information we already have. Assumptions disclosed rather than resolved. Time-boxed, no gap-closing loop, no SOW. Reviewed by a DL as a **fifteen-minute sanity check** on whether the uncertainty is honestly priced into the range.
- **Speed 2 — Committed.** Iterate on the gaps that materially move the number until the range tightens, then the SOW. The full premises review and the estimate sign-off.

**The difference is not which steps run — it is whether we chase the gaps.** A priced ROM needs the whole chain, because the tool will not produce a number from a short one. Running the tool was never the expensive part; the expensive part is the human loop of interviews and follow-ups that converts assumed into confirmed. That is where the weeks go, and it is why Scopezilla can feel like it costs a DL more time rather than less: the tool got fast, the loop did not.

**Ask:** agreement on the two speeds and the ownership rule, and sponsorship for the five actions below, all achievable inside a month.

**What this is not.** It recovers duplicated effort and stops us over-investing in deals that will not close. It does not add capacity. If demand exceeds what these five items recover, the queue returns, and that is a demand and headcount conversation above this paper.

---

## What is happening today

| Pattern | What it costs |
|---|---|
| DL runs the whole flow, hands to SSSL for SOW and Org62 | Pulls the DL away from a delivery team of fifteen. Sustainable on a few deals, not as a default. |
| SSSL runs the whole flow, architect re-runs it | The expensive one, and the source of the DL complaint that Scopezilla costs them *more* time than before: they used to scope a deal once, and now they review someone else's scoping and re-do it anyway. Senior time spent twice on the same deal. |
| Both work the deal simultaneously | Ownership collision. Scopezilla is git-backed, so concurrent editing of the same step produces conflicts, not collaboration. |

## Root cause

**Every deal gets the gap-closing loop, regardless of the confidence it needs.** An early-stage qualification and a deal we are about to commit to receive the same treatment. Chasing answers is the expensive part of scoping — not running the tool — and we have never made an explicit decision about when to stop chasing and price the uncertainty instead.

**No named owner per step.** A Scopezilla step has one author by construction. Shared ownership of a step is not a collaboration model, it is a merge conflict.

**The approval has no audit surface.** The DL is asked to approve a conclusion without visibility of the premises it rests on. Re-deriving the scope is cheaper than reading it, so that is what happens. Everything needed is already captured in the project repository; it has never been surfaced as a review. This is why the re-run happens, and it is what makes Scopezilla a net cost to a DL rather than a saving.

---

## The model: two speeds

**Speed 1 — ROM at ±30%, and the default.** A single pass through the chain — scope, sizing, duration basis, roster, price — on the information already available. The load-bearing assumptions are disclosed rather than chased, and the ±30% band is what buys the right to stop. Time-boxed, with no gap-closing loop and no SOW. SSSL-led, and sanity-checked by a DL before it is shared.

**Speed 2 — Committed.** The same chain, but now we iterate: close the gaps that materially move the number, tighten the range, then the SOW. This is where the full premises review and the estimate sign-off sit.

**Both speeds run essentially the same steps.** A priced ROM needs the whole derivation — the tool refuses to manufacture a number from a short chain, which is deliberate and correct. What separates the speeds is iteration and gap closure, not step selection. Anyone looking for the saving in "fewer steps" will not find it there.

**DL involvement scales in three steps:**

| | Review | What the DL does |
|---|---|---|
| ROM | Sanity check | A fifteen-minute read off the standardised page |
| Committed, simple | Full premises review | Reads the page, signs the estimate |
| Committed, complex | Full premises review | Approves the design skeleton live, then reads and signs |

Simple and complex is the DL's call at intake, and it is a judgment rather than a scorecard.

**The ROM sanity check asks one thing: is the uncertainty honestly priced into the range?** A ±30% ROM is defensible when the load-bearing assumptions are visible and the band genuinely covers them. It is indefensible when it is ±30% around a wrong premise. Four questions, and nothing more:

1. Are the load-bearing assumptions visible, and are they the right ones?
2. Is anything scoped as a build that the platform actually ships — the error a ±30% band will not absorb?
3. Does the band actually cover the identified risk, or is the ±30% cosmetic?
4. Is there an obvious delivery-readiness red flag — an immovable date, absent sponsorship, a dependency nobody owns?

Output is "fine to share as a ROM" or "not yet". It is a read, not a meeting.

**Speed is set at intake and defaults to ROM.** Speed 2 requires a stated reason, which puts the burden of proof on the expensive option rather than the cheap one. That is the mechanism that makes the default hold under pressure.

**Promotion from ROM to committed is the normal path, not an exception.** Most deals should reach speed 2 only once there is a reason to believe they will close, and promotion is the trigger for DL involvement.

**Otherwise, who does what does not vary.** Whoever holds the deal runs the deterministic steps. The SSSL owns everything commercial. The appendix sets this out step by step.

**No scoping starts without a completed intake.** A one-screen deal shape: clouds in scope, integration surface, greenfield or brownfield, fixed date or not, configuration-shaped or build-shaped, client and buying pattern, and the speed required. A deal that arrives as a verbal ask does not enter the queue. This is the cheapest rework prevention available.

**Handoffs are pull requests.** Each phase runs on its own branch in the deal repository, so the handoff is a reviewable diff rather than a document drop. This is what makes the review possible and is the most direct fix for the re-run.

## The review, and the return leg

This is the **full review, at speed 2**. The ROM sanity check above is the short form of it.

The DL approves the **delivery** of the deal, across all of it and not only its architecture: scope, governance, assumptions and risk. The commercials — rate, price, margin, commercial terms — are the SSSL's and are explicitly **not** in this review.

So the review is on the **premises, not the conclusions**, against a fixed question set and a time box:

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
| 1 | Set speed at intake, defaulting to ROM. Speed 2 requires a stated reason. Time-box the ROM pass and agree the sanity check as a fifteen-minute read against four questions | DL lead + SSSL lead | Week 1 |
| 2 | Publish the step ownership map (appendix), one named owner per step, with a stated turnaround on anything crossing roles | DL lead + SSSL lead | Week 2 |
| 3 | No scoping starts without a completed intake | SSSL lead | Week 1 |
| 4 | Build the review artifact and kill the re-run: the standardised page the DL reads at both intensities, and the triaged return of findings. A report over data we already hold, built as a skill on Scopezilla | | Week 4 |
| 5 | Record the speed chosen, simple or complex, and one line of rationale on every deal | SSSL lead | Week 1 |

Items 1, 2, 3 and 5 are conventions we can publish this week at no cost. Item 4 is the only build, and it is load-bearing for all of them: a fifteen-minute ROM review is only possible if the page is good enough to read instead of re-derive. If it is not, DLs will keep re-running and nothing else here matters.

Action 5 matters most over time. We are designing from anecdote because we have no data. Twenty recorded decisions tell us whether the ROM default is holding, how many deals actually reach speed 2, and therefore what the real DL load is.

## What this does not solve

**It does not create capacity.** It recovers duplicated effort and stops us over-investing in deals that will not close. With both roles saturated, if Account Partner demand exceeds what these items recover, the queue returns. Managing that demand, or funding the capacity, sits above this paper.

**The review verifies process, not correctness.** It can confirm the gates were run and the decisions grounded. It cannot confirm they were resolved correctly. A confirmed tag attests that someone stood behind a claim, not that they were right.

**ROM is a disclosed trade, and the ±30% is the whole of it.** Stopping before the gaps are closed buys speed and pays for it in range. That only works if the assumptions behind the band are stated on the output rather than discovered later by whoever quotes it, and if the band is never quietly narrowed on the way to a client. A ROM that has passed the sanity check is a ±30% number, not a commitment and not a basis for a SOW.

**The saving is smaller than "two speeds" makes it sound.** Both speeds run the same steps, so the recovered time comes from three places only: not re-running someone else's work, not iterating on deals that will not close, and holding the ROM pass inside its time box so it cannot quietly become a committed estimate. That third one is a discipline, not a mechanism, and it will need enforcing.

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

These run at **both** speeds — a priced ROM needs the whole chain. At ROM they run once on the information available, with assumptions disclosed. At committed, we iterate until the gaps that move the number are closed. The two exceptions are marked.

| Step | What the judgment is | DL involvement |
|---|---|---|
| `discover` | Extraction audit, gaps and assumptions | Read at the review; SSSL runs it |
| `requirements` | Epic boundaries, scope stubs, double-counting, gap register | Read at the review; approves the skeleton live on a complex deal |
| **`design`** | **Architecture forks, grounding, T-shirt sizing** | **Approves the skeleton on a complex deal.** At ROM, unresolved forks are disclosed as assumptions rather than closed |
| `roadmap` | Phasing, dependencies, duration basis | Reviews the duration basis and the Phase 0 call |
| `efficiency` | AI delivery bands, which set the AI-native lane | Owns; only when an AI-native lane is being priced |
| **`estimate`** | **Named roster with justified counts; Solution Lead sign-off** | **Signs — this is the delivery approval** |
| `grill-me-on-scope` | Over- and under-sizing, confidence resolution | Owns — **speed 2 only**, it is the gap-closing pass |
| `risk-review` | Overall risk rating and its basis | Owns — **speed 2 only**; at ROM, risks are noted, not rated |
| `revise` | Blast radius of an approved change | Re-approves what it touches |

## A3. Commercial judgment — the SSSL's

`commercials` runs at **both** speeds — a priced ROM needs a validated rate, so it cannot be skipped. `sow-scope` is speed 2 only: the SOW is the one thing a ROM genuinely does not include.

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

**The `estimate` sign-off is the delivery approval, and the tool's own boundary matches ours.** Scopezilla keeps rates out of `estimate` entirely — the roster, effort and duration live there, and rates exist only in `commercials`. So the sign-off it already stops for is a delivery sign-off, not a commercial one, which is exactly the line we are drawing. Running that sign-off and a separate delivery approval as two distinct gates is duplicated latency, and a candidate cause of the slowness we are trying to explain. Merge them.

**Roadmap, sponsorship and customer obligations are DL-owned** because the DL owns delivery governance and the delivery managers. They are not commercial steps.

**The AP has no vote in the speed.** Their incentive runs one way — more scoping coverage de-risks their deal at no cost to them. Speed is an internal capacity decision, not a deal-team decision, and "the AP asked" is not a stated reason for speed 2.

**Post-award steps are out of this map.** `quantum-leap` (build handoff) and `backlog` (user stories for a delivery team) belong to the delivery operating model.

**Where the split is genuinely arguable:** `roadmap` (delivery judgment, but the SSSL can draft the sequencing once sizes exist) and `efficiency` (the bands set the AI-native lane and therefore the price, so we have placed them with the DL). Both are worth a decision rather than a default.
