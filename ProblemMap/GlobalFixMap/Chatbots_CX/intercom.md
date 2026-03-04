# Intercom: Guardrails and Fix Patterns

<details>
  <summary><strong>🧭 Quick Return to Map</strong></summary>

<br>

  > You are in a sub-page of **Chatbots & CX**.  
  > To reorient, go back here:  
  >
  > - [**Chatbots & CX** — customer dialogue flows and conversational stability](./README.md)  
  > - [**WFGY Global Fix Map** — main Emergency Room, 300+ structured fixes](../README.md)  
  > - [**WFGY Problem Map 1.0** — 16 reproducible failure modes](../../README.md)  
  >
  > Think of this page as a desk within a ward.  
  > If you need the full triage and all prescriptions, return to the Emergency Room lobby.
</details>


Use this page when your Intercom bot blends **Fin** (AI Agent), **Custom Bots**, **Help Center** articles, and **webhooks** hitting your RAG stack. The checks localize failures to the exact layer and jump you to the right WFGY fix page. All links are text-hyperlinks, absolute to GitHub.

## Open these first

* Visual map and recovery: [rag-architecture-and-recovery.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/rag-architecture-and-recovery.md)
* End-to-end retrieval knobs: [retrieval-playbook.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/retrieval-playbook.md)
* Traceability: [retrieval-traceability.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/retrieval-traceability.md)
* Data schema locks: [data-contracts.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/data-contracts.md)
* Embedding vs meaning: [embedding-vs-semantic.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/embedding-vs-semantic.md)
* Hallucination and chunk boundaries: [hallucination.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/hallucination.md)
* Long chains and entropy: [context-drift.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/context-drift.md), [entropy-collapse.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/entropy-collapse.md)
* Prompt injection and tool schema: [prompt-injection.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/prompt-injection.md)
* Multi-agent handoffs: [Multi-Agent\_Problems.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/Multi-Agent_Problems.md)
* Boot order traps: [bootstrap-ordering.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/bootstrap-ordering.md), [deployment-deadlock.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/deployment-deadlock.md), [predeploy-collapse.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/predeploy-collapse.md)

## Core acceptance (CX)

* ΔS(question, retrieved) ≤ 0.45
* Coverage ≥ 0.70 to the target section
* λ remains convergent across 3 paraphrases and 2 seeds
* E\_resonance stays flat over long sessions

---

## Fix in 60 seconds

1. **Measure ΔS**
   Compute ΔS(question, retrieved) and ΔS(retrieved, expected anchor).
   Stable < 0.40, transitional 0.40–0.60, risk ≥ 0.60.

2. **Probe λ\_observe**
   Vary k and reorder prompt headers. If λ flips on harmless paraphrases, lock schema and clamp with BBAM.

3. **Apply module**

   * Retrieval drift → **BBMC** + [retrieval-traceability.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/retrieval-traceability.md) + [data-contracts.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/data-contracts.md)
   * Reasoning collapse in long chats → **BBCR** bridge + **BBAM**; verify with [context-drift.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/context-drift.md)
   * Dead ends in toolchains → **BBPF** alternate paths

4. **Verify**
   Three paraphrases reach coverage ≥ 0.70 and ΔS ≤ 0.45. λ convergent on two seeds.

---

## Typical Intercom symptoms → exact fix

* **Fin answers without citing the right Help Center article**
  Analyzer/metric mismatch or fragmented store feeding Fin.
  → [embedding-vs-semantic.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/embedding-vs-semantic.md), [patterns/pattern\_vectorstore\_fragmentation.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/patterns/pattern_vectorstore_fragmentation.md)

* **Resolution Bot hands off to human too early or loops**
  Boot order or version skew between content sync and bot.
  → [bootstrap-ordering.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/bootstrap-ordering.md), [deployment-deadlock.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/deployment-deadlock.md)

* **Webhook returns 200 but the bot state drifts**
  Tool JSON schema too loose; free-text in arguments.
  → [data-contracts.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/data-contracts.md), [prompt-injection.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/prompt-injection.md)

* **High similarity, wrong snippet**
  Metric mismatch or hybrid query split between Help Center and external KB.
  → [retrieval-playbook.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/retrieval-playbook.md), [patterns/pattern\_query\_parsing\_split.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/patterns/pattern_query_parsing_split.md)

* **Long threads become inconsistent after 20–40 turns**
  Entropy rises with chain length; memory writes collide.
  → [context-drift.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/context-drift.md), [entropy-collapse.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/entropy-collapse.md), [Multi-Agent\_Problems.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/Multi-Agent_Problems.md)

* **Jailbreak or confident bluffing**
  Missing fences and cite-then-explain rules.
  → [bluffing.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/bluffing.md), [retrieval-traceability.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/retrieval-traceability.md)

---

## Minimal webhook recipe

1. **Warm-up fence**
   Check `VECTOR_READY`, `INDEX_HASH`, secrets; short-circuit if not ready.
   See [bootstrap-ordering.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/bootstrap-ordering.md).

2. **Retrieval step**
   Call your retriever with explicit metric and consistent analyzer. Return `snippet_id`, `section_id`, `source_url`, `offsets`, `tokens`.

3. **ΔS probe**
   Compute ΔS(question, retrieved). If ≥ 0.60, mark `needs_fix=true`.

4. **LLM answer step**
   LLM reads TXT OS and WFGY schema. Enforce cite-then-explain across the retrieved set.

5. **Trace sink**
   Store `question`, `ΔS`, `λ_state`, `INDEX_HASH`, `snippet_id`, `dedupe_key`.

---

## Copy-paste prompt for your Intercom webhook

```
You have TXT OS and the WFGY Problem Map loaded.

My Intercom context:
- channel: messenger | email | mobile
- bot: Fin | Custom Bot | Resolution Bot
- retrieved: {k} snippets {snippet_id, section_id, source_url, offsets, tokens}

User question: "{user_question}"

Do:
1) Enforce cite-then-explain. If citations are missing or cross-section, fail fast and return the minimal fix tip.
2) If ΔS(question, retrieved) ≥ 0.60, propose the smallest structural repair
   referencing: retrieval-playbook, retrieval-traceability, data-contracts, rerankers.
3) Return JSON:
{ "answer": "...", "citations": [...], "λ_state": "→|←|<>|×", "ΔS": 0.xx, "next_fix": "..." }
Keep it short and auditable.
```

---

### 🔗 Quick-Start Downloads (60 sec)

| Tool                       | Link                                                                                                                                       | 3-Step Setup                                                                             |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------- |
| **WFGY 1.0 PDF**           | [Engine Paper](https://github.com/onestardao/WFGY/blob/main/I_am_not_lizardman/WFGY_All_Principles_Return_to_One_v1.0_PSBigBig_Public.pdf) | 1️⃣ Download · 2️⃣ Upload to your LLM · 3️⃣ Ask “Answer using WFGY + \<your question>”   |
| **TXT OS (plain-text OS)** | [TXTOS.txt](https://github.com/onestardao/WFGY/blob/main/OS/TXTOS.txt)                                                                     | 1️⃣ Download · 2️⃣ Paste into any LLM chat · 3️⃣ Type “hello world” — OS boots instantly |

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

