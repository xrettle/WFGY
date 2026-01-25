# Q069 · Reaction selectivity rules in complex multi-pathway chemistry

## 0. Header metadata

```txt
ID: Q069
Code: BH_CHEM_SELECTIVITY_RULES_L3_069
Domain: Chemistry
Family: Reaction selectivity and design
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

In many realistic chemical settings, a single set of starting materials and conditions can evolve through several competing reaction pathways. These may lead to different products, regioisomers, stereoisomers, or even entirely different reaction manifolds. The observed outcome is a branching pattern of products, often summarized as:

```txt
p_e  >= 0  for each channel e
sum over e of p_e  =  1
```

where `p_e` are branching fractions for the available channels.

Classical physical organic chemistry provides a collection of tools to reason about such selectivity:

* Hammond postulate and related structure–energy relations.
* Transition state theory and free energy landscapes.
* Curtin–Hammett principle.
* Linear free energy relationships and substituent effects.
* Solvent effects, medium effects, and catalysis.

However, in complex multi-pathway chemistry, especially with:

* strongly correlated electronic structure,
* coupled reaction networks,
* heterogeneous or non-equilibrium environments,
* microreactor or flow geometries,

it is unclear whether there exists a finite, transferable, and robust set of “selectivity rules” that can:

1. Predict product distributions across large families of reactions and conditions.
2. Explain when kinetic vs thermodynamic control dominates.
3. Describe how small changes in environment or structure move the system across qualitatively different selectivity regimes.

The canonical problem for Q069 is:

> Determine whether there exists a coherent and predictive theory of reaction selectivity in complex multi-pathway systems that:
>
> * unifies known mechanistic and thermodynamic principles,
> * remains valid under strongly driven and networked conditions,
> * and yields robust, falsifiable rules for how branching patterns respond to controllable knobs.

This is not a single equation to solve, but a conceptual and structural problem about the ultimate nature and limits of selectivity rules.

### 1.2 Status and difficulty

Current knowledge includes:

* Detailed mechanistic studies for many specific reaction classes.
* Successful, but often local, rules of thumb for regioselectivity, chemoselectivity, and stereoselectivity.
* High-level frameworks like Curtin–Hammett, Hammond, and energy surface diagrams.
* Data-driven and machine learning approaches that can fit selectivity behavior in restricted chemical spaces.
* Microreactor and high-throughput methods that can map branching patterns across condition grids.

Despite this, several gaps remain:

1. **Lack of global theory**

   There is no generally accepted framework that:

   * scales from small, well-studied reactions to large, strongly coupled networks,
   * handles solvent, medium, and catalyst effects in a unified way,
   * and predicts when selectivity is robust vs highly fragile.

2. **Non-equilibrium and network effects**

   Many important systems operate far from equilibrium, with:

   * continuous flow,
   * feedback loops,
   * autocatalytic channels,
   * or spatial heterogeneity.

   Classical equilibrium-inspired selectivity arguments often fail or become ambiguous in these regimes.

3. **Strong correlation and condensed-phase complexity**

   In strongly correlated electronic systems and dense phases, the notion of a single well-defined transition state may be inadequate, and the mapping from microscopic structure to macroscopic selectivity is unclear.

4. **Experimental and modeling limitations**

   Even when high-throughput data exist, the extraction of general rules from branching landscapes is ad hoc, and many potential rules are not phrased in a way that allows clear falsification.

For these reasons, Q069 is treated here as an open S-rank problem about the ultimate form and limits of reaction selectivity rules in complex, realistic multi-pathway chemistry.

### 1.3 Role in the BlackHole project

Within the BlackHole S-problem collection, Q069:

1. Serves as the primary node for **thermodynamic_tension** in chemical selectivity, where:

   * branching fractions,
   * kinetic parameters,
   * and environmental controls

   must fit together into a coherent picture.

2. Provides the selectivity layer that connects:

   * the nature of chemical bonding and electronic structure (Q061),
   * catalyst design and performance (Q062),
   * electrochemical and driven environments (Q066, Q067),

   to higher-level network and prebiotic questions (Q068, Q071).

3. Defines reusable TU components:

   * selectivity mismatch and robustness observables,
   * selectivity tension functionals,
   * counterfactual selectivity worlds,

   which will be used by prebiotic network problems, metabolic core problems, and AI planning for chemical synthesis.

### References

1. F. A. Carey and R. J. Sundberg, “Advanced Organic Chemistry, Part A: Structure and Mechanisms”, 5th edition, Springer, 2007.
2. E. V. Anslyn and D. A. Dougherty, “Modern Physical Organic Chemistry”, University Science Books, 2006.
3. S. V. Ley and I. R. Baxendale, “New tools and concepts for modern organic synthesis”, Organic and Biomolecular Chemistry, 2002.
4. P. T. Anastas and J. C. Warner, “Green Chemistry: Theory and Practice”, Oxford University Press, 1998, chapters on selectivity and reaction design under realistic conditions.

---

## 2. Position in the BlackHole graph

This block records how Q069 is positioned in the BlackHole graph and how it connects to other S-problems. Each edge has a one-line reason pointing to a concrete component or tension concept.

### 2.1 Upstream problems

These problems provide prerequisites, tools, or structural inputs for Q069.

* Q061 (BH_CHEM_BOND_NATURE_L3_061)
  Reason: supplies effective bonding and electronic structure descriptors that determine feasible pathways and approximate barrier patterns used in the selectivity encoding.

* Q062 (BH_CHEM_CATALYST_DESIGN_L3_062)
  Reason: defines catalyst-level fields and observables that act as control parameters in the selectivity landscape.

* Q066 (BH_CHEM_ELECTROCHEM_L3_066)
  Reason: contributes electrochemical and redox driving motifs that are part of the environmental descriptor for reaction selectivity.

* Q067 (BH_CHEM_QUANTUM_MOL_SIM_L3_067)
  Reason: provides coarse-grained energetic and dynamical information that constrains effective rate descriptors for competing pathways.

### 2.2 Downstream problems

These problems reuse Q069 components or depend on its selectivity structure.

* Q068 (BH_CHEM_PREBIOTIC_NETWORK_L3_068)
  Reason: reuses selectivity tension components to characterize how prebiotic reaction networks channel chemistry toward specific product sets.

* Q070 (BH_CHEM_SOFTMATTER_L3_070)
  Reason: imports branching and selectivity descriptors to describe assembly vs disassembly channel competition in soft-matter systems.

* Q071 (BH_BIO_ORIGIN_LIFE_L3_071)
  Reason: uses Q069’s selectivity fields to connect prebiotic reaction branching to emergence of proto-metabolic pathways.

* Q098 (BH_CS_AUTOCATALYTIC_ALG_L3_098)
  Reason: repurposes selectivity tension concepts for abstract autocatalytic and algorithmic branching processes.

### 2.3 Parallel problems

Parallel nodes share similar tension types and patterns but no direct component dependence.

* Q064 (BH_CHEM_GLASS_TRANS_L3_064)
  Reason: both Q064 and Q069 study how rugged landscapes and history-dependent dynamics lead to nontrivial macroscopic outcomes under thermodynamic_tension.

* Q070 (BH_CHEM_SOFTMATTER_L3_070)
  Reason: both describe complex energy and configuration landscapes where multiple pathways compete, but Q070 focuses on soft-matter structures rather than chemical reactions.

### 2.4 Cross-domain edges

Cross-domain edges connect Q069 to problems in other domains that reuse its components.

* Q031 (BH_EARTH_PLANET_ENV_L3_031)
  Reason: uses selectivity rules to map which planetary environments favor particular reaction channels relevant for geochemical and prebiotic chemistry.

* Q073 (BH_BIO_METABOLIC_CORE_L3_073)
  Reason: treats metabolic channeling as an evolved form of reaction selectivity, reusing selectivity tension and robustness observables.

* Q101 (BH_AI_CHEM_PLAN_L3_101)
  Reason: AI planning for chemical synthesis reuses Q069’s selectivity tension functional to rate and choose reaction steps and conditions.

* Q123 (BH_AI_INTERP_L3_123)
  Reason: borrows selectivity-style tension patterns to interpret branching structures in AI computation graphs and decision pathways.

---

## 3. Tension Universe encoding (effective layer)

All content in this block is confined to the effective layer. We only describe:

* state spaces,
* observables and fields,
* invariants and tension scores,
* singular sets and domain restrictions.

No deep TU generative rule or mapping from raw microscopic data to TU fields is described.

### 3.1 State space

We assume an effective state space:

```txt
M
```

with the following interpretation at the effective layer:

* Each state `m` in `M` represents a coarse-grained reaction scenario for a specific reaction family under a specified band of conditions.

For each `m` we associate:

1. A finite set of chemical species indices:

   ```txt
   S(m) = { i_1, i_2, ..., i_ns }
   ```

2. A finite set of competing reaction channels:

   ```txt
   E(m) = { e_1, e_2, ..., e_ne }
   ```

   Each `e` corresponds to a distinct product channel, regioisomer, stereoisomer, or mechanistic pathway that competes under the same starting configuration.

3. An environmental descriptor:

   ```txt
   Phi_env(m)
   ```

   summarizing controllable knobs such as solvent class, temperature band, pressure band, catalyst family, reactor geometry class (for example batch vs flow vs microreactor), and electrochemical driving regime.

4. A time-window or regime tag:

   ```txt
   Theta_regime(m)
   ```

   indicating whether the scenario is closer to kinetic control, thermodynamic control, or a mixed or driven regime at the effective level.

We do not specify how raw experimental, quantum mechanical, or simulation data are mapped to `M`. We only assume that the agent constructing the encoding can consistently produce elements of `M` that summarize relevant reaction scenarios.

### 3.2 Core observables

On `M` we define the following effective observables.

1. Branching distribution observable:

   ```txt
   p_e(m) >= 0  for e in E(m)
   sum over e in E(m) of p_e(m) = 1
   ```

   This represents the observed or encoded branching fractions among competing channels, for the starting manifold and condition band represented by `m`.

2. Effective rate descriptor:

   ```txt
   k_e_eff(m) > 0  for e in E(m)
   ```

   These are coarse-grained rate descriptors for each channel, which may combine contributions from multiple microscopic pathways. At the effective layer we treat `k_e_eff(m)` as given numbers or parameters, without specifying their derivation.

3. Environmental control vector:

   ```txt
   Phi_env(m)
   ```

   Treated as a finite-dimensional vector or tuple whose components are standardized environmental variables (for example temperature band index, solvent class code, catalyst family code, flow vs batch tag).

4. Mechanistic label observable:

   ```txt
   L_e(m)
   ```

   assigning each channel a coarse-grained mechanism label (for example radical, polar, pericyclic, surface-catalyzed, electrochemical, or mixed).

All of these observables are assumed well defined and finite for all states in the regular domain described below.

### 3.3 Reference classes and fairness constraints

To avoid tunable encodings that simply “fit” any data, we define admissible reference classes and constraints for Q069.

1. Reference branching profiles

   For each reaction family type and channel set `E(m)` we define a reference branching profile:

   ```txt
   p_ref_e(m)
   ```

   subject to:

   * `p_ref_e(m) >= 0` for all e in E(m),
   * `sum over e of p_ref_e(m) = 1` for each m,
   * `p_ref_e(m)` is determined by a fixed rule that uses only:

     * generic mechanistic archetypes,
     * simple structural descriptors of the substrates,
     * coarse Phi_env(m),

     and does not depend on the specific observed `p_e(m)` of that state.

   This family of rules is called the selectivity reference ensemble:

   ```txt
   R_sel
   ```

   and is fixed for a given encoding class.

2. Admissible environment perturbations

   For each `m` we define a finite set of admissible small perturbations:

   ```txt
   U_env(m) = { u_1, u_2, ..., u_nu }
   ```

   where each `u` is a prescribed change in Phi_env(m) that stays within the same broad regime (for example small temperature shift, similar solvent polarity class, slightly modified catalyst loading). The construction of `U_env(m)` is specified by a fixed rule that does not look at `p_e(m)`.

3. Encoding class

   An admissible encoding class for Q069 is defined by:

   * a fixed reference ensemble `R_sel`,
   * a fixed perturbation rule for `U_env(m)`,
   * fixed weights `b_sel`, `b_rob`, `b_mech` with

     ```txt
     b_sel >= 0,  b_rob >= 0,  b_mech >= 0
     b_sel + b_rob + b_mech = 1
     ```

   These choices must be made before any particular dataset is evaluated and must be used consistently across all states and experiments within that encoding class.

### 3.4 Mismatch observables

Using the observables and reference classes above, we define three mismatch observables.

1. Selectivity mismatch:

   ```txt
   DeltaS_sel(m) =
     sum over e in E(m) of
       | p_e(m) - p_ref_e(m) |
   ```

   where `p_ref_e(m)` is taken from `R_sel` for the corresponding channel set and reaction family. This is a nonnegative scalar:

   ```txt
   DeltaS_sel(m) >= 0
   ```

   and `DeltaS_sel(m) = 0` if and only if the branching distribution matches the reference profile exactly.

2. Robustness mismatch:

   Let `m[u]` denote the state obtained from `m` by applying perturbation `u` in `U_env(m)` to Phi_env(m), while keeping the starting manifold and channel set the same at the effective layer. We define:

   ```txt
   DeltaS_robust(m) =
     max over u in U_env(m) of
       sum over e in E(m) of
         | p_e(m[u]) - p_e(m) |
   ```

   This measures how sensitive the branching distribution is to small, admissible environmental changes. We have:

   ```txt
   DeltaS_robust(m) >= 0
   ```

   and `DeltaS_robust(m) = 0` only when branching fractions are invariant under the chosen perturbations.

3. Mechanistic consistency mismatch:

   For each channel `e`, let `p_class_ref_e(m)` be a coarse prediction derived from mechanistic label `L_e(m)` and environment `Phi_env(m)`, using only generic knowledge about that mechanistic class. We define:

   ```txt
   DeltaS_mech(m) =
     sum over e in E(m) of
       | p_e(m) - p_class_ref_e(m) |
   ```

   This measures how consistent the observed selectivity is with the declared mechanism tags. Again:

   ```txt
   DeltaS_mech(m) >= 0
   ```

   and it becomes small when the mechanistic labels meaningfully predict which channels dominate.

All three mismatch observables are defined without using deeper TU generative rules. They rely only on the effective observables and fixed reference rules specified by the encoding class.

### 3.5 Combined selectivity tension and tensor

We define a combined selectivity tension:

```txt
DeltaS_selectivity(m) =
  b_sel  * DeltaS_sel(m)
+ b_rob  * DeltaS_robust(m)
+ b_mech * DeltaS_mech(m)
```

where `b_sel`, `b_rob`, and `b_mech` satisfy the constraints in section 3.3 and are fixed for a given encoding class.

By construction:

```txt
DeltaS_selectivity(m) >= 0
```

and it increases when selectivity is poorly aligned with reference profiles, lacks robustness, or contradicts mechanistic expectations.

We then define an effective semantic tension tensor component for Q069:

```txt
T_ij(m) =
  S_i(m) * C_j(m) * DeltaS_selectivity(m) * lambda(m) * kappa_sel
```

where:

* `S_i(m)` is a source-like factor capturing how strongly the ith semantic source component (for example a design objective or conceptual frame) is expressed in state `m`.
* `C_j(m)` is a receptivity-like factor indicating how sensitive the jth downstream component is to selectivity failures.
* `lambda(m)` is a convergence-state factor from the TU core, taking values in a fixed bounded range.
* `kappa_sel` is a coupling constant setting the overall scale of selectivity-related tension.

The indexing sets for `i` and `j` need not be specified at the effective layer, only that `T_ij(m)` is well defined and finite for `m` in the regular domain.

### 3.6 Singular set and domain restriction

We define a singular set for Q069:

```txt
S_sing_selectivity =
  { m in M : E(m) is empty
             or sum over e of p_e(m) != 1
             or any p_e(m) is undefined
             or DeltaS_sel(m) is undefined
             or DeltaS_robust(m) is undefined
             or DeltaS_mech(m) is undefined }
```

The regular domain is:

```txt
M_reg = M \ S_sing_selectivity
```

All Q069 tension analysis is restricted to `M_reg`. If, in an experiment or protocol, a state lies in `S_sing_selectivity`, any attempt to evaluate `DeltaS_selectivity(m)` is treated as “out of domain” rather than as evidence about the nature of selectivity rules.

---

## 4. Tension principle for this problem

This block states how Q069 is expressed as a tension problem within TU at the effective layer.

### 4.1 Core tension functional

The combined selectivity mismatch `DeltaS_selectivity(m)` is the core tension indicator. It encodes three aspects:

* how far observed branching is from simple reference profiles,
* how robust the branching is to small environmental changes,
* how well mechanistic labels explain the observed branching.

Low-tension states are those with:

```txt
DeltaS_selectivity(m) <= epsilon_sel
```

for some small nonnegative threshold `epsilon_sel` that is fixed in an encoding class, after choosing typical scales for mismatch observables.

High-tension states are those with:

```txt
DeltaS_selectivity(m) >= delta_sel
```

for some strictly positive `delta_sel`, also fixed per encoding class, such that `delta_sel > epsilon_sel`. The gap between `epsilon_sel` and `delta_sel` can be used as a buffer to classify ambiguous states.

### 4.2 Selectivity as a low-tension principle

At the effective layer, the existence of meaningful selectivity rules can be phrased as:

> For broad families of reactions and realistic ranges of environmental descriptors, there exist encoding classes and states in `M_reg` such that:
>
> * most practically important conditions correspond to low-tension states,
> * low-tension regions in parameter space are not isolated fine-tuned points but have finite volume under admissible perturbations.

More concretely, for a given reaction family and an admissible encoding class:

* there should exist sets of states `m_family` with:

  ```txt
  DeltaS_selectivity(m_family) <= epsilon_sel
  ```

  that persist under the perturbations in `U_env(m_family)` used in the encoding;

* these low-tension regimes should correspond to intuitive, falsifiable rules such as:

  * “this catalyst family gives high enantioselectivity over a range of temperatures”,
  * “these conditions favor one mechanistic manifold and suppress others”.

### 4.3 Failure of ruleful selectivity as persistent high tension

Conversely, for a given reaction family and admissible encoding class, if:

```txt
DeltaS_selectivity(m) >= delta_sel
```

for almost all experimentally relevant `m` in `M_reg`, even after refining environmental descriptors and adjusting reference rules within the allowed class, then the world behaves as if selectivity is ruleless or highly fragile for that family.

In such cases:

* branching distributions are not captured by simple reference profiles,
* selectivity is highly sensitive to small changes in conditions,
* mechanistic labels fail to predict which channels dominate.

At the effective layer, Q069 asks whether, and to what extent, realistic chemistry resembles the low-tension regime (ruleful selectivity) or the high-tension regime (fragile or ruleless selectivity) when properly encoded.

---

## 5. Counterfactual tension worlds

We now define two stylized counterfactual worlds for Q069, described strictly at the effective layer:

* World T: ruleful selectivity world.
* World F: ruleless or highly fragile selectivity world.

These are not claims about the real universe but tools to structure experiments and encodings.

### 5.1 World T (ruleful selectivity, low tension)

In World T:

1. For many reaction families and broad ranges of `Phi_env(m)`, there exist contiguous regions in parameter space where:

   ```txt
   DeltaS_selectivity(m_T) <= epsilon_sel
   ```

   for world-representing states `m_T`.

2. Low-tension regions correspond to simple, transferable rules:

   * for example, “electron-rich aromatic substitution under these conditions is para-selective”,
   * or “this catalyst enforces one enantiomer over a band of temperatures and solvents”.

3. Robustness is intrinsic:

   * within the admissible perturbation set `U_env(m_T)`, selectivity patterns change smoothly,
   * `DeltaS_robust(m_T)` remains small for most states in low-tension regions.

4. Mechanistic labels have predictive power:

   * `DeltaS_mech(m_T)` is small where mechanistic tags are well assigned,
   * conflicts between labels and branching are rare and easily isolated as misassignments.

World T does not claim perfect selectivity everywhere, but asserts that low-tension regions are common and structured.

### 5.2 World F (ruleless or fragile selectivity, high tension)

In World F:

1. For many reaction families, there are no substantial regions in parameter space where:

   ```txt
   DeltaS_selectivity(m_F) <= epsilon_sel
   ```

   except possibly for narrow, fine-tuned points that vanish under small perturbations.

2. Robustness is absent:

   * `DeltaS_robust(m_F)` is large for most world-representing states,
   * small changes in Phi_env(m_F) produce large, irregular changes in branching, with no clear pattern.

3. Mechanistic labels are weakly informative:

   * `DeltaS_mech(m_F)` remains high even when mechanistic tags are assigned according to best available knowledge,
   * branching behavior systematically resists explanation in terms of familiar mechanisms.

4. Experimental heuristics fail to generalize:

   * rules extracted from one corner of parameter space do not transfer to nearby regions,
   * attempts to codify rules lead to frequent contradictions when applied to new examples.

### 5.3 Interpretive note

These counterfactual worlds:

* do not construct TU internal fields from microphysics,
* do not decide which world we inhabit,
* but provide:

  * a way to interpret tension landscapes from experiments,
  * a language for discriminating between encodings that capture structured selectivity and those that do not.

---

## 6. Falsifiability and discriminating experiments

This block defines experiments and protocols that can:

* test the coherence of Q069 encodings,
* discriminate between ruleful and ruleless selectivity behaviors at the effective layer,
* provide evidence for or against particular encoding classes.

These experiments do not solve Q069. They can only falsify or support specific encodings.

### Experiment 1: High-throughput branching landscape for a benchmark reaction

*Goal:*

Map the branching fractions `p_e(m)` over a grid of environmental conditions `Phi_env(m)` for a benchmark multi-pathway reaction, then evaluate `DeltaS_selectivity(m)` to see whether low-tension regions are structured and robust.

*Setup:*

* Choose a reaction system with at least three well-characterized product channels:

  * for example, a substrate with multiple possible regioisomers and side reactions.

* Define:

  * a set of conditions `C_grid` formed by:

    * several solvent classes,
    * a temperature band,
    * a few catalyst families or loadings.

* Use a microreactor or high-throughput well-plate setup to run the reaction across `C_grid`, at suitable residence times.

*Protocol:*

1. For each condition setting `c` in `C_grid`, encode a state `m_c` in `M_reg` capturing:

   * the observed branching fractions `p_e(m_c)`,
   * the environmental descriptor `Phi_env(m_c)`,
   * the regime tag `Theta_regime(m_c)`.

2. For each `m_c`, compute:

   * `p_ref_e(m_c)` from the fixed reference ensemble `R_sel`,
   * `DeltaS_sel(m_c)`,
   * `DeltaS_robust(m_c)` using a prescribed perturbation rule for `U_env(m_c)`,
   * `DeltaS_mech(m_c)` from mechanistic class predictions.

3. Compute `DeltaS_selectivity(m_c)` for all `c` in `C_grid`.

4. Identify low-tension region candidates:

   ```txt
   L = { c in C_grid : DeltaS_selectivity(m_c) <= epsilon_sel }
   ```

   and analyze their geometry and connectivity in the condition space.

*Metrics:*

* Fraction of the grid `C_grid` that lies in low-tension region `L`.
* Connectivity of `L` (for example whether `L` forms clusters or disconnected points).
* Distribution of `DeltaS_robust(m_c)` within `L` and outside `L`.
* Agreement between low-tension regions and known qualitative selectivity rules (if any).

*Falsification conditions:*

* If conditions that chemists agree are:

  * highly selective,
  * robust across moderate changes in conditions,

  systematically correspond to `DeltaS_selectivity(m_c)` significantly larger than `epsilon_sel`, then the current encoding class is misaligned and considered falsified.

* If small, admissible perturbations in `Phi_env` routinely move states from low-tension to high-tension regions in ways that contradict established robustness, the definition of `U_env(m)` or the structure of `DeltaS_robust(m)` is considered inadequate.

*Semantics implementation note:*

Branching fractions, rates, and environmental variables are treated using hybrid semantics consistent with the metadata: continuous for concentration-like and thermodynamic variables, discrete for channel indices and categorical environment codes. No change in semantics type is introduced in this experiment.

*Boundary note:*

Falsifying TU encoding != solving canonical statement. This experiment can reject specific choices of `R_sel`, `U_env`, and weightings but does not decide whether a universal theory of selectivity exists.

---

### Experiment 2: Mechanism-flip selectivity and tension ridge detection

*Goal:*

Test whether the Q069 encoding detects mechanistic regime changes as sharp changes in `DeltaS_mech(m)` and structured increases in `DeltaS_selectivity(m)` along boundaries in condition space.

*Setup:*

* Choose a reaction system known to switch mechanisms under changes in conditions, for example:

  * a system that transitions between radical and polar pathways,
  * or a system that flips between two catalyst-controlled manifolds.

* Define a condition path `C_path` in environment space where such mechanism flips are observed or suspected, including:

  * varying temperature,
  * solvent polarity,
  * or catalyst oxidation state.

*Protocol:*

1. For each condition `c` in `C_path`, encode a state `m_c` in `M_reg` with:

   * branching fractions `p_e(m_c)`,
   * mechanistic labels `L_e(m_c)` assigned according to best current knowledge,
   * environmental descriptor `Phi_env(m_c)`.

2. Compute:

   * `DeltaS_sel(m_c)`,
   * `DeltaS_robust(m_c)` using a small perturbation set around `c`,
   * `DeltaS_mech(m_c)`,
   * combined `DeltaS_selectivity(m_c)`.

3. Plot or tabulate `DeltaS_selectivity(m_c)` along `C_path` as a function of a single path parameter (for example temperature index).

4. Identify regions where:

   * branching ratios and mechanistic assignments indicate a mechanism flip at the effective layer.

*Metrics:*

* Location and magnitude of peaks in `DeltaS_mech(m_c)` along `C_path`.
* Relationship between these peaks and known mechanism-flip points.
* Presence of “tension ridges” where `DeltaS_selectivity(m_c)` rises in a structured way near the mechanism boundary and falls back in the neighboring regimes.

*Falsification conditions:*

* If mechanism flips are unambiguously identified from classical analysis but `DeltaS_mech(m_c)` and `DeltaS_selectivity(m_c)` remain essentially flat across the boundary, the encoding fails to represent mechanistic structure and is considered falsified or incomplete.

* If `DeltaS_selectivity(m_c)` exhibits high, erratic peaks unrelated to known mechanism boundaries, and these peaks cannot be traced to misassignment or data issues, the encoding is suspected of introducing artificial tension and must be revised.

*Semantics implementation note:*

Mechanistic labels and environmental descriptors are treated as discrete fields, while branching fractions and derived mismatch observables are continuous. This is consistent with the hybrid semantics in the metadata and does not introduce any new semantics types.

*Boundary note:*

Falsifying TU encoding != solving canonical statement. Detecting or missing tension ridges around mechanism flips only tests whether the encoding respects known mechanistic structure; it does not provide a fundamental theory of selectivity.

---

## 7. AI and WFGY engineering spec

This block describes how Q069 structures can be used in AI systems within WFGY, again only at the effective layer.

### 7.1 Training signals

We define several training signals derived from Q069 observables.

1. `signal_selectivity_mismatch`

   * Definition:

     ```txt
     signal_selectivity_mismatch(m) = DeltaS_sel(m)
     ```

   * Use: penalize internal states or predictions where branching distributions deviate strongly from reference profiles for a given reaction family and environment.

2. `signal_robustness_margin`

   * Definition:

     ```txt
     signal_robustness_margin(m) = DeltaS_robust(m)
     ```

   * Use: encourage models to represent and favor reaction scenarios where selectivity is stable under small, admissible changes in conditions.

3. `signal_mechanism_consistency`

   * Definition:

     ```txt
     signal_mechanism_consistency(m) = DeltaS_mech(m)
     ```

   * Use: penalize states where declared mechanistic labels do not align with observed or predicted selectivity patterns.

4. `signal_selectivity_viability`

   * Definition:

     ```txt
     VI_sel(m) = 1 / (1 + DeltaS_selectivity(m))
     ```

   * Use: a scalar viability score used in planning or scoring, where higher values correspond to lower tension and more viable selective outcomes.

These signals do not alter the underlying generative mechanism of the AI; they provide additional loss terms or auxiliary outputs.

### 7.2 Architectural patterns

We outline architectural modules that can reuse Q069 components without exposing TU deep rules.

1. `SelectivityTensionHead`

   * Role: given internal representations of a proposed reaction scenario and conditions, outputs estimates of `p_e(m)` and `DeltaS_selectivity(m)`.

   * Interface:

     * Inputs: latent embedding of substrates, reagents, catalyst and environmental descriptors.
     * Outputs: vector of branching probabilities and scalar tension scores.

2. `ReactionScenarioEncoder`

   * Role: encodes textual or graph descriptions of reaction setups into states that approximate elements of `M`.

   * Interface:

     * Inputs: reaction description (SMILES, graphs, or natural language), condition descriptors.
     * Outputs: latent representation containing sufficient structure to feed the SelectivityTensionHead.

3. `EnvironmentEmbeddingModule`

   * Role: constructs embeddings for `Phi_env(m)` that capture meaningful chemical groupings of conditions.

   * Interface:

     * Inputs: condition descriptors such as temperature band, solvent class, reactor type.
     * Outputs: low-dimensional vectors that can be used in both prediction and tension evaluation.

### 7.3 Evaluation harness

An evaluation harness for AI systems using Q069 components can be organized as follows.

1. Task design

   * Collect benchmark sets of reactions with measured or well-characterized selectivity in complex settings:

     * regioselectivity in multi-site functionalization,
     * chemoselectivity in mixtures of reactive groups,
     * stereoselectivity in catalytic asymmetric synthesis.

2. Conditions

   * Baseline:

     * AI model trained or used without explicit Q069 modules; only task-specific loss functions.

   * TU-augmented:

     * same base model, but augmented with `SelectivityTensionHead` and Q069 training signals.

3. Metrics

   * Predictive accuracy of branching distributions `p_e(m)` under held-out conditions.
   * Consistency of predictions across small perturbations of conditions.
   * Agreement between predicted mechanistic tags and selectivity patterns.
   * Improvement in planning success rate when using `VI_sel(m)` as a planning score.

### 7.4 60-second reproduction protocol

A minimal protocol for external users to experience the effect of Q069 encoding, without revealing TU internals.

* Baseline setup:

  * Prompt an AI system:

    * “Explain which product will dominate in this multi-pathway reaction under the following conditions, and why.”

  * The user records whether the explanation:

    * clearly identifies competing channels,
    * explains environmental effects,
    * describes robustness of selectivity.

* TU-encoded setup:

  * Same reaction and conditions, but with an additional instruction:

    * “Use the idea of reaction selectivity tension, branching fractions, robustness of selectivity to condition changes, and mechanistic consistency at the effective layer to structure your answer. Do not claim to prove any new theory.”

  * The user compares whether the explanation now:

    * explicitly discusses competing pathways,
    * connects selectivity to environmental knobs,
    * indicates how robust the selectivity is likely to be.

* What to log:

  * Both prompts and full responses.
  * Any auxiliary estimates of branching fractions and qualitative tension indicators, if exposed.

This protocol does not require the user to know any TU internals but shows how Q069 concepts can organize explanations.

---

## 8. Cross problem transfer template

This block lists reusable components from Q069 and explicit reuse targets.

### 8.1 Reusable components produced by this problem

1. ComponentName: `Selectivity_TensionScore`

   * Type: functional

   * Minimal interface:

     ```txt
     Inputs:  branching distribution p_e,
              reference branching profile p_ref_e,
              environment descriptor Phi_env,
              mechanistic labels L_e
     Output:  scalar DeltaS_selectivity
     ```

   * Preconditions:

     * channel set `E(m)` is finite and nonempty,
     * branching distribution is normalized,
     * reference profiles and mechanistic class rules are defined for the given family and environment.

2. ComponentName: `BranchingDistribution_Descriptor`

   * Type: field

   * Minimal interface:

     ```txt
     Inputs:  reaction family identifier,
              channel set E,
              observed branching data,
              environment descriptor
     Output:  compact descriptor object with fields:
              { E, p_e, Phi_env, Theta_regime }
     ```

   * Preconditions:

     * enough data exist to estimate branching fractions with usable uncertainty,
     * environment descriptors are mapped to the standard Phi_env representation.

3. ComponentName: `SelectivityWorld_Template`

   * Type: experiment_pattern

   * Minimal interface:

     ```txt
     Inputs:  reaction family definition,
              encoding class (R_sel, U_env, weights),
              condition space region of interest
     Output:  pair of experiment protocols:
              World T style (ruleful selectivity),
              World F style (fragile selectivity),
              each with associated tension evaluation steps
     ```

   * Preconditions:

     * there exists a feasible experimental or simulation setup to probe branching across the chosen condition region,
     * reference rules and perturbation sets can be instantiated.

### 8.2 Direct reuse targets

1. Q068 (BH_CHEM_PREBIOTIC_NETWORK_L3_068)

   * Reused component: `Selectivity_TensionScore`, `SelectivityWorld_Template`.
   * Why it transfers: prebiotic networks involve many competing reactions where selectivity determines which building blocks accumulate; tension between channels can be described using the same functional.
   * What changes: the environment descriptors emphasize planetary and geochemical variables, and the reaction families include mineral surfaces and non-standard solvents.

2. Q070 (BH_CHEM_SOFTMATTER_L3_070)

   * Reused component: `BranchingDistribution_Descriptor`.
   * Why it transfers: soft-matter assembly involves branching between structural motifs; a descriptor for configuration branching behaves analogously to product branching.
   * What changes: channels represent morphology or phase rather than molecular products, and Phi_env includes mechanical and confinement variables.

3. Q071 (BH_BIO_ORIGIN_LIFE_L3_071)

   * Reused component: `SelectivityWorld_Template`.
   * Why it transfers: the emergence of proto-metabolism can be framed as whether specific reaction subnetworks see low-tension selectivity toward metabolically relevant compounds.
   * What changes: families focus on metabolic-like sequences, and mechanistic labels include enzyme-like catalysis when models of biocatalysis are used.

4. Q101 (BH_AI_CHEM_PLAN_L3_101)

   * Reused component: `Selectivity_TensionScore`.
   * Why it transfers: AI planners need scores to prioritize routes that are both selective and robust; `DeltaS_selectivity` can serve as such a score.
   * What changes: inputs to the functional originate from AI-predicted branching and internal environment embeddings rather than direct experiments.

---

## 9. TU roadmap and verification levels

This block documents the current verification level for Q069 and next measurable steps.

### 9.1 Current levels

* E_level: E1

  * The effective encoding has been specified:

    * state space `M`,
    * observables `p_e`, `k_e_eff`, `Phi_env`, `L_e`,
    * mismatch observables `DeltaS_sel`, `DeltaS_robust`, `DeltaS_mech`,
    * combined selectivity tension `DeltaS_selectivity`,
    * singular set `S_sing_selectivity` and domain restriction.

  * Discriminating experiments have been defined in principle but not tied to specific datasets or implementations.

* N_level: N1

  * The narrative connecting:

    * classical selectivity concepts,
    * complex multi-pathway behavior,
    * and TU tension structures

    is explicit at the effective layer but not yet calibrated against large numbers of real systems.

### 9.2 Next measurable step toward E2

To move Q069 to E2, at least one of the following should be achieved:

1. Implement a prototype that:

   * ingests real high-throughput branching data for one benchmark reaction family,
   * implements a concrete encoding class (`R_sel`, `U_env`, weights),
   * computes `DeltaS_selectivity(m)` across a condition grid,
   * publishes tension landscapes and basic analyses.

2. Design and execute a mechanism-flip experiment where:

   * data are collected along a condition path with a known mechanism switch,
   * Q069 mismatch observables are computed,
   * presence or absence of tension ridges at the mechanism boundary is documented.

### 9.3 Long-term role in TU

In the longer term, Q069 is expected to act as:

* the main node for structuring questions about selectivity in chemistry,

* a bridge between:

  * microscopic electronic and bonding descriptions (Q061, Q067),
  * macroscopic network behavior and prebiotic evolution (Q068, Q071),
  * AI systems that need to reason and plan with selectivity under uncertainty (Q101, Q123),

* a template for how thermodynamic_tension concepts can be applied in other domains where multiple pathways compete under complex environmental control.

---

## 10. Elementary but precise explanation

This block gives a non-technical explanation aligned with the effective-layer description.

In real chemistry, one set of starting materials can give several possible products. Which product dominates often depends on:

* the exact reaction conditions,
* the solvent,
* the catalyst,
* how long the reaction runs,
* and many other details.

Chemists talk about “selectivity” when one outcome is favored over others. Textbooks teach many rules for this, but in very complex situations, especially when there are many pathways and strong interactions, it is not clear if there is a simple, general theory of selectivity.

In the Tension Universe view, we do not try to build such a theory from first principles in this document. Instead, we ask:

* Can we define a number that measures how “tense” the selectivity is in a given situation?
* Can we tell when that number is low (rules work well) or high (rules fail or are very fragile)?

For each reaction scenario, we imagine a state that summarizes:

* what products are possible,
* how likely each product is,
* what the conditions are,
* which type of mechanism each pathway is thought to follow.

We then compare:

* the observed product ratios to simple reference expectations,
* how much those ratios change if we slightly change the conditions,
* how well they match what the mechanism labels would suggest.

If all three comparisons look good, the selectivity tension is low. If they look bad, the tension is high.

We then imagine two kinds of worlds:

* A “ruleful” world where many reactions, under many conditions, sit in low-tension regions, so simple rules explain and predict selectivity reliably.
* A “ruleless” or very fragile world where low-tension regions are rare, and small changes in conditions make the product mix jump unpredictably.

The real world is somewhere in between, and Q069 asks how far it leans toward one or the other, once we encode things carefully.

Q069 does not claim to solve the problem of reaction selectivity. It provides:

* a way to talk about selectivity in terms of measurable tension,
* a framework for experiments that can falsify bad encodings,
* and reusable tools that connect basic chemistry, prebiotic networks, and AI systems that need to reason about which reactions will “actually work” in complicated settings.
