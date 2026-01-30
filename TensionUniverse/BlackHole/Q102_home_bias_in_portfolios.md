# Q102 · Home bias in portfolios

## 0. Header metadata

```txt
ID: Q102
Code: BH_ECON_HOME_BIAS_L3_102
Domain: Economics
Family: International finance / portfolio choice
Rank: S
Projection_dominance: I
Field_type: incentive_field
Tension_type: incentive_tension
Status: Open_problem_encoded
Semantics: hybrid
E_level: E1
N_level: N1
Last_updated: 2026-01-30
```

---

## 0. Effective layer disclaimer

All statements in this entry are made strictly at the effective layer of the Tension Universe (TU) framework.

* The object of this file is to define an **effective layer encoding** of the home bias puzzle in international portfolios.
* The file only introduces:

  * state spaces and observables,
  * tension functionals,
  * invariants and experiment templates,
  * and reusable engineering components.
* The file does **not**:

  * solve the canonical home bias problem,
  * prove or disprove any theorem about optimal portfolios,
  * introduce any new economic theorem beyond the cited literature,
  * define any TU generative rule or partial differential equation,
  * construct any explicit mapping from raw micro data to internal TU fields,
  * claim that we know which counterfactual tension world the real world belongs to.

Throughout this entry:

* “World,” “state,” and “configuration” refer to **effective layer models**.
* Statements about “low tension” or “high tension” are always conditional on:

  * a fixed encoding class for Q102,
  * fixed fairness constraints,
  * and the declared domain of observables.

This document must not be cited as evidence that the home bias puzzle has been solved. It is only a specification of how to **encode and measure** home bias tension inside the TU program.

Any substantial change to the encoding class for Q102, including changes in benchmark libraries, cost functions, parameter bounds, or global thresholds, corresponds to a new version of this file and must be recorded as such.

---

## 1. Canonical problem and status

### 1.1 Canonical statement

In standard frictionless international asset pricing models, a representative investor who can costlessly trade all risky assets is predicted to hold a globally diversified portfolio. In the simplest benchmark, each country’s equity is held in proportion to its share of world market capitalization. In more elaborate models, optimal holdings reflect correlations, risk premia, and hedging demands, but still imply substantial foreign diversification for most investors.

Empirically, portfolios display a strong and persistent **home bias**:

* Investors hold a much larger fraction of their risky portfolios in domestic assets than global diversification benchmarks would suggest.
* This pattern holds for households, pension funds, mutual funds, and at the country level, across many decades and market regimes.
* The bias remains even after controlling for simple measures of currency risk, transaction costs, and basic capital controls.

Canonical questions include:

1. How large is the gap between observed domestic weights and global diversification benchmarks, once we control for standard frictions and risk factors?
2. To what extent can information frictions, institutional constraints, and behavioral preferences explain this gap?
3. Does there exist a unified and measurable way to separate “explained” home bias from residual anomalous tension?

Within BlackHole Q102, the problem is treated as an **incentive_tension** question at the effective layer. The goal is not to solve home bias in general. The goal is to encode it as a measurable mismatch between observed portfolios and plausible friction adjusted benchmarks under explicit fairness constraints.

### 1.2 Status and difficulty

Key empirical and theoretical facts:

* Cross country data show that domestic shares of equity portfolios are often far above what global diversification would predict. This holds in major markets such as the United States, Japan, and Europe, and is even more pronounced in some emerging markets.
* Classical work documented both severe home bias and high turnover in foreign holdings. This combination is difficult to reconcile with simple stories based only on fixed costs or lack of interest in foreign assets.
* International macro puzzles, including imperfect risk sharing and consumption correlations that are too low, are tightly related to home bias in portfolios.

A large literature has explored explanations based on:

* information asymmetries,
* transaction and monitoring costs,
* institutional and regulatory restrictions,
* background risk and non traded assets,
* behavioral preferences, such as familiarity, salience, or patriotism.

Despite many partial successes, there is no consensus single explanation that quantitatively accounts for the full magnitude and persistence of home bias across different countries and time periods. The problem is structurally difficult because:

* multiple mechanisms can produce similar patterns,
* relevant frictions and preferences are hard to measure directly,
* equilibrium outcomes involve higher order interactions among many agents and institutions,
* global datasets are heterogeneous in coverage and quality.

From the TU perspective, Q102 remains an open problem. This file records an **E1 level encoding** of the puzzle and an **N1 level narrative** around incentive tension. It does not claim that the encoding is unique or complete, and it does not claim that friction only stories are sufficient.

### 1.3 Role in the BlackHole project

Within the BlackHole S problem collection, Q102 serves three roles.

1. It is a central example of **incentive_tension** in economic systems. Investors face local incentives, frictions, and perceptions that pull their portfolios away from global risk sharing benchmarks.

2. It provides a bridge between micro level portfolio decisions and macro level outcomes, such as:

   * systemic risk concentration,
   * international imbalance patterns,
   * and cross country differences in exposure to common shocks.

3. It supplies reusable components for:

   * encoding hidden exposures and their deviation from benchmarks,
   * decomposing observed anomalies into friction driven and residual parts,
   * testing how far a tension based description can go without committing to a unique structural model of preferences or expectations.

All three roles are restricted to the effective layer. Q102 does not specify any TU level explanation for why home bias exists. It only provides tools for measuring and organizing the puzzle within the TU ecosystem.

### References

1. French, K. R., and Poterba, J. M. (1991). “Investor Diversification and International Equity Markets.” American Economic Review, Papers and Proceedings, 81(2), 222–226.
2. Tesar, L. L., and Werner, I. M. (1995). “Home Bias and High Turnover.” Journal of International Money and Finance, 14(4), 467–492.
3. Obstfeld, M., and Rogoff, K. (2000). “The Six Major Puzzles in International Macroeconomics. Is There a Common Cause?” In NBER Macroeconomics Annual 2000, Volume 15, 339–412.
4. Coeurdacier, N., and Rey, H. (2013). “Home Bias in Open Economy Financial Macroeconomics.” Journal of Economic Literature, 51(1), 63–115.

---

## 2. Position in the BlackHole graph

This block records how Q102 is placed among Q001 to Q125 as a node in the BlackHole graph. All edges are expressed as Q identifiers and short reasons, so that the graph can be aggregated as an adjacency list.

### 2.1 Upstream problems

These nodes provide prerequisites or background structures that Q102 relies on at the effective layer.

* Q101 · Equity premium puzzle
  Reason: Supplies baseline risk and return anomalies that any home bias tension functional must be consistent with, especially for risky assets and their premia.

* Q059 · Ultimate thermodynamic cost of information processing
  Reason: Provides a template for modeling information processing and monitoring costs as effective energy like quantities that influence portfolio choices.

* Q104 · Dynamics of wealth and income inequality
  Reason: Provides macro constraints on wealth distribution and saving behavior, which limit feasible aggregate portfolio positions across countries.

### 2.2 Downstream problems

These nodes reuse Q102 components or treat Q102 as a prerequisite.

* Q105 · Prediction of systemic crashes
  Reason: Uses Q102’s investor exposure fields and tension scores to characterize regional concentration risk and the build up of systemic fragility.

* Q106 · Robustness of multilayer networks
  Reason: Reuses Q102’s portfolio network representation as one instance of a multilayer exposure graph, where home bias shapes link strengths.

* Q110 · Evolution of institutions
  Reason: Uses Q102’s friction decomposition to study how institutional rules and regulations evolve in response to persistent incentive tension in international portfolios.

### 2.3 Parallel problems

These share similar tension types but do not directly reuse Q102 components.

* Q104 · Dynamics of wealth and income inequality
  Reason: Both study persistent deviations from simple benchmark distributions, framed as incentive_tension and risk_tail_tension on economic states.

* Q107 · Mechanisms of large scale collective action
  Reason: Both involve mismatches between individually optimal local choices and globally efficient configurations in large populations.

### 2.4 Cross domain edges

These connect Q102 to problems in other domains that reuse its patterns.

* Q059 · Ultimate thermodynamic cost of information processing
  Reason: Reuses the mapping from information frictions to effective costs as a way to parameterize energetic limits of information processing in physical systems.

* Q121 · Alignment of advanced AI systems
  Reason: Treats local portfolio preferences versus global diversification as an analogy for local objective functions versus global alignment targets in AI.

* Q123 · Scalable interpretability of AI models
  Reason: Uses Q102’s hidden exposure versus benchmark exposure pattern as an analogue for hidden internal states of AI models that diverge from user specified targets.

No external URLs are used in this block. All references are internal to the BlackHole S problem graph.

---

## 3. Tension Universe encoding (effective layer)

This block defines the effective layer encoding of home bias in TU terms. It only introduces observable state spaces, fields, functionals, invariants, and a bookkeeping tensor. It does not specify any hidden TU generative rules or mappings from raw data to internal TU fields.

### 3.1 State space

We introduce an effective state space

```txt
M
```

where each element `m` in `M` represents a portfolio world configuration at a given horizon. The configuration is summarized at the level of investor groups and country level asset categories.

For each state `m` in `M` we assume:

* A finite set of investor groups

  ```txt
  G = { g_1, g_2, ..., g_G }
  ```

  for example households, pension funds, mutual funds, insurance companies.

* A partition of risky assets into domestic and foreign categories for each country, represented by

  ```txt
  A_dom
  A_for
  ```

* A time horizon index `h` that specifies the relevant period, such as one year.

The state `m` can be seen as a point in a finite dimensional hybrid space that contains:

```txt
w_{g,a}(m)     portfolio weights by group and asset category
mu_{g,a}(m)    expected or average returns
sigma_{g,a}(m) risk measures
C_info(g; m)   information related costs for each group
C_inst(g; m)   institutional or regulatory costs
env(m)         environment descriptors, such as market size and openness
```

The continuous quantities live in a real vector space, and the indices, group labels, and asset categories are discrete. This is the sense in which the metadata declares `Semantics: hybrid`.

We do not describe how these quantities are computed from raw observations. We only assume that for any configuration we use in an experiment, there exists a corresponding state `m` in `M` that encodes those summary values.

### 3.2 Portfolio observables

We define effective observables that summarize domestic and foreign exposures, benchmark allocations, and cost terms for each group `g` in `G`.

1. Domestic weight

```txt
w_dom(m; g) = sum over a in A_dom of w_{g,a}(m)
```

2. Foreign weight

```txt
w_for(m; g) = sum over a in A_for of w_{g,a}(m)
```

We assume that for each group `g` in `G`:

```txt
w_dom(m; g) >= 0
w_for(m; g) >= 0
w_dom(m; g) + w_for(m; g) <= 1
```

so that there may also be safe or non risky assets outside this split.

3. Global benchmark weight

We define a benchmark domestic weight `w_global_star(m; g)` through an admissible benchmark rule. Consider a finite library of benchmark functions

```txt
Lib_benchmark = { B_1, B_2, ..., B_K }
```

Each `B_k` maps environment descriptors to benchmark weights:

```txt
w_global_star(m; g) = B_k( env(m); g )
```

with the following fairness constraints.

* Each `B_k` can depend on variables such as:

  * world market capitalization shares,
  * correlations among asset classes,
  * macro level risk measures,
  * ex ante properties of investor groups.
* Each `B_k` cannot depend on:

  * realized individual portfolio weights `w_{g,a}(m)` for the same horizon,
  * realized individual returns `mu_{g,a}(m)` for group `g` at that horizon.

In any given encoding class, one function `B_k` is chosen once for all states and all groups, before inspecting their specific portfolio weights or home bias gaps. This prevents benchmark rules that silently fit the observed home bias.

4. Cost observables

We introduce cost observables for each group `g`:

```txt
C_info(m; g) >= 0
C_inst(m; g) >= 0
```

Interpretation:

* `C_info(m; g)` is the effective cost for group `g` of monitoring and understanding foreign assets to the precision required for investing.
* `C_inst(m; g)` is the effective cost induced by institutions or regulations, such as reporting requirements, capital restrictions, and tax differentials.

These costs are produced by functions in finite libraries

```txt
Lib_info = { C_info^1, ..., C_info^P }
Lib_inst = { C_inst^1, ..., C_inst^Q }
```

with constraints analogous to `Lib_benchmark`:

* Cost functions can depend on environment descriptors and ex ante investor group characteristics.
* Cost functions cannot depend on realized portfolio weights for the same group and period.
* For a given encoding class, one function from each library is chosen and fixed before calculating tension.

### 3.3 Gap and normalized gap observables

The raw home bias gap for group `g` in state `m` is

```txt
Gap_raw(m; g) = w_dom(m; g) - w_global_star(m; g)
```

To compare across different scales of domestic holdings, we introduce a normalized gap:

```txt
epsilon_w > 0    fixed small constant

Gap_norm(m; g) = Gap_raw(m; g) / ( w_global_star(m; g) + epsilon_w )
```

The constant `epsilon_w` is fixed once for Q102 and does not vary across experiments, groups, or datasets. This prevents division by zero and ensures that extreme cases with very small benchmark weights do not dominate the tension score through trivial scaling.

### 3.4 Cost based explainability observable

We compress information and institutional costs into a single effective explainable gap for each group `g`:

```txt
k_info >= 0
k_inst >= 0
k_info + k_inst <= 1

Gap_explain(m; g) = k_info * C_info(m; g) + k_inst * C_inst(m; g)
```

The constants `k_info` and `k_inst` are fixed once for Q102. They do not depend on group, period, or experiment. They control how much home bias can be considered explainable by costs alone inside this encoding class.

### 3.5 Incentive mismatch and aggregate tension

The effective incentive mismatch for group `g` is

```txt
DeltaS_incentive(m; g) =
    max( 0, abs( Gap_norm(m; g) ) - Gap_explain(m; g) )
```

This is always nonnegative and satisfies:

* `DeltaS_incentive(m; g) = 0` if normalized home bias can be fully explained by the encoded cost terms.
* `DeltaS_incentive(m; g) > 0` if the home bias gap remains large even after subtracting costs.

We define weights `pi_g(m)` that describe the relative importance of each group, for example based on wealth or total assets under management. They satisfy:

```txt
pi_g(m) >= 0    for all g in G
sum over g in G of pi_g(m) = 1
```

Fairness constraint for group weights:

* The rule that maps observable group properties to `pi_g(m)` must be specified as part of the encoding class.
* The rule may depend on ex ante quantities such as total assets or wealth shares.
* The rule must not depend on `Gap_norm(m; g)`, `Gap_raw(m; g)`, or `DeltaS_incentive(m; g)` themselves.

The aggregate home bias tension for state `m` is

```txt
Tension_HB(m) =
  sum over g in G of
    pi_g(m) * DeltaS_incentive(m; g)
```

By construction, `Tension_HB(m)` is nonnegative and reflects the residual incentive tension after explicit frictions have been taken into account.

### 3.6 Resolution parameter and multi scale behavior

To avoid trivializing home bias by coarse aggregation, we introduce an integer resolution parameter `r` that indexes the level of detail in the asset classification. For each `r` we obtain a derived state `m_r` that uses a classification with `r` domestic and foreign asset buckets per country, such as sectors or market segments.

For each `m_r` we can compute:

```txt
Tension_HB_r(m) = Tension_HB(m_r)
```

We are interested in how `Tension_HB_r(m)` behaves as `r` increases over a finite range of resolutions that are empirically accessible.

* In a world where home bias is mostly explained by costs and measurement limits, the sequence `Tension_HB_r(m)` should remain bounded and ideally drift toward a controlled band as more detail is incorporated.
* In a world with deep structural anomalies, the sequence may stabilize at a positive lower bound even as resolution improves.

No particular rate of convergence is assumed. Only the qualitative behavior of `Tension_HB_r(m)` over finite ranges of `r` is used as an observable.

### 3.7 Singular set and domain restrictions

Some states can make the above observables undefined or non finite. For example:

* `w_global_star(m; g)` may be undefined if environment descriptors are inconsistent.
* Costs can be undefined or infinite for certain groups.
* Portfolio weights may not sum to a meaningful total if data are incomplete.

We define the singular set:

```txt
S_sing = {
  m in M :
  some w_global_star(m; g) undefined or not finite, or
  some C_info(m; g) or C_inst(m; g) undefined or not finite, or
  some w_dom(m; g) or w_for(m; g) outside [0, 1]
}
```

Effective analysis is restricted to the regular set:

```txt
M_reg = M \ S_sing
```

Within `M_reg` all observables and the tension functional are well defined and finite. No ad hoc truncation or clipping is applied. States in `S_sing` are simply not used in Q102 experiments.

### 3.8 Global invariant and tensor embedding

For families of states drawn from data or simulations, we define a global home bias invariant. Let `D_panel` be a finite collection of states that represent observed configurations across countries and time. Let `w_state(m_data)` be nonnegative weights that sum to one over `D_panel` and are specified in advance, without reference to `Tension_HB_r`.

For a fixed resolution `r` we define:

```txt
I_HB_encoding(r) =
  sum over m_data in D_panel of
    w_state(m_data) * Tension_HB_r(m_data)
```

The function `I_HB_encoding(r)` is part of the encoding and provides a coarse global summary of residual home bias tension at resolution `r`.

To connect Q102 to the general TU bookkeeping tensor, we embed `Tension_HB` into a rank two tensor:

```txt
T_ij_HB(m) =
  S_i(m) * C_j(m) * Tension_HB(m) * lambda_HB(m) * kappa_HB
```

where:

* `S_i(m)` are source factors representing the strength of the i-th economic or informational signal in configuration `m`,
* `C_j(m)` are receptivity factors representing the sensitivity of the j-th downstream component to home bias tension,
* `lambda_HB(m)` is a convergence state factor at the effective layer for Q102,
* `kappa_HB` is a coupling constant for this incentive tension channel.

In this file, `T_ij_HB` is used only as a bookkeeping device to make contact with other TU components. No dynamical law or field equation for `T_ij_HB` is specified.

---

## 4. Tension principle for this problem

This block states how Q102 is described as a tension problem in TU terms at the effective layer. The focus is on the behavior of `Tension_HB_r(m)` and `I_HB_encoding(r)` under a fixed encoding class and fairness constraints.

### 4.1 Core tension functional

The core functional has already been defined as:

```txt
Tension_HB(m) =
  sum over g in G of
    pi_g(m) * max( 0,
                   abs( Gap_norm(m; g) ) - Gap_explain(m; g) )
```

with:

* `Gap_norm(m; g)` describing the size of home bias relative to a global benchmark,
* `Gap_explain(m; g)` describing how much bias is justified by encoded information and institutional costs,
* `pi_g(m)` weighting investors by the scale of their activities based on ex ante observables.

Properties at the effective layer:

1. `Tension_HB(m) >= 0` for all `m` in `M_reg`.
2. `Tension_HB(m) = 0` if for every group, normalized home bias is fully explained by the chosen cost structure.
3. `Tension_HB(m)` increases as the share of groups with residual unexplained gaps increases.
4. Given the fairness constraints on benchmark and cost functions, and on `pi_g(m)`, `Tension_HB(m)` cannot be made arbitrarily small on a fixed dataset by adjusting parameters inside a single encoding class.

### 4.2 Home bias as a low tension principle

At the effective layer, a friction driven explanation of home bias corresponds to the following low tension principle.

Define an encoding class `E_HB` that consists of:

* a choice of benchmark function `B_k` from `Lib_benchmark`,
* a pair of cost functions from `Lib_info` and `Lib_inst`,
* constants `k_info`, `k_inst`, `epsilon_w`,
* a rule for group weights `pi_g(m)` based on ex ante observables,
* a set of tolerance functions `epsilon_HB(r)`, `tau_low(r)`, and `tau_high(r)` for relevant resolutions,
* and fixed constants used in experiments, such as `B_hor` for horizon ranges.

All elements above must be fixed **before** inspecting the pattern of home bias gaps and tension scores on a given dataset.

We say that a world is low tension with respect to Q102 and encoding class `E_HB` if there exist states `m` in `M_reg` that represent the observed portfolio configurations within this encoding class and satisfy:

```txt
Tension_HB_r(m) <= epsilon_HB(r)
```

for all resolutions `r` in a finite range `R_obs` of interest, where:

* `epsilon_HB(r)` is a nonnegative function of `r` fixed as part of `E_HB`,
* `epsilon_HB(r)` does not grow without bound over the resolutions used in empirical analysis.

The low tension principle for Q102 is:

> For realistic encoding classes in `E_HB`, the observed world admits representative states with small and controlled home bias tension across relevant resolutions, when portfolios are evaluated against friction aware benchmarks.

This principle is a statement about the existence of low tension states in `M_reg` under a fixed encoding class. It is not a claim that the underlying structural cause of home bias is known.

### 4.3 Persistent high tension and failure of friction only explanations

If home bias cannot be explained by any encoding in `E_HB` that respects the fairness constraints, then we expect to see persistent high tension in the effective observables.

Formally, there exists a positive constant `delta_HB` and a nonempty subset of states `W_obs` in `M_reg` such that for every encoding in `E_HB` and for all `m` in `W_obs` and resolutions `r` in `R_obs` we have:

```txt
Tension_HB_r(m) >= delta_HB
```

The constant `delta_HB` acts as a lower bound on residual tension. Its existence within the effective layer signals that friction only explanations, as encoded in `E_HB`, are insufficient.

This statement does not claim that home bias is unexplainable. It only reports that, under the specified encoding constraints, there remains a nontrivial residual incentive tension that must be attributed to deeper factors such as preferences, beliefs, or structural constraints that are not modeled in Q102.

---

## 5. Counterfactual tension worlds

We now describe two counterfactual worlds at the effective layer. They differ only in the observable patterns of home bias tension, not in any hidden TU structure.

### 5.1 World T: friction aligned portfolios

World T represents a world in which home bias is mostly explained by information and institutional frictions captured in Q102’s observables and encoding class.

Characteristics:

1. For most investor groups and countries, domestic overweight is moderate and closely aligned with reasonable cost measures. We have:

   ```txt
   abs( Gap_norm(m_T; g) ) <= Gap_explain(m_T; g) + small_margin
   ```

   for most `g` in `G`.

2. Over time, as information technologies improve and regulatory barriers fall, both `C_info` and `C_inst` decrease, and observed gaps shrink alongside them. The sequence `Tension_HB_r(m_T)` either decreases or stays near a stable low band as resolution increases.

3. Large deviations from global benchmarks are concentrated in settings where costs and constraints are clearly documented and large, such as markets with strict capital controls or very opaque foreign assets.

4. Aggregate tension remains low:

   ```txt
   Tension_HB_r(m_T) <= epsilon_HB(r)
   ```

   for admissible resolutions `r` and the tolerance function `epsilon_HB` fixed by the encoding class.

### 5.2 World F: structural home bias anomaly

World F represents a world where home bias has a significant structural component that cannot be captured by the modeled costs and constraints.

Characteristics:

1. Even in environments with low measured information and institutional costs, many groups display large normalized gaps:

   ```txt
   abs( Gap_norm(m_F; g) ) >> Gap_explain(m_F; g)
   ```

2. Historical episodes of financial liberalization and technology driven reduction in information costs do not lead to proportional declines in home bias. The sequence `Tension_HB_r(m_F)` remains large or converges to a strictly positive lower band.

3. Some investor groups with similar risk profiles and access to information display markedly different home bias levels, in ways that cannot be explained by the cost variables encoded in Q102.

4. Aggregate tension is bounded away from zero across resolutions in the observed range:

   ```txt
   Tension_HB_r(m_F) >= delta_HB
   ```

   for a constant `delta_HB` that remains strictly positive for realistic encoding classes.

### 5.3 Interpretive note

These counterfactual worlds are not proposed as full structural models. They are templates for patterns in observables:

* World T corresponds to friction aligned portfolios, where Q102’s encoding can absorb most of the bias into measurable cost terms.
* World F corresponds to a structural anomaly, where even generous encodings leave a persistent residual.

Q102 does not decide which world we live in. It makes the distinction between these patterns explicit and testable at the level of effective observables, without exposing any deep TU generative rule.

---

## 6. Falsifiability and discriminating experiments

This block specifies experiments that can falsify particular Q102 encodings or parameter choices. They do not prove or disprove any underlying theory of home bias. They only test whether a proposed tension encoding is coherent with observed data under the declared fairness conditions.

In all experiments:

* The encoding class `E_HB` including `B_k`, `Lib_info`, `Lib_inst`, `k_info`, `k_inst`, `epsilon_w`, `pi_g` rules, and global thresholds such as `tau_low(r)`, `tau_high(r)`, and `B_hor` must be fixed **before** computing any tension scores on the target dataset.
* Any substantial change to these choices constitutes a new encoding class and must be treated as a different version of Q102.

### Experiment 1: Cross country panel tension profiling

**Goal**

Evaluate whether a given Q102 encoding class `E_HB` can keep `Tension_HB_r` within a plausible low band when applied to historical cross country portfolio data.

**Setup**

Data:

* Panel data on portfolio allocations by investor group and country over multiple decades.
* Market capitalization, risk measures, and indicators of financial integration.
* Proxies for information costs, such as analyst coverage and data availability.
* Proxies for institutional costs, such as capital controls and taxation of foreign holdings.

Encoding:

* Choose one benchmark rule `B_k` in `Lib_benchmark` before inspecting any portfolio weights or home bias gaps.
* Choose cost functions in `Lib_info` and `Lib_inst` using only environment descriptors and ex ante group characteristics.
* Fix constants `k_info`, `k_inst`, `epsilon_w` for Q102 as a whole.
* Fix the rule for `pi_g(m)` and the threshold functions `tau_low(r)` and `tau_high(r)` as part of `E_HB`.

**Protocol**

1. For each country, time period, and investor group, construct a state `m_data` in `M_reg` that encodes the relevant summary statistics.
2. For each `m_data`, compute:

   * `w_dom(m_data; g)`, `w_for(m_data; g)`,
   * `w_global_star(m_data; g)`,
   * `C_info(m_data; g)`, `C_inst(m_data; g)`,
   * `Gap_norm(m_data; g)`, `Gap_explain(m_data; g)`,
   * `DeltaS_incentive(m_data; g)`,
   * `Tension_HB_r(m_data)` for selected resolutions `r`.
3. Build distributions of `Tension_HB_r(m_data)` across countries and groups for each `r`.
4. Compute the global invariant `I_HB_encoding(r)` for the chosen `D_panel` and weights `w_state(m_data)`.

**Metrics**

* Fraction of states where `Tension_HB_r(m_data) <= tau_low(r)`.
* Fraction of states where `Tension_HB_r(m_data) >= tau_high(r)`.
* Cross country and cross group variation in `Tension_HB_r(m_data)` and its correlation with cost proxies.
* Behavior of `I_HB_encoding(r)` across resolutions.

**Falsification conditions**

* If, for every encoding in `E_HB` that respects fairness constraints, the fraction of states with `Tension_HB_r(m_data) > tau_high(r)` remains large across country groups and does not shrink over time, then Q102’s current encoding class is considered falsified as a friction only description of home bias at this effective layer.
* If small changes in benchmark and cost functions within the same encoding class produce arbitrarily large swings in `Tension_HB_r(m_data)` on the same dataset, the encoding is considered unstable and rejected.

**Semantics implementation note**

The experiment treats portfolio weights, returns, and costs as continuous variables indexed by discrete groups and countries, in line with the hybrid setting declared in the metadata. No additional TU layer is introduced in this experiment.

**Boundary note**

Falsifying a TU encoding in this experiment does not solve the canonical home bias puzzle. It only rejects specific choices of benchmark and cost encodings under the given fairness constraints.

---

### Experiment 2: Event study of friction reducing reforms

**Goal**

Test whether Q102’s cost based encoding predicts meaningful declines in `Tension_HB_r` following identifiable reductions in information or institutional frictions.

**Setup**

Data:

* A set of events where a country implements reforms that plausibly reduce `C_info` or `C_inst` for some investor groups, such as:

  * removal or relaxation of capital controls,
  * introduction of international trading platforms,
  * major improvements in financial disclosure for foreign firms,
  * regulatory changes that ease cross border investment.
* Portfolio allocations before and after the events for affected and unaffected groups.
* External documentation that defines the event set independently of any observed pattern in `Tension_HB_r`.

Encoding:

* Use a fixed encoding class `E_HB` chosen prior to analyzing the event windows, including the functions in `Lib_benchmark`, `Lib_info`, `Lib_inst`, constants, and `pi_g` rules.
* Fix a bound `B_event` that characterizes a minimum expected reduction in tension when costs fall by a given amount, as part of `E_HB`.

**Protocol**

1. For each event, identify a pre window and a post window that are long enough to capture portfolio adjustments, for example three to five years.
2. For each window, construct states `m_before` and `m_after` in `M_reg` that encode:

   * portfolio weights,
   * benchmark weights,
   * cost proxies for the affected and comparison groups.
3. Compute:

   * `Tension_HB_r(m_before)` and `Tension_HB_r(m_after)` for selected resolutions `r`,
   * changes in `C_info` and `C_inst`,
   * changes in `Gap_norm` for affected groups.
4. Compare the observed changes in `Tension_HB_r` with the changes predicted by the cost reductions implied by the encoding.

**Metrics**

* Average change in `Tension_HB_r` for affected groups versus unaffected comparison groups.
* Relationship between reductions in `C_info` and `C_inst` and reductions in `Tension_HB_r`.
* Frequency of events where tension does not respond to cost changes in the direction implied by the encoding.

**Falsification conditions**

* If a sizable set of events shows large, sustained reductions in cost proxies but negligible change in `Tension_HB_r` for affected groups, then the encoding is considered insufficient, since it fails to connect cost changes to tension reductions.
* If the sign of tension change frequently contradicts the implied direction, for example tension increases when costs fall in ways not explained by better risk sharing or diversification, the encoding is considered misaligned and rejected.

**Semantics implementation note**

This experiment treats time windows as separate states and focuses on discrete before and after comparisons. Continuous cost and weight changes are mapped into the same hybrid state space `M` used elsewhere.

**Boundary note**

Falsifying a TU encoding in this experiment does not show that home bias is purely structural, nor that it is purely friction driven. It only shows that a specific way of encoding friction effects is inadequate.

---

## 7. AI and WFGY engineering spec

This block describes how Q102 can be used in AI and WFGY systems at the effective layer. It focuses on training signals, architectural patterns, evaluation protocols, and a minimal reproduction protocol.

All uses described here operate strictly at the effective layer and do not expose any TU generative rules.

### 7.1 Training signals

1. `signal_home_bias_gap`

   * Definition: derived from `Gap_norm(m; g)` for groups or contexts described in text or structured data.
   * Use: penalize or highlight model states where descriptions of portfolios suggest large normalized gaps without corresponding explanations or friction terms.

2. `signal_cost_alignment`

   * Definition: a signal that measures how much of `Gap_norm(m; g)` can be attributed to `Gap_explain(m; g)` based on explicit information and institutional frictions present in the context.
   * Use: encourage models to distinguish between bias that is explained by costs and bias that remains as residual tension.

3. `signal_home_bias_tension_score`

   * Definition: directly equal to `DeltaS_incentive(m; g)` or `Tension_HB(m)` depending on the granularity of the representation.
   * Use: act as an auxiliary loss term or diagnostic signal when training agents that reason about international portfolios or macro financial puzzles.

4. `signal_counterfactual_separation`

   * Definition: a measure of how clearly a model’s outputs differ when prompted under World T style assumptions versus World F style assumptions for home bias.
   * Use: encourage the model to maintain consistent internal representations for distinct counterfactual worlds.

### 7.2 Architectural patterns

1. `HomeBiasTensionHead`

   * Role: a lightweight module that takes internal embeddings associated with portfolio and macro finance contexts and outputs estimates of:

     * `Gap_norm`,
     * `Gap_explain`,
     * `DeltaS_incentive`,
     * and an aggregate `Tension_HB` where appropriate.
   * Interface:

     * Inputs: context embeddings plus any structured descriptors of portfolios and frictions.
     * Outputs: scalar or small vector of tension metrics.

2. `ConstraintAwarePortfolioFilter`

   * Role: a filter that checks whether candidate portfolio recommendations are consistent with described global diversification benchmarks and explicit frictions.
   * Interface:

     * Inputs: candidate allocations, benchmark descriptors, friction descriptors.
     * Outputs: a tension score and a mask or set of warnings indicating over concentration or unexplained home bias.

3. `FrictionDecompositionExplainer`

   * Role: a module that decomposes a given home bias description into:

     * a part explained by information and institutional frictions,
     * and a residual part that remains unexplained.
   * Interface:

     * Inputs: text or structured descriptions of portfolios and frictions.
     * Outputs: a structured explanation that assigns portions of the gap to different components and reports residual tension.

### 7.3 Evaluation harness

A simple harness for evaluating AI systems equipped with Q102 components.

1. Task selection:

   * A curated set of questions and case studies concerning:

     * home bias in different countries,
     * the effects of financial integration and reforms,
     * the relationship between home bias and other macro puzzles.

2. Conditions:

   * Baseline:

     * The model answers questions with no explicit use of tension scores or Q102 modules.
   * TU augmented:

     * The model uses the HomeBiasTensionHead and FrictionDecompositionExplainer to structure its internal reasoning and explanations.

3. Metrics:

   * Coherence:

     * consistency between the narrative explanation and the implied direction and magnitude of home bias tension.
   * Separation:

     * ability to clearly distinguish between friction based explanations and residual anomalies.
   * Stability:

     * robustness of explanations across small variations in problem framing or additional contextual information.

### 7.4 Sixty second reproduction protocol

A minimal protocol that external users can run with a generic AI system.

Baseline setup:

* Prompt:

  * Ask the AI to explain what the home bias puzzle is and why it matters for global diversification, without any mention of tension, Q102, or WFGY.
* Observation:

  * Record whether the answer:

    * confuses measurement issues with structural puzzles,
    * mixes friction based and behavioral explanations without clear separation,
    * lacks an explicit benchmark and residual analysis.

TU encoded setup:

* Prompt:

  * Ask the AI the same question, but instruct it to:

    * define a benchmark global portfolio,
    * define a measure of home bias gap,
    * separate bias that can be explained by costs and constraints from residual bias,
    * and refer to a simple tension score when summarizing the situation.
* Observation:

  * Record whether the explanation becomes more structured, for example:

    * global benchmark first,
    * measurable gap second,
    * friction based explanation third,
    * residual anomaly last.

Comparison metric:

* A simple rubric based on:

  * clarity of benchmark versus realized allocation,
  * explicit use of cost and constraint information,
  * explicit reporting of what remains unexplained.

What to log:

* The prompts and responses for both setups.
* If available, internal estimates of `Tension_HB` from Q102 style modules, for later analysis.

This protocol gives users a quick, reproducible way to feel the difference between unconstrained explanations and explanations that follow the Q102 encoding.

---

## 8. Cross problem transfer template

This block lists components produced by Q102 and describes how they transfer to other BlackHole nodes.

### 8.1 Reusable components produced by this problem

1. ComponentName: `HomeBiasTensionScore`

   * Type: functional
   * Minimal interface:

     * Inputs:

       * `portfolio_summary`:

         * domestic and foreign weights by group and country,
       * `benchmark_summary`:

         * global benchmark weights by group and country,
       * `cost_summary`:

         * information and institutional cost measures by group.
     * Output:

       * `tension_value`:

         * a nonnegative scalar equal to `Tension_HB(m)` for a constructed state.
   * Preconditions:

     * Inputs must be consistent with a state in `M_reg`, including non negative weights and defined benchmark and cost values.

2. ComponentName: `InvestorExposureField`

   * Type: field
   * Minimal interface:

     * Inputs:

       * `portfolio_summary`,
       * mapping of investors to asset categories and jurisdictions.
     * Output:

       * `exposure_tensor`:

         * a three index array that records exposures by investor group, country, and asset bucket.
   * Preconditions:

     * The mapping from investors to assets is well defined and covers the relevant risky asset categories.

3. ComponentName: `FrictionDecompositionTemplate`

   * Type: experiment_pattern
   * Minimal interface:

     * Inputs:

       * `portfolio_datasets`,
       * `friction_proxies`,
       * definitions of `Lib_benchmark`, `Lib_info`, and `Lib_inst`.
     * Output:

       * a decomposition of each observed gap into:

         * an explainable part assigned to frictions,
         * a residual part treated as incentive tension.
   * Preconditions:

     * Friction proxies must be measurable and mapped into cost observables without using realized portfolio weights.

### 8.2 Direct reuse targets

1. Target: Q101 · Equity premium puzzle

   * Reused component:

     * `FrictionDecompositionTemplate`.
   * Why it transfers:

     * The decomposition of risk premia into parts explainable by risk and cost versus residual anomalies parallels the decomposition of home bias gaps.
   * What changes:

     * Inputs are now equity returns and consumption risk measures rather than domestic and foreign weights.

2. Target: Q105 · Prediction of systemic crashes

   * Reused components:

     * `InvestorExposureField`, `HomeBiasTensionScore`.
   * Why it transfers:

     * Systemic crashes often involve concentrated exposures within regions. Home bias defines one specific pattern of concentration in the exposure tensor.
   * What changes:

     * Outputs are linked to measures of network fragility, and additional layers of exposures, such as derivative positions, may be added.

3. Target: Q121 and Q123 · AI alignment and interpretability

   * Reused component:

     * `FrictionDecompositionTemplate`.
   * Why it transfers:

     * The pattern of separating explainable deviations from residual anomalies under constraints can be reused to analyze AI behavior, where:

       * explicit constraints and objectives play the role of frictions and benchmarks,
       * residual misalignment plays the role of unexplained home bias.
   * What changes:

     * Portfolios are replaced by policy choices or internal representations of AI systems, and benchmarks are defined by user intentions or safety criteria.

---

## 9. TU roadmap and verification levels

This block explains how Q102 is positioned in the TU verification ladder and what the next measurable steps are.

### 9.1 Current levels

* E_level: E1

  * A coherent effective layer encoding exists, including:

    * state space `M`,
    * observables for weights, benchmarks, and costs,
    * a well defined tension functional `Tension_HB(m)` and its multi resolution version `Tension_HB_r(m)`,
    * a singular set `S_sing` and regular domain `M_reg`,
    * and a global invariant `I_HB_encoding(r)`.

  * Discriminating experiment patterns are defined in outline but not yet instantiated with concrete datasets.

* N_level: N1

  * The narrative connecting global diversification benchmarks, observed portfolios, frictions, and residual anomalies is explicit but not yet solidified into a quantitative practice or a standard industry toolkit.

### 9.2 Next measurable step toward E2

To move from E1 to E2, both of the following should be implemented:

1. A concrete choice of encoding class `E_HB`:

   * specific functions in `Lib_benchmark`, `Lib_info`, and `Lib_inst`,
   * fixed values for `k_info`, `k_inst`, and `epsilon_w`,
   * a chosen definition of group weights `pi_g(m)` based on ex ante observables,
   * fixed threshold functions `epsilon_HB(r)`, `tau_low(r)`, `tau_high(r)`,
   * fixed constants for experiments such as `B_hor` and `B_event`.

2. A pilot implementation of Experiment 1:

   * using an accessible cross country portfolio dataset,
   * computing example values of `Tension_HB_r(m_data)` and `I_HB_encoding(r)` for several countries and time periods,
   * publishing the resulting tension profiles and the encoding details as an explicit version of Q102.

Once this is done, Q102’s encoding becomes a falsifiable object in practice rather than a purely conceptual template.

### 9.3 Long term role in the TU program

In the longer term, Q102 is expected to serve as:

* A reference implementation of incentive_tension in a setting where agents choose among local and global options under frictions.
* A bridge between financial puzzles and other domains where local allegiance or familiarity competes with global efficiency.
* A laboratory for AI systems that reason about global allocations under constraints, testing whether they can track which parts of anomalies are explained and which remain as residual tension.

At all stages, Q102 remains an effective layer specification. Any future deep TU interpretation of home bias must be stated and justified separately.

---

## 10. Elementary but precise explanation

This block gives an explanation aimed at non specialists while remaining faithful to the effective layer encoding.

In simple terms, the home bias puzzle says:

> People and institutions put much more of their money into assets from their own country than basic financial theory would suggest is safe or optimal.

If everyone could invest easily in any country, with no extra cost or complexity, then the usual advice would be to diversify worldwide. In reality, portfolios are strongly tilted toward domestic assets.

The Tension Universe view does not try to say exactly why this happens. Instead, it tries to measure how big the puzzle really is, and how much of it can be explained by visible frictions.

The steps are:

1. For each group of investors and each country, define three things:

   * how much of their risky portfolio is domestic versus foreign,
   * what a reasonable global benchmark would be,
   * how costly it is for them to understand and hold foreign assets, including rules and regulations.

2. Compute the **gap** between what they actually do and what the benchmark says they might do, and normalize this gap so that it is comparable across cases.

3. Compute how much of this gap could reasonably be explained by information and institutional costs.

4. Define a **tension score** for each group:

   * if the gap is mostly explained by costs, tension is near zero,
   * if a big gap remains after subtracting costs, tension is positive.

5. Combine tension across groups to get an overall home bias tension for the world or for a given country, possibly at different levels of detail.

6. Repeat this across countries, time periods, and different levels of resolution to see whether the tension stays small or remains large.

The framework then considers two types of worlds:

* In a friction aligned world, as information gets better and rules become friendlier, costs go down and the tension score goes down with them. Most of the home bias can be assigned to costs.
* In a structural anomaly world, even when costs fall, tension stays high. Portfolios stay very domestic for reasons that the simple friction story cannot capture.

Q102 does not claim to know which world we live in. It provides:

* a clear way to compute tension scores from observable quantities,
* a way to test whether a given friction based explanation fits the data under explicit fairness constraints,
* and reusable components for other problems where local choices systematically deviate from global benchmarks.

All of this is done at the effective layer. No assumption is made that the TU encoding itself is the deepest description of reality. It is treated as a scientific tool that can be implemented, tested, falsified, and refined.

---

## Tension Universe effective-layer footer

### Scope of claims

* This page is part of the **WFGY / Tension Universe** S problem collection.
* The goal of this document is to specify an **effective layer encoding** of the home bias puzzle (Q102).
* It does not claim to solve the canonical home bias problem.
* It does not introduce any new economic theorem beyond what is already established in the cited literature.
* It should not be cited as evidence that home bias has been resolved or that any particular mechanism has been proven correct.

### Effective-layer boundary

* All objects used here (state space `M`, observables, cost functions, tension scores, invariants, and tensors) live at the **effective layer** of the TU framework.
* No generative TU rule, field equation, or deep axiom is specified in this file.
* No explicit mapping from raw transaction level data to internal TU fields is given. The file only assumes that such mappings exist for the purpose of defining effective observables.
* Statements about “worlds” in this file refer to effective layer models. They are not assertions about metaphysical or ultimate states of the universe.

### Encoding and fairness boundary

* A Q102 encoding class `E_HB` consists of:

  * a benchmark function chosen from `Lib_benchmark`,
  * cost functions chosen from `Lib_info` and `Lib_inst`,
  * constants `k_info`, `k_inst`, `epsilon_w`,
  * a rule for group weights `pi_g(m)` based on ex ante observables,
  * threshold functions `epsilon_HB(r)`, `tau_low(r)`, `tau_high(r)`,
  * and fixed constants for experiments such as `B_hor` and `B_event`.
* All of these elements must be fixed **before** tension scores are computed on a target dataset.
* None of these elements may be tuned directly on `Gap_norm`, `DeltaS_incentive`, or `Tension_HB` patterns for specific datasets.
* Any substantial change in:

  * benchmark library choices,
  * cost function families,
  * parameter bounds,
  * weight rules,
  * or global thresholds,
    corresponds to a different encoding class and should be recorded as a new version of this document.

### Falsifiability and experiments

* The experiments in Section 6 are designed to test and potentially falsify **encodings** of home bias tension at the effective layer.
* Falsifying a particular encoding class does not prove that home bias is unsolvable, and it does not establish any particular structural explanation.
* Passing the experiments does not prove that the encoding is unique or that all relevant frictions have been captured.
* The intended scientific workflow is iterative:

  * specify an encoding class,
  * implement the invariants and experiments,
  * compare with data,
  * and refine or replace the encoding as needed.

### Use in engineering and AI systems

* The engineering interfaces in Section 7 (signals, heads, filters, and templates) are designed as **effective layer components**.
* They are intended to:

  * improve clarity and consistency when AI systems reason about home bias and related macro finance puzzles,
  * provide measurable tension scores that can be logged and audited,
  * and support cross problem transfer inside the TU program.
* They are not safety proofs and do not guarantee that AI systems will behave correctly in all financial settings.

### Relation to TU charters

This page should be read together with the following charters:

* [TU Effective Layer Charter](../Charters/TU_EFFECTIVE_LAYER_CHARTER.md)
* [TU Encoding and Fairness Charter](../Charters/TU_ENCODING_AND_FAIRNESS_CHARTER.md)
* [TU Tension Scale Charter](../Charters/TU_TENSION_SCALE_CHARTER.md)
* [TU Global Guardrails](../Charters/TU_GLOBAL_GUARDRAILS.md)

These charters provide the global rules for:

* what counts as an effective layer statement,
* how encoding classes are defined and versioned,
* how tension scales are calibrated across problems,

and should be considered part of the background contract under which Q102 is specified.
