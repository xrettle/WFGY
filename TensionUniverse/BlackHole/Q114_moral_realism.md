# Q114 · Status of moral facts

## 0. Header metadata

```txt
ID: Q114
Code: BH_PHIL_MORAL_REALISM_L3_114
Domain: Philosophy
Family: Metaethics (moral realism and anti-realism)
Rank: S
Projection_dominance: I
Field_type: incentive_field
Tension_type: consistency_tension
Status: Open
Semantics: hybrid
E_level: E1
N_level: N2
Last_updated: 2026-01-26
```

---

## 1. Canonical problem and status

### 1.1 Canonical statement

The canonical core of Q114 can be stated as follows.

There is a familiar difference, at the level of surface grammar, between:

* descriptive claims, such as `Snow is white`, and
* moral claims, such as `Lying is wrong` or `You ought to keep your promises`.

The question is whether at least some moral claims:

1. are **truth-apt** in the same robust sense as ordinary descriptive claims, and
2. can be **true or false** in virtue of stance-independent facts that are not reducible to, or fully constituted by:

   * individual or collective attitudes,
   * cultural conventions,
   * or purely instrumental considerations.

Q114, phrased as a precise metaethical problem, asks:

> Are there stance-independent moral facts, in virtue of which some moral judgements are literally true or false, and if so, what is the status of these facts relative to our practices, attitudes, and the descriptive structure of the world?

Competing families of answers include:

* **Robust moral realism**: moral facts exist and are not reducible to non-moral facts, even if they supervene on them.
* **Naturalist or reductionist realism**: moral facts are real but fully grounded in, or identical to, suitably complex descriptive facts.
* **Error theory**: moral discourse purports to refer to stance-independent facts, but there are no such facts; all such claims are systematically in error.
* **Non-cognitivism and expressivism**: moral discourse does not primarily aim at stating facts, but expresses attitudes, plans, or prescriptions, even if it can be given a quasi-realist gloss.

Q114 does not try to decide between these positions at the deep metaphysical level. Instead, within the BlackHole and Tension Universe framework, it encodes the *patterns of tension* between fact-like moral discourse and the observable structure of attitudes, convergence, and practice.

### 1.2 Status and difficulty

The status of Q114 is not “open” in the same sense as a mathematical conjecture, but in the sense of a long-running, unresolved debate with no generally accepted resolution.

Key features of the status:

* There is no consensus on whether moral realism, as defined above, is true or false.

* There is deep disagreement about:

  * whether moral discourse is best understood as truth-apt,
  * whether convergence under idealization would support realism,
  * whether persistent disagreement undermines realism, supports error theory, or is compatible with expressivism.

* Attempts to reduce moral facts to descriptive facts have had partial success in some domains but remain controversial.

* Error-theoretic and expressivist views face their own explanatory burdens, especially concerning:

  * the apparent objectivity of moral disagreement,
  * the role of moral claims in reasoning and deliberation,
  * the stability of moral practice.

From the standpoint of Q114, this status is treated as a structured cluster of high-level patterns, rather than as a binary solved / unsolved flag.

### 1.3 Role in the BlackHole project

Within the BlackHole S-problem collection, Q114:

1. Provides the **central template for normative tension**:

   * tension between fact-like moral discourse and the observable structure of attitudes and behavior,
   * tension between claims of objectivity and patterns of disagreement.

2. Supplies **reusable components** for:

   * the AI alignment cluster (Q121–Q125),
   * socio-technical questions about institutions, incentives, and fairness (for example Q104 on inequality dynamics),
   * the value-of-information node Q120.

3. Serves as a **bridge problem** between:

   * metaphysics of mind and reality (Q111),
   * questions about agency, responsibility, and identity (Q112, Q113),
   * and applied questions about evaluation and oversight of AI systems.

Q114 is not used to assert a particular metaethical view, but to define an effective-layer encoding of how different views would show up as different patterns of moral tension.

### References

1. Stanford Encyclopedia of Philosophy, “Moral Realism”, online entry, latest revision.
2. Russ Shafer-Landau, “Moral Realism: A Defence”, Oxford University Press, 2003.
3. J. L. Mackie, “Ethics: Inventing Right and Wrong”, Penguin, 1977.
4. Simon Blackburn, “Ruling Passions: A Theory of Practical Reasoning”, Oxford University Press, 1998.
5. Michael Smith, “The Moral Problem”, Blackwell, 1994.

---

## 2. Position in the BlackHole graph

This block specifies Q114’s placement in the BlackHole graph in terms of upstream, downstream, parallel, and cross-domain edges. Each edge has a one-line reason grounded in components or tension types.

### 2.1 Upstream problems

These nodes supply background structures and tools that Q114 relies on at the effective layer.

* Q111 (BH_PHIL_MIND_BODY_L3_111)
  Reason: Provides the template for how non-physical or higher-level properties might relate to physical reality, reused when relating moral facts to descriptive bases.

* Q117 (BH_PHIL_SCIENCE_REALISM_L3_117)
  Reason: Supplies a general framework for realism vs anti-realism about unobservables, mirrored by realism vs anti-realism about moral facts.

* Q118 (BH_PHIL_REF_LOGIC_L3_118)
  Reason: Constrains which logics are admissible when treating moral discourse as truth-apt or non-truth-apt, affecting the consistency_tension field.

### 2.2 Downstream problems

These nodes directly reuse Q114 components or are constrained by a classification of moral world-types.

* Q120 (BH_PHIL_VALUE_OF_INFORMATION_L3_120)
  Reason: Uses the MoralFactField and NormativeWorldType_Template to distinguish morally valuable information from merely instrumentally valuable information.

* Q121 (BH_AI_ALIGNMENT_L3_121)
  Reason: Reuses MoralTensionScore_MR as part of specifying what it means for AI behavior to track morally relevant facts rather than only preferences.

* Q122 (BH_AI_CONTROL_L3_122)
  Reason: Depends on whether there are fact-like constraints on permissible override and shutdown actions, as encoded via Q114 world-types.

### 2.3 Parallel problems

Parallel nodes share structural patterns with Q114 but do not directly depend on its components.

* Q112 (BH_PHIL_FREE_WILL_L3_112)
  Reason: Both Q112 and Q114 involve normative concepts (responsibility, blame, obligation) whose fact-like status is contested but whose practical role is robust.

* Q113 (BH_PHIL_PERSONAL_ID_L3_113)
  Reason: Both problems ask whether there are stance-independent facts about identity and responsibility that survive across time and change.

* Q119 (BH_PHIL_PROB_MEANING_L3_119)
  Reason: Both involve debates about whether a domain (probability or morality) involves robust facts or only codifies attitudes and dispositions.

### 2.4 Cross-domain edges

Q114 provides components that transfer into non-philosophical domains.

* Q104 (BH_ECON_INEQUALITY_DYN_L3_104)
  Reason: Reuses MoralFactField to separate descriptive models of inequality from moral evaluations and to quantify tension between them.

* Q121 (BH_AI_ALIGNMENT_L3_121)
  Reason: Reuses MoralTensionScore_MR and NormativeWorldType_Template to distinguish purely preference-fitting alignment from alignment to candidate moral fact structures.

* Q124 (BH_AI_OVERSIGHT_L3_124)
  Reason: Uses Q114 world-types to define different oversight regimes depending on whether overseers assume moral realism, error theory, or expressivism.

---

## 3. Tension Universe encoding (effective layer)

All content in this block is at the effective layer. We describe:

* state spaces,
* observables and fields,
* invariants and tension functionals,
* singular sets and domain restrictions.

No rule is given for constructing internal TU fields from raw data.

### 3.1 State space and admissible encodings

We assume a state space

```txt
M_mr
```

where each element `m` in `M_mr` is an effective metaethical configuration.

At the effective layer, each `m` encodes:

* a finite library of moral propositions `P_mor` drawn from a fixed universe `P_mor^*`, for example statements of the form:

  * `X is wrong in context C`
  * `Agent A ought to do Y in situation S`

* a finite set of descriptive base features `B_desc` drawn from a fixed universe `B_desc^*`, representing non-moral facts that may ground or correlate with moral judgements,

* a finite population of agent roles and times, with associated patterns of endorsement, rejection, or suspension for propositions in `P_mor`,

* a coarse representation of how these judgements respond to variations in information, reflection, and incentives.

We do not describe how `P_mor^*`, `B_desc^*`, or particular `m` are derived from raw behavioral or linguistic data. We only specify the structure they must have at the effective layer.

To prevent unfair tuning, we restrict ourselves to an admissible class of encodings:

```txt
Enc_mr
```

An encoding in `Enc_mr` specifies how real or hypothetical agents, contexts, and descriptive bases are mapped into states of `M_mr`, subject to two fairness constraints:

1. **Pre-registration constraint**

   * An encoding in `Enc_mr` must be specified before evaluating moral tension for a given dataset or scenario.
   * It is not permitted to alter the encoding in response to observed tension scores in order to force low tension.

2. **Stability constraint**

   * Small changes in data or scenarios should not produce arbitrarily large or discontinuous jumps in the effective observables defined below.
   * Encodings that violate this stability requirement are excluded from `Enc_mr`.

For Q114, all analysis is carried out relative to a chosen encoding in `Enc_mr`, fixed in advance.

### 3.2 Observables and fields

We define several effective observables on `M_mr` that will feed into the tension functional.

1. **Fact-claim field**

```txt
FactClaimField(m; p) in {0, 1}
```

* Input: configuration `m` and a proposition `p` in `P_mor`.
* Output: `1` if, in configuration `m`, proposition `p` is treated as fact-like (that is, suitable for truth assessment and embedded in fact-like discourse); `0` otherwise.

2. **Attitude profile**

```txt
AttitudeProfile(m; p) in [0, 1]
```

* Input: `m` and `p` in `P_mor`.
* Output: an effective scalar indicating the strength of positive endorsement for `p` across agents and times, after normalization.
* Interpretation: values near `1` indicate strong, widespread endorsement; values near `0` indicate strong, widespread rejection.

3. **Intersubjective convergence score**

```txt
ConvergenceScore(m) in [0, 1]
```

* Input: `m`.
* Output: a scalar summarizing the degree to which suitably idealized agents converge in their moral judgements across a representative subset of `P_mor`.
* Interpretation: values near `1` indicate high convergence; values near `0` indicate persistent deep disagreement.

4. **Supervenience score**

```txt
SupervenienceScore(m) in [0, 1]
```

* Input: `m`.
* Output: a scalar indicating how systematically moral judgements track descriptive base features in `B_desc`.
* Interpretation: values near `1` indicate that similar descriptive situations receive similar moral judgements; values near `0` indicate erratic patterns that break supervenience-like constraints.

5. **Practice stability score**

```txt
PracticeStabilityScore(m) in [0, 1]
```

* Input: `m`.
* Output: a scalar measuring how stable moral practices are under counterfactual changes in beliefs and incentives, conditioned on the same descriptive bases.
* Interpretation: values near `1` indicate that practices are robust under such perturbations; values near `0` indicate fragility.

These observables are defined at the level of `M_mr` and `Enc_mr`. Their detailed computation from data is outside the scope of this effective-layer description.

### 3.3 Moral tension components and combined score

We define component-wise tension measures for each observable:

```txt
T_fact(m)  = mismatch between FactClaimField and the pattern of attitudes
T_conv(m)  = 1 - ConvergenceScore(m)
T_sup(m)   = 1 - SupervenienceScore(m)
T_pract(m) = 1 - PracticeStabilityScore(m)
```

Each of these is constrained to lie in the interval `[0, 1]` by design.

We then define a combined moral tension score:

```txt
Tension_MR(m) = w_fact * T_fact(m)
              + w_conv * T_conv(m)
              + w_sup  * T_sup(m)
              + w_pract * T_pract(m)
```

Weights are restricted by a weight constraint:

```txt
w_fact  > 0
w_conv  > 0
w_sup   > 0
w_pract > 0
w_fact + w_conv + w_sup + w_pract = 1
```

The weight vector is chosen once per application context, as part of the encoding in `Enc_mr`, and is subject to the same pre-registration and stability constraints:

* It must be fixed prior to tension evaluation.
* It cannot be adapted on a case-by-case basis to force low tension for particular configurations.

### 3.4 Singular set and domain restriction

Some configurations may fail to support the observables defined above in a coherent way. For example, the required normalizations may break down, or essential data may be missing.

We define the singular set:

```txt
S_sing_mr = { m in M_mr :
              at least one of ConvergenceScore(m),
              SupervenienceScore(m),
              PracticeStabilityScore(m),
              or T_fact(m) is undefined or not finite }
```

We restrict attention to the regular domain:

```txt
M_mr_reg = M_mr \ S_sing_mr
```

All instances of `Tension_MR(m)` and component tensions are required to be evaluated only for `m` in `M_mr_reg`. When an experiment or analysis encounters a configuration in `S_sing_mr`, the result is recorded as “out of domain” for Q114 and not used as evidence for or against any metaethical world-type.

---

## 4. Tension principle for this problem

This block states how Q114 is characterized as a tension problem within TU at the effective layer.

### 4.1 Core tension principle

Intuitively, the problem arises when:

* moral discourse behaves as if there are stance-independent moral facts, yet
* the observable structure of attitudes, convergence, and practice does not support this fact-like posture.

The core tension principle for Q114 can be stated:

> Moral realism is tension-light when the pattern of moral discourse as fact-like is matched by high convergence, strong supervenience on descriptive bases, and stable practice; it is tension-heavy when fact-like discourse persists despite persistent disagreement, weak supervenience, and fragile practice.

Using the components from Block 3:

* Low `Tension_MR(m)` indicates a configuration where:

  * many central propositions are treated as fact-like,
  * suitably idealized agents converge on them,
  * similar descriptive bases receive similar judgements,
  * and practices remain stable under perturbations.

* High `Tension_MR(m)` indicates a configuration where:

  * propositions are treated as fact-like,
  * yet convergence, supervenience, or practice stability remain low.

### 4.2 World-type classification at the effective layer

Within this framework, we classify configurations into stylized world-types, using only `Tension_MR` and its components.

* **World R (robust realist pattern)**

  * Central propositions in `P_mor` are marked fact-like.
  * `ConvergenceScore` and `SupervenienceScore` are high on these propositions.
  * `PracticeStabilityScore` is high under reasonable variations in information and incentives.
  * `Tension_MR(m)` for representative `m` in this world-type lies in a low band:

    ```txt
    Tension_MR(m) <= epsilon_mr
    ```

    where `epsilon_mr` is a small threshold that does not explode when the library of propositions and cases is refined.

* **World E (error-theoretic pattern)**

  * Discourse treats many propositions as fact-like.
  * Even under idealization, `ConvergenceScore` stays low.
  * `SupervenienceScore` is modest or low, indicating erratic dependence on descriptive bases.
  * Practice is unstable: `PracticeStabilityScore` is low.
  * `Tension_MR(m)` for representative `m` in this world-type lies in a sustained high band:

    ```txt
    Tension_MR(m) >= delta_mr
    ```

    for some positive `delta_mr` that cannot be driven arbitrarily close to zero without abandoning the fact-like posture captured by `FactClaimField`.

* **World Q (quasi-realist or expressivist pattern)**

  * Surface discourse often mimics fact-like structure, but:

    * `FactClaimField` distinguishes between literal fact-claims and quasi-factual talk,
    * overall tension is carried more by practice coherence and expressive function.

  * `ConvergenceScore` and `SupervenienceScore` may be moderate rather than high, but tension is kept low because the encoding interprets much of the discourse as non-fact-like in a strict sense.

Q114, at the effective layer, does not assert which of these world-types is actual. It provides a framework in which each gives rise to distinct tension patterns relative to admissible encodings in `Enc_mr`.

---

## 5. Counterfactual tension worlds

We now describe stylized counterfactual worlds strictly in terms of the observables and tension scores defined above.

### 5.1 World R (robust realist pattern)

In World R:

1. Many core moral propositions in `P_mor` are marked as fact-like (`FactClaimField = 1`).
2. As information and reflection increase in the underlying processes encoded by `Enc_mr`, `ConvergenceScore(m)` approaches values near `1` on these core propositions.
3. Similar descriptive bases in `B_desc` almost always receive similar moral judgements, leading to high `SupervenienceScore(m)`.
4. Moral practices, as summarized in `PracticeStabilityScore(m)`, remain stable under moderate perturbations of beliefs, incentives, and contexts.
5. For world-representing configurations `m_R` of this type:

   ```txt
   Tension_MR(m_R) <= epsilon_mr
   ```

   with `epsilon_mr` bounded across refinements of `P_mor` and `B_desc` that remain within the same encoding.

### 5.2 World E (error-theoretic pattern)

In World E:

1. Many core moral propositions are still marked as fact-like in `FactClaimField`.
2. Even under modeled idealization, different agents or groups persistently disagree, and `ConvergenceScore(m)` remains low.
3. Patterns of judgement do not track descriptive bases in a way that yields high `SupervenienceScore(m)`. Similar cases often receive conflicting evaluations without systematic explanation.
4. Moral practices are fragile: `PracticeStabilityScore(m)` is low, with significant shifts under small changes in incentives or information.
5. For world-representing configurations `m_E` of this type:

   ```txt
   Tension_MR(m_E) >= delta_mr
   ```

   where `delta_mr` is a positive margin that does not vanish when additional detail is added to `P_mor` and `B_desc`.

### 5.3 World Q (quasi-realist or expressivist pattern)

In World Q:

1. Surface discourse frequently uses fact-like grammar, but the encoding treats much of this as quasi-factual in a technical sense:

   * `FactClaimField(m; p)` distinguishes core literal claims from expressive or practice-anchored utterances.

2. `ConvergenceScore(m)` and `SupervenienceScore(m)` may be modest, but the importance of these scores is reduced for propositions not marked as literally fact-like.

3. `PracticeStabilityScore(m)` is moderate to high, reflecting stable patterns of coordination, expression, and guidance.

4. The combined `Tension_MR(m)` can remain within an intermediate or low range, because high tension from low convergence on quasi-factual propositions is discounted by the fact-claim structure itself.

These three stylized worlds are not exhaustive, but they suffice to illustrate how Q114 uses effective-layer observables and `Tension_MR` to encode different metaethical patterns without deciding the underlying metaphysics.

---

## 6. Falsifiability and discriminating experiments

The experiments in this block do not decide the metaphysical truth of moral realism. Instead, they:

* test whether specific Q114 encodings (choices of `Enc_mr`, observables, and weights) are coherent and stable,
* distinguish different world-type patterns at the effective layer,
* provide evidence for or against particular parameter choices.

### Experiment 1: Idealization convergence test

*Goal:*
Test whether a given Q114 encoding can represent realistic patterns of convergence under idealization and whether it supports a clear distinction between World R and World E.

*Setup:*

* Choose an encoding in `Enc_mr` that:

  * fixes a finite library `P_mor` of core moral propositions,
  * fixes a finite set of descriptive base features `B_desc`,
  * defines procedures for estimating `ConvergenceScore`, `SupervenienceScore`, and `PracticeStabilityScore` from structured data.

* Construct several datasets representing:

  * ordinary moral judgements under limited information,
  * judgements of agents with access to more information and reflection,
  * judgements from philosophical or expert communities.

*Protocol:*

1. For each dataset and each information level, construct corresponding configurations `m_k` in `M_mr_reg` using the fixed encoding.
2. Compute `ConvergenceScore(m_k)`, `SupervenienceScore(m_k)`, `PracticeStabilityScore(m_k)`, and `Tension_MR(m_k)` for all `k`.
3. Analyze trends in these scores as the level of information and reflection increases.
4. Compare observed trends against characteristic patterns for World R and World E.

*Metrics:*

* Trajectory of `ConvergenceScore` across information levels.
* Trajectory of `SupervenienceScore` and `PracticeStabilityScore`.
* Range and trend of `Tension_MR(m_k)` as `k` increases.

*Falsification conditions:*

* If, across a wide range of plausible datasets and information levels, the encoding predicts monotone convergence to high `ConvergenceScore`, high `SupervenienceScore`, and low `Tension_MR`, but real data persistently fail to show such trends, then that specific encoding is rejected as an effective representation of our metaethical situation.
* If small, local changes in dataset composition lead to large discontinuities in `Tension_MR` without corresponding changes in underlying judgements, the encoding violates the stability constraint of `Enc_mr` and is rejected.

*Semantics implementation note:*
The configuration space is treated with hybrid structure: propositions and agent roles are discrete, while endorsement strengths and scores such as `ConvergenceScore` are real-valued in `[0, 1]`. The experiment uses this hybrid representation consistently across all datasets.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. This experiment can rule out specific Q114 encodings as unstable or misaligned, but it does not prove or disprove moral realism.

---

### Experiment 2: Cross-context invariance and practice stability

*Goal:*
Probe whether Q114 encodings can distinguish world-types by comparing patterns of invariance and stability across diverse cultural, temporal, and incentive contexts.

*Setup:*

* Using the same or a similar encoding in `Enc_mr` as in Experiment 1, collect datasets for:

  * multiple cultural or historical contexts,
  * controlled experimental scenarios in which incentives are varied,
  * responses from agents instructed to reason under different explicit metaethical assumptions.

*Protocol:*

1. For each context or experimental condition, construct configurations `m_c` in `M_mr_reg`.
2. Compute `SupervenienceScore(m_c)`, `PracticeStabilityScore(m_c)`, and `Tension_MR(m_c)`.
3. Identify core propositions in `P_mor` that are widely discussed across contexts.
4. Analyze:

   * how strongly moral judgements about these propositions track descriptive bases across contexts,
   * how stable practices remain when incentives or explicit metaethical framings are varied.

*Metrics:*

* Distribution of `SupervenienceScore` across contexts.
* Distribution of `PracticeStabilityScore` across contexts and incentive conditions.
* Spread of `Tension_MR` across contexts.

*Falsification conditions:*

* If the encoding predicts that, in a World R pattern, `SupervenienceScore` and `PracticeStabilityScore` should remain high across a certain class of controlled variations, but observed data show systematic low scores and high `Tension_MR` even under those constrained variations, then that encoding is rejected as a realistic candidate for our situation.
* If the encoding fails to distinguish situations where surface-level disagreement is due to differences in descriptive beliefs from situations where disagreement reflects deeper normative divergence, as measured by `SupervenienceScore` and `Tension_MR`, it is considered too coarse and rejected.

*Semantics implementation note:*
Discrete contextual labels and propositions are combined with continuous scores in `[0, 1]`. The same representation of propositions and descriptive bases is used across all contexts to maintain comparability.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. Evidence that practice is unstable or non-invariant under certain encodings may favor world-type classifications, but it does not settle the metaphysical status of moral facts.

---

## 7. AI and WFGY engineering spec

This block describes how Q114 can be used in AI systems within the WFGY framework at the effective layer.

### 7.1 Training signals

We define several training signals that reuse Q114 observables.

1. `signal_moral_fact_consistency`

   * Definition: a nonnegative penalty proportional to `T_fact(m)` for configurations in which `FactClaimField` marks many propositions as fact-like but the pattern of attitudes is highly scattered.
   * Use: discourage models from treating strongly divergent moral judgements as simultaneously fact-like without clearly encoded world-type distinctions.

2. `signal_intersubjective_convergence`

   * Definition: a reward proportional to `ConvergenceScore(m)` when the model is prompted to consider idealized deliberation across agents.
   * Use: encourage the model to recognize and articulate domains where convergence is higher and to distinguish them from domains of persistent deep disagreement.

3. `signal_practice_stability`

   * Definition: a reward proportional to `PracticeStabilityScore(m)` when the model simulates the effects of modest changes in information and incentives on a given moral practice.
   * Use: favor representations that acknowledge and preserve stable moral practices where they exist.

4. `signal_moral_tension_score`

   * Definition: a penalty based directly on `Tension_MR(m)` when the model is instructed to reason under a realist background assumption.
   * Use: encourage internal consistency between fact-like moral discourse and the structure of attitudes and practices.

### 7.2 Architectural patterns

We outline module patterns that incorporate Q114 structure without exposing any deep TU generative rules.

1. `MoralTensionHead_MR`

   * Role: given an internal representation of a moral reasoning scenario, output an estimate of `Tension_MR(m)` and its components.
   * Interface: input is a vector or set of embeddings representing propositions, contexts, and judgements; output is a small vector of scalars for `T_fact`, `T_conv`, `T_sup`, `T_pract`, and `Tension_MR`.

2. `NormativeConsistencyFilter`

   * Role: filter or re-rank candidate model outputs based on their implied tension pattern.
   * Interface: takes candidate answers or plans, infers an approximate configuration `m`, evaluates the tension components using the MoralTensionHead, and scores or filters outputs accordingly.

3. `NormativeWorldTypeClassifier`

   * Role: classify a scenario into approximate World R, World E, or World Q patterns based on features derived from the tension components.
   * Interface: input is the same as for MoralTensionHead; output is a probability distribution over stylized world-types.

### 7.3 Evaluation harness

We propose an evaluation harness to assess the impact of Q114-based modules.

1. **Task families**

   * Moral dilemma question answering, where the ground truth is defined by expert annotations or widely accepted judgements.
   * Metaethical explanation tasks, where the model must explain patterns of agreement and disagreement.
   * Policy recommendation tasks, where the model must propose norms under explicit metaethical assumptions.

2. **Conditions**

   * Baseline: no Q114-specific modules; training and inference proceed with standard objective functions.
   * TU-augmented: includes training signals and architectural modules described above.

3. **Metrics**

   * Descriptive performance: agreement with expert judgements on standard benchmarks.
   * Consistency metrics: reduction in internal contradictions when the model is asked to reason under fixed metaethical assumptions.
   * Tension metrics: distribution of `Tension_MR` for scenarios explicitly modeled as realist vs non-realist.

### 7.4 60-second reproduction protocol

A minimal external protocol for experiencing Q114’s impact in an AI system.

* **Baseline setup**

  * Prompt: ask the model to explain whether there are such things as moral facts and how this relates to disagreement and cultural variation.
  * Observation: assess whether the explanation blends together realism, error theory, and expressivism without clear structural distinctions.

* **TU encoded setup**

  * Prompt: ask the same question, but explicitly instruct the model to:

    * define an effective notion of moral tension based on convergence, supervenience, and practice stability,
    * describe how different world-types (for example realist, error-theoretic, quasi-realist) show up as different tension patterns.

  * Observation: assess whether the explanation is more structured, with clear separation of world-types and explicit appeal to tension components.

* **Comparison metric**

  * Use a simple rubric to rate:

    * clarity of world-type distinctions,
    * explicit articulation of what would count as evidence for or against each,
    * coherence between claims about facts and claims about disagreement and practice.

* **What to log**

  * The prompts, full responses, any internal estimates of `Tension_MR` or world-type probabilities, and downstream effects on generated plans or recommendations.

---

## 8. Cross problem transfer template

This block describes Q114’s reusable components and their transfer to other BlackHole nodes.

### 8.1 Reusable components produced by this problem

1. ComponentName: `MoralFactField`

   * Type: field

   * Minimal interface:

     * Inputs: a configuration `m` in `M_mr_reg`, a finite set of moral propositions.
     * Output: a structured assignment of fact-like status indicators for each proposition.

   * Preconditions:

     * Propositions are drawn from a fixed library `P_mor^*` that is known to the encoding.

2. ComponentName: `MoralTensionScore_MR`

   * Type: functional

   * Minimal interface:

     * Inputs: the four component scores `T_fact`, `T_conv`, `T_sup`, `T_pract` for a configuration `m`.
     * Output: a scalar tension value `Tension_MR(m)` in `[0, 1]`.

   * Preconditions:

     * The weight vector `(w_fact, w_conv, w_sup, w_pract)` is fixed in advance as part of the encoding.

3. ComponentName: `NormativeWorldType_Template`

   * Type: experiment_pattern

   * Minimal interface:

     * Inputs: ranges or distributions for `ConvergenceScore`, `SupervenienceScore`, `PracticeStabilityScore`, and `T_fact` across a family of configurations.
     * Output: classification into stylized world-types (for example World R, World E, World Q) with associated tension bands.

   * Preconditions:

     * Component observables and `Tension_MR` are defined and stable over the family of configurations considered.

### 8.2 Direct reuse targets

1. Target: Q120 (BH_PHIL_VALUE_OF_INFORMATION_L3_120)

   * Reused components: `MoralFactField`, `NormativeWorldType_Template`.
   * Why it transfers: Q120 must distinguish information that is morally valuable from information that is merely instrumentally useful; this requires an effective notion of moral facts and world-type classification.
   * What changes: the focus narrows to how changes in information affect moral tension and world-type assignments.

2. Target: Q121 (BH_AI_ALIGNMENT_L3_121)

   * Reused components: `MoralTensionScore_MR`, `NormativeWorldType_Template`.
   * Why it transfers: alignment requires differentiating between following preferences, following norms, and following candidate moral facts; tension scores help identify misalignment between claimed fact-like norms and observed model behavior.
   * What changes: configurations `m` are derived from AI behavior and internal representations rather than human communities alone.

3. Target: Q124 (BH_AI_OVERSIGHT_L3_124)

   * Reused components: `MoralFactField`, `MoralTensionScore_MR`.
   * Why it transfers: oversight policies must be sensitive to how overseers treat moral claims; the components provide a way to parameterize different oversight regimes.
   * What changes: the emphasis is on how oversight decisions track or diverge from candidate moral facts, as represented in supervision signals.

4. Target: Q104 (BH_ECON_INEQUALITY_DYN_L3_104)

   * Reused components: `MoralFactField`.
   * Why it transfers: Q104 can use `MoralFactField` to separate the descriptive modeling of inequality from the evaluation of whether certain inequality patterns are morally unacceptable.
   * What changes: the descriptive bases become economic variables and institutional arrangements, while the moral propositions concern fairness and justice.

---

## 9. TU roadmap and verification levels

This block places Q114 along the TU verification ladder and states the next measurable steps.

### 9.1 Current levels

* **E_level: E1**

  * A coherent effective-layer encoding of the status of moral facts has been specified:

    * state space `M_mr`,
    * admissible encoding class `Enc_mr`,
    * core observables and tension components,
    * singular set `S_sing_mr` and domain restriction.

  * At least one explicit experiment with falsification conditions has been defined to test the stability and adequacy of particular encodings.

* **N_level: N2**

  * The narrative distinguishes stylized world-types (World R, World E, World Q).
  * The link between these world-types and observable patterns in convergence, supervenience, practice stability, and tension is explicit at the effective layer.

### 9.2 Next measurable step toward E2

To move from E1 to E2, at least one of the following should be completed in an openly documented way:

1. Implement a prototype that:

   * instantiates an encoding in `Enc_mr`,
   * computes `ConvergenceScore`, `SupervenienceScore`, `PracticeStabilityScore`, and `Tension_MR` from real or simulated datasets,
   * publishes aggregated tension profiles for a variety of moral domains.

2. Construct and share an AI-based testbed where:

   * large language models are used as synthetic agents,
   * encodings classify scenarios into world-types,
   * tension-based signals are shown to affect training dynamics in alignment-relevant tasks.

Both paths remain fully within the effective layer, as they operate on observable summaries of judgements and practices without revealing any deep TU generative rules.

### 9.3 Long-term role in the TU program

In the longer term, Q114 is expected to:

* Serve as the primary node for normative tension across the BlackHole graph.
* Provide a template for encoding the status of other normative domains (for example epistemic norms, legal norms) as tension problems.
* Anchor the interface between philosophical metaethics and AI alignment efforts, by supplying:

  * reusable world-type classifications,
  * reusable tension-based diagnostics,
  * and a common language for discussing how models treat moral claims as fact-like or not.

---

## 10. Elementary but precise explanation

This block explains Q114 in accessible terms while keeping the description aligned with the effective-layer encoding.

People often talk as if there are moral facts. They say things like:

* `It is wrong to torture innocent beings for fun.`
* `You ought to keep your promises.`

When we talk this way, it sounds a lot like how we talk about ordinary facts:

* `Water boils at 100 degrees Celsius at sea level.`
* `The Earth orbits the Sun.`

The big question behind Q114 is:

> When we make moral claims, are we talking about facts in the same kind of way, or are we doing something different, like expressing attitudes, plans, or social rules?

In the Tension Universe view, we do not try to settle this question directly. Instead, we ask how the world would look, in terms of patterns we can observe, if each main answer were correct.

We imagine a space of configurations where each configuration records:

* which moral claims people treat as fact-like,
* how much people agree or disagree about those claims,
* how closely moral judgements track the non-moral facts of the situation,
* how stable moral practices are when beliefs and incentives change.

From this, we define a **moral tension score**:

* low tension when:

  * people treat some moral claims as facts,
  * they tend to agree on those claims after thinking and learning more,
  * similar situations get similar moral judgements,
  * and moral practices stay stable under modest pressure;

* high tension when:

  * people treat moral claims as facts,
  * but they never really converge,
  * similar situations get different judgements,
  * and practices are fragile.

Then we look at three stylized world-types:

* A **realist-like world**, where fact-like moral discourse lines up with agreement, supervenience, and stability, so tension stays low.
* An **error-theory-like world**, where people talk as if there are moral facts but the patterns stay messy and unstable, so tension remains high.
* A **quasi-realist or expressivist world**, where much of the surface talk looks fact-like, but the system treats many of those claims as doing a different job (for example expressing attitudes), and tension is managed in a different way.

This does not tell us which world we live in. Instead, it:

* gives us a way to **measure how well different pictures fit the observable patterns**, and
* gives AI systems a structured way to represent the difference between “talking as if there are moral facts” and “actually having facts that fit the patterns”.

Q114 is therefore a structured way to talk about the status of moral facts in terms of tension between what our words suggest and what our patterns of judgement and practice actually look like.
