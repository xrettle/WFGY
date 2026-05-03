# Polaris Experiments

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

## Why This Page Exists

Most AI result pages show only the final score.

This page is different.

The goal is to expose the experiment trail itself:

| Layer | What is exposed |
| --- | --- |
| Test layer | case manifests and branch descriptions |
| Output layer | raw model outputs |
| Parse layer | parsed structured outputs |
| Verdict layer | case verdicts, family verdicts, stage verdicts, certificates |
| Cost layer | token accounting and token related records |
| Audit layer | leakage checks, hard veto checks, warning tables, Blackfan style audit records |
| Integrity layer | SHA256 hashes and manifest records |

For non technical readers, this means:

You do not have to trust a screenshot.

You can download the evidence.

For engineers, this means:

You can inspect the raw outputs, parsed outputs, verdict rows, token tables, audit records, and integrity files directly.

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

This is the first public evidence layer before the full **2026 05 05** open source release.

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

## How To Read The Evidence

If you are not an engineer, start here:

| Step | What to open | What it tells you |
| --- | --- | --- |
| 1 | README inside each package | What this experiment branch is about |
| 2 | final verdict or certificate file | Whether the branch passed its current gate |
| 3 | token accounting file | How much token budget was used |
| 4 | audit files | Whether leakage, warnings, hard vetoes, or failure surfaces were found |
| 5 | raw outputs | What the model actually produced |

If you are an engineer, start here:

| Step | What to inspect | Why it matters |
| --- | --- | --- |
| 1 | raw outputs | Confirms that the run produced real model responses |
| 2 | parsed outputs | Shows how outputs were converted into structured records |
| 3 | case verdicts | Connects each case to a verdict |
| 4 | family or stage verdicts | Shows broader pattern level results |
| 5 | token accounting | Shows cost and token efficiency behavior |
| 6 | audit records | Shows leakage checks, warning checks, hard veto checks, or source quality checks |
| 7 | SHA256 manifests | Lets readers verify file integrity |

---

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

---

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

---

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

---

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

---

# What The Evidence Supports

The current public evidence supports a scoped reading:

Under the tested Polaris workloads, structured task representations can preserve strong output behavior, reduce token cost in the PP01 branch, and maintain inspectable evidence chains across raw outputs, parsed outputs, verdicts, audits, and hashes.

More specifically:

| Branch | Supported reading |
| --- | --- |
| PP01 | Strong evidence for topology first token reduction under the tested OSK workload |
| PP02A | Strong evidence for a T4 evidence branch reaching seal pass after a weaker reference |
| PP02B | Public evidence for a math oriented structured evaluation passing current T4 certificate checks |
| PP02C | Public evidence for coding repair and contract validation passing current sandbox and hard veto checks |

This is a public experiment trail.

It is not only a final claim.

---

# What This Evidence Does Not Claim

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

This is the first public evidence layer before the **2026 05 05** open source release.

---

# What Is Not Included Yet

These packages are public evidence packages, not full execution packages.

They do not include:

| Excluded item | Current status |
| --- | --- |
| Execution notebooks | Not included in this first evidence layer |
| Full mathematical logic | Planned for the 2026 05 05 open source release |
| Full implementation spine | Planned for later public release stages |
| Complete Colab reproduction notebooks | Planned to be linked through the official WFGY repository |
| Final universal benchmark suite | Not claimed in this first evidence layer |

This release makes the evidence inspectable first.

The deeper mathematical logic and reproduction materials are planned to follow after the open source release begins.

---

# Reproducibility Plan

The experiments are designed for Colab based reproduction workflows.

The current ZIP files are public evidence packages, not full execution packages.

That means:

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

# Integrity Hashes

SHA256 values for the current public ZIP files:

| Package | SHA256 |
| --- | --- |
| `wfgy5_polaris_protocol_pp01_t4_osk_320case_public_evidence_20260503.zip` | `ff0caa1d7784199d4dcddf558a822041bc026a93b57dfe9e5af0ce3245311856` |
| `wfgy5_polaris_protocol_pp02a_t4_120case_public_evidence_20260503.zip` | `28f2ca19a0a6bac27967bedbc07b4c2f9b44f1c212687ae74512967d42a2e7ad` |
| `wfgy5_polaris_protocol_pp02b_sp_120case_public_evidence_20260503.zip` | `10c5d39a15d74afb29d89386147ba60e830fc624b050d53f0e4187c97fe3df65` |
| `wfgy5_polaris_protocol_pp02c_t4_120case_public_evidence_20260503.zip` | `a85b7919da2fae8c543189fbaf586e3573af73642a1e410e49e5df6a5e6bb9f8` |
| `wfgy5_polaris_protocol_public_evidence_bundle_20260503.zip` | `50ed006c83f25d69b3080da044882e21663ada2cecb432622b843411d078657e` |

---

# Suggested Short Description

Public evidence layer for WFGY 5.0 Polaris Protocol, including raw outputs, parsed outputs, verdicts, token accounting, audits, SHA256 records, and pre release experiment packages for PP01, PP02A, PP02B, and PP02C.

---

# Current Status

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
| Full implementation release | Planned after the 2026 05 05 open source release begins |
| License | MIT License, unless a specific file states otherwise |
| Repository | https://github.com/onestardao/WFGY |

---

# Final Note

This folder exists to make the evidence visible before the full open source release.

The current packages show the experiment trail:

case design, raw output, parsing, scoring, token accounting, audit, verdicts, and integrity records.

The full mathematical logic and reproduction materials are planned to follow after the 2026 05 05 release begins.
