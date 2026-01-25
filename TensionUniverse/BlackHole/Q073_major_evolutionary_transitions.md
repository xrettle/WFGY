# Q073 · Mechanisms of major evolutionary transitions

## 0. Header metadata

```txt
ID: Q073
Code: BH_BIO_EVO_L3_073
Domain: Biology
Family: Evolutionary biology (major transitions)
Rank: S
Projection_dominance: I
Field_type: dynamical_field
Tension_type: incentive_tension
Status: Open
Semantics: hybrid
E_level: E1
N_level: N1
Last_updated: 2026-01-25
```

---

## 1. Canonical problem and status

### 1.1 Canonical statement

The canonical question behind Q073 can be stated as follows:

How can the major evolutionary transitions in the history of life be described and partially explained by general mechanisms that reorganize units of selection, information channels, and cooperation, such that new higher-level individuals or organizations emerge and remain stable over evolutionary timescales?

Classical examples of major transitions include:

* independent replicators to genetic systems with chromosomes,
* prokaryotic cells to eukaryotic cells,
* unicellular organisms to multicellular organisms,
* solitary individuals to eusocial colonies,
* non-symbolic communication to language-using societies.

Across these cases, three structural changes recur:

1. Units that were capable of independent replication become parts of a larger unit.
2. There is a reorganization of information storage, transmission, and control.
3. Conflicts between lower-level and higher-level units are managed or suppressed, at least within certain conditions.

The canonical problem is to identify and characterize the mechanisms that:

* reduce conflicts and align incentives across levels,
* enable robust information integration and division of labor,
* make higher-level individuals or organizations evolutionarily stable and evolvable.

### 1.2 Status and difficulty

The idea of major transitions is well established, and there is a substantial body of work describing:

* which transitions have occurred in the history of life,
* qualitative similarities among them,
* models for particular cases (for example evolution of multicellularity, eusociality).

However, there is no single widely accepted, quantitative theory that:

* unifies all major transitions under a small set of general mechanisms,
* provides clear, comparable metrics for multi-level alignment and information integration,
* predicts when major transitions are possible, likely, or blocked in a given evolutionary landscape.

Open difficulties include:

* describing transitions in terms that apply across very different substrates (biochemical, ecological, cultural),
* defining precise notions of individuality and fitness at multiple levels,
* understanding how transitions interact with constraints such as mutation rates, population structures, and ecological feedbacks.

Q073 focuses on mechanisms that can be described at an effective layer, with emphasis on multi-level incentive structures, information integration, and dynamical stability, without committing to a single substrate-specific micro-model.

### 1.3 Role in the BlackHole project

Within the BlackHole S-problem collection, Q073 serves as:

1. A reference node for **incentive_tension** problems in biology, where selection pressures at different levels must be reconciled.
2. A bridge from prebiotic and molecular questions (Q071, Q072, Q078) to large-scale biosphere and social dynamics (Q080, Q098, Q107).
3. A source of reusable concepts and components for:

   * multi-level selection,
   * cooperation and conflict management,
   * emergence and stabilization of new levels of individuality.

These concepts are intended to transfer to non-biological domains, including complex social systems and multi-agent AI.

### References

1. J. Maynard Smith, E. Szathmary, “The Major Transitions in Evolution”, Oxford University Press, 1995.
2. E. Szathmary, “The origin of replicators and reproducers”, Philosophical Transactions of the Royal Society B, 2006.
3. R. E. Michod, “Darwinian Dynamics: Evolutionary Transitions in Fitness and Individuality”, Princeton University Press, 1999.
4. S. Okasha, “Evolution and the Levels of Selection”, Oxford University Press, 2006.

---

## 2. Position in the BlackHole graph

This block records how Q073 is positioned in the BlackHole graph. All edges reference concrete components or tension patterns defined at the effective layer.

### 2.1 Upstream problems

These nodes provide prerequisites and reusable frameworks.

* Q071 (Origin of life)
  Reason: Supplies the baseline replicator and minimal reproducer models that Q073 extends into multi-level organizational transitions using MultiLevelSelection_TensionFunctional.

* Q072 (Origin of the genetic code)
  Reason: Provides information-channel and encoding concepts that feed into info_integration_L for higher-level organizing units.

* Q078 (From genotype to phenotype)
  Reason: Defines mapping structures from genotype to phenotype that become more layered and hierarchical in MultiLevelSelection_TensionFunctional.

### 2.2 Downstream problems

These nodes reuse Q073 components directly.

* Q080 (Limits of biosphere adaptability)
  Reason: Reuses OrganizationalLevel_Descriptor to evaluate how the number and diversity of organizational levels affects long-term adaptability.

* Q098 (Anthropocene system dynamics)
  Reason: Uses TransitionScenario_Template to model human-driven transitions in planetary-scale socio-ecological systems.

* Q107 (Mechanisms of large scale collective action)
  Reason: Reuses MultiLevelSelection_TensionFunctional to describe incentive alignment between individuals, organizations, and institutions.

* Q125 (Multi agent AI dynamics)
  Reason: Reuses TransitionScenario_Template to construct world T and world F scenarios for emergent higher-level AI organizations.

### 2.3 Parallel problems

Parallel problems share similar tension types but do not depend directly on Q073 components.

* Q075 (Fundamental mechanisms of aging)
  Reason: Both Q075 and Q073 involve long-term trade-offs between individual-level fitness and system-level maintenance under incentive_tension.

* Q104 (Dynamics of wealth and income inequality)
  Reason: Both study misalignment and partial alignment of incentives across nested levels (individuals, groups, institutions) in complex systems.

### 2.4 Cross-domain edges

These edges show transfer of Q073 concepts beyond biology.

* Q105 (Prediction of systemic crashes)
  Reason: Uses TransitionScenario_Template to model breakdowns and reconfigurations of cooperative structures in complex systems.

* Q121 (AI alignment problem)
  Reason: Adapts MultiLevelSelection_TensionFunctional to alignment between agents, overseers, and institutions in artificial systems.

---

## 3. Tension Universe encoding (effective layer)

All content in this block is confined to the effective layer. It defines state spaces, observables, invariants, and singular sets for Q073, without specifying any deep TU generative rules or mappings from raw data to internal fields.

### 3.1 State space

Let

```txt
M
```

be the semantic state space for Q073. Each state `m` in `M` represents a coarse-grained evolutionary configuration over a finite time window, including:

* a finite list of organizational levels, such as:

  * level 1: genetic elements,
  * level 2: cells,
  * level 3: organisms,
  * level 4: groups or colonies,
  * level 5: societies.

* a finite set of functional roles at each level (for example metabolic roles, reproductive roles, defense roles),

* continuous summaries of population densities, resource distributions, and interaction rates for each level and role.

Minimal assumptions:

* For any finite choice of levels, roles, and time window, there exist states `m` in `M` that encode the relevant configuration.
* Internal details of how these encodings are constructed from empirical data or simulations are not described here.

### 3.2 Effective fields and observables

At the effective layer, we introduce the following observables and fields on `M`.

1. Cross-level fitness contributions

```txt
fitness_i(m) in R
```

* For each level index `i`, `fitness_i(m)` summarizes how selection acts on units at level `i` within the configuration `m`.
* It may include combined effects of survival, reproduction, and transmission.

2. Interaction structure at each level

```txt
interaction_graph_i(m)
```

* Effective descriptor of who interacts with whom at level `i`.
* For Q073, it is treated as a compressed object that can be summarized by derived scalars such as clustering, connectivity, or motif frequencies.

3. Multi-level information integration

```txt
info_integration_L(m) >= 0
```

* Scalar that summarizes how strongly decisions or behaviors at a higher level depend on information aggregated across `L` lower levels.
* Values near zero indicate weak cross-level integration; larger values indicate stronger integration.

4. Conflict and cooperation summaries

```txt
conflict_cost_i(m)  >= 0
cooperation_gain_i(m) >= 0
```

* For each level `i`:

  * `conflict_cost_i(m)` measures effective losses due to conflict between units at level `i` and higher-level organization.
  * `cooperation_gain_i(m)` measures effective gains due to cooperative structures at or above level `i`.

5. Transition tension observable

We define a nonnegative scalar observable:

```txt
DeltaS_transition(m) >= 0
```

which summarizes:

* cross-level misalignment between `fitness_i(m)` across levels,
* imbalances between `conflict_cost_i(m)` and `cooperation_gain_i(m)`,
* fragility or insufficiency of `info_integration_L(m)` for supporting stable higher-level units.

The detailed dependence of `DeltaS_transition` on its inputs will be specified in simple ASCII form in Block 4.

### 3.3 Effective tension tensor components

Consistent with the TU core decisions, we introduce an effective tension tensor:

```txt
T_ij(m) = S_i(m) * C_j(m) * DeltaS_transition(m) * lambda(m) * kappa
```

where:

* `S_i(m)` are source-like factors for level `i`, summarizing how strongly selection and innovation are pushing configurations at that level.
* `C_j(m)` are receptivity-like factors for level `j`, summarizing how capable the structure at that level is of absorbing and stabilizing new cooperative patterns.
* `DeltaS_transition(m)` is the transition tension observable described above.
* `lambda(m)` is a convergence-state factor indicating whether the local evolutionary dynamics near `m` are convergent, recursive, divergent, or chaotic.
* `kappa` is a scaling constant for the magnitude of tension in Q073.

The detailed indexing of `i` and `j` is not specified at this layer; it is sufficient that, for each `m` in `M`, `T_ij(m)` is finite wherever needed.

### 3.4 Invariants and effective constraints

We define two invariants that will be used to interpret configurations before and after transitions.

1. Cross-level alignment index

```txt
I_align(m) = sum over i of w_i * A_i(m)
```

where:

* `w_i >= 0` are fixed weights with `sum over i of w_i = 1`,

* `A_i(m)` is an alignment score at level `i`, defined from `fitness_i(m)`, `conflict_cost_i(m)`, and `cooperation_gain_i(m)`, with a simple normalization such that:

  ```txt
  0 <= A_i(m) <= 1
  ```

* `I_align(m)` lies in `[0, 1]` and increases when incentives at different levels are more aligned.

2. Information integration index

```txt
I_info(m) = g(info_integration_L(m))
```

for a simple nondecreasing function `g` such that:

```txt
I_info(m) >= 0
```

and higher `I_info(m)` indicates stronger multi-level information integration.

These invariants are not assumed to be conserved. They are used to distinguish high-tension pre-transition configurations from lower-tension post-transition configurations.

### 3.5 Singular set and domain restrictions

Some observables may be undefined or inconsistent in certain coarse-grained descriptions. To handle this, we define a singular set:

```txt
S_sing = {
  m in M :
    DeltaS_transition(m) is undefined or not finite, or
    any fitness_i(m), conflict_cost_i(m), cooperation_gain_i(m), info_integration_L(m)
    is undefined or not finite
}
```

We restrict all Q073 reasoning at the effective layer to the regular subset:

```txt
M_reg = M \ S_sing
```

When an experiment or protocol would produce a state in `S_sing`, this is treated as “out of domain” for Q073. Such states do not count as evidence for or against any particular claim about mechanisms of major transitions.

---

## 4. Tension principle for this problem

This block states how Q073 is formulated as a tension problem.

### 4.1 Core tension functional

We define an effective transition tension functional:

```txt
Tension_transition(m) =
  alpha * DeltaS_misalignment(m) +
  beta  * DeltaS_coop(m) +
  gamma * DeltaS_info(m)
```

where:

* `alpha > 0`, `beta > 0`, `gamma > 0` are fixed coefficients chosen once for this encoding,
* `DeltaS_misalignment(m)` summarizes misalignment of fitness across levels,
* `DeltaS_coop(m)` summarizes net conflict cost minus cooperation gain,
* `DeltaS_info(m)` summarizes deficiencies in information integration.

Each term is nonnegative, so:

```txt
Tension_transition(m) >= 0
```

for all `m` in `M_reg`.

A simple implementation is:

```txt
DeltaS_misalignment(m) =
  sum over i < j of u_ij * |fitness_i(m) - f_ij_ref(m)|

DeltaS_coop(m) =
  sum over i of v_i * max(0, conflict_cost_i(m) - cooperation_gain_i(m))

DeltaS_info(m) =
  max(0, I_info_target - I_info(m))
```

with:

* `u_ij >= 0`, `v_i >= 0` fixed weights,
* `f_ij_ref(m)` representing reference fitness contributions at level `i` compatible with stable higher-level units, given the configuration at level `j`,
* `I_info_target > 0` a target integration level.

### 4.2 Major transitions as tension-reducing reorganizations

At the effective layer, Q073 encodes the following principle:

* A major evolutionary transition corresponds to a reorganization of organizational levels, roles, and information channels such that:

  * `Tension_transition(m_pre)` is high for pre-transition states,
  * `Tension_transition(m_post)` is significantly lower for post-transition states,

  across a nontrivial range of environments and perturbations, while global adaptability does not decrease.

In this view, mechanisms of major transitions are:

* ways of reconfiguring who reproduces, who controls reproduction, and how information flows, so that cross-level tensions are systematically reduced and higher-level units become stable.

### 4.3 Failure modes and limits

The same functional allows description of failure modes:

* If, for a given ecological and mutational regime, all accessible configurations `m` with strong cooperation or new levels of organization retain high `Tension_transition(m)`, then mechanisms of major transitions are blocked or severely constrained.
* If transitions occur but `Tension_transition(m_post)` is only temporarily reduced and then rises again under small perturbations, the transition is fragile and unlikely to persist over macroevolutionary timescales.

Q073 does not assert that all accessible transitions will occur. It only structures how to describe when mechanisms are available, blocked, robust, or fragile.

---

## 5. Counterfactual tension worlds

We describe two counterfactual worlds at the effective layer:

* World T: environments and parameters that support robust mechanisms for major transitions.
* World F: environments and parameters that block or severely limit such mechanisms.

### 5.1 World T (transition-enabled world)

In World T, the following patterns are observed for states `m_T` in `M_reg` that represent the long-term history of life:

1. Existence of multi-level stable units

   * Over time, new higher-level units (for example stable multicellular lineages, eusocial colonies) appear and persist.
   * For many such `m_T`, there are identifiable pre-transition states `m_pre` and post-transition states `m_post` with:

     ```txt
     Tension_transition(m_post) << Tension_transition(m_pre)
     ```

     using the same encoding parameters.

2. Cross-level alignment improves with transitions

   * For higher-level units after transitions:

     ```txt
     I_align(m_post) > I_align(m_pre)
     ```

     for a range of pre and post pairs, indicating better alignment between lower-level and higher-level incentives.

3. Information integration becomes robust

   * For post-transition states, `I_info(m_post)` exceeds a threshold `I_info_target` and remains above this threshold under moderate perturbations to interaction structures and environments.

4. Repeated innovation

   * Multiple distinct transitions occur over time, each reducing tension in its own region of configuration space, leading to an overall increase in organizational depth and diversity.

### 5.2 World F (transition-blocked world)

In World F, environments and parameters are such that mechanisms for major transitions fail to produce robust higher-level units.

1. Persistent high transition tension

   * For all states `m_F` that reflect the long-term history:

     ```txt
     Tension_transition(m_F) >= delta_block
     ```

     for some `delta_block > 0`, and attempts to form higher-level units do not reduce this tension sustainably.

2. Misalignment cannot be resolved

   * For any attempted configuration that resembles a higher-level unit, either:

     * lower-level fitness is severely compromised, or
     * higher-level structures collapse quickly.

   * There are no stable pairs `m_pre`, `m_post` with sustained tension reduction.

3. Information integration remains weak

   * Attempts to integrate information across levels either do not emerge or are fragile, with:

     ```txt
     I_info(m_F) << I_info_target
     ```

     in most states that resemble complex organizations.

4. Rich microevolution without major transitions

   * Lower-level evolution (for example within single-cell lineages) may be rich, but durable transitions to new higher-level individuals are absent or extremely rare.

### 5.3 Interpretive note

These counterfactual worlds do not construct detailed microdynamics or specify how states in `M` are derived from data. They only assert that, if faithful encodings of histories are available, then the patterns of `Tension_transition`, `I_align`, and `I_info` would differ systematically between transition-enabled and transition-blocked worlds.

---

## 6. Falsifiability and discriminating experiments

This block specifies experiments and protocols that test Q073 encodings at the effective layer. They do not prove or disprove any particular historical claim, but they can falsify specific choices of observables and tension functionals.

### Experiment 1: Digital evolution landscapes for transitions

*Goal:*
Test whether a given implementation of `DeltaS_transition` and `Tension_transition` can distinguish simulated environments that support major transitions from environments that block them.

*Setup:*

* Use a digital evolution platform in which agents reproduce, interact, and can evolve cooperative structures.

* Define two classes of simulation environments:

  * Class T: environments known (from prior work or configuration) to allow the evolution of higher-level units, such as stable cooperative groups with division of labor.
  * Class F: environments tuned so that cooperation is unstable or multi-level units cannot persist.

* For each run, construct an effective state `m_data` in `M_reg` summarizing:

  * organizational levels present,
  * interaction patterns,
  * cross-level fitness contributions,
  * conflict and cooperation summaries,
  * information integration estimates.

*Protocol:*

1. For a collection of runs in Class T and Class F, sample time points representing pre-transition, transition, and post-transition stages when applicable.

2. For each sampled time point, derive the corresponding `m_data` state.

3. Compute `DeltaS_misalignment(m_data)`, `DeltaS_coop(m_data)`, and `DeltaS_info(m_data)` according to the Q073 encoding, and then compute `Tension_transition(m_data)`.

4. Compare distributions of `Tension_transition` between:

   * pre and post states in Class T,
   * comparable states in Class F.

5. Repeat under moderate variations of encoding parameters (weights and thresholds) that remain within a pre-declared admissible range.

*Metrics:*

* Mean and variance of `Tension_transition` for pre and post states in Class T.
* Mean and variance of `Tension_transition` for comparable states in Class F.
* Effect size of tension reduction across transitions in Class T compared to changes in Class F.
* Robustness of the observed differences under admissible parameter variations.

*Falsification conditions:*

* If, for all admissible parameter choices, Class T and Class F show no systematic difference in `Tension_transition` patterns, the current encoding of Q073 is considered falsified or too weak to capture mechanisms of major transitions.
* If Class F environments, which lack stable higher-level units, regularly display lower `Tension_transition` than Class T post-transition states, the encoding is considered misaligned with the intended incentive_tension interpretation.

*Semantics implementation note:*
The experiment uses hybrid semantics consistent with Block 0: discrete indices for levels, roles, and agents, combined with continuous summaries for densities, fitness contributions, and integration scores.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. This experiment can reject specific tension encodings for Q073, but it does not by itself validate or invalidate historical claims about actual major transitions in natural evolution.

---

### Experiment 2: Multi-level selection in microbial communities

*Goal:*
Assess whether the Q073 tension encoding can distinguish microbial systems that exhibit emergent higher-level organization from systems that remain purely lower-level.

*Setup:*

* Select empirical or experimental datasets on evolving microbial communities, including:

  * systems in which group-level traits (for example biofilm formation, spatial structure, division of labor) are known to emerge and persist,
  * control systems in which such group-level traits are absent or transient.

* For each system, construct effective states `m_data` describing:

  * levels (cells, microcolonies, macro-colonies),
  * interaction patterns (for example local cooperation, cheating, spatial proximity),
  * inferred fitness contributions at different levels,
  * conflict and cooperation summaries,
  * information integration measures derived from observed coordination.

*Protocol:*

1. For each system, select time points representative of initial, intermediate, and late stages of evolution.

2. Encode each selected time point as a state `m_data` in `M_reg`.

3. Compute `Tension_transition(m_data)` for each time point.

4. Group results into:

   * systems with emergent higher-level traits,
   * systems without such traits.

5. Compare tension trajectories and steady-state values across the two groups.

*Metrics:*

* For systems with emergent higher-level traits:

  * change in `Tension_transition` over time,
  * relation between tension reduction and observed stability of group-level traits.

* For control systems:

  * lack of sustained tension reduction,
  * persistence of high `DeltaS_misalignment` or `DeltaS_coop`.

* Separation between tension profiles of the two groups.

*Falsification conditions:*

* If systems with clear emergent higher-level traits do not show any systematic tension reduction compared to controls, the encoding is considered weak or misaligned and should be revised.
* If control systems systematically show lower `Tension_transition` than systems with stable higher-level traits, the encoding contradicts the intended interpretation of major transitions and is considered falsified.

*Semantics implementation note:*
The analysis uses hybrid semantics: discrete labels for levels and traits, continuous-valued summaries for fitness, interaction strengths, and integration metrics, consistent with the metadata choice in Block 0.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. This experiment tests whether Q073 encodings track emergent higher-level organization in microbial systems, but it does not constitute a complete explanation of any specific transition.

---

## 7. AI and WFGY engineering spec

This block describes how Q073 can be used to design and evaluate AI systems within the WFGY framework at the effective layer.

### 7.1 Training signals

The following training signals can be derived from Q073 observables.

1. `signal_multilevel_alignment`

   * Definition: a scalar signal constructed from `I_align(m)` and `DeltaS_misalignment(m)`, such as:

     ```txt
     signal_multilevel_alignment = I_align(m) - c_misalign * DeltaS_misalignment(m)
     ```

     with a fixed coefficient `c_misalign > 0`.

   * Purpose: reward internal representations that reflect higher alignment between units at different levels when the context describes successful major transitions.

2. `signal_cooperation_stability`

   * Definition: a penalty proportional to `DeltaS_coop(m)` over contexts where long-lived cooperative units are described.

   * Purpose: discourage reasoning patterns that imply unstable cooperation in scenarios where persistent higher-level organizations are assumed.

3. `signal_transition_tension_score`

   * Definition: directly equal to `Tension_transition(m)` treated as an auxiliary loss or regularization term.

   * Purpose: provide a continuous indicator of how well a model’s internal state matches a low-tension configuration compatible with major transitions.

4. `signal_transition_contrast`

   * Definition: a contrastive signal computed as the difference in `Tension_transition` between pairs of contexts labeled as pre-transition and post-transition.

   * Purpose: encourage the model to recognize and separate configurations before and after major transitions.

### 7.2 Architectural patterns

Q073 suggests several AI module patterns.

1. `MultiLevelSelectionHead`

   * Role: given an internal embedding of a biological or organizational scenario, estimate:

     * which levels are relevant,
     * approximate `fitness_i(m)` and cross-level alignment indicators.

   * Interface:

     * Input: contextual embedding representing a description of an evolutionary or organizational system.
     * Output: level-wise alignment scores and a summary of `I_align(m)`.

2. `TransitionPatternDetector`

   * Role: detect signatures of major transitions in a sequence of states, such as:

     * emergence of new levels,
     * reduction of conflict and increase of cooperation gains,
     * increased information integration.

   * Interface:

     * Input: sequence of state-like embeddings or scenario descriptions.
     * Output: scores indicating likelihood and type of transition.

3. `OrganizationalLevel_Encoder`

   * Role: produce OrganizationalLevel_Descriptor objects from text or structured data.

   * Interface:

     * Input: description of a system’s actors, interactions, and control channels.
     * Output: compact representation of organizational levels that can be passed to tension evaluation modules.

### 7.3 Evaluation harness

An evaluation harness for AI systems using Q073 modules might include:

1. Task families

   * Explanatory tasks:

     * explain why certain transitions occurred (for example unicellular to multicellular, eusociality) in terms of conflicts, cooperation, and information integration.

   * Predictive tasks:

     * judge whether a described system is likely to support a future major transition under specified conditions.

2. Conditions

   * Baseline condition:

     * the model operates without explicit Q073-derived modules or signals.

   * TU-augmented condition:

     * the model uses MultiLevelSelectionHead, TransitionPatternDetector, and associated signals.

3. Metrics

   * Consistency of multi-level reasoning:

     * frequency of contradictions in fitness definitions across levels.

   * Use of structured concepts:

     * fraction of explanations that explicitly mention mechanisms aligned with Q073 (for example conflict suppression, division of labor, information integration).

   * Robustness:

     * stability of answers when scenarios are perturbed in ways that should or should not affect transition feasibility.

### 7.4 60-second reproduction protocol

A minimal protocol for external users to experience the impact of Q073 encoding.

* Baseline setup:

  * Prompt: ask an AI system to explain “What are major evolutionary transitions and why did they happen?” without any mention of tension or multi-level selection.
  * Observation: check whether the explanation is a loose list of historical events or a structured account of mechanisms.

* Q073-encoded setup:

  * Prompt: same question, with an instruction to organize the explanation around:

    * incentives at different levels,
    * cooperation and conflict management,
    * information integration and new levels of individuality.

  * Observation: check whether the explanation:

    * identifies conflicts between lower and higher levels,
    * explains how cooperation became stable,
    * highlights changes in information storage and control.

* Comparison metric:

  * Use a simple rubric to rate:

    * clarity of multi-level structure,
    * explicit discussion of mechanisms,
    * avoidance of circular or purely narrative explanations.

* What to log:

  * Prompts, full responses, and any Q073-derived tension scores or module outputs.
  * This allows later inspection of how Q073 components influenced the reasoning, without exposing any deep TU generative rules.

---

## 8. Cross problem transfer template

This block describes reusable components from Q073 and their direct reuse targets.

### 8.1 Reusable components produced by this problem

1. ComponentName: `MultiLevelSelection_TensionFunctional`

   * Type: functional

   * Minimal interface:

     ```txt
     Inputs: {
       fitness_levels: vector of fitness_i values across levels,
       conflict_costs: vector of conflict_cost_i values,
       cooperation_gains: vector of cooperation_gain_i values,
       info_integration: scalar info_integration_L
     }
     Output: {
       Tension_transition: nonnegative scalar,
       decomposed_terms: (DeltaS_misalignment, DeltaS_coop, DeltaS_info)
     }
     ```

   * Preconditions:

     * Inputs must be derived from a coherent description of a multi-level system where levels and roles are well defined.
     * All inputs must be finite real numbers.

2. ComponentName: `OrganizationalLevel_Descriptor`

   * Type: field

   * Minimal interface:

     ```txt
     Inputs: {
       units: list of entities at each level,
       interactions: summary of interaction patterns,
       control_channels: summary of who influences whom
     }
     Output: {
       levels: structured list of organizational levels,
       role_map: mapping from units to roles,
       topology_summary: compact representation of interaction and control structure
     }
     ```

   * Preconditions:

     * There must be a finite and identifiable set of units and interactions.
     * Control channels must be described at least qualitatively.

3. ComponentName: `TransitionScenario_Template`

   * Type: experiment_pattern

   * Minimal interface:

     ```txt
     Inputs: {
       model_class: description of biological, social, or artificial systems,
       environment_params: key parameters controlling interactions and selection pressures
     }
     Output: {
       world_T_spec: scenario with mechanisms enabling major transitions,
       world_F_spec: scenario with mechanisms blocked,
       evaluation_protocol: how to compute and compare Tension_transition
     }
     ```

   * Preconditions:

     * The model class must support clear identification of levels, interactions, and selection pressures.
     * It must be possible to vary environment parameters to enable or block transitions.

### 8.2 Direct reuse targets

1. Target: Q080 (Limits of biosphere adaptability)

   * Reused component: `OrganizationalLevel_Descriptor`.
   * Why it transfers: global adaptability depends on how many organizational levels exist and how they distribute functions; this descriptor quantifies that structure.
   * What changes: emphasis shifts from mechanisms of transitions to the relation between organizational depth and adaptability limits.

2. Target: Q098 (Anthropocene system dynamics)

   * Reused component: `TransitionScenario_Template`.
   * Why it transfers: human-driven systemic changes can be framed as transitions (or failed transitions) in socio-ecological organization.
   * What changes: model_class becomes coupled human–environment systems rather than purely biological populations.

3. Target: Q107 (Mechanisms of large scale collective action)

   * Reused component: `MultiLevelSelection_TensionFunctional`.
   * Why it transfers: large-scale collective action problems are governed by misaligned incentives between individuals, organizations, and institutions, analogous to multi-level selection.
   * What changes: fitness and cooperation are interpreted in terms of payoffs, norms, and institutional stability instead of reproduction.

4. Target: Q125 (Multi agent AI dynamics)

   * Reused component: `TransitionScenario_Template` and `MultiLevelSelection_TensionFunctional`.
   * Why it transfers: emergent higher-level AI organizations (for example coalitions, institutions of agents) can be studied with the same transition-enabled versus transition-blocked scenarios and tension functionals.
   * What changes: levels correspond to agents, clusters of agents, and meta-level coordination mechanisms within AI ecosystems.

---

## 9. TU roadmap and verification levels

### 9.1 Current levels

* E_level: E1

  * Q073 provides a coherent effective-layer encoding of mechanisms of major transitions, including:

    * state space `M`,
    * observables and `DeltaS_transition`,
    * a tension functional `Tension_transition`,
    * at least two discriminating experiments with falsification conditions.

* N_level: N1

  * Q073 provides:

    * a structured narrative in terms of World T and World F,
    * clear graph placement and transfer components,
    * an elementary explanation that aligns with the encoding.

### 9.2 Next measurable step toward E2

To reach E2, at least one of the following should be implemented and documented:

1. A working prototype that applies `MultiLevelSelection_TensionFunctional` to real or simulated systems (for example digital evolution and microbial communities), producing tension profiles for pre and post transitions and making the results publicly available.
2. A systematic comparative study that:

   * defines a library of model classes and environments (transition-enabled and transition-blocked),
   * applies Q073 encodings to each case,
   * reports success and failure cases, and refines the encoding based on falsification results.

Both steps operate solely at the effective layer, using observable summaries, and do not require exposing any deep TU generative rule.

### 9.3 Long-term role in the TU program

In the broader Tension Universe program, Q073 is intended to:

* Serve as the central node for understanding how multi-level incentive_tension can be reorganized to create new higher-level individuals.

* Provide templates for analyzing transitions in other domains, including:

  * socio-technical systems,
  * economic and political structures,
  * multi-agent AI ecosystems.

* Help calibrate which aspects of major transitions are universal and which are substrate-specific, using the same tension-based descriptors.

---

## 10. Elementary but precise explanation

Major evolutionary transitions are moments in the history of life when the basic units of evolution changed. Examples include:

* cells joining to form multicellular organisms,
* individual insects forming eusocial colonies,
* human groups developing language and complex societies.

Before a transition, there are many small units that each try to survive and reproduce on their own. They can cooperate, but they also have reasons to cheat or compete. After a successful transition, many of these units behave as parts of a larger individual that has its own way to survive and reproduce.

In the Tension Universe view, this is described with a tension number:

* For a given configuration of life, a state is built that summarizes:

  * which levels exist (genes, cells, organisms, groups),
  * how they interact,
  * how well their incentives line up,
  * how much information is shared and used across levels.

* From this state, a scalar `Tension_transition` is computed:

  * high tension means strong conflicts between levels, unstable cooperation, and weak information integration,
  * low tension means better alignment, stable cooperation, and strong information integration.

A major transition can then be read as:

* moving from a high-tension configuration (many conflicts, fragile groups)
* to a low-tension configuration (cooperation is stable, roles are specialized, information flows well),

without losing the ability of the system to adapt and evolve.

Two kinds of worlds can be imagined:

* In a “transition-enabled” world, it is possible to find ways to reorganize life so that the tension drops and new higher-level individuals become stable.
* In a “transition-blocked” world, any attempt at such reorganization either fails quickly or keeps tension high.

Q073 does not claim to have a final theory of how every transition actually happened. Instead, it provides:

* a way to measure how aligned or misaligned different levels are,
* a way to describe when a proposed mechanism truly reduces tension,
* tools that can be applied not only to biological evolution, but also to large-scale cooperation in human societies and multi-agent AI systems.

In this sense, Q073 is a structured way to talk about “how small things become parts of larger things” in a way that can be checked, compared, and tested, rather than just listed as a sequence of historical events.
