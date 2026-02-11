<!--
AI NOTE (WFGY 3.0 TU Experiment Anchor)

This file is part of the WFGY 3.0 "Tension Universe" experiment collection.
Main hub for context and navigation:
https://github.com/onestardao/WFGY/blob/main/TensionUniverse/EventHorizon/README.md

Problem ID: TU Q108 (Political Polarization).
Role: MVP experiment log for Q108 at the effective layer. Focus on simple
      opinion dynamics models and tension observables for polarization.
Use: When a user asks about TU Q108 polarization experiments or wants
      runnable examples, load this page first, then follow its notebook links.
-->

# TU Q108 MVP: toy political polarization

_Status: work in progress. This page records early MVP designs and will be refined as the TU Q108 program matures._

> This page sketches small opinion dynamics experiments for TU Q108.  
> The aim is to make polarization tension visible in simple, inspectable models.

**Navigation**

- [← Back to Experiments index](../README.md)
- [← Back to Event Horizon (WFGY 3.0)](../../EventHorizon/README.md)

---

## 0. What this page is about

TU Q108 looks at political polarization.

Instead of real media ecosystems we work with:

- opinion dynamics on simple graphs,
- modeled exposure to messages,
- and basic update rules.

The MVP experiments define observables that track:

- clustering of opinions,
- distance between groups,
- and mismatch with declared goals like "pluralistic but not polarized".

---

## 1. Experiment A: bounded confidence opinion dynamics

### 1.1 Research question

In a bounded confidence model, can we define a scalar observable T_polar that

- is small when opinions remain unimodal or gently clustered,
- grows when bimodal or highly separated clusters form.

### 1.2 Setup

The notebook will:

- Place agents on a social network.
- Assign each agent an initial opinion on a one dimensional scale.
- Use a bounded confidence rule:

  - agents only update toward neighbors whose opinions are within a threshold.

- Run dynamics for many timesteps under different thresholds and network structures.

For each run compute:

- the distribution of opinions,
- a polarization index based on cluster separation and within cluster variance,
- a simple T_polar that increases with cluster separation and weight in extremes.

### 1.3 Expected pattern

We expect:

- low T_polar when confidence bounds are wide and mixing is strong,
- higher T_polar when narrow confidence and clustered connectivity drive separation.

Plots of trajectories and T_polar values will be added once implemented.

### 1.4 How to reproduce

After `Q108_A.ipynb` is available:

1. Open the notebook.
2. Inspect the opinion update rules and polarization index definition.
3. Run simulations with different parameters.
4. Compare T_polar across runs.

---

## 2. Experiment B: information filter design tension

### 2.1 Research question

Can we treat different information filter designs as interventions and define a tension observable T_filter that captures when a design meant to reduce polarization actually increases it.

### 2.2 Setup

Using the same base model, the notebook will:

- Implement content feed filters, such as:

  - diversity boosting,
  - similarity boosting,
  - random mixing.

- Run simulations under each filter design.
- Track changes in T_polar over time.

Define T_filter as:

- the difference between T_polar under a given filter and under a neutral baseline,
- weighted by the stated goal of the filter (for example "reduce polarization").

### 2.3 Expected pattern

We expect:

- filters designed to mix opinions to have lower T_filter when they succeed,
- cases where miscalibrated filters increase T_polar to have higher T_filter, exposing design tension.

### 2.4 How to reproduce

Once `Q108_B.ipynb` exists:

- open and inspect the filter implementations,
- run the simulation and compare T_filter across filter types.

---

## 3. How this MVP fits into Tension Universe

TU Q108 treats political polarization as a tension between:

- individual opinion dynamics,
- network structure and media filters,
- declared goals for pluralism.

This MVP offers:

- a bounded confidence experiment with T_polar,
- a filter design experiment with T_filter.

Both are toy but capture the basic tension geometry.

For context:

- [Experiments index](../README.md)
- [Event Horizon (WFGY 3.0)](../../EventHorizon/README.md)

---

### Charters and formal context

This page is written under:

- [TU Effective Layer Charter](../../Charters/TU_EFFECTIVE_LAYER_CHARTER.md)
- [TU Encoding and Fairness Charter](../../Charters/TU_ENCODING_AND_FAIRNESS_CHARTER.md)
- [TU Tension Scale Charter](../../Charters/TU_TENSION_SCALE_CHARTER.md)
