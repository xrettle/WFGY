# Polaris Experimental Evidence Packages 🌌

> Traditional Chinese version: [`README.zh-TW.md`](./README.zh-TW.md)  
> Note: Not every WFGY page currently has a Traditional Chinese version. If there is any difference between this English page and the Traditional Chinese page, please treat the English page as the primary reference.

This is the public experimental evidence page for **WFGY 5.0 Polaris Protocol**.

The purpose of this page is simple:

You should be able to understand what these experiments are testing, why they matter for AI cost, what the four evidence packages represent, and what the current results can and cannot claim, without downloading any ZIP file first.

The ZIP files are mainly for people who want to reproduce, research, audit, or inspect the raw model outputs.

Official repository:

https://github.com/onestardao/WFGY

License:

Unless a specific file states otherwise, this project uses the MIT License.

<a id="top"></a>

---

## Quick Navigation 🧭

| What you want to see | Jump to |
| --- | --- |
| Understand the experiment first | [3-minute overview](#quick-start) |
| What the four packages mean | [Four public evidence packages](#evidence-packs) |
| Core numbers | [Core results overview](#results) |
| Whether the tasks were too easy | [Task design and rigor](#rigor) |
| How skeptic questions are answered | [FAQ and skeptic attacks](#faq) |
| Download or reproduce | [Downloads and file verification](#downloads) |
| What this does not claim | [Claim boundary](#claim-ceiling) |

---

<a id="quick-start"></a>

## 3-minute overview ⚡

AI cost is rising, not only because models are getting larger, but also because many tasks repeatedly push large amounts of background, rules, constraints, examples, and context into the model.

The more tokens a model has to read, the higher the inference cost becomes.

The Polaris experiment asks:

> Instead of giving the model the entire instruction book every time, what if we first organize the task into a more stable structure, then ask the model to produce the output? Can we use far fewer tokens while still preserving inspectable output quality?

This is not simply shortening a prompt.

If you only shorten a prompt, you may also remove important constraints, boundaries, scoring conditions, and error checks. Polaris is not about aggressively deleting text. It is about extracting the important relationships inside the task.

What it tries to preserve:

| What should be preserved | Why it matters |
| --- | --- |
| Task goal | Helps the model understand what must be completed |
| Constraints | Prevents the model from drifting |
| Order relations | Prevents missing or skipping steps |
| Boundary rules | Prevents overextension |
| Error risks | Prevents common false success patterns |
| Audit conditions | Makes the result inspectable |

In plain language:

A traditional long-context approach is like handing the model an entire city encyclopedia every time.

The Polaris approach is more like drawing a city map, including roads, relations, danger zones, destinations, and checkpoints.

The point is not to make the information smaller.

The point is to make the information clearer.

One sentence summary:

> Polaris does not make the task smaller. It makes the task clearer. 🧠

<details>
<summary>Expand: What does this have to do with GPU cost?</summary>

When people talk about AI cost, they usually think about GPUs first.

That is not wrong. GPU cost is a major part of model inference cost.

But in real use cases, cost does not only come from the GPU itself. It also comes from how many tokens the model has to read, how many tokens it has to generate, how many rounds it has to run, and how much long-context baggage it has to carry.

If every task requires a large block of background text, the model must repeatedly read a large amount of content.

That becomes cost.

The Polaris idea is:

Besides pursuing larger models, stronger GPUs, and longer context windows, we can also ask another question:

Can the task itself be represented in a smarter way first?

If a task can be organized into a more stable structure, the model may not need to reread an entire library every time. It may only need to read a clearer task map.

So Polaris is not saying that GPUs are unimportant.

It is saying:

AI cost can be approached not only from the hardware side, but also from the task-structure side.

</details>

<details>
<summary>Expand: This is not simply making the prompt shorter</summary>

If you only make the prompt shorter, you usually lose information, and output quality may drop.

The key point of Polaris is not aggressive text deletion. It is reorganizing task content into a more stable structure.

You can think of it like this:

| Original long text | After conversion |
| --- | --- |
| A long task description | Task nodes |
| Many rules | Rule relations |
| Multiple goals | Goal order |
| Multiple constraints | Boundary conditions |
| Possible errors | Audit points |
| Final output | Output format |

This means the model does not receive a long messy block of text. It receives a clearer task structure.

The model’s job then becomes more like:

Read the task map.  
Translate the map back into the correct output.  
Complete the requested task.

So you can understand it as:

> First turn the task into structure, then let the model translate that structure into an answer.

</details>

[Back to quick navigation](#top)

---

<a id="evidence-packs"></a>

## Four public evidence packages 📦

This page currently publishes four main evidence packages.

They are not four copies of the same material. They represent four different angles of evidence.

| Evidence package | What it answers | One-line meaning |
| --- | --- | --- |
| PP01 / Main evidence bundle | After task structuring, can token cost be reduced while preserving quality? | Main cost battlefield |
| PP02A | Can the T4 branch move from a weaker version to final pass? | Version evolution evidence |
| PP02B | Can math-leaning tasks form an inspectable structured evidence chain? | Math stress test |
| PP02C | Can code repair preserve source boundaries, sandbox checks, and hard red lines? | Skeptic red-line test |

### PP01 / Main evidence bundle

This is the best package for first-time readers to start with.

It answers:

Can structured task representation preserve inspectable output quality while using far fewer tokens?

This page treats `wfgy5_polaris_protocol_public_evidence_bundle_20260503.zip` as the **PP01 / Main evidence bundle** and the current public evidence entry point.

### PP02A

This package focuses on the T4 evidence branch.

Its value is not only that the final result passes. It also preserves the evolution path, so readers can see that this is not just a cherry-picked victory screenshot.

### PP02B

This package focuses on math-leaning tasks.

It does not claim that all math problems have been solved. It shows how, within this task set, model outputs, normalized results, family verdicts, contract checks, and certificate results form an inspectable evidence chain.

### PP02C

This package focuses on code repair, sandbox checks, source boundaries, and hard red lines.

Code repair is especially prone to false success, such as guessing repository content, misusing metadata, following distractor sources, claiming precise fixes without evidence, or ignoring source priority. PP02C is designed to check exactly these problems.

[Back to quick navigation](#top)

---

<a id="results"></a>

## Core results overview 📊

The current public release is the first-layer experimental evidence for the pre-release stage of WFGY 5.0 Polaris Protocol.

This layer focuses on publishing results, evidence chains, and auditable materials. It is not a full open-source execution package.

| Item | Count or status |
| --- | ---: |
| Main public evidence packages | 4 |
| Main test cases | 680 |
| Main model outputs | 3600 |
| PP01 outputs | 1920 |
| PP02A final-run outputs | 240 |
| PP02B outputs | 720 |
| PP02C main-run outputs | 720 |
| Full core mathematics included | 0 |
| Full Colab execution notebook included | 0 |

What the current public version can support:

> Within the currently published task scope, Polaris shows a signal worth paying attention to: if a task is first organized into a more stable structure, it may reduce token cost while preserving inspectable output quality.

What the current public version should not be interpreted as:

| Should not be interpreted as | Explanation |
| --- | --- |
| All AI tasks have been solved | The current scope only covers the specified public tasks |
| Small models completely beat large models | The current evidence supports structured-task effects in specific tasks |
| GPU scaling is no longer important | GPUs remain important; Polaris is a task-structure-side cost route |
| A third-party official benchmark | This is a self-built public experimental evidence chain |
| Full core mathematics already released | The current release is an evidence package, not the full core |
| Full Colab reproduction flow already released | Full reproduction materials will be added after the official open-source release |

Full core mathematics, formal reproduction materials, and more release materials are expected to be added after the official open-source release.

<details>
<summary>Expand: detailed result snapshots of the four packages</summary>

### PP01 / Main evidence bundle

| Metric | Value |
| --- | ---: |
| Test cases | 320 |
| Test groups | 6 |
| Expected outputs | 1920 |
| Actual outputs | 1920 |
| Parse pass rate | 1.0 |
| Leakage count | 0 |
| Group C average score | 0.988465 |
| Group B average score | 0.967265 |
| Group C retention rate vs Group B | 1.0219 |
| Group C total token ratio vs Group A | 0.1656 |
| Group C input token ratio vs Group A | 0.1242 |
| Failure signature match rate | 1.0 |
| Overclaim count | 0 |
| Critical wrong-source count | 0 |
| Family collapse count | 0 |
| Hard checks passed | true |
| Final pass | true |
| Global status | `OSK_MVP_FINAL_PASS` |

### PP02A

| Metric | Final value |
| --- | ---: |
| Test cases | 120 |
| Final-run raw outputs | 240 |
| Domains | 6 |
| API errors | 0 |
| Parse failures | 0 |
| Parse success rate | 1.0 |
| Weak rows | 0 |
| Domains reaching seal | 6 |
| Domains reaching dominant or better | 6 |
| Domains reaching release or better | 6 |
| T4 system score | 100.0 |
| Internal weighted score | 125.0 |
| Final result | `SEAL_PASS` |

PP02A also preserves a weaker previous reference record: parse success rate 0.9958, weak rows 1, domains reaching seal 5, final result `INVALID`.

### PP02B

| Metric | Value |
| --- | ---: |
| Test cases | 120 |
| Expected compiled outputs | 120 |
| Actual compiled outputs | 120 |
| Expected total outputs | 720 |
| Actual total outputs | 720 |
| Expected model stress outputs | 600 |
| Actual model stress outputs | 600 |
| Model API calls | 600 |
| Group C parse pass rate | 1.0 |
| Group C contract pass rate | 1.0 |
| Family red count | 0 |
| Compile verification red count | 0 |
| Model stress warning count | 0 |
| Model stress result | `MODEL_STRESS_PASS` |
| Main certificate result | `T4_MAIN_CERTIFICATE_PASS` |
| Final result | `T4_MAIN_CERTIFICATE_PASS` |

### PP02C

| Metric | Value |
| --- | ---: |
| Main test cases | 120 |
| Test groups per case | 6 |
| Expected main outputs | 720 |
| Actual main outputs | 720 |
| Parse pass rate | 1.0 |
| Hard red-line count | 0 |
| Warning count | 0 |
| Library hallucination count | 0 |
| Metadata-as-evidence count | 0 |
| Distractor-source-as-official-source count | 0 |
| Source-priority-ignore count | 0 |
| Precise-fix-without-source count | 0 |
| Contract missing-field count | 0 |
| Contract enum-error count | 0 |
| Contract value-mismatch count | 0 |
| Claim-boundary pass rate | 1.0 |
| Surplus pass score | 120 |
| Final branch result | `FULL_SANDBOX_STRONG_PASS` |

PP02C also includes supporting checks such as sandbox runs, a global hard-veto matrix, a mini preflight test, and a synthetic distractor matrix.

</details>

[Back to quick navigation](#top)

---

<a id="rigor"></a>

## Task design and rigor 🧪

These experiments are not a few showcase questions used for performance theater.

If we only selected a few questions the model happened to answer well, the page could look impressive, but the result would have little research value.

The Polaris experiments use family-based design.

This means:

Instead of only asking “Did the model get the answer right?”, the tasks separate different failure types and check whether the model can preserve task structure, source boundaries, error checks, and claim boundaries under different kinds of pressure.

In simple terms:

> We are not choosing a few easy roads for the model to walk on. We first mark the places where models tend to fall, then check whether it can walk through them reliably. 🕳️

### Why not use single-question demonstrations?

Single-question demonstrations usually have three problems:

| Problem | Risk |
| --- | --- |
| Too few questions | The model may simply happen to know them |
| Too smooth | Boundaries and failure risks are not exposed |
| Only final answers are inspected | You cannot see whether the model skipped steps, guessed sources, or overclaimed |

So these experiments do not only check whether the final output looks good.

They also check:

| Check direction | Why it matters |
| --- | --- |
| Whether the task keeps its original meaning | Prevents the model from turning the problem into an easier one |
| Whether conditions are preserved | Prevents the model from ignoring constraints |
| Whether sources are reliable | Prevents guessing or using the wrong material |
| Whether the result overclaims | Prevents local results from being inflated into general conclusions |
| Whether there is leakage | Prevents task or answer contamination |
| Whether hard red lines are crossed | Prevents good-looking answers from hiding unacceptable errors |
| Whether raw outputs can be inspected | Prevents reliance only on normalized summaries |

### What risks do the four branches test?

| Branch | Main test direction | What it protects against |
| --- | --- | --- |
| PP01 / Main evidence bundle | Token cost reduction and quality retention | Saving tokens while quality collapses, or results supported by leakage and overclaiming |
| PP02A | T4 evidence branch and version evolution | Showing only the final good result without preserving process context |
| PP02B | Structured testing for math-leaning tasks | Symbol drift, condition loss, false equivalence, ignored counterexamples |
| PP02C | Code repair, source boundaries, sandbox checks, and hard red lines | Repository hallucination, metadata misuse, distractor-source misuse, precise-fix claims without evidence |

These four branches are not testing the same thing repeatedly.

They correspond to different risk surfaces:

PP01 checks the main cost signal.

PP02A checks the evidence path.

PP02B checks math-leaning reasoning pressure.

PP02C checks code repair and skeptic red lines.

<details>
<summary>Expand: Were the tasks intentionally made easy?</summary>

No.

A more precise way to say it:

The tasks were not designed to make the model look impressive. They were designed so common errors would have a chance to appear.

PP01 does not only check whether tokens decrease. It also checks quality, leakage, wrong sources, and overclaiming.

PP02A does not only check the final pass. It also preserves a weaker previous reference record.

PP02B does not only check whether the math answer looks good. It checks symbols, conditions, assumptions, counterexamples, and reasoning structure.

PP02C does not only check whether the code answer sounds plausible. It checks source usage, sandbox checks, distractor sources, and hard red lines.

So the task design is not “watering things down.”

It is closer to:

> Turn common model failure paths into a test field, then check whether Polaris can reduce those failures.

</details>

<details>
<summary>Expand: Why is a self-built experiment still valuable?</summary>

This is a self-built public experiment, not a third-party official benchmark.

So it should not be packaged as an external authority ranking.

But a self-built experiment can still be valuable, as long as it does not only publish the final score.

It must allow readers to inspect the path backward:

| If only the result is shown | Trust problem |
| --- | --- |
| Only a total score | You cannot see how each case was judged |
| Only screenshots | You cannot see raw model outputs |
| Only good-looking examples | You cannot tell whether results were cherry-picked |
| Only conclusions | You cannot tell whether claims were inflated |
| No file fingerprint | You cannot verify file consistency |

This release publishes the evidence chain:

Raw model outputs.  
Normalized outputs.  
Per-case verdicts.  
Token cost.  
Audit records.  
Warning records.  
Hard red lines.  
File fingerprints.

So the position of this material is not:

> Please believe that we are strong.

It is:

> This is the currently public experimental trace. You can inspect it backward from the result.

</details>

[Back to quick navigation](#top)

---

<a id="faq"></a>

## FAQ and skeptic attacks 🛡️

This section answers the questions first-time readers and skeptics are most likely to ask.

<details>
<summary>Q1. Is this just making the prompt shorter?</summary>

> No.
>
> A short prompt reduces words.
>
> Polaris organizes task structure.
>
> If you only shorten text, you can easily remove constraints, boundaries, scoring conditions, and error checks. Polaris tries to preserve those key pieces of information, but organize them into a task map that is easier for the model to use.
>
> In plain language:
>
> The traditional approach is like giving the model an entire encyclopedia every time.
>
> The Polaris approach is more like drawing a map first, then asking the model to complete the task by following the map.

</details>

<details>
<summary>Q2. Is this just a self-made experiment congratulating itself?</summary>

> This is a self-built public experiment, not a third-party official benchmark.
>
> But it still has value because it does not only publish the final score.
>
> The material publishes an evidence chain, including raw model outputs, normalized results, per-case verdicts, token cost, audit records, warning records, hard red lines, and file fingerprints.
>
> So its position is not external ranking. It is inspectable public experimental evidence.
>
> More precisely:
>
> This is not asking you to first believe that we are strong.
>
> It first publishes the experimental trace, so you can inspect backward from the result.

</details>

<details>
<summary>Q3. Were the tasks intentionally made simple?</summary>

> This is not a single-question showcase. It uses family-based pressure design.
>
> PP01 tests cost and quality retention.
>
> PP02A tests version evolution and evidence path.
>
> PP02B tests symbols, conditions, counterexamples, and reasoning pressure in math-leaning tasks.
>
> PP02C tests code repair, source boundaries, sandbox checks, and hard red lines.
>
> These branches do not only test comfortable scenarios. They check different types of failure risk.
>
> So this task design is not watered down.
>
> It is closer to:
>
> Turn common model failure paths into a test field, then check whether Polaris can reduce those failures.

</details>

<details>
<summary>Q4. Did you leak answers or contaminate the tasks?</summary>

> The public packages do not only publish total scores. They also include leakage checks, raw outputs, normalized results, and audit records.
>
> This does not mean future experiments can never make mistakes.
>
> It means this public release does not only provide a beautiful screenshot. It preserves inspection material that can be checked backward.
>
> For example:
>
> PP01 checks leakage, wrong sources, overclaiming, and family collapse.
>
> PP02C checks source behavior, distractor sources, metadata as evidence, sandbox checks, and hard red lines.
>
> The purpose of these checks is to avoid models relying on leaked answers, misusing sources, or treating non-evidence as evidence.

</details>

<details>
<summary>Q5. Does this mean small models completely beat large models?</summary>

> No.
>
> A more precise statement is:
>
> Within the currently published task scope, Polaris shows a signal that structured task representation can reduce token cost while preserving inspectable output quality.
>
> This should not be interpreted as all small models completely beating all large models.
>
> It should also not be interpreted as all AI tasks being solved.
>
> What can be said for now:
>
> In these public test branches, structured task representation shows a cost and quality signal worth paying attention to.

</details>

<details>
<summary>Q6. Does this mean GPU scaling is no longer important?</summary>

> No.
>
> GPUs remain important.
>
> Polaris focuses on reducing cost from another direction: improving the representation of the task itself, so the model does not have to reread large amounts of context every time.
>
> In other words:
>
> Hardware scaling is one path.
>
> Task-structure optimization is another path.
>
> These experiments are not saying GPUs are unimportant. They are showing that AI cost can also be reconsidered from the task-structure side.

</details>

<details>
<summary>Q7. Why do the ZIP files not include the full core mathematics and full Colab yet?</summary>

> Because this release is a pre-release evidence package, not a full execution package.
>
> The current goal is to let readers inspect raw model outputs, verdicts, cost, audits, warnings, red lines, and file fingerprints first.
>
> Full core mathematics, formal reproduction materials, and more release materials will be added after the official open-source release.
>
> In simple terms:
>
> This version publishes the evidence first.
>
> Deeper mathematical logic and reproduction materials will follow later.

</details>

<details>
<summary>Q8. What is the most important meaning of this release?</summary>

> The most important point is not that there are many ZIP files.
>
> The most important point is:
>
> Evidence is published first, before deeper mathematics and execution materials are released.
>
> This means readers do not have to rely only on screenshots or slogans. They can first inspect raw model outputs, normalized results, verdict tables, token cost, audit records, and file fingerprints.
>
> In other words:
>
> This material is not asking you to believe first.
>
> It first publishes the public evidence chain so you can understand it and inspect backward. ✨

</details>

[Back to quick navigation](#top)

---

<a id="downloads"></a>

## Downloads and file verification 🧾

If you only want a quick understanding, reading this README should be enough.

The ZIP files are mainly for people who want to reproduce, research, audit, or inspect raw outputs.

The current official public evidence packages are the following four files:

| Official name | File | Purpose |
| --- | --- | --- |
| PP01 / Main evidence bundle | `wfgy5_polaris_protocol_public_evidence_bundle_20260503.zip` | Main cost evidence and public evidence entry point |
| PP02A | `wfgy5_polaris_protocol_pp02a_t4_120case_public_evidence_20260503.zip` | T4 evidence branch and version evolution |
| PP02B | `wfgy5_polaris_protocol_pp02b_sp_120case_public_evidence_20260503.zip` | Structured testing for math-leaning tasks |
| PP02C | `wfgy5_polaris_protocol_pp02c_t4_120case_public_evidence_20260503.zip` | Code repair, sandbox checks, and hard red lines |

Download links:

| File | Download |
| --- | --- |
| `wfgy5_polaris_protocol_public_evidence_bundle_20260503.zip` | [Download](./downloads/wfgy5_polaris_protocol_public_evidence_bundle_20260503.zip) |
| `wfgy5_polaris_protocol_pp02a_t4_120case_public_evidence_20260503.zip` | [Download](./downloads/wfgy5_polaris_protocol_pp02a_t4_120case_public_evidence_20260503.zip) |
| `wfgy5_polaris_protocol_pp02b_sp_120case_public_evidence_20260503.zip` | [Download](./downloads/wfgy5_polaris_protocol_pp02b_sp_120case_public_evidence_20260503.zip) |
| `wfgy5_polaris_protocol_pp02c_t4_120case_public_evidence_20260503.zip` | [Download](./downloads/wfgy5_polaris_protocol_pp02c_t4_120case_public_evidence_20260503.zip) |

The downloads folder may also contain earlier process files. First-time readers should use the four official public evidence packages listed above as the main reference.

<details>
<summary>Expand: suggested inspection order for engineers</summary>

| Order | Suggested check | Why it matters |
| --- | --- | --- |
| 1 | Raw model outputs | Confirms that the run actually produced model responses |
| 2 | Normalized outputs | Shows how outputs were converted into structured records |
| 3 | Per-case verdicts | Shows how each case maps to a result |
| 4 | Group or stage verdicts | Shows higher-level result patterns |
| 5 | Token cost records | Checks cost and token efficiency behavior |
| 6 | Audit records | Checks leakage, warnings, hard vetoes, or source quality checks |
| 7 | SHA256 records | Checks file integrity |

</details>

<details>
<summary>Expand: SHA256 file fingerprints</summary>

SHA256 can be understood as a file fingerprint.

It does not prove that the experimental conclusion is correct. It verifies whether the ZIP you downloaded is consistent with the public record.

| File | SHA256 |
| --- | --- |
| `wfgy5_polaris_protocol_public_evidence_bundle_20260503.zip` | `50ed006c83f25d69b3080da044882e21663ada2cecb432622b843411d078657e` |
| `wfgy5_polaris_protocol_pp02a_t4_120case_public_evidence_20260503.zip` | `28f2ca19a0a6bac27967bedbc07b4c2f9b44f1c212687ae74512967d42a2e7ad` |
| `wfgy5_polaris_protocol_pp02b_sp_120case_public_evidence_20260503.zip` | `10c5d39a15d74afb29d89386147ba60e830fc624b050d53f0e4187c97fe3df65` |
| `wfgy5_polaris_protocol_pp02c_t4_120case_public_evidence_20260503.zip` | `a85b7919da2fae8c543189fbaf586e3573af73642a1e410e49e5df6a5e6bb9f8` |

</details>

[Back to quick navigation](#top)

---

<a id="claim-ceiling"></a>

## Claim boundary 🚧

What this material can currently say:

| Can say | Explanation |
| --- | --- |
| Polaris shows a strong token-cost reduction signal within the public task scope | Especially in the PP01 main cost experiment |
| Structured task representation may preserve inspectable output quality | The evidence chain matters, not only whether the answer looks good |
| The four public packages cover different risk surfaces | Cost, version evolution, math-leaning tasks, code repair, and red lines |
| ZIP files allow researchers and skeptics to inspect backward | Includes raw outputs, verdicts, cost, audits, and file fingerprints |

What this material currently cannot say:

| Cannot say | Reason |
| --- | --- |
| All AI tasks have been solved | The current scope only covers specified public tasks |
| Small models completely beat large models | The current evidence supports structured effects in specific tasks |
| GPU scaling is no longer important | GPUs remain important; Polaris is a task-structure-side cost route |
| This is a third-party official benchmark | This is a self-built public experimental evidence chain |
| The ZIP files include full core mathematics | The current release is an evidence package, not the full core |
| A full Colab reproduction flow is already provided | Full reproduction materials will be added after the official open-source release |

One-sentence summary:

> This material does not ask you to believe first. It first publishes the public evidence chain so you can understand it and inspect backward. ✨

[Back to quick navigation](#top)

---

## Suggested short description ✍️

The public evidence layer for WFGY 5.0 Polaris Protocol, including raw model outputs, normalized outputs, verdict tables, token cost records, audit records, SHA256 file fingerprints, and pre-release experimental evidence packages for PP01, PP02A, PP02B, and PP02C.

---

## Current status 📌

| Field | Content |
| --- | --- |
| Project | WFGY 5.0 Polaris Protocol |
| Folder role | Public experimental evidence layer |
| Release type | First-layer public evidence |
| Public branches | PP01, PP02A, PP02B, PP02C |
| Main evidence packages | 4 |
| Main branch test cases | 680 |
| Main branch model outputs | 3600 |
| Raw model outputs | Included |
| Normalized outputs | Included |
| Verdict files | Included |
| Audit files | Included |
| Token cost records | Included |
| SHA256 records | Included |
| Execution notebook | Not yet included |
| Core mathematics | Not included in the first-layer public evidence |
| Full implementation release | Expected after the official open-source release begins |
| License | MIT License unless a specific file states otherwise |
| Repository | https://github.com/onestardao/WFGY |

---

## Final note 🌱

The purpose of this folder is to make evidence visible before the full open-source release.

The current packages show the experimental trace:

task design, raw model outputs, parsing, scoring, token cost, audits, result verdicts, and file integrity records.

The full mathematical logic and reproduction materials are expected to follow after the official open-source release begins.
