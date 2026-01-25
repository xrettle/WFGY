# Q055 · Graph isomorphism exact complexity

## 0. Header metadata

```txt
ID: Q055
Code: BH_CS_GI_COMPLEXITY_L3_055
Domain: Computer science
Family: Computational complexity
Rank: S
Projection_dominance: I
Field_type: combinatorial_field
Tension_type: complexity_tension
Status: Open
Semantics: discrete
E_level: E1
N_level: N1
Last_updated: 2026-01-25
```

---

## 1. Canonical problem and status

### 1.1 Canonical statement

The graph isomorphism problem (GI) is:

Input: two finite graphs G and H on the same number of vertices.
Question: is there a bijection between the vertex sets of G and H that preserves adjacency?

In standard notation:

Given graphs `G = (V_G, E_G)` and `H = (V_H, E_H)` with `|V_G| = |V_H|`, decide whether there exists a bijection

`f : V_G -> V_H`

such that for all vertices `u, v` in `V_G`,

`(u, v) in E_G` if and only if `(f(u), f(v)) in E_H`.

The decision problem GI is known to be in `NP`, since a bijection can be guessed and verified in polynomial time. The exact complexity status of GI is unknown.

The canonical open question is:

> Is graph isomorphism in P, or is it NP complete, or does it lie in an intermediate complexity class between P and NP complete?

### 1.2 Status and known results

Key known facts include:

* GI is in NP.
* GI is not known to be in P.
* GI is not known to be NP complete.
* If GI were NP complete under many standard kinds of reductions, then the polynomial time hierarchy would collapse. This is widely considered unlikely.
* Babai announced a quasipolynomial time algorithm for GI, which places GI in time `n^{polylog n}`.
* There are polynomial time algorithms for important special cases, such as graphs of bounded degree, graphs with bounded eigenvalue multiplicity, and several others.

Despite major progress on algorithms and structural understanding, the exact complexity class of GI remains unresolved.

### 1.3 Role in the BlackHole project

Within the BlackHole S problem collection, Q055 has three main roles:

1. It is the canonical example of a problem whose known algorithms suggest relative easiness compared with typical NP complete problems, yet no proof places it in P.
2. It anchors a family of open complexity classification problems, including exact complexity questions for other candidate intermediate problems.
3. It provides a clean testbed for Tension Universe encodings of:

   * complexity evidence,
   * reduction evidence,
   * stability of algorithmic behavior across graph families.

### References

1. Laszlo Babai, “Graph isomorphism in quasipolynomial time”, published version in the Journal of the ACM, based on the 2015 preprint and later revisions.
2. Martin Grohe, “Descriptive Complexity, Canonisation, and Definable Graph Structure Theory”, Cambridge University Press, 2017, chapters on graph isomorphism and logical definability.
3. Oded Goldreich, “Computational Complexity: A Conceptual Perspective”, Cambridge University Press, 2008, sections on NP, intermediate problems, and GI.
4. Michael R. Garey and David S. Johnson, “Computers and Intractability: A Guide to the Theory of NP Completeness”, W. H. Freeman, 1979, background on NP, reductions, and candidate intermediate problems.

---

## 2. Position in the BlackHole graph

This block records how Q055 sits inside the BlackHole graph as nodes and edges among Q001 to Q125. Each edge has a one line reason that points to a concrete component or tension type.

### 2.1 Upstream problems

These problems provide prerequisites, tools, or general foundations that Q055 relies on at the effective layer.

* Q020 (BH_CS_P_VS_NP_L3_020)
  Reason: Supplies the general complexity tension framework for P, NP, and intermediate classes that Q055 specializes to the GI case.

* Q021 (BH_CS_AVERAGE_WORST_GAP_L3_021)
  Reason: Provides notions of complexity gap and evidence aggregation that are reused for GI tension between worst case, average case, and practical performance.

* Q023 (BH_MATH_FINITE_GROUPS_L3_023)
  Reason: Supplies group theoretic tools and invariants that appear in several GI algorithms and in the GI complexity narrative.

### 2.2 Downstream problems

These problems directly reuse components from Q055 or depend on its complexity tension structure.

* Q056 (BH_CS_CIRCUIT_LOWER_L3_056)
  Reason: Uses the GI tension encoding as a contrast case when studying circuit lower bounds and barriers for NP complete problems.

* Q057 (BH_CS_RL_GENERALIZATION_L3_057)
  Reason: Reuses the evidence aggregation patterns from GI complexity to frame generalization tension in reinforcement learning between empirical ease and worst case hardness.

* Q059 (BH_CS_INFO_THERMODYN_L3_059)
  Reason: Uses Q055 style gap measures between abstract complexity and observed resource usage as templates for information thermodynamics in computation.

### 2.3 Parallel problems

Parallel nodes share similar complexity tension but no direct component dependence.

* Q022 (BH_CS_AVERAGE_CASE_COMPLEXITY_L3_022)
  Reason: Both Q055 and Q022 study gaps between worst case and typical behavior using similar tension style invariants.

* Q024 (BH_CS_CSP_PHASE_L3_024)
  Reason: Both analyze structural transitions in problem difficulty across parameter ranges although the underlying problems differ.

### 2.4 Cross domain edges

Cross domain edges connect Q055 to problems in other domains that can reuse its components.

* Q039 (BH_PHYS_QTURBULENCE_L3_039)
  Reason: Reuses the idea of intermediate regimes between simple and fully chaotic behavior, encoded via tension profiles that do not clearly match either extreme.

* Q123 (BH_AI_INTERP_L3_123)
  Reason: Uses the GI tension encoding as an analogy for interpretability tasks where models appear easy to probe yet lack a clean structural complexity classification.

---

## 3. Tension Universe encoding (effective layer)

All content in this block is at the effective layer. Only state spaces, observables, invariants, tension scores, and singular sets are described. No hidden generative rules or constructions from raw data are specified.

### 3.1 State space

We assume the existence of a discrete semantic state space

`M`

with the following interpretation at the effective layer:

* Each state `m` in `M` represents a coherent “GI complexity world configuration” that includes:

  * a family of graph instances or graph distributions,
  * a portfolio of known algorithms with empirical and theoretical performance summaries,
  * a set of known reductions between GI and other problems,
  * meta information about how these elements cohere.

We do not describe how such states are generated from raw data or proofs. We only assume that for each choice of graph families and algorithm portfolios, there exist states `m` that encode their summaries in a discrete and finite way.

### 3.2 Effective fields and observables

We introduce the following observables on `M`.

1. Algorithmic performance summary

```txt
Perf_GI(m; F)
```

* Input: a state `m` and a graph family descriptor `F` (for example, constant degree graphs, random regular graphs, strongly regular graphs).
* Output: a discrete tuple summarizing the time and space performance of the best known GI algorithms on `F`, including asymptotic guarantees (when known) and representative empirical scaling.

2. Reduction complexity summary

```txt
Red_GI(m)
```

* Input: a state `m`.
* Output: a tuple that encodes:

  * known reductions from GI to other problems,
  * known reductions from other problems to GI,
  * constraints on possible reductions (for example, classes of reductions that would collapse hierarchies if GI were complete).

3. Evidence for membership in P

```txt
E_P(m)
```

* Input: a state `m`.
* Output: a nonnegative scalar that summarizes how strongly the configuration encoded in `m` supports the hypothesis that GI has polynomial time algorithms. This may aggregate:

  * algorithmic progress,
  * structural decompositions,
  * lack of strong lower bound evidence.

4. Evidence for NP completeness

```txt
E_NPC(m)
```

* Input: a state `m`.
* Output: a nonnegative scalar that summarizes how strongly the configuration supports the hypothesis that GI is NP complete. This may aggregate:

  * failed attempts at polynomial time algorithms,
  * structural resemblance to NP complete problems,
  * absence of barriers to certain reductions.

5. Evidence for intermediate status

```txt
E_INT(m)
```

* Input: a state `m`.
* Output: a nonnegative scalar that summarizes evidence that GI is neither in P nor NP complete under standard assumptions, for example:

  * links to collapses of the polynomial hierarchy if GI were NP complete,
  * stability of algorithmic progress in a quasipolynomial region,
  * parallels with other candidate intermediate problems.

All three evidence quantities are defined so that higher values mean stronger support for the corresponding hypothesis, within the encoded configuration.

### 3.3 Complexity tension observables

We define normalized evidence scores by forcing them into a common scale, for example by dividing each by a reference maximum over an admissible class of states. At the effective layer, we treat the normalized values as given:

```txt
p_P(m), p_NPC(m), p_INT(m) in [0, 1]
```

that sum to at most 1 and represent a coarse allocation of evidence among three competing hypotheses.

1. P versus intermediate tension

```txt
DeltaS_P_INT(m) = |p_P(m) - p_INT(m)|
```

2. P versus NP complete tension

```txt
DeltaS_P_NPC(m) = |p_P(m) - p_NPC(m)|
```

3. Normalized total conflict

```txt
DeltaS_total(m) = p_P(m) + p_NPC(m) + p_INT(m) - max{p_P(m), p_NPC(m), p_INT(m)}
```

`DeltaS_total(m)` measures how much significant support is spread across multiple competing hypotheses instead of concentrating on one.

### 3.4 Effective tension tensor components

We define an effective complexity tension tensor for Q055:

```txt
T_ij(m) = S_i(m) * C_j(m) * DeltaS_total(m) * lambda(m) * kappa_GI
```

where:

* `S_i(m)` are source like factors that encode how strongly different communities or methodologies act as sources of claims about GI (for example algorithm design, complexity theory, group theory).
* `C_j(m)` are receptivity like factors encoding how sensitive downstream applications or theories are to the exact status of GI.
* `DeltaS_total(m)` is the total conflict measure.
* `lambda(m)` is a convergence factor from the TU core that encodes whether the current evidence aggregation is stable or not.
* `kappa_GI` is a fixed coupling constant that sets the scale for GI related complexity tension.

The indexing of `i` and `j` is not specified. It is sufficient that for each state `m`, `T_ij(m)` is well defined and finite.

### 3.5 Singular set and domain restrictions

There are configurations where the observables above are not well defined, for example when:

* the encoded evidence is contradictory,
* reductions are mis specified,
* normalized scores cannot be consistently assigned.

We collect such states into a singular set:

```txt
S_sing = { m in M : p_P(m), p_NPC(m), p_INT(m) cannot be assigned in a coherent way }
```

All Q055 tension analysis is restricted to:

```txt
M_reg = M \ S_sing
```

When a configuration would fall into `S_sing`, it is treated as outside the domain of the effective Q055 encoding rather than as evidence about the real world status of GI.

---

## 4. Tension principle for this problem

This block states how Q055 is characterized as a tension problem within TU.

### 4.1 Core complexity tension functional

We define the GI complexity tension functional:

```txt
Tension_GI(m) = F(DeltaS_P_INT(m), DeltaS_P_NPC(m), DeltaS_total(m))
```

where `F` is a fixed nonnegative function, for example a weighted sum:

```txt
Tension_GI(m) = a * DeltaS_P_INT(m)
               + b * DeltaS_P_NPC(m)
               + c * DeltaS_total(m)
```

with constants `a, b, c > 0` chosen once for the encoding and held fixed.

Properties:

* `Tension_GI(m) >= 0` for all `m` in `M_reg`.
* `Tension_GI(m)` is small when evidence is coherently concentrated on a single hypothesis about GI.
* `Tension_GI(m)` is large when significant evidence supports conflicting hypotheses.

### 4.2 GI in P as a low tension principle

At the effective layer, the hypothesis that GI is in P corresponds to world configurations where:

* states `m` representing mature scientific consensus have:

  ```txt
  p_P(m) close to 1
  p_NPC(m) and p_INT(m) close to 0
  ```

* the tension functional satisfies:

  ```txt
  Tension_GI(m) <= epsilon_P
  ```

for some small threshold `epsilon_P` that does not grow when more data or more refined analyses are added within the admissible encoding class.

### 4.3 GI intermediate as a structured tension principle

The hypothesis that GI is intermediate corresponds to configurations where:

* states `m` representing mature consensus have:

  ```txt
  p_INT(m) significantly larger than both p_P(m) and p_NPC(m)
  ```

* yet there remains residual tension because no simple class contains GI:

  ```txt
  0 < Tension_GI(m) <= epsilon_INT
  ```

for some moderate band `epsilon_INT` that reflects stable but non trivial disagreement between different forms of evidence.

### 4.4 GI NP complete as persistent high tension

The hypothesis that GI is NP complete corresponds to configurations where any state `m` that remains faithful to known collapse results and hierarchy structure must exhibit:

```txt
p_NPC(m) not dominant, or
Tension_GI(m) >= delta_NPC
```

with `delta_NPC > 0` that cannot be reduced without contradicting respected meta results about the polynomial time hierarchy.

At the effective layer, Q055 is the claim that for any encoding consistent with standard complexity theory, the real world lies either in a low tension P like regime or in an intermediate structured tension regime, and that NP complete like regimes remain in a high tension band.

---

## 5. Counterfactual tension worlds

We outline three counterfactual worlds, all described at the effective layer:

* World P: GI is in P.
* World INT: GI is intermediate.
* World NPC: GI is NP complete.

### 5.1 World P (GI in P, low complexity tension)

In World P:

1. Algorithmic pattern

   * States `m_P` encode polynomial time algorithms for GI that are simple enough to unify existing quasipolynomial algorithms and structural results.
   * The observable `Perf_GI(m_P; F)` shows polynomial time behavior across broad graph families.

2. Evidence allocation

   * Evidence scores satisfy:

     ```txt
     p_P(m_P) close to 1
     p_INT(m_P) and p_NPC(m_P) close to 0
     ```

3. Tension value

   * For mature configurations:

     ```txt
     Tension_GI(m_P) <= epsilon_P
     ```

   * where `epsilon_P` is a small bound reflecting residual technical uncertainties rather than structural conflict.

### 5.2 World INT (GI intermediate, structured but bounded tension)

In World INT:

1. Algorithmic pattern

   * States `m_INT` encode algorithms that are significantly faster than worst case NP complete problems but do not admit clear polynomial bounds.
   * Quasipolynomial or mildly superpolynomial algorithms remain the best general methods despite extensive work.

2. Evidence allocation

   * Evidence scores satisfy:

     ```txt
     p_INT(m_INT) dominant
     p_P(m_INT) and p_NPC(m_INT) both nonzero but clearly smaller
     ```

3. Tension value

   * For mature configurations, the tension sits in a stable intermediate band:

     ```txt
     0 < Tension_GI(m_INT) <= epsilon_INT
     ```

   * The nonzero value reflects enduring disagreement about how to classify GI, but the upper bound reflects that the disagreement is bounded and structured.

### 5.3 World NPC (GI NP complete, persistent high tension)

In World NPC:

1. Algorithmic pattern

   * States `m_NPC` encode strong reductions that make GI NP complete under widely accepted reductions.
   * Yet these reductions create conflicts with standard beliefs about hierarchies or with other complexity evidence.

2. Evidence allocation

   * Evidence scores are unbalanced:

     ```txt
     p_NPC(m_NPC) high from reductions
     p_INT(m_NPC) high from meta results
     p_P(m_NPC) low but nonzero from special case algorithms
     ```

3. Tension value

   * Because evidence pulls in conflicting directions, we have:

     ```txt
     Tension_GI(m_NPC) >= delta_NPC
     ```

   * with `delta_NPC` bounded away from zero in any encoding that respects known collapse results, so the high tension cannot be removed without sacrificing major parts of complexity theory.

### 5.4 Interpretive note

These worlds do not claim to construct underlying TU fields, nor do they predict which world is actual. They only state that if a world with one of these hypotheses were realized in a stable and coherent way, then the GI complexity tension patterns would resemble the ones described.

---

## 6. Falsifiability and discriminating experiments

The following experiments test Q055 encodings, not the truth of GI itself. They can falsify specific choices of observables or parameterizations.

### Experiment 1: Stability of evidence allocation under new algorithms

*Goal:*
Test whether `p_P(m)` and `p_INT(m)` remain stable when new GI algorithms or refinements are incorporated.

*Setup:*

* Start from a baseline state `m_base` that encodes current best algorithms and reductions.
* Construct updated states `m_update` that add hypothetical improvements, for example faster group theoretic methods or better invariant based algorithms.

*Protocol:*

1. For each candidate improvement, form a corresponding `m_update`.
2. Recompute `E_P(m_update)`, `E_NPC(m_update)`, and `E_INT(m_update)` using the fixed evidence aggregation rules.
3. Normalize to obtain `p_P(m_update)`, `p_NPC(m_update)`, `p_INT(m_update)`.
4. Compare the vectors `(p_P, p_NPC, p_INT)` between `m_base` and each `m_update`.

*Metrics:*

* Maximum change in each normalized score between `m_base` and `m_update`.
* Change in `Tension_GI(m)` between baseline and updates.
* Presence or absence of sudden jumps that do not match the qualitative significance of the algorithmic change.

*Falsification conditions:*

* If small, incremental improvements in algorithms cause large and erratic swings in `p_P`, `p_NPC`, or `p_INT` without a clear structural reason, the evidence aggregation and normalization scheme is considered unstable and the current encoding is rejected.
* If a modest improvement tuned to be neutral with respect to P versus INT classification produces a large decrease in `Tension_GI`, the encoding is considered too sensitive and is rejected.

*Semantics implementation note:*
All states and observables are treated as discrete summaries of algorithms and reductions, consistent with the discrete semantics declared in the metadata.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. This experiment can reject unstable GI tension encodings but does not decide whether GI is in P, intermediate, or NP complete.

---

### Experiment 2: Reduction sensitivity and hierarchy constraints

*Goal:*
Check whether the encoding of `E_NPC(m)` respects known constraints about reductions and hierarchy collapses.

*Setup:*

* Define a family of hypothetical reductions from NP complete problems to GI that vary in strength and side effects on known complexity hierarchies.
* For each type of reduction, build a state `m_red` that encodes its existence and consequences.

*Protocol:*

1. Construct several types of hypothetical reduction scenarios:

   * reductions that would collapse the polynomial time hierarchy,
   * reductions that preserve the hierarchy,
   * weak reductions that only relate restricted NP complete problems to restricted GI variants.

2. For each scenario, assign a state `m_red` and compute `E_NPC(m_red)` and `E_INT(m_red)` according to the fixed evidence rules.

3. Normalize to obtain `p_NPC(m_red)` and `p_INT(m_red)` and compute `Tension_GI(m_red)`.

*Metrics:*

* Relative sizes of `p_NPC(m_red)` and `p_INT(m_red)` across scenarios.
* Tension values `Tension_GI(m_red)` for each scenario.
* Whether hierarchy violating scenarios produce higher tension than hierarchy preserving ones.

*Falsification conditions:*

* If hierarchy collapsing reductions yield low `Tension_GI` and high `p_NPC` without any increase in `p_INT`, the encoding is misaligned with standard complexity beliefs and is rejected.
* If all reduction scenarios produce almost identical evidence vectors and tension values, the encoding fails to distinguish structurally different worlds and is rejected.

*Semantics implementation note:*
All reductions are treated as discrete objects in the encoding. No continuous approximations are introduced.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. This experiment only tests whether the GI tension encoding respects widely accepted meta results.

---

## 7. AI and WFGY engineering spec

This block describes how Q055 can be used as an engineering module for AI systems within WFGY, at the effective layer.

### 7.1 Training signals

1. `signal_GI_consistency_score`

   * Definition: a signal derived from `Tension_GI(m)` for contexts where the model makes claims about the complexity of GI or related problems.
   * Purpose: penalize internal states that reflect self contradictory views about GI complexity.

2. `signal_P_vs_INT_balance`

   * Definition: a signal based on `DeltaS_P_INT(m)`, encouraging the model to commit to a coherent story about whether its current reasoning leans toward P like or intermediate like interpretations.
   * Purpose: discourage answers that mix incompatible assumptions.

3. `signal_reduction_awareness`

   * Definition: a signal that increases when the model proposes reductions that contradict known hierarchy constraints while still asserting low tension.
   * Purpose: align model reasoning about GI with standard complexity meta results.

### 7.2 Architectural patterns

1. `GI_Complexity_Profile_Head`

   * Role: given the internal representation of a conversation about GI, produce an estimated evidence vector `(p_P, p_NPC, p_INT)` and `Tension_GI(m)`.
   * Interface: input is a latent embedding of the dialogue; outputs are four scalars and auxiliary explanations.

2. `Reduction_Constraint_Checker`

   * Role: inspect candidate claims about GI related reductions and assign a consistency score based on known hierarchy constraints.
   * Interface: input is a structured representation of a proposed reduction; output is a discrete label or score indicating plausible, unknown, or conflict.

### 7.3 Evaluation harness

1. Task selection

   * Choose question sets about GI complexity, including:

     * basic facts and standard beliefs,
     * hypothetical scenarios involving new algorithms,
     * hypothetical reductions and their consequences.

2. Conditions

   * Baseline: model without GI specific heads or signals.
   * TU based: model with GI complexity heads and training signals active.

3. Metrics

   * Accuracy on factual questions about GI and its relation to P, NP, and NP complete problems.
   * Internal consistency across different parts of the conversation (for example avoiding claiming that GI is believed NP complete while also claiming that such a result would be surprising and unsupported).
   * Quality of explanations for why certain scenarios increase or decrease `Tension_GI`.

### 7.4 60 second reproduction protocol

A minimal protocol for external users to observe the effect of GI tension encoding.

* Baseline setup

  * Prompt: ask the AI to explain the status of graph isomorphism and why it is considered different from typical NP complete problems.
  * Observation: record the explanation, focusing on whether it mixes informal claims or misses key hierarchy constraints.

* TU encoded setup

  * Prompt: same question, plus an instruction to use “GI complexity tension” and an internal evidence vector `(p_P, p_NPC, p_INT)` when organizing the explanation.
  * Observation: record whether the answer becomes more structured, explicitly addressing the three hypotheses.

* Comparison metric

  * Rate both answers on coherence, coverage of key arguments, and explicit tracking of which hypothesis is being discussed.
  * Optionally ask independent reviewers which answer better matches the actual state of knowledge in complexity theory.

* What to log

  * Prompts, outputs, and any intermediate GI tension scores produced by the model.
  * This allows external review without exposing internal TU generative rules.

---

## 8. Cross problem transfer template

### 8.1 Reusable components produced by this problem

1. ComponentName: `GI_EvidenceVector_Encoder`

   * Type: ai_module

   * Minimal interface:

     * Inputs: textual or symbolic context about the graph isomorphism problem.
     * Outputs: discrete scores `(p_P, p_NPC, p_INT)` and `Tension_GI(m)`.

   * Preconditions:

     * The input must specify which aspects of GI are being discussed, so that the encoder can focus on complexity status rather than general graph theory.

2. ComponentName: `ComplexityTensionFunctional_Generic`

   * Type: functional

   * Minimal interface:

     * Inputs: a small number of normalized evidence scores for competing hypotheses about a problem.
     * Output: a single scalar tension value analogous to `Tension_GI(m)`.

   * Preconditions:

     * Evidence scores must be pre normalized to a common scale and must be interpretable as relative support levels.

### 8.2 Direct reuse targets

1. Q020 (P versus NP)

   * Reused component: `ComplexityTensionFunctional_Generic`.
   * Why it transfers: P versus NP can be encoded using a similar small set of competing hypotheses and evidence measures.
   * What changes: the specific evidence dimensions and normalization rules reflect different algorithmic and lower bound landscapes.

2. Q022 (Average case complexity)

   * Reused component: `GI_EvidenceVector_Encoder` as a pattern.
   * Why it transfers: the idea of encoding multiple competing hypotheses and their evidence generalizes to discussions about average case versus worst case complexity.
   * What changes: the hypotheses and observables focus on distributional hardness rather than classification of a single problem.

3. Q056 (Strong circuit lower bounds)

   * Reused component: `ComplexityTensionFunctional_Generic`.
   * Why it transfers: Q056 also involves competing hypotheses about feasibility of certain lower bounds and their consequences for complexity classes.
   * What changes: evidence scores now measure strength of known lower bounds, barriers, and meta complexity results.

---

## 9. TU roadmap and verification levels

### 9.1 Current levels

* E_level: E1

  * The GI complexity tension encoding has been specified at the level of state space, observables, and a core tension functional.
  * Two discriminating experiments have been outlined, with falsification conditions that can reject unstable or misaligned encodings.

* N_level: N1

  * The narrative framing distinguishes P, intermediate, and NP complete hypotheses and relates them to tension values.
  * Counterfactual worlds are described in a way that can be instantiated in simple model scenarios.

### 9.2 Next measurable step toward E2

To reach E2, at least one of the following should be implemented:

1. A concrete scoring scheme that maps real publications and algorithmic results about GI to approximate `p_P`, `p_NPC`, and `p_INT` values, together with a public worked example.
2. A prototype that allows users to specify hypothetical algorithm or reduction scenarios and automatically computes `Tension_GI(m)` and compares it with baseline configurations.

Both steps operate entirely at the effective layer by manipulating summaries of evidence and do not expose any deep TU generative rules.

### 9.3 Long term role in the TU program

In the long run, Q055 is expected to serve as:

* the main example of a complexity classification tension problem in the discrete domain,
* a template for encoding other candidate intermediate problems,
* a bridge between pure complexity theory narratives and AI reasoning about complexity claims.

---

## 10. Elementary but precise explanation

This block gives a non expert explanation that still matches the effective layer encoding.

The graph isomorphism problem asks:

> Given two networks with the same number of nodes, are they really the same network in disguise, just with the nodes renamed?

This is easy to state and sits inside NP, because if someone hands you a proposed renaming, you can check it quickly. The puzzle is to understand exactly how hard this problem is in the worst case.

There are three main possibilities people talk about:

1. GI is in P. There is a polynomial time algorithm that solves every instance.
2. GI is NP complete. It is as hard as the hardest problems in NP.
3. GI is intermediate. It is neither in P nor NP complete under standard assumptions.

Over many years, researchers have found very fast algorithms for many kinds of graphs and even a quasipolynomial time algorithm in general. At the same time, there are strong reasons to think that GI being NP complete would have strange consequences for other parts of complexity theory. This creates tension between different pieces of evidence.

In the Tension Universe view, we do not pick a winner. Instead, we:

* collect evidence for each of the three hypotheses,
* normalize these pieces of evidence into a small set of scores,
* combine them into a single number called `Tension_GI`.

If almost all the evidence points to one hypothesis and very little points to the others, `Tension_GI` is small. If serious evidence points in different directions, `Tension_GI` becomes large.

We then imagine three types of worlds:

* a world where GI clearly falls into P and tension is very low,
* a world where GI sits in a stable intermediate region and tension is moderate but controlled,
* a world where GI is NP complete, yet that choice fights with other complexity beliefs and the tension cannot be made small.

This does not decide which world is real. Instead, it gives us a precise way to talk about how “confused” or “coherent” our current understanding is, and a way to test whether a proposed encoding of GI complexity is reasonable. Q055 is the reference node for this kind of complexity tension story in the discrete setting.
