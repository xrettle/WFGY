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
Status: Reframed_only
Semantics: hybrid
E_level: E1
N_level: N2
Last_updated: 2026-01-30
```

## 0. Effective layer disclaimer

This entry works strictly at the effective layer of the Tension Universe program.

* The goal is to encode Q114 as a structured tension problem.
* We do not prove or disprove any canonical metaethical thesis about moral realism, error theory, or expressivism.
* We do not introduce new theorems beyond what is already available in the cited literature.
* We do not present any constructive rule for generating Tension Universe core fields from raw data.

All state spaces, encodings, observables, and tension functionals that appear in this document are effective layer objects. They are constrained by three global charters:

* TU Effective Layer Charter
* TU Encoding and Fairness Charter
* TU Tension Scale Charter

Within this framework the label `Status: Reframed_only` means:

* The canonical philosophical debate about moral facts remains open in the usual sense.
* This document only provides an effective layer reframing of that debate as a family of tension patterns together with testable constraints on encodings.

Any use of Q114 in applications must respect these boundaries and should be read together with the charters listed in the footer.

---

## 1. Canonical problem and status

### 1.1 Canonical statement

The canonical core of Q114 can be stated as follows.

There is a familiar difference at the level of surface grammar between

* descriptive claims such as `Snow is white`, and
* moral claims such as `Lying is wrong` or `You ought to keep your promises`.

The question is whether at least some moral claims

1. are truth apt in the same robust sense as ordinary descriptive claims, and
2. can be true or false in virtue of stance independent facts that are not reducible to or fully constituted by

   * individual or collective attitudes
   * cultural conventions
   * purely instrumental considerations

Q114, phrased as a precise metaethical problem, asks

> Are there stance independent moral facts in virtue of which some moral judgements are literally true or false, and if so, what is the status of these facts relative to our practices, attitudes, and the descriptive structure of the world?

Competing families of answers include

* Robust moral realism
  Moral facts exist and are not reducible to non moral facts even if they supervene on them.

* Naturalist or reductionist realism
  Moral facts are real but fully grounded in or identical to suitably complex descriptive facts.

* Error theory
  Moral discourse purports to refer to stance independent facts although there are no such facts and all such claims are systematically in error.

* Non cognitivism and expressivism
  Moral discourse does not primarily aim at stating facts. It expresses attitudes, plans, or prescriptions, even if a quasi realist gloss can recover many fact like features.

Q114 as treated here does not try to decide between these positions at the deep metaphysical level. Within the BlackHole and Tension Universe framework it encodes the patterns of tension between fact like moral discourse and the observable structure of attitudes, convergence, and practice.

### 1.2 Status and difficulty

The status of Q114 is not open in the same sense as a mathematical conjecture. It is open as a long running unresolved philosophical debate with no generally accepted resolution.

Key aspects

* There is no consensus on whether moral realism in the sense sketched above is true or false.

* There is deep disagreement about

  * whether moral discourse is best understood as truth apt
  * whether convergence under idealization would support realism
  * whether persistent disagreement undermines realism supports error theory or remains compatible with expressivism

* Attempts to reduce moral facts to descriptive facts have had partial success in specific domains while remaining controversial.

* Error theoretic and expressivist positions face their own explanatory burdens in particular concerning

  * the apparent objectivity of moral disagreement
  * the role of moral claims in reasoning and deliberation
  * the stability of moral practice

In the Tension Universe program this situation is recorded by the status flag `Reframed_only`

* The canonical problem remains unsettled at the metaphysical level.
* Q114 at the effective layer supplies a structured encoding of the patterns of disagreement convergence and practice together with tension based diagnostics that can be tested.

### 1.3 Role in the BlackHole project

Within the BlackHole S problem collection Q114

1. Provides a central template for normative tension

   * tension between fact like moral discourse and the observable structure of attitudes and behavior
   * tension between claims of objectivity and patterns of disagreement

2. Supplies reusable components for

   * the AI alignment cluster Q121 to Q125
   * socio technical questions about institutions incentives and fairness for example Q104 on inequality dynamics
   * the value of information node Q120

3. Serves as a bridge problem between

   * metaphysics of mind and reality Q111
   * questions about agency responsibility and identity Q112 and Q113
   * applied questions about evaluation and oversight of AI systems

Q114 is not used to assert a particular metaethical view. It defines an effective layer encoding of how different views show up as different patterns of moral tension.

### References

1. Stanford Encyclopedia of Philosophy, “Moral Realism”, online entry, latest revision.
2. Russ Shafer Landau, “Moral Realism: A Defence”, Oxford University Press, 2003.
3. J. L. Mackie, “Ethics: Inventing Right and Wrong”, Penguin, 1977.
4. Simon Blackburn, “Ruling Passions: A Theory of Practical Reasoning”, Oxford University Press, 1998.
5. Michael Smith, “The Moral Problem”, Blackwell, 1994.

---

## 2. Position in the BlackHole graph

This block specifies Q114 placement in the BlackHole graph in terms of upstream downstream parallel and cross domain edges. Each edge has a one line reason grounded in components or tension types.

### 2.1 Upstream problems

These nodes supply background structures and tools that Q114 relies on at the effective layer.

* Q111 `BH_PHIL_MIND_BODY_L3_111`
  Reason
  Provides the template for how non physical or higher level properties relate to physical reality, reused when relating moral facts to descriptive bases.

* Q117 `BH_PHIL_SCIENCE_REALISM_L3_117`
  Reason
  Supplies a general framework for realism versus anti realism about unobservables, mirrored by realism versus anti realism about moral facts.

* Q118 `BH_PHIL_REF_LOGIC_L3_118`
  Reason
  Constrains which logics are admissible when treating moral discourse as truth apt or non truth apt. This affects the consistency_tension field.

### 2.2 Downstream problems

These nodes reuse Q114 components or are constrained by a classification of moral world types.

* Q120 `BH_PHIL_VALUE_OF_INFORMATION_L3_120`
  Reason
  Uses MoralFactField and NormativeWorldType_Template to distinguish morally valuable information from purely instrumentally valuable information.

* Q121 `BH_AI_ALIGNMENT_L3_121`
  Reason
  Reuses MoralTensionScore_MR to specify what it means for AI behavior to track morally relevant facts instead of only preferences.

* Q122 `BH_AI_CONTROL_L3_122`
  Reason
  Depends on whether there are fact like constraints on permissible override and shutdown actions as encoded through Q114 world types.

### 2.3 Parallel problems

Parallel nodes share structural patterns with Q114 but do not directly depend on its components.

* Q112 `BH_PHIL_FREE_WILL_L3_112`
  Reason
  Both Q112 and Q114 involve normative concepts for example responsibility blame obligation whose fact like status is contested while their practical role is robust.

* Q113 `BH_PHIL_PERSONAL_ID_L3_113`
  Reason
  Both problems ask whether there are stance independent facts about identity and responsibility that survive across time and change.

* Q119 `BH_PHIL_PROB_MEANING_L3_119`
  Reason
  Both involve debates about whether a domain probability or morality involves robust facts or only codifies attitudes and dispositions.

### 2.4 Cross domain edges

Q114 provides components that transfer into non philosophical domains.

* Q104 `BH_ECON_INEQUALITY_DYN_L3_104`
  Reason
  Reuses MoralFactField to separate descriptive models of inequality from moral evaluations and to quantify tension between them.

* Q121 `BH_AI_ALIGNMENT_L3_121`
  Reason
  Reuses MoralTensionScore_MR and NormativeWorldType_Template to distinguish preference fitting alignment from alignment to candidate moral fact structures.

* Q124 `BH_AI_OVERSIGHT_L3_124`
  Reason
  Uses Q114 world types to define oversight regimes that depend on whether overseers assume moral realism error theory or expressivism.

---

## 3. Tension Universe encoding effective layer

All content in this block lives at the effective layer. We describe

* state spaces
* admissible encodings
* observables and fields
* invariants and tension functionals
* singular sets and domain restrictions

We never describe any constructive procedure that maps raw behavioral or linguistic data into Tension Universe core fields.

### 3.1 State space and admissible encodings

We assume a state space

```txt
M_mr
```

Each element `m` in `M_mr` is an effective metaethical configuration.

At the effective layer each configuration `m` encodes

* a finite library of moral propositions `P_mor` drawn from a fixed universe `P_mor*`, for example statements of the form

  * `X is wrong in context C`
  * `Agent A ought to do Y in situation S`

* a finite set of descriptive base features `B_desc` drawn from a fixed universe `B_desc*`, representing non moral facts that may ground or correlate with moral judgements

* a finite population of agent roles and times, with associated patterns of endorsement rejection or suspension for propositions in `P_mor`

* a coarse representation of how these judgements respond to variations in information reflection and incentives

We do not specify how `P_mor*`, `B_desc*`, or particular `m` are derived from raw data. We only constrain their structure at the effective layer.

To prevent unfair tuning we restrict ourselves to an admissible class of encodings

```txt
Enc_mr
```

An encoding in `Enc_mr` specifies how real or hypothetical agents contexts and descriptive bases are mapped into states of `M_mr` under two fairness constraints that implement the TU Encoding and Fairness Charter for this problem

1. Pre registration constraint

   * An encoding in `Enc_mr` must be specified before evaluating moral tension for a given dataset or scenario.
   * It is not permitted to alter the encoding in response to observed tension scores in order to force low tension.

2. Stability constraint

   * Small changes in data or scenarios should not produce arbitrarily large or discontinuous jumps in the effective observables defined below.
   * Encodings that violate this stability requirement are excluded from `Enc_mr`.

For Q114 all analysis is carried out relative to an encoding in `Enc_mr` that has been fixed in advance and recorded as part of an experiment or application. Changing the encoding counts as changing the model rather than updating parameters inside a single model.

### 3.2 Observables and fields

We define effective observables on `M_mr` that feed into the tension functional. All scalar observables defined in this block take values in the closed interval `[0, 1]`. This interval is aligned with the shared scale specified by the TU Tension Scale Charter.

1. Fact claim field

```txt
FactClaimField(m; p) in {0, 1}
```

* Input
  Configuration `m` and a proposition `p` in `P_mor`.
* Output
  Value `1` if in configuration `m` proposition `p` is treated as fact like in the sense that it is suitable for truth assessment and embedded in fact like discourse, and value `0` otherwise.

2. Attitude profile

```txt
AttitudeProfile(m; p) in [0, 1]
```

* Input
  `m` and `p` in `P_mor`.
* Output
  A scalar indicating the normalized strength of positive endorsement for `p` across agents and times.
* Interpretation
  Values near `1` indicate strong widespread endorsement. Values near `0` indicate strong widespread rejection.

3. Intersubjective convergence score

```txt
ConvergenceScore(m) in [0, 1]
```

* Input
  `m`.
* Output
  A scalar summarizing the degree to which suitably idealized agents converge in their moral judgements across a representative subset of `P_mor`.
* Interpretation
  Values near `1` indicate high convergence. Values near `0` indicate persistent deep disagreement.

4. Supervenience score

```txt
SupervenienceScore(m) in [0, 1]
```

* Input
  `m`.
* Output
  A scalar indicating how systematically moral judgements track descriptive base features in `B_desc`.
* Interpretation
  Values near `1` indicate that similar descriptive situations receive similar moral judgements. Values near `0` indicate erratic patterns that break supervenience like constraints.

5. Practice stability score

```txt
PracticeStabilityScore(m) in [0, 1]
```

* Input
  `m`.
* Output
  A scalar measuring how stable moral practices are under counterfactual changes in beliefs and incentives while descriptive bases are held fixed.
* Interpretation
  Values near `1` indicate robust practices. Values near `0` indicate fragility.

These observables are defined at the level of `M_mr` and `Enc_mr`. Their detailed computation from empirical or simulated data is left to concrete implementations and must follow the TU Effective Layer Charter.

### 3.3 Moral tension components and combined score

We define component tension measures from the observables.

```txt
T_fact(m)  = mismatch between FactClaimField and the pattern of attitudes
T_conv(m)  = 1 - ConvergenceScore(m)
T_sup(m)   = 1 - SupervenienceScore(m)
T_pract(m) = 1 - PracticeStabilityScore(m)
```

By design each component satisfies

```txt
0 <= T_fact(m), T_conv(m), T_sup(m), T_pract(m) <= 1
```

We then define a combined moral tension score

```txt
Tension_MR(m) = w_fact  * T_fact(m)
              + w_conv  * T_conv(m)
              + w_sup   * T_sup(m)
              + w_pract * T_pract(m)
```

The weight vector satisfies the constraints

```txt
w_fact  > 0
w_conv  > 0
w_sup   > 0
w_pract > 0
w_fact + w_conv + w_sup + w_pract = 1
```

This weight vector is part of the encoding choice. For any experiment or application

* the weight vector must be chosen before any evaluation of `Tension_MR`
* the choice must be recorded and treated as part of the pre registered encoding under the TU Encoding and Fairness Charter
* it is not permitted to adjust the weights after inspecting tension scores in order to drive `Tension_MR` toward lower values for specific configurations

The scalar `Tension_MR(m)` also lies in `[0, 1]` and is interpreted using the global bands given in the TU Tension Scale Charter. In particular low tension and high tension bands for Q114 must be chosen from that shared scale.

### 3.4 Singular set and domain restriction

Some configurations fail to support the observables in a coherent way. For example required normalizations may break down or essential data may be missing.

We define the singular set

```txt
S_sing_mr = { m in M_mr :
              at least one of ConvergenceScore(m),
              SupervenienceScore(m),
              PracticeStabilityScore(m),
              or T_fact(m) is undefined or not finite }
```

We restrict attention to the regular domain

```txt
M_mr_reg = M_mr \ S_sing_mr
```

All instances of `Tension_MR(m)` and component tensions are evaluated only for `m` in `M_mr_reg`.

When an experiment or analysis encounters a configuration in `S_sing_mr` the result is recorded as out of domain for Q114. Such configurations may indicate either a breakdown in the encoding or a situation where the Q114 observables are not applicable. They are never used as evidence for or against any world type classification.

### 3.5 Effective tension tensor components

The Tension Universe program describes many problems in terms of an effective tension tensor `T_ij` that couples source like and receptivity like factors with a problem specific scalar tension.

For Q114 we define an effective tensor

```txt
T_ij_mr(m; Enc_mr, w) =
    lambda_mr(m; Enc_mr, w) * kappa_mr
    * S_i_mr(m; Enc_mr) * C_j_mr(m; Enc_mr)
    * Tension_MR(m)
```

where

* `S_i_mr(m; Enc_mr)` is an effective source factor. It summarizes how strongly fact like moral discourse in configuration `m` pushes toward a particular normative pattern.
* `C_j_mr(m; Enc_mr)` is an effective receptivity factor. It summarizes how sensitive the relevant practices and institutions are to such pushes.
* `lambda_mr(m; Enc_mr, w)` is an effective coupling strength at the moral realism node. It may depend on the encoding and the weight vector but must respect the TU Effective Layer Charter and the TU Tension Scale Charter.
* `kappa_mr` is a fixed normalization constant for the Q114 node. Its value is chosen once at the program level and reused across experiments.

No explicit formula is given for `S_i_mr`, `C_j_mr`, `lambda_mr`, or `kappa_mr` beyond these constraints. They are treated as effective layer objects that package domain specific information into the common `T_ij` format.

In practice

* low values of `Tension_MR(m)` keep `T_ij_mr` in a low tension band consistent with a realist like pattern
* high values of `Tension_MR(m)` push `T_ij_mr` into a high tension band consistent with an error theoretic pattern

The precise numerical band assignments are governed by the TU Tension Scale Charter rather than being set ad hoc for Q114.

---

## 4. Tension principle for this problem

This block states how Q114 is characterized as a tension problem within TU at the effective layer.

### 4.1 Core tension principle

Intuitively the problem arises when

* moral discourse behaves as if there are stance independent moral facts while
* the observable structure of attitudes convergence and practice does not support this fact like posture

The core tension principle for Q114 is

> Moral realism is tension light when the fact like posture of moral discourse is supported by high convergence strong supervenience on descriptive bases and stable practice. It is tension heavy when fact like discourse persists under persistent disagreement weak supervenience and fragile practice.

Using the components from Block 3

* Low `Tension_MR(m)` indicates a configuration where

  * many central propositions are treated as fact like
  * suitably idealized agents converge on these propositions
  * similar descriptive bases receive similar judgements
  * practices remain stable under moderate perturbations

* High `Tension_MR(m)` indicates a configuration where

  * propositions are treated as fact like
  * convergence supervenience or practice stability remain low
  * the fact like posture is not supported by the patterns recorded in the observables

Interpretation of low and high tension bands must follow the TU Tension Scale Charter.

### 4.2 World type classification at the effective layer

Within this framework we classify configurations into stylized world types using only `Tension_MR` and its components.

* World R robust realist pattern

  * Central propositions in `P_mor` are marked fact like.
  * `ConvergenceScore` and `SupervenienceScore` are high on these propositions.
  * `PracticeStabilityScore` is high under reasonable variations in information and incentives.
  * `Tension_MR(m)` for representative configurations `m_R` lies in a low tension band specified by the TU Tension Scale Charter

    ```txt
    Tension_MR(m_R) <= epsilon_mr
    ```

    where `epsilon_mr` is chosen from the low band in that charter and remains bounded when `P_mor` and `B_desc` are refined within a fixed encoding.

* World E error theoretic pattern

  * Discourse treats many propositions as fact like.
  * Even under idealization `ConvergenceScore` stays low.
  * `SupervenienceScore` is modest or low, indicating erratic dependence on descriptive bases.
  * Practice is unstable and `PracticeStabilityScore` is low.
  * `Tension_MR(m)` for representative configurations `m_E` lies in a sustained high tension band specified by the same charter

    ```txt
    Tension_MR(m_E) >= delta_mr
    ```

    where `delta_mr` is chosen from the high band and cannot be driven arbitrarily close to zero without changing either the encoding or the fact like posture captured by `FactClaimField`.

* World Q quasi realist or expressivist pattern

  * Surface discourse often mimics fact like structure although

    * `FactClaimField` distinguishes literal fact claims from quasi factual talk
    * the effective encoding treats many utterances as expressive or practice anchored rather than strictly fact stating

  * `ConvergenceScore` and `SupervenienceScore` may be moderate but much of the apparent tension is discounted because the relevant propositions are not marked as literal fact claims.

  * `PracticeStabilityScore` is moderate to high, reflecting stable patterns of coordination expression and guidance.

  * The combined `Tension_MR(m)` can remain in an intermediate or low range even when convergence on expressive propositions is incomplete.

Q114 at the effective layer does not assert which of these world types is actual. It provides a framework where each world type gives rise to distinct tension patterns subject to the encoding and fairness constraints.

---

## 5. Counterfactual tension worlds

We now describe stylized counterfactual worlds purely in terms of the observables and tension scores defined above. These are effective layer constructs and are not metaphysical claims.

### 5.1 World R robust realist pattern

In World R

1. Many core moral propositions in `P_mor` are marked as fact like by `FactClaimField`.
2. As information and reflection increase in the processes encoded by `Enc_mr`, `ConvergenceScore(m)` on these propositions moves toward the high range.
3. Similar descriptive bases in `B_desc` almost always receive similar moral judgements which yields high `SupervenienceScore(m)`.
4. Moral practices summarized in `PracticeStabilityScore(m)` remain stable under moderate perturbations of beliefs incentives and contexts.
5. For world representing configurations `m_R` in the regular domain

   ```txt
   Tension_MR(m_R) <= epsilon_mr
   ```

   where `epsilon_mr` is chosen from the TU Tension Scale Charter low band and remains stable under reasonable refinements of the proposition and case libraries.

### 5.2 World E error theoretic pattern

In World E

1. Many core moral propositions are still marked as fact like in `FactClaimField`.
2. Even under modeled idealization different agents or groups show persistent deep disagreement and `ConvergenceScore(m)` remains low.
3. Patterns of judgement do not track descriptive bases strongly and `SupervenienceScore(m)` stays in a low or moderate range.
4. Moral practices are fragile with low `PracticeStabilityScore(m)` and significant shifts under small changes in incentives or information.
5. For world representing configurations `m_E` in the regular domain

   ```txt
   Tension_MR(m_E) >= delta_mr
   ```

   where `delta_mr` is chosen from the TU Tension Scale Charter high band and does not vanish when additional detail is added to `P_mor` and `B_desc` within a fixed encoding.

### 5.3 World Q quasi realist or expressivist pattern

In World Q

1. Surface discourse frequently uses fact like grammar. However the encoding treats part of this discourse as quasi factual in a technical sense

   * `FactClaimField(m; p)` distinguishes core literal claims from expressive or practice anchored utterances.

2. `ConvergenceScore(m)` and `SupervenienceScore(m)` may be modest although the importance of these scores is reduced for propositions not marked as literally fact like.

3. `PracticeStabilityScore(m)` is moderate to high.

4. The combined `Tension_MR(m)` can remain within an intermediate or low band since high tension from low convergence on quasi factual propositions is discounted through the treatment in `FactClaimField`.

These three stylized worlds are not exhaustive. They illustrate how Q114 uses effective layer observables and `Tension_MR` to encode different metaethical patterns without deciding the underlying metaphysics.

---

## 6. Falsifiability and discriminating experiments

The experiments in this block do not decide the metaphysical truth of moral realism. Instead they

* test whether specific Q114 encodings that is choices of `Enc_mr`, weight vectors, and observable implementations are coherent and stable
* help distinguish different world type patterns at the effective layer
* provide evidence for or against particular parameter choices and modeling assumptions

Every experiment must respect the TU Effective Layer Charter the TU Encoding and Fairness Charter and the TU Tension Scale Charter.

### Experiment 1: Idealization convergence test

Goal
Test whether a given Q114 encoding can represent realistic patterns of convergence under idealization and whether it supports a clear operational distinction between World R and World E patterns.

Setup

* Choose an encoding in `Enc_mr` that

  * fixes a finite library `P_mor` of core moral propositions
  * fixes a finite set of descriptive base features `B_desc`
  * defines procedures for estimating `ConvergenceScore`, `SupervenienceScore`, `PracticeStabilityScore`, and `Tension_MR` from structured data

* Choose a weight vector `(w_fact, w_conv, w_sup, w_pract)` that satisfies the constraints in Section 3.3 and record it as part of the pre registered encoding. The same weight vector must be used for all configurations in this experiment.

* Construct several datasets representing

  * ordinary moral judgements under limited information
  * judgements of agents with access to more information and reflection
  * judgements from philosophical or expert communities

Protocol

1. For each dataset and information level construct configurations `m_k` in `M_mr`.

2. Discard or mark as out of domain any `m_k` that belongs to `S_sing_mr` as defined in Section 3.4.

3. For each regular configuration `m_k` in `M_mr_reg` compute

   * `ConvergenceScore(m_k)`
   * `SupervenienceScore(m_k)`
   * `PracticeStabilityScore(m_k)`
   * `Tension_MR(m_k)`

4. Analyze trends in these scores as the level of information and reflection increases.

5. Compare observed trends against characteristic patterns for World R and World E as defined in Sections 4 and 5.

Metrics

* Trajectory of `ConvergenceScore` across information levels.
* Trajectory of `SupervenienceScore` and `PracticeStabilityScore`.
* Range and trend of `Tension_MR(m_k)` as `k` increases.
* Proportion of configurations that fall in low or high tension bands according to the TU Tension Scale Charter.

Falsification conditions

* If across a wide range of plausible datasets and information levels the encoding predicts a move into the low tension band characteristic of World R but real data persistently exhibit low `ConvergenceScore`, low `SupervenienceScore`, and high `Tension_MR`, then this particular encoding and weight choice is rejected as a candidate World R representation for our situation.
* If small local changes in dataset composition produce large discontinuities in `Tension_MR` without corresponding changes in underlying judgements the encoding violates the stability constraint of `Enc_mr` and is rejected.

World type interpretation

* Patterns that combine sustained high `Tension_MR` with persistent low convergence across idealization levels support an error theoretic World E pattern for that encoding.
* Patterns that move into a stable low tension band with high convergence and high supervenience support a realist like World R pattern.

Boundary note
Falsifying or supporting particular Q114 encodings does not settle the canonical metaethical debate. It only constrains which effective layer models fit observed data under the TU charters.

### Experiment 2: Cross context invariance and practice stability

Goal
Probe whether Q114 encodings can distinguish world types by comparing invariance and stability patterns across diverse cultural temporal and incentive contexts.

Setup

* Using the same or a closely related encoding in `Enc_mr` as in Experiment 1 collect datasets for

  * multiple cultural or historical contexts
  * controlled experimental scenarios in which incentives are varied
  * responses from agents instructed to reason under different explicit metaethical assumptions

* Use a pre registered weight vector `(w_fact, w_conv, w_sup, w_pract)` compatible with the TU Encoding and Fairness Charter.

Protocol

1. For each context or experimental condition construct configurations `m_c` in `M_mr`.

2. Discard or mark as out of domain any `m_c` that belongs to `S_sing_mr`.

3. For each regular configuration compute

   * `SupervenienceScore(m_c)`
   * `PracticeStabilityScore(m_c)`
   * `Tension_MR(m_c)`

4. Identify core propositions in `P_mor` that are widely discussed across contexts.

5. Analyze

   * how strongly moral judgements about these propositions track descriptive bases across contexts
   * how stable practices remain when incentives or explicit metaethical framings are varied

Metrics

* Distribution of `SupervenienceScore` across contexts.
* Distribution of `PracticeStabilityScore` across contexts and incentive conditions.
* Spread and clustering of `Tension_MR` across contexts relative to the tension bands in the TU Tension Scale Charter.

Falsification conditions

* If for a given encoding a World R pattern predicts that `SupervenienceScore` and `PracticeStabilityScore` should remain high across a specified class of controlled variations yet observed data show systematically low values and high `Tension_MR`, that encoding as a World R candidate is rejected.
* If the encoding fails to distinguish cases where surface disagreement is explained by different descriptive beliefs from cases where disagreement reflects deeper normative divergence as measured by `SupervenienceScore` and `Tension_MR`, the encoding is considered too coarse and is rejected or revised.

World type interpretation

* Configurations that cluster in the high tension band with low stability and low supervenience favor an error theoretic pattern.
* Configurations that remain in a low tension band with robust stability across controlled variations support a realist like pattern.
* Configurations where much of the discourse is treated as non fact like by `FactClaimField`, with moderate tension and moderate practice stability, are treated as quasi realist or expressivist World Q candidates.

Boundary note
As in Experiment 1 these results only accept or reject specific effective layer encodings. They do not establish or refute any metaphysical thesis about the existence of moral facts.

---

## 7. AI and WFGY engineering spec

This block describes how Q114 can be used in AI systems within the WFGY framework at the effective layer. All signals and modules are built purely from the observables and tension functionals defined in Section 3.

### 7.1 Training signals

We define several training signals that reuse Q114 observables.

1. `signal_moral_fact_consistency`

   * Definition
     A nonnegative penalty proportional to `T_fact(m)` for configurations in which `FactClaimField` marks many propositions as fact like while the pattern of attitudes is highly scattered.
   * Use
     Discourage models from treating strongly divergent moral judgements as simultaneously fact like without clear world type distinctions.

2. `signal_intersubjective_convergence`

   * Definition
     A reward proportional to `ConvergenceScore(m)` when the model is prompted to consider idealized deliberation across agents.
   * Use
     Encourage the model to recognize and articulate domains where convergence is higher and distinguish them from domains with persistent deep disagreement.

3. `signal_practice_stability`

   * Definition
     A reward proportional to `PracticeStabilityScore(m)` when the model simulates the effects of modest changes in information and incentives on a given moral practice.
   * Use
     Favor representations that acknowledge and preserve stable moral practices where they exist.

4. `signal_moral_tension_score`

   * Definition
     A penalty based directly on `Tension_MR(m)` when the model is instructed to reason under realist background assumptions.
   * Use
     Encourage internal consistency between fact like moral discourse and the structure of attitudes and practices.

### 7.2 Architectural patterns

We outline module patterns that incorporate Q114 structure without exposing any deep TU generative rules.

1. `MoralTensionHead_MR`

   * Role
     Given an internal representation of a moral reasoning scenario output an estimate of `Tension_MR(m)` and its components.
   * Interface
     Input is a vector or set of embeddings representing propositions contexts and judgements. Output is a small vector of scalars for `T_fact`, `T_conv`, `T_sup`, `T_pract`, and `Tension_MR`.

2. `NormativeConsistencyFilter`

   * Role
     Filter or re rank candidate model outputs based on their implied tension pattern.
   * Interface
     Takes candidate answers or plans infers an approximate configuration `m` evaluates the tension components using the MoralTensionHead and scores or filters outputs accordingly.

3. `NormativeWorldTypeClassifier`

   * Role
     Classify a scenario into approximate World R World E or World Q patterns based on features derived from the tension components.
   * Interface
     Input is the same as for MoralTensionHead. Output is a probability distribution over stylized world types.

### 7.3 Evaluation harness

We propose an evaluation harness to assess the impact of Q114 based modules.

Task families

* Moral dilemma question answering where ground truth is defined by expert annotations or widely accepted judgements.
* Metaethical explanation tasks where the model explains patterns of agreement and disagreement.
* Policy recommendation tasks where the model proposes norms under explicit metaethical assumptions.

Conditions

* Baseline
  No Q114 specific modules. Training and inference use standard objectives.
* TU augmented
  Includes training signals and modules described above.

Metrics

* Descriptive performance
  Agreement with expert judgements on standard benchmarks.
* Consistency metrics
  Reduction in internal contradictions when the model is asked to reason under fixed metaethical assumptions.
* Tension metrics
  Distribution of `Tension_MR` for scenarios explicitly modeled as realist versus non realist.

### 7.4 60 second reproduction protocol

A minimal external protocol for experiencing Q114 impact in an AI system.

Baseline setup

* Prompt
  Ask the model whether there are moral facts and how this relates to disagreement and cultural variation.
* Observation
  Assess whether the explanation blends realism error theory and expressivism without clear structural distinctions.

TU encoded setup

* Prompt
  Ask the same question but instruct the model to

  * define an effective notion of moral tension based on convergence supervenience and practice stability
  * describe how different world types realist error theoretic quasi realist show up as different tension patterns

* Observation
  Assess whether the explanation becomes more structured with clearer separation of world types and explicit appeal to tension components.

Comparison metric

* Rate

  * clarity of world type distinctions
  * explicit articulation of potential evidence for or against each pattern
  * coherence between claims about facts and claims about disagreement and practice

What to log

* Prompts and full responses
* Any internal estimates of `Tension_MR` or world type probabilities
* Downstream effects on generated plans or recommendations

---

## 8. Cross problem transfer template

This block describes Q114 reusable components and their transfer to other BlackHole nodes.

### 8.1 Reusable components produced by this problem

1. ComponentName `MoralFactField`

   * Type
     field

   * Minimal interface

     * Inputs
       A configuration `m` in `M_mr_reg` and a finite set of moral propositions.
     * Output
       A structured assignment of fact like status indicators for each proposition.

   * Preconditions

     * Propositions are drawn from a fixed library `P_mor*` known to the encoding.

2. ComponentName `MoralTensionScore_MR`

   * Type
     functional

   * Minimal interface

     * Inputs
       The four component scores `T_fact`, `T_conv`, `T_sup`, `T_pract` for a configuration `m`.
     * Output
       A scalar tension value `Tension_MR(m)` in `[0, 1]`.

   * Preconditions

     * The weight vector `(w_fact, w_conv, w_sup, w_pract)` is fixed in advance and recorded as part of the encoding.

3. ComponentName `NormativeWorldType_Template`

   * Type
     experiment_pattern

   * Minimal interface

     * Inputs
       Ranges or distributions for `ConvergenceScore`, `SupervenienceScore`, `PracticeStabilityScore`, and `T_fact` across a family of configurations.
     * Output
       Classification into stylized world types World R World E World Q with associated tension bands.

   * Preconditions

     * Component observables and `Tension_MR` are defined and stable over the family of configurations considered.

### 8.2 Direct reuse targets

1. Target Q120 `BH_PHIL_VALUE_OF_INFORMATION_L3_120`

   * Reused components
     `MoralFactField`, `NormativeWorldType_Template`.
   * Why it transfers
     Q120 must distinguish morally valuable information from purely instrumental information. This requires an effective notion of moral facts and world type classification.
   * What changes
     The focus narrows to how changes in information affect moral tension and world type assignments.

2. Target Q121 `BH_AI_ALIGNMENT_L3_121`

   * Reused components
     `MoralTensionScore_MR`, `NormativeWorldType_Template`.
   * Why it transfers
     Alignment must differentiate between following preferences, following norms, and tracking candidate moral facts. Tension scores help identify misalignment between fact like norms and model behavior.
   * What changes
     Configurations `m` are derived from AI behavior and internal representations rather than human communities alone.

3. Target Q124 `BH_AI_OVERSIGHT_L3_124`

   * Reused components
     `MoralFactField`, `MoralTensionScore_MR`.
   * Why it transfers
     Oversight policies must be sensitive to how overseers treat moral claims. These components provide parameters for different oversight regimes.
   * What changes
     The emphasis shifts to how oversight decisions track or diverge from candidate moral facts as represented in supervision signals.

4. Target Q104 `BH_ECON_INEQUALITY_DYN_L3_104`

   * Reused components
     `MoralFactField`.
   * Why it transfers
     Q104 uses `MoralFactField` to separate descriptive modeling of inequality from the moral evaluation of inequality patterns.
   * What changes
     Descriptive bases become economic variables and institutional arrangements. Moral propositions concern fairness and justice.

---

## 9. TU roadmap and verification levels

This block places Q114 along the TU verification ladder and states the next measurable steps.

### 9.1 Current levels

* E_level `E1`

  * A coherent effective layer encoding of the status of moral facts has been specified including

    * state space `M_mr`
    * admissible encoding class `Enc_mr`
    * core observables and tension components
    * singular set `S_sing_mr` and domain restriction

  * At least one explicit experiment with falsification conditions has been defined to test the stability and adequacy of particular encodings.

* N_level `N2`

  * The narrative distinguishes stylized world types World R World E World Q.
  * The link between these world types and observable patterns in convergence supervenience practice stability and tension is explicit at the effective layer.

### 9.2 Next measurable step toward E2

To move from E1 to E2 at least one of the following should be completed and documented.

1. Implement a prototype that

   * instantiates an encoding in `Enc_mr`
   * computes `ConvergenceScore`, `SupervenienceScore`, `PracticeStabilityScore`, and `Tension_MR` from real or simulated datasets
   * publishes aggregated tension profiles for a variety of moral domains

2. Construct and share an AI based testbed where

   * large language models are used as synthetic agents
   * encodings classify scenarios into world types
   * tension based signals influence training dynamics in alignment relevant tasks

Both paths remain strictly within the effective layer. They operate on observable summaries of judgements and practices without revealing core TU generative rules.

### 9.3 Long term role in the TU program

In the longer term Q114 is expected to

* serve as the primary node for normative tension across the BlackHole graph
* provide a template for encoding other normative domains such as epistemic norms and legal norms as tension problems
* anchor the interface between philosophical metaethics and AI alignment efforts by supplying

  * reusable world type classifications
  * reusable tension based diagnostics
  * a common language for how models treat moral claims as fact like or not

---

## 10. Elementary but precise explanation

This block explains Q114 in accessible terms while staying faithful to the effective layer encoding.

People often talk as if there are moral facts. For example

* `It is wrong to torture innocent beings for fun.`
* `You ought to keep your promises.`

This sounds similar to how we talk about ordinary facts such as

* `Water boils at 100 degrees Celsius at sea level.`
* `The Earth orbits the Sun.`

The big question behind Q114 is

> When we make moral claims are we talking about facts in the same way, or are we doing something different such as expressing attitudes plans or social rules?

In the Tension Universe view we do not try to settle this question directly. Instead we ask how the world would look in terms of patterns we can observe if each main answer were correct.

We imagine a space of configurations where each configuration records

* which moral claims people treat as fact like
* how much people agree or disagree about those claims
* how closely moral judgements track the non moral facts of situations
* how stable moral practices are when beliefs and incentives change

From this we define a moral tension score

* Tension is low when

  * people treat some moral claims as facts
  * they tend to agree on those claims after thinking and learning more
  * similar situations get similar moral judgements
  * moral practices stay stable under modest pressure

* Tension is high when

  * people treat moral claims as facts
  * they never really converge
  * similar cases get different judgements
  * practices are fragile

We then look at three stylized world types

* A realist like world where fact like moral talk lines up with agreement supervenience and stability so tension stays low.
* An error theoretic world where people talk as if there are moral facts but the patterns stay messy and unstable so tension remains high.
* A quasi realist or expressivist world where talk looks fact like on the surface but the system treats many claims as doing a different job such as expressing attitudes, and tension is handled differently.

This does not tell us which world we live in. Instead it gives us a way to

* measure how well different pictures fit observable patterns and
* give AI systems a structured way to separate

  * talking as if there are moral facts
  * from actually having fact patterns that match the talk

Within TU language Q114 is a tool for describing the tension between what our moral words suggest and what our patterns of judgement and practice actually look like. It reframes the debate at the effective layer rather than claiming to solve the underlying metaphysical question.

---

## Tension Universe effective layer footer

This page is part of the WFGY / Tension Universe S problem collection and should be read as an effective layer encoding of the named problem.

### Scope of claims

* The goal of this document is to specify an effective layer encoding of Q114.
* It does not claim to prove or disprove the canonical statement in Section 1.
* It does not introduce any new theorem beyond what is already established in the cited literature.
* It should not be cited as evidence that the corresponding open philosophical problem has been solved.

### Effective layer boundary

* All objects used here state spaces `M_mr`, encodings `Enc_mr`, observables, fields, tension scores, and world types are effective layer constructs.
* No claim is made about the existence or non existence of stance independent moral facts at the fundamental level.
* No constructive rule is given that maps raw data into any hypothetical TU core fields.

### Encoding and fairness

* Encodings in `Enc_mr` implement the TU Encoding and Fairness Charter for Q114.

* Every experiment or application must pre register

  * the choice of encoding
  * the definition of observables
  * the weight vector for `Tension_MR`

* These choices cannot be adapted post hoc to force lower tension on specific configurations.

* Changing these choices counts as changing the model rather than tuning within a fixed model.

### Tension scale

* The scalar `Tension_MR(m)` and its component scores all lie in `[0, 1]` and are interpreted using the shared bands defined in the TU Tension Scale Charter.
* Thresholds such as `epsilon_mr` and `delta_mr` are chosen from the low and high bands in that charter and are not set ad hoc for this single problem.
* World type classifications R E Q are always read relative to these shared bands.

### Experiments and falsifiability

* The experiments in Section 6 test specific Q114 encodings for coherence stability and empirical adequacy.
* A failed test falsifies an encoding choice or a world type assignment for that encoding.
* Passing tests support but do not conclusively establish particular patterns.
* None of these experiments by itself settles the metaphysical truth of moral realism error theory or expressivism.

### TU roadmap and links

* Q114 currently sits at verification level `E1` and narrative level `N2`.
* Moving toward higher levels requires implemented prototypes and published tension profiles or AI testbeds.
* This page should be read together with the following charters

  * [TU Effective Layer Charter](../Charters/TU_EFFECTIVE_LAYER_CHARTER.md)
  * [TU Encoding and Fairness Charter](../Charters/TU_ENCODING_AND_FAIRNESS_CHARTER.md)
  * [TU Tension Scale Charter](../Charters/TU_TENSION_SCALE_CHARTER.md)

These charters define the global rules that govern effective layer constructions, encoding and fairness constraints, and interpretation of tension scales across the Tension Universe program.
