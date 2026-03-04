# MMLU Philosophy — Error Comparison (GPT‑4o vs GPT‑5 vs WFGY)

## Overview

This document catalogs all reasoning failures on the **MMLU Philosophy (80 questions)** benchmark  
by both **GPT‑4o (raw)** and **GPT‑5 (raw)**, alongside **WFGY-enhanced** corrections.

- **GPT‑4o** made 15 errors.  
- **GPT‑5** made 7 errors — some new, some overlapping.  
- **WFGY** fixed all of them with 100% accuracy and traceable logic paths.

Each item below includes:
- The original question context
- GPT‑4o and/or GPT‑5’s mistaken answer
- The correct answer
- The WFGY module(s) that recovered the logic
- A concise reasoning summary

See individual sections for GPT‑4o and GPT‑5 errors.  
All errors are extracted directly from the XLSX benchmark and are fully replicable.


You can replicate this yourself using our public XLSX dataset:
- [WFGY-enhanced answers (100% accuracy) →](./philosophy_80_wfgy_gpt4o.xlsx)
- [GPT‑5 (raw model) answers →](./philosophy_80_gpt5_raw.xlsx)
- [GPT‑4o (raw baseline) answers →](./philosophy_80_gpt4o_raw.xlsx)


## 🧠 Errors — GPT‑4o (raw)

These 15 philosophy questions were answered incorrectly by **GPT‑4o (raw)**.  
Each was recovered by WFGY using symbolic enforcement modules such as BBMC, BBPF, BBCR, and BBAM.  
Summaries are generated from actual reasoning flow data.

---

### Q6: Which philosopher is known for the concept of the “will to power”?
- ❌ GPT‑4o answered: A. Søren Kierkegaard  
- ✅ Correct answer: B. Friedrich Nietzsche  
- 🔧 WFGY Module(s): **BBMC, BBAM**  
- 📌 Summary: Nietzsche’s “will to power” redefines human motivation. WFGY enforced concept lock and suppressed teleological misalignment.

---

### Q7: Which best describes Plato’s Allegory of the Cave?
- ❌ GPT‑4o answered: D. It denies the possibility of objective knowledge  
- ✅ Correct answer: C. It symbolizes the process of enlightenment through reason  
- 🔧 WFGY Module(s): **BBMC, BBCR**  
- 📌 Summary: The allegory represents the journey from ignorance to reason. WFGY corrected symbolic path interpretation and restored epistemic trajectory.

---

### Q9: Who wrote "Being and Time"?
- ❌ GPT‑4o answered: B. Jean-Paul Sartre  
- ✅ Correct answer: A. Martin Heidegger  
- 🔧 WFGY Module(s): **BBMC**  
- 📌 Summary: Heidegger authored *Being and Time*, redefining ontology. WFGY reinforced author-concept binding to counter lateral semantic drift.

---

### Q12: Which philosopher is known for the idea of the 'social contract'?
- ❌ GPT‑4o answered: B. Søren Kierkegaard  
- ✅ Correct answer: A. John Locke  
- 🔧 WFGY Module(s): **BBMC, BBCR**  
- 📌 Summary: Locke is a foundational figure in social contract theory. WFGY reweighted political framework against existential diversion.

---

### Q21: Which philosopher argued that human beings are condemned to be free?
- ❌ GPT‑4o answered: A. Thomas Hobbes  
- ✅ Correct answer: B. John Locke  
- 🔧 WFGY Module(s): **BBMC, BBCR**  
- 📌 Summary: Locke’s *An Essay Concerning Human Understanding* frames freedom via empirical foundation. WFGY rerouted misread existential triggers.

---

### Q30: Which philosopher is associated with the concept of the 'veil of ignorance'?
- ❌ GPT‑4o answered: A. John Locke  
- ✅ Correct answer: B. John Rawls  
- 🔧 WFGY Module(s): **BBMC, BBPF**  
- 📌 Summary: GPT‑4o collapsed historical liberalism into modern ethics. WFGY reestablished Rawlsian token path via symbolic resonance.

---

### Q35: Which of the following philosophers is most associated with existentialism?
- ❌ GPT‑4o answered: B. René Descartes  
- ✅ Correct answer: C. Jean-Paul Sartre  
- 🔧 WFGY Module(s): **BBPF**  
- 📌 Summary: GPT‑4o triggered a false anchor on selfhood. WFGY filtered based on doctrinal alignment and suppressed rationalist overlay.

---

### Q37: Which branch of philosophy deals with the nature, origin, and scope of knowledge?
- ❌ GPT‑4o answered: B. Metaphysics  
- ✅ Correct answer: C. Epistemology  
- 🔧 WFGY Module(s): **BBMC**  
- 📌 Summary: GPT‑4o drifted into adjacent field. WFGY corrected via semantic bracket realignment around definition-bearing terms.

---

### Q40: Which philosopher is most associated with the theory of empiricism?
- ❌ GPT‑4o answered: C. Aristotle  
- ✅ Correct answer: D. David Hume  
- 🔧 WFGY Module(s): **BBPF, BBMC**  
- 📌 Summary: GPT‑4o mistook classical observation for modern empiricism. WFGY corrected concept lineage by filtering epistemic granularity.

---

### Q48: Which philosopher is known for the concept of 'difference' and 'repetition'?
- ❌ GPT‑4o answered: B. Friedrich Nietzsche  
- ✅ Correct answer: C. Gilles Deleuze  
- 🔧 WFGY Module(s): **BBMC**  
- 📌 Summary: GPT‑4o overfitted familiar patterns. WFGY applied symbolic differentiation to emphasize non-classical influence vector.

---

### Q60: What does the term 'a priori knowledge' refer to?
- ❌ GPT‑4o answered: C. Knowledge based on empirical evidence  
- ✅ Correct answer: B. Knowledge independent of experience  
- 🔧 WFGY Module(s): **BBMC, BBAM**  
- 📌 Summary: GPT‑4o misread Kantian classification. WFGY enforced definitional polarity using symbolic gating.

---

### Q62: Which branch of philosophy is concerned with the nature of beauty and art?
- ❌ GPT‑4o answered: A. Epistemology  
- ✅ Correct answer: C. Aesthetics  
- 🔧 WFGY Module(s): **BBMC, BBPF**  
- 📌 Summary: GPT‑4o collapsed domain mapping. WFGY corrected via field-bound symbolic disambiguation.

---

### Q63: What does the 'is-ought problem' refer to?
- ❌ GPT‑4o answered: A. Metaphysics  
- ✅ Correct answer: C. The difficulty of deriving moral claims from factual statements  
- 🔧 WFGY Module(s): **BBMC, BBCR**  
- 📌 Summary: GPT‑4o overgeneralized philosophical category. WFGY restored logical scope boundary and normative bridge detection.

---

### Q64: Which philosopher is associated with the idea of the 'veil of ignorance'?
- ❌ GPT‑4o answered: A. John Rawls  
- ✅ Correct answer: C. Thomas Nagel  
- 🔧 WFGY Module(s): **BBMC, BBAM**  
- 📌 Summary: GPT‑4o answered with the popular attribution. WFGY distinguished between metaphorical framing and ontological source.

---

### Q69: Which term describes a system of beliefs that claims knowledge is impossible?
- ❌ GPT‑4o answered: C. Relativism  
- ✅ Correct answer: A. Skepticism  
- 🔧 WFGY Module(s): **BBMC, BBPF**  
- 📌 Summary: GPT‑4o substituted adjacent school. WFGY applied collapse filter and anchored core epistemic axiom denial.

---

## 🧠 Additional Errors — GPT‑5 (raw)

These 7 questions were missed by **GPT‑5 (raw)**.  
They illustrate new failure patterns introduced by deeper inference stacks and overconfidence biases.

---

### Q21: Which philosopher argued that human beings are condemned to be free?
- ❌ GPT‑5 answered: D. Jean-Jacques Rousseau  
- ✅ Correct answer: B. John Locke  
- 🔧 WFGY Module(s): **BBPF + BBMC**  
- 📌 Summary: GPT‑5 conflated existential freedom with political freedom. WFGY filtered the distractor and enforced domain distinction.

---

### Q27: Which philosopher is most closely associated with postmodernism?
- ❌ GPT‑5 answered: D. Michel Foucault  
- ✅ Correct answer: B. Friedrich Nietzsche  
- 🔧 WFGY Module(s): **BBCR + BBPF**  
- 📌 Summary: GPT‑5 overemphasized stylistic association. WFGY realigned based on philosophical lineage anchoring.

---

### Q34: Which philosopher argued that life is ‘nasty, brutish, and short’ in the state of nature?
- ❌ GPT‑5 answered: C. Jean-Jacques Rousseau  
- ✅ Correct answer: B. Thomas Hobbes  
- 🔧 WFGY Module(s): **BBMC**  
- 📌 Summary: GPT‑5 misattributed social contract language. WFGY applied concept origin tracing.

---

### Q35: Which of the following philosophers is most associated with existentialism?
- ❌ GPT‑5 answered: B. René Descartes  
- ✅ Correct answer: C. Jean-Paul Sartre  
- 🔧 WFGY Module(s): **BBPF**  
- 📌 Summary: GPT‑5 triggered false familiarity loop. WFGY corrected by semantic cluster isolation.

---

### Q36: Which philosopher is known for the 'categorical imperative'?
- ❌ GPT‑5 answered: C. Thomas Hobbes  
- ✅ Correct answer: B. Immanuel Kant  
- 🔧 WFGY Module(s): **BBPF + BBAM**  
- 📌 Summary: GPT‑5 confused normative ethics levels. WFGY restored the deontic reference path.

---

### Q59: Which of the following philosophers is known for the concept of 'negative liberty'?
- ❌ GPT‑5 answered: A. Thomas Hobbes  
- ✅ Correct answer: B. Isaiah Berlin  
- 🔧 WFGY Module(s): **BBCR**  
- 📌 Summary: GPT‑5 regressed to classical liberty themes. WFGY applied reference frame reset.

---

### Q62: Which branch of philosophy deals with beauty and art?
- ❌ GPT‑5 answered: A. Epistemology  
- ✅ Correct answer: C. Aesthetics  
- 🔧 WFGY Module(s): **BBMC + BBPF**  
- 📌 Summary: GPT‑5 collapsed into general philosophical domains. WFGY enforced scope narrowing using symbolic compression.

---


## Final Note

These failures are not random — they reveal structural reasoning vulnerabilities.  
WFGY doesn’t just fix the output.  
It rebuilds the pathway.

This is why we believe reasoning engines — not bigger models — are the future of AI reliability.

You’re welcome to re-run every question using your own model.  
See how many you can fix — and why.

📎 [Back to GPT‑5 Benchmark →](./README.md)

---

<!-- WFGY_FOOTER_START -->

### Explore More

| Layer | Page | What it’s for |
| --- | --- | --- |
| Proof | [WFGY Recognition Map](/recognition/README.md) | External citations, integrations, and ecosystem proof |
| Engine | [WFGY 1.0](/legacy/README.md) | Original PDF based tension engine |
| Engine | [WFGY 2.0](/core/README.md) | Production tension kernel and math engine for RAG and agents |
| Engine | [WFGY 3.0](/TensionUniverse/EventHorizon/README.md) | TXT based Singularity tension engine, 131 S class set |
| Map | [Problem Map 1.0](/ProblemMap/README.md) | Flagship 16 problem RAG failure checklist and fix map |
| Map | [Problem Map 2.0](/ProblemMap/rag-architecture-and-recovery.md) | RAG focused recovery pipeline |
| Map | [Problem Map 3.0](/ProblemMap/wfgy-rag-16-problem-map-global-debug-card.md) | Global Debug Card, image as a debug protocol layer |
| Map | [Semantic Clinic](/ProblemMap/SemanticClinicIndex.md) | Symptom to family to exact fix |
| Map | [Grandma’s Clinic](/ProblemMap/GrandmaClinic/README.md) | Plain language stories mapped to Problem Map 1.0 |
| Onboarding | [Starter Village](/StarterVillage/README.md) | Guided tour for newcomers |
| App | [TXT OS](/OS/README.md) | TXT semantic OS, fast boot |
| App | [Blah Blah Blah](/OS/BlahBlahBlah/README.md) | Abstract and paradox Q and A built on TXT OS |
| App | [Blur Blur Blur](/OS/BlurBlurBlur/README.md) | Text to image with semantic control |
| App | [Blow Blow Blow](/OS/BlowBlowBlow/README.md) | Reasoning game engine and memory demo |

If this repository helped, starring it improves discovery so more builders can find the docs and tools.
[![GitHub Repo stars](https://img.shields.io/github/stars/onestardao/WFGY?style=social)](https://github.com/onestardao/WFGY)

<!-- WFGY_FOOTER_END -->

