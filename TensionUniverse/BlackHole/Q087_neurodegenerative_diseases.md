# Q087 · Mechanisms of neurodegenerative diseases

## 0. Header metadata

```txt
ID: Q087
Code: BH_NEURO_DEGEN_DISEASE_L3_087
Domain: Neuroscience
Family: Neurodegeneration and maintenance failure
Rank: S
Projection_dominance: M
Field_type: multi_scale_dynamical_field
Tension_type: structural_degradation_tension
Status: Open
Semantics: hybrid
E_level: E1
N_level: N2
Last_updated: 2026-01-30
````

---

## 0. Effective layer disclaimer and scope

All statements in this entry are made strictly at the effective layer of the Tension Universe (TU) framework.

1. We restrict ourselves to observables, effective fields, tension functionals, extremality patterns, dynamical constraints, and testable predictions.

2. We do not specify any underlying axiom system, generating rules, or constructive derivations of TU itself.
   We do not give any explicit mapping from raw biological or clinical data into internal TU fields.
   We only assume that TU compatible models exist which reproduce the observables defined here, and that later sections will introduce a regular domain where these objects are well defined.

3. This document does not provide medical advice or clinical guidance.
   It must not be used to diagnose individual patients, decide treatments, or replace clinical judgement.
   Any use of these ideas in medical contexts requires separate, fully independent validation and regulation.

4. This page does not claim to have solved the mechanisms of Alzheimer disease, Parkinson disease, or any other neurodegenerative condition.
   It specifies one candidate family of tension encodings and experiment templates that can be falsified, improved, or replaced.

5. This entry should be read together with the TU charters listed in the footer, which define global constraints on effective layer encodings, fairness, tension scales, and cross problem comparisons.

6. All statements that involve tension functionals or dynamics are implicitly restricted to the regular domain introduced in Section 3.5.
   Configurations in the corresponding singular set lie outside the scope of Q087 and cannot be used to support or refute mechanistic claims.

---

## 1. Canonical problem and status

### 1.1 Canonical statement

The canonical form of Q087 can be stated as follows.

> Mechanisms of neurodegenerative diseases.
> For conditions such as Alzheimer disease, Parkinson disease, frontotemporal dementia, and related syndromes, what are the multi scale mechanisms that initiate and drive progressive neuronal loss, synaptic failure, and network level dysfunction, and can we identify a constrained set of structural first causes that explain:
>
> * selective vulnerability of regions and cell types,
> * slow but persistent progression over years and decades,
> * partial overlap and divergence between different clinical syndromes,
> * and the interaction between molecular pathology, network dynamics, and maintenance systems.

More concretely, at the effective layer we ask whether there exists:

* a multi component tension functional `DeltaS_neurodeg(m)` defined on a state space of long term brain configurations,
* a critical surface `Sigma_crit` in that state space,

such that:

* crossing `Sigma_crit` in the direction of increasing `DeltaS_neurodeg` corresponds to entering an effectively irreversible regime of neurodegenerative progression,
* while remaining on the low tension side is compatible with healthy aging or subclinical changes.

The problem is not to assert a single molecular trigger.
It is to identify:

* a small set of structurally necessary tension components,
* the way they combine into long term drift of neural and support systems,
* and conditions under which this drift becomes self reinforcing.

### 1.2 Status and difficulty

Empirically, many mechanisms have been implicated in neurodegenerative diseases.
Examples include:

* misfolded and aggregating proteins such as amyloid beta, tau, alpha synuclein, TDP-43,
* mitochondrial dysfunction and oxidative stress,
* impaired proteostasis and autophagy,
* neuroinflammation and glial dysregulation,
* vascular and glymphatic failure,
* impaired sleep and circadian maintenance.

However, there is no single universally accepted model that:

* unifies these mechanisms across diseases and stages,
* explains selective vulnerability in a quantitative manner,
* connects maintenance failures over decades to late clinical collapse,
* and gives a well defined long term risk functional that can be tested in realistic cohorts.

Difficulties include:

* strong heterogeneity across individuals, genes, and environments,
* multi scale coupling between molecular, cellular, network, and behavioural levels,
* practical and ethical constraints on long duration human experiments,
* limitations of animal models and in vitro systems in capturing long human timescales.

The problem is therefore considered open at the level of a unified, quantitatively constrained theory.
Many partial models exist for specific diseases, pathways, or stages, but none fully resolve the first cause question in a way that is both mechanistic and broadly integrative.

### 1.3 Role in the BlackHole project

Within the BlackHole S level problem collection, Q087 plays several roles.

1. It is the central neurodegeneration node that links:

   * sleep and maintenance (Q086),
   * plasticity and coding (Q083, Q085),
   * consciousness and cognitive function (Q081, Q084),

   to long term structural failure.

2. It serves as a prototype for modelling irreversible transitions in biological systems, where:

   * slow accumulation of multiple tensions,
   * finite reserve and repair capacities,

   lead to abrupt functional collapse.

3. It provides an anchor point for connecting:

   * human aging and demographic risk (Q098, Q100),
   * analogues of maintenance and degradation in AI systems (Q123),

   through a shared language of tension functionals and critical surfaces.

---

## 2. Position in the BlackHole graph

This section records how Q087 sits inside the BlackHole graph as nodes and edges among Q001 to Q125.
Edges are listed with short reasons that refer to concrete components or tension types.

### 2.1 Upstream problems

These problems provide prerequisites, tools, or general foundations that Q087 relies on at the effective layer.

* Q081 (BH_NEURO_CONSCIOUS_HARD_L3_081)
  Reason: Specifies high level cognitive functions and subjective experience that are progressively affected by neurodegeneration.

* Q082 (BH_NEURO_MEMORY_CONSOL_L3_082)
  Reason: Encodes systems level memory consolidation across brain structures, which is selectively disrupted when long term circuits degrade.

* Q083 (BH_NEURO_CODING_L3_083)
  Reason: Provides coding and representation tools to describe how neural patterns are corrupted or lost.

* Q084 (BH_NEURO_MEMORY_STORE_L3_084)
  Reason: Encodes memory systems and storage constraints that are directly targeted in Alzheimer and related diseases.

* Q085 (BH_NEURO_PLASTICITY_RULES_L3_085)
  Reason: Gives plasticity dynamics whose long term saturation or misregulation plays a role in vulnerability and compensation.

* Q086 (BH_NEURO_SLEEP_FUNC_L3_086)
  Reason: Supplies a multi function maintenance tension functional whose chronic disruption can contribute to degeneration risk.

* Placeholder for future systemic or vascular nodes in other families, once they are assigned Q indices in the final BlackHole list.
  Reason: Provide background risk structure that modulates Q087 tension trajectories, for example cardiovascular and metabolic constraints.

### 2.2 Downstream problems

These problems reuse components of Q087 or depend on its tension structure.

* Q088 (BH_NEURO_DEV_CRIT_WINDOWS_L3_088)
  Reason: Uses Q087 style multi scale tension but focuses on early developmental windows rather than late life degeneration.

* Q089 (BH_NEURO_PREDICTIVE_CODE_L3_089)
  Reason: Incorporates degradation of coding and prediction circuits as a source of systematic prediction error and misperception.

* Q098 (BH_EARTH_ANTHROPOCENE_L3_098)
  Reason: Uses population distributions of neurodegeneration risk and cognitive decline as micro level constraints on large scale societal capacity.

* Q100 (BH_SOC_PANDEMIC_RISK_L3_100)
  Reason: Treats neurodegeneration as one factor in population vulnerability, especially where crises require high cognitive performance in aging societies.

* Q123 (BH_AI_INTERP_L3_123)
  Reason: Uses Q087 as a template for thinking about long term degradation of AI systems under continuous operation and imperfect maintenance.

### 2.3 Parallel problems

Parallel nodes share similar tension types but no direct component dependence.

* Q086 (BH_NEURO_SLEEP_FUNC_L3_086)
  Reason: Both use multi component maintenance tensions, but Q086 focuses on daily cycles while Q087 focuses on multi year trajectories.

* Any problem encoding chronic systemic diseases where repair and wear compete, such as future cardiovascular or metabolic nodes once they are given Q indices.
  Reason: Share the structural idea of drift toward a critical surface defined by damage versus repair.

### 2.4 Cross domain edges

Cross domain edges connect Q087 to problems in other domains that can reuse its structures.

* Q098 (BH_EARTH_ANTHROPOCENE_L3_098)
  Reason: Q087 tension trajectories can be aggregated into population level risk fields for cognitive capacity in Anthropocene scenarios.

* Q100 (BH_SOC_PANDEMIC_RISK_L3_100)
  Reason: Neurodegeneration patterns affect resilience and response capacity during pandemics and other large scale shocks.

* Q123 (BH_AI_INTERP_L3_123)
  Reason: Q087 provides a pattern for encoding gradual degradation and sudden failure in complex AI systems that run continuously.

All firm edges listed above use Q indices and informal descriptions only, with no external URLs, so that the full Q001 to Q125 graph can be assembled as a consistent adjacency list.
Any placeholder references to future nodes are explicitly marked and are not part of the current edge set.

---

## 3. Tension Universe encoding (effective layer)

All content in this section is at the effective layer.
We describe:

* state spaces,
* observables and fields,
* mismatch quantities and tension scores,
* dynamical updates and critical sets.

We do not describe hidden generative rules or any mapping from raw data to TU internal fields.

### 3.1 State space and encoding class

We assume the existence of a multi scale state space

```txt
M_neurodeg
```

with the following effective interpretation.

* Each element `m` in `M_neurodeg` represents a coherent multi year brain world configuration for an individual or a homogeneous subgroup, including:

  * molecular and cellular summaries relevant for neurodegeneration,
  * synaptic and local circuit integrity,
  * large scale network dynamics,
  * maintenance and clearance history, including sleep and vascular support,
  * cognitive and functional outcomes,
  * reserve and compensation capacity.

* Time is represented implicitly by encoding a finite window such as ten to thirty years into the structure of `m`.
  In addition, for dynamical statements we consider trajectories `m(t)` that traverse `M_neurodeg` over coarse time steps.

We do not specify how raw imaging, pathology, genetics, fluid biomarkers, or behavioural data are mapped into `M_neurodeg`.
We only assume that for any realistic cohort and time range there exist states `m` that encode coherent summaries sufficient to evaluate the observables defined below.

We denote by `E_neurodeg` the class of admissible encodings from raw neurodegeneration relevant data into `M_neurodeg`.
For any concrete study or experiment, the implementer must first register a finite registry

```txt
Registry_ND = { E_1, ..., E_K } subset of E_neurodeg
```

and pick one element `E_k` from this registry for the main analysis.
All state constructions, observables, and tension scores in that study must be computed using `E_k` and the library choices fixed in advance.

### 3.2 Effective fields and observables

All observables introduced here use hybrid semantics.
Discrete events and measurements over time are summarised into continuous effective quantities that live on `M_neurodeg`, such as long term averages, distributions, or coarse grained fields.

We introduce the following effective observables and fields on `M_neurodeg`.

1. Molecular and proteostatic burden field

   ```txt
   Prot_burden(m; region, species)
   ```

   Output: an effective measure of the burden of misfolded or aggregation prone proteins, proteostatic stress, and related molecular pathology in a given brain region and species context.

   Values may include aggregated summaries of markers such as amyloid, tau, alpha synuclein, or others, without committing to specific assays.

2. Synaptic and local circuit integrity field

   ```txt
   Syn_health(m; region)
   ```

   Output: an effective indicator of synaptic density, spine health, and microcircuit viability in a specified region or network module.

3. Large scale network dynamics field

   ```txt
   Net_dyn(m; scale)
   ```

   Output: effective descriptors of functional connectivity, oscillatory coordination, and network level integration at chosen spatial and temporal scales.

4. Maintenance and support field

   ```txt
   Maint_sup(m; window)
   ```

   Output: summaries of maintenance related processes across a time window, including sleep architecture and tension (for example via `DeltaS_sleep` from Q086), vascular and glymphatic support, metabolic balance, and immune regulation.

5. Clinical and functional outcome field

   ```txt
   Clin_func(m; domain)
   ```

   Output: effective measures of cognitive performance, motor function, daily living capacity, and other relevant functional endpoints across domains such as memory, executive control, language, and movement.

6. Reserve and compensation capacity field

   ```txt
   Reserve_cap(m)
   ```

   Output: an effective scalar or vector that captures cognitive reserve, network redundancy, and capacity for structural and functional compensation in the face of damage.

All of these observables are assumed to be well defined and finite for states in a regular subset of `M_neurodeg` described below.
They are constructed from `E_k` and from finite encodings registered before outcome analysis.

### 3.3 Mismatch observables and finite encoding libraries

We define three primary nonnegative mismatch quantities that measure distinct aspects of deviation from a healthy regime.

1. Molecular and proteostatic tension

   ```txt
   DeltaS_mol(m) >= 0
   ```

   Interpretation: deviation of `Prot_burden(m; ...)` and related markers from reference patterns compatible with long term molecular stability.

   Example encoding family:

   * `Lib_mol = { MolEncoding_1, ..., MolEncoding_Km }`
   * A typical `MolEncoding_k` might define a normalised combination of:

     * regional misfolded protein load,
     * chaperone and proteostasis indicators,
     * mitochondrial stress markers,

     aggregated into a scalar mismatch by a fixed formula chosen before data analysis.

2. Circuit and network tension

   ```txt
   DeltaS_circuit(m) >= 0
   ```

   Interpretation: deviation of `Syn_health(m; region)` and `Net_dyn(m; scale)` from reference patterns that support robust cognition in the given species and context.

   Example encoding family:

   * `Lib_circuit = { CircEncoding_1, ..., CircEncoding_Kc }`
   * A typical `CircEncoding_r` might combine:

     * loss of synaptic density in vulnerable regions,
     * disruption of functional connectivity patterns,
     * increased network noise or instability,

     into a scalar mismatch.

3. Maintenance and clearance tension

   ```txt
   DeltaS_maint(m) >= 0
   ```

   Interpretation: deviation of `Maint_sup(m; window)` from reference maintenance and clearance regimes known to support long term brain health.

   Example encoding family:

   * `Lib_maint = { MaintEncoding_1, ..., MaintEncoding_Kh }`
   * A typical `MaintEncoding_h` might:

     * import `DeltaS_sleep(m_sleep)` from Q086 for relevant windows,
     * add vascular, glymphatic, and metabolic clearance indicators,
     * combine them into a scalar mismatch.

To represent weightings between these components we introduce a finite weight library:

```txt
Lib_weights = {
  (w_mol, w_circuit, w_maint) in R^3 :
  w_mol, w_circuit, w_maint >= 0,
  w_mol + w_circuit + w_maint = 1,
  and the triple belongs to a finite pre specified set
}
```

Each element of the libraries `Lib_mol`, `Lib_circuit`, `Lib_maint`, and `Lib_weights` is a concrete, finite specification that includes:

* explicit choice of observables and normalisations,
* reference classes and rescalings,
* closed form expressions for the mismatch.

Fairness constraints for experiments and analyses:

* For any given study or model evaluation, one element from each library is selected before detailed outcome inspection.
* Once selected, these encodings and weights must be held fixed for all subsequent analysis in that context.
* Adaptive retuning of encodings or weights as a function of observed outcomes is not permitted inside the same registered experiment.

For bookkeeping, each concrete combination

```txt
Version_ND = (
  E_k,
  MolEncoding_k,
  CircEncoding_r,
  MaintEncoding_h,
  (w_mol, w_circuit, w_maint),
  parameters for H(m)
)
```

defines one Q087 effective layer encoding version.
Experiments that claim to use Q087 must record which `Version_ND` they instantiate.

### 3.4 Combined neurodegeneration tension functional

We define the combined neurodegeneration tension functional:

```txt
DeltaS_neurodeg(m) =
    w_mol    * DeltaS_mol(m)
  + w_circuit * DeltaS_circuit(m)
  + w_maint   * DeltaS_maint(m)
```

with the following constraints.

* The weights `(w_mol, w_circuit, w_maint)` are chosen from `Lib_weights`.

* For each encoding triplet we require:

  ```txt
  w_mol    >= w_min
  w_circuit >= w_min
  w_maint   >= w_min
  ```

  for some fixed `w_min` in `(0, 1/3]`, to avoid any component being effectively ignored.

As a baseline proposal for early E1 work, one may include in `Lib_weights` a small set of triplets such as:

```txt
(0.4, 0.3, 0.3),
(0.3, 0.4, 0.3),
(0.3, 0.3, 0.4)
```

with `w_min` chosen for example as `0.25`.
Choosing one of these triplets then corresponds to three nearby versions that emphasise different components without dropping any of them.

Under these conditions:

* `DeltaS_neurodeg(m) >= 0` for all `m` in the regular domain,
* `DeltaS_neurodeg(m)` cannot be forced to zero by setting one mismatched component to zero weight.

This functional is intended as a candidate summary of multi scale strain on brain structure and function that is relevant for neurodegeneration.

### 3.5 Singular set and regular domain

Some configurations may lack sufficient information to evaluate all components, or may produce undefined quantities under the chosen encodings.
We define the singular set:

```txt
S_sing_neurodeg = {
  m in M_neurodeg :
  DeltaS_mol(m), DeltaS_circuit(m), or DeltaS_maint(m)
  is undefined or not finite under the chosen encodings
}
```

and the regular domain:

```txt
M_neurodeg_reg = M_neurodeg \ S_sing_neurodeg
```

All statements about `DeltaS_neurodeg`, and all experiments described, are restricted to `M_neurodeg_reg`.

Configurations in `S_sing_neurodeg` cannot be used for tension based conclusions.
They must not be used as the basis for clinical decisions or for judging the adequacy of the encodings.
They can however be used to debug encodings, measurement choices, or data quality.

### 3.6 Dynamic tension evolution

We consider coarse grained trajectories

```txt
t = 0, 1, 2, ..., T
```

where each time step represents a fixed multi year interval, and

```txt
m_t in M_neurodeg_reg
```

represents the brain state at time step `t`.

We assume the existence of an effective update map:

```txt
m_{t+1} = F_world(m_t, u_t, noise_t)
```

where:

* `u_t` encodes controllable or partially controllable influences such as:

  * lifestyle and environmental exposures,
  * medical treatments and preventive actions,
  * systemic comorbidities,

* `noise_t` encodes stochastic influences not controlled by the agent or system.

We do not specify how `F_world` is generated at a deeper level.
We only require that for any fixed choice of encodings and weights, the sequence `DeltaS_neurodeg(m_t)` is well defined along the trajectory as long as `m_t` remains in `M_neurodeg_reg`.

For tension evolution we posit an effective drift relation:

```txt
DeltaS_neurodeg(m_{t+1}) - DeltaS_neurodeg(m_t)
    = G(m_t, u_t) + epsilon_t
```

where:

* `G` is an effective drift functional that depends only on the current state and control variables, not on future values.
* `epsilon_t` is an error term that captures model mismatch and stochastic variations.
  For any fixed encoding, `epsilon_t` is assumed to have bounded magnitude in expectation over a moderate horizon.

We define the cumulative neurodegeneration tension over a horizon `T`:

```txt
A_T = sum_{t=0}^{T} DeltaS_neurodeg(m_t) * dt
```

where `dt` represents the time step duration as physical years.

This cumulative quantity is one candidate measure of long term exposure to degradation relevant tension.

### 3.7 Critical surface and irreversible transition

We introduce an auxiliary functional:

```txt
H(m) = alpha * Damage_index(m) - beta * Reserve_cap(m)
```

where:

* `Damage_index(m)` is an effective scalar functional built from:

  * high values of `DeltaS_mol(m)` and `DeltaS_circuit(m)`,
  * explicit markers of structural damage and cell loss,

  with a specification chosen from a finite library, for example `Lib_H_damage`.

* `Reserve_cap(m)` is the reserve capacity field defined earlier.

* `alpha` and `beta` are positive constants chosen from a finite set `Lib_H_params` prior to analysis.

We define the critical surface:

```txt
Sigma_crit = { m in M_neurodeg_reg : H(m) = 0 }
```

Interpretation:

* `H(m) < 0` corresponds to configurations where reserve dominates over damage,
  damage is present but can be compensated.

* `H(m) > 0` corresponds to configurations where damage dominates reserve,
  the system is in a regime where compensation is structurally inadequate.

We do not claim that this particular linear form is unique or correct.
It is a candidate encoding that can be tested.
Alternative forms of `H` can be introduced as long as they are specified in finite libraries and subjected to the same falsification logic.

Crossing `Sigma_crit` from the region `H(m) < 0` to `H(m) > 0` is interpreted at the effective layer as entering a regime of neurodegenerative progression in which reversal through small adjustments becomes unlikely.

The operational definition of crossing `Sigma_crit` in experiments, for example via thresholds on structural and functional markers, is considered part of the encoding version and must be preregistered before outcome analysis.

---

## 4. Tension principle for this problem

### 4.1 Core neurodegeneration tension functional

The core effective functional is `DeltaS_neurodeg(m)` defined above.
It combines:

* molecular and proteostatic tension,
* circuit and network tension,
* maintenance and clearance tension,

under a constrained weighting scheme.

For any `m` in `M_neurodeg_reg`, a value of `DeltaS_neurodeg(m)` near zero corresponds to a configuration that lies within the reference band of the chosen encodings.
In practice we expect small but nonzero values even in healthy aging.

### 4.2 Healthy aging as low tension regime

At the effective layer, healthy aging can be phrased as follows.

> For individuals who age without major neurodegenerative disease, there exist trajectories `m(t)` and parameter choices such that:
>
> * `DeltaS_neurodeg(m(t))` remains within a low and relatively stable band over decades,
> * `H(m(t))` remains negative, meaning reserve capacity remains sufficient,
> * cumulative tension `A_T` remains below thresholds associated with irreversible structural collapse.

More concretely, for a given encoding choice and species we posit the existence of constants:

```txt
epsilon_neurodeg > 0
T_healthy > 0
```

such that for typical healthy aging trajectories:

```txt
DeltaS_neurodeg(m(t)) <= epsilon_neurodeg
H(m(t)) < 0
for all 0 <= t <= T_healthy
```

with `T_healthy` representing a substantial fraction of the lifespan.

### 4.3 Neurodegeneration as irreversible high tension transition

Neurodegeneration corresponds to trajectories for which there exists a time `t*` such that:

```txt
H(m(t*)) = 0
H(m(t)) > 0 for t > t* on a long horizon
DeltaS_neurodeg(m(t)) stays above a disorder specific lower bound
```

and cumulative tension `A_T` exceeds a disease specific threshold.

The irreversibility statement is effective layer only.
It asserts that under the chosen encodings and observed interventions, trajectories that have crossed the critical surface and accumulated sufficient tension have not, in available data, returned to low tension states without major structural loss.

This framing separates:

* encoding choices that can be tested and falsified,
* empirical facts about observed trajectories,

from any deeper claim about absolute impossibility of reversal.

---

## 5. Counterfactual tension worlds

We now describe three counterfactual worlds at the effective layer.
They are tools for reasoning about Q087, not literal metaphysical claims.

### 5.1 World N: neurodegeneration tied to maintenance tension

In World N, maintenance and clearance play a central role.

Key properties:

1. There exists a strong statistical association between long term `DeltaS_maint(m)` and eventual crossing of `Sigma_crit` in typical populations, even after controlling for genetics and age.
   In tension language, conditional expectations such as

   ```txt
   E[DeltaS_neurodeg | high DeltaS_maint]
   ```

   are significantly higher than

   ```txt
   E[DeltaS_neurodeg | low DeltaS_maint]
   ```

   under matched baselines.

2. Interventions that reduce `DeltaS_maint(m)` early in life trajectories can delay or reduce the probability of crossing `Sigma_crit`.

3. Genetic variants and environmental exposures influence neurodegeneration risk largely through their effects on maintenance tension and its interaction with molecular and circuit tensions.

### 5.2 World W: wear and tear with weak maintenance role

In World W, neurodegeneration is driven mainly by intrinsic wear and random damage.

Key properties:

1. Long term `DeltaS_neurodeg(m)` is dominated by `DeltaS_mol(m)` and `DeltaS_circuit(m)` in ways that are only weakly influenced by `DeltaS_maint(m)`.

2. Manipulations that significantly alter sleep, maintenance, or clearance patterns have limited effect on the probability or timing of crossing `Sigma_crit`, once age and genotype are fixed.

3. Maintenance tension is largely an epiphenomenon of broader deterioration rather than a primary driver.
   Variance in `DeltaS_neurodeg` explained by maintenance factors is small compared with variance explained by molecular and circuit components.

### 5.3 World G: strong genetic initiation with modulatory maintenance

In World G, some subpopulations have strong genetic drivers, yet maintenance still modulates expression.

Key properties:

1. For individuals carrying high impact mutations, `DeltaS_mol(m)` is elevated from early life and dominates `DeltaS_neurodeg(m)`.

2. Even so, differences in `DeltaS_maint(m)` and `DeltaS_circuit(m)` can shift the age of onset and severity by significant margins.

3. For the majority without such mutations, maintenance and other modifiable factors remain major determinants of crossing `Sigma_crit`.

### 5.4 Interpretive note

These worlds are not exclusive or exhaustive.
They express patterns in observable quantities under different parameterisations.
Empirical work can gradually rule out or constrain parts of these worlds by testing how `DeltaS_neurodeg` and its components behave under interventions and across cohorts.

---

## 6. Falsifiability and discriminating experiments

This section specifies effective layer experiments and protocols that can:

* test the coherence of the Q087 encoding,
* distinguish between different neurodegeneration tension models under the same data,
* and provide evidence for or against particular encoding and weight choices.

All experiments are restricted to `M_neurodeg_reg`.
Encoding and weight choices in each experiment must be taken from the finite libraries defined earlier and fixed before outcome analysis.
Definitions of `Sigma_crit` in terms of observed markers are also part of the preregistered encoding version.

These experiments cannot prove or disprove any biological claim in a strict sense.
They can falsify specific TU encodings for Q087.

### Experiment 1: Longitudinal cohort with maintenance and tension history

**Goal**

Test whether trajectories with higher long term `DeltaS_maint(m)` and `DeltaS_neurodeg(m)` are more likely to cross the critical surface `Sigma_crit` over a multi decade horizon.

**Setup**

* Population: a large prospective cohort of middle aged individuals without clinical neurodegenerative disease at baseline.

* Follow up: repeated assessments every several years, over at least ten to twenty years.

* Collected observables:

  * `Prot_burden(m; region, species)` via imaging and fluid biomarkers,
  * `Syn_health(m; region)` and `Net_dyn(m; scale)` via imaging and electrophysiology,
  * `Maint_sup(m; window)` including sleep metrics and vascular indicators,
  * `Clin_func(m; domain)` across cognitive and functional domains,
  * `Reserve_cap(m)` via education, occupation, and network redundancy proxies.

**Protocol**

1. Before data analysis, register:

   * one encoding from `Lib_mol`,
   * one encoding from `Lib_circuit`,
   * one encoding from `Lib_maint`,
   * one weight triplet from `Lib_weights`,
   * one encoding of `Damage_index(m)` from `Lib_H_damage` and parameters `(alpha, beta)` from `Lib_H_params`,
   * one operational definition of crossing `Sigma_crit` in terms of structural and functional markers.

2. For each participant and time interval, construct effective states `m_t` in `M_neurodeg_reg` using a single `E_k` from `Registry_ND`.

3. Compute `DeltaS_mol(m_t)`, `DeltaS_circuit(m_t)`, `DeltaS_maint(m_t)`, `DeltaS_neurodeg(m_t)`, `H(m_t)`.

4. Define an empirical approximation of crossing `Sigma_crit` by:

   * a combination of structural markers exceeding thresholds, and
   * clinically meaningful decline in `Clin_func(m; domain)` beyond predefined limits.

5. Estimate associations between:

   * baseline and time averaged `DeltaS_maint(m_t)` and `DeltaS_neurodeg(m_t)`,
   * and the probability and timing of crossing `Sigma_crit`.

**Metrics**

* Distributions of `DeltaS_neurodeg(m_t)` over time in individuals who do or do not cross `Sigma_crit`.
* Hazard ratios for crossing `Sigma_crit` across quantiles of `DeltaS_maint(m_t)` and `DeltaS_neurodeg(m_t)` at baseline and mid life.
* Goodness of fit of the drift model `G(m_t, u_t)` when fitted to observed changes.

**Falsification conditions**

The selected encoding is considered falsified if, after appropriate controls:

* there is no detectable monotone relationship between baseline or time averaged `DeltaS_neurodeg(m_t)` and subsequent crossing of `Sigma_crit`, or

* encodings with different weight choices but similar biological meaning produce arbitrarily different conclusions, in a way that cannot be justified by measurement noise.

This does not falsify all possible Q087 encodings.
It rejects the specific combination of libraries and parameters used in this experiment as a candidate baseline.

**Audit trace requirements**

For this experiment, the following must be logged:

* identifiers of the selected encodings for each library and weight set,
* the chosen `E_k` in `Registry_ND`,
* summary distributions of observables and tension scores,
* the operational definition of crossing `Sigma_crit`,
* a record of any deviations from the preregistered plan.

**Domain note**

All analyses must explicitly report the fraction of states that fall into `S_sing_neurodeg`.
Such states cannot be counted in tension based distributions or used to support or refute World N, W, or G.
They should instead be used to debug encodings or data quality.

**Boundary note**

This experiment can support or refute particular tension encodings as useful summary variables.
It does not by itself identify a biologically unique first cause mechanism, nor does it provide clinical risk prediction tools.

---

### Experiment 2: Manipulation of maintenance tension in high risk groups

**Goal**

Quantify the effect of targeted maintenance interventions on the trajectory of `DeltaS_neurodeg(m_t)` and the probability of crossing `Sigma_crit` in populations at elevated risk.

**Setup**

* Population: individuals at high genetic or family risk for neurodegenerative diseases, but currently asymptomatic.

* Arms:

  * intensive maintenance intervention arm, combining:

    * structured sleep improvement based on Q086,
    * vascular risk control,
    * metabolic regulation,

  * standard care arm.

* Observables:

  * the same categories as in Experiment 1, with higher resolution for maintenance related variables.

**Protocol**

1. Register encodings and weights as in Experiment 1, possibly reusing a subset for consistency, including a fixed definition of `Sigma_crit`.

2. Implement interventions for a fixed period, for example five to ten years, with regular assessments.

3. Construct state trajectories `m_t` in `M_neurodeg_reg` for each individual.

4. Compute tension components and track whether and when individuals cross `Sigma_crit` by the same operational definition.

**Metrics**

* Differences in the trajectory of `DeltaS_maint(m_t)` and `DeltaS_neurodeg(m_t)` between arms.
* Differences in incidence and timing of crossing `Sigma_crit`.
* Changes in estimated drift functional `G(m_t, u_t)` associated with intervention.

**Falsification conditions**

Given a fixed encoding:

* If intensive interventions clearly improve observable maintenance markers but do not produce any measurable reduction in `DeltaS_maint(m_t)` or `DeltaS_neurodeg(m_t)` compared with standard care, the maintenance encoding is misaligned.

* If `DeltaS_maint(m_t)` and `DeltaS_neurodeg(m_t)` show substantial arm differences but there is no corresponding difference in structural or functional outcomes over time, this particular combination of tension components and critical surface encodings is called into question.

**Audit trace requirements**

* Full specification of intervention components and adherence metrics.
* Public registration of encoding choices and `Sigma_crit` operationalisation.
* Summary statistics that allow independent groups to recompute tension trajectories from observables.

**Domain note**

As in Experiment 1, states in `S_sing_neurodeg` must be tracked separately and excluded from core tension trajectories.
Their rate of occurrence should be reported as a quality indicator.

**Boundary note**

This experiment tests the sensitivity of Q087 encodings to realistic interventions.
It does not guarantee that interventions are clinically sufficient or optimal.

---

### Experiment 3: Circuit repair, compensation, and tension rebalancing

**Goal**

Investigate whether circuit level repair or compensation observed in imaging and electrophysiology corresponds to measurable reductions in `DeltaS_circuit(m)` and `DeltaS_neurodeg(m)` even when molecular burden remains high.

**Setup**

* Population: individuals with early neurodegenerative changes and mild cognitive impairment.

* Interventions:

  * cognitive training,
  * neuromodulation techniques,
  * combination programs that aim to enhance network level compensation.

* Observables:

  * `Syn_health(m; region)` and `Net_dyn(m; scale)` with high spatial and temporal resolution,
  * `Prot_burden(m; region, species)` to monitor molecular pathology,
  * `Clin_func(m; domain)`.

**Protocol**

1. Pre register a set of `Lib_circuit` encodings that are designed to detect compensation patterns.

2. Before seeing post intervention outcomes, select one `CircEncoding_r` to use in the main analysis, along with the full Q087 encoding stack.

3. Track trajectories `m_t` across intervention and follow up periods in `M_neurodeg_reg`.

4. Compute changes in `DeltaS_circuit(m_t)` and `DeltaS_neurodeg(m_t)` and relate them to changes in `Clin_func(m; domain)`.

**Metrics**

* The degree to which circuit level improvements translate into reduced tension scores despite stable or rising molecular burden.

* The extent to which such reductions delay or prevent crossing `Sigma_crit`.

**Falsification conditions**

* If circuit repair clearly improves network integration and function but the chosen `DeltaS_circuit(m)` and `DeltaS_neurodeg(m)` fail to reflect any tension reduction, the encoding does not capture compensation and is inadequate.

* If encodings predict large tension reductions that are not matched by improved function, this inconsistency indicates misalignment between the encodings and real world dynamics.

**Audit trace requirements**

* Identification of the specific `CircEncoding_r` and justification for its choice before outcome analysis.

* Logging of all intermediate tension values and their relationship to observable changes.

**Domain note**

Any time points that fall into `S_sing_neurodeg` must be flagged and excluded from plots or statistics that claim to show tension reduction.
They can still be reported as part of the audit log.

**Boundary note**

This experiment probes the flexibility of Q087 encodings in representing compensation.
It does not settle the deeper question of how much compensation is biologically possible.

---

## 7. AI and WFGY engineering spec

This section describes how Q087 can be used as an engineering module in AI systems within the WFGY framework at the effective layer.

All examples in this section can be implemented using synthetic or anonymised data.
Any application that touches real clinical data must pass through separate data governance, privacy, and ethics processes not covered by this document.

### 7.1 Training signals

We define several training signals that encourage models to reason coherently about neurodegeneration as multi component tension rather than as a single scalar label.

1. `signal_neurodeg_tension_profile`

   * Definition: an auxiliary loss that guides the model to predict qualitative patterns of `DeltaS_mol(m)`, `DeltaS_circuit(m)`, and `DeltaS_maint(m)` given descriptions of long term exposures and clinical states.

   * Purpose: push the model toward multi scale thinking instead of one dimensional severity.

2. `signal_maintenance_vs_damage_separation`

   * Definition: a loss that penalises conflation of maintenance factors with irreversible damage, by encouraging distinct latent channels corresponding to `DeltaS_maint(m)` and `Damage_index(m)`.

   * Purpose: maintain a conceptual separation between modifiable maintenance and accumulated damage.

3. `signal_critical_surface_awareness`

   * Definition: a loss that encourages the model to recognise when described scenarios are near a putative critical surface `Sigma_crit` versus firmly on one side.

   * Purpose: improve explanations about thresholds, tipping points, and early versus late interventions.

4. `signal_counterfactual_worlds_neurodeg`

   * Definition: a signal that trains the model to keep reasoning about World N, World W, and World G separate when prompts specify which world to assume.

   * Purpose: avoid mixing incompatible assumptions in a single explanation.

These signals can be implemented purely at the level of structured reasoning about hypothetical scenarios, without access to real patient data.
If they are ever applied to real clinical datasets, that step lies outside Q087 and must be covered by independent review.

### 7.2 Architectural patterns

We outline module patterns that reuse Q087 structures without exposing any deep TU generative rules.

1. `NeurodegTensionHead`

   * Role: given an internal representation of a scenario involving aging, risk factors, and maintenance, output an estimated qualitative pattern of `DeltaS_neurodeg(m)` and its components.

   * Interface:

     * Inputs: contextual embeddings plus structured metadata describing age, risk factors, and observed changes.
     * Outputs:

       * `tension_value` (proxy for `DeltaS_neurodeg`),
       * `tension_mol`, `tension_circuit`, `tension_maint` as decomposed components,
       * optional `H_estimate` as a proxy for `H(m)`.

   * Usage: should only be used to structure reasoning and explanations.
     It must not be used as a direct clinical risk score.

2. `MaintenanceHistoryEncoder`

   * Role: encode long term maintenance histories into a representation suitable for predicting `DeltaS_maint(m)` and its interaction with other tensions.

   * Interface:

     * Inputs: sequences of maintenance relevant events and states.
       For example sleep patterns, cardiovascular metrics, lifestyle changes.

     * Outputs: a vector summarising maintenance tension trajectory features.

   * Connection: feed this representation into `NeurodegTensionHead`.

3. `NeurodegScenarioFilter`

   * Role: filter model outputs that make implausible claims about neurodegeneration trajectories given tension structure.

   * Interface:

     * Inputs: candidate outputs containing statements about disease risk and progression.
     * Outputs: a score indicating consistency with qualitative properties of `DeltaS_neurodeg`, and flags for likely contradictions.

### 7.3 Evaluation harness

A simple evaluation harness for AI models augmented with Q087 structures can operate at the narrative level.

1. Task selection

   * Construct a set of text based scenarios that describe:

     * different patterns of long term maintenance and risk,
     * different combinations of molecular and circuit level findings,
     * different intervention timings.

   * For each scenario, expert designed qualitative expectations for tension component behaviour are recorded.

2. Conditions

   * Baseline condition: model answers questions about these scenarios without explicit Q087 prompts.

   * Q087 enhanced condition: model is asked to organise reasoning using multi component tension and critical surface concepts.

3. Metrics

   * Structural clarity: whether explanations distinguish between maintenance and damage, and mention multi scale interactions.

   * Consistency: whether narratives about different time points in the same scenario maintain coherent tension trajectories.

   * Counterfactual separation: whether the model respects specified world assumptions (World N, W, G).

### 7.4 Clinical safety boundary

Because Q087 directly references human diseases, explicit safety rules are required.

1. Models that implement Q087 based modules must not present outputs as personalised medical advice.

2. Any use of Q087 language in user facing contexts should include a clear notice that:

   * the explanation is conceptual and educational,
   * it is not a risk prediction tool,
   * users should seek real clinical care for health concerns.

3. Q087 based modules may be used for research planning, hypothesis generation, and narrative consistency checks, but only within frameworks that have their own ethical review.

### 7.5 Sixty second reproduction protocol

For external reviewers, a minimal protocol can illustrate the difference between reasoning with and without Q087 structures.

* Baseline:

  * Ask the model to explain why two people with similar ages but different life histories might differ in neurodegeneration risk.
  * Observe whether the explanation uses only vague labels or whether it considers multi scale mechanisms.

* Q087 framed:

  * Ask the model to explain the same scenario explicitly in terms of `DeltaS_mol`, `DeltaS_circuit`, `DeltaS_maint`, and a critical surface `Sigma_crit`.
  * Compare whether the explanation becomes more structured and whether it respects maintenance versus damage separation.

This protocol does not involve real data.
It is a behavioural check on structured reasoning.

---

## 8. Cross problem transfer template

### 8.1 Reusable components produced by Q087

1. ComponentName: `NeurodegMultiScaleState`

   * Type: state representation

   * Minimal interface:

     * Inputs: summaries of molecular, circuit, maintenance, functional, and reserve features over multi year windows.
     * Output: an element in a representation compatible with `M_neurodeg_reg`.

   * Preconditions: summaries must be internally consistent and within realistic ranges.

2. ComponentName: `NeurodegTensionFunctional`

   * Type: functional

   * Minimal interface:

     * Inputs: a `NeurodegMultiScaleState` representation and identifiers of encodings from `Lib_mol`, `Lib_circuit`, `Lib_maint`, `Lib_weights`, `Lib_H_damage`, and `Lib_H_params`.
     * Outputs:

       * `DeltaS_mol(m)`, `DeltaS_circuit(m)`, `DeltaS_maint(m)`,
       * `DeltaS_neurodeg(m)`,
       * `H(m)` and a flag for location relative to `Sigma_crit`.

   * Preconditions: encodings and weights must be declared before evaluation on actual data.

3. ComponentName: `NeurodegTrajectoryExperiment_Template`

   * Type: experiment pattern

   * Minimal interface:

     * Inputs: specification of population, follow up duration, observables, interventions, and an encoding version `Version_ND`.
     * Output: a protocol that defines how to construct `m_t`, how to compute tension trajectories, and how to log audit traces.

   * Preconditions: experiments must be ethically feasible and practically implementable.

### 8.2 Direct reuse targets

1. Q098 (BH_EARTH_ANTHROPOCENE_L3_098)

   * Reused components: `NeurodegTensionFunctional`, `NeurodegTrajectoryExperiment_Template`.
   * Why it transfers: population distributions of `DeltaS_neurodeg(m)` can be aggregated into societal level measures of cognitive capacity and vulnerability.

2. Q100 (BH_SOC_PANDEMIC_RISK_L3_100)

   * Reused components: `NeurodegMultiScaleState`, `NeurodegTensionFunctional`.
   * Why it transfers: neurodegeneration patterns affect resilience and response capacity during crises.

3. Q123 (BH_AI_INTERP_L3_123)

   * Reused components: conceptual pattern of cumulative tension and critical surfaces.
   * Why it transfers: long running AI systems can exhibit analogous slow degradation under continuous load and incomplete maintenance.

All reuse is at the effective layer.
No deep TU mechanisms are exported.

---

## 9. TU roadmap and verification levels

### 9.1 Current levels

For Q087, the current verification levels are:

* E_level: E1

  * A coherent effective encoding of multi scale neurodegeneration tension has been specified.
  * State space, observables, mismatch quantities, combined tension functional, dynamics, and a critical surface are defined.
  * At least one experiment template with falsification conditions has been described.

* N_level: N2

  * The narrative linking molecular, circuit, maintenance, reserve, and irreversible transition is explicit and internally consistent at the effective layer.
  * Counterfactual worlds (World N, World W, World G) are defined in terms of observables.

These levels correspond to the flags in the header metadata.

### 9.2 Next measurable step toward E2

To move from E1 to E2, at least one of the following must be achieved.

1. Implementation of a prototype analysis pipeline that:

   * instantiates specific encodings from `Lib_mol`, `Lib_circuit`, `Lib_maint`, `Lib_weights`, `Lib_H_damage`, and `Lib_H_params`,
   * computes `DeltaS_neurodeg(m_t)` and related quantities for a real cohort with longitudinal data,
   * publishes both procedures and anonymised tension summaries along with falsification outcomes for the chosen encodings.

2. Execution of a partial version of Experiment 1 or Experiment 2, where:

   * the arm structure, observables, encodings, and weight choices are clearly registered in advance,
   * resulting distributions of tension trajectories and empirical crossing of `Sigma_crit` are documented.

These steps remain purely at the effective layer.
They do not require specifying internal TU generative rules.

### 9.3 Long term role in the TU programme

In the long term, Q087 is expected to serve as:

* The central node for neurodegeneration related tension modelling, connecting neuroscience, aging, public health, and AI reliability.

* A benchmark example of how to encode slow, multi scale, partially irreversible transitions using:

  * finite encoding libraries,
  * explicit fairness constraints,
  * dynamic tension evolution and critical surfaces.

* A source of reusable patterns for other biological and technological systems that combine:

  * maintenance versus damage,
  * reserve versus burden,
  * slow drift toward thresholds.

---

## 10. Elementary but precise explanation

This block is written for non specialists while remaining aligned with the effective layer description.

Neurodegenerative diseases such as Alzheimer and Parkinson are puzzling.
They appear slowly, often over many years.
They affect some brain regions more than others.
They often involve several types of damage at once.

This document does not claim to know the final biological answer.
Instead, it proposes a way to describe the problem in a more structured way.

1. We imagine that each brain has a kind of long term stress score, called `DeltaS_neurodeg(m)`.
   This score is not one simple number in reality.
   It is built from three parts:

   * molecular and protein stress,
   * damage to circuits and networks,
   * failures of maintenance and cleaning processes such as sleep, blood flow, and waste clearance.

2. We also imagine that each brain has a reserve, called `Reserve_cap(m)`.
   This includes extra connections, backup pathways, and ways to work around small problems.

3. We then define a kind of boundary, called `Sigma_crit`.
   On one side of this boundary, reserve is strong enough to handle the level of damage.
   On the other side, damage has become too large compared to reserve, and the system is in trouble.

In this picture:

* Healthy aging means that the combined stress stays relatively low,
  and the system stays on the safe side of the boundary.

* Neurodegeneration means that over many years the combined stress grows,
  reserve is used up,
  and eventually the system crosses the boundary into a regime where problems spread and are hard to reverse.

The document then:

* gives precise names to the different kinds of stress and reserve,
* defines how they could be combined into a single tension score,
* describes how this score might change over time,
* and suggests experiments that could test whether this way of measuring things is useful.

It also sets clear boundaries.

* It does not say that we already know how to stop Alzheimer or Parkinson.
* It does not provide rules for diagnosing or treating individuals.
* It only offers a structured way to think about the problem and to design future studies.

In the Tension Universe programme, this is what it means to treat neurodegenerative mechanisms as an S level problem.
We first build careful definitions at the effective layer.
Any stronger claims must respect these definitions and must be tested against real data.

---

## Tension Universe effective-layer footer

This page is part of the WFGY / Tension Universe S problem collection.

### Scope of claims

* The goal of this document is to specify an effective layer encoding of the named problem.
* It does not claim to prove or disprove any canonical biomedical hypothesis.
* It does not introduce new biological theorems beyond what is consistent with existing literature.
* It must not be cited as evidence that neurodegenerative diseases have been solved or that specific interventions are effective.
* Any engineering suggestions in Sections 7 and 8 are proposals for tools and benchmarks, not guarantees of safety or clinical performance.

### Effective layer boundary

* All objects used here, including state spaces `M`, observables, invariants, tension scores, dynamic maps, and critical sets, live inside the effective layer of the TU framework.
* They are one candidate family of encodings compatible with current knowledge.
  They are not asserted to be unique, final, or literally realised in biology.
* No claim is made that `DeltaS_neurodeg(m)` or any related functional can be measured directly without additional modelling assumptions.
* When this page is used in empirical or AI work, all mappings from raw data into the objects defined here must be documented separately and can themselves be tested or falsified.

### Relation to TU charters

This page should be read together with the following charters.

* [TU Effective Layer Charter](../Charters/TU_EFFECTIVE_LAYER_CHARTER.md)
* [TU Encoding and Fairness Charter](../Charters/TU_ENCODING_AND_FAIRNESS_CHARTER.md)
* [TU Tension Scale Charter](../Charters/TU_TENSION_SCALE_CHARTER.md)
* [TU Global Guardrails](../Charters/TU_GLOBAL_GUARDRAILS.md)

These charters define global constraints on how effective layer objects are introduced, how encoding families and weights are selected, and how tension scales are compared across problems.

---
