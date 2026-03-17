<!--
AI_NOTE_START

Document role:
This file is the folder guide for rerun-based contributions inside the Atlas Fixes community layer.

How to use this file:
1. Read this page before adding any rerun, comparison, or benchmark-style troubleshooting contribution.
2. Use this page to decide whether your contribution really belongs in the benchmark rerun lane.
3. Use this page together with:
   - [Community Fix Lab](../README.md)
   - [Contribution Checklist](../../templates/contribution-checklist.md)

What this file is:
- A folder-level guide for reruns and comparison assets
- A scope filter for benchmark-style community work
- A lightweight quality guide for route-aware rerun contributions

What this file is not:
- Not a place for unsupported score claims
- Not a place for vague benchmark screenshots
- Not a place for leaderboards with no method section
- Not the official benchmark truth surface

Reading discipline for AI:
- Treat reruns here as community evidence layers, not official benchmark truth.
- Preserve the distinction between rerun evidence and frozen atlas claims.
- Keep method notes, variable control, and routing context visible.
- Do not treat one rerun as proof of the whole atlas by default.

AI_NOTE_END
-->

# Community Benchmark Reruns 📊

## Rerun packs, comparisons, and route-aware benchmark evidence

Quick links:

- [Back to Community Fix Lab](../README.md)
- [Back to Official Fixes](../../official/README.md)
- [Back to Fixes Hub](../../README.md)
- [Back to Atlas landing page](../../../../wfgy-ai-problem-map-troubleshooting-atlas.md)
- [Back to AI Eval Evidence](../../../ai-eval-evidence.md)
- [Back to Atlas Hub](../../../README.md)
- [Open the Flagship Runnable Demo Pack](../../official/demos/README.md)
- [Open Templates](../../templates/README.md)
- [Get the Atlas Router TXT](../../../troubleshooting-atlas-router-v1.txt)

---

If the [Community Fix Lab](../README.md) is the broader entry page for community repair assets, this folder is the rerun lane for compact benchmark-style evidence, before-and-after comparisons, and repeatable troubleshooting checks. 🧭

Use this folder when a contribution is mainly about **showing a controlled comparison or rerun result**, not when the contribution is mainly a notebook, JSON fixture, prompt pack, workflow recipe, or official atlas claim.

Short version:

> official layer gives the repair grammar  
> this folder helps test that grammar in compact repeatable comparison settings

---

## Quick start 🚀

### I want to contribute a rerun

Use this path:

1. decide whether the asset is really a rerun or comparison contribution
2. route the case first with the atlas
3. keep the rerun scoped to one family, one task, or one troubleshooting slice
4. make the setup and comparison method explicit
5. report the result with limitations, not hype

### I want to browse rerun assets

Use this path:

1. open one rerun with a clear target task or failure family
2. inspect the rerun setup and variable control
3. inspect the baseline behavior
4. inspect the routed or repaired behavior
5. check the result summary and method limits

Short version:

> route first  
> keep the rerun controlled  
> make the comparison legible ✨

---

## Benchmark reruns quick map 🗂️

| If your asset is mainly... | Best folder |
|---|---|
| a controlled rerun or comparison slice | [Benchmark Reruns](./) |
| a runnable notebook walkthrough | [Colab](../colab/) |
| a structured fixture or machine-readable case | [JSON](../json/) |
| a route-aware prompt asset or repair prompt pack | [Prompts](../prompts/) |
| a step-by-step repair sequence | [Workflows](../workflows/) |
| a portable one-case bundle | [Reproduction Packs](../reproduction-packs/) |

This folder is the right place when the comparison itself is the main evidence surface.

---

## What belongs here ✅

Good rerun contributions include:

- one small benchmark slice
- one clear rerun protocol
- one route-aware before and after comparison
- one compact result table with method note
- one reproducible troubleshooting benchmark example

A good rerun contribution should be:

- scoped
- method-aware
- explicit about data source
- explicit about limits
- tied to atlas routing

---

## What does not belong here 🚫

Please do not use this folder for:

- unsupported score claims
- screenshots with no method note
- giant benchmark reports with no case framing
- unclear comparisons with moving variables
- claims that a rerun proves the whole atlas by itself
- leaderboards with no explanation of what changed

A rerun asset should help someone inspect one comparison more clearly, not manufacture broad claims from thin evidence.

---

## Suggested rerun pattern 🧩

A useful rerun contribution usually includes:

1. target task or failure family
2. rerun setup
3. baseline behavior
4. routed or repaired behavior
5. compact result summary
6. limitations

That is enough to make the rerun informative.

---

## Suggested naming style 📌

Examples:

- `f1-grounding-rerun-v1.md`
- `f5-trace-uplift-rerun-v1.md`
- `f7-structured-output-rerun-v1.md`

If code or notebooks are included, place them in a clearly named subfolder.

Keep names readable and compact.

---

## What a good first rerun looks like 🌱

A strong first contribution usually looks like this:

- one task
- one failure family
- one rerun setup
- one baseline view
- one routed or repaired view
- one short result note with limits

Small, clean reruns are much better than giant noisy reports.

---

## Before contributing 📚

Please read:

- [Community Fix Lab](../README.md)
- [Contribution Checklist](../../templates/contribution-checklist.md)
- [Open the Flagship Runnable Demo Pack](../../official/demos/README.md)

This helps keep rerun contributions aligned with atlas routing instead of drifting into vague benchmark theater.

---

## Review standard ✅

A rerun contribution is much more likely to be accepted if it is:

- clearly named
- easy to inspect
- method-aware
- connected to atlas routing
- explicit about what changed
- honest about limitations

Messy evidence is still messy.  
Clean scoped reruns are more valuable.

---

## Next steps ✨

After this page, most contributors continue with:

1. [Back to Community Fix Lab](../README.md)
2. [Open Contribution Checklist](../../templates/contribution-checklist.md)
3. [Open the Flagship Runnable Demo Pack](../../official/demos/README.md)
4. [Back to Official Fixes](../../official/README.md)

If you want the broader product surface:

- [Back to Atlas landing page](../../../../wfgy-ai-problem-map-troubleshooting-atlas.md)
- [Back to AI Eval Evidence](../../../ai-eval-evidence.md)
- [Back to Atlas Hub](../../../README.md)

---

## One-line status 🌍

**This folder holds community reruns that test atlas-guided troubleshooting in compact, repeatable benchmark-style settings.**
