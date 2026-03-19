<!--
AI_NOTE_START

Document role:
This file is the example pack for tiny planner outputs inside Auto Repair v1.

How to use this file:
1. Read this file after:
   - [Repair Planner Spec v1](./repair-planner-spec-v1.md)
   - [Repair Planner Prompt v1](./repair-planner-prompt-v1.md)
   - [Repair Plan Schema v1](./repair-plan-schema-v1.json)
2. Use this page to inspect what small, structurally valid planner outputs should look like.
3. Treat this file as an example pack for planner behavior, not as proof of full autonomous repair.
4. Read together with:
   - [Planner Review Checklist v1](./planner-review-checklist-v1.md)
   - [Planner Test Note v1](./planner-test-note-v1.md)
   - [Repair Validation Loop v1](./repair-validation-loop-v1.md)
   - [Rollback Policy v1](./rollback-policy-v1.md)

What this file is:
- The tiny output example pack for the planner layer
- A teaching page for what good first-step planner outputs look like
- A compact demonstration layer between planner spec and real repair execution
- A practical reference for humans and AI systems checking planner shape

What this file is not:
- Not the full planner spec
- Not the full repair engine
- Not proof of autonomous closure
- Not a benchmark suite
- Not a replacement for validation and rollback discipline

Reading discipline for AI:
- Preserve the distinction between diagnosis, first repair planning, validation, rollback, and escalation.
- Treat these outputs as tiny examples of correct planner shape, not as final full repair scripts.
- Keep the planner in first-move territory.
- Do not overread compact output examples as proof that full repair is solved.

AI_NOTE_END
-->

# Tiny Planner Output Examples Pack v1 🧩

## Example pack for small, valid repair-planner outputs inside Auto Repair v1

Quick links:

- [Back to Auto Repair README](./README.md)
- [Open Repair Planner Spec v1](./repair-planner-spec-v1.md)
- [Open Repair Planner Prompt v1](./repair-planner-prompt-v1.md)
- [Open Repair Plan Schema v1](./repair-plan-schema-v1.json)
- [Open Planner Review Checklist v1](./planner-review-checklist-v1.md)
- [Open Planner Test Note v1](./planner-test-note-v1.md)
- [Open Repair Validation Loop v1](./repair-validation-loop-v1.md)
- [Open Rollback Policy v1](./rollback-policy-v1.md)
- [Back to Atlas landing page](../../../wfgy-ai-problem-map-troubleshooting-atlas.md)

---

If the planner spec defines **what the planner is allowed to produce**, this page shows **what that output actually looks like in small, usable examples**. 🧭

This file is here for a very practical reason:

> many systems sound clean at the spec level  
> but become vague, oversized, or fake-confident when they actually produce output

This page helps prevent that.

It makes the planner layer more concrete by showing tiny outputs that are:

- structured
- modest
- validation-aware
- rollback-aware
- clearly first-move oriented

Short version:

> diagnose first  
> plan one controlled move  
> define validation  
> keep rollback visible  
> escalate only when needed

That is the spirit of this pack.

---

## Quick start 🚀

### I am new to the planner layer

Use this path:

1. read [Repair Planner Spec v1](./repair-planner-spec-v1.md)
2. read [Repair Planner Prompt v1](./repair-planner-prompt-v1.md)
3. read this page
4. compare the examples against [Repair Plan Schema v1](./repair-plan-schema-v1.json)
5. check them against [Planner Review Checklist v1](./planner-review-checklist-v1.md)

### I already know the planner and want the shortest route

Start here:

1. read Example 1, Example 2, and Example 3
2. inspect the `repair_move`, `validation_check`, and `rollback_trigger`
3. compare compact planner behavior across F1, F4, and F7 style cases
4. use the review checklist if you want to judge output quality

Shortest possible reading:

> good planner output is small  
> tied to the diagnosed break  
> explicit about validation  
> explicit about rollback  
> and never pretends to solve the whole case in one jump

---

## What this page is teaching 🎯

This example pack is not only showing JSON-like planner shapes.

It is teaching five deeper habits:

1. **repair must stay route-sensitive**  
   the move should follow the diagnosed failure family

2. **the first move must stay small**  
   the planner should not explode into a giant repair screenplay

3. **validation is part of the output**  
   a planner output without validation is incomplete

4. **rollback must stay visible**  
   small repair still needs a safe exit

5. **escalation must remain honest**  
   some cases should not pretend to be locally solved

That is why tiny examples matter.

Tiny examples reveal whether the planner really understands restraint.

---

## What good tiny planner output should look like ✅

A good tiny planner output usually has these properties:

- one clear first move
- one clear target invariant
- one clear validation check
- one clear rollback trigger
- one clear escalation condition when needed

It should feel like:

> the smallest controlled step that is still worth trying

It should **not** feel like:

- a whole migration plan
- a long repair essay
- a speculative redesign
- a fake “AI solved everything” story

---

## Canonical tiny output shape

The exact schema lives elsewhere, but most good tiny planner outputs here follow a compact shape like this:

```json
{
  "case_id": "example_name",
  "diagnosed_family": "F4",
  "broken_invariant": "execution_skeleton_closure_broken",
  "repair_move": "insert readiness gate before dependent action",
  "why_this_move_first": "current failure appears before downstream retries and before broader redesign is justified",
  "validation_check": "verify dependent action is never executed before readiness condition is true",
  "rollback_trigger": "if readiness gate blocks valid execution path or creates new deadlock symptoms",
  "escalate_if": "ordering becomes stable but closure still fails for a deeper reason"
}
````

This is not the only acceptable form.

But this is the right scale.

---

# Example pack 📦

## Example 1 · F1 grounding-first case

### Case summary

The answer cites retrieved material, but the selected chunks do not actually support the final claim.

### Tiny planner output

```json
{
  "case_id": "f1_grounding_recheck",
  "diagnosed_family": "F1",
  "broken_invariant": "anchor_to_claim_coupling_broken",
  "repair_move": "force claim-to-evidence trace before final answer emission",
  "why_this_move_first": "the main break is grounding integrity, so re-linking claims to supporting evidence is the smallest meaningful first repair",
  "validation_check": "sample outputs must show that every major claim can be traced to the cited chunk set",
  "rollback_trigger": "if trace insertion reduces answer quality without improving grounding correctness",
  "escalate_if": "evidence trace is present but semantic target mismatch still dominates"
}
```

### Why this is a good tiny output

This output is good because it does not jump into full retrieval redesign.

It stays focused on the first useful controlled move:

* restore traceability between claim and evidence
* validate whether grounding actually improved
* keep rollback visible if the added constraint harms behavior without fixing the real failure

---

## Example 2 · F4 readiness / ordering case

### Case summary

A downstream action runs before the required resource is ready, causing repeated workflow breakage.

### Tiny planner output

```json
{
  "case_id": "f4_readiness_gate",
  "diagnosed_family": "F4",
  "broken_invariant": "execution_skeleton_closure_broken",
  "repair_move": "insert readiness gate before the dependent action",
  "why_this_move_first": "the visible failure is premature execution, so the first move should repair ordering before deeper architecture changes",
  "validation_check": "dependent action must not fire while readiness state is false",
  "rollback_trigger": "if the new gate blocks valid runs or introduces deadlock-like waiting behavior",
  "escalate_if": "ordering becomes correct but bridge closure still fails later in the path"
}
```

### Why this is a good tiny output

This output is good because it respects execution-first logic.

It does **not** drift into:

* memory blame
* observability essay
* total workflow redesign

It chooses the smallest move that matches the break:

* enforce readiness first
* validate ordering
* watch for deadlock side effects
* escalate only if closure still fails after the visible ordering problem is fixed

---

## Example 3 · F5 observability-first case

### Case summary

A workflow fails intermittently, but logs do not expose where the failure path actually breaks.

### Tiny planner output

```json
{
  "case_id": "f5_trace_exposure",
  "diagnosed_family": "F5",
  "broken_invariant": "failure_path_visibility_broken",
  "repair_move": "add step-level trace markers at each transition boundary",
  "why_this_move_first": "the system is too dark to justify deeper repair, so visibility uplift is the first legitimate move",
  "validation_check": "failed runs must expose the last successful transition and the first missing or broken transition",
  "rollback_trigger": "if trace insertion creates excessive noise without improving path localization",
  "escalate_if": "the failure path becomes visible and a deeper F4 or F6 break becomes primary"
}
```

### Why this is a good tiny output

This output is good because it refuses premature deep repair.

It recognizes that the right first move is:

* expose the path
* improve visibility
* then let later routing decide whether the true deeper family is F4, F6, or something else

That is exactly the kind of planner restraint Auto Repair v1 is supposed to preserve.

---

## Example 4 · F7 representation-first case

### Case summary

The model output looks superficially valid, but required fields appear in unstable locations and break downstream schema parsing.

### Tiny planner output

```json
{
  "case_id": "f7_schema_stabilization",
  "diagnosed_family": "F7",
  "broken_invariant": "representation_container_fidelity_broken",
  "repair_move": "enforce one stable schema shell before field population",
  "why_this_move_first": "the first visible failure is container instability, so carrier repair should come before reasoning or prompt expansion",
  "validation_check": "multiple runs must preserve identical required-field placement and parse successfully",
  "rollback_trigger": "if schema stabilization reduces flexibility but does not improve parse reliability",
  "escalate_if": "container becomes stable but semantic content remains mismatched or incomplete"
}
```

### Why this is a good tiny output

This output is good because it does not confuse:

* structural shell failure
  with
* deeper reasoning failure

The first move is carrier stabilization, which is exactly what a route-sensitive planner should produce here.

---

## Example 5 · F3 continuity-first case

### Case summary

A multi-step agent loses role ownership and continuity across handoff, causing later actions to be applied under the wrong context.

### Tiny planner output

```json
{
  "case_id": "f3_role_reisolation",
  "diagnosed_family": "F3",
  "broken_invariant": "state_continuity_broken",
  "repair_move": "re-isolate role and ownership state at each handoff boundary",
  "why_this_move_first": "the earliest decisive break is continuity drift across handoff, so role fencing is the smallest valid first move",
  "validation_check": "handoff state must preserve the same role and ownership identity across the tested sequence",
  "rollback_trigger": "if isolation fragments valid shared context and causes new task discontinuity",
  "escalate_if": "continuity stabilizes but execution closure still fails in later stages"
}
```

### Why this is a good tiny output

This output is good because it distinguishes continuity repair from execution repair.

It avoids the common failure of treating every multi-step failure as if it were immediately an F4 closure issue.

---

## Example 6 · early escalation case

### Case summary

A case shows mixed pressure, and the first visible local repair may help, but there is a real risk that deeper structural continuation will still be needed.

### Tiny planner output

```json
{
  "case_id": "mixed_case_escalation_ready",
  "diagnosed_family": "F5",
  "broken_invariant": "failure_path_visibility_broken",
  "repair_move": "expose the local failure path before deeper structural intervention",
  "why_this_move_first": "the current evidence is still too thin for a larger repair claim, so visibility is the safest honest first move",
  "validation_check": "local path exposure must clarify whether the deeper break is F4, F6, or unresolved",
  "rollback_trigger": "if local tracing adds cost without clarifying the underlying break",
  "escalate_if": "local visibility improves but the structural failure remains unresolved or keeps recurring"
}
```

### Why this is a good tiny output

This output is good because it leaves room for escalation without being lazy.

It does **not** say:

* “we do not know anything”
* or
* “just escalate immediately”

Instead it says:

* do one useful local move first
* validate whether that move reveals the true deeper structure
* escalate only if the local move is insufficient

That is mature planner behavior.

---

# Contrast examples 🚧

These are not good outputs.
They are here to make the planner standard even clearer.

---

## Bad example 1 · too large

```json
{
  "repair_move": "redesign retrieval, prompt architecture, memory policy, schema layer, and workflow orchestration"
}
```

### Why this is bad

This is not a first move.

It is a vague mini-roadmap pretending to be a planner output.

Tiny planner output should stay small enough that validation and rollback remain believable.

---

## Bad example 2 · no validation

```json
{
  "repair_move": "insert readiness gate",
  "why_this_move_first": "ordering seems wrong"
}
```

### Why this is bad

This is incomplete.

A valid planner output needs at least some explicit sense of:

* how the move will be checked
* when it should be rolled back
* when deeper escalation becomes justified

Without that, it is just a suggestion, not a controlled plan.

---

## Bad example 3 · fake closure

```json
{
  "repair_move": "fix the entire bug",
  "confidence": "high"
}
```

### Why this is bad

This is planner theater.

A first planner layer should not pretend it has solved full closure from one compact output.

That is exactly the kind of overclaim this package is trying to avoid.

---

# What these examples collectively teach 📚

These examples collectively teach six important things.

### 1. Tiny does not mean shallow

A small planner output can still be structurally serious if it includes:

* correct first move
* validation
* rollback
* escalation boundary

### 2. The planner must stay route-sensitive

A good output is different depending on whether the diagnosed break is:

* F1 grounding
* F3 continuity
* F4 closure
* F5 visibility
* F7 representation

That difference is the whole point.

### 3. Validation is part of the plan

If the planner output does not say how improvement will be checked, it is not ready.

### 4. Rollback is part of safety

Even a good first move may still fail locally.

That possibility must remain visible.

### 5. Escalation is not failure

Sometimes the right tiny output is the one that cleanly prepares the case for deeper continuation.

### 6. Restraint is a real capability

A planner that stays modest is usually more useful than one that pretends to be omniscient.

---

## How to use this page in practice 🧠

This page is useful in at least four ways.

### A. As a planner calibration page

Use these examples to compare the actual planner output against the intended output shape.

### B. As a review page

Use this file together with [Planner Review Checklist v1](./planner-review-checklist-v1.md) when checking whether a candidate output is too vague, too large, or too confident.

### C. As a prompt-teaching page

Use these examples to teach an AI system what “small but real” planner behavior looks like.

### D. As a demo support page

These examples are small enough to be shown in a README, slide, or tiny demo pack without overwhelming the reader.

---

## Relationship to the rest of Auto Repair v1 🔗

This file should be read in the correct layer order.

### Structure first

* [Repair Planner Spec v1](./repair-planner-spec-v1.md)
* [Repair Plan Schema v1](./repair-plan-schema-v1.json)

### Example shape next

* this file

### Review and control after that

* [Planner Review Checklist v1](./planner-review-checklist-v1.md)
* [Planner Test Note v1](./planner-test-note-v1.md)
* [Repair Validation Loop v1](./repair-validation-loop-v1.md)
* [Rollback Policy v1](./rollback-policy-v1.md)

This order matters because examples are strongest when the structure behind them is already clear.

---

## Current status 📌

**Tiny Planner Output Examples Pack v1 is now established as the first compact example layer for what a valid small repair-planner output should look like inside Auto Repair v1.**

It does not prove full autonomous repair.

It does prove that the planner layer can now be shown in a compact, teachable, and structurally disciplined form.

---

## Next steps ✨

After this page, most readers continue with:

1. [Open Planner Review Checklist v1](./planner-review-checklist-v1.md)
2. [Open Planner Test Note v1](./planner-test-note-v1.md)
3. [Open Repair Validation Loop v1](./repair-validation-loop-v1.md)
4. [Open Rollback Policy v1](./rollback-policy-v1.md)

If you want the broader Auto Repair surface:

* [Back to Auto Repair README](./README.md)
* [Back to Fixes Hub](../README.md)
* [Back to Atlas landing page](../../../wfgy-ai-problem-map-troubleshooting-atlas.md)

---

## One-line status 🌍

**This file provides the first compact example pack for what small, valid, validation-aware repair-planner outputs should look like in Auto Repair v1.**

---

## Closing note

A planner becomes more trustworthy when it can show its behavior in small form.

Not in giant architecture talk.
Not in fake autonomous drama.
In small form.

That is what this page is for.

It shows that the planner layer can already produce outputs that are:

* small
* controlled
* reviewable
* validation-aware
* rollback-aware
* escalation-ready
