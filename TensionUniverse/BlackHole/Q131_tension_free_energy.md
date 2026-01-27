# Q131 · Tension mediated free energy in open physical systems

## 0. Header metadata

```txt
ID: Q131
Code: BH_PHYS_TENSION_FREE_ENERGY_L3_131
Domain: Physics
Family: Nonequilibrium thermodynamics and information
Rank: S
Projection_dominance: P
Field_type: hybrid_field
Tension_type: free_energy_tension
Status: Reframed_only
Semantics: hybrid
E_level: E2
N_level: N2
Last_updated: 2026-01-27
````

---

## 1. Canonical problem and status

### 1.1 Classical problem statement

In classical and modern thermodynamics, "free energy" is the portion of a system's energy that can be converted into useful work under specified environmental constraints.

For a system with internal energy `U`, entropy `S`, and volume `V`, in contact with an environment at fixed temperature `T_env` and pressure `p_env`, standard free energy quantities include:

```txt
Helmholtz free energy:  F = U - T_env * S
Gibbs free energy:      G = U + p_env * V - T_env * S
```

For a cyclic process that starts at state `x_initial` and ends at state `x_final`, the maximum extractable work `W_out_max` satisfies inequalities of the general form:

```txt
W_out_max <= F(x_initial) - F(x_final)
```

or, under appropriate constraints,

```txt
W_out_max <= G(x_initial) - G(x_final)
```

when the environment is treated as an infinite reservoir and all other state variables are returned to their initial values.

The canonical problem behind Q131 is:

> Given an open system immersed in one or more reservoirs, and given nonequilibrium structure and information in those reservoirs, what are the sharp limits on extractable work and efficiency, and how can these limits be expressed as tension-style invariants and observables?

Q131 explicitly excludes any violation of:

* conservation of energy for closed descriptions, and
* nonnegative total entropy production for physically realistic processes.

### 1.2 Status and difficulty

The core laws of thermodynamics are well established and experimentally confirmed. There exist:

* mature formulations of equilibrium free energy,
* extended frameworks for nonequilibrium thermodynamics,
* information-theoretic treatments linking work and information processing.

However, several aspects remain nontrivial:

1. Unified treatment of structural resources

   * Real systems exploit not only temperature and pressure gradients, but also:

     * chemical gradients,
     * concentration differences,
     * spatial and temporal correlations,
     * and information encoded in control structures.
   * A fully unified "resource theory of free energy" for arbitrary open systems is still under active development.

2. Operational bounds under complex constraints

   * For realistic engineering systems (including computation),

     * computing tight bounds on extractable work,
     * under constraints on control, measurement, and feedback,
       is technically difficult and often problem specific.

3. Integration with computation and learning

   * For AI and computing systems, relating:

     * algorithmic structure,
     * representation complexity,
     * and physical energy cost,
       in a way that gives usable design rules, remains partially open.

The Tension Universe formulation in Q131 does not claim to solve these open directions.
Instead, it reframes them into a common language of:

* tension fields,
* free_energy_tension functionals,
* and explicit energy and entropy invariants.

### 1.3 Role in the BlackHole project

Within the BlackHole S-problem collection, Q131 plays three roles:

1. **Physical sanity check for TU**

   It demonstrates that TU-style tension encodings can reproduce standard free energy limits without breaking conservation or the second law.

2. **Bridge between physics and AI energy limits**

   It provides the physical side of the link to AI and computation problems such as:

   * Q059 (information thermodynamics in computation),
   * Q129 and Q130 (energy limits for AI).

3. **Classifier for "free energy" claims**

   It defines effective-layer criteria that separate:

   * coherent open-system energy-harvesting architectures, from
   * perpetual motion style designs that rely on hidden reservoirs or missing entropy accounting.

### References

1. H. B. Callen, "Thermodynamics and an Introduction to Thermostatistics", 2nd edition, Wiley, 1985.
2. D. Kondepudi and I. Prigogine, "Modern Thermodynamics: From Heat Engines to Dissipative Structures", Wiley, 1998.
3. R. Landauer, "Irreversibility and Heat Generation in the Computing Process", IBM Journal of Research and Development, 5(3), 1961.
4. J. M. R. Parrondo, J. M. Horowitz, and T. Sagawa, "Thermodynamics of information", Nature Physics, 11, 131–139, 2015.

---

## 2. Position in the BlackHole graph

This block records how Q131 sits in the BlackHole graph among Q001–Q130.

### 2.1 Upstream problems

Upstream nodes provide foundations, tools, or conceptual scaffolding that Q131 reuses.

* Q032 (BH_PHYS_QTHERMO_L3_032)
  Reason: Supplies the general thermodynamic and quantum thermodynamic framework for energy, entropy, and work observables used in Q131.

* Q035 (BH_PHYS_QMETROLOGY_LIMIT_L3_035)
  Reason: Provides limit concepts for precision measurement of tiny energy and heat flows, supporting the practical meaning of Q131's invariants.

* Q059 (BH_CS_INFO_THERMODYN_L3_059)
  Reason: Encodes information-theoretic energy costs that Q131 integrates into the free_energy_tension functional.

* Q129 (BH_AI_ENERGY_LIMIT_L3_129)
  Reason: Describes high-level energy bounds for AI systems that Q131 grounds in physical free energy and open-system thermodynamics.

### 2.2 Downstream problems

Downstream nodes reuse Q131 components or treat Q131 as a prerequisite.

* Q130 (BH_AI_OOD_ENERGY_LIMIT_L3_130)
  Reason: Reuses Q131's FreeEnergyTensionFunctional and EnergyEntropyLedger components to define energy-aware AI generalization limits.

* Future node: "Self-maintaining open systems under tension"
  Reason: Will reuse Q131's open-system state space and free_energy_tension invariants to study persistent far-from-equilibrium structures.

### 2.3 Parallel problems

Parallel nodes share similar tension types but have no direct component dependence.

* Q036 (BH_PHYS_HIGH_TC_MECH_L3_036)
  Reason: Both Q036 and Q131 analyze emergent phases and resource-like order parameters as structured tension in many-body systems.

* Q040 (BH_PHYS_QBLACKHOLE_INFO_L3_040)
  Reason: Both study how energy, entropy, and information interact under strong constraints, one in condensed matter and the other in gravitational systems.

### 2.4 Cross domain edges

Cross-domain edges connect Q131 to problems in other domains that can reuse its components.

* Q059 (BH_CS_INFO_THERMODYN_L3_059)
  Reason: Reuses Q131's EnergyEntropyLedger component to express energy and entropy accounting in computational processes.

* Q130 (BH_AI_OOD_ENERGY_LIMIT_L3_130)
  Reason: Uses Q131's free_energy_tension concept to define energy budget and dissipative cost constraints for AI models under distribution shift.

* Q123 (BH_AI_INTERP_L3_123)
  Reason: Can reuse Q131's idea of mapping internal representations to resource-like tension fields, now interpreted as energy and complexity rather than spectra.

---

## 3. Tension Universe encoding (effective layer)

All content in this block stays strictly at the effective layer.
We only define:

* state spaces,
* observables and fields,
* invariants and tension scores,
* singular sets and domain restrictions.

No hidden generative rules or mappings from raw experimental data to internal TU fields are described.

### 3.1 State space of open tension-energy configurations

We define a state space `M` whose elements are effective descriptions of open systems interacting with environments.

Each state `m` in `M` encodes, at some finite resolution:

1. A finite set of reservoirs:

   ```txt
   R = { R_1, R_2, ..., R_n }
   ```

   For each reservoir `R_k`, the state includes effective variables such as:

   ```txt
   U_k(m)   internal energy
   S_k(m)   entropy
   V_k(m)   volume or analogous extensive variable (optional)
   other_k  other relevant extensive variables (optional)
   ```

2. A work storage subsystem `W_store`:

   With an effective stored work quantity:

   ```txt
   W_store(m) >= 0
   ```

3. A description of coupling channels:

   A finite set `C_channels` describing how reservoirs and `W_store` can exchange energy and entropy, including:

   ```txt
   allowed_flows(m)
   control_patterns(m)
   ```

4. A tension field over the configuration:

   An effective field `Tau_FE(m)` representing gradients and structure that can drive energy and entropy flows, for example:

   * temperature gradients,
   * chemical potential gradients,
   * concentration gradients,
   * structured correlations that act as resources.

We do not specify how `m` is constructed from underlying microstates or experimental data.
We assume only that each `m` provides well defined values for the observables introduced below.

We also assume a refinement ladder:

```txt
M_1 subset M_2 subset ... subset M_k subset ...
```

where `M_k` restricts:

* the number of reservoirs,
* the number of channels,
* and the resolution of `Tau_FE(m)`.

### 3.2 Energy and entropy observables

On `M` we define the following effective observables.

1. Total energy of the closed description:

```txt
E_total(m) = sum over k of U_k(m) + E_other(m)
```

where `E_other(m)` collects any additional stored energy, including `W_store(m)`.

2. Total entropy of the closed description:

```txt
S_total(m) = sum over k of S_k(m) + S_other(m)
```

where `S_other(m)` includes entropy assigned to any coarse-grained environment pieces explicitly in the description.

3. Work output observable:

```txt
W_out(m) = W_store(m) - W_store_initial_reference
```

for a chosen reference value `W_store_initial_reference` corresponding to the start of a process.

4. Heat exchanged with an environment slice `E_env_j`:

```txt
Q_env_j(m)
```

for each environment slice that is represented explicitly.

We require that:

```txt
E_total(m) is finite
S_total(m) is finite
```

for all `m` in the regular domain described below.

### 3.3 Free energy and free_energy_tension observables

We define an effective free energy observable `F_free(m)` as a function of:

* the internal energies `U_k(m)`,
* the entropies `S_k(m)`,
* and relevant environmental parameters included in `m`, such as effective temperature or pressure fields.

For example, in a simple single-reservoir setting:

```txt
F_free(m) = U_1(m) - T_env(m) * S_1(m)
```

More generally, `F_free(m)` is any functional that:

* reduces to standard free energy in the appropriate limit, and
* is monotonically nonincreasing in idealized reversible work extraction processes.

We then define a free energy tension observable:

```txt
Tension_FE(m) >= 0
```

with the intended meaning:

* `Tension_FE(m)` measures how much structured resource remains that can, in principle, be converted into work, given the couplings encoded in `C_channels`.

We require that:

1. If no gradients, structure, or disequilibria remain in `m`, then:

   ```txt
   Tension_FE(m) = 0
   ```

2. For a process represented by a sequence of states:

   ```txt
   m_0, m_1, ..., m_T
   ```

   with work extracted into `W_store`, we have an inequality of the form:

   ```txt
   W_out_total <= F_free(m_0) - F_free(m_T)
   ```

   and also:

   ```txt
   W_out_total <= integral_over_process Tension_FE(m_t) dt
   ```

   for a suitable effective time parameter, within the approximation used by the encoding.

Here `W_out_total` is computed from the change in `W_store` between `m_0` and `m_T`.

### 3.4 Information structure observables

We introduce two information-related observables.

1. Configuration information:

```txt
I_config(m) >= 0
```

which measures, at the effective layer, how much structured information is present in:

* control patterns,
* correlations between reservoirs,
* and any explicit data used to drive feedback.

2. Information processing cost lower bound:

```txt
cost_info(m) >= 0
```

which is an effective lower bound on the energy cost needed to:

* acquire,
* store,
* or erase,

the information represented in `I_config(m)`.

We impose the qualitative constraint:

```txt
cost_info(m) <= k_info * I_config(m)
```

for some encoding-dependent constant `k_info`, meaning that information is not treated as a free resource.
Any architecture that implicitly assumes unbounded work extraction from information with zero associated cost would violate this observable constraint.

### 3.5 Effective tension tensor

To align with TU core conventions, we define an effective tension tensor:

```txt
T_ij(m) = S_i(m) * C_j(m) * Tension_FE(m) * lambda(m) * kappa
```

where:

* `S_i(m)` are source-like factors encoding how strongly the `i`-th part of the configuration can drive transformations,
* `C_j(m)` are receptivity-like factors encoding how sensitive the `j`-th degree of freedom is to free energy tension,
* `lambda(m)` encodes the local reasoning or control regime (for example, convergent or divergent control),
* `kappa` is a constant setting the scale for this family of problems.

We do not specify the index sets for `i` and `j` or the detailed dependence of `S_i`, `C_j`, and `lambda` on `m`.
We require only that:

```txt
Tension_FE(m) = 0  implies  T_ij(m) = 0 for all i, j
```

within the domain of interest.

### 3.6 Invariants and constraints

We define three effective invariants.

1. Energy balance invariant:

For a process represented by a sequence of states in `M`:

```txt
m_0, m_1, ..., m_T
```

we define:

```txt
I_E_balance = E_total(m_T) - E_total(m_0) - E_external_input
```

where `E_external_input` is the explicitly modeled energy injected from outside the modeled closed description.
A valid encoding should satisfy:

```txt
I_E_balance = 0
```

within modeling tolerance.

2. Entropy production invariant:

We define total entropy production over the process:

```txt
Delta_S_total = S_total(m_T) - S_total(m_0)
```

and require:

```txt
Delta_S_total >= 0
```

for physically realistic processes.

3. Free energy bound invariant:

We define:

```txt
I_FE_bound = W_out_total - ( F_free(m_0) - F_free(m_T) )
```

A valid encoding must satisfy:

```txt
I_FE_bound <= 0
```

This ensures that work output never exceeds the decrease in free energy.

### 3.7 Singular set and domain restriction

We define the singular set:

```txt
S_sing = {
  m in M :
  E_total(m) is undefined or not finite
  or S_total(m) is undefined or not finite
  or F_free(m) is undefined
}
```

The regular domain is:

```txt
M_reg = M \ S_sing
```

All Q131 analysis is restricted to `M_reg`.
Any proposed "free energy" architecture that cannot be mapped to a well defined `m` in `M_reg` is treated as out of domain, not as evidence for new physics.

---

## 4. Tension principle for this problem

This block states how Q131 is characterized as a tension problem in TU.

### 4.1 Core principle

The core principle is:

> Free energy is structured tension in an open system that can be converted into work, up to hard limits set by energy conservation and entropy production, and these limits can be expressed as inequalities involving free_energy_tension and TU invariants.

Operationally, this means:

1. The free energy tension observable `Tension_FE(m)` measures how far the configuration `m` is from a "relaxed" state with no exploitable gradients or structure.

2. As work is extracted and entropy is produced, `Tension_FE(m)` should decrease, unless new structured resources are imported from external reservoirs.

3. Any claim of "free energy" gain must be representable as:

   * either import of structured resources (increasing `Tension_FE(m)` from outside the modeled system),
   * or reallocation of tension between subsystems, subject to the global energy and entropy constraints.

### 4.2 Low-tension and high-tension regimes

We introduce two qualitative regimes for world-representing states in `M_reg`.

1. Low-tension regime:

   * `Tension_FE(m)` is small.
   * No large gradients or nonequilibrium resources remain.
   * Any additional work extraction would require importing new low-entropy resources from outside the modeled system.

2. High-tension regime:

   * `Tension_FE(m)` is large enough to support significant additional work extraction.
   * There exist identifiable gradients, chemical potentials, or informational structures that are not yet fully exploited.

Q131 does not assert that the physical world will always move toward low-tension states, only that:

* all physically valid free energy extraction processes must respect the inequalities defined in Block 3,
* and any apparent violation indicates an error in modeling or accounting, not a new form of free energy.

### 4.3 Diagnosing invalid "free energy" designs

From the TU perspective, a "free energy" design is classified as invalid at the effective layer if:

1. It cannot be mapped to a state in `M_reg` with well defined `E_total`, `S_total`, and `F_free`.

2. Its claimed performance implies:

   ```txt
   I_E_balance != 0
   ```

   for any consistent choice of `E_external_input`.

3. Its claimed performance would produce:

   ```txt
   Delta_S_total < 0
   ```

   in a closed description.

4. It requires:

   ```txt
   I_FE_bound > 0
   ```

   that is, net work greater than free energy decrease, with no external structured resource.

In such cases, Q131 classifies the proposal as a **perpetual motion illusion** at the effective layer.

---

## 5. Counterfactual tension worlds

We now outline two counterfactual worlds, both described strictly through observables and invariants.

### 5.1 World TFE (tension-consistent free energy world)

In World TFE:

1. Every device and architecture that appears to extract "free energy" can be mapped to `M_reg` with well defined `E_total`, `S_total`, and `F_free`.

2. For any process:

   ```txt
   m_0 -> m_T
   ```

   representing the combined system plus explicit environment slices, the invariants satisfy:

   ```txt
   I_E_balance = 0
   Delta_S_total >= 0
   I_FE_bound <= 0
   ```

   within modeling and measurement tolerances.

3. Structured resources such as temperature gradients, chemical potentials, and informational constraints appear in `Tau_FE(m)` and `Tension_FE(m)` as nonzero contributions.

4. Over time, if no new structured resources are imported, typical world trajectories show:

   ```txt
   Tension_FE(m_t) decreasing
   ```

   and

   ```txt
   F_free(m_t) decreasing
   ```

   as gradients relax and work is extracted or dissipated.

### 5.2 World PPM (perpetual motion illusion world)

In World PPM:

1. Many device proposals are described only partially. They omit some reservoirs or environment interactions, leading to ill-defined `E_total` or `S_total`.

2. Effective encodings that attempt to treat such devices as closed lead to:

   ```txt
   E_total(m_T) - E_total(m_0) > 0
   ```

   with `E_external_input = 0`, which violates energy conservation.

3. Entropy accounting, if performed over a closed description, would imply:

   ```txt
   Delta_S_total < 0
   ```

   in contradiction with the second law.

4. The claimed work output satisfies:

   ```txt
   W_out_claimed > F_free(m_0) - F_free(m_T)
   ```

   even under generous assumptions about free energy, indicating that `I_FE_bound > 0`.

In World PPM, the TU framework does not validate the device.
Instead, it classifies the proposal as:

* incomplete (if it cannot be embedded into `M_reg`),
* or inconsistent (if it violates the invariants).

### 5.3 Interpretive note

These counterfactual worlds do not introduce new physics.
They simply clarify two behaviors:

* In TFE, tension encodings reveal the structure of legitimate free energy extraction processes.
* In PPM, tension encodings expose the missing pieces in perpetual motion arguments.

Q131 only operates at this effective-layer diagnostic level.

---

## 6. Falsifiability and discriminating experiments

This block specifies experiments and protocols that can:

* test whether a specific Q131 encoding is coherent and useful,
* discriminate between good and bad parameterizations of `Tension_FE`,
* and diagnose whether a proposed "free energy" device is compatible with the invariants.

These experiments do not claim to discover new physics.
They are designed to falsify or refine Q131-style encodings.

### Experiment 1: Two-reservoir heat engine under tension encoding

*Goal:*
Test whether the chosen `Tension_FE` and invariants reproduce standard free energy bounds for a textbook two-reservoir heat engine.

*Setup:*

* System: a working medium coupled to:

  * a hot reservoir at temperature `T_hot`,
  * a cold reservoir at temperature `T_cold`.
* Environment: modeled as two large reservoirs `R_hot` and `R_cold` plus a work storage subsystem `W_store`.
* TU encoding: choose a simple form of `F_free(m)` and `Tension_FE(m)` that reduces to Helmholtz or Gibbs free energy in the appropriate limit.

*Protocol:*

1. Construct a family of states `m_cycle(k)` representing discrete stages of a quasi-static or finite-time engine cycle, starting and ending at the same internal state of the working medium.

2. For each `m_cycle(k)` compute:

   * `E_total(m_cycle(k))`,
   * `S_total(m_cycle(k))`,
   * `F_free(m_cycle(k))`,
   * `Tension_FE(m_cycle(k))`,
   * and the incremental work and heat flows.

3. Integrate these quantities over one cycle to obtain:

   * `W_out_total`,
   * `Delta_S_total`,
   * and any changes in `F_free`.

4. Evaluate the invariants:

   * `I_E_balance`,
   * `Delta_S_total`,
   * and `I_FE_bound`.

*Metrics:*

* Magnitude of `I_E_balance` relative to numerical tolerances.
* Sign and magnitude of `Delta_S_total`.
* Sign and magnitude of `I_FE_bound`.

*Falsification conditions:*

* If, for physically reasonable parameter choices and sufficiently accurate numerical methods, the encoding produces:

  * `I_E_balance` significantly different from zero, or
  * `Delta_S_total < 0` for a closed description, or
  * `I_FE_bound > 0` in a regime where standard thermodynamics predicts `W_out_total` is bounded by free energy decrease,

  then the current definition of `F_free(m)` or `Tension_FE(m)` is considered falsified for Q131.

* If small, physically plausible changes in modeling assumptions produce arbitrarily large swings in `Tension_FE(m)` without changes in `E_total` or `S_total`, the encoding is considered unstable and rejected.

*Semantics implementation note:*
This experiment uses a mixed representation where reservoir temperatures and entropies are treated as continuous variables, while cycle stages and coupling patterns are treated as discrete configuration labels, in line with the hybrid metadata in Block 0.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. This experiment can falsify a particular free_energy_tension encoding, but it does not challenge the underlying laws of thermodynamics.

---

### Experiment 2: Diagnostic test on proposed "free energy" architectures

*Goal:*
Provide a systematic procedure for testing whether a proposed "free energy" device is compatible with Q131 invariants, and classify common failure modes.

*Setup:*

* Input: a textual or schematic description of a device that claims to:

  * extract net work from a single reservoir,
  * or operate as a perpetual motion machine of the first or second kind,
  * or produce net work with no apparent fuel.

* TU encoding: map the description into a candidate state sequence in `M`, attempting to:

  * identify reservoirs,
  * identify work storage,
  * identify coupling channels,
  * and define `E_total`, `S_total`, and `F_free`.

*Protocol:*

1. Attempt to construct a closed description by including all identifiable reservoirs and environment slices that interact with the device.

2. For each step in the claimed operation, define a state `m_step(k)` and compute:

   * `E_total(m_step(k))` if possible,
   * `S_total(m_step(k))` if possible,
   * `F_free(m_step(k))` if possible,
   * `W_out_step(k)` claimed or implied by the description.

3. Aggregate over a full cycle to obtain:

   * `E_total(m_T) - E_total(m_0)`,
   * `Delta_S_total`,
   * `W_out_total`,
   * `F_free(m_0) - F_free(m_T)`.

4. Evaluate invariants:

   * `I_E_balance`,
   * `Delta_S_total`,
   * `I_FE_bound`.

*Metrics:*

* Whether a mapping into `M_reg` is possible.
* Sign of `Delta_S_total`.
* Sign of `I_FE_bound`.
* Existence of unmodeled reservoirs or implicit energy sources.

*Falsification conditions:*

* If the device cannot be mapped into `M_reg` because `E_total` or `S_total` is not definable, the proposal is classified as out of domain and rejected as an effective-layer description.

* If the mapping yields:

  ```txt
  I_E_balance != 0
  ```

  for `E_external_input = 0`, the encoding plus device description is considered inconsistent.

* If the mapping yields:

  ```txt
  Delta_S_total < 0
  ```

  for a closed description, the device is classified as violating the second law.

* If the mapping yields:

  ```txt
  I_FE_bound > 0
  ```

  meaning claimed work exceeds free energy decrease, and no external structured resource is modeled, the device is classified as a perpetual motion illusion in Q131 terms.

*Semantics implementation note:*
This experiment uses a mixed representation where many details of the device are coarse-grained into effective energies and entropies, while the presence or absence of reservoirs and flows is tracked as discrete structure.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. This experiment classifies device proposals within Q131's effective-layer framework; it does not discover or refute new fundamental physics.

---

## 7. AI and WFGY engineering spec

This block describes how Q131 can be used as an engineering module for AI systems within WFGY.

### 7.1 Training signals

We define several training signals that encode Q131-style constraints.

1. `signal_energy_ledger_consistency`

   * Definition: A penalty proportional to the absolute value of `I_E_balance` inferred from a model's description of physical or computational processes.
   * Purpose: Encourage the model to produce descriptions where energy accounting is explicit and consistent.

2. `signal_entropy_production_sign`

   * Definition: A penalty applied whenever a described closed process implies `Delta_S_total < 0` within the effective encoding.
   * Purpose: Train the model to avoid narratives that violate the second law in closed systems.

3. `signal_free_energy_bound_respect`

   * Definition: A penalty proportional to the positive part of `I_FE_bound`, when the model suggests work extraction exceeding free energy decrease.
   * Purpose: Align model reasoning with free energy bounds.

4. `signal_tension_resource_awareness`

   * Definition: A signal that rewards explicit identification of gradients, reservoirs, and information structures as resources contributing to `Tension_FE(m)`.
   * Purpose: Make the model more explicit about what "fuels" a process, instead of treating work as coming from nowhere.

### 7.2 Architectural patterns

We outline three reusable architectural modules.

1. `FreeEnergyTensionHead`

   * Role: Given a latent representation of a physical or computational scenario, output an estimate of `Tension_FE(m)` and related invariants.
   * Interface:

     * Input: scenario embedding plus optional structured metadata,
     * Output: scalar estimate of tension, plus estimated `I_E_balance`, `Delta_S_total`, and `I_FE_bound`.

2. `EnergyEntropyLedger`

   * Role: Maintain a running ledger of energy and entropy contributions across the steps of a reasoning chain or simulated process.
   * Interface:

     * Input: sequence of actions or transformations,
     * Output: updated estimates of `E_total`, `S_total`, `W_out_total`, and diagnostic flags for invariant violations.

3. `FE_ConstraintLayer`

   * Role: Post-process candidate outputs (for example, design proposals or explanations) to:

     * flag violations of Q131 invariants,
     * propose minimal repairs that restore consistency.
   * Interface:

     * Input: raw model output,
     * Output: annotated output plus suggested corrections.

### 7.3 Evaluation harness

We propose an evaluation harness to test AI systems equipped with Q131 modules.

1. Task design

   * Collect a benchmark of:

     * classical thermodynamics problems,
     * free energy calculations,
     * and "too good to be true" device proposals.

2. Baseline condition

   * The model answers without access to Q131-specific modules or signals.
   * Measure:

     * frequency of energy accounting errors,
     * frequency of second law violations,
     * susceptibility to perpetual motion style arguments.

3. TU condition

   * The model uses `FreeEnergyTensionHead` and `EnergyEntropyLedger` internally.
   * The training signals from 7.1 are active during fine-tuning.

4. Metrics

   * Reduction in energy and entropy accounting errors.
   * Increase in correct classification of unrealistic device proposals.
   * Consistency of explanations about where energy and free energy come from and where they go.

### 7.4 60-second reproduction protocol

A minimal public-facing protocol to demonstrate the impact of Q131 encoding.

* Baseline setup

  * Prompt: "Explain why a device that claims to produce unlimited electrical power from a single room-temperature reservoir is or is not physically possible."
  * Observe:

    * whether the model gives vague or hand-wavy answers,
    * whether energy and entropy accounting are explicit.

* TU encoded setup

  * Prompt: same question, with an added instruction:

    * "Use energy balance, total entropy production, and free energy bounds, as defined in a tension-based encoding, to analyze this device."
  * Observe:

    * whether the model identifies missing reservoirs,
    * whether it computes or at least qualitatively tracks `I_E_balance`, `Delta_S_total`, and `I_FE_bound`.

* Comparison metric

  * Human evaluators rate:

    * clarity of energy and entropy accounting,
    * correctness of the physical conclusion,
    * explicitness of identifying failure modes.

* What to log

  * Prompts,
  * full responses,
  * and any auxiliary estimates of invariants produced by Q131 modules.

These logs allow external auditors to verify that the model is not merely repeating slogans, but is applying consistent accounting.

---

## 8. Cross problem transfer template

### 8.1 Reusable components produced by this problem

1. ComponentName: `FreeEnergyTensionFunctional`

   * Type: functional
   * Minimal interface:

     * Inputs:

       * effective reservoir states,
       * coupling configuration,
       * and control structure summaries,
     * Output:

       * `Tension_FE_value` (nonnegative scalar).
   * Preconditions:

     * Inputs must include enough information to compute `F_free` and the invariants in Block 3.

2. ComponentName: `EnergyEntropyLedger`

   * Type: observable
   * Minimal interface:

     * Inputs:

       * sequence of process steps with effective energy and entropy changes,
     * Output:

       * cumulative estimates of `E_total`, `S_total`, `W_out_total`,
       * and the invariants `I_E_balance`, `Delta_S_total`, `I_FE_bound`.
   * Preconditions:

     * Each step must specify how energy and entropy are exchanged between subsystems.

3. ComponentName: `OpenSystemConfigDescriptor`

   * Type: field
   * Minimal interface:

     * Inputs:

       * list of reservoirs,
       * work storage subsystem,
       * coupling pattern metadata,
     * Output:

       * a structured representation suitable as input to `FreeEnergyTensionFunctional` and `EnergyEntropyLedger`.
   * Preconditions:

     * Reservoirs must be represented with finite effective variables, and the couplings must be specified at the level of channels and flows.

### 8.2 Direct reuse targets

1. Q059 (BH_CS_INFO_THERMODYN_L3_059)

   * Reused components:

     * `EnergyEntropyLedger`,
     * `OpenSystemConfigDescriptor`.
   * Why it transfers:

     * Q059 studies energy and entropy costs in computation, which can be encoded as open systems with reservoirs and control operations.
   * What changes:

     * Reservoirs become information and memory subsystems, and the main cost is associated with measurement and erasure operations.

2. Q130 (BH_AI_OOD_ENERGY_LIMIT_L3_130)

   * Reused components:

     * `FreeEnergyTensionFunctional`.
   * Why it transfers:

     * Q130 needs an effective notion of resource tension for AI models under distribution shift, including compute and energy budgets.
   * What changes:

     * Reservoirs include hardware, data pipelines, and training budgets; `Tension_FE` is interpreted as remaining resource capacity rather than purely physical free energy.

3. Q036 (BH_PHYS_HIGH_TC_MECH_L3_036)

   * Reused components:

     * `OpenSystemConfigDescriptor`.
   * Why it transfers:

     * High temperature superconductivity involves complex open systems exchanging energy and entropy with environments.
   * What changes:

     * The emphasis shifts to how order parameters and emergent phases relate to effective free energy landscapes.

4. Q040 (BH_PHYS_QBLACKHOLE_INFO_L3_040)

   * Reused components:

     * `EnergyEntropyLedger`.
   * Why it transfers:

     * Black hole information studies require careful tracking of energy, entropy, and information flow between fields and horizons.
   * What changes:

     * Reservoirs become gravitational and quantum fields; entropy accounting must respect horizon area laws.

---

## 9. TU roadmap and verification levels

### 9.1 Current levels

* E_level: E2

  * A coherent effective encoding of free energy in terms of `Tension_FE`, `F_free`, and TU invariants has been specified.
  * At least two explicit experiment templates exist to test and potentially falsify Q131 encodings.

* N_level: N2

  * The narrative linking:

    * energy and entropy accounting,
    * free energy,
    * and free energy tension,
      is explicit and compatible with standard thermodynamics.
  * Counterfactual worlds TFE and PPM have been described in a way that can be instantiated in concrete models.

### 9.2 Next measurable step toward E3

To move from E2 to E3, at least one of the following should be implemented:

1. A reference implementation of `FreeEnergyTensionFunctional` and `EnergyEntropyLedger` applied to:

   * a two-reservoir heat engine,
   * and one nontrivial nonequilibrium system,

   with results published as open data, including:

   * `Tension_FE(m_t)`,
   * `I_E_balance`,
   * `Delta_S_total`,
   * and `I_FE_bound`.

2. A diagnostic toolkit that takes as input:

   * textual descriptions of "free energy" devices,

   and outputs:

   * a classification into TFE-compatible or PPM-like,
   * plus a minimal set of missing or inconsistent energy and entropy terms.

Both steps remain at the effective layer and do not require revealing any deeper TU generative rules.

### 9.3 Long-term role in the TU program

In the long-term TU roadmap, Q131 is intended to:

* act as a "physics firewall" for any TU-based claims involving energy and free energy,
* provide reusable accounting components for AI, computation, and cosmology nodes,
* and serve as a concrete example where TU unification does not break established physical laws.

If TU is to be taken seriously as a candidate for a cross-domain structural framework, Q131 must remain conservative and compatible with mainstream thermodynamics.

---

## 10. Elementary but precise explanation

This block gives a nontechnical explanation aligned with the effective-layer description.

In ordinary physics, "free energy" is not magic energy from nowhere.
It is a way of counting how much useful work you can get from a system that:

* has some stored energy,
* is in contact with an environment,
* and has gradients or imbalances you have not yet used.

For example:

* a hot object next to a cold object,
* a tank of compressed gas next to empty space,
* or a charged battery,

all have free energy. Once you let them relax completely, the free energy goes down and the ability to do work disappears.

In the Tension Universe view, we say:

* these gradients and structures are a kind of **tension**, and
* free energy is a way to measure how strong that tension is.

Q131 builds a language where:

* each situation is encoded as a state,
* the total energy and total entropy of the closed description can be computed,
* and a special number called `Tension_FE` tells you how much resource is left.

Then we impose a few strict rules:

1. Energy does not appear from nowhere.
   Across a full process, the total energy of the closed description stays the same.

2. Entropy, in a closed description, does not go down overall.
   You can locally make things more ordered, but only by dumping disorder somewhere else.

3. The work you can get out is at most as big as the drop in free energy, and at most as big as what the tension measure says is still available.

With these rules, Q131 can do two things:

* describe good designs that really do harvest free energy from gradients and structure, and
* show where "free energy" proposals cheat, usually by:

  * hiding a reservoir,
  * forgetting an entropy cost,
  * or treating information as if it were free work.

The important point is that Q131 is not claiming a new way to break physics.
Instead, it says:

* if you want to talk about free energy inside Tension Universe,
* you must pass standard physics checks,
* and you must write down your energy and entropy ledger clearly.

This way, Q131 becomes both:

* a unifying way to think about resources across physics, computation, and AI, and
* a filter that prevents the framework from being used to justify impossible "perpetual motion" stories.
