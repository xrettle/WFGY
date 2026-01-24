# Q035 · Exact quantum metrology limits

## 0. Header metadata

```txt
ID: Q035
Code: BH_PHYS_QMETROLOGY_LIMIT_L3_035
Domain: Physics
Family: Quantum metrology and precision measurement
Rank: S
Projection_dominance: P
Field_type: dynamical_field
Tension_type: consistency_tension
Status: Partial
Semantics: continuous
E_level: E1
N_level: N1
Last_updated: 2026-01-24
````

---

## 1. Canonical problem and status

### 1.1 Canonical statement

Quantum metrology studies how precisely one can estimate physical parameters using quantum systems and measurements. Typical tasks include estimating:

* a phase shift in an interferometer,
* a frequency or energy splitting,
* a small field strength,
* a time delay or propagation constant.

In each task, there are constraints on the available resources, such as:

* number of probes `N`,
* total interrogation time `T`,
* average energy or photon number `E`,
* access to entanglement, coherence, or ancillary systems,
* noise model and environment (for example dephasing, loss, thermal noise).

Classical metrology leads to the so called standard quantum limit (SNL), where the mean squared error scales as

`error ~ 1 / sqrt(R_eff)`

for an appropriate effective resource measure `R_eff` (for example `R_eff = N`). Under ideal conditions and carefully prepared entangled states, quantum metrology can in principle achieve Heisenberg-like scaling

`error ~ 1 / R_eff`

when all relevant resources are accounted for.

The canonical question addressed by Q035 at the effective layer is:

> Given a well specified parameter estimation task, a resource budget, and a noise model, what are the exact achievable limits on estimation precision, and how can we encode the tension between claimed protocols and those limits in a way that is stable, falsifiable, and transferable?

This includes:

* defining effective resource metrics and error measures,
* encoding known or conjectured lower bounds on error in terms of those resources,
* characterizing when apparent violations (for example “super-Heisenberg” scaling) are genuine or artifacts of incomplete resource accounting.

### 1.2 Status and difficulty

Several major results in quantum estimation theory establish bounds on estimation error using tools such as:

* quantum Fisher information (QFI),
* classical Fisher information (CFI),
* quantum Cramer Rao inequalities,
* geometric distances on the space of quantum states.

For many standard single parameter models with simple noise, the optimal asymptotic scaling is known and can sometimes be achieved by explicit protocols. However, there remain significant challenges:

* multi parameter estimation with incompatible observables,
* complex noise models and decoherence,
* adaptive and sequential strategies,
* full accounting of all physical resources (including control pulses, ancillas, and error correction overhead),
* regimes where entanglement and nonclassical states provide advantages that are subtle to quantify.

The difficulty is not only to derive abstract bounds, but to encode them in a way that:

* is robust under changed modeling assumptions,
* does not allow hidden resource redefinitions,
* can be used across domains as a reusable template for “limits under constraints”.

### 1.3 Role in the BlackHole project

Within the BlackHole S problem collection, Q035 plays several roles:

1. It is the primary node for translating “fundamental limits on quantum parameter estimation” into a structured consistency tension between resources, noise, and error statistics.
2. It provides a template for how to encode limit statements in other domains (for example computation, thermodynamics, AI probing) using similar resource vs performance structures.
3. It acts as a bridge between theoretical quantum estimation results and practical questions such as:

   * when can a claimed metrological advantage be trusted,
   * how to interpret “beating the Heisenberg limit” under full resource accounting,
   * how to compare different experimental designs in a unified tension framework.

### References

1. V. Giovannetti, S. Lloyd, L. Maccone, “Quantum Metrology”, Physical Review Letters 96, 010401 (2006).
2. V. Giovannetti, S. Lloyd, L. Maccone, “Advances in quantum metrology”, Nature Photonics 5, 222–229 (2011).
3. M. G. A. Paris, “Quantum estimation for quantum technology”, International Journal of Quantum Information 7, 125–137 (2009).
4. L. Pezze, A. Smerzi, M. K. Oberthaler, R. Schmied, P. Treutlein, “Quantum metrology with nonclassical states of atomic ensembles”, Reviews of Modern Physics 90, 035005 (2018).

---

## 2. Position in the BlackHole graph

This block locates Q035 within the BlackHole graph. Each edge is given with a one line reason referring to concrete components or tension types. All references are internal Q identifiers.

### 2.1 Upstream problems

These problems provide prerequisites or general frameworks that Q035 depends on at the effective layer.

* Q021 (BH_PHYS_QG_L3_021)
  Reason: Supplies a framework for how quantum fields and spacetime resources are defined at high energy scales, which constrains how extreme metrology tasks must count resources.

* Q032 (BH_PHYS_QTHERMO_L3_032)
  Reason: Provides thermodynamic resource concepts such as work, entropy production, and coherence, which feed directly into Q035 resource metrics and cost functions.

* Q034 (BH_PHYS_QCLASS_CROSSOVER_L3_034)
  Reason: Encodes how quantum behavior degrades to classical limits under noise and coarse graining, a key ingredient in defining standard quantum limits.

* Q031 (BH_PHYS_EFT_GRAV_BREAK_L3_031)
  Reason: Gives bounds on the validity of effective field theories, which restrict the regime where metrological claims about fundamental constants can be made.

### 2.2 Downstream problems

These problems reuse Q035 components or treat Q035 as a prerequisite.

* Q036 (BH_PHYS_HIGH_TC_MECH_L3_036)
  Reason: Uses Q035 resource and limit encoding to bound how precisely microscopic parameters can be inferred from noisy condensed matter experiments.

* Q059 (BH_CS_INFO_THERMODYN_L3_059)
  Reason: Reuses Q035 style “precision vs cost” metrics when studying the tradeoff between information gain and thermodynamic expenditure.

* Q061 (BH_CHEM_REACTION_PATHWAYS_L3_061)
  Reason: Depends on Q035 to quantify how accurately reaction parameters can be estimated before attempting fine grained quantum control of chemical reactions.

* Q123 (BH_AI_INTERP_L3_123)
  Reason: Uses Q035 metrology style probing as a template for assessing how well internal AI representations can be resolved under bounded compute and data.

### 2.3 Parallel problems

Parallel nodes share similar structure and tension types but do not depend directly on Q035 components.

* Q032 (BH_PHYS_QTHERMO_L3_032)
  Reason: Both Q032 and Q035 encode resource vs performance limits, but in thermodynamic work extraction and parameter estimation respectively.

* Q034 (BH_PHYS_QCLASS_CROSSOVER_L3_034)
  Reason: Both study how quantum advantages shrink toward classical behavior as noise and scale increase, viewed through different observables.

* Q039 (BH_PHYS_QTURBULENCE_L3_039)
  Reason: In both problems, complex many body fields create a gap between microscopic quantum description and coarse grained observables that must be reconciled.

### 2.4 Cross domain edges

Cross domain edges point to problems in other domains that reuse Q035 components.

* Q051 (BH_CS_COMP_LIMITS_L3_051)
  Reason: Reuses Q035’s limit encoding methodology for computation, translating resource vs error tradeoffs into time, energy, and precision constraints.

* Q059 (BH_CS_INFO_THERMODYN_L3_059)
  Reason: Shares the same “precision vs cost” structure, borrowing Q035 style resource measures and tension scores.

* Q101 (BH_SOC_MACRO_FORECAST_L3_101)
  Reason: Treats macro level forecasting as a noisy parameter estimation problem, importing Q035 style limits into social and economic observables.

* Q123 (BH_AI_INTERP_L3_123)
  Reason: Applies metrological notions of probing internal AI structures with fixed resource budgets, with Q035 providing the core template.

---

## 3. Tension Universe encoding (effective layer)

All content in this block is at the effective layer. We describe only:

* state spaces,
* observables and fields,
* invariants and tension scores,
* singular sets and domain restrictions.

We do not describe any hidden generative rule or explicit mapping from raw laboratory data to internal TU fields.

### 3.1 State space

We define an effective state space

```txt
M_35
```

Elements `m` in `M_35` are interpreted as “quantum metrology experiment configurations” at the level needed for tension analysis. For each `m`, the encoding exposes the following effective components:

* A parameter label `theta` to be estimated.

* A resource tuple

  ```txt
  R = (N, T, E)
  ```

  where:

  * `N` is an effective probe number,
  * `T` is an effective interrogation time,
  * `E` is an effective energy or signal strength measure.

* A noise label `noise(m)` taken from a fixed finite noise set

  ```txt
  Noise_set = { noiseless, dephasing, loss, thermal, composite }
  ```

* An experiment strategy label `strategy(m)` that identifies:

  * a probe state class (for example coherent, GHZ like, spin squeezed),
  * a measurement class (for example photon counting, homodyne, collective spin readout),
  * a data processing rule.

We do not specify how any of these components are constructed or implemented. We only assume that for each physically meaningful scenario in the intended scope, there exists at least one `m` in `M_35` that encodes it.

### 3.2 Finite reference library and admissible encoding class

We define a finite reference library

```txt
L_Q35 = { scenario_1, scenario_2, ..., scenario_K }
```

Each `scenario_k` is a labeled combination of:

* a parameter type and target value,
* a resource budget range,
* a noise model from `Noise_set`,
* a strategy template (for example coherent state interferometry, GHZ metrology, spin squeezing plus adaptive readout).

The library `L_Q35` is fixed in advance for Q035 and is not allowed to change after any experiment has been evaluated.

An admissible encoding class `E_Q35` is defined as the set of all maps from `L_Q35` into tuples

```txt
(R_eff, error_stat, qfi_stat, noise_label, strategy_label)
```

such that:

1. `R_eff` is computed from the underlying physical description using a fixed, scenario independent rule. For example:

   ```txt
   R_eff = N
   R_eff = N * T
   R_eff = N * E
   ```

   for a predetermined choice among a small finite set.

2. `error_stat` is a scalar or low dimensional vector summarizing estimation error for the parameter `theta` in that scenario. It must be based on standard error measures such as mean squared error, not tuned post hoc to match a desired limit.

3. `qfi_stat` is a summary of the quantum Fisher information or a related bound for the given scenario.

4. `noise_label` is taken from `Noise_set`.

5. `strategy_label` identifies the strategy class from a fixed finite list.

Fairness constraints for `E_Q35`:

* The rule that determines `R_eff`, `error_stat`, and `qfi_stat` must be fixed before any tension evaluation is performed.
* It is forbidden to change `R_eff` or redefine error measures after observing whether a scenario appears to beat a limit.
* Encodings that depend on outcomes of `error_stat` to choose `R_eff` are not in `E_Q35`.

All effective tension analysis in Q035 is restricted to encodings in `E_Q35`.

### 3.3 Observables and fields

We introduce the following effective observables on `M_35` for admissible encodings.

1. Effective resource metric

```txt
R_eff(m) >= 0
```

* A scalar resource measure derived from `R = (N, T, E)` and the noise label via a fixed rule.
* Examples include `R_eff = N`, `R_eff = N * T`, or a weighted sum that reflects total physical cost.

2. Error observable

```txt
error(m) >= 0
```

* A scalar summarizing the estimation error for `theta` under the strategy encoded in `m`.
* Typically a mean squared error or a similar one dimensional measure.

3. Quantum Fisher information summary

```txt
QFI(m) >= 0
```

* A scalar or effective scalar derived from the quantum Fisher information for the probe and noise model encoded in `m`.

4. Classical Fisher information summary

```txt
CFI(m) >= 0
```

* A scalar or effective scalar derived from the classical statistics of measurement outcomes under the strategy encoded in `m`.

5. Scaling exponent estimator

For a scenario `scenario_k` realized at multiple resource levels

```txt
R_eff(m_1), R_eff(m_2), ..., R_eff(m_L)
```

with corresponding errors

```txt
error(m_1), error(m_2), ..., error(m_L)
```

we define a scaling exponent estimate

```txt
alpha(m_1, ..., m_L)
```

obtained by fitting a model of the form

```txt
error ~ c / (R_eff ^ alpha)
```

over a finite set of resource levels. The precise fitting procedure is part of the encoding design and is fixed in advance.

### 3.4 Limit references and invariants

We choose a finite family of reference limit functions

```txt
Limit_family = { Limit_SNL, Limit_HL, Limit_noise_1, ..., Limit_noise_J }
```

Each `Limit_j(R_eff)` is a nonnegative function on the nonnegative reals, representing a theoretically justified lower bound on `error` for a given noise class and resource definition.

Examples include:

* `Limit_SNL(R_eff) = c_1 / sqrt(R_eff)` for standard quantum limit behavior.
* `Limit_HL(R_eff) = c_2 / R_eff` for Heisenberg like scaling under ideal conditions.
* `Limit_noise_j(R_eff)` capturing decoherence limited scaling.

For each state `m` in `M_35` with noise label `noise(m)`, we select an appropriate limit function

```txt
Limit_Q35(m; R_eff) in Limit_family
```

according to fixed rules determined by `noise(m)` and `strategy_label`.

We then define a main mismatch observable

```txt
DeltaS_Q35_limit(m) = max( 0, error(m) - Limit_Q35(m; R_eff(m)) )
```

which measures by how much the observed or encoded error exceeds the selected limit.

Additional invariants:

1. Scaling stability invariant

For a set of states representing a single scenario at multiple resource levels, we define

```txt
I_scaling = | alpha(m_1, ..., m_L) - alpha_ref |
```

where `alpha_ref` is a reference exponent associated with the chosen limit function (for example `alpha_ref = 1/2` for SNL or `alpha_ref = 1` for HL).

2. Resource fairness invariant

We define

```txt
I_resource = |R_eff(m) - R_base(m)|
```

where `R_base(m)` is a baseline resource estimate derived from a simplified physical model. Large or inconsistent deviations across similar scenarios signal resource accounting anomalies.

### 3.5 Singular set and domain restrictions

Some configurations lead to ill defined or divergent observables. We define a singular set

```txt
S_sing_35 = { m in M_35 :
              QFI(m) is undefined or infinite
              or error(m) is undefined or infinite
              or R_eff(m) is undefined or not finite }
```

The regular domain is

```txt
M_35_reg = M_35 \ S_sing_35
```

Rules:

* All tension functionals and invariants in Q035 are only evaluated on `M_35_reg`.
* When a protocol description leads to a state in `S_sing_35`, this is treated as “out of domain”, not as evidence for or against the physical limits themselves.

---

## 4. Tension principle for this problem

This block states how Q035 is viewed as a tension problem within TU at the effective layer.

### 4.1 Core tension functional

We define an effective tension functional

```txt
Tension_Q35(m) =
    w_limit * DeltaS_Q35_limit(m)
  + w_scaling * I_scaling(m_group)
  + w_resource * I_resource(m)
```

where:

* `w_limit`, `w_scaling`, and `w_resource` are fixed nonnegative weights chosen once for the entire encoding class `E_Q35`.
* `m_group` is a small set of states representing the same scenario at different `R_eff` values, used to compute `I_scaling`.

Properties:

* `Tension_Q35(m) >= 0` for all `m` in `M_35_reg`.

* `Tension_Q35(m)` is small when:

  * `error(m)` tracks the appropriate limit `Limit_Q35(m; R_eff(m))`,
  * scaling exponents match the theoretical expectations,
  * resource accounting is consistent.

* `Tension_Q35(m)` is large when:

  * error statistics, scaling patterns, or resource usage differ in a way that contradicts known quantum estimation theory under the chosen resource definition.

### 4.2 TU aligned metrology worlds

At the effective layer, a TU aligned metrology world is one in which:

* There exists at least one encoding in `E_Q35` such that, for all physically realizable scenarios in the intended scope, there are states `m_true` in `M_35_reg` satisfying

  ```txt
  Tension_Q35(m_true) <= epsilon_Q35
  ```

  for some small threshold `epsilon_Q35` determined by modeling uncertainties and experimental variability.

* For protocols that are claimed to saturate or approach fundamental limits, such as Heisenberg scaling, the low tension region is stable under:

  * modest refinement of resource definitions,
  * inclusion of realistic noise contributions,
  * increased measurement statistics.

### 4.3 TU misaligned metrology worlds

A TU misaligned metrology world is one in which, even after adopting fair resource accounting and realistic noise models, one can construct families of states `m_claim` in `M_35_reg` such that:

* The encoded errors appear to beat all applicable `Limit_Q35(m; R_eff(m))` across resource levels, and
* For any encoding in `E_Q35` that is faithful to the physical scenario, the tension functional satisfies

  ```txt
  Tension_Q35(m_claim) >= delta_Q35
  ```

  for some strictly positive `delta_Q35` that does not vanish under refinement.

In such a world, either the accepted limits must be revised, or the underlying physical theory diverges from the assumptions used to derive those limits.

---

## 5. Counterfactual tension worlds

We now define two counterfactual worlds, both described strictly in terms of observable patterns and admissible encodings.

### 5.1 World T: internally consistent limits

In World T:

1. For every scenario class in `L_Q35` and each admissible encoding in `E_Q35`, there exists a regular state `m_T` in `M_35_reg` such that:

   ```txt
   Tension_Q35(m_T) <= epsilon_Q35
   ```

   where `epsilon_Q35` is small compared to the scale of `error(m_T)`.

2. As resource levels increase and encodings are refined along a predetermined sequence `refine(k)`, the tension values remain bounded and stable:

   ```txt
   Tension_Q35(m_T(k)) -> a small band
   ```

   where `m_T(k)` are refined representations of the same physical scenario.

3. Apparent “super-Heisenberg” protocols, when fully encoded with honest `R_eff` and noise models, fall back into the low tension band by revealing hidden resource costs or degraded noise behavior.

4. Quantum estimation theory, as currently formulated in the references listed above, is sufficient to explain the observed patterns in `error`, `QFI`, and scaling exponents within the uncertainty margins.

### 5.2 World F: persistent violations

In World F:

1. There exists at least one family of scenarios in `L_Q35` and sequences of states `m_F(k)` in `M_35_reg` such that:

   ```txt
   error(m_F(k)) << Limit_Q35(m_F(k); R_eff(m_F(k)))
   ```

   for growing `R_eff(m_F(k))`, where `<<` indicates much smaller than any known bound from the reference limit family.

2. Attempts to incorporate additional resources into `R_eff` or adjust noise models within `E_Q35` do not eliminate this discrepancy. For every encoding in `E_Q35` that respects the formal rules, the tension functional satisfies:

   ```txt
   Tension_Q35(m_F(k)) >= delta_Q35
   ```

   for some `delta_Q35 > 0` independent of `k`.

3. Scaling exponents `alpha(m_F(k))` remain significantly larger than the theoretical `alpha_ref` associated with the applicable limit, even when the sample size, noise characterization, and resource definitions are systematically improved.

4. The persistent high tension cannot be attributed to finite sample artifacts or modeling errors; instead it indicates that the assumed bounds or the underlying physical postulates are incomplete.

### 5.3 Interpretive note

These counterfactual worlds do not construct internal TU fields from raw microscopic models. They only state that, if there exist encodings in `E_Q35` that faithfully reflect the behavior of physical metrology experiments, then the patterns of `error`, `QFI`, resource usage, and tension would differ in the ways described above in World T and World F.

---

## 6. Falsifiability and discriminating experiments

This block specifies experiments and protocols that can falsify particular Q035 encodings within `E_Q35`. Falsification here means rejecting a chosen tension encoding, not proving or disproving any ultimate physical limit.

### Experiment 1: Scaling test under controlled dephasing

*Goal:*
Test whether the chosen `Tension_Q35` encoding correctly classifies standard and entanglement enhanced protocols under a fixed dephasing model, and whether tension remains stable under refinement.

*Setup:*

* Choose a set of phase estimation scenarios in `L_Q35`:

  * Scenario A: coherent state interferometry with dephasing noise.
  * Scenario B: GHZ like or spin squeezed probes with dephasing noise.

* For each scenario, fix:

  * a sequence of resource levels `R_eff` by varying `N` and `T` according to a predefined rule,
  * a noise strength parameter for dephasing, held constant across resource levels.

* For each resource level, define an effective state `m_data` encoding:

  * observed or simulated estimation error `error(m_data)`,
  * `QFI(m_data)` and `CFI(m_data)` summaries,
  * the fixed `R_eff(m_data)` and noise label.

*Protocol:*

1. For each scenario and each resource level, compute `DeltaS_Q35_limit(m_data)` using the agreed reference limits `Limit_SNL` and `Limit_noise_dephasing`.
2. For groups of states representing the same scenario at multiple resource levels, compute `alpha(m_group)` and `I_scaling`.
3. Evaluate `I_resource` using a baseline resource estimate `R_base(m_data)` derived from a simplified physical model.
4. Compute `Tension_Q35(m_data)` for all states.
5. Analyze how `Tension_Q35` behaves as resource levels increase and as the refine index `k` moves along a predetermined refinement sequence (for example finer time resolution or more accurate noise calibration).

*Metrics:*

* Distribution of `Tension_Q35` values for Scenario A vs Scenario B.
* Trend of `Tension_Q35` with increasing `R_eff`.
* Stability of `I_scaling` and `I_resource` across refine steps.

*Falsification conditions:*

* If Scenario A (classical like) consistently shows low tension and Scenario B (entanglement enhanced) shows high tension in regimes where theory predicts an advantage for entanglement, the encoding may be misaligned.
* If small, justified changes in the modeling details (for example small variations in dephasing rate) cause large, discontinuous jumps in `Tension_Q35` classification for similar states, the encoding is considered unstable and rejected.
* If no choice of reasonable weights `w_limit`, `w_scaling`, and `w_resource` (fixed in advance) yields a clear separation between well understood protocols and obviously flawed toy protocols, the chosen form of `Tension_Q35` is considered inadequate.

*Semantics implementation note:*
All quantities are treated as continuous fields over resource and noise parameters consistent with the metadata. Discrete sampling of resource levels is only an approximation to the underlying continuous dependence.

*Boundary note:*
Falsifying TU encoding != solving canonical statement.

---

### Experiment 2: Multi parameter and adaptive protocol test

*Goal:*
Evaluate whether the Q035 encoding remains coherent and discriminative when applied to multi parameter and adaptive metrology protocols.

*Setup:*

* Select a small set of multi parameter Ramsey spectroscopy or atomic ensemble experiments in `L_Q35`, each involving:

  * simultaneous estimation of a vector `theta = (theta_1, theta_2)`,
  * a chosen adaptive measurement strategy,
  * a specific noise model (for example partial dephasing plus loss).

* For each experiment and resource level, construct a state `m_multi` in `M_35_reg` encoding:

  * marginal and joint error summaries for the parameters,
  * aggregated `QFI(m_multi)` and `CFI(m_multi)` entries,
  * a vector resource measure collapsed to a scalar `R_eff(m_multi)` via a fixed rule.

*Protocol:*

1. Define an extended reference limit function `Limit_multi(R_eff)` based on known multi parameter bounds or conservative extensions of single parameter limits.
2. For each `m_multi`, compute a combined error measure `error(m_multi)` by a fixed norm on the error vector (for example Euclidean norm).
3. Evaluate `DeltaS_Q35_limit(m_multi)` with respect to `Limit_multi`.
4. For sequences of states at different resource levels, estimate a scaling exponent `alpha_multi` and compute `I_scaling`.
5. Compute `Tension_Q35(m_multi)` and compare across different strategies and noise settings.

*Metrics:*

* Comparison of `Tension_Q35` for naive non adaptive strategies vs carefully designed adaptive strategies.
* Behavior of `Tension_Q35` as resource levels and number of adaptive rounds increase.
* Sensitivity of tension to changes in the resource definition rule within `E_Q35`.

*Falsification conditions:*

* If the encoding assigns lower tension to clearly suboptimal strategies than to known near optimal strategies across a broad range of resources, the encoding is considered misaligned.
* If tension classifications for very similar multi parameter setups fluctuate drastically under small and justified changes in modeling details, the encoding fails a stability requirement and is rejected.
* If for any plausible `Limit_multi` from the theoretical literature the encoding cannot distinguish between clearly inconsistent toy models and realistic protocols, the `Limit_multi` selection or the way errors are aggregated is considered inadequate.

*Semantics implementation note:*
The multi parameter quantities are modeled as continuous fields over parameter space, with discrete sampling in practice representing finite experimental or numerical resolution.

*Boundary note:*
Falsifying TU encoding != solving canonical statement.

---

## 7. AI and WFGY engineering spec

This block describes how Q035 can be used as an engineering module for AI systems in the WFGY framework, without revealing any deep TU generative rules.

### 7.1 Training signals

We define several training signals that can be used as auxiliary losses or diagnostics.

1. `signal_resource_scaling_consistency`

   * Definition: a nonnegative signal proportional to `I_scaling` for scenarios where multiple resource levels are available.
   * Purpose: penalize internal representations that imply scaling exponents inconsistent with known limits when the context assumes those limits.

2. `signal_qfi_vs_error_gap`

   * Definition: a signal constructed from the gap between the Cramer Rao type bound implied by `QFI(m)` and the actual error `error(m)`.
   * Purpose: discourage reasoning patterns that rely on unattainable precision for a given `QFI`.

3. `signal_limit_tension_score`

   * Definition: directly equal to `Tension_Q35(m)` for states associated with problem Q035.
   * Purpose: provide a scalar consistency indicator that can be minimized when the system is instructed to respect known metrology limits.

4. `signal_protocol_classification_stability`

   * Definition: a measure of how stable the classification of protocols (for example “within limits” vs “suspicious”) remains under small variations in problem statements or resource descriptions.
   * Purpose: encourage robustness in limit based judgments.

### 7.2 Architectural patterns

We outline module patterns that can reuse Q035 structures.

1. `MetrologyLimitChecker`

   * Role: given a natural language or symbolic description of a metrology scenario, produce an approximate `Tension_Q35` score and simple explanations of which components (limit mismatch, scaling, resource fairness) contribute most.
   * Interface:

     * Inputs: embeddings of the problem description, including parameter type, resource claims, noise description, and protocol class.
     * Outputs: a scalar tension value, plus a small vector for `(DeltaS_Q35_limit, I_scaling, I_resource)`.

2. `ResourceAccountingAssistant`

   * Role: suggest consistent choices for `R_eff` and related resource metrics based on physical and operational descriptions.
   * Interface:

     * Inputs: description of experimental setup, including probes, time, control operations, and ancillary systems.
     * Outputs: a small set of candidate `R_eff` definitions, each with a justification.

3. `ScalingPatternExtractor`

   * Role: given multiple descriptions or simulation summaries at different resource levels, estimate scaling exponents and generate summaries for use by `MetrologyLimitChecker`.
   * Interface:

     * Inputs: tuples `(R_eff, error)` for a scenario.
     * Outputs: estimated `alpha` and uncertainty, plus a flag indicating whether the data supports reliable scaling analysis.

### 7.3 Evaluation harness

We propose an evaluation harness for AI systems that use Q035 components.

1. Task selection

   * Assemble a benchmark of metrology related texts, including:

     * real experimental papers and proposals,
     * synthetic scenarios where resource accounting is intentionally incomplete,
     * toy examples that violate known bounds.

2. Experimental conditions

   * Baseline: model operates without Q035 specific modules.
   * Q035 enhanced: model uses `MetrologyLimitChecker` and `ResourceAccountingAssistant` to evaluate claims before answering.

3. Metrics

   * Accuracy in identifying obviously inconsistent “beyond Heisenberg” claims.
   * Rate of false positives, where valid protocols are incorrectly flagged as impossible.
   * Consistency of explanations regarding which resources or noise processes explain why a protocol is or is not within limits.

4. Logging

   * For each task, record the raw answer, the tension scores, and a short structured explanation so that symptoms of failure can be analyzed without revealing TU internals.

### 7.4 60 second reproduction protocol

A minimal protocol to allow external users to feel the impact of Q035 encoding.

* Baseline setup:

  * Prompt: ask an AI system to evaluate whether a given quantum metrology proposal is physically plausible, without mentioning WFGY or tension.
  * Observation: note whether the answer discusses resources, noise, and limits in a coherent way or focuses only on headline scaling claims.

* Q035 encoded setup:

  * Prompt: present the same proposal, but instruct the system to:

    * explicitly identify the resource metric `R_eff`,
    * compare claimed errors to `Limit_SNL` and `Limit_HL`,
    * produce an informal `Tension_Q35` style verdict.

  * Observation: note whether the answer now highlights hidden resource costs, noise assumptions, and scaling details.

* Comparison metric:

  * Evaluate which answer better matches expert expectations about feasibility and which one gives more precise reasons.

* What to log:

  * The prompts, the two answers, and the scalar tension estimates, for later qualitative and quantitative assessment.

---

## 8. Cross problem transfer template

This block lists reusable components produced by Q035 and shows how they transfer to other problems.

### 8.1 Reusable components produced by this problem

1. ComponentName: `MetrologyResourceMetric_R_eff`

   * Type: field

   * Minimal interface:

     ```txt
     Inputs: description of probes, time budget, energy or photon number, control operations
     Output: scalar R_eff >= 0
     ```

   * Preconditions:

     * The description must provide enough information to compute `R_eff` under one of the fixed rules in `E_Q35`.

2. ComponentName: `ScalingExponentEstimator_alpha`

   * Type: functional

   * Minimal interface:

     ```txt
     Inputs: finite set of pairs (R_eff_i, error_i)
     Output: alpha_est, alpha_uncertainty
     ```

   * Preconditions:

     * At least three distinct resource levels with reliable error estimates.

3. ComponentName: `MetrologyTensionFunctional_TQ35`

   * Type: functional

   * Minimal interface:

     ```txt
     Inputs: R_eff, error, noise_label, strategy_label
     Output: Tension_Q35_value >= 0
     ```

   * Preconditions:

     * A suitable limit function from `Limit_family` must be defined for the given noise and strategy labels.

### 8.2 Direct reuse targets

1. Target: Q032 (quantum thermodynamics limits)

   * Reused components: `MetrologyResourceMetric_R_eff`, `MetrologyTensionFunctional_TQ35`.
   * Why it transfers: thermodynamic limits also relate performance (for example work extraction or cooling) to resources (for example energy, coherence). The same structure of a resource metric, a limit function, and a tension score can be reused.
   * What changes: the observables become thermodynamic output quantities instead of parameter estimation error, and `Limit_family` is replaced by thermodynamic bound functions.

2. Target: Q059 (information vs thermodynamics)

   * Reused components: `MetrologyResourceMetric_R_eff`, `ScalingExponentEstimator_alpha`, `MetrologyTensionFunctional_TQ35`.
   * Why it transfers: information extraction tasks have analogous tradeoffs between resources and accuracy, so the scaling and tension patterns can be reused.
   * What changes: `error` is replaced by information loss or misclassification rates, and resource definitions may include memory and communication costs.

3. Target: Q123 (AI interpretability via spectral probes)

   * Reused components: `MetrologyResourceMetric_R_eff`, `ScalingExponentEstimator_alpha`.
   * Why it transfers: probing internal AI representations resembles an estimation task where probes and compute are resources and interpretability quality is the “precision”.
   * What changes: the noise labels and limits refer to model stochasticity and approximation errors rather than physical decoherence.

---

## 9. TU roadmap and verification levels

This block explains where Q035 stands in the TU verification ladder and what the next measurable steps are.

### 9.1 Current verification levels

* E_level: E1

  * A coherent effective encoding has been specified, including:

    * a finite library `L_Q35`,
    * an admissible encoding class `E_Q35` with fairness constraints,
    * defined observables and main tension functionals,
    * a singular set `S_sing_35`.

  * Experiments have been outlined with clear falsification conditions for specific encodings.

* N_level: N1

  * The narrative linking resources, limits, and tension is explicit but still high level.
  * Counterfactual worlds and cross domain transfers have been sketched, but not fully specialized to large numbers of concrete examples.

### 9.2 Next measurable steps toward higher levels

To move from E1 and N1 toward E2 and N2, at least the following steps should be implemented:

1. Instantiate a concrete `L_Q35` with a small finite number of explicit scenarios (for example phase estimation with coherent and GHZ states under several noise models).
2. For each scenario, produce numerical tables that map resource levels to errors, QFI values, and tension scores under one chosen encoding in `E_Q35`.
3. Run the discriminating experiments from Block 6 on real or simulated data and publish tension profiles as open data for independent scrutiny.
4. Document at least one concrete failure case where a naive encoding is falsified and a refined encoding brings tension back into a stable low band.

These steps are compatible with the effective layer constraints because they work entirely with observable summaries and fixed encoding rules, not with deep TU generative mechanisms.

### 9.3 Long term role in the TU program

In the longer term, Q035 is expected to:

* Serve as the reference node for all “limit under constraints” problems involving quantum resources.
* Provide a template for building similar tension encodings in computation, thermodynamics, and AI interpretability.
* Help calibrate how much structure can be encoded at the effective layer before one risks leaking deep generative rules.
* Act as a testbed for integrating experimental data, theoretical bounds, and AI reasoning under a unified, falsifiable tension framework.

---

## 10. Elementary but precise explanation

This block gives an explanation suitable for non specialists while remaining consistent with the effective layer description.

In simple terms, quantum metrology is about using quantum systems to measure things as precisely as possible. For example, you might want to measure a tiny phase shift in an interferometer, a very small magnetic field, or a very accurate clock frequency.

To evaluate what is possible, you have to look at three ingredients:

1. The resources you spend: number of particles, time, energy, and how much quantum control you use.
2. The noise around you: decoherence, loss, thermal effects, and imperfections.
3. The errors you get: how far your estimate is from the true value, on average.

There are known mathematical limits that say, under certain assumptions, you can never beat certain error scales. The standard quantum limit says you should expect an error that goes like `1 / sqrt(N)` if you use `N` independent probes. Under ideal conditions and with specially designed quantum states, you can sometimes reach an error that goes like `1 / N`, which is called Heisenberg like scaling.

The challenge is that in real life:

* resources are complicated to count,
* noise is hard to model,
* and there is a temptation to declare “super advantages” without checking all costs.

The Tension Universe view does not try to prove new theorems about what is fundamentally possible. Instead, it asks:

* For each metrology setup, can we encode a few key numbers: a fair resource measure, an error summary, and a limit function?
* Can we define a tension score that is small when the setup behaves as theory expects and large when something is inconsistent?

If a claimed protocol looks better than all known limits, but the tension score is small once you include all hidden resources and noise, then the claim may be reasonable. If, after careful accounting, the tension remains large and cannot be explained away, then either the claim is flawed or the limits and assumptions must be revised.

Q035 is the node that formalizes this idea. It tells us how to turn metrology claims into:

* a set of observable quantities,
* a family of reference limits,
* and a tension functional that can be tested and reused.

This helps both humans and AI systems reason about quantum metrology in a structured way, without pretending to have proofs of ultimate physical bounds and without exposing any deep internal rules of the Tension Universe framework.
