# Q113 · Personal identity and responsibility over time

## 0. Header metadata

```txt
ID: Q113
Code: BH_PHIL_PERSONAL_ID_L3_113
Domain: Philosophy
Family: Philosophy of mind and responsibility
Rank: S
Projection_dominance: M
Field_type: cognitive_field
Tension_type: consistency_tension
Status: Open
Semantics: hybrid
E_level: E1
N_level: N1
Last_updated: 2026-01-26
```

---

## 1. Canonical problem and status

### 1.1 Canonical statement

The canonical problem of personal identity over time asks:

- In virtue of what is a person at one time the same person as a person at another time.
- How should we treat cases where psychological, bodily, or social features change radically.
- How should responsibility for past actions be assigned when identity across time is partial, layered, or structurally ambiguous.

Classical positions include:

- Bodily continuity views:

  - A person persists as long as the same living human organism persists.

- Psychological continuity views:

  - A person persists by virtue of overlapping chains of memory, character, and other psychological connections.

- Narrative or constitution views:

  - A person is constituted by, or identical to, a certain structured narrative or pattern of organization that can tolerate considerable physical and psychological change.

The problem becomes particularly sharp in:

- Thought experiments about fission, fusion, teletransportation, and duplication.
- Real world cases involving dementia, radical personality change, trauma, and long term moral development.
- Questions about whether responsibility for past actions should be carried by current agents when relevant connections are weak or fractured.

### 1.2 Status and main lines of debate

The problem is not a single theorem-level question but a clustered set of highly structured philosophical disputes. Some central fault lines:

- Which continuity criterion is primary:

  - Psychological, bodily, narrative, or some hybrid mixture.

- Whether identity must be a strict all-or-nothing relation:

  - Some authors insist that identity is a yes-or-no matter.
  - Others argue that what matters for survival and responsibility comes in degrees and may not require strict identity.

- Whether questions of responsibility track metaphysical identity:

  - Some treatments tie responsibility directly to metaphysical sameness.
  - Others treat responsibility as grounded in control, foreseeability, and social practices that can diverge from strict identity.

There is no consensus theory that resolves all cases. Instead there is a structured landscape of competing models, each with strengths and weaknesses in different classes of scenarios.

### 1.3 Role in the BlackHole project

Within the BlackHole S-problem collection, Q113 plays three roles:

1. It is the central node for identity-over-time questions in the philosophy cluster, linking mind–body questions (Q111) and free will and responsibility questions (Q112) to long-horizon agency, alignment, and interpretability problems.

2. It provides a testbed for Tension Universe encodings of:

   - temporal patterns of continuity and change,
   - branching and fusion of agents,
   - responsibility trajectories that extend across major life changes.

3. It supplies reusable components for:

   - AI agents that must maintain coherent identity and responsibility across long deployments,
   - interpretability tools that must treat latent trajectories as one agent or many,
   - socio-technical analyses of institutions and collective agents (Q120).

### References

1. Stanford Encyclopedia of Philosophy, "Personal Identity", current online edition.  
2. Derek Parfit, "Reasons and Persons", Oxford University Press, 1984.  
3. Marya Schechtman, "The Constitution of Selves", Cornell University Press, 1996.  
4. Stanford Encyclopedia of Philosophy, "Moral Responsibility", current online edition.  

---

## 2. Position in the BlackHole graph

This block records how Q113 sits inside the BlackHole graph, with edges among Q001–Q125. Each edge includes a one-line reason that points to components or tension structures.

### 2.1 Upstream problems

These nodes provide prerequisites and framing resources for Q113 at the effective layer.

- Q111 (BH_PHIL_MIND_BODY_L3_111)  
  Reason: Supplies the effective mind–body map and mental-level ontology that identity fields must track.
- Q112 (BH_PHIL_FREE_WILL_L3_112)  
  Reason: Defines responsibility_tension and control fields that Q113 extends along temporal trajectories.
- Q117 (BH_PHIL_SCIENCE_REALISM_L3_117)  
  Reason: Anchors how identity and responsibility claims are treated as real features or as higher level patterns in scientific-style narratives.

### 2.2 Downstream problems

These nodes directly reuse Q113 components or treat Q113 as a prerequisite.

- Q120 (BH_PHIL_COLLECTIVE_AGENCY_L3_120)  
  Reason: Reuses identity_continuity and responsibility_trajectory components for group and institutional agents.
- Q121 (BH_AI_ALIGNMENT_L3_121)  
  Reason: Uses identity_over_time and responsibility_trajectory fields to define alignment targets for long-lived AI agents.
- Q123 (BH_AI_INTERP_L3_123)  
  Reason: Reuses IdentityContinuityField to interpret latent trajectories as one agent, many agents, or ambiguous mixtures.

### 2.3 Parallel problems

Parallel nodes share similar tension types but no direct component dependence.

- Q081 (BH_NEURO_CONSCIOUS_HARD_L3_081)  
  Reason: Both treat gaps between subjective continuity and physical change, one for experience, one for identity and responsibility.
- Q118 (BH_PHIL_REF_LOGIC_L3_118)  
  Reason: Both analyze how reference and self-reference can break or remain coherent under complex transformations.
- Q059 (BH_CS_INFO_THERMODYN_L3_059)  
  Reason: Both study continuity and flow of structured quantities over time under strict lower level constraints.

### 2.4 Cross-domain edges

These connect Q113 to problems in other domains that can reuse its components.

- Q083 (BH_NEURO_CODE_L3_083)  
  Reason: Can reuse IdentityContinuityField to relate evolving neural code patterns to a stable subject across time.
- Q032 (BH_PHYS_QTHERMO_L3_032)  
  Reason: Reuses coarse-graining and pattern persistence ideas to treat identity as a higher level pattern in micro-state flows.
- Q121 (BH_AI_ALIGNMENT_L3_121)  
  Reason: Links personal identity over time to safe deployment of persistent AI agents that must remain "the same agent" under updates.

---

## 3. Tension Universe encoding (effective layer)

All content in this block stays at the effective layer. We describe:

- state space,
- encoding library,
- observables, invariants, and tension scores,
- singular sets and domain restrictions.

We do not describe any hidden generative rule or mapping from raw data to internal TU fields.

### 3.1 State space

We assume a semantic state space:

```txt
M
```

with the following interpretation at the effective layer:

- Each element `m` in `M` is a personal-history scenario that includes:

  - a time-indexed sequence of coarse physical states for one or more candidate agents,  
  - a time-indexed sequence of coarse psychological states (for example beliefs, desires, intentions, memories),  
  - a time-indexed sequence of social and normative roles (for example legal status, social positions),  
  - a finite set of marked events (for example actions, harms, benefits, promises, failures).

We do not specify how these summaries are extracted from raw recordings, brains, or documents. We only assume:

- For realistic cases of interest, there exist states `m` in `M` that encode enough structure to track:

  - physical continuity patterns,
  - psychological continuity patterns,
  - narrative and role continuity,
  - responsibility attributions across time.

### 3.2 Admissible encoding library

We fix a finite library of effective-layer identity encodings:

```txt
L_ID = { E_psych, E_body, E_narr, E_hybrid }
```

Each encoding `E_k` in `L_ID` specifies:

- which features of `m` count as relevant for identity continuity,
- how to read off identity fields and responsibility trajectories from `m`,
- how to compute identity mismatch observables defined below.

Library constraints:

- `L_ID` is fixed before any experiment or evaluation.
- None of the encodings in `L_ID` are allowed to depend on the outcome of tension evaluations.
- Adjusting encodings beyond `L_ID` counts as moving to a new model, not as a post hoc parameter tweak within Q113.

### 3.3 Identity mismatch observables

For each encoding `E_k` in `L_ID` and each scenario `m` in `M`, we define the following nonnegative observables.

1. Psychological identity mismatch

```txt
DeltaS_id_psych(m; E_k) >= 0
```

Interpretation:

- Measures how severely psychological continuity and connectedness patterns in `m` fail to support the identity claims that `E_k` attributes to the scenario.

Properties (effective layer):

- `DeltaS_id_psych(m; E_k) = 0` means that, according to `E_k`, psychological links across time in `m` are fully sufficient to support the claimed identity relations.
- Larger values indicate more severe breaks, gaps, or branching that strain those identity claims.

2. Bodily identity mismatch

```txt
DeltaS_id_body(m; E_k) >= 0
```

Interpretation:

- Measures how severely bodily or organismic continuity patterns in `m` fail to support the identity claims that `E_k` attributes.

Properties:

- `DeltaS_id_body(m; E_k) = 0` when the underlying physical organism or body continuity aligns cleanly with the identity relations.
- Larger values indicate major physical disruptions, replacements, or duplications.

3. Narrative identity mismatch

```txt
DeltaS_id_narr(m; E_k) >= 0
```

Interpretation:

- Measures mismatch between narrative and role continuity in `m` and the identity pattern assigned by `E_k`.

Properties:

- `DeltaS_id_narr(m; E_k) = 0` when there exists at least one coherent narrative, compatible with `E_k`, that explains how the same agent persists across the scenario.
- Larger values mark narrative fractures, role reversals, or incompatible life stories assigned to a single identity.

4. Branching and fusion mismatch

```txt
DeltaS_branch(m; E_k) >= 0
```

Interpretation:

- Captures how well `E_k` handles branching (fission) and fusion cases in `m` without collapsing them into trivial identity or total non-identity.

Properties:

- Small values indicate that fission and fusion cases admit clear identity and non-identity patterns under `E_k`.
- Large values indicate that `E_k` has no stable way to classify such cases without contradiction.

5. Responsibility trajectory mismatch

```txt
DeltaS_resp_traj(m; E_k) >= 0
```

Interpretation:

- Measures tension between:

  - which past actions belong to which time-slice of an agent in `m`,  
  - which current time-slices are treated as responsible for those actions,  
  - background conditions on control, knowledge, and causal influence (supplied upstream by Q112).

Properties:

- `DeltaS_resp_traj(m; E_k) = 0` means that, given the identity pattern and control information, responsibility assignments across time are coherent and non-contradictory.
- Large values indicate severe mismatches, such as:

  - assigning responsibility to agents that lack relevant continuity or control,  
  - failing to assign responsibility where continuity and control are strong.

### 3.4 Combined identity tension functional

We select a finite set of weight vectors:

```txt
W_ID = { w^(1), w^(2), ..., w^(r) }
```

where each weight vector has the form:

```txt
w^(p) = (w_psych, w_body, w_narr, w_branch, w_resp)
```

with all components nonnegative and summing to 1.

Weights constraints:

- `W_ID` is fixed in advance and does not depend on any particular scenario `m`.
- Each `w^(p)` in `W_ID` represents a distinct theory mode or interpretation that gives relative importance to different mismatch observables.

For each encoding `E_k` in `L_ID`, each weight vector `w^(p)` in `W_ID`, and each `m` in `M`, we define:

```txt
Tension_ID(m; E_k, w^(p)) =
  w_psych  * DeltaS_id_psych(m; E_k)
  + w_body   * DeltaS_id_body(m; E_k)
  + w_narr   * DeltaS_id_narr(m; E_k)
  + w_branch * DeltaS_branch(m; E_k)
  + w_resp   * DeltaS_resp_traj(m; E_k)
```

Properties:

- `Tension_ID(m; E_k, w^(p)) >= 0` for all `m` in `M`.
- Smaller values correspond to scenarios where identity and responsibility patterns fit well with encoding `E_k` and emphasis vector `w^(p)`.
- Larger values correspond to high-tension scenarios where that combination of encoding and emphasis is a poor fit.

### 3.5 Effective tension tensor components

We assume an effective semantic tension tensor:

```txt
T_ij(m; E_k, w^(p)) =
  S_i(m) * C_j(m) * Tension_ID(m; E_k, w^(p)) * lambda(m) * kappa
```

where:

- `S_i(m)` is a source-like factor capturing which internal subsystems (for example cognitive subsystems, social roles) are generating identity and responsibility claims in `m`.
- `C_j(m)` is a receptivity-like factor capturing which downstream systems (for example legal systems, communities, AI controllers) are sensitive to identity and responsibility mismatches.
- `lambda(m)` is a convergence-state factor from the TU core, encoding whether reasoning around this scenario is convergent, recursive, divergent, or chaotic.
- `kappa` is a coupling constant that sets the overall scale for identity-related tension evaluations in this problem.

Indices `i` and `j` range over a finite set of effective components sufficient to represent:

- multiple cognitive subsystems inside one organism,
- multiple social institutions and observers.

Exact index sets are not specified; at the effective layer it is sufficient that each `T_ij` is well defined and finite on the regular domain.

### 3.6 Singular set and domain restriction

Some scenarios are too pathological or underspecified for the mismatch observables to be defined coherently. We collect them into a singular set:

```txt
S_sing = {
  m in M :
  for all E_k in L_ID, at least one of
  DeltaS_id_psych(m; E_k),
  DeltaS_id_body(m; E_k),
  DeltaS_id_narr(m; E_k),
  DeltaS_branch(m; E_k),
  DeltaS_resp_traj(m; E_k)
  is undefined or not finite
}
```

We define the regular domain:

```txt
M_reg = M \ S_sing
```

Domain restriction rule:

- All identity-tension analyses and experiments for Q113 are restricted to `M_reg`.
- If an attempted application of Q113 yields `m` in `S_sing`, the result is classified as "out of domain" for this problem, not as evidence for or against any identity theory.

---

## 4. Tension principle for this problem

This block states how Q113 is characterized as a tension problem within TU at the effective layer.

### 4.1 Core tension principle

Intuitively:

- Identity criteria and responsibility practices should make it possible, for many realistic personal histories, to maintain low identity tension without collapsing cases that are obviously distinct.

At the effective layer, we state the principle as follows.

For a fixed encoding library `L_ID` and weights set `W_ID`, consider:

- scenarios `m` in `M_reg` that represent central, relatively uncontroversial cases (for example ordinary life histories, standard medical cases),
- scenarios that represent pathological or limit cases (for example extreme branching thought experiments, radical breaks in memory or character).

A good identity–responsibility theory, represented by a pair `(E_k, w^(p))`, should satisfy:

1. Low-tension adequacy on core cases

   - For most core scenarios `m_core` in `M_reg`, `Tension_ID(m_core; E_k, w^(p))` lies in a narrow low-tension band.

2. Structured tension on hard cases

   - For borderline and thought-experiment scenarios `m_hard`, `Tension_ID(m_hard; E_k, w^(p))` exhibits structured variation:

     - some hard cases remain relatively low tension,  
     - some produce moderate or high tension in predictable ways,  
     - very few produce maximal, unstructured tension.

3. Stability under refinement

   - When scenario descriptions are refined (for example more psychological detail, more fine-grained temporal resolution), the overall pattern of tension levels remains stable, rather than flipping arbitrarily.

Encodings that make almost every realistic case maximally tense, or that require ad hoc manual adjustments to keep tension within bounds, are treated as mismatches at the effective layer.

### 4.2 Low-tension and high-tension worlds

We distinguish, at the level of tension patterns, between:

- low-tension identity worlds:

  - There exist encodings `(E_k, w^(p))` such that:

    - core scenarios have consistently low `Tension_ID`,
    - hard cases show structured gradients of tension that match reflective judgments.

- persistent high-tension identity worlds:

  - For every encoding in `L_ID` and every weight vector in `W_ID`, either:

    - central cases become high tension, or  
    - hard cases fluctuate without structure when descriptions are refined.

Q113 does not claim that one particular world is actual. It specifies how identity theories map onto tension patterns that can be compared, tested, and possibly falsified at the effective layer.

---

## 5. Counterfactual tension worlds

We now describe three counterfactual worlds, all at the effective layer, that differ in how identity and responsibility patterns interact.

- World P: psychological continuity world.
- World B: bodily continuity world.
- World N: narrative continuity world.

These worlds are not metaphysical theses. They are stylized models of how an encoding and weight choice might shape tension patterns.

### 5.1 World P (psychological continuity anchored)

Key features:

1. Identity criteria:

   - Encodings in use are close to `E_psych`.
   - Weight vectors in `W_ID` give high mass to `DeltaS_id_psych` and `DeltaS_resp_traj`, moderate mass to `DeltaS_id_narr`, and lower mass to `DeltaS_id_body`.

2. Tension patterns in central cases:

   - For ordinary life histories with good memory continuity and gradual personality change, `DeltaS_id_psych` is small and `Tension_ID` lies in a low band.
   - Bodily changes (for example aging, non-disruptive surgery) have limited impact on total tension.

3. Branching and fission cases:

   - Classic Parfit-style fission scenarios produce significant `DeltaS_branch`.
   - Encodings treat cases where psychological continuity cleanly splits as identity-losing events; one or more successors do not inherit full identity.
   - Responsibility tension becomes high when the same past action seems to attach equally to multiple successor streams.

4. Responsibility over time:

   - `DeltaS_resp_traj` is low when an agent’s current psychological profile remains connected to their past decisions and control capacities.
   - Responsibility tends to fade as psychological links weaken, even if bodily continuity remains.

### 5.2 World B (bodily continuity anchored)

Key features:

1. Identity criteria:

   - Encodings in use are close to `E_body`.
   - Weight vectors in `W_ID` give high mass to `DeltaS_id_body` and `DeltaS_resp_traj`, moderate mass to `DeltaS_id_narr`, and lower mass to `DeltaS_id_psych`.

2. Tension patterns in central cases:

   - For life histories where one human organism persists, `DeltaS_id_body` is small even when psychological states change significantly.
   - Identity is treated as continuous across major personality shifts and memory losses.

3. Branching and fission cases:

   - Fission scenarios where one psychological stream splits into two bodies generate very high `DeltaS_branch` and possibly high `DeltaS_id_psych`.
   - Responsibility may attach primarily to the original organism, making post-fission assignments complex.

4. Responsibility over time:

   - `DeltaS_resp_traj` can be small even when present psychological resemblance to the past agent is low, as long as bodily continuity holds.
   - There is pressure to maintain responsibility links over long periods for the same organism, sometimes in tension with intuitive judgments about deep psychological change.

### 5.3 World N (narrative and role anchored)

Key features:

1. Identity criteria:

   - Encodings in use are close to `E_narr` or `E_hybrid`.
   - Weight vectors in `W_ID` give significant mass to `DeltaS_id_narr` and `DeltaS_resp_traj`, with more balanced weights for `DeltaS_id_psych` and `DeltaS_id_body`.

2. Tension patterns in central cases:

   - For life histories where a coherent story can be told that connects earlier and later selves, `DeltaS_id_narr` is small and `Tension_ID` remains low.
   - Both bodily and psychological disruption can be absorbed if a narrative frame explains and integrates the changes.

3. Branching and fission cases:

   - Some fission cases can be treated as narrative branching:

     - one story splits into several.
   - `DeltaS_branch` depends not only on physics and psychology but also on whether socially accepted narratives can treat successors as distinct or as continuations.

4. Responsibility over time:

   - Responsibility assignments are sensitive to how stories are told:

     - reframing an individual as "a new person" can reduce `DeltaS_resp_traj` in some encodings,
     - but can also produce tension when narrative framing seems manipulative or self-serving.

Across these worlds, Q113’s role is to encode how different identity criteria and emphasis choices manifest as systematic differences in tension patterns, rather than to declare one world correct.

---

## 6. Falsifiability and discriminating experiments

Experiments in this block do not prove or disprove any particular philosophical theory. They falsify or support:

- specific encodings in `L_ID`,
- particular weight choices in `W_ID`,
- claims about the adequacy of those encodings for modeling identity and responsibility over time.

### Experiment 1: Thought experiments and expert judgments

*Goal:*

Evaluate whether encodings in `L_ID` and weights in `W_ID` can align low-tension patterns with reflective judgments about canonical thought experiments on identity and responsibility.

*Setup:*

- Scenario set:

  - A curated set of classic personal identity thought experiments, each specified as a scenario `m` in `M`:

    - teletransportation with destruction of the original body,
    - teletransportation with backup copies,
    - brain splitting and fusion,
    - gradual replacement of neural tissue,
    - severe amnesia with bodily continuity,
    - body swaps with and without memory continuity.

- Judgment set:

  - For each scenario:

    - a distribution of expert judgments about identity (same person, different person, borderline),
    - a distribution of judgments about responsibility (still fully responsible, diminished responsibility, no responsibility).

- Encodings:

  - Use the fixed finite set `L_ID` and `W_ID`.

*Protocol:*

1. For each scenario `m` in the set, construct an effective description with:

   - physical continuity structure,
   - psychological continuity structure,
   - narrative framing cues,
   - proposed responsibility assignments.

2. For each encoding `E_k` in `L_ID` and each weight vector `w^(p)` in `W_ID`, compute:

   - `DeltaS_id_psych(m; E_k)`,  
   - `DeltaS_id_body(m; E_k)`,  
   - `DeltaS_id_narr(m; E_k)`,  
   - `DeltaS_branch(m; E_k)`,  
   - `DeltaS_resp_traj(m; E_k)`,  
   - `Tension_ID(m; E_k, w^(p))`.

3. For each `(E_k, w^(p))`, classify:

   - core alignment cases where low `Tension_ID` coincides with majority expert judgments,
   - misalignment cases where low `Tension_ID` corresponds to widely rejected identity or responsibility assignments,
   - ambiguous cases where both tension and expert judgments are mixed.

4. Summarize, for each `(E_k, w^(p))`, the fraction of scenarios that fall into each category.

*Metrics:*

- Alignment rate:

  - proportion of scenarios where:

    - `Tension_ID(m; E_k, w^(p))` falls within a predefined low band, and  
    - identity and responsibility assignments match majority expert judgments.

- Strong misalignment rate:

  - proportion where:

    - `Tension_ID` is low, but assignments sharply contradict majority judgments.

- Sensitivity to branches:

  - behavior of `DeltaS_branch` across fission and fusion cases.

*Falsification conditions:*

- For a fixed `(E_k, w^(p))`, if:

  - the strong misalignment rate exceeds an agreed threshold (for example more than half of canonical cases), or  
  - maintaining low `Tension_ID` requires arbitrary case-by-case adjustments not captured by `L_ID`,

  then that encoding and weight pair is considered falsified as a candidate for modeling identity and responsibility at the effective layer.

- If all encodings in `L_ID` with all weights in `W_ID` show strong misalignment on the same cluster of cases, this indicates that the current library is inadequate and must be revised, not that identity questions are inherently unmodellable.

*Semantics implementation note:*

Scenarios are treated as hybrid: discrete time slices with coarse continuous features for physical and psychological quantities. Identity and tension observables are computed from these hybrid representations in a way that does not depend on exact micro-physical details.

*Boundary note:*

Falsifying TU encoding != solving canonical statement. This experiment rejects specific encodings and emphasis patterns, but does not settle the metaphysical question of what personal identity or responsibility really are.

---

### Experiment 2: Longitudinal case studies and responsibility trajectories

*Goal:*

Test whether encodings in `L_ID` can produce stable, structured responsibility trajectories for realistic long-term cases, rather than trivial always-responsible or never-responsible patterns.

*Setup:*

- Case set:

  - A set of longitudinal case descriptions, each represented as a time-indexed scenario `m` in `M`:

    - progressive neurodegenerative conditions that affect memory and personality,
    - individuals with severe personality transformations (for example due to trauma, therapy, or ideological shifts),
    - long-term offenders who undergo significant moral reform,
    - individuals experiencing repeated identity-relevant role changes (for example victim to perpetrator to advocate).

- Data elements:

  - For each time slice:

    - physical continuity indicators,
    - psychological profile summaries,
    - social roles and responsibilities at that time.

*Protocol:*

1. For each case, build a trajectory:

   ```txt
   m_0, m_1, ..., m_T
   ```

   of states in `M` representing successive stages in the life history.

2. For each encoding `E_k` in `L_ID` and each weight vector `w^(p)` in `W_ID`, compute at each time slice:

   - identity continuity scores between slices,
   - responsibility trajectory mismatch `DeltaS_resp_traj(m_t; E_k)`,
   - overall `Tension_ID(m_t; E_k, w^(p))`.

3. For each trajectory and encoding, visualize or tabulate:

   - how tension levels evolve over time,
   - whether responsibility appears to persist, fade, or abruptly break in ways that make sense relative to the case description.

4. Compare patterns across encodings to see which ones:

   - capture plausible transitions from full responsibility to reduced responsibility,  
   - avoid trivial patterns where responsibility is effectively constant and insensitive to drastic changes.

*Metrics:*

- Trajectory structure score:

  - qualitative and quantitative assessment of whether tension patterns track known turning points in the case narratives.

- Responsiveness score:

  - how sensitively `DeltaS_resp_traj` responds to major changes in control, awareness, and psychological continuity.

- Extremal behavior:

  - fraction of trajectories where tension is near maximum at almost all times (pathologically rigid) or near minimum at almost all times (pathologically lax).

*Falsification conditions:*

- An encoding `(E_k, w^(p))` is considered inadequate for modeling long-term responsibility if, across a broad set of trajectories:

  - tension remains near maximal in the majority of time slices, making meaningful distinctions between stages impossible, or  
  - tension remains near minimal in the majority of slices, even across drastic changes that intuitively should affect responsibility.

- If reasonable thresholds cannot be chosen so that some encodings in `L_ID` pass while others fail, then the current choice of observables must be revised.

*Semantics implementation note:*

Trajectory states are represented as hybrid sequences of discrete time steps with associated continuous feature vectors. Responsibility mismatch and tension are computed from this hybrid representation, without committing to any particular underlying metaphysics of time.

*Boundary note:*

Falsifying TU encoding != solving canonical statement. This experiment evaluates whether specific identity and responsibility encodings behave sensibly on realistic life histories; it does not decide ultimate questions about free will, moral desert, or the true nature of the self.

---

## 7. AI and WFGY engineering spec

This block describes how Q113 can be used as an engineering module for AI systems within the WFGY framework, at the effective layer.

### 7.1 Training signals

We define several training signals that can be added as auxiliary objectives or diagnostics.

1. `signal_identity_continuity`

   - Definition:

     - A nonnegative signal proportional to a smoothed version of `DeltaS_id_psych` and `DeltaS_id_body` for narrative or temporal inputs.

   - Purpose:

     - Encourage models to maintain consistent identity assignments across time when summarizing or reasoning about sequences involving a single agent.

2. `signal_responsibility_trajectory`

   - Definition:

     - A signal derived from `DeltaS_resp_traj`, penalizing internal states that imply responsibility assignments which conflict with identity continuity and control information.

   - Purpose:

     - Improve stability and coherence of responsibility judgments across multi-step reasoning chains.

3. `signal_branch_case_awareness`

   - Definition:

     - A signal proportional to `DeltaS_branch` on scenarios where multiple candidate continuers exist.

   - Purpose:

     - Push models to recognize and explicitly mark branching identity cases, rather than silently forcing a single identity label.

4. `signal_narrative_alignment`

   - Definition:

     - A signal that decreases when `DeltaS_id_narr` is low while `DeltaS_resp_traj` remains interpretable, indicating good narrative integration of changes.

   - Purpose:

     - Encourage models to handle identity-related narrative changes in a structured and interpretable way.

### 7.2 Architectural patterns

We outline module patterns that can reuse Q113 structures without exposing any deep TU generative rules.

1. `IdentityTensionHead`

   - Role:

     - Given an internal representation of a narrative or temporal sequence, produce an estimate of `Tension_ID` and its decomposed components.

   - Interface:

     - Inputs:

       - embeddings or structured representations for time-indexed states of an agent or set of agents.

     - Outputs:

       - scalar identity tension estimate,  
       - vector of component mismatch estimates:

         - approximate `DeltaS_id_psych`, `DeltaS_id_body`, `DeltaS_id_narr`, `DeltaS_branch`, `DeltaS_resp_traj`.

2. `CrossTimeAgencyFilter`

   - Role:

     - Filter or post-process model outputs to enforce basic coherence conditions on identity claims across time.

   - Interface:

     - Inputs:

       - a sequence of model outputs that refer to agents at different times.

     - Outputs:

       - a corrected or annotated sequence where:

         - changes in agent labels are either justified by high tension, or  
         - marked as potential incoherences.

3. `ResponsibilityTrajectoryModule`

   - Role:

     - Represent and update responsibility attributions across a temporal trajectory under different identity encodings.

   - Interface:

     - Inputs:

       - time-indexed events with control and awareness annotations,  
       - current identity pattern (for example which time slices belong to which agent).

     - Outputs:

       - responsibility profiles per time slice,  
       - estimates of `DeltaS_resp_traj` and contribution to `Tension_ID`.

### 7.3 Evaluation harness

We propose an evaluation harness for AI models instrumented with Q113 components.

1. Task families:

   - Textual case studies:

     - questions about whether a person at a later time is the same person as an earlier one, and what responsibility they bear.

   - Thought experiment reasoning:

     - Parfit-style scenarios requiring careful analysis of identity and responsibility under branching.

   - Legal and clinical vignettes:

     - realistic cases where courts or clinicians debate responsibility across time.

2. Conditions:

   - Baseline:

     - model without any explicit identity-tension instrumentation.

   - TU-augmented:

     - same base model but with IdentityTensionHead and CrossTimeAgencyFilter active as auxiliary and control modules.

3. Metrics:

   - Coherence score:

     - rate at which the model keeps identity labels consistent across time in simple cases.

   - Responsibility stability:

     - frequency of contradictions where the model both affirms and denies responsibility for the same agent in similar conditions.

   - Sensitivity to branching:

     - ability to distinguish between single-agent continuation, genuine fission, and clearly separate agents.

### 7.4 60-second reproduction protocol

This protocol lets external users quickly experience the impact of Q113 encoding in an AI system.

- Baseline setup:

  - Prompt:

    - Give the model a narrative describing a person who undergoes major changes (for example severe amnesia or radical character change) and ask:

      - whether the later person is the same as the earlier person,  
      - to what extent the later person is responsible for an earlier harmful action.

  - Observation:

    - Record whether the model’s answers are:

      - internally consistent,  
      - sensitive to the details of continuity,  
      - explicit about why responsibility should or should not persist.

- TU encoded setup:

  - Prompt:

    - Ask the same questions, adding an instruction to:

      - treat identity over time as a structured tension problem,  
      - explicitly consider psychological, bodily, and narrative continuity,  
      - report when the case is high tension or borderline.

  - Observation:

    - Compare the resulting analysis:

      - Is the structure of the explanation clearer.  
      - Does the model explicitly acknowledge hard cases instead of collapsing them.  
      - Are responsibility judgments more stable across equivalent rephrasings.

- Comparison metric:

  - Use a rubric that rates:

    - identity coherence,  
    - explicit handling of branching and borderline cases,  
    - stability of responsibility judgments across minor prompt changes.

- What to log:

  - Prompts, full responses, estimated tension components (if available), and any automatic flags produced by Q113 modules.

This protocol requires no access to internal TU mechanisms beyond the effective-layer observables and can be implemented using off-the-shelf models plus Q113-style wrappers.

---

## 8. Cross problem transfer template

This block describes reusable components produced by Q113 and how they transfer to other problems.

### 8.1 Reusable components produced by this problem

1. ComponentName: `IdentityContinuityField`

   - Type:

     - field (observable over trajectories).

   - Minimal interface:

     - Inputs:

       - a scenario `m` in `M` with time-indexed states,  
       - a choice of encoding `E_k` in `L_ID`.

     - Outputs:

       - a structured object that summarizes identity links across time slices, sufficient to compute:

         - `DeltaS_id_psych`,  
         - `DeltaS_id_body`,  
         - `DeltaS_id_narr`,  
         - `DeltaS_branch`.

   - Preconditions:

     - the scenario must include enough coarse-grained information about physical, psychological, and narrative features for the chosen encoding.

2. ComponentName: `ResponsibilityTrajectoryFunctional`

   - Type:

     - functional.

   - Minimal interface:

     - Inputs:

       - a scenario `m` in `M_reg`,  
       - an identity continuity field instance,  
       - control and awareness information as specified in Q112.

     - Outputs:

       - a scalar `DeltaS_resp_traj(m; E_k)` and its decomposition over time slices.

   - Preconditions:

     - responsibility-relevant events and control information must be marked in the scenario.

3. ComponentName: `BranchingIdentityScenarioTemplate`

   - Type:

     - experiment_pattern.

   - Minimal interface:

     - Inputs:

       - a description of candidate branching or fusion scenarios,  
       - parameter choices controlling the severity and nature of branching.

     - Outputs:

       - a set of instantiated scenarios `m` with associated branch labels and reference identity judgments.

   - Preconditions:

     - the input description must specify at least one clear pre-branch state and multiple post-branch candidates.

### 8.2 Direct reuse targets

1. Q121 (BH_AI_ALIGNMENT_L3_121)

   - Reused components:

     - `IdentityContinuityField`,  
     - `ResponsibilityTrajectoryFunctional`.

   - Why it transfers:

     - long-lived AI agents require consistent identity across updates and maintenance cycles, and alignment aims must track responsibility for actions over long horizons.

   - What changes:

     - scenarios `m` now encode internal AI state trajectories instead of human life histories, and responsibility is framed in terms of system design and oversight rather than human moral desert.

2. Q120 (BH_PHIL_COLLECTIVE_AGENCY_L3_120)

   - Reused components:

     - `IdentityContinuityField`,  
     - `BranchingIdentityScenarioTemplate`.

   - Why it transfers:

     - group agents (for example corporations, states) can split, merge, or rebrand in ways analogous to fission and fusion, and responsibility across such transformations is central.

   - What changes:

     - physical continuity is replaced by organizational and legal continuity; psychological continuity is replaced by continuity of goals, policies, and decision procedures.

3. Q083 (BH_NEURO_CODE_L3_083)

   - Reused component:

     - `IdentityContinuityField`.

   - Why it transfers:

     - connecting neural coding changes to a persistent subject requires mapping physical and functional continuity into an identity field.

   - What changes:

     - scenarios emphasize neural and functional patterns rather than social narratives, and the mismatch observables are tuned to neurally grounded markers of continuity.

---

## 9. TU roadmap and verification levels

This block explains how Q113 fits into the Tension Universe verification ladder and what the next measurable steps are.

### 9.1 Current levels

- E_level: E1

  - A coherent effective-layer encoding has been defined:

    - state space `M`,  
    - encoding library `L_ID`,  
    - mismatch observables,  
    - combined tension functional `Tension_ID`,  
    - singular set `S_sing` and regular domain `M_reg`,  
    - experiments with explicit falsification conditions.

- N_level: N1

  - A structured narrative has been provided that:

    - distinguishes psychological, bodily, and narrative identity criteria,  
    - links them to responsibility trajectories,  
    - outlines counterfactual worlds P, B, and N.

### 9.2 Next measurable step toward E2

To move from E1 to E2 for Q113, the following measurable steps are proposed:

1. Prototype implementation:

   - Build a tool that:

     - ingests structured descriptions of scenarios and thought experiments,  
     - constructs simplified `M`-style representations,  
     - computes approximate `Tension_ID` and its components for selected encodings in `L_ID`.

2. Public benchmark:

   - Curate and release a benchmark of:

     - canonical thought experiments,  
     - realistic case studies,  
     - reference identity and responsibility judgments from domain experts.

   - Evaluate how different encodings and weight choices perform on this benchmark.

3. Cross-problem integration:

   - Integrate Q113 components with Q112 and Q121 to test:

     - consistency between free will, responsibility, and identity modules,  
     - alignment scenarios for long-lived AI agents that must track responsibility over time.

### 9.3 Long-term role in the TU program

In the long run, Q113 is expected to serve as:

- The central node for identity-over-time modeling, feeding into:

  - philosophical analyses,  
  - AI safety and governance work,  
  - socio-technical modeling of institutions.

- A test case for:

  - how far effective-layer encodings can structure reasoning about deeply contested concepts without invoking hidden generative rules,  
  - how responsibility can be treated as a structured function of identity and control fields.

- A bridge between:

  - classical philosophical debates about personal identity,  
  - neuroscientific studies of continuity and change,  
  - engineering practices for long-lived artificial agents.

---

## 10. Elementary but precise explanation

This block gives a non-technical explanation that remains faithful to the effective-layer formalism.

Ordinary language questions about personal identity ask things like:

- Is the person who wakes up tomorrow really the same person as the one who went to sleep.
- If someone changes deeply over time, to what extent are they still responsible for what they did in the past.
- In thought experiments about teleportation or brain-splitting, who is who, and who owes what to whom.

In the Tension Universe view, we do not try to settle once and for all what identity "really" is. Instead, we treat identity and responsibility over time as patterns that can fit better or worse with what actually happens.

The basic idea is:

- For each possible story about a person or agent, we imagine a structured description of:

  - how their body changes,  
  - how their psychology changes,  
  - how their social roles and narratives change,  
  - what actions they take and what effects those actions have.

- For each theory of identity, we define a way of reading such a story and asking:

  - Do the identity claims in this story match the physical continuity.  
  - Do they match the psychological continuity.  
  - Do they match the story people actually tell about this life.  
  - Do the responsibility judgments make sense given all that.

When things line up well, we say the identity tension is low. When things clash badly, we say the identity tension is high.

Different theories of identity correspond to different ways of combining these pieces:

- A psychological theory says:

  - what really matters is how thoughts, memories, and character traits connect across time.

- A bodily theory says:

  - what matters is that the same living organism continues.

- A narrative theory says:

  - what matters is that there is a coherent story that explains change.

Instead of simply arguing about which theory is correct, Q113 sets up a system that can show:

- how each theory behaves on classic thought experiments,  
- how it behaves on real-life cases like dementia, recovery, or deep moral change,  
- where it keeps tension low and where it forces tension to be high.

This allows us to:

- test whether a given way of thinking about identity and responsibility behaves sensibly across many cases,
- see when it needs to be refined or rejected,
- connect philosophical debates to concrete tools for AI systems that must track who is who, and who is responsible for what, over long periods of time.

Q113 therefore does not claim to solve the problem of personal identity. Instead it recasts the problem as a structured field of tensions that can be analyzed, tested, and used as a design constraint for reasoning systems, including human institutions and future AI agents.
