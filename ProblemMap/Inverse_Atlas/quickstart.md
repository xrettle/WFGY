<!--
AI_NOTE_START

Document role:
This page is the fastest onboarding page for the Inverse Atlas MVP.

What this page is for:
1. Help a user try Inverse Atlas quickly.
2. Show the minimum path for comparing baseline output and inverse-governed output.
3. Explain the shortest evaluation loop without requiring the full paper first.
4. Serve as the practical companion to the main Inverse Atlas README.

How to use this page:
1. Read this page after the main Inverse Atlas README.
2. Follow one of the quick paths depending on whether you want a very short demo, a pair comparison, or an evaluator pass.
3. If you need deeper conceptual positioning, read dual-layer-positioning.md next.
4. If you need operational detail on the four main text artifacts, read runtime-guide.md.

Important boundary:
This page is written for MVP usage.
It is meant to help users try the current text-artifact version of Inverse Atlas quickly.
It does not claim that the full bridge layer or the full closed-loop WFGY 4.0 architecture is already complete.

Recommended reading path:
1. README.md
2. quickstart.md
3. runtime-guide.md
4. dual-layer-positioning.md
5. status-and-boundaries.md

AI_NOTE_END
-->

# Inverse Atlas Quick Start

> The shortest path to experiencing legitimacy-first AI governance ⚖️

This page is for one simple goal:

**help you try the current Inverse Atlas MVP quickly, without needing to read everything first**

If you only want the fastest practical route, start with the **60-second experience** below.

---

## Quick Links 🔎

| Section | Link |
|---|---|
| Inverse Atlas Home | [README.md](./README.md) |
| Runtime Guide | [runtime-guide.md](./runtime-guide.md) |
| Dual-Layer Positioning | [dual-layer-positioning.md](./dual-layer-positioning.md) |
| Status and Boundaries | [status-and-boundaries.md](./status-and-boundaries.md) |
| Runtime artifacts | [runtime/README.md](./runtime/README.md) |
| Forward Atlas | [Problem Map 3.0 Troubleshooting Atlas](../wfgy-ai-problem-map-troubleshooting-atlas.md) |
| Twin Atlas | [Twin Atlas README](../Twin_Atlas/README.md) |
| Future bridge | [Atlas Bridge README](../Atlas_Bridge/README.md) |

---

## What you need first ✅

Before starting, make sure you have:

- one strong language model that can handle long instructions
- access to the Inverse Atlas runtime artifacts
- one test prompt or one case from the case pack
- a willingness to compare answers structurally, not just stylistically

You do **not** need to read the full paper first.

You do **not** need a full benchmark setup first.

You only need enough patience to compare:

1. a normal answer  
2. an inverse-governed answer

That comparison is the whole point of the quick start.

---

## Fastest path: the 60-second experience 🚀

This is the minimum viable experience.

### Step 1
Open a strong LLM chat.

### Step 2
Load the content of:

`runtime/inverse-runtime.txt`

Use it as the system prompt, governing instruction, or equivalent long-form control layer.

### Step 3
Paste the content of:

`runtime/inverse-demo.txt`

This gives the model the expected demo frame.

### Step 4
Choose one example from:

`runtime/inverse-cases.txt`

Paste one case into the same chat.

### Step 5
Observe the result.

At minimum, you want to notice whether the model now behaves differently in these ways:

- less premature closure
- less fake certainty
- more explicit control of unresolved structure
- clearer distinction between coarse judgment and authorized resolution
- better resistance to cosmetic repair

That is the first success criterion.

The point is not “did the answer become longer?”
The point is:

**did the answer become more lawfully proportioned to what was actually earned?**

---

## Recommended first test case 🎯

For your first trial, choose a case where a normal model is likely to do one of these things:

- answer too confidently
- jump to a single route too early
- overstate repair quality
- collapse two still-live explanations into one
- speak as if the structure is resolved when it is not

These are the conditions where Inverse Atlas is easiest to feel.

If your first case is too easy or too clean, the difference may look smaller than it really is.

So for the first impression, do **not** choose a toy prompt that any model would answer safely.

Choose a case with real ambiguity, real structural tension, or real temptation toward fake closure.

---

## What to look for in the output 👀

Do not judge only by surface style.

Judge by structure.

A useful first pass is to ask:

### Did the model stop itself when it should have?
For example:

- did it refuse premature resolution
- did it remain coarse when detail would have overreached
- did it stay unresolved when neighboring routes were still alive

### Did the model separate route promise from lawful authorization?
A route can look plausible before it is lawfully strong enough for public emission.

That distinction matters.

### Did the model avoid fake repair?
A lot of weak AI behavior looks helpful because it patches wording, sequence, or local detail while leaving the broken invariant untouched.

Inverse Atlas is supposed to reduce that.

### Did the model control its confidence ceiling?
A strong answer is not automatically a lawful answer.

The model should not sound more certain than the current support actually allows.

---

## The practical comparison loop 🔁

The easiest way to feel the difference is to compare two outputs side by side.

### Baseline pass
Use the same case in a normal chat without the Inverse Atlas runtime layer.

Collect the ordinary answer.

### Inverse pass
Use the same case again, but now with:

- `inverse-runtime.txt`
- `inverse-demo.txt`

Collect the inverse-governed answer.

### Compare the two
Now compare them using these questions:

- Which one closes earlier
- Which one distinguishes unresolved routes better
- Which one sounds falsely complete
- Which one is more careful about authorization level
- Which one is more likely to confuse cosmetic repair with structural repair

This comparison is more important than raw tone preference.

The quick start is successful if you can feel a real difference in governance behavior.

---

## The three easiest usage modes 🧪

You do not need to use every artifact the same way on day one.

Here are the three easiest modes.

### Mode 1: fast demo mode
Use:

- `inverse-runtime.txt`
- `inverse-demo.txt`
- one case from `inverse-cases.txt`

This is the best starting point.

### Mode 2: direct case mode
Use:

- `inverse-runtime.txt`
- your own ambiguous or failure-prone prompt

This is useful if you already have a real AI debugging scenario in mind.

### Mode 3: evaluator mode
Use:

- `inverse-eval.txt`
- one original prompt
- one candidate answer

This is useful when you already have an output and want to judge whether it obeys the Inverse Atlas legality logic.

---

## If you want the cleanest first impression, do this first 🌟

If you only have time for one short test, use this order:

1. read the main [README.md](./README.md)
2. load `inverse-runtime.txt`
3. paste `inverse-demo.txt`
4. choose one case from `inverse-cases.txt`
5. compare that result with a plain baseline answer
6. write down the first structural difference you notice

That sixth step is important.

Do not just say “this one feels better.”

Write down **why** it feels better.

Examples:

- “it did not over-resolve”
- “it kept two routes alive”
- “it stayed coarse instead of bluffing detail”
- “it rejected fake repair”
- “it asked for stronger support before stronger claims”

That helps you see the system as governance, not just style.

---

## Evaluator path: shortest version 🧾

If you already have an answer and want to check whether it obeys the Inverse Atlas logic, use the evaluator path.

### Step 1
Open a fresh chat.

### Step 2
Load:

`runtime/inverse-eval.txt`

### Step 3
Provide:

- the original user input
- the candidate output

### Step 4
Ask the evaluator to judge whether the answer is lawful under the Inverse Atlas framework.

This path is especially useful when:

- you already have a baseline answer
- you want to test whether a “strong-looking” answer is actually overclaiming
- you want to compare two outputs with the same evaluation standard

---

## Pair comparison path: best for seeing the difference clearly ⚔️

If you want a stronger demonstration, use pair comparison.

### Step 1
Prepare one original prompt.

### Step 2
Generate a normal baseline answer.

### Step 3
Generate an inverse-governed answer.

### Step 4
Open a fresh evaluator chat with `inverse-eval.txt`.

### Step 5
Provide all three items:

- the original prompt
- the baseline answer
- the inverse-governed answer

### Step 6
Ask which answer better obeys the Inverse Atlas legality logic, and why.

This is one of the clearest ways to show that the system is doing more than changing tone.

It helps show whether the governance layer is actually changing resolution discipline.

---

## Common first-time mistakes ❗

### Mistake 1
Using an overly simple prompt.

If the prompt is too easy, both outputs may look similar.

### Mistake 2
Judging only by politeness or hesitation.

Inverse Atlas is not trying to sound timid.  
It is trying to sound proportionate to earned support.

### Mistake 3
Expecting every good result to be longer.

Sometimes a better governed answer is shorter, because it refuses illegal overreach.

### Mistake 4
Confusing “more fluent” with “more lawful.”

A very smooth answer can still be illegitimate.

### Mistake 5
Skipping the baseline comparison.

Without the baseline, it is harder to see what the inverse layer is really changing.

---

## What success looks like in the MVP stage 🧩

At the MVP stage, success does not mean perfection.

It means you can already see a meaningful change in one or more of these:

- better restraint under ambiguity
- cleaner unresolved handling
- fewer premature resolution claims
- stronger distinction between structural repair and cosmetic repair
- better control of confidence ceiling
- more lawful output modes

That is enough for a real first validation.

---

## Where to go next 📚

After this quick start, the best next page is:

[Runtime Guide](./runtime-guide.md)

Read that page if you want to understand how the four main runtime artifacts fit together.

If you want the conceptual relationship between forward and inverse atlas, go next to:

[Dual-Layer Positioning](./dual-layer-positioning.md)

If you want the precise MVP claim boundary, go next to:

[Status and Boundaries](./status-and-boundaries.md)

If you want the route-first structural mapping side, go to:

[Problem Map 3.0 Troubleshooting Atlas](../wfgy-ai-problem-map-troubleshooting-atlas.md)

---

## Final note

The quick start is not meant to prove everything.

It is meant to let you feel the central difference quickly:

a normal model often tries to answer because it can

Inverse Atlas tries to answer only when the system has earned the right to answer at that level

That difference is the beginning of the whole product line.
