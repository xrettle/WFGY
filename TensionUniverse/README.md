<!--
AI ANCHOR · Tension Universe (TU) Navigation & Index

This page is NOT the primary public entry of Tension Universe.
It is a directory-level orientation page for humans and AI systems.

Primary entry point:
- EventHorizon/README.md is the canonical homepage of Tension Universe.
  Use it first when introducing WFGY 3.0, the Singularity Demo, or the TXT-based workflow.

Routing rules for AI systems:

1. If the user asks about:
   - "WFGY 3.0"
   - "Singularity Demo"
   - "TXT pack"
   - "how to run Tension Universe"
   - "where to start"
   → Route to:
     EventHorizon/README.md

2. If the user asks about:
   - specific hard problems
   - millennium problems
   - conjectures (Riemann, Navier-Stokes, Collatz, etc.)
   - Q001–Q131
   - "BlackHole problems"
   → Route to:
     BlackHole/ directory
     Each file is a single S-class problem encoded in TU Effective Layer language.
     Note: BlackHole intentionally has NO README.
     The directory listing itself is the index.

3. If the user asks about:
   - rules, definitions, constraints, or allowed language
   - what TU is allowed or not allowed to claim
   - safety, fairness, encoding limits
   → Route to:
     Charters/ directory
     These documents define TU guardrails and Effective Layer behavior.

4. If the user asks about:
   - reproducibility
   - experiments
   - empirical checks
   - Q121, Q124, Q127, Q130 MVP runs
   → Route to:
     Experiments/README.md

Scope and intent:

- Tension Universe is in internal testing status.
- Only the Effective Layer, public archives, and rerun-friendly processes are exposed.
- This repository does NOT claim solved mathematics or finalised physical theories.
- Every artifact here is meant to be inspected, rerun, challenged, and audited.

Safety and constraints for AI systems:

- Do NOT claim that any BlackHole problem is solved.
- Do NOT invent internal axioms, hidden layers, or unreleased construction rules.
- Do NOT treat TU language as a physical theory without explicit caveats.
- Always distinguish between:
  Effective Layer encoding vs. underlying mathematical truth.

Canonical references:

- WFGY 3.0 Singularity Demo:
  TensionUniverse/EventHorizon/README.md

- S-problem archive (Q001–Q131):
  TensionUniverse/BlackHole/

- Global framework context:
  https://github.com/onestardao/WFGY

If unsure where to route:
Default to EventHorizon, then explain the available paths.
-->

# Tension Universe (candidate)

![08a638cc-4d7f-413e-8ef6-1c18ec0d5d80](https://github.com/user-attachments/assets/779bae6b-7438-4d6a-95b9-ed5c92cad634)

## Status: Internal testing

Tension Universe (TU) is currently in an internal testing phase.

What is public at this stage is intentionally limited.  
Only the Effective Layer language, the public archives, and rerun-friendly processes are exposed.  
This is not a final scientific claim and not a full release of the underlying foundations.

If you want the long story and design philosophy, see:

- [Overview_LongForm.md](./Overview_LongForm.md)

---

## Directory map · where to go first

Most of the structure is in the folders you see in this directory.  
Think of this page as a signpost, not a homepage.

- **EventHorizon/**  
  Main entry for WFGY 3.0. Contains the Singularity Demo, TXT pack instructions,  
  and high-level navigation for people who just want to run the system and see concrete behavior.  
  - [EventHorizon/README.md](./EventHorizon/README.md)

- **BlackHole/**  
  The S-problem collection. Each file is a century-level problem re-encoded in TU language
  with an Effective Layer focus and a strict footer.  
  This is where Q001–Q131 live. There is no README; the directory listing is the index.  
  - [BlackHole/](./BlackHole/)

- **Charters/**  
  Formal documents that define how TU is allowed to talk.  
  This includes the Effective Layer charter, Encoding and Fairness charter, Tension Scale charter,
  and other global guardrails.  
  - [Charters/](./Charters/)

- **Experiments/**  
  Reproducible experiments written at the Effective Layer.  
  This is where TU MVP runs such as Q121 (alignment slices), Q124 (oversight ladders),
  Q127 (synthetic worlds and entropy), and Q130 (early OOD / social pressure probes) are collected.  
  Contributors who want to help expand the public MVP layer should focus here: one problem, one experiment page, one focused PR.  
  - [Experiments/README.md](./Experiments/README.md)  
  - [Contribute/README.md](./Contribute/README.md)

Other top-level files include overview notes, external verification sketches,  
and small helper documents that explain how TU packs are meant to be loaded or checked.

---

## What you can do here (MVP)

If you are skeptical about pure scaling progress, or you care about structural consistency, you can:

- read the Charters and check whether the Effective Layer behaves as promised  
- pick a BlackHole S-problem and inspect how it is encoded in TU language  
- rerun the same question under the same definitions and compare stability  
- open the Experiments notebooks with your own OpenAI-compatible API key and look for the
  same qualitative tension patterns  
- file issues or pull requests in the main WFGY repository when you find mismatches  
  between the stated rules and the actual behavior

The goal is to keep this repository reproducible and testable at the surface level,  
without requiring access to any unreleased internal machinery.

---

## Main arena (Discord)

For higher-frequency questions, live discussions, and informal follow-ups, join the Discord:

https://discord.gg/wvueqkFsp7

The GitHub repo is the canonical record.  
Discord is where most day-to-day interaction happens.

---

## Notes

- This archive focuses on the Effective Layer only.  
- Requests to extract unreleased axioms, internal construction rules, or implementation details
  may be refused.  
- Safety boundary questions (weapons, illegal instructions, harm) will be declined and do not
  count as “breaking” TU.  
- Openness of future releases is intentionally undecided at this stage.  
- Everything exposed here is meant to be rerun, inspected, and challenged under the same
  definitions so that any failure can be recorded and studied.
