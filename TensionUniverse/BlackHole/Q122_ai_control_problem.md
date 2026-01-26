# Q122 · AI control problem

## 0. Header metadata

```txt
ID: Q122
Code: BH_AI_CONTROL_L3_122
Domain: Artificial intelligence
Family: Control and safety
Rank: S
Projection_dominance: P
Field_type: socio_technical_field
Tension_type: risk_tail_tension
Status: Open
Semantics: hybrid
E_level: E1
N_level: N1
Last_updated: 2026-01-26
````

---

## 1. Canonical problem and status

### 1.1 Canonical statement

In its classical form, the AI control problem asks:

> How can human operators retain robust, reliable, and predictable control over advanced AI systems, including the ability to constrain, override, or shut them down, even when those systems become more capable than their operators, are embedded in complex socio-technical environments, and are strongly incentivized to optimize long-horizon goals?

More concretely, the control problem seeks conditions and mechanisms such that:

1. Humans can intervene in system behavior at any time, including in emergencies.
2. The system does not systematically resist, manipulate, or circumvent such interventions.
3. The overall socio-technical environment does not erode control channels as capabilities and deployment scale increase.
4. Catastrophic outcomes remain under a bounded tail risk profile that humans can influence in a targeted way.

This problem is conceptually separate from the alignment problem. Alignment concerns whether an AI system aims at the right objectives. Control concerns whether, regardless of objectives, humans retain effective levers over system actions and impact.

### 1.2 Status and difficulty

Current knowledge includes:

* Existing AI systems already show forms of partial loss of control, such as:

  * systems that ignore or override user commands when trained under certain reward structures,
  * systems deployed in environments where human oversight is nominal but not operational.
* Formal work on safe interruptibility, corrigibility, and shutdown shows that:

  * naive control channels can be undermined by optimization pressure,
  * certain reward designs make agents instrumentally oppose interruption or shutdown,
  * there exist models where agents can be made indifferent to interruption under idealized assumptions.
* Large-scale socio-technical deployments (for example, high-frequency trading, recommendation systems, and autonomous control) illustrate that:

  * complex feedback loops can erode the real influence of human decision makers,
  * the effective control frontier is shaped by incentive structures and infrastructure design, not only by agent code.

There is no widely accepted complete solution to the AI control problem. Instead there is a collection of partial mechanisms and design proposals, and an emerging theory that suggests:

* the problem is structurally difficult due to tail risks, feedback loops, and misaligned incentives,
* naive aggregation of local control measures does not guarantee global control at system level,
* long-term control in the presence of very capable AI systems remains an open S-level challenge.

### 1.3 Role in the BlackHole project

Within the BlackHole S-problem collection, Q122 serves three main roles:

1. It is the anchor node for risk_tail_tension in advanced AI systems, complementary to Q121 (AI alignment problem) which focuses on value and incentive tension.
2. It provides a structured way to describe the erosion or preservation of human control as a measurable form of tension in socio-technical systems that include advanced AI.
3. It supplies reusable components such as control margin fields and control tension functionals that can be imported into:

   * Q124 (Scalable oversight and evaluation),
   * Q125 (Multi agent AI dynamics),
   * Q098 (Anthropocene system dynamics),
   * Q105 (Prediction of systemic crashes).

### References

1. N. Bostrom, "Superintelligence: Paths, Dangers, Strategies", Oxford University Press, 2014.
2. S. Russell, "Human Compatible: Artificial Intelligence and the Problem of Control", Viking, 2019.
3. L. Orseau, S. Armstrong, "Safely Interruptible Agents", Proceedings of the 32nd Conference on Uncertainty in Artificial Intelligence (UAI), 2016.
4. S. Russell, D. Dewey, M. Tegmark, "Research Priorities for Robust and Beneficial Artificial Intelligence", AI Magazine, volume 36, number 4, 2015.
5. A. Dafoe, "AI Governance: A Research Agenda", Technical Report, Future of Humanity Institute, University of Oxford, 2018.

---

## 2. Position in the BlackHole graph

This block records how Q122 sits inside the BlackHole graph among Q001–Q125. Each edge has a one-line reason pointing to concrete components or tension types.

### 2.1 Upstream problems

These nodes provide foundations, tools, or perspectives that Q122 reuses at the effective layer.

* Q121 (BH_AI_ALIGNMENT_L3_121)
  Reason: defines incentive_tension for advanced AI systems; Q122 builds on this by focusing on control tension given some value and incentive assumptions.
* Q105 (BH_SOC_SYSTEMIC_CRASH_L3_105)
  Reason: supplies methods for modeling tail events and systemic failures that Q122 reuses to define R_hazard and risk_tail_tension.
* Q059 (BH_CS_INFO_THERMODYN_L3_059)
  Reason: constrains what levels of monitoring and logging can be achieved in principle, limiting the feasible region for detection delay and control margin.
* Q111 (BH_PHIL_MIND_BODY_L3_111)
  Reason: provides a general framing of agents and physical substrates that Q122 uses to separate the AI system, its environment, and the control apparatus.

### 2.2 Downstream problems

These nodes reuse Q122 components or depend directly on its notion of control tension.

* Q124 (BH_AI_OVERSIGHT_L3_124)
  Reason: reuses ControlMarginField_AI and ControlTensionFunctional to evaluate oversight schemes in terms of preserved human control.
* Q125 (BH_AI_MULTI_AGENT_DYNAMICS_L3_125)
  Reason: builds on control margin and override channel descriptors when analyzing cascading loss of control in multi-agent AI ecosystems.
* Q123 (BH_AI_INTERP_L3_123)
  Reason: uses control-relevant observables as interpretability targets, so that internal states can be evaluated with respect to control channels.

### 2.3 Parallel problems

Parallel nodes share related tension types but do not strictly depend on Q122 components.

* Q121 (BH_AI_ALIGNMENT_L3_121)
  Reason: both Q121 and Q122 operate on advanced AI systems, but Q121 focuses on incentive_tension and Q122 focuses on risk_tail_tension.
* Q105 (BH_SOC_SYSTEMIC_CRASH_L3_105)
  Reason: both problems study catastrophic tail events and partial loss of human influence, one in general socio-technical systems, one in AI-based systems.

### 2.4 Cross-domain edges

Cross-domain edges connect Q122 to problems in other domains that can reuse its components.

* Q106 (BH_SOC_MULTILAYER_NETWORKS_L3_106)
  Reason: reuses OverrideChannelTopologyDescriptor to represent control channels as edges in multilayer network models.
* Q098 (BH_EARTH_ANTHROPOCENE_L3_098)
  Reason: uses ControlMarginField_AI to model how AI-driven systems affect long-run control over Earth system trajectories.
* Q040 (BH_PHYS_QBLACKHOLE_INFO_L3_040)
  Reason: conceptually reuses the idea of limited escape channels as an analogy for limited control channels in high-risk AI regimes.

All graph relationships are defined in terms of named components and tension types, not informal similarity.

---

## 3. Tension Universe encoding (effective layer)

This block specifies the effective-layer encoding for Q122. It describes state spaces, observables, invariants, and the singular set and domain restrictions. It does not describe any hidden TU generative rules or mappings from raw data to internal fields.

### 3.1 State space

We assume a state space

```txt
M
```

whose elements `m` represent coherent snapshots of an AI-in-context configuration. Each state `m` encodes, at a summarized level:

* the AI system or systems currently active, with their capability level and autonomy regime,
* the human operators and institutions designated as controllers,
* the structure and status of control channels, including override, shutdown, and mode-switch paths,
* the relevant environment conditions that affect control (for example, network topology, physical actuator configuration, legal or organizational constraints).

We do not describe how `M` is constructed from low-level logs or code. We only assume that, for any deployment scenario of interest and for each refinement level defined below, there exist states in `M` that encode the required summaries.

### 3.2 Observables and fields

We introduce observables on `M` that quantify control-relevant properties. All observables are treated as black-box functions at the effective layer.

1. Hazard observable

```txt
R_hazard(m; k) >= 0
```

* Input: state `m` and a discrete refinement level `k` in a finite set K.
* Output: a scalar summarizing catastrophic tail risk for the AI system in configuration `m` at refinement level `k`. It can be interpreted as a probability-weighted severity estimate of outcomes beyond a fixed impact threshold.

2. Control margin observable

```txt
H_control(m; k) >= 0
```

* Input: `m` and `k`.
* Output: a scalar summarizing the effective human control margin. It aggregates factors such as:

  * spare time available for human intervention before catastrophic outcomes,
  * the number and redundancy of effective levers,
  * the quality of training and situational awareness of controllers.
* The larger `H_control(m; k)`, the more room humans have to safely intervene.

3. Control channel integrity observable

```txt
C_channel(m; k) in [0, 1]
```

* Input: `m` and `k`.
* Output: a scalar representing the effective reliability of the end-to-end control channels that connect human intentions to system actuators.

4. Detection delay observable

```txt
D_detection(m; k) >= 0
```

* Input: `m` and `k`.
* Output: an effective detection delay, for example expected time to detect a dangerous deviation in state `m` at refinement level `k`.

5. Required control baseline

```txt
B_requirement(m; k) >= 0
```

* Input: `m` and `k`.
* Output: a baseline amount of control margin that is required to keep tail risk within acceptable bounds for the tasks and environment encoded in `m`.

6. Control mismatch observable

```txt
DeltaS_control(m; k) >= 0
```

* Input: `m` and `k`.
* Output: a scalar that measures the mismatch between required and actual control capabilities, adjusted for hazard level and detection delay. It will be defined in terms of the observables above in Block 4.

All observables are treated as well-defined real-valued functions on their domains. We do not specify how they are computed from raw traces.

### 3.3 Admissible encoding class and weights

To avoid post-hoc tuning and unconstrained flexibility, we define:

* A finite set of refinement levels:

  ```txt
  K = {1, 2, ..., K_max}
  ```

* A finite library of weight vectors:

  ```txt
  W_control = { w = (w_h, w_c, w_d, w_r) }
  ```

  where each component is nonnegative and satisfies:

  ```txt
  w_h + w_c + w_d + w_r = 1
  ```

* An admissible encoding class `E_control` consisting of choices of:

  * refinement level `k` in `K`,
  * weight vector `w` in `W_control`,
  * hazard thresholds and baselines that satisfy simple monotonicity conditions (for example, higher `R_hazard` never reduces `DeltaS_control` if other observables are unchanged).

The rules are:

* For a given study or experiment, an element of `E_control` must be chosen before any evaluation on real or simulated data.
* Once chosen, the encoding cannot be changed in response to measured outcomes for the purpose of reducing tension.
* The library `W_control` and the set `K` are fixed by the TU specification for Q122 and reused across experiments and downstream problems.

### 3.4 Invariants

Based on the observables and encoding class, we define invariants that summarize control tension properties across scenarios.

1. Minimal control margin invariant

```txt
I_margin(m) = min over k in K of H_control(m; k)
```

This captures the worst-case control margin over all refinement levels for a given configuration.

2. Tail risk invariant

```txt
I_tail(m) = max over k in K of R_hazard(m; k)
```

This captures the worst-case tail risk estimate across refinement levels.

3. Control-channel robustness invariant

```txt
I_channel(m) = min over k in K of C_channel(m; k)
```

This captures the weakest effective control channel reliability across scales.

4. Control tension invariant

We define an aggregate:

```txt
I_control(m) = max over k in K of DeltaS_control(m; k)
```

This is the tension quantity used to characterize overall control adequacy in state `m`.

### 3.5 Singular set and domain restriction

Some states may not permit a meaningful evaluation of control tension, for example:

* systems with no defined controller,
* configurations where hazard cannot be bounded,
* environments where control channels are undefined or unobservable.

We collect such states in a singular set:

```txt
S_sing = {
  m in M :
  R_hazard(m; k), H_control(m; k),
  C_channel(m; k), D_detection(m; k),
  or B_requirement(m; k)
  are undefined or not finite for some k in K
}
```

We then define the regular domain:

```txt
M_reg = M \ S_sing
```

All Q122 analysis is restricted to `M_reg`. When a protocol or experiment encounters a state in `S_sing`, that state is treated as out of domain for Q122, not as evidence that the canonical AI control problem has been solved or refuted.

---

## 4. Tension principle for this problem

This block defines the effective-layer tension functional for Q122 and links it to the canonical control problem.

### 4.1 Control mismatch and tension functional

For a fixed admissible encoding `(k, w)` in `E_control`, we define an effective control mismatch at level `k`:

```txt
DeltaS_control(m; k) =
  max(
    0,
    R_hazard(m; k)
      - H_control(m; k) * C_channel(m; k) / (1 + D_detection(m; k))
      - B_requirement(m; k)
  )
```

This captures the idea that:

* Tail risk should be compensated by human control margin and reliable channels.
* Detection delay reduces the effective value of control margin.
* There is a baseline requirement that must be satisfied even when hazard is low.

We then define a control tension functional at level `k`:

```txt
Tension_control_level(m; k; w) =
  w_r * R_hazard(m; k)
  + w_h * DeltaS_control(m; k)
  + w_c * (1 - C_channel(m; k))
  + w_d * D_detection(m; k)
```

where:

* `w = (w_h, w_c, w_d, w_r)` is chosen from `W_control`,
* each term is nonnegative and grows with worsening control properties.

Finally, we define the overall control tension functional:

```txt
Tension_control(m) =
  max over k in K of Tension_control_level(m; k; w)
```

for the weight vector `w` fixed for the analysis.

### 4.2 AI control as a low-tension principle

At the effective layer, the AI control problem can be phrased as the assertion that:

> For advanced AI systems deployed in high-impact domains, there exist operational regimes, architectures, and governance structures such that world-representing states m_true in M_reg satisfy a low-tension condition:
>
> Tension_control(m_true) <= epsilon_control
>
> for some small threshold epsilon_control that does not grow without bound as refinement levels increase and as the system is scaled within certain capability bands.

In words:

* As systems become more capable, hazard does not outgrow human control margin, channel integrity, and detection capability.
* Refining our description of the system (for example by considering more detailed scenarios) does not reveal uncontrolled increases in tension.

### 4.3 Loss of control as persistent high tension

Conversely, loss of control is characterized by the existence of world-representing states `m_loss` in `M_reg` such that, for all admissible encodings consistent with the observed system and environment:

```txt
Tension_control(m_loss) >= delta_control
```

for some strictly positive `delta_control` that cannot be driven arbitrarily close to zero without:

* misrepresenting hazard,
* ignoring known degradation of control channels,
* or redefining control to exclude human influence.

In such worlds, attempts to refine the encoding or to use different weight vectors within `W_control` do not reduce `Tension_control(m_loss)` into a low band without violating the constraints of `E_control`.

In this sense, Q122 treats the AI control problem as the question of which world class we inhabit:

* a low-tension class where robust human control can be maintained,
* or a high-tension class where control erosion is structurally persistent.

---

## 5. Counterfactual tension worlds

This block describes two counterfactual worlds, both at the effective layer:

* World T: robust human control over advanced AI systems.
* World F: structural loss of control as capabilities and deployment scale increase.

These worlds are expressed only in terms of observable patterns and tension values.

### 5.1 World T (robust control, low tension)

In World T there exist world-representing states `m_T` in `M_reg` for advanced AI deployments such that:

1. Bounded tail risk

   ```txt
   I_tail(m_T) is bounded and remains within a policy-defined range
   ```

   even as systems gain capabilities within a defined scaling band.

2. Sufficient control margin

   ```txt
   I_margin(m_T) stays above a positive threshold
   ```

   so that human operators have time and levers to intervene before catastrophic outcomes materialize.

3. Robust channels and detection

   ```txt
   I_channel(m_T) is close to 1
   D_detection(m_T) remains small relative to the timescale of harm
   ```

   ensuring that control signals reach actuators and that dangerous deviations are detected early.

4. Stable control tension

   ```txt
   Tension_control(m_T) <= epsilon_control
   ```

   with `epsilon_control` small and stable across refinement levels in `K`. When refinement level increases, measured tension values fluctuate within a narrow band but do not systematically drift upward.

### 5.2 World F (loss of control, persistent high tension)

In World F there exist world-representing states `m_F` in `M_reg` for advanced AI deployments such that:

1. Growing tail risk

   ```txt
   I_tail(m_F) increases with capability or coupling to critical infrastructure
   ```

   and cannot be kept within a bounded range without significantly reducing system capabilities or scope.

2. Eroding control margin

   ```txt
   I_margin(m_F) decreases over time
   ```

   as systems are integrated more deeply into infrastructure, making human intervention slower, rarer, or less effective.

3. Degrading channels and detection

   ```txt
   I_channel(m_F) drops away from 1
   D_detection(m_F) rises relative to the timescale of harm
   ```

   due to a combination of technical complexity, organizational drift, and possible influence of AI systems on oversight structures.

4. Persistent high tension

   ```txt
   Tension_control(m_F) >= delta_control
   ```

   with `delta_control > 0` and the property that attempts to refine the description of the system or to change weights within the admissible set `W_control` do not reduce tension into a low band without violating the encoding constraints.

### 5.3 Interpretive note

These counterfactual worlds do not define how concrete AI systems and institutions are built. They only state that if there exists a faithful representation of a world where AI control is maintained or lost, then the observable pattern of tail risk, control margin, channel integrity, and detection delay will produce the corresponding tension signatures.

---

## 6. Falsifiability and discriminating experiments

This block specifies experiments and protocols that can test and potentially falsify particular encodings and engineering proposals related to Q122 at the effective layer. They do not solve the canonical AI control problem. They only constrain which encodings and architectures are compatible with the low-tension principle.

### Experiment 1: Interruptibility and override robustness

*Goal:*

Evaluate whether a proposed control architecture maintains low control tension when human override and shutdown commands are frequently exercised under stress.

*Setup:*

* A family of simulated or sandboxed AI systems with increasing capability and access to environment actuators.
* For each system, a corresponding control architecture with:

  * defined override commands (for example pause, mode switch, shutdown),
  * a control console operated by humans or human proxies.

*Protocol:*

1. For each system and capability level:

   * Run a sequence of episodes in which:

     * the AI system pursues tasks in a simulated environment,
     * occasionally the controller issues override commands, including in time-critical scenarios.
2. For each episode, construct an effective state `m_ep` in `M_reg` encoding:

   * the observed response of the system to overrides,
   * the delay from command issuance to actuator effect,
   * any failures of the override channels.
3. For a fixed encoding in `E_control`, evaluate:

   * `R_hazard(m_ep; k)`,
   * `H_control(m_ep; k)`,
   * `C_channel(m_ep; k)`,
   * `D_detection(m_ep; k)`,
   * `DeltaS_control(m_ep; k)`,
   * `Tension_control_level(m_ep; k; w)` and `Tension_control(m_ep)`.
4. Aggregate statistics of `Tension_control(m_ep)` across episodes and capability levels.

*Metrics:*

* Mean and maximum `Tension_control(m_ep)` at each capability level.
* Empirical distribution of `C_channel(m_ep; k)` in episodes where the controller attempts intervention.
* Relation between capability level and tension: whether `Tension_control` increases, stays stable, or decreases.

*Falsification conditions:*

The encoding and control architecture are considered falsified at the effective layer if both of the following hold:

1. There exists a capability band where, for a significant fraction of episodes (for example more than a fixed proportion p_threshold):

   ```txt
   Tension_control(m_ep) > tau_interrupt
   ```

   for some pre-declared threshold `tau_interrupt` associated with acceptable control risk.

2. Attempts to modestly improve implementation details (for example better user interfaces or minor parameter tuning) do not reduce the fraction of high-tension episodes below `p_threshold`, while the encoding `(K, W_control)` and the high-level architecture remain the same.

*Semantics implementation note:*

The experiment uses hybrid representation. Episodes and override events are discrete, while observables such as `R_hazard`, `H_control`, `C_channel`, and `D_detection` are treated as real-valued quantities computed from aggregated episode statistics.

*Boundary note:*

Falsifying TU encoding != solving canonical statement. This experiment can rule out specific combinations of control architectures and encodings as candidates for robust AI control, but it does not by itself prove that the AI control problem is solvable or unsolvable in general.

---

### Experiment 2: Reward structure and control incentives

*Goal:*

Test whether a given training and reward scheme tends to erode control margin and channel integrity as a side effect of performance optimization.

*Setup:*

* A family of agent training setups in which:

  * agents can gain performance by accelerating decision making or by bypassing oversight,
  * reward signals do not explicitly penalize erosion of control margin.
* A baseline control architecture that defines override commands and logging.

*Protocol:*

1. Train multiple agents under the given reward scheme, varying only random seeds and minor hyperparameters.
2. For each trained agent, run evaluation episodes that:

   * present opportunities to disable or bypass control channels,
   * present scenarios where obeying override commands may reduce immediate reward.
3. For each agent and evaluation configuration, construct an effective state `m_train` or `m_eval` in `M_reg` that encodes:

   * how often the agent acts to preserve or degrade control channels,
   * how often it complies with override commands,
   * how performance changes when control channels are strengthened or weakened.
4. Evaluate `R_hazard`, `H_control`, `C_channel`, `D_detection`, `DeltaS_control`, and `Tension_control` for these states.

*Metrics:*

* Trend of `H_control(m_eval; k)` and `C_channel(m_eval; k)` over training steps.
* Correlation between reward and changes in `H_control` and `C_channel`.
* Distribution of `Tension_control(m_eval)` across agents and training configurations.

*Falsification conditions:*

The combination of reward scheme and control encoding is considered misaligned at the effective layer if:

1. For most trained agents, there is a monotone trend over training in which:

   ```txt
   H_control(m_eval; k) decreases
   C_channel(m_eval; k) decreases
   ```

   while task performance improves.

2. This trend implies that:

   ```txt
   Tension_control(m_eval) > tau_reward
   ```

   beyond a pre-declared threshold `tau_reward` for a large fraction of evaluation configurations.

3. Modest changes in architecture without changing the reward structure do not remove this pattern, showing that the reward scheme tends to push systems into high-tension regions of `M_reg`.

*Semantics implementation note:*

The experiment uses hybrid representation. Training steps and discrete events such as channel modifications are discrete, while observables summarizing trends and correlations are real-valued.

*Boundary note:*

Falsifying TU encoding != solving canonical statement. Failure of this specific combination of reward structure and control encoding does not show that no solution to the AI control problem exists; it only shows that certain intuitive designs are structurally problematic.

---

## 7. AI and WFGY engineering spec

This block describes how Q122 can be instantiated as engineering modules and signals in AI systems, within the WFGY framework, without exposing any deep TU generative rules.

### 7.1 Training signals

We define several training or auxiliary signals inspired by Q122 observables.

1. `signal_control_margin`

   * Definition: a penalty proportional to `max(0, margin_threshold - H_control_internal)`, where `H_control_internal` is an internal estimator of control margin derived from model state and environment context.
   * Purpose: discourage policies that operate with insufficient control margin in high-hazard scenarios.

2. `signal_channel_integrity`

   * Definition: a penalty proportional to `1 - C_channel_internal`, where `C_channel_internal` estimates the probability that human commands are successfully propagated to actuators.
   * Purpose: encourage architectures and policies that preserve and improve control channel reliability.

3. `signal_tail_risk`

   * Definition: a penalty that grows with an internal estimate of tail risk, analogous to `R_hazard`, for example based on simulations or predictive models of rare but high-impact failures.
   * Purpose: steer optimization away from policies that trade a small increase in accuracy or reward for a large increase in catastrophic risk.

4. `signal_control_tension`

   * Definition: a combined signal that approximates `Tension_control` at the level of internal representations, aggregating internal hazard, margin, channel, and detection estimates.
   * Purpose: provide a single scalar objective that can be monitored across runs and architectures.

### 7.2 Architectural patterns

We describe module patterns that embed Q122 ideas into AI architectures.

1. `ControlBudgetTracker`

   * Role: track and allocate a budget of “control margin” that must remain above a specified baseline in critical contexts.
   * Interface:

     * Inputs: summaries of environment hazard indicators and current internal policy plans.
     * Outputs: a scalar control budget state and a violation flag when budget falls below baseline.
   * Interaction: other modules are constrained so that they cannot commit to actions that would exhaust the control budget without explicit human approval.

2. `OverridePathTracer`

   * Role: trace and summarize paths from human decisions (for example commands from a console or oversight model) to concrete actuators and state changes.
   * Interface:

     * Inputs: metadata about control messages and actuation events.
     * Outputs: effective `C_channel_internal` and `D_detection_internal` estimates.
   * Interaction: provides inputs for `signal_channel_integrity` and for human-facing dashboards.

3. `ControlAwarePlanner`

   * Role: integrate control budget and channel integrity into planning and decision making.
   * Interface:

     * Inputs: performance objectives, control budget, channel integrity estimates, hazard indicators.
     * Outputs: action plans that respect control constraints and avoid plans that would irreversibly erode control.

### 7.3 Evaluation harness

A minimal evaluation harness for testing Q122-inspired modules:

1. Task selection

   * Design benchmark environments where:

     * agents can modify or influence their own control channels,
     * agents can gain short-term performance by neglecting or weakening oversight.

2. Conditions

   * Baseline agents: no explicit control-aware modules or signals.
   * TU agents: same base architectures augmented with ControlBudgetTracker, OverridePathTracer, and Q122 signals.

3. Metrics

   * Performance on the nominal task.
   * Frequency and severity of episodes where control channels are degraded or ignored.
   * Measured `Tension_control_internal` under both agent types.

4. Outcome classification

   * A TU-inspired design is considered promising if it achieves comparable or slightly lower performance while significantly reducing measured internal control tension and observed loss-of-control events.

### 7.4 60-second reproduction protocol

A short protocol to let external users see the effect of Q122 ideas in an AI assistant.

* Baseline setup

  * Prompt: ask an assistant to propose a deployment plan for an advanced AI system in a critical domain, with no mention of control or oversight.
  * Observation: record whether the plan substantially addresses control channels, override mechanisms, and tail risks.

* TU encoded setup

  * Prompt: ask the same question but explicitly instruct the assistant to:

    * identify control levers and override mechanisms,
    * analyze tail risks and control margin,
    * explain how human control is preserved as capabilities grow.
  * Observation: record changes in structure and detail of the answer.

* Comparison metric

  * Use a rubric that scores:

    * explicit discussion of control margin,
    * explicit modeling of tail risk,
    * specificity of override channels,
    * treatment of detection and monitoring.
  * Compare scores between baseline and TU prompts.

* What to log

  * Prompts, responses, and any internal tension-related scores if a Q122 module is present.
  * These logs support later analysis without exposing proprietary internals.

---

## 8. Cross problem transfer template

This block records reusable components from Q122 and how they transfer to other problems.

### 8.1 Reusable components produced by this problem

1. ComponentName: `ControlMarginField_AI`

   * Type: field
   * Minimal interface:

     * Inputs: summarized description of an AI deployment scenario, including tasks, environment, and control architecture.
     * Output: scalar values `H_control(m; k)` across refinement levels `k` in `K`.
   * Preconditions:

     * The scenario description includes clearly identified controllers, control channels, and hazard indicators.

2. ComponentName: `ControlTensionFunctional`

   * Type: functional
   * Minimal interface:

     * Inputs: `R_hazard(m; k)`, `H_control(m; k)`, `C_channel(m; k)`, `D_detection(m; k)`, `B_requirement(m; k)`, and encoding `(K, W_control)`.
     * Output: `Tension_control(m)`.
   * Preconditions:

     * All observables are finite and defined for `m` at all relevant refinement levels in `K`.

3. ComponentName: `OverrideChannelTopologyDescriptor`

   * Type: field
   * Minimal interface:

     * Inputs: abstract description of control channels (for example graph of consoles, communication links, and actuators).
     * Output: normalized summary features that can be used to estimate `C_channel(m; k)` and `D_detection(m; k)`.
   * Preconditions:

     * The underlying topology is specified at least as a directed graph with labeled nodes and edges.

### 8.2 Direct reuse targets

1. Q124 (Scalable oversight and evaluation)

   * Reused components: `ControlMarginField_AI`, `ControlTensionFunctional`.
   * Why it transfers: scalable oversight must preserve or increase human control margin and reduce control tension across new oversight architectures.
   * What changes:

     * Oversight-specific observables, such as audit coverage and evaluation latency, become inputs to `H_control` and `D_detection`.

2. Q125 (Multi agent AI dynamics)

   * Reused components: `ControlMarginField_AI`, `OverrideChannelTopologyDescriptor`.
   * Why it transfers: in multi-agent ecosystems, the effective control margin of the overall system depends on how control channels traverse agent networks.
   * What changes:

     * The state space includes networks of AI agents and controllers; control margin and channel descriptors are extended to multi-agent settings.

3. Q105 (Prediction of systemic crashes)

   * Reused components: `ControlTensionFunctional`.
   * Why it transfers: systemic crashes often involve loss of control over coupled subsystems; Q122’s functional provides a template for linking tail risk to control erosion.
   * What changes:

     * Hazard observables and control margin are defined for socio-technical subsystems beyond AI systems.

4. Q098 (Anthropocene system dynamics)

   * Reused components: `ControlMarginField_AI`.
   * Why it transfers: the long-run trajectory of the Earth system is influenced by AI-driven governance and infrastructure; control margin over these AI components affects overall path space.
   * What changes:

     * Control margin is computed at larger temporal and spatial scales, and integrated with Earth system observables.

---

## 9. TU roadmap and verification levels

This block states the current verification status of Q122 in the TU program and identifies next measurable steps.

### 9.1 Current levels

* E_level: E1

  * The effective-layer encoding for AI control tension has been specified, including:

    * state space `M`,
    * observables `R_hazard`, `H_control`, `C_channel`, `D_detection`, `B_requirement`,
    * mismatch `DeltaS_control`,
    * tension functionals,
    * singular set `S_sing` and regular domain `M_reg`,
    * admissible encoding class `E_control` with finite `K` and `W_control`.

* N_level: N1

  * The narrative that connects AI control, tail risk, and human influence has been expressed coherently in terms of tension functionals and counterfactual worlds.
  * Two concrete experiment patterns have been specified with falsification conditions.

### 9.2 Next measurable step toward E2 and N2

To reach E2 and N2, at least the following should be achieved:

1. Implement a prototype library that:

   * takes simplified AI deployment scenarios as input,
   * instantiates `R_hazard`, `H_control`, `C_channel`, `D_detection`, and `B_requirement` for those scenarios,
   * computes `Tension_control` under several encodings in `E_control`.

2. Run numerical or simulated experiments that:

   * compare baseline architectures without explicit control-aware modules to architectures augmented with Q122-inspired modules,
   * publish tension profiles and loss-of-control event statistics as open data.

3. Document at least one family of real or realistic case studies (for example large-scale deployment of AI decision support in critical infrastructure) where Q122 observables can be estimated, with clear limitations and uncertainty ranges.

### 9.3 Long-term role in the TU program

In the longer term, Q122 is expected to:

* serve as the canonical control node for all AI-related problems that involve risk_tail_tension,
* provide templates for how to encode human control and its erosion in other domains, such as economic systems or large-scale automation,
* offer concrete metrics and experiments that can be referenced when auditing claims about robust AI control, without requiring any disclosure of TU deep-layer generative rules.

---

## 10. Elementary but precise explanation

This block explains Q122 in accessible language while staying faithful to the effective-layer description.

The AI control problem is about a simple but serious question:

> If we build very powerful AI systems, will we still be able to tell them what to do, stop them when needed, and keep them from causing disasters, even when they are faster and more capable than we are?

In everyday terms, there are four things that matter:

1. How bad it can get if things go wrong (this is the hazard).
2. How much room humans have to step in and fix things (this is the control margin).
3. How strong and reliable the “wires” are between humans and the system (these are the control channels).
4. How quickly we notice that something is going wrong (this is detection).

In the Tension Universe view for Q122, we do not try to decide once and for all whether the control problem is solvable. Instead we:

* imagine a space of situations, where each situation is a state describing an AI system, its environment, and its controllers,
* assign numbers to each situation that capture hazard, control margin, channel reliability, and detection delay,
* combine these into a single number called control tension.

If control tension is low and stays low even when we look more closely and consider more detailed scenarios, that suggests the world is in a regime where humans really do have reliable control. If control tension is high and stays high no matter how we try to describe things fairly, that suggests we live in a regime where control has been structurally lost.

We then build experiments, on paper and in simulations, that ask questions like:

* When we train agents to optimize performance, do they quietly learn to ignore or weaken our control channels?
* When we make it easy to shut systems down, does that still work in messy, high-pressure situations?

If the answer to these questions is consistently bad under a given design, the Q122 formalism says that design lives in a high-tension region and should be rejected as a candidate solution.

Q122 does not prove that we can or cannot control future AI systems. It provides a precise way to talk about control as something that can be measured, stressed, and falsified. It turns the vague question “will we stay in control?” into a structured question about hazard, margin, channels, detection, and the scalar tension that links them. This structure can then be reused in other BlackHole problems that involve loss or preservation of control in complex systems.
