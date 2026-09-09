# Scopezilla Operating Model: Roles, Handoffs and Speed

**Internal — for discussion** · 9 September 2026

---

## Executive summary

Scopezilla removed the old division of labour without replacing it. Solution scoping and estimation used to sit with the Delivery Leader (DL); SOW creation and negotiation sat with the Services Solution Sales Lead (SSSL). The tool now lets either role run the entire flow, and no one has said who should.

The result is three patterns, all of them slower than the model they replaced. The cost is not the number of handoffs. It is that the handoffs are unbounded: no named owner, no defined input, no defined output. The most expensive pattern is the SSSL running the flow and the architect re-running it before approving, and the re-run is the diagnostic. The architect re-derives the scope because they cannot audit it, so redoing the work is cheaper than reading it.

**Proposal:** two speeds, chosen by the DL at intake, both running to a single common review artifact, with one clean handoff in each. Nothing about the tool changes. What changes is who owns which step, and what the approver actually reads at the gate.

**Ask:** agreement on the two-lane model and the ownership split, and sponsorship for the five actions below.

---

## What is happening today

| Pattern | What it costs |
|---|---|
| DL runs the whole flow, hands to SSSL for SOW and Org62 | The pre-Scopezilla model with a new tool. DL is the bottleneck; the SSSL adds nothing until the end. |
| SSSL runs the whole flow, architect re-runs it | The expensive one. Duplicated effort, and the delivery approval is made on an output whose inputs the approver cannot see. |
| Both work the deal simultaneously | Ownership collision. Scopezilla is git-backed, so concurrent editing of the same step produces conflicts, not collaboration. |

## Root cause

**No named owner per step.** A Scopezilla step has one author by construction. Shared ownership of a step is not a collaboration model, it is a merge conflict.

**The approval has no audit surface.** The DL is asked to approve a conclusion (a scope, a size, a SOW) without visibility of the premises it rests on: which claims were confirmed versus assumed, how the load-bearing architecture decisions were resolved, and what is still open. Everything needed is already captured in the project repository. It has never been surfaced as a review.

---

## The model: two speeds

The lanes differ in **where the architect's time sits**, not whether the architect is involved. Both end at the same delivery approval.

**Lane A — Architect-started.** The DL is present at the two gates where implementation judgment does its work: the epic skeleton (epic boundaries, scope stubs, double-counting) and the architecture skeleton (the load-bearing forks and the relative sizing everything downstream inherits). After the design gate, the deal hands to the SSSL for roadmap, commercials, narratives, packaging and the SOW. This is two touchpoints, not a full run.

**Lane B — SSSL-led.** The SSSL runs the flow. The DL's involvement is the review at the end.

**Routing.** The DL makes the call, at intake, from a one-screen deal shape the SSSL provides: clouds in scope, integration surface, greenfield or brownfield, fixed date or not, configuration-shaped or build-shaped, client and buying pattern. Judgment, not a scorecard — the DL owns the delivery outcome, so the DL owns the routing into it. Default is Lane B; the DL escalates on risk and complexity. A stated turnaround applies, or the bottleneck simply moves to the routing decision.

**Promotion.** The lane is revisable. A call made at intake rests on very little; discovery is what reveals whether a deal is hard. After the epics land, the SSSL flags anything that changed the shape and the DL can pull the deal into Lane A. This is the insurance against discovering a bad routing call at final review, which is the re-run we are trying to eliminate.

**Handoffs are pull requests.** Each phase runs on its own branch in the deal repository. The handoff is a reviewable diff, not a document drop. This is what makes Lane B auditable and is the single most direct fix for the re-run pattern.

## The review, and the return leg

The review is on the **premises, not the conclusions**, against a fixed question set and a time box:

- Confirmed / assumed / unknown split, particularly on the epics driving the size
- Every load-bearing architecture decision and how it was grounded
- Open gaps and source conflicts against the Phase 0 trigger
- What the scope excludes, and whether the exclusions are deliberate

The failure mode here is not the model, it is an approver signing quickly under volume. A fixed question set and a time box keep it a check rather than a signature.

**The review is surfaced as one standardised page**, generated from the deal's own data rather than written by hand. Same layout on every deal, so any two are comparable and the DL is never reading a bespoke document. It reports; the DL decides.

**Findings return to the SSSL as review comments on the pull request.** No separate rework process: the diff is already the handoff, so the objections attach to it, threading and resolution are tracked, and approval is the merge. This also produces a durable record of every objection raised, which is what Action 5 needs to turn judgment into an observable pattern.

**Findings are triaged into three kinds, because they need different work to close.** Naming them is what stops the return leg reproducing the same ambiguity in reverse:

| Finding | What it means | How it closes |
|---|---|---|
| Wrong | A decision resolved incorrectly, or an epic mis-sized | Recompute the downstream impact and re-run what it touches |
| Unproven | Stated as confirmed with no basis, or a capability named with nothing behind it | Stress-test and resolve, or demote it to a recorded gap |
| Missing | An implied activity nobody surfaced, typically change, testing or release management | Back to scope definition |

---

## Actions

| # | Action | Owner | By |
|---|---|---|---|
| 1 | Publish the step ownership map: every Scopezilla step tagged deterministic / implementation judgment / commercial judgment, one named owner each | DL lead + SSSL lead | |
| 2 | Adopt branch-per-phase handoffs on deal repositories so every handoff is a reviewable diff | DL lead | |
| 3 | Stand up the delivery review gate, both directions: the standardised page the DL reads, and the triaged return of findings to the SSSL. Adapt the existing review reporting rather than building new | | |
| 3a | Test pull-request review with two DLs before standardising on it; agree the written-findings fallback if it does not land | DL lead | |
| 4 | Curate the implementation and developer guides for our clouds into every deal's knowledge base | | |
| 5 | Record the lane decision and one line of rationale on every deal | SSSL lead | Immediate |

Action 5 is the cheapest and the most important over time. We are designing from anecdote because we have no data. Twenty recorded decisions turn the DL's judgment into an observable pattern, and the escalation criteria then write themselves from real calls rather than being invented up front.

## What this does not solve

**The review verifies process, not correctness.** It can confirm the gates were run and the decisions were grounded. It cannot confirm they were resolved correctly. A confirmed tag attests that someone stood behind a claim, not that they were right.

**Lane B is only safe where being wrong is recoverable.** The fence is tighter than any artifact can tell us, particularly in verticals where we have limited local delivery experience to draw on.

**Routing adds a touchpoint.** Small, but real. It needs a stated turnaround or it becomes the new queue.
