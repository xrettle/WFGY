# Q101 · Equity premium puzzle

## 0. Header metadata

```txt
ID: Q101
Code: BH_ECON_EQUITY_PREM_L3_101
Domain: Economics
Family: asset_pricing
Rank: S
Projection_dominance: I
Field_type: incentive_field
Tension_type: incentive_tension
Status: Open
Semantics: continuous
E_level: E1
N_level: N1
Last_updated: 2026-01-26
```

---

## 1. Canonical problem and status

### 1.1 Canonical statement

In standard asset pricing, consider a representative investor with time-separable preferences, smooth consumption, and a stable attitude toward risk. Let

```txt
R_equity_real = long run average real return on a broad equity portfolio
R_safe_real   = long run average real return on a very low default risk asset
EP_obs        = R_equity_real - R_safe_real
```

Empirical studies for major developed economies, most famously the United States in the twentieth century, report values of `EP_obs` on the order of several percentage points per year.

In the same models, using plausible values for risk aversion, consumption growth volatility, and other macroeconomic quantities, the model-implied equity premium

```txt
EP_model = model_implied_equity_premium(gamma, consumption_risk, etc.)
```

is typically much smaller. For wide ranges of standard parameter values, the gap

```txt
EP_gap = EP_obs - EP_model
```

remains large. Matching the observed `EP_obs` often requires extreme risk aversion, implausible disaster probabilities, or other features that conflict with other data.

The equity premium puzzle is the claim that, within the canonical class of models and plausible parameter ranges, the observed equity premium appears too large relative to what the models predict.

### 1.2 Status and difficulty

The equity premium puzzle has remained an open challenge in macro-finance since its formal statement in the mid 1980s. It is not a single theorem, but a persistent mismatch between theory and data.

Partial lines of progress include:

* Habit formation and non time-separable preferences.
* Rare disaster models and heavy-tailed consumption or dividend risks.
* Incomplete markets and heterogeneous agents with limited risk sharing.
* Long run risks models, where growth and volatility have persistent components.
* Market frictions, borrowing constraints, and behavioral departures from full rationality.

None of these approaches has produced a universally accepted resolution. Many can reduce the gap in specific settings, but often at the cost of introducing parameters or mechanisms that are difficult to reconcile with other evidence.

The puzzle remains an organizing problem for research in asset pricing and macro-finance.

### 1.3 Role in the BlackHole project

Within the BlackHole S-problem collection, Q101 serves as:

1. The anchor node for macro-finance and asset-pricing puzzles where prices, risks, and preferences interact.
2. A prototype for incentive tensions where observed rewards and theoretical compensation for risk do not align.
3. A test bed for encoding:

   * long horizon return data,
   * model-implied premia and preference parameters,
   * regularity constraints on economic mechanisms,
   * a structured tension functional that separates “puzzle persists” from “puzzle dissolves” worlds.

### References

1. Rajnish Mehra and Edward C. Prescott, "The Equity Premium: A Puzzle", Journal of Monetary Economics, 1985.
2. John H. Cochrane, "Asset Pricing", Princeton University Press, second edition, 2005.
3. Rajnish Mehra (editor), "The Handbook of the Equity Risk Premium", Elsevier, 2008.
4. National Bureau of Economic Research (NBER), topic pages and working papers on asset pricing and the equity premium, various years.

---

## 2. Position in the BlackHole graph

This block records how Q101 sits in the BlackHole graph as a node with edges to other problems. Each edge has a one line reason that refers to components or tension structures defined in this file.

### 2.1 Upstream problems

These nodes provide foundations, tools, or conceptual frames that Q101 reuses at the effective layer.

* Q059 (BH_CS_INFO_THERMODYN_L3_059)
  Reason: Supplies information and thermodynamic style constraints reused when interpreting the cost of risk and reward inside the EquityPremium_Tension_Functional.

* Q091 (BH_EARTH_CLIMATE_SENS_L3_091)
  Reason: Shares a template for representing long horizon uncertainty and tail risks, which informs the construction of RegularityPenalty in Block 3.

* Q120 (BH_PHIL_VALUE_OF_INFORMATION_L3_120)
  Reason: Provides conceptual tools for how beliefs and information shape incentives, which are imported into the incentive_tension framing of Q101.

### 2.2 Downstream problems

These nodes directly reuse Q101 components or treat Q101 as a prerequisite.

* Q104 (BH_ECON_INEQUALITY_DYN_L3_104)
  Reason: Reuses EquityPremium_Tension_Functional and RiskPreferenceConsistency_Observer to model how persistent premia interact with wealth accumulation and inequality.

* Q105 (BH_COMPLEX_CRASHES_L3_105)
  Reason: Uses MacroFinance_Counterfactual_Template to define crash scenarios where premium dynamics and tail events generate systemic tension.

* Q121 (BH_AI_ALIGNMENT_L3_121)
  Reason: Adapts the incentive_tension and risk tail structure from Q101 as an analogy for misaligned reward schemes in AI agents.

### 2.3 Parallel problems

Parallel nodes share similar tension types but do not yet share concrete components.

* Q102 (BH_ECON_HOME_BIAS_L3_102)
  Reason: Encodes a related incentive_tension between diversification theory and observed portfolio choices, though it focuses on portfolio location rather than premia.

* Q048 (BH_COSMO_H0_TENSION_L3_048)
  Reason: Mirrors the pattern of a stable gap between model predictions and measured values, expressed as a structured tension, but in cosmology rather than macro-finance.

### 2.4 Cross-domain edges

These edges link Q101 to nodes in other domains that can reuse its components.

* Q032 (BH_PHYS_QTHERMO_L3_032)
  Reason: Can reuse the way Q101 translates between risk compensation, effective temperature style quantities, and incentive_tension.

* Q059 (BH_CS_INFO_THERMODYN_L3_059)
  Reason: Shares cross-domain methods for connecting economic reward structures to information processing and resource constraints.

* Q123 (BH_AI_INTERP_L3_123)
  Reason: Uses the decomposition of Tension_EP into mismatch and regularity terms as an interpretability pattern for latent "risk versus reward" circuits in AI models.

---

## 3. Tension Universe encoding (effective layer)

All content in this block remains at the effective layer. We describe:

* state spaces,
* observable fields and mismatch terms,
* invariants and tension scores,
* singular sets and domain restrictions.

We do not describe any hidden generative rule or any explicit mapping from raw time series into internal TU fields.

### 3.1 State space

We assume a semantic state space

```txt
M_econ
```

with the following interpretation at the effective layer.

Each state `m` in `M_econ` represents a coherent macro-finance configuration consisting of:

* a choice of asset pricing model from a finite library,
* a choice of data pack from a finite library of empirical summaries,
* a vector of long run summary statistics for returns and consumption,
* a parameter vector capturing the key preference and technology parameters for the chosen model.

Formally, we assume that for each state `m` there exist:

```txt
model(m) in L_model
data(m)  in L_data
theta(m) in Theta_model(model(m))
```

and a summary vector `S(m)` that contains the relevant long horizon statistics. We do not describe how `S(m)` is constructed from raw time series.

### 3.2 Model and data libraries

We define two finite libraries that are fixed at the level of this problem.

1. Model library

```txt
L_model = { M_1, M_2, ..., M_K }
```

Each `M_k` is a canonical asset pricing specification, for example:

* basic CRRA representative agent model,
* habit formation model,
* rare disaster augmented model,
* long run risk model,
* simple incomplete markets model.

For each `M_k` we specify a compact parameter domain

```txt
Theta_model(M_k)
```

that includes only parameter values considered economically plausible, such as:

* risk aversion in a bounded interval `[gamma_lo, gamma_hi]`,
* consumption growth parameters in ranges consistent with macro data,
* disaster probabilities and sizes in ranges supported by historical evidence.

The exact boundaries are fixed once for Q101 and do not depend on any particular dataset.

2. Data library

```txt
L_data = { D_1, D_2, ..., D_J }
```

Each `D_j` is a data pack that contains:

* long run summaries of equity and safe asset returns for a given country and period,
* matching summaries of consumption or income growth,
* basic metadata about sample length and data quality.

Examples include:

* United States twentieth century data,
* post war samples for developed economies,
* global panels of equity premia.

The choice of which countries and periods to include in `L_data` is fixed at the level of Q101.

3. Weighting rules and fairness constraints

We introduce nonnegative weights

```txt
w_model(k) >= 0,  sum over k w_model(k) = 1
w_data(j)  >= 0,  sum over j w_data(j)  = 1
```

that specify how models and datasets are aggregated when computing global invariants.

Fairness constraints:

* `L_model`, `L_data`, `Theta_model`, `w_model`, and `w_data` are chosen without using the size of the equity premium in any specific dataset.
* No weight or parameter bound is allowed to depend on the observed value of `EP_obs` in an individual dataset.
* Inside this file, these choices are treated as fixed and cannot be changed to fit particular data.

### 3.3 Observables and mismatch fields

We define the following effective observables for each state `m` in `M_econ`.

1. Observed returns

```txt
R_equity(m) = long run average equity return summary from data(m)
R_safe(m)   = long run average safe asset return summary from data(m)
EP_obs(m)   = R_equity(m) - R_safe(m)
```

These are long horizon summaries already contained in `S(m)`.

2. Model implied equity premium

```txt
EP_model(m) = model_implied_premium( model(m), theta(m), S(m) )
```

This is the equity premium implied by the chosen asset pricing model `model(m)` with parameters `theta(m)` and the data summaries in `S(m)`.

3. Equity premium mismatch

```txt
DeltaS_prem(m) = | EP_obs(m) - EP_model(m) |
```

This is nonnegative and is small when the model matches the observed equity premium for that state.

4. Preference consistency observable

We define an effective risk aversion observable

```txt
gamma_eff(m)
```

that represents the risk aversion level that the chosen model and state imply.

We choose fixed constants

```txt
gamma_lo > 0
gamma_hi > gamma_lo
```

representing a plausible range for effective risk aversion.

Preference mismatch is defined as

```txt
DeltaS_pref(m) =
  max( 0, gamma_eff(m) - gamma_hi )
+ max( 0, gamma_lo - gamma_eff(m) )
```

This penalizes parameter choices that imply either extremely low or extremely high effective risk aversion relative to this fixed band.

5. Regularity penalty

We introduce a nonnegative regularity penalty

```txt
RegularityPenalty(m) >= 0
```

that captures violations of simple macro-finance regularity conditions, such as:

* implausibly high disaster frequencies or sizes relative to `data(m)`,
* negative or unstable consumption growth,
* credible violations of basic no-arbitrage checks at the summary level.

The exact definition is part of the encoding and is fixed for Q101. It depends only on `model(m)`, `theta(m)`, and the summary data in `S(m)`.

### 3.4 Tension tensor and invariants

At the effective layer, we define the equity premium tension score as

```txt
Tension_EP(m) =
  a * DeltaS_prem(m)
+ b * DeltaS_pref(m)
+ c * RegularityPenalty(m)
```

with constants

```txt
a > 0
b > 0
c > 0
```

fixed once at the level of Q101 and not adjusted per dataset or model.

We embed this score into a TU-style tension tensor

```txt
T_ij(m) = S_i(m) * C_j(m) * Tension_EP(m) * lambda(m) * kappa
```

where:

* `S_i(m)` is a source factor representing the strength of the i-th economic signal or assumption in the configuration.
* `C_j(m)` is a receptivity factor representing the sensitivity of the j-th downstream component to the equity premium tension.
* `lambda(m)` is a convergence state factor from the TU core.
* `kappa` is a coupling constant for macro-finance incentive tension.

We also define a simple global invariant over the encoding:

```txt
I_EP_encoding =
  sum over j [ w_data(j) * Tension_EP( m_star(j) ) ]
```

where `m_star(j)` is a representative state for dataset `D_j`:

* `model(m_star(j))` is selected from `L_model`,
* `theta(m_star(j))` is chosen in `Theta_model(model(m_star(j)))`,
* the selection is made according to a fixed rule that does not depend on `EP_obs(m_star(j))` beyond what is allowed by the fairness constraints.

This invariant summarizes how much tension remains once we have attempted to reconcile each dataset with the model library.

### 3.5 Singular set and domain restrictions

Some states may fail to produce well defined or finite tension scores. We define the singular set

```txt
S_sing = { m in M_econ :
           Tension_EP(m) is undefined
           or not finite
           or any required observable is missing }
```

We impose the following domain restriction:

* All equity premium tension analysis is restricted to the regular set

  ```txt
  M_reg = M_econ \ S_sing
  ```

* If an experiment or protocol attempts to evaluate `Tension_EP(m)` for `m` in `S_sing`, the result is treated as "out of domain" and not as evidence about the underlying economic mechanisms.

---

## 4. Tension principle for this problem

This block states how Q101 is characterized as a tension problem in the TU framework.

### 4.1 Core tension principle

At the effective layer, the equity premium puzzle is encoded as a structured gap between:

1. Observed long run equity premia, `EP_obs(m)`.
2. Model implied premia, `EP_model(m)`, from a fixed library of canonical models with plausible parameters.
3. Regularity conditions on preferences and macro-finance variables.

The core principle is:

* If there exist states in `M_reg` that represent the real world and keep `Tension_EP(m)` small and stable across the model and data libraries, then the puzzle dissolves at the effective layer.
* If every such state that reduces `DeltaS_prem` to a small value forces either large preference mismatch or large regularity penalties, then the puzzle persists as high tension.

### 4.2 Low tension worlds

In a low tension world, there exist world-representing states `m` in `M_reg` such that:

```txt
DeltaS_prem(m)   is small
DeltaS_pref(m)   is small
RegularityPenalty(m) is small
Tension_EP(m)    <= epsilon_EP
```

for a fixed small threshold `epsilon_EP` that does not grow without bound as we extend the data library or refine parameter grids.

Moreover, these low tension states can be selected using rules that are consistent across countries and horizons under the fairness constraints.

### 4.3 High tension worlds

In a high tension world, for any admissible choice of models, parameters, and selection rules that respect the fairness constraints, world-representing states `m` in `M_reg` satisfy:

```txt
Tension_EP(m) >= delta_EP
```

for some strictly positive `delta_EP` that cannot be driven close to zero without:

* leaving the parameter domains `Theta_model`,
* or inducing very large regularity penalties.

At the level of the encoding, Q101 is the claim that the world belongs either to a low tension sector or to a high tension sector, and that this distinction can be probed without revealing any deep TU generative rules.

---

## 5. Counterfactual tension worlds

We now describe two counterfactual worlds purely through patterns of observables and tension scores.

### 5.1 World T (puzzle dissolves)

In World T:

1. For each major dataset `D_j` in `L_data`, there exists at least one state `m_j` in `M_reg` with:

   ```txt
   Tension_EP(m_j) <= epsilon_EP
   ```

   under selection rules that obey the fairness constraints.

2. As we extend the sample period or add comparable countries, the distribution of `Tension_EP(m_j)` values remains stable and clustered below `epsilon_EP`, once data quality differences are controlled for.

3. Lower tension is achieved by modest adjustments in model choice and parameters within `L_model` and `Theta_model`, without pushing `gamma_eff(m)` or disaster probabilities into extreme ranges.

4. The global invariant `I_EP_encoding` stays below a moderate bound:

   ```txt
   I_EP_encoding <= I_EP_low
   ```

   even when `L_data` is enlarged.

Interpretation: when models and data are enriched within reasonable bounds, the apparent puzzle can be explained away at the effective layer.

### 5.2 World F (puzzle persists)

In World F:

1. For many datasets `D_j` in `L_data`, every attempt to choose a state `m_j` in `M_reg` that makes `DeltaS_prem(m_j)` small leads to either:

   * large `DeltaS_pref(m_j)`, or
   * large `RegularityPenalty(m_j)`.

2. There exists a positive constant `delta_EP` such that for a large subset of datasets:

   ```txt
   Tension_EP(m_j) >= delta_EP
   ```

   for all admissible selections of `model(m_j)` and `theta(m_j)`.

3. Attempts to reduce tension by changing models or parameters within `L_model` and `Theta_model` produce strong instabilities across countries or horizons, rather than a coherent low tension pattern.

4. The global invariant satisfies:

   ```txt
   I_EP_encoding >= I_EP_high
   ```

   with `I_EP_high > I_EP_low`, and this inequality remains robust when reasonable extensions to `L_model` and `L_data` are made.

Interpretation: the equity premium puzzle reflects a structural mismatch between the canonical model library and real world risk and return patterns, rather than a thin artifact of calibration.

### 5.3 Interpretive note

These counterfactual worlds do not define or construct the internal TU fields from raw microeconomic data. They only state that, if such world models exist at the effective layer, then the observable tension patterns would fall into one of these two classes.

---

## 6. Falsifiability and discriminating experiments

This block specifies experiments and protocols that can test and potentially falsify the Q101 encoding. They do not solve the economic puzzle, but can reject specific forms of the tension functional or encoding class.

### Experiment 1: Cross country stability of equity premium tension

*Goal:*
Test whether the Q101 encoding can maintain a coherent low tension pattern across countries without violating fairness constraints.

*Setup:*

* Use a fixed model library `L_model` and data library `L_data` as defined in Block 3.
* Fix `Theta_model`, `w_model`, `w_data`, and the constants `gamma_lo`, `gamma_hi`, `a`, `b`, `c`, `epsilon_EP`, `I_EP_low`, and `I_EP_high` at the level of Q101.
* For each dataset `D_j`, prepare a small set of candidate states `m_jk` in `M_reg` corresponding to different models and parameter vectors in `Theta_model`.

*Protocol:*

1. For each dataset `D_j` and each candidate state `m_jk`, compute:

   ```txt
   Tension_EP(m_jk)
   ```

2. For each `D_j`, apply a selection rule that:

   * chooses one representative state `m_star(j)` among the `m_jk`,
   * uses only information permitted by the fairness constraints (for example, cross validation or pre-committed model choice),
   * does not adjust `w_model` or `w_data`.

3. Compute the global invariant:

   ```txt
   I_EP_encoding =
     sum over j [ w_data(j) * Tension_EP(m_star(j)) ]
   ```

4. Record the distribution of `Tension_EP(m_star(j))` across countries.

*Metrics:*

* Fraction of datasets `D_j` with `Tension_EP(m_star(j)) <= epsilon_EP`.
* Value of `I_EP_encoding`.
* Dispersion of `Tension_EP(m_star(j))` across countries.

*Falsification conditions:*

* If, for any reasonable selection rule that respects the fairness constraints, fewer than a fixed fraction `q` of datasets can be assigned states with `Tension_EP(m_star(j)) <= epsilon_EP`, and `I_EP_encoding` is persistently above `I_EP_high`, then the current encoding of `Tension_EP` and the associated parameter bounds is considered falsified at the effective layer.
* If small bounded changes in `Theta_model` or the regularity penalty produce arbitrarily large and irregular jumps in the pattern of `Tension_EP(m_star(j))` across countries, the encoding is considered unstable and rejected.

*Semantics implementation note:*
All observables are treated as real valued quantities on a continuous state space. No discrete or hybrid representation is introduced in this experiment.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. This experiment can reject the current Q101 encoding, but it does not by itself explain or resolve the equity premium puzzle.

---

### Experiment 2: Horizon dependence of equity premium tension

*Goal:*
Assess whether the encoding produces reasonable and stable tension patterns when the investment horizon changes.

*Setup:*

* Select a subset of datasets in `L_data` where long run return statistics are available at multiple horizons, for example 5 year, 10 year, and 30 year averages.
* For each chosen dataset `D_j` and each horizon `h` in `{5, 10, 30}`, define summary statistics and corresponding states `m_j(h)` in `M_reg`.

*Protocol:*

1. For each dataset `D_j` and each horizon `h`, compute:

   ```txt
   Tension_EP(m_j(h))
   ```

2. For each `D_j`, evaluate the range:

   ```txt
   Range_j = max over h Tension_EP(m_j(h))
             - min over h Tension_EP(m_j(h))
   ```

3. Summarize the set of `Range_j` values across all selected datasets.

*Metrics:*

* Distribution of `Tension_EP(m_j(h))` over horizons.
* Distribution of `Range_j` across datasets.
* Correlation between horizon and average tension level.

*Falsification conditions:*

* If for a large fraction of datasets the range `Range_j` exceeds a fixed bound `B_hor` that was set in advance, and there is no clear economic explanation for this horizon sensitivity, then the encoding is considered inconsistent with stable long run behavior and is rejected.
* If reducing `Range_j` requires re-tuning parameters or regularity penalties beyond the pre-set `Theta_model` domains or fairness constraints, the encoding is considered to rely on hidden adjustments and is rejected.

*Semantics implementation note:*
The same continuous field interpretation for economic observables is used at all horizons. The only change is the horizon over which summary statistics are computed.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. This experiment can show that a specific way of encoding horizon dependence is inadequate, without resolving the economic origin of the equity premium.

---

## 7. AI and WFGY engineering spec

This block describes how Q101 can be used as an engineering module for AI systems within the WFGY framework, at the effective layer.

### 7.1 Training signals

We define training signals that can be used to steer models when they reason about asset pricing and macro-finance.

1. `signal_equity_premium_gap`

   * Definition: a nonnegative signal proportional to `DeltaS_prem(m)` when the model constructs or evaluates macro-finance scenarios.
   * Purpose: penalize internal representations or outputs that imply equity premia far from what the chosen model and parameters would predict, when such models are assumed.

2. `signal_preference_consistency`

   * Definition: a signal based on `DeltaS_pref(m)` that increases when implied risk aversion moves outside `gamma_lo` and `gamma_hi`.
   * Purpose: discourage explanations that fit the equity premium only by invoking extreme risk aversion.

3. `signal_regular_behavior`

   * Definition: a signal derived from `RegularityPenalty(m)` that increases when disaster probabilities, consumption paths, or other macro quantities become inconsistent with the data library.
   * Purpose: enforce basic macro-finance regularity even when the model is trying to match observed premia.

4. `signal_global_tension`

   * Definition: a scalar signal equal or proportional to `Tension_EP(m)` for world-representing states.
   * Purpose: provide a compact tension indicator that can be minimized in tasks where consistency with a given asset pricing framework is part of the background.

### 7.2 Architectural patterns

We outline module patterns that reuse Q101 structures.

1. `EquityPremium_TensionHead`

   * Role: a head that reads internal representations of macro-finance contexts and outputs an estimate of `Tension_EP(m)`.
   * Interface:

     * Inputs: embeddings corresponding to model choice, parameter summaries, and data summaries.
     * Outputs: a scalar tension estimate and its decomposition into `DeltaS_prem`, `DeltaS_pref`, and `RegularityPenalty`.
   * Use: can be trained as an auxiliary task and then used at inference to detect when an answer relies on an inconsistent premium story.

2. `RiskPreferenceConsistency_Observer`

   * Role: an observer that infers `gamma_eff(m)` and related preference summaries from the model’s internal state.
   * Interface:

     * Inputs: internal representations of consumption paths, risk comparisons, and narrative explanations.
     * Outputs: an estimated `gamma_eff` and `DeltaS_pref`.
   * Use: can act as a filter to flag answers that implicitly require extreme risk attitudes.

3. `MacroFinance_Counterfactual_Gateway`

   * Role: a module that makes explicit whether the model is reasoning under a “puzzle dissolves” or “puzzle persists” assumption.
   * Interface:

     * Inputs: a flag or prompt indicating World T or World F and the relevant macro context.
     * Outputs: constrained internal states that are consistent with the chosen world’s tension pattern.
   * Use: keeps the model from mixing assumptions about the state of the puzzle within a single reasoning chain.

### 7.3 Evaluation harness

We sketch an evaluation harness for AI models that use Q101 components.

1. Task selection

   * Construct a benchmark of questions involving:

     * explanations of the equity premium,
     * tradeoffs between risk and return,
     * implications of different asset pricing models.

2. Conditions

   * Baseline condition:

     * Model answers questions without explicit tension heads or observers.
   * TU condition:

     * Model uses `EquityPremium_TensionHead` and `RiskPreferenceConsistency_Observer` to generate auxiliary signals, and is trained to avoid high tension states when the puzzle is assumed resolved.

3. Metrics

   * Consistency of explanations across countries and horizons.
   * Frequency of implicit extreme risk aversion in the explanations.
   * Stability of reasoning when toggling between “puzzle persists” and “puzzle dissolves” prompts.

### 7.4 60 second reproduction protocol

A minimal protocol to let external users experience the Q101 encoding.

* Baseline setup

  * Prompt: ask an AI system to explain why the equity premium is considered puzzling, including model predictions and observed returns, without mentioning tension or WFGY.
  * Observation: record whether the explanation mixes incompatible parameter choices or leaves unexplained gaps.

* TU encoded setup

  * Prompt: same question, but explicitly instruct the system to:

    * track `EP_obs`, `EP_model`, and `Tension_EP`,
    * avoid explanations that rely on extreme risk aversion or implausible disasters.
  * Observation: record whether the explanation becomes more structured, with clear statements about which pieces of the gap are being addressed.

* Comparison metric

  * Use a simple rubric that scores:

    * clarity about what is observed and what is modeled,
    * explicit treatment of parameter plausibility,
    * coherence when switching between different countries or periods.

* What to log

  * Prompts and full responses from both setups.
  * Any auxiliary `Tension_EP` and `DeltaS_pref` estimates produced by the heads.
  * These logs enable later inspection without exposing any internal TU generative rule.

---

## 8. Cross problem transfer template

This block lists reusable components produced by Q101 and the problems that can reuse them.

### 8.1 Reusable components produced by this problem

1. ComponentName: `EquityPremium_Tension_Functional`

   * Type: functional
   * Minimal interface:

     * Inputs: `macro_return_summary`, `model_spec`, `param_vector`
     * Output: `tension_value` (nonnegative scalar)
   * Preconditions:

     * `macro_return_summary` comes from a dataset in `L_data`.
     * `model_spec` is an element of `L_model`.
     * `param_vector` lies in the corresponding `Theta_model(model_spec)`.
     * The functional implements the definition of `Tension_EP` from Block 3.

2. ComponentName: `RiskPreferenceConsistency_Observer`

   * Type: observable
   * Minimal interface:

     * Inputs: `consumption_summary`, `param_vector`
     * Outputs: `gamma_eff_est`, `preference_mismatch_score`
   * Preconditions:

     * `consumption_summary` is compatible with the same dataset as `macro_return_summary`.
     * `param_vector` lies in the model’s parameter domain.
     * The mismatch score aligns with `DeltaS_pref` from Block 3.

3. ComponentName: `MacroFinance_Counterfactual_Template`

   * Type: experiment_pattern
   * Minimal interface:

     * Inputs: `model_class`, `data_pack`
     * Output: a pair `{World_T_protocol, World_F_protocol}` describing how to test whether tension is reducible or persistent.
   * Preconditions:

     * `model_class` can produce long run premia and preference summaries.
     * `data_pack` contains returns and macro quantities needed for Q101 style tension evaluation.

### 8.2 Direct reuse targets

1. Q104 (BH_ECON_INEQUALITY_DYN_L3_104)

   * Reused components: `EquityPremium_Tension_Functional`, `RiskPreferenceConsistency_Observer`.
   * Why it transfers: wealth and income inequality dynamics depend on the gap between returns to risk and safe assets; the same tension decomposition helps identify regimes where high premia persist.
   * What changes: additional observables for savings behavior and wealth distribution are added to the state space, but the core tension functional remains intact.

2. Q105 (BH_COMPLEX_CRASHES_L3_105)

   * Reused component: `MacroFinance_Counterfactual_Template`.
   * Why it transfers: systemic crashes can be studied as transitions between low and high tension macro-finance worlds, with Q101 serving as the baseline for normal conditions.
   * What changes: new components for network structure and contagion are added, and the experiments focus on how small shocks in premiums interact with fragile structures.

3. Q121 (BH_AI_ALIGNMENT_L3_121)

   * Reused components: `EquityPremium_Tension_Functional` (as an analogy) and `RiskPreferenceConsistency_Observer`.
   * Why it transfers: both asset pricing and AI alignment involve incentive structures where high rewards can be misaligned with underlying risks or constraints.
   * What changes: the economic observables are replaced by reward and safety observables in AI systems, but the pattern of decomposing tension into mismatch and regularity terms is preserved.

---

## 9. TU roadmap and verification levels

This block states where Q101 sits in the TU verification ladder and what the next measurable steps are.

### 9.1 Current levels

* E_level: E1

  * An effective layer encoding of the equity premium puzzle has been specified, including:

    * a finite model library and parameter domains,
    * a finite data library,
    * a precise tension functional,
    * explicit fairness constraints.

* N_level: N1

  * A coherent narrative has been given that explains the puzzle as an incentive tension between observed returns, model predictions, and regularity constraints.
  * Counterfactual worlds and experiments have been outlined.

### 9.2 Next measurable step toward E2

To move from E1 to E2, at least one of the following should be implemented:

1. A working prototype that:

   * instantiates `L_model`, `L_data`, and `Theta_model`,
   * computes `Tension_EP(m)` for selected states,
   * reports `I_EP_encoding` and horizon dependence patterns for real data.

2. A systematic study of synthetic macro-finance model worlds where:

   * some worlds are engineered to have resolving mechanisms for the puzzle,
   * others are constructed to keep high tension,
   * the Q101 encoding is tested for its ability to separate these cases.

Both steps can be carried out without revealing any deep TU generative rules.

### 9.3 Long term role in the TU program

In the longer term, Q101 is expected to function as:

* The reference node for economic and financial incentive tensions involving risk premia.
* A calibration site for how TU encodings handle the interaction between data, models, and regularity constraints in complex social systems.
* A bridge from macro-finance to other domains, such as inequality dynamics and AI alignment, through reusable tension structures.

---

## 10. Elementary but precise explanation

At an elementary level, the equity premium puzzle is about a simple question:

*Why do stocks seem to pay so much more than very safe assets, when our usual models say people should not need that much extra reward to hold them?*

Historically, in many countries, broad stock markets have earned much higher average returns than safe government bonds, even after adjusting for inflation. At the same time, measures of how risky consumption and income are suggest that investors should not require such a large extra return if they behave according to standard textbook models.

In those models, you can adjust a few knobs:

* how much people dislike risk,
* how smooth or volatile their consumption is,
* how often big disasters happen.

But even when you turn these knobs across wide plausible ranges, the model’s predicted equity premium often stays far below what the data show. If you force the model to match the observed premium, you may end up with people who are unrealistically afraid of risk, or with disasters that are far more frequent or severe than history supports.

In the Tension Universe view, instead of trying to prove or disprove a specific mathematical statement, we do the following:

1. We collect a small library of standard asset pricing models and a small library of datasets about returns and consumption.
2. For each combination of model and data, we compute three things:

   * the observed equity premium,
   * the premium that the model predicts,
   * how extreme the implied preferences and macro assumptions are.
3. We combine these into a single number called `Tension_EP`.

This tension number is small when:

* the model’s premium is close to the observed premium,
* the implied preferences sit in a reasonable range,
* the macro assumptions stay within regular patterns.

The number is large when you only get a good fit by stretching preferences or macro assumptions beyond what seems credible.

Then we imagine two kinds of worlds:

* In a “puzzle dissolves” world, as we improve models and data, we can find configurations where the tension number is small across countries and horizons.
* In a “puzzle persists” world, every attempt to get a small tension number somewhere makes it large somewhere else, or forces us into very implausible parameter regions.

Q101 does not tell us which world we live in. It does not solve the equity premium puzzle. What it does is:

* provide a precise way to talk about how big the mismatch is,
* make clear what counts as a fair way to compare models and data,
* create reusable tools that help analyze similar tensions in inequality, systemic risk, and AI alignment.

In this sense, Q101 is the macro-finance prototype for incentive tension problems in the Tension Universe framework.
