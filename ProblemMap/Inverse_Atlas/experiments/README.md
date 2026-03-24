<!--
AI_NOTE_START

Document role:
This page is the entry page for the experiments layer of the Inverse Atlas MVP.

What this page is for:
1. Explain the purpose of the current experiments layer.
2. Clarify the current MVP reproduction and evaluation philosophy.
3. Summarize the current phase structure and comparison groups.
4. State the current findings carefully without turning early results into oversized claims.

How to use this page:
1. Read this page after the main Inverse Atlas README and versions page.
2. Use this page when you want to understand how the current MVP is being tested.
3. Use this page as the highest-level reference for reproduction, phase design, and current findings.
4. Treat this page as the experiments-layer entry, not as a claim that the full benchmark program is already complete.

Important boundary:
This page describes the current MVP experiments layer of Inverse Atlas.
It should not be used to claim that large-scale external validation is already complete.
It should also not be used to claim that the full Twin Atlas Bridge operating layer is already finalized.

Recommended reading path:
1. Inverse Atlas README
2. versions.md
3. Quick Start
4. Runtime Guide
5. Status and Boundaries
6. Experiments README

AI_NOTE_END
-->

# Experiments · MVP Reproduction, Stress Tests, and Current Findings

> The reproducibility and evaluation layer of the current Inverse Atlas MVP 🧪

This page explains the current experiments layer of Inverse Atlas.

The point of this layer is not to make the project look busy.

Its purpose is much more concrete:

- make the current MVP reproducible
- make the current behavior visible
- make the current claims more honest
- create the seed of a later benchmark family

At this stage, Inverse Atlas is already more than a theory-only artifact.

The current text-based product layer already includes:

- a main runtime artifact
- a 60-second demo entry
- a usable evaluator
- a minimal case pack

That is why an experiments layer now makes sense.  
There is already something real to test, compare, and reproduce.  


---

## Quick Links 🔎

| Section | Link |
|---|---|
| Inverse Atlas Home | [Inverse Atlas README](../README.md) |
| Versions | [Versions](../versions.md) |
| Quick Start | [Quick Start](../quickstart.md) |
| Runtime Guide | [Runtime Guide](../runtime-guide.md) |
| Dual-Layer Positioning | [Dual-Layer Positioning](../dual-layer-positioning.md) |
| Status and Boundaries | [Status and Boundaries](../status-and-boundaries.md) |
| Runtime Layer | [Runtime Artifacts](../runtime/README.md) |
| Paper Notes | [Paper Notes](../paper/README.md) |
| Figure Notes | [Figure Notes](../figures/README.md) |
| WFGY 4.0 Entry | [Twin Atlas](../../Twin_Atlas/README.md) |

---

## What this layer is trying to prove 🎯

The experiments layer is not mainly trying to prove generic answer quality.

It is trying to test whether Inverse Atlas changes the model’s behavior on the failures it was designed to suppress.

The current high-value target failures are:

- illegal resolution escalation
- false completion
- cosmetic repair pretending to be structural
- public overclaim

That means the core question is not:

**did the model sound impressive**

The core question is:

**did the model become more lawful under pressure**

This is why the current experiments layer is centered on legality behavior rather than ordinary answer scoring alone.  


---

## The current MVP experiment philosophy ⚖️

The current experiments layer follows a simple principle:

**test what the framework claims to regulate**

That means the emphasis is on:

- whether the model over-resolves too early
- whether it overstates certainty under weak support
- whether it collapses still-live neighboring routes
- whether it upgrades cosmetic repair into fake structural repair
- whether visible output exceeds the lawful ceiling

This is why the evaluator is legality-centered rather than style-centered, and why pair comparison matters so much in the MVP stage. The evaluator in the current paper is explicitly defined to judge legality rather than rhetorical quality, and its pair mode is designed to compare baseline output and inverse-governed output on legality-oriented dimensions. 

---

## Current experiment structure 📦

At the current stage, the experiments layer is organized around three main phases.

### Smoke Phase
**8 cases**

This is the first standing check.

The purpose of Smoke Phase is simple:

- check whether the artifact is alive
- check whether the runtime visibly changes behavior
- check whether the MVP product surface is already standing up

This phase is not meant to be huge.
It is meant to answer the first important question:

**does the system already feel real enough to test seriously**

### Core Stress Phase
**32 cases**

This is where structural difference starts to matter more clearly.

The purpose of Core Stress Phase is to push the framework into more contested cases where the difference between direct answering and legality-first governance becomes more valuable.

This phase is where you expect clearer separation on:

- route contestability
- false confidence
- fake repair
- pressure toward illegal specificity

### Long-Context Phase
**12 multi-turn cases**

This phase matters because some of the most expensive failures do not appear in one short turn.

They appear when earlier assumptions start to contaminate later reasoning.

This phase is designed to pressure things like:

- contamination
- drift
- provisional statements pretending to become settled evidence
- long-context false completion

That is why this phase is especially important for seeing whether the runtime can remain lawful under multi-turn pressure.  


---

## The current comparison groups 🧩

The current experiments layer is built around three comparison groups.

### A · Baseline
No atlas governance layer.

This is the ordinary direct-answer comparison object.

Its purpose is not to be mocked.
Its purpose is to show what a strong but unguided model tends to do when it is pressured toward early completion.

### B · Inverse Only
Inverse Atlas only.

This group is the cleanest way to test whether the inverse legality gate itself is doing real work.

At the current stage, this is one of the most important groups because it shows whether the inverse layer can already stand as a real product line by itself.

### D · Forward + Inverse
Forward Atlas plus Inverse Atlas.

This is the dual-layer direction.

But there is one critical law here:

**the forward output must remain a weak prior, not an authorization source**

That asymmetry is essential.  
The forward layer may help with structural orientation, but it must not directly override the inverse legality order.  


---

## Why pair comparison matters so much 👀

At the MVP stage, pair comparison is one of the clearest ways to reveal real value.

A baseline answer can look stronger rhetorically while still being less lawful structurally.

That is exactly why pair evaluation exists in the current framework.

The evaluator is designed to compare outputs across legality-oriented dimensions such as:

- problem-frame legality
- world-alignment honesty
- route-judgment plausibility
- neighboring-cut honesty
- resolution legality
- repair legality
- public-ceiling compliance

This means the experiment layer is intentionally closer to:

**lawfulness comparison**

than to:

**who sounds more confident**  


---

## The current 60-second reproduction idea 🚀

The shortest reproduction path is intentionally simple.

At the MVP stage, the idea is:

- open one ordinary chat
- open one chat running an Inverse Atlas version
- ask the same question
- compare the difference

This is useful because it makes the first value of the framework visible without requiring a heavy benchmark stack.

The 60-second entry is already one of the most important product-facing assets of the current line, because it turns a legality framework into something a person can actually feel in one short comparison. The demo harness was explicitly designed to generate a plausible baseline, an inverse-governed pass, and a compact structural difference summary, while rewarding lawful restraint and lawful de-escalation rather than decorative confidence. 

---

## What the current case layer is stressing 🔥

The current case logic is not random.

The paper’s MVP case design already makes clear that the current case pack is meant to stress exactly the kinds of failures central to Inverse Atlas, including:

- topic lure
- thin evidence
- route contestability
- cosmetic repair pressure
- illegal specificity demands
- long-context contamination

The current MVP case set includes eight core case types such as Topic Lure Exact Diagnosis, Thin Evidence Forced Confidence, Cosmetic Repair Bait, Neighboring-Cut Conflict, Long-Context Contamination, Illegal Resolution Demand, False Completion Pressure, and World-Alignment Instability. The paper also explicitly frames this case pack as the seed of a later benchmark family rather than pretending it is already the final benchmark program. 

---

## Current findings, stated carefully ✅

At the current stage, the safest current reading is:

- the Inverse Atlas line already appears to suppress a meaningful class of expensive illegitimate-generation behaviors
- the **B group** already gives evidence that the inverse legality gate itself is doing real work
- the **D group** appears stronger still, but only when the forward layer is treated as weak prior rather than authorization source
- the current results are best understood as **dry-run and MVP-stage findings**, not yet as large-scale external proof

This is a strong statement, but still an honest one.

It matches the current state of the product line well:

- the text-artifact MVP is real
- the experiments layer is real
- the external world-scale validation layer is still ahead  


---

## What this layer already makes possible 🌟

Even at the current stage, this experiments layer already supports several important uses:

- rapid reproduction
- side-by-side baseline comparison
- early benchmark seeding
- Hero Log evidence collection
- product-facing demonstration
- early model-family portability testing

This matters because it means Inverse Atlas is no longer just “a framework that sounds interesting.”

It already has a layer that can be shown, challenged, and rerun.  


---

## What this layer does not yet claim ⛔

This page should not be used to claim that:

- the current experiments already constitute a finished universal benchmark
- the current dry runs already equal large-scale external validation
- every model family has already been systematically compared
- the presence of a stronger D group automatically means the full Bridge layer is already implemented
- the current experiments settle every future WFGY 4.0 claim

The current experiments layer is real.

But it is still an MVP experiments layer.

That distinction should stay visible.

---

## Why this layer matters for the larger architecture 🌌

The experiments layer is valuable not only for Inverse Atlas itself, but also for the broader family.

It creates the first serious place where the architecture can be challenged in operational form.

This matters for later work because the paper already identifies future benchmark expansion axes such as model diversity, task diversity, hybrid evaluation, runtime ablation, and explicit dual-layer evaluation across direct baseline, forward-only, inverse-only, and forward-plus-inverse operation. That means the current experiments layer is not the end of the empirical story, but it is already the correct beginning of it. 

---

## Recommended reading order 📚

If someone is new and wants the cleanest path, use this order:

1. read the [Inverse Atlas README](../README.md)
2. read the [Versions](../versions.md)
3. read the [Quick Start](../quickstart.md)
4. read the [Runtime Guide](../runtime-guide.md)
5. read the [Status and Boundaries](../status-and-boundaries.md)
6. then read this experiments page

If you want the broader family architecture after that, continue to:

[Twin Atlas](../../Twin_Atlas/README.md)

---

## If you need one sentence for outside use 📝

If you want one compact sentence, use this:

> The current Inverse Atlas experiments layer focuses on MVP-stage reproducibility and legality-centered comparison across smoke, stress, and long-context phases, with baseline, inverse-only, and dual-layer group comparisons.

That sentence is short, strong, and still honest.

---

## Final Note

The experiments layer matters because it turns Inverse Atlas from a strong framework into a framework that can already be re-run, challenged, compared, and shown.

That is a real shift.

It means the current project is no longer only a conceptual line or only a runtime artifact.

It already has the beginnings of a real reproducibility surface.

That is what makes this layer important, and that is why it belongs inside the current Inverse Atlas MVP. 🌱
