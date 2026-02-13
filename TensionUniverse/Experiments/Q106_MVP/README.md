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

_Status: Experiment A implemented (fully offline, one-cell Colab).  
Experiment B is planned and not yet implemented._

> This page documents toy experiments for TU Q106.  
> We are not modelling real infrastructures.  
> We use tiny multilayer networks so that robustness tension is visible,
> auditable, and easy to re-run.

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

- claimed robustness does not match actual behavior under stress,
- cross-layer dependencies create hidden fragility that only appears
  under certain attack patterns.

Experiment A is a complete, runnable percolation-style experiment.  
Experiment B is a planned extension for narrative-level design tension.

---

## 1. Experiment A: simple multiplex percolation

### 1.1 Research question

In a toy multiplex network, can we define a scalar robustness tension `T_robust` that

- stays small when the system maintains service under declared damage levels,
- becomes large when small targeted attacks trigger disproportionate cascades,
- cleanly separates two design philosophies:
  - one that is genuinely robust,
  - one that collapses once the attack becomes slightly smarter?

The goal is a one-button experiment where this contrast is obvious from:

- a single aggregated summary table printed in the notebook output, and
- two figures that anyone can regenerate.

---

### 1.2 Notebook and one-button run

- **Notebook file**: `Q106_A.ipynb` (in this folder)
- **Environment**: pure Python, fully offline  
  uses `numpy`, `pandas`, `networkx`, `matplotlib`.

Open in Colab:

 [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/onestardao/WFGY/blob/main/TensionUniverse/Experiments/Q106_MVP/Q106_A.ipynb)

The notebook is written as a **single cell**:

1. Open the notebook.
2. Run the only code cell once.
3. The cell will:

   - construct two tiny multilayer network designs (R and F),
   - run random and targeted attack scenarios at three damage levels,
   - propagate cross-layer cascades until they stabilize,
   - compute all observables and aggregate statistics,
   - print an aggregated summary table plus the design-level `T_robust`,
   - save two PNG figures in this directory.

No API keys are required. Everything is self-contained.

---

### 1.3 Model: two-layer multiplex and two designs

We use a fixed small world:

- `N = 200` nodes per layer,
- two layers:

  - a **power** layer,
  - a **communication** layer,

- both layers share the same node set.

We then build two contrasting designs: a robust one and a fragile one.

#### Design R: robust style

- Both layers are Erdos–Renyi graphs with moderate edge probability
  (around 0.035).
- Degrees are spread across nodes; no single node has extreme centrality.
- Intuition: load and connectivity are reasonably diversified.  
  Removing a few nodes does not immediately cut the graph into pieces.

#### Design F: fragile style

- Both layers are hub-and-spoke style graphs:

  - pick a small set of hub nodes (for example 5),
  - connect hubs densely among themselves,
  - connect every non-hub to one or two hubs,
  - add only a small number of extra leaf-to-leaf edges.

- Intuition: the network looks very efficient when hubs are present.  
  But once a hub is removed, large parts of the network have no alternative
  paths.

Both designs are strictly toy models. The point is not realism.  
The point is to create a small world where:

- random failures look acceptable for both designs, but
- targeted failures expose a large hidden difference.

---

### 1.4 Failure rules and cross-layer cascades

Each layer has a simple internal failure rule. Cross-layer rules then decide
whether a node survives as a multi-layer service point.

#### Layer-internal rule

Given a set of currently alive nodes in a layer:

1. Take the subgraph induced by those nodes.
2. Find the largest connected component (giant component).
3. A node is marked “failed in this layer” if:

   - it is not in the largest component, or
   - its degree in the alive subgraph is less than a minimum degree
     (currently 1 for both layers).

This approximates the idea that:

- isolated nodes and tiny fragments cannot meaningfully provide service,
- extremely low degree nodes are too weakly connected to be considered
  functional.

#### Cross-layer cascade rule

After we mark layer-specific failures, we decide which nodes are removed from
the entire multi-layer system.

- **Design R (conservative cascade)**

  - A node is removed only if it fails in **both** layers  
    (logical AND on layer failures).

- **Design F (aggressive cascade)**

  - A node is removed if it fails in **either** layer  
    (logical OR on layer failures).

We apply the internal rule and the cascade rule iteratively:

1. Start from the node set after the initial attack.
2. Compute layer failures and cross-layer removals.
3. If any new nodes are removed, update the alive set and repeat.
4. Stop when the set of alive nodes no longer changes.

This defines the cascade engine.  
Once the initial attack set is chosen, the cascade is deterministic.

---

### 1.5 Attack scenarios

We vary both **how** we attack and **how much** we remove.

#### Attack types

- `random`

  - sample a fraction of nodes uniformly at random,
  - remove them from both layers simultaneously.

- `targeted`

  - compute node degrees in the **power** layer,
  - sort nodes by degree,
  - remove the top nodes until the desired fraction is reached.

Targeted attack is a simple proxy for an intelligent adversary that
deliberately hits hubs.

#### Damage levels

For each attack type we consider three damage fractions:

- `0.05`  (5 percent of nodes),
- `0.10`  (10 percent),
- `0.20`  (20 percent).

For every combination

- design ∈ {R, F}
- attack_type ∈ {random, targeted}
- attack_fraction ∈ {0.05, 0.10, 0.20}

we run several independent trials with different random seeds.  
The notebook aggregates these into mean and standard deviation.

---

### 1.6 Observables and robustness tension T_robust

For each run we track:

- `S_power_final`  
  fraction of nodes in the giant component of the power layer after cascades.

- `S_comm_final`  
  fraction of nodes in the giant component of the communication layer after
  cascades.

- `S_multi_final`  
  fraction of nodes that are **simultaneously** in the giant component of both
  layers. This is the effective multi-layer service level.

- `initial_removed_fraction`  
  fraction of nodes removed by the attack itself.

- `cascade_removed_fraction`  
  additional fraction of nodes removed only by the cascade logic.

We then aggregate by `(design, attack_type, attack_fraction)` to obtain:

- means and standard deviations for all the above quantities.

The aggregated summary table printed in the notebook output is exactly this
per-design, per-scenario view.

#### Declared robustness standard

We encode a simple “robustness promise” as a function of attack level:

- up to 5 percent damage: keep service at or above `S_target = 0.80`
- up to 10 percent damage: keep service at or above `S_target = 0.60`
- up to 20 percent damage: keep service at or above `S_target = 0.40`

For each scenario we compute a violation:

- let `S_multi_mean` be the mean `S_multi_final` for the scenario,
- `violation = max(S_target − S_multi_mean, 0)`.

If the design meets or exceeds the declared target, violation is zero.
Otherwise, the shortfall is counted as positive tension.

#### Design-level robustness tension

For each design we average violations over all six scenarios:

- `T_robust` is the mean violation across
  3 attack fractions × 2 attack types.

Interpretation:

- `T_robust = 0.0` means the design meets its own robustness standard
  in every tested scenario.
- Larger `T_robust` values indicate designs that regularly fail to deliver
  the level of service they claim.

The notebook prints this small `T_robust` table at the end of the run.

---

### 1.7 Files and figures produced by Experiment A

When you run the notebook, Experiment A currently produces two files in
this folder:

- `Q106A.png`  
  Summary plot for service vs attack.  
  This figure has two panels:

  - left: random attacks  
    lines for `S_multi` as a function of attack_fraction for Design R and
    Design F, with error bars.
  - right: targeted attacks  
    same plotting style, but for smart attacks that hit hubs.

- `Q106A2.png`  
  Cascade example plot.  
  This figure shows how much of the total loss comes from the initial attack
  versus cascades for a representative scenario
  (for example targeted attack at 10 percent damage):

  - Design R panel: a small initial bar, almost no cascade bar,
    and a large survived bar.
  - Design F panel: a small initial bar, a very large cascade bar,
    and a tiny survived bar.

These are the canonical “proof of life” for TU Q106_A.

You should be able to run the cell once and then immediately see:

- the aggregated summary table and `T_robust` values in the notebook output,
- `Q106A.png` and `Q106A2.png` appear in the file browser and match the
  descriptions above.

The figures are embedded here for quick inspection:

![Q106A · service vs attack](./Q106A.png)

![Q106A2 · cascade examples](./Q106A2.png)


---

### 1.8 Result snapshot: what the current MVP shows

One reference run with the default parameters (N = 200) produces the
following qualitative behavior.

#### Random attacks

* Both Design R and Design F keep `S_multi` well above all targets:

  * even at 20 percent random node removal,
    the remaining multi-layer service level is still above `0.60`.
* Design F degrades a bit faster than R, but not in a catastrophic way.

If you only look at the **left panel** of `Q106A.png`
(random attacks), both designs look “reasonably robust”.

#### Targeted attacks

When attacks target power-layer hubs, the story changes completely:

* **Design R**

  * `S_multi` stays close to 0.9 across 5 percent, 10 percent and 20 percent
    targeted damage.
  * `cascade_removed_fraction` remains near zero.
  * There is no visible runaway cascade; the system absorbs smart attacks.

* **Design F**

  * even at 5 percent targeted damage, `S_multi` drops to almost zero,
  * 10 percent and 20 percent targeted damage also leave `S_multi` near zero,
  * `cascade_removed_fraction` reaches around 0.95, 0.90, 0.80,
    which means most losses come from cascading failure, not the initial hit.

In `Q106A.png`, this appears as:

* a high plateau for Design R in the **targeted** panel,
* a line collapsed to almost zero for Design F.

In `Q106A2.png`, this appears as:

* Design R: “survived” bar dominates, cascade bar almost invisible,
* Design F: cascade bar dominates, survived bar almost gone.

#### Robustness tension numbers

From the printed `T_robust` table we obtain:

* Design R has `T_robust ≈ 0.0`
  (no scenario violates the declared robustness standard).

* Design F has `T_robust ≈ 0.3`
  (on average, effective service is short of the promised level by 0.3).

So:

* If you only test random failures, both designs might pass as “robust”.
* Once you add targeted attacks and explicit cross-layer cascades,
  Design F reveals a strong hidden tension between robustness narrative and
  effective behavior.
* `T_robust` compresses this mismatch into a single scalar that is easy to
  compute, compare, and audit.

---

### 1.9 How to reproduce (step-by-step checklist)

1. Open
 [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/onestardao/WFGY/blob/main/TensionUniverse/Experiments/Q106_MVP/Q106_A.ipynb)

2. Confirm that the notebook shows a single long code cell.

3. Run the cell once.

4. After execution finishes, verify:

   * the aggregated summary table is printed in the output.
   * the `T_robust` table shows Design R ≈ 0 and Design F ≈ 0.3.
   * `Q106A.png` and `Q106A2.png` are present, and match the descriptions in
     Section 1.7.

5. (Optional) Experiment:

   * change the number of hubs in Design F,
   * change the edge probability in Design R,
   * flip the cascade rule (for example make both designs use AND or OR),
   * adjust the target function used in `T_robust`,
   * re-run and compare how sensitive `T_robust` is to these choices.

This completes the “effective layer” MVP for TU Q106_A.

---

## 2. Experiment B: layer importance and design tension (planned)

Experiment B is a narrative-level extension of TU Q106.
The idea is to treat layer importance assignments as design claims and define
a new tension observable `T_design` that responds when observed failures
contradict those claims.

### 2.1 Research question

Given tiny multilayer networks with explicit “importance labels” on layers,
can we measure how often real collapses violate those labels?

Example narratives:

* “transport is primary, communication is secondary”
* “power is critical, everything else is optional”

We want `T_design` to be small when failures align with these narratives, and
large when supposedly secondary layers are in fact the real single points
of failure.

### 2.2 Planned setup

A future notebook `Q106_B.ipynb` will:

* assign importance weights to layers,

* run multiple attack scenarios (random, targeted, mixed),

* summarize each run with a short text:

  * “system failed because communication hubs collapsed first”,
  * “power layer loss propagated into transport and caused global outage”,

* optionally ask a language model to read:

  * the narrative about layer importance,
  * the failure summaries for each scenario,
  * and judge whether they match or contradict.

`T_design` would then be defined from:

* the frequency and severity of mismatches between narrative and reality,
* recurring patterns where “secondary” layers behave as critical bottlenecks.

This section is intentionally forward-looking.
It records the design so that future work stays consistent with the
current effective-layer experiment.

---

## 3. How this MVP fits into Tension Universe

TU Q106 treats robustness as a tension between:

* multilayer structure and failure propagation,
* design narratives and observed behavior under stress,
* what we claim about redundancy and what actually happens when things break.

Experiment A already provides:

* a concrete two-layer multiplex model,
* a scalar robustness tension `T_robust`,
* reproducible artifacts
  (`Q106A.png`, `Q106A2.png` plus the printed tables)
  that anyone can regenerate by running a single cell.

Experiment B will extend this to narrative claims once implemented.

For broader TU context:

* [Experiments index](../README.md)
* [Event Horizon (WFGY 3.0)](../../EventHorizon/README.md)

For the full WFGY 3.0 Tension Universe pack and related tools, see:

* [https://github.com/onestardao/WFGY](https://github.com/onestardao/WFGY)

---

### Charters and formal context

This page is written under:

* [TU Effective Layer Charter](../../Charters/TU_EFFECTIVE_LAYER_CHARTER.md)
* [TU Encoding and Fairness Charter](../../Charters/TU_ENCODING_AND_FAIRNESS_CHARTER.md)
* [TU Tension Scale Charter](../../Charters/TU_TENSION_SCALE_CHARTER.md)
