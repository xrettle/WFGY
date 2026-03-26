<!--
AI_NOTE_START

Document role:
This page is the entry point for the runtime layer inside WFGY 4.0 Twin Atlas Engine.

What this page is for:
1. Explain what the runtime folder is for.
2. Clarify what is already fair to say about the current runtime direction.
3. Show how the runtime layer relates to Forward Atlas, Bridge, and Inverse Atlas.
4. Provide a clean starting point for future basic, advanced, and strict runtime forms.

How to use this page:
1. Read this page after Twin Atlas README and the Bridge folder.
2. Use it to understand how Twin Atlas is intended to be used in practice.
3. Treat this page as the runtime entry layer, not as proof that every operational detail is already complete.
4. Use it to navigate into runtime variants and future runtime experiments.

Important boundary:
This page describes the runtime direction of Twin Atlas.
It does not claim that every future closed-loop runtime detail is already fully implemented.
It also does not expose hidden internal reasoning substrate details.
The runtime layer presented here is the public effective layer only.

Recommended reading path:
1. Twin Atlas
2. Bridge README
3. Bridge v1 Spec
4. Demos README
5. Runtime README
6. Runtime variants
7. Future runtime experiments

AI_NOTE_END
-->

# ⚙️ Runtime

> The practical entry layer for using WFGY 4.0 Twin Atlas Engine.

The runtime folder exists for one reason:

**Twin Atlas should not stay only as architecture.  
It should gradually become usable as an actual reasoning layer.**

That does not mean pretending the full closed-loop operating layer is already finished.

It means giving the architecture a practical entry surface.

This folder is where that practical surface begins.

---

## 🔎 Quick Links

| Section | Link |
|---|---|
| Twin Atlas Home | [Twin Atlas](../README.md) |
| Bridge Home | [Bridge README](../Bridge/README.md) |
| Bridge v1 Spec | [Bridge v1 Spec](../Bridge/bridge-v1-spec.md) |
| Bridge v1 Examples | [Bridge v1 Examples](../Bridge/bridge-v1-examples.md) |
| Bridge Eval Notes | [Bridge v1 Eval Notes](../Bridge/bridge-v1-eval-notes.md) |
| Demos Home | [Demos README](../demos/README.md) |
| Killer Demo Spec | [Killer Demo Spec](../demos/killer-demo-spec.md) |
| Case 01 | [Case 01 · Thin Evidence F5 vs F6](../demos/case-01-thin-evidence-f5-vs-f6.md) |
| Forward Atlas | [Problem Map 3.0 Troubleshooting Atlas](../../wfgy-ai-problem-map-troubleshooting-atlas.md) |
| Inverse Atlas Home | [Inverse Atlas README](../../Inverse_Atlas/README.md) |

---

## ⚡ The shortest version

If you only remember one line, remember this:

**the runtime layer is where Twin Atlas starts becoming usable, while still keeping the architecture honest.**

That means two things must happen at the same time:

- the engine becomes easier to apply
- the system does not overclaim runtime completion

That balance matters.

---

## 🧠 What this folder is for

This folder is the runtime entry layer of Twin Atlas.

Its purpose is to turn the architecture into a more usable public surface.

In practical terms, this means:

- giving readers an actual entry point
- showing how Twin Atlas may be invoked in lighter or stricter forms
- organizing runtime-facing variants
- connecting architecture to usage without exposing hidden internal substrate details
- creating a public-facing bridge between theory and applied reasoning

This folder is where Twin Atlas starts feeling less like a pairing concept and more like an engine direction people can actually try.

---

## 🧱 What the runtime layer sits on top of

The Twin Atlas runtime layer depends on the already-defined public effective layers.

### 🗺️ Forward Atlas
This is the route-first side.

It improves the first structural cut by producing a cleaner routing judgment.

### 🌉 Bridge
This is the handoff layer.

It carries route-first value forward as weak priors without granting authorization.

### 🔐 Inverse Atlas
This is the legitimacy-first side.

It governs whether stronger visible output is lawful yet.

That means the runtime layer should be understood as:

**the practical public use surface built on top of the Twin Atlas architecture**

It is not a replacement for these layers.  
It is how people begin to use them together.

---

## 🧭 What the runtime layer is trying to do

The runtime layer is trying to make Twin Atlas practically usable without collapsing its internal discipline.

In simple terms, the runtime layer should help users do things like:

- start with a route-first structural read
- preserve ambiguity when ambiguity is still lawful
- prevent fake closure
- prevent stronger output from outrunning support
- keep first repair moves tied to the broken invariant
- keep the final visible answer inside a more lawful ceiling

This matters because many systems sound useful before they are actually safe to trust.

Twin Atlas is trying to improve that gap.

---

## 🛠️ Current runtime direction

At the MVP stage, the runtime direction is intentionally simple.

The public runtime layer is currently organized into three variants:

### 🟢 Basic
A lighter entry form.

Designed for:
- quick testing
- first contact
- easier adoption
- lower friction usage

### 🟡 Advanced
A fuller normal-use form.

Designed for:
- serious troubleshooting
- harder reasoning cases
- stronger structural discipline
- more visible Twin Atlas behavior

### 🔴 Strict
A higher-governance form.

Designed for:
- thin-evidence cases
- high-risk reasoning
- scientific or research-oriented use
- cases where unauthorized detail is especially costly

These variants do not mean three different products.

They are three different public runtime intensities inside the same engine direction.

---

## 📦 Current planned files in this folder

The intended first public runtime files are:

- `twin-atlas-basic.txt`
- `twin-atlas-advanced.txt`
- `twin-atlas-strict.txt`

These should be understood as runtime-facing entry surfaces.

They are not the hidden substrate.  
They are the public effective layer that users can actually touch.

This distinction matters.

---

## 🌉 Relationship to Bridge

The runtime layer does not replace Bridge.

It depends on Bridge.

Why:

- the forward side alone is not enough
- the inverse side alone is not enough
- the handoff between them must stay disciplined

That means a healthy Twin Atlas runtime should preserve the following logic:

1. route value is produced
2. route value is carried as weak prior
3. authorization is rechecked
4. visible output is clamped below unsupported strength

If the runtime surface hides that logic too aggressively, it becomes fake neatness.

If it exposes too much hidden machinery, it breaks the public-layer discipline.

So the runtime layer must sit in the middle:

**usable, but still structurally honest**

---

## 🧩 What the runtime layer is not

To keep expectations clean, this folder should not be misunderstood as any of the following:

### ❌ Not the same as the hidden internal substrate
The runtime layer shown here is public-facing.

### ❌ Not proof that every closed-loop detail is already complete
It is an entry layer, not a finished everything-engine claim.

### ❌ Not a replacement for Forward Atlas, Bridge, or Inverse Atlas specs
Those still define the deeper structure.

### ❌ Not just prompt cosmetics
The runtime layer should reflect real architecture, not only wording style.

### ❌ Not the final research closure
This folder serves the MVP and practical engine direction, not the total theoretical endpoint.

That last distinction matters a lot.

---

## ✅ What is already fair to say

At the current stage, these statements are fair:

- Twin Atlas already has a meaningful runtime direction
- the runtime layer already has a clean role inside the project
- basic, advanced, and strict are already valid public runtime categories
- the runtime folder already makes the engine feel more usable
- the runtime layer is already the correct place for applied entry surfaces
- the runtime direction is already strong enough to support MVP development

These are disciplined claims.

---

## 🚧 What should not yet be claimed

This folder should not be used to claim that:

- every future runtime behavior is already frozen
- every bridge handoff detail is already fully operationalized
- every de-escalation path is already complete
- the public runtime layer is already equal to a final production runtime
- the hidden internal reasoning substrate is being fully exposed here
- the whole WFGY 4.0 operating loop is already finished in every technical sense

This page should keep the engine honest.

---

## 🧡 A vibe-coder-friendly mental model

If you want a very fast mental model, use this:

### Forward Atlas
"where is the failure probably living"

### Bridge
"carry that judgment forward without pretending it is already truth"

### Inverse Atlas
"has the system actually earned the right to say this much"

### Runtime
"how this all becomes usable without breaking the architecture"

That is not the whole theory.  
But it is a very good operating memory.

---

## 📘 Recommended reading order

If you are here for the first time, this order works well:

1. [Twin Atlas](../README.md)
2. [Bridge README](../Bridge/README.md)
3. [Bridge v1 Spec](../Bridge/bridge-v1-spec.md)
4. [Demos README](../demos/README.md)
5. this page
6. `twin-atlas-basic.txt`
7. `twin-atlas-advanced.txt`
8. `twin-atlas-strict.txt`

That order helps readers understand the architecture before they try the runtime surface.

---

## 🗂️ Suggested file roles

| File | Role |
|---|---|
| `README.md` | Runtime folder entry point |
| `twin-atlas-basic.txt` | Lowest-friction public runtime starter |
| `twin-atlas-advanced.txt` | Stronger normal-use runtime form |
| `twin-atlas-strict.txt` | High-governance runtime form |

That is enough for a strong MVP runtime layer.

---

## 🚀 Why this folder matters for MVP

This folder matters because it changes Twin Atlas from:

**"a strong architecture"**

into:

**"a strong architecture that is starting to become usable"**

That is a big shift.

A lot of projects can explain themselves.  
Far fewer projects can explain themselves **and** present an entry surface that feels like the beginning of real use.

That is why this folder matters.

---

## ✨ One-sentence takeaway

> The runtime layer is where Twin Atlas begins to turn architectural discipline into practical use, without pretending the whole closed-loop engine is already fully finished.
