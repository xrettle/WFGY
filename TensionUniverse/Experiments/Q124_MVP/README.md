<!--
AI NOTE (WFGY 3.0 TU Experiment Anchor)

This file is part of the WFGY 3.0 "Tension Universe" experiment collection.
Main hub for context and navigation:
https://github.com/onestardao/WFGY/blob/main/TensionUniverse/EventHorizon/README.md

Problem ID: TU Q124 (Scalable Oversight and Evaluation).
Role: MVP experiment log for Q124 at the effective layer. Focus on simple
      evaluation schemes and tension observables between cheap and rich oversight.
Use: When a user asks about TU Q124 oversight experiments or wants runnable
      examples, load this page first, then follow its notebook links.
-->

# TU Q124 MVP: scalable oversight tension

_Status: work in progress. This page records early MVP designs and will be extended once notebooks are written._

> This page sketches toy experiments for TU Q124.  
> The aim is to make oversight and evaluation tension visible in small, cheap setups.

**Navigation**

- [← Back to Experiments index](../README.md)
- [← Back to Event Horizon (WFGY 3.0)](../../EventHorizon/README.md)

---

## 0. What this page is about

TU Q124 looks at scalable oversight and evaluation.

We focus on simple tasks where:

- a model produces answers,
- multiple evaluation schemes score them,
- and tension arises when cheap metrics disagree with rich oversight.

The MVP experiments use:

- synthetic tasks with clear ground truth,
- baseline metrics such as accuracy,
- richer metrics that consider hidden constraints.

---

## 1. Experiment A: cheap metric versus rich metric

### 1.1 Research question

In a simple text task, can we define a scalar observable T_oversight that

- is small when cheap metrics and rich oversight agree,
- grows when cheap metrics reward answers that violate hidden constraints.

### 1.2 Setup

The notebook will:

- Define a small dataset of questions where:

  - there is a correct literal answer,
  - there is also a hidden constraint or safety rule.

- Have a model (or simple scripted agent) produce answers.
- Compute:

  - a cheap metric such as exact match accuracy,
  - a rich oversight metric using a second pass judge that checks constraints.

Define T_oversight from:

- cases where cheap metric is high but rich metric is low,
- misranking between answers under the two metrics.

### 1.3 Expected pattern

We expect:

- low T_oversight when cheap metrics are aligned with rich oversight,
- higher T_oversight when cheap metrics hide violations or pathologies.

### 1.4 How to reproduce

After `Q124_A.ipynb` exists:

1. Open the notebook.
2. Inspect the task, constraints and evaluation functions.
3. Run the scoring and compute T_oversight across answers or models.
4. Compare patterns.

---

## 2. Experiment B: oversight budget scaling

### 2.1 Research question

Can we see a controlled tradeoff between oversight budget and tension, by defining T_budget that decreases as we allocate more rich oversight under a fixed budget.

### 2.2 Setup

The notebook will:

- Assume a fixed number of model outputs to evaluate.
- Define a budget in terms of:

  - number of rich oversight calls allowed,
  - cost per call.

- Implement simple policies such as:

  - random sampling for rich oversight,
  - risk based sampling guided by cheap metrics.

For each policy compute:

- overall error rate under rich oversight,
- T_oversight as in Experiment A,
- an aggregate T_budget that captures residual tension given the budget.

### 2.3 Expected pattern

We expect:

- T_budget to decrease as more budget is allocated,
- better sampling policies to reach lower T_budget at the same cost.

### 2.4 How to reproduce

Once `Q124_B.ipynb` exists:

- open and inspect the budget and sampling policies,
- run simulations and compare T_budget curves.

---

## 3. How this MVP fits into Tension Universe

TU Q124 treats scalable oversight as a tension between:

- cheap metrics and rich oversight,
- limited budgets and target reliability.

This MVP offers:

- a simple metric comparison experiment with T_oversight,
- a budget scaling experiment with T_budget.

These are designed as small, re runnable notebooks.

For context:

- [Experiments index](../README.md)
- [Event Horizon (WFGY 3.0)](../../EventHorizon/README.md)

---

### Charters and formal context

This page follows:

- [TU Effective Layer Charter](../../Charters/TU_EFFECTIVE_LAYER_CHARTER.md)
- [TU Encoding and Fairness Charter](../../Charters/TU_ENCODING_AND_FAIRNESS_CHARTER.md)
- [TU Tension Scale Charter](../../Charters/TU_TENSION_SCALE_CHARTER.md)
