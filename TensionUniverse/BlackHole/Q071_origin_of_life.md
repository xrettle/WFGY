# Q071 · Origin of life

## 0. Header metadata

```txt
ID: Q071
Code: BH_BIO_ORIGIN_LIFE_L3_071
Domain: Biology
Family: Origin of life and early evolution
Rank: S
Projection_dominance: I
Field_type: dynamical_field
Tension_type: consistency_tension + thermodynamic_tension
Status: Open
Semantics: hybrid
E_level: E1
N_level: N2
Last_updated: 2026-01-30
```

---

## 0. Effective layer disclaimer

All statements in this entry are made strictly at the **effective layer** of the Tension Universe (TU) framework.

* The goal of this document is to specify an **effective-layer encoding** of the origin-of-life problem in terms of:

  * state spaces,
  * observables and fields,
  * invariants and tension scores,
  * singular sets and domain restrictions,
  * experiment and module templates for AI and modeling work.

* This page does **not**:

  * prove or disprove any canonical statement about the origin of life,
  * claim that life is easy or hard to originate in the real universe,
  * introduce new theorems beyond what is already established in the cited literature,
  * assert that any specific origin-of-life scenario has been verified in nature.

* We do **not**:

  * specify any underlying axiom system for TU itself,
  * reveal deep TU generative rules or constructive derivations,
  * give explicit mappings from raw experimental or planetary data to internal TU fields.
    All such mappings are treated as part of an admissible encoding class described at this layer.

* Whenever this document speaks about:

  * state spaces such as `M_life`,
  * observables such as `Phi_energy` or `Phi_min_life`,
  * tension measures such as `DeltaS_prebiotic` or `Tension_OoL`,
  * counterfactual worlds such as World T and World F,
    these objects live inside the effective layer and are subject to the constraints described here and in the TU charters.

* Experiments in Section 6 can **falsify or support** particular effective-layer encodings.
  Success or failure of these experiments does **not** resolve the real origin-of-life question, which requires independent empirical and theoretical work.

This page uses the **hybrid semantics** choice recorded in the header. Continuous quantities and discrete entities are combined in a controlled way that remains within the effective-layer boundary.

---

## 1. Canonical problem and status

### 1.1 Canonical statement

The origin of life problem asks:

Under realistic planetary conditions, how can purely physical and chemical processes give rise to systems that are:

* self-maintaining,
* capable of reliable heredity,
* able to undergo open-ended evolution,

so that it is meaningful to call them living?

More precisely, the problem is to understand whether there exist physically plausible pathways from nonliving matter to minimal living systems that:

* respect known physical and chemical laws,
* do not require ad hoc fine tuning beyond what planetary environments could provide,
* produce entities that satisfy reasonable criteria for life, such as:

  * bounded compartments,
  * metabolism or energy processing,
  * information storage and inheritance,
  * variation and selection.

There is no single universally agreed formal definition of life. However, for the purposes of this BlackHole entry, we treat minimal living systems as those that:

* maintain themselves far from thermodynamic equilibrium by harvesting and dissipating free energy,
* preserve and transmit informational structures with better than random fidelity,
* can generate heritable variation that selection can act upon.

### 1.2 Status and difficulty

The origin of life remains an open, cross disciplinary problem.

Key points:

* There is no consensus on a unique pathway from purely chemical environments to minimal life.

* Several major scenario families exist, including but not limited to:

  * metabolism first,
  * RNA first or other information first,
  * lipid first or compartment first,
  * network or collective origins.

* Modern work emphasizes:

  * far from equilibrium chemistry and driven systems,
  * autocatalytic and mutually catalytic networks,
  * protocell models that combine compartments, chemistry, and heredity.

Despite extensive theoretical and experimental progress, no single scenario has been demonstrated that:

* is robust over a wide range of planetary conditions,
* explains the emergence of all key life properties in a unified way,
* is widely accepted as the canonical solution.

The problem is extremely difficult because it sits at the intersection of:

* physical chemistry,
* planetary science and geochemistry,
* molecular biology and evolution,
* information theory and thermodynamics.

### 1.3 Role in the BlackHole project

Within the BlackHole S problem collection, Q071 plays the following roles:

1. It is the anchor node for biological emergence problems at the boundary between nonliving and living matter.

2. It provides a template for encoding emergence under constraint as a tension problem, where:

   * energy flows,
   * molecular complexity,
   * information storage,
   * environmental variability

   must be in a mutually compatible regime for life like systems to appear and persist.

3. It supplies reusable components for:

   * prebiotic chemistry problems,
   * major transitions in evolution,
   * biosphere and planetary co evolution,
   * analogies between biological origin and AI emergence in design spaces.

### References

1. NASA Astrobiology Program, “The Origins of Life”, official overview article on origin of life research directions and constraints.
2. John Maynard Smith, Eors Szathmary, “The Origins of Life: From the Birth of Life to the Origin of Language”, Oxford University Press, 1999.
3. Pier Luigi Luisi, “The Emergence of Life: From Chemical Origins to Synthetic Biology”, Cambridge University Press, 2006.
4. Gesteland, Cech, Atkins (editors), “The RNA World”, Cold Spring Harbor Laboratory Press, second edition, and later editions, for RNA centered origin scenarios.

---

## 2. Position in the BlackHole graph

This block records how Q071 sits in the BlackHole graph. Each edge has a one line reason that points to concrete components or tension patterns.

### 2.1 Upstream problems

Upstream nodes provide foundations in chemistry, planetary context, and general constraints.

* Q061 (BH_CHEM_BOND_NATURE_L3_061)
  Reason: supplies effective descriptions of bonding and strong correlation in complex molecular systems, which constrain which prebiotic structures are physically realistic.

* Q068 (BH_CHEM_PREBIOTIC_NETWORK_L3_068)
  Reason: provides prebiotic reaction network templates and far from equilibrium chemistry patterns that serve as the chemical substrate for origin of life paths.

* Q093 (BH_EARTH_CARBON_CYCLE_L3_093)
  Reason: encodes large scale carbon cycling and planetary redox context that set long timescale boundary conditions for prebiotic environments.

### 2.2 Downstream problems

Downstream nodes reuse components or depend on Q071 tension structure.

* Q072 (BH_BIO_GENETIC_CODE_L3_072)
  Reason: reuses information channel and coding components that Q071 defines for pre genetic information carriers.

* Q073 (BH_BIO_EVO_COMPLEXITY_L3_073)
  Reason: builds on Q071 life bootstrapping path patterns to describe later major evolutionary transitions.

* Q079 (BH_BIO_ORIGIN_EUKARYOTES_L3_079)
  Reason: uses Q071 protocell and metabolic tension components as base states for endosymbiosis based scenarios.

* Q080 (BH_BIO_BIOSPHERE_LIMITS_L3_080)
  Reason: treats Q071 emergence of living systems as the initial condition for long run biosphere adaptability analyses.

### 2.3 Parallel problems

Parallel nodes share similar tension types but do not directly depend on Q071.

* Q078 (BH_BIO_DEVELOPMENTAL_L3_078)
  Reason: both encode mappings between underlying configurations and emergent stable phenotypes under strong constraints, but at different stages of biological organization.

* Q091 (BH_EARTH_CLIMATE_SENS_L3_091)
  Reason: both express consistency_tension between global physical conditions and emergent system level behavior in driven, dissipative systems.

* Q032 (BH_PHYS_QTHERMO_L3_032)
  Reason: parallel in expressing tension between microscopic dynamics and macroscopic thermodynamic laws in far from equilibrium regimes.

### 2.4 Cross domain edges

Cross domain edges connect Q071 to problems in other domains that can reuse its components.

* Q059 (BH_CS_INFO_THERMODYN_L3_059)
  Reason: reuses entropy to information tradeoff functionals defined in Q071 when analyzing the thermodynamic cost of maintaining informational structures.

* Q098 (BH_EARTH_ANTHROPOCENE_L3_098)
  Reason: uses origin of life style feedback maps as references when modeling later anthropogenic feedback loops as another layer of self modifying biosphere.

* Q121 (BH_AI_ALIGNMENT_L3_121)
  Reason: reuses emergence under constraint components to frame AI emergence under safety constraints as an abstract life like origin problem in design space.

---

## 3. Tension Universe encoding (effective layer)

All content in this block is at the effective layer. We only describe:

* state spaces,
* observables and fields,
* invariants and tension scores,
* singular sets and domain restrictions.

We do not describe any hidden generative rules or explicit mappings from raw data to internal TU fields. All such mappings are treated as elements of an admissible encoding class, described in Section 3.6 and governed by the TU charters.

### 3.1 State space

We assume a semantic state space

```txt
M_life
```

with the following effective interpretation:

* Each state `m` in `M_life` represents a coarse grained prebiotic to proto life world slice for some environment window. This includes:

  * distributions of relevant small molecules, polymers, and complexes,
  * effective descriptions of energy flow and disequilibrium,
  * indicators of information carrying structures such as templates, polymers, or reaction networks,
  * coarse indicators of self maintenance and replication.

We do not specify how these states are built from experimental or simulation data. We only assume that, for any physically meaningful environment window, there exist states in `M_life` that encode summaries appropriate to that window.

### 3.2 Observables and fields

We introduce the following observables and fields on `M_life`. Each is a map from `M_life` to a real parameter region inside a fixed parameter space.

1. Free energy throughput observable

   ```txt
   Phi_energy(m) >= 0
   ```

   * Input: `m` in `M_life`.
   * Output: an effective scalar describing the rate of usable free energy flow through the environment window represented by `m`.
   * Interpretation: low values mean too little driving, extremely high values may correspond to destructive or highly chaotic regimes.

2. Structural complexity observable

   ```txt
   Phi_structure(m) >= 0
   ```

   * Input: `m` in `M_life`.
   * Output: an effective scalar summarizing the richness and diversity of molecular assemblies and networks at a chosen coarse resolution.
   * Interpretation: too low means only simple components, too high may signal fragile, over fragmented structures.

3. Replication fidelity observable

   ```txt
   Phi_repl(m) in [0, 1]
   ```

   * Input: `m` in `M_life`.
   * Output: an effective measure of replication fidelity of information carrying structures, where 0 means no meaningful heredity and 1 means perfect copying at the considered scale.

4. Compartmentalization observable

   ```txt
   Phi_compartment(m) >= 0
   ```

   * Input: `m` in `M_life`.
   * Output: an effective scalar describing the prevalence and robustness of bounded compartments, such as protocells, vesicles, or other micro environments.

5. Minimal life indicator

   ```txt
   Phi_min_life(m) in [0, 1]
   ```

   * Input: `m` in `M_life`.
   * Output: an effective indicator of how close the configuration is to satisfying a chosen set of minimal life criteria.
     Values near 1 indicate that:

     * self maintenance,
     * heredity,
     * evolvability
       are all present at the coarse level, while values near 0 indicate nonliving regimes.

### 3.3 Tension measures

We define three primary mismatch or tension measures.

1. Prebiotic energy structure tension

   ```txt
   DeltaS_prebiotic(m) >= 0
   ```

   * Measures the mismatch between free energy throughput and structural complexity.
   * Intended behavior:

     * large if `Phi_energy` is too low to sustain the observed `Phi_structure`,
     * large if `Phi_energy` is so high that structures encoded in `Phi_structure` cannot persist,
     * small when there is a compatible band of energy input that supports the structures present.

2. Information fidelity tension

   ```txt
   DeltaS_info(m) >= 0
   ```

   * Measures the mismatch between information richness and replication fidelity.
   * Intended behavior:

     * large if there is high structural or informational diversity but replication is so error prone that stable heredity cannot emerge,
     * small when there is a balance between complexity and fidelity that allows accumulation of functional information.

3. Environmental compatibility tension

   ```txt
   DeltaS_env(m) >= 0
   ```

   * Measures the mismatch between environmental fluctuations and the stability of self maintaining structures.
   * Intended behavior:

     * large if environmental variation is so extreme that compartments or networks cannot persist,
     * large if the environment is too static to allow exploration and selection,
     * small in regimes where environmental variation supports exploration without constant destruction.

We do not specify explicit formulas for these quantities at this level. We only require that each is a well defined, nonnegative function on `M_life` that can be estimated from suitable summaries inside the hybrid semantics choice.

### 3.4 Combined origin of life tension

We define a combined origin of life tension functional:

```txt
Tension_OoL(m) = a * DeltaS_prebiotic(m)
               + b * DeltaS_info(m)
               + c * DeltaS_env(m)
```

where:

* `a`, `b`, `c` are fixed positive weights chosen once for a given encoding family,
* `Tension_OoL(m) >= 0` for all `m` in `M_life`,
* low values indicate regimes favorable for emergence and persistence of minimal life,
* high values indicate regimes that strongly resist such emergence.

The choice of weights is part of the encoding design. For a given family of encodings, the weights are:

* selected from a finite, pre specified set of allowed triples `(a, b, c)` that is documented together with the encoding,
* fixed before any evaluation on real or simulated data,
* not adjusted in response to observed tension outputs.

### 3.5 Singular set and domain restriction

Some states may not support meaningful evaluation of the observables defined above. We collect such states into a singular set:

```txt
S_sing = {
  m in M_life :
    Phi_energy(m), Phi_structure(m), Phi_repl(m), or Phi_compartment(m)
    is undefined, not finite, or inconsistent with known physical constraints
}
```

We define the regular domain:

```txt
M_reg = M_life \ S_sing
```

All tension analysis for Q071 is restricted to `M_reg`. When an experiment or protocol would attempt to evaluate `Tension_OoL(m)` for a state outside `M_reg`, the result is treated as out of domain and not as evidence about the viability of origin of life pathways.

### 3.6 Encoding class and fairness constraints

The objects and functionals in this section are instantiated through an **admissible encoding class**, which is constrained to avoid arbitrary tuning.

* For each concrete study or tool there is:

  * a finite family of allowed mappings from experimental or simulated summaries to states in `M_life`,
  * a finite family of formulas or parametrizations for `DeltaS_prebiotic`, `DeltaS_info`, and `DeltaS_env`,
  * a finite set of allowed weight triples `(a, b, c)` as described above.

* An admissible encoding is defined by:

  * choosing one mapping into `M_life` from the allowed family,
  * choosing one set of formulas or parametrizations for the three `DeltaS` measures,
  * choosing one weight triple `(a, b, c)` from the allowed set.

* These choices must satisfy the following fairness constraints:

  * they are made before inspecting the tension outputs for the data that will be used in evaluation,
  * they are recorded in a way that allows external audit,
  * they are not modified in response to particular tension results for individual states or paths,
  * if a new encoding is proposed, it is evaluated as a new element of the encoding class rather than as a hidden adjustment of an existing one.

The detailed rules for defining encoding families, documenting choices, and preventing post hoc tuning are governed by the **TU Encoding and Fairness Charter**. This page only specifies how those rules are applied at the level of Q071.

---

## 4. Tension principle for this problem

This block states how Q071 is characterized as a tension problem within TU, at the effective layer.

### 4.1 Core origin of life principle

We encode the origin of life problem as a statement about the existence and structure of low tension paths in `M_life`.

We consider paths

```txt
gamma = (m_0, m_1, ..., m_K)
```

where:

* `m_0` encodes a purely chemical prebiotic state,
* `m_K` encodes a minimal living state with `Phi_min_life(m_K)` close to 1,
* intermediate states are in `M_reg`.

For a given path `gamma`, we define the path tension:

```txt
Tension_path(gamma) = max over k in {0,...,K} of Tension_OoL(m_k)
```

The core origin of life tension principle is stated at the effective layer as follows:

* In life friendly planetary settings, there exist paths from nonliving to minimal living states in `M_reg` whose path tension stays within a moderate band.
* In life hostile settings, any such path must cross segments with high path tension that cannot be removed while staying within realistic physical and environmental constraints.

This principle does not claim a unique microscopic mechanism. It only describes structural differences in the space of possible pathways when viewed through Q071 tension observables.

### 4.2 Life friendly vs life hostile regimes

We say an environment class is life friendly at the effective layer if, for realistic initial states:

* there exist many paths `gamma` that connect nonliving to minimal living states,
* the corresponding `Tension_path(gamma)` values are bounded by a relatively low threshold,
* these low tension paths persist under moderate changes in planetary parameters, such as energy flux or composition.

We say an environment class is life hostile if:

* any path from nonliving to minimal living states in `M_reg` must cross segments where `Tension_OoL(m_k)` remains above a high threshold for many steps,
* small parameter changes do not open new low tension paths.

In this language the origin of life question asks which regime Earth like and other planetary environments fall into, once we fix an admissible encoding.

---

## 5. Counterfactual tension worlds

We describe two counterfactual worlds, both at the effective layer:

* World T: life emergence is generically supported.
* World F: life emergence is extremely fine tuned or effectively impossible.

We do not specify deep microscopic details. We only describe patterns of observables and tension.

### 5.1 World T (life friendly origin)

In World T:

1. Prebiotic corridors

   * For a broad range of plausible prebiotic chemistries and energy fluxes, there exist families of paths `gamma` in `M_reg` with:

     ```txt
     Tension_path(gamma) <= tau_T_low
     ```

     where `tau_T_low` is a moderate threshold.

2. Robustness to parameter changes

   * When planetary parameters such as energy input, pH, and composition are varied within realistic bounds, low tension paths deform but do not disappear.
     The band of viable regimes occupies a significant volume in parameter space.

3. Multiple mechanistic routes

   * Metabolism first, information first, and compartment first scenarios, when encoded as paths in `M_life`, all admit low tension representatives.
     They share common structural features when viewed through `DeltaS_prebiotic`, `DeltaS_info`, and `DeltaS_env`.

4. Convergence to minimal life

   * Many initial states flow, under coarse grained dynamics, into regions where `Phi_min_life(m)` increases and `Tension_OoL(m)` decreases, so the emergence of minimal life is likely over geological timescales.

### 5.2 World F (life hostile origin)

In World F:

1. Narrow or absent low tension corridors

   * For most plausible planetary parameter settings, any path from prebiotic to minimal living states satisfies:

     ```txt
     Tension_path(gamma) >= tau_F_high
     ```

     where `tau_F_high` is a high threshold that reflects structural obstacles.

2. Extreme fine tuning

   * Only extremely narrow, finely tuned subsets of parameter space admit marginal paths where `Tension_path(gamma)` is not overwhelmingly large, and even these paths may be fragile to small perturbations.

3. Mechanistic fragility

   * Specific mechanisms such as a particular metabolism first route may appear viable in isolation.
     When environmental and network constraints are fully accounted for, `DeltaS_prebiotic`, `DeltaS_info`, or `DeltaS_env` become large, and low tension paths collapse.

4. Flow to nonliving attractors

   * Typical initial states flow into regions where `Phi_min_life(m)` remains near 0 and `Tension_OoL(m)` stays high or oscillatory, so the emergence of minimal life is extremely unlikely even over long times.

### 5.3 Interpretive note

These counterfactual worlds do not assert that our universe belongs to either case. They state that, if we could construct effective models of prebiotic and proto life regimes that are consistent with data and with the TU charters, then:

* World T and World F would give distinct patterns in:

  * path counts,
  * path tensions,
  * robustness under parameter variation.

Experiments and simulations can then test whether specific Q071 encodings behave more like World T or World F in controlled settings at the effective layer.

---

## 6. Falsifiability and discriminating experiments

This block specifies experiments and protocols that can:

* test the coherence of the Q071 encoding,
* distinguish between different origin of life tension models,
* provide evidence for or against particular parameter choices.

These experiments cannot prove or disprove that life origin is easy or hard in reality. They can falsify or support specific effective-layer encodings inside the admissible class.

### Experiment 1: Protocell ensemble tension profiling

**Goal**
Test whether a proposed encoding of `Tension_OoL` can distinguish regimes where protocell like systems emerge generically from regimes where they remain rare or unstable in laboratory experiments.

**Setup**

* Prepare families of in vitro protocell systems, for example:

  * fatty acid vesicles,
  * lipid vesicles with encapsulated catalysts,
  * other compartment like assemblies,

  under controlled conditions of composition, energy input, and environmental cycling.

* Before any measurements and tension calculations, fix:

  * a concrete procedure for mapping experimental summaries to states `m_lab` in `M_reg`,
  * a concrete choice of formulas for `DeltaS_prebiotic`, `DeltaS_info`, and `DeltaS_env` from the admissible encoding class,
  * one allowed weight triple `(a, b, c)` for this experimental program.

* For each experimental condition, define an effective state `m_lab` in `M_reg` that summarizes:

  * free energy throughput,
  * structural complexity of compartments and internal contents,
  * replication fidelity for any templating structures,
  * stability and turnover of compartments.

These choices and procedures are documented and made available for external audit, in line with the TU Encoding and Fairness Charter.

**Protocol**

1. For each condition, construct `m_lab` using the fixed procedure that was chosen before inspecting results.

2. Estimate `Phi_energy(m_lab)`, `Phi_structure(m_lab)`, `Phi_repl(m_lab)`, and `Phi_compartment(m_lab)` from experimental summaries.

3. Compute `DeltaS_prebiotic(m_lab)`, `DeltaS_info(m_lab)`, `DeltaS_env(m_lab)` using the chosen encoding.

4. Compute `Tension_OoL(m_lab)` for each condition.

5. Group conditions into:

   * emergent protocell regimes, where robust, self maintaining compartments are observed,
   * non emergent regimes, where such structures are absent or extremely fragile.

6. Compare the distributions of `Tension_OoL(m_lab)` between the two groups.

**Metrics**

* Separation between the distributions of `Tension_OoL(m_lab)` in emergent vs non emergent regimes.
* Stability of this separation when experimental noise and minor changes in encoding parameters inside the admissible class are taken into account.
* Sensitivity analysis on how much the classification depends on the weights `(a, b, c)` within the allowed set.

**Falsification conditions**

* If, across a wide range of reasonable parameter choices that respect known chemistry and thermodynamics and that obey the fairness constraints, the encoding assigns similar `Tension_OoL` values to regimes with clear protocell emergence and to regimes with no emergence, then the encoding is considered falsified as a useful origin of life tension model at this layer.
* If small, arbitrary changes in encoding details that remain inside the nominal class can flip the classification of many conditions without any clear physical reason, the encoding is considered unstable and rejected at this level.

**Semantics implementation note**
This experiment uses a mixed continuous and discrete representation consistent with the hybrid choice recorded in the header. Continuous aspects cover energy and concentration fields, while discrete aspects cover counts of compartments and template copies.

**Boundary note**
Falsifying a TU encoding at this level is not the same as solving the canonical origin of life statement. Failure of a particular `Tension_OoL` encoding in this laboratory context does not resolve the real origin of life problem. It only shows that the tested encoding is not an adequate effective-layer model for these systems.

---

### Experiment 2: Digital chemistries and artificial life models

**Goal**
Assess whether Q071 style tension encodings track known transitions between nonliving and life like regimes in computational chemistries and artificial life systems.

**Setup**

* Select or construct computational models such as:

  * artificial chemistries with reaction rules and spatial structure,
  * digital organisms in environments where replication, mutation, and selection are well characterized.

* Identify parameter regions where:

  * the system is known to remain in nonliving like states, without self maintaining replicators,
  * the system reliably develops self maintaining, evolving entities.

* Before running the sweeps, fix:

  * a mapping procedure from raw model states and statistics to effective states `m_dig` in `M_reg`,
  * specific formulas from the admissible class for the three `DeltaS` measures,
  * one allowed weight triple `(a, b, c)` for this analysis.

* Map model states to effective states `m_dig` by summarizing:

  * effective energy flow or resource consumption,
  * structural complexity of entities,
  * replication fidelity statistics,
  * stability of compartments or local structures.

These design choices are recorded so that an external auditor can reconstruct them.

**Protocol**

1. For each parameter setting and time window, construct `m_dig` according to the fixed mapping procedure.

2. Estimate observables `Phi_energy(m_dig)`, `Phi_structure(m_dig)`, `Phi_repl(m_dig)`, and `Phi_compartment(m_dig)` from model statistics.

3. Compute `DeltaS_prebiotic(m_dig)`, `DeltaS_info(m_dig)`, `DeltaS_env(m_dig)` and `Tension_OoL(m_dig)`.

4. Plot `Tension_OoL(m_dig)` across parameter sweeps that are known to pass through origin like transitions in the model.

5. Compare tension patterns with known phase diagrams of the model.

**Metrics**

* Correlation between low `Tension_OoL(m_dig)` regions and known life like regimes in the model.
* Ability of `Tension_OoL(m_dig)` to signal upcoming transitions as parameters approach critical values.
* Robustness of tension patterns to different but reasonable summary mappings from raw model states to `m_dig` inside the allowed family.

**Falsification conditions**

* If the encoding assigns consistently low tension to parameter regimes that are known to be nonliving in the model, while assigning consistently high tension to regimes that are known to produce self maintaining, evolving structures, the encoding is considered misaligned and rejected for Q071.
* If the encoding fails to show any structured variation in tension across parameter sweeps where the model exhibits sharp changes in behavior, the encoding is considered too insensitive to be useful for Q071.

**Semantics implementation note**
This experiment uses the same hybrid representation choice that is recorded in the header. Discrete model entities and continuous summary statistics are treated in a consistent way.

**Boundary note**
Falsifying or supporting a TU encoding on these artificial systems is not the same as answering how life actually arose on Earth. It only informs how good the encoding is as an abstract origin of life model at the effective layer.

---

## 7. AI and WFGY engineering spec

This block describes how Q071 can be used as an engineering module for AI systems within the WFGY framework, at the effective layer. All such uses respect the TU Effective Layer Charter and do not expose deep TU generative rules.

### 7.1 Training signals

We define several training signals for models that reason about origin of life scenarios.

1. `signal_life_path_coherence`

   * Definition: a penalty proportional to inconsistencies in `Tension_OoL` along a proposed origin of life path `gamma` described by the model. Large jumps into high tension states without explanation increase the penalty.
   * Purpose: encourage models to produce narratives in which progression from nonliving to living regimes follows relatively smooth low tension paths, or explicitly highlights where tension spikes and why.

2. `signal_prebiotic_compatibility`

   * Definition: a penalty based on `DeltaS_prebiotic(m)` and `DeltaS_env(m)` whenever the model proposes prebiotic environments or chemistries.
   * Purpose: discourage answers that rely on energy or environmental conditions that are incompatible with known constraints, by assigning higher tension to such proposals.

3. `signal_info_fidelity_band`

   * Definition: a signal based on `DeltaS_info(m)` when the model claims that reliable heredity and open ended evolution are possible in a scenario.
   * Purpose: ensure that claims of information rich heredity are paired with sufficient replication fidelity at the effective layer.

4. `signal_origin_assumption_clarity`

   * Definition: a signal that rewards explicit declaration of assumptions about environment, chemistry, and information carriers, and penalizes mixing incompatible assumptions without acknowledging transitions.
   * Purpose: encourage clear separation of different scenario families instead of blending them into a single vague story.

### 7.2 Architectural patterns

We outline module patterns that can reuse Q071 structures without exposing any deep TU rules.

1. `OoL_TensionHead`

   * Role: given an internal representation of an origin of life scenario, this module outputs estimates of `DeltaS_prebiotic`, `DeltaS_info`, `DeltaS_env`, and `Tension_OoL`.
   * Interface:

     * Inputs: encoded scenario features such as environmental conditions, chemistry, and information carriers.
     * Outputs: a small set of tension values and a combined `Tension_OoL` scalar.

2. `EnvScenarioFilter`

   * Role: filters or reweights proposed scenarios according to their tension values.
   * Interface:

     * Inputs: candidate scenario representations with associated tension outputs from `OoL_TensionHead`.
     * Outputs: scores that can be used to rank or discard scenarios that sit deep in high tension regions.

3. `LifePathPlanner`

   * Role: proposes multi step paths `gamma` from prebiotic conditions to minimal living states that minimize `Tension_path(gamma)` while satisfying external constraints.
   * Interface:

     * Inputs: initial and target conditions, plus constraints.
     * Outputs: candidate paths and their associated path tension metrics.

### 7.3 Evaluation harness

We suggest an evaluation harness for models augmented with Q071 modules.

1. Task selection

   * Construct a benchmark of questions and tasks related to origin of life scenarios, including:

     * explain and compare major scenarios,
     * critique impossible or highly speculative proposals,
     * design plausible lab or model experiments.

2. Conditions

   * Baseline condition: model with no explicit Q071 tension modules.
   * TU condition: model with `OoL_TensionHead` and `EnvScenarioFilter` active, and training signals from Section 7.1 integrated.

3. Metrics

   * Consistency: fraction of answers that maintain coherent environmental and chemical assumptions across multi step explanations.
   * Constraint respect: rate at which answers stay within known physical and chemical bounds.
   * Scenario clarity: qualitative rating of how well the model distinguishes different scenario families and states their assumptions.

4. Analysis

   * Compare baseline vs TU condition across these metrics.
   * Inspect cases where tension aware models change their answers or explanations in nontrivial ways that align better with scientific constraints.

### 7.4 60 second reproduction protocol

A minimal protocol to let external users experience the effect of Q071 encoding in an AI system.

* Baseline setup:

  * Prompt: ask the model to explain “How might life have emerged from nonliving chemistry on early Earth?” without mentioning tension or TU.
  * Observation: record whether the explanation quickly mixes incompatible assumptions or relies on vague “and then life appeared” steps.

* TU encoded setup:

  * Prompt: ask the same question but require the model to:

    * identify key stages in an origin path,
    * comment on whether each stage is likely to be low or high tension under Q071 style measures,
    * highlight critical bottlenecks where tension spikes.

  * Observation: compare the structure, explicit identification of bottlenecks, and use of constraints.

* Comparison metric:

  * Rate answers on structure, explicit handling of constraints, and clarity about what is speculative versus well grounded.

* What to log:

  * Full prompts,
  * full responses,
  * any Q071 tension estimates produced by internal modules, if available.

These logs allow later inspection of behavior without exposing any deep TU generative rules.

---

## 8. Cross problem transfer template

This block describes reusable components produced by Q071 and their transfer to other problems.

### 8.1 Reusable components produced by this problem

1. ComponentName: `PrebioticNetwork_TensionField`

   * Type: field or functional.

   * Minimal interface:

     * Inputs: coarse grained descriptions of prebiotic chemical networks and environmental conditions.
     * Output: `DeltaS_prebiotic(m)` and `DeltaS_env(m)` values for an effective state `m`.

   * Preconditions:

     * The input description must encode coherent networks and environment summaries at the chosen resolution.
     * Known physical and chemical constraints must be respected so that the resulting state belongs to `M_reg`.

2. ComponentName: `LifeBootstrap_PathPattern`

   * Type: experiment_pattern.

   * Minimal interface:

     * Inputs: specifications of initial nonliving states, candidate intermediate states, and minimal life criteria.
     * Output: a family of paths `gamma` and associated `Tension_path(gamma)` values.

   * Preconditions:

     * All states along each path must be mappable into `M_reg`.
     * Minimal life criteria must be stated clearly enough to evaluate `Phi_min_life(m_K)` for terminal states.

3. ComponentName: `EntropyToInformation_Tradeoff_OoL`

   * Type: functional.

   * Minimal interface:

     * Inputs: estimates of energy dissipation, entropy production, and information storage metrics for states in `M_life`.
     * Output: a summary scalar or small vector describing how effectively entropy production is being converted into stable informational structure.

   * Preconditions:

     * Inputs must be derived from compatible summaries so that comparisons across states are meaningful.

### 8.2 Direct reuse targets

1. Q068 (prebiotic reaction networks)

   * Reused component: `PrebioticNetwork_TensionField`.
   * Why it transfers: Q068 focuses on nonliving reaction networks and energy flows. Q071 field can be used to evaluate whether those networks sit in low or high tension regimes for life like emergence.
   * What changes: minimal life criteria are not invoked. Focus is on identifying life ready regions of parameter space rather than full origin paths.

2. Q072 (origin of the genetic code)

   * Reused component: `LifeBootstrap_PathPattern`.
   * Why it transfers: coding and translation systems can be treated as phases along a life bootstrapping path that begin after minimal life is already present.
   * What changes: the target states require richer information structures and coding capacity. `Phi_min_life` is supplemented with additional code specific indicators.

3. Q080 (biosphere adaptability and limits)

   * Reused component: `EntropyToInformation_Tradeoff_OoL`.
   * Why it transfers: long term biosphere behavior depends on how effectively the system converts energy flows into robust informational and structural complexity.
   * What changes: the functional is extended to higher levels of organization, aggregating over many living subsystems rather than focusing on the initial origin.

4. Q121 (AI alignment in design space)

   * Reused component: `LifeBootstrap_PathPattern`.
   * Why it transfers: alignment can be framed as the emergence of self maintaining agentic systems in design space, under multiple constraints, analogous to life like origin paths.
   * What changes: states represent AI design and deployment configurations, while tension components measure alignment risk and resource constraints instead of chemistry and prebiotic environment.

---

## 9. TU roadmap and verification levels

This block explains how Q071 is positioned along the TU verification ladder and what the next measurable steps are.

### 9.1 Current levels

* E_level: E1

  * A coherent effective layer encoding of origin of life tension has been specified.
  * Core observables, tension measures, and singular sets are defined in a way that can be instantiated without exposing deep TU rules.
  * At least two concrete experiments have been proposed with clear falsification conditions for specific encodings.

* N_level: N2

  * The narrative linking energy flows, structural complexity, information fidelity, and environmental conditions is explicit and internally coherent.
  * Counterfactual worlds and transfer patterns are described in a way that can be applied to laboratory systems, digital models, and AI engineering.

### 9.2 Next measurable step toward E2

To move from E1 to E2, one or more of the following should be carried out at the effective layer:

1. Implement a prototype tool that:

   * takes experimental or simulated summaries,
   * maps them to states in `M_life` using an admissible encoding,
   * computes `DeltaS_prebiotic`, `DeltaS_info`, `DeltaS_env`, and `Tension_OoL`,
   * publishes example tension profiles for real protocell experiments or digital chemistries as open data.

2. Use the prototype to evaluate several competing origin of life scenarios and show that:

   * the tool separates obviously viable from obviously non viable regimes in controlled tests,
   * conclusions are robust across reasonable variations in encoding details that remain inside the admissible class.

3. Document admissible encoding classes and fairness constraints for selecting mappings and weights, in a way that:

   * prevents arbitrary tuning away of tension,
   * allows independent groups to reimplement the same encoding and test reproducibility.

These steps operate entirely at the effective layer and do not require revealing any deep TU generative rules.

### 9.3 Long term role in the TU program

In the long term, Q071 is expected to serve as:

* the central biological emergence node that all later major transitions connect back to,
* a reference problem for designing tension measures that capture emergence under constraint in domains where full proofs or reconstructions are not feasible,
* a bridge between:

  * prebiotic chemistry,
  * planetary science,
  * evolutionary theory,
  * information thermodynamics,
  * AI emergence under safety constraints.

Q071 thus helps test whether the Tension Universe framework can organize reasoning about the origin of life in a way that is:

* scientifically grounded,
* falsifiable at the encoding level,
* reusable across multiple domains,

without claiming any resolution of the canonical origin of life problem.

---

## 10. Elementary but precise explanation

This block gives an explanation suitable for non specialists, while remaining aligned with the effective layer description.

The origin of life problem asks a simple looking question with very deep content:

How could something like a cell, which keeps itself going and makes copies of itself, arise from nothing but rocks, water, and simple molecules on a young planet?

In the Tension Universe view, we do not try to guess a single detailed story about early Earth. Instead, we look at three kinds of pressure that any origin of life story must satisfy:

1. There must be enough usable energy so that complex structures can form and keep running, but not so much that everything is constantly destroyed.

2. There must be a way to store and copy information well enough that useful structures are not lost in noise.

3. The environment must change in a way that allows exploration and selection, but not in a way that wipes out promising systems faster than they appear.

For any given situation, we attach numbers to these three pressures. When the numbers are small, we say the tension is low and life like systems could appear and survive. When they are large, we say the tension is high and life like systems are unlikely.

We then imagine paths that start from just chemistry and end at minimal life. Along each path, we ask:

* Does the combined tension stay moderate most of the way?
* Or are there unavoidable peaks where the tension is so high that the path is effectively blocked, given known physics and chemistry?

If there are many paths with low tension, the world is life friendly in this effective sense. If every path runs into very high tension, the world is life hostile.

Laboratory protocell experiments and digital life models let us test whether our way of measuring tension makes sense. If our tension measures cannot even tell apart simple cases where we already know that life like behavior appears or fails, then our encoding is wrong and must be replaced. If they do separate those cases, we gain some confidence that we are capturing something real about the structure of the origin of life problem, even though we are still far from a complete story of how life actually began on Earth.

This explanation does not claim that Earth belongs to World T or World F, or that life origin is easy or hard in the actual universe. It only explains how Q071 organizes different ideas and scenarios into a framework that can be tested and refined at the effective layer.

---

## Tension Universe effective-layer footer

This page is part of the **WFGY / Tension Universe** S problem collection.

### Scope of claims

* The goal of this document is to specify an effective layer encoding of the named problem.
* It does not claim to prove or disprove the canonical statement in Section 1.
* It does not introduce any new theorem beyond what is already established in the cited literature.
* It should not be cited as evidence that the corresponding open problem has been solved, or that any specific origin of life scenario is realized in nature.

### Effective-layer boundary

* All objects used here, including state spaces such as `M_life`, observables, invariants, tension scores, and counterfactual worlds, live inside the TU effective layer.
* No deep TU generative rule, axiom system, or internal construction of TU fields from raw data is exposed or assumed.
* Mappings from experimental, observational, or simulated data to TU objects are treated as elements of an admissible encoding class and are always subject to the TU Effective Layer Charter.

### Encoding and fairness

* Encodings of this problem are restricted to finite, pre specified families of:

  * data to state mappings,
  * tension formulas or parametrizations,
  * weight choices and refinement schemes.

* Choices inside those families are:

  * made before inspecting evaluation results for the data that will be used,
  * recorded in a way that supports independent reconstruction,
  * not adjusted in response to particular tension outputs for specific instances.

* These constraints are intended to prevent arbitrary tuning away of tension and to keep encodings falsifiable.

### Falsifiability and experiments

* Experiments and protocols described in this page are designed to test the behavior of Q071 encodings on laboratory systems, digital models, or AI reasoning tasks.
* A failed test falsifies a particular encoding or parameter choice at the effective layer, not the canonical origin of life statement itself.
* A successful test provides evidence that an encoding is coherent and useful, while still falling short of any claim that the real universe behaves exactly as described by that encoding.

### Relation to other TU charters

* The detailed rules for:

  * defining effective layer objects,
  * constructing and auditing encodings,
  * interpreting tension scales and thresholds,
    are given in the TU charters. This page should be read as an application of those rules to the specific case Q071, not as a replacement.

This page should be read together with the following charters:

* [TU Effective Layer Charter](../Charters/TU_EFFECTIVE_LAYER_CHARTER.md)
* [TU Encoding and Fairness Charter](../Charters/TU_ENCODING_AND_FAIRNESS_CHARTER.md)
* [TU Tension Scale Charter](../Charters/TU_TENSION_SCALE_CHARTER.md)
* [TU Global Guardrails](../Charters/TU_GLOBAL_GUARDRAILS.md)
