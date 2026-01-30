# Q085 · General rules of synaptic plasticity

## 0. Header metadata

```txt
ID: Q085
Code: BH_NEURO_PLASTICITY_RULES_L3_085
Domain: Neuroscience
Family: Synaptic plasticity and learning rules
Rank: S
Projection_dominance: M
Field_type: dynamical_field
Tension_type: consistency_tension
Status: Open
Semantics: hybrid
E_level: E1
N_level: N1
Last_updated: 2026-01-30
```

---

## 0. Effective layer disclaimer

All statements in this entry are made strictly at the effective layer of the Tension Universe (TU) framework.

* We only specify state spaces, observables, effective fields, tension quantities, admissible encoding classes, and counterfactual patterns.
* We do not define or assume any explicit TU axiom system, field equations, or constructive generative rules for TU itself.
* We do not specify any explicit mapping from raw biological measurements or simulation data to internal TU fields. Any such mapping is treated as a black box that must respect the constraints of the encoding class defined in this document.
* We do not claim to prove or disprove the canonical problem in Section 1. This page does not introduce any new mathematical theorems beyond what is already established in the cited literature.
* No part of this document should be cited as a solution to Q085. It should only be used as an effective layer encoding and engineering tool.

The semantics for this page are hybrid. Discrete spike events and trial markers are combined with continuous summary statistics, as described in Section 3.2. Detailed global rules for effective layer behavior, encoding fairness, and tension scale are given in the Tension Universe charters listed in the footer of this page.

---

## 1. Canonical problem and status

### 1.1 Canonical statement

The canonical problem behind Q085 can be stated as follows:

> Are there general rules of synaptic plasticity that describe how synapses change their strength in response to activity, in a way that is sufficiently universal across brain regions, cell types, and species to count as genuine "laws" of learning in the brain, while remaining compatible with stability, biophysical constraints, and behavioral function?

More concretely, the question asks:

1. Whether synaptic changes can be summarized by a relatively small set of rule templates, such as:

   * Hebbian like rules ("cells that fire together wire together"),
   * spike timing dependent plasticity (STDP),
   * three factor rules involving pre, post, and modulatory signals,
   * homeostatic and metaplasticity mechanisms.
2. Whether these templates can be applied across many circuits without causing instability or loss of function.
3. How these rules balance local information, for example pre and post activity, with global constraints such as energy, safety, and network performance.

The "general rules" need not be identical at every synapse. The question is whether there is a compact family of rule types and parameters that accounts for most synaptic changes observed in healthy nervous systems.

### 1.2 Status and difficulty

Empirically, many types of synaptic plasticity have been observed:

* long term potentiation (LTP),
* long term depression (LTD),
* timing dependent rules (STDP),
* rate based plasticity,
* neuromodulator gated learning,
* homeostatic synaptic scaling,
* metaplasticity, which means plasticity of plasticity.

However:

* These phenomena vary widely across brain regions, cell types, and developmental stages.
* Detailed rules often depend on experimental conditions, for example spike timing windows, firing rates, and neuromodulatory context.
* Simple textbook rules are often only approximate descriptions.

The difficulty of the problem has at least two parts.

1. It is not clear whether all of this diversity can be compressed into a small family of rule templates without losing structure that is essential for real circuits.
2. Any proposed general rule must be checked against:

   * the need for long term network stability,
   * limitations on energy and molecular resources,
   * the ability to support learning across many tasks and timescales.

There is no accepted final theory that captures synaptic plasticity as a small set of general laws with a status comparable to simple relations like Ohm's law in basic electrical circuits.

### 1.3 Role in the BlackHole project

Within the BlackHole S problem collection, Q085 serves as:

1. The central node for how local synaptic changes are organized and constrained by global function in the brain.
2. A bridge between:

   * Q083 (neural coding and representations),
   * Q084 (memory storage and retention),
   * Q089 (predictive coding and inference),
   * Q087 (neurodegeneration and breakdown of plasticity).
3. A template for framing adaptation rules in AI systems:

   * learning rule design,
   * stability under continual learning,
   * analogies to alignment and oversight constraints in artificial agents.

In the Tension Universe view, Q085 is the place where local learning rules are explicitly tied to tension between:

* local synaptic dynamics,
* circuit stability,
* task performance,
* biophysical limits.

### References

1. Kandel ER, Schwartz JH, Jessell TM, Siegelbaum SA, Hudspeth AJ. Principles of Neural Science. 5th edition. McGraw Hill, 2013. Chapters on synaptic plasticity and learning.
2. Caporale N, Dan Y. Spike timing dependent plasticity: a Hebbian learning rule. Annual Review of Neuroscience. 2008;31:25 46.
3. Turrigiano GG, Nelson SB. Homeostatic plasticity in the developing nervous system. Nature Reviews Neuroscience. 2004;5(2):97 107.
4. Gerstner W, Kistler WM, Naud R, Paninski L. Neuronal Dynamics: From Single Neurons to Networks and Models of Cognition. Cambridge University Press, 2014. Chapters on synaptic plasticity and learning rules.

---

## 2. Position in the BlackHole graph

This block records how Q085 sits inside the BlackHole graph among Q001 to Q125. Each edge is listed with a one line reason pointing to a concrete component or tension pattern.

### 2.1 Upstream problems

These problems provide prerequisites or background frameworks that Q085 depends on at the effective layer.

* Q081 (BH_NEURO_CONSCIOUS_HARD_L3_081)
  Reason: Sets global constraints on what kinds of neural processes must ultimately support conscious experience, which plasticity rules need to respect at scale.

* Q083 (BH_NEURO_CODE_L3_083)
  Reason: Defines neural coding schemes that plasticity rules must read and transform when updating synaptic weights.

* Q084 (BH_NEURO_MEMORY_STORE_L3_084)
  Reason: Specifies memory storage and retention requirements that general plasticity rules must satisfy in order to avoid catastrophic forgetting or instability.

### 2.2 Downstream problems

These problems directly reuse components or depend on Q085 tension structure.

* Q087 (BH_NEURO_DEGEN_DISEASE_L3_087)
  Reason: Reuses SynapticStabilityIndex and PlasticityRuleSignature to model how plasticity failures lead to neurodegenerative changes.

* Q089 (BH_NEURO_PREDICTIVE_CODE_L3_089)
  Reason: Uses PlasticityRuleSignature and PlasticityWorldTemplate to define how predictive coding updates are implemented in synapses.

* Q090 (BH_NEURO_SOC_BRAIN_L3_090)
  Reason: Depends on general plasticity rules to explain how social cognition and higher order circuits adapt over development and experience.

### 2.3 Parallel problems

Parallel nodes share similar tension types but no direct component dependence.

* Q082 (BH_NEURO_BINDING_L3_082)
  Reason: Both study consistency_tension between local neural events and global coherent patterns. Q082 focuses on feature binding and Q085 focuses on weight changes.

* Q088 (BH_NEURO_DEV_PATTERN_L3_088)
  Reason: Both examine how local rules give rise to organized structure. Q088 focuses on developmental pattern formation and Q085 focuses on ongoing learning.

### 2.4 Cross domain edges

Cross domain edges connect Q085 to problems in other domains that can reuse its components.

* Q057 (BH_CS_RL_GENERALIZATION_L3_057)
  Reason: Uses PlasticityRuleSignature as a biological template for reinforcement learning update rules and their generalization limits.

* Q121 (BH_AI_ALIGNMENT_L3_121)
  Reason: Applies SynapticStabilityIndex like measures to constrain long term parameter updates in aligned AI systems.

* Q124 (BH_AI_OVERSIGHT_L3_124)
  Reason: Reuses PlasticityWorldTemplate as an experiment pattern for oversight of powerful adaptive AI that continuously updates internal parameters.

---

## 3. Tension Universe encoding (effective layer)

All content in this block is at the effective layer. We only describe:

* state spaces,
* effective fields and observables,
* invariants and tension quantities,
* singular sets and domain restrictions.

We do not describe any hidden generative rules or any mapping from raw biological data to internal TU fields.

### 3.1 State space

We posit a state space:

```txt
M
```

interpreted as the plasticity world state space for Q085.

* Each state `m` in `M` represents a plasticity world snapshot at the scale of:

  * a local population or microcircuit,
  * over a finite observation window.

For each state `m` we assume the existence of:

1. A description of synaptic weight changes over that window for a selected set of synapses.
2. A summary of pre and post neuronal activity patterns and relevant modulatory signals in that window.
3. A coarse description of circuit level function during and shortly after that window, for example whether firing statistics and basic behavioral outputs remain within acceptable ranges.

We do not specify how biological recordings, simulations, or models are encoded into `m`. We only require that for each experimental or model context of interest there exist states in `M` that encode the required summaries in a well defined way that respects the encoding constraints described below.

### 3.2 Hybrid field implementation

Because the metadata semantics are hybrid, we conceptually split each `m` into two parts.

1. A continuous part that includes:

   * synaptic weights and their changes,
   * average firing rates over time bins,
   * real valued modulatory levels,
   * aggregated measures of stability and task performance.

2. A discrete part that includes:

   * individual spike event times,
   * discrete trial events,
   * categorical labels for context or task conditions.

The effective observables below are defined as functions of these continuous and discrete parts. We do not expose any rule for constructing those parts from raw data. The coupling is assumed to proceed through simple interfaces such as counting spikes in time windows, averaging rate like quantities, and aggregating over finite sets of synapses or neurons.

### 3.3 Effective observables and fields

We introduce the following effective observables on `M`. All are real valued, bounded, and defined on a regular subset described below.

1. Plasticity rule signature

```txt
RuleSignature(m; region) in R^k_sig
```

* Input: a state `m` and a labeled region or cell population.
* Output: a low dimensional vector that summarizes which plasticity rule template best describes synaptic changes in that region during the observation window.
* Examples of template features:

  * sensitivity to pre versus post firing rates,
  * dependence on precise spike timing,
  * presence of neuromodulator gating,
  * strength of homeostatic components.
* We assume a finite library of templates and a fixed mapping from observed changes to this signature.

2. Synaptic stability index

```txt
StabilityIndex(m; circuit) in [0, 1]
```

* Input: a state `m` and a labeled circuit or network.
* Output: a scalar index where:

  * values near 1 indicate high stability under continued application of observed plasticity rules,
  * values near 0 indicate that continued application leads to runaway excitation, quiescence, or loss of function over relevant timescales.
* Defined through a standardized stability test applied to the encoded circuit summaries.

3. Task generalization score

```txt
GeneralizationScore(m; task_family) in [0, 1]
```

* Input: a state `m` and a family of related tasks or inputs.
* Output: a scalar describing how well the observed plasticity rules support learning across that task family without major retuning.

4. Biophysical feasibility index

```txt
BioFeasibility(m; region) in [0, 1]
```

* Input: a state `m` and a region or preparation.
* Output: a scalar describing how compatible the implied synaptic changes are with known biophysical constraints such as:

  * resource limits,
  * receptor trafficking rates,
  * structural remodeling bounds.
* Values near 1 indicate good compatibility. Values near 0 indicate strong tension with known limits.

### 3.4 Tension quantities

We define three nonnegative tension quantities on the regular domain.

1. Local global consistency tension

```txt
DeltaS_local_global(m) >= 0
```

* Measures mismatch between:

  * the local RuleSignature across synapses in the circuit,
  * and the global StabilityIndex.
* Constructed so that:

  * small values occur when a simple local rule template coexists with high circuit stability,
  * large values occur when local rules imply instability or require finely tuned global corrections.

2. Generalization tension

```txt
DeltaS_generalization(m) >= 0
```

* Measures the tension between:

  * the simplicity of the effective rule templates encoded in RuleSignature,
  * and the GeneralizationScore across the task family.
* Small values indicate that simple rules generalize well.
* Large values indicate that either rules are complex and overfitted, or simple rules perform poorly.

3. Biophysical constraint tension

```txt
DeltaS_biophysical(m) >= 0
```

* Measures mismatch between:

  * implied synaptic changes per unit time,
  * and BioFeasibility indices.
* Small values indicate that rules operate comfortably within known constraints.
* Large values indicate that rules would require sustained changes incompatible with known biology.

### 3.5 Singular set and domain restrictions

Some encodings or contexts can lead to ill defined or unbounded observables. We therefore define the singular set:

```txt
S_sing = { m in M :
           at least one of
           RuleSignature, StabilityIndex,
           GeneralizationScore, BioFeasibility,
           DeltaS_local_global, DeltaS_generalization,
           DeltaS_biophysical
           is undefined or not finite }
```

and the regular domain:

```txt
M_reg = M \ S_sing
```

All tension analysis for Q085 is restricted to `M_reg`. If an experimental or model state maps into `S_sing`, this is treated as out of domain for this encoding and not as evidence about whether general plasticity rules exist.

---

## 4. Tension principle for this problem

This block states how Q085 is represented as a tension problem in TU, purely at the effective layer.

### 4.1 Core plasticity tension functional

We define a combined plasticity tension functional:

```txt
Tension_plasticity(m) =
    w_local_global * DeltaS_local_global(m)
  + w_generalization * DeltaS_generalization(m)
  + w_bio * DeltaS_biophysical(m)
```

with the following constraints.

* `w_local_global`, `w_generalization`, and `w_bio` are nonnegative real numbers.
* They satisfy `w_local_global + w_generalization + w_bio = 1`.
* Each weight lies in a fixed bounded interval, for example:

```txt
w_local_global in [0.2, 0.6]
w_generalization in [0.2, 0.6]
w_bio in [0.2, 0.6]
```

* The triple `(w_local_global, w_generalization, w_bio)` is fixed in advance as part of the encoding and does not depend on the particular state `m` or on the experimental data used later.

The numerical ranges and tolerance bands for this tension functional are chosen in a pre registered analysis plan consistent with the TU Tension Scale Charter. For any admissible choice within that plan, the functional is required to satisfy:

* `Tension_plasticity(m) >= 0` for all `m` in `M_reg`.
* `Tension_plasticity(m)` is small when all three component tensions are small.
* `Tension_plasticity(m)` becomes large if any component remains large despite reasonable adjustments of rule parameters inside the fixed template library described below.

### 4.2 Admissible rule template library and encoding class

To avoid trivial tuning, we fix in advance a finite library:

```txt
L = { L_1, L_2, ..., L_K }
```

of plasticity rule templates, where:

* Each `L_k` specifies a simple parametric form for how synaptic weights change as a function of local pre, post, and modulatory variables.
* The number `K` and the functional forms of `L_k` are chosen once and then held fixed for all experiments and model analyses that use this encoding of Q085.
* Rule parameters inside each `L_k` may vary within bounded ranges to capture known biological diversity. These ranges are specified in advance and are not expanded ad hoc to fit individual datasets.

RuleSignature is defined so that each state `m` is effectively associated with one template or a small mixture of templates from `L`, together with parameter ranges. The tension quantities in Section 3.4 and the combined tension functional in Section 4.1 are computed relative to this fixed template library and fixed weight ranges.

The choices listed below are all treated as part of a pre registered analysis plan.

* The definition of the state space `M` and its regular subset `M_reg`.
* The observables and tension quantities in Section 3.
* The finite template library `L` and its parameter bounds.
* The admissible ranges of `w_local_global`, `w_generalization`, and `w_bio`.
* Thresholds and bands derived from `epsilon_plasticity` and `delta_plasticity` in Sections 4.3 and 4.4, chosen according to the TU Tension Scale Charter.

Together these elements define an admissible encoding class for Q085, which we denote by:

```txt
E_plasticity
```

Any concrete instantiation that claims to implement the Q085 TU encoding at the effective layer must specify its state summaries, template choices, and tension thresholds in a way that belongs to `E_plasticity`. Changing `L` beyond the fixed library, or changing weight ranges or thresholds outside the pre registered plan, counts as switching to a different encoding rather than as a new data point for the same encoding.

### 4.3 Q085 as a low tension principle

At the effective layer, Q085 is encoded as the following low tension possibility.

> There exists a nontrivial region of `M_reg` representing real biological circuits and tasks, in which the combined tension functional `Tension_plasticity(m)` remains within a low band when evaluated with respect to the fixed template library `L`, the fixed weight ranges, and the encoding class `E_plasticity`.

More concretely, there should exist states `m_bio` in `M_reg` representing real circuits such that:

```txt
Tension_plasticity(m_bio) <= epsilon_plasticity
```

for a small threshold `epsilon_plasticity`. The value of `epsilon_plasticity` and the associated low tension band are selected according to the TU Tension Scale Charter and recorded in a pre registered plan before data analysis.

This low tension should remain attainable across:

* multiple brain regions and species,
* multiple task families,
* multiple experimental preparations,

without changing the finite library `L` and without moving outside the admissible ranges for the weights and thresholds in `E_plasticity`.

The statement above is an effective layer claim about the existence of low tension regions in state space. It is not a claim that we have already demonstrated such regions for real biological circuits. Whether real circuits behave like this is an empirical question.

### 4.4 Failure as persistent high plasticity tension

The opposite possibility is that, even after reasonable optimization of parameters within the fixed library `L` and within the admissible weight ranges, we find that:

```txt
Tension_plasticity(m_bio) >= delta_plasticity
```

for all states `m_bio` representing real circuits in the sense of this encoding, where `delta_plasticity` is a strictly positive lower bound.

The value of `delta_plasticity` is chosen in advance, within a bounded range specified by the TU Tension Scale Charter and the pre registered plan. It is not set after inspection of the data.

If such a positive lower bound persists and cannot be brought below the low tension band by refining data summaries or by tuning parameters inside `L`, while still respecting `E_plasticity`, then this specific TU encoding of general rules of synaptic plasticity would be falsified at the effective layer.

This would not prove that no general rules exist in reality. It would indicate that this particular template library, weight specification, and tension decomposition, as captured in `E_plasticity`, cannot capture those rules if they exist.

---

## 5. Counterfactual tension worlds

We now describe two counterfactual worlds at the effective layer.

* World T: general plasticity rules exist and are well captured by a small template family inside `L`.
* World F: plasticity is fundamentally fragmented and resists such compression.

Both are described by patterns of observables and tensions, not by any deep generative mechanism.

### 5.1 World T: rule like plasticity world

In World T:

1. Template compression

   * A small subset of templates in `L` explains most observed RuleSignature patterns across many circuits and species.
   * Diversity exists but is structured around these main template families and remains inside the admissible encoding class `E_plasticity`.

2. Local global alignment

   * For typical states `m_T` representing healthy circuits, `DeltaS_local_global(m_T)` is small.
   * Local synaptic updates implied by RuleSignature are consistent with high StabilityIndex values.

3. Task generalization

   * For a wide range of task families, `GeneralizationScore(m_T; task_family)` is high while RuleSignature remains within the fixed template family.
   * `DeltaS_generalization(m_T)` stays low for many tasks without large changes in templates.

4. Biophysical compatibility

   * BioFeasibility remains high for plasticity regimes that support learning, and `DeltaS_biophysical(m_T)` stays low over long timescales.

5. Overall tension

   * There exist states `m_T` with `Tension_plasticity(m_T)` in a narrow low tension band across many contexts, relative to the band defined by `epsilon_plasticity` and the Tension Scale Charter.

### 5.2 World F: idiosyncratic plasticity world

In World F:

1. Template fragmentation

   * RuleSignature patterns vary so widely that no small subset of templates in the fixed library `L` can capture them without large residuals.
   * Attempts to compress plasticity into a compact rule family inside `E_plasticity` lead to high mismatch.

2. Local global mismatch

   * For typical states `m_F`, local RuleSignature patterns imply instability unless strong, ad hoc global corrections are deployed.
   * `DeltaS_local_global(m_F)` remains large for many realistic activity regimes.

3. Poor generalization

   * High GeneralizationScore can only be achieved with sharply different templates or parameter settings for each task, leading to high `DeltaS_generalization(m_F)` when using a shared rule family.

4. Biophysical stress

   * Many plausible rule configurations that yield learning would require sustained synaptic changes that are incompatible with known biophysical limits, leading to high `DeltaS_biophysical(m_F)`.

5. Overall tension

   * For all reasonable states `m_F` and parameter choices inside the fixed library and weight ranges of `E_plasticity`, `Tension_plasticity(m_F)` stays above a significant lower bound comparable to `delta_plasticity`, indicating persistent high tension.

### 5.3 Interpretive note

These worlds do not claim that we can fully simulate all biological detail. They only assert that if real circuits behave as in World T or World F, then, under the encoding class `E_plasticity`:

* World T maps into a region of `M_reg` where low tension states exist and are common.
* World F maps into `M_reg` where high tension states are unavoidable, given the fixed template library, weight ranges, and thresholds.

---

## 6. Falsifiability and discriminating experiments

This block specifies experiments and protocols that can:

* test the coherence of the Q085 encoding,
* discriminate between rule like and idiosyncratic plasticity patterns at the effective layer,
* falsify specific choices of template library and weights inside `E_plasticity`.

They do not prove or disprove the existence of ultimate biological laws. They only accept or reject this particular effective layer encoding.

Throughout this section, all choices of template library, weight ranges, tension bands, and decision criteria are assumed to be specified in a pre registered analysis plan that is consistent with:

* the TU Effective Layer Charter,
* the TU Encoding and Fairness Charter,
* the TU Tension Scale Charter.

### Experiment 1: Cross region template compression

*Goal*
Test whether a fixed finite library of plasticity templates can account for observed synaptic changes across many brain regions with low local global tension when evaluated inside `E_plasticity`.

*Setup*

* Data

  * Collect published or newly acquired plasticity measurements from multiple brain areas, species, and preparations.
  * Each dataset should include pre and post activity measures, neuromodulatory context, and observed synaptic changes.
* Fixed encoding choices

  * Choose the finite template library `L`, the admissible parameter ranges, the admissible ranges of `w_local_global`, `w_generalization`, `w_bio`, and the low and high tension bands guided by `epsilon_plasticity` and `delta_plasticity` before analyzing the datasets.
  * Define RuleSignature, StabilityIndex, and `DeltaS_local_global` according to this encoding, without dataset specific modifications.

*Protocol*

1. For each dataset and region, construct a state `m_data` in `M_reg` that summarizes:

   * RuleSignature based on fitting one or more templates in `L`,
   * StabilityIndex based on network level analyses or models guided by the data.
2. Compute `DeltaS_local_global(m_data)` for each state.
3. Aggregate results across regions and species into a distribution of local global tension values.
4. Optionally stratify by region type, cell class, or developmental stage.

*Metrics*

* Distribution of `DeltaS_local_global(m_data)` across all states.
* Fraction of states with `DeltaS_local_global(m_data)` and `Tension_plasticity(m_data)` below the low tension band derived from `epsilon_plasticity`.
* Variation of these quantities across regions and species.

*Falsification conditions*

* If, for the fixed `L`, weight ranges, and tension bands defined in `E_plasticity`, a large majority of states show `DeltaS_local_global(m_data)` or `Tension_plasticity(m_data)` beyond a pre specified tolerance, and this cannot be reduced by parameter tuning within each template, then this encoding of general rules is rejected at the effective layer.
* If local global tension behaves erratically between very similar regions or species without a clear structural reason, the definitions of RuleSignature and StabilityIndex are considered misaligned with the TU Encoding and Fairness Charter and must be revised or discarded. Such a revision would count as moving to a different encoding, not as a success or failure of the original `E_plasticity`.

*Semantics implementation note*
All variables are treated as hybrid signals. Discrete spike events and trial markers are aggregated into continuous rate like and summary statistics, which then feed into the state space `M` and the observables defined in Section 3, in line with the hybrid semantics declared in the header disclaimer.

*Boundary note*
Falsifying this TU encoding at the effective layer does not solve the canonical problem. The experiment can reject the specific combination of `L`, weight ranges, and observables contained in `E_plasticity`, but it does not establish that nature lacks general synaptic rules.

---

### Experiment 2: Stability under ongoing learning in model circuits

*Goal*
Evaluate whether synaptic plasticity templates from the fixed library `L` can support stable ongoing learning in realistic model circuits without producing high tension or collapse when scored by `Tension_plasticity`.

*Setup*

* Construct or select several model circuits, for example:

  * recurrent networks with biologically plausible connectivity and activity regimes,
  * parameter ranges for synaptic weights and firing thresholds that fall inside realistic bounds.
* For each circuit:

  * Implement one or more templates from `L` as the synaptic update rule.
  * Define a family of tasks or input statistics for the circuit to learn.

All template choices, parameter ranges, tension bands, and stopping criteria are fixed before experiments, consistent with `E_plasticity` and the TU charters.

*Protocol*

1. For each circuit and template choice, run the model under ongoing learning for a long sequence of epochs with realistic activity statistics.
2. At regular checkpoints, construct states `m_model` encoding:

   * RuleSignature (from the instantiated template and parameters),
   * StabilityIndex (based on activity boundedness and functional performance),
   * GeneralizationScore (on held out tasks),
   * BioFeasibility (based on constraints such as average weight magnitude and update rates).
3. Compute `DeltaS_local_global(m_model)`, `DeltaS_generalization(m_model)`, and `DeltaS_biophysical(m_model)` at each checkpoint.
4. Track `Tension_plasticity(m_model)` over learning time.

*Metrics*

* Time series of `Tension_plasticity(m_model)` for each circuit template pair.
* Proportion of learning runs that remain in the low tension band derived from `epsilon_plasticity` throughout training.
* Failure modes, including:

  * runaway activity or quiescence,
  * catastrophic forgetting,
  * violations of biophysical constraints inferred from BioFeasibility.

*Falsification conditions*

* If for most circuits and tasks, all templates in `L` lead to runs where `Tension_plasticity(m_model)` frequently or persistently exceeds the upper band associated with `delta_plasticity`, then the encoding is considered inconsistent with stable ongoing learning at the effective layer.
* If small variations in template parameters inside their admissible ranges cause extreme swings in tension or stability with no clear structural reason, the encoding is treated as poorly conditioned under the TU Encoding and Fairness Charter and should be revised. Such a revision again counts as changing the encoding, not as a success of the original one.

*Semantics implementation note*
Model circuits are simulated with discrete time steps and spikes, but observables and tension quantities are computed from continuous approximations such as average firing rates and weight statistics, consistent with the hybrid field interpretation in Section 3.2.

*Boundary note*
Falsifying this encoding does not establish a final answer to whether general biological rules exist. It only shows that the particular package of state summaries, template library, and tension scales in `E_plasticity` is not adequate.

---

## 7. AI and WFGY engineering spec

This block describes how Q085 can be used as an engineering module for AI systems inside the WFGY framework, at the effective layer.

### 7.1 Training signals

We define several training or regularization signals inspired by the observables of Q085.

1. `signal_plasticity_stability`

   * Definition: a penalty proportional to an AI analogue of `DeltaS_local_global`, computed from the relation between internal weight update proposals and a stability measure for the system after applying them.
   * Purpose: discourage update rules that preserve task performance only by relying on fragile or unstable dynamics.

2. `signal_rule_sharing_across_tasks`

   * Definition: a measure of how similar the effective update rules are across related tasks, adjusted by a performance term.
   * Purpose: encourage reuse of a small family of update templates when generalization remains good, analogous to low `DeltaS_generalization`.

3. `signal_update_bio_analogue`

   * Definition: a soft constraint that penalizes sustained very large or very frequent internal parameter changes, in analogy to `DeltaS_biophysical`.
   * Purpose: encourage learning rules that achieve good performance without extreme per step changes.

4. `signal_plasticity_world_consistency`

   * Definition: a measure of how consistent the model own explanations of its update behavior are with a fixed template family when probed as a plasticity world.
   * Purpose: provide a self consistency check on adaptive behavior, analogous to monitoring whether an AI system remains inside a low tension region of `E_plasticity`.

### 7.2 Architectural patterns

We outline module patterns that can reuse Q085 components without exposing any deep TU generative rules.

1. `TU_SynapticUpdateHead`

   * Role: maps internal representations and gradient like signals into:

     * update directions for parameters,
     * an estimated internal RuleSignature,
     * a stability proxy that approximates StabilityIndex.
   * Interface:

     * Inputs: latent state, task context, candidate gradients.
     * Outputs: proposed parameter update, rule signature vector, stability score.

2. `TU_HomeostaticController`

   * Role: maintains long term bounds on effective weights or activations based on analogues of BioFeasibility.
   * Interface:

     * Inputs: moving averages of parameter norms and activations.
     * Outputs: small corrective factors that nudge the system back into a safe regime.

3. `TU_PlasticityProbe`

   * Role: diagnostic module that constructs approximate RuleSignature, GeneralizationScore, and tension quantities given logs of updates and performance.
   * Interface:

     * Inputs: history of updates, tasks, and performance metrics.
     * Outputs: proxy values for Q085 observables and a scalar AI tension estimate.

### 7.3 Evaluation harness

We suggest an evaluation harness for AI models augmented with Q085 inspired modules.

1. Task selection

   * A suite of continual learning and multi task benchmarks where the model must adapt over time and where catastrophic forgetting and instability are common risks.

2. Conditions

   * Baseline condition

     * Conventional optimization and learning without explicit Q085 constraints.
   * TU augmented condition

     * The same base model, but with TU_SynapticUpdateHead and TU_HomeostaticController, plus Q085 derived signals included in the objective.

3. Metrics

   * Stability

     * Fraction of training runs that remain stable, which means no divergence and no collapse of performance.
   * Generalization

     * Performance on held out tasks or distribution shifts after long adaptation.
   * Plasticity tension

     * A tracked analogue of `Tension_plasticity` computed from logs via TU_PlasticityProbe.

4. Outcome

   * The goal is not to mimic biology exactly. The goal is to test whether viewing updates through the Q085 lens gives more stable and interpretable adaptive behavior, and whether low tension regimes in the AI analogue of `E_plasticity` correlate with desirable engineering properties.

### 7.4 60 second reproduction protocol

A minimal protocol to let external users experience the effect of Q085 style constraints in an AI system.

* Baseline setup

  * Prompt an AI system to design an update rule for continual learning across several tasks without any reference to biological plasticity or tension.
  * Ask it to comment qualitatively on expected stability and generalization.

* TU encoded setup

  * Prompt the same system, but now request:

    * an update rule described in terms of local versus global information,
    * explicit discussion of stability, generalization, and biophysical analogue constraints,
    * a simple scalar plasticity tension estimate for the proposed rule, analogous to `Tension_plasticity`.

* Comparison metric

  * Human evaluators rate:

    * clarity of assumptions,
    * explicitness about stability and constraints,
    * degree to which the rule could be monitored over time.

* What to log

  * Both sets of prompts and responses,
  * any internal tension estimates,
  * post hoc success or failure of the proposed rules in toy implementations.

These logs can later be analyzed as AI plasticity worlds and scored using Q085 like observables, without exposing any deep TU generative structure.

---

## 8. Cross problem transfer template

This block describes the main reusable components produced by Q085 and how they transfer to other problems.

### 8.1 Reusable components produced by this problem

1. ComponentName: `PlasticityRuleSignature`

   * Type: field.
   * Minimal interface:

     * Inputs: summaries of synaptic changes, local activity statistics, and modulatory context.
     * Output: a finite dimensional vector indicating which plasticity template from a fixed library best describes the data.
   * Preconditions:

     * Inputs must be drawn from a context where synaptic changes and activity can be reliably summarized.

2. ComponentName: `SynapticStabilityIndex`

   * Type: functional.
   * Minimal interface:

     * Inputs: summaries of network activity and connectivity over a learning period.
     * Output: a scalar in the interval from 0 to 1 indicating the degree of stability under continued learning.
   * Preconditions:

     * The network must be sufficiently well characterized to estimate the impact of continued updates.

3. ComponentName: `PlasticityWorldTemplate`

   * Type: experiment_pattern.
   * Minimal interface:

     * Inputs: a class of circuits or models and a family of candidate plasticity rules.
     * Output: a standardized experiment design for assessing tension quantities, including local global, generalization, and biophysical tensions over time.
   * Preconditions:

     * The circuits or models must expose enough observables to construct the Q085 observables at the effective layer.

### 8.2 Direct reuse targets

1. Q084 (Long term memory storage and retention)

   * Reuses: `PlasticityRuleSignature`, `SynapticStabilityIndex`.
   * Why it transfers: long term memory requires that plasticity both store information and preserve stability over long timescales, which these components help quantify.
   * What changes: observables are computed over longer time windows and with memory specific performance criteria.

2. Q087 (Neurodegenerative disease mechanisms)

   * Reuses: `SynapticStabilityIndex`, `PlasticityWorldTemplate`.
   * Why it transfers: many disease hypotheses involve maladaptive plasticity and breakdown of stability. These components quantify how far circuits move into high tension regimes.
   * What changes: additional observables for degeneration markers and structural loss are added.

3. Q089 (Predictive coding in the brain)

   * Reuses: `PlasticityRuleSignature`.
   * Why it transfers: predictive coding schemes require a match between error signals and synaptic updates. The signature field captures which rule templates are compatible with such schemes.
   * What changes: task families focus on prediction error reduction and inference quality.

4. Q121 (AI alignment under continual adaptation)

   * Reuses: `SynapticStabilityIndex`, `PlasticityWorldTemplate`.
   * Why it transfers: alignment can be seen as a constraint on how update rules move internal states. These components are used as analogues for safe adaptation.
   * What changes: observables operate on AI parameter updates and alignment metrics instead of biological synapses.

---

## 9. TU roadmap and verification levels

This block places Q085 along the TU verification ladder and outlines next steps.

### 9.1 Current levels

* E_level: E1

  * A coherent effective encoding of general rules of synaptic plasticity has been specified.
  * State space, observables, tension quantities, and a combined tension functional are defined on a regular domain `M_reg` with an explicit singular set.
  * An admissible encoding class `E_plasticity` has been defined, including a finite template library and constrained weight ranges.
  * At least one discriminating experiment with falsification conditions is provided.

* N_level: N1

  * The narrative clearly separates:

    * local synaptic dynamics,
    * global stability and performance,
    * biophysical constraints.
  * Rule like and idiosyncratic worlds are distinguished in terms of observable tension patterns.

### 9.2 Next measurable step toward E2

To reach E2, at least one of the following should be implemented, while remaining strictly at the effective layer.

1. An instantiated template library `L` with:

   * explicit functional forms for a small number of plasticity rules,
   * parameter ranges informed by empirical data,
   * open source code for mapping data summaries into RuleSignature and tension quantities.
2. A pilot study applying Experiment 1 to:

   * a curated meta dataset of plasticity experiments,
   * with published distributions of `DeltaS_local_global` and associated conclusions about compression into a small number of templates.
3. A set of model circuit experiments based on Experiment 2, demonstrating:

   * how different template choices affect stability and generalization,
   * how `Tension_plasticity(m_model)` behaves over long adaptation.

None of these steps require specifying TU axioms or deep generative mechanisms. They only refine the effective layer encoding.

### 9.3 Long term role in the TU program

In the long term, Q085 is expected to serve as:

* The reference node for all problems in the cluster where local learning rules, global behavior, and long term safety must be jointly considered.
* A bridge between biological and artificial learning rule design, providing:

  * a language for discussing update rules as tension balancing mechanisms,
  * a set of reusable metrics for stability and generalization.
* A template for other domains in which local update rules under global constraints are central, such as:

  * social learning systems,
  * institutional adaptation,
  * large scale AI training regimes.

---

## 10. Elementary but precise explanation

Synaptic plasticity is the process by which connections between neurons get stronger or weaker when they are used. Without it, brains could not learn or adapt.

Over many years, scientists have found many different kinds of plasticity.

* Some depend on how often neurons fire.
* Some depend on the exact timing of spikes.
* Some depend on chemicals that signal reward or attention.
* Some act slowly to keep overall activity in a safe range.

The big question in Q085 is:

> Are there a few general rules that really describe how all these changes work, or is every synapse doing something different?

In the Tension Universe view, we do not try to guess the hidden mechanisms in full detail. Instead, we ask four simple questions.

* For a given circuit, can we describe its plasticity by a simple rule template.
* Does that rule keep the circuit stable when learning continues for a long time.
* Does it let the circuit handle many tasks without needing a new rule for each one.
* Does it stay within what biology can realistically support.

We turn these questions into numbers.

* A signature that says which rule template is being used.
* A stability score between 0 and 1.
* A generalization score between 0 and 1.
* A feasibility score between 0 and 1.
* A combined tension value that is small when everything fits nicely and large when something is off.

Then we consider two kinds of worlds.

* In a rule like world, a small set of rule templates works well across many circuits and tasks. Tension stays low, using the scale defined in the TU Tension Scale Charter.
* In an idiosyncratic world, any small set of templates fails, and tension stays high no matter how you tune within the allowed limits.

This way of looking at synaptic plasticity does not prove what the true rules are. It gives:

* a clear way to say what we mean by general rules at the effective layer,
* a way to test whether a proposed family of rules is good enough inside a fixed encoding class,
* and a set of tools that can also be used to design and monitor learning rules in AI systems.

Q085 is therefore the place where the intuition about how connections change is turned into a structured tension problem that links neuroscience and AI, while staying inside the effective layer and without exposing any deep TU generative machinery. It is a working scientific tool, not a proof of any final biological law.

---

## Tension Universe effective-layer footer

This page is part of the WFGY / Tension Universe S problem collection.

### Scope of claims

* The goal of this document is to specify an effective layer encoding of the problem Q085, which concerns general rules of synaptic plasticity.
* It does not claim to prove or disprove the canonical statement in Section 1.
* It does not introduce any new theorem beyond what is already established in the cited literature.
* It should not be cited as evidence that the corresponding open problem has been solved.

### Effective-layer boundary

* All objects used here, including state spaces `M`, observables, invariants, tension scores, and counterfactual worlds, live strictly at the effective layer of the Tension Universe framework.
* No TU axiom system, field equation, or generative rule is specified or assumed beyond what is needed to define the effective objects in Sections 3 and 4.
* Any mapping from raw biological or simulation data into the state space and observables is treated as a black box that must respect the constraints of the encoding class `E_plasticity`.
* The counterfactual worlds described in Section 5 are interpretive tools for organizing observable patterns. They do not assert that nature actually realizes those worlds.

### Encoding, fairness, and tension scale

* The admissible encoding class `E_plasticity` is defined by the combination of:

  * the regular state space `M_reg`,
  * the observables and tension quantities listed in Section 3,
  * the finite template library `L` and its parameter bounds,
  * the admissible weight ranges and tension thresholds associated with `Tension_plasticity`.
* Choices of template library, parameter bounds, weights, and thresholds are to be specified in pre registered analysis plans that follow the TU Encoding and Fairness Charter.
* Low and high tension bands, including thresholds such as `epsilon_plasticity` and `delta_plasticity`, are chosen and interpreted according to the TU Tension Scale Charter.
* Any substantial change to `L`, to the observables, or to the admissible ranges of weights and thresholds constitutes a change of encoding and must be documented as such rather than treated as a new data point for the same encoding.

This page should be read together with the following charters:

* [TU Effective Layer Charter](../Charters/TU_EFFECTIVE_LAYER_CHARTER.md)
* [TU Encoding and Fairness Charter](../Charters/TU_ENCODING_AND_FAIRNESS_CHARTER.md)
* [TU Tension Scale Charter](../Charters/TU_TENSION_SCALE_CHARTER.md)
* [TU Global Guardrails](../Charters/TU_GLOBAL_GUARDRAILS.md)
