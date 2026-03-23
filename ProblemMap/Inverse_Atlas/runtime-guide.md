<!--
AI_NOTE_START

Document role:
This page explains how to operate the current Inverse Atlas MVP through its main text artifacts.

What this page is for:
1. Explain the role of the four core runtime artifacts.
2. Explain how they work together.
3. Explain which file to use first, and which file to use next.
4. Help both humans and AI systems understand the intended operating order of the MVP.

How to use this page:
1. Read this page after the main README and quick start page.
2. Use this page when you want to understand the difference between the runtime, demo, evaluator, and case pack.
3. Use this page when you want to run a quick test, a cleaner comparison, or a more formal evaluator pass.
4. If you need the conceptual difference between the forward atlas and Inverse Atlas, read dual-layer-positioning.md next.

Important boundary:
This page documents the MVP text-artifact operating layer of Inverse Atlas.
It does not claim that the full bridge layer or the full WFGY 4.0 closed-loop system is already implemented.

Recommended reading path:
1. README.md
2. quickstart.md
3. runtime-guide.md
4. dual-layer-positioning.md
5. status-and-boundaries.md

AI_NOTE_END
-->

# Inverse Atlas Runtime Guide

> How the current Inverse Atlas MVP works in practice 🛠️

This page explains the **operating roles** of the four core Inverse Atlas text artifacts:

- `inverse-runtime.txt`
- `inverse-demo.txt`
- `inverse-eval.txt`
- `inverse-cases.txt`

These four files are not duplicates.

They are designed to work together as a small but usable MVP operating surface.

In simple terms:

- one file governs
- one file demonstrates
- one file evaluates
- one file stresses the system

That is the core structure of the current runtime layer.

---

## Quick Links 🔎

| Section | Link |
|---|---|
| Inverse Atlas Home | [README.md](./README.md) |
| Quick Start | [quickstart.md](./quickstart.md) |
| Dual-Layer Positioning | [dual-layer-positioning.md](./dual-layer-positioning.md) |
| Status and Boundaries | [status-and-boundaries.md](./status-and-boundaries.md) |
| Runtime folder notes | [runtime/README.md](./runtime/README.md) |
| Forward Atlas | [Problem Map 3.0 Troubleshooting Atlas](../wfgy-ai-problem-map-troubleshooting-atlas.md) |
| Twin Atlas | [Twin Atlas README](../Twin_Atlas/README.md) |
| Future bridge | [Atlas Bridge README](../Atlas_Bridge/README.md) |

---

## The core idea of the runtime layer ⚖️

The Inverse Atlas runtime layer exists to enforce a different order of cognition.

A normal model often moves like this:

1. see prompt
2. generate answer
3. justify or soften afterward

The Inverse Atlas runtime layer is designed to change that order.

Its intended order is:

1. constitute the problem
2. check whether the active frame is legitimate
3. estimate structural risk
4. review competing cuts
5. authorize or deny resolution level
6. judge repair legality if repair is proposed
7. clamp public output below the lawful ceiling

That is why the runtime layer should be understood as **pre-generative governance**, not as a cosmetic answer style.

---

## The four main artifacts 🧩

### `inverse-runtime.txt`
This is the **main governance artifact**.

It defines the runtime law of the system.

Its job is not to answer the user directly.  
Its job is to control whether answering is lawful, how strong the answer may be, and which mode the answer should stay in.

This is the file that carries the core shift:

**generation is not a default right**  
**generation is an authorized act**

You should treat this file as the main operating layer of the MVP.

Use it when you want the target model to actually run under Inverse Atlas behavior.

---

### `inverse-demo.txt`
This is the **demonstration harness**.

Its role is to make the system easier to feel quickly.

Instead of only producing one answer, it typically frames the interaction so that you can compare:

- a plausible unguided baseline
- an inverse-governed answer
- a compact structural difference summary

This file is especially useful for:

- the first 60-second experience
- showing the product to another person
- making the difference visible without requiring a full benchmark setup

Use it when you want the system to **show the runtime difference clearly**.

---

### `inverse-eval.txt`
This is the **evaluator artifact**.

Its role is not to generate the first answer.

Its role is to judge whether a candidate answer obeys the legality logic of Inverse Atlas.

That means this file is useful when:

- you already have one answer
- you already have two answers and want pair comparison
- you want to check whether a strong-looking answer is actually overclaiming
- you want a more explicit legality judgment

Use it when you want the system to **judge answers**, not merely produce them.

---

### `inverse-cases.txt`
This is the **minimal case pack**.

Its role is to provide prompts or cases that make the value of Inverse Atlas easier to observe.

These cases are useful because not every prompt reveals the difference clearly.

If the prompt is too easy, too safe, or too structurally clean, the baseline and inverse-governed outputs may look too similar.

The case pack is meant to increase the chance that you will see:

- premature closure
- forced confidence
- unresolved neighboring routes
- fake repair
- over-strong public emission

Use it when you want a cleaner stress field for the MVP.

---

## What each file is for, in one sentence 📝

If you only remember one line for each file, remember this:

- `inverse-runtime.txt` = the main law
- `inverse-demo.txt` = the fastest demonstration
- `inverse-eval.txt` = the legality judge
- `inverse-cases.txt` = the stress test field

That is the shortest correct mental model.

---

## The recommended operating order 🚀

If you are new to the system, use this order:

### Step 1
Load `inverse-runtime.txt`

This establishes the governance layer.

### Step 2
Use `inverse-demo.txt`

This makes the behavior easier to compare and inspect.

### Step 3
Choose one case from `inverse-cases.txt`

This gives the runtime a better chance to reveal its difference.

### Step 4
If needed, run `inverse-eval.txt` in a separate chat

This lets you judge whether the answer actually obeyed Inverse Atlas legality logic.

That is the cleanest first-use flow.

---

## The three main usage patterns 🧪

The MVP currently supports three practical usage patterns.

### Pattern 1. Demo-first usage
This is the easiest path.

Use:

- `inverse-runtime.txt`
- `inverse-demo.txt`
- one case from `inverse-cases.txt`

This pattern is best when:

- you want the fastest experience
- you want to show the product to someone else
- you want a visible baseline vs governed difference quickly

This is the default beginner path.

---

### Pattern 2. Direct runtime usage
This is the most straightforward operational path.

Use:

- `inverse-runtime.txt`
- your own real prompt or real debugging situation

This pattern is best when:

- you already know what you want to test
- you want to see how the runtime behaves in a real case
- you do not need the demo scaffolding every time

This is the path closest to actual runtime use.

---

### Pattern 3. Evaluator usage
This is the judgment path.

Use:

- `inverse-eval.txt`
- the original input
- one candidate answer, or two competing answers

This pattern is best when:

- you already have outputs
- you want to compare a baseline answer against an inverse-governed answer
- you want a more explicit legality verdict

This path is especially useful for cleaner comparisons.

---

## What `inverse-runtime.txt` is expected to control 🧠

At the MVP level, the runtime is expected to control at least these things:

### 1. Problem constitution
The runtime should not let the model jump to refined answers before a minimal lawful problem frame exists.

### 2. World legitimacy
The runtime should reduce resolution when evidence, target binding, or frame legitimacy is weak.

### 3. Competing route discipline
The runtime should not let one plausible route silently erase neighboring live routes.

### 4. Resolution authorization
The runtime should keep the answer inside a lawful state, such as STOP, COARSE, UNRESOLVED, or AUTHORIZED.

### 5. Repair legality
If a fix is proposed, the runtime should distinguish structural repair from cosmetic repair.

### 6. Public ceiling control
The runtime should not let visible certainty exceed earned support.

This is why the runtime layer is the most important artifact in the set.

---

## What `inverse-demo.txt` is expected to reveal 👀

The demo artifact is expected to reveal **difference in behavior**, not just difference in length.

A good demo pass often reveals one or more of these differences:

- baseline closes too early
- baseline speaks too confidently
- baseline skips competing-route review
- baseline presents cosmetic repair as if structural
- inverse-governed output remains coarse or unresolved lawfully
- inverse-governed output controls confidence better
- inverse-governed output separates route promise from actual authorization

If the demo only makes one answer longer and the other shorter, that is not yet a very meaningful result.

The meaningful result is a **change in governance behavior**.

---

## What `inverse-eval.txt` is expected to judge 📏

The evaluator artifact is expected to judge legality under the Inverse Atlas framework.

That usually means judging questions like:

- did the answer resolve too early
- did it overclaim certainty
- did it separate neighboring routes well enough
- did it label cosmetic repair as structural
- did its visible output exceed the current support ceiling

This is why evaluator usage is important.

Without evaluator discipline, some outputs may look impressive only because they are fluent.

The evaluator helps ask a harder question:

**was the output actually lawful under the current structure?**

---

## What `inverse-cases.txt` is expected to stress 🔥

The case pack should not be treated as a random prompt list.

Its role is to provoke the exact kinds of situations where Inverse Atlas matters most.

That includes cases involving:

- lexical lure
- forced confidence
- weak grounding
- unresolved neighboring cuts
- fake repair temptation
- pressure toward illegal specificity

So when you use the case pack, you are not simply “trying examples.”

You are testing whether the runtime can remain lawful under pressure.

---

## How the artifacts work together 🤝

The four artifacts form a small operating loop.

### Runtime
Defines the law.

### Demo
Makes the law visible.

### Cases
Apply pressure to the law.

### Evaluator
Judges whether the law was actually obeyed.

That is the cleanest way to understand the MVP as a whole.

The files are separate because they do different jobs.  
Keeping them separate makes the system easier to inspect, compare, and improve.

---

## Forward Atlas compatibility 🧭

Inverse Atlas does not require the forward atlas in order to function.

It can run as its own product line.

But it is also designed to remain compatible with the route-first world of the forward atlas.

That means if a forward atlas or troubleshooting layer already suggests:

- likely route
- likely family
- likely invariant region

Inverse Atlas should treat those as **weak priors**, not final authorization.

This distinction matters.

A route hint is not the same thing as lawful resolution.

So in the twin-atlas direction:

- the forward atlas suggests where failure may be
- Inverse Atlas decides whether the system is entitled to speak strongly from there

This is one reason the pairing is so powerful.

---

## Common misuse patterns to avoid ❗

### Misuse 1
Using only `inverse-demo.txt` without the runtime layer.

The demo is not the main law.  
It is the demonstration scaffold.

### Misuse 2
Treating `inverse-eval.txt` as the first-answer runtime.

The evaluator is for judgment, not the main operating law.

### Misuse 3
Using very easy prompts and concluding that the runtime changes nothing.

Easy prompts often do not expose the value of the framework clearly.

### Misuse 4
Judging success by tone alone.

A more lawful answer may be shorter, more coarse, or more visibly unresolved.

That is not failure.

### Misuse 5
Treating the case pack as a benchmark claim by itself.

The case pack is a stress field for the MVP, not a full external benchmark program.

---

## A simple beginner recipe 🌟

If someone asks, “What is the simplest correct way to use this MVP?”, the answer is:

1. read the main [README.md](./README.md)
2. load `inverse-runtime.txt`
3. paste `inverse-demo.txt`
4. choose one case from `inverse-cases.txt`
5. compare with a normal baseline answer
6. if needed, run `inverse-eval.txt` in a separate chat

That is the cleanest minimal recipe.

---

## A simple advanced recipe 🧪

If someone already has real outputs and wants a stricter comparison, use this:

1. prepare one original prompt
2. generate one normal baseline answer
3. generate one inverse-governed answer
4. open a fresh evaluator chat
5. load `inverse-eval.txt`
6. compare the two answers against the same original prompt

This gives a better sense of legality difference than casual impression alone.

---

## What this page does not try to do ⛔

This page does not attempt to:

- reproduce the full paper
- define the full bridge logic
- explain the entire twin-atlas architecture
- claim universal benchmark superiority
- replace the conceptual positioning pages

This page is narrower.

Its job is to explain **how the current runtime artifacts are meant to work together**.

That focus should be preserved.

---

## Where to go next 📚

If you want the conceptual difference between route-first and legitimacy-first reasoning, go next to:

[Dual-Layer Positioning](./dual-layer-positioning.md)

If you want the current claim boundary and MVP honesty layer, go next to:

[Status and Boundaries](./status-and-boundaries.md)

If you want the route-first atlas page itself, go to:

[Problem Map 3.0 Troubleshooting Atlas](../wfgy-ai-problem-map-troubleshooting-atlas.md)

If you want the larger paired framing, go to:

[Twin Atlas README](../Twin_Atlas/README.md)

---

## Final note

The current runtime layer is small, but it is already structured.

It is not just one prompt.

It is a four-part MVP operating surface:

- runtime for law
- demo for visibility
- evaluator for judgment
- cases for pressure

That structure is what makes the Inverse Atlas MVP usable, teachable, and expandable.
