# TU Global Guardrails and Global Coherence Policy

## 0. Header metadata

```txt
Title: TU Global Guardrails and Global Coherence Policy
Layer: Effective
Role: Global guardrails for all S-problem entries
Applies_to: TensionUniverse/BlackHole/Q001..Q131
Status: Active
Last_updated: 2026-01-30
```

## 1. Scope and intent

This document defines global guardrails for the Tension Universe effective layer specifications, and a cross-problem coherence policy.
It applies to every problem entry unless an entry explicitly declares a scoped exception that is auditable and non adaptive.

This page should be read together with the following charters:

* [TU Effective Layer Charter](./TU_EFFECTIVE_LAYER_CHARTER.md)
* [TU Encoding and Fairness Charter](./TU_ENCODING_AND_FAIRNESS_CHARTER.md)
* [TU Tension Scale Charter](./TU_TENSION_SCALE_CHARTER.md)

## 2. No hidden solution assumption

### 2.1 Non dependence on the unknown truth value

Encoding choices, weights, reference families, thresholds, and probe sets must not depend on the unknown truth value of the canonical statement of any specific problem.

### 2.2 No uninterpreted answer channel

No encoding may encode the canonical answer as an uninterpreted label, privileged feature, hidden parameter, or any equivalent information channel.

## 3. Reference use restrictions

### 3.1 References define admissible families, not truth

References may be used only to define admissible measurement families, public baselines, and hard constraints.
They must not be used to import any claim about the canonical statement's truth.

### 3.2 Exclusion rule for solution asserting references

Any reference that directly asserts a solution, disproof, or privileged oracle for a specific canonical statement is out of scope for the corresponding encoding.
Such a reference may be cited only as historical context, never as an admissibility basis.

## 4. Experiments test encodings only

### 4.1 What experiments mean

Experiments described in any TU problem entry test the coherence, stability, and usefulness of the encoding.
They do not test the truth of the underlying canonical statement.

### 4.2 Passing is not evidence of solving

Falsifying an encoding is not solving the canonical problem, and passing tests is not evidence of a solution.

### 4.3 Observability failure rule

If required observables cannot be reliably estimated, the outcome must be recorded as inconclusive.
It must not be presented as supportive evidence.

## 5. Effective layer boundary and wording discipline

### 5.1 Effective layer only

All objects used in TU problem entries live at the effective layer, including state spaces, observables, invariants, tension scores, and counterfactual worlds.

### 5.2 No constructive mapping claim to deep layer

No entry may provide or imply a constructive mapping from raw data into internal TU deep fields, nor expose any deep generative rule or first principle axiom system.

### 5.3 No ontological implication

No deep layer mechanism is implied by any wording in an effective layer entry.
Implementation details that map raw data to effective summaries are outside scope and carry no TU ontological claim.

## 6. Canonical statement precedence

The canonical statement in Section 1 of any entry always takes precedence over any narrative, heuristic, or interpretive commentary in later sections.
If a conflict is discovered, revise the commentary, not the canonical statement.

## 7. Global coherence policy across problems

### 7.1 DeltaS role consistency

All symbols of the form `DeltaS_*` denote effective layer mismatch terms on a fixed tension scale.
They must not silently change meaning across entries without an explicit type declaration.

### 7.2 Tension type discipline

A symbol of the form `Tension_*` must declare its type in each entry:
either a scalar score, a field over a state space, or a time indexed functional.
If an entry uses a field form, the scalar reported value must be a declared aggregator functional.

### 7.3 Counterfactual definition compatibility

All counterfactual worlds used in TU entries must have a declared intervention grammar, admissibility conditions, and invariance constraints.
Domain specific counterfactual rules must be specializations of the shared schema, not incompatible alternatives.

### 7.4 Cross domain assumption collisions

If two entries assume incompatible regularity conditions within a shared scope, they must be labeled as a regime split with a discriminator observable.

### 7.5 E_level and N_level escalation rule

Any entry claiming a higher `E_level` or `N_level` must provide stronger observability contracts, stricter falsification blocks, and a reproducibility plan.
Otherwise it must be treated as baseline level.

## 8. Failure modes

An encoding is considered failed if:

### 8.1 Instability under admissible perturbations

Small admissible perturbations of measurement choices produce qualitatively unstable conclusions.

### 8.2 Conflict with established results

The encoding contradicts established theorems or hard constraints in the cited field under the declared interpretation.

### 8.3 Non auditability

Required identifiers, probe sets, weights, thresholds, and version tags are missing or ambiguous.

## 9. Versioning and non mutation

### 9.1 Semantic changes require a new version

Any non trivial change to encoding choices, probe sets, normalization rules, thresholds, or weights defines a new encoding version and must be logged with explicit version tags and hashes.

### 9.2 Program level changes

Any change that affects multiple problems must be made here or in charter level documents, not by silent local edits to individual problem files.

## 10. Notation and symbol overloading (effective-layer documents)

This section specifies how notation in TU effective-layer documents is interpreted when symbols are reused or appear ambiguous.

### 10.1 Canonical names vs local shorthands

1. For each problem entry, the **canonical objects** are the ones that appear as:

   * named fields in the header metadata block (for example `Field_type`, `Tension_type`, `E_level`, `N_level`), and
   * explicitly defined observables and functionals in the encoding block (for example `DeltaS_total(m)`, `Tension_FE(m)`, `Tension_OOD(m)`).

2. Single-letter or short LaTeX-style symbols that appear only inside the narrative text of a problem entry are treated as **local shorthands**.
   They are editorial devices for readability.
   They do not, by themselves, introduce new TU wide objects.

3. When a local shorthand symbol conflicts with an existing canonical name or with a standard symbol in a cited reference, the canonical name and the cited reference take precedence.
   The shorthand is interpreted as a non binding notation choice and not as a separate object.

### 10.2 Local namespaces for each problem entry

1. Each problem entry `QXXX` is interpreted as having its own **local notation namespace** at the effective layer.

   * Canonical names inside `QXXX` define objects only for that problem.
   * Reusing the same letter or shorthand in a different entry `QYYY` does not imply that the objects are identical, unless this is explicitly stated.

2. Cross-problem arguments and constructions must refer to objects by their canonical names
   (for example `DeltaS_ref_Q130`, `Tension_OOD_Q130`, `Tension_FE_Q131`)
   or by explicit textual descriptions, not by bare single-letter symbols.

3. Any TU document that needs to identify the same object across multiple problems must do so by:

   * citing the problem IDs, and
   * using the canonical names given in the corresponding encoding blocks.

### 10.3 Resolution of intra document symbol collisions

1. Within a single problem entry, if the same symbol appears to be used for two different purposes, the following resolution rule applies:

   * the meaning given in the first explicit formal definition in the encoding block is treated as the **binding definition** for that symbol within the effective-layer encoding;
   * later uses of the same symbol that are inconsistent with this binding definition are treated as editorial notation errors and do not change the effective-layer encoding.

2. When such collisions are detected, they should be:

   * documented in errata or future revisions, and
   * corrected by renaming the local shorthand or by replacing it with the canonical name.

3. Until a revision is published, downstream work must:

   * follow the binding definition from the encoding block for any formal reasoning, and
   * ignore conflicting shorthand uses when they would otherwise create ambiguity.

### 10.4 Protection against notation based attacks

1. Falsification, criticism, or replication of TU encodings must address:

   * the canonical objects and constraints as defined in the header metadata and encoding blocks, and
   * the experiments and invariants that refer to those objects.

2. Attacks that rely solely on:

   * ambiguous or inconsistent single-letter shorthands, or
   * purely typographical symbol reuse without a change in the canonical definitions,
     are treated as notation-level issues.
     They can motivate editorial corrections but do not, by themselves, falsify the underlying TU encoding.

3. This clause does not protect genuinely inconsistent or contradictory canonical definitions.
   If a header, encoding block, or experiment block defines incompatible invariants for the same canonical object, this is a real defect and must be treated as a substantive problem, not as a notation issue.
