# Q067 · Exact quantum simulation of complex molecules

## 0. Header metadata

```txt
ID: Q067
Code: BH_CHEM_QUANTUM_MOL_SIM_L3_067
Domain: Chemistry
Family: quantum_chemistry
Rank: S
Projection_dominance: I
Field_type: dynamical_field
Tension_type: computational_tension
Status: Open
Semantics: hybrid
E_level: E2
N_level: N2
Last_updated: 2026-01-25
```

---

## 1. Canonical problem and status

### 1.1 Canonical statement

The canonical problem behind Q067 can be stated as follows.

Given:

* realistic molecular systems with many electrons and nuclei, including strongly correlated and chemically complex cases,
* target observables such as ground state energies, excitation energies, and reaction barriers,
* a practical notion of “chemical accuracy” (for example energy errors on the order of 1 kcal/mol),

ask whether there exist computational strategies that:

1. achieve chemical accuracy for these observables,
2. do so with resource requirements that scale acceptably with system size and complexity,
3. remain compatible with known physical limits on information processing and noise.

Here “computational strategies” include:

* classical approximate methods (for example coupled cluster, density functional theory, tensor network methods),
* fully quantum algorithms (for example phase estimation, variational quantum eigensolvers, quantum imaginary time),
* hybrid classical–quantum pipelines.

The problem is not to construct a particular algorithm inside this document. Instead, it is to capture, at the effective layer, the tension between:

* the physical many-body structure of molecules,
* the algorithmic difficulty of representing and evolving their quantum states,
* the practical limits of classical and quantum hardware.

### 1.2 Status and difficulty

Several facts are known.

1. In classical quantum chemistry, a hierarchy of methods exists:

   * mean-field approaches (for example Hartree–Fock),
   * low-order perturbation and coupled cluster methods,
   * multi-reference and strongly correlated techniques.

   These methods can often achieve chemical accuracy for small and moderately correlated systems, but their cost typically grows steeply with system size or correlation strength.

2. Quantum algorithms promise asymptotic advantages for simulating quantum systems. There are algorithmic families that, in principle, can approximate molecular eigenvalues with polynomial resources in some parameters, but:

   * known gate counts and error correction overheads for chemically relevant systems remain extremely high,
   * near-term noisy hardware significantly constrains what can be done in practice.

3. From the viewpoint of computational complexity, closely related problems such as local Hamiltonian ground state estimation are QMA-hard in general. This suggests that fully general, uniformly efficient algorithms for arbitrary quantum systems are unlikely.

4. On the other hand, real molecules occupy a structured subset of all possible Hamiltonians. It remains an open problem to precisely characterize which families of chemically relevant systems admit scalable, chemically accurate simulation on realistic hardware.

Thus the canonical problem behind Q067 is open. It sits at the intersection of quantum chemistry, computational complexity, and quantum information, and it is widely regarded as one of the central challenges in turning quantum simulation into a practical tool for chemistry and materials science.

### 1.3 Role in the BlackHole project

Within the BlackHole S-problem collection, Q067 has three main roles.

1. It is the flagship example of a **computational_tension** problem in chemistry, where physical fidelity, algorithmic cost, and correlation complexity must be balanced.

2. It acts as a bridge node between:

   * microscopic chemical structure (Q061, Q065, Q066),
   * fundamental quantum information limits (Q031, Q052),
   * and thermodynamic resource constraints (Q059).

3. It supplies reusable components for:

   * describing molecular complexity at the effective layer,
   * defining tension functionals that mix accuracy, cost, and correlation,
   * constructing counterfactual “simulable” and “intractable” chemical worlds.

### References

1. S. McArdle, S. Endo, A. Aspuru-Guzik, S. C. Benjamin, X. Yuan,
   “Quantum computational chemistry”, Reviews of Modern Physics 92, 015003 (2020).

2. I. Kassal, J. D. Whitfield, A. Perdomo-Ortiz, M. H. Yung, A. Aspuru-Guzik,
   “Simulating chemistry using quantum computers”, Annual Review of Physical Chemistry 62, 185–207 (2011).

3. P. Helgaker, T. Jorgensen, J. Olsen,
   “Molecular Electronic-Structure Theory”, Wiley, 2000.

4. J. D. Whitfield, J. Biamonte, A. Aspuru-Guzik,
   “Simulation of electronic structure Hamiltonians using quantum computers”, Molecular Physics 109, 735–750 (2011).

---

## 2. Position in the BlackHole graph

This block records Q067’s position in the BlackHole graph. Each edge comes with a one-line reason that points to a concrete component or tension type.

### 2.1 Upstream problems

Upstream nodes provide prerequisites, tools, or general foundations that Q067 relies on at the effective layer.

* Q031 (BH_PHYS_QINFO_L3_031)
  Reason: Supplies general limits and structures of quantum information processing that bound possible simulation algorithms and error correction strategies.

* Q035 (BH_PHYS_QMETROLOGY_LIMIT_L3_035)
  Reason: Provides physical limits on precision and noise that constrain what counts as achievable chemical accuracy in practice.

* Q052 (BH_CS_PVSBPP_L3_052)
  Reason: Encodes the comparative power of quantum and classical computation, which shapes expectations for quantum simulation advantages.

* Q059 (BH_CS_INFO_THERMODYN_L3_059)
  Reason: Introduces thermodynamic cost frameworks for information processing, which Q067 uses to define realistic cost observables.

### 2.2 Downstream problems

Downstream nodes directly reuse Q067 components or treat Q067 as a prerequisite.

* Q063 (BH_CHEM_PROTEIN_FOLDING_L3_063)
  Reason: Reuses molecular complexity descriptors and tension functionals to assess feasibility of quantum-assisted protein folding simulations.

* Q061 (BH_CHEM_BOND_NATURE_L3_061)
  Reason: Depends on Q067’s many-body simulation components to probe strongly correlated chemical bonds at high fidelity.

* Q065 (BH_CHEM_ROOMTC_SUPER_L3_065)
  Reason: Relies on Q067-style simulation tension analysis for candidate superconducting materials with complex electronic structure.

* Q066 (BH_CHEM_ELECTROCHEM_L3_066)
  Reason: Reuses simulation cost and accuracy descriptors for electrochemical interfaces and redox processes.

### 2.3 Parallel problems

Parallel nodes share similar tension types but no direct component dependence.

* Q032 (BH_PHYS_QTHERMO_L3_032)
  Reason: Both Q032 and Q067 involve many-body quantum systems where resource limits and accuracy tradeoffs are central.

* Q036 (BH_PHYS_HIGH_TC_MECH_L3_036)
  Reason: Both analyze strongly correlated quantum systems whose emergent behavior depends on subtle spectral and correlation structure.

* Q070 (BH_CHEM_SOFTMATTER_L3_070)
  Reason: Shares the difficulty of navigating large configuration spaces and complex energy landscapes, though in a different physical regime.

### 2.4 Cross-domain edges

Cross-domain edges connect Q067 to other domains that reuse its components.

* Q081 (BH_NEURO_CONSCIOUS_HARD_L3_081)
  Reason: Uses Q067’s “simulation tension” ideas as a conceptual contrast for the feasibility of quantum-level brain models.

* Q098 (BH_EARTH_ANTHROPOCENE_L3_098)
  Reason: Reuses molecular complexity descriptors and cost observables for climate-relevant chemical processes such as atmospheric chemistry.

* Q121 (BH_AI_ALIGNMENT_L3_121)
  Reason: Treats Q067-style tension as an example of high-stakes simulation where misalignment about feasibility and accuracy can have downstream risks.

---

## 3. Tension Universe encoding (effective layer)

All content in this block is at the effective layer. We only describe:

* state spaces,
* observables and fields,
* invariants and tension scores,
* singular sets and domain restrictions.

We do not describe any hidden generative rules or how internal TU fields are constructed from raw data.

### 3.1 State space

We posit a semantic state space:

```txt
M
```

where each state

```txt
m in M
```

represents a coherent “simulation-world configuration” for a particular molecular system at a chosen resolution. At the effective layer, a state `m` includes:

* a system descriptor: nuclear charges, approximate geometry, and qualitative classification (for example weakly or strongly correlated),
* a representation descriptor: basis set choice, active space specification, and truncation scheme,
* an algorithm descriptor: classical method family, quantum algorithm class, or hybrid pipeline type,
* a resource descriptor: abstract resource budget such as time steps, logical qubits, memory footprint,
* a target descriptor: which observables are to be computed and what error tolerances are required.

We do not specify how these descriptors are encoded or computed from raw data. We only require that for each physically meaningful molecular instance and reasonable simulation setup, there exist states in `M` that encode them coherently.

### 3.2 Observables and fields

We introduce the following effective observables on `M`.

1. Energy error observable

```txt
E_error: M -> R_plus
```

* `E_error(m)` is a nonnegative scalar that summarizes the deviation between the simulated energy (or set of energies) and a trusted reference or ideal target for the configuration represented by `m`.

2. Computational cost observable

```txt
C_cost: M -> R_plus
```

* `C_cost(m)` represents an effective total cost, normalized to a consistent unit such as logical gate count, time-to-solution, or a composite cost that combines several resource types.

3. Resolution observable

```txt
R_res: M -> R_plus
```

* `R_res(m)` summarizes the resolution or expressiveness of the chosen representation (for example basis set size, active space dimension, or number of orbitals).

4. Correlation complexity observable

```txt
F_corr: M -> R_plus
```

* `F_corr(m)` measures the effective strength and complexity of electronic correlations captured in the configuration. It is an abstract indicator; larger values correspond to stronger and more intricate correlations.

5. Spectral complexity observable

```txt
S_spec: M -> R_plus
```

* `S_spec(m)` captures features of the low-energy spectrum such as density of low-lying excitations or entanglement-related complexity.

All these observables are assumed to be finite for states in the regular domain defined below.

### 3.3 Tension components

We define three primary tension components, using fixed thresholds that are part of the encoding and chosen in advance.

Let:

```txt
epsilon_chem > 0    (chemical accuracy energy scale)
C_budget    > 0     (normalized acceptable cost budget)
```

These constants are fixed for the encoding and do not depend on individual molecules.

1. Accuracy tension

```txt
DeltaS_accuracy(m) = max(0, E_error(m) / epsilon_chem - 1)
```

* If `E_error(m)` is below the chemical accuracy threshold, `DeltaS_accuracy(m)` is zero.
* If `E_error(m)` exceeds the threshold, `DeltaS_accuracy(m)` grows linearly in the excess factor.

2. Cost tension

```txt
DeltaS_cost(m) = max(0, C_cost(m) / C_budget - 1)
```

* If `C_cost(m)` is within the budget, `DeltaS_cost(m)` is zero.
* If costs exceed the budget, `DeltaS_cost(m)` measures the relative overshoot.

3. Complexity tension

We define a simple normalized complexity tension:

```txt
C_ref(m) = f_corr_ref(F_corr(m), R_res(m), S_spec(m))
DeltaS_complexity(m) = max(0, C_cost(m) / C_ref(m) - 1)
```

where:

* `f_corr_ref` is a fixed reference function that maps correlation and resolution descriptors to an expected cost scale for well-matched algorithms,
* `C_ref(m)` is positive and finite on the regular domain.

Intuitively, `DeltaS_complexity(m)` becomes large when the actually used cost is much higher than what would be expected from a reasonably well-designed method for that level of correlation and resolution.

### 3.4 Combined tension functional and tensor

We define the combined Q067 tension functional as:

```txt
alpha, beta, gamma > 0 with alpha + beta + gamma = 1

Tension_QSIM(m) = alpha * DeltaS_accuracy(m)
                + beta  * DeltaS_cost(m)
                + gamma * DeltaS_complexity(m)
```

The coefficients `alpha`, `beta`, and `gamma` are:

* fixed globally for Q067,
* chosen before any experiments or data analysis,
* independent of the particular molecule or simulation configuration.

They are not tuned per system; this fairness constraint prevents trivial post hoc reduction of tension.

Consistent with the general TU core decisions, we can package this into an effective tension tensor:

```txt
T_ij(m) = S_i(m) * C_j(m) * Tension_QSIM(m) * lambda(m) * kappa
```

where:

* `S_i(m)` is a source-like factor capturing how strongly the ith source component is engaged by the simulation (for example how much a downstream application depends on accuracy),
* `C_j(m)` is a receptivity-like factor describing how sensitive the jth downstream component is to simulation tension,
* `lambda(m)` is a convergence-state factor indicating whether local reasoning about simulation tradeoffs is convergent, recursive, divergent, or chaotic,
* `kappa` is a fixed overall coupling constant.

The detailed indexing sets for `i` and `j` are not needed at the effective layer, only that `T_ij(m)` is finite on the regular domain.

### 3.5 Singular set and domain restriction

Some observables can become undefined or unbounded in pathological or improperly specified configurations. We collect such cases in a singular set:

```txt
S_sing = {
  m in M :
  any of E_error(m), C_cost(m), R_res(m), F_corr(m), S_spec(m)
  is undefined or not finite
}
```

We then define the regular domain:

```txt
M_reg = M \ S_sing
```

All Q067 tension analysis is restricted to `M_reg`. If an experiment or protocol would require evaluating `Tension_QSIM(m)` for a state in `S_sing`, the result is treated as “out of domain” rather than as meaningful evidence about the underlying physical or computational limits.

---

## 4. Tension principle for this problem

This block states how Q067 is characterized as a tension problem within TU, at the effective layer.

### 4.1 Admissible encoding class

We consider an admissible class of encodings:

```txt
E_QSIM
```

where each encoding in `E_QSIM` specifies:

* how states in `M` are constructed from high-level descriptions of molecules and algorithms,
* how `E_error`, `C_cost`, `R_res`, `F_corr`, and `S_spec` are computed from those states,
* fixed constants `epsilon_chem`, `C_budget`, and the function `f_corr_ref`,
* fixed weights `alpha`, `beta`, `gamma` with `alpha + beta + gamma = 1`.

All members of `E_QSIM` share the same global thresholds and weights; differences between encodings are limited to:

* how they map realistic hardware and algorithm families into abstract cost units,
* how they choose reference cost scales `C_ref(m)` consistent with known complexity and physical constraints.

No encoding is allowed to adapt `epsilon_chem`, `C_budget`, `alpha`, `beta`, or `gamma` on a per-instance basis.

### 4.2 Q067 as a low-tension principle

At the effective layer, Q067 can be framed as a low-tension principle:

> For chemically relevant families of molecules and realistic hardware assumptions, there should exist encodings in `E_QSIM` and sequences of states in `M_reg` such that simulation tension remains in a bounded low band as system size and correlation complexity grow within that family.

More concretely, fix:

* an admissible encoding `E` in `E_QSIM`,
* a family of molecules indexed by a size or complexity parameter `n`.

Then Q067’s optimistic scenario asserts that there exist states `m_n` in `M_reg` representing feasible simulation strategies such that:

```txt
Tension_QSIM(m_n) <= epsilon_QSIM
```

for all `n` in the considered range, where `epsilon_QSIM` is a modest, encoding-level constant that does not grow with `n` inside the specified family.

### 4.3 Q067 failure as persistent high tension

The contrasting scenario is that for some families of chemically relevant molecules and realistic assumptions, any admissible encoding and any coherent simulation strategy will eventually incur high tension.

Formally, for a given family and any encoding `E` in `E_QSIM`, every sequence of states `m_n` in `M_reg` representing feasible simulation attempts satisfies:

```txt
Tension_QSIM(m_n) >= delta_QSIM(n)
```

where:

* `delta_QSIM(n)` is a positive function,
* `delta_QSIM(n)` grows beyond acceptable levels as `n` increases,
* the growth cannot be removed by changing algorithms or representations within the constraints of `E_QSIM`.

In this scenario, high accuracy, reasonable cost, and correlation complexity are jointly incompatible beyond modest sizes. Q067 then functions as a statement that the world forces us into high simulation tension for those families.

The role of this block is not to decide which scenario is true, but to define what it means, at the effective layer, for Q067 to be “low-tension satisfiable” or “high-tension forced”.

---

## 5. Counterfactual tension worlds

We now sketch two counterfactual worlds at the effective layer:

* World T: “TU-simulable chemistry” where simulation tension remains controllable for relevant families.
* World F: “intractable chemistry at scale” where tension grows beyond acceptable bounds.

These worlds are expressed only in terms of observables and tension scores. They do not expose any deep TU generative rules.

### 5.1 World T (TU-simulable chemistry)

In World T:

1. Bounded tension across families

   * For many chemically important families (for example organic molecules, moderate transition metal complexes, key biomolecular fragments), there exist sequences of states `m_T(n)` in `M_reg` such that:

     ```txt
     Tension_QSIM(m_T(n)) <= epsilon_QSIM
     ```

     with `epsilon_QSIM` modest and independent of `n` in the considered range.

2. Balanced accuracy and cost

   * For these `m_T(n)`, accuracy and cost tensions remain under control:

     ```txt
     DeltaS_accuracy(m_T(n)) <= epsilon_acc
     DeltaS_cost(m_T(n))     <= epsilon_cost
     ```

     where both `epsilon_acc` and `epsilon_cost` are small encoding-level constants.

3. Correlation-aware strategies

   * As `F_corr(m_T(n))` and `S_spec(m_T(n))` increase for more correlated systems, encodings in `E_QSIM` can adjust representations and algorithms so that `DeltaS_complexity(m_T(n))` remains in a reasonable band.
   * New algorithmic ideas or hardware improvements may be needed, but the pattern remains one of bounded, manageable tension.

### 5.2 World F (intractable chemistry at scale)

In World F:

1. Unavoidable high tension for some families

   * There exist families of chemically natural molecules and realistic hardware assumptions such that for any encoding in `E_QSIM` and any sequence of states `m_F(n)` in `M_reg` representing simulation efforts, one eventually has:

     ```txt
     Tension_QSIM(m_F(n)) >= delta_QSIM
     ```

     where `delta_QSIM` is a strictly positive constant that marks a high tension band.

2. Tradeoff breakdown

   * Attempts to suppress `DeltaS_accuracy(m_F(n))` below chemical accuracy lead to explosive growth in `DeltaS_cost(m_F(n))`.
   * Attempts to keep `C_cost(m_F(n))` under the budget force `E_error(m_F(n))` so high that `DeltaS_accuracy(m_F(n))` remains large.

3. Correlation barrier

   * For strongly correlated systems, increases in `F_corr(m_F(n))` and `S_spec(m_F(n))` lead to correlation tension that cannot be relieved without violating known complexity bounds or physical hardware limits.
   * This manifests as `DeltaS_complexity(m_F(n))` that stays large even when representations and algorithms are varied within the admissible class.

In World F, high simulation tension is not an artifact of poor algorithms or badly chosen encodings. It is a structural feature of the interplay between chemistry, computation, and hardware limits.

### 5.3 Interpretive note

These counterfactual worlds do not assert which world we actually inhabit. They only state that, if world models consistent with either scenario exist, then Q067’s observables and tension functionals can distinguish their large-scale patterns in a clean, effective-layer language.

---

## 6. Falsifiability and discriminating experiments

This block specifies experiments and protocols that can:

* test the coherence and usefulness of Q067’s encoding,
* discriminate between different encodings inside `E_QSIM`,
* reject encodings that fail to reflect known facts about quantum simulation in chemistry.

They do not prove or disprove the canonical problem. They only validate or falsify specific effective-layer encodings.

### Experiment 1: Classical vs quantum simulation scaling

*Goal:*

Assess whether a given Q067 encoding can represent and distinguish realistic tension patterns for classical and quantum simulation strategies across a benchmark ladder of molecules.

*Setup:*

* Choose a family of benchmark molecules with increasing size and correlation complexity, for example:

  * small organic molecules,
  * medium-sized organic and inorganic molecules,
  * strongly correlated transition metal complexes.

* For each molecule, collect from the literature or controlled studies:

  * best-known classical methods and their estimated costs and errors,
  * proposed quantum algorithms (where available) and their estimated logical costs and errors under reasonable hardware assumptions.

* Fix:

  * one encoding `E` in `E_QSIM`,
  * constants `epsilon_chem`, `C_budget`,
  * weights `alpha`, `beta`, `gamma`,
  * a mapping from algorithm descriptions and hardware assumptions to `C_cost(m)`.

*Protocol:*

1. For each molecule and each simulation strategy (classical or quantum), construct a state `m_data` in `M_reg` that encodes:

   * system class,
   * representation choices,
   * algorithm type,
   * estimated `E_error(m_data)` and `C_cost(m_data)`,
   * correlation and spectral indicators `F_corr(m_data)` and `S_spec(m_data)`.

2. Compute `DeltaS_accuracy(m_data)`, `DeltaS_cost(m_data)`, and `DeltaS_complexity(m_data)` using the rules in Block 3.

3. Compute `Tension_QSIM(m_data)` for all strategies and system sizes.

4. Plot or tabulate `Tension_QSIM(m_data)` versus size or complexity for classical and quantum strategies.

*Metrics:*

* For each size or complexity level:

  * minimum, maximum, and average `Tension_QSIM` across strategies,
  * relative ranking of classical versus quantum strategies.

* Scaling behavior:

  * how `Tension_QSIM` changes with size for each class of methods.

*Falsification conditions:*

* If for known cases where classical simulation is already clearly feasible and quantum simulation proposals are immature, the encoding systematically assigns:

  ```txt
  Tension_QSIM(quantum) << Tension_QSIM(classical)
  ```

  without support from cost and error data, the encoding is considered misaligned and rejected.

* If for known near-term regimes where quantum algorithms are believed to provide no practical benefit, the encoding cannot produce a tension pattern where classical methods are at least competitive, it is rejected.

* If small variations in `E` inside `E_QSIM` produce arbitrarily different qualitative tension rankings for the same data, the encoding class is considered too unstable and is rejected.

*Semantics implementation note:*

All quantities are treated within the hybrid semantics declared in the metadata, with continuous fields for costs and errors and discrete descriptors for algorithm types and basis choices.

*Boundary note:*

Falsifying TU encoding != solving canonical statement. This experiment can reject specific effective encodings but does not decide whether large-scale exact quantum simulation of complex molecules is possible in principle.

---

### Experiment 2: Active space refinement tension

*Goal:*

Test whether Q067’s tension components behave plausibly under systematic refinement of representations for strongly correlated molecules.

*Setup:*

* Select a small set of strongly correlated molecular systems such as:

  * transition metal dimers,
  * small clusters with open-shell character,
  * molecules known to be challenging for single-reference methods.

* For each system, construct a refinement ladder of simulation setups:

  * increasing active space size,
  * improved basis sets,
  * more sophisticated correlation treatments.

* Use a single encoding `E` in `E_QSIM` with fixed thresholds and weights.

*Protocol:*

1. For each rung of the refinement ladder, construct a state `m_ref(k)` in `M_reg` encoding:

   * the chosen active space and basis,
   * the correlation method class,
   * estimated or measured `E_error(m_ref(k))` and `C_cost(m_ref(k))`,
   * updated correlation and spectral indicators.

2. Compute `DeltaS_accuracy(m_ref(k))`, `DeltaS_cost(m_ref(k))`, `DeltaS_complexity(m_ref(k))`, and `Tension_QSIM(m_ref(k))`.

3. Trace how each tension component changes as `k` increases.

*Metrics:*

* For each system:

  * sequence of accuracy, cost, and complexity tensions along the ladder,
  * any tradeoff points where accuracy improvements stall or cost becomes dominant.

* Qualitative patterns:

  * whether there is a regime where tension decreases, stabilizes, or inevitably grows.

*Falsification conditions:*

* If the encoding yields a pattern where:

  * `E_error(m_ref(k))` decreases,
  * `C_cost(m_ref(k))` and `F_corr(m_ref(k))` increase in ways consistent with known algorithmic expectations,

  but `Tension_QSIM(m_ref(k))` shows unmotivated oscillations or non-monotonic jumps not explainable by tradeoff decisions, the encoding is considered incoherent and rejected.

* If in regimes where practitioners know that further refinement is practically hopeless, the encoding keeps `Tension_QSIM(m_ref(k))` in a low band, it is considered unrealistic and rejected.

*Semantics implementation note:*

Refinement is modeled as a discrete sequence of configuration changes inside the hybrid semantics declared in the metadata. No continuous limits are taken over unbounded resolution; instead, we work with finite, realistic ladders.

*Boundary note:*

Falsifying TU encoding != solving canonical statement. This experiment tests whether the chosen tension functional tracks realistic refinement behavior but does not determine absolute limits of quantum simulation.

---

## 7. AI and WFGY engineering spec

This block describes how Q067 can be used as an engineering module for AI systems under the WFGY framework, at the effective layer.

### 7.1 Training signals

We define several training signals derived from Q067 observables.

1. `signal_chem_accuracy_tension`

   * Definition:

     ```txt
     signal_chem_accuracy_tension(m) = DeltaS_accuracy(m)
     ```

   * Purpose: penalize internal states or outputs that imply chemically relevant quantities can be computed with unrealistically small errors at negligible cost.

2. `signal_cost_realism`

   * Definition:

     ```txt
     signal_cost_realism(m) = DeltaS_cost(m)
     ```

   * Purpose: discourage reasoning patterns where the model proposes simulation schemes whose cost is far beyond any reasonable budget without acknowledging resource constraints.

3. `signal_corr_awareness`

   * Definition:

     ```txt
     signal_corr_awareness(m) = DeltaS_complexity(m)
     ```

   * Purpose: encourage the model to adjust its claims when dealing with strongly correlated molecules, rather than extrapolating weakly correlated intuition.

4. `signal_qsim_tension_total`

   * Definition:

     ```txt
     signal_qsim_tension_total(m) = Tension_QSIM(m)
     ```

   * Purpose: provide a single scalar that summarizes the overall simulation tension and can be used as an auxiliary loss in training.

### 7.2 Architectural patterns

We outline module patterns for AI systems that reuse Q067 components.

1. `QSIM_TensionHead`

   * Role: takes the model’s internal representation of a quantum chemistry or materials simulation query and outputs an estimated `Tension_QSIM(m)` along with its components.

   * Interface:

     ```txt
     inputs: internal_embeddings_for_query
     outputs: tension_total, (DeltaS_accuracy, DeltaS_cost, DeltaS_complexity)
     ```

2. `ActiveSpacePlanner`

   * Role: suggests refinement steps in basis and active space choices that trade accuracy against cost while monitoring tension components.

   * Interface:

     ```txt
     inputs: current_state_descriptor, target_accuracy
     outputs: candidate_next_descriptor, expected_tension_change
     ```

3. `ComplexityGuard`

   * Role: checks whether proposed simulation strategies implicitly violate known complexity or hardware limits, using `F_corr`, `S_spec`, and `C_cost`.

   * Interface:

     ```txt
     inputs: simulation_plan_descriptor
     outputs: guard_score (low means safe, high means likely unrealistic)
     ```

### 7.3 Evaluation harness

We propose an evaluation harness for AI models augmented with Q067 modules.

1. Task set

   * A curated benchmark of questions and design tasks such as:

     * “Is this simulation of a large correlated molecule realistic on near-term hardware?”
     * “Which approximations are acceptable to reach chemical accuracy here?”
     * “Compare two simulation strategies in terms of feasibility and reliability.”

2. Conditions

   * Baseline condition:

     * Model answers tasks with no explicit Q067 modules or tension-based signals.

   * TU-augmented condition:

     * Model uses `QSIM_TensionHead`, `ActiveSpacePlanner`, and `ComplexityGuard` as auxiliary tools.

3. Metrics

   * Rate at which the model proposes obviously unrealistic simulation claims.
   * Internal consistency of cost and accuracy statements across multiple steps.
   * Alignment with expert assessments on which regimes are feasible and which are likely intractable.

### 7.4 60-second reproduction protocol

A minimal 60-second protocol for external users.

* Baseline setup

  * Prompt: ask the AI, “Can we exactly simulate this complex correlated molecule to chemical accuracy on current hardware?” with a short description of the molecule and no mention of tension or TU.
  * Observation: record whether the answer is vague, over-optimistic, or ignores cost and correlation issues.

* TU-encoded setup

  * Prompt: same question, but add instructions such as “explicitly reason about simulation tension, including accuracy, cost, and correlation complexity, using Q067-style observables.”
  * Observation: check whether the answer now discusses:

    * correlation difficulty,
    * cost vs accuracy tradeoffs,
    * realistic hardware constraints.

* Comparison metric

  * Use a simple rubric assessing:

    * explicit mention of tradeoffs,
    * realism of cost assumptions,
    * clarity about what is currently possible.

* What to log

  * Prompts, model responses, internal tension estimates from `QSIM_TensionHead` if available.
  * This enables later analysis of how Q067 modules influenced reasoning, without revealing any deep TU construction.

---

## 8. Cross problem transfer template

This block lists reusable components produced by Q067 and how they transfer to other problems.

### 8.1 Reusable components produced by this problem

1. ComponentName: `QSIM_TensionFunctional`

   * Type: functional

   * Minimal interface:

     ```txt
     inputs: E_error, C_cost, F_corr, S_spec, resolution_descriptor
     output: tension_value
     ```

   * Preconditions:

     * Inputs must represent coherent summaries for a single simulation configuration in `M_reg`, using the same thresholds and weights as defined for Q067.

2. ComponentName: `MolecularComplexityDescriptor`

   * Type: field

   * Minimal interface:

     ```txt
     inputs: system_descriptor
     outputs: (size_parameter, correlation_indicator, spectral_complexity_indicator)
     ```

   * Preconditions:

     * The system descriptor provides enough information to classify molecules along size and correlation dimensions.

3. ComponentName: `ActiveSpaceRefinementPattern`

   * Type: experiment_pattern

   * Minimal interface:

     ```txt
     inputs: initial_simulation_descriptor, refinement_steps
     outputs: ladder_of_descriptors_with_expected_tension_trends
     ```

   * Preconditions:

     * The refinement steps are realistic and consistent with known quantum chemistry practice.

### 8.2 Direct reuse targets

1. Q063 (BH_CHEM_PROTEIN_FOLDING_L3_063)

   * Reused components: `MolecularComplexityDescriptor`, `ActiveSpaceRefinementPattern`.
   * Why it transfers: protein folding simulations also involve complex energy landscapes and strong interactions; these components help describe where quantum or enhanced classical simulations might be feasible.
   * What changes: the system descriptors now refer to biomolecular fragments and coarse-grained models, but the structure of the refinement ladder and tension trends remains similar.

2. Q061 (BH_CHEM_BOND_NATURE_L3_061)

   * Reused components: `QSIM_TensionFunctional`, `MolecularComplexityDescriptor`.
   * Why it transfers: understanding chemical bonds in strongly correlated systems requires fine control over accuracy and cost in local many-body simulations.
   * What changes: the emphasis shifts toward local bond descriptors and bond-centric observables, but the underlying tension between correlation complexity and simulation resources is the same.

3. Q065 (BH_CHEM_ROOMTC_SUPER_L3_065)

   * Reused components: all three listed above.
   * Why it transfers: candidate high-temperature superconductors often involve large, strongly correlated unit cells whose electronic structures are difficult to simulate.
   * What changes: the notion of “chemical accuracy” may be adapted to focus on pairing gaps, critical temperatures, or phase boundaries, while cost and correlation descriptors follow Q067’s style.

---

## 9. TU roadmap and verification levels

This block explains Q067’s place on the TU verification ladder and the next measurable steps.

### 9.1 Current levels

* E_level: E2

  * Effective-layer observables, tension components, and a combined tension functional have been specified.
  * Concrete experiment templates exist with falsification conditions for encodings in `E_QSIM`.

* N_level: N2

  * Narrative links between physical chemistry, computational cost, and TU tension are explicit and coherent.
  * World T and World F counterfactuals are defined in terms of observable tension patterns.

### 9.2 Next measurable steps toward E3 and N3

To advance toward E3:

1. Implement at least one concrete encoding in `E_QSIM`:

   * map actual literature data for a benchmark set of molecules and methods into `M_reg`,
   * compute `Tension_QSIM` values and publish them as open data.

2. Run Experiment 1 and Experiment 2 with real or realistically simulated numbers, and document:

   * whether tension patterns align with expert expectations,
   * which parts of the encoding need adjustment.

To advance toward N3:

1. Build a cross-domain narrative that connects Q067’s simulation tension concepts to:

   * Q061 and Q065 in chemistry,
   * Q031 and Q052 in quantum information and complexity,
   * Q121 in AI alignment.

2. Demonstrate that this narrative can be communicated to specialists in each domain without requiring any knowledge of TU’s deeper layers.

Both sets of steps operate strictly at the effective layer and respect the constraints in the constitution.

### 9.3 Long-term role in the TU program

In the long term, Q067 is intended to serve as:

* the reference node for computational_tension problems involving quantum many-body systems in chemistry,
* a calibration point where claims about quantum advantage and practical feasibility can be grounded in a structured tension formalism,
* a bridge between theoretical complexity results and engineering-level decisions about simulation pipelines.

---

## 10. Elementary but precise explanation

This block gives a non-technical explanation that remains faithful to the effective-layer description.

Chemists want to predict what molecules will do. For simple molecules, current methods already work very well. For large or strongly correlated molecules, things get much harder.

People hope that quantum computers will one day let us simulate complicated molecules exactly, or at least well enough to design new drugs and materials. At the same time, there are reasons to think that some of these problems might be fundamentally hard and may always demand huge resources.

Q067 does not try to answer the full question once and for all. Instead, it builds a careful language for talking about the tension in these simulations.

In this language, every simulation attempt is described by:

* how accurate it is,
* how much computational effort it needs,
* how complicated the molecule’s quantum behavior is.

From these pieces, Q067 defines a single number called the simulation tension. Low tension means “good enough accuracy at reasonable cost for this level of complexity”. High tension means “something has to give, either accuracy or cost”.

Then Q067 asks us to imagine two types of worlds:

* In a “simulable chemistry” world, for the molecules we care most about, we can keep the tension low by choosing smart methods and using good hardware.
* In an “intractable chemistry” world, for some families of molecules, the tension stays high no matter what we try, unless we accept huge costs or poor accuracy.

Q067 does not decide which kind of world we actually live in. It does three more modest but important things.

1. It gives precise rules for how to measure tension in a way that cannot be easily cheated by changing the rules after we see the results.
2. It sets up experiments and data analyses that can tell us whether a particular way of encoding this tension matches what chemists and physicists already know.
3. It produces reusable tools that other hard problems, such as protein folding or superconductivity, can borrow when they need to talk about the limits of simulation.

In this way, Q067 turns a vague question about “whether quantum computers will solve chemistry” into a structured, testable story about how accuracy, cost, and complexity pull against each other in the space of possible worlds.
