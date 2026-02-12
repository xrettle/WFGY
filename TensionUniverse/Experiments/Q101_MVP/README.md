<!--
AI NOTE (WFGY 3.0 TU Experiment Anchor)

This file is part of the WFGY 3.0 "Tension Universe" experiment collection.
Main hub for context and navigation:
https://github.com/onestardao/WFGY/blob/main/TensionUniverse/EventHorizon/README.md

Problem ID: TU Q101 (Equity Premium Puzzle).
Role: MVP experiment log for Q101 at the effective layer. Focus on tiny
      consumption based models and tension observables between predicted and observed premia.
Use: When a user asks about TU Q101 equity premium experiments or wants
      runnable examples, load this page first, then follow its notebook links.
-->

# TU Q101 MVP: toy equity premium tension

_Status: MVP A implemented (offline, single cell). MVP B is design only and will be added later._

> TU Q101 encodes the equity premium puzzle as a tension between
> simple consumption based models and stylised target bands for
> long run equity premia.  
> The goal is to expose where the puzzle appears in tiny toy worlds,
> not to resolve real markets.

**Navigation**

- [← Back to Experiments index](../README.md)  
- [← Back to Event Horizon (WFGY 3.0)](../../EventHorizon/README.md)

---

## 0. What this page is about

TU Q101 looks at the equity premium puzzle as a structured mismatch between

- predicted premia from simple asset pricing models, and  
- empirical style targets for long run equity premia.

The MVP here uses small simulated economies with

- consumption processes,  
- risk free and risky assets,  
- representative agents with utility functions,

and tracks tension observables when the model cannot match observed premia without extreme parameters.

Users can understand the result just by reading this page.  
Running the Colab notebook is only required if you want to reproduce the numbers or modify parameters.

---

## 1. Experiment A: simple consumption based asset pricing model

### 1.1 Research question

If we build a minimal consumption based asset pricing model, can we define a scalar observable `T_premium` that

- is small when predicted equity premia and volatility stay inside a plausible band,  
- and grows when the model only matches targets by pushing risk aversion or other parameters into unrealistic regions.

### 1.2 Notebook and Colab entry

**Notebook**

- `TensionUniverse/Experiments/Q101_MVP/Q101_A.ipynb`

**One click Colab**

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/onestardao/WFGY/blob/main/TensionUniverse/Experiments/Q101_MVP/Q101_A.ipynb)

The notebook is a single cell script.  
All runs are fully offline. No API key is needed.

### 1.3 Model and tension observable

The notebook simulates three tiny consumption based worlds and computes a scalar tension observable `T_premium` for each world.

Core ingredients:

- A lognormal consumption growth process.  
- Two assets:
  - a risk free asset with return `R_f`,  
  - a risky asset whose payoff is correlated with consumption.
- A representative agent with power utility and risk aversion `gamma`.
- Standard consumption based pricing:
  - stochastic discount factor `m = beta * g^{-gamma}`,  
  - prices from expectations of `m` and payoffs,  
  - equity premium `E[R_e] - R_f` and volatility `vol`.

For each world the notebook:

1. Sweeps `gamma` over a grid from 0.5 to 20.  
2. For every `gamma`, computes the implied equity premium and volatility.  
3. Picks `gamma*` that gets closest to a target long run equity premium.

Target band and plausible parameter region (stylised):

- Target long run equity premium: **6.0%**.  
- Plausible risk aversion range for the representative agent: **gamma in [1.0, 5.0]**.  
- Premium mismatch is scaled at **2.0% per unit** in the tension score.

The scalar observable `T_premium` combines three components at `gamma*`:

1. Premium mismatch  
   - absolute deviation between implied and target premium, scaled by 2% per unit.  
2. Risk aversion penalty  
   - zero if `gamma*` is in [1, 5],  
   - linear penalty when `gamma*` lies outside this plausible band.  
3. Volatility penalty  
   - linear penalty when the realised volatility falls outside a simple per world target interval.

Weights are chosen so that premium mismatch and risk aversion dominate, with volatility as a weaker regulariser.

Configured scenarios:

- `no_puzzle`  
  High volatility world with strongly correlated risky asset. A moderate `gamma` can support a six percent equity premium without stress.

- `realistic_puzzle`  
  Low volatility consumption world that is closer to real data. We still demand a six percent equity premium. The model tends to require very large `gamma` values to get close.

- `anemic_asset`  
  Low volatility risky asset. Consumption volatility is low and the risky asset itself is not very volatile. Asking for six percent premium here is almost impossible without extreme parameters.

### 1.4 First reference run

All simulations complete in a single cell.  
The notebook prints a summary table sorted by `T_premium` (lower means closer to a plausible world):

- Target premium: **6.0%** for all worlds.  
- Plausible `gamma` band: **[1.0, 5.0]**.

Key outputs from the reference run:

- **no_puzzle**  
  - `gamma* ≈ 3.46` (inside plausible band)  
  - model premium ≈ **5.83%** (difference −0.17%)  
  - volatility ≈ **0.22**  
  - `T_premium ≈ 0.035`  

- **realistic_puzzle**  
  - `gamma* = 20.0` (hitting the right edge of the grid)  
  - model premium ≈ **4.53%** (difference −1.47%)  
  - volatility ≈ **0.28**  
  - `T_premium ≈ 1.52`  

- **anemic_asset**  
  - `gamma* = 20.0`  
  - model premium ≈ **1.28%** (difference −4.72%)  
  - volatility ≈ **0.11**  
  - `T_premium ≈ 2.14`  

Quick interpretation:

- In the **no_puzzle** world, a moderate risk aversion around three and a half already delivers a premium very close to six percent, with reasonable volatility. Tension is almost zero.  
- In the **realistic_puzzle** world, matching a six percent premium demands extreme risk aversion. Even at `gamma = 20` the model only reaches about four and a half percent. Tension is clearly elevated.  
- In the **anemic_asset** world, the risky asset is too quiet. The model cannot get anywhere near six percent premium even at the most extreme `gamma` on the grid. Tension is highest.

This behaviour is also visible in the plots saved by the notebook:

![TU Q101_A · Model equity premium vs risk aversion gamma](./Q101A.png)

The premium versus `gamma` plot shows that only the high volatility world passes through the six percent target band for plausible `gamma` values.  
The low volatility and anemic asset worlds stay far below the target even when `gamma` is pushed to extremes.

![TU Q101_A · T_premium per scenario](./Q101A2.png)

The `T_premium` bar chart summarises the story in a single view:

- `no_puzzle` sits near zero tension,  
- `realistic_puzzle` has moderate tension,  
- `anemic_asset` has the largest tension.

### 1.5 How to reproduce

To reproduce or modify the experiment:

1. Open `Q101_A.ipynb` in Colab using the badge above.  
2. Read the header block that explains the three worlds, target band and tension definition.  
3. Run the single cell to:
   - simulate all three worlds,  
   - sweep `gamma`,  
   - compute `T_premium` and print the summary table,  
   - regenerate the two plots and save them as  
     - `Q101A_premium_vs_gamma.png`  
     - `Q101A_T_premium.png`.  
4. Adjust parameters if you want to explore variants, for example different target premia or different volatility ranges.

---

## 2. Experiment B: narrative models versus numerical models

### 2.1 Research question

Can we use a language model to evaluate narrative explanations for the equity premium and compare them against the toy numerical model, defining a narrative tension observable `T_narrative`.

### 2.2 Setup (design only)

The planned notebook will:

- Generate a small set of narrative hypotheses, for example  
  - rare disasters,  
  - habit formation,  
  - institutional constraints.  
- For each configuration of the toy numerical model, produce a short summary describing its mechanism.  
- Ask a language model to judge which narrative hypothesis best fits the numerical summary.  
- Extract consistency scores.

`T_narrative` will be defined as a function of:

- mismatch between assigned narrative and true simulated mechanism,  
- low consistency scores when the narrative does not fit the numerical story.

### 2.3 Expected pattern

We expect:

- lower `T_narrative` when numerical mechanisms and selected narratives match,  
- higher `T_narrative` when narratives and numerical structure disagree.

This bridges TU Q101 with narrative level explanations at the effective layer.  
Implementation of `Q101_B.ipynb` is deferred to a later iteration.

---

## 3. How this MVP fits into Tension Universe

TU Q101 treats the equity premium puzzle as a tension between

- simple asset pricing models,  
- empirical style target bands,  
- and narrative explanations.

This MVP page currently provides:

- a minimal numerical experiment with `T_premium` that shows where a toy model world behaves plausibly and where it runs into the equity premium puzzle,  
- a planned narrative experiment with `T_narrative` that will connect numerical mechanisms to verbal stories.

Both are starting points at the effective layer, not final economic models.

For the broader project:

- [Experiments index](../README.md)  
- [Event Horizon (WFGY 3.0)](../../EventHorizon/README.md)

---

### Charters and formal context

The design of this MVP follows:

- [TU Effective Layer Charter](../../Charters/TU_EFFECTIVE_LAYER_CHARTER.md)  
- [TU Encoding and Fairness Charter](../../Charters/TU_ENCODING_AND_FAIRNESS_CHARTER.md)  
- [TU Tension Scale Charter](../../Charters/TU_TENSION_SCALE_CHARTER.md)
