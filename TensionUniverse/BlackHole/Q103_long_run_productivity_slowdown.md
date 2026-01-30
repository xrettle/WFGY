<!-- QUESTION_ID: TU-Q103 -->
# Q103 · Long run productivity slowdown

## 0. Header metadata

```txt
ID: Q103
Code: BH_ECON_GROWTH_SLOW_L3_103
Domain: Economics
Family: Long run growth and structural change
Rank: S
Projection_dominance: I
Field_type: socio_technical_field
Tension_type: incentive_tension
Status: Open_problem_encoded
Semantics: hybrid
E_level: E1
N_level: N2
Last_updated: 2026-01-30
```

---

## 0. Effective layer disclaimer

All content in this file is written strictly at the effective layer of the Tension Universe (TU) framework.

* The goal is to specify an effective layer encoding of the long run productivity slowdown puzzle:

  * state spaces,
  * observables and fields,
  * mismatch and tension functionals,
  * an admissible encoding class for potentials and constraints,
  * falsifiable experiment templates,
  * reusable components for other problems and for AI systems.
* This file does not:

  * define or assume any particular deep axiom system or generative rule for TU,
  * introduce any TU field equations or dynamical laws in the mathematical physics sense,
  * claim that the canonical productivity slowdown problem is solved,
  * introduce new theorems beyond what is already established in the cited literature.

All tension statements in this file are quantified relative to a fixed admissible encoding class `E_prod` defined in Section 3.4. Changing the encoding class corresponds to a different effective layer model and should be treated as a different version of this document.

This page should be read together with the TU charters that define effective layer scope, encoding and fairness rules, and tension scale conventions. The footer lists the corresponding charter files.

---

## 1. Canonical problem and status

### 1.1 Canonical statement

Q103 concerns the puzzle often called the long run productivity slowdown in advanced economies.

In many high income economies, measured trend labor productivity and total factor productivity (TFP) growth appear to be lower in recent decades than during earlier post war periods. At the same time, there are strong claims about ongoing technological progress, digital transformation, and substantial investment in intangible capital.

The effective question is:

> Why has measured trend productivity growth in advanced economies been persistently lower than in earlier decades, even after accounting for known factors such as demographics, sectoral shifts, and measurement improvements?

Formulated as an open problem:

1. There is no widely accepted unified explanation that quantitatively reconciles:

   * observed slowdown in productivity growth,
   * technological and innovation indicators,
   * structural constraints such as demographics and climate.
2. Competing narratives exist:

   * “technological exhaustion” or fewer transformative inventions,
   * measurement errors and mismeasurement of digital and intangible output,
   * structural demand and policy failures,
   * deep institutional or distributional constraints.
3. No single model has achieved broad consensus as the correct resolution of the slowdown puzzle.

Q103 frames this as a structural puzzle rather than a narrow parameter estimation problem.

### 1.2 Status and difficulty

Key points about current status:

1. Measurement of productivity

   * Official statistics agencies publish detailed productivity indicators and multifactor productivity estimates.
   * There is substantial uncertainty about the correct treatment of quality change, digital services, and intangibles.

2. Structural explanations

   * Some authors argue that earlier growth was unusually strong due to one time general purpose technologies and that current growth is “normal”.
   * Others emphasize secular stagnation, chronic demand weakness, and an excess of savings over investment.
   * A third line stresses structural headwinds such as demographics, education, inequality, and environmental constraints.

3. Empirical difficulty

   * Data are noisy and cover only a limited number of long episodes.
   * Structural change and policy shifts overlap in time with technological change.
   * Causal identification is hard and many models fit subsets of the facts but not the whole picture.

At present there is no standard solution. The problem remains an open and debated issue in macroeconomics and complex socio technical systems.

### 1.3 Role in the BlackHole project

Within the BlackHole S collection, Q103 has three main roles:

1. It is the primary socio technical instance of an incentive tension problem, where:

   * there is a gap between apparent technological opportunity and realized aggregate output per worker,
   * the gap interacts with institutional and distributional structures.

2. It provides a macroeconomic anchor for several financial and policy puzzles:

   * Q101 (equity premium puzzle),
   * Q102 (home bias),
   * Q104 (inequality dynamics),
   * Q105 (systemic crashes),
     all of which need a structured view of long run productivity regimes.

3. It is a test case for Tension Universe encodings of:

   * hybrid state spaces that mix continuous macro variables and discrete regimes,
   * mismatch functionals between potential and actual outcomes,
   * constraint aware interpretations of long horizon economic trajectories.

### References

1. OECD, “OECD Compendium of Productivity Indicators”, OECD Publishing, multiple editions.
2. US Bureau of Labor Statistics, “Multifactor Productivity Trends” and related technical notes, various years.
3. Robert J. Gordon, “The Rise and Fall of American Growth”, Princeton University Press, 2016.
4. Lawrence H. Summers, “U.S. Economic Prospects: Secular Stagnation, Hysteresis, and the Zero Lower Bound”, Business Economics, 2014.
5. OECD, “The Future of Productivity”, OECD Publishing, 2015.

---

## 2. Position in the BlackHole graph

This block specifies how Q103 connects to other S problems. Each edge includes a one line reason pointing to concrete components or tension structures.

### 2.1 Upstream problems

Upstream nodes provide background structures and tools that Q103 reuses.

1. Q104 · Dynamics of wealth and income inequality (BH_ECON_INEQUALITY_DYN_L3_104)
   Reason: Inequality dynamics affect demand, human capital, and innovation incentives, which enter the state space and constraints used in Q103 productivity tension.

2. Q106 · Robustness of multilayer networks (BH_COMPLEX_NETWORK_ROBUST_L3_106)
   Reason: Firm, sector, and technology networks determine how innovation and productivity gains diffuse, and Q103 imports these network robustness concepts into its diffusion observables.

3. Q059 · Ultimate thermodynamic cost of information processing (BH_CS_INFO_THERMODYN_L3_059)
   Reason: Physical limits on information processing and communication provide a background ceiling for potential productivity, which Q103 treats as one component of its potential growth bounds.

### 2.2 Downstream problems

Downstream nodes reuse Q103 components or take Q103 outputs as inputs.

1. Q101 · Equity premium puzzle (BH_ECON_EQUITY_PREM_L3_101)
   Reason: Long run expected productivity growth is a key driver of fundamentals in asset pricing, and Q101 reuses the Q103 ProductivityTensionIndex as a macro input into risk return consistency checks.

2. Q102 · Home bias in portfolios (BH_ECON_HOME_BIAS_L3_102)
   Reason: Cross country differences in productivity regimes and slowdown patterns feed into perceived foreign versus domestic expected returns, using Q103 GrowthRegimeMap as part of the explanation.

3. Q109 · Global migration patterns (BH_SOC_MIGRATION_L3_109)
   Reason: Persistent productivity differentials across regions shape long run migration flows, and Q109 uses Q103 regime labels and tension patterns as drivers of migration incentives.

4. Q105 · Prediction of systemic crashes (BH_COMPLEX_CRASHES_L3_105)
   Reason: Long periods of subdued productivity growth can set up fragile financial and social structures, and Q105 reuses Q103 regime shift markers in its systemic risk experiments.

### 2.3 Parallel problems

Parallel nodes share similar tension structures but not direct component reuse.

1. Q098 · Anthropocene system dynamics (BH_EARTH_ANTHROPOCENE_L3_098)
   Reason: Both Q103 and Q098 track slow changes in coupled human systems, with tension between inherited models and observed large scale trajectories.

2. Q091 · Equilibrium climate sensitivity (BH_EARTH_CLIMATE_SENS_L3_091)
   Reason: Both require integrating uncertain long run response parameters from diverse data into an effective tension functional between models and reality.

3. Q092 · Climate tipping points (BH_EARTH_TIPPING_L3_092)
   Reason: Both reveal hidden thresholds where gradual trends accumulate into sharp regime changes in complex systems.

### 2.4 Cross domain edges

Cross domain edges link Q103 to nodes in other domains that can reuse its components.

1. Q093 · Full carbon cycle feedbacks (BH_EARTH_CARBON_CYCLE_L3_093)
   Reason: Carbon cycle constraints and mitigation strategies limit feasible productivity paths, and Q093 supplies constraint variables that Q103 imports into its potential growth calculations.

2. Q121 · AI alignment problem (BH_AI_ALIGNMENT_L3_121)
   Reason: Highly capable AI systems could reset productivity regimes; Q121 uses Q103 world scenarios as macro background when considering socio technical outcomes of aligned or misaligned systems.

3. Q124 · Scalable oversight and evaluation (BH_AI_OVERSIGHT_L3_124)
   Reason: Oversight of AI systems that influence macroeconomic policy needs a structured productivity tension map, which Q103 provides as the macro template for evaluation protocols.

---

## 3. Tension Universe encoding (effective layer)

All content in this block lives at the effective layer. We describe state spaces, observables, mismatch functionals, tension tensors, invariants, and singular sets. We do not describe any hidden generative rules or procedures that build internal TU fields from raw data.

### 3.1 State space

We assume an effective state space

```txt
M
```

with elements `m` representing macro productivity regime states for one or more economies.

Each `m` encodes, for a chosen country or group of countries and a specified time window:

* trend labor productivity growth `g_L` over that window,
* trend total factor productivity growth `g_TFP`,
* investment ratios in tangible and intangible capital,
* measures of innovation intensity such as R and D and patent or knowledge indicators,
* basic structural and constraint variables:

  * demographic profiles,
  * education and human capital indicators,
  * resource and environmental constraints,
  * institutional features relevant for long run growth.

We do not specify how these summaries are computed from micro data. We only assume that for any reasonable macro dataset and time window, there exist states `m` in `M` that encode the corresponding summaries.

Because Q103 mixes continuous macro variables with discrete regime labels, we treat:

* numerical aggregates such as growth rates and ratios as continuous coordinates,
* regime labels such as “post war boom”, “IT revolution”, “slowdown regime” as discrete tags attached to states.

### 3.2 Observables and fields

We introduce the following observables and fields on `M`.

1. Actual productivity growth observable

```txt
g_actual(m)
```

* Input: a state `m`.
* Output: a real number representing the trend productivity growth rate observed in the encoded time window and economy or group.
* This includes both labor productivity and TFP as appropriate for the chosen definition.

2. Potential productivity growth observable

```txt
g_potential(m)
```

* Input: a state `m`.
* Output: a real number representing an encoded estimate of feasible productivity growth given the technology, capital, demographics, and constraints in `m`.
* This is not a forecast model in the deep sense. It is an effective layer summary consistent with known physical, technological, and demographic limits and with observed historical patterns in periods judged to be high productivity regimes.

The mapping `m -> g_potential(m)` is part of the admissible encoding class `E_prod` described in 3.4.

3. Innovation effort index

```txt
I_innov(m)
```

* Input: a state `m`.
* Output: a nonnegative scalar summarizing innovation intensity, such as combined R and D effort, intangible investment, and diffusion indicators for general purpose technologies.

4. Constraint vector

```txt
C_constraints(m)
```

* Input: a state `m`.
* Output: a finite dimensional vector capturing binding constraints on productivity:

  * demographic dependency ratios,
  * climate and environmental policies,
  * resource limitations,
  * institutional rigidity measures.

5. Regime label field

```txt
R_regime(m)
```

* Input: a state `m`.
* Output: a discrete label that places the state in a coarse regime class:

  * for example “catch up growth”, “frontier boom”, “slowdown and plateau”.

### 3.3 Mismatch observables

We define mismatch observables that measure how far actual outcomes deviate from encoded potential under given constraints.

1. Core productivity gap

```txt
DeltaS_prod(m) = max(0, g_potential(m) - g_actual(m))
```

Properties:

* `DeltaS_prod(m) >= 0` for all `m` in the regular domain.
* `DeltaS_prod(m) = 0` if actual growth reaches or exceeds the encoded potential growth value.

2. Innovation to outcome mismatch

```txt
DeltaS_innov(m) = f_innov(I_innov(m), g_actual(m))
```

where `f_innov` is a nonnegative function that increases when innovation effort is high but measured productivity growth remains low relative to historical benchmarks for similar levels of effort.

3. Constraint consistency mismatch

```txt
DeltaS_const(m) = f_const(C_constraints(m), g_potential(m))
```

where `f_const` increases if encoded potential growth is inconsistent with the constraint vector, for example if it implies unphysical resource use or demographic profiles that contradict actual trends.

The precise forms of `f_innov` and `f_const` are part of the encoding choice but must satisfy:

* nonnegativity,
* boundedness for realistic parameter ranges,
* monotone behavior in intuitive directions (higher mismatch gives higher value).

### 3.4 Admissible encoding class and fairness conditions

To avoid arbitrary adjustments that erase tension, we restrict the encoding to an admissible class `E_prod` with the following properties.

1. Fixed reference library

There exists a finite library of reference regimes

```txt
L_ref = { m_ref(1), ..., m_ref(K) }
```

covering well documented historical episodes of:

* high productivity growth with known drivers,
* moderate growth,
* clear slowdown periods.

For each reference element, both `g_actual` and `g_potential` are fixed by convention, and these values define scale and calibration for the problem.

2. Constraint aware potentials

For any state `m`, `g_potential(m)` must be chosen from a rule that:

* respects physical and demographic constraints encoded in `C_constraints(m)`,
* is consistent with the reference library when `m` is close to some `m_ref(k)` in observable space.

3. No outcome dependent tuning for potentials

The rule for `g_potential(m)` cannot depend on the realized value of `g_actual(m)` for that same state except through fixed calibration parameters shared across all states. In particular, no state specific rescaling is allowed that would automatically make `DeltaS_prod(m)` small.

4. Stability under refinement

If a sequence of encodings

```txt
m(k)
```

refines a macro history by using smaller time windows or more detailed sector decomposition, the sequence of potentials

```txt
g_potential(m(k))
```

must remain within a bounded interval that is consistent with the reference library and constraints, rather than diverging or oscillating arbitrarily.

5. Fixed mismatch functionals and weights

The functions `f_innov` and `f_const`, the combination weights `w_prod`, `w_innov`, `w_const`, and any thresholds such as `epsilon_prod` and `delta_prod` used later are also part of the encoding class `E_prod`:

* they are fixed ex ante for a given version of this file,
* they are shared across all countries, time windows, and datasets covered by that encoding,
* they cannot be retuned on a per state or per window basis to reduce `DeltaS_innov`, `DeltaS_const`, or `DeltaS_total`,
* they cannot be tuned directly on observed slowdown patterns or on the distribution of `DeltaS_total` itself.

All tension statements in later blocks are implicitly quantified over encoding choices that satisfy these fairness conditions.

### 3.5 Tension tensor

We define an effective semantic tension tensor consistent with the general TU core form.

```txt
T_ij(m) = S_i(m) * C_j(m) * DeltaS_total(m) * lambda_regime(m) * kappa_prod
```

where:

* `S_i(m)` are source factors, indexed by sectors or innovation domains, that measure how strongly each source contributes to productivity potential in the encoded state.

* `C_j(m)` are receptivity factors, indexed by adoption channels such as labor markets, financial systems, and institutional structures, that capture how sensitive each channel is to potential gains.

* `DeltaS_total(m)` is a combined mismatch:

  ```txt
  DeltaS_total(m) = w_prod * DeltaS_prod(m)
                    + w_innov * DeltaS_innov(m)
                    + w_const * DeltaS_const(m)
  ```

  with fixed nonnegative weights `w_prod`, `w_innov`, and `w_const` chosen once for all states in the encoding and included in `E_prod`.

* `lambda_regime(m)` is a regime factor that depends on `R_regime(m)` and indicates whether the system is in a convergent, plateau, or stagnation like state.

* `kappa_prod` is a constant that sets the overall scale of productivity tension in this problem and is part of `E_prod`.

Weights and scale factors are fixed ex ante and cannot be tuned per state. They are part of the encoding specification and must be documented in any concrete implementation.

In this file, `T_ij(m)` is used only as a bookkeeping tensor to embed Q103 into the TU bookkeeping space. No field equation or dynamical law for `T_ij` is specified or assumed here.

### 3.6 Invariants and effective constraints

We introduce two invariants to summarize tension patterns across states.

1. Cross economy tension spread

```txt
I_spread = sup over m in M_reg of DeltaS_prod(m)
           - inf over m in M_reg of DeltaS_prod(m)
```

where `M_reg` is the regular part of the state space defined below.

This invariant measures how wide the productivity tension band is across economies and time windows within a given encoding.

2. Regime persistence indicator

For a sequence of states `m(t)` that track a single economy over time, we define:

```txt
I_persist = limsup over long horizons of DeltaS_prod(m(t))
```

measured over sliding windows of fixed length. If `I_persist` is small for many economies, the encoding suggests no deep slowdown puzzle. If it is consistently large in episodes that line up with measured slowdowns, the encoding supports the existence of a structural puzzle.

Both invariants are always evaluated under a fixed encoding in `E_prod`. Changing the encoding class changes the values of these invariants and corresponds to a new effective layer model and a new version of this file.

### 3.7 Singular set and domain restrictions

Some states contain periods where macro aggregates are ill defined or dominated by shocks, for example:

* major wars,
* hyperinflation or monetary collapse,
* extreme natural disasters or pandemics where data series are broken.

We define a singular set:

```txt
S_sing = { m in M : g_actual(m) is undefined or not stable,
                    or C_constraints(m) is not meaningfully specified }
```

Domain restriction:

* All tension analysis, including `DeltaS_prod`, `DeltaS_innov`, `DeltaS_const`, and invariants `I_spread`, `I_persist`, is restricted to:

  ```txt
  M_reg = M \ S_sing
  ```

Handling rule:

* States in `S_sing` are labelled as singular regimes and may be used to document data gaps or crises but are not used to draw conclusions about the presence or absence of a structured slowdown puzzle.

This is a restricted domain treatment of singularities. No attempt is made to regularize tension values inside `S_sing`. Instead those states are explicitly marked as out of scope for Q103 tension evaluation.

---

## 4. Tension principle for this problem

This block states how Q103 is characterized as a tension problem in TU language.

### 4.1 Core tension statement

At the effective layer, Q103 asserts that the productivity slowdown puzzle can be understood as tension between:

1. encoded potential productivity growth paths that respect technological, demographic, and physical constraints, and
2. actual measured productivity growth paths, given a fair encoding class `E_prod`.

Using the mismatch `DeltaS_prod(m)` and combined mismatch `DeltaS_total(m)`, the principle can be expressed as:

* In a world where there is no deep slowdown puzzle, for most states `m` that represent advanced economy regimes in `M_reg`, there exist admissible encodings such that `DeltaS_total(m)` stays in a low band consistent with historical high growth episodes or with plausible physical and demographic limitations.
* In a world where a genuine structural slowdown exists, even when encodings are refined and calibrated using `E_prod`, a large set of states exhibit persistent high `DeltaS_total(m)` values that cannot be removed without violating constraints or reference consistency.

Q103 does not assert which pattern holds in the actual world. It only sets up a structured way to talk about these patterns.

### 4.2 Refinement and stability

Consider a refinement sequence of encodings for a given economy and broad time period, indexed by `k`:

```txt
m(k)
```

where each refinement either:

* uses narrower time windows within the same era,
* introduces more detailed sectoral decomposition,
* incorporates improved measurement of intangibles or constraints.

The encoding class `E_prod` requires that:

* `g_potential(m(k))` and `DeltaS_total(m(k))` remain within bounded intervals that respect:

  * constraint awareness,
  * reference library calibration.

Q103 tension principle distinguishes two patterns.

1. Low tension pattern

   There exists a refinement path such that:

   ```txt
   sup over k of DeltaS_total(m(k)) <= epsilon_prod
   ```

   for some small threshold `epsilon_prod` that depends on the era and the precision of data but does not grow without bound as more detail is added.

2. High tension pattern

   For every refinement path consistent with `E_prod`, for some economies and eras:

   ```txt
   liminf over k of DeltaS_total(m(k)) >= delta_prod
   ```

   for some strictly positive `delta_prod`. In this case, the slowdown puzzle remains visible even after careful constraint and measurement corrections.

Both `epsilon_prod` and `delta_prod` are treated as fixed parts of the encoding class `E_prod`:

* they are chosen before looking at the detailed pattern of `DeltaS_total` for any specific dataset,
* they are not tuned post hoc to make particular slowdown episodes appear or disappear.

Q103 uses these thresholds only as qualitative separators between low tension and high tension patterns, not as claims about exact numerical values in the real world.

---

## 5. Counterfactual tension worlds

We now describe two counterfactual worlds at the effective layer.

* World T: little or no structural long run productivity slowdown.
* World F: persistent, structural productivity slowdown in advanced economies.

These are not complete models of reality. They are templates for how observables and tension patterns differ.

### 5.1 World T (no deep slowdown)

In World T:

1. Potential and actual alignment

   * For states `m_T` representing major advanced economies across long periods, admissible encodings can be found such that:

     ```txt
     DeltaS_prod(m_T) is small and does not show long periods of sustained elevation
     ```

     once constraints are properly accounted for.

2. Innovation and growth coupling

   * High values of `I_innov(m_T)` tend to coincide with higher `g_actual(m_T)` in a way that matches patterns in the reference library episodes.
   * The mismatch `DeltaS_innov(m_T)` stays within a band similar to earlier high growth eras.

3. Constraint consistency

   * As environmental and demographic constraints become tighter, `g_potential(m_T)` naturally adjusts downward, and `DeltaS_const(m_T)` stays small.
   * There is no need to posit unexplained headwinds beyond those encoded constraints.

4. Regime transitions

   * Changes in `R_regime(m_T)` from boom to plateau are accompanied by observables that explain the change in `DeltaS_total(m_T)` without leaving a large unexplained residual.

Overall, in World T the productivity slowdown puzzle dissolves when constraints and measurement are handled correctly. Tension is mostly explained by known mechanisms.

### 5.2 World F (structural slowdown)

In World F:

1. Persistent gap

   * For many advanced economies, admissible encodings still show periods where:

     ```txt
     DeltaS_prod(m_F) stays above a positive threshold delta_prod for several decades
     ```

     even after constraints and measurement corrections.

2. Innovation tension

   * High `I_innov(m_F)` coexists with modest `g_actual(m_F)` in a way that pushes `DeltaS_innov(m_F)` into a sustained high band.
   * Innovation appears to concentrate in domains with limited aggregate impact, or adoption mechanisms are blocked.

3. Constraint mismatch

   * Attempts to justify low `g_actual(m_F)` purely by tightening constraints lead to large `DeltaS_const(m_F)` values or conflicts with other observable facts.
   * There appears to be slack: potential growth under reasonable constraints is higher than realized growth.

4. Regime stickiness

   * Once economies enter slowdown regimes in `R_regime(m_F)`, sequences `m_F(t)` show high `I_persist`. The system appears trapped in high tension states that are not easily exited.

In this world, the productivity slowdown remains a genuine macro puzzle in the TU sense. Tension cannot be removed without changing basic assumptions about behavior, institutions, or technology.

### 5.3 Interpretive comment

Q103 does not claim that the actual world is World T or World F. Instead it specifies patterns that would be observed in each, measured through:

* the size and persistence of `DeltaS_total`,
* the behavior of invariants `I_spread` and `I_persist`,
* the compatibility of encodings with constraints and reference episodes.

Evidence can then be discussed in terms of how close observed data and models are to each world template.

---

## 6. Falsifiability and discriminating experiments

This block describes experiments and protocols that can falsify particular Q103 encodings at the effective layer. They do not solve the economic problem. They only test whether a given encoding class `E_prod` and chosen functionals behave in a reasonable and stable way.

### Experiment 1: Historical panel productivity tension profiling

*Goal*

Assess whether a single encoding within `E_prod` produces a coherent tension profile across advanced economies and decades, or whether it behaves in an unstable or trivial way.

*Setup*

* Data:

  * Panel data for a set of advanced economies over several decades, including:

    * trend labor productivity and TFP estimates,
    * measures of innovation effort and investment,
    * demographic indicators and resource or environmental policies.
* Encoding:

  * Fix one encoding in `E_prod` that specifies:

    * how `g_potential(m)` is computed from observed constraints and technology proxies,
    * how `DeltaS_innov` and `DeltaS_const` are defined,
    * fixed weights `w_prod`, `w_innov`, and `w_const`,
    * reference library `L_ref`,
    * and any thresholds used for classification.
  * The same encoding must be used for all countries and all time windows in the panel in a given experiment run. Using different encodings for different subsets of the panel counts as changing the problem specification and corresponds to a separate experiment.

*Protocol*

1. Select a set of country period windows, for example ten year windows covering the post war period to the present for each economy.
2. For each window, construct a state `m_data` in `M` that encodes the macro summaries for that economy and period, then project it to `M_reg` if it is not in the singular set.
3. Compute `DeltaS_prod(m_data)`, `DeltaS_innov(m_data)`, `DeltaS_const(m_data)`, and `DeltaS_total(m_data)` for all regular states.
4. Compute the invariants:

   * `I_spread` over the full panel,
   * approximate `I_persist` for each economy by tracking long sequences of windows.
5. Examine whether:

   * `DeltaS_total(m_data)` is almost always near zero (trivial encoding),
   * `DeltaS_total(m_data)` is unstable or highly sensitive to small changes in encoding parameters,
   * `DeltaS_total(m_data)` exhibits structured patterns that match known slowdown episodes.

*Metrics*

* Distribution of `DeltaS_total` across country period states.
* Cross economy variance of `DeltaS_total` in each decade.
* Persistence statistics for `DeltaS_total` above a chosen tension threshold.
* Sensitivity of these quantities to modest changes in encoding parameters that remain within `E_prod`.

*Falsification conditions*

If, for all reasonable parameter choices within `E_prod`, one of the following holds:

1. `DeltaS_total(m_data)` remains extremely close to zero for almost all states even when clear slowdown episodes are included, then the encoding is considered trivial and rejected.
2. Small changes in encoding parameters cause `DeltaS_total(m_data)` to jump between very different profiles with no clear mathematical or empirical justification, then the encoding is considered unstable and rejected.
3. `DeltaS_total(m_data)` systematically fails to reflect widely acknowledged high growth and slowdown periods in any interpretable way, then the encoding is considered misaligned and rejected.

Rejecting the encoding means that this particular choice of potentials, constraints, mismatch functionals, and weights is not a valid Q103 effective layer representation.

*Semantics implementation note*

All observables in this experiment are represented as hybrid states: continuous aggregates for growth rates and indexes, plus discrete tags for countries and time windows. The computations are carried out using standard real valued arithmetic and conventional time series aggregation without introducing any additional discrete structure.

*Boundary note*

Falsifying a TU encoding does not solve the canonical slowdown problem. Passing this experiment also does not prove that the canonical problem has been solved. It only shows that, for the tested data, a particular encoding behaves in a stable and interpretable way.

---

### Experiment 2: Constraint adjusted potential growth scenarios

*Goal*

Test whether plausible constraint aware potential growth models can explain observed slowdown by themselves, or whether a persistent unexplained tension remains under realistic assumptions.

*Setup*

* Data:

  * Historical data for one or more reference economies with well studied slowdown episodes.

* Models:

  * A small family of potential growth mappings consistent with `E_prod`, each defined by a function:

    ```txt
    g_potential(m; theta)
    ```

    with parameters `theta` that capture different views about:

    * demographic headwinds,
    * environmental and climate policies,
    * institutional and educational constraints.

* Parameter ranges:

  * Parameter ranges are restricted by external evidence, for example demographic projections and policy targets, and cannot be freely tuned for each window.

*Protocol*

1. For each window and economy, encode a state `m_data` with observed `g_actual`, constraint vector `C_constraints`, and innovation indicators.

2. For each model choice `theta` within allowed ranges, compute `g_potential(m_data; theta)` and then:

   ```txt
   DeltaS_prod(m_data; theta) = max(0, g_potential(m_data; theta) - g_actual(m_data))
   ```

3. Compute combined tension `DeltaS_total(m_data; theta)` using the same functions and weights as in Experiment 1.

4. For each economy, track how `DeltaS_total(m_data; theta)` behaves across pre slowdown and slowdown windows under each model.

5. Compare:

   * whether there exists any `theta` that keeps `DeltaS_total` low in both eras,
   * whether models that keep tension low in the slowdown era contradict physical, demographic, or institutional constraints.

*Metrics*

* For each model `theta`, the maximum `DeltaS_total(m_data; theta)` during slowdown windows.
* For each model `theta`, differences in `DeltaS_total` between high growth and slowdown eras.
* Indicators of whether parameter values required to fit slowdown periods remain within external constraint ranges.

*Falsification conditions*

* If every model in the admissible family `g_potential(m; theta)` that keeps `DeltaS_total` low during slowdown periods requires parameter values that contradict external evidence about constraints, the encoding is considered misaligned and rejected.
* If the only way to keep `DeltaS_total` low is to select different parameter values for each window in a way that effectively depends on `g_actual(m_data)` or on the realized `DeltaS_total(m_data; theta)` pattern, then the encoding is rejected for violating the no outcome dependent tuning rule and is no longer in `E_prod`.
* If for some models within the allowed ranges `DeltaS_total` is consistently high in slowdown periods while remaining low in earlier periods, this counts as evidence for a genuine structural slowdown pattern under that encoding, not as falsification.

In particular, parameter choices must be fixed at the level of economies or eras according to external evidence, not at the level of individual windows to chase low tension scores.

*Semantics implementation note*

The models are implemented using continuous real valued functions of constraints and parameters. Regime labels remain discrete tags used for interpretation, and no additional structure beyond standard real analysis and time aggregation is introduced.

*Boundary note*

Falsifying a TU encoding in this experiment does not solve the canonical slowdown problem. Passing this experiment also does not identify a unique correct economic theory. It only shows that, under the tested assumptions, a particular constraint based encoding behaves coherently.

---

## 7. AI and WFGY engineering spec

This block describes how Q103 can be used as an engineering module within AI systems and WFGY style semantic infrastructure, still at the effective layer.

### 7.1 Training signals

We define several training signals derived from Q103 observables.

1. `signal_productivity_gap`

   * Definition: a nonnegative signal proportional to `DeltaS_prod(m)` for states where the model is discussing long term growth.
   * Purpose: discourage reasoning that implicitly equates potential and actual growth when there is evidence of a gap, and encourage explicit acknowledgment of the puzzle.

2. `signal_innovation_tension`

   * Definition: a signal related to `DeltaS_innov(m)`, activated when narratives describe strong innovation with weak aggregate productivity gains.
   * Purpose: make the model mark and track situations where innovation and growth are decoupled.

3. `signal_constraint_alignment`

   * Definition: a penalty based on `DeltaS_const(m)` when potential growth is claimed without referencing constraints.
   * Purpose: encourage explanations that explicitly connect growth to demographic, environmental, and institutional realities.

4. `signal_regime_shift_awareness`

   * Definition: a signal tied to changes in `R_regime(m)` over time in a narrative.
   * Purpose: reward the model for identifying and labeling regime shifts, for example transitions from high growth to slowdown, rather than treating history as uniform.

### 7.2 Architectural patterns

We outline module patterns that integrate Q103 features into AI systems.

1. `ProductivityTensionHead`

   * Role: given a hidden representation of a macroeconomic context, output an estimate of `DeltaS_total` and a simple decomposition into `DeltaS_prod`, `DeltaS_innov`, and `DeltaS_const`.
   * Interface:

     * Inputs: context embeddings plus tags indicating that the topic involves long run growth.
     * Outputs: scalar tension estimate and a short vector of component scores.

2. `RegimeLabeler`

   * Role: label narrative segments or data windows with regime tags consistent with Q103 regime concepts.
   * Interface:

     * Inputs: time ordered macro descriptions or data summaries.
     * Outputs: regime labels and confidence scores.

3. `ConstraintOverlayModule`

   * Role: adjust baseline growth narratives by overlaying explicit constraint vectors from Q093 and other nodes, and recomputing `g_potential` at the effective layer.
   * Interface:

     * Inputs: baseline growth descriptors, constraint vectors.
     * Outputs: adjusted potential growth estimates and implied tension scores.

These modules operate within the AI system and use Q103 encodings as internal structure. They do not expose or depend on any deep TU generative rules.

### 7.3 Evaluation harness

We propose an evaluation harness to test whether adding Q103 modules improves AI reasoning about growth.

1. Tasks

   * Explain historical growth patterns and slowdown episodes for specific economies.
   * Compare growth experiences across countries.
   * Evaluate hypothetical policy scenarios that claim to restore high productivity growth.

2. Conditions

   * Baseline condition:

     * The model answers these tasks with no explicit access to Q103 modules.
   * Q103 condition:

     * The model uses ProductivityTensionHead, RegimeLabeler, and ConstraintOverlayModule as auxiliary components and can access Q103 derived signals.

3. Metrics

   * Structural coherence: frequency of explanations that distinguish potential from actual growth and mention constraints.
   * Tension awareness: frequency with which the model explicitly notes puzzles where innovation and productivity are decoupled.
   * Stability: robustness of answers under counterfactual prompts that adjust constraints or regimes.

### 7.4 60 second reproduction protocol

A minimal user facing protocol to observe the impact of Q103 encoding.

* Baseline setup

  * Prompt: “Explain why productivity growth in advanced economies appears to have slowed in recent decades compared to the post war period. Discuss possible explanations.”
  * Observation: record whether the answer mixes possible causes without distinguishing between potential and actual growth, and whether it treats the slowdown as a random fact or as a structured puzzle.

* TU encoded setup

  * Prompt: same content, with an additional instruction:

    * “Organize your answer using the idea of a gap between potential productivity growth and actual measured productivity, and be explicit about constraints and innovation effort.”
  * Observation: record whether the answer introduces concepts that mirror `DeltaS_prod`, `DeltaS_innov`, `DeltaS_const`, and regime shifts, even if it does not use these names.

* Comparison metric

  * Use a rubric that scores:

    * clarity of the potential versus actual distinction,
    * explicit treatment of constraints,
    * recognition of persistent puzzles rather than one shot shocks.

* What to log

  * Prompts,
  * full answers,
  * any auxiliary tension estimates produced by internal Q103 modules.

These logs can be inspected later to evaluate whether Q103 encodings improve reasoning quality.

---

## 8. Cross problem transfer template

This block lists reusable components produced by Q103 and the problems that reuse them.

### 8.1 Reusable components produced by this problem

1. ComponentName: `ProductivityTensionIndex`

   * Type: functional
   * Minimal interface:

     * Inputs:

       * `g_actual`,
       * `g_potential`,
       * `I_innov`,
       * `C_constraints`.
     * Output:

       * scalar `DeltaS_total` and component scores `DeltaS_prod`, `DeltaS_innov`, `DeltaS_const`.
   * Preconditions:

     * Inputs are coherent summaries for a defined time window and economy,
     * potential values come from an encoding in `E_prod`.

2. ComponentName: `GrowthRegimeMap`

   * Type: field
   * Minimal interface:

     * Inputs:

       * country or region identifier,
       * time coordinates,
       * macro indicators.
     * Output:

       * regime label `R_regime` and associated regime parameters such as typical growth rates and tension ranges.
   * Preconditions:

     * Data cover a sufficiently long period to identify regimes.

3. ComponentName: `ConstraintAdjustedPotentialModel`

   * Type: experiment_pattern or ai_module
   * Minimal interface:

     * Inputs:

       * baseline potential mapping,
       * constraint vector,
       * parameter set `theta` within allowed ranges.
     * Output:

       * adjusted `g_potential` values consistent with constraints,
       * implied changes in `DeltaS_prod` and `DeltaS_total`.
   * Preconditions:

     * Constraints are specified and calibrated using external evidence,
     * parameter ranges respect external physical and demographic limits.

### 8.2 Direct reuse targets

1. Q101 · Equity premium puzzle

   * Reuses:

     * `ProductivityTensionIndex`.
   * Why:

     * Long run expected productivity growth and its uncertainty feed into asset returns. Q101 can use `DeltaS_total` as a macrostate input when assessing consistency between observed returns and fundamentals.
   * What changes:

     * Q101 maps productivity tension to risk premia tension, possibly adding financial sector observables.

2. Q102 · Home bias in portfolios

   * Reuses:

     * `GrowthRegimeMap`.
   * Why:

     * Persistent differences in regimes and tension across countries influence perceived relative returns and risk. Investors may prefer domestic markets if foreign regimes are perceived as high tension or hard to interpret.
   * What changes:

     * Q102 combines regime labels with investor information sets and institutional frictions.

3. Q104 · Dynamics of wealth and income inequality

   * Reuses:

     * `ConstraintAdjustedPotentialModel`.
   * Why:

     * Distributional changes can alter potential growth through human capital and demand channels. Q104 can use Q103 potentials as feedback inputs when studying inequality growth loops.
   * What changes:

     * Q104 attaches distributional states and feedback rules to constraint vectors.

4. Q105 · Prediction of systemic crashes

   * Reuses:

     * `GrowthRegimeMap` and selected outputs of `ProductivityTensionIndex`.
   * Why:

     * Systemic crashes often occur after prolonged periods of misaligned expectations and macro tension. Q105 uses regime shifts and rising `DeltaS_total` as early warning inputs.
   * What changes:

     * Q105 mixes productivity tension with financial leverage and network fragility measures.

5. Q098 · Anthropocene system dynamics

   * Reuses:

     * `ConstraintAdjustedPotentialModel`.
   * Why:

     * Anthropocene dynamics involve joint evolution of human activity and planetary constraints. Q098 combines productivity potentials with environmental trajectories to assess feasible development paths.
   * What changes:

     * Environmental state becomes central in the constraint vector, and planetary boundaries shape long horizon potential.

---

## 9. TU roadmap and verification levels

This block describes Q103 verification status and future steps at the effective layer.

### 9.1 Current E and N levels

* E_level: E1

  * A coherent effective layer encoding has been specified:

    * state space `M`,
    * observables `g_actual`, `g_potential`, `I_innov`, `C_constraints`,
    * mismatch functionals,
    * admissible encoding class `E_prod` with explicit fairness constraints,
    * tension tensor structure,
    * falsifiable experiment templates.
  * No specific numerical implementation or published dataset is assumed here.

* N_level: N2

  * The narrative of the slowdown puzzle is explicitly tied to:

    * a gap between potential and actual growth,
    * constraint aware potentials,
    * persistent high tension in some worlds.
  * Counterfactual worlds T and F are described in terms of patterns in `DeltaS_total` and invariants rather than slogans.

These E1 and N2 labels are intended to match the corresponding definitions in the TU Effective Layer and Encoding and Fairness charters listed in the footer.

### 9.2 Next measurable steps toward higher levels

To move toward E2 and beyond, at least one of the following should be realized:

1. Construct and document a working reference implementation of `E_prod` for a small panel of advanced economies, including:

   * transparent definitions of `g_potential`,
   * explicit parameter ranges and constraint mappings,
   * published `DeltaS_total` profiles for major slowdown episodes.

2. Run both experiments in Section 6 with public data and publish:

   * raw data used,
   * code for computing tension metrics,
   * resulting figures and tables.

Independent repetition by other researchers would then open a path toward E3.

### 9.3 Long term role in TU

Longer term, Q103 is expected to:

* provide a standard socio technical template for puzzles where:

  * there is a belief in high potential performance,
  * actual performance stagnates or slows,
  * multiple overlapping explanations exist,
* support cross links between macroeconomics, environmental constraints, and AI policy nodes,
* act as a reference case for AI systems:

  * to practice tension aware reasoning about complex historical trajectories,
  * to avoid oversimplified narratives that ignore constraints or persistent puzzles.

---

## 10. Elementary but precise explanation

This block explains Q103 to non specialists while remaining aligned with the effective layer encoding.

Over the last decades many advanced economies have seen slower growth in output per worker than in the decades after the Second World War. At the same time, there are obvious signs of rapid technological change: computers, the internet, smartphones, digital platforms, and new kinds of services.

The question behind Q103 is simple to state but hard to answer:

> If technology is still advancing, why does measured productivity growth look slower for many rich countries?

In Tension Universe language, we do not try to pick a single cause. Instead we ask how to describe the puzzle itself in a precise way.

We imagine a big space of macro states. Each state summarizes, for some country and time period:

* how fast productivity actually grew,
* how strong innovation and investment were,
* what the demographics, environmental limits, and institutions looked like.

For each state we ask two things:

1. How fast could productivity reasonably have grown, given the technology and constraints at that time?
   This is `g_potential`.

2. How fast did it actually grow?
   This is `g_actual`.

We then define a gap:

```txt
DeltaS_prod = max(0, g_potential - g_actual)
```

If this number is small, there is not much puzzle. If it is large for many countries and periods, the puzzle is strong. We also track two related gaps:

* cases where innovation effort is high but growth is low,
* cases where claimed potential growth seems inconsistent with basic constraints like demographics or climate policy.

Q103 then draws two kinds of worlds.

* In one kind of world, once we look carefully at constraints and measurement, the gaps stay small. The slowdown looks more like an illusion caused by misreading the data or by new limits coming into play.
* In the other kind of world, the gaps stay large even after careful correction. The slowdown is a real structural puzzle, not just a statistical accident.

We do not decide which world we live in. Instead Q103 provides:

* a way to talk about the slowdown in terms of observable gaps rather than only stories,
* a way to test whether particular explanations and encodings behave in a stable and honest way,
* building blocks that other problems, such as financial puzzles and climate policy questions, can reuse.

It should be read as a precise language for measuring and organizing this puzzle at the effective layer, not as a claim that TU already captures the deepest truth about economic growth or the universe.

---

## Tension Universe effective-layer footer

This page is part of the **WFGY / Tension Universe** S problem collection.

### Scope of claims

* The goal of this document is to specify an effective layer encoding of the long run productivity slowdown puzzle.
* It does not claim to prove or disprove the canonical statement in Section 1.
* It does not introduce any new theorem beyond what is already established in the cited literature.
* It should not be cited as evidence that the corresponding open problem has been solved.

### Effective-layer boundary

* All objects used here (state space `M`, observables, invariants, tension scores, counterfactual worlds, AI modules) live at the TU effective layer.
* No assumption is made about any specific TU axiom system, deep generative rule, or field equation behind these effective objects.
* The tension tensor `T_ij` is used only as a bookkeeping device for Q103 and does not define any dynamical law in this file.
* Any statement about “worlds” in this document refers to patterns in observables and tension scores, not to metaphysical claims about reality.

### Encoding and fairness conventions

* All potentials, mismatch functionals, weights, and thresholds are chosen inside the admissible encoding class `E_prod` described in Section 3.4.
* For a given version of this file, a single encoding choice is used across all states, countries, and time windows in any experiment.
* Per window or per state tuning of potentials or mismatch functions to erase tension is outside `E_prod` and invalidates the corresponding experiment.
* Invariants such as `I_spread` and `I_persist` are always interpreted relative to a fixed encoding class. Changing the encoding class changes their values and corresponds to a new effective model.

### Engineering and AI use

* The AI and WFGY engineering spec in Section 7 describes how Q103 can be used as a module to improve reasoning about productivity and growth.
* Using this module in AI systems does not by itself prove that the system is safe, aligned, or economically correct.
* Q103 provides structured training signals and evaluation tasks. It does not replace domain expertise, empirical work, or policy analysis.

### Charters

This page should be read together with the following charters:

* [TU Effective Layer Charter](../Charters/TU_EFFECTIVE_LAYER_CHARTER.md)
* [TU Encoding and Fairness Charter](../Charters/TU_ENCODING_AND_FAIRNESS_CHARTER.md)
* [TU Tension Scale Charter](../Charters/TU_TENSION_SCALE_CHARTER.md)
* [TU Global Guardrails](../Charters/TU_GLOBAL_GUARDRAILS.md)
