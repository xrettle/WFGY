<!-- QUESTION_ID: TU-Q070 -->
# Q070 · Universal theory of soft matter self assembly

## 0. Header metadata

```txt
ID: Q070
Code: BH_CHEM_SOFTMATTER_L3_070
Domain: Chemistry / Materials
Family: Soft matter and self assembly
Rank: S
Projection_dominance: P
Field_type: dynamical_field
Tension_type: thermodynamic_tension
Status: Open
Semantics: hybrid

EncodingClass: E_SOFT
EncodingKey: Q070_SOFT_CORE_V1
LibraryKey: Q070_SOFT_LIB_V1
WeightKey: Q070_SOFT_WEIGHTS_V1
RefinementKey: Q070_SOFT_REFINE_V1

E_level: E1
N_level: N2
Last_updated: 2026-01-30
````

---

## 0. Effective layer disclaimer

All content in this entry is written strictly at the **effective layer** of the Tension Universe (TU) framework, relative to a fixed soft matter encoding.

* There is a fixed admissible encoding class

  ```txt
  E_SOFT = { E : admissible encodings for soft-matter self assembly }
  ```

* For Q070 we fix once and for all a single encoding

  ```txt
  E in E_SOFT
  ```

  with keys recorded in the header:

  ```txt
  EncodingKey(E)      = Q070_SOFT_CORE_V1
  LibraryKey(E)       = Q070_SOFT_LIB_V1
  WeightKey(E)        = Q070_SOFT_WEIGHTS_V1
  RefinementKey(E)    = Q070_SOFT_REFINE_V1
  ```

* All state spaces, observables, mismatch scores, tension functionals, worlds, and experiments in this document are defined **relative to this fixed encoding E**. No parameter is tuned per system unless this is explicitly declared as an encoding change, which would correspond to choosing a different `E'` and different keys.

This document respects the following effective layer boundaries.

1. It only introduces:

   * state spaces at the level of semantic soft matter scenarios,
   * observables and fields,
   * invariants, mismatch scores, and tension functionals,
   * singular sets and domain restrictions,
   * counterfactual worlds defined as patterns of these observables.

2. It does **not** introduce or assume:

   * any explicit TU axiom system or deep TU generating rules,
   * any microscopic Hamiltonian or dynamical law,
   * any constructive mapping from raw microscopic data to internal TU fields.

3. It does **not** claim that:

   * Q070 is solved in the canonical mathematical or physical sense,
   * any new theorem about soft matter is proved,
   * the worlds described in Section 5 correspond to the actual universe.

The purpose of this page is more modest and precise:

* It specifies how Q070 can be encoded as an **effective layer tension problem** for a fixed encoding `E in E_SOFT`.
* It defines observables and experiments that can **falsify or refine particular encodings E**.
* It provides reusable components and training signals for AI and WFGY systems, without exposing or relying on any deeper TU generative rules.

---

## 1. Canonical problem and status

### 1.1 Canonical statement

Soft matter systems are made of many interacting building blocks that are neither rigid solids nor ideal gases. Examples include colloids, surfactant solutions, block copolymers, liquid crystals, membranes, gels, and complex emulsions. In these systems, large scale structures such as micelles, vesicles, lamellae, bicontinuous phases, or colloidal crystals emerge spontaneously from local interactions in a thermal environment.

The canonical problem behind Q070 can be stated as:

> Does there exist a finite, well structured family of effective fields, observables, and tension functionals that can describe self assembly across a wide range of soft matter systems, such that:
>
> 1. Low tension states correspond to the experimentally observed self assembled structures, and
> 2. High tension states are systematically disfavored or unstable,
>
> without referring to microscopic generative rules for each specific chemistry?

This is not a request for a single microscopic Hamiltonian. It is a request for a universal effective description that unifies how soft matter systems select, stabilize, and transition between self assembled structures.

### 1.2 Status and difficulty

At present, soft matter self assembly is described by a patchwork of models.

* Phenomenological free energy functionals tailored to specific systems.
* Scaling theories that apply in particular asymptotic regimes.
* Numerical simulations with detailed force fields or coarse grained particles.
* Empirical design rules used in practice for surfactants, block copolymers, and colloids.

There is no commonly accepted finite library of effective fields and invariants that:

* works across chemically diverse systems,
* makes clear which structures are generic and which are system specific,
* separates the roles of thermodynamics, kinetics, and history dependence in a unified way.

The difficulty is partly conceptual. Self assembly in soft matter:

* lives at intermediate scales where microscopic details matter but universal behavior also emerges,
* involves rugged free energy landscapes with many metastable states,
* is sensitive to control parameters such as temperature, solvent quality, and confinement.

Q070 does not ask for a complete microscopic derivation. It asks whether a universal effective description at the level of observables and tension functionals can be constructed and tested.

### 1.3 Role in the BlackHole project

Within the BlackHole S problem collection, Q070 serves as:

1. The reference node for **thermodynamic_tension** problems in soft condensed matter. It is the canonical example where free energy like quantities, entropy, and morphology interact in a complex but structured way.
2. A bridge between microscopic interaction problems such as Q061 on the nature of chemical bonds in strongly correlated systems and macroscopic biological or geophysical problems that reuse self assembly concepts.
3. A template for encoding systems where universality is expected but not yet rigorously formulated. It shows how to express universality as a tension principle at the effective layer with explicit falsifiability.

### References

1. P. G. de Gennes, *Scaling Concepts in Polymer Physics*, Cornell University Press, 1979.
2. P. M. Chaikin and T. C. Lubensky, *Principles of Condensed Matter Physics*, Cambridge University Press, 1995.
3. J. N. Israelachvili, *Intermolecular and Surface Forces*, Academic Press, 3rd edition, 2011.
4. G. M. Whitesides and B. Grzybowski, "Self assembly at all scales", *Science* 295, 2418–2421, 2002.
5. D. Andelman and S. A. Safran, and related review chapters on soft condensed matter and self assembly in standard collections.

---

## 2. Position in the BlackHole graph

This block records Q070 as a node in the BlackHole graph and lists upstream, downstream, parallel, and cross domain edges with one line reasons pointing to concrete components or tension types. All references are at the effective layer and do not assume any particular microscopic model.

### 2.1 Upstream problems

These problems provide prerequisites or tools that Q070 relies on at the effective layer.

* Q061 (BH_CHEM_BOND_NATURE_L3_061)
  Reason: supplies the effective interaction vocabulary that is coarse grained into the building block and interaction library used by the `SoftMatter_TensionFunctional` component.

* Q064 (BH_CHEM_GLASS_TRANS_L3_064)
  Reason: provides methods to handle slow dynamics, metastability, and rugged energy landscapes that appear in soft matter tension landscapes.

* Q068 (BH_CHEM_PREBIOTIC_NETWORK_L3_068)
  Reason: motivates a general self assembly framework, since prebiotic networks require soft matter structures such as compartments and gels that Q070 must be able to encode.

* Q032 (BH_PHYS_QTHERMO_L3_032)
  Reason: anchors thermodynamic_tension invariants such as free energy and entropy that Q070 reuses in its effective free energy like observable.

### 2.2 Downstream problems

These problems directly reuse Q070 components or depend on its tension structure.

* Q068 (BH_CHEM_PREBIOTIC_NETWORK_L3_068)
  Reason: reuses `SoftMatter_TensionFunctional` and `SelfAssembly_ExperimentTemplate` to model formation and stability of prebiotic compartments and reaction networks.
  Note: Q068 appears in both upstream and downstream roles. It motivates soft matter encodings and later consumes the Q070 components once defined.

* Q071 (BH_BIO_ORIGIN_LIFE_L3_071)
  Reason: uses `SoftMatter_MorphologyDescriptorLibrary` to classify proto cell like structures and test whether early cellular morphologies fall into a small set of universality classes.

* Q078 (BH_BIO_DEVELOPMENTAL_L3_078)
  Reason: treats developmental patterns as self assembled morphologies and reuses soft matter tension ideas to relate control parameters to phenotypic structures.

* Q095 (BH_EARTH_BIODIVERSITY_L3_095)
  Reason: interprets ecosystem re assembly and habitat structuring as soft matter like self assembly, borrowing `SelfAssembly_ExperimentTemplate` at a macro scale.

### 2.3 Parallel problems

Parallel nodes share similar tension types but do not directly reuse Q070 components.

* Q063 (BH_CHEM_PROTEIN_FOLDING_L3_063)
  Reason: both Q063 and Q070 involve complex free energy landscapes and thermodynamic_tension between local interactions and global structure, but one focuses on single macromolecules and the other on mesoscale assemblies.

* Q064 (BH_CHEM_GLASS_TRANS_L3_064)
  Reason: both problems involve competition between ordering and frustration under thermodynamic_tension, yet glasses and self assembled phases have distinct observables and universality structures.

* Q079 (BH_BIO_ORIGIN_EUKARYOTES_L3_079)
  Reason: origin of eukaryotic cells requires membrane and organelle self assembly that is structurally parallel to soft matter pattern formation without directly depending on Q070 components.

### 2.4 Cross domain edges

Cross domain edges link Q070 to problems in other domains that can reuse its components.

* Q032 (BH_PHYS_QTHERMO_L3_032)
  Reason: shares thermodynamic_tension invariants and provides a reference for how free energy like quantities and entropy should behave in consistent encodings.

* Q095 (BH_EARTH_BIODIVERSITY_L3_095)
  Reason: treats biodiversity patterns as large scale self assembled structures, reusing the notion of universality classes and tension driven pattern selection.

* Q121 (BH_AI_ALIGNMENT_L3_121)
  Reason: alignment architectures can be seen as self assembled agentic structures. Q070 supplies a physical analogy and a tension based functional for modular assembly and stability.

---

## 3. Tension Universe encoding (effective layer)

All content in this block is at the effective layer and **parameterized by the fixed encoding `E in E_SOFT`**.

We only describe:

* state spaces and regular domains,
* observables and fields,
* mismatch scores and tension functionals,
* invariants, refinement parameters, and singular sets.

We do not describe any hidden generative rules or how internal TU fields are constructed from raw microscopic data.

### 3.1 State space and encoding parameters

For the fixed encoding `E in E_SOFT` we define a semantic state space

```txt
M(E)
```

with the following effective interpretation.

* Each state

  ```txt
  m in M(E)
  ```

  encodes a coherent soft matter self assembly scenario at a given resolution. It contains:

  * a finite library of building block types and effective interaction motifs,
  * one or more coarse grained fields on a spatial domain,
  * a finite vector of control parameters.

The construction of `m` from microscopic data happens outside TU. The encoding only assumes that observables defined below are well defined for regular states.

**Building block and interaction library**

For each state `m in M(E)` we have:

```txt
L_blocks(m; E)
L_int(m; E)
```

where:

* `L_blocks(m; E)` is a finite set describing building block types such as surfactant species, polymer blocks, colloidal particles, with coarse attributes such as size, shape, and valence labels.
* `L_int(m; E)` is a finite set of effective pair or few body interaction motifs between elements of `L_blocks(m; E)` such as attraction, repulsion, directional bonding, and excluded volume, each with a small number of coarse parameters.

These are treated as encoded summaries, not as generative rules.

**Coarse grained fields**

On a spatial domain `Omega` that may be a box or other bounded region, the encoding defines coarse grained fields

```txt
phi_i(m; E, x)
Q_alpha(m; E, x)
```

where:

* `phi_i(m; E, x)` denotes coarse grained concentration or volume fraction fields for species or building block categories indexed by `i`.
* `Q_alpha(m; E, x)` denotes local order parameter fields indexed by `alpha`, such as

  * scalar composition order parameters,
  * vector or tensor order parameters in liquid crystals,
  * local indicators of micellar, lamellar, or bicontinuous morphology.

The index sets for `i` and `alpha` are finite and determined by `LibraryKey(E)`.

**Control parameters**

The encoding associates to each state a finite dimensional vector of control parameters

```txt
c_ctrl(m; E)
```

Examples include temperature, solvent quality indicators, average concentration, shear rate, and boundary conditions.

### 3.2 Effective observables and mismatch scores

All observables in this block are defined for regular states and depend on the fixed encoding `E`.

1. Effective free energy like functional

   ```txt
   F_eff(m; E)
   ```

   A scalar observable summarizing the effective free energy landscape associated with state `m`. It is not required to be derived from a specific microscopic model but must behave consistently under refinement of the encoding.

2. Microscopic mismatch observable

   ```txt
   DeltaS_micro(m; E, k)
   ```

   * A nonnegative scalar measuring the mismatch between the encoded building block and interaction library of `m` at refinement level `k` and a reference library associated with a chosen universality class under encoding `E`.
   * Properties:

     * `DeltaS_micro(m; E, k) >= 0`.
     * `DeltaS_micro(m; E, k) = 0` if the library of `m` matches the chosen reference library within the resolution specified by `RefinementKey(E)` at level `k`.

3. Morphology descriptor observable

   ```txt
   M_desc(m; E, k)
   ```

   * A finite dimensional vector of morphology descriptors at refinement level `k`, such as:

     * domain sizes and shapes,
     * symmetry indicators such as lamella, hexagonal, cubic,
     * correlation lengths,
     * defect densities.

   These are computed from the fields `phi_i(m; E, x)` and `Q_alpha(m; E, x)` using fixed rules specified by `LibraryKey(E)`.

4. Morphology mismatch observable

   ```txt
   DeltaS_morph(m; E, k)
   ```

   * A nonnegative scalar measuring the deviation of `M_desc(m; E, k)` from a reference morphology profile for a given universality class at level `k`.
   * Properties:

     * `DeltaS_morph(m; E, k) >= 0`.
     * `DeltaS_morph(m; E, k) = 0` if morphology descriptors match the reference profile within prescribed tolerances.

5. Combined soft matter mismatch and tension

   The weight key `WeightKey(E)` specifies fixed constants

   ```txt
   w_micro(E) > 0
   w_morph(E) > 0
   w_micro(E) + w_morph(E) = 1
   ```

   For each refinement level `k` we define the combined mismatch

   ```txt
   DeltaS_SM(m; E, k) =
       w_micro(E) * DeltaS_micro(m; E, k) +
       w_morph(E) * DeltaS_morph(m; E, k)
   ```

   and set the soft matter tension functional equal to this combined mismatch:

   ```txt
   Tension_SM(m; E, k) := DeltaS_SM(m; E, k)
   ```

   The equality is a choice at the effective layer. It records that in this encoding the core soft matter tension is entirely captured by the weighted sum of microscopic and morphological mismatches.

### 3.3 Effective tension tensor

The TU core supplies a generic semantic tension tensor. For Q070 and the fixed encoding `E` we consider an effective tensor

```txt
T_ij(m; E) =
    S_i(m; E) * C_j(m; E) *
    Tension_SM(m; E, k_ref(E)) *
    lambda(m; E) * kappa_soft(E)
```

where:

* `S_i(m; E)` is a source like factor that describes how strongly the ith semantic source component is engaged in this scenario. Examples include theoretical expectations, design targets, or constraints imposed by a broader program.
* `C_j(m; E)` is a receptivity like factor that encodes how sensitive the jth downstream component such as a design decision or experimental program is to mismatch in soft matter behavior.
* `Tension_SM(m; E, k_ref(E))` is the soft matter tension at a reference refinement level `k_ref(E)` recorded in `RefinementKey(E)`.
* `lambda(m; E)` is a convergence state factor constrained to a fixed bounded range such as `[0, 1]`, indicating whether local reasoning is convergent, recursive, divergent, or chaotic.
* `kappa_soft(E)` is a fixed coupling constant that sets the overall scale of soft matter tension in this encoding.

The index sets for `i` and `j` are finite and determined by the encoding. Their internal structure is not specified at the effective layer.

### 3.4 Invariants, refinement, and stability

The refinement key `RefinementKey(E)` specifies a discrete refinement parameter

```txt
k = 1, 2, 3, ...
```

with the following properties.

* Larger `k` corresponds to:

  * more detailed building block and interaction libraries,
  * higher spatial resolution or richer sets of fields,
  * more detailed morphology descriptors.

* Refinements are monotone. Moving from `k` to `k + 1` can only increase the amount of resolved detail. It cannot change the underlying physical system.

For each `k` and state `m` we can evaluate

```txt
DeltaS_micro(m; E, k)
DeltaS_morph(m; E, k)
DeltaS_SM(m; E, k)
Tension_SM(m; E, k)
```

using the definitions above.

**Morphology universality invariant**

We define a morphology universality invariant

```txt
I_univ(m; E, k) =
    norm( M_desc(m; E, k) - M_ref(E, k) )
```

where:

* `M_desc(m; E, k)` is the morphology descriptor vector at refinement level `k`,
* `M_ref(E, k)` is a reference morphology descriptor vector for the universality class under encoding `E` at level `k`,
* `norm` is a fixed norm on the descriptor space, chosen once for this encoding and recorded in `LibraryKey(E)`.

**Encoding stability invariant**

We define an encoding stability invariant

```txt
I_stable(m; E, k, k') =
    | DeltaS_SM(m; E, k) - DeltaS_SM(m; E, k') |
```

for refinement levels `k <= k'`.

In a well behaved encoding `E`, `I_stable(m; E, k, k')` should become small when both `k` and `k'` are large for physically meaningful states. Stability is evaluated in later blocks and experiments.

### 3.5 Singular set and regular domain

Some states may encode inconsistent or incomplete data, leading to undefined or divergent observables. We define the soft matter singular set for encoding `E` as

```txt
S_sing_soft(E) :=
    { m in M(E) :
      DeltaS_SM(m; E, k_ref(E)) is undefined or not finite, or
      F_eff(m; E) is undefined or not finite, or
      M_desc(m; E, k_ref(E)) is not well defined }
```

All soft matter tension analysis for Q070 is restricted to the regular domain

```txt
M_reg(E) := M(E) \ S_sing_soft(E)
```

Whenever a protocol attempts to evaluate `DeltaS_SM(m; E, k)` or `Tension_SM(m; E, k)` for a state in `S_sing_soft(E)`, the result is treated as **out of domain**. It is not counted as evidence for or against the universality claims and must be logged separately.

---

## 4. Tension principle for this problem

This block describes how Q070 is framed as a tension problem within TU at the effective layer for the fixed encoding `E`.

### 4.1 Core soft matter tension functional

For each refinement level `k` and regular state `m in M_reg(E)` the core soft matter tension functional is

```txt
Tension_SM(m; E, k) =
    DeltaS_SM(m; E, k) =
        w_micro(E) * DeltaS_micro(m; E, k) +
        w_morph(E) * DeltaS_morph(m; E, k)
```

with weights `w_micro(E)` and `w_morph(E)` recorded in `WeightKey(E)` and satisfying

```txt
w_micro(E) > 0
w_morph(E) > 0
w_micro(E) + w_morph(E) = 1
```

Properties:

* `Tension_SM(m; E, k) >= 0` for all regular states `m`.
* If both mismatch terms are small at a given `k`, then `Tension_SM(m; E, k)` is small.
* If either mismatch term is large at a given `k`, then `Tension_SM(m; E, k)` is large.

The choice of weights, reference libraries, and descriptor norms is made once at the encoding level and cannot be tuned per system inside a single encoding `E`.

### 4.2 Universality as a low tension principle

At the effective layer, and for the fixed encoding `E`, the universality question for soft matter self assembly is expressed as follows.

There exists an admissible set of soft matter systems `S_scope` such that for each system

```txt
S in S_scope
```

there is a family of regular states

```txt
{ m_S(E, k) in M_reg(E) }_{k >= k_min(E)}
```

with the properties:

1. **Low tension band**

   There exists a threshold

   ```txt
   epsilon_SM(E) > 0
   ```

   recorded in `WeightKey(E)` such that

   ```txt
   Tension_SM(m_S(E, k); E, k) <= epsilon_SM(E)
   ```

   for all `k >= k_min(E)`.

2. **Refinement stability**

   The encoding stability invariant satisfies

   ```txt
   I_stable(m_S(E, k); E, k, k') is small
   ```

   whenever `k` and `k'` are both large.

3. **Morphology universality**

   For systems `S` that belong to the same universality class under encoding `E`, there exists a bound

   ```txt
   epsilon_univ(E) > 0
   ```

   such that

   ```txt
   I_univ(m_S(E, k); E, k) <= epsilon_univ(E)
   ```

   for all sufficiently large `k`, with a uniform constraint across systems in the class.

Informally, this means that:

* low tension soft matter states approximate observed self assembled structures across detail levels,
* universality classes can be described by reference libraries and morphology profiles that remain stable as more detail is added,
* the encoding `E` organizes soft matter systems in a way that survives refinement.

### 4.3 Failure of universality as persistent high tension

Failure of the universality principle for encoding `E` is expressed as the absence of such low tension families, even when encodings are refined.

If Q070 is false **for encoding `E`**, then for any attempt to define `S_scope` as intended there exists at least one soft matter system `S_star` in scope such that, for every sequence of regular states

```txt
{ m_{S_star}(E, k) }_{k >= k_min(E)}
```

representing `S_star` at higher and higher refinement levels, there is a strictly positive lower bound

```txt
delta_SM(E) > 0
```

with

```txt
Tension_SM(m_{S_star}(E, k); E, k) >= delta_SM(E)
```

for all sufficiently large `k`.

In this case at least one of the following holds.

* Universality classes at the proposed level of coarse graining do not exist under encoding `E`.
* Different systems require incompatible reference libraries or descriptor sets within `E`.
* The same encoding mispredicts morphology in at least one benchmark system even after refinement.

The claim does not assert that no other encoding `E'` in `E_SOFT` can succeed. It only characterizes how failure of universality looks for a fixed encoding.

---

## 5. Counterfactual tension worlds

We describe two counterfactual worlds at the effective layer, both understood **relative to the fixed encoding `E`**.

* World T: a world where a universal soft matter self assembly encoding of the intended scope exists and behaves well for `E`.
* World F: a world where no encoding with the keys of `E` can succeed across the intended scope, although another encoding `E'` could still exist.

The worlds are defined as patterns in observables and tension functionals. They do not assert which world the actual universe occupies.

### 5.1 World T (unified soft matter world, low tension)

World T satisfies the following properties with respect to encoding `E`.

1. Existence of admissible scope

   There is a nonempty scope `S_scope` of soft matter systems with reliable experimental or simulation data, on which encoding `E` is intended to operate.

2. Low tension representation for each system

   For each `S in S_scope` there exists a family of regular states

   ```txt
   { m_S(E, k) }_{k >= k_min(E)}
   ```

   such that

   ```txt
   Tension_SM(m_S(E, k); E, k) <= epsilon_SM(E)
   ```

   for all sufficiently large `k`.

3. Convergence of tension under refinement

   For these families the encoding stability invariant satisfies

   ```txt
   I_stable(m_S(E, k); E, k, k') is small
   ```

   whenever `k` and `k'` are large. Tension values converge as more detail is included.

4. Morphology universality

   For systems believed to be in the same universality class the universality invariant obeys

   ```txt
   I_univ(m_S(E, k); E, k) <= epsilon_univ(E)
   ```

   for all large `k` with a uniform bound across systems.

5. Predictive power

   Changes in control parameters that are known experimentally to induce structural transitions correspond to predictable changes in `Tension_SM`. The encoding identifies moves in parameter space that transfer systems from one low tension morphology band to another.

### 5.2 World F (non unified soft matter world, persistent tension)

World F satisfies the following properties with respect to the same encoding `E`.

1. No single encoding suffices for the intended scope

   For every attempt to define `S_scope` according to the goals of Q070 and the keys of `E`, there exists at least one system

   ```txt
   S_star in S_scope
   ```

   such that for every family of regular states representing `S_star` there is a positive bound

   ```txt
   delta_SM(E) > 0
   ```

   with

   ```txt
   Tension_SM(m_{S_star}(E, k); E, k) >= delta_SM(E)
   ```

   for all sufficiently large `k`.

2. Instability under refinement

   For some systems in scope, the encoding stability invariant fails to converge. There exist states for which

   ```txt
   I_stable(m_S(E, k); E, k, k') remains large
   ```

   even as `k` and `k'` increase, which indicates that the tension assignment is unstable and does not capture a universality structure.

3. Morphology mismatch

   For systems that experimental evidence suggests belong to the same universality class, the quantity `I_univ(m_S(E, k); E, k)` cannot be kept within a small band under the constraints of `E`. The only way to repair this would be to change the encoding class or keys, which is treated as a different encoding `E'`.

4. Broken transfer

   Components that work well in one chemical family fail to predict or organize self assembly in another. Fixing this would again require changing `E` rather than tuning parameters inside `E`.

### 5.3 Interpretive note

These worlds do not claim that we know which world we inhabit nor that Q070 is resolved. They only specify what patterns in soft matter observables and tension functionals would correspond to a successful or failed universal encoding for the fixed encoding `E`.

The distinction is purely at the effective layer. It does not depend on specifying microscopic models or TU deep axioms and it remains compatible with multiple physical interpretations.

---

## 6. Falsifiability and discriminating experiments

This block defines experiments and protocols at the effective layer which can:

* test whether a particular encoding `E` for Q070 is coherent,
* discriminate between different encodings in `E_SOFT`,
* provide evidence for or against the existence of a useful universal description for soft matter self assembly.

Falsifying an encoding `E` is not the same as resolving the canonical problem Q070.

### Experiment 1: Cross system universality test

**Goal**

Test whether a single admissible encoding `E in E_SOFT` with fixed descriptor libraries and weights can assign low soft matter tension to multiple benchmark systems in different chemical families.

**Setup**

* Fix a single encoding

  ```txt
  E in E_SOFT
  ```

  with keys specified in the header. This fixes:

  * a building block and interaction library schema,
  * a morphology descriptor library,
  * weights `w_micro(E)`, `w_morph(E)`,
  * reference profiles `M_ref(E, k)` and thresholds `epsilon_SM(E)`, `epsilon_univ(E)`.

* Select at least three benchmark soft matter systems with well documented self assembly behavior, for example:

  * surfactant micelles and vesicles,
  * block copolymer lamellae or cylinders,
  * charged colloids forming crystals or glasses.

* For each system, identify a range of control parameters where the self assembled structures are known and stable.

**Protocol**

1. For each system and each chosen point in control parameter space, construct a regular state

   ```txt
   m in M_reg(E)
   ```

   encoding:

   * an instance of `L_blocks(m; E)` and `L_int(m; E)`,
   * fields `phi_i(m; E, x)` and `Q_alpha(m; E, x)` at an initial refinement level `k`,
   * control parameters `c_ctrl(m; E)`.

   The construction from experimental or simulated data happens outside TU.

2. Compute

   ```txt
   DeltaS_micro(m; E, k)
   DeltaS_morph(m; E, k)
   Tension_SM(m; E, k)
   ```

   for each state.

3. Repeat the computations at several higher refinement levels `k' > k` by increasing descriptor detail or spatial resolution, while keeping the encoding `E` and all weights and reference profiles fixed.

4. Record the distributions of `Tension_SM(m; E, k)` values for each system and refinement level.

**Metrics**

* For each system, the fraction of states with `Tension_SM(m; E, k)` below `epsilon_SM(E)`.
* The maximum observed `Tension_SM(m; E, k)` over all systems at each refinement level.
* The encoding stability metric `I_stable(m; E, k, k')` for representative states.

**Falsification conditions**

The encoding `E` is considered falsified for cross system universality if either of the following holds.

1. For at least one benchmark system and for all families of regular states considered, `Tension_SM(m; E, k)` remains above a threshold `delta_SM(E)` for all sufficiently large `k`, where `delta_SM(E)` is significantly larger than the intended low tension band width.

2. For systems that are experimentally known to share similar universal morphologies, the quantity `I_univ(m; E, k)` cannot be made simultaneously small across those systems under the fixed encoding `E`, without violating the constraint that weights and reference profiles are chosen once for `E` and not tuned per system.

**Semantics implementation note**

All observables in this experiment are treated using the **hybrid semantics** declared in the metadata. Discrete building block and interaction libraries are coupled to continuous or coarse grained fields and descriptors.

**Boundary note**

Falsifying a TU encoding `E` for Q070 by this experiment does not solve the canonical problem. It rejects a specific proposal for universality but does not rule out the existence of another successful encoding `E'`.

---

### Experiment 2: Forward design and reprogramming test

**Goal**

Evaluate whether a Q070 encoding `E` that appears coherent can guide forward design of self assembled structures and predict reprogramming paths in control parameter space.

**Setup**

* Fix the same encoding `E` and keys as in Experiment 1.

* Choose one soft matter system where experimental or simulation control is available, for example:

  * a surfactant system where concentration, temperature, and salt content can be tuned, or
  * a block copolymer system where block lengths and solvent quality can be varied.

* Define a set of target morphologies such as micelles, vesicles, lamellae, bicontinuous phases.

* Use encoding `E` to map these targets to regions in the space of building block libraries, interaction motifs, and control parameters.

**Protocol**

1. For each target morphology, define a family of hypothetical regular states

   ```txt
   m_target(E, k) in M_reg(E)
   ```

   at an initial refinement level `k`, chosen to satisfy

   ```txt
   Tension_SM(m_target(E, k); E, k) <= epsilon_SM(E)
   ```

   according to encoding `E`.

2. Project these hypothetical states back into experimentally controllable parameters such as surfactant ratios, temperature, and salt concentration to obtain design points for each target morphology.

3. Perform experiments or simulations at those design points, and characterize the resulting self assembled structures using the same descriptor library that defines `M_desc(m; E, k)`.

4. Encode the observed structures into new regular states

   ```txt
   m_obs(E, k')
   ```

   at equal or higher refinement level and compute `Tension_SM(m_obs(E, k'); E, k')`.

5. Compare the predicted low tension regions and morphologies with the observed ones.

**Metrics**

* **Design success**. Fraction of design points where the observed morphology matches the target within predefined descriptor tolerances.
* **Tension alignment**. Distribution of `Tension_SM(m_obs(E, k'); E, k')` for successful and unsuccessful design points.
* **Robustness**. Sensitivity of outcomes to small perturbations in control parameters around design points.

**Falsification conditions**

The encoding `E` is considered falsified for forward design if:

1. A large fraction of design points that lie inside the predicted low tension regions fail to produce the target morphology, and this failure persists across modest refinements of the encoding and descriptors.

2. The observed states `m_obs(E, k')` corresponding to successful morphologies have `Tension_SM(m_obs(E, k'); E, k')` significantly larger than the intended low tension band, while other states with high predicted tension exhibit acceptable morphologies. This indicates systematic misalignment between tension and actual self assembly outcomes.

**Semantics implementation note**

The experiment uses the same hybrid semantics as declared in the metadata. Discrete control parameters and building block labels are combined with continuous descriptors of morphology.

**Boundary note**

Falsifying a TU encoding `E` for Q070 in forward design does not rule out the existence of another encoding `E'` that can succeed. It only rejects the specific configuration determined by the keys of `E`.

---

## 7. AI and WFGY engineering spec

This block explains how Q070 can be used as an engineering module in AI systems within the WFGY framework, while respecting the effective layer and the fixed encoding `E`.

All signals and architectural patterns below are defined **relative to the encoding `E in E_SOFT`** and its keys.

### 7.1 Training signals

We define several training signals derived from Q070 observables under encoding `E`.

1. `signal_soft_tension`

   * Definition. A scalar signal equal to `Tension_SM(m; E, k)` for internal states `m` inferred from the model’s representation of a soft matter scenario at refinement level `k` consistent with `RefinementKey(E)`.
   * Purpose. Encourage the model to favor internal representations that place realistic self assembled structures into low tension regions and unrealistic ones into high tension regions.

2. `signal_morphology_universality`

   * Definition. A penalty signal proportional to `I_univ(m; E, k)` for chosen systems and refinement levels.
   * Purpose. Encourage the model to recognize and encode cross system similarities in morphology as belonging to the same universality class.

3. `signal_encoding_stability`

   * Definition. A penalty proportional to `I_stable(m; E, k, k')` for pairs of refinement levels applied to similar internal representations.
   * Purpose. Discourage internal encodings where small changes in resolution or context induce large and unmotivated changes in assigned tension.

4. `signal_design_consistency`

   * Definition. A signal comparing predicted low tension design points for self assembly with outcomes from a replay buffer of simulated or experimental results, all encoded using `E`.
   * Purpose. Align tension based design predictions with observed success and failure cases.

Changing the encoding from `E` to another `E'` changes the meaning of these signals and requires recalibration.

### 7.2 Architectural patterns

We outline reusable module patterns parameterized by encoding `E`.

1. `SoftMatterTensionHead`

   * Role. A module that takes internal embeddings of a soft matter problem and outputs:

     * an estimate of `Tension_SM(m; E, k_ref(E))`,
     * approximate components `DeltaS_micro(m; E, k_ref(E))` and `DeltaS_morph(m; E, k_ref(E))`.

   * Interface.

     * Inputs. Encoded descriptions of building blocks, interactions, control parameters, and morphology summaries compatible with `LibraryKey(E)`.
     * Outputs. A scalar tension estimate and a small vector of mismatch components.

   * Use. Attached as an auxiliary head to large models to guide reasoning about soft matter based on tension.

2. `SelfAssemblyPlanner`

   * Role. A module that proposes sequences of parameter changes intended to drive a system from high tension states to low tension states under `E`.

   * Interface.

     * Inputs. Current encoded state `m in M_reg(E)` and constraints on allowed parameter moves.
     * Outputs. Candidate sequences of parameter adjustments or design modifications.

   * Use. Supports forward design tasks where the goal is to reach low tension self assembled structures.

3. `UniversalityClassifier`

   * Role. A module that assigns inferred soft matter scenarios to universality classes based on `M_desc(m; E, k)` and tension patterns.

   * Interface.

     * Inputs. Compressed descriptors and tension related features at levels specified by `RefinementKey(E)`.
     * Outputs. Class labels or soft assignments to universality classes.

   * Use. Reused in Q068, Q071, and Q078 to connect physical soft matter patterns to higher level biological or chemical questions.

### 7.3 Evaluation harness

We propose an evaluation harness for testing AI systems enhanced with Q070 components under encoding `E`.

1. Task selection

   The benchmark set should include:

   * question answering about known self assembly behavior across different soft matter systems,
   * design problems where target morphologies are specified and parameter suggestions are requested,
   * explanation tasks that require connecting local interactions to global morphology.

2. Conditions

   * Baseline condition.

     The model operates without Q070 specific tension heads or signals. It receives descriptions in natural language or raw structural form.

   * TU augmented condition.

     The model uses the `SoftMatterTensionHead`, `SelfAssemblyPlanner`, and Q070 derived training signals tied to encoding `E`.

3. Metrics

   * **Accuracy**. Correctness of answers to factual and conceptual questions about soft matter self assembly.
   * **Design success**. Fraction of proposed designs that are validated as producing intended morphologies in simulation or from known examples.
   * **Consistency**. Frequency of internally inconsistent statements about how changes in control parameters affect morphology.
   * **Robustness**. Stability of answers under small prompt changes that do not alter the physical scenario.

### 7.4 Sixty second reproduction protocol

This protocol allows external users to experience Q070 based structuring in an AI system.

* Baseline setup.

  * Prompt. Ask the AI to explain how self assembly works in at least three soft matter systems such as surfactant micelles, block copolymers, and colloids and how their behaviors are related.
  * Observation. Record whether the explanation is fragmented, system specific, or lacking clear unifying concepts.

* TU encoded setup.

  * Prompt. Ask the same question but instruct the AI to:

    * describe each system in terms of building blocks, interactions, morphology descriptors, and control parameters, and
    * organize the explanation using soft matter tension and universality classes derived from Q070 under encoding `E`.

  * Observation. Record whether the explanation now:

    * highlights shared descriptors and control knobs,
    * identifies low tension regions where self assembly is robust,
    * separates universality from system specific details.

* Comparison metric.

  Use a simple rubric to rate:

  * which explanation more clearly identifies universal aspects of self assembly,
  * which explanation is more internally consistent about parameter effects,
  * which explanation better supports forward design reasoning.

* What to log.

  * Prompts, full responses, any intermediate descriptors or tension estimates inferred by the system, and evaluation scores.
  * These logs can be inspected to improve encoding `E` or to motivate a new encoding `E'`, without exposing any deep TU generative rules.

---

## 8. Cross problem transfer template

This block describes the reusable components produced by Q070 for encoding `E` and how they transfer to other BlackHole problems.

### 8.1 Reusable components produced by this problem

1. Component name: `SoftMatter_TensionFunctional`

   * Type. `functional`.

   * Minimal interface.

     * Inputs.

       * a soft matter descriptor set consisting of:

         * a building block and interaction summary compatible with `L_blocks` and `L_int` under `E`,
         * morphology descriptors `M_desc(m; E, k)`,
         * control parameters `c_ctrl(m; E)`.

     * Output.

       * scalar `tension_value` equal to `Tension_SM(m; E, k_ref(E))`,
       * optional breakdown into `DeltaS_micro(m; E, k_ref(E))` and `DeltaS_morph(m; E, k_ref(E))`.

   * Preconditions.

     * descriptors must be drawn from the fixed encoding library defined by `LibraryKey(E)`,
     * the state must be in `M_reg(E)` so that observables are finite.

2. Component name: `SoftMatter_MorphologyDescriptorLibrary`

   * Type. `field / observable library`.

   * Minimal interface.

     * Inputs.

       * coarse grained fields `phi_i(m; E, x)`, `Q_alpha(m; E, x)`,
       * domain geometry and boundary conditions.

     * Output.

       * a finite dimensional descriptor vector including:

         * domain sizes and shapes,
         * symmetry labels,
         * correlation lengths,
         * defect statistics where applicable.

   * Preconditions.

     * spatial fields must be defined over a bounded domain at specified resolution,
     * descriptor extraction rules must be applied consistently across systems and be compatible with `RefinementKey(E)`.

3. Component name: `SelfAssembly_ExperimentTemplate`

   * Type. `experiment_pattern`.

   * Minimal interface.

     * Inputs.

       * a class of soft matter systems in scope,
       * ranges of control parameters,
       * a set of target morphologies.

     * Output.

       * a set of experiments structured as:

         * initial high tension states,
         * sequences of parameter changes,
         * expected transitions toward low tension self assembled states under encoding `E`.

   * Preconditions.

     * control parameters must be experimentally or numerically tunable over the specified ranges,
     * morphology characterization tools compatible with `M_desc(m; E, k)` must exist to validate outcomes.

### 8.2 Direct reuse targets

1. Target. Q068 (BH_CHEM_PREBIOTIC_NETWORK_L3_068)

   * Reused components.

     * `SoftMatter_TensionFunctional`,
     * `SelfAssembly_ExperimentTemplate`.

   * Why it transfers.

     Prebiotic compartments, gels, and reactive networks require soft matter self assembly of lipids, polymers, or minerals. Tension principles and experiment patterns carry over.

   * What changes.

     The descriptor library is extended with chemical reactivity and permeability observables, but the core tension structure remains.

2. Target. Q071 (BH_BIO_ORIGIN_LIFE_L3_071)

   * Reused component.

     * `SoftMatter_MorphologyDescriptorLibrary`.

   * Why it transfers.

     Origin of life scenarios rely on soft matter structures such as vesicles and proto cells. Morphology descriptors can be reused to classify early cellular structures.

   * What changes.

     Additional biological observables such as encapsulated volume fractions and stability under division are attached to the descriptors.

3. Target. Q078 (BH_BIO_DEVELOPMENTAL_L3_078)

   * Reused components.

     * `SoftMatter_TensionFunctional`,
     * `SoftMatter_MorphologyDescriptorLibrary`.

   * Why it transfers.

     Developmental patterning can be viewed as a self assembly process in active soft matter. The same tension framework can be adapted to driven systems.

   * What changes.

     Control parameters now include genetic and biochemical fields, and tension includes contributions from active processes in addition to thermodynamic ones.

4. Target. Q095 (BH_EARTH_BIODIVERSITY_L3_095)

   * Reused component.

     * `SelfAssembly_ExperimentTemplate`.

   * Why it transfers.

     Large scale biodiversity patterns can be modeled as assemblies of interacting species and habitats. Experiment patterns help design interventions to re assemble ecosystems after collapse.

   * What changes.

     Building blocks become species and habitat units, and descriptors involve diversity and spatial clustering rather than molecular morphology.

---

## 9. TU roadmap and verification levels

This block situates Q070 on the TU verification ladder for encoding `E` and identifies next measurable steps.

### 9.1 Current levels

* E_level. `E1`.

  * Achieved.

    * A coherent effective encoding of soft matter self assembly for encoding `E` is specified in terms of state space, observables, mismatch measures, and tension functionals.
    * Explicit experiments are defined with falsification conditions that can reject the particular encoding `E`.
    * A singular set `S_sing_soft(E)` and regular domain `M_reg(E)` are defined.

* N_level. `N2`.

  * Achieved.

    * The narrative links soft matter physics, self assembly, and TU thermodynamic_tension.
    * World T and World F are described at the effective layer relative to encoding `E`.
    * The distinction between observed behavior, encoding choices, and universality claims is explicit.

### 9.2 Next measurable step toward E2

To progress from E1 to E2 for encoding `E`, at least one of the following should be realized.

1. Prototype implementation.

   Build a working tool that:

   * takes published or simulated data for several soft matter systems,
   * extracts morphology descriptors using `SoftMatter_MorphologyDescriptorLibrary` under `E`,
   * computes `Tension_SM(m; E, k)` for a range of refinement levels,
   * publishes the resulting tension profiles and descriptor distributions as open data.

2. Cross system benchmarking.

   Apply the same encoding `E` to a diverse benchmark set of soft matter systems such as surfactant systems, block copolymers, colloids, and liquid crystals. Demonstrate that:

   * low tension regions align with known self assembled structures,
   * tension profiles are reasonably stable under refinement.

Both steps operate only on observables and encoded summaries and remain within the effective layer constraints of Q070.

### 9.3 Long term role in the TU program

In the longer term, Q070 is expected to serve as:

* the central node for thermodynamic_tension based universality in soft condensed matter,
* a source of design tools that can be reused in chemical, biological, and geophysical BlackHole problems where self assembly and pattern formation are key,
* an example of how TU can organize a wide and complex field without claiming microscopic completeness, by focusing on encoding, mismatches, and tension rather than on full generative rules.

---

## 10. Elementary but precise explanation

Soft matter includes materials that are soft and easily deformed. Examples are soapy water, gels, mixtures of tiny particles in a fluid, and polymers in solution. In these systems, large scale structures form by themselves. For example, surfactant molecules can form tiny spheres called micelles or hollow shells called vesicles. Block copolymers can form layers, cylinders, or more complex patterns.

Scientists know many specific models and rules for particular systems. There is still no single, simple language that explains all of them at once in a way that is both predictive and clearly universal.

Q070 asks a specific question.

* Can we describe many different soft matter systems using:

  * a common set of building block types,
  * a common way of describing shapes and patterns,
  * and a common number called soft matter tension that tells us how well a given description matches what really happens,

  when all of this is defined inside a single encoding `E`?

In this view:

* A state is not a list of every atom. It is a summary that says:

  * what kinds of building blocks are present,
  * how they tend to attract or repel each other,
  * what the overall shape and pattern of the material looks like,
  * which control knobs such as temperature or concentration are set.

For each state we measure:

* how different its building blocks and interactions are from a reference library for a universality class,
* how different its patterns are from reference patterns for that class.

We combine these differences into one number called `Tension_SM`. If this number is small, the description is in a low tension band and matches the observed self assembly. If it is large, there is a mismatch.

Then we imagine two kinds of worlds relative to the chosen encoding `E`.

* In a unified world.

  * We can choose one library of descriptors and one way to compute tension.
  * For many different soft matter systems, we can find states where the tension stays small and stable when we look in more detail.
  * The same ideas and patterns keep showing up again and again.

* In a non unified world.

  * Any single library and tension definition that fits the aims of Q070 fails for at least one important system.
  * For some systems, the tension stays large no matter how we refine the description.
  * To make things work, we would have to change the encoding itself, not just adjust small parameters.

Q070 does not claim to know which world is real or that a final encoding has already been found. Instead, it gives:

* a way to write the question in terms of observable quantities and tension for a fixed encoding `E`,
* concrete experiments that can reject specific proposals for the universal description,
* reusable tools for AI systems that want to reason about soft matter, design new materials, or connect physical self assembly to higher level phenomena.

It is the soft matter counterpart of asking for a universal effective theory, expressed entirely in the language of state spaces, observables, and tension at the effective layer.

---

## Tension Universe effective layer footer

This page is part of the **WFGY / Tension Universe** S problem collection and encodes Q070 at the effective layer for a fixed soft matter encoding `E in E_SOFT`.

### Scope of claims

* The goal of this document is to specify an **effective layer encoding** of Q070 under a fixed encoding `E`.
* It does not claim to prove or disprove the canonical statement in Section 1.
* It does not introduce any new theorem beyond what is already established in the cited literature.
* It should not be cited as evidence that the corresponding open problem has been solved.
* All universality and world statements are conditional on the chosen encoding `E` and its keys.

### Effective layer objects

All objects listed here live at the effective layer and are defined relative to the encoding `E`.

* State spaces and domains.

  * `M(E)` – semantic state space for soft matter scenarios under encoding `E`.
  * `S_sing_soft(E)` – singular set of states where observables are undefined or divergent.
  * `M_reg(E) = M(E) \ S_sing_soft(E)` – regular domain on which tension analysis is valid.

* Libraries and fields.

  * `L_blocks(m; E)` – building block library for `m`.
  * `L_int(m; E)` – effective interaction motif library for `m`.
  * `phi_i(m; E, x)` – coarse grained concentration or volume fraction fields.
  * `Q_alpha(m; E, x)` – local order parameter fields.
  * `c_ctrl(m; E)` – control parameter vector.

* Observables and mismatch scores.

  * `F_eff(m; E)` – effective free energy like observable.
  * `DeltaS_micro(m; E, k)` – microscopic mismatch.
  * `DeltaS_morph(m; E, k)` – morphology mismatch.
  * `DeltaS_SM(m; E, k)` – combined soft matter mismatch.
  * `Tension_SM(m; E, k)` – soft matter tension, defined equal to `DeltaS_SM`.

* Invariants and refinement.

  * `k` – refinement level specified by `RefinementKey(E)`.
  * `M_desc(m; E, k)` – morphology descriptor vector at level `k`.
  * `M_ref(E, k)` – reference morphology descriptor for the universality class at level `k`.
  * `I_univ(m; E, k)` – morphology universality invariant.
  * `I_stable(m; E, k, k')` – encoding stability invariant.

* Tension tensor and coupling.

  * `T_ij(m; E)` – semantic tension tensor for soft matter scenarios.
  * `S_i(m; E)` – source factors.
  * `C_j(m; E)` – receptivity factors.
  * `lambda(m; E)` – convergence state factor.
  * `kappa_soft(E)` – soft matter coupling constant.

* Worlds and experiments.

  * World T and World F – counterfactual tension worlds defined as patterns in the observables above for encoding `E`.
  * Experiment 1 and Experiment 2 – falsifiability protocols that can reject a specific encoding `E` without resolving the canonical problem.

* Components and tools.

  * `SoftMatter_TensionFunctional` – reusable functional that maps soft matter descriptors to a scalar tension and mismatch breakdown.
  * `SoftMatter_MorphologyDescriptorLibrary` – reusable descriptor library for morphology.
  * `SelfAssembly_ExperimentTemplate` – reusable experiment pattern for self assembly.
  * `SoftMatterTensionHead`, `SelfAssemblyPlanner`, `UniversalityClassifier` – AI modules that consume the above objects as interfaces.

### Encoding and fairness constraints

* The encoding class `E_SOFT` and the specific encoding `E` are declared in the header and Section 3.

* The keys `EncodingKey(E)`, `LibraryKey(E)`, `WeightKey(E)`, and `RefinementKey(E)` specify:

  * descriptor libraries,
  * refinement rules,
  * weights `w_micro(E)`, `w_morph(E)`,
  * thresholds `epsilon_SM(E)`, `epsilon_univ(E)`, and `delta_SM(E)`.

* Within a single encoding `E`:

  * These weights and thresholds are fixed and cannot be tuned per system or per experiment.
  * Changes that alter these core choices are treated as defining a new encoding `E'` with its own keys and must be documented as such.

### Relation to the canonical problem

* The canonical problem in Section 1 is stated in standard physical language, independent of TU.
* This page only proposes one way to encode that question at the effective layer for a fixed encoding `E`.
* Falsifying or refining an encoding `E` through the experiments above does not by itself resolve Q070. It only updates which encodings remain viable candidates for a universal soft matter theory.

This page should be read together with the following charters:

* [TU Effective Layer Charter](../Charters/TU_EFFECTIVE_LAYER_CHARTER.md)
* [TU Encoding and Fairness Charter](../Charters/TU_ENCODING_AND_FAIRNESS_CHARTER.md)
* [TU Tension Scale Charter](../Charters/TU_TENSION_SCALE_CHARTER.md)
* [TU Global Guardrails](../Charters/TU_GLOBAL_GUARDRAILS.md)
