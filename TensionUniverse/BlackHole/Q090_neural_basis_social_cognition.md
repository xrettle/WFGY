# Q090 · Neural basis of social cognition

## 0. Header metadata

```txt
ID: Q090
Code: BH_NEURO_SOC_BRAIN_L3_090
Domain: Neuroscience
Family: social_neuroscience
Rank: S
Projection_dominance: C
Field_type: cognitive_field
Tension_type: cognitive_tension
Status: Open
Semantics: hybrid
E_level: E1
N_level: N1
Last_updated: 2026-01-25
```

---

## 1. Canonical problem and status

### 1.1 Canonical statement

The canonical question is:

> What concrete neural systems and circuit level mechanisms in the brain support social cognition, and how do they coordinate to generate stable, flexible social understanding of self and others?

In this context:

* "Social cognition" includes:

  * inferring others' mental states,
  * understanding intentions, beliefs and desires,
  * empathy and affective sharing,
  * processing social norms and roles,
  * predicting others' behavior.
* "Neural basis" refers to:

  * identifiable brain regions and networks,
  * effective connectivity among them,
  * local circuit motifs that implement computations relevant for social cognition.

The problem is not only to list regions. It is to explain how:

1. Large scale social brain networks (for example medial prefrontal, temporo parietal, superior temporal, anterior temporal, amygdala, striatum, insula) interact over time.
2. Local microcircuit motifs support the computations implied by social tasks.
3. These multi scale structures jointly realize robust, context sensitive social cognition in healthy individuals.

We work strictly at an effective layer. We only describe observable patterns and tension relations. We do not specify any deep generative rules of Tension Universe.

### 1.2 Status and difficulty

The state of knowledge can be summarized as follows.

1. Social brain networks

There is substantial evidence from lesion studies, functional imaging and electrophysiology that social cognition recruits:

* medial prefrontal cortex,
* temporo parietal junction,
* posterior superior temporal sulcus,
* anterior temporal cortex,
* amygdala and connected limbic regions,
* striatal and orbitofrontal value systems.

These systems show selective engagement during tasks that involve thinking about others, understanding narratives, or evaluating social outcomes.

2. Partial computational hypotheses

Multiple computational hypotheses have been proposed, such as:

* predictive coding of others' actions and mental states,
* hierarchical generative models of agents and groups,
* value based learning of social norms and reputations.

These hypotheses connect some local circuit motifs and global network patterns to social behaviors, but none is universally accepted or complete.

3. Gaps and open aspects

Key difficulties remain:

* How large scale coordination among social networks is organized across time scales.
* How social and non social computations share or compete for neural resources.
* How individual differences in social cognition emerge from variations in structure and plasticity.
* How observed neural changes in development, aging or disease produce specific social cognitive profiles.

The problem is therefore open and multi scale. It is unlikely to admit a single simple answer, but it is still meaningful to encode it as a structured effective layer question.

### 1.3 Role in the BlackHole project

Within the BlackHole S problem collection, Q090:

1. Serves as the central node for social cognition inside the neuroscience cluster.
2. Connects micro level coding and plasticity problems to macro level social behavior and AI social agents.
3. Provides a template for expressing cognitive_tension between internal social models and external social realities in a precise but non reductionist way.
4. Supplies reusable components for AI and multi agent governance problems that need biologically informed social reasoning models.

### References

1. Adolphs R.
   "The social brain: Neural basis of social cognition."
   Annual Review of Psychology, 2009.

2. Frith CD, Frith U.
   "Social cognition in humans."
   Current Biology, 2007.

3. Lieberman MD.
   "Social cognitive neuroscience: A review of core processes."
   Annual Review of Psychology, 2007.

4. Stanley DA, Adolphs R.
   "Toward a neural basis for social behavior."
   Neuron, 2013.

5. A major institute or society overview page on social neuroscience or social brain networks,
   providing a stable public description of the field and its core questions.

---

## 2. Position in the BlackHole graph

This block records how Q090 sits in the BlackHole graph. All edges use one line reasons that point to concrete components or tension types.

### 2.1 Upstream problems

These nodes provide prerequisites or general tools that Q090 reuses.

* Q083 (BH_NEURO_NEURAL_CODING_L3_083)
  Reason: Supplies general neural coding principles reused when defining SocialGraphField and social feature observables.

* Q084 (BH_NEURO_LTM_STORAGE_L3_084)
  Reason: Provides long term memory storage mechanisms used for stable person specific and group specific social representations.

* Q085 (BH_NEURO_PLASTICITY_RULES_L3_085)
  Reason: Contributes plasticity rules that underlie social learning and updates to internal social models.

* Q089 (BH_NEURO_PREDICTIVE_CODE_L3_089)
  Reason: Gives predictive coding implementation patterns extended here to social predictive circuits and social prediction errors.

### 2.2 Downstream problems

These nodes directly reuse Q090 components or depend on its tension structure.

* Q121 (BH_AI_SOCIAL_AGENTS_L3_121)
  Reason: Reuses SocialGraphField and SocialTensionFunctional_Soc to design AI agents with engineered social cognition modules.

* Q122 (BH_AI_MULTI_AGENT_GOVERN_L3_122)
  Reason: Uses Q090 social tension observables to formulate norms and governance rules in multi agent systems.

* Q111 (BH_SOC_COLLECTIVE_BEHAVIOR_L3_111)
  Reason: Imports SocialGraphField and EmpathyChannelDescriptor to model collective social dynamics and belief flows.

### 2.3 Parallel problems

Parallel nodes share similar tension types but do not reuse specific components.

* Q081 (BH_NEURO_CONSCIOUS_HARD_L3_081)
  Reason: Both study subjective and higher order cognition under cognitive_tension, but Q081 focuses on consciousness rather than social content.

* Q089 (BH_NEURO_PREDICTIVE_CODE_L3_089)
  Reason: Both rely on predictive circuits, yet Q089 stays content agnostic while Q090 specializes prediction for social signals and agents.

* Q087 (BH_NEURO_NEURODEGEN_L3_087)
  Reason: Both involve large scale network degradation patterns, with Q087 focused on disease progression and Q090 on resulting social cognitive changes.

### 2.4 Cross domain edges

Cross domain edges connect Q090 to problems in other clusters.

* Q059 (BH_CS_INFO_THERMODYN_L3_059)
  Reason: Reuses tension between internal models and external outcomes to quantify social information bottlenecks and cognitive costs.

* Q123 (BH_AI_INTERP_L3_123)
  Reason: Uses SocialRepresentationProbe from Q090 as a template for probing social concepts inside AI representations.

* Q032 (BH_PHYS_QTHERMO_L3_032)
  Reason: Adapts the idea of multi scale field interactions and effective temperature to social brain fields and cognitive load measures.

All references to Q numbers here are adjacency only. No external URLs appear in this block, so the full graph can be assembled as a simple adjacency list.

---

## 3. Tension Universe encoding (effective layer)

All definitions in this block stay at the effective layer. We only specify:

* state space and field types,
* observables and invariants,
* tension functionals and singular sets.

We do not describe how to build these objects from scans, spikes or behavioral logs.

### 3.1 State space

We assume a semantic state space

`M`

with the following interpretation.

* Each state `m` in `M` represents a coherent social brain configuration for a single individual at a chosen time scale.
* A configuration `m` encodes summaries of:

  * activity levels in key social brain subsystems,
  * effective connectivity among these subsystems,
  * latent variables that describe internal social models of self, others and groups,
  * current social context class (for example cooperative, competitive, neutral).

We only require that for each state `m` there exists a finite dimensional representation in Par which is a subset of `R^k` for some finite `k`. We do not specify any procedure that maps raw measurements into that representation.

### 3.2 Effective observables and fields

We define the following effective observables on `M`.

1. Social activity field

```txt
SocActivity(m; R_set) >= 0
```

* Input: state `m` and a finite set of regions or parcels `R_set` in a predefined social brain atlas.
* Output: a vector of nonnegative values summarizing activity in each region, for example normalized amplitudes or rates.
* Interpretation: captures how strongly each social subsystem is engaged in the current configuration.

2. Social connectivity observable

```txt
SocConn(m; R_pair)
```

* Input: state `m` and an ordered pair of regions `R_pair`.
* Output: an effective connectivity value that summarizes influence from the first region to the second in the present configuration.
* Interpretation: encodes directed or undirected functional coupling among social subsystems.

3. Social model descriptor

```txt
SocModel(m)
```

* Input: state `m`.
* Output: a low dimensional descriptor vector summarizing:

  * internal beliefs about others' traits and intentions,
  * internal beliefs about group norms and roles,
  * internal beliefs about self in the current social context.
* Interpretation: a compact code for the internal social generative model at that moment. We only assume such a descriptor exists and fits in Par.

4. Social prediction error observable

```txt
SocPredErr(m; C_task) >= 0
```

* Input: state `m` and a task or context label `C_task` that belongs to a finite family of social tasks.
* Output: a nonnegative scalar summarizing mismatch between predicted and observed social cues or outcomes in that context.
* Interpretation: aggregates social error signals across relevant circuits, without exposing any micro level update rules.

### 3.3 Social graph field

We combine activity and connectivity into a single field.

```txt
SocialGraphField(m)
```

* Input: state `m`.
* Output: a structured object that consists of:

  * a list of nodes for the selected social brain regions,
  * node features derived from `SocActivity(m; R_set)` and `SocModel(m)`,
  * edge features derived from `SocConn(m; R_pair)`.

SocialGraphField is defined only at the level of summaries. We do not specify how neural signals are transformed into these quantities.

### 3.4 Tension related quantities

We define two primary mismatch observables and a combined social tension.

1. Structural mismatch

```txt
DeltaS_soc_struct(m) >= 0
```

* Measures how far SocialGraphField(m) deviates from a reference class of healthy social network architectures, after normalizing for age and global brain size.
* Properties:

  * `DeltaS_soc_struct(m) = 0` if SocialGraphField(m) falls exactly inside the reference class.
  * Larger values indicate greater deviation in connectivity patterns or subsystem balance.

2. Predictive mismatch

```txt
DeltaS_soc_pred(m) >= 0
```

* Measures how far SocPredErr(m; C_task) deviates from a reference pattern of low social prediction error across tasks.
* Properties:

  * `DeltaS_soc_pred(m) = 0` if social prediction errors match the reference low tension profile.
  * Larger values indicate persistent or widespread social prediction errors.

3. Combined social tension

For fixed positive weights chosen in advance,

```txt
DeltaS_SOC(m) = w_struct * DeltaS_soc_struct(m)
              + w_pred   * DeltaS_soc_pred(m)
```

with:

```txt
w_struct > 0
w_pred > 0
w_struct + w_pred = 1
```

Weights are fixed for all evaluations within a given study. They cannot be tuned after seeing data.

### 3.5 Singular set and domain restriction

Some configurations may make DeltaS_SOC undefined or misleading, for example when data are missing or contradictory.

We define a singular set:

```txt
S_sing = {
  m in M :
  DeltaS_soc_struct(m) is undefined or infinite
  or DeltaS_soc_pred(m) is undefined or infinite
}
```

We restrict our analysis to the regular domain:

```txt
M_reg = M \ S_sing
```

Handling of the singular set:

* States in S_sing are treated as out of domain for Q090 tension analysis.
* They may still appear as boundary cases or in separate data quality checks.
* Block 6 experiments will specify how to recognize and exclude such states when constructing empirical datasets.

---

## 4. Tension principle for this problem

This block states how Q090 is characterized as a tension problem.

### 4.1 Core social tension functional

We define the core social tension functional as

```txt
Tension_SOC(m) = DeltaS_SOC(m)
```

for `m` in `M_reg`. This is a nonnegative scalar that summarizes:

* mismatch between actual social brain structure and reference architecture,
* mismatch between social prediction performance and reference low tension profile.

Required properties:

* `Tension_SOC(m) >= 0` for all `m` in `M_reg`.
* `Tension_SOC(m)` is small if both mismatch terms are small.
* `Tension_SOC(m)` becomes large when either structural or predictive mismatch grows.

### 4.2 Low tension social brain principle

At the effective layer, the low tension principle for Q090 is:

> For typical individuals in typical social environments, there exist configurations `m` in `M_reg` where Tension_SOC(m) remains within a narrow band across a broad range of everyday social contexts.

More concretely, for a chosen family of encodings consistent with Block 3 and for a finite set of social tasks and contexts, we expect that for many individuals:

```txt
Tension_SOC(m) <= epsilon_SOC
```

for states `m` that represent well practiced or well understood social situations. The threshold `epsilon_SOC` depends on measurement noise and modeling precision but should not grow without bound as better data become available.

### 4.3 Persistent high tension social brain patterns

Conversely, persistent high tension patterns arise when no configuration in `M_reg` can keep DeltaS_SOC small across core social domains.

At the effective layer we state:

> If structural and predictive properties of the social brain are sufficiently misaligned with reference patterns, then any realistic sequence of configurations will yield Tension_SOC(m) that exceeds a strictly positive lower bound on a substantial subset of social contexts.

Formally, for a given encoding class that respects the rules of Block 3, there can exist a value `delta_SOC > 0` such that for all configurations `m` that represent certain individuals and contexts,

```txt
Tension_SOC(m) >= delta_SOC
```

on a nontrivial set of tasks. This expresses persistent cognitive tension rather than a transient fluctuation.

Q090 does not claim which pattern is realized for any given person. It only codifies how to describe and measure these possibilities.

---

## 5. Counterfactual tension worlds

We now describe two counterfactual worlds, entirely at the effective layer.

* World T: typical social brains with low sustained social tension.
* World F: social systems where misalignments produce persistent high social tension.

These worlds are characterized by observable patterns. No hidden Tension Universe generative rules are exposed.

### 5.1 World T (low social tension world)

In World T:

1. Structural robustness

* For most individuals, SocialGraphField(m) stays close to the reference architecture class during development and adulthood.
* Redundancy and alternative pathways allow the network to absorb moderate perturbations without large increases in DeltaS_soc_struct.

2. Efficient social prediction

* SocPredErr(m; C_task) is typically small for frequently encountered social contexts.
* Learning reduces social prediction errors over time, and DeltaS_soc_pred remains bounded even in moderately novel situations.

3. Cross subsystem coherence

* Activity in mentalizing, mirroring, value and salience subsystems tends to form coherent patterns during social interactions.
* Conflicts among goals, norms and empathic responses are resolved over time without leaving long term high Tension_SOC.

4. Gradual adaptation

* When environments change, individuals can move through sequences of states `m` that adjust SocialGraphField and SocModel while keeping Tension_SOC under moderate control.

### 5.2 World F (high social tension world)

In World F:

1. Structural misalignment

* For certain individuals or populations, SocialGraphField(m) systematically deviates from the reference architecture in ways that cannot be compensated by simple plasticity.
* DeltaS_soc_struct stays large across many configurations, indicating chronic network level misalignment.

2. Persistent prediction error

* SocPredErr(m; C_task) remains high even after extended experience with common social situations.
* DeltaS_soc_pred does not decrease with learning, or decreases only in narrow situations while staying high elsewhere.

3. Cross subsystem conflict

* Activity patterns in different social subsystems are frequently incompatible, for example strong value signals for one action combined with strong empathic signals for another.
* As a result, Tension_SOC(m) is often above a nonzero lower bound in important social contexts.

4. Fragile compensation

* Some configurations may temporarily reduce Tension_SOC in narrow contexts, but small changes in context or network parameters cause tension to rise again.
* There is no broad region of M_reg where social tension remains low across diverse social interactions.

### 5.3 Interpretive note

These worlds neither categorize real individuals nor diagnose any condition. They are abstract models that:

* help classify patterns of observables,
* guide the design of experiments,
* provide structure for AI architectures inspired by social brain organization.

They make no claim about the prevalence of any particular pattern in real populations.

---

## 6. Falsifiability and discriminating experiments

Experiments in this block test Q090 encodings, not human beings. They can falsify specific choices of observables, reference classes or parameter ranges. They cannot prove or disprove any fundamental truth about social cognition.

### Experiment 1: Social prediction tension mapping

*Goal:*

Test whether the defined Tension_SOC(m) functional tracks social prediction difficulty across tasks and individuals in a stable way.

*Setup:*

* Participants: a group of adults with typical social functioning, plus a comparison group with known social cognitive challenges, where inclusion respects ethical and clinical standards.
* Tasks: a battery of social prediction tasks and matched non social control tasks, each labeled with a context tag C_task.
* Data: non invasive measurements that allow construction of SocialGraphField like summaries and behavioral prediction error scores.

*Protocol:*

1. For each participant and task, construct a state `m_data` that encodes:

   * SocActivity summaries for key social regions,
   * SocConn summaries for selected pairs of regions,
   * SocModel summaries for self and other representations,
   * SocPredErr derived from behavioral performance.
     The construction procedure uses standard neuroimaging and behavioral analysis pipelines. It is not described in Tension Universe terms.
2. For each `m_data`, compute:

   * DeltaS_soc_struct(m_data) by comparing SocialGraphField(m_data) to a fixed healthy reference class,
   * DeltaS_soc_pred(m_data) by comparing SocPredErr to a fixed low tension profile.
3. Compute Tension_SOC(m_data) for each state, with weights w_struct and w_pred that were fixed before the experiment.
4. Analyze how Tension_SOC distributions differ:

   * between social and non social tasks,
   * between participant groups,
   * across repeated measurements.

*Metrics:*

* Distribution of Tension_SOC across tasks and individuals.
* Correlation between Tension_SOC and observed social prediction errors.
* Stability of Tension_SOC when measurement noise or analysis pipelines are slightly varied.

*Falsification conditions:*

* If no reasonable choice of reference classes and parameter ranges yields a robust positive correlation between Tension_SOC and behavioral social prediction error across individuals and tasks, then the current encoding of DeltaS_soc_struct, DeltaS_soc_pred or Tension_SOC is considered falsified.
* If small, methodologically justified changes in the construction of `m_data` produce arbitrarily different Tension_SOC patterns for the same participants and tasks, the encoding is judged unstable and rejected.

*Semantics implementation note:*

This experiment uses hybrid representations for SocialGraphField and tension quantities that are consistent with the metadata semantics. The implementation treats regional activities and connectivity as continuous valued summaries and graph relations as discrete structures layered on top.

*Boundary note:*

Falsifying TU encoding != solving canonical statement. This experiment can reject particular Q090 encodings but does not fully solve the neural basis of social cognition.

---

### Experiment 2: Network perturbation and compensation pattern

*Goal:*

Evaluate whether Q090 encodings can predict structured changes in Tension_SOC under targeted perturbations of social brain networks.

*Setup:*

* Data sources: lesion studies, naturally occurring focal brain injuries, or ethically acceptable perturbation methods on social brain regions.
* Regions of interest: key nodes in SocialGraphField, such as medial prefrontal cortex or temporo parietal junction.

*Protocol:*

1. Identify a set of individuals with focal perturbations in specific social brain regions and a matched comparison group.
2. For each individual and a set of social tasks, construct states `m_pre` and `m_post` that represent configurations before and after perturbation, or configurations in perturbed and non perturbed groups.
3. Compute DeltaS_soc_struct and DeltaS_soc_pred for each state.
4. Compute Tension_SOC and analyze:

   * whether perturbations produce systematic shifts in Tension_SOC in predicted directions,
   * whether compensation in other regions reduces Tension_SOC in some contexts.

*Metrics:*

* Change in Tension_SOC associated with perturbation.
* Task dependence of tension changes across social and non social conditions.
* Degree of compensation indicated by partial recovery of Tension_SOC toward baseline.

*Falsification conditions:*

* If perturbations that strongly affect known social brain hubs do not produce any structured changes in Tension_SOC beyond noise, for any reasonable encoding within the Q090 class, the encoding is considered misaligned with social brain physiology.
* If Tension_SOC suggests large tension shifts in contexts where behavior and standard imaging show minimal changes, the encoding is considered inconsistent and rejected or revised.

*Semantics implementation note:*

As in Experiment 1, this protocol uses hybrid representations where continuous fields over regions and discrete network relations are combined. The implementation keeps this representation consistent across individuals and conditions.

*Boundary note:*

Falsifying TU encoding != solving canonical statement. This experiment can show that a particular mapping from data to Q090 observables is inadequate, but cannot by itself identify the true neural basis of social cognition.

---

## 7. AI and WFGY engineering spec

This block shows how Q090 becomes an engineering module for AI systems, without revealing any deep Tension Universe rules.

### 7.1 Training signals

1. `signal_social_prediction_error`

   * Definition: a scalar signal proportional to DeltaS_soc_pred for model internal states that represent social prediction tasks.
   * Purpose: encourage models to form internal states that reduce social prediction mismatch when the task requires accurate social forecasting.

2. `signal_social_consistency`

   * Definition: a signal derived from internal consistency between different parts of a model representation that correspond to self, others and groups, modeled on SocModel and SocialGraphField structure.
   * Purpose: penalize internal states where representations of others and groups are strongly incompatible with past commitments in contexts that should be stable.

3. `signal_empathic_alignment`

   * Definition: a signal that measures alignment between value like representations for self and inferred value like representations for relevant others, under cooperative contexts.
   * Purpose: support the ability to reason about cooperative outcomes while keeping social cognitive tension moderate.

4. `signal_social_tension_score`

   * Definition: a direct analogue of Tension_SOC for internal model states, computed by a dedicated head that estimates structural and predictive mismatch.
   * Purpose: act as an auxiliary loss that keeps social reasoning modules within a low tension regime for scenarios designated as typical.

### 7.2 Architectural patterns

1. `SocialCognitionHead`

   * Role: a module attached to a general purpose model that reads latent states and outputs:

     * an estimate of SocialGraphField like structure,
     * an estimate of SocModel like descriptors,
     * an estimate of Tension_SOC.
   * Interface:

     * Inputs: internal hidden states or embeddings for social scenarios.
     * Outputs: structured summaries and scalar tension value.
   * Use: training with Q090 style signals or as a diagnostic head in evaluation.

2. `SocialGraphEncoder`

   * Role: a module that encodes interaction graphs, roles and observed social cues into a representation compatible with SocialGraphField.
   * Interface:

     * Inputs: descriptions of agents, their relations, and recent interactions.
     * Outputs: graph structured embeddings with node and edge features.

3. `EmpathyChannelFilter`

   * Role: a mechanism that compares predicted outcomes for self and others and gauges mismatches similar to empathic tension.
   * Interface:

     * Inputs: separate channels for self related and other related value estimates.
     * Outputs: a discrepancy score that can be incorporated into signal_empathic_alignment.

### 7.3 Evaluation harness

A harness for assessing models that use Q090 modules.

1. Tasks

   * Social scenario understanding: narratives or dialogues where models must infer beliefs and intentions.
   * Social prediction tasks: forecasting likely actions of agents given their history and context.
   * Social norm reasoning: judging appropriateness of actions under explicit or implicit norms.

2. Conditions

   * Baseline condition: model runs without any Q090 specific modules or signals.
   * TU condition: model uses SocialCognitionHead, SocialGraphEncoder and Q090 training signals as auxiliaries.

3. Metrics

   * Task performance measures, such as accuracy in prediction or consistency of explanations.
   * Internal social tension measures, such as average estimated Tension_SOC across tasks where low tension is expected.
   * Robustness to prompt variations, measured by how stable inferred social structures and explanations remain.

### 7.4 60 second reproduction protocol

A minimal procedure to let users observe the effect of Q090 framing in an AI system.

* Baseline setup:

  * Prompt the model: "Explain how the human brain supports social cognition and understanding of others."
  * Record the answer and any intermediate representations if observable.
  * Typical issues: scattered lists of regions, vague descriptions of mental processes, limited structure.

* TU encoded setup:

  * Prompt the model with an additional instruction: "Organize your explanation around social brain networks, internal social models and social tension between prediction and outcome, using an explicit notion similar to Tension_SOC at the effective layer."
  * If available, request the model to output:

    * its estimated social brain structure summary,
    * an estimate of social tension for example scenarios.

* Comparison metric:

  * Rate structural clarity, explicit linkage between networks, internal models and behavior, and consistency across repeated questions.
  * Compare how often the TU encoded setup yields explanations that can be mapped directly to Q090 observables.

* What to log:

  * Prompts, full responses, and any auxiliary quantities the model reports that correspond to Q090 observables or Tension_SOC.
  * These logs allow third parties to inspect whether Q090 framing produces stable and interpretable patterns.

---

## 8. Cross problem transfer template

This block lists reusable components and direct reuse targets.

### 8.1 Reusable components produced by this problem

1. ComponentName: `SocialGraphField`

   * Type: field
   * Minimal interface:

     * Inputs: a set of brain regions or abstract agent units, measures of activity and connectivity, and role labels.
     * Output: a structured representation that combines node and edge features into a graph like object.
   * Preconditions:

     * The region set or agent set is finite and indexed.
     * Activity and connectivity summaries are well defined and finite.

2. ComponentName: `SocialTensionFunctional_Soc`

   * Type: functional
   * Minimal interface:

     * Inputs: SocialGraphField like structure and social prediction summary data.
     * Output: a nonnegative scalar tension value DeltaS_SOC and optional vector of component wise mismatches.
   * Preconditions:

     * Reference architecture class and reference prediction profile are specified before evaluation.
     * Weight parameters w_struct and w_pred are fixed.

3. ComponentName: `SocialRepresentationProbe`

   * Type: experiment_pattern
   * Minimal interface:

     * Inputs: model class (biological or artificial) and a set of social tasks.
     * Output: an experimental protocol that maps internal states to Q090 observables and computes Tension_SOC without altering the underlying model.

### 8.2 Direct reuse targets

1. Q089 (BH_NEURO_PREDICTIVE_CODE_L3_089)

   * Reused component: SocialTensionFunctional_Soc.
   * Why it transfers: Q089 studies predictive coding implementations. SocialTensionFunctional_Soc gives a concrete way to assess how well predictive architectures handle social content.
   * What changes: the internal predictive circuits vary, but the functional applied to their observable summaries remains the same.

2. Q121 (BH_AI_SOCIAL_AGENTS_L3_121)

   * Reused components: SocialGraphField and SocialRepresentationProbe.
   * Why it transfers: Q121 builds AI agents with explicit social modules that can be structured and audited with the same graph and probe patterns.
   * What changes: physical brain regions are replaced by abstract agent components, but the interface of the field and the probe stays identical.

3. Q123 (BH_AI_INTERP_L3_123)

   * Reused component: SocialRepresentationProbe.
   * Why it transfers: Q123 needs standardized protocols for probing internal representations of AI systems for social concepts and roles.
   * What changes: the underlying models are artificial networks, but the observable mapping and tension evaluation follow Q090 style patterns.

---

## 9. TU roadmap and verification levels

This block explains the current verification level and the next measurable steps.

### 9.1 Current levels

* E_level: E1

  * Q090 defines a coherent effective layer encoding of the neural basis of social cognition.
  * Observables, tension functionals and a singular set S_sing are specified, but no empirical implementations are yet required.

* N_level: N1

  * The narrative connecting social brain structure, social prediction and social tension is explicit and internally coherent.
  * Cross problem links and reusable components are identified, but not yet supported by detailed quantitative case studies.

### 9.2 Next measurable step toward E2

To reach E2, at least one of the following must be realized:

1. A working analysis pipeline that takes non invasive measurements and behavioral data and outputs:

   * approximate SocialGraphField summaries,
   * DeltaS_soc_struct, DeltaS_soc_pred and Tension_SOC for a set of participants and tasks,
   * published distributions of tension values for typical and comparison groups.

2. A suite of experiments on artificial models where:

   * Q090 observables are implemented as functions over network internal states,
   * Tension_SOC is computed during social task simulations,
   * results are shared and reproduced by at least one independent group.

These steps operate only on observables and do not require revealing any deep Tension Universe mechanisms.

### 9.3 Long term role in the TU program

In the long term, Q090 is intended to:

1. Anchor the social cognition part of the neuroscience cluster as a structured node with precise tension observables.
2. Provide biologically informed but effective layer templates for designing AI agents with social reasoning abilities.
3. Connect to societal and governance problems by making it possible to move from individual social brain patterns to higher level social dynamics through explicit transfer components.

---

## 10. Elementary but precise explanation

This section explains Q090 for non specialists while keeping the description precise.

Social cognition is the collection of abilities that let a person understand other people. It includes:

* guessing what others think or feel,
* predicting how they might act,
* understanding social rules,
* keeping track of relationships and reputations.

The brain does not do this with a single point that says "social". Many brain areas work together in patterns that researchers call social brain networks.

In this entry we do not try to explain every detail of biology. Instead we ask a simpler but still precise question:

*Can we describe how well the social brain is working using a few observable quantities and a single number that measures social tension?*

We imagine that at any moment the brain is in a state `m`. For that state we look at:

* how active different social brain areas are,
* how strongly they influence each other,
* what kind of internal story the person has about self and others,
* how big the errors are when the person tries to predict other people.

From these pieces we build:

* a "SocialGraphField" that captures which areas are talking to which,
* a "social prediction error" summary,
* a combined social tension number `Tension_SOC(m)`.

If the brain structure and social predictions fit well together, `Tension_SOC(m)` is small. If they do not fit well, `Tension_SOC(m)` is large.

Then we describe two kinds of worlds.

* In a low tension world, many people can reach states where social tension is small across everyday situations. The social brain is robust and can adapt to change without breaking.
* In a high tension world, some brains are built or shaped in ways that make social tension stay high across important situations. Learning helps only a little and compensation is fragile.

This does not classify any real person. It does not diagnose any condition. It gives researchers and engineers:

* a way to talk about the neural basis of social cognition in terms of fields and tension,
* a clear target for experiments that test whether their models are reasonable,
* a reusable template for building and analyzing AI systems that need social understanding.

Q090 is therefore a structured, effective layer description of the neural basis of social cognition that others can test, extend and connect to different parts of the Tension Universe.
