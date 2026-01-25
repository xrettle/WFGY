# Q068 · Prebiotic chemistry networks

## 0. Header metadata

```txt
ID: Q068
Code: BH_CHEM_PREBIOTIC_NETWORK_L3_068
Domain: Chemistry
Family: Prebiotic chemistry and origins of life
Rank: S
Projection_dominance: M
Field_type: dynamical_field
Tension_type: thermodynamic_tension
Status: Open
Semantics: hybrid
E_level: E1
N_level: N1
Last_updated: 2026-01-25
```

---

## 1. Canonical problem and status

### 1.1 Canonical statement

Consider plausible prebiotic environments on early Earth (or similar planets), driven far from equilibrium by energy fluxes such as light, redox gradients, or geothermal heat. Within such environments, complex chemical reaction networks involving small molecules, simple polymers, and mineral surfaces can, in principle, emerge and evolve.

The canonical problem for Q068 is:

> Do there exist physically realistic, non-equilibrium prebiotic chemical networks that:
>
> 1. are robustly sustained by environmental driving,
> 2. maintain and propagate nontrivial chemical organization over long times,
> 3. can, in a well defined sense, increase their functional complexity,
>
> without already presupposing modern biological machinery?

Equivalently, in more operational terms:

> Under realistic early Earth conditions, can we identify classes of reaction networks and environmental protocols that support long-lived, self-sustaining, and structurally organized prebiotic chemistry, rather than quickly relaxing to chemical equilibrium or trivial steady states?

The problem is not simply to propose isolated reaction sequences, but to understand the structure and existence of entire network regimes that can act as proto-metabolic scaffolds.

### 1.2 Status and difficulty

Progress has been made in several directions:

* Identification of specific prebiotic reaction pathways (for example nucleotide precursors, simple peptides, lipid precursors) under plausible early Earth conditions.
* Development of systems chemistry models that explore network-level behavior beyond single reactions.
* Non-equilibrium thermodynamics frameworks that relate entropy production, fluxes, and emergent structures.

However, there is no widely accepted, quantitative theory that:

* unifies non-equilibrium driving, network topology, and environmental variability,
* clearly distinguishes regimes that support robust prebiotic organization from those that do not,
* connects laboratory-scale experiments with planetary-scale constraints in a systematic way.

The problem remains extremely hard because it sits at the intersection of:

* complex reaction network dynamics,
* disordered and heterogeneous geochemical environments,
* non-equilibrium thermodynamics and information-like notions of organization.

### 1.3 Role in the BlackHole project

Within the BlackHole collection, Q068 serves as:

1. The core S-level node for **prebiotic chemistry networks**, linking chemistry to origins-of-life biology.
2. A template for thermodynamic_tension problems where sustained non-equilibrium structure and organization must be explained without invoking existing biological machinery.
3. An interface node between:

   * chemical S problems (Q061–Q070),
   * biological and origins-of-life problems (Q071–Q080),
   * planetary environment and climate problems in other domains.

Q068 is also the first place where non-equilibrium chemical networks are explicitly encoded in Tension Universe terms.

### References

1. I. Prigogine and G. Nicolis, “Self-Organization in Non-Equilibrium Systems”, Wiley, 1977.
2. J. D. Sutherland, “The Origin of Life Out of Equilibrium”, reported in modern reviews of prebiotic chemistry and non-equilibrium driving.
3. E. Smith and H. J. Morowitz, “The Origin and Nature of Life on Earth: The Emergence of the Fourth Geosphere”, Cambridge University Press, 2016.
4. General reviews on prebiotic chemistry and systems chemistry in standard origin-of-life textbooks and survey articles.

---

## 2. Position in the BlackHole graph

This block records how Q068 sits in the BlackHole graph. Each edge has a one-line reason pointing to concrete components or tension types.

### 2.1 Upstream problems

These provide foundations, tools, or constraints that Q068 reuses at the effective layer.

* Q061 (BH_CHEM_BOND_NATURE_L3_061)
  Reason: Supplies effective descriptions of strongly correlated chemical bonding used inside the network state space and flux descriptors.

* Q062 (BH_CHEM_CATALYST_DESIGN_L3_062)
  Reason: Provides design-level views of catalysis that feed into how catalytic motifs are represented in prebiotic network observables.

* Q066 (BH_CHEM_ELECTROCHEM_L3_066)
  Reason: Contributes non-equilibrium electrochemical motifs reused as template fields for environmental driving and energy flux observables.

* Q067 (BH_CHEM_QUANTUM_MOL_SIM_L3_067)
  Reason: Enables high-accuracy effective parameters for key prebiotic reactions, which are then aggregated in the network-level encoding.

### 2.2 Downstream problems

These directly reuse Q068 components or depend on its notion of prebiotic network tension.

* Q069 (BH_CHEM_SELECTIVITY_RULES_L3_069)
  Reason: Reuses network-based selectivity components to frame reaction selectivity as emergent from prebiotic network structures.

* Q070 (BH_CHEM_SOFTMATTER_L3_070)
  Reason: Uses the non-equilibrium network observables of Q068 as prototypes for soft-matter self-assembly under continuous driving.

* Q071 (BH_BIO_ORIGIN_LIFE_L3_071)
  Reason: Builds on Q068’s prebiotic network tension to specify when a network crosses into proto-biological organization.

* Q072 (BH_BIO_GENETIC_CODE_L3_072)
  Reason: Treats the emergence of coding as a special case of structured channels embedded in driven chemical networks defined at the Q068 level.

### 2.3 Parallel problems

Parallel nodes share similar tension types or structural motifs, but no direct component dependence.

* Q064 (BH_CHEM_GLASS_TRANS_L3_064)
  Reason: Both Q064 and Q068 involve rugged energy landscapes and non-equilibrium structure formation, expressed via thermodynamic_tension.

* Q070 (BH_CHEM_SOFTMATTER_L3_070)
  Reason: Both focus on sustained non-equilibrium organization in soft condensed matter, though Q068 is specific to prebiotic chemistry.

### 2.4 Cross-domain edges

Cross-domain edges mark problems that can reuse Q068 components or interpret them in other settings.

* Q031 (BH_EARTH_PLANET_ENV_L3_031)
  Reason: Uses Q068’s environment flux descriptors to constrain which planetary surface and subsurface conditions support prebiotic networks.

* Q073 (BH_BIO_METABOLIC_CORE_L3_073)
  Reason: Reuses prebiotic network motifs as ancestral templates for core metabolic networks.

* Q098 (BH_CS_AUTOCATALYTIC_ALG_L3_098)
  Reason: Adopts the network-level tension formalism from Q068 to analyze autocatalytic structures in abstract algorithmic networks.

---

## 3. Tension Universe encoding (effective layer)

This block describes the effective-layer encoding of prebiotic chemistry networks. It only specifies state spaces, observables, invariants, tension functionals, and singular sets. It does not describe any deep generative rule or any mapping from raw data to internal TU fields.

### 3.1 State space

We postulate an effective state space

```txt
M
```

with the following interpretation:

* Each state `m` in `M` represents a coarse-grained configuration of a prebiotic chemical network in a specified environment, including:

  * a finite set of chemical species and reaction channels,
  * an effective representation of network topology (who reacts with whom),
  * aggregate information about fluxes, entropy production, and environmental driving.

We do not specify how `m` is constructed from underlying microstates. At the effective layer we only require:

* For any finite laboratory or geochemical setup in a bounded region and time window, there exist states in `M` that encode a consistent coarse-grained description of the network under that setup.

### 3.2 Effective fields and observables

We introduce the following observables and fields on `M`.

1. Species abundance field

```txt
C_i(m) >= 0
```

* For each species index `i` in a finite set associated with `m`, `C_i(m)` is an effective abundance (for example concentration) at a chosen reference time window.

2. Reaction flux field

```txt
J_e(m)
```

* For each reaction channel index `e` in the network associated with `m`, `J_e(m)` is an effective net flux (for example average reaction rate in a chosen time window).
* Fluxes can be positive, negative, or zero, depending on direction conventions.

3. Environmental driving descriptor

```txt
Phi_env(m)
```

* A finite-dimensional descriptor of environmental driving, aggregating quantities such as:

  * light intensity bands,
  * redox potential differences,
  * temperature gradients,
  * pH gradients.

4. Entropy production rate

```txt
Sigma_net(m) >= 0
```

* An effective scalar observable summarizing the network-level entropy production rate associated with the combination of reaction fluxes and environmental driving.
* We assume that for states in the regular domain (defined below), Sigma_net(m) is finite and well defined.

5. Structural organization score

```txt
O_struct(m)
```

* A scalar observable that summarizes structural organization of the network, such as:

  * presence and strength of cycles,
  * modularity,
  * redundancy of key pathways,
  * separation between fast and slow subnetworks.

The definition of O_struct(m) is encoding dependent but must be fixed in advance of any particular experiment.

### 3.3 Mismatch observables and reference classes

To define tension, we introduce mismatch observables relative to fixed reference classes.

1. Reference ensembles

We assume fixed reference ensembles that do not depend on the specific target state `m`:

* A reference ensemble of reaction networks that are:

  * random or near-equilibrium, given the same species list and total driving magnitudes, and
  * constructed according to a fixed, pre-declared protocol.

* A reference ensemble of environmental profiles compatible with the same total energy flux scale.

These ensembles are part of the admissible encoding class and are fixed before any evaluation of specific states.

2. Structural mismatch observable

```txt
DeltaS_struct(m) >= 0
```

* Measures how far the structural organization of the network in `m` deviates from the reference ensemble, in terms of O_struct(m) and related quantities.
* DeltaS_struct(m) is zero when the network organization is indistinguishable from typical reference networks and increases as the organization becomes more structured or more fragile in ways of interest.

3. Flux mismatch observable

```txt
DeltaS_flux(m) >= 0
```

* Measures how far the flux pattern J_e(m) and associated Sigma_net(m) deviate from what would be expected for near-equilibrium or reference-driven networks under similar Phi_env(m).
* DeltaS_flux(m) is zero when fluxes and entropy production are compatible with a reference regime and positive when they show significant non-equilibrium organization signatures.

4. Robustness mismatch observable

```txt
DeltaS_robust(m) >= 0
```

* Encodes how sensitive the network behavior is to small perturbations in Phi_env(m) and species abundances.
* DeltaS_robust(m) is small when the network maintains its organizational features under moderate environmental fluctuations and larger when it collapses or becomes chaotic under such perturbations.

All three mismatch observables are fixed functions for a chosen encoding and must not be adjusted post hoc in response to particular data.

### 3.4 Combined prebiotic network tension

We define a combined mismatch:

```txt
DeltaS_pre(m) = a_struct * DeltaS_struct(m)
                + a_flux   * DeltaS_flux(m)
                + a_robust * DeltaS_robust(m)
```

with fixed nonnegative weights satisfying:

```txt
a_struct + a_flux + a_robust = 1
a_struct >= 0
a_flux   >= 0
a_robust >= 0
```

The weights are part of the admissible encoding class and must be chosen once, based on general principles, not tuned separately for each state or experiment.

### 3.5 Effective tension tensor and regular domain

We assume an effective tension tensor:

```txt
T_ij(m) = S_i(m) * C_j(m) * DeltaS_pre(m) * lambda(m) * kappa
```

where:

* S_i(m) is a source-like factor for semantic or functional dimensions indexed by i.
* C_j(m) is a receptivity-like factor for downstream or cognitive dimensions indexed by j.
* DeltaS_pre(m) is the combined mismatch defined above.
* lambda(m) is a convergence-state factor from the TU core, taking values in a fixed bounded interval.
* kappa is a constant that sets the overall scale of prebiotic network tension.

We define the singular set:

```txt
S_sing = { m in M :
           Sigma_net(m) is undefined or not finite
           or any of DeltaS_struct(m), DeltaS_flux(m),
           DeltaS_robust(m) are undefined or not finite }
```

and restrict effective analysis to:

```txt
M_reg = M \ S_sing
```

Whenever an experiment or evaluation attempts to use states in S_sing, the result is treated as “out of domain” rather than as evidence for or against the existence of robust prebiotic networks.

---

## 4. Tension principle for this problem

This block states how Q068 is characterized as a tension problem within TU at the effective layer.

### 4.1 Core prebiotic network tension functional

We define:

```txt
Tension_prebiotic(m) = DeltaS_pre(m)
```

for m in M_reg. This is nonnegative and encodes how “strained” a given prebiotic network configuration is relative to reference ensembles and robustness criteria.

Low Tension_prebiotic(m) means:

* structure and fluxes are in a regime compatible with sustained, organized non-equilibrium behavior under the chosen environment.

High Tension_prebiotic(m) means:

* the configuration is fragile, near collapse, or incompatible with the required non-equilibrium organization.

### 4.2 Prebiotic viability as low-tension regime

At the effective layer, Q068 can be framed as the statement that there exist physically realistic, environmentally compatible states `m_viable` in M_reg such that:

```txt
Tension_prebiotic(m_viable) <= epsilon_pre
```

for a small threshold epsilon_pre that:

* reflects acceptable deviations from reference ensembles and robustness criteria,
* remains bounded as we increase resolution in network description and environmental detail,
* is determined by encoding choices fixed in advance.

Such states represent viable prebiotic networks: they are neither trivial random networks nor finely tuned equilibria, but organized structures sustained by non-equilibrium driving.

### 4.3 Failure regimes as persistent high tension

Conversely, if in all physically realistic settings and encodings within the admissible class we find that:

```txt
Tension_prebiotic(m_real) >= delta_pre
```

for some strictly positive delta_pre that cannot be reduced by making the encoding more detailed or the data more accurate, then the world would be in a regime that does not support robust prebiotic chemical networks.

Thus, at the effective layer, Q068 distinguishes:

* worlds in which low-tension prebiotic network regimes exist and can be instantiated,
* worlds in which all realistic prebiotic chemistry falls into high-tension regimes.

---

## 5. Counterfactual tension worlds

We now consider two counterfactual worlds, described only via observables.

### 5.1 World T (prebiotic networks viable)

World T is a world where non-equilibrium prebiotic chemistry readily forms robust networks under plausible environmental conditions.

1. Network emergence

* For a broad set of geochemical settings, one can construct states `m_T` in M_reg such that:

  ```txt
  DeltaS_struct(m_T) is small,
  DeltaS_flux(m_T) is small,
  DeltaS_robust(m_T) is small.
  ```

2. Entropy production and structure

* Sigma_net(m_T) is positive and remains in a band where non-equilibrium driving is strong enough to support structure but not so extreme as to destroy it.

3. Environmental robustness

* Moderate changes in Phi_env(m_T) do not push networks into S_sing, and Tension_prebiotic(m_T) stays below epsilon_pre over a range of conditions.

### 5.2 World F (prebiotic networks fragile or absent)

World F is a world where prebiotic networks are either extremely fragile or do not reach meaningful organization.

1. Collapse to equilibrium

* For most plausible geochemical settings, any state `m_F` in M_reg that shows initial organization quickly evolves toward configurations with:

  ```txt
  O_struct(m_F) near reference values,
  DeltaS_struct(m_F) and DeltaS_flux(m_F) large or poorly controlled.
  ```

2. Flux and robustness

* Small perturbations in Phi_env(m_F) or C_i(m_F) lead to drastic changes in J_e(m_F), pushing states into S_sing or into regimes with high Tension_prebiotic(m_F).

3. Absence of low-tension regime

* No matter how the encoding resolution is refined within the admissible class, it is not possible to identify states that maintain Tension_prebiotic below a reasonable epsilon_pre over long time windows.

### 5.3 Interpretive note

These worlds do not specify how networks or environments are generated from microphysics. They only assert that, for any such generative mechanism compatible with a given world, there exist or do not exist effective states with the observable properties described above.

---

## 6. Falsifiability and discriminating experiments

This block lists experiments that can falsify specific Q068 encodings at the effective layer.

### Experiment 1: Microreactor network persistence under controlled driving

*Goal:*
Test whether the chosen Tension_prebiotic encoding correctly distinguishes persistent, organized network behavior from transient or trivial chemistry in microreactor experiments.

*Setup:*

* Use microfluidic or batch microreactor platforms with simple prebiotic mixtures (for example carbon sources, inorganic ions, potential catalysts).
* Apply controlled non-equilibrium driving (for example periodic temperature cycling, redox gradients, or light pulses).
* Define a fixed protocol to map experimental conditions to environmental descriptors Phi_env and to extract effective C_i, J_e, Sigma_net, and O_struct.

*Protocol:*

1. Prepare multiple experimental conditions with different driving protocols but similar overall chemical composition.
2. For each condition, record time series of species abundances and reaction rates sufficient to estimate C_i(m_exp), J_e(m_exp), Sigma_net(m_exp), and O_struct(m_exp).
3. For each experiment, construct a state m_exp in M_reg reflecting the coarse-grained network.
4. Compute DeltaS_struct(m_exp), DeltaS_flux(m_exp), DeltaS_robust(m_exp), and Tension_prebiotic(m_exp) using the fixed encoding.
5. Compare tension values and network lifetimes across conditions.

*Metrics:*

* Distribution of Tension_prebiotic(m_exp) across all experiments.
* Correlation between tension values and observed network persistence or structural richness.
* Stability of Tension_prebiotic(m_exp) estimates under small variations in the extraction protocol.

*Falsification conditions:*

* If experiments that clearly show long-lived, structurally rich networks systematically yield high Tension_prebiotic values (above a pre-declared upper bound), while trivial or short-lived chemistry yields lower tension, the encoding is misaligned and considered falsified.
* If small, arbitrary changes in the extraction protocol cause large, uncontrolled swings in Tension_prebiotic without physical justification, the encoding is considered unstable and rejected.

*Semantics implementation note:*
All observables C_i, J_e, Sigma_net, and O_struct are estimated in a hybrid representation consistent with the metadata, but the internal details of that representation remain outside the TU description.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. This experiment can reject specific Q068 encodings, but it does not in itself establish the existence or absence of viable prebiotic networks in nature.

---

### Experiment 2: Planetary-scale constraint via environmental ensembles

*Goal:*
Assess whether the Q068 encoding can identify planetary environments that are compatible with low-tension prebiotic networks.

*Setup:*

* Use geophysical and geochemical models to generate ensembles of early Earth or exoplanet surface and subsurface environments.
* For each environment, define effective environmental descriptors Phi_env and constraints on possible chemical inventory.

*Protocol:*

1. For each environment in the ensemble, define a family of hypothetical networks consistent with the allowed chemistry and driving.
2. For each such network, define states m_model in M_reg with estimated C_i, J_e, Sigma_net, and O_struct.
3. Evaluate Tension_prebiotic(m_model) for all model states using the fixed encoding.
4. For each environment, identify whether there exist model states with Tension_prebiotic below epsilon_pre.

*Metrics:*

* Fraction of environments that admit at least one low-tension network state.
* Distribution of Tension_prebiotic across environments.
* Sensitivity of conclusions to modest changes in environmental parameters within the same ensemble.

*Falsification conditions:*

* If the encoding labels almost all plausible early Earth environments as high-tension regimes without any low-tension pockets, but independent origin-of-life arguments strongly suggest otherwise, the encoding is suspect and may be rejected.
* If the encoding is so permissive that almost any environment is labeled as low tension without discriminating physically meaningful differences, it fails to provide useful constraints and is considered ineffective.

*Semantics implementation note:*
The mapping from geophysical model output to Phi_env and to network parameters is handled outside TU. The Q068 description only requires that the resulting observables be well defined and fall inside M_reg.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. Planetary-scale constraints can rule out particular encodings or parameter choices, but they do not by themselves determine whether Q068 has a positive or negative answer in the real universe.

---

## 7. AI and WFGY engineering spec

This block describes how Q068 can be instantiated as an AI and WFGY module at the effective layer.

### 7.1 Training signals

1. `signal_entropy_profile_alignment`

   * Definition: a signal proportional to DeltaS_flux(m) and Sigma_net(m), penalizing configurations where non-equilibrium driving is either too weak or too strong to sustain structure.
   * Purpose: encourage the model to recognize and favor regimes where non-equilibrium fluxes are compatible with organized prebiotic networks.

2. `signal_structural_organization_score`

   * Definition: a signal derived from O_struct(m) and DeltaS_struct(m), rewarding internal representations that capture network motifs associated with robust prebiotic organization.
   * Purpose: bias the model toward explanations where persistent cycles, modularity, and controlled branching appear in prebiotic scenarios.

3. `signal_robustness_margin`

   * Definition: a signal that tracks DeltaS_robust(m) and measures how much environmental variation can be tolerated before the network collapses.
   * Purpose: penalize narratives that rely on extremely fine-tuned conditions.

4. `signal_prebiotic_viability_index`

   * Definition: a scalar defined as

     ```txt
     VI(m) = 1 / (1 + Tension_prebiotic(m))
     ```

     so that VI(m) is near 1 for low-tension configurations and small for high-tension ones.
   * Purpose: provide a compact viability score used as an auxiliary target or classifier for prebiotic scenarios.

### 7.2 Architectural patterns

1. `PrebioticNetworkEncoder`

   * Role: maps textual or structured descriptions of prebiotic scenarios into internal representations corresponding to states m in M_reg.
   * Interface: takes as input descriptions of species, reactions, and environmental conditions; outputs latent codes used to estimate C_i, J_e, Sigma_net, O_struct, and Tension_prebiotic.

2. `NonEquilibriumTensionHead`

   * Role: a small head network that reads internal embeddings and outputs estimates of DeltaS_struct, DeltaS_flux, DeltaS_robust, and Tension_prebiotic.
   * Interface: provides scalar or low-dimensional outputs that can be monitored during training and evaluation.

3. `EnvironmentFluxModule`

   * Role: a module that encodes environmental descriptions into Phi_env-like latent variables.
   * Interface: feeds into both the PrebioticNetworkEncoder and the NonEquilibriumTensionHead to keep environment-network coupling consistent.

### 7.3 Evaluation harness

1. Task selection

   * A curated set of benchmark questions and case studies on prebiotic chemistry, non-equilibrium networks, and origins-of-life scenarios.

2. Conditions

   * Baseline: model answers questions without explicit access to Q068 modules.
   * TU condition: model uses PrebioticNetworkEncoder and NonEquilibriumTensionHead, with signals from Q068 used during training or inference.

3. Metrics

   * Accuracy on questions where non-equilibrium and network aspects are central.
   * Internal consistency across multi-step reasoning about prebiotic scenarios.
   * Diversity and plausibility of proposed network structures and environmental combinations.

### 7.4 60-second reproduction protocol

* Baseline setup

  * Prompt: ask the AI to describe how non-equilibrium conditions might support the origin of life, and to contrast “just random chemistry” with structured prebiotic networks.
  * Observation: record whether the explanation clearly distinguishes trivial chemistry from persistent, organized networks.

* TU encoded setup

  * Prompt: same theme, but explicitly instruct the AI to reason in terms of:

    * network organization,
    * entropy production and fluxes,
    * robustness under environmental variation,
    * a single viability index akin to VI(m).

  * Observation: compare structure, clarity, and use of network-level concepts.

* Comparison metric

  * Simple rubric rating:

    * explicit mention of network motifs,
    * treatment of non-equilibrium driving,
    * discussion of robustness rather than fine-tuning.

* What to log

  * Prompts, full responses, and any tension or viability scores estimated by Q068 modules, for later analysis.

---

## 8. Cross problem transfer template

### 8.1 Reusable components produced by this problem

1. ComponentName: `PrebioticNetwork_TensionScore`

   * Type: functional

   * Minimal interface:

     ```txt
     inputs: network_description, environment_description
     output: tension_value >= 0
     ```

   * Preconditions:

     * Inputs must be sufficient to define effective C_i, J_e, Sigma_net, and O_struct without leaving M_reg.

2. ComponentName: `NonEquilibriumFlux_Descriptor`

   * Type: field

   * Minimal interface:

     ```txt
     inputs: environment_description
     output: Phi_env_like_descriptor
     ```

   * Preconditions:

     * Environment description must include enough information to define non-equilibrium driving magnitudes and directionality.

3. ComponentName: `CounterfactualPrebioticWorld_Template`

   * Type: experiment_pattern

   * Minimal interface:

     ```txt
     inputs: model_class_of_networks
     output: (WorldT_experiment, WorldF_experiment)
     ```

   * Preconditions:

     * The model class must support generation of networks under varying environmental driving and allow estimation of Tension_prebiotic.

### 8.2 Direct reuse targets

1. Q069 (reaction selectivity rules)

   * Reused component: `PrebioticNetwork_TensionScore`.
   * Why it transfers: selectivity can be reframed as the emergence of low-tension paths in a network, so the same functional helps characterize selective regimes.
   * What changes: the focus shifts from long-term persistence to specificity of products under competing pathways.

2. Q070 (soft matter self assembly)

   * Reused component: `NonEquilibriumFlux_Descriptor`.
   * Why it transfers: soft matter self-assembly also depends on how non-equilibrium driving couples to structure.
   * What changes: observables are now structural motifs in soft materials rather than purely chemical reaction networks.

3. Q071 (origin of life)

   * Reused component: `CounterfactualPrebioticWorld_Template`.
   * Why it transfers: Q071 needs explicit World T and World F constructions for different origins-of-life scenarios built on prebiotic networks.
   * What changes: additional observables covering information storage and replication are added on top of the Q068 framework.

---

## 9. TU roadmap and verification levels

### 9.1 Current levels

* E_level: E1

  * An effective encoding of prebiotic network tension has been specified, including observables, mismatch functionals, and singular sets.
  * Concrete experimental patterns exist to falsify specific encodings.

* N_level: N1

  * The narrative connects prebiotic networks, non-equilibrium driving, and organization, but has not yet been tied to a broad set of concrete models and data.

### 9.2 Next measurable step toward E2

To move from E1 to E2, at least one of the following should be implemented:

1. A software prototype that, given a structured description of a prebiotic experiment or model, computes Tension_prebiotic and its components and publishes the results for multiple scenarios.
2. A published series of microreactor experiments designed explicitly according to the Q068 experiment templates, with documented tension profiles for different driving protocols.

### 9.3 Long-term role in the TU program

In the longer term, Q068 is expected to:

* anchor all prebiotic network and non-equilibrium chemistry problems in the BlackHole graph,
* provide a standard way to compare different origins-of-life proposals in terms of network-level thermodynamic_tension,
* serve as a bridge between chemical, biological, and planetary S problems that involve sustained non-equilibrium organization.

---

## 10. Elementary but precise explanation

Classically, researchers in origin-of-life studies ask questions like:

* What chemicals were available on early Earth?
* What reactions could happen?
* Could those reactions, step by step, lead to life?

In this problem, we focus on a more network-based view.

Imagine a huge web of reactions, where molecules change into other molecules, powered by sunlight, heat, or chemical gradients. Some webs are boring: you mix things, they react once, and then everything calms down. Other webs might be special: they keep cycling, reinforcing certain pathways, and forming structures that last.

Q068 asks, in effect:

* Can such special, self-sustaining webs of reactions exist under realistic early Earth conditions?
* If they do, what makes them different from the boring kinds?

In the Tension Universe view, we do not try to simulate every molecule. Instead, we build a coarse description of the network:

* how many molecules of each type there are,
* how fast reactions flow,
* how much “push” comes from the environment,
* how organized the network structure is.

Then we define a single quantity, called here Tension_prebiotic, that measures how “strained” or “fragile” the network is. If Tension_prebiotic is low, the network looks like one that can keep going and stay organized. If it is high, the network looks fragile or trivial.

We then consider two kinds of worlds:

* In a good world, there are many ways for nature to set up low-tension networks, so prebiotic chemistry has plenty of room to explore and organize.
* In a bad world, almost all networks are high-tension: they either collapse quickly or never become interesting in the first place.

This does not prove how life actually started. It does something more modest but useful:

* It gives a precise way to talk about “interesting prebiotic chemistry” versus “just random reactions”.
* It suggests specific experiments and models that can test whether our way of measuring this difference makes sense.
* It provides tools that can be reused in other problems, such as how early metabolism or coding might have built on these prebiotic networks.

Q068 is therefore the main S-level problem for turning vague ideas about “chemical soups” into a structured, testable notion of prebiotic networks under non-equilibrium conditions.
