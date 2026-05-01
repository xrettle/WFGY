# Polaris Experiments

> Public experiment layer for **WFGY 5.0 Polaris Protocol**.  
> Status: public-safe aggregate evidence, not final benchmark release.

This folder records the current public experiment layer of **WFGY 5.0 Polaris Protocol**.

The goal of these experiments is to study a **topology-first route for AI generation**. Instead of treating longer context, larger models, or more compute as the only path to stronger AI output, Polaris asks whether generation becomes more stable when the task topology is preserved before the transformer begins producing text.

In this view, the important object is not only the prompt text.

The important object is the structure carried into generation.

That structure may include role layout, dependency order, causal pressure, evidence anchors, boundary conditions, failure paths, repair routes, continuity constraints, and claim ceilings.

The current public experiment area contains two main evidence branches:

1. **AI Tsunami**
2. **Moses**

These branches should not be read as identical tests. They play different roles in the Polaris evidence map.

---

## Download Public-Safe Data Packages

The current public-safe aggregate ZIP packages are stored in:

`Polaris/experiments/downloads/`

### AI Tsunami Public-Safe Data Package

**Download:**

[WFGY_AI_TSUNAMI_PUBLIC_SAFE_DATA_PACKAGE_20260501.zip](./downloads/WFGY_AI_TSUNAMI_PUBLIC_SAFE_DATA_PACKAGE_20260501.zip)

**SHA256:**

```text
934962c4a59c8ab0ec672dcbb666053a5e80f0072dfae7fff187ee0b042cc005
````

### Moses Public-Safe Data Package

**Download:**

[WFGY_MOSES_PUBLIC_SAFE_DATA_PACKAGE_20260501.zip](./downloads/WFGY_MOSES_PUBLIC_SAFE_DATA_PACKAGE_20260501.zip)

**SHA256:**

```text
ab6091898deb09ada3c71c9a4f2fd9b1fc8acc1ea42629b42ca942a9e35f5cfb
```

These ZIP files are **public-safe aggregate packages**.

They are intended for public reading, high-level review, and claim-boundary inspection. They are not reproducibility packages and are not implementation releases.

---

## 1. AI Tsunami Branch

**Current public status:** fixed PASS branch
**Current role:** topology-conservation / compression / negative-control evidence
**Public claim level:** T4 Robustness Expansion PASS under scoped topology-conservation workloads

AI Tsunami is the cleanest fixed passing branch in the current public package set.

It tests whether a correct compressed topology packet can preserve high output quality while using far fewer tokens than a long-context baseline.

The important comparison is not simply:

> long prompt vs short prompt

The important comparison is:

* long-context baseline
* correct compressed topology packet
* corrupted topology condition

This lets the experiment ask a stronger question:

> Does the model preserve quality because the useful topology is still present?

The public aggregate data shows that the correct topology packet stayed at long-context-level quality while using a much smaller token budget, and that the corrupted topology condition collapsed in the expected direction.

This supports the topology-first direction of Polaris Protocol under the tested scope.

The safe public summary is:

> AI Tsunami has passed T4 Robustness Expansion under scoped topology-conservation workloads.

---

## 2. Moses Branch

**Current public status:** composite closure / merge-preparation evidence
**Current role:** robustness / patch verification / failure-surface tracking
**Public claim level:** not independent full T4 v2 ALL PASS

Moses is included as the second public evidence branch, but it should be read with its caveat intact.

The Moses public-safe package records a composite closure state for merge preparation. It includes clean full API evidence at the earlier locked MVP stage and a T4 composite record based on full T4 v1 pipeline execution plus a targeted patch mini verifier.

Moses is **not** marked as a full independent T4 v2 ALL PASS result yet.

The reason is specific and preserved in the public record:

* the T4 full v1 pipeline executed completely
* the output count completed
* parse, leakage, scorer-shortcut, and poison checks remained clean at the aggregate level
* but the T4 full v1 verdict halted due to localized design and judge issues
* a later patch mini verifier targeted the known failure surfaces and passed at mini scale

Therefore, the current Moses status is:

> composite closed for merge preparation, not full independent T4 v2 pass.

This is not hidden or softened. It is part of the honest experiment record.

Moses should currently be read as a transitional robustness branch. It is useful evidence for merge preparation, but it does not yet authorize full ALL PASS language.

---

## 3. How To Read The Two Branches Together

AI Tsunami and Moses answer different questions.

AI Tsunami asks:

> Can correct topology preservation maintain output quality with fewer tokens?

Moses asks:

> Can the system track robustness, failure surfaces, and patch verification well enough to prepare for merge-level work?

Together, they form the current public Polaris experiment map.

AI Tsunami provides the stronger fixed pass signal.

Moses provides transitional robustness and merge-preparation evidence, while keeping the remaining full-pass limitation visible.

The intended reading is:

> AI Tsunami is the fixed topology-conservation pass.
> Moses is the honest composite closure branch, awaiting later correction and update before any full ALL PASS language.

Together, they support the topology-first research direction of WFGY 5.0 Polaris Protocol, but they do not yet authorize universal claims.

---

## 4. What The Public Packages Contain

The public packages may include:

* public README files
* public claim boundaries
* aggregate CSV metrics
* aggregate JSON metrics
* public composite verdict summaries
* redaction and safety notes
* SHA256 manifests

They are designed to show public aggregate results without exposing private experiment machinery.

These packages are meant to let readers inspect the public result layer, not reconstruct the private engine.

---

## 5. What The Public Packages Do Not Contain

The public packages intentionally do **not** include:

* executable notebooks
* Colab notebooks
* raw evidence zips
* raw outputs
* parsed outputs
* prompt manifests
* case payloads
* judge rows
* scorer / evaluator code
* detailed failure-surface records
* private scoring contracts
* internal mathematical spine materials

The public packages are result summaries, not reconstruction kits.

They are public-safe aggregate records.

---

## 6. Current Evidence Interpretation

The current evidence supports a scoped topology-first interpretation:

> Under tested topology-conservation workloads, correct topology packets can preserve high output quality with far fewer tokens, while corrupted topology can produce predictable degradation.

This is meaningful, but scoped.

It supports Polaris as a research and protocol direction.

It does not complete the entire AI problem.

The main interpretation is:

> Generation quality may depend less on raw context length alone, and more on whether the model receives the correct task topology before generation begins.

This is the reason Polaris treats topology as a first-class generation object.

---

## 7. What This Does Not Claim

This experiment folder does **not** claim:

* all AI tasks are solved
* all benchmarks are complete
* GPU scaling is globally disproven
* small models universally beat large models
* coding is fully proven
* math is fully proven
* creative generation is fully proven
* multimodal generation is fully proven
* agent execution is fully proven
* Moses and Tsunami are fully merged
* Polaris Protocol is final

The current public status is narrower:

> public-safe aggregate evidence for the current Polaris experiment layer.

---

## 8. Update Plan

Planned updates may include:

* dedicated AI Tsunami explanation page
* dedicated Moses explanation page
* updated Moses data after correction
* merge-interface notes
* public result interpretation
* download index updates
* final claim-boundary map

Until then, this folder should be read as an active experiment area, not a final release.

---

## Current Package Index

| Package                             | Role                                         | Download                                                                      | SHA256                                                             |
| ----------------------------------- | -------------------------------------------- | ----------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| AI Tsunami Public-Safe Data Package | fixed topology-conservation PASS branch      | [Download](./downloads/WFGY_AI_TSUNAMI_PUBLIC_SAFE_DATA_PACKAGE_20260501.zip) | `934962c4a59c8ab0ec672dcbb666053a5e80f0072dfae7fff187ee0b042cc005` |
| Moses Public-Safe Data Package      | composite closure / merge-preparation branch | [Download](./downloads/WFGY_MOSES_PUBLIC_SAFE_DATA_PACKAGE_20260501.zip)      | `ab6091898deb09ada3c71c9a4f2fd9b1fc8acc1ea42629b42ca942a9e35f5cfb` |

---

## Status

**Project:** WFGY 5.0 Polaris Protocol
**Folder role:** public experiment layer
**Data type:** public-safe aggregate evidence
**Final benchmark:** not yet released
**Implementation release:** not included
**Core mathematical spine:** not included
