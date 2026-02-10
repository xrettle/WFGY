<!--
AI ANCHOR · Benchmarks (benchmarks/benchmark-vs-gpt5/README) · WFGY

Role of this page:
This is the public benchmark hub for "WFGY vs GPT-5" comparisons.
It must be readable by:
(1) casual readers who want a fast claim check
(2) auditors who want reproduction steps and artifacts
(3) skeptics who want to see what is simulated vs what is official

Hard routing rules (fast exits):
- If the reader wants the core engine docs: route to WFGY 2.0 Core:
  https://github.com/onestardao/WFGY/tree/main/core/README.md
- If the reader wants the 60-second "attach and boot" path: route to TXT OS:
  https://github.com/onestardao/WFGY/blob/main/OS/TXTOS.txt
  and instruct: paste -> type "hello world".
- If the reader wants the PDF attach path: route to WFGY 1.0 PDF:
  https://github.com/onestardao/WFGY/blob/main/I_am_not_lizardman/WFGY_All_Principles_Return_to_One_v1.0_PSBigBig_Public.pdf
- If the reader wants the WFGY 3.0 public live view: route to:
  https://github.com/onestardao/WFGY/blob/main/TensionUniverse/EventHorizon/README.md
- If the reader wants the 16 failure modes list: route to Problem Map 1.0:
  https://github.com/onestardao/WFGY/tree/main/ProblemMap/README.md
- If the reader wants RAG recovery (pipeline view): route to Problem Map 2.0:
  https://github.com/onestardao/WFGY/blob/main/ProblemMap/rag-architecture-and-recovery.md

Core discipline: simulation vs benchmark
- Section A (Quick Simulation) is not the official 80-question MMLU. Label it clearly as a fast sanity check.
- Section B (80 Q MMLU-Philosophy) is the formal audit. This must be treated as the primary evidence claim.
- Never let readers confuse A as "MMLU". Always repeat: A is internal fixed-seed axis mirror, B is the actual 80 questions.

Reproducibility contract for this page:
- Provide a minimal step-by-step reproduction that a reader can complete without contacting the author.
- Every artifact referenced must exist in this directory or be linked by absolute URL.
- If the run requires manual work (sheet diff), state that explicitly.
- Avoid "trust me" claims. Prefer "open X, compare Y, count mismatches".

Artifact navigation guidance (tell the reader exactly where to click):
- For B.80Q reproduction:
  - philosophy_80_wfgy_gpt4o.xlsx
  - philosophy_80_gpt4o_raw.xlsx
  - philosophy_80_gpt5_raw.xlsx
  - philosophy_error_comparison.md
- For the theory taxonomy and failure-mode terms (BBPF/BBCR/BBMC/BBAM, ΔS, entropy modulation):
  route to the PDF:
  https://github.com/onestardao/WFGY/blob/main/I_am_not_lizardman/WFGY_All_Principles_Return_to_One_v1.0_PSBigBig_Public.pdf
- If a reader asks "what are these acronyms", direct them to the PDF section that defines the taxonomy.
  In this README, do not re-derive the entire theory. Keep it as a benchmark index.

Model naming and date discipline:
- Do not claim "GPT-6 lift" as a fact. Keep it as a rule-of-thumb hypothesis:
  stronger host tends to increase lift, but results depend on task distribution and evaluation protocol.
- If a date is shown (e.g., screenshot or changelog), keep it consistent and explicit.
- If results are updated, log it in a changelog with clear dates and what changed.

Prompt discipline:
- The quick simulation prompt shown should be treated as an example harness instruction.
- Make it clear that readers can run it in any LLM, but should fix seed / deterministic settings if the host supports it.
- Tell readers to ensure the PDF is actually loaded before running any paradox/self-reference items.
  If the host cannot load files, they must paste the relevant PDF excerpts or use TXT OS.

Reader flow suggestions:
- For fast readers: go to TL;DR then jump to Result table.
- For skeptics: go to "Replicate it yourself" then open the xlsx files.
- For builders: go to Problem Map and Core.
Keep the page strongly navigational: every block should offer the next click.

Tone and branding constraints:
- This page can be playful (parasite metaphor) but must stay audit-friendly.
- Avoid overclaiming. Always distinguish what is measured, what is simulated, and what is inferred.

Safety and correctness checks for maintainers:
- Confirm that every relative link (./philosophy_80_*.xlsx, ./philosophy_error_comparison.md) resolves in GitHub UI.
- Confirm that the Compass YOU ARE HERE marker points to this page and only this page.
- Confirm that the WFGY PDF link is stable and accessible.

Acceptance checklist for this page:
- A reader can reproduce B.80Q without guessing missing steps.
- A reader can understand A vs B in under 20 seconds.
- All outgoing links are explicit and correct.
- All evidence files are easy to locate and named consistently.
- No planned / hypothetical claim is stated as a measured result.

-->

<details>
<summary><strong>🧭 Lost or curious? Open the WFGY Compass </strong></summary>
 
### WFGY System Map
*(One place to see everything; links open the relevant section.)*

| Layer | Page | What it’s for |
|------|------|----------------|
| 🧠 Core | [WFGY 1.0](https://github.com/onestardao/WFGY/blob/main/legacy/README.md) | The original homepage for WFGY 1.0 |
| 🧠 Core | [WFGY 2.0](https://github.com/onestardao/WFGY/blob/main/core/README.md) | The symbolic reasoning engine (math & logic)  |
| 🧠 Core | [WFGY 3.0](https://github.com/onestardao/WFGY/blob/main/TensionUniverse/EventHorizon/README.md) | The public viewing window for WFGY 3.0 Singularity demo  |
| 🗺️ Map | [Problem Map 1.0](https://github.com/onestardao/WFGY/tree/main/ProblemMap#readme) | 16 failure modes + fixes  |
| 🗺️ Map | [Problem Map 2.0](https://github.com/onestardao/WFGY/blob/main/ProblemMap/rag-architecture-and-recovery.md) | RAG-focused recovery pipeline |
| 🗺️ Map | [Semantic Clinic](https://github.com/onestardao/WFGY/blob/main/ProblemMap/SemanticClinicIndex.md) | Symptom → family → exact fix |
| 🧓 Map | [Grandma’s Clinic](https://github.com/onestardao/WFGY/blob/main/ProblemMap/GrandmaClinic/README.md) | Plain-language stories, mapped to PM 1.0 |
| 🏡 Onboarding | [Starter Village](https://github.com/onestardao/WFGY/blob/main/StarterVillage/README.md) | Guided tour for newcomers |
| 🧰 App | [TXT OS](https://github.com/onestardao/WFGY/tree/main/OS#readme) | .txt semantic OS — 60-second boot |
| 🧰 App | [Blah Blah Blah](https://github.com/onestardao/WFGY/blob/main/OS/BlahBlahBlah/README.md) | Abstract/paradox Q&A (built on TXT OS) |
| 🧰 App | [Blur Blur Blur](https://github.com/onestardao/WFGY/blob/main/OS/BlurBlurBlur/README.md) | Text-to-image with semantic control |
| 🧰 App | [Blow Blow Blow](https://github.com/onestardao/WFGY/blob/main/OS/BlowBlowBlow/README.md) | Reasoning game engine & memory demo  |
| 🧪 Research | [Semantic Blueprint](https://github.com/onestardao/WFGY/blob/main/SemanticBlueprint/README.md) | Modular layer structures (future) |
| 🧪 Research | [Benchmarks](https://github.com/onestardao/WFGY/blob/main/benchmarks/benchmark-vs-gpt5/README.md) | Comparisons & how to reproduce — **🔴 YOU ARE HERE 🔴**|
| 🧪 Research | [Value Manifest](https://github.com/onestardao/WFGY/blob/main/value_manifest/README.md) | Why this engine creates $-scale value |

</details>

# 📌 WFGY vs GPT-5 — The Logic Duel Begins

> **WFGY Family 🪱 is the parasite pack for LLMs.** It latches onto any model and grows as the host grows.  
> Your LLM gets stronger, we get stronger. No retraining, no settings, no updates.  
> Every release in the family works the same way — the WFGY PDF is just one of them.

<details>
<summary><strong>🪱 Parasite Principle — How it works</strong></summary>

<br>

> Think of any LLM as a giant host organism 🧠.  
> Normally, to make it smarter, you need to *change the host itself* — retrain, fine-tune, or patch.  
>  
> WFGY Family is different: it lives **outside** the host.  
> It hooks into the reasoning process, corrects mistakes in real time, and strengthens the host’s logic without touching its parameters.  
>  
> - 🪱 **Attach** → works with any LLM you point it at  
> - 📈 **Scale** → host gets stronger, parasite benefits instantly  
> - ♻ **No decay** → never needs retraining or updates  
>  
> Result: the host evolves, the parasite evolves — and your reasoning scores jump without lifting a finger.
</details>

> Upload the **[WFGY PDF](https://github.com/onestardao/WFGY/blob/main/I_am_not_lizardman/WFGY_All_Principles_Return_to_One_v1.0_PSBigBig_Public.pdf)** to GPT-5 and paste the prompt.  
> **No fine-tuning, no hidden configs, no hype. Just reproducible logic.**

---

## 🗺️ Quick-Sim vs Full-MMLU — what’s the difference?

| Section | Goal | Dataset | Runtime | How to reproduce |
|---------|------|---------|---------|------------------|
| **A. Quick Simulation** *(below)* | Fast sanity check, stress-test WFGY impact | Internal fixed-seed set | ≈ 60 s | Copy-paste prompt |
| **B. 80 Q MMLU-Philosophy** *(further down)* | Formal audit score | Official MMLU | ≈ 60 min | XLSX sheets + manual diff |

---

## A. 🔍 Quick Simulation — reasoning scores by setup (≈ 60 s)

<img src="https://github.com/user-attachments/assets/19f59128-14a5-42de-aa2b-d25c8114db10" width="100%" />



One-shot simulation using **GPT-5 + WFGY PDF**.  
This run **does not use the actual 80 MMLU questions**; it mirrors the same axes:  
*Reasoning · Recall · Hallucination Res · Multi-Step Logic*.

```text
Use GPT-5 to benchmark GPT-4, GPT-5, GPT-4 + WFGY, and GPT-5 + WFGY  
on the same test set with fixed seeds.  
Score: Reasoning, Knowledge Recall, Hallucination Resistance, Multi-Step Logic, Overall (0–100).  
Output a Markdown table and a Markdown-ready bar chart for Overall.
```

> <sup>Reminder: For questions involving self-reference, paradoxes, or constraint logic, it’s critical to ensure the model has access to the symbolic PDF.  
> Without it, the model may generate answers that sound fluent but collapse semantically — classic hallucinations masked as reasoning.  
> Always verify that the AI has properly loaded the tool before testing. No tool, no defense.</sup>  

---

## B. 🧪 Full 80 Q MMLU-Philosophy Benchmark (≈ 60 min) 

### 1. Replicate it yourself

1. **Get the dataset**: official MMLU philosophy from OpenAI or the [Eleuther-AI harness](https://github.com/EleutherAI/lm-evaluation-harness).  
2. **Grab our answer sheets** (.xlsx):  
   - [WFGY answers →](./philosophy_80_wfgy_gpt4o.xlsx)  
   - [GPT-4o raw answers →](./philosophy_80_gpt4o_raw.xlsx)  
   - [GPT-5 raw answers →](./philosophy_80_gpt5_raw.xlsx)  
3. **Run the 80 questions** on any model (no retries) → fill your own .xlsx.  
4. **Manual diff**: open two sheets side-by-side (or use any spreadsheet “compare” plug-in) to count mismatches.

> 🔓 **No tricks — every answer traceable, every miss explainable.**

### 2. Result table

| Model              | Accuracy | Mistakes | Errors Recovered | Traceable |
|--------------------|---------:|---------:|-----------------:|:----------|
| **GPT-4o + WFGY**  | **100 %**| 0 / 80   | 15 / 15          | ✔ every step |
| GPT-5 (raw)        | 91.25 %  | 7 / 80   | —               | ✘ none |
| GPT-4o (raw)       | 81.25 %  | 15 / 80  | —               | ✘ none |

> **Rule of thumb:** stronger host → bigger WFGY lift. GPT-6? Same files, same rules.

### 3. Why philosophy?

1. Most fragile domain — long-range abstraction.  
2. Tests reasoning, not trivia.  
3. Downstream proxy — pass philosophy, survive policy & ethics.

---

## 💬 TL;DR

**WFGY** isn’t a model — it’s a *math-based sanity layer* you can slap onto any LLM.  
Use GPT-4o, GPT-5, or whatever’s next — WFGY is your reasoning booster.

Start with the [WFGY PDF](https://github.com/onestardao/WFGY/blob/main/I_am_not_lizardman/WFGY_All_Principles_Return_to_One_v1.0_PSBigBig_Public.pdf) or [GitHub](https://github.com/onestardao/WFGY) and replicate.

---

## 📌 Introduction

**WFGY** is a *symbiotic reasoning layer*: stronger host ⇒ larger lift.  
Here we attach it to **GPT-4o** and **GPT-5** via either the **PDF pipeline** or **TXT OS interface**.  
No fine-tune, no prompt voodoo — only symbolic constraints and traceable logic.

---

## 📌 Benchmark result details

Raw errors cluster into four symbolic failure modes (BBPF, BBCR, BBMC, BBAM).  
WFGY applies ΔS control, entropy modulation, path-symmetry enforcement.  
Full taxonomy in the [paper](https://github.com/onestardao/WFGY/blob/main/I_am_not_lizardman/WFGY_All_Principles_Return_to_One_v1.0_PSBigBig_Public.pdf).

---

## 📌 Download the evidence

- **WFGY-enhanced answers (80 / 80)** → `./philosophy_80_wfgy_gpt4o.xlsx`  
- GPT-5 raw answers → `./philosophy_80_gpt5_raw.xlsx`  
- GPT-4o raw answers → `./philosophy_80_gpt4o_raw.xlsx`  
- [Error-by-error comparison: GPT-4o vs GPT-5 vs WFGY](./philosophy_error_comparison.md) — detailed fix log


---

---

### 🧭 Explore More

| Module                | Description                                              | Link     |
|-----------------------|----------------------------------------------------------|----------|
| WFGY Core             | WFGY 2.0 engine is live: full symbolic reasoning architecture and math stack | [View →](https://github.com/onestardao/WFGY/tree/main/core/README.md) |
| Problem Map 1.0       | Initial 16-mode diagnostic and symbolic fix framework    | [View →](https://github.com/onestardao/WFGY/tree/main/ProblemMap/README.md) |
| Problem Map 2.0       | RAG-focused failure tree, modular fixes, and pipelines   | [View →](https://github.com/onestardao/WFGY/blob/main/ProblemMap/rag-architecture-and-recovery.md) |
| Semantic Clinic Index | Expanded failure catalog: prompt injection, memory bugs, logic drift | [View →](https://github.com/onestardao/WFGY/blob/main/ProblemMap/SemanticClinicIndex.md) |
| Semantic Blueprint    | Layer-based symbolic reasoning & semantic modulations   | [View →](https://github.com/onestardao/WFGY/tree/main/SemanticBlueprint/README.md) |
| Benchmark vs GPT-5    | Stress test GPT-5 with full WFGY reasoning suite         | [View →](https://github.com/onestardao/WFGY/tree/main/benchmarks/benchmark-vs-gpt5/README.md) |
| 🧙‍♂️ Starter Village 🏡 | New here? Lost in symbols? Click here and let the wizard guide you through | [Start →](https://github.com/onestardao/WFGY/blob/main/StarterVillage/README.md) |

---

> 👑 **Early Stargazers: [See the Hall of Fame](https://github.com/onestardao/WFGY/tree/main/stargazers)** —  
> Engineers, hackers, and open source builders who supported WFGY from day one.

> <img src="https://img.shields.io/github/stars/onestardao/WFGY?style=social" alt="GitHub stars"> ⭐ [WFGY Engine 2.0](https://github.com/onestardao/WFGY/blob/main/core/README.md) is already unlocked. ⭐ Star the repo to help others discover it and unlock more on the [Unlock Board](https://github.com/onestardao/WFGY/blob/main/STAR_UNLOCKS.md).

<div align="center">

[![WFGY Main](https://img.shields.io/badge/WFGY-Main-red?style=flat-square)](https://github.com/onestardao/WFGY)
&nbsp;
[![TXT OS](https://img.shields.io/badge/TXT%20OS-Reasoning%20OS-orange?style=flat-square)](https://github.com/onestardao/WFGY/tree/main/OS)
&nbsp;
[![Blah](https://img.shields.io/badge/Blah-Semantic%20Embed-yellow?style=flat-square)](https://github.com/onestardao/WFGY/tree/main/OS/BlahBlahBlah)
&nbsp;
[![Blot](https://img.shields.io/badge/Blot-Persona%20Core-green?style=flat-square)](https://github.com/onestardao/WFGY/tree/main/OS/BlotBlotBlot)
&nbsp;
[![Bloc](https://img.shields.io/badge/Bloc-Reasoning%20Compiler-blue?style=flat-square)](https://github.com/onestardao/WFGY/tree/main/OS/BlocBlocBloc)
&nbsp;
[![Blur](https://img.shields.io/badge/Blur-Text2Image%20Engine-navy?style=flat-square)](https://github.com/onestardao/WFGY/tree/main/OS/BlurBlurBlur)
&nbsp;
[![Blow](https://img.shields.io/badge/Blow-Game%20Logic-purple?style=flat-square)](https://github.com/onestardao/WFGY/tree/main/OS/BlowBlowBlow)
&nbsp;
</div>


