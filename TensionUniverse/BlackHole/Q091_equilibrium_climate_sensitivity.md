# Q091 · Equilibrium climate sensitivity

## 0. Header metadata

```txt
ID: Q091
Code: BH_EARTH_CLIMATE_SENS_L3_091
Domain: Earth system and climate
Family: Climate dynamics
Rank: S
Projection_dominance: I
Field_type: dynamical_field
Tension_type: thermodynamic_tension
Status: Partial
Semantics: continuous
E_level: E1
N_level: N1
Encoding_key: TU_BH_Q091_ECS_v1
Last_updated: 2026-01-30
```

---

## 0. Effective layer disclaimer

All statements in this entry are made strictly at the effective layer of the Tension Universe (TU) framework.

* We only specify observable summaries, state spaces, mismatch functionals, tension scores, and counterfactual worlds.
* We do not specify any TU axiom system, deep generative rule, or constructive procedure that produces TU fields from first principles.
* We do not provide any explicit mapping from raw climate data or model output to internal TU objects. Such mappings are treated as implementation choices outside the scope of this page.
* We do not claim to determine the true value of equilibrium climate sensitivity (ECS), nor to prove any new theorem or bound about ECS.
* Nothing in this document should be cited as evidence that the underlying scientific questions about climate sensitivity have been solved.

The role of this entry is to define one concrete effective layer encoding of Q091, together with falsifiable experiments that can test whether this encoding behaves in a stable and coherent way.

---

## 1. Canonical problem and status

### 1.1 Canonical statement

Equilibrium climate sensitivity (ECS) is an effective number that describes how much the global mean surface temperature will eventually change when the radiative forcing of the climate system is increased by a specified amount and then held fixed until a new equilibrium is reached.

In the standard physical setting:

* A reference climate state is chosen, usually a preindustrial baseline.
* The atmospheric concentration of carbon dioxide is doubled relative to this reference.
* Other long lived greenhouse gases and forcing agents are treated in a consistent way, according to a specified protocol.
* The climate system is allowed to evolve until fast and intermediate feedbacks have acted and the atmosphere and upper ocean approach a new statistical equilibrium.

The canonical definition used in many assessments can be summarised as follows.

* ECS is the eventual change in global mean surface air temperature, expressed in degrees Celsius or Kelvin, for a doubling of carbon dioxide concentration, after the ocean and atmosphere have reached a new quasi equilibrium.
* Very slow components of the system, such as large ice sheets and deep geologic carbon cycle processes, are usually excluded from this definition, since they equilibrate on much longer time scales.

Equivalently, one can say:

* A radiative forcing associated with carbon dioxide doubling is defined by physical radiative transfer calculations and atmospheric structure.
* For a given climate model or physical world, an effective equilibrium temperature response to this forcing is defined.
* ECS is the ratio between this equilibrium temperature change and the specified forcing scenario, which can be reported as a single temperature change if the forcing is treated as a fixed constant.

The central scientific questions are not whether ECS exists, but:

* What range of ECS values is consistent with basic physical principles and available observations.
* Whether there is a reasonably narrow band in which ECS is likely to lie.
* How this band changes when new evidence, models, and observational records are incorporated.

### 1.2 Status and difficulty

Equilibrium climate sensitivity has been studied for many decades. Several features of the problem are considered robust:

* Basic radiative physics gives a lower bound. Even without feedbacks, a doubling of carbon dioxide leads to a clear positive temperature response.
* Feedbacks from water vapor, lapse rate changes, clouds, surface albedo, and other processes modify this basic response, often amplifying it.
* Multiple lines of evidence are available, including coupled atmosphere ocean general circulation models, simple energy balance models, instrumental records, and paleoclimate reconstructions.

At the same time, substantial uncertainty remains:

* Cloud feedbacks, especially from low clouds in the subtropics, are difficult to constrain and can strongly affect ECS.
* Ocean heat uptake, particularly in the deep ocean, introduces long adjustment time scales that complicate the relationship between transient warming and equilibrium warming.
* Observational records are finite in length and subject to internal variability, measurement uncertainty, and forcing uncertainty, all of which can obscure the forced signal.

Recent assessments have generally concluded that:

* Very low ECS values are unlikely, given multiple consistent lines of evidence.
* Very high ECS values are also disfavored, but cannot be completely ruled out, especially when considering uncertainties in cloud feedbacks and paleoclimate constraints.
* A central range of ECS values is reasonably well supported, but this range remains wide enough that it has large implications for long term climate risk and policy.

The Q091 problem is therefore:

* Partially constrained by a large and growing body of physical and statistical evidence.
* Still open with respect to the exact numeric range and the behaviour of tails in the ECS distribution.
* Structurally difficult because it involves thermodynamics, fluid dynamics, radiative transfer, feedback analysis, and statistical inference, all at once.

### 1.3 Role in the BlackHole project

Within the BlackHole S problem collection, Q091 plays several roles.

1. It is the primary example of a thermodynamic_tension problem in the Earth system domain, where global energy balance, feedbacks, and long time scale dynamics interact in nontrivial ways.

2. It provides a reference node for other Earth system problems that reuse its components, such as climate tipping points, carbon cycle feedbacks, and Anthropocene steady states.

3. It offers a way to express climate sensitivity as a tension problem:

   * between imposed forcings and resulting temperature responses,
   * between model based and observation based estimates of ECS,
   * between physically plausible feedback strengths and statistical fits to data.

Q091 does not aim to determine a single true value of ECS. Instead, it frames ECS as:

* an observable that lives in an effective state space,
* a source of thermodynamic_tension when different lines of evidence fail to align,
* a calibration problem for how TU encodings behave when applied to complex, partially observed physical systems.

### References

1. IPCC, 2021. Climate Change 2021: The Physical Science Basis. Contribution of Working Group I to the Sixth Assessment Report of the Intergovernmental Panel on Climate Change. Cambridge University Press. See Chapter 7 and the Summary for Policymakers sections on climate feedbacks and equilibrium climate sensitivity.
2. Knutti, R., and Hegerl, G. C., 2008. The equilibrium sensitivity of the Earth’s temperature to radiation changes: observations and model results. Nature Geoscience 1, 735–743.
3. Roe, G. H., and Baker, M. B., 2007. Why is climate sensitivity so unpredictable. Science 318, 629–632.
4. Sherwood, S. C., Webb, M. J., Annan, J. D., Armour, K. C., Forster, P. M., et al., 2020. An assessment of Earth's climate sensitivity using multiple lines of evidence. Reviews of Geophysics 58, e2019RG000678.

---

## 2. Position in the BlackHole graph

This block records how Q091 sits inside the BlackHole graph as nodes and edges among Q001–Q125. Each edge is listed with a one line reason that points to a concrete component or tension type.

### 2.1 Upstream problems

These problems provide prerequisites, tools, or general foundations that Q091 relies on at the effective layer.

* Q032 (BH_PHYS_QTHERMO_L3_032)
  Reason: Provides coarse grained thermodynamic and energy balance principles used to define global energy budget fields for Q091.

* Q093 (BH_EARTH_CARBON_CYCLE_L3_093)
  Reason: Supplies carbon cycle feedback structure that determines effective forcing and feedback parameters in the `ECS_TensionFunctional`.

* Q094 (BH_EARTH_OCEAN_MIX_L3_094)
  Reason: Defines constraints on deep ocean mixing and circulation that shape long term heat uptake and the mapping from forcing to `DeltaT_eq`.

### 2.2 Downstream problems

These problems directly reuse Q091 components or depend on Q091 tension structure.

* Q092 (BH_EARTH_TIPPING_L3_092)
  Reason: Reuses `ECS_TensionFunctional` as an input when estimating how close the system is to climate tipping thresholds.

* Q098 (BH_EARTH_ANTHROPOCENE_L3_098)
  Reason: Uses `EquilibriumClimateState_Descriptor` to define Anthropocene steady state candidates under different forcing trajectories.

* Q099 (BH_EARTH_WATER_STRESS_L3_099)
  Reason: Uses ECS driven equilibrium warming from Q091 as a driver for long term freshwater redistribution scenarios.

### 2.3 Parallel problems

Parallel nodes share similar tension types but no direct component dependence.

* Q041 (BH_COSMO_DARKMATTER_L3_041)
  Reason: Both involve hidden components inferred from indirect observables under thermodynamic_tension between energy budgets and observed fields.

* Q059 (BH_CS_INFO_THERMODYN_L3_059)
  Reason: Both analyse links between information measures and thermodynamic budgets, but in Q091 the system is the climate rather than an abstract information engine.

### 2.4 Cross domain edges

Cross domain edges connect Q091 to problems in other domains that can reuse its components.

* Q059 (BH_CS_INFO_THERMODYN_L3_059)
  Reason: Reuses the idea of a tension functional that compares energy balance models with data constrained descriptions as a case study of information thermodynamics.

* Q121 (BH_AI_ALIGNMENT_L3_121)
  Reason: Uses ECS based risk tails and `EquilibriumClimateState_Descriptor` as inputs into long term alignment scenarios where powerful AI systems plan over climate outcomes.

---

## 3. Tension Universe encoding (effective layer)

All content in this block is at the TU effective layer. We describe:

* state space,
* observables and fields,
* mismatch components and combined tension scores,
* singular sets and domain restrictions,
* the encoding class and its fairness constraints.

We do not describe any hidden TU generative rules or any constructive mapping from raw data to TU objects.

### 3.1 State space

We assume the existence of a state space

```txt
M
```

with the following interpretation at the effective layer.

* Each element `m` in `M` represents a coherent climate sensitivity configuration for a specified forcing scenario.
* A state `m` aggregates:

  * a global energy budget summary for that scenario,
  * a compact set of feedback descriptors (for example water vapor, cloud, and surface albedo feedbacks),
  * an effective equilibrium global mean temperature response `DeltaT_eq(m)` to the scenario,
  * a score describing how strongly `m` is constrained by observations rather than purely by model structure.

We do not specify how these states are constructed from simulations or observations. We only require that for any fixed forcing scenario of interest, there exist states in `M` that encode reasonable candidate equilibrium responses whose observables are finite and well defined.

We also assume there is a fixed reference forcing constant

```txt
F_2xCO2 > 0
```

associated with carbon dioxide doubling relative to a baseline. This constant is part of the physical context and is not tuned during TU experiments.

### 3.2 Effective fields and observables

We introduce the following effective fields and observables on `M`.

1. Effective forcing for the scenario

   ```txt
   F_eq(m)
   ```

   * A nonnegative scalar representing the effective radiative forcing for the scenario encoded in `m`, in consistent units.
   * For the canonical ECS scenario, `F_eq(m)` is equal to `F_2xCO2`, but the encoding allows other scenarios if needed.

2. Equilibrium temperature response

   ```txt
   DeltaT_eq(m)
   ```

   * The long term equilibrium change in global mean surface temperature, relative to the chosen baseline, for the forcing scenario encoded in `m`.
   * This is an effective quantity that summarises the eventual response including fast and intermediate feedbacks.

3. Equilibrium climate sensitivity number

   We define

   ```txt
   ECS(m) = DeltaT_eq(m) / F_ref
   ```

   where `F_ref` is a fixed positive constant chosen once for Q091. In the canonical case `F_ref` is equal to `F_2xCO2`. The explicit numerical value of `F_ref` is not part of the TU encoding.

4. Feedback vector

   ```txt
   FeedbackVector(m)
   ```

   * A vector valued observable that encodes the aggregated contributions of the main feedbacks.
   * Components may correspond to specific physical feedbacks, but at the effective layer we treat them as unnamed entries in a finite dimensional vector.

5. Observation constraint score

   ```txt
   ObsConstraintScore(m)
   ```

   * A scalar in a fixed closed interval, for example between 0 and 1.
   * A higher value means that the state `m` is more strongly supported by observations, such as historical energy budget fits, emergent constraints, or paleoclimate reconstructions.
   * A lower value means the state is based mainly on unconstrained or weakly constrained model structure.

All of these observables are assumed to be real valued functions on a suitable subset of `M`. The procedures that construct them from data or models are part of implementation and are not specified here.

### 3.3 Mismatch and tension components

We now define mismatch components that will be combined into a tension functional. To avoid after the fact tuning, we fix a small library of reference objects and weight choices before any experiment is considered.

#### 3.3.1 Admissible reference band for ECS

We choose a closed interval

```txt
[ECS_low_ref, ECS_high_ref]
```

that represents a reference band for ECS values, based on external scientific assessments. The precise numeric values are not important for TU; what matters is that:

* the band is fixed once for this encoding key,
* it is wide enough to include ECS values that are physically plausible under current knowledge,
* it is narrow enough that lying far outside the band signals meaningful tension.

We also fix a finite library of possible bands

```txt
B_1, B_2, ..., B_K
```

that may be used in later encoding versions. In this encoding `TU_BH_Q091_ECS_v1`, we use a single primary band `[ECS_low_ref, ECS_high_ref]`.

#### 3.3.2 Sensitivity mismatch

We define the sensitivity mismatch

```txt
DeltaS_sens(m)
```

as follows.

* If `ECS_low_ref <= ECS(m) <= ECS_high_ref`, then

  ```txt
  DeltaS_sens(m) = 0 .
  ```

* Otherwise,

  ```txt
  DeltaS_sens(m) = distance from ECS(m) to the nearest bound
  ```

  where distance is taken in the usual real number sense.

This mismatch is always nonnegative and is zero exactly when `ECS(m)` lies inside the reference band.

#### 3.3.3 Model versus observation mismatch

For states in `M` that represent worlds where both models and observations are available, we assume the existence of two derived quantities:

```txt
ECS_model(m)
ECS_obs(m)
```

* `ECS_model(m)` is the ECS implied by model based analysis inside `m`.
* `ECS_obs(m)` is the ECS implied by observation based constraints in `m`.

We then define

```txt
DeltaS_model(m) = (ECS_model(m) - ECS_obs(m))^2
```

where the square is taken in the usual real sense. This term is nonnegative and measures disagreement between model and observation based ECS estimates.

#### 3.3.4 Feedback structure mismatch

We define a function

```txt
FeedbackRangePenalty(FeedbackVector(m))
```

that satisfies:

* it is nonnegative,
* it is equal to zero if all components of `FeedbackVector(m)` lie inside predetermined physically acceptable ranges and the implied net feedback strength lies inside a predetermined plausible band,
* it is positive if any component lies outside those ranges or if the combination of components implies net feedback strength that is outside the chosen plausible band.

We then set

```txt
DeltaS_feedback(m) = FeedbackRangePenalty(FeedbackVector(m)) .
```

This captures the tension between feedback combinations encoded in `m` and basic physical limits.

#### 3.3.5 Combined ECS mismatch

We fix three positive weights

```txt
w_sens, w_model, w_fb
```

satisfying

```txt
w_sens + w_model + w_fb = 1 .
```

These weights are:

* chosen once for this encoding key from a finite set of simple rational tuples,
* recorded as part of the encoding,
* not adjusted in response to any experiment result.

We then define the combined ECS mismatch

```txt
DeltaS_ECS(m) = w_sens  * DeltaS_sens(m)
              + w_model * DeltaS_model(m)
              + w_fb    * DeltaS_feedback(m) .
```

By construction, `DeltaS_ECS(m)` is nonnegative and equals zero only when:

* ECS lies inside the reference band,
* model based and observation based ECS estimates agree,
* feedbacks lie inside their acceptable ranges.

### 3.4 Effective tension tensor and singular set

#### 3.4.1 Effective tension tensor

Consistent with the TU core pattern, we define an effective tension tensor

```txt
T_ij(m) = S_i(m) * C_j(m) * DeltaS_ECS(m) * lambda(m) * kappa
```

where:

* `S_i(m)` is a source like factor for the i th semantic source component, such as the strength of climate forcing and risk discussion in the current reasoning context,
* `C_j(m)` is a receptivity like factor for the j th downstream component that is affected by climate sensitivity assumptions,
* `DeltaS_ECS(m)` is the combined mismatch defined above,
* `lambda(m)` is a convergence state factor that indicates whether reasoning around `m` is in a convergent, recursive, divergent, or chaotic mode, and is bounded between fixed positive constants,
* `kappa` is a coupling constant that sets the overall scale for ECS related thermodynamic_tension in this encoding.

The details of `S_i`, `C_j`, and `lambda` are not exposed here. We only assume that for every `m` in the regular domain defined below, `T_ij(m)` is finite.

#### 3.4.2 Singular set and domain restriction

Some observables can become undefined or unbounded. To handle this, we define the singular set

```txt
S_sing = { m in M :
           ECS(m) is undefined or not finite
           or F_eq(m) <= 0
           or FeedbackVector(m) is undefined
           or ObsConstraintScore(m) is undefined } .
```

We then define the regular domain

```txt
M_reg = M \ S_sing .
```

All Q091 tension functionals and experiments are evaluated only on `M_reg`. If a procedure would require evaluating `DeltaS_ECS(m)` or `Tension_ECS(m)` for `m` in `S_sing`, the result is treated as out of domain and is not interpreted as evidence about ECS or about the truth of any physical proposition.

We do not attempt to regularise or interpret singular states in a weak or extended sense in this encoding.

### 3.5 Encoding class and fairness constraints (ECS)

For Q091 and encoding key `TU_BH_Q091_ECS_v1`, the encoding class and fairness rules are as follows.

1. **Reference bands**

   * A finite library of ECS bands `B_1, ..., B_K` is defined from external scientific assessments before any TU experiment is designed.
   * This encoding uses a single primary band `[ECS_low_ref, ECS_high_ref] = B_1`.
   * The choice of `B_1` is fixed for this encoding key and is not tuned in response to tension outputs.

2. **Weight library**

   * The weights `(w_sens, w_model, w_fb)` are selected from a finite library of simple rational triples, for example `(1/3, 1/3, 1/3)` or `(1/2, 1/4, 1/4)`.
   * Once a triple is chosen for `TU_BH_Q091_ECS_v1`, it remains fixed across all experiments and all states.

3. **Observation constraint mapping**

   * The mapping from raw fit quality or likelihood metrics to `ObsConstraintScore(m)` is treated as part of the encoding.
   * A specific monotone mapping into the interval `[0, 1]` is chosen and documented in implementation notes, but not altered for individual models or datasets.
   * The same mapping must be applied uniformly to all states in all experiments under this encoding key.

4. **Feedback penalty specification**

   * Physically acceptable ranges for individual feedback components and a plausible band for net feedback strength are chosen from external literature before experiments are defined.
   * These ranges, and the function `FeedbackRangePenalty`, are part of the encoding.
   * They are applied uniformly to all states. They are not adjusted separately for particular models or scenarios.

5. **Constant parameters**

   * The constant `eps_obs` used in `Tension_ECS(m)` is chosen once, from a reasonable numerical range, and is kept fixed for this encoding key.
   * The coupling constant `kappa` and bounds for `lambda(m)` are also fixed as part of the encoding.

6. **Versioning**

   * Any change in reference bands, weight libraries, mapping rules, or penalty ranges defines a new encoding key, such as `TU_BH_Q091_ECS_v2`.
   * Results obtained under different encoding keys must not be merged as if they came from a single encoding.

All experiments in Section 6 are required to use exactly the encoding class specified here and in the TU Encoding and Fairness Charter.

---

## 4. Tension principle for this problem

This block states how Q091 is characterised as a tension problem within TU, at the effective layer.

### 4.1 Core ECS tension functional

We define an effective ECS tension functional

```txt
Tension_ECS(m) = DeltaS_ECS(m) / max(ObsConstraintScore(m), eps_obs)
```

where:

* `DeltaS_ECS(m)` is the combined mismatch from Section 3.3.5,
* `ObsConstraintScore(m)` is the observation constraint score from Section 3.2,
* `eps_obs` is a small positive constant fixed once for this encoding.

This functional behaves as follows.

* For states that are strongly constrained by observations, large mismatch leads to large ECS tension.
* For states that are weakly constrained, the denominator prevents arbitrarily large scores, but large mismatches are still penalised.
* If a state fits the reference band, the model observation agreement, and the feedback ranges while being well constrained, then `Tension_ECS(m)` is small.

### 4.2 ECS as a low tension principle

At the effective layer, Q091 can be phrased as the following low tension principle.

> In physically reasonable world models that respect known climate physics and observational constraints, there exists a narrow band of ECS values for which the ECS tension functional remains small and stable under refinement of data and models.

More concretely, consider a sequence of states

```txt
m_1, m_2, ..., m_k, ...
```

that represent increasingly refined descriptions of the same real world, as more data and more detailed models are incorporated, while the encoding class and weights remain fixed. The low tension principle asserts that there exists a band

```txt
[ECS_low_star, ECS_high_star]
```

such that for states whose ECS lies inside this band,

```txt
Tension_ECS(m_k) <= tau_low
```

for a small threshold `tau_low` that does not grow without bound as `k` increases, except for fluctuations that can be explained by finite data and model resolution.

### 4.3 ECS failure as persistent high tension

The complementary high tension picture is the following.

> If the combination of physical laws, feedback structures, and observational records is such that no stable ECS band exists, then any encoding that remains faithful to the evidence will show persistent high ECS tension.

In this picture, for any candidate band `[ECS_low, ECS_high]` and for any encoding that deserves to be called faithful, we would eventually find states representing the real world for which

```txt
Tension_ECS(m_fail) >= tau_high
```

where `tau_high` is a fixed positive threshold that cannot be made arbitrarily small just by refining the description. In practice this would manifest as:

* model based ECS and observation based ECS estimates that remain far apart,
* feedback combinations that repeatedly violate plausible ranges,
* an inability to identify a narrow band of ECS values for which tension is reliably low.

Q091 does not assert which of these pictures is realised in our universe. It provides:

* a way to express the problem in terms of a tension functional,
* a structured list of observables to monitor,
* a language to compare low tension and high tension worlds.

---

## 5. Counterfactual tension worlds

We now describe two counterfactual worlds at the effective layer.

* World L: a low sensitivity world.
* World H: a high sensitivity world.

We do not construct any deep generative rules. We only describe patterns in observables and tension scores.

### 5.1 World L (low sensitivity world)

In World L:

1. **ECS band**

   * Most observationally supported states `m_L` satisfy

     ```txt
     ECS(m_L) in [ECS_low_L, ECS_high_L]
     ```

     where `[ECS_low_L, ECS_high_L]` is a band near the lower end of physically plausible sensitivities.

2. **Sensitivity and model observation mismatch**

   * For these states, `DeltaS_sens(m_L)` is close to zero because ECS lies well inside the reference band.
   * `DeltaS_model(m_L)` is small because model based and observation based ECS estimates are compatible.
   * `DeltaS_feedback(m_L)` is small because feedback combinations lie inside their plausible ranges.

3. **Global ECS tension**

   * The ECS tension functional satisfies

     ```txt
     Tension_ECS(m_L) <= tau_low
     ```

     for a modest threshold `tau_low`, with fluctuations that shrink or remain bounded as data and models are refined.

4. **Long term response pattern**

   * Equilibrium warming remains moderate even under large forcing.
   * Many states combine:

     * moderate `DeltaT_eq(m_L)`,
     * consistent feedback vectors,
     * high observation constraint scores.

### 5.2 World H (high sensitivity world)

In World H:

1. **ECS band**

   * Many observationally relevant states `m_H` satisfy

     ```txt
     ECS(m_H) in [ECS_low_H, ECS_high_H]
     ```

     where `[ECS_low_H, ECS_high_H]` is a band near the upper end of plausible sensitivities.

2. **Sensitivity and model observation tension**

   * If reference bands and feedback ranges are chosen based on standard arguments, then:

     * `DeltaS_sens(m_H)` tends to be larger, because ECS values sit near or beyond the upper part of the reference band.
     * `DeltaS_model(m_H)` can be large when models that imply high ECS struggle to match historical energy budget constraints.
     * `DeltaS_feedback(m_H)` can be large when required feedback combinations approach or exceed physically plausible limits.

3. **Global ECS tension**

   * For many states representing the real world under this assumption, we have

     ```txt
     Tension_ECS(m_H) >= tau_high
     ```

     for a strictly positive `tau_high` that persists under refinement.

4. **Long term response pattern**

   * Equilibrium warming is large under realistic forcing trajectories.
   * States with high observation constraint scores still require large feedback strengths, leading to sustained thermodynamic_tension between different lines of evidence.

### 5.3 Interpretive note

These counterfactual worlds do not say which world is real. They illustrate:

* how the same TU encoding behaves under two different assumptions about the structure of ECS,
* how observable patterns such as `ECS(m)`, `FeedbackVector(m)`, and `ObsConstraintScore(m)` would lead to different tension profiles,
* how the existence or absence of a stable low tension ECS band becomes a central question.

---

## 6. Falsifiability and discriminating experiments

This block specifies experiments at the effective layer that can:

* test the coherence of the Q091 encoding,
* distinguish between different ECS related tension models,
* provide evidence for or against particular parameter choices.

These experiments can falsify specific TU encodings related to Q091. They do not prove or disprove any physical law by themselves.

All experiments in this section must use exactly the encoding class described in Section 3.5 and in the TU Encoding and Fairness Charter. In particular, reference bands, weights, feedback ranges, `eps_obs`, and observation mapping rules are fixed in advance and applied uniformly to all states in an experiment.

### Experiment 1: Historical energy balance tension profile

**Goal**

Test whether the chosen ECS tension functional `Tension_ECS` aligns in a stable way with historical energy balance constraints, given fixed encoding parameters.

**Setup**

* Use published reconstructions of:

  * global mean surface temperature over the historical period,
  * radiative forcing histories (greenhouse gases, aerosols, solar, volcanic),
  * estimates of ocean heat content change.

* Fix, before any calculations:

  * the reference band `[ECS_low_ref, ECS_high_ref]` from the encoding class,
  * the weight triple `(w_sens, w_model, w_fb)`,
  * the constant `eps_obs`,
  * the mapping rules for `ObsConstraintScore(m)`.

* Construct a simple energy balance model class that can be run over a range of ECS values, for example from 1 to 6 degrees Celsius per carbon dioxide doubling.

**Protocol**

1. For each candidate ECS value in the chosen range, calibrate an energy balance model to the historical forcing and temperature records, using a standard calibration procedure.

2. For each calibrated model, construct a state `m_hist(ECS_value)` in `M_reg` that encodes:

   * `F_eq(m_hist)`,
   * `DeltaT_eq(m_hist)` implied by the model under sustained forcing,
   * `ECS_model(m_hist)` equal to the ECS value used in the model,
   * `ECS_obs(m_hist)` inferred from an independent energy balance fit or inversion,
   * a `FeedbackVector(m_hist)` consistent with the model’s feedback structure,
   * an `ObsConstraintScore(m_hist)` derived from fit quality through the fixed mapping.

3. For each `m_hist(ECS_value)`, compute:

   * `DeltaS_sens(m_hist)`,
   * `DeltaS_model(m_hist)`,
   * `DeltaS_feedback(m_hist)`,
   * `DeltaS_ECS(m_hist)`,
   * `Tension_ECS(m_hist)`.

4. Summarise `Tension_ECS(m_hist)` as a function of ECS value, for example by plotting the tension profile or reporting statistics across calibration variants.

**Metrics**

* The location and width of the ECS band where `Tension_ECS(m_hist)` is minimal.
* The level of `Tension_ECS(m_hist)` outside this band.
* Stability of these features when:

  * the time window is slightly changed,
  * observational uncertainties are varied within reasonable limits,
  * alternative but consistent calibration methods are used.

**Falsification conditions**

* If, after fixing encoding parameters as described, no reasonably narrow ECS band can be identified where `Tension_ECS(m_hist)` is consistently lower than outside the band, then this particular tension encoding is considered falsified for Q091.
* If very small changes in encoding choices inside the allowed library can move the apparent low tension band across most of the ECS range without a clear physical reason, then the encoding is considered unstable and rejected.

**Semantics note**

All quantities in this experiment are treated as continuous fields or continuous time series summaries, consistent with the continuous semantics declared in the metadata. No discrete or hybrid encodings are introduced here.

**Boundary note**

Falsifying this TU encoding does not solve the canonical ECS problem. This experiment can reject specific choices of `Tension_ECS` and related parameters, but it does not directly determine the true value of ECS.

---

### Experiment 2: Model ensemble versus emergent constraints

**Goal**

Check whether the ECS tension encoding can systematically distinguish between model states that are compatible with emergent constraints and those that are not.

**Setup**

* Consider a multi model ensemble of climate models, each with:

  * a diagnosed ECS value,
  * a set of feedback parameters,
  * simulated observables that can be compared with emergent constraint relationships.

* Obtain one or more emergent constraint relationships from the literature that link present day or historical climate statistics to ECS.

* Fix all encoding parameters as in Section 3.5, including reference band, weight triple, feedback ranges, `eps_obs`, and observation mapping rules. These choices are applied uniformly to every model in the ensemble.

**Protocol**

1. For each model in the ensemble, construct a state `m_model` in `M_reg` that encodes:

   * `ECS_model(m_model)` equal to the model’s ECS,
   * `ECS_obs(m_model)` derived from emergent constraint relationships applied to the model’s simulated climate statistics,
   * `FeedbackVector(m_model)` built from the model’s feedback diagnostics,
   * `ObsConstraintScore(m_model)` based on how well the model matches the emergent constraint data, mapped through the fixed observation mapping.

2. Compute `DeltaS_sens(m_model)`, `DeltaS_model(m_model)`, `DeltaS_feedback(m_model)`, and `Tension_ECS(m_model)` for each model.

3. Partition the models into three sets:

   * models that are broadly consistent with the emergent constraints,
   * models that are clearly inconsistent,
   * models with very low observation constraint scores (for example `ObsConstraintScore(m_model)` below a fixed threshold), which can be treated as a weakly constrained reference group.

4. Compare the distributions of `Tension_ECS(m_model)` across these sets.

**Metrics**

* Mean and spread of `Tension_ECS(m_model)` for models that respect emergent constraints.
* Mean and spread for models that violate emergent constraints.
* Overlap between the two distributions, and how it compares with the weakly constrained group.

**Falsification conditions**

* If models that respect emergent constraints do not show lower ECS tension than models that violate them, in a statistically clear way, the current choice of `Tension_ECS` and mismatch components is considered misaligned for Q091.
* If models with very similar observables and feedbacks receive very different tension scores without explanation from the mismatch components, the encoding is judged inconsistent and rejected.

**Semantics note**

Model outputs and constraints are treated as continuous summary statistics and fields, consistent with the continuous semantics from the metadata. The TU encoding does not change the emergent constraint definitions; it only uses them as external inputs.

**Boundary note**

Falsifying this TU encoding does not say that any particular climate model or emergent constraint is wrong. It shows that the chosen ECS tension encoding does not align well with the structure of the model ensemble and constraints.

---

## 7. AI and WFGY engineering spec

This block describes how Q091 can be used as an engineering module for AI systems within the WFGY framework, at the effective layer.

### 7.1 Training signals

We define several training signals that can be used in AI models to encourage ECS aware and tension aware reasoning about climate questions.

1. `signal_ecs_band_penalty`

   * Definition: a nonnegative signal proportional to `DeltaS_sens(m)` whenever the model proposes or relies on an ECS value outside the reference band.
   * Purpose: discourage reasoning paths that assume extremely low or extremely high ECS values without clearly marking them as speculative.

2. `signal_feedback_consistency`

   * Definition: a signal based on `DeltaS_feedback(m)` that increases when implied feedback combinations violate physical ranges.
   * Purpose: guide the model toward feedback narratives that respect known limits even when reasoning qualitatively.

3. `signal_obs_model_gap`

   * Definition: a signal derived from `DeltaS_model(m)` that measures disagreement between model implied and observation implied ECS in the current state.
   * Purpose: penalise explanations or scenarios that rely on models far from observational constraints, unless this fact is explicitly highlighted.

4. `signal_ecs_tension_score`

   * Definition: directly equal to `Tension_ECS(m)` for a given internal state `m`.
   * Purpose: provide a scalar tension indicator that can be minimised or monitored when answering questions where long term climate response is relevant.

### 7.2 Architectural patterns

We outline module patterns that can reuse Q091 structures without revealing any deep TU generative rules.

1. `ClimateSensitivityHead`

   * Role: given an internal representation of a climate related context, produce an estimate of `Tension_ECS(m)` and its components.
   * Interface:

     * Inputs: embeddings or structured summaries representing forcing, feedbacks, and evidence.
     * Outputs: a scalar tension estimate and a small set of component scores such as `DeltaS_sens`, `DeltaS_model`, and `DeltaS_feedback`.

2. `EarthSystemRiskFilter`

   * Role: flag answers that imply high equilibrium climate sensitivity combined with weak evidence, or that understate risks given the assumed ECS band.
   * Interface:

     * Inputs: candidate answers and their associated internal states.
     * Outputs: soft masks or scores indicating whether the answer should be revised or explicitly marked as high uncertainty.

3. `TU_ClimateObserver`

   * Role: map internal representations into a simplified `EquilibriumClimateState_Descriptor` for use by other parts of the system.
   * Interface:

     * Inputs: embeddings connected to climate state descriptions.
     * Outputs: a low dimensional descriptor capturing forcing, ECS estimates, and key feedback indicators.

### 7.3 Evaluation harness

We suggest an evaluation harness for AI models that include Q091 based modules.

1. **Task selection**

   * Select sets of questions that require reasoning about long term warming under different emission or forcing scenarios.
   * Include questions that test understanding of the difference between transient and equilibrium response.

2. **Conditions**

   * Baseline condition:

     * The model operates without Q091 specific modules.
     * Answers are judged on correctness and internal consistency.

   * TU condition:

     * The model uses Q091 modules to track `Tension_ECS` and related signals.
     * High tension answers can be revised or explicitly marked as speculative.

3. **Metrics**

   * Consistency of ECS related statements across different parts of the same conversation.
   * Frequency of contradictory claims about warming under specified forcing scenarios.
   * Clarity of distinction between well constrained ranges and speculative extremes in both conditions.

### 7.4 60 second reproduction protocol

A minimal protocol to let external users experience the impact of Q091 encoding in an AI system.

* **Baseline setup**

  * Prompt: ask the AI to explain what equilibrium climate sensitivity is and how it affects long term warming under carbon dioxide doubling, without mentioning tension or ECS bands.
  * Observation: record whether the explanation clearly separates central estimates from extreme possibilities and explains why uncertainty exists.

* **TU encoded setup**

  * Prompt: ask the same question, but request that the AI explicitly organise the explanation around:

    * a reference ECS band,
    * sources of tension between models and observations,
    * the idea of a low tension ECS band.

  * Observation: record whether the explanation:

    * identifies a central ECS band,
    * discusses feedbacks and observational constraints,
    * highlights which parts of the range are high tension.

* **Comparison metric**

  * Use a rubric that scores:

    * conceptual accuracy,
    * explicitness of assumptions,
    * internal consistency about ECS ranges and risks.

* **What to log**

  * Both answers,
  * internal tension scores if available,
  * any flags raised by `EarthSystemRiskFilter`.

This protocol does not require access to TU internals. It only uses Q091 components as an organising frame for explanations.

---

## 8. Cross problem transfer template

This block describes the reusable components produced by Q091 and how they transfer to other problems.

### 8.1 Reusable components produced by this problem

1. **ComponentName**: `ECS_TensionFunctional`

   * Type: functional

   * Minimal interface:

     * Inputs: a bundle containing `F_eq`, `DeltaT_eq`, `FeedbackVector`, `ECS_model`, `ECS_obs`, and `ObsConstraintScore` for a state.
     * Output: a nonnegative scalar `tension_value` equal to `Tension_ECS(m)`.

   * Preconditions:

     * The input bundle corresponds to a state in `M_reg` where all fields are defined and finite.
     * The reference band, weights, and other encoding parameters are those fixed for `TU_BH_Q091_ECS_v1`.

2. **ComponentName**: `EquilibriumClimateState_Descriptor`

   * Type: field

   * Minimal interface:

     * Inputs: a forcing scenario descriptor and associated physical context.
     * Output: a compact descriptor of the equilibrium climate state, including `F_eq`, `DeltaT_eq`, `ECS`, and a small number of feedback and constraint indicators.

   * Preconditions:

     * The scenario falls within the range where an equilibrium description is meaningful.
     * Required physical information such as approximate energy budget and feedback structure is available.

3. **ComponentName**: `ECS_CounterfactualWorld_Template`

   * Type: experiment_pattern

   * Minimal interface:

     * Inputs: a specification of a low ECS band and a high ECS band, plus simple constraints on feedback ranges and observational support.
     * Output: two experiment templates describing World L and World H style scenarios and how to compute `Tension_ECS` in each.

   * Preconditions:

     * The bands and constraints respect basic physical and observational limits and are fixed before any data fitting.

### 8.2 Direct reuse targets

1. **Q092 (BH_EARTH_TIPPING_L3_092)**

   * Reused component: `ECS_TensionFunctional`.
   * Why it transfers: climate tipping analyses often depend on both the magnitude and timing of warming relative to thresholds. ECS related tension directly affects how close the system is to such thresholds in the long term.
   * What changes: in Q092, the output of `ECS_TensionFunctional` is combined with tipping specific fields such as critical temperatures and feedback switches, forming a composite tension measure.

2. **Q098 (BH_EARTH_ANTHROPOCENE_L3_098)**

   * Reused component: `EquilibriumClimateState_Descriptor`.
   * Why it transfers: Anthropocene dynamics depend on the long term climate state under sustained human forcing. ECS based descriptors provide a base layer for those states.
   * What changes: Q098 augments the descriptor with socio economic variables and land use patterns, and uses it to define multiple possible Anthropocene equilibria.

3. **Q121 (BH_AI_ALIGNMENT_L3_121)**

   * Reused component: `ECS_CounterfactualWorld_Template`.
   * Why it transfers: alignment scenarios that consider long horizon planning under climate uncertainty can reuse World L and World H style branches as environmental backdrops.
   * What changes: in Q121, the focus shifts from physical accuracy to the impact of different ECS worlds on AI decisions and safety constraints. ECS tension becomes part of a broader risk landscape.

---

## 9. TU roadmap and verification levels

This block explains how Q091 is positioned along the TU verification ladder and what the next measurable steps are.

### 9.1 Current levels

* **E_level: E1**

  * A concrete effective layer encoding for ECS has been specified, including:

    * state space observables,
    * mismatch components,
    * a combined tension functional,
    * a singular set and domain restriction,
    * an encoding class with fairness constraints.

  * At least two experiments have clear falsification conditions that apply to the encoding.

* **N_level: N1**

  * The narrative linking ECS, feedbacks, and tension is explicit and coherent at a basic level.
  * It is accessible to readers familiar with climate science but does not yet explore deeper structural links to other BlackHole problems.

### 9.2 Next measurable step toward E2

To move from E1 to E2 for Q091, at least one of the following should be implemented in practice.

1. A working tool that:

   * reads standardised datasets for historical forcing, temperature, and ocean heat content,
   * constructs states `m_data` in `M_reg`,
   * computes `Tension_ECS(m_data)` over a range of ECS values and model structures,
   * publishes the resulting tension profiles together with the encoding parameters.

2. A model ensemble analysis that:

   * uses `ECS_TensionFunctional` on a multi model ensemble,
   * documents how tension scores distribute between models that are consistent with emergent constraints and those that are not,
   * demonstrates that these findings are reproducible by independent groups.

These steps remain at the effective layer. They operate on observable summaries and model outputs, not on any hidden TU generative rules.

### 9.3 Long term role in the TU program

In the long term, Q091 is expected to serve as:

* the central node for thermodynamic_tension problems in the Earth system cluster,
* a test bed for encoding complex, partially constrained physical problems where both natural variability and anthropogenic forcing are present,
* a bridge between Earth system science and AI safety questions that rely on climate trajectories, by providing a disciplined way to talk about equilibrium responses and their uncertainty.

---

## 10. Elementary but precise explanation

Equilibrium climate sensitivity is a way of summarising a complex question in a single number:

* If we double the amount of carbon dioxide in the atmosphere and then wait a long time for the climate system to settle down, how much warmer will the planet become on average.

We know that:

* Without feedbacks, the answer would be a modest warming.
* In reality, feedbacks from water vapor, clouds, snow and ice, and other processes amplify the warming.
* Different models and different lines of evidence do not all agree on the exact amount.

In the Tension Universe view, we do not try to pick one magic number for ECS. Instead, we do three things.

First, we describe states.

* A state collects basic facts for a given scenario:

  * how strong the forcing is,
  * how much equilibrium warming is implied,
  * how the main feedbacks add up,
  * how well this picture matches observations.

Second, we measure mismatches.

* We check whether ECS in that state falls inside a reasonable reference band.
* We check whether model based and observation based ECS estimates agree.
* We check whether the feedbacks look physically plausible.

Each mismatch is turned into a nonnegative number. If everything lines up well, these numbers are small. If something is off, they grow.

Third, we combine mismatches into a tension score.

* The ECS tension is small when a state fits all of the following:

  * ECS is inside the reference band,
  * models and observations agree,
  * feedbacks stay inside plausible ranges.

* The tension becomes large when these pieces conflict.

We can then imagine:

* a low sensitivity world, where there is a narrow band of ECS values that keeps tension low as we add more data,
* a high sensitivity world, where any honest attempt to match observations and physics with high ECS values leads to persistent high tension.

This approach does not tell us which world is real. It does something more modest and controlled.

* It gives us a clear list of observables to watch.
* It provides experiments that can falsify bad ways of encoding climate sensitivity.
* It creates building blocks that other problems, such as tipping points and Anthropocene dynamics, can reuse.

Q091 is therefore the place in the Tension Universe where equilibrium climate sensitivity is turned from a single mysterious number into a structured tension problem that can be analysed, tested, and linked to many other questions.

---

## Tension Universe effective-layer footer

This page is part of the **WFGY / Tension Universe** S-problem collection.

### Scope of claims

* The goal of this document is to specify an effective-layer encoding of the named problem.
* It does not claim to prove or disprove the canonical problem statement in Section 1.
* It does not state any new theorem, inequality, or numerical bound beyond what is already established in the cited literature.
* It must not be cited as evidence that the corresponding scientific or mathematical problem has been solved.

### Effective-layer boundary

* All objects used here (state spaces `M`, observables, invariants, tension scores, counterfactual worlds) live at the effective layer of the Tension Universe framework.
* They are bookkeeping devices for reasoning and experiment design, not assertions about fundamental ontology.
* No axiom system, generative rule, or constructive definition of Tension Universe fields is specified or assumed in this page.
* Any mapping from raw data or model output to TU objects is part of an implementation level encoding choice and remains outside the scope of this document.

### Encoding and fairness

* All encoding choices for this problem (reference bands, weight libraries, penalty functions, and observation constraint mappings) are fixed in advance for the encoding key declared in the metadata.
* Changing these choices defines a new encoding key and a new object of study; such changes must not be merged with results obtained under the previous encoding.
* The experiments in Section 6 are required to use exactly the encoding class declared in Section 3.5 and in the TU Encoding and Fairness Charter.

### Falsifiability

* Each experiment in Section 6 specifies conditions under which this particular effective-layer encoding would be judged unstable, misaligned, or falsified.
* Falsifying an encoding does not falsify the canonical scientific problem; it only shows that a given TU representation is inadequate.
* Passing these experiments does not turn conjectural scientific claims into theorems; it only shows that the encoding behaves coherently under the tested conditions.

This page should be read together with the following charters:

* [TU Effective Layer Charter](../Charters/TU_EFFECTIVE_LAYER_CHARTER.md)
* [TU Encoding and Fairness Charter](../Charters/TU_ENCODING_AND_FAIRNESS_CHARTER.md)
* [TU Tension Scale Charter](../Charters/TU_TENSION_SCALE_CHARTER.md)
