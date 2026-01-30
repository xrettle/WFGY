<!-- QUESTION_ID: TU-Q025 -->
# Q025 · Baryon asymmetry of the universe

## 0. Header metadata

```txt
ID: Q025
Code: BH_PHYS_BARYON_ASYM_L3_025
Domain: Physics
Family: High energy physics and cosmology
Rank: S
Projection_dominance: P
Field_type: dynamical_field
Tension_type: thermodynamic_tension
Status: Open problem
Semantics: hybrid
E_level: E1
N_level: N1
Encoding_class: A_enc_BA
EncodingKey_Q025: ENC_BA_v1_2026_01_29
LibraryKey_ref_Q025: LIB_BA_REF_v1
WeightKey_Q025: WSET_BA_v1
Last_updated: 2026-01-30
```

---

## 0. Effective layer disclaimer

All statements in this entry are made strictly at the **effective layer** of the Tension Universe (TU) framework.

* This page encodes the baryon asymmetry of the universe as a **thermodynamic tension problem** using:

  * state spaces
  * observable summaries
  * mismatch and tension functionals
  * falsifiable, versioned encodings.
* It does **not**:

  * prove or disprove any specific baryogenesis mechanism
  * select a unique microscopic model of high energy physics or cosmology
  * introduce new theorems beyond what is already established in the cited literature
  * describe or expose any TU internal axiom system, generative rule set, or constructive derivation.

In particular:

* We do **not** specify how raw quantum fields, initial conditions, or detailed Lagrangians are mapped into TU internal fields.
* We only assume the existence of TU compatible models that reproduce the observable summaries used here.
* All tension scores are **bookkeeping tools** at the effective layer, not claims about the fundamental nature of the universe.

Any conclusion about “low tension” or “high tension” refers to a **fixed, admissible encoding** in the class `A_enc_BA` and should not be read as a proof that the baryon asymmetry problem is solved.

---

## 1. Canonical problem and status

### 1.1 Canonical statement

Observations of the early universe show a small but robust excess of baryons over antibaryons. This excess is usually summarized by an effective baryon to photon ratio

```txt
eta_B = n_B / n_gamma
```

where

* `n_B` is the net baryon number density (baryons minus antibaryons)
* `n_gamma` is the photon number density.

Data from big bang nucleosynthesis and the cosmic microwave background indicate that

* `eta_B` is nonzero
* `eta_B` has a value of order `10^(-10)` in suitable units
* this value is tightly constrained by independent observations.

In standard high energy physics, most fundamental interactions treat particles and antiparticles approximately symmetrically. If the universe started in a nearly symmetric state, any persistent net baryon number today must be generated dynamically through processes that:

* violate baryon number
* violate charge conjugation (C) and charge parity (CP)
* depart from thermal equilibrium at some stage of cosmic evolution.

These three requirements are known as the **Sakharov conditions**.

The canonical problem is:

> Explain, within a consistent high energy and cosmological framework, why the universe ends up with the observed value of `eta_B` rather than zero or some incompatible value, using dynamics that satisfy the Sakharov conditions and all current experimental bounds.

No unique mechanism is confirmed by data. Many candidate scenarios exist, including electroweak baryogenesis, leptogenesis, and grand unified baryogenesis.

The goal of this page is **not** to select one mechanism as true. The goal is to encode the problem as a TU style **thermodynamic tension** node, with a clear effective state space, mismatch functionals, and falsifiable encodings.

### 1.2 Status and difficulty

Empirically:

* `eta_B` is measured with high precision from big bang nucleosynthesis and cosmic microwave background data.
* The value is consistent across independent analyses and cosmological probes.

Theoretically:

* The Standard Model of particle physics contains some CP violation and baryon number violation at the nonperturbative level, but most analyses suggest this is insufficient to produce the observed `eta_B` under standard cosmological conditions.
* Many extensions of the Standard Model introduce new sources of CP violation, new heavy particles, or new phase transitions that can generate baryon asymmetry.
* None of these mechanisms has direct experimental confirmation so far.

The problem is considered very difficult because it couples:

* detailed particle physics
* early universe thermodynamics and phase transitions
* cosmological parameter inference.

It is not a single equation to solve. It is a global compatibility and existence question for realistic microphysical and cosmological models.

### 1.3 Role in the BlackHole project

Within the BlackHole S problem collection, Q025 plays three roles:

1. It is the flagship example of a **thermodynamic_tension** problem in cosmology, where small asymmetries must be generated and preserved through nontrivial dynamics.
2. It connects high energy particle physics nodes (Q021, Q022, Q023, Q024) with late time cosmological inference nodes (Q041, Q044, Q048) by enforcing consistency of baryon content.
3. It provides a template for encoding:

   * conserved and approximately conserved charges
   * asymmetric initial conditions
   * tension between microphysical parameters and large scale observations
     in a way that is falsifiable at the effective layer.

### References

1. P. A. Zyla et al., “Review of Particle Physics”, Progress of Theoretical and Experimental Physics 2020. Sections on big bang nucleosynthesis and cosmological parameters.
2. E. W. Kolb and M. S. Turner, “The Early Universe”, Addison Wesley, 1990. Chapters on baryogenesis and early universe phase transitions.
3. A. D. Sakharov, “Violation of CP invariance, C asymmetry, and baryon asymmetry of the universe”, JETP Letters 5, 24 (1967).
4. A. Riotto and M. Trodden, “Recent progress in baryogenesis”, Annual Review of Nuclear and Particle Science 49, 35 (1999).

---

## 2. Position in the BlackHole graph

This block records how Q025 sits inside the BlackHole graph as nodes and edges among Q001–Q125. Each edge has a one line reason that points to a concrete component or tension type.

### 2.1 Upstream problems

These problems provide prerequisites, tools, or general foundations that Q025 relies on at the effective layer.

* Q021 (`BH_PHYS_QG_L3_021`)
  Reason: supplies high energy completion patterns where baryon number violating interactions can naturally arise.

* Q022 (`BH_PHYS_HIERARCHY_L3_022`)
  Reason: constrains the range of energy scales and couplings for phase transitions relevant to baryogenesis.

* Q023 (`BH_PHYS_STRONG_CP_L3_023`)
  Reason: encodes one potential source of CP violation that may influence baryon asymmetry.

* Q024 (`BH_PHYS_NEUTRINO_MASS_L3_024`)
  Reason: provides neutrino sector structures and CP phases that are central to leptogenesis scenarios.

### 2.2 Downstream problems

These problems directly reuse Q025 components or depend on its outputs.

* Q041 (`BH_COSMO_DARKMATTER_L3_041`)
  Reason: uses the baryon density as a reference scale for the dark matter to baryon ratio and matter content constraints.

* Q044 (`BH_PHYS_PRIMORDIAL_IC_L3_044`)
  Reason: treats baryon asymmetry as part of the effective initial condition data that any primordial initial condition model must reproduce.

* Q048 (`BH_COSMO_H0_TENSION_L3_048`)
  Reason: uses baryon density constraints from early universe fits as part of the global parameter set influencing H0 inference.

### 2.3 Parallel problems

Parallel nodes share similar tension types but no direct component dependence.

* Q041 (`BH_COSMO_DARKMATTER_L3_041`)
  Reason: both Q025 and Q041 treat matter content as a thermodynamic and consistency tension between microphysics and cosmology.

* Q042 (`BH_PHYS_DARK_ENERGY_L3_042`)
  Reason: both deal with effective energy components whose density and evolution must match large scale observations under thermodynamic_tension.

### 2.4 Cross-domain edges

Cross-domain edges connect Q025 to problems in other domains that can reuse its components.

* Q098 (`BH_SOC_ANTHROPOCENE_DYN_L3_098`)
  Reason: reuses charge like asymmetry patterns and conservation structures when modeling human driven imbalances in planetary systems.

* Q121 (`BH_AI_ALIGNMENT_L3_121`)
  Reason: uses the idea that small early asymmetries amplified by dynamics can lead to large late time imbalances in AI behavior.

---

## 3. Tension Universe encoding (effective layer)

All content in this block is at the effective layer. We only describe:

* state spaces
* observables and fields
* invariants and tension scores
* singular sets and domain restrictions
* admissible encodings and fairness constraints
* sector level embedding into the TU tension tensor.

We do **not** describe any hidden generative rules or any mapping from raw microscopic data to TU internal fields.

### 3.1 State space

We assume a semantic state space

```txt
M_BA
```

with the following interpretation at the effective layer:

* Each element `m` in `M_BA` represents a coherent macro configuration for baryon asymmetry, consisting of:

  * effective cosmological parameters relevant to baryon and photon densities
  * coarse grained high energy physics parameters, such as CP violating phases and masses of relevant particles
  * descriptors of the thermal history where departure from equilibrium may occur
  * a compact summary of the resulting baryon to photon ratio and related observables.

We do not specify how these configurations are constructed from raw quantum fields or detailed initial conditions. We only assume:

* For any macro scenario that can be discussed in standard baryogenesis terms, there exist states `m` in `M_BA` that encode its effective properties.
* For the actual universe, there exist one or more states `m_obs` in `M_BA` that encode the best fit cosmological parameters and observed `eta_B`.

### 3.2 Effective fields and observables (hybrid semantics)

In line with `Semantics: hybrid`, we distinguish:

* **Continuous valued observables** (real or vector valued):

  * `eta_B(m)`
  * `B_minus_L(m)`
  * `CP_asym(m; channel)` for each channel
  * `neq_measure(m; epoch)` for each epoch
  * `rho_baryon(m; t)`
  * `rho_radiation(m; t)`
* **Discrete indices**:

  * `channel` labels reaction or decay channels
  * `epoch` labels coarse segments of the thermal history
  * any finite index sets for model classes or scenario tags.

No additional semantic type is introduced. All constructions below use only this continuous plus discrete hybrid structure.

We introduce the following effective fields and observables on `M_BA`.

1. Baryon to photon ratio

```txt
eta_B(m)
```

* Input: state `m` in `M_BA`.
* Output: real number representing the effective baryon to photon ratio implied by `m` at late times.
* Interpretation: should agree with the standard `eta_B` inferred from cosmological data when `m` encodes our universe.

2. Baryon minus lepton charge

```txt
B_minus_L(m)
```

* Input: `m`.
* Output: real number or a small vector describing the effective conserved or approximately conserved baryon minus lepton charge content.
* Interpretation: tracks charges that are important in many baryogenesis mechanisms.

3. CP violation indicators

```txt
CP_asym(m; channel)
```

* Input: `m` and a label `channel` for a reaction or decay channel.
* Output: real number between 0 and 1 representing the effective strength of CP violation in that channel, normalized so that:

  * `0` means no CP violation in that channel
  * values closer to `1` indicate strong CP violation.

Only a finite set of channels is needed at the effective layer.

4. Departure from equilibrium measure

```txt
neq_measure(m; epoch)
```

* Input: `m` and a label `epoch` for a segment of the thermal history (for example pre transition, during transition, post transition).
* Output: nonnegative scalar summarizing how far from equilibrium the system is in that epoch.
* Values near `0` represent near equilibrium; larger values represent stronger departure.

5. Energy density histories

```txt
rho_baryon(m; t)
rho_radiation(m; t)
```

* Input: `m` and a coarse grained time coordinate `t` in a specified range.
* Output: real valued functions or sampled values representing effective baryon energy density and radiation energy density as functions of cosmic time, in units consistent with standard cosmology.

6. Observed band for baryon ratio

We assume the existence of a fixed observed band

```txt
eta_B_obs_min
eta_B_obs_max
```

such that any acceptable encoding that matches data must satisfy

```txt
eta_B_obs_min <= eta_B(m_obs) <= eta_B_obs_max
```

for a state `m_obs` that encodes our universe.

The numerical values and their uncertainties are supplied by an external source pack and versioned under `LibraryKey_ref_Q025`. This page does not fix particular numbers; it only assumes such a band is given and versioned.

### 3.3 Invariants and effective constraints

At the effective layer we define the following invariants and constraints.

1. B minus L approximate conservation

For states representing the Standard Model or many of its extensions, we may have:

```txt
B_minus_L(m) is approximately constant over the thermal history
```

up to small corrections, except when explicit violation is introduced. This constraint is used to test whether a proposed baryogenesis mechanism is coherent with known conservation laws.

2. Consistency with observed baryon ratio

For states that claim to represent our universe, we require:

```txt
eta_B_obs_min <= eta_B(m) <= eta_B_obs_max
```

This is a hard constraint for low tension states. Large deviations contribute to tension.

3. Sakharov condition indicators

We define three nonnegative indicators:

```txt
S_1(m)  for baryon number violation
S_2(m)  for C and CP violation
S_3(m)  for departure from equilibrium
```

Each `S_k(m)` is defined so that:

* `S_k(m) = 0` means the corresponding condition is completely absent or unsatisfied
* `S_k(m) = 1` means the condition is fully available at the required level
* intermediate values encode partial satisfaction.

`S_k(m)` are derived, at the effective layer, from coarse grained descriptors such as:

* `CP_asym(m; channel)` for a finite set of channels
* `neq_measure(m; epoch)` across relevant epochs
* the presence or absence of effective baryon number violating operators.

For low tension baryogenesis scenarios, the triplet `(S_1, S_2, S_3)` must follow patterns that permit efficient generation and preservation of `eta_B`.

4. Cosmological evolution consistency

We require a basic consistency relation between baryon energy density and radiation energy density, for example the ratio

```txt
R_BR(m; t) = rho_baryon(m; t) / rho_radiation(m; t)
```

must remain within ranges compatible with standard cosmology across the relevant epochs. The detailed functional form is not fixed here; only the existence of consistency constraints is assumed.

### 3.4 Singular set and domain restrictions

Some states may encode incomplete or contradictory information. To handle this, we define a singular set:

```txt
S_sing_BA = {
  m in M_BA :
    eta_B(m) is undefined or not finite
    or B_minus_L(m) is undefined
    or at least one S_k(m) is undefined
    or some required CP_asym(m; channel) is undefined
    or some required neq_measure(m; epoch) is undefined
    or rho_baryon(m; t) or rho_radiation(m; t) cannot be assigned consistently
}
```

We restrict all tension analysis to the regular subset:

```txt
M_BA_reg = M_BA \ S_sing_BA
```

If an experiment or protocol attempts to evaluate the tension functional for a state in `S_sing_BA`, the result is treated as **out of domain** and not as physical evidence about baryon asymmetry.

### 3.5 Admissible encoding class and fairness constraints

We now define the admissible encoding class `A_enc_BA` for Q025. Each element of `A_enc_BA` specifies how macro descriptions and data are mapped into tension scores, subject to fairness and versioning constraints.

An encoding element `E_BA` in `A_enc_BA` consists of:

1. **Observation band and references**

   * A fixed band `[eta_B_obs_min, eta_B_obs_max]` for the baryon to photon ratio, taken from a specific set of cosmological analyses.
   * A reference library for cosmological histories and parameter sets, versioned under `LibraryKey_ref_Q025`.

2. **Mismatch function for the baryon ratio**

   * A function

     ```txt
     d_eta(eta; band)
     ```

     chosen from a simple library `D_BA`, such that:

     * `d_eta(eta; band) = 0` when `eta` lies inside the band
     * `d_eta(eta; band)` is nonnegative and monotonically increases with distance from the band
     * the functional form is specified before any tension values for world describing states are computed.

3. **Mismatch functional for the Sakharov indicators**

   * A function

     ```txt
     H_BA(S_1, S_2, S_3)
     ```

     chosen from a simple library `H_BA`, such that:

     * `H_BA(1, 1, 1)` is small, representing a configuration where all three conditions are present at sufficient strength
     * `H_BA` is large when any of the three indicators is near `0` in a regime where baryogenesis is supposed to occur
     * `H_BA` is nonnegative and continuous on `[0, 1]^3`.

4. **Cosmological mismatch functional**

   * A function

     ```txt
     DeltaS_cosmo(m)
     ```

     chosen from a library `C_BA`, such that:

     * `DeltaS_cosmo(m) = 0` when `rho_baryon(m; t)` and `rho_radiation(m; t)` follow reference curves within uncertainties
     * `DeltaS_cosmo(m)` is nonnegative and increases as deviations from reference cosmology grow
     * the functional form depends only on coarse summaries and does not use detailed scenario specific tuning.

5. **Weight triple and thresholds**

   * A triple of rational weights:

     ```txt
     (w_eta, w_Sakh, w_cos)
     ```

     satisfying:

     ```txt
     w_eta  > 0
     w_Sakh > 0
     w_cos  > 0
     w_eta + w_Sakh + w_cos = 1
     ```

     with each weight a rational number of denominator at most 10, selected from a library `L_w_BA` identified by `WeightKey_Q025`.

   * Thresholds:

     ```txt
     epsilon_BA  > 0   (low tension band upper bound)
     delta_BA    > 0   (high tension lower bound)
     T_fail      > 0   (failure threshold for certain experiments)
     ```

     chosen once per encoding element and recorded as part of `E_BA`.

6. **Versioning and fairness**

   * The pair `(EncodingKey_Q025, LibraryKey_ref_Q025)` identifies:

     * the chosen band, reference library, mismatch function libraries, and thresholds.
   * Once a specific encoding element `E_BA` is fixed:

     * the functions `d_eta`, `H_BA`, `DeltaS_cosmo`, the weight triple `(w_eta, w_Sakh, w_cos)`, and thresholds `epsilon_BA`, `delta_BA`, `T_fail` are all **fixed** for all states and experiments in Q025.
   * Any change in these functions, weights, or thresholds must be treated as a **new encoding element** with a new `EncodingKey_Q025`.
   * Encodings are not allowed to be adjusted **after** inspecting individual tension values for particular worlds in order to force low tension.

`A_enc_BA` is therefore a **family of pre committed, versioned encodings**. All statements about low or high tension for Q025 are always understood relative to a fixed element `E_BA` in `A_enc_BA`.

### 3.6 Sector tension tensor embedding

To connect the scalar baryon asymmetry tension to the TU tension tensor, we define an effective sector embedding:

```txt
T_ij_BA(m) = S_i(m) * C_j(m) * Tension_BA(m) * lambda(m) * kappa_BA
```

where:

* `Tension_BA(m)` is the scalar tension functional defined in Section 4 under a fixed encoding element `E_BA`.
* `S_i(m)` is a source-like factor for the i-th semantic component, capturing how strongly that component depends on baryon asymmetry.
* `C_j(m)` is a receptivity-like factor for the j-th cognitive or modeling component, capturing how sensitive it is to baryon sector deviations.
* `lambda(m)` is a convergence-state factor, bounded within a fixed range (for example in `[lambda_min, lambda_max]`), describing whether local reasoning in that component is convergent, recursive, or unstable.
* `kappa_BA` is a sector specific coupling constant setting the overall scale of baryon asymmetry related tension.

The index sets for `i` and `j`, and the detailed forms of `S_i`, `C_j`, and `lambda`, are not needed at this level. It is sufficient that, for each `m` in `M_BA_reg`, all `T_ij_BA(m)` are finite and well defined.

This embedding does not introduce any new axioms or generative rules; it only locates Q025 within the global TU tension tensor structure.

---

## 4. Tension principle for this problem

This block states how Q025 is characterized as a tension problem within TU at the effective layer, assuming a fixed encoding element `E_BA` in `A_enc_BA`.

### 4.1 Core tension functional

Given `E_BA` with mismatch functions and weights as in Section 3.5, we define three mismatch quantities on `M_BA_reg`.

1. Baryon ratio mismatch

```txt
DeltaS_eta(m) =
  0                         if eta_B_obs_min <= eta_B(m) <= eta_B_obs_max
  d_eta(eta_B(m); band_BA)  otherwise
```

where:

* `band_BA = [eta_B_obs_min, eta_B_obs_max]` is the fixed observational band for `E_BA`
* `d_eta` is the chosen mismatch function for `E_BA`.

2. Sakharov mismatch

We define:

```txt
DeltaS_Sakh(m) = H_BA(S_1(m), S_2(m), S_3(m))
```

where `H_BA` is the chosen Sakharov mismatch functional for `E_BA`.

3. Cosmological mismatch

We define:

```txt
DeltaS_cosmo(m)
```

as the chosen cosmological mismatch functional for `E_BA`, a nonnegative scalar summarizing mismatch between `rho_baryon(m; t), rho_radiation(m; t)` and the reference cosmological evolution.

We then define the baryon asymmetry tension functional:

```txt
Tension_BA(m) =
  w_eta  * DeltaS_eta(m)
+ w_Sakh * DeltaS_Sakh(m)
+ w_cos  * DeltaS_cosmo(m)
```

with weights `(w_eta, w_Sakh, w_cos)` given by the weight triple in `E_BA`, satisfying the fairness and rationality constraints stated earlier.

By construction:

* `Tension_BA(m) >= 0` for all `m` in `M_BA_reg`.
* `Tension_BA(m) = 0` only when:

  * `eta_B(m)` lies inside the observed band
  * the Sakharov indicators collectively represent a fully coherent baryogenesis window
  * the cosmological evolution is compatible with the chosen reference.
* `Tension_BA(m)` grows when any of the three mismatch components grows, with weight determined by `(w_eta, w_Sakh, w_cos)`.

### 4.2 Low-tension principle

At the effective layer, the Q025 **low tension principle** can be stated as follows, relative to a fixed encoding element `E_BA`:

> There exist states `m` in `M_BA_reg` that represent our universe such that the baryon asymmetry tension functional `Tension_BA(m)` is small and remains stable under reasonable refinement of the encoding.

More concretely:

* For the fixed `E_BA`, there exists at least one state `m_obs` in `M_BA_reg` such that:

  * `eta_B(m_obs)` lies in the observed band
  * the Sakharov indicators and cosmological evolution encoded in `m_obs` lead to

    ```txt
    Tension_BA(m_obs) <= epsilon_BA
    ```

    where `epsilon_BA` is the low tension threshold attached to `E_BA`.
* Refining the encoding to include more accurate data or finer resolution, while staying inside the same encoding class `A_enc_BA`, does not systematically force `Tension_BA` for the corresponding refined states to exceed acceptable bounds.

This statement does **not** assert any particular microphysical mechanism. It only asserts that there is at least one macro configuration within the allowed encoding class that yields low tension.

### 4.3 High-tension failure

The complementary high tension scenario is:

> For every state `m` in `M_BA_reg` that respects current microphysical bounds and cosmological constraints, the baryon asymmetry tension functional `Tension_BA(m)` remains bounded away from zero.

Formally, for the fixed `E_BA` there exists a strictly positive constant `delta_BA` (stored in `E_BA`) such that, for all admissible states `m` representing realistic microphysics and cosmology,

```txt
Tension_BA(m) >= delta_BA > 0
```

In this case:

* Either `eta_B(m)` cannot be placed within the observed band
* Or the Sakharov indicators cannot simultaneously reach values needed for efficient baryogenesis
* Or the implied cosmological evolution becomes incompatible with other observations.

Such a result would **falsify the encoding element `E_BA` for Q025 at the effective layer**, not the underlying physics and not TU as a whole. A different encoding element in `A_enc_BA` might still admit low tension explanations.

---

## 5. Counterfactual tension worlds

We outline two counterfactual worlds at the effective layer, both interpreted relative to a fixed encoding element `E_BA`:

* World T: baryon asymmetry is dynamically explained in a low tension way.
* World F: baryon asymmetry remains unexplained under all realistic configurations in the chosen encoding element.

These worlds are described through observable patterns and tension values, not through any hidden construction rules.

### 5.1 World T (asymmetry dynamically explained, low tension)

In World T:

1. Observed baryon ratio

   * There exist states `m_T` in `M_BA_reg` representing our universe such that:

     ```txt
     eta_B_obs_min <= eta_B(m_T) <= eta_B_obs_max
     ```

   * The uncertainty band and inferred value are consistent with the source pack associated with `LibraryKey_ref_Q025`.

2. Sakharov triplet behavior

   * For relevant epochs, the triplet `(S_1(m_T), S_2(m_T), S_3(m_T))` reaches values near `(1, 1, 1)` in at least one thermal history window, indicating that baryon number violation, CP violation, and departure from equilibrium all occur in a suitable way.
   * Outside those windows, the indicators may relax, but the generated asymmetry remains frozen in.

3. Cosmological evolution

   * `rho_baryon(m_T; t)` and `rho_radiation(m_T; t)` follow curves that match standard cosmology within uncertainties for the epochs relevant to nucleosynthesis and the cosmic microwave background.
   * No hidden inconsistency appears in late time matter density.

4. Tension band

   * For these states `m_T`, the baryon asymmetry tension functional satisfies:

     ```txt
     Tension_BA(m_T) <= epsilon_BA
     ```

     with `epsilon_BA` the low tension threshold of `E_BA`.
   * Refining the encoding or adding more precise data does not drive `Tension_BA` for the refined states above this threshold in a systematic way.

### 5.2 World F (persistent high tension, asymmetry not coherently explained)

In World F:

1. Observed baryon ratio mismatch

   * For any state `m_F` that attempts to encode our universe consistently with microphysics and cosmology, `eta_B(m_F)` either remains near zero or falls outside the observed band in a way that cannot be corrected without breaking other constraints.

2. Sakharov triplet obstruction

   * Attempts to make `(S_1(m_F), S_2(m_F), S_3(m_F))` simultaneously large in the right epoch lead to conflicts with experimental limits on CP violation, baryon number violation, or cosmological history.
   * Any configuration that produces significant baryon asymmetry violates at least one known bound.

3. Cosmological evolution conflict

   * For states that match the observed `eta_B`, the implied energy density histories `rho_baryon(m_F; t)` and `rho_radiation(m_F; t)` deviate from cosmological observations in a way that cannot be repaired within the encoding element `E_BA`.

4. Persistent tension

   * For all such realistic states `m_F`, there is a lower bound:

     ```txt
     Tension_BA(m_F) >= delta_BA
     ```

     with `delta_BA > 0` the high tension lower bound stored in `E_BA`.
   * Attempts to reduce tension by changing reference bands, mismatch functions, or weights without changing `EncodingKey_Q025` are considered **out of scope** and not allowed.

### 5.3 Interpretive note

These counterfactual worlds do not claim to construct TU internal fields from raw data. They describe how observable summaries behave, and how the baryon asymmetry tension functional reacts, under different high level assumptions.

Any real application must still be grounded in detailed microphysical models and cosmological data. Q025 only provides a **structured language** for expressing and testing how “strange” or “natural” the baryon asymmetry looks under a given encoding.

---

## 6. Falsifiability and discriminating experiments

This block specifies experiments and protocols at the effective layer that can:

* test the coherence of a given encoding element `E_BA` for Q025
* distinguish between competing baryon asymmetry encodings
* provide evidence for or against particular parameter choices.

These experiments do **not** prove or disprove any specific baryogenesis mechanism. They can falsify TU encodings of Q025 at the effective layer.

### Experiment 1: Joint cosmological inference of `eta_B` and tension evaluation

**Goal**
Test whether the chosen `Tension_BA` functional under a fixed `E_BA` can remain small for states that match the jointly inferred baryon to photon ratio from big bang nucleosynthesis and cosmic microwave background data.

**Setup**

* Input data:

  * standard big bang nucleosynthesis measurements
  * cosmic microwave background observations that constrain `eta_B`.
* Construct a band `[eta_B_obs_min, eta_B_obs_max]` from these analyses, as part of the reference library identified by `LibraryKey_ref_Q025`.
* Fix an encoding element `E_BA` in `A_enc_BA`, including:

  * the band `band_BA`
  * mismatch functions `d_eta`, `H_BA`, `DeltaS_cosmo`
  * weights `(w_eta, w_Sakh, w_cos)`
  * thresholds `epsilon_BA`, `delta_BA`, `T_fail`.

**Protocol**

1. Build a family of effective states `{m_data}` in `M_BA_reg` that encode:

   * best fit cosmological parameters
   * `eta_B` values across the allowed band
   * compatible baryon and radiation density histories.

2. For each `m_data`, compute:

   ```txt
   DeltaS_eta(m_data)
   DeltaS_Sakh(m_data)
   DeltaS_cosmo(m_data)
   Tension_BA(m_data)
   ```

   using the functions and weights from `E_BA`.

3. Assign Sakharov indicators `S_k(m_data)` and cosmological mismatch `DeltaS_cosmo(m_data)` using rules that are **part of `E_BA`** or its associated libraries, not chosen ad hoc per scenario.

4. Study how `Tension_BA(m_data)` varies as one moves within the observational band and among different choices of baryogenesis parameters that remain compatible with current bounds, while keeping `E_BA` fixed.

**Metrics**

* Minimal value of `Tension_BA(m_data)` attained across the family.
* Range of `Tension_BA` values for configurations that closely match `eta_B` and other cosmological data.
* Sensitivity of the tension distribution to small perturbations of model parameters, holding `E_BA` fixed.

**Falsification conditions**

* If, for all realistic choices of microphysical and thermal-history parameters consistent with known constraints, every `m_data` satisfying the observational band has

  ```txt
  Tension_BA(m_data) > T_fail
  ```

  then the current encoding element `E_BA` is considered **falsified at the effective layer** and must be replaced by a new element with a new `EncodingKey_Q025`.
* If small, justified changes in **model parameters** (not in the encoding itself) significantly change `Tension_BA` in ways that invert the ranking of obviously more and less plausible scenarios, `E_BA` is considered unstable and rejected.

**Semantics implementation note**
All quantities in this experiment use the `Semantics: hybrid` structure: continuous fields for densities and time evolution, discrete indices for channels and epochs. No additional semantic type is introduced.

**Boundary note**
Falsifying `E_BA` does not solve the canonical baryon asymmetry problem. It only rejects a particular choice of encoding for Q025.

---

### Experiment 2: Model world comparison of baryogenesis scenarios

**Goal**
Assess whether the Q025 encoding can systematically distinguish between classes of microphysical models that can and cannot plausibly generate the observed baryon asymmetry, relative to a fixed encoding element `E_BA`.

**Setup**

* Define two model classes:

  * Class T: baryogenesis scenarios that are widely regarded as capable, in principle, of generating the observed `eta_B` under some parameter choices (for example standard leptogenesis or specific electroweak baryogenesis models).
  * Class F: scenarios that either preserve baryon symmetry too strongly or lack enough CP violation or departure from equilibrium to generate significant asymmetry.

* For each class, build a finite library of effective macro states `{m_T_model}`, `{m_F_model}` in `M_BA_reg`, encoding representative parameter sets and thermal histories.

* The membership of these libraries and the mapping from microscopic models to states are part of an externally specified **model pack** that is fixed before tension evaluation and tied to `LibraryKey_ref_Q025`.

**Protocol**

1. For each model in Class T, construct one or more states `m_T_model` in `M_BA_reg` that encode its typical parameter values, thermal history, and expected `eta_B` range.

2. For each model in Class F, construct states `m_F_model` representing realistic configurations within that class.

3. For each `m_T_model` and `m_F_model`, compute:

   ```txt
   DeltaS_eta(m)
   DeltaS_Sakh(m)
   DeltaS_cosmo(m)
   Tension_BA(m)
   ```

   using the fixed encoding element `E_BA`.

4. Compare the distributions of `Tension_BA` for Class T and Class F.

**Metrics**

* Mean and variance of `Tension_BA` in Class T and Class F.
* Separation between the two distributions, measured by a simple distance or overlap metric.
* Fraction of Class T states with tension below a chosen low tension threshold (for example `epsilon_BA` or a multiple thereof), and fraction of Class F states above a high tension threshold (for example `T_fail`).

**Falsification conditions**

* If the encoding consistently assigns **lower** tension to Class F states than to Class T states in a robust way, the encoding element `E_BA` is considered misaligned and rejected for Q025.
* If the two distributions heavily overlap so that no reasonable thresholds (selected before looking at model specific tension values) yield a meaningful separation, the encoding is considered ineffective for distinguishing plausible from implausible baryogenesis scenarios.

**Semantics implementation note**
The model states use the same hybrid structure as Q025 in general. No additional internal structure is exposed beyond the effective fields already defined.

**Boundary note**
Falsifying `E_BA` or a model pack does not select a unique correct baryogenesis scenario. It evaluates the **discriminating power** of the encoding between model classes at the effective layer.

---

## 7. AI and WFGY engineering spec

This block describes how Q025 can be used as an engineering module for AI systems within the WFGY framework, at the effective layer and under a fixed encoding element `E_BA`. It does not treat AI outputs as physical experiments; all signals are internal diagnostic or training tools.

### 7.1 Training signals

We define several training signals that an AI system can use as auxiliary objectives in physics or cosmology reasoning tasks.

1. `signal_etaB_band_consistency`

   * Definition: a penalty signal proportional to `DeltaS_eta(m)` when the context assumes standard cosmology.
   * Purpose: encourage internal states where derived baryon asymmetry values remain inside or close to the observational band.

2. `signal_Sakharov_triplet_consistency`

   * Definition: a signal based on `DeltaS_Sakh(m)`, with lower values when the Sakharov triplet behaves coherently for a proposed baryogenesis epoch.
   * Purpose: guide the model away from narratives that claim successful baryogenesis while failing one of the three Sakharov conditions.

3. `signal_cosmo_tension_profile`

   * Definition: a signal driven by `DeltaS_cosmo(m)` that increases when proposed baryon history conflicts with known energy density evolution.
   * Purpose: penalize explanations that generate `eta_B` at the cost of breaking cosmological consistency.

4. `signal_counterfactual_separation_BA`

   * Definition: a signal that measures how clearly the model keeps separate its reasoning under a World T style assumption and a World F style assumption for Q025.
   * Purpose: reduce inconsistent mixing of assumptions in long reasoning chains about baryon asymmetry.

These signals are used **only** as internal training or evaluation aids. They do not constitute new experimental evidence about the physical universe.

### 7.2 Architectural patterns

We outline module patterns that can reuse Q025 structures without revealing any deep TU generative rules.

1. `BaryogenesisTensionHead`

   * Role: a head that, given an internal representation of a physics context, estimates `Tension_BA(m)` as an auxiliary output.
   * Interface: maps internal embeddings to:

     * a scalar tension estimate
     * an optional vector of the three mismatch components `(DeltaS_eta, DeltaS_Sakh, DeltaS_cosmo)`.

2. `CosmoParamProjector_BA`

   * Role: a module that projects internal states onto an effective cosmological parameter set, including `eta_B`, matter density parameters, and simple indicators of thermal history.
   * Interface: takes context embeddings as input and outputs a small set of scalar parameters that can feed into the Q025 encoding.

3. `SakharovConditionClassifier`

   * Role: a module that infers approximate values of `S_1`, `S_2`, `S_3` from the description of microphysics and phase transitions in the context.
   * Interface: converts symbolic or numerical context features into the three indicators used by `H_BA`.

These modules act as **observers** of model internals at the effective layer. They do not modify TU generative rules and do not access any hidden axiom system.

### 7.3 Evaluation harness

We suggest an evaluation harness for AI models augmented with Q025 modules under a fixed encoding element `E_BA`.

1. Task design

   * A set of questions about baryon asymmetry, baryogenesis scenarios, and consistency with experimental bounds.
   * Each question specifies whether standard cosmology and observational `eta_B` constraints are assumed.

2. Conditions

   * Baseline: model operates without Q025 specific modules or signals.
   * TU enhanced: model uses the `BaryogenesisTensionHead` and related signals as auxiliary heads.

3. Metrics

   * Accuracy on questions that require connecting Sakharov conditions, microphysics, and `eta_B`.
   * Internal consistency of multi step explanations concerning how asymmetry arises and freezes in.
   * Frequency of answers that either violate known bounds or propose impossible combinations of parameters.

### 7.4 60-second reproduction protocol

A minimal protocol allowing external users to experience the **structuring effect** of Q025 encoding in an AI system, without treating AI responses as physical evidence.

* Baseline setup

  * Prompt: ask the AI to explain why there is more matter than antimatter in the universe, and what the Sakharov conditions are, without any mention of WFGY or tension.
  * Observation: record whether the explanation is fragmented, whether it misses constraints from cosmology, or whether it mixes incompatible mechanisms.

* TU encoded setup

  * Prompt: ask the same question but additionally instruct the AI to:

    * treat `eta_B` as a key observable
    * explain how the three Sakharov conditions control the generation of `eta_B`
    * discuss tension between microphysics and cosmology using a single scalar indicator derived from Q025.
  * Observation: record whether the explanation becomes more structured and more explicit about the interplay between microphysics, thermal history, and cosmological data.

* Comparison metric

  * Use a human rubric that scores:

    * clarity of the role of `eta_B`
    * explicit use of the three Sakharov conditions
    * presence or absence of obvious inconsistencies.

* What to log

  * Prompts, responses, any internal estimates of `Tension_BA(m)`, and derived parameter summaries.
  * These logs allow later inspection of how the Q025 modules influenced reasoning, without exposing any deep TU generative rule.

---

## 8. Cross problem transfer template

This block describes the reusable components produced by Q025 and how they transfer to other problems, subject to their own encoding classes and fairness constraints.

### 8.1 Reusable components produced by this problem

1. ComponentName: `BaryogenesisConditionTriplet`

   * Type: functional
   * Minimal interface:

     * Inputs: coarse grained microphysics descriptors (couplings, CP phases, masses), thermal history descriptors (phase transition types and epochs).
     * Outputs: three indicators `(S_1, S_2, S_3)` in the range `[0, 1]`.
   * Preconditions:

     * Input descriptions must be coherent enough that it is meaningful to talk about baryon number violation, CP violation, and departure from equilibrium in at least one epoch.
     * The functional does not require any detailed microscopic dynamics beyond what is encoded in these descriptors.

2. ComponentName: `AsymmetryTensionFunctional_BA`

   * Type: functional
   * Minimal interface:

     * Inputs: `eta_eff` (an effective asymmetry ratio), an observed band `[eta_min, eta_max]`, a small vector of condition indicators, and cosmology mismatch scalars.
     * Output: a nonnegative tension scalar representing the mismatch between microphysics driven asymmetry and observed constraints.
   * Preconditions:

     * The observed band and conditions are defined in a self consistent way for the domain of interest.
     * A weight set and thresholds, analogous to `(w_eta, w_Sakh, w_cos, epsilon_BA, delta_BA, T_fail)`, are defined by the **target problem’s encoding**, not by Q025.
     * The same fixed weights and functional form are used for all states in a given application.

3. ComponentName: `CosmoMatterContentDescriptor`

   * Type: field
   * Minimal interface:

     * Inputs: a context describing matter and radiation components in a cosmological model.
     * Output: a small vector summarizing relative densities of baryons, dark matter, radiation, and possibly other components at key epochs.
   * Preconditions:

     * The context must specify at least a basic cosmological model with well defined matter content parameters.

### 8.2 Direct reuse targets

1. Q041 (Nature of dark matter)

   * Reused components: `AsymmetryTensionFunctional_BA`, `CosmoMatterContentDescriptor`.
   * Why it transfers: the dark matter to baryon ratio can be treated as an asymmetry between visible and non visible matter components, with tension defined relative to cosmological constraints.
   * What changes:

     * `eta_eff` becomes a ratio involving dark matter density.
     * The observed band and condition indicators are adjusted to reflect dark matter physics rather than baryon number.
     * Q041 must define its own encoding class, keys, and thresholds; it does **not** inherit `EncodingKey_Q025` or `WeightKey_Q025`.

2. Q044 (Initial conditions of the universe)

   * Reused component: `BaryogenesisConditionTriplet`.
   * Why it transfers: any proposed initial condition model that includes pre existing asymmetries must satisfy or explain why the Sakharov triplet is or is not realized dynamically.
   * What changes:

     * The focus shifts to classifying which families of initial conditions admit a later epoch where `(S_1, S_2, S_3)` behave like successful baryogenesis.
     * Q044 defines its own encoding and tension functional.

3. Q098 (Anthropocene system dynamics)

   * Reused component: `AsymmetryTensionFunctional_BA` as a **pattern**.
   * Why it transfers: similar functional forms can be used to encode tension between asymmetries in human activity and planetary capacity, replacing baryon charges with resource or impact asymmetries.
   * What changes:

     * The meaning of `eta_eff` and condition indicators changes from particle physics quantities to socio technical indicators.
     * All encodings and fairness constraints are defined within Q098’s own encoding class.

**Cross problem reuse rule**
Any target problem that reuses Q025 components must:

* Define its own encoding class and regular domain.
* Provide its own encoding keys, reference libraries, weight sets, and thresholds.
* Treat Q025 components as templates or subroutines, not as shared global parameters.
* Avoid silently reusing Q025’s `EncodingKey_Q025`, `LibraryKey_ref_Q025`, or `WeightKey_Q025`.

---

## 9. TU roadmap and verification levels

This block explains how Q025 is positioned along the TU verification ladder and what the next measurable steps are, for a given encoding class `A_enc_BA`.

### 9.1 Current levels

* E_level: E1

  * A coherent effective encoding of baryon asymmetry in terms of a thermodynamic tension functional has been specified.
  * At least two experiments with explicit falsification conditions, tied to a versioned encoding element `E_BA`, are provided.
  * The singular set `S_sing_BA` and the regular domain `M_BA_reg` are defined.
  * The embedding into the TU tension tensor is explicitly stated.

* N_level: N1

  * The narrative connecting baryon asymmetry, Sakharov conditions, and cosmological observations is explicit at the effective layer.
  * Counterfactual worlds and model world experiments are described in a way that can be instantiated by external implementations.

### 9.2 Next measurable step toward E2

To reach E2 for a specific encoding element `E_BA`, the following steps are proposed:

1. Implement a working open source prototype that, given published cosmological fits and a small library of baryogenesis scenarios, computes `Tension_BA(m)` for each scenario and publishes the resulting tension profiles.
2. Explicitly define a finite library of model states in Classes T and F and run Experiment 2 end to end, with clear thresholds and classification statistics.
3. Document the chosen mismatch functions, weights, and thresholds for `E_BA` in a machine readable format tied to `EncodingKey_Q025`, and provide independent reproduction instructions.

These steps operate entirely at the level of observable summaries and effective functionals, consistent with the effective layer constraints.

### 9.3 Long-term role in the TU program

In the long term, Q025 is expected to serve as:

* The reference node for charge and matter asymmetry problems in cosmology and related fields.
* A template for encoding small but crucial asymmetries that emerge from early universe dynamics as thermodynamic tension problems.
* An example of how TU style tension functionals can structure debates about mechanisms without claiming proof, by isolating where tension resides between data and proposed dynamics.

---

## 10. Elementary but precise explanation

The basic puzzle behind Q025 is simple to say:

> The universe appears to contain matter made of baryons, but almost no antibaryons. Why did matter win, and why by this particular small amount?

If the universe had started with exactly equal amounts of matter and antimatter, and if the laws of physics always treated them perfectly symmetrically, then most baryons and antibaryons would have annihilated each other, leaving behind almost only radiation. That is not what we see.

Standard physics tells us that, under some conditions, the universe can generate a small excess of baryons through processes that:

* change baryon number
* treat matter and antimatter slightly differently
* happen when the universe is not in smooth thermal equilibrium.

These are the Sakharov conditions. Many detailed models try to use them to generate the observed baryon asymmetry, but none is uniquely confirmed.

From the Tension Universe point of view, Q025 does not try to pick a winning model. Instead, it does three things:

1. It treats the baryon to photon ratio `eta_B` as a key observable that must fall inside a narrow band set by cosmological data.
2. It defines simple indicators that say how strongly the Sakharov conditions are available in a given scenario.
3. It combines these, together with basic cosmological consistency, into a single number called the baryon asymmetry tension `Tension_BA`.

Roughly:

* `Tension_BA` is small when a scenario:

  * produces the observed `eta_B`
  * uses the Sakharov conditions in a coherent way
  * fits with what we know about the history of the universe.
* `Tension_BA` is large when a scenario:

  * fails to produce enough asymmetry
  * relies on forbidden or unrealistic physics
  * or conflicts with cosmological observations.

We then consider families of possible worlds or model scenarios and ask, for a fixed encoding:

* In **low tension worlds**, do there exist configurations with small baryon asymmetry tension that look like our universe?
* In **high tension worlds**, is the tension always large no matter how we adjust parameters inside realistic bounds?

This does not prove which mechanism is correct. It does not bypass the need for detailed calculations and experiments. What it does provide is:

* a clear way to express the problem in terms of observable quantities
* a single tension functional that can be tested and falsified
* reusable components that apply to other problems about asymmetries in physics and beyond.

Q025 is therefore the main baryon asymmetry node in the Tension Universe framework, and a concrete example of how to encode a difficult cosmological puzzle at the effective layer without revealing any deep generative rules.

---

## Tension Universe effective-layer footer

This page is part of the **WFGY / Tension Universe** S-problem collection and should be interpreted strictly at the **effective layer**.

### Scope of claims

* The goal of this document is to specify an **effective-layer encoding** of the baryon asymmetry problem (Q025) as a thermodynamic tension node.
* It does **not** claim to:

  * prove or disprove any specific baryogenesis mechanism
  * select a unique microscopic theory of high energy physics or cosmology
  * introduce any new theorem about baryon asymmetry.
* It should **not** be cited as evidence that the baryon asymmetry of the universe has been solved at the fundamental level.

### Effective-layer boundary

* All objects used here (state spaces `M_BA`, observables, invariants, tension scores, counterfactual worlds) live at the **effective layer** of the TU framework.
* No TU axioms, generative rules, or internal fields are exposed or modified by this page.
* All mappings from:

  * raw experimental data
  * detailed microphysical models
  * initial conditions
    into the state space `M_BA` are delegated to external implementations and reference libraries.

### Encoding and fairness

* Q025 uses a versioned encoding class `A_enc_BA`.

* The current encoding element is identified by:

  ```txt
  Encoding_class: A_enc_BA
  EncodingKey_Q025: ENC_BA_v1_2026_01_29
  LibraryKey_ref_Q025: LIB_BA_REF_v1
  WeightKey_Q025: WSET_BA_v1
  ```

* For any fixed encoding element in `A_enc_BA`:

  * the observational band for `eta_B`,
  * the mismatch functionals `d_eta`, `H_BA`, `DeltaS_cosmo`,
  * the weights `(w_eta, w_Sakh, w_cos)`,
  * and the thresholds `epsilon_BA`, `delta_BA`, `T_fail`
    are all fixed **before** evaluating tension for particular worlds.

* Any change to these ingredients is considered a **new encoding** and must receive a new `EncodingKey_Q025`.

* Encodings must not be tuned after seeing world specific tension values in order to force low tension.

### Cross-problem reuse boundary

* Components exported from Q025 (such as `BaryogenesisConditionTriplet`, `AsymmetryTensionFunctional_BA`, `CosmoMatterContentDescriptor`) are reusable **templates**.
* Any target problem that reuses these components must:

  * define its own encoding class and regular domain
  * provide its own encoding keys, reference libraries, weight sets, and thresholds
  * not silently reuse `EncodingKey_Q025`, `LibraryKey_ref_Q025`, or `WeightKey_Q025`.
* Low or high tension statements in other problems cannot be inferred directly from Q025; they must be established within the target problem’s own encoding.

### Relation to TU charters

This page should be read together with the following charters:

* [TU Effective Layer Charter](../Charters/TU_EFFECTIVE_LAYER_CHARTER.md)
* [TU Encoding and Fairness Charter](../Charters/TU_ENCODING_AND_FAIRNESS_CHARTER.md)
* [TU Tension Scale Charter](../Charters/TU_TENSION_SCALE_CHARTER.md)
* [TU Global Guardrails](../Charters/TU_GLOBAL_GUARDRAILS.md)
