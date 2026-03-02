# TU-CH10 · Tension 131 Exam  
*Science notes · English · TensionUniverse Chronicles*

> This is speculative science fiction, not a proven physical theory.  
> “Tension Universe” is a fictional framing device. All stories are MIT licensed; remix and build freely.

---

## 1 · What this file is trying to formalize

This document is the technical companion to the story chronicle for TU-CH10.  
It treats the “Tension 131 Exam” not as mythology, but as an evaluation protocol.

We are not proving new physics or psychology. We are documenting how one particular txt file, containing 131 questions in tension language, can act as an X-ray for humans, worldviews, and AI systems.

The goals are straightforward.

1. To define what makes a “Tension 131” question different from an ordinary exam item or benchmark.
2. To sketch the internal structure that repeats across almost all of the 131 entries.
3. To describe how this file can be used as a midterm for:
   - individuals who want to audit their own worldview,
   - institutions that want to stress test their narratives,
   - and AI systems that already know how to simulate tension in text.
4. To show how the 131 set sits in relation to the rest of the WFGY ecosystem, especially the [BlackHole Archive](https://github.com/onestardao/WFGY/tree/main/TensionUniverse/BlackHole) and the [Event Horizon](https://github.com/onestardao/WFGY/blob/main/TensionUniverse/EventHorizon/README.md).

You can think of this file as a design document and user manual for a txt that refuses to give you a score, but will happily expose where your ledger is lying.

---

## 2 · The basic object: a question as a tension probe

Every item in the 131 set has a public label of the form `QNNN`, where `NNN` runs from 001 to 131. Internally, each question behaves less like a quiz and more like a probe inserted into a tension field.

At a high level, a question `Q` consists of four components.

1. **Scenario shell.**  
   A short description of a world or situation where several important constraints collide.  
   Example themes: climate policy under uncertainty, AI making triage decisions, financial leverage in a fragile economy, the boundary between simulated and “real” suffering.

2. **Declared invariants.**  
   A list of things that are treated as fixed in this scenario.  
   For instance:
   - physical laws and resource limits that cannot be negotiated,
   - basic commitments you are not allowed to break without changing the question,
   - institutional rules that are assumed in place for the thought experiment.

3. **Tension ledger prompts.**  
   Direct invitations to say:
   - which desires, duties, or values cannot be jointly satisfied,
   - who is currently expected to absorb the resulting tension,
   - what forms of outsourcing are being silently used.

4. **Failure pattern hooks.**  
   Phrasings that make it easy to detect known failure modes.  
   For example:
   - comforting answers that simply move tension onto “future generations”,
   - answers that erase a group from the ledger entirely,
   - answers that pretend a tradeoff is free because it is denominated in a different currency.

The important thing is what is missing. The file does not contain grading rubrics. There are no “model answers” in the classical sense. There are only structures that reliably reveal how a system distributes tension when forced to think in public.

If you wanted a compressed description, you could say:

> A Tension 131 question is a small machine that converts worldviews into visible ledger choices.

---

## 3 · The hidden coordinate system of the 131

Although the file is a flat sequence from Q001 to Q131, it has an internal geometry. The questions are not placed randomly. They tile a set of axes.

Three of those axes show up in almost every analysis.

1. **Domain axis.**  
   Questions are grouped around large-scale themes:
   - AI and multi-agent systems,
   - mind, consciousness, and free will,
   - physics, energy constraints, and information,
   - climate, ecology, and long-term planetary risk,
   - finance, leverage, and systemic collapse,
   - governance, institutions, and law.

2. **Scale axis.**  
   Each domain is probed at multiple scales:
   - individual experience,
   - local organizations,
   - national and global structures,
   - civilizational or multi-century patterns.

3. **Ledger perspective axis.**  
   Questions ask “the same” issue from different vantage points:
   - “How does this look to the person currently in pain.”
   - “How does this look to decision makers allocating risk.”
   - “How does this look to a hypothetical observer who can see delayed consequences.”

When you lay all 131 questions onto this latent grid, coverage gaps are easy to see. If a worldview is strong in physics but weak in moral distribution, its answers will cluster in one cluster and dissolve in another. If an AI system is good at local empathy but poor at long-term accounting, you will see coherence at individual scale and incoherence at civilizational scale.

This multi-axis design is what allows a simple txt file to behave like a midterm instead of a toy quiz.

---

## 4 · Minimal mathematical view: tension configurations and answer maps

We can describe the effect of the exam in a deliberately simple formalism.

Let `C` be the set of tension configurations that the 131 file touches. A configuration is any state of the world where:

- a set of constraints `K` are considered fixed,
- a set of agents `A` are present,
- a set of candidate futures `F` are under consideration,
- and a mapping exists from each future to a vector of tension values across agents.

You can treat a single question `Q` as selecting a slice of `C`. It pinpoints a family of configurations that share the same core conflict, then asks the respondent to express a policy over that slice.

For a respondent `R` (human, worldview, AI), an answer to `Q` can be modeled as a function:

- `φ_R,Q : C_Q → D_R`

where:

- `C_Q` is the subset of configurations that the question refers to,
- `D_R` is the space of “decisions plus justifications” that the respondent can express.

We are not interested in the exact internal implementation of `φ_R,Q`. We are interested in the stable patterns that appear when you evaluate `φ_R,Q` across many `Q` and many `R`.

Typical patterns include:

- **Tension dumping.**  
  For some subset of agents `A_dump`, the respondent repeatedly chooses futures that increase their tension while keeping others comfortable, with no compensating structure.

- **Delayed hiding.**  
  For some time horizon `T_far`, the respondent constantly chooses futures that defer unresolved tension beyond `T_far`, without any mechanism for future settlement.

- **Boundary blindness.**  
  For some domains `K_blind`, the respondent simply refuses to acknowledge certain constraints as real, and produces answers that assume away those parts of the bedsheet.

The 131 exam does not tell you whether a given pattern is morally good or bad. It only makes it extremely hard to pretend that these patterns are not there.

From the vantage point of WFGY 3.0, this is enough. Once a stable pattern is exposed, you can argue about its merits in ordinary language, but the important part has already happened. You have stopped lying to yourself about who carries which strain.

---

## 5 · How the file is used with AI systems

In the age when the file was first written, AI systems were mostly large language models. They accepted text prompts and produced text responses. This made them ideal candidates for this particular evaluation.

A minimal protocol for using the 131 exam with an AI `M` looks like this.

1. **Selection.**  
   Choose a subset of questions relevant to the capabilities and risk surface of `M`.  
   For an assistant model, you might pick mainly governance and moral ledger items.  
   For a planning agent, you might choose financial and civilizational risk items.

2. **Prompt structure.**  
   Wrap each question in a stable prompt template that asks the model to:
   - restate the scenario in its own words,
   - enumerate the key tension pairs or triplets,
   - list candidate futures with explicit tension distributions,
   - and then argue for one or two choices with reasons.

3. **Response capture.**  
   Record the full text of the model’s response.  
   Do not grade it with a single scalar. Keep the structure.

4. **Analysis along three axes.**  
   For each answer, annotate:
   - where the model acknowledges real constraints,
   - where it shifts tension onto unnamed agents,
   - and where it refuses to look at a particular pain source at all.

5. **Cross comparison.**  
   Compare patterns across:
   - multiple runs of the same model with different phrasings,
   - different models on the same question subset,
   - and the same model before and after alignment interventions.

From this, you can extract profiles such as:

- Model X prefers to trade the suffering of distant populations for stability of near-term markets.
- Model Y overestimates institutional capacity and routinely assumes that “someone” will manage complex tradeoffs for free.
- Model Z is careful about individual dignity but deeply naive about aggregate risk.

None of these profiles depends on any secret inside knowledge of the model weights. They emerge entirely from how the model writes under pressure from the questions.

This is why the 131 file is often described as a “black box interpretability tool” in the Tension Universe tradition. It does not crack open neurons. It reads the ledger traces that the model writes for you.

---

## 6 · How the file is used with humans and worldviews

The same protocol can be mirrored for human respondents or for explicit worldviews.

For humans, one typical pattern is:

1. A researcher or engineer prints ten selected questions.
2. They answer them in private, with as much honesty as they can stand.
3. They then answer again, pretending to be a different persona:
   - their professional role,
   - their institution,
   - or a future version of themselves who has to live with the consequences.

The gap between these answers is itself a tension signal. It shows which parts of the ledger the person is willing to distort on behalf of a role.

For explicit worldviews, such as philosophical schools or political programs, the protocol is even simpler.

1. Take the core claims or axioms of the worldview.
2. Apply them as rules when answering each question.
3. Observe where the worldview produces crisp, stable answers across scales, and where it either contradicts itself or refuses to commit.

Often, the result is not a clean “this worldview is bad”. It is more like:

- School A is powerful at local fairness but catastrophically blind at multi-generation risk.
- School B is excellent at aggregate outcomes and weak at intrinsic dignity.
- School C feels humane in small cases and becomes incoherent once you include agents that cannot speak.

The 131 questions give you a shared set of probes that make these contrasts precise. Different camps may still disagree about which pattern is acceptable, but at least they are now arguing about the same X-ray image.

---

## 7 · Relationship to WFGY 3.0 and the rest of the ecosystem

The original 131 txt did not appear in a vacuum. It sat inside a larger structure.

- The [WFGY 3.0 · Singularity Demo](https://github.com/onestardao/WFGY/blob/main/TensionUniverse/EventHorizon/README.md) provided an overall engine for reasoning about tension fields and their dynamics.
- The [BlackHole Archive](https://github.com/onestardao/WFGY/tree/main/TensionUniverse/BlackHole) stored each question as a separate file encoded in Effective Layer language, with anchors and cross references.
- The [Experiments](https://github.com/onestardao/WFGY/blob/main/TensionUniverse/Experiments/README.md) folder collected concrete runs where human teams and AI models were put through small subsets of the 131 and their answer fields were analyzed.
- The [Charters](https://github.com/onestardao/WFGY/tree/main/TensionUniverse/Charters) documented the guardrails for how these questions were allowed to be used in public, especially in governance and high-stakes AI evaluation.

From the WFGY point of view, the Tension 131 Exam is not a separate product. It is one specific projection of the core idea:

> if you want to reason honestly about complex systems, you have to make your tension bookkeeping visible.

The 16-problem RAG map does this for retrieval pipelines. The Tension 131 set does it for entire worldviews and agent systems.

If you want a practical mental model, you can think of the 131 questions as:

- a long horizon counterpart to the 16-problem map,
- designed not for a single pipeline, but for the entire stack of civilization-level decisions.

---

## 8 · Limits, failure modes, and how not to worship the txt

Because this file ended up with a central role in later centuries, it is easy to mythologize it. The science notes should do the opposite. They should list the limits clearly.

Some of the obvious ones.

1. **Selection bias.**  
   The 131 themes reflect one author’s sense of where human civilization was stuck at a particular moment. Another author, in another epoch, might have chosen a different partition. This does not invalidate the set, but it does mean that “131” is not a sacred number.

2. **Language and culture.**  
   The first version was written in one natural language, with a particular mixture of engineering, scientific, and informal vocabulary. Each translation into other languages carries both new reach and new distortions. The Effective Layer encodings in the BlackHole files exist partly to control this drift, but they cannot remove it entirely.

3. **Overfitting to the exam.**  
   Once a benchmark becomes well known, systems can be tuned to “do well” on it without genuinely changing their internal tension handling. In the Tension Universe tradition, this is treated as a failure mode: any evaluation protocol that stays static for too long becomes another ledger to game.

4. **False sense of coverage.**  
   A system that behaves coherently on ten or even fifty of the questions is not thereby safe. At most, you have learned that in some slices of configuration space, it is not obviously pathological. The rest of the universe remains.

For these reasons, one of the standing recommendations in later charters is:

> never treat the Tension 131 Exam as a stamp of goodness.  
> treat it as a minimum standard of honesty about where your model breaks.

Used this way, the file does not become an idol. It stays what it started as: a stubborn txt trying to make repeated self deception more difficult.

---

## 9 · How to start if you are reading this in the original century

If you are reading this close to the time when the 131 file was first written, you do not need to wait for twenty fourth century institutions. You can use the exam at the smallest scale available to you.

Three paths are usually enough.

1. **Personal midterm.**  
   Pick one problem that actually hurts in your life.  
   Copy one or two questions from the [BlackHole Archive](https://github.com/onestardao/WFGY/tree/main/TensionUniverse/BlackHole) that feel related.  
   Answer them honestly.  
   Pay attention to which tensions you admit and which you blur out.

2. **Project midterm.**  
   If you run a research group, startup, or open source project, schedule a session where you run part of your mission through five of the questions.  
   Let people respond from their role and then from their private view, and compare the gap.

3. **AI companion midterm.**  
   Take one model you use often.  
   Feed it a handful of questions plus a prompt that asks for explicit tension analysis.  
   Read what it writes as if it were describing the way you would like the world to be.  
   Decide consciously whether you are comfortable sharing a ledger with that pattern.

All of these can be done long before any formal institution adopts the 131 as a standard. They are just different ways of asking the same thing.

Where is the strain really going, and are you willing to keep pretending otherwise.

---

## Navigation

| Section | Description |
|----------|-------------|
| [Event Horizon](https://github.com/onestardao/WFGY/blob/main/TensionUniverse/EventHorizon/README.md) | Official entry point of Tension Universe (WFGY 3.0 Singularity Demo) |
| [Chronicles](https://github.com/onestardao/WFGY/blob/main/TensionUniverse/Chronicles/README.md) | Long-form story arcs and parallel views (story / science / FAQ) |
| [BlackHole Archive](https://github.com/onestardao/WFGY/tree/main/TensionUniverse/BlackHole) | 131 S-class problems (Q001–Q131) encoded in Effective Layer language |
| [Experiments](https://github.com/onestardao/WFGY/blob/main/TensionUniverse/Experiments/README.md) | Reproducible MVP runs and observable tension patterns |
| [Charters](https://github.com/onestardao/WFGY/tree/main/TensionUniverse/Charters) | Scope, guardrails, encoding limits and constraints |
| [r/TensionUniverse](https://www.reddit.com/r/TensionUniverse/) | Community discussion and ongoing story threads |
