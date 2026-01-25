# Q084 · Long term memory storage mechanisms

## 0. Header metadata

```txt
ID: Q084
Code: BH_NEURO_MEMORY_STORE_L3_084
Domain: Neuroscience
Family: Memory and learning
Rank: S
Projection_dominance: I
Field_type: cognitive_field
Tension_type: consistency_tension
Status: Open
Semantics: continuous
E_level: E1
N_level: N2
Last_updated: 2026-01-25
```

---

## 1. Canonical problem and status

### 1.1 Canonical statement

The canonical question for Q084 is:

> How can long term memories be stored and remain stable in biological neural systems over timescales of months to decades, given that the underlying synaptic and molecular substrates turn over on much shorter timescales?

More precisely, Q084 asks for a mechanistic account that explains, at the level of neural circuits and synapses:

1. What the physical substrate of long term memory is in the brain.
2. How this substrate remains sufficiently stable over long periods despite molecular turnover, noise, and ongoing plasticity.
3. How this substrate remains compatible with continued learning and reorganization rather than saturating or collapsing.

The question is not only about which brain regions are involved, but about the concrete storage mechanisms and their stability properties across multiple spatial and temporal scales.

### 1.2 Status and difficulty

Several classes of mechanisms have been proposed as candidates for long term memory storage, including:

* persistent modifications of synaptic strength, for example through long term potentiation and long term depression,
* structural changes in synaptic connectivity, such as formation and elimination of dendritic spines,
* changes in intrinsic excitability of neurons,
* cell assembly and engram theories, where specific neuron populations encode and retrieve particular memories,
* molecular level mechanisms, such as persistent kinase activity, local protein synthesis, epigenetic marks, or prion like state changes.

Despite extensive experimental and theoretical work, there is no unified, quantitatively validated account that simultaneously explains:

* how memories can remain stable over years,
* how the underlying proteins and structures can be continuously renewed,
* how networks can keep learning new information without catastrophic interference,
* how storage capacity scales with brain size, energy, and structural constraints.

The problem is considered very hard because it couples molecular biology, synaptic biophysics, circuit level dynamics, systems level consolidation, and behavior. Many existing models address only a subset of these dimensions.

### 1.3 Role in the BlackHole project

Within the BlackHole S problem collection, Q084 plays several roles:

1. It is the core S level problem for the stability of memory in biological neural systems.
2. It provides a test case for cross scale tension between microscopic volatility and macroscopic stability.
3. It anchors a cluster of problems on learning, plasticity, sleep, and neurodegeneration, including:

   * Q083 (neural coding principles),
   * Q085 (rules of synaptic plasticity),
   * Q086 (fundamental function of sleep),
   * Q087 (mechanisms of neurodegenerative diseases).

Q084 is also a bridge between neuroscience and AI problems on memory architectures, continual learning, and stability plasticity tradeoffs.

### References

1. Eric R. Kandel, James H. Schwartz, Thomas M. Jessell, Steven A. Siegelbaum, and A. J. Hudspeth, “Principles of Neural Science”, 5th edition, McGraw Hill, 2012, chapters on synaptic plasticity and memory storage.
2. Larry R. Squire and Eric R. Kandel, “Memory: From Mind to Molecules”, 2nd edition, Roberts and Company Publishers, 2008.
3. Susumu Tonegawa, Mark D. Morrissey, and Takashi Kitamura, “The role of engram cells in the systems consolidation of memory”, Nature Reviews Neuroscience, 2018.
4. Wulfram Gerstner, Werner M. Kistler, Richard Naud, and Liam Paninski, “Neuronal Dynamics: From Single Neurons to Networks and Models of Cognition”, Cambridge University Press, 2014, sections on learning and memory.

---

## 2. Position in the BlackHole graph

This block records how Q084 sits inside the BlackHole graph as nodes and edges among Q001 to Q125. Each edge includes a one line reason that points to a concrete component or tension type.

### 2.1 Upstream problems

These problems provide prerequisites, tools, or conceptual foundations that Q084 relies on at the effective layer.

* Q083 (BH_NEURO_CODE_L3_083)
  Reason: Supplies general neural coding principles that constrain what patterns can serve as memory traces in networks.
* Q085 (BH_NEURO_PLASTICITY_RULES_L3_085)
  Reason: Provides effective rules for synaptic plasticity that underlie memory formation and modification.
* Q082 (BH_NEURO_BINDING_L3_082)
  Reason: Constrains how distributed neural features can be bound into coherent memory episodes at the circuit level.
* Q088 (BH_NEURO_DEV_PATTERN_L3_088)
  Reason: Describes how cortical maps develop, which sets initial structural conditions for where and how long term memories can be stored.

### 2.2 Downstream problems

These problems reuse Q084 components or depend on its tension structure.

* Q086 (BH_NEURO_SLEEP_FUNC_L3_086)
  Reason: Reuses memory stability and consolidation components to define how sleep stages support long term memory maintenance.
* Q087 (BH_NEURO_DEGEN_DISEASE_L3_087)
  Reason: Uses Q084 invariants as baselines for identifying pathological breakdowns of long term memory storage.
* Q089 (BH_NEURO_PREDICTIVE_CODE_L3_089)
  Reason: Depends on stable memory substrates to implement predictive coding across long timescales.

### 2.3 Parallel problems

Parallel nodes share similar tension types but no direct component dependence.

* Q081 (BH_NEURO_CONSCIOUS_HARD_L3_081)
  Reason: Both involve consistency_tension between neural processes and high level cognitive phenomena that persist over time.
* Q091 (BH_EARTH_CLIMATE_SENS_L3_091)
  Reason: Both deal with long term stability of a system state under ongoing fluctuations and internal turnover.

### 2.4 Cross domain edges

Cross domain edges connect Q084 to problems in other domains that can reuse its components.

* Q104 (BH_AI_MEMORY_ARCH_L3_104)
  Reason: Reuses Q084 stability plasticity tension components as templates for AI memory architecture design.
* Q105 (BH_AI_CONTINUAL_LEARN_L3_105)
  Reason: Uses Q084 invariants to define acceptable tradeoffs between retaining old information and learning new tasks.
* Q120 (BH_AI_SAFETY_SPEC_L3_120)
  Reason: Reuses long term stability patterns as analogies for maintaining safety relevant information in AI systems over long deployment periods.

All cross domain references are via Q identifiers and do not require external links.

---

## 3. Tension Universe encoding (effective layer)

All content in this block is at the effective layer. We describe only:

* state spaces,
* observables and fields,
* invariants and tension scores,
* singular sets and domain restrictions.

We do not describe any hidden generative rules or any explicit mapping from raw biological data to internal TU fields.

### 3.1 State space

We assume a state space

`M_mem`

with the following interpretation:

* Each element `m` in `M_mem` represents a coherent configuration of a memory relevant neural system across a set of spatial and temporal scales.

At the effective layer, a state `m` packages:

* coarse summaries of synaptic strengths and connectivity patterns in selected brain regions,
* summaries of structural features such as spine densities and network motifs,
* summaries of molecular and cellular processes that influence stability, such as turnover rates and plasticity statistics,
* summaries of behavioral performance on memory tasks over time.

We do not specify how these summaries are constructed from experimental measurements. We only assume that:

* for any experimental condition and time window of interest, there exist states in `M_mem` that encode the corresponding effective summaries.

### 3.2 Effective fields and observables

We define several effective observables on `M_mem`. All observables are treated as real valued or low dimensional vector valued functions of `m`.

1. Memory retention profile

```txt
R_mem(m; tau)
```

* Input: a state `m` and a retention interval `tau` in a fixed range of timescales.
* Output: a scalar summarizing how much of a reference memory can be retrieved after delay `tau`.
* Interpretation: higher values indicate better retention.

2. Substrate turnover profile

```txt
T_sub(m; tau)
```

* Input: the same `m` and time interval `tau`.
* Output: an estimate of how much of the underlying physical substrate for memory has been replaced during `tau`, for example through protein turnover or structural remodeling.

3. Stability mismatch observable

```txt
DeltaS_stability(m; tau)
```

* Input: state `m` and `tau`.
* Output: a nonnegative scalar measuring the mismatch between observed retention `R_mem(m; tau)` and what would be expected from the observed turnover `T_sub(m; tau)` under a simple baseline model that does not include special stabilizing mechanisms.
* Properties:

  * `DeltaS_stability(m; tau) >= 0` for all `m` and `tau`,
  * `DeltaS_stability(m; tau) = 0` when retention is fully explained by a baseline model given the turnover, within a tolerated error band.

4. Plasticity load observable

```txt
L_plast(m)
```

* Input: state `m`.
* Output: a scalar summarizing the amount of new learning or plasticity events that occur within a fixed reference period.
* Interpretation: high `L_plast(m)` means the system is strongly engaged in learning and adaptation.

5. Interference mismatch observable

```txt
DeltaS_interf(m)
```

* Input: state `m`.
* Output: a nonnegative scalar summarizing the degree to which long term memories are degraded when substantial new learning occurs, beyond what a reference balanced plasticity model would predict.
* Properties:

  * `DeltaS_interf(m) >= 0` for all `m`,
  * `DeltaS_interf(m)` is small if the system manages stability plasticity tradeoffs well.

6. Combined memory storage mismatch

Given fixed positive weights `w_stab` and `w_interf` that satisfy

```txt
w_stab + w_interf = 1
```

we define:

```txt
DeltaS_mem(m) = w_stab * DeltaS_stability(m; tau_ref)
              + w_interf * DeltaS_interf(m)
```

for a fixed reference interval `tau_ref` chosen within the long term memory range.

The weights and `tau_ref` are part of an admissible encoding class defined at the effective layer and must be chosen before examining detailed experimental outcomes.

### 3.3 Effective tension tensor components

We assume an effective tension tensor over `M_mem` consistent with the TU core decision:

```txt
T_ij(m) = S_i(m) * C_j(m) * DeltaS_mem(m) * lambda_mem(m) * kappa_mem
```

where:

* `S_i(m)` is a family of source factors representing how strongly different memory related subsystems contribute to the overall state, for example hippocampal, cortical, and subcortical components.
* `C_j(m)` is a family of receptivity factors indicating how sensitive different cognitive or behavioral outputs are to memory storage mismatches.
* `DeltaS_mem(m)` is the combined storage mismatch defined above.
* `lambda_mem(m)` encodes the current convergence class of the memory subsystem, for example stable, adapting, or failing, within a fixed bounded range.
* `kappa_mem` is a coupling constant that sets the overall scale of consistency_tension for Q084.

The detailed indexing sets for `i` and `j` are not needed at the effective layer. It is sufficient that each product is well defined and finite for all states in the regular domain.

### 3.4 Invariants, admissible encodings, and constraints

To prevent hidden parameter tuning, we restrict attention to an admissible encoding class `E_mem` with the following properties:

1. Finite reference library

   * A fixed finite library of baseline models is specified for:

     * how retention should decay as a function of substrate turnover in the absence of special stabilizing mechanisms,
     * how interference should scale with plasticity load in a simple balanced plasticity model.

   * Each library element defines baseline predictions for `R_mem` and interference behaviour. The library is fixed before any evaluation of specific experimental datasets.

2. Fixed parameter ranges

   * The weights `w_stab` and `w_interf` satisfy:

     ```txt
     w_stab in [0.3, 0.7]
     w_interf in [0.3, 0.7]
     w_stab + w_interf = 1
     ```

   * A particular choice within these ranges is selected once per study or protocol and not adjusted post hoc in response to observed results.

3. Resolution and refinement

   * The retention interval `tau_ref` is chosen from a discrete set of intervals that cover the long term range, for example a fixed set of days to months.
   * Refinement corresponds to using more intervals from this discrete set and more detailed descriptions of the same domains, not to redefining the underlying variables.

4. Encoding stability

   * Small changes in the summaries that define `m` lead to small changes in `DeltaS_stability`, `DeltaS_interf`, and `DeltaS_mem` in the usual sense of continuity for real valued functions.

Under these constraints, the memory storage inconsistency described by `DeltaS_mem(m)` cannot be trivially removed by reselecting reference models, weights, or resolution after inspecting the data.

### 3.5 Singular set and domain restrictions

Some states may yield undefined or unbounded mismatch measures, for example if:

* retention data are missing or inconsistent,
* substrate turnover or plasticity statistics are not measured in a compatible way,
* the chosen baseline models do not apply to the regime represented by `m`.

We define the singular set:

```txt
S_sing_mem = { m in M_mem :
               DeltaS_stability(m; tau_ref) is undefined or not finite
               or DeltaS_interf(m) is undefined or not finite }
```

The regular domain for Q084 analysis is:

```txt
M_reg_mem = M_mem \ S_sing_mem
```

All tension functionals and experiments in this document are interpreted only on `M_reg_mem`. When a state falls into `S_sing_mem`, it is treated as out of domain for Q084 rather than as evidence about memory storage mechanisms.

---

## 4. Tension principle for this problem

This block states how Q084 is viewed as a tension problem within the Tension Universe framework.

### 4.1 Core tension functional

We define the core memory storage tension functional:

```txt
Tension_mem(m) = G(DeltaS_stability(m; tau_ref),
                   DeltaS_interf(m))
```

where `G` is a nonnegative function satisfying:

```txt
Tension_mem(m) = alpha_mem * DeltaS_stability(m; tau_ref)
               + beta_mem * DeltaS_interf(m)
```

with fixed positive constants `alpha_mem` and `beta_mem` chosen in advance within a bounded range and not tuned to specific results.

Basic properties:

* `Tension_mem(m) >= 0` for all `m` in `M_reg_mem`.
* `Tension_mem(m)` is small when retention performance is consistent with substrate turnover and when interference is low relative to plasticity load.
* `Tension_mem(m)` grows when retention appears too good or too fragile relative to turnover, or when interference is excessive relative to plasticity load.

The exact numerical values of `alpha_mem` and `beta_mem` are part of the admissible encoding class `E_mem` and must be specified before running any experiments.

### 4.2 Low tension principle for viable memory storage

At the effective layer, viable long term memory mechanisms are characterized by the following principle:

> In a healthy biological system with functioning long term memory, there exist states in `M_reg_mem` that represent typical operating conditions, for which the memory storage tension `Tension_mem(m)` lies within a stable low tension band across a wide range of timescales and learning conditions.

More concretely, for any admissible encoding in `E_mem`, there should exist a family of states `{m_healthy}` such that:

```txt
Tension_mem(m_healthy) <= epsilon_mem
```

for some small threshold `epsilon_mem` that does not grow unbounded as measurement resolution improves and as more data from similar conditions are incorporated.

### 4.3 Failure modes as persistent high tension

If a proposed memory storage mechanism is fundamentally inadequate, then for any encoding within `E_mem` that faithfully reflects the relevant data, we expect to see persistent high tension:

```txt
Tension_mem(m_fail) >= delta_mem
```

for some strictly positive `delta_mem` that cannot be driven to zero by refining the summaries or adding more data, as long as the encoding remains faithful.

Examples of such failure modes include:

* retention that decays much faster than expected given the observed substrate turnover,
* retention that is only achievable at the cost of catastrophic interference when new learning occurs,
* retention that requires unrealistic fine tuning of parameters or structures that are not robust to noise or biological variability.

In this way, Q084 is framed as a distinction between worlds where long term memory can be implemented within a low tension regime and worlds where any implementation leads to unavoidable high tension.

---

## 5. Counterfactual tension worlds

We describe two counterfactual worlds at the effective layer:

* World T_mem: biological systems possess robust, scalable long term memory mechanisms.
* World F_mem: any apparent long term memory is fragile or requires unrealistic fine tuning, leading to persistent inconsistency.

### 5.1 World T_mem (robust long term memory)

In World T_mem:

1. Retention under turnover

   * For representative states `m_T` in `M_reg_mem`, retention profiles `R_mem(m_T; tau)` remain high over long intervals `tau` even when substrate turnover `T_sub(m_T; tau)` is substantial.
   * The stability mismatch `DeltaS_stability(m_T; tau)` remains bounded within a low band across a range of `tau` in the long term regime.

2. Stability plasticity tradeoff

   * Plasticity load `L_plast(m_T)` can be high without causing large `DeltaS_interf(m_T)`.
   * The system can acquire new memories while preserving many older ones, within capacity limits, such that `Tension_mem(m_T)` stays below `epsilon_mem` for typical operating conditions.

3. Cross scale coherence

   * Measurements at different resolutions and timescales lead to compatible estimates of `DeltaS_stability` and `DeltaS_interf`, so that refinement does not introduce systematic growth in tension.

### 5.2 World F_mem (fragile or unrealistic memory storage)

In World F_mem:

1. Retention collapse

   * For representative states `m_F`, either retention `R_mem(m_F; tau)` decays too quickly relative to turnover, producing large `DeltaS_stability`, or retention is maintained only under very restricted conditions.

2. Interference dominated regime

   * When plasticity load `L_plast(m_F)` increases, `DeltaS_interf(m_F)` grows rapidly, indicating that new learning severely disrupts previously stored memories.
   * No encoding in `E_mem` can keep `Tension_mem(m_F)` below a modest threshold while both retention and ongoing learning are present.

3. Refinement instability

   * As data resolution improves or longer timescales are considered, estimates of `DeltaS_stability` or `DeltaS_interf` show systematic growth, suggesting that apparent stability at coarse scales hides deeper inconsistency.

### 5.3 Interpretive note

These counterfactual worlds do not claim to construct internal TU fields from molecular or circuit level data. They only assert that, if models existed that faithfully summarize either robust or fragile memory regimes, then the effective tension patterns defined above would differ in the described ways.

---

## 6. Falsifiability and discriminating experiments

This block specifies experiments and protocols at the effective layer that can:

* test the coherence of the Q084 encoding,
* distinguish between different candidate memory storage mechanisms,
* falsify specific parameter choices within `E_mem`.

These experiments cannot fully solve Q084, but they can reject particular encodings or mechanistic hypotheses.

### Experiment 1: Retention versus substrate turnover in identified circuits

*Goal:*
Test whether candidate mechanisms can maintain low stability mismatch `DeltaS_stability` when both retention and substrate turnover are measured in the same circuit over long timescales.

*Setup:*

* Select a brain region and memory task where many studies already exist, for example hippocampal dependent spatial memory in rodents.

* For the same animals, measure:

  * behavioral retention performance `R_mem(m; tau)` at several long term intervals `tau`,
  * molecular or structural turnover `T_sub(m; tau)` for synaptic proteins or spines in the relevant circuits.

* Define baseline models in the reference library for how retention should decay if no special stabilizing mechanisms are present.

*Protocol:*

1. For each animal and interval `tau`, construct a state `m_data` in `M_reg_mem` that packages the effective summaries of retention and turnover.
2. Using the fixed baseline models and parameter choices from `E_mem`, compute `DeltaS_stability(m_data; tau)` for each interval.
3. Aggregate the values of `DeltaS_stability` across animals and intervals, and compute `Tension_mem(m_data)` using the fixed `alpha_mem` and `beta_mem`.
4. Compare the observed distribution of `Tension_mem(m_data)` with the predefined low tension band and with predictions from candidate mechanistic models.

*Metrics:*

* Distribution of `DeltaS_stability(m_data; tau)` across intervals.
* Fraction of states with `Tension_mem(m_data)` below the low tension band threshold.
* Consistency of tension estimates across different baseline models in the finite reference library.

*Falsification conditions:*

* If for all choices within `E_mem` the observed `Tension_mem(m_data)` is systematically above the low tension band for realistic parameter ranges, then the combination of candidate mechanisms and encoding is considered falsified at the effective layer.
* If small changes in the choice of baseline model within the finite library lead to arbitrarily large changes in `Tension_mem(m_data)` without corresponding changes in the underlying data, the encoding is considered unstable and rejected.

*Semantics implementation note:*
All observables in this experiment are treated as continuous summaries, such as retention probabilities and turnover fractions, consistent with the continuous field type stated in the metadata.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. This experiment can reject specific encodings or mechanistic combinations, but it does not by itself provide a complete solution to Q084.

---

### Experiment 2: Stability plasticity tradeoff under controlled training regimes

*Goal:*
Assess whether candidate memory storage mechanisms can keep `DeltaS_interf` and `Tension_mem` low when substantial new learning occurs over extended periods.

*Setup:*

* Use an animal model or artificial neural network model where training protocols can be precisely controlled.

* Design two regimes:

  * Regime A: moderate initial learning followed by long term maintenance with little new learning.
  * Regime B: comparable initial learning followed by sustained new learning in overlapping domains.

* Measure:

  * retention performance on initial memories in both regimes,
  * plasticity load `L_plast(m)` in both regimes,
  * any available correlates of substrate turnover.

*Protocol:*

1. For each condition and time point, construct states `m_A` and `m_B` in `M_reg_mem` encoding retention, plasticity load, and any turnover summaries.
2. Compute `DeltaS_interf(m_A)` and `DeltaS_interf(m_B)` using the fixed reference library and encoding parameters.
3. Compute `Tension_mem(m_A)` and `Tension_mem(m_B)` for each time point.
4. Compare tension trajectories between regimes and against predictions of specific mechanistic models, for example models relying mainly on synaptic weight changes versus those relying more on structural changes.

*Metrics:*

* Time courses of `DeltaS_interf` and `Tension_mem` in regimes A and B.
* Differences in tension between regimes for similar levels of plasticity load.
* Robustness of results across different base models within the finite reference library.

*Falsification conditions:*

* If a candidate mechanism predicts low interference under regime B but the observed `DeltaS_interf` and `Tension_mem` remain high across all admissible encodings, the candidate mechanism is considered falsified at the effective layer.
* If no choice within `E_mem` yields a clear separation between mechanisms with high and low interference in this protocol, the current encoding may be considered too coarse or misaligned and should be revised.

*Semantics implementation note:*
All quantities are treated as continuous summaries over time and across trials, consistent with the continuous field description of the observables.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. This experiment tests the adequacy of specific mechanisms and encodings, not the entire space of possible long term memory solutions.

---

## 7. AI and WFGY engineering spec

This block describes how Q084 can be used as an engineering module for AI systems in the WFGY framework, without exposing any deep TU generative rules.

### 7.1 Training signals

We define several training signals that encourage AI models to respect memory stability and plasticity constraints analogous to Q084.

1. `signal_retention_under_change`

   * Definition: a penalty signal derived from `DeltaS_stability` when the model is evaluated on tasks where the input distribution or internal representations are perturbed over time.
   * Purpose: encourage internal memory representations that remain usable even as other parts of the model are updated.

2. `signal_interference_cost`

   * Definition: a signal derived from `DeltaS_interf` when the model is trained sequentially on multiple tasks and then tested on earlier tasks.
   * Purpose: penalize internal configurations that cause large performance drops on earlier tasks after new training.

3. `signal_mem_tension_score`

   * Definition: an aggregate scalar equal to `Tension_mem(m_ai)` for an AI state `m_ai` that summarizes retention and plasticity behaviour across several tasks.
   * Purpose: provide a compact scalar to minimize during meta learning or architecture search for continual learning systems.

4. `signal_capacity_efficiency`

   * Definition: an additional signal that combines retention performance, plasticity load, and parameter or resource usage into an efficiency estimate.
   * Purpose: bias the system toward mechanisms that achieve low `Tension_mem` without excessive resource consumption.

### 7.2 Architectural patterns

We outline architecture level patterns that can reuse Q084 components.

1. `MemoryStabilityMonitor`

   * Role: a module that monitors internal representations and performance metrics over time and computes an estimate of `Tension_mem(m_ai)`.
   * Interface: takes as input summaries of performance on previous tasks, current training gradients, and resource usage; outputs a scalar tension score and a decomposition into stability and interference components.

2. `ProtectedReplayBuffer`

   * Role: a module that maintains a curated buffer of experiences or representations that support low `DeltaS_stability` and low `DeltaS_interf`.
   * Interface: receives candidate items for storage, scores them using Q084 inspired signals, and decides which to keep, refresh, or discard.

3. `DualStoreController`

   * Role: a control module that manages two or more memory subsystems, for example a fast plastic store and a slow stable store, using Q084 tension signals to decide when to transfer information between them.
   * Interface: takes tension estimates and task level performance as inputs; outputs storage and consolidation actions.

### 7.3 Evaluation harness

An evaluation harness for AI systems that incorporate Q084 inspired components can be structured as follows.

1. Task suite

   * A set of sequential tasks that require learning and retaining information over long horizons, such as continual classification, reinforcement learning with revisited tasks, or language tasks with persistent knowledge.

2. Conditions

   * Baseline condition: model with standard training procedures and no explicit Q084 modules.
   * TU condition: model with MemoryStabilityMonitor, ProtectedReplayBuffer, and possibly DualStoreController.

3. Metrics

   * Retention of early tasks after many training steps on later tasks.
   * Speed of adaptation on new tasks.
   * Capacity efficiency, for example retained performance per parameter or per unit of compute.
   * Q084 tension metrics, such as empirical proxies for `DeltaS_stability`, `DeltaS_interf`, and `Tension_mem`.

### 7.4 60 second reproduction protocol

A minimal protocol for external users to see the impact of Q084 inspired design.

* Baseline setup

  * Prompt: ask an AI model without Q084 modules to learn a small sequence of tasks and then test it on the initial tasks after further training.
  * Observation: record performance drops and any visible signs of catastrophic forgetting.

* TU encoded setup

  * Prompt: use the same tasks, but with explicit instructions that the model should use an internal mechanism to monitor memory stability and interference, exposed through a high level description of Q084 inspired signals.
  * Observation: record whether retention is improved and whether the explanation of the mechanism reflects the stability plasticity tradeoff.

* Comparison metric

  * Compare task accuracy and simple quantitative proxies for tension, such as drop in accuracy on early tasks divided by the amount of new training, between the two setups.

* What to log

  * Task sequences, training commands, evaluation metrics, and any exposed tension scores.
  * This allows external observers to replay the setup without needing to access internal implementation details.

---

## 8. Cross problem transfer template

This block describes reusable components produced by Q084 and how they transfer to other problems.

### 8.1 Reusable components produced by this problem

1. ComponentName: `MemStorageTensionFunctional`

   * Type: functional

   * Minimal interface:

     * Inputs: `retention_profile`, `turnover_profile`, `plasticity_profile`
     * Output: `tension_value` as a nonnegative scalar

   * Preconditions:

     * Profiles must be defined over compatible timescales and for the same system or model.

2. ComponentName: `StabilityPlasticityInvariant`

   * Type: observable

   * Minimal interface:

     * Inputs: `task_performance_history`, `training_history`
     * Output: `invariant_value` that combines retention and interference into a single stability plasticity indicator

   * Preconditions:

     * Histories must be long enough to capture both initial learning and later interference.

3. ComponentName: `MemSingularSetDetector`

   * Type: experiment_pattern

   * Minimal interface:

     * Inputs: a candidate dataset or model description
     * Output: a classification into regular domain or `S_sing_mem`, together with a short reason

   * Preconditions:

     * The dataset or model must provide enough information to assess whether the required observables are defined and bounded.

### 8.2 Direct reuse targets

1. Q086 (BH_NEURO_SLEEP_FUNC_L3_086)

   * Reused component: `MemStorageTensionFunctional`.
   * Why it transfers: sleep related hypotheses can be evaluated by measuring how tension changes when sleep patterns are manipulated.
   * What changes: observables are extended to include sleep stage statistics and replay indicators.

2. Q087 (BH_NEURO_DEGEN_DISEASE_L3_087)

   * Reused component: `StabilityPlasticityInvariant` and `MemSingularSetDetector`.
   * Why it transfers: neurodegenerative diseases can be characterized as trajectories that move systems into or near `S_sing_mem` and raise stability plasticity tension.
   * What changes: additional disease specific biomarkers are added to the inputs.

3. Q104 (BH_AI_MEMORY_ARCH_L3_104)

   * Reused component: `MemStorageTensionFunctional`.
   * Why it transfers: AI memory architectures can use the same functional to evaluate how well they balance retention and plasticity across tasks.
   * What changes: biological observables are replaced with model internal metrics.

4. Q105 (BH_AI_CONTINUAL_LEARN_L3_105)

   * Reused component: `StabilityPlasticityInvariant`.
   * Why it transfers: continual learning benchmarks directly measure interference and retention, so the invariant provides a standard way to compare methods.
   * What changes: the timescale axis is defined in training steps or episodes instead of biological time.

---

## 9. TU roadmap and verification levels

This block explains Q084’s current verification levels and next measurable steps.

### 9.1 Current levels

* E_level: E1

  * The effective layer encoding of long term memory storage tension is specified.
  * Observables, mismatch measures, and a core tension functional are defined, along with an admissible encoding class `E_mem`.
  * At least one concrete experimental protocol is provided that could falsify specific encodings.

* N_level: N2

  * The narrative linking microscopic turnover, macroscopic retention, and stability plasticity tradeoffs is explicit and internally coherent.
  * Counterfactual robust and fragile worlds are described and tied to observable patterns.

### 9.2 Next measurable step toward E2

To move from E1 to E2, at least one of the following should be implemented:

1. A concrete analysis of existing experimental datasets that jointly report retention and substrate turnover, using `DeltaS_stability`, `DeltaS_interf`, and `Tension_mem` with a specified encoding from `E_mem`.
2. A systematic study of artificial neural network models under continual learning regimes, where Q084 inspired tension metrics are used to compare different architectural mechanisms.

These steps require no changes to the effective layer definitions and do not expose any deep TU generative rules.

### 9.3 Long term role in the TU program

In the longer term, Q084 is expected to serve as:

* a reference node for all stability plasticity tradeoff problems, biological and artificial,
* a template for how to encode cross scale tension between volatile substrates and stable information,
* a bridge between neuroscience theories of memory and AI design of memory architectures.

---

## 10. Elementary but precise explanation

This block provides a non technical explanation aligned with the effective layer description.

The simple question behind Q084 is:

> How can the brain store memories for years when the parts that make up the brain are always changing?

Proteins are replaced, synapses appear and disappear, activity patterns fluctuate, and yet many people can remember events from childhood. At the same time, the brain keeps learning new things without completely erasing everything it already knows.

In the Tension Universe view, we do not try to guess every microscopic detail. Instead, we ask:

* For a given brain or model, how well do long term memories survive compared to how fast the underlying parts change?
* How much do old memories get damaged when new learning happens?
* Can we wrap these effects into a single number called memory storage tension?

We picture a space of states where each state summarizes:

* how well a memory is remembered after some time,
* how much the physical substrate has turned over in that time,
* how much new learning has taken place.

From these summaries we build:

* a stability mismatch that measures whether retention looks too good or too fragile given the turnover,
* an interference mismatch that measures how badly old memories suffer when new learning is heavy,
* a combined tension score that is low when things look healthy and high when they do not.

Then we compare two kinds of worlds.

* In a robust memory world, there are many situations where tension stays low: memories survive for a long time, new learning is possible, and the picture remains consistent when we look more closely.
* In a fragile memory world, tension cannot be kept low: either memories fade too fast, or they survive only by blocking new learning, or the picture falls apart when we add more detail.

This framing does not solve Q084. It does not tell us exactly which molecules or circuits are responsible. What it does is:

* force us to be clear about what counts as success or failure,
* give us practical ways to test candidate mechanisms and models,
* create a common language that connects biology and AI work on long term memory.

Q084 is therefore the memory storage counterpart of other high level consistency problems in the BlackHole and Tension Universe program, focused on the puzzle of how information can remain stable while the hardware that carries it never stops changing.
