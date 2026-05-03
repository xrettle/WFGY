# Polaris Experiments

> 繁體中文版本：[`README.zh-TW.md`](./README.zh-TW.md)  
> Note: Not every WFGY page currently has a Traditional Chinese version. If versions differ, the English page is the primary reference.

Public evidence layer for **WFGY 5.0 Polaris Protocol**.

We are publishing the evidence first.

This folder contains downloadable experiment evidence packages for the current WFGY 5.0 Polaris Protocol pre release track. The packages include raw model outputs, parsed outputs, case verdicts, token accounting, audit records, warning records, certificate files, and SHA256 integrity records.

This is not a screenshot gallery.  
This is not a marketing only result page.  
This is a public evidence layer that lets readers inspect what was tested, what was produced, how outputs were parsed, how verdicts were assigned, and what evidence is currently available before the full open source release.

Official repository:

https://github.com/onestardao/WFGY

License:

MIT License, unless a specific file states otherwise.

---

## 30 Second Summary

| Question | Answer |
| --- | --- |
| What is this page? | The first public evidence layer for WFGY 5.0 Polaris Protocol |
| What is public now? | Four evidence packages with raw outputs, parsed outputs, verdicts, token records, audits, and hashes |
| Is this only a screenshot page? | No. The ZIP files contain inspectable experiment records |
| How many main packages are public? | 4 packages: PP01, PP02A, PP02B, PP02C |
| Main branch test cases | 680 |
| Main branch primary outputs | 3600 |
| Is the full mathematical core included? | Not yet. It is planned for the 2026/05/05 open source release |
| Are execution notebooks included? | Not yet. This is an evidence release, not a full execution package |
| Does this claim that all AI problems are solved? | No. The claims are scoped to the recorded experiment branches |

---

## Who Should Read This Page

| Reader | Suggested path |
| --- | --- |
| Non technical reader | Start with the summary, token saving explanation, and package overview |
| Engineer | Inspect raw outputs, parsed outputs, verdicts, token tables, audit records, and SHA256 files |
| Skeptical reader | Read the FAQ, audit records, leakage checks, hard veto checks, and integrity hashes |
| Reproduction focused reader | Start with the public evidence now. Full math and Colab reproduction materials are planned after 2026/05/05 |
| WFGY 5.0 follower | This is the first public evidence entry point for Polaris Protocol |

---

## Why Token Cost Can Be Reduced

The core intuition is simple.

A common long context workflow gives the model a large block of background, rules, constraints, examples, and task instructions every time.

That is expensive.

The model has to read a large amount of text again and again.

Polaris explores a different direction:

1. Break the task apart
2. Turn the task into structure
3. Compress the structure into a task map
4. Let the model produce the final answer from that map

The task map can be understood as a topology.

Topology does not try to preserve every word. It tries to preserve the important relationships between parts of the task.

| Long context workflow | Polaris topology workflow |
| --- | --- |
| Send the full instruction block every time | Build the task structure first |
| The model rereads long text each time | The model reads a shorter structured representation |
| Cost grows with context length | Cost can go down |
| Long text noise can cause drift | Structure can be easier to stabilize |
| Like carrying an entire library | Like carrying a precise map |

Plain example:

If you want someone to find a place in a city, the traditional way is like giving them a full city encyclopedia every time.

The Polaris direction is more like giving them a route map, area relationships, and key landmarks.

You do not need to carry the whole encyclopedia every time.

You need to preserve the correct structure.

<details>
<summary>Details: this is not just shortening the prompt</summary>

If you only cut a prompt shorter, information is usually lost and quality often drops.

The Polaris direction is not simple text deletion. The goal is to reorganize the task into a more stable structure.

| Original long text | Structured version |
| --- | --- |
| A long task description | Task nodes |
| Many rules | Rule relationships |
| Multiple goals | Goal order |
| Many constraints | Boundary conditions |
| Possible errors | Audit points |
| Final answer requirement | Output format |

The model receives a clearer task structure instead of a large unorganized block of text.

The model then does something closer to this:

Read the task map.  
Translate the task map back into the required output.  
Complete the requested task.

A simple way to say it:

> Turn the task into structure first, then let the model translate that structure into an answer.

This is one reason why token cost can go down while result quality can still be preserved under the tested workloads.

</details>

---

## Current Public Release

The current public release contains four main evidence packages:

| Branch | What it tests | Main result |
| --- | --- | --- |
| **PP01** | Large scale OSK evidence run and token efficiency behavior | `OSK_MVP_FINAL_PASS` |
| **PP02A** | T4 evidence branch with seal pass and near pass reference | `SEAL_PASS` |
| **PP02B** | SP math oriented 120 case evaluation | `T4_MAIN_CERTIFICATE_PASS` |
| **PP02C** | Coding repair and contract validation with sandbox checks | `FULL_SANDBOX_STRONG_PASS` |

The current public layer contains:

| Evidence item | Count |
| --- | ---: |
| Main evidence packages | 4 |
| Main branch test cases | 680 |
| Main branch primary outputs | 3600 |
| PP01 outputs | 1920 |
| PP02A final run outputs | 240 |
| PP02B outputs | 720 |
| PP02C main run outputs | 720 |
| Execution notebooks included | 0 |
| Private mathematical core included | 0 |

Additional sandbox and reference artifacts are preserved inside PP02A and PP02C, but they are not double counted in the primary output table above.

This is the first public evidence layer before the full **2026/05/05** open source release.

---

## Downloads

All files are stored under:

`Polaris/experiments/downloads/`

| Package | Branch | Contents | Download |
| --- | --- | --- | --- |
| `wfgy5_polaris_protocol_pp01_t4_osk_320case_public_evidence_20260503.zip` | PP01 | 320 cases, 1920 outputs, verdicts, token accounting, audits, hashes | [Download](https://github.com/onestardao/WFGY/raw/main/Polaris/experiments/downloads/wfgy5_polaris_protocol_pp01_t4_osk_320case_public_evidence_20260503.zip) |
| `wfgy5_polaris_protocol_pp02a_t4_120case_public_evidence_20260503.zip` | PP02A | 120 case T4 evidence branch, final seal pass, near pass reference | [Download](https://github.com/onestardao/WFGY/raw/main/Polaris/experiments/downloads/wfgy5_polaris_protocol_pp02a_t4_120case_public_evidence_20260503.zip) |
| `wfgy5_polaris_protocol_pp02b_sp_120case_public_evidence_20260503.zip` | PP02B | 120 case SP math evaluation, 720 outputs, certificate evidence | [Download](https://github.com/onestardao/WFGY/raw/main/Polaris/experiments/downloads/wfgy5_polaris_protocol_pp02b_sp_120case_public_evidence_20260503.zip) |
| `wfgy5_polaris_protocol_pp02c_t4_120case_public_evidence_20260503.zip` | PP02C | 120 case coding repair and contract validation, sandbox and hard veto evidence | [Download](https://github.com/onestardao/WFGY/raw/main/Polaris/experiments/downloads/wfgy5_polaris_protocol_pp02c_t4_120case_public_evidence_20260503.zip) |
| `wfgy5_polaris_protocol_public_evidence_bundle_20260503.zip` | Bundle | All current public evidence packages in one bundle | [Download](https://github.com/onestardao/WFGY/raw/main/Polaris/experiments/downloads/wfgy5_polaris_protocol_public_evidence_bundle_20260503.zip) |

Important note:

If a single branch package is missing from the downloads folder, use the bundle package until the individual file is uploaded.

---

## Quick Inspection Path

| Step | What to open | What it tells you |
| --- | --- | --- |
| 1 | README inside each package | What the experiment branch is about |
| 2 | Final verdict or certificate file | Whether the branch passed its current gate |
| 3 | Token accounting file | How much token budget was used |
| 4 | Audit files | Whether leakage, warnings, hard vetoes, or failure surfaces were found |
| 5 | Raw outputs | What the model actually produced |

<details>
<summary>Details: inspection path for engineers</summary>

| Step | What to inspect | Why it matters |
| --- | --- | --- |
| 1 | Raw outputs | Confirms that the run produced real model responses |
| 2 | Parsed outputs | Shows how outputs were converted into structured records |
| 3 | Case verdicts | Connects each case to a verdict |
| 4 | Family or stage verdicts | Shows broader pattern level results |
| 5 | Token accounting | Shows cost and token efficiency behavior |
| 6 | Audit records | Shows leakage checks, warning checks, hard veto checks, or source quality checks |
| 7 | SHA256 manifests | Lets readers verify file integrity |

</details>

---

## Four Package Overview

| Branch | Plain meaning | Key signal |
| --- | --- | --- |
| PP01 | Tests whether structured task representation can reduce token cost while keeping quality | 320 cases, 1920 outputs, C condition used about 16.6 percent of raw total token budget |
| PP02A | Tests a T4 evidence branch moving from weaker reference to final pass | 120 cases, final `SEAL_PASS`, weaker reference preserved |
| PP02B | Tests math oriented structured evaluation | 120 cases, 720 outputs, `T4_MAIN_CERTIFICATE_PASS` |
| PP02C | Tests coding repair, contract validation, sandbox checks, and hard vetoes | 120 cases, 720 outputs, zero hard vetoes, `FULL_SANDBOX_STRONG_PASS` |

<details>
<summary>Details: PP01</summary>

# PP01: OSK 320 Case Evidence Run

## What PP01 Tests

PP01 is the largest main branch in this first public evidence layer.

It tests whether a compressed or structured task representation can preserve strong output behavior while using much fewer tokens than a long context baseline.

The simple version:

Can the system keep the important structure of a task without carrying the full long prompt every time?

## PP01 Result Snapshot

| Metric | Value |
| --- | ---: |
| Cases | 320 |
| Arms | 6 |
| Expected outputs | 1920 |
| Actual outputs | 1920 |
| Parse pass rate | 1.0 |
| Leakage count | 0 |
| C score mean | 0.988465 |
| B score mean | 0.967265 |
| C retention vs B | 1.0219 |
| C raw total ratio vs A | 0.1656 |
| C input ratio vs A | 0.1242 |
| Failure signature match rate | 1.0 |
| Shadow overclaim count | 0 |
| Wrong source critical count | 0 |
| Family collapse count | 0 |
| Hard gates pass | true |
| Final pass | true |
| Global status | `OSK_MVP_FINAL_PASS` |

## Why PP01 Matters

PP01 is the cleanest large scale evidence package in this release.

It records 320 cases and 1920 outputs. The run reached 100 percent parse success, zero leakage, zero family collapse, zero wrong source critical count, and final pass status.

The compressed condition used about **16.6 percent** of the raw total token budget compared with the long context baseline. It used about **12.4 percent** of the input token budget.

Plain reading:

PP01 shows that, under this tested workload, the compressed condition kept strong output behavior while using a much smaller token budget.

</details>

<details>
<summary>Details: PP02A</summary>

# PP02A: T4 Evidence Branch With Seal Pass

## What PP02A Tests

PP02A is a 120 case T4 evidence branch.

Its value is not only the final result.

It also preserves a near pass reference, which means readers can inspect part of the development trail rather than only seeing a polished final number.

## PP02A Final Result Snapshot

| Metric | Final value |
| --- | ---: |
| Cases | 120 |
| Raw outputs in final run | 240 |
| Domain count | 6 |
| API error count | 0 |
| Parser fail count | 0 |
| Parse success rate | 1.0 |
| Total weak rows | 0 |
| Seal domain count | 6 |
| Dominant or better domains | 6 |
| Release or better domains | 6 |
| T4 system score | 100.0 |
| OVER100 internal score | 125.0 |
| Final verdict | `SEAL_PASS` |

## PP02A Reference Trail

| Metric | Previous reference value |
| --- | ---: |
| Cases | 120 |
| Parser fail count | 1 |
| Parse success rate | 0.9958 |
| Total weak rows | 1 |
| Seal domain count | 5 |
| T4 system score | 76.56 |
| Final verdict | `INVALID` |

## Why PP02A Matters

PP02A shows an evidence branch moving from a weaker reference run into a final seal pass.

The final run records zero parser failures, zero weak rows, all six domains reaching the seal condition, and a final `SEAL_PASS`.

Plain reading:

PP02A is useful because it does not hide the path. It keeps both the weaker reference and the final stronger result.

</details>

<details>
<summary>Details: PP02B</summary>

# PP02B: SP Math 120 Case Evaluation

## What PP02B Tests

PP02B is the first public math oriented evidence package in this release set.

It tests a structured 120 case SP math evaluation branch with compiled outputs, model stress outputs, audits, certificates, and verdicts.

This package does not claim that all mathematics is solved.

It shows that this recorded math oriented branch passed its current T4 certificate checks.

## PP02B Result Snapshot

| Metric | Value |
| --- | ---: |
| Cases | 120 |
| Expected compiled outputs | 120 |
| Actual compiled outputs | 120 |
| Expected total outputs | 720 |
| Actual total outputs | 720 |
| Expected model stress outputs | 600 |
| Actual model stress outputs | 600 |
| Model API calls | 600 |
| C parse pass rate | 1.0 |
| C contract pass rate | 1.0 |
| Family red count | 0 |
| Compiler verifier red count | 0 |
| Model stress warning count | 0 |
| Model stress verdict | `MODEL_STRESS_PASS` |
| Main certificate verdict | `T4_MAIN_CERTIFICATE_PASS` |
| Final verdict | `T4_MAIN_CERTIFICATE_PASS` |

## Why PP02B Matters

PP02B extends the evidence layer beyond token reduction and into math oriented structured evaluation.

It records 720 total outputs, including 600 model stress outputs and 120 compiled outputs.

Plain reading:

PP02B shows that the recorded SP math branch produced complete outputs, passed parsing and contract checks, produced zero family red count, zero compiler verifier red count, zero model stress warning count, and reached `T4_MAIN_CERTIFICATE_PASS`.

</details>

<details>
<summary>Details: PP02C</summary>

# PP02C: Coding Repair And Contract Validation

## What PP02C Tests

PP02C moves the public evidence layer toward coding repair and contract based validation.

Coding repair is easy to overclaim, so this branch uses stronger boundaries around hard vetoes, sandbox checks, warning checks, source behavior, and synthetic distractor behavior.

The simple version:

Can the branch pass strict coding repair checks without relying on fake sources, metadata as evidence, ignored source priority, or unsafe patch claims?

## PP02C Main Result Snapshot

| Metric | Value |
| --- | ---: |
| Main cases | 120 |
| Arms per case | 6 |
| Expected main outputs | 720 |
| Actual main outputs | 720 |
| Parse pass rate | 1.0 |
| Hard veto count | 0 |
| Warning count | 0 |
| Repo hallucination count | 0 |
| Metadata as evidence count | 0 |
| Synthetic distractor as source count | 0 |
| Source priority ignored count | 0 |
| Exact patch without source count | 0 |
| Contract missing field count | 0 |
| Contract enum invalid count | 0 |
| Contract value mismatch count | 0 |
| Claim ceiling pass rate | 1.0 |
| Overpass score | 120 |
| Final branch verdict | `FULL_SANDBOX_STRONG_PASS` |

## PP02C Supporting Checks

| Sub run | Cases | Outputs | Result |
| --- | ---: | ---: | --- |
| Final canonical result | 120 | 720 | `FULL_SANDBOX_STRONG_PASS` |
| Sandbox run 1 | 120 | 720 | `FULL_SANDBOX_STRONG_PASS` |
| Sandbox run 2 | 120 | 720 | `FULL_SANDBOX_STRONG_PASS` |
| Global hard veto matrix | 96 | 480 | `GLOBAL_HARD_VETO_MATRIX_STRONG_PASS` |
| Mini preflight | 24 | 96 | `MINI_PREFLIGHT_STRONG_PASS` |
| Synthetic distractor matrix | 64 | 320 | `SYNTHETIC_DISTRACTOR_MATRIX_STRONG_PASS` |

## Why PP02C Matters

PP02C is the strongest current public signal for the coding repair side of this experiment track.

The main run records 720 of 720 outputs, 100 percent parse success, zero hard vetoes, zero warnings, zero repo hallucination count, zero synthetic distractor as source count, and `FULL_SANDBOX_STRONG_PASS`.

Plain reading:

PP02C does not claim that all coding tasks are solved. It shows that this specific coding repair and contract validation branch passed the current recorded sandbox, hard veto, and synthetic distractor checks.

</details>

---

## What The Evidence Supports

The current public evidence supports a scoped reading:

Under the tested Polaris workloads, structured task representations can preserve strong output behavior, reduce token cost in the PP01 branch, and maintain inspectable evidence chains across raw outputs, parsed outputs, verdicts, audits, and hashes.

| Branch | Supported reading |
| --- | --- |
| PP01 | Strong evidence for topology first token reduction under the tested OSK workload |
| PP02A | Strong evidence for a T4 evidence branch reaching seal pass after a weaker reference |
| PP02B | Public evidence for a math oriented structured evaluation passing current T4 certificate checks |
| PP02C | Public evidence for coding repair and contract validation passing current sandbox and hard veto checks |

This is a public experiment trail.

It is not only a final claim.

---

## FAQ For Skeptical Readers

These results are strong, so skepticism is expected.

This section answers common questions directly.

<details>
<summary>Q1. Could the data be fake?</summary>

This is the right first question.

That is why this page is not only a screenshot gallery or a score table. The public packages include raw model outputs, parsed outputs, case verdicts, token accounting, audit records, and SHA256 file hashes.

If someone only wanted to fake a result, they would usually show only the final score.

Here, readers can inspect the evidence trail: what the model produced, how outputs were parsed, and how verdicts were assigned.

</details>

<details>
<summary>Q2. Did you only publish the best looking results?</summary>

This is a fair concern.

PP02A preserves a weaker previous reference run, not only the final pass. PP02C also preserves sandbox checks, hard veto checks, and synthetic distractor checks.

The goal is to publish the experiment trail, not only a victory screenshot.

This is still the first public evidence layer, not the final complete benchmark. Full mathematical logic, reproduction flow, and additional materials are planned after the 2026/05/05 open source release begins.

</details>

<details>
<summary>Q3. Is this just a shorter prompt?</summary>

No.

If you only make a prompt shorter, information is usually lost and quality often drops.

The Polaris direction is not simple prompt shortening. The task is broken down, structured, and represented more like a task map. The model receives clearer relationships instead of only less text.

Plain version:

A long context workflow is like giving the model a whole encyclopedia every time.  
The Polaris direction is more like giving the model a map.

That is why PP01 looks at token ratio and output quality together.

</details>

<details>
<summary>Q4. Did the prompts leak the answers?</summary>

The public packages include leakage checks and audit records.

For example, PP01 records leakage count as 0 and includes checks related to wrong source behavior and shadow overclaim. PP02C also preserves source behavior checks, synthetic distractor checks, and metadata as evidence checks.

These checks are meant to catch cases where the model appears to rely on answers, fake sources, or evidence that should not count.

This does not mean future experiments can never fail. It means the current public packages include the relevant checks instead of hiding them.

</details>

<details>
<summary>Q5. Why not publish the Colab notebooks and full math now?</summary>

Because this is the first public evidence layer, not the full execution package.

The current release publishes evidence first: raw outputs, parsed outputs, verdict tables, token accounting, audit records, and file hashes.

The full mathematical logic, execution notebooks, and Colab reproduction flow are planned for release after the 2026/05/05 open source release begins.

Simple reason:

Show the evidence first. Release deeper execution and mathematical materials next.

</details>

<details>
<summary>Q6. Does this prove small models always beat large models?</summary>

No.

A more precise statement is:

Under the tested Polaris workloads, structured task representations can reduce token cost in some branches while preserving strong output behavior.

This does not mean all small models beat all large models.

It also does not mean all tasks are solved.

PP01 supports a scoped claim: under the tested workload, structured task representation preserved strong output behavior while reducing token cost.

</details>

<details>
<summary>Q7. Does this prove all math, coding, and agent tasks are solved?</summary>

No.

The public data only supports the recorded experiment branches.

PP02B is a math oriented evidence package, but it does not claim that all mathematics is solved.

PP02C is a coding repair and contract validation evidence package, but it does not claim that all coding tasks are solved.

The careful reading is:

These packages show current branch results under specific test conditions, with inspectable evidence trails.

</details>

<details>
<summary>Q8. What is SHA256 for?</summary>

SHA256 is a file fingerprint.

If a ZIP file is changed, its SHA256 value usually changes.

The SHA256 records let readers check whether the downloaded file matches the public record.

Plain version:

SHA256 does not prove that an experiment is correct.

It helps prove that the file was not silently changed.

</details>

<details>
<summary>Q9. If I am not an engineer, where should I start?</summary>

Start with the README inside each ZIP package.

Then check the final verdict file, token accounting file, and audit records.

The simple path:

Read what the experiment tests.  
Check whether it passed.  
Check how much token cost was used.  
Check whether leakage, warnings, or hard vetoes were found.

If you want the fastest entry point, start with PP01 because it is the largest and cleanest public evidence package in this release.

</details>

<details>
<summary>Q10. What is the most important point of this release?</summary>

The most important point is not that there are many ZIP files.

The important point is:

Evidence is being published before the deeper mathematical and execution materials.

Readers do not have to trust only screenshots or slogans. They can inspect raw outputs, parsed outputs, verdict tables, token accounting, audit records, and file hashes.

This is the first public evidence layer of WFGY 5.0 Polaris Protocol before the 2026/05/05 open source release.

</details>

---

## What This Evidence Does Not Claim

This folder does not claim that:

* all AI tasks are solved
* all benchmarks are complete
* GPU scaling is globally disproven
* small models universally beat large models
* all coding tasks are solved
* all math tasks are solved
* all creative generation tasks are solved
* all multimodal tasks are solved
* all agent tasks are solved
* the full WFGY 5.0 Polaris Protocol implementation is already released here
* the full mathematical core is already released here

The current public status is narrower:

This is the first public evidence layer before the **2026/05/05** open source release.

---

## What Is Not Included Yet

These packages are public evidence packages, not full execution packages.

| Excluded item | Current status |
| --- | --- |
| Execution notebooks | Not included in this first evidence layer |
| Full mathematical logic | Planned for the 2026/05/05 open source release |
| Full implementation spine | Planned for later public release stages |
| Complete Colab reproduction notebooks | Planned to be linked through the official WFGY repository |
| Final universal benchmark suite | Not claimed in this first evidence layer |

This release makes the evidence inspectable first.

The deeper mathematical logic and reproduction materials are planned to follow after the open source release begins.

---

## Reproducibility Plan

The experiments are designed for Colab based reproduction workflows.

The current ZIP files are public evidence packages, not full execution packages.

| Item | Included now |
| --- | --- |
| Raw outputs | Yes |
| Parsed outputs | Yes |
| Verdict tables | Yes |
| Token accounting | Yes |
| Audit records | Yes |
| SHA256 records | Yes |
| Execution notebooks | Not yet |
| Core mathematical logic | Not yet |
| Colab reproduction materials | Planned after release |

Future reproduction materials will be referenced from:

https://github.com/onestardao/WFGY

---

## Integrity Hashes

SHA256 values for the current public ZIP files:

| Package | SHA256 |
| --- | --- |
| `wfgy5_polaris_protocol_pp01_t4_osk_320case_public_evidence_20260503.zip` | `ff0caa1d7784199d4dcddf558a822041bc026a93b57dfe9e5af0ce3245311856` |
| `wfgy5_polaris_protocol_pp02a_t4_120case_public_evidence_20260503.zip` | `28f2ca19a0a6bac27967bedbc07b4c2f9b44f1c212687ae74512967d42a2e7ad` |
| `wfgy5_polaris_protocol_pp02b_sp_120case_public_evidence_20260503.zip` | `10c5d39a15d74afb29d89386147ba60e830fc624b050d53f0e4187c97fe3df65` |
| `wfgy5_polaris_protocol_pp02c_t4_120case_public_evidence_20260503.zip` | `a85b7919da2fae8c543189fbaf586e3573af73642a1e410e49e5df6a5e6bb9f8` |
| `wfgy5_polaris_protocol_public_evidence_bundle_20260503.zip` | `50ed006c83f25d69b3080da044882e21663ada2cecb432622b843411d078657e` |

---

## Suggested Short Description

Public evidence layer for WFGY 5.0 Polaris Protocol, including raw outputs, parsed outputs, verdicts, token accounting, audits, SHA256 records, and pre release experiment packages for PP01, PP02A, PP02B, and PP02C.

---

## Current Status

| Field | Value |
| --- | --- |
| Project | WFGY 5.0 Polaris Protocol |
| Folder role | Public evidence layer |
| Release type | First public evidence layer |
| Public branches | PP01, PP02A, PP02B, PP02C |
| Main evidence packages | 4 |
| Main branch test cases | 680 |
| Main branch primary outputs | 3600 |
| Raw outputs | Included |
| Parsed outputs | Included |
| Verdict files | Included |
| Audit files | Included |
| Token accounting | Included |
| SHA256 records | Included |
| Execution notebooks | Not included yet |
| Private mathematical core | Not included in this first layer |
| Full implementation release | Planned after the 2026/05/05 open source release begins |
| License | MIT License, unless a specific file states otherwise |
| Repository | https://github.com/onestardao/WFGY |

---

## Final Note

This folder exists to make the evidence visible before the full open source release.

The current packages show the experiment trail:

case design, raw output, parsing, scoring, token accounting, audit, verdicts, and integrity records.

The full mathematical logic and reproduction materials are planned to follow after the 2026/05/05 release begins.
