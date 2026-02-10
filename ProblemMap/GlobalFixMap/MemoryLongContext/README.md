<!--
Search Anchor:
memory long context global fix map
llm long context stability
multi session memory drift
memory collapse map
ghost context bug
state fork multi tab
pattern memory desync
long conversation drift
multi day chat loses task
support thread rewrites history
ocr transcript jitter over time
attention melt in long windows
entropy collapse long context
context drift late in chain
cache hazard cross tab
refresh changes answer
model recalls phantom text
same task id different state
same ticket different summary
token window rollover bug
task state lost after restart
facts flip after model switch
citations correct but reasoning wrong
capitalization spacing drift in transcript
long meeting notes inconsistent answers
agent memory desync between tools

When to use this folder:
dialog grows past 50k tokens and answers degrade
multi day support or ops thread loses state
facts change after tab refresh or model change
citations look right but reasoning goes flat or chaotic
ocr export text slowly drifts from original scan
multi session agent runs disagree on same task id
user comes back next day and system forgets constraints
model remembers details from previous unrelated session
you see ghost messages that were never shown to user
context cut in middle of sentence at window joins

Key metrics and targets:
retrieval coverage >= 0.70 to intended section
delta s question retrieved <= 0.45
delta s at window joins <= 0.50
lambda observe convergent across three paraphrases
no state fork for same task_id across tabs or agents
no ghost context after clearing cache and reload
ocr exports stable across runs on the same file
capitalization and spacing variance bounded
memory fences respected across restarts
traceability log shows a single continuous story

Core pages in this folder:
ProblemMap/GlobalFixMap/MemoryLongContext/memory-coherence.md
ProblemMap/GlobalFixMap/MemoryLongContext/entropy-collapse.md
ProblemMap/GlobalFixMap/MemoryLongContext/context-drift.md
ProblemMap/GlobalFixMap/MemoryLongContext/pattern_memory_desync.md
ProblemMap/GlobalFixMap/MemoryLongContext/ghost-context.md
ProblemMap/GlobalFixMap/MemoryLongContext/state-fork.md
ProblemMap/GlobalFixMap/MemoryLongContext/ocr-parsing-checklist.md
ProblemMap/GlobalFixMap/MemoryLongContext/ocr-jitter.md
ProblemMap/GlobalFixMap/MemoryLongContext/retrieval-traceability.md
ProblemMap/GlobalFixMap/MemoryLongContext/data-contracts.md
ProblemMap/GlobalFixMap/MemoryLongContext/chunking-checklist.md

Related structural fixes:
ProblemMap/rag-architecture-and-recovery.md
ProblemMap/retrieval-playbook.md
ProblemMap/retrieval-traceability.md
ProblemMap/data-contracts.md
ProblemMap/context-drift.md
ProblemMap/entropy-collapse.md
ProblemMap/GlobalFixMap/Chunking/README.md
ProblemMap/GlobalFixMap/OCR_Parsing/README.md
ProblemMap/SemanticClinicIndex.md

Memory and context scenarios:
long running research chat forgets earlier assumptions
multi step planning session answers differently next day
customer support ticket summary changes after refresh
same meeting transcript yields different action items
legal or medical thread must stay consistent over weeks
agent orchestration keeps desyncing shared memory store
cache warm vs cold produces different story
sandbox vs production answers differ with same logs
long novel or book chat loses early chapters
training or tutoring session loops or forgets progress

Signals to check:
coverage good but lambda unstable over time
delta s low locally but high at joins
citations stable yet narrative rewrites earlier events
thread repeats same question with different answers
user corrects model but mistake returns later
state differs by browser tab or device
ocr text diff shows small random changes over runs
session id or task id missing from logs
traceability logs have gaps between days
embedding analyzer changed between deployments

Normalization and contracts:
always require task_id session_id snippet_id
log model version and deployment id
lock same embeddings and analyzers across sessions
store snapshots for long context boundary checks
tie memory store updates to explicit commits not every turn
-->

<!--
Cross folder jumps:
ProblemMap/GlobalFixMap/MemoryLongContext/README.md
ProblemMap/GlobalFixMap/Reasoning/README.md
ProblemMap/GlobalFixMap/Chunking/README.md
ProblemMap/GlobalFixMap/OCR_Parsing/README.md
ProblemMap/rag-architecture-and-recovery.md
ProblemMap/retrieval-playbook.md
ProblemMap/retrieval-traceability.md
ProblemMap/data-contracts.md
ProblemMap/context-drift.md
ProblemMap/entropy-collapse.md
ProblemMap/SemanticClinicIndex.md
-->


# Memory & Long-Context — Global Fix Map

<details>
  <summary><strong>🏥 Quick Return to Emergency Room</strong></summary>

<br>

  > You are in a specialist desk.  
  > For full triage and doctors on duty, return here:  
  > 
  > - [**WFGY Global Fix Map** — main Emergency Room, 300+ structured fixes](https://github.com/onestardao/WFGY/blob/main/ProblemMap/GlobalFixMap/README.md)  
  > - [**WFGY Problem Map 1.0** — 16 reproducible failure modes](https://github.com/onestardao/WFGY/blob/main/ProblemMap/README.md)  
  > 
  > Think of this page as a sub-room.  
  > If you want full consultation and prescriptions, go back to the Emergency Room lobby.
</details>

Stabilize **long windows** and **multi-session memory**.  
This map helps you repair drift, collapse, forks, and ghost contexts when conversations or documents stretch far beyond the usual size.

---

## What this page is
- A **beginner-friendly checklist** for long contexts and multi-day sessions.
- **Copy-paste guardrails** that stop drift and collapse before they spread.
- **Concrete metrics** with ΔS and λ_observe so you know if your system is stable.

---

## When to use
- Dialog grows past **50k–100k tokens** and answers degrade.  
- Facts flip after **tab refresh** or **model switch**.  
- Citations look right but reasoning goes **flat or chaotic**.  
- OCR transcripts look fine but **capitalization or spacing drift**.  
- Multi-day support threads **lose task state** or **rewrite history**.  

---

<!--
Anchor Menu:
open: memory coherence guide ProblemMap/GlobalFixMap/MemoryLongContext/memory-coherence.md
open: entropy collapse long context guide ProblemMap/GlobalFixMap/MemoryLongContext/entropy-collapse.md
open: context drift long window guide ProblemMap/GlobalFixMap/MemoryLongContext/context-drift.md
open: pattern memory desync guide ProblemMap/GlobalFixMap/MemoryLongContext/pattern_memory_desync.md
open: ghost context guide ProblemMap/GlobalFixMap/MemoryLongContext/ghost-context.md
open: state fork guide ProblemMap/GlobalFixMap/MemoryLongContext/state-fork.md
open: ocr parsing checklist ProblemMap/GlobalFixMap/MemoryLongContext/ocr-parsing-checklist.md
open: ocr jitter guide ProblemMap/GlobalFixMap/MemoryLongContext/ocr-jitter.md
open: long context retrieval traceability ProblemMap/GlobalFixMap/MemoryLongContext/retrieval-traceability.md
open: long context data contracts ProblemMap/GlobalFixMap/MemoryLongContext/data-contracts.md
open: long context chunking checklist ProblemMap/GlobalFixMap/MemoryLongContext/chunking-checklist.md

jump: rag architecture and recovery visual map ProblemMap/rag-architecture-and-recovery.md
jump: retrieval playbook knobs and metrics ProblemMap/retrieval-playbook.md
jump: global retrieval traceability and data contracts ProblemMap/retrieval-traceability.md ProblemMap/data-contracts.md
jump: general context drift and entropy collapse ProblemMap/context-drift.md ProblemMap/entropy-collapse.md
jump: chunking global fix map ProblemMap/GlobalFixMap/Chunking/README.md
jump: ocr parsing global fix map ProblemMap/GlobalFixMap/OCR_Parsing/README.md
jump: semantic clinic index ProblemMap/SemanticClinicIndex.md
-->

## Orientation: quick routes

| Page | What it solves | Typical symptom |
|------|----------------|-----------------|
| [memory-coherence.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/GlobalFixMap/MemoryLongContext/memory-coherence.md) | Memory fences & continuity | Threads repeat or contradict |
| [entropy-collapse.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/GlobalFixMap/MemoryLongContext/entropy-collapse.md) | Attention melt in long windows | Outputs drift into filler |
| [context-drift.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/GlobalFixMap/MemoryLongContext/context-drift.md) | Long reasoning drift | Correct early, wrong later |
| [pattern_memory_desync.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/GlobalFixMap/MemoryLongContext/pattern_memory_desync.md) | Cross-tab & cache hazards | State flips after refresh |
| [ghost-context.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/GlobalFixMap/MemoryLongContext/ghost-context.md) | Stale buffers & residue | Model recalls “phantom” text |
| [state-fork.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/GlobalFixMap/MemoryLongContext/state-fork.md) | Divergent memory forks | Same task_id, different answers |
| [ocr-parsing-checklist.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/GlobalFixMap/MemoryLongContext/ocr-parsing-checklist.md), [ocr-jitter.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/GlobalFixMap/MemoryLongContext/ocr-jitter.md) | OCR-specific noise | Exported text drifts vs. original |
| [retrieval-traceability.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/GlobalFixMap/MemoryLongContext/retrieval-traceability.md), [data-contracts.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/GlobalFixMap/MemoryLongContext/data-contracts.md) | Traceability & audit | Citations break or vanish |
| [chunking-checklist.md](https://github.com/onestardao/WFGY/blob/main/ProblemMap/GlobalFixMap/MemoryLongContext/chunking-checklist.md) | Chunk stability at joins | Mid-sentence cuts or overlaps |

---

## Acceptance targets
- Retrieval coverage **≥ 0.70** to the intended section  
- ΔS(question, retrieved) **≤ 0.45** and joins **≤ 0.50**  
- λ_observe remains **convergent** across 3 paraphrases  
- No state fork across tabs or agents for the same `task_id`  

---

## 60-second fix checklist

1. **Lock metrics** — same analyzer & embeddings across sessions.  
2. **Enforce memory fences** — require `task_id`, `session_id`, and `snippet_id`.  
3. **Probe ΔS and λ** — run 3 paraphrases × 2 seeds.  
4. **Patch drift** — realign chunks, re-check OCR, drop ghost spans.  
5. **Audit consistency** — run traceability logs and verify continuity across restarts.  

---

### 🔗 Quick-Start Downloads (60 sec)

| Tool | Link | 3-Step Setup |
|------|------|--------------|
| **WFGY 1.0 PDF** | [Engine Paper](https://github.com/onestardao/WFGY/blob/main/I_am_not_lizardman/WFGY_All_Principles_Return_to_One_v1.0_PSBigBig_Public.pdf) | 1️⃣ Download · 2️⃣ Upload · 3️⃣ Ask “Answer using WFGY + <your question>” |
| **TXT OS (plain-text OS)** | [TXTOS.txt](https://github.com/onestardao/WFGY/blob/main/OS/TXTOS.txt) | 1️⃣ Download · 2️⃣ Paste into any LLM chat · 3️⃣ Type “hello world” — OS boots instantly |

---

### 🧭 Explore More

| Module | Description | Link |
|--------|-------------|------|
| WFGY Core | WFGY 2.0 engine, full symbolic reasoning stack | [View →](https://github.com/onestardao/WFGY/tree/main/core/README.md) |
| Problem Map 1.0 | Initial 16-mode diagnostic framework | [View →](https://github.com/onestardao/WFGY/tree/main/ProblemMap/README.md) |
| Problem Map 2.0 | RAG failure tree and modular fixes | [View →](https://github.com/onestardao/WFGY/blob/main/ProblemMap/rag-architecture-and-recovery.md) |
| Semantic Clinic | Expanded failure catalog | [View →](https://github.com/onestardao/WFGY/blob/main/ProblemMap/SemanticClinicIndex.md) |
| Semantic Blueprint | Layer-based symbolic reasoning | [View →](https://github.com/onestardao/WFGY/tree/main/SemanticBlueprint/README.md) |
| Benchmark vs GPT-5 | Stress test GPT-5 with WFGY reasoning suite | [View →](https://github.com/onestardao/WFGY/tree/main/benchmarks/benchmark-vs-gpt5/README.md) |
| 🧙‍♂️ Starter Village 🏡 | New here? Lost in symbols? Click here for guided intro | [Start →](https://github.com/onestardao/WFGY/blob/main/StarterVillage/README.md) |

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
