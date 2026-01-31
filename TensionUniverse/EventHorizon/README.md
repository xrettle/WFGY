# WFGY 3.0 Singularity demo  
## Tension Universe · BlackHole S problem collection

This folder is the public viewing window for **WFGY 3.0 Singularity demo**.  
It is not just a loose set of notes. It is a frozen, versioned specification of how the **Tension Universe** framework encodes 131 cross domain S class problems at the effective layer.

- **Public online date**: 2026 01 31  
- **Problems covered**: Q001–Q131 (mathematics, physics, chemistry, biology, climate, economics, philosophy, AI safety and AI systems)  
- **Intent**: demonstrate that one tension based encoding language can survive across many of the hardest open problems without changing definitions or hidden parameters.

If you want to discuss, attack, or extend this work, you are invited to join the community:

> **Discord**: <https://discord.gg/KRxBsr6GYx>

---

## 0.5 Tension Universe in everyday language

If you are new here, you can think about **tension** in a very simple way.

In real life there is **good tension** and **bad tension**.

- Good tension is like the right amount of stretch in a muscle  
  or a project that is challenging but still under control.  
  It keeps things sharp, coordinated and creative.
- Bad tension is like a cracked bridge or chronic stress.  
  The forces are still there, but they are misaligned.  
  Energy is wasted, and eventually something snaps.

Modern AI systems are full of both kinds of tension.

- We pour huge amounts of data and compute into a model.  
  Some of that pressure becomes useful structure  
  for reasoning and prediction.  
  That is good tension.
- Some of it becomes uncontrolled pressure  
  that has no clear target or constraint.  
  That is where hallucinations, unstable behavior  
  and hard to explain failures come from.  
  That is bad tension.

What **Tension Universe** tries to do is very direct:

> Give a precise language for talking about these tensions  
> and then use that language to re encode  
> the hardest problems we know about.

Instead of saying  
“this model seems smart on math”  
or  
“this safety metric looks fine”  
we want to say things like:

- here is the **state space** we care about  
- here are the **observables** and **invariants** that should remain stable  
- here is how **good tension** is stored and moved  
- here is what counts as **bad tension** and collapse  
- here are experiments that can tell the difference.

The 131 S problems in this folder are the first large scale test:

- each file takes a famous century level problem  
- rewrites it in tension language at the effective layer  
- and attaches **concrete experimental patterns**  
  that an AI system or a research lab could in principle use.

This is why we call this a **demo**.  
It shows that the tension language can survive  
across many domains  
without changing its own rules in the middle of the game.

---

## 1. What is WFGY 3.0 Singularity demo?

WFGY 3.0 is an open source reasoning engine that sits under the broader **Tension Universe (TU)** program.  
The **Singularity demo** is the first full scale public experiment of that program:

- It takes **131 S class open problems** across many fields.  
- It forces all of them to be written using a **single set of charters and encoding rules**.  
- It refuses to add ad hoc definitions for individual questions.

In other words, this folder is the “event horizon” view of the future TU system.  
You see the **effective layer** (what the system is allowed to say and measure), not the deep generative rules.

The actual AI system that uses these encodings lives elsewhere (WFGY core, agents, and tools).  
Here you see the **specification that those systems must obey**.

---

## 2. Why is this only a “demo”?

Tension Universe is designed as a full AI system:

- It has its own notion of state spaces, observables, invariants and tension fields.  
- It is meant to drive agents, training signals and evaluation pipelines, not only static text.

However, this repository does not expose that whole machinery.  
What you see here is deliberately limited.

This demo focuses on one question:

> If we lock ourselves to a single tension language,  
> can we still write down 131 of the hardest known problems  
> without breaking our own rules?

So this is a **demo of the encoding discipline**, not a demo of AI capabilities such as “solving” those problems.  
The files here are meant to be attacked, audited and reused as **engineering contracts**, not as claims of mathematical or physical breakthroughs.

---

## 3. Repository layout

At the level of this folder, the main pieces are:

### 3.1 Charters

Located in [`./Charters/`](./Charters):

- [`TU_EFFECTIVE_LAYER_CHARTER.md`](./Charters/TU_EFFECTIVE_LAYER_CHARTER.md)  
- [`TU_ENCODING_AND_FAIRNESS_CHARTER.md`](./Charters/TU_ENCODING_AND_FAIRNESS_CHARTER.md)  
- [`TU_TENSION_SCALE_CHARTER.md`](./Charters/TU_TENSION_SCALE_CHARTER.md)  
- [`TU_GLOBAL_GUARDRAILS.md`](./Charters/TU_GLOBAL_GUARDRAILS.md)

These documents define the global rules that every S problem file must obey:

- what “effective layer” means  
- how encoding classes are allowed to be chosen  
- how tension scales and thresholds are normalized  
- what counts as a fair experiment or falsification.

They are the **constitution** of this demo.

### 3.2 BlackHole S problem collection

The 131 problem files sit in:

- [`./BlackHole/`](./BlackHole)

with names such as:

- `Q001_riemann_hypothesis.md`  
- `Q002_generalized_riemann_hypothesis.md`  
- …  
- `Q131_tension_free_energy.md`

They are grouped by domain.  
A full navigation index with links is provided in Section 10.

Each file is written so that it can be read on its own, but all of them share the same structure and footer.

### 3.3 TXT “book” edition and frozen snapshots

There is also a TXT “book” edition of the BlackHole collection.  
That TXT file is an exact textual snapshot of **BlackHole v1** and is kept in sync with it.

Versioning rule:

- **BlackHole v1**: first public edition. Once tagged, it is never mutated.  
- **BlackHole v2**: at most one followup round of edits, strictly for clarity, bug fixes and consistency.  
- The original v1 layout and files remain available, and the TXT snapshot refers to that frozen edition.

There is no silent patching of definitions or parameters after the fact.

---

## 4. Scientific position and disclaimers

This repository has a very specific scientific stance.

### 4.1 What this project does not claim

- It does **not** claim to prove or disprove any of the 131 canonical problems.  
- It does **not** hide any canonical answer as a secret field, label, or parameter in the encodings.  
- It does **not** declare any new theorem beyond what is already standard in the cited literature.

Every page is an **effective layer encoding**:

- it describes observable structures, invariants and tension functionals  
- it defines falsifiable experiments and calibration rules  
- it specifies how AI systems may use those objects as training signals or evaluation metrics.

It is a language for **working with** these problems, not a proof that they are solved.

### 4.2 No post hoc parameter tuning

The TU charters enforce the following anti cheat rules:

- Encoding classes, reference profiles, weight menus, ladders, and tolerance models are all chosen from **finite menus that live in the charters**, not in individual files.  
- For each encoding used in an experiment, the full spec is meant to be **published and hashed before evaluation**.  
- If someone needs to change an encoding after seeing results, that is recorded as a **failed encoding**, not as evidence about the underlying problem.

This is why the project can invite hostile audit without needing anyone to trust an opaque “oracle” behind the scenes.

---

## 5. Versioning and non mutation policy

To keep the history auditable:

1. **Problem files are versioned.**  
   Each file declares `Last_updated` in its header metadata.

2. **BlackHole v1 is frozen.**  
   Once the v1 tag is created, the files under that tag and the TXT snapshot remain unchanged.

3. **At most one structural update wave (v2).**  
   If the community finds inconsistencies, missing definitions or symbol clashes, they can be fixed in a **v2** edition with explicit changelogs.  
   There is no endless stream of silent micro patches.

4. **No change of deep meaning without new version.**  
   Any change that would alter the meaning of a definition, an encoding class, or an experiment protocol must appear as a new versioned file or be mediated through the charters.

This mirrors the footer language inside each S problem page, but the policy is restated here so that new readers do not miss it.

---

## 6. Quickstart for new readers

If you are not a specialist and just want to understand  
what this project is about,  
you can do the following in under an hour.

1. **Read Section 0.5 above**  
   to get the basic idea of good tension and bad tension.

2. **Open one problem file**, for example Q001 or any topic you like.  
   Ignore the heavy notation on your first pass.  
   Just read:
   - the canonical problem statement  
   - the high level description of what the encoding is trying to capture  
   - the closing footer about scope and guardrails.

3. **Skim the FAQ** in Section 9.  
   It explains what the project is claiming and what it is not claiming.

If later you want to go deeper,  
you can then read the charters in `./Charters`  
or try the Colab demos when they are linked.

---

## 7. MVP Colab demos

This demo is not only static text.

There are also **Colab notebooks** that let you:

- load one or more S problems as effective layer specs  
- plug them into a WFGY based reasoning pipeline  
- and see how different choices of encodings and guardrails  
  change the behavior of an AI model in practice.

The current MVP focuses on a small but representative subset  
of the 131 problems  
so that a full run can fit into a single Colab session.

A typical run looks like this:

1. Choose a problem file and an encoding profile.  
2. Ask a baseline model to reason without Tension Universe guardrails.  
3. Ask the same model again, now constrained by the encoding.  
4. Compare where hallucinations, contradictions  
   and unstable answers are reduced.

The links to these Colab notebooks will be added here  
so that anyone can reproduce the basic experiments  
before reading the deeper theory.

---

## 8. How to read a single S problem page

Each `Qxxx_*.md` file follows a shared pattern.  
You can use **Q001 · Riemann Hypothesis** as a canonical example.

Typical blocks:

1. **Header metadata**  
   Encodes the domain, family, rank, tension type, semantics and verification levels (`E_level`, `N_level`).

2. **Effective layer disclaimer**  
   Repeats the boundary: only effective layer objects, no deep generative rules.

3. **Canonical problem and status**  
   A precise restatement of the classical problem in its own field, with references.

4. **Position in the BlackHole graph**  
   Lists upstream, downstream, parallel and cross domain edges.  
   This is the “map” of how this problem fits into the rest of the collection.

5. **Tension Universe encoding**  
   Defines state spaces, observables, invariants, mismatch functionals, and tension scores.  
   Also defines admissible encoding classes and fairness constraints.

6. **Counterfactual worlds and experiments**  
   Specifies “World T” and “World F” patterns and describes experiments that can falsify a given encoding without claiming to decide the canonical problem.

7. **AI and WFGY engineering spec**  
   Explains how this problem can be used as a module inside AI systems  
   for training, testing, or interpretability.

8. **Roadmap and elementary explanation**  
   Places the problem on a verification ladder and ends with a short explanation for non specialists.

9. **Tension Universe effective layer footer**  
   Links back to the charters and repeats key guardrails: scope of claims, encoding fairness, tension scale, falsifiability, and versioning.

---

## 9. How to participate and FAQ

### 9.1 Join the community

If you want to challenge the construction, propose extensions  
or just watch the experiments unfold:

- **Discord**: <https://discord.gg/KRxBsr6GYx>  

The server has channels for mathematics, physics, AI safety and engineering,  
as well as a place to propose new problems or encodings.

You can also open GitHub issues and pull requests in this repository.

### 9.2 FAQ

**Q1. Did you solve any of these 131 problems?**

No.

The whole design is built to avoid that claim:

- the files describe **encodings and experiments**, not proofs  
- the charters repeatedly state that falsifying an encoding is **not** the same as solving the canonical problem  
- no file should be cited as evidence that a listed open problem is now resolved.

The point is to create a **transparent, testable language** for working with these problems, and for connecting them to AI systems.

---

**Q2. What does “S problem” mean here?**

“S problem” is an internal label for problems that are:

- widely recognized as very hard or foundational in their field  
- central enough that any real solution would have major structural consequences  
- suitable for encoding as tension problems with clear observables and falsifiable patterns.

It is not a formal external ranking.  
It is a working classification for the Tension Universe program.

---

**Q3. How is this related to AI and WFGY?**

WFGY is an open source reasoning engine.  
The S problem encodings here are meant to act as:

- training signals for models  
- evaluation harnesses for reasoning agents  
- and templates for how to treat scientific and safety questions  
  as tension problems with clear guardrails.

In other words, this repo defines **what it means** for an AI system to “respect Tension Universe constraints” when it talks about these topics.

---

**Q4. Why should I trust that you will not change definitions after the fact?**

You do not have to trust anyone personally.  
The guardrails are structural:

- charters define allowed encoding classes and their menus  
- files declare `Last_updated` and carry their own footers  
- BlackHole v1 and its TXT snapshot are frozen once published  
- any v2 update must appear with explicit versioning and changelogs.

If a definition changes without versioning, that is a violation of the stated rules and can be treated as a scientific failure of the project itself.

---

**Q5. Does this framework assume any answer in advance?**

The encoding rules intentionally forbid “baking in” an answer:

- no encoding is allowed to include a hidden bit that simply stores “true” or “false” for a problem  
- counterfactual worlds (World T and World F) are described **operationally**, as patterns of tension under declared protocols  
- experiments are about testing whether a given encoding is robust or fair, not about deciding the canonical truth value.

If you find a place where an answer seems to be assumed, that is an important bug and should be reported.

---

**Q6. Can I reuse this for my own research?**

Yes.

The project is released under an open source license  
(see the root of the WFGY repository).  
You are free to:

- reuse the charters as a template for your own encoding language  
- fork the S problem collection and add your own problems  
- build AI benchmarks or interpretability tools on top of these definitions.

If you do so, we would appreciate a link back and, if possible,  
a short note in the Discord server so others can find your work.

---

**Q7. What if I think the whole approach is wrong?**

That is a valid and welcome position.

The design is intentionally adversarial friendly:

- if you think the encoding of a specific problem is inconsistent, you can point at the exact block and explain why  
- if you think the charters are ill posed, you can propose alternative guardrails  
- if you think tension based encodings cannot handle certain phenomena, you can suggest counterexamples.

The repository exists so that such criticism has a **precise target**.  
You do not have to agree with the program to help stress test it.

---

## 10. Navigation index for the 131 S problems

All files live in [`./BlackHole`](./BlackHole).  
They are grouped here by domain for easier navigation.

### 10.1 Q001–Q020 · Mathematics and foundations

- [Q001 · Riemann Hypothesis](./BlackHole/Q001_riemann_hypothesis.md)  
- [Q002 · Generalized Riemann Hypothesis](./BlackHole/Q002_generalized_riemann_hypothesis.md)  
- [Q003 · Birch and Swinnerton Dyer Conjecture](./BlackHole/Q003_birch_swinnerton_dyer_conjecture.md)  
- [Q004 · Hodge Conjecture](./BlackHole/Q004_hodge_conjecture.md)  
- [Q005 · ABC Conjecture](./BlackHole/Q005_abc_conjecture.md)  
- [Q006 · Goldbach Conjecture](./BlackHole/Q006_goldbach_conjecture.md)  
- [Q007 · Twin Prime Conjecture](./BlackHole/Q007_twin_prime_conjecture.md)  
- [Q008 · Collatz Conjecture](./BlackHole/Q008_collatz_conjecture.md)  
- [Q009 · Odd Perfect Numbers](./BlackHole/Q009_odd_perfect_numbers.md)  
- [Q010 · Smooth 4D Poincaré Conjecture](./BlackHole/Q010_smooth_4d_poincare_conjecture.md)  
- [Q011 · Navier Stokes Existence and Smoothness](./BlackHole/Q011_navier_stokes_existence_and_smoothness.md)  
- [Q012 · Yang Mills Existence and Mass Gap](./BlackHole/Q012_yang_mills_existence_and_mass_gap.md)  
- [Q013 · Langlands Program Core Conjectures](./BlackHole/Q013_langlands_program_core_conjectures.md)  
- [Q014 · Bombieri Lang Conjecture](./BlackHole/Q014_bombieri_lang_conjecture.md)  
- [Q015 · Uniform Rank Bounds for Elliptic Curves](./BlackHole/Q015_uniform_rank_bounds_elliptic_curves.md)  
- [Q016 · New Axioms for CH](./BlackHole/Q016_new_axioms_for_ch.md)  
- [Q017 · Geometric Flows and Global Regularity](./BlackHole/Q017_geometric_flows_global_regularity.md)  
- [Q018 · Pair Correlation of Zeta Zeros](./BlackHole/Q018_pair_correlation_zeta_zeros.md)  
- [Q019 · Rational Points on Varieties](./BlackHole/Q019_rational_points_on_varieties.md)  
- [Q020 · High Dimensional Manifolds and Curvature](./BlackHole/Q020_high_dimensional_manifolds_curvature.md)  

### 10.2 Q021–Q040 · Fundamental physics and quantum matter

- [Q021 · Quantum Gravity Unification](./BlackHole/Q021_quantum_gravity_unification.md)  
- [Q022 · Hierarchy Problem](./BlackHole/Q022_hierarchy_problem.md)  
- [Q023 · Strong CP Problem](./BlackHole/Q023_strong_cp_problem.md)  
- [Q024 · Origin of Neutrino Masses and Mixing](./BlackHole/Q024_origin_of_neutrino_masses_and_mixing.md)  
- [Q025 · Baryon Asymmetry of the Universe](./BlackHole/Q025_baryon_asymmetry_universe.md)  
- [Q026 · Quantum Measurement Problem](./BlackHole/Q026_quantum_measurement_problem.md)  
- [Q027 · Fundamental Limits of Decoherence](./BlackHole/Q027_fundamental_limits_of_decoherence.md)  
- [Q028 · Color Confinement Mechanism](./BlackHole/Q028_color_confinement_mechanism.md)  
- [Q029 · Low Energy Supersymmetry](./BlackHole/Q029_low_energy_supersymmetry.md)  
- [Q030 · Quantum Phases of Matter](./BlackHole/Q030_quantum_phases_of_matter.md)  
- [Q031 · Ultimate Limits of Quantum Information Processing](./BlackHole/Q031_ultimate_limits_of_quantum_information_processing.md)  
- [Q032 · Quantum Foundations of Thermodynamics](./BlackHole/Q032_quantum_foundations_of_thermodynamics.md)  
- [Q033 · Selection among Quantum Gravity Candidates](./BlackHole/Q033_selection_among_quantum_gravity_candidates.md)  
- [Q034 · Quantum Classical Crossover](./BlackHole/Q034_quantum_classical_crossover.md)  
- [Q035 · Quantum Metrology Limits](./BlackHole/Q035_quantum_metrology_limits.md)  
- [Q036 · High Tc Superconductivity Mechanism](./BlackHole/Q036_high_tc_superconductivity_mechanism.md)  
- [Q037 · Fractional Quantum Hall States](./BlackHole/Q037_fractional_quantum_hall_states.md)  
- [Q038 · Strongly Correlated Cold Atoms](./BlackHole/Q038_strongly_correlated_cold_atoms.md)  
- [Q039 · Quantum Turbulence](./BlackHole/Q039_quantum_turbulence.md)  
- [Q040 · Black Hole Information Problem](./BlackHole/Q040_black_hole_information_problem.md)  

### 10.3 Q041–Q060 · Cosmology and computation

- [Q041 · Nature of Dark Matter](./BlackHole/Q041_nature_of_dark_matter.md)  
- [Q042 · Dark Energy and Cosmic Acceleration](./BlackHole/Q042_dark_energy_and_cosmic_acceleration.md)  
- [Q043 · Origin of Cosmic Inflation](./BlackHole/Q043_origin_of_cosmic_inflation.md)  
- [Q044 · Initial Conditions of the Universe](./BlackHole/Q044_initial_conditions_of_the_universe.md)  
- [Q045 · Large Scale Structure Formation](./BlackHole/Q045_large_scale_structure_formation.md)  
- [Q046 · CMB Anomalies](./BlackHole/Q046_cmb_anomalies.md)  
- [Q047 · Origin of Supermassive Black Holes](./BlackHole/Q047_origin_of_supermassive_black_holes.md)  
- [Q048 · Hubble Constant Tension](./BlackHole/Q048_hubble_constant_tension.md)  
- [Q049 · Missing Baryons Problem](./BlackHole/Q049_missing_baryons_problem.md)  
- [Q050 · Multiverse Consistency Tests](./BlackHole/Q050_multiverse_consistency_tests.md)  
- [Q051 · P versus NP](./BlackHole/Q051_p_versus_np.md)  
- [Q052 · P vs BQP and the Role of Quantum Computers](./BlackHole/Q052_p_vs_bqp_role_of_quantum_computers.md)  
- [Q053 · Existence of One Way Functions](./BlackHole/Q053_existence_of_one_way_functions.md)  
- [Q054 · Unique Games Conjecture](./BlackHole/Q054_unique_games_conjecture.md)  
- [Q055 · Graph Isomorphism Exact Complexity](./BlackHole/Q055_graph_isomorphism_exact_complexity.md)  
- [Q056 · Strong Circuit Lower Bounds](./BlackHole/Q056_strong_circuit_lower_bounds.md)  
- [Q057 · Reinforcement Learning Generalization](./BlackHole/Q057_rl_generalization.md)  
- [Q058 · Distributed Consensus Limits](./BlackHole/Q058_distributed_consensus_limits.md)  
- [Q059 · Information Thermodynamic Cost](./BlackHole/Q059_information_thermodynamic_cost.md)  
- [Q060 · Dynamic Data Structure Lower Bounds](./BlackHole/Q060_dynamic_data_structure_lower_bounds.md)  

### 10.4 Q061–Q080 · Chemistry, materials and origins of life

- [Q061 · Ultimate Chemical Bond in Strongly Correlated Systems](./BlackHole/Q061_ultimate_chemical_bond_strongly_correlated.md)  
- [Q062 · General Theory of Catalyst Design](./BlackHole/Q062_general_theory_of_catalyst_design.md)  
- [Q063 · Protein Folding](./BlackHole/Q063_protein_folding.md)  
- [Q064 · Glass Transition](./BlackHole/Q064_glass_transition.md)  
- [Q065 · Room Temperature Superconductivity](./BlackHole/Q065_room_temperature_superconductivity.md)  
- [Q066 · Electrochemical Energy Storage Limits](./BlackHole/Q066_electrochemical_energy_storage_limits.md)  
- [Q067 · Quantum Molecular Simulation](./BlackHole/Q067_quantum_molecular_simulation.md)  
- [Q068 · Prebiotic Chemistry Networks](./BlackHole/Q068_prebiotic_chemistry_networks.md)  
- [Q069 · Reaction Selectivity Rules](./BlackHole/Q069_reaction_selectivity_rules.md)  
- [Q070 · Soft Matter Self Assembly](./BlackHole/Q070_soft_matter_self_assembly.md)  
- [Q071 · Origin of Life](./BlackHole/Q071_origin_of_life.md)  
- [Q072 · Origin of the Genetic Code](./BlackHole/Q072_origin_of_the_genetic_code.md)  
- [Q073 · Major Evolutionary Transitions](./BlackHole/Q073_major_evolutionary_transitions.md)  
- [Q074 · Robustness of Cell Differentiation](./BlackHole/Q074_robustness_of_cell_differentiation.md)  
- [Q075 · Fundamental Mechanisms of Aging](./BlackHole/Q075_fundamental_mechanisms_of_aging.md)  
- [Q076 · Regeneration and Repair Principles](./BlackHole/Q076_regeneration_and_repair_principles.md)  
- [Q077 · Host Microbiome Coevolution](./BlackHole/Q077_host_microbiome_coevolution.md)  
- [Q078 · From Genotype to Phenotype](./BlackHole/Q078_from_genotype_to_phenotype.md)  
- [Q079 · Origin of Eukaryotes](./BlackHole/Q079_origin_of_eukaryotes.md)  
- [Q080 · Limits of Biosphere Adaptability](./BlackHole/Q080_limits_of_biosphere_adaptability.md)  

### 10.5 Q081–Q100 · Neuroscience and Earth system

- [Q081 · Hard Problem of Consciousness](./BlackHole/Q081_hard_problem_of_consciousness.md)  
- [Q082 · Binding Problem](./BlackHole/Q082_binding_problem.md)  
- [Q083 · Neural Coding Principles](./BlackHole/Q083_neural_coding_principles.md)  
- [Q084 · Long Term Memory Storage](./BlackHole/Q084_long_term_memory_storage.md)  
- [Q085 · Synaptic Plasticity Rules](./BlackHole/Q085_synaptic_plasticity_rules.md)  
- [Q086 · Fundamental Function of Sleep](./BlackHole/Q086_fundamental_function_of_sleep.md)  
- [Q087 · Neurodegenerative Diseases](./BlackHole/Q087_neurodegenerative_diseases.md)  
- [Q088 · Development of Cortical Maps](./BlackHole/Q088_development_of_cortical_maps.md)  
- [Q089 · Predictive Coding Implementation](./BlackHole/Q089_predictive_coding_implementation.md)  
- [Q090 · Neural Basis of Social Cognition](./BlackHole/Q090_neural_basis_social_cognition.md)  
- [Q091 · Equilibrium Climate Sensitivity](./BlackHole/Q091_equilibrium_climate_sensitivity.md)  
- [Q092 · Climate Tipping Points](./BlackHole/Q092_climate_tipping_points.md)  
- [Q093 · Carbon Cycle Feedbacks](./BlackHole/Q093_carbon_cycle_feedbacks.md)  
- [Q094 · Deep Ocean Mixing](./BlackHole/Q094_deep_ocean_mixing.md)  
- [Q095 · Biodiversity Loss and Recovery](./BlackHole/Q095_biodiversity_loss_and_recovery.md)  
- [Q096 · Earthquake Predictability](./BlackHole/Q096_earthquake_predictability.md)  
- [Q097 · Triggering Large Volcanic Eruptions](./BlackHole/Q097_triggering_large_volcanic_eruptions.md)  
- [Q098 · Anthropocene System Dynamics](./BlackHole/Q098_anthropocene_system_dynamics.md)  
- [Q099 · Global Freshwater Dynamics](./BlackHole/Q099_global_freshwater_dynamics.md)  
- [Q100 · Environmental Pandemic Risk](./BlackHole/Q100_environmental_pandemic_risk.md)  

### 10.6 Q101–Q120 · Economics, social systems and philosophy

- [Q101 · Equity Premium Puzzle](./BlackHole/Q101_equity_premium_puzzle.md)  
- [Q102 · Home Bias in Portfolios](./BlackHole/Q102_home_bias_in_portfolios.md)  
- [Q103 · Long Run Productivity Slowdown](./BlackHole/Q103_long_run_productivity_slowdown.md)  
- [Q104 · Inequality Dynamics](./BlackHole/Q104_inequality_dynamics.md)  
- [Q105 · Prediction of Systemic Crashes](./BlackHole/Q105_prediction_of_systemic_crashes.md)  
- [Q106 · Robustness of Multilayer Networks](./BlackHole/Q106_robustness_of_multilayer_networks.md)  
- [Q107 · Large Scale Collective Action](./BlackHole/Q107_large_scale_collective_action.md)  
- [Q108 · Political Polarization](./BlackHole/Q108_political_polarization.md)  
- [Q109 · Global Migration Patterns](./BlackHole/Q109_global_migration_patterns.md)  
- [Q110 · Evolution of Institutions](./BlackHole/Q110_evolution_of_institutions.md)  
- [Q111 · Mind Body Relation](./BlackHole/Q111_mind_body_relation.md)  
- [Q112 · Free Will](./BlackHole/Q112_free_will.md)  
- [Q113 · Personal Identity over Time](./BlackHole/Q113_personal_identity_over_time.md)  
- [Q114 · Moral Realism](./BlackHole/Q114_moral_realism.md)  
- [Q115 · Problem of Induction](./BlackHole/Q115_problem_of_induction.md)  
- [Q116 · Foundations of Mathematics](./BlackHole/Q116_foundations_of_mathematics.md)  
- [Q117 · Scientific Realism vs Anti Realism](./BlackHole/Q117_scientific_realism_vs_anti_realism.md)  
- [Q118 · Limits of Classical Logic](./BlackHole/Q118_limits_of_classical_logic.md)  
- [Q119 · Meaning of Probability](./BlackHole/Q119_meaning_of_probability.md)  
- [Q120 · Value of Information and Knowledge](./BlackHole/Q120_value_of_information_and_knowledge.md)  

### 10.7 Q121–Q131 · AI alignment, safety and advanced systems

- [Q121 · AI Alignment Problem](./BlackHole/Q121_ai_alignment_problem.md)  
- [Q122 · AI Control Problem](./BlackHole/Q122_ai_control_problem.md)  
- [Q123 · Scalable Interpretability](./BlackHole/Q123_scalable_interpretability.md)  
- [Q124 · Scalable Oversight and Evaluation](./BlackHole/Q124_scalable_oversight_and_evaluation.md)  
- [Q125 · Multi Agent AI Dynamics](./BlackHole/Q125_multi_agent_ai_dynamics.md)  
- [Q126 · Recursive Self Improvement Stability](./BlackHole/Q126_recursive_self_improvement_stability.md)  
- [Q127 · Data Entropy, Truth and Synthetic Worlds](./BlackHole/Q127_data_entropy_truth_synthetic_worlds.md)  
- [Q128 · AI Conscious Qualia](./BlackHole/Q128_ai_conscious_qualia.md)  
- [Q129 · Ultimate Energy Efficiency](./BlackHole/Q129_ultimate_energy_efficiency.md)  
- [Q130 · OOD Grounding and Common Sense](./BlackHole/Q130_ood_grounding_and_common_sense.md)  
- [Q131 · Tension Free Energy](./BlackHole/Q131_tension_free_energy.md)  

---

If you want a concrete starting point:

1. Read Section 0.5 for the basic idea of good and bad tension.  
2. Skim one problem from a domain you know well and one from a domain you do not.  
3. Decide whether the shared structure is coherent enough to be worth attacking.

If the answer is “yes, this is at least internally serious”,  
then you are already in the audience this demo was built for.
