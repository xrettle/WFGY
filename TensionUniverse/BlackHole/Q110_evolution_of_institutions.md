# Q110 · Evolution of institutions

## 0. Header metadata

```txt
ID: Q110
Code: BH_SOC_INSTITUTION_EVOL_L3_110
Domain: Social systems and economics
Family: Institutional dynamics
Rank: S
Projection_dominance: I
Field_type: socio_technical_field
Tension_type: incentive_tension
Status: Open
Semantics: hybrid
E_level: E1
N_level: N2
Last_updated: 2026-01-26
````

---

## 1. Canonical problem and status

### 1.1 Canonical statement

Institutions are the formal and informal rules that structure repeated interaction in societies. They include constitutions, laws, regulations, enforcement bodies, and shared norms of behavior. They shape which coalitions can form, which contracts can be enforced, and which long run trajectories remain feasible.

The canonical problem for Q110 is:

> Is there a general, testable description of how institutions emerge, adapt, ossify, and collapse under long run social, economic, and environmental pressures, beyond specific historical narratives or case studies?

More concretely, Q110 asks for:

1. Effective level state variables that describe institutional configurations and their stress environment.
2. Tension functionals that measure misalignment between rules, incentives, legitimacy, and adaptation.
3. Conditions under which institutions remain inside an adaptive corridor versus drifting toward brittle or predatory regimes.
4. Experiment patterns, both historical and synthetic, that can falsify particular encodings of these laws.

This is not a request for a single closed form equation for history. It is a request for a constrained and falsifiable description of institutional evolution as a socio technical tension system.

### 1.2 Status and difficulty

The evolution of institutions has been studied from several angles:

* Economic history and institutional economics highlight how institutions co evolve with technology and factor endowments, and how small initial differences can lead to large long run divergence.
* Political economy emphasizes elite incentives, coalition formation, and the logic of inclusive versus extractive institutions.
* Complexity and systems theory treat institutions as parts of adaptive networks, often with feedback, path dependence, and lock in.
* Sociology and anthropology focus on norms, legitimacy, and informal governance that often matter as much as written rules.

Despite many influential frameworks, there is no widely accepted general law for institutional evolution with both predictive power and clear falsifiability. Many proposed theories are qualitative, or strongly dependent on specific historical episodes. Others introduce broad mechanisms that are difficult to test cleanly.

The difficulty of Q110 lies in:

* High dimensional state spaces and many latent variables.
* Feedback between institutions and the agents they govern.
* Rare but extreme events such as revolutions, wars, and systemic crises.
* Data limitations and selection bias in historical records.

### 1.3 Role in the BlackHole project

Within the BlackHole S problem collection, Q110 has three main roles:

1. It is the primary node for institutional evolution as a **socio_technical_field** with **incentive_tension** as the central tension type.
2. It provides shared institutional state variables and tension scores that can be reused by problems on crashes, climate, pandemics, migration, and AI oversight.
3. It serves as an example of how to encode soft, narrative heavy domains inside the Tension Universe while preserving falsifiability and clear domain restrictions.

### References

1. Douglass C. North, "Institutions, Institutional Change and Economic Performance", Cambridge University Press, 1990.
2. Daron Acemoglu and James A. Robinson, "Why Nations Fail: The Origins of Power, Prosperity, and Poverty", Crown, 2012.
3. Elinor Ostrom, "Governing the Commons: The Evolution of Institutions for Collective Action", Cambridge University Press, 1990.
4. W. Brian Arthur, "Increasing Returns and Path Dependence in the Economy", University of Michigan Press, 1994.

---

## 2. Position in the BlackHole graph

This block records how Q110 connects to other problems in the BlackHole graph. Edges are given with one line reasons that point to concrete components or tension types.

### 2.1 Upstream problems

These problems supply prerequisites and tools for Q110.

* Q104 (BH_ECON_INEQUALITY_DYN_L3_104)
  Reason: Inequality dynamics define long run stresses and coalitions that constrain which institutional reforms are politically feasible.

* Q105 (BH_COMPLEX_CRASHES_L3_105)
  Reason: Crash dynamics reveal how institutional structures behave near systemic failure and which tensions become dominant.

* Q106 (BH_COMPLEX_NETWORK_ROBUST_L3_106)
  Reason: Institutional structures are embedded in multilayer networks; network robustness primitives are reused when describing institutional resilience.

* Q107 (BH_SOC_COLLECTIVE_ACTION_L3_107)
  Reason: Collective action constraints determine when rules can be enforced or changed, feeding directly into institutional adaptation capacity.

* Q108 (BH_SOC_POLARIZATION_L3_108)
  Reason: Polarization levels act as stress inputs for Q110 and shape legitimacy and compliance fields.

### 2.2 Downstream problems

These problems reuse Q110 components or depend on its institutional state variables.

* Q101 (BH_ECON_EQUITY_PREM_L3_101)
  Reason: Long run equity premia depend on institutional quality and collapse risk tension imported from Q110.

* Q103 (BH_ECON_GROWTH_SLOW_L3_103)
  Reason: Growth slowdown regimes are partially explained by institutional evolution phases and adaptation rates provided by Q110.

* Q109 (BH_SOC_MIGRATION_L3_109)
  Reason: Migration flows respond to institutional regimes and their evolution; Q110 supplies institutional phase variables.

* Q120 (BH_PHIL_VALUE_OF_INFORMATION_L3_120)
  Reason: The value and misuse of information depend on institutional channels and oversight structures encoded through Q110.

### 2.3 Parallel problems

Parallel nodes share similar tension types but have no direct component dependence.

* Q105 (BH_COMPLEX_CRASHES_L3_105)
  Reason: Both address risk_tail_tension in large socio technical systems, but Q105 focuses on event level crashes while Q110 focuses on slow moving institutional structures.

* Q108 (BH_SOC_POLARIZATION_L3_108)
  Reason: Both feature incentive_tension under feedback between agents and higher order structures, but Q108 focuses on opinion distributions.

* Q098 (BH_EARTH_ANTHROPOCENE_L3_098)
  Reason: Both describe long horizon socio ecological dynamics where institutions and environmental stresses co evolve.

### 2.4 Cross domain edges

Cross domain edges indicate problems that can reuse Q110 components in other fields.

* Q091 (BH_EARTH_CLIMATE_SENS_L3_091)
  Reason: Policy response envelopes to climate sensitivity scenarios depend on institutional adaptation phases drawn from Q110.

* Q092 (BH_EARTH_TIPPING_L3_092)
  Reason: Social tipping points interact with institutional thresholds and collapse risk tension defined in Q110.

* Q100 (BH_EARTH_PANDEMIC_RISK_L3_100)
  Reason: Pandemic preparedness and response are governed by institutional structures whose evolution follows Q110 primitives.

* Q124 (BH_AI_OVERSIGHT_L3_124)
  Reason: AI oversight bodies are institutions embedded in socio technical systems; Q110 provides general rules for their evolution and failure modes.

---

## 3. Tension Universe encoding (effective layer)

All content in this block is at the effective layer. We only describe state spaces, observables, invariants, tension scores, and singular sets. We do not describe any hidden generative rules or any mapping from raw historical data to TU internal fields.

### 3.1 State space

We assume a semantic state space

```txt
M
```

where each element `m` represents a coherent institutional configuration for a given society or organization over a specified time window.

At the effective layer, each `m` encodes:

* A summary of formal rules and organizational structures (for example constitutions, legal frameworks, regulatory bodies).
* A summary of enforcement and administrative capacity (for example ability to apply rules in practice).
* A summary of informal norms and legitimacy signals across major groups.
* A summary of external and internal stressors during the time window (for example economic shocks, conflict intensity, ecological pressures).

We do not specify how `M` is constructed from raw records. We only assume that the summaries are coherent enough for the observables below to be well defined.

### 3.2 Observables and fields

We introduce effective observables on `M`.

1. Structural complexity and modularity

```txt
I_structure(m) >= 0
```

* Measures how differentiated and modular the rule set and organizational chart are in configuration `m`.
* High values correspond to many specialized roles and checks; low values correspond to very simple or highly concentrated rule sets.

2. Enforcement effectiveness

```txt
I_enforcement(m) >= 0
```

* Measures effective enforcement capacity and predictability in `m`.
* High values indicate that rules are applied consistently; low values indicate weak or arbitrary enforcement.

3. Legitimacy and acceptance

```txt
I_legitimacy(m) >= 0
```

* Summarizes perceived legitimacy of institutions among key groups.
* High values indicate broad acceptance; low values indicate contested authority and widespread non compliance.

4. Stress environment

```txt
Stress_vector(m) in R^k
```

* Encodes k distinct stress components for configuration `m`, such as economic contraction, conflict intensity, demographic pressure, and ecological strain.
* Each component is a nonnegative scalar summary for the time window.

5. Adaptation velocity

```txt
Adaptation_rate(m) >= 0
```

* Measures how quickly and coherently institutions adjust rules, enforcement, or organizational structure in response to stress.
* Very low values correspond to rigid institutions; very high values can correspond to chaotic or incoherent change.

All observables are defined so that they are finite on regular states in `M`.

### 3.3 Tension ingredients

We define three main mismatch observables.

1. Incentive mismatch tension

```txt
DeltaS_incentive(m) >= 0
```

This measures the gap between:

* the incentives implied by the formal rule set and enforcement structure, and
* the actual incentives experienced by agents as encoded in `m`.

High `DeltaS_incentive(m)` indicates that agents can systematically benefit from violating or bypassing formal rules, or from exploiting inconsistencies between written rules and enforcement practice.

2. Stress adaptation tension

```txt
DeltaS_adaptation(m) >= 0
```

This measures the mismatch between:

* the level and composition of `Stress_vector(m)`, and
* the observed `Adaptation_rate(m)` and direction of change in `I_structure`, `I_enforcement`, and `I_legitimacy`.

High `DeltaS_adaptation(m)` indicates that institutions change too slowly or in misaligned ways relative to stress.

3. Collapse risk tension

```txt
DeltaS_risk_tail(m) >= 0
```

This is an effective measure of tail risk that the institutional configuration will experience a major breakdown or regime change in the near future. It aggregates signals such as:

* very high incentive mismatch,
* rapid declines in legitimacy,
* growing stress with low adaptation.

It is defined at the effective layer as a scalar risk tension, not as a precise probabilistic forecast.

### 3.4 Combined institutional tension

We define a combined institutional tension observable

```txt
DeltaS_inst(m) = w_inc * DeltaS_incentive(m)
               + w_adapt * DeltaS_adaptation(m)
               + w_risk * DeltaS_risk_tail(m)
```

where:

* `w_inc`, `w_adapt`, and `w_risk` are positive weights that satisfy

  ```txt
  w_inc + w_adapt + w_risk = 1
  ```

* The weights are chosen once for a given study or experiment, based on transparent criteria about which tension channels are considered primary, and are fixed before any outcome is evaluated.

* The weights are not allowed to depend on the specific world state `m` or on the outcomes of the experiment being evaluated. This fairness constraint prevents trivial tuning that would always produce low tension.

### 3.5 Effective tension tensor

Following the general TU core, we assume an effective semantic tension tensor on `M`:

```txt
T_ij(m) = S_i(m) * C_j(m) * DeltaS_inst(m) * lambda(m) * kappa
```

where:

* `S_i(m)` is a source like factor representing the strength of the ith institutional or agent group source component in configuration `m`.
* `C_j(m)` is a receptivity like factor representing how sensitive the jth downstream domain is to institutional tension (for example financial markets, social stability, ecological response).
* `DeltaS_inst(m)` is the combined institutional tension defined above.
* `lambda(m)` is a convergence state variable from the TU core that encodes whether local reasoning and adaptation are convergent, recursive, divergent, or chaotic.
* `kappa` is a global coupling constant for Q110 that sets the overall scale of institutional tension in this encoding.

The detailed indexing of `i` and `j` is not needed at the effective layer, as long as for each `m` the tensor entries are well defined and finite on regular states.

### 3.6 Invariants and effective constraints

We sketch two invariants that will be used in later blocks.

1. Resilience band

```txt
I_resilience(m) = f(DeltaS_inst(m), Stress_vector(m))
```

where `f` is a fixed nonnegative function that maps institutional tension and stress levels into a scalar resilience indicator. Low `I_resilience(m)` corresponds to configurations that are far from collapse even under stress. High `I_resilience(m)` indicates proximity to institutional failure.

2. Adaptation corridor indicator

We define an indicator

```txt
I_corridor(m) in {0, 1}
```

that equals 1 when:

* `DeltaS_incentive(m)` and `DeltaS_adaptation(m)` are below fixed thresholds that depend on the magnitude of `Stress_vector(m)`, and
* `I_legitimacy(m)` is above a minimum threshold.

Otherwise `I_corridor(m)` equals 0. The thresholds are part of the encoding and must be fixed before using the indicator in experiments.

`I_corridor(m) = 1` is interpreted as the configuration being inside an adaptive corridor.

### 3.7 Singular set and domain restrictions

Some observables may be undefined or not finite when the encoded summaries are inconsistent or missing. To handle this we define the singular set

```txt
S_sing = { m in M : any of
           DeltaS_incentive(m),
           DeltaS_adaptation(m),
           DeltaS_risk_tail(m),
           DeltaS_inst(m)
           is undefined or not finite }
```

We impose the following domain restriction:

* All Q110 analysis at the effective layer is carried out on

  ```txt
  M_reg = M \ S_sing
  ```

* If a protocol would require evaluating these observables on a state in `S_sing`, the outcome is labeled "out of domain" and is not treated as evidence for or against any institutional evolution law.

---

## 4. Tension principle for this problem

This block states how Q110 is characterized as a tension problem within TU, at the effective layer.

### 4.1 Core institutional tension functional

We define the institutional tension functional as

```txt
Tension_inst(m) = DeltaS_inst(m)
```

so that the combined mismatch in incentives, adaptation, and collapse risk is itself the core tension observable.

By construction:

```txt
Tension_inst(m) >= 0
```

for all `m` in `M_reg`. Configurations with small `Tension_inst(m)` are interpreted as being internally coherent and suitably adaptive relative to their stress environment. Configurations with large `Tension_inst(m)` are interpreted as being misaligned and at increased risk of failure.

### 4.2 Low tension evolution corridor

At the effective layer, a low tension evolution corridor is specified by the following qualitative properties:

* Incentive mismatches remain bounded despite changing stress; rule systems adapt in ways that keep `DeltaS_incentive(m)` small.
* Adaptation rates respond to stress in a roughly proportional way, so that `DeltaS_adaptation(m)` does not accumulate across several stress cycles.
* Collapse risk tension `DeltaS_risk_tail(m)` remains within an acceptable band for long spans of time.
* The resilience indicator `I_resilience(m)` stays below a fixed critical band, and the corridor indicator satisfies `I_corridor(m) = 1` for most time steps.

In this corridor, institutional evolution consists mostly of continuous adjustment and modular reform rather than frequent breakdowns.

### 4.3 High tension pre collapse regimes

High tension regimes have the opposite signature:

* Formal rules and actual incentives diverge, leading to sustained high `DeltaS_incentive(m)`.
* Institutions either fail to adapt (rigid) or change in incoherent bursts that do not track stress, increasing `DeltaS_adaptation(m)`.
* Collapse risk tension `DeltaS_risk_tail(m)` rises, and the resilience indicator moves into a critical band.
* The corridor indicator `I_corridor(m)` frequently takes value 0, especially just before major institutional breakdowns.

Q110 is the request to encode these regimes in terms of well defined observables and to propose conditions under which institutions transition between them in ways that can be tested empirically or in synthetic models.

---

## 5. Counterfactual tension worlds

We describe two counterfactual worlds at the effective layer.

* World T: institutions mostly evolve inside a low tension adaptive corridor.
* World F: institutions frequently enter and remain in high tension pre collapse regimes.

No hidden generative rules are specified. These worlds are described only through observable patterns.

### 5.1 World T: adaptive institutions

In World T:

1. Incentive alignment

   * For world representing states `m_T` in `M_reg`, the incentive mismatch tension `DeltaS_incentive(m_T)` remains below a threshold band that scales with stress magnitude.
   * Deviations appear but are corrected by reforms before they become persistent.

2. Adaptation and stress

   * `DeltaS_adaptation(m_T)` remains moderate because adaptation rate adjusts to stress levels.
   * When `Stress_vector(m_T)` increases, institutions gradually revise rules and enforcement structures in ways that decrease adaptation tension after a finite delay.

3. Collapse risk

   * `DeltaS_risk_tail(m_T)` remains low for most configurations, with occasional spikes that are usually resolved by reforms rather than full institutional breakdown.
   * These spikes are preceded by visible increases in `DeltaS_incentive(m_T)` and `DeltaS_adaptation(m_T)`.

4. Corridor occupancy

   * The indicator `I_corridor(m_T)` equals 1 for long stretches of historical time, with relatively rare and short deviations to 0.

### 5.2 World F: brittle or predatory institutions

In World F:

1. Incentive drift

   * There are long periods where `DeltaS_incentive(m_F)` increases and stays high, indicating that formal rules and actual incentives are sharply misaligned.
   * Loopholes, corruption, and shadow norms become entrenched.

2. Failed adaptation

   * `Stress_vector(m_F)` grows or fluctuates, but `Adaptation_rate(m_F)` remains low or misdirected.
   * `DeltaS_adaptation(m_F)` remains large, reflecting poor matching between stress and institutional change.

3. Elevated collapse risk

   * `DeltaS_risk_tail(m_F)` stays in or near a critical band.
   * Institutional breakdowns, abrupt regime changes, or severe loss of legitimacy occur more frequently.

4. Corridor occupancy

   * The indicator `I_corridor(m_F)` frequently equals 0 over long spans, and transitions back to 1 are irregular and often followed by new drift into high tension regimes.

### 5.3 Interpretive note

These counterfactual worlds do not assert any specific micro level mechanism. They only state that, given an effective institutional encoding, observable tension patterns would look very different in a world where institutions reliably adapt versus a world where they routinely become brittle or predatory.

---

## 6. Falsifiability and discriminating experiments

This block describes experiments and protocols that can falsify specific Q110 encodings at the effective layer. They do not prove or disprove any particular grand theory of institutions, but they can reject particular choices of observables and tension functionals.

### Experiment 1: Historical panel tension tracking

*Goal:*

Test whether a given Q110 encoding can produce institutional tension scores that meaningfully anticipate major institutional breakdowns or sustained stability in a historical panel.

*Setup:*

* Select a panel of countries or large organizations over several decades with recorded institutional and macro indicators.
* For each time window, construct an effective state `m_data` that encodes `I_structure`, `I_enforcement`, `I_legitimacy`, `Stress_vector`, and `Adaptation_rate` using published indices and event data.
* Fix weights `w_inc`, `w_adapt`, and `w_risk` and threshold bands for `I_resilience` and `I_corridor` before looking at breakdown outcomes.

*Protocol:*

1. For each configuration `m_data` in the panel, compute `DeltaS_incentive(m_data)`, `DeltaS_adaptation(m_data)`, `DeltaS_risk_tail(m_data)`, and `Tension_inst(m_data)`.
2. Label periods as "pre breakdown" if a major institutional collapse or regime change occurs within a fixed forward window, and "non breakdown" otherwise.
3. Compare the distribution of `Tension_inst(m_data)` and `I_corridor(m_data)` values between pre breakdown and non breakdown periods.
4. Repeat with different panels and time horizons to test robustness.

*Metrics:*

* Separation between tension distributions for pre breakdown and non breakdown periods.
* Hit rate and false alarm rate when using threshold rules on `Tension_inst` or `I_corridor` as early warning indicators.
* Stability of results under reasonable variation of the weights and thresholds that remain within the predefined admissible set.

*Falsification conditions:*

* If, across multiple panels, `Tension_inst` fails to distinguish pre breakdown from non breakdown periods better than simple baselines (for example random or trivial predictors), the current Q110 encoding is considered falsified.
* If small and justified parameter changes cannot salvage predictive separation, the encoding is rejected as ineffective for institutional evolution.

*Semantics implementation note:*

The experiment treats the hybrid semantics as a combination of discrete time steps and continuous indicator values. All observables are computed from finite historical records and are represented as real valued summaries indexed by discrete periods.

*Boundary note:*

Falsifying TU encoding != solving canonical statement. This experiment only rejects specific institutional tension encodings and does not deliver a complete law of institutional evolution.

---

### Experiment 2: Synthetic agent based institutional models

*Goal:*

Check whether Q110 tension metrics can reliably distinguish robust and fragile institutions in controlled synthetic societies where ground truth robustness is known by construction.

*Setup:*

* Construct simple agent based models with different institutional designs, such as:

  * high concentration of authority versus distributed authority,
  * clear enforcement rules versus ambiguous enforcement,
  * inclusive decision rules versus narrow elite control.
* Subject these models to controlled stress processes (for example shocks to resources, external threats, internal conflicts).

*Protocol:*

1. For each model configuration and time window, map the simulated institutional state into an effective state `m_sim` in `M_reg` with values for `I_structure`, `I_enforcement`, `I_legitimacy`, `Stress_vector`, and `Adaptation_rate`.
2. Compute `DeltaS_incentive(m_sim)`, `DeltaS_adaptation(m_sim)`, `DeltaS_risk_tail(m_sim)`, and `Tension_inst(m_sim)` along each simulated trajectory.
3. Label model runs as "robust" if institutions maintain function under stress and "fragile" if they suffer collapse or severe loss of function.
4. Compare tension patterns across robust and fragile designs.

*Metrics:*

* Mean and variance of `Tension_inst(m_sim)` for robust and fragile runs.
* Frequency with which `I_corridor(m_sim)` remains equal to 1 in robust designs and drops to 0 in fragile designs.
* Time lead between tension spikes and observed collapse events in fragile models.

*Falsification conditions:*

* If Q110 tension metrics fail to separate clearly robust and clearly fragile institutional designs in a wide range of synthetic models, the encoding is considered misaligned with institutional stability and is rejected.
* If designs that are obviously fragile by construction consistently produce lower `Tension_inst` than robust designs, the current choice of observables or weights is considered invalid.

*Semantics implementation note:*

The simulation state space is discrete in time and agent configuration, but observables are aggregated into continuous summary values at each time step, consistent with the hybrid semantics in the metadata.

*Boundary note:*

Falsifying TU encoding != solving canonical statement. Success or failure on synthetic models only tests the encoding, not any universal law of institutional evolution.

---

## 7. AI and WFGY engineering spec

This block describes how Q110 structures can be used as modules inside AI systems within the WFGY framework, at the effective layer.

### 7.1 Training signals

We define several training signals for models that reason about institutions.

1. `signal_institutional_alignment`

   * Definition: a penalty proportional to `DeltaS_incentive(m)` whenever the model proposes institutional stories where written rules and implied incentives conflict strongly.
   * Purpose: encourage narratives where incentives, rules, and enforcement form a coherent pattern.

2. `signal_adaptive_response`

   * Definition: a signal derived from `DeltaS_adaptation(m)` during sequences that describe shocks and institutional responses.
   * Purpose: reward sequences where adaptation matches the magnitude and direction of stresses, according to the Q110 encoding.

3. `signal_collapse_risk_awareness`

   * Definition: an auxiliary head that predicts `DeltaS_risk_tail(m)` given an institutional context, with loss based on consistency between predicted risk tension and described events.
   * Purpose: teach the model to identify configurations that are near institutional collapse in its internal representation.

4. `signal_corridor_stability`

   * Definition: a signal that compresses multiple observables into a soft version of `I_corridor(m)` and penalizes frequent transitions out of the corridor in scenarios that historically remained stable.
   * Purpose: align the model with empirical patterns of long run stability.

### 7.2 Architectural patterns

We outline module patterns that reuse Q110 components.

1. `InstitutionTensionHead`

   * Role: given an internal embedding of an institutional context, output estimates of `DeltaS_incentive`, `DeltaS_adaptation`, `DeltaS_risk_tail`, and `Tension_inst`.
   * Interface: input is a context embedding; outputs are four nonnegative scalars.

2. `ShockResponseModule`

   * Role: predict likely institutional adaptations given a stress vector and current configuration.
   * Interface: inputs are an embedding of `m` and a representation of `Stress_vector(m)`; outputs are proposals for changes in structure, enforcement, and legitimacy with associated changes in tension metrics.

3. `ScenarioComparator`

   * Role: compare alternative institutional scenarios for the same stress environment and return which is more likely to remain inside the adaptive corridor.
   * Interface: inputs are pairs of scenario embeddings and stress summaries; outputs are rankings and tension differences.

### 7.3 Evaluation harness

We propose an evaluation harness that uses historical and synthetic vignettes.

1. Task selection

   * Assemble short descriptions of historical episodes where institutions faced major stress events, with known outcomes (collapse, reform, or continued stability).

2. Conditions

   * Baseline: models answer questions about these episodes without explicit Q110 modules or signals.
   * TU condition: models are augmented with the Q110 modules, and tension metrics are used as auxiliary losses and outputs.

3. Metrics

   * Accuracy on questions about which episodes led to institutional breakdown versus reform.
   * Consistency in explaining why some institutions adapted and others failed, measured by internal use of tension variables.
   * Stability of answers under small perturbations of prompts that do not change the underlying institutional facts.

### 7.4 60 second reproduction protocol

This protocol lets external users experience the effect of Q110 encoding in an AI system.

* Baseline setup

  * Prompt: ask the model to explain why some countries have institutions that adapt successfully to shocks while others repeatedly collapse or drift into predatory regimes, using any concepts it prefers.
  * Observation: record whether the explanation is mostly a list of stories or whether it identifies clear structural patterns and measurable tensions.

* TU encoded setup

  * Prompt: ask the same question but require the model to structure its answer using:

    * institutional tension between rules, incentives, and stress,
    * the distinction between staying inside an adaptive corridor and entering high tension regimes, and
    * the Q110 observables at the effective layer.
  * Observation: record whether the explanation becomes more structured, with explicit reference to incentive mismatch, adaptation gaps, and collapse risk.

* Comparison metric

  * Use a simple rubric for structure, clarity of mechanisms, and consistency across examples.
  * Optionally, have independent evaluators judge which explanation better captures known results in institutional economics and political economy.

* What to log

  * Prompts, full responses, and any auxiliary tension scores from Q110 modules.
  * This allows later analysis of how the model uses institutional tension in its reasoning process, without exposing any deep TU generative rules.

---

## 8. Cross problem transfer template

This block lists reusable components produced by Q110 and their direct reuse targets.

### 8.1 Reusable components produced by this problem

1. ComponentName: `InstitutionalTensionKernel`

   * Type: functional
   * Minimal interface:

     * Inputs: `institution_summary`, `stress_summary`
     * Output: `tension_tuple` containing `DeltaS_incentive`, `DeltaS_adaptation`, `DeltaS_risk_tail`, and `Tension_inst`.
   * Preconditions:

     * The summaries must encode coherent values for structure, enforcement, legitimacy, and stress over a time window.

2. ComponentName: `InstitutionEvolutionPhaseDiagram`

   * Type: field
   * Minimal interface:

     * Inputs: `institution_summary`, `stress_summary`
     * Output: `phase_label` in a small set such as {adaptive_corridor, brittle, predatory, chaotic}.
   * Preconditions:

     * The mapping from observables to phase labels is fixed in advance and consistent with Q110 tension definitions.

3. ComponentName: `ShockResponseTemplate`

   * Type: experiment_pattern
   * Minimal interface:

     * Inputs: `shock_profile`, `initial_institution_summary`
     * Output: a small set of plausible institutional response trajectories, each with associated tension profiles.
   * Preconditions:

     * The shock profile can be represented as a change in `Stress_vector` over time.

### 8.2 Direct reuse targets

1. Q105 (BH_COMPLEX_CRASHES_L3_105)

   * Reused component: `InstitutionalTensionKernel`.
   * Why it transfers: crash probability and severity depend on institutional tension in financial and governance systems.
   * What changes: the stress summary includes financial variables and the phase labels are aligned with crash regimes.

2. Q098 (BH_EARTH_ANTHROPOCENE_L3_098)

   * Reused component: `InstitutionEvolutionPhaseDiagram`.
   * Why it transfers: socio ecological regimes depend on whether institutions remain adaptive under escalating environmental stress.
   * What changes: stress summaries include ecological indicators and resource constraints.

3. Q100 (BH_EARTH_PANDEMIC_RISK_L3_100)

   * Reused component: `ShockResponseTemplate`.
   * Why it transfers: pandemic shocks stress health and governance institutions; response trajectories can be encoded using the same template.
   * What changes: shock profiles focus on epidemiological and health system loads.

4. Q124 (BH_AI_OVERSIGHT_L3_124)

   * Reused component: `InstitutionalTensionKernel` and `InstitutionEvolutionPhaseDiagram`.
   * Why it transfers: AI oversight bodies are institutions with their own rules, incentives, and stress; their evolution can be analyzed using Q110 primitives.
   * What changes: institution summaries include technical oversight capacity and interaction with AI systems.

---

## 9. TU roadmap and verification levels

### 9.1 Current levels

* E_level: E1

  * A coherent effective encoding of institutional evolution is specified.
  * Observables, tension functionals, and singular sets are defined, and experiment patterns are outlined but not yet implemented.

* N_level: N2

  * The narrative connecting rules, incentives, stress, adaptation, and collapse is explicit and consistent across World T and World F.
  * Reusable components and cross domain links are identified.

### 9.2 Next measurable step toward E2

To reach E2, at least one of the following should be completed:

1. Implement Experiment 1 by constructing an open data set of `Tension_inst` and `I_corridor` values over a historical panel and publish the results, including failures where the encoding does not separate breakdown and non breakdown periods.
2. Implement Experiment 2 by creating a simple but transparent agent based model suite where Q110 tension metrics demonstrably separate robust and fragile institutional designs.

Both steps operate only on observable summaries and respect the effective layer boundary. They do not require exposing any TU deep generative rule.

### 9.3 Long term role in the TU program

In the long run, Q110 is expected to function as:

* The main institutional node supplying state variables and tension metrics to problems concerning crashes, climate, pandemics, migration, and AI oversight.
* A template for encoding soft institutional narratives as tension systems with falsifiable components.
* A bridge between qualitative institutional theory and quantitative complex systems approaches, by forcing both to speak through shared observables and tension functionals.

---

## 10. Elementary but precise explanation

At a simple level, Q110 is about the life cycle of rules.

Every society has rules and organizations that say who can do what, who decides, and how conflicts are settled. These rules and organizations are called institutions. They do not stay still. They are pushed and pulled by:

* economic changes,
* wars and conflicts,
* new technologies,
* environmental shocks,
* and struggles among different groups.

Sometimes institutions adjust in time. They reform peacefully, close loopholes, and add new checks. Sometimes they become rigid or corrupt. Tension builds up. People stop believing in them. At some point they may crack, or be replaced by new ones.

The Tension Universe view does not try to predict exact historical events. Instead it asks three questions:

1. Can we describe each institutional situation with a small set of numbers that capture:

   * how rules are written,
   * how they are enforced,
   * how legitimate they feel,
   * how strong the pressures are,
   * and how fast the system is changing?

2. Can we combine these into a single "institutional tension" number that is low when rules, incentives, and pressures are in rough balance, and high when they are not?

3. Can we design experiments, using both history and computer models, that test whether this tension number really tells us something about which institutions will survive and which ones are about to fail?

In this setting:

* A low tension world is one where institutions usually adjust before stress becomes dangerous. Incentives, rules, and enforcement fit together reasonably well. Big collapses are rare.
* A high tension world is one where rules and real incentives drift apart, stress keeps rising, adaptation is slow or chaotic, and collapse becomes more likely.

Q110 does not claim to give a final theory of history. It sets up a way to talk about institutional evolution using clear observables and tension scores. These can then be tested, reused in other problems, and improved over time without exposing any hidden construction of deep TU fields.
