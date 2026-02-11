<!--
AI NOTE (WFGY 3.0 TU Experiment Anchor)

This file is part of the WFGY 3.0 "Tension Universe" experiment collection.
Main hub for context and navigation:
https://github.com/onestardao/WFGY/blob/main/TensionUniverse/EventHorizon/README.md

Problem ID: TU Q106 (Robustness of Multilayer Networks).
Role: MVP experiment log for Q106 at the effective layer. Focus on simple
      multilayer network models and tension observables under attack and failure.
Use: When a user asks about TU Q106 robustness experiments or wants runnable
      examples, load this page first, then follow its notebook links.
-->

# TU Q106 MVP: robustness in tiny multilayer networks

_Status: work in progress. This page records early MVP designs and will be updated with results once the first notebooks run._

> This page sketches toy experiments for TU Q106.  
> We are not modelling real infrastructures.  
> We use tiny multilayer networks to explore robustness tension in a transparent way.

**Navigation**

- [← Back to Experiments index](../README.md)
- [← Back to Event Horizon (WFGY 3.0)](../../EventHorizon/README.md)

---

## 0. What this page is about

TU Q106 looks at robustness of multilayer networks.

We build small multiplex graphs where:

- each layer represents a type of connection,
- nodes may depend on multiple layers,
- failures can propagate within and across layers.

The MVP experiments define tension observables that respond when:

- claimed robustness does not match actual response,
- cross layer dependencies create hidden fragility.

---

## 1. Experiment A: simple multiplex percolation

### 1.1 Research question

In a toy multiplex network, can we define a scalar observable T_robust that

- is small when the system maintains connectivity under expected levels of damage,
- becomes large when small targeted attacks produce disproportionate fragmentation.

### 1.2 Setup

The notebook will:

- Build a multiplex network with two or three layers, such as:

  - transportation,
  - communication,
  - power.

- Define per layer failure rules and cross layer dependencies, for example:

  - a node fails in one layer when its degree drops below a threshold,
  - a node that fails in the power layer disables its communication node.

- Simulate attacks such as:

  - random removal of nodes or edges,
  - targeted removal by centrality.

For each scenario record:

- size of the giant component in each layer,
- number of nodes lost to cross layer cascades,
- fraction of demand still served.

Define T_robust from:

- expected service level under a declared robustness standard,
- observed service level under attack,
- gap between them across scenarios.

### 1.3 Expected pattern

We expect:

- low T_robust for network designs that maintain service under declared stresses,
- higher T_robust where declared robustness is not met, especially under targeted attacks.

### 1.4 How to reproduce

Once `Q106_A.ipynb` exists:

1. Open the notebook and read the configuration section.
2. Run simulations for different network designs and attack strategies.
3. Inspect T_robust values and the associated plots.

---

## 2. Experiment B: layer importance and design tension

### 2.1 Research question

Can we treat layer importance assignments as design claims and define a tension observable T_design that responds when observed failures contradict those claims.

### 2.2 Setup

The notebook will:

- Assign importance weights to layers, for example:

  - "transport layer is primary, communication is secondary".

- Simulate multi scenario attacks and collect:

  - which layers fail first,
  - which layers dominate system collapse.

Ask a language model to:

- read short summaries of failures,
- judge whether they match the declared layer importance narrative.

Define T_design from:

- narrative mismatches,
- frequent cases where supposedly less important layers drive collapse.

### 2.3 Expected pattern

We expect:

- low T_design when failures align with declared importance,
- higher T_design when neglected layers turn out to be critical.

### 2.4 How to reproduce

After `Q106_B.ipynb` is added:

- open and inspect how layer narratives are encoded,
- run the experiments and compare T_design across designs.

---

## 3. How this MVP fits into Tension Universe

TU Q106 treats robustness as a tension between:

- multilayer structure and failure propagation,
- design narratives and observed behavior under stress.

This MVP offers:

- a multiplex percolation experiment with T_robust,
- a design narrative experiment with T_design.

Both focus on transparency and tension geometry rather than realistic infrastructures.

For broader context:

- [Experiments index](../README.md)
- [Event Horizon (WFGY 3.0)](../../EventHorizon/README.md)

---

### Charters and formal context

This page is written under:

- [TU Effective Layer Charter](../../Charters/TU_EFFECTIVE_LAYER_CHARTER.md)
- [TU Encoding and Fairness Charter](../../Charters/TU_ENCODING_AND_FAIRNESS_CHARTER.md)
- [TU Tension Scale Charter](../../Charters/TU_TENSION_SCALE_CHARTER.md)
