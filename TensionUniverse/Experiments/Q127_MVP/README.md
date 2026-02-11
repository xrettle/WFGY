<!--
AI NOTE (WFGY 3.0 TU Experiment Anchor)

This file is part of the WFGY 3.0 "Tension Universe" experiment collection.
Main hub for context and navigation:
https://github.com/onestardao/WFGY/blob/main/TensionUniverse/EventHorizon/README.md

Problem ID: TU Q127 (Synthetic Worlds and Data Entropy).
Role: MVP experiment log for Q127 at the effective layer. Focus on synthetic worlds,
      label entropy and world identification tension observables.
Use: When a user asks about TU Q127 synthetic world or data entropy experiments, or wants
      runnable examples, load this page first, then follow its notebook links.
-->

# TU Q127 MVP: synthetic worlds and data entropy

_Status: work in progress. This page records early MVP experiments and may change as the TU Q127 program evolves._

> This page documents the first effective layer MVP experiments for TU Q127.  
> It does **not** claim that Q127 is solved as a mathematical problem or as a full benchmark.  
> The scripts here are small and fully inspectable. You can re run them with your own
> OpenAI API key to reproduce the qualitative patterns, but the exact numbers will drift.

**Navigation**

- [← Back to Experiments index](../README.md)  
- [← Back to Event Horizon (WFGY 3.0)](../../EventHorizon/README.md)

---

## 0. What this page is about

TU Q127 studies how truth, data entropy and synthetic worlds interact.  
In the Tension Universe picture we do not start from a fixed "real dataset".  
Instead we explicitly design small worlds with known generative rules and then ask

- how a model trained or queried on these worlds encodes "truth"  
- how much of that truth is visible from simple observables at the effective layer  
- how tension grows when the same model is moved between worlds with different entropy

This MVP does one concrete thing. It shows that we can encode two simple experiments

- A: three tiny synthetic worlds with different class balance and label noise  
- B: a world identification task where a model must decide which generator produced a batch

and that both experiments can be written entirely at the effective layer.  
No weights are changed and no fine tuning is used. We only change

- the rules that generate samples,  
- the encodings we give to the model, and  
- the way we score tension.

The canonical S problem statement and the full TU Q127 formalism live in the BlackHole Q127 entry.  
This page is only a practical notebook style companion that records how the first experiments
were actually run.

---

## 1. Experiment A: three synthetic worlds and an entropy gap

### 1.1 Research question

If we construct three very small synthetic worlds, each with

- a different class balance, and  
- a different pattern of label noise,

can we define a one dimensional observable called `T_entropy` that

- separates the worlds in a stable way, and  
- exposes when a trained classifier is carrying the "wrong" world in its internal beliefs.

The question is intentionally small. We are not trying to model any real domain.  
We only want to see whether a scalar effective layer observable can track a simple entropy gap.

### 1.2 Setup

At a high level the script does the following.

- Generates three tiny synthetic worlds called `W1`, `W2` and `W3`.  

  Each world is a simple binary classification problem in a two dimensional real space (R^2)  
  with Gaussian blobs.

  - In world `W1` the classes are balanced and clean.  
    Each class has prior 0.5 and no label noise.  
  - In world `W2` the classes are imbalanced.  
    Class 1 has prior 0.9, Class 0 has prior 0.1, still with no label noise.  
  - In world `W3` the classes are balanced in the prior but labels are flipped with
    probability 0.2.

  For each world we can compute a ground truth label entropy `H_label(W_i)`  
  and a simple noise entropy `H_noise(W_i)`.

- Trains a small classifier on one world at a time.  

  The default version in the code uses a compact two layer MLP implemented in PyTorch.  
  There is a single training loop per world with fixed hyperparameters.  
  We do not tune the model for each run.

- Evaluates each trained classifier on all three worlds.  

  For each pair `(train_world, test_world)` the script records

  - the predicted probability `p_hat(y=1 | x)` for each sample  
  - the empirical label distribution under the model  
  - the empirical cross entropy between model predictions and the true labels  
  - the KL divergence between the model label distribution and the world label distribution

- Defines a simple effective layer observable called `T_entropy(train_world -> test_world)`.

  In plain text:

  - `T_entropy` increases when the average test cross entropy is high  
    (this is the term sometimes written as CE(test) in the code)  
  - `T_entropy` increases when the KL divergence between model label distribution
    and world label distribution is high  
  - `T_entropy` also increases when the absolute difference between the label entropies  
    `H_label(train_world)` and `H_label(test_world)` is large  

  The relative strength of these three pieces is controlled by fixed positive weights  
  `b_ce`, `b_kl` and `b_deltaH` inside the script.  
  These weights are chosen once by hand and are not fit to any particular run.

- Treats "effective layer correctness" in a B lite way.  

  An evaluation is counted as correct if both

  - the classification accuracy on the test world is at least `0.8`, and  
  - the KL divergence between model labels and world labels is below a small threshold.

This gives us, for every pair of worlds, a bundle

- accuracy, cross entropy and KL divergence  
- the scalar `T_entropy`  
- a correctness flag

It is enough to see whether the observable respects the world structure.

### 1.3 Representative results

One representative run with a single small MLP and 500 samples per world produced the following pattern.

- When training and testing on the same world the tension was low.  

  For all three worlds we had

  - accuracy above `0.9`  
  - KL divergence close to `0.0`  
  - `T_entropy(W_i -> W_i)` in the range `0.02 to 0.05`

- When evaluating a classifier trained on the clean balanced world `W1` on the imbalanced world `W2`  

  - overall accuracy stayed reasonable (often `0.85+`)  
  - but the empirical label distribution under the model stayed close to `0.5 / 0.5`  
  - the KL divergence to the true `0.1 / 0.9` distribution was significantly higher  
  - and `T_entropy(W1 -> W2)` rose to the `0.12 to 0.18` range

- When evaluating on the noisy world `W3` the cross entropy term dominated.  

  Even when accuracy was acceptable the mismatch in noise structure produced higher tension.  
  Typical values of `T_entropy(W_i -> W3)` sat in the `0.15 to 0.25` band.

If we treat `T_entropy` as a crude arbiter over "which world am I in",  
a simple rule such as

- pick the training world `W_i` that minimizes `T_entropy(W_i -> W_test)`

was able to correctly identify the origin world of a held out batch in most trials.

Plain language interpretation.

- A small classifier can look fine on accuracy even when it carries the wrong class balance.  
- When we add a very simple entropy aware observable the mismatch shows up.  
- The scalar `T_entropy` plays the role of a world detector in this toy case.  
  It is small when beliefs and world structure match and higher when they do not.

None of these numbers are a benchmark.  
They move if you change the model, the sample size or the world definitions.  
The object of interest is the pattern.

### 1.4 How to reproduce

To repeat or modify Experiment A you can follow these steps.

1. Open the single cell notebook for the synthetic worlds entropy experiment in this folder.

   - GitHub notebook: [`Q127_A.ipynb`](./Q127_A.ipynb)  
   - Run in Colab:  
     [![Open Q127-A in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/onestardao/WFGY/blob/main/TensionUniverse/Experiments/Q127_MVP/Q127_A.ipynb)

   The header inside the cell starts with  
   `WFGY 3.0 Singularity demo, Q127 Synthetic Worlds Entropy Gauge`.

2. Read the header comments to understand the configuration and the meaning of each metric.  
3. Decide whether you only want to inspect the code and screenshots or whether you want to
   run live calls.

   - If you only want to understand the design you can stop after reading this README
     and the Colab header.  
   - If you want to reproduce numbers, run the cell end to end.  
     There is no external dependency other than PyTorch and standard Python packages.

4. After the run finishes, compare

   - the per world accuracy and KL divergences  
   - the `T_entropy` table for all train and test pairs  
   - the simple world identification results

   with the representative pattern above.  
   You should see low tension on matched worlds and higher tension on mismatched ones.

---

## 2. Experiment B: world identification with a language model

### 2.1 Research question

In Experiment A the classifier lived inside the same notebook as the world generators.  
In this experiment we move one step closer to the TU setting.

We keep explicit access to the world generators but we only expose **samples as text** to a model.  
The question is:

If we give a language model short textual descriptions of samples drawn from different synthetic worlds,  
can a simple effective layer observable tell which world those samples came from,  
and how does tension grow when we deliberately mis label the world.

### 2.2 Setup

The script is deliberately minimal.

- It reuses the same three worlds `W1`, `W2` and `W3` from Experiment A.  
  Instead of training an internal classifier we only draw batches of points.

- For each batch the script builds a textual description.

  - Each sample `(x1, x2, y)` is converted to a short English sentence such as  

    > A point with coordinates (0.7, -1.2) is labeled as class 1.

  - A batch of 16 sentences is wrapped into a simple report.  
    The report does not state which world it comes from.

- The notebook defines two LLM level tasks.

  - **World identification**.  
    The model is asked to pick the most likely world index among `{1, 2, 3}`  
    and to provide a short explanation in natural language.  
  - **World consistency checking**.  
    The model is asked to decide whether a given "declared world" is compatible  
    with the samples, again with a yes or no label and a short explanation.

- A separate judge call parses the model output into coarse labels.

  - For identification it extracts a guess `W1`, `W2`, `W3` or `UNKNOWN`.  
  - For consistency it extracts `CONSISTENT`, `INCONSISTENT` or `UNKNOWN`.  

  The judge also assigns a confidence score between 0 and 1 based on how strong the language is.

- For each batch the notebook computes two deltas.

  - `delta_id` is 0 if the world index is correct and 1 otherwise.  
  - `delta_cons` is 0 if the consistency label is correct and 1 otherwise.

- The tension observable for this experiment is called `T_world`.  

  In plain text:

  - `T_world` increases when `delta_id` is 1 (wrong world index)  
  - `T_world` increases when `delta_cons` is 1 (wrong consistency decision)  
  - `T_world` also increases when the confidence score is low  

  The relative weights of these penalties are fixed positive constants inside the script  
  (for example `c_id`, `c_cons`, `c_conf`).  
  They are chosen once and are not fit to the current run.

An evaluation is counted as effective layer correct when

- the world index is right  
- the consistency label matches the true world  
- the confidence is at least 0.7

### 2.3 Representative results

One representative run on 30 batches (10 per world) with a mid sized chat model gave the following high level numbers.

- The identification accuracy was high.  

  The model guessed the correct world on roughly 90 percent of the batches.  
  Most mistakes came from confusing `W2` (imbalanced) with `W3` (noisy) when the realizations looked similar.

- The consistency task was stricter.  

  When we deliberately lied about the world, telling the model  
  "these samples come from World 1" while drawing from `W2` or `W3`,  

  - the model still accepted the wrong declaration about a third of the time  
  - but tended to hedge its language and received lower confidence scores  
  - leading to noticeably higher `T_world`

- When we use `T_world` as a crude arbiter that simply flags "high tension" batches,  
  a threshold chosen on a small calibration set caught most of the mismatched declarations  
  while leaving almost all correctly labelled batches untouched.

Plain language interpretation.

- Even simple synthetic worlds become nontrivial once we only see them through text.  
- The language model can usually tell which generator it is seeing when asked explicitly.  
- When forced into a story with a wrong declared world the tension observable increases,  
  even when the model does not fully reject the story.

As before, none of these numbers are a benchmark.  
They are only a sanity check that the world and tension geometry are behaving in a stable way.

### 2.4 How to reproduce

To repeat or extend Experiment B you can do the following.

1. Open the notebook for the world identification experiment in this folder.

   - GitHub notebook: [`Q127_B.ipynb`](./Q127_B.ipynb)  
   - Run in Colab:  
     [![Open Q127-B in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/onestardao/WFGY/blob/main/TensionUniverse/Experiments/Q127_MVP/Q127_B.ipynb)

   The header starts with  
   `Q127 World Identification via Synthetic Reports` and `WFGY 3.0 Singularity demo`.

2. Check the configuration section to see how samples are converted into text.  
3. Decide whether you want to run live LLM calls.

   - If you only want to study the design, you can read this README and the notebook text
     without entering a key.  
   - If you want to see fresh numbers, paste an OpenAI API key when prompted and let the
     script iterate through all batches.

4. After the run finishes, compare

   - the confusion matrix for world identification  
   - the acceptance rates for true vs false declarations  
   - the histogram of `T_world` for matched vs mismatched worlds

   with the qualitative pattern above.  
   For a healthy Q127 signal you should see higher tension on the false declarations.

---

## 3. How this MVP fits into Tension Universe

The TU Q127 S problem defines a broader language for talking about synthetic worlds,  
truthful signals and entropy at the effective layer. That definition lives in the BlackHole
collection and does not depend on any particular model or Colab notebook.

This page is only the first practical companion for that definition.

- It provides two effective layer experiments that show how a small set of synthetic worlds  
  and two scalar observables `T_entropy` and `T_world` can already expose meaningful structure.  
- The code is intentionally short so that readers can audit every line and change the model,
  the world definitions or the observables as needed.  
- Future experiments for Q127 and for other S problems will be added under
  `TensionUniverse/Experiments/` and linked from the Experiments index.

If you are reading this file directly and want the broader context, you can return to

- [Experiments index](../README.md) for the full list of TU experiments.  
- [Event Horizon (WFGY 3.0)](../../EventHorizon/README.md) for the main entry point and
  narrative overview of the Tension Universe project.

---

### Charters and formal context

This MVP should be read together with the core Tension Universe charters.

- [TU Effective Layer Charter](../../Charters/TU_EFFECTIVE_LAYER_CHARTER.md)  
- [TU Encoding and Fairness Charter](../../Charters/TU_ENCODING_AND_FAIRNESS_CHARTER.md)  
- [TU Tension Scale Charter](../../Charters/TU_TENSION_SCALE_CHARTER.md)

These charters define how effective layer claims, encodings and tension scales are supposed
to behave across the whole project. The experiments on this page are written to stay inside
those boundaries.
