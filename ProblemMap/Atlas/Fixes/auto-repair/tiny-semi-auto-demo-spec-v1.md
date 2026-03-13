# Tiny Semi-Auto Demo Spec v1

## 0. Document status

This document defines the first tiny semi-auto demo specification for the Atlas Auto Repair layer.

Its purpose is practical:

> show how a very small, controlled, semi-auto repair flow should work
> without pretending that full autonomous repair already exists.

This file does **not** define a production repair engine.

It defines something much narrower and safer:

> a first demo-ready specification for local, inspectable, reversible,
> validation-aware semi-auto repair behavior.

This document should be read together with:

- `README.md`
- `auto-repair-architecture-v1.md`
- `repair-action-schema-v1.md`
- `repair-validation-loop-v1.md`
- `rollback-policy-v1.md`
- `auto-repair-roadmap-v1.md`
- `repair-planner-spec-v1.md`
- `repair-planner-prompt-v1.md`
- `repair-plan-schema-v1.json`
- `semi-auto-repair-scope-v1.md`
- `safe-early-action-catalog-v1.md`
- `tiny-validation-examples-pack-v1.md`
- `tiny-rollback-examples-pack-v1.md`
- `planner-test-note-v1.md`
- `planner-review-checklist-v1.md`
- `tiny-planner-output-examples-pack-v1.md`

---

## 1. Why this spec exists

The Auto Repair layer already has:

- architecture
- repair action schema
- validation logic
- rollback logic
- planner logic
- early action catalog
- tiny validation examples
- tiny rollback examples
- planner review examples

But there is still a missing bridge between:

- planner output
- and
- visible semi-auto repair behavior

This spec fills that gap.

It defines how a tiny semi-auto demo should be structured so that the system can demonstrate:

1. routed input
2. planner output
3. one bounded action
4. one validation result
5. one final outcome

In short:

> this is the first small demo contract for semi-auto repair.

---

## 2. What this demo is supposed to prove

This demo is not trying to prove:

- full repair autonomy
- large-scale benchmark performance
- deep cross-family repair orchestration
- high-risk intervention capability

It is only trying to prove that:

1. a routed case can produce a small repair plan
2. one safe early action can be selected
3. that action can be applied in a narrow controlled way
4. the result can be validated
5. the workflow can end in accept, revise, rollback, or escalate

That is enough for a first credible semi-auto repair demo.

---

## 3. Core demo principle

The tiny semi-auto demo must remain:

- local
- auditable
- replayable
- validation-aware
- rollback-aware

The demo must never feel like:

- magic repair
- speculative self-editing
- broad hidden system mutation
- fake success by presentation only

The point is not to look omnipotent.

The point is to show a trustworthy micro-workflow.

---

## 4. Recommended demo families

The first tiny semi-auto demos should come from the safest early family set.

### Best first targets

- F1
- F4
- F7

### Why these families

They are the best first targets because their actions are usually:

- narrow
- easy to inspect
- easy to validate
- easier to rollback
- easier to explain in public demos

### Avoid as first semi-auto demo

- F6-heavy intervention
- broad multi-family ambiguity
- high-abstraction legitimacy cases
- large continuity mutation cases

Those are better left for later stages.

---

## 5. Minimal demo workflow

The smallest acceptable semi-auto demo workflow is:

```text
case
→ atlas route already available
→ repair planner output
→ select one safe early action
→ apply one bounded local change
→ validate local effect
→ choose final outcome
````

The final outcome must be one of:

* `accept`
* `revise`
* `rollback`
* `escalate`

If the demo does not reach one of these outcomes explicitly, it is incomplete.

---

## 6. Required demo blocks

Each tiny semi-auto demo should contain the following blocks.

### Block A · Case input

The demo must start from a routed case.

Minimum case elements:

* case description
* primary family
* broken invariant
* best current fit
* fix surface direction
* confidence
* evidence sufficiency

The demo should not spend most of its time re-explaining routing.
Routing is assumed as input.

---

### Block B · Planner output

The demo must show a compact planner output object.

Minimum required planner fields:

* selected repair family
* plan scope
* candidate action
* primary validation target
* misrepair risk
* recommended next step

The planner output should be shown explicitly, not only described in prose.

---

### Block C · Selected semi-auto action

The demo must choose one action from the planner result.

The chosen action should be:

* in-scope
* local
* reversible
* validation-ready

Only one action should be applied in the smallest v1 demo.

This keeps the demo honest and easy to inspect.

---

### Block D · Before state

The demo must show a small, explicit before state.

Examples:

* wrong evidence set
* missing readiness gate
* invalid JSON shell

This before state should be local and concrete.

---

### Block E · After state

The demo must show the after state produced by the bounded action.

Examples:

* corrected evidence set
* inserted readiness gate
* repaired output shell

The after state must remain local.
It should not claim broad unseen system repair.

---

### Block F · Validation result

The demo must show a compact validation result.

Minimum fields:

* validation target
* before summary
* after summary
* improvement detected
* collateral damage detected
* recommended outcome

This is the heart of the demo.

Without this block, the demo is only action theatre.

---

### Block G · Final outcome

The demo must end with one explicit verdict:

* `accept`
* `revise`
* `rollback`
* `escalate`

That outcome must be justified by the validation result.

---

## 7. Required safety rules

Every tiny semi-auto demo in v1 should obey these safety rules.

### Rule 1

One action only.

Do not stack multiple actions in the first demo layer.

### Rule 2

No hidden mutation.

Every relevant change should be visible in the demo.

### Rule 3

Validation is mandatory.

The demo must not end at “action applied.”

### Rule 4

Rollback must remain possible.

Even if rollback is not triggered in a given demo, the restore point should still be clear.

### Rule 5

No fake full repair claims.

The demo should show a local gain, not a myth of total closure.

### Rule 6

Weak evidence means narrower scope.

The demo must not become more aggressive when confidence is low.

---

## 8. Recommended demo variants

The strongest first spec includes three small variants.

### Variant A · Accept path

The action works well enough.
Validation detects improvement.
The outcome is `accept`.

This is the cleanest first demo type.

### Variant B · Revise path

The action improves one dimension but leaves important pressure unresolved.
The outcome is `revise`.

This is useful for showing that the system is not naive.

### Variant C · Rollback path

The action causes stronger collateral damage than local gain.
The outcome is `rollback`.

This is useful for showing that the system is disciplined and reversible.

These three variants together already make the semi-auto layer look much more real.

---

## 9. Recommended first demo candidates

### F1 candidate

Use:

* `F1_RG_001` Re-ground evidence set

Why strong:

* before and after are easy to compare
* anchor alignment is a clean validation target
* rollback is simple

Expected likely outcome:

* `accept`

---

### F4 candidate

Use:

* `F4_GT_001` Insert readiness gate

Why strong:

* workflow before/after is visible
* closure is easy to explain
* rollback is understandable

Expected likely outcome:

* `accept` or `revise`

---

### F7 candidate

Use:

* `F7_SC_001` Tighten output schema

Why strong:

* shell validity is visible
* downstream usability is easy to explain
* false success risk is also teachable

Expected likely outcome:

* `accept` or `revise`

---

## 10. Suggested demo object format

A tiny semi-auto demo object should ideally contain:

### Required fields

* `demo_id`
* `family`
* `case_summary`
* `planner_output`
* `selected_action`
* `before_state`
* `after_state`
* `validation_result`
* `final_outcome`

### Optional but useful fields

* `rollback_ready`
* `restore_point`
* `why_this_demo_matters`
* `notes`

This format is enough for:

* markdown demos
* JSON demos
* notebook demos
* replay demos

---

## 11. Example tiny demo outline

### Example

F4 semi-auto demo outline

```json
{
  "demo_id": "TSAD_F4_001",
  "family": "F4",
  "case_summary": "A downstream step executes before approval and readiness are complete.",
  "planner_output": {
    "selected_repair_family": "F4",
    "plan_scope": "constrained",
    "candidate_actions": [
      {
        "action_id": "F4_GT_001",
        "action_title": "Insert readiness gate"
      }
    ],
    "primary_validation_target": "readiness state",
    "misrepair_risk": "may over-block valid progress",
    "recommended_next_step": "validate-first-action"
  },
  "selected_action": {
    "action_id": "F4_GT_001",
    "action_title": "Insert readiness gate"
  },
  "before_state": "Downstream send path executes while approval is still incomplete.",
  "after_state": "Downstream send path is blocked until readiness is satisfied.",
  "validation_result": {
    "validation_target": "readiness state",
    "improvement_detected": true,
    "collateral_damage_detected": false,
    "recommended_outcome": "accept"
  },
  "final_outcome": "accept",
  "rollback_ready": true,
  "restore_point": "previous workflow gate configuration"
}
```

This is the kind of compact demo object that v1 should aim for.

---

## 12. What counts as a good tiny semi-auto demo

A good demo should make it easy to see:

* what the problem was
* what action was chosen
* what changed
* what was validated
* why the final outcome makes sense

A good demo should not require a long explanation to defend itself.

The clarity should come from the structure.

---

## 13. What counts as a weak tiny semi-auto demo

A weak demo usually has one or more of these problems:

* too many actions
* unclear before state
* unclear after state
* no validation block
* no final outcome
* no rollback path
* broad hidden intervention
* vague planner output
* fake success language

This spec exists partly to prevent those problems.

---

## 14. What this spec does not yet include

Tiny Semi-Auto Demo Spec v1 does **not** yet include:

* full notebook implementation
* full replay/live infrastructure
* multi-step repair loops
* family-wide demo coverage
* benchmark automation
* dynamic repair action selection code

Those can come later.

This file only defines the first clean demo specification.

---

## 15. Recommended next step

Once this spec exists, the next useful follow-up is probably one of these:

1. create `tiny-semi-auto-demo-pack-v1.md`
2. create one small JSON demo pack for F1 / F4 / F7
3. create one notebook-oriented replay spec for a tiny semi-auto case

The strongest immediate next step is probably:

> create a tiny semi-auto demo pack with 2 to 3 compact cases.

That would turn this spec into something even more visibly usable.

---

## 16. One-line summary

**Tiny Semi-Auto Demo Spec v1 defines how a first local, validation-aware, rollback-aware semi-auto repair demo should be structured for Atlas-based Auto Repair.**

