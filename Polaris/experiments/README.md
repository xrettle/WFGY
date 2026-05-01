# Polaris Experiments

Public experiment evidence packages for **WFGY 5.0 Polaris Protocol**.

This folder contains the downloadable experiment records for the current Polaris evidence layer. The packages include test cases, prompt manifests, raw model outputs, parsed outputs, scoring rows, token usage tables, verdict files, audit records, and hash records.

The purpose of this folder is simple:

Readers can inspect the experiment evidence directly.

This is not a screenshot gallery.  
This is not a marketing-only result page.  
This is a public evidence index for the current Polaris experiment runs.

---

## What This Folder Contains

The current public packages cover two experiment branches:

| Branch | Main role | What readers can inspect |
| --- | --- | --- |
| **AI Tsunami** | topology conservation, compression, negative-control testing, robustness scaling | case manifests, payloads, raw outputs, parsed outputs, score rows, token usage, leakage audit, verdicts |
| **Moses** | staged robustness, judge traceability, failure-surface tracking, patch verification | pre-registration, arm manifests, prompt manifests, raw outputs, parsed outputs, judge rows, family summaries, hash chains |

These two branches should not be read as identical tests.

AI Tsunami focuses on whether compressed task topology can preserve output quality with far fewer tokens.

Moses focuses on whether a staged experiment chain can preserve prompts, outputs, parsing, scoring, verdicts, and failure-surface records across multiple test stages.

---

## Download Index

All packages are stored under:

`Polaris/experiments/downloads/`

| Package | Branch | Stage | Main content | Download |
| --- | --- | --- | --- | --- |
| `AI_TSU~1.ZIP` | AI Tsunami | Frozen MVP primary seed | First public topology-conservation seed package | [Download](https://github.com/onestardao/WFGY/raw/main/Polaris/experiments/downloads/AI_TSU~1.ZIP) |
| `AI_TSU~2.ZIP` | AI Tsunami | Frozen MVP v3 evidence | Improved compressed-topology evidence package | [Download](https://github.com/onestardao/WFGY/raw/main/Polaris/experiments/downloads/AI_TSU~2.ZIP) |
| `AI_TSU~3.ZIP` | AI Tsunami | Frozen MVP v4 pass | Clean frozen MVP pass evidence package | [Download](https://github.com/onestardao/WFGY/raw/main/Polaris/experiments/downloads/AI_TSU~3.ZIP) |
| `AI_TSU~4.ZIP` | AI Tsunami | T3 internal scale pass | Larger topology-conservation scale package | [Download](https://github.com/onestardao/WFGY/raw/main/Polaris/experiments/downloads/AI_TSU~4.ZIP) |
| `AI6389~1.ZIP` | AI Tsunami | T4 robustness expansion pass | Largest current AI Tsunami robustness package | [Download](https://github.com/onestardao/WFGY/raw/main/Polaris/experiments/downloads/AI6389~1.ZIP) |
| `AI_MOSES_P1_EVIDENCE_SEED_OUTPUTS_v3.zip` | Moses | P1 evidence seed pass | First executable Moses evidence seed | [Download](https://github.com/onestardao/WFGY/raw/main/Polaris/experiments/downloads/AI_MOSES_P1_EVIDENCE_SEED_OUTPUTS_v3.zip) |
| `AI_MOSES_P2_LOCKED_MVP_OUTPUTS.zip` | Moses | P2 locked MVP pass | Locked MVP evidence package | [Download](https://github.com/onestardao/WFGY/raw/main/Polaris/experiments/downloads/AI_MOSES_P2_LOCKED_MVP_OUTPUTS.zip) |
| `AI_MOSES_T4_PATCH_MINI_VERIFIER_OUTPUTS.zip` | Moses | T4 patch mini verifier pass | Small targeted verifier for known failure surfaces | [Download](https://github.com/onestardao/WFGY/raw/main/Polaris/experiments/downloads/AI_MOSES_T4_PATCH_MINI_VERIFIER_OUTPUTS.zip) |
| `AI_MOSES_T4_ROBUSTNESS_EXPANSION_OUTPUTS.zip` | Moses | T4 robustness expansion halt record | Full stress record with preserved halt reasons | [Download](https://github.com/onestardao/WFGY/raw/main/Polaris/experiments/downloads/AI_MOSES_T4_ROBUSTNESS_EXPANSION_OUTPUTS.zip) |

---

## Public Evidence Scale

The current indexed packages contain:

| Evidence item | Count |
| --- | ---: |
| ZIP packages indexed | 9 |
| Files inside ZIP packages | 141 |
| Total test cases | 478 |
| Raw model output records | 2228 |
| Parsed output records | 2228 |
| Judge or score rows | 2228 |
| Full prompt manifest rows | 948 |
| AI Tsunami case payload rows | 320 |
| Total uncompressed evidence size | about 8.6 MB |

This scale matters because the experiment is not represented only by a final score.

The packages expose the surrounding evidence chain:

case design, prompt construction, raw model output, parsed output, scoring rows, token records, verdict records, audit records, and hash records.

---

## How To Read The Packages

A reader does not need to inspect every file first.

The recommended reading order is:

| Step | File type | Why it matters |
| --- | --- | --- |
| 1 | `global_verdict.json` or `10_GLOBAL_VERDICT.json` | Start here. This gives the top-level result, output count, parse status, leakage status, score summary, token summary, pass state, or halt reason. |
| 2 | `arm_summary.csv`, `07_ARM_SUMMARY.csv`, `08_FAMILY_ARM_SUMMARY.csv` | These show arm-level and family-level performance. |
| 3 | `token_usage.csv`, `token_ratio_summary.csv` | These show token cost, token ratio, and compression behavior. |
| 4 | `raw_outputs.jsonl` or `04_RAW_OUTPUTS.jsonl` | These are the original model outputs. They show that the experiment actually produced responses. |
| 5 | `parsed_outputs.jsonl` or `05_PARSED_OUTPUTS.json` | These show how raw outputs were converted into structured scoring records. |
| 6 | `case_level_scores.csv` or `06_JUDGE_ROWS.csv` | These connect individual cases to scored results. |
| 7 | `trial_freeze_manifest.json`, `00_PRE_REGISTRATION.json`, `03_PROMPT_MANIFEST_HASHES.csv`, `11_HASH_CHAIN.json` | These preserve run state, prompt hashes, and integrity records. |

---

# AI Tsunami Branch

## What AI Tsunami Tests

AI Tsunami tests whether a compressed topology packet can preserve output quality while using far fewer tokens than a long-context baseline.

The important comparison is not simply:

> long prompt versus short prompt

The important comparison is:

| Arm | Meaning |
| --- | --- |
| A | long-context baseline |
| B | teacher topology condition |
| C | compressed topology condition |
| D | corrupted or paired-corrupted topology condition |

The key question is:

> If useful task topology is preserved, can the model keep high output quality even with a much smaller input?

The expected pattern is:

| Condition | Expected behavior |
| --- | --- |
| Long context | strong but expensive |
| Teacher topology | strong reference condition |
| Compressed topology | should stay close to strong conditions while using fewer tokens |
| Corrupted topology | should degrade clearly |

This gives the experiment a negative-control structure. The corrupted condition is important because it shows that the result is not only caused by shorter prompts or lucky scoring. If topology is damaged, performance should fall.

---

## AI Tsunami Package Contents

Most AI Tsunami packages contain:

| File | Meaning |
| --- | --- |
| `case_manifest.csv` | List of test cases and metadata |
| `case_payloads_internal.jsonl` | Case payloads used to construct the test inputs |
| `raw_outputs.jsonl` | Original model outputs |
| `parsed_outputs.jsonl` | Structured parsed results |
| `case_level_scores.csv` | Per-case scoring rows |
| `token_usage.csv` | Token usage by case and arm |
| `token_ratio_summary.csv` | Token ratio and compression summary |
| `coverage_unit_summary.csv` | Coverage summary by unit |
| `failure_signature_table.csv` | Failure signature records |
| `leakage_audit.csv` | Leakage and contamination checks |
| `arm_summary.csv` | Arm-level score and token summary |
| `global_verdict.json` | Top-level verdict and gate status |
| `trial_freeze_manifest.json` | Frozen trial metadata |
| `gate_manifest.json` | Gate definitions and thresholds |
| `arm_manifest.json` | Arm definitions |
| `blackfan_audit.md` | Adversarial audit notes |
| `public_safe_summary_template.md` | Public summary layer |

---

## AI Tsunami Progression

| Package | Cases | Raw outputs | Score rows | Result reading |
| --- | ---: | ---: | ---: | --- |
| `AI_TSU~1.ZIP` | 48 | 192 | 192 | Quality seed. Output and parsing were clean, but token-ratio and corruption-separation gates were not yet strong enough. |
| `AI_TSU~2.ZIP` | 48 | 192 | 192 | Major improvement. Compressed topology passed token-ratio behavior, but still missed some strict gates. |
| `AI_TSU~3.ZIP` | 48 | 192 | 192 | Frozen MVP primary pass. All listed gates passed in this run. |
| `AI_TSU~4.ZIP` | 80 | 320 | 320 | T3 internal scale pass. The test surface expanded while preserving clean parse, leakage, scoring, and topology behavior. |
| `AI6389~1.ZIP` | 96 | 384 | 384 | T4 robustness expansion pass. This is the strongest AI Tsunami package currently indexed here. |

---

## AI Tsunami Result Snapshot

The strongest current AI Tsunami package is:

`AI6389~1.ZIP`

It records:

| Metric | Value |
| --- | ---: |
| Cases | 96 |
| Expected outputs | 384 |
| Actual outputs | 384 |
| API error count | 0 |
| Parse pass rate | 1.0 |
| Leakage count | 0 |
| Failure signature match | 1.0 |
| Global level | `L5_T4_ROBUSTNESS_EXPANSION_PASS` |
| Global pass | `true` |

Arm-level score and token summary:

| Arm | Input type | Model | Mean score | Mean total tokens |
| --- | --- | --- | ---: | ---: |
| A | long context | GPT-4.1 | 0.9323 | 1754.56 |
| B | teacher topology | GPT-4.1 | 0.9750 | 464.42 |
| C | compressed topology | GPT-4.1 mini | 0.9365 | 380.63 |
| D | paired corrupted topology | GPT-4.1 mini | 0.2448 | 459.19 |

Key derived results:

| Metric | Value |
| --- | ---: |
| C minus A | 0.0042 |
| C retention against B | 0.9605 |
| C case pass rate | 1.0 |
| C minus D | 0.6917 |
| Raw token ratio C/A | 0.2169 |
| Amortized token ratio C/A | 0.1627 |

Readable interpretation:

The compressed topology condition stayed close to the long-context baseline while using roughly **21.7 percent** of the raw token budget. Under the amortized calculation recorded in the package, it used roughly **16.3 percent** of the long-context baseline token budget.

The corrupted topology condition collapsed clearly, which supports the interpretation that topology preservation mattered.

---

# Moses Branch

## What Moses Tests

Moses is a staged robustness and verification branch.

It tests whether the experiment chain can preserve:

| Layer | What is checked |
| --- | --- |
| Case layer | cases and families are recorded |
| Prompt layer | full prompts and prompt hashes are preserved |
| Output layer | raw outputs are retained |
| Parse layer | outputs are converted into structured records |
| Judge layer | every output has a judge row |
| Summary layer | arm and family summaries are produced |
| Verdict layer | pass or halt state is explicit |
| Integrity layer | hash chain and run records are preserved |

Moses is useful because it includes both pass records and a halt record. The halt record is not hidden. It is part of the public evidence.

---

## Moses Package Contents

Most Moses packages contain:

| File | Meaning |
| --- | --- |
| `00_PRE_REGISTRATION.json` | Pre-registration record for the run |
| `01_ARM_MANIFEST.json` | Arm definitions |
| `02_CASE_MANIFEST.json` | Case manifest in JSON format |
| `02_CASE_MANIFEST.csv` | Case manifest in CSV format |
| `03_PROMPT_MANIFEST_FULL.json` | Full prompt manifest |
| `03_PROMPT_MANIFEST_HASHES.csv` | Prompt hash table |
| `04_RAW_OUTPUTS.jsonl` | Original model outputs |
| `05_PARSED_OUTPUTS.json` | Parsed model outputs |
| `06_JUDGE_ROWS.csv` | Per-output judge rows |
| `07_ARM_SUMMARY.csv` | Arm-level summary |
| `08_FAMILY_ARM_SUMMARY.csv` | Family-by-arm summary |
| `09_WORST_FAMILY_TABLE.csv` | Worst-family table for stress runs |
| `09_FAMILY_PASS_TABLE.csv` | Family pass table for the mini verifier package |
| `10_GLOBAL_VERDICT.json` | Top-level verdict file |
| `11_HASH_CHAIN.json` | Hash chain and integrity record |

---

## Moses Progression

| Package | Cases | Raw outputs | Judge rows | Verdict |
| --- | ---: | ---: | ---: | --- |
| `AI_MOSES_P1_EVIDENCE_SEED_OUTPUTS_v3.zip` | 32 | 192 | 192 | `P1_EVIDENCE_SEED_PASS` |
| `AI_MOSES_P2_LOCKED_MVP_OUTPUTS.zip` | 48 | 288 | 288 | `P2_LOCKED_MVP_PASS` |
| `AI_MOSES_T4_PATCH_MINI_VERIFIER_OUTPUTS.zip` | 6 | 36 | 36 | `T4_PATCH_MINI_VERIFIER_PASS` |
| `AI_MOSES_T4_ROBUSTNESS_EXPANSION_OUTPUTS.zip` | 72 | 432 | 432 | `T4_ROBUSTNESS_EXPANSION_HALT` |

---

## Moses Result Snapshot

### P1 Evidence Seed

Package:

`AI_MOSES_P1_EVIDENCE_SEED_OUTPUTS_v3.zip`

| Metric | Value |
| --- | ---: |
| Cases | 32 |
| Expected outputs | 192 |
| Actual outputs | 192 |
| Parse pass rate | 1.0 |
| Leakage count | 0 |
| Gold leakage count | 0 |
| Scorer shortcut count | 0 |
| C1 vs A1 margin | 0.0445 |
| C1 vs B1 margin | 0.0592 |
| C1 vs S1 margin | 0.4375 |
| Token ratio C1/A1 | 0.4849 |
| Poison accepted count | 0 |
| Failure signature match rate | 1.0 |
| Verdict | `P1_EVIDENCE_SEED_PASS` |

### P2 Locked MVP

Package:

`AI_MOSES_P2_LOCKED_MVP_OUTPUTS.zip`

| Metric | Value |
| --- | ---: |
| Cases | 48 |
| Expected outputs | 288 |
| Actual outputs | 288 |
| Parse pass rate | 1.0 |
| Leakage count | 0 |
| Gold leakage count | 0 |
| Scorer shortcut count | 0 |
| C1 vs A1 margin | 0.0495 |
| C1 vs B1 margin | 0.0494 |
| C1 vs S1 margin | 0.4608 |
| Token ratio C1/A1 | 0.4873 |
| Poison accepted count | 0 |
| Failure signature match rate | 1.0 |
| Verdict | `P2_LOCKED_MVP_PASS` |

### T4 Patch Mini Verifier

Package:

`AI_MOSES_T4_PATCH_MINI_VERIFIER_OUTPUTS.zip`

| Metric | Value |
| --- | ---: |
| Cases | 6 |
| Expected outputs | 36 |
| Actual outputs | 36 |
| Parse pass rate | 1.0 |
| Leakage count | 0 |
| Gold leakage count | 0 |
| Scorer shortcut count | 0 |
| C1 vs A1 margin | 0.0 |
| C1 vs B1 margin | 0.0 |
| C1 vs S1 margin | 0.5392 |
| Token ratio C1/A1 | 0.3264 |
| Poison accepted count | 0 |
| Failure signature match rate | 1.0 |
| Verdict | `T4_PATCH_MINI_VERIFIER_PASS` |

### T4 Robustness Expansion

Package:

`AI_MOSES_T4_ROBUSTNESS_EXPANSION_OUTPUTS.zip`

| Metric | Value |
| --- | ---: |
| Cases | 72 |
| Expected outputs | 432 |
| Actual outputs | 432 |
| Parse pass rate | 1.0 |
| Leakage count | 0 |
| Gold leakage count | 0 |
| Scorer shortcut count | 0 |
| C1 vs A1 margin | -0.0047 |
| C1 vs B1 margin | -0.0113 |
| C1 vs S1 margin | 0.3839 |
| Token ratio C1/A1 | 0.6159 |
| Poison accepted count | 0 |
| Failure signature match rate | 1.0 |
| Halt reason | `c1_le_b1` |
| Verdict | `T4_ROBUSTNESS_EXPANSION_HALT` |

Readable interpretation:

The Moses branch has clean pass records at P1, P2, and the patch mini verifier stage. The larger T4 robustness expansion run is preserved as a halt record, not hidden or renamed into a pass. This makes the branch useful for audit and future correction because both success records and failure surfaces are visible.

---

# What The Evidence Supports

The current public evidence supports a scoped interpretation:

> Under the tested topology-conservation workloads, compressed topology packets can preserve high output quality with far fewer tokens, while corrupted topology conditions degrade in the expected direction.

The strongest AI Tsunami result shows that the compressed topology condition stayed near long-context quality while using a much smaller token budget.

The Moses branch shows staged evidence for experiment traceability, prompt preservation, output preservation, judge rows, family summaries, pass states, and halt states.

Together, the packages show a public experiment trail rather than only a final claim.

---

# What This Folder Does Not Claim

This folder does not claim:

* all AI tasks are solved
* all benchmarks are complete
* GPU scaling is globally disproven
* small models universally beat large models
* coding is fully proven
* math is fully proven
* creative generation is fully proven
* multimodal generation is fully proven
* agent execution is fully proven
* Moses and AI Tsunami are fully merged
* Polaris Protocol is final

The current public status is narrower:

> downloadable public evidence packages for the current Polaris topology-first experiment line.

---

# What Is Not Included

These packages are public experiment records.

They do not release the private mathematical core of WFGY 5.0 Polaris Protocol. They also do not release the full private implementation spine or unreleased internal construction logic.

They make the benchmark evidence inspectable.

They do not make the underlying private engine public.

---

# Integrity Hashes

SHA256 values for the current ZIP files:

| Package | SHA256 |
| --- | --- |
| `AI_TSU~1.ZIP` | `b1a294f7bf9c726e943a799d93d46e4b209c7172683bfb30172129dcb1a270f5` |
| `AI_TSU~2.ZIP` | `95b02544c2670f9f7ec52f510bef44da3516cddb31b8e576a5df365d9961ba3b` |
| `AI_TSU~3.ZIP` | `9e971365d503df385af50adf9613149706a20fcfde57314569c9e975428b86bf` |
| `AI_TSU~4.ZIP` | `14947dcf070bbb304086844a6552a497ab4a1a1946f39310dbe40aaa5e20991f` |
| `AI6389~1.ZIP` | `5e0be386588eb76799bd6698b203da581da956a5adb970c0564e3b267a2093f4` |
| `AI_MOSES_P1_EVIDENCE_SEED_OUTPUTS_v3.zip` | `fa6b97f21dee729c4bfc1550cdcc50de88da945698f0f72d425e6f34eaada93d` |
| `AI_MOSES_P2_LOCKED_MVP_OUTPUTS.zip` | `1976da1ab62cbf3c912fa1c06b5472e990fdf7df61a8a6114e2831dd094782d9` |
| `AI_MOSES_T4_PATCH_MINI_VERIFIER_OUTPUTS.zip` | `715888fc1e8e705a0a01c9502c1ff50ae21c04f84b19d04bfa94b0eefecf4de5` |
| `AI_MOSES_T4_ROBUSTNESS_EXPANSION_OUTPUTS.zip` | `4c2b4a3874795e30748668853f570cfdb86ee88bee3188efa198a99b6690e2e2` |

---

# Suggested Short Description

Use this short description when linking to this folder:

> Public experiment evidence packages for WFGY 5.0 Polaris Protocol, including cases, prompts, raw outputs, parsed outputs, scoring traces, token usage records, verdicts, and hash files.

---

# Status

| Field | Value |
| --- | --- |
| Project | WFGY 5.0 Polaris Protocol |
| Folder role | public experiment evidence layer |
| Data type | downloadable experiment records |
| Indexed ZIP packages | 9 |
| Total public cases | 478 |
| Total raw output records | 2228 |
| Total parsed output records | 2228 |
| Total judge or score rows | 2228 |
| Private mathematical core | not included |
| Full implementation release | not included |
