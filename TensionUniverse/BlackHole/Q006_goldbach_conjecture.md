# Q006 · Goldbach conjecture

## 0. Header metadata

```txt
ID: Q006
Code: BH_MATH_GOLDBACH_L3_006
Domain: Mathematics
Family: Additive number theory
Rank: S
Projection_dominance: I
Field_type: combinatorial_field
Tension_type: consistency_tension
Status: Open
Semantics: discrete
E_level: E2
N_level: N2
Last_updated: 2026-01-24
````

---

## 1. Canonical problem and status

### 1.1 Canonical statement

Goldbach’s conjecture (binary or “strong” Goldbach) is the statement:

> Every even integer `N >= 4` can be written as the sum of two prime numbers.

Equivalently:

For each even integer `N >= 4`, there exist primes `p_1`, `p_2` such that

```txt
N = p_1 + p_2 .
```

Often one defines, for each even `N`, the number of Goldbach representations

```txt
r_2(N) = count of ordered pairs (p_1, p_2) of primes with p_1 + p_2 = N .
```

The conjecture then says that `r_2(N) >= 1` for all even `N >= 4`.

There is also a “weak” or “ternary” Goldbach conjecture stating that every odd integer greater than or equal to 7 can be written as the sum of three primes; that weaker form has been proved, while the binary form remains open.

In this Q006 entry we focus on the binary conjecture.

### 1.2 Status and difficulty

Goldbach’s conjecture has been open since the eighteenth century and is one of the central problems of additive number theory. Key partial results include:

* Almost all even integers can be written as the sum of two primes. More precisely, classical work of Estermann and others shows that the set of even `N` failing to be a sum of two primes has asymptotic density zero, under suitable hypotheses and methods of analytic number theory.

* Chen’s theorem: every sufficiently large even integer `N` can be represented as

  ```txt
  N = p + P_2
  ```

  where `p` is a prime and `P_2` is an “almost prime” (an integer with at most two prime factors, counted with multiplicity).

* Various results using the circle method give bounds of the form “every sufficiently large odd integer is the sum of at most five primes”; combined with older work, this leads to very strong approximate versions of Goldbach-type statements.

* Extensive numerical verification has checked Goldbach’s conjecture for all even `N` up to large computational limits. These verifications push the potential first counterexample, if any exists, far out of reach of current computation.

No general proof or disproof is known. The problem is deeply connected with the distribution of prime numbers and with techniques from analytic number theory, such as exponential sums and the circle method.

### 1.3 Role in the BlackHole project

Within the BlackHole S-problem collection, Q006 plays several roles:

1. It is the canonical example of an additive number theory problem where **coverage** of a discrete line (even integers) by a structured set (prime pairs) is the central observable.

2. It provides a prototype for **discrete consistency_tension**: tension between observed coverage and multiplicity of representations and the expected behavior predicted by density models derived from prime distributions.

3. It links spectral and density information (Q001, Q019) to concrete combinatorial events: whether each even `N` in a window has at least one admissible representation.

4. It acts as a discrete counterpart to spectral problems, useful to test how TU encodings behave when everything lives on the integers rather than on continuous fields.

### References

1. R. K. Guy, “Unsolved Problems in Number Theory”, 3rd edition, Springer, 2004, Part A, section on Goldbach’s conjecture.
2. T. Tao, “Every odd number greater than 1 is the sum of at most five primes”, Annals of Mathematics, 2014, based on arXiv:1201.6656.
3. T. Estermann, “On Goldbach’s problem: Proof that almost all even positive integers are sums of two primes”, Proceedings of the London Mathematical Society, 1938.
4. A. Ivić, “The Riemann Zeta-Function: Theory and Applications”, Dover Publications, reprint edition, chapters on additive prime problems.

---

## 2. Position in the BlackHole graph

This block records how Q006 sits inside the BlackHole graph. Every edge has a one-line reason pointing to a concrete component or tension object.

### 2.1 Upstream problems

These problems provide prerequisites or reusable structures that Q006 relies on at the effective layer.

* Q001 (BH_MATH_NUM_L3_001 · Riemann Hypothesis)
  Reason: supplies spectral and density constraints for primes that underlie the expected number of Goldbach representations and the Goldbach mismatch profiles.

* Q005 (BH_MATH_ABC_L3_005 · abc conjecture)
  Reason: provides global constraints on sums of integers and prime factors that can be reused to bound “pathological” additive decompositions interacting with Goldbach coverage.

* Q019 (BH_MATH_DIOPH_DENSITY_L3_019 · Diophantine density frameworks)
  Reason: offers general density and counting frameworks on the integers that are reused to formalize coverage of even integers by prime pairs.

### 2.2 Downstream problems

These problems directly reuse Q006 components or depend on Q006’s tension structures.

* Q007 (BH_MATH_TWINPRIME_L3_007 · Twin prime conjecture)
  Reason: reuses the EvenIntegerWindow and PrimePairWindow structures to define and compare small-gap prime pair tension versus Goldbach coverage tension.

* Q008 (BH_MATH_COLLATZ_L3_008 · Collatz conjecture)
  Reason: reuses the discrete coverage and windowing formalism to compare coverage of positive integers by Collatz orbits with coverage of the even line by prime pairs.

* Q009 (BH_MATH_NONLINEAR_PRIMEPATTERN_L3_009 · Nonlinear prime patterns)
  Reason: reuses Q006’s discrete combinatorial tension library as a baseline for more complicated additive and multiplicative prime patterns.

### 2.3 Parallel problems

Parallel nodes share similar tension types but no direct component dependence.

* Q001 (BH_MATH_NUM_L3_001 · Riemann Hypothesis)
  Reason: both encode consistency between prime distributions and deeper structures (spectral versus additive), using related mismatch and tension functionals.

* Q007 (BH_MATH_TWINPRIME_L3_007)
  Reason: both focus on primes in pairs; Q006 on sums, Q007 on gaps, with similar counting and window-based invariants.

* Q009 (BH_MATH_NONLINEAR_PRIMEPATTERN_L3_009)
  Reason: all three describe discrete fields on integers populated by primes and analyze pattern frequencies under consistency_tension.

### 2.4 Cross-domain edges

Cross-domain edges connect Q006 to problems in other domains that can reuse its components.

* Q059 (BH_CS_INFO_THERMODYN_L3_059 · Information and thermodynamics)
  Reason: reuses discrete coverage sequences as examples of structured, sparse occupancy patterns for information density and redundancy models.

* Q123 (BH_AI_INTERP_L3_123 · AI representation interpretability)
  Reason: uses Goldbach-style coverage and multiplicity patterns as benchmark structures for testing whether AI internal representations understand arithmetic relations.

---

## 3. Tension Universe encoding (effective layer)

All content in this block is at the effective layer. We only describe:

* discrete state spaces,
* observables and fields,
* invariants and tension scores,
* singular sets and domain restrictions,
* finite encoding libraries and refinement behavior.

We do not describe any rule mapping raw prime tables or proofs into internal TU fields.

### 3.1 State space

We assume a state space

```txt
M
```

with the following effective interpretation:

* Each state `m` in `M` encodes a finite **Goldbach window** of even integers and associated prime pair information.

* For each `m`, there is an associated even-integer window

  ```txt
  W(m) = { N : N_min(m) <= N <= N_max(m), N even } .
  ```

* For each even `N` in `W(m)`, the state `m` carries a summary of prime pairs `(p_1, p_2)` with

  ```txt
  p_1 + p_2 = N
  ```

  in a way that is sufficient to evaluate the observables defined below.

The construction of `m` from raw data is not specified here. We only assume that:

* For any finite window and prime pair data that could arise in practice, there exist states in `M` that encode it.

### 3.2 Effective observables and fields

We introduce several observables and fields on `M`, defined only at the level needed for tension evaluation.

1. Goldbach coverage observable

```txt
GoldbachCoverage(m) in [0, 1]
```

* Input: a state `m` with window `W(m)`.
* Output: the fraction of even integers in `W(m)` that admit at least one representation as a sum of two primes.

Formally, if `E(m)` is the set of even integers in `W(m)` and `E_cov(m)` is the subset with at least one prime pair representation, then

```txt
GoldbachCoverage(m) = |E_cov(m)| / |E(m)| .
```

2. Goldbach multiplicity profile

```txt
GoldbachMultiplicity(m; N) >= 0
```

* Input: state `m` and an even integer `N` in `W(m)`.
* Output: the number of distinct ordered prime pairs `(p_1, p_2)` with `p_1 + p_2 = N` as encoded in `m`.

We also define a multiplicity summary for the window:

```txt
MultProfile(m) = summary of { GoldbachMultiplicity(m; N) : N in W(m) } .
```

The exact form of the summary (for example a small set of moments or counts by bin) is fixed once for Q006 and not adapted to the data.

3. Expected coverage and multiplicity

We assume a finite library of admissible **density models**:

```txt
D_j for j in J_stage1
```

and a finite family of windows indexed by an integer `k`:

```txt
W_k = { N : 2^k <= N <= 2^(k+1), N even }
for k in K_stage1 .
```

For each pair `(k, j)` we define expected coverage and multiplicity profiles:

```txt
GoldbachCoverageExp(k, j) in [0, 1]
GoldbachMultExp(k, j)    = fixed summary vector
```

These expectations come from standard heuristic density models for prime pairs, calibrated once and for all for each `(k, j)` using classical analytic number theory. They are not adjusted based on the observed data in a particular state `m`.

Each state `m` in `M` is associated with one of the windows `W_k` and a fixed density model `D_j` via a coupling rule described below.

4. Additive coverage mismatch

```txt
DeltaS_add(m) >= 0
```

This is defined by

```txt
DeltaS_add(m) =
    | GoldbachCoverage(m) - GoldbachCoverageExp(k, j) |
```

where `(k, j)` is the window and model pair associated with `m`.

5. Multiplicity mismatch

```txt
DeltaS_mult(m) >= 0
```

This measures the deviation between the observed multiplicity profile `MultProfile(m)` and the expected profile `GoldbachMultExp(k, j)`. For example:

```txt
DeltaS_mult(m) =
    distance( MultProfile(m), GoldbachMultExp(k, j) )
```

where `distance` is a fixed nonnegative function chosen once for Q006 (for example an `L2` style distance between summary vectors). The precise form is part of the encoding and not tuned by the data.

6. Combined Goldbach mismatch

```txt
DeltaS_GC(m) >= 0
```

We define

```txt
DeltaS_GC(m) =
    a_add * DeltaS_add(m) + a_mult * DeltaS_mult(m)
```

with fixed weights `a_add > 0` and `a_mult > 0` satisfying

```txt
a_add + a_mult = 1 .
```

These weights are selected once for Q006 based on theoretical considerations and are held fixed for all states and all experiments. Changing them defines a different encoding, which must be treated as a separate object.

### 3.3 Finite encoding library and refinement order

To avoid post hoc parameter tuning, we fix:

1. A finite index set of window scales

```txt
K_stage1 = { k_0, k_0 + 1, ..., k_1 }
```

with associated windows `W_k` as above.

2. A finite set of density models `D_j` with index set `J_stage1`.

3. A coupling rule

```txt
Couple(k) = j(k)
```

that maps each `k` in `K_stage1` to a density model `D_j(k)` in `J_stage1`.

This rule is fixed once and is independent of any observed coverage mismatches. For example, it may choose density models according to the size of `W_k` or a simple analytic regime, but not by minimizing `DeltaS_GC`.

4. A refinement order on windows

```txt
refine(k) = k + 1
```

for all `k` in `K_stage1` with `k + 1` still in `K_stage1`.

Refining means moving from window `W_k` to `W_(k+1)` and updating the associated model from `D_j(k)` to `D_j(k+1)` via the same fixed coupling rule.

### 3.4 Effective tension tensor component

In line with the TU core decision, we define an effective tension tensor component over `M`:

```txt
T_ij(m) = S_i(m) * C_j(m) * DeltaS_GC(m) * lambda(m) * kappa_GC
```

where:

* `S_i(m)` is a source factor describing how strongly component `i` is driven by Goldbach-related claims in the configuration `m` (for example, how strongly the context insists on full coverage of even integers).

* `C_j(m)` is a receptivity factor describing how sensitive component `j` is to deviations from Goldbach-like behavior (for example, how much a given reasoning path depends on additive prime structure).

* `DeltaS_GC(m)` is the combined Goldbach mismatch defined above.

* `lambda(m)` is the convergence-state factor from the TU core, taking values in a fixed range that encodes whether local reasoning is convergent, recursive, divergent, or chaotic.

* `kappa_GC` is a fixed coupling constant setting the overall scale of Goldbach-related consistency_tension.

The indexing sets for `i` and `j` are not specified here. It is sufficient that, for each `m` in the regular domain, `T_ij(m)` is finite and well defined.

### 3.5 Singular set and domain restrictions

Some states may encode incomplete or inconsistent data, or values outside the domain of the observables above. We collect these into a singular set:

```txt
S_sing = { m in M :
           GoldbachCoverage(m) is undefined
           or MultProfile(m) is undefined
           or DeltaS_GC(m) is not finite }
```

We restrict all Goldbach tension analysis to the regular domain

```txt
M_reg = M \ S_sing .
```

When an experiment or protocol would require evaluating `DeltaS_GC(m)` for `m` in `S_sing`, the result is treated as “out of domain” and does not count as evidence for or against Goldbach’s conjecture.

---

## 4. Tension principle for this problem

This block states how Q006 is treated as a tension problem within TU at the effective layer.

### 4.1 Core tension functional

We define an explicit Goldbach tension functional:

```txt
Tension_GC(m) =
    b_add * DeltaS_add(m) +
    b_mult * DeltaS_mult(m) +
    b_hole * HoleIndicator(m)
```

where:

* `b_add > 0`, `b_mult > 0`, `b_hole > 0` are fixed weights with

  ```txt
  b_add + b_mult + b_hole = 1 ,
  ```

  chosen once and not tuned by data.

* `HoleIndicator(m)` is defined by

  ```txt
  HoleIndicator(m) = 0
      if every even N in W(m) has GoldbachMultiplicity(m; N) >= 1

  HoleIndicator(m) = 1
      otherwise .
  ```

Then:

* `Tension_GC(m) >= 0` for all `m` in `M_reg`.

* `Tension_GC(m)` is small when both coverage and multiplicity mismatch are small and there are no uncovered even integers.

* `Tension_GC(m)` is large when coverage gaps or multiplicity anomalies occur.

### 4.2 Goldbach as a low-tension principle

At the effective layer, Goldbach’s conjecture can be stated as:

> For each large enough window scale in the finite library, there exist world-representing states whose Goldbach tension is consistently small and whose coverage is complete.

More concretely, for each `k` in `K_stage1` above some threshold `k_crit`, there should exist states `m_T(k)` in `M_reg` that encode the actual universe on `W_k` such that:

```txt
HoleIndicator(m_T(k)) = 0
Tension_GC(m_T(k))    <= epsilon_GC(k)
```

for a family of thresholds `epsilon_GC(k)` with the following properties:

* Each `epsilon_GC(k)` is chosen in advance based on theoretical expectations and uncertainties for that scale, not tuned to fit observed mismatches.

* The sequence `epsilon_GC(k)` does not grow without bound along the refinement order; for example it may stay bounded or slowly decrease.

### 4.3 Goldbach failure as persistent high tension

If Goldbach is false, then for any encoding in the admissible class described above, world-representing states eventually exhibit persistent high tension.

Formally, there would exist a lower bound `delta_GC > 0` and an infinite subsequence of indices `k` in `K_stage1` such that for all states `m_F(k)` in `M_reg` that accurately encode the real world on `W_k`:

```txt
HoleIndicator(m_F(k)) = 1
Tension_GC(m_F(k))    >= delta_GC .
```

In this case, the low-tension band defined by `epsilon_GC(k)` would never be consistently reached for all large windows.

Thus, at the effective layer, Q006 is the claim that our universe belongs to the low-tension branch rather than the high-tension branch with respect to the fixed finite encoding library and tension definition.

---

## 5. Counterfactual tension worlds

We describe two counterfactual worlds, both at the effective layer and both expressed only in terms of observables and tension functionals.

* World T: Goldbach true, globally low Goldbach tension.
* World F: Goldbach false, persistent high Goldbach tension.

### 5.1 World T (Goldbach true, low discrete tension)

In World T:

1. Complete coverage

   * For every window index `k` above some `k_crit`, the world-representing state `m_T(k)` satisfies

     ```txt
     GoldbachCoverage(m_T(k)) = 1
     HoleIndicator(m_T(k))    = 0 .
     ```

2. Stable multiplicity statistics

   * For the same windows, the multiplicity mismatch remains small:

     ```txt
     DeltaS_mult(m_T(k)) <= epsilon_mult(k)
     ```

     where `epsilon_mult(k)` is a pre-chosen tolerance that does not blow up along the refinement order.

3. Bounded tension

   * The overall Goldbach tension satisfies

     ```txt
     Tension_GC(m_T(k)) <= epsilon_GC(k)
     ```

     for all sufficiently large `k` in `K_stage1`, with `epsilon_GC(k)` defined as in Block 4.

4. Refinement stability

   * As windows refine via `refine(k) = k + 1`, the tension values `Tension_GC(m_T(k))` form a sequence that remains in a low band and does not display unmotivated spikes caused by the encoding itself.

### 5.2 World F (Goldbach false, persistent high tension)

In World F:

1. Structural coverage gaps

   * There exists an infinite subsequence of window indices `k` and corresponding states `m_F(k)` representing the real world on `W_k` such that

     ```txt
     GoldbachCoverage(m_F(k)) < 1
     HoleIndicator(m_F(k))    = 1 .
     ```

   * These gaps are not localized early anomalies but appear at arbitrarily large scales.

2. Unremovable mismatch

   * Even within the finite density model library and coupling rules, windows with coverage gaps cannot be reinterpreted as low-tension states. For all admissible models attached to such windows, the combined mismatch remains bounded away from zero.

3. Persistent high tension

   * There is a fixed `delta_GC > 0` such that

     ```txt
     Tension_GC(m_F(k)) >= delta_GC
     ```

     for all large `k` in the subsequence.

4. Refinement behavior

   * Refining windows does not wash out the tension: as `k` increases along the subsequence, high tension persists instead of relaxing into the low band defined in World T.

### 5.3 Interpretive note

These worlds do not claim any method to construct internal TU fields from raw data. They only assert that, if there exist effective models of our universe that respect the encoding constraints, then the pattern of Goldbach tension across window scales must qualitatively match one of these two scenarios.

---

## 6. Falsifiability and discriminating experiments

This block specifies experiments at the effective layer that can:

* falsify specific choices of the Q006 tension encoding,
* test robustness of the encoding against synthetic and real data,
* distinguish between tension patterns expected in World T and World F models.

They do not prove or disprove Goldbach’s conjecture itself.

### Experiment 1: Finite-window numerical tension profile

*Goal:*
Test whether the chosen `Tension_GC` functional produces stable, nontrivial tension profiles on real Goldbach data and can distinguish windows with and without coverage holes.

*Setup:*

* Choose an upper bound `N_max` up to which Goldbach representations have been computed or can be computed in practice.

* Select indices `k` in `K_stage1` such that `W_k` is contained in `[4, N_max]`.

* For each such `k`, construct a state `m_real(k)` encoding:

  * the actual coverage of even integers in `W_k`,
  * the multiplicity distribution over `W_k`.

* Construct synthetic “holey” windows by removing all representations for a small set of even integers in selected windows, producing states `m_hole(k)` with artificially induced gaps.

*Protocol:*

1. For each `k` with `W_k` inside the computed range, evaluate:

   ```txt
   GoldbachCoverage(m_real(k))
   DeltaS_add(m_real(k))
   DeltaS_mult(m_real(k))
   Tension_GC(m_real(k))
   ```

2. For each synthetic state `m_hole(k)`, evaluate the same observables and tension.

3. Compare the distributions of `Tension_GC` values for real and synthetic states across all tested windows.

*Metrics:*

* For each `k`, the value of `Tension_GC(m_real(k))`.

* For each `k`, the value of `Tension_GC(m_hole(k))`.

* Separation of these values across the set of windows; for example, the minimal difference

  ```txt
  min_k ( Tension_GC(m_hole(k)) - Tension_GC(m_real(k)) )
  ```

* Stability of `Tension_GC(m_real(k))` as `k` varies within the tested range.

*Falsification conditions:*

* If for many windows, `Tension_GC(m_hole(k))` lies in the same numeric band as `Tension_GC(m_real(k))`, so that windows with large artificial gaps cannot be distinguished from real windows, the encoding is considered inadequate and rejected.

* If small changes to the pre-chosen weights `b_add`, `b_mult`, `b_hole` or to the density model library cause arbitrary flips in which windows appear low-tension or high-tension, without clear mathematical reasons, then the encoding is considered unstable and must be revised.

*Encoding implementation note:*
This experiment only assumes that the state `m` can be evaluated through the observables in Block 3. It does not depend on any particular method of constructing `m` from raw prime tables and does not expose any deeper TU generative mechanism.

*Boundary note:*
Falsifying TU encoding != solving canonical statement.

---

### Experiment 2: Model-world comparison for Goldbach-like sequences

*Goal:*
Assess whether the Q006 tension encoding can consistently distinguish between synthetic sequences that satisfy Goldbach-like coverage and sequences with structured coverage gaps.

*Setup:*

* Construct or select two families of synthetic model worlds over the same window scales:

  * Family T models: for each even integer `N` in the window, at least one admissible representation is provided, possibly generated by a random mechanism that mimics known Goldbach heuristics.

  * Family F models: for each window, a small but structured set of even integers is assigned zero representations, while other integers behave similarly to Family T.

* For each model world and window index `k`, construct a state `m_T_model(k)` or `m_F_model(k)` in `M_reg` that encodes:

  * coverage of the window,
  * multiplicity summaries, following the same observable definitions as in Block 3.

*Protocol:*

1. For each model world state, compute:

   ```txt
   GoldbachCoverage(m_T_model(k)) or GoldbachCoverage(m_F_model(k))
   DeltaS_add(m_T_model(k))      or DeltaS_add(m_F_model(k))
   DeltaS_mult(m_T_model(k))     or DeltaS_mult(m_F_model(k))
   Tension_GC(m_T_model(k))      or Tension_GC(m_F_model(k))
   ```

2. Aggregate tension values over all `k` and over all models in each family.

3. Compare the distributions of `Tension_GC` in Family T and Family F.

*Metrics:*

* Mean and variance of `Tension_GC` over Family T and Family F.
* A simple separation measure, such as the difference between mean values of `Tension_GC` in the two families.
* Sensitivity of this separation to the particular choice of density models and weights `b_add`, `b_mult`, `b_hole` when those choices remain within the admissible encoding class.

*Falsification conditions:*

* If, under admissible choices of the encoding parameters, the distributions of `Tension_GC` for Family T and Family F cannot be separated in a consistent way, then the encoding is considered non-discriminating and rejected.

* If some members of Family F (with explicit coverage gaps) systematically receive lower tension than typical members of Family T, the encoding is considered misaligned with the intended consistency_tension semantics and must be revised.

*Encoding implementation note:*
The construction of synthetic model worlds is left to external methods. At the TU level, only the aggregate observables and tension values are used, and no assumptions are made about the internal mechanism that generated the synthetic data.

*Boundary note:*
Falsifying TU encoding != solving canonical statement.

---

## 7. AI and WFGY engineering spec

This block describes how Q006 can be used as a module in AI and WFGY systems at the effective layer.

### 7.1 Training signals

We list several training signals that use Q006 observables and tension.

1. `signal_goldbach_coverage_band`

   * Definition: a penalty signal proportional to

     ```txt
     | GoldbachCoverage(m) - GoldbachCoverageExp(k, j(k)) |
     ```

     whenever the context assumes Goldbach-like behavior on window `W_k`.

   * Purpose: push internal representations toward windows where observed coverage ratios match the expected ones whenever that is part of the task assumptions.

2. `signal_goldbach_multiplicity_shape`

   * Definition: a signal based on `DeltaS_mult(m)`, possibly rescaled, applied in contexts where the model is asked to reason about the typical number of representations of even integers.

   * Purpose: encourage the model to learn multiplicity patterns that are compatible with standard analytic number theory heuristics.

3. `signal_goldbach_tension_scalar`

   * Definition: directly equal to `Tension_GC(m)` when the model encodes a state `m` for a given window.

   * Purpose: act as a single scalar regularizer that discourages high-tension states when solving problems that assume Goldbach-like behavior.

4. `signal_world_T_vs_world_F_consistency`

   * Definition: a pair of signals comparing the model’s outputs under world T style prompts (assuming Goldbach) and world F style prompts (negating or questioning Goldbach), together with the corresponding tensions.

   * Purpose: ensure that the model cleanly separates the two assumptions and maintains internal consistency in each world, instead of mixing them.

### 7.2 Architectural patterns

We describe module patterns that can reuse Q006 structures without revealing any deeper TU construction.

1. `EvenWindowField`

   * Role: a module that maps internal task representations into discrete windows `W_k` over the even integers, together with an index `k` and model index `j(k)`.

   * Interface:

     * Input: internal embeddings of a number theory context and a scale hint.
     * Output: a discrete window index `k`, a representation of `W_k`, and a handle for the associated density model `D_j(k)`.

2. `PrimePairScanner`

   * Role: a module that produces or retrieves candidate prime pairs `(p_1, p_2)` for a given even `N` in a window.

   * Interface:

     * Input: internal representations plus an even integer `N`.
     * Output: a list or summary of candidate prime pairs used to compute `GoldbachMultiplicity(m; N)`.

3. `TU_DiscreteTensionHead_GC`

   * Role: a tension head that, given window-level summaries, outputs `Tension_GC(m)` and its components.

   * Interface:

     * Input: coverage ratio, multiplicity summary, expected profiles.
     * Output: `DeltaS_add(m)`, `DeltaS_mult(m)`, `Tension_GC(m)`.

### 7.3 Evaluation harness

We outline an evaluation harness to compare baseline AI systems and TU-augmented systems on Goldbach-related reasoning tasks.

1. Task design

   * Construct a benchmark of tasks that include:

     * explaining Goldbach’s conjecture and known partial results,
     * reasoning about hypothetical coverage gaps,
     * extrapolating multiplicity patterns,
     * comparing windows with known coverage versus synthetic windows with removed representations.

2. Conditions

   * Baseline condition: model answers tasks without any explicit tension-based modules.

   * TU condition: model uses `EvenWindowField`, `PrimePairScanner`, and `TU_DiscreteTensionHead_GC` to maintain and report Goldbach tension during reasoning.

3. Metrics

   * Task accuracy on factual questions about Goldbach and related results.
   * Internal consistency when prompted with world T and world F assumptions.
   * Correlation between reported `Tension_GC` and the presence or absence of coverage gaps in synthetic tasks.

### 7.4 60-second reproduction protocol

A simple protocol for external users:

* Baseline setup

  * Prompt: ask an AI system to explain Goldbach’s conjecture, its status, and why “almost all even integers” results are not yet a full proof.
  * Observation: identify whether the explanation correctly distinguishes between full coverage and almost-all results.

* TU encoded setup

  * Prompt: same as above, but add a request: “Structure your explanation in terms of coverage of even windows by prime pairs and a Goldbach tension index that is low when coverage is complete and expected multiplicities match.”

  * Observation: compare the structure and clarity of this answer with the baseline; in particular, whether the model explicitly talks about coverage ratios, multiplicity patterns, and what it would mean for tension to stay high.

* Comparison metric

  * Simple rubric scoring on structure, explicit mention of coverage and tension, and clarity of what is still unknown.

* What to log

  * Prompts, outputs, and any `Tension_GC` values or components that the system chooses to expose.

---

## 8. Cross problem transfer template

This block lists reusable components from Q006 and how they transfer to other problems.

### 8.1 Reusable components produced by this problem

1. ComponentName: `GoldbachCoverage_Field`

   * Type: field

   * Minimal interface:

     ```txt
     Inputs:  even_window W, prime_pair_summary
     Output:  coverage_ratio in [0, 1]
     ```

   * Preconditions:

     * `W` is a finite set of even integers.
     * `prime_pair_summary` is sufficient to determine whether each `N` in `W` has at least one prime pair representation.

2. ComponentName: `GoldbachMultiplicity_Profile`

   * Type: observable

   * Minimal interface:

     ```txt
     Inputs:  even_window W, prime_pair_summary
     Output: multiplicity_summary_vector
     ```

   * Preconditions:

     * For each `N` in `W`, the number of representations is well defined and finite.
     * The summary vector is constructed using a fixed rule shared across all uses.

3. ComponentName: `Tension_GC_Functional`

   * Type: functional

   * Minimal interface:

     ```txt
     Inputs:  coverage_ratio, multiplicity_summary_vector,
              expected_coverage, expected_multiplicity_summary
     Output: tension_scalar >= 0
     ```

   * Preconditions:

     * Expected values come from a model in the admissible density library.
     * Weights `b_add`, `b_mult`, `b_hole` are those fixed for Q006.

### 8.2 Direct reuse targets

1. Q007 (BH_MATH_TWINPRIME_L3_007 · Twin prime conjecture)

   * Reused component: `GoldbachCoverage_Field`, `GoldbachMultiplicity_Profile`.
   * Why it transfers: twin prime problems also consider pairs of primes in a discrete window; the same field and multiplicity machinery can be reused by changing the definition of admissible pairs from “sum equals N” to “difference equals 2”.
   * What changes: the window and pair definition change, but the way coverage and multiplicity are summarized remains the same.

2. Q009 (BH_MATH_NONLINEAR_PRIMEPATTERN_L3_009 · Nonlinear prime patterns)

   * Reused component: `Tension_GC_Functional` as a template.
   * Why it transfers: Q009 studies more complex prime patterns, but still needs to compare observed coverage and multiplicity with expectations from model distributions.
   * What changes: observables now report patterns for polynomial or other nonlinear relations, while the functional form of coverage and multiplicity based tension is adapted but conceptually inherited from Q006.

---

## 9. TU roadmap and verification levels

### 9.1 Current levels

* E_level: E2

  * An explicit discrete encoding of Goldbach in terms of coverage, multiplicity, and a finite encoding library has been specified.
  * Tension functionals and singular sets are clearly defined at the effective layer.

* N_level: N2

  * World T and World F scenarios are clearly described in terms of tension patterns.
  * Cross-problem links and reuse targets are identified.

### 9.2 Next measurable step toward E3

To move from E2 to E3, concrete implementations and public artifacts are needed, such as:

1. A working implementation that, given prime tables up to `N_max`, constructs states `m_real(k)` for multiple window scales and publishes open data for:

   ```txt
   GoldbachCoverage(m_real(k))
   MultProfile(m_real(k))
   Tension_GC(m_real(k))
   ```

2. A collection of synthetic model worlds (both Goldbach-like and with designed gaps) and corresponding tension profiles, published with code that reproduces the results.

Both can be done without exposing any deeper TU generative rule; they only rely on the effective observables described here.

### 9.3 Long-term role in the TU program

In the broader Tension Universe program, Q006 is expected to serve as:

* The canonical discrete testbed for consistency_tension on the integer line.

* A bridge between purely spectral problems (like Q001) and more directly combinatorial problems (like Q007 and Q009).

* A calibration point for how discrete tension encodings behave when pushed to extremely hard open problems, and for how AI systems can use such encodings to reason about additive number theory without claiming proofs.

---

## 10. Elementary but precise explanation

This block gives an explanation aimed at non-specialists, while remaining faithful to the effective-layer description.

The classical Goldbach conjecture says:

> Every even number `N >= 4` can be written as the sum of two prime numbers.

For example:

```txt
4 = 2 + 2
6 = 3 + 3
8 = 3 + 5
10 = 5 + 5 or 3 + 7
```

We can ask two basic questions:

1. For a given even number `N`, does there exist at least one way to write it as a sum of two primes?

2. For a whole range of even numbers, how many such representations do we usually see?

In the Tension Universe view, we do not try to prove or disprove Goldbach directly. Instead, we choose a window of even numbers, say from `N_min` to `N_max`, and look at:

* how many of those even numbers are actually covered by at least one prime pair,
* how the number of representations per even number compares to what standard prime number heuristics would predict.

From this we build:

* a coverage ratio between 0 and 1,
* a summary of how many representations typical even numbers have,
* a Goldbach tension number that is small when coverage and representation counts look as expected, and large when they do not.

Then we imagine two kinds of worlds:

* In a Goldbach-true world, every sufficiently large even number has at least one representation, and the Goldbach tension stays small and stable when we look at bigger and bigger windows.

* In a Goldbach-false world, at some point there would be even numbers with no representations at all; their windows would have large Goldbach tension that does not go away as we refine our view.

This framework does not tell us which world we live in. It does not provide a proof. What it does provide is:

* a clear way to describe what we can observe about Goldbach behavior in finite ranges,
* a precise notion of what “low tension” and “high tension” mean in this context,
* a reusable template that can be applied to other discrete prime pattern problems.

Q006 is thus the canonical example of how Tension Universe encodes a famous unsolved problem on the integers using coverage, multiplicity, and a controlled notion of discrete tension.

