# Contribute to Tension Universe MVP Experiments

Tension Universe is being built as an open experimental field.

This contribution lane is focused on one specific type of work:

adding or improving MVP experiment pages inside the `TensionUniverse/Experiments/` collection.

This is not a general rewrite lane for the whole project.

The main purpose of this contribution path is to help expand the experiment layer of Tension Universe in a clean, structured, inspectable way, one page at a time.

## Scope of contribution

The expected contribution scope is narrow by design.

For public contributors, the preferred contribution is:

- add a new MVP experiment page for an open Tension Universe problem
- improve an existing MVP experiment page under `TensionUniverse/Experiments/`
- add small supporting notebook links, Colab links, screenshots, or structured notes that belong to that MVP page

In most cases, a contribution should focus on MVP experiment content only.

This keeps the core narrative stable while allowing the experiment field to grow in public.

## Where MVP experiments live

MVP experiment pages belong under:

`TensionUniverse/Experiments/`

A standard location looks like this:

`TensionUniverse/Experiments/Q091_MVP/README.md`

This means:

- each experiment gets its own folder
- each folder contains one main `README.md`
- optional notebooks, screenshots, or small assets can live next to that README

Examples of supporting files inside the same folder may include:

- `Q091_A.ipynb`
- `Q091_B.ipynb`
- `Q091A.png`
- `Q091A2.png`
- `Q091A3.png`

This structure keeps each experiment self-contained and easy to review.

## What counts as an MVP experiment

In this project, an MVP experiment does not mean a final proof, a complete benchmark, or a solved scientific claim.

An MVP experiment means:

- a small, inspectable experiment page
- a narrow and clearly defined question
- a reproducible or at least reviewable setup
- a first runnable or design-level protocol
- a documented relation to one specific Tension Universe problem

Most MVP experiments in the 131-problem field should be possible to build with:

- AI-assisted drafting
- a small notebook
- Google Colab
- text-first synthetic inputs
- lightweight plots, tables, or screenshots when useful

The intended standard is practical and transparent, not oversized.

## Problem alignment is required

Every MVP experiment page must map to a real Tension Universe problem.

The title, problem id, and direction should align with the canonical 131-problem field and the WFGY 3.0 reference pack.

Primary reference:

[WFGY 3.0 Singularity Demo AutoBoot SHA256 Verifiable TXT](https://raw.githubusercontent.com/onestardao/WFGY/refs/heads/main/TensionUniverse/WFGY-3.0_Singularity-Demo_AutoBoot_SHA256-Verifiable.txt)

That reference defines the broader system language and problem field.

Contributors do not need to reproduce the entire system pack, but they should stay aligned with the intended problem identity, naming, and direction.

If a page does not clearly map to a valid Tension Universe problem, it is unlikely to be accepted.

## Standard MVP page format

Contributors should follow the established experiment-page style already used in the project.

A strong MVP page usually includes the following parts.

### 1. Anchor comment block

At the top of the file, include a short HTML comment block that explains:

- this file belongs to the WFGY 3.0 Tension Universe experiment collection
- the main navigation hub
- the problem id
- the role of the page
- how this page should be used

This helps both human readers and AI systems understand the page context before reading the body.

### 2. Clear title with problem id

The main title should include:

- the TU problem id
- the fact that this is an MVP page
- a short descriptive experiment title

For example:

`# TU Q091 MVP: equilibrium climate sensitivity tension slices`

### 3. Honest status line

Near the top, include a status line that clearly states the implementation state.

Examples:

- MVP A implemented with a first reference run
- design-only at this stage
- first notebook draft checked in
- reference screenshots added, notebook pending cleanup

The status line should be factual and not exaggerated.

### 4. Navigation links

Near the top of the page, include navigation back to:

- the Experiments index
- the Event Horizon main entry

This keeps the experiment layer tied back to the main project structure.

### 5. Notebook and asset references

If the MVP includes runnable notebooks or screenshots, list them clearly near the top.

Google Colab links are strongly encouraged when available.

The ideal pattern is:

- one readable README
- one small notebook
- optional screenshots or static outputs

### 6. A narrow “what this page is about” section

Early in the page, explain:

- what the TU problem is
- what this MVP page is trying to test
- what this page does not claim to solve

This prevents confusion between a first experiment and a final theoretical claim.

### 7. One or more experiment sections

A standard MVP page may contain:

- Experiment A
- Experiment B
- later extensions if needed

Each experiment section should normally include:

- a research question
- a setup
- a design intent or expected pattern
- a simple reproduction path
- reference-run notes if available

This makes the page useful even before it becomes a polished benchmark.

### 8. Context and charter links

Where relevant, the page should link back to:

- the broader Experiments index
- Event Horizon
- any related charter or formal context page

This helps preserve system coherence across the project.

## Recommended writing style for MVP pages

A good MVP experiment page should be:

- narrow in scope
- explicit about assumptions
- easy to inspect
- honest about limitations
- written as a first serious experiment, not as a final claim

Please avoid:

- pretending an MVP solves the full problem
- oversized philosophical claims without a usable protocol
- disconnected content that does not map cleanly to a TU problem id
- dumping raw notes without structure

A small but well-shaped page is much more valuable than a large vague draft.

## Preferred contribution shape

The cleanest contribution is usually:

1. choose one valid TU problem
2. create or improve one folder under `TensionUniverse/Experiments/`
3. write one structured `README.md`
4. attach a small notebook or design protocol if useful
5. keep the PR limited to that experiment scope

This project strongly prefers focused PRs over large mixed changes.

## Submission path

There are two preferred ways to contribute.

### Option 1

Open an issue first, claim a problem, then submit your MVP page.

This is the best path when you want to avoid overlap.

### Option 2

Submit a focused PR directly for a small experiment-page addition or improvement.

This works best when the draft is already prepared and tightly scoped.

In either case, please keep the contribution limited to the relevant MVP experiment material.

## Contributor credit

Accepted MVP experiment pages may include a small contributor credit block at the bottom of the page.

This is intended to acknowledge meaningful work on that specific experiment page.

It is not ownership of the whole Tension Universe project, and it does not override the editorial direction of the project.

For consistency, contributor credit uses a fixed format and only accepts GitHub links.

See the format guide here:

[Contributor credit format](./contributor-credit-format.md)

## Open experiment board

To find currently open or planned MVP work, use the public experiment board:

[Open experiments board](./open-experiments.md)

That board is the simplest place to see which experiments are already complete, in progress, or still open for contribution.

## A note for early contributors

This page does not promise traffic, status, or outcomes.

But early contributors are often the first visible names attached to experiment pages that later become useful reference points inside a growing system.

If you believe the Tension Universe direction is worth building, one of the clearest ways to leave a real mark is to help turn open problems into inspectable MVP experiments.

## Editorial review

All contributed content may be edited for:

- clarity
- formatting
- naming consistency
- structure
- alignment with the broader Tension Universe direction

This keeps the experiment layer coherent as more pages are added.

If your contribution is accepted, your contributor credit can remain attached to that page using the standard format.

## Start here

If you want to contribute, the simplest next step is:

1. open the experiment board
2. choose one valid TU problem
3. draft one structured MVP page under `TensionUniverse/Experiments/`
4. submit a focused issue or PR

The field is still expanding.

If you want to help build it, build one experiment page at a time.
