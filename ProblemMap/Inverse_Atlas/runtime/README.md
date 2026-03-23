<!--
AI_NOTE_START

Document role:
This page is the entry page for the runtime folder of the Inverse Atlas MVP.

What this page is for:
1. Explain the role of each runtime artifact in this folder.
2. Explain the intended reading and usage order.
3. Help both humans and AI systems avoid confusing runtime, demo, evaluator, and case-pack roles.
4. Serve as the local navigation page for the runtime layer of Inverse Atlas.

How to use this page:
1. Read this page if you entered the runtime folder directly.
2. Use this page to identify which file should be loaded first and which file should be used for demonstration or evaluation.
3. Use this page together with the higher-level runtime-guide.md page when you need more operating context.
4. If you need the larger conceptual positioning of Inverse Atlas, return to the main README.

Important boundary:
This page documents the current runtime folder of the Inverse Atlas MVP.
It does not claim that the runtime folder alone is the whole architecture.
It also does not claim that the future bridge layer or the full closed-loop WFGY 4.0 system is already complete.

Recommended reading path:
1. ../README.md
2. ../quickstart.md
3. ../runtime-guide.md
4. runtime/README.md
5. inverse-runtime.txt
6. inverse-demo.txt
7. inverse-eval.txt
8. inverse-cases.txt

AI_NOTE_END
-->

# Runtime Artifacts · Inverse Atlas Runtime Folder Guide

> The local entry point for the operational text layer of Inverse Atlas 🛠️

This page explains the four core text artifacts inside the `runtime/` folder.

Each file has a different job.

They are related, but they are **not interchangeable**.

If you only remember one idea from this page, remember this:

- one file defines the law
- one file shows the difference
- one file judges legality
- one file applies pressure

That is the simplest correct model of this folder.

---

## Quick Links 🔎

| Section | Link |
|---|---|
| Inverse Atlas Home | [../README.md](../README.md) |
| Quick Start | [../quickstart.md](../quickstart.md) |
| Runtime Guide | [../runtime-guide.md](../runtime-guide.md) |
| Dual-Layer Positioning | [../dual-layer-positioning.md](../dual-layer-positioning.md) |
| Status and Boundaries | [../status-and-boundaries.md](../status-and-boundaries.md) |
| Forward Atlas | [Problem Map 3.0 Troubleshooting Atlas](../../wfgy-ai-problem-map-troubleshooting-atlas.md) |
| Twin Atlas | [Twin Atlas README](../../Twin_Atlas/README.md) |
| Future bridge | [Atlas Bridge README](../../Atlas_Bridge/README.md) |

---

## What this folder contains 📦

This folder contains the main operational text artifacts of the current Inverse Atlas MVP:

- `inverse-runtime.txt`
- `inverse-demo.txt`
- `inverse-eval.txt`
- `inverse-cases.txt`

These files work together as a compact runtime surface for the current product line.

They support four different functions:

- governance
- demonstration
- evaluation
- stress testing

That is why they are separated into different files instead of being collapsed into one giant prompt.

---

## Which file should be read first 🚀

If you opened this folder and want the shortest correct entry order, use this sequence:

1. read this page
2. load `inverse-runtime.txt`
3. use `inverse-demo.txt`
4. choose one case from `inverse-cases.txt`
5. if needed, evaluate outputs with `inverse-eval.txt`

That is the cleanest beginner order.

If you only want the single most important file in this folder, it is:

**`inverse-runtime.txt`**

That file is the main law of the runtime layer.

---

## File 1 · `inverse-runtime.txt` ⚖️

This is the **main governance artifact**.

It is the most important file in the runtime folder.

Its job is to establish the operating law of Inverse Atlas.

This file should be used when you want the target model to behave under legitimacy-first governance rather than ordinary answer-first generation.

In practical terms, this file is responsible for controlling things like:

- whether the problem is formed well enough
- whether the active frame is legitimate enough
- whether competing routes are still alive
- whether strong resolution is actually authorized
- whether proposed repair is structural or merely cosmetic
- whether visible confidence exceeds lawful support

You should treat this file as:

- the primary runtime layer
- the core behavioral contract
- the most important file in the folder

### Best use
Use this file as the main system prompt, governing layer, or long-form control layer when you actually want to run Inverse Atlas behavior.

### Not for
Do not treat this file as only a summary note or an optional add-on.
Without this file, the rest of the folder loses its central law.

---

## File 2 · `inverse-demo.txt` 🎬

This is the **demonstration harness**.

Its job is to make the difference between normal generation and inverse-governed generation easier to observe quickly.

This file is especially useful when:

- you want a first impression
- you want a short product demonstration
- you want to show someone else what changes
- you want a cleaner baseline vs governed comparison

A good demo pass is not just about style difference.

It should help reveal differences like:

- less premature closure
- less fake certainty
- better unresolved handling
- better distinction between route promise and lawful authorization
- better resistance to cosmetic repair

### Best use
Use this file together with `inverse-runtime.txt` when you want the fastest meaningful experience.

### Not for
Do not treat this file as the main law of the system.
It is the show layer, not the governance core.

---

## File 3 · `inverse-eval.txt` 📏

This is the **evaluator artifact**.

Its role is to judge answers rather than produce the first answer.

That means this file is useful when you already have:

- one candidate answer
- two competing answers
- a baseline answer and an inverse-governed answer
- a strong-looking answer that you suspect may be overclaiming

This file helps ask a harder question:

**does the answer obey the legality logic of Inverse Atlas?**

That may include questions like:

- did it resolve too early
- did it overstate certainty
- did it erase still-live neighboring routes
- did it confuse cosmetic repair with structural repair
- did it exceed the current public confidence ceiling

### Best use
Use this file in a fresh chat or separate evaluation pass after one or more answers already exist.

### Not for
Do not treat this file as the primary runtime layer for ordinary first-answer generation.

---

## File 4 · `inverse-cases.txt` 🔥

This is the **minimal case pack**.

Its purpose is to provide stress fields where the value of Inverse Atlas is easier to see.

Not every prompt is equally useful for testing governance behavior.

If a prompt is too easy, too safe, or too structurally clean, then the difference between a baseline answer and an inverse-governed answer may be too small to notice.

This file exists to increase the chance of exposing failures such as:

- early collapse
- forced confidence
- unresolved route erasure
- fake repair temptation
- illegal specificity

### Best use
Use one case from this file when you want a stronger first demonstration or a more revealing runtime comparison.

### Not for
Do not treat this file as a final benchmark claim by itself.
It is a compact MVP stress field, not a finished universal benchmark suite.

---

## The four files in one glance 👀

If you want the shortest correct summary, use this:

| File | Role | Main question |
|---|---|---|
| `inverse-runtime.txt` | Governance layer | What is lawful to emit? |
| `inverse-demo.txt` | Demonstration layer | Can the governance difference be seen clearly? |
| `inverse-eval.txt` | Evaluation layer | Did the answer obey Inverse Atlas legality? |
| `inverse-cases.txt` | Stress layer | Can the runtime stay lawful under pressure? |

That table is a good fast memory aid.

---

## Recommended usage patterns 🧪

### Pattern 1 · Fast first demo
Use:

- `inverse-runtime.txt`
- `inverse-demo.txt`
- one case from `inverse-cases.txt`

This is the best first-use path.

### Pattern 2 · Real-case runtime test
Use:

- `inverse-runtime.txt`
- your own real prompt or real debugging situation

This is useful when you want to test actual runtime behavior without demo scaffolding.

### Pattern 3 · Output judgment pass
Use:

- `inverse-eval.txt`
- one original prompt
- one or more candidate answers

This is useful when you want explicit legality judgment after outputs already exist.

---

## What this folder is trying to achieve 🧠

This folder is not just a collection of text files.

It is trying to implement a different reasoning order.

A normal model often behaves like this:

1. receive prompt
2. answer fast
3. soften or justify afterward

The runtime layer of Inverse Atlas is trying to impose a different order:

1. check whether the problem is actually constituted
2. check whether the current frame is legitimate
3. estimate resolution risk
4. review neighboring routes
5. authorize or deny resolution level
6. judge repair legality
7. limit public emission to what is lawfully supported

That is why this folder should be understood as an **operating surface**, not just a set of documents.

---

## How this folder relates to the rest of Inverse Atlas 🧭

This runtime folder is the most operational part of the current MVP.

But it is not the whole product line.

The larger Inverse Atlas documentation still matters because it explains:

- what the product is
- why legitimacy-first governance is needed
- how the runtime should be understood conceptually
- where the current boundary of the MVP is
- how this line relates to the forward Atlas
- how the twin-atlas direction is forming

So this folder is the operational core, but not the entire conceptual frame.

---

## How this folder relates to the forward Atlas 🤝

The runtime folder belongs to Inverse Atlas, not to the forward Atlas.

Still, it is useful to understand the compatibility:

- the forward Atlas helps identify likely structural region and likely route
- the Inverse Atlas runtime layer decides whether the system is actually entitled to resolve strongly from there

So if the forward Atlas suggests a plausible region, that suggestion should still be treated here as a **route prior**, not as automatic authorization.

That distinction is one of the most important parts of the larger twin-atlas logic.

---

## Common mistakes to avoid ❗

### Mistake 1
Loading `inverse-demo.txt` but not `inverse-runtime.txt`

The demo can help reveal the difference, but it is not the main law.

### Mistake 2
Using `inverse-eval.txt` as if it were the first-answer runtime

The evaluator judges.
It does not replace the runtime layer.

### Mistake 3
Using only very easy prompts

Easy prompts often hide the value of the framework.

### Mistake 4
Judging success only by tone

A more lawful answer may be shorter, coarser, or visibly unresolved.

### Mistake 5
Assuming the case pack is already a finished benchmark program

It is an MVP stress field, not the final proof of universal superiority.

---

## If you only have one minute ⏱️

Use this path:

1. load `inverse-runtime.txt`
2. paste `inverse-demo.txt`
3. choose one case from `inverse-cases.txt`
4. compare with a plain baseline answer
5. use `inverse-eval.txt` only if you want a stricter judgment pass afterward

That is the shortest correct use of this folder.

---

## Where to go next 📚

If you want the higher-level operational explanation, go to:

[../runtime-guide.md](../runtime-guide.md)

If you want the shortest practical onboarding path, go to:

[../quickstart.md](../quickstart.md)

If you want the larger conceptual relation between the two atlas lines, go to:

[../dual-layer-positioning.md](../dual-layer-positioning.md)

If you want the current truth boundary of the MVP, go to:

[../status-and-boundaries.md](../status-and-boundaries.md)

If you want the route-first side of the family, go to:

[Problem Map 3.0 Troubleshooting Atlas](../../wfgy-ai-problem-map-troubleshooting-atlas.md)

---

## Final note

This runtime folder is small, but it already has internal structure.

It should be understood as a four-part operational layer:

- runtime for law
- demo for visibility
- evaluator for judgment
- cases for pressure

That separation is not clutter.

It is what makes the Inverse Atlas MVP easier to use, easier to explain, and easier to grow. 🌱
