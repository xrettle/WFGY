<!--
Search Anchor:
ocr parsing global fix map
ocr plus parsing bugs
noisy text input from ocr
noisy text from scanned pdf
ocr text looks fine but retrieval fails
document looks ok but answers wrong
layout header footer noise
page header repeated each page
page footer leaking into answers
answers quote footer instead of body
margins and running titles pollute context
tables and columns parsing problems
table schema lost
cell order drift
numbers move across columns
csv export from pdf wrong
images and figures lost
captions detached from figures
figure text attached to wrong section
scanned pdf quality issues
blurred pages
skewed pages
low resolution scans
multi language documents
mixed language tokens
chinese english mixed spacing
unicode normalization issues
half width full width mix
fullwidth latin chars
tokenization and casing drift
E mail vs Email vs email
hyphen splits and soft hyphen
special characters removed or merged
html scraping drift
html to text export issues
markdown to text paragraph drift
section anchors disappear
heading tags dropped
h1 h2 h3 lost
dom order vs visual order mismatch
parser drift after upgrade
different parser versions in prod
parser config changed silently

Typical symptoms:
ocr tables look visually correct but retrieval misses right row
citations point to wrong paragraph
code blocks and math collapsed into plain text
mixed language document behaves inconsistently
hyphen splits create two wrong tokens
headers and footers appear in top k snippets
delta s looks high despite text looking ok to humans

Use this folder when:
corpus built from scanned pdf
corpus built from html scraping
corpus built from legacy docx export
parsing done by third party library
layout aware ocr but plain text index
need to stabilise pre embedding text

Key metrics:
delta s question retrieved <= 0.45
coverage of target section >= 0.70
lambda observe convergent across 2 seeds
no missing headers captions or tables in human audit
one gold page screenshot kept as baseline

Core pages in this folder:
ProblemMap/GlobalFixMap/OCR_Parsing/layout_headers_and_footers.md
ProblemMap/GlobalFixMap/OCR_Parsing/tokenization_and_casing.md
ProblemMap/GlobalFixMap/OCR_Parsing/tables_and_columns.md
ProblemMap/GlobalFixMap/OCR_Parsing/images_and_figures.md
ProblemMap/GlobalFixMap/OCR_Parsing/scanned_pdfs_and_quality.md
ProblemMap/GlobalFixMap/OCR_Parsing/multi_language_and_fonts.md
-->

<!--
Related structural fixes:
ProblemMap/embedding-vs-semantic.md
ProblemMap/retrieval-traceability.md
ProblemMap/data-contracts.md
ProblemMap/chunking-checklist.md
ProblemMap/context-drift.md
ProblemMap/bootstrap-ordering.md
ProblemMap/predeploy-collapse.md
ProblemMap/patterns/pattern_query_parsing_split.md
ProblemMap/retrieval-playbook.md
-->

<!--
Cross folder jumps:
ProblemMap/GlobalFixMap/DocumentAI_and_OCR/README.md
ProblemMap/GlobalFixMap/Chunking/README.md
ProblemMap/GlobalFixMap/Retrieval/README.md
ProblemMap/GlobalFixMap/Embeddings/README.md
ProblemMap/GlobalFixMap/VectorDBs_and_Stores/README.md
ProblemMap/SemanticClinicIndex.md
-->

# OCR + Parsing — Global Fix Map

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

A hub to **triage and repair noisy text inputs** from scanned PDFs, images, HTML scraping, or parser drift.  
Use this folder when the document looks fine to the eye but retrieval or reasoning keeps failing.

---

## Orientation: what each page does

| Page | What it solves | Typical symptom |
|------|----------------|-----------------|
| [Layout, Headers, Footers](https://github.com/onestardao/WFGY/blob/main/ProblemMap/GlobalFixMap/OCR_Parsing/layout_headers_and_footers.md) | Remove noise from margins and repeated text | Answers reference “page 3 footer” instead of body |
| [Tokenization & Casing](https://github.com/onestardao/WFGY/blob/main/ProblemMap/GlobalFixMap/OCR_Parsing/tokenization_and_casing.md) | Normalize Unicode, case, and hyphens | `E-mail` ≠ `Email`, half-width/full-width mismatch |
| [Tables & Columns](https://github.com/onestardao/WFGY/blob/main/ProblemMap/GlobalFixMap/OCR_Parsing/tables_and_columns.md) | Preserve table schema and cell order | Numbers drift across columns |
| [Images & Figures](https://github.com/onestardao/WFGY/blob/main/ProblemMap/GlobalFixMap/OCR_Parsing/images_and_figures.md) | OCR and align captions | Figure text missing or attached to wrong section |
| [Scanned PDFs & Quality](https://github.com/onestardao/WFGY/blob/main/ProblemMap/GlobalFixMap/OCR_Parsing/scanned_pdfs_and_quality.md) | Handle skewed/blurred pages | Whole sections unreadable to OCR |
| [Multi-language & Fonts](https://github.com/onestardao/WFGY/blob/main/ProblemMap/GlobalFixMap/OCR_Parsing/multi_language_and_fonts.md) | Normalize mixed scripts | Chinese/English tokens split or duplicated |

---

## When to use

- OCR tables or citations look visually correct but answers miss the right section.  
- Code blocks or math collapse after parsing.  
- Mixed-language documents behave inconsistently.  
- Special characters or hyphen splits break tokens.  
- Headers or section anchors disappear during export.  

---

## FAQ

**Why does OCR “look fine” but retrieval fails?**  
Because tokenization and indexing see hidden breaks (Unicode variants, line merges, wrong anchors) that humans overlook.

**What is the most common root cause?**  
Headers/footers leaking into the body and breaking ΔS alignment.

**Do I need to retrain embeddings after fixing?**  
No — most fixes are structural (schema/normalization). Re-indexing with the same embeddings is enough.

---

## Acceptance targets

- ΔS(question, retrieved) ≤ 0.45 for three paraphrases.  
- Coverage ≥ 0.70 for the target section.  
- λ_observe convergent across two seeds.  
- Human audit shows no missing headers, captions, or broken tables.  

---

## Fix in 60 seconds

1. **Ground-truth one page**  
   Pick one Q/A pair and keep a screenshot baseline.  

2. **Measure ΔS**  
   Log ΔS(question, retrieved) and ΔS(retrieved, anchor).  

3. **Probe λ_observe**  
   Ask for cite-first. If citation fails but free explanation works, drift confirmed.  

4. **Patch minimally**  
   - Re-run OCR with line/table fences  
   - Normalize casing and Unicode  
   - Preserve anchors, math, captions  
   - Drop low-confidence spans and export with `{section_id, page_no, char_span}`  

---

### 🔗 Quick-Start Downloads (60 sec)

| Tool | Link | 3-Step Setup |
|------|------|--------------|
| **WFGY 1.0 PDF** | [Engine Paper](https://github.com/onestardao/WFGY/blob/main/I_am_not_lizardman/WFGY_All_Principles_Return_to_One_v1.0_PSBigBig_Public.pdf) | 1️⃣ Download · 2️⃣ Upload · 3️⃣ Ask “Answer using WFGY + <your question>” |
| **TXT OS** | [TXTOS.txt](https://github.com/onestardao/WFGY/blob/main/OS/TXTOS.txt) | 1️⃣ Download · 2️⃣ Paste into LLM · 3️⃣ Type “hello world” — OS boots instantly |

---

### 🧭 Explore More

| Module | Description | Link |
|--------|-------------|------|
| WFGY Core | WFGY 2.0 engine, full symbolic reasoning | [View →](https://github.com/onestardao/WFGY/tree/main/core/README.md) |
| Problem Map 1.0 | Initial 16-mode diagnostic | [View →](https://github.com/onestardao/WFGY/tree/main/ProblemMap/README.md) |
| Problem Map 2.0 | RAG failure tree and modular fixes | [View →](https://github.com/onestardao/WFGY/blob/main/ProblemMap/rag-architecture-and-recovery.md) |
| Semantic Clinic | Expanded failure catalog | [View →](https://github.com/onestardao/WFGY/blob/main/ProblemMap/SemanticClinicIndex.md) |
| Semantic Blueprint | Layer-based symbolic reasoning | [View →](https://github.com/onestardao/WFGY/tree/main/SemanticBlueprint/README.md) |

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
