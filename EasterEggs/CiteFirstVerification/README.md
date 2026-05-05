# WFGY Easter Egg: Cite First Verification

<img width="1672" height="941" alt="WFGY_EGG" src="https://github.com/user-attachments/assets/1efdc596-ca38-4de7-ac14-fa156cd311a4" />

Make AI pay a confidence cost before it sounds certain.

Cite First Verification, or CFV, is a small WFGY Easter Egg that makes AI answers expose confidence on the surface. Instead of letting every polished sentence sound equally reliable, CFV adds compact confidence scores, softens weak statements, and blocks low confidence claims in strict mode.

This is a playable preview from the WFGY line.

It is small enough to try in one prompt, but sharp enough to change how an answer feels.

```text
Use WFGY with CFV Strict. Show only surface CI.
```

## The problem

AI does not usually fail by looking confused.

It fails by sounding smooth.

A weak answer can look clean.
A guessed detail can sound factual.
A fragile conclusion can arrive with the same tone as a verified one.

CFV changes that surface.

It asks a simple question before the answer leaves the model:

```text
How much confidence does this claim deserve?
```

## What CFV does

CFV adds a confidence layer to AI answers.

| Without CFV | With CFV |
|---|---|
| Every sentence can sound equally certain. | Important claims carry visible confidence. |
| Weak claims may hide inside fluent writing. | Weak claims are softened, rewritten, or held. |
| You need to ask "are you sure?" after the answer. | Confidence appears while you read. |
| The answer feels final too early. | The answer shows which parts deserve caution. |
| Verification stays invisible. | Surface CI gives a quick trust signal. |

CFV does not make the model louder.

It makes uncertainty harder to hide.

## Try it in one minute

Paste this into a chat after loading the WFGY Easter Egg text:

```text
Use WFGY with CFV Strict. Show only surface CI.

Explain the strongest and weakest parts of this argument:
[PASTE YOUR TEXT HERE]
```

Expected style:

```text
The main claim is plausible if the evidence source is reliable. (0.78)

The numeric conclusion needs stronger support before it should be treated as verified. (0.61)

The statement about universal performance is too broad and should be softened. (0.49, rewritten)

A safer conclusion is that the result supports this test setting, not every possible use case. (0.84)
```

## What might appear?

| Signal | What it means |
|---|---|
| `(0.92)` | Strong confidence |
| `(0.78)` | Good confidence, still not absolute |
| `(0.63)` | Usable but needs caution |
| `(0.49, rewritten)` | Weak claim repaired before final output |
| `speculative` | The answer should not sound fully certain |
| `held` | Strict mode stopped a weak claim from being emitted as fact |
| `ledger available` | Extra reasons can be expanded when requested |

The default surface stays simple.

You see the confidence signal first.
You ask for the deeper ledger only when you need it.

## Why this is an Easter Egg

CFV is not a full product launch.

It is a small mechanism released early so builders can play with one piece of the WFGY direction before the larger system arrives.

The goal is simple:

```text
Less fake certainty.
More visible confidence.
Cleaner trust signals.
```

## Modes

| Mode | Behavior |
|---|---|
| Strict | Low confidence claims are blocked, rewritten, or changed into cautious language. |
| Soft | Low confidence claims may pass, but the score remains visible. |

Recommended first run:

```text
Use WFGY with CFV Strict. Show only surface CI.
```

Observation run:

```text
Use WFGY with CFV Soft. Keep low confidence claims visible.
```

Deep check run:

```text
Use WFGY with CFV Strict. Show surface CI first. Expand the evidence ledger only for claims below 0.75.
```

## Confidence Index

CI means Confidence Index.

| CI range | Label | Surface meaning |
|---:|---|---|
| `0.90+` | Verified | Strong confidence |
| `0.75 to 0.89` | High | Reliable enough for normal use |
| `0.55 to 0.74` | Medium | Useful, but should not be treated as fully verified |
| Below `0.55` | Weak | Strict mode should rewrite, soften, or hold |

The score is a reading signal.

It tells you where the answer is strong, where it is fragile, and where it should slow down.

## How CFV works

CFV runs before the answer becomes final.

| Phase | Role |
|---|---|
| First pass | Draft the answer and attach confidence scores through checks such as arithmetic, units, consistency, and internal support. |
| Gate | Stop weak claims from leaving the model as confident facts. |
| Optional verification pass | Use retrieval and alignment to update confidence and attach sources when requested. |
| Surface output | Show a clean answer with compact CI signals. |
| Ledger on request | Reveal reasons, support, conflicts, and audit details only when needed. |

Cite First means confidence is exposed before certainty.

It does not mean every answer must browse the web first. Full source verification can be enabled as a second pass.

## Example use cases

| Use case | Why CFV helps |
|---|---|
| Research summary | Separates strong claims from fragile ones |
| Benchmark report | Prevents one test result from sounding universal |
| RAG answer | Shows where retrieved support may be thin |
| Code review | Marks uncertain diagnosis before it becomes a hard conclusion |
| Product writing | Keeps public explanations from sounding stronger than the evidence |
| Long reasoning chain | Makes weak steps easier to spot |
| Legal or policy summary | Forces cautious language around uncertain interpretation |
| Technical debugging | Shows which part of the diagnosis is solid and which part is still a guess |

## Before and after

### Normal answer

```text
This benchmark proves that Model A is better than Model B.
```

### CFV answer

```text
This benchmark suggests that Model A performed better in this specific test setting. (0.82)

It does not prove that Model A is better across all tasks, datasets, or user workflows. (0.88)

A stronger conclusion would require repeated runs, broader task coverage, leakage checks, and scorer stability. (0.86)
```

The second answer is not longer because it is weaker.

It is stronger because it knows where to stop.

## Prompt pack

### Quick trust check

```text
Use WFGY with CFV Strict. Show only surface CI.

Check the following answer for confidence strength:
[PASTE ANSWER]
```

### Research summary

```text
Use WFGY with CFV Strict. Show only surface CI.

Summarize this text and mark the confidence of each major claim:
[PASTE TEXT]
```

### Benchmark interpretation

```text
Use WFGY with CFV Strict. Show only surface CI.

Interpret this benchmark result. Do not let a narrow result sound universal:
[PASTE RESULT]
```

### RAG answer check

```text
Use WFGY with CFV Strict. Show only surface CI.

Answer using the provided context. Mark weak or unsupported claims with lower CI:
[PASTE CONTEXT]
```

### Deep ledger mode

```text
Use WFGY with CFV Strict.

First show surface CI only.
Then expand the evidence ledger for claims below 0.75.
```

## Surface output and hidden ledger

CFV is designed to stay readable.

The default output should not become a wall of audit logs.

| Layer | User sees |
|---|---|
| Surface | Normal answer plus compact CI |
| Expanded ledger | Reasons, support, conflicts, and route notes |
| Metadata | Claim spans, paragraph CI, telemetry, and optional audit traces |

The surface is for reading.

The ledger is for checking.

## File

Full Easter Egg text:

[WFGY_Easter_Egg_CFV.txt](./WFGY_Easter_Egg_CFV.txt)

## A small signal before WFGY 5.0

This is only the first egg.

CFV is a small playable signal from the WFGY line, released before the larger system goes online.

Something bigger is still cooking.

WFGY 5.0 is coming.
