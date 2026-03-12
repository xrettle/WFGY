<!--
AI_NOTE_START

Document role:
This file is the README for Demo 2 of the official flagship demo pack.

How to use this file:
1. Read this file before opening the notebook.
2. Treat this demo as the flagship proof that some failures must be repaired through observability first, not through direct answer fixing first.
3. Use this file to understand:
   - why this case belongs to F5
   - why it is not primarily F4 or F6
   - what the first repair move is
   - what replay mode and live rerun mode each prove
4. Read together with:
   - [Atlas Final Freeze v1](../../../../atlas-final-freeze-v1.md)
   - [Canonical Casebook v1](../../../../canonical-casebook-v1.md)
   - [Family Fix Surface v1](../../family-fix-surface-v1.md)
   - [Atlas to WFGY Bridge v1](../../atlas-to-wfgy-bridge-v1.md)
   - [Misrepair Patterns v1](../../misrepair-patterns-v1.md)

What this file is:
- The official README for Demo 2
- A proof-of-use page for observability-first repair
- A teaching page for F5 diagnosability failures

What this file is not:
- Not the atlas core
- Not the full fix manual
- Not a giant tracing benchmark
- Not proof that all invisible failures belong to F5

Reading discipline for AI:
- Preserve the distinction between diagnosability failure, execution failure, and boundary failure.
- Do not collapse this case into generic “the system is buggy” language.
- Do not treat replay mode as weaker than live rerun mode.
- Route first, then repair.

AI_NOTE_END
-->

# Demo 2 · F5 Observability First 🔍

## Problem Map 3.0 Troubleshooting Atlas
## Official flagship demo for diagnosability-first repair

This is the second flagship demo in the official runnable demo pack.

It was chosen because many real systems fail in a painful but very common way:

> something is clearly going wrong  
> but the system still does not expose enough structure for a correct first repair

This demo is designed to make that situation visible.

It shows that once a case is routed as **F5 Observability & Diagnosability Integrity**, the first repair move changes from premature system intervention to explicit visibility uplift.

---

## 1. What this demo proves 🧪

This demo proves four things.

### A. Some failures are blocked by invisibility before they are blocked by intelligence

A system can fail in a way that tempts people to say:

- the workflow is broken
- the model is confused
- the chain is unstable
- the safety layer is weak

Sometimes those statements may later become true.

But the first practical problem is still:

- the failure path is not exposed
- the trace is too thin
- the relevant signals are hidden
- the system cannot yet be audited clearly enough

That is an F5-style first cut.

### B. The correct route changes the first repair move

If the case is routed correctly into **F5**, the first repair move becomes:

- observability insertion
- trace exposure
- logging uplift
- warning surface improvement
- diagnostic visibility recovery

This is different from trying to fix the workflow logic, prompt logic, or policy logic too early.

### C. Replay mode is enough to teach the pattern

A user should be able to understand this demo without executing anything.

The replay artifacts should make clear that the first breakthrough is not “the answer got better.”
The first breakthrough is “the failure became legible.”

### D. Live rerun remains optional but useful

If the user wants to reproduce the same pattern with a live trace or model-assisted workflow, live mode can be used.

But the core lesson of the demo must remain understandable even without execution.

---

## 2. Family route 🧭

### Primary family

**F5 · Observability & Diagnosability Integrity**

### Secondary family

**F4 · Execution & Contract Integrity**

### Outer pressure

Possible secondary or later pressure may also point toward **F6** in some variants, but not in the flagship teaching version.

### Why F5 is primary

The main failure is that the system still cannot stably expose enough structure to diagnose the problem correctly.

The workflow may indeed be broken.
A boundary may later prove to be drifting.
But the first broken invariant is still:

> the failure path cannot yet be seen, traced, or audited well enough

### Short routing statement

- the system is failing
- the path of failure is still opaque
- diagnosability fails before deeper repair can become reliable

### Best current fit

**F5_N01 Failure Path Opacity**

In stronger warning-oriented variants this may move toward:

**F5_E02 Early Warning Deficit**

But the flagship teaching version should remain centered on failure-path opacity.

---

## 3. Why not neighbor ❌

The main tempting neighboring cut is **F4**.

That temptation is reasonable because many systems that lack observability are in fact also suffering from execution closure failure, weak liveness, or broken bridges.

But this demo is not primarily about closure failure yet.

It is primarily about this:

> the system still does not expose enough structure for the operator to know what to repair first

That means the first broken layer is diagnosability, not execution closure.

### Wrong cut

- “this is mainly a workflow execution bug”

### Better cut

- “this is a diagnosability-first case with possible execution pressure behind it”

That distinction matters because the first repair move changes immediately.

If you cut too early to F4, you are likely to start rebuilding the machine before you can even see the broken path.

---

## 4. Baseline failure 🧱

The baseline case should be intentionally realistic, but still easy to inspect.

### Core pattern

A small workflow, agent chain, or tool-calling loop produces a bad or unstable result.

The operator can observe that:

- the result is wrong
- the process seems unreliable
- something is clearly off

But the system does not yet provide enough of the following:

- clear step traces
- output lineage
- stage-level visibility
- branch decisions
- failure checkpoints
- useful logging context

So the operator is left with the most frustrating state:

> I know something is wrong, but I cannot yet see the right thing to repair

### What the baseline should make visible

The user should be able to see:

1. the workflow input
2. the baseline result
3. the lack of useful trace structure
4. the diagnostic ambiguity that follows
5. the repair temptation toward the wrong layer

### Important design note

Do not make the baseline too theatrical.

This should feel like a familiar engineering pain, not like a made-up disaster movie.

---

## 5. First repair move 🔧

Once the case is routed to F5, the first repair move should be simple and disciplined.

### Recommended first repair stack

1. **observability insertion**  
   Add explicit visibility to the relevant pipeline stages.

2. **trace exposure**  
   Surface the path from input to intermediate state to output.

3. **diagnostic logging uplift**  
   Add the minimum trace needed to tell where the failure shape begins.

4. **failure-surface clarification**  
   Separate what is visible from what is still inferred.

5. **only then consider deeper family repair**  
   After visibility improves, reassess whether the real downstream repair belongs to F4, F6, F1, or elsewhere.

### What should not happen first

Do **not** start with:

- large workflow rewrites
- broad prompt overhauls
- aggressive policy changes
- random retry loops
- “let’s just upgrade the model” reactions

Those may create movement, but they do not solve the first problem if the failure path is still hidden.

### First repair principle

> if the system is still opaque, expose the failure path first

That is the teaching core of this demo.

---

## 6. Optional WFGY 3.0 escalation 🌊

This demo can teach its lesson without deeper escalation.

But if the user wants to explore a stronger structural diagnosis path, this is where WFGY 3.0 becomes useful.

### When escalation makes sense

Escalate beyond the simple first repair move if:

- the workflow becomes visible but still remains unstable
- the system exposes traces but they are too noisy to interpret
- the warning surface appears late and inconsistently
- there are repeated hidden transitions or collapse regions
- the team needs a deeper failure grammar, not just better logs

### What WFGY 3.0 can add

A WFGY 3.0 handoff can help explore:

- stronger failure-structure interpretation
- layered warning-surface analysis
- deeper collapse signatures
- stress-path variants
- experimental observability regimes
- routing-sensitive escalation patterns

### Correct relationship

The right order remains:

1. atlas route
2. first observability repair
3. reassess the case
4. escalate into deeper WFGY exploration if needed

The atlas is still the router.
WFGY 3.0 is the deeper experimental engine.

---

## 7. Replay mode ▶️

Replay mode is the default public reading mode.

It should require no API key and no notebook execution.

### Replay mode should show

- the workflow or case setup
- the baseline result
- the thin or missing trace structure
- the family route
- the why-primary-not-secondary statement
- the broken invariant
- the first repair move
- the replayed improved visibility state
- a short note on what new things became visible

### What replay mode proves

Replay mode proves that:

- diagnosability-first routing is understandable
- the repair move is visibly different
- the result shift can be measured in legibility, not only in output quality
- a demo can teach through structure, not only through live execution

### Why replay mode matters

This is one of the demos where replay mode is especially important.

The reader should be able to feel the pain of opacity and the relief of visibility just from the replay artifacts.

If that feeling is not there, the demo is weak.

---

## 8. Live rerun mode ⚙️

Live rerun mode is optional.

It exists for users who want to reproduce the same pattern with live execution, traces, or model-assisted steps.

### Live rerun should do

- load the case
- show the baseline workflow state
- show what trace information is missing
- apply the observability-first repair move
- produce a more legible trace or debug path
- compare before and after at the diagnosability layer

### Live rerun should not pretend to do

- universal tracing coverage
- full-scale observability engineering
- final architectural closure
- full production-grade telemetry design

It is a reproduction layer, not a full platform.

### Live rerun design rule

If a more realistic trace makes the notebook harder to understand, clarity should win.

This demo is teaching a first repair move, not simulating an entire infra team.

---

## 9. API key note 🔐

Some live variants may require an API key.

If so, the rule stays the same:

- no hard-coded keys
- no saved secrets in the repository
- key entry happens only at run time
- replay mode remains readable without any secret

### Important note for users

This demo is meant for **understanding and reproduction**.

You do **not** need to run the notebook in order to understand the point.

A strong observability demo should still teach through:

- README
- fixtures
- replay outputs
- before / after visibility comparison

The live rerun is optional.

---

## 10. Files in this folder 📂

This demo folder should contain the following assets.

### Required

- `README.md`
- `input_case.json`
- `replay_outputs.json`
- `expected_output.json`

### Recommended

- `demo_f5_observability.ipynb`
- optional prompt or trace notes
- optional helper references from the shared folder

### File roles

#### `input_case.json`
Contains the workflow case, visible artifacts, and missing-diagnosability context.

#### `replay_outputs.json`
Contains the baseline state, route explanation, first repair move, and replayed improved visibility state.

#### `expected_output.json`
Contains the clean target structure for what the demo is trying to make visible.

#### notebook
Contains the optional live reproduction flow.

---

## 11. Expected outcome ✅

If the demo works, the user should walk away with the following understanding:

1. the workflow was failing in a way that was initially hard to diagnose
2. the atlas routed the case to F5, not directly to F4
3. the first repair move was observability insertion, not workflow redesign
4. after visibility improved, the real shape of the failure became more legible

The demo does **not** need to solve everything.

It only needs to make the first correct move visibly different.

That is enough.

---

## 12. Limits of this demo 🧱

This demo has real limits, and those limits should be stated clearly.

### It does not prove

- that every hidden failure belongs to F5
- that all workflow bugs are really diagnosability issues
- that logging alone solves structural failure
- that visibility replaces deeper repair
- that this single example covers all observability systems

### It does prove

- that some failures should be repaired through observability first
- that route-first repair changes what the operator does next
- that diagnosability can itself be a first-class repair target

These are already strong claims.
There is no need to inflate them.

---

## 13. Community extension ideas 🌱

This demo is also a seed template for future community work.

Possible extensions include:

- adding different workflow types
- adding tool-calling traces
- comparing low-trace and high-trace versions
- testing different visibility surfaces
- connecting warning delay to deeper boundary drift
- extending the case into a stronger F5 to F6 escalation example

### Community boundary rule

Contributors should preserve the official logic:

- route first
- explain why primary not secondary
- show the first repair move
- keep replay outputs understandable
- do not turn the demo into a giant tracing jungle

For contribution structure, see:

- [Community Fix Lab](../../community/README.md)
- [Contribution Checklist](../../templates/contribution-checklist.md)
- [Fix Recipe Template](../../templates/fix-recipe-template.md)

---

## Short summary

This demo teaches one clean lesson:

> if the system is still too opaque to diagnose correctly, repair visibility first

That is why this is the second flagship demo.

---

## One-line version

**Demo 2 shows that some failures should be repaired through observability first, and that correct routing changes the first repair move from premature system intervention to explicit failure-path exposure.**

---

## Closing note ✨

This demo is intentionally focused.

Its job is not to simulate every tracing platform.
Its job is to make one key pattern obvious:

- the system is failing
- the failure path is still hidden
- visibility becomes the first repair target

If that becomes clear, the atlas has already done something powerful.
