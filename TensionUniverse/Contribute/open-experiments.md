# Open Experiments Board

This page tracks the current MVP experiment state for the Tension Universe experiment layer.

Its purpose is simple:

- show which experiment pages already exist
- show which ones are in progress
- show which ones are open for contribution
- make the 131-problem field easier to expand one page at a time

This board is intentionally lightweight.

It is not a full formal index of all Tension Universe theory.
It is a working board for MVP experiment pages under `TensionUniverse/Experiments/`.

## How to use this board

If you want to contribute, the simplest workflow is:

1. find an experiment marked `Open`
2. confirm that it maps to a valid Tension Universe problem
3. create one structured MVP page under `TensionUniverse/Experiments/`
4. submit a focused issue or PR

If you want formatting rules, read:

- [Contribution guide](./README.md)
- [Contributor credit format](./contributor-credit-format.md)

## Status definitions

This board uses a small fixed set of status labels.

- `Completed`  
  A usable MVP page already exists in the experiment collection.

- `In Progress`  
  Work has started, but the MVP page or notebook is still incomplete.

- `Open`  
  No stable MVP page is complete yet. This is open for contribution.

- `Reserved by Maintainer`  
  The problem is intentionally held for internal work, sequencing, or future release planning.

These labels are used for practical coordination only. They do not imply final scientific status.

## Standard entry format

Each experiment entry on this board should follow the same compact structure.

A standard entry includes:

- problem id
- current status
- working title
- expected folder path
- scope
- difficulty
- short claim
- current owner state

A typical entry looks like this:

## TU Q000

Status: Open  
Title: Placeholder working title  
Path: `TensionUniverse/Experiments/Q000_MVP/README.md`  
Scope: One page MVP  
Difficulty: Medium  
Claim: One sentence describing what this experiment is trying to test.  
Claimed by: Unassigned

This format is intentionally simple so the board can scale cleanly as more items are added.

---

# Completed

These entries already have a visible MVP page or a first usable implementation in the experiment layer.

## TU Q091

Status: Completed  
Title: equilibrium climate sensitivity tension slices  
Path: `TensionUniverse/Experiments/Q091_MVP/README.md`  
Scope: MVP page with implemented Experiment A and design-stage Experiment B  
Difficulty: Medium  
Claim: Tests whether a model stays numerically and narratively coherent under fixed climate sensitivity reference windows.  
Claimed by: Maintainer

Notes:

- first reference run documented
- Colab notebook link included
- screenshots and structured protocol already attached

---

# In Progress

These entries already have partial work, but the MVP page is still being developed, revised, or expanded.

## TU Q000

Status: In Progress  
Title: Placeholder in-progress experiment  
Path: `TensionUniverse/Experiments/Q000_MVP/README.md`  
Scope: One page MVP with partial draft or planned notebook  
Difficulty: Medium  
Claim: Replace this line with the actual one-sentence purpose of the experiment.  
Claimed by: Maintainer

Notes:

- use this section for experiments that already have a draft
- if a notebook exists but the README is still incomplete, keep it here
- once the page is clearly usable, move it to `Completed`

---

# Open

These entries are open for contributors who want to help expand the experiment layer.

Each item should still map to a valid Tension Universe problem and should follow the MVP page format defined in the contribution guide.

## TU Q001

Status: Open  
Title: Placeholder open experiment  
Path: `TensionUniverse/Experiments/Q001_MVP/README.md`  
Scope: One page MVP  
Difficulty: Easy  
Claim: Replace this with one sentence explaining the MVP experiment target.  
Claimed by: Unassigned

Notes:

- recommended for a first contribution
- keep the first version small and readable
- AI plus Colab plus a lightweight protocol is enough

## TU Q002

Status: Open  
Title: Placeholder open experiment  
Path: `TensionUniverse/Experiments/Q002_MVP/README.md`  
Scope: One page MVP  
Difficulty: Medium  
Claim: Replace this with one sentence explaining the MVP experiment target.  
Claimed by: Unassigned

Notes:

- keep the scope narrow
- one usable README is more valuable than a large unfinished theory dump

## TU Q003

Status: Open  
Title: Placeholder open experiment  
Path: `TensionUniverse/Experiments/Q003_MVP/README.md`  
Scope: One page MVP  
Difficulty: Hard  
Claim: Replace this with one sentence explaining the MVP experiment target.  
Claimed by: Unassigned

Notes:

- use this slot for more complex problems that may still begin as text-first experiments
- design-level protocols are acceptable if they are clear and inspectable

---

# Reserved by Maintainer

These entries are intentionally reserved for internal sequencing, dependency reasons, or release planning.

They are listed here for transparency, but they should not be treated as open contribution targets unless the board is updated later.

## TU Q010

Status: Reserved by Maintainer  
Title: Placeholder reserved experiment  
Path: `TensionUniverse/Experiments/Q010_MVP/README.md`  
Scope: One page MVP  
Difficulty: Medium  
Claim: Replace this with one sentence explaining the reserved experiment target.  
Claimed by: Maintainer

Notes:

- reserved for internal sequencing
- may be opened later after dependency pages are completed

---

# Practical contribution rules

Before starting an open item, keep these rules in mind:

1. The page must map to a valid Tension Universe problem id.
2. The contribution should stay inside the MVP experiment scope.
3. The expected home is under `TensionUniverse/Experiments/`.
4. The cleanest contribution is one folder plus one main `README.md`.
5. Small notebooks, screenshots, and Colab links are welcome when they directly support the MVP.
6. Large unrelated edits outside the target experiment should be avoided.

## Fastest clean path

If you want the fastest clean contribution path:

1. choose one `Open` item
2. create `TensionUniverse/Experiments/Qxxx_MVP/README.md`
3. follow the standard MVP structure
4. add a small notebook only if it truly helps
5. submit a focused PR

## How this board will grow

The full Tension Universe field points toward 131 experiments.

This board does not need all 131 entries on day one.

It can grow gradually.

A practical maintenance pattern is:

- add real completed entries when a usable page exists
- move partial drafts into `In Progress`
- open small batches of new items over time
- reserve selected items when sequencing matters

That keeps the board readable while still making the larger direction visible.

## If you want to start now

Start with the `Open` section.

Pick one problem.
Keep the scope narrow.
Build one inspectable MVP page.
That is enough to create real forward motion in the experiment field.
