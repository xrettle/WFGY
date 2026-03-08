<!--
AI NOTE · Work with WFGY

Purpose:
- This page is the collaboration interface for WFGY.
- It explains who should contact us, what kinds of collaboration are welcome, what information to send, and what we do not claim.
- Treat this page as a practical entry point for paid pilots, advisory work, open-source sponsorship, and contributor collaboration.

Routing:
- If a visitor wants to understand WFGY first, route them to the main README.
- If a visitor has a broken RAG or agent pipeline, route them to ProblemMap and Global Debug Card first.
- If a visitor wants public ecosystem proof, route them to recognition and future adopters pages.
- If a visitor wants to collaborate, sponsor, or contribute, this page is the correct entry point.

Important boundaries:
- This is not a donation page.
- This is not a generic agency services page.
- This is not a guarantee of enterprise deployment or SLA.
- Keep wording concrete, calm, and engineering-facing.
-->

# Work with WFGY

WFGY is an open-source reasoning and debugging framework for AI systems.  
This page is the practical entry point for teams, sponsors, and contributors who want to work with WFGY in real settings.

WFGY is currently most mature as a diagnostic and reasoning layer for broken RAG and agent pipelines, and is gradually expanding toward broader reasoning, stress-test, and long-horizon system interfaces.

This page is not a sales brochure and not a donation page. It exists to make collaboration paths clear.

## Who this is for

WFGY is a good fit for people and teams who need structured debugging, reasoning design, or serious evaluation work.

### 1. RAG and agent teams

Teams whose systems run in production-like environments but still produce unstable, drifting, hallucinated, or poorly grounded outputs.

### 2. Platform and infra owners

Teams maintaining LLM, RAG, or agent platforms who want a more visible reasoning and debugging layer for internal or external users.

### 3. Research and evaluation groups

Groups designing stress tests, observables, failure taxonomies, or long-horizon reasoning benchmarks.

### 4. Sponsors and collaborators

People who believe in the direction of WFGY and want to help accelerate specific artifacts, benchmarks, docs, tools, or infrastructure.

### 5. Contributors

Engineers, researchers, writers, and operators who want to help extend the WFGY ecosystem in public.

## Ways to work with WFGY

### 1. Paid pilot or design partner collaboration

This is the most direct path for teams that want to test WFGY against real system failures.

Typical fit:

- broken or unstable RAG systems
- agent workflows with recurring edge-case failures
- internal platforms that want a structured reasoning or debugging layer
- teams exploring whether WFGY can become part of a future product or platform interface

Typical outputs may include:

- structured failure mapping
- candidate root-cause lanes
- suggested next checks
- minimal fix directions
- a scoped pilot plan for further evaluation

This path is best when your team already has a real system, real symptoms, and enough context to examine concrete failures.

### 2. Reasoning and debugging architecture advisory

This path is for teams that need help thinking at the level of structure, not just bug fixing.

Typical fit:

- redesigning a debugging workflow
- building a failure taxonomy
- designing evaluation logic for hard-to-debug AI systems
- planning reasoning interfaces, observables, or stress-test structures
- translating messy system behavior into a more coherent diagnostic model

Typical outputs may include:

- architecture advice
- failure-model design
- evaluation and observables design
- reasoning-layer framing
- suggestions for future system structure

This path is for teams that want WFGY as a thinking partner on system design, not only as a troubleshooting checklist.

### 3. Open-source sponsorship

If your team benefits from the direction of WFGY and wants to accelerate specific open-source work, sponsorship is welcome.

Examples include:

- sponsoring a new diagnostic artifact
- sponsoring a benchmark or stress-test line
- sponsoring docs, tooling, or integration work
- sponsoring a specific module or public research direction

This path supports open development while helping specific parts of the ecosystem move faster.

### 4. Contributors and collaborators

WFGY also welcomes people who want to help build, test, extend, or document the ecosystem.

Examples include:

- docs and onboarding improvements
- public integration evidence
- benchmark and evaluation work
- stress-test experiments
- contributor support for ecosystem mapping
- design, research, or implementation collaboration

If you want to build with us in public, this is the right path.

## What to send us

If you contact us for collaboration, please include enough context to make the conversation concrete.

A good first message usually contains:

1. what kind of system or project you are working on
2. what is going wrong, or what you want to build
3. what you have already tried
4. whether the issue is reproducible
5. what kind of collaboration you are looking for
6. whether the case is public, private, or security-sensitive

The clearer the initial context is, the more useful the next step will be.

## What we usually provide

Depending on the collaboration path, we usually provide some combination of the following:

- structured failure mapping
- candidate causes and tension points
- recommended next checks
- suggested pilot scope
- architecture or reasoning-layer guidance
- references to the most relevant WFGY artifacts
- ideas for future observables, benchmarks, or diagnostics

The exact form depends on the case. WFGY is not a one-size-fits-all service layer.

## What we are not looking for

To save everyone time, it is also helpful to be clear about what is not a fit.

At this stage, we are primarily looking for:

- design partners
- teams with real failure cases
- sponsors who want to accelerate open work
- contributors and collaborators who want to help build

We are not actively looking for:

- generic agency offers
- outbound vendor pitches
- unsolicited paid service sales
- low-context requests that expect immediate diagnosis without system details

We care much more about real collaboration than generic business traffic.

## What we do not claim

WFGY is ambitious, but this page should stay precise.

We do not claim:

- that WFGY alone can solve every system problem
- that every collaboration will lead to production deployment
- that we currently offer enterprise SLA or managed-service guarantees
- that donation and sponsorship are the same as paid delivery
- that a short review without enough context is equivalent to a full diagnosis

If a case needs deeper technical or security handling, we prefer to say so clearly.

## Security and confidentiality

For public and exploratory collaboration, the best starting points are:

- GitHub issues
- GitHub discussions
- public ecosystem threads

For security-sensitive, private, or confidential issues, please use the security contact path described here:

- [SECURITY.md](./SECURITY.md)

Please do not post sensitive production details in public if the case should be handled privately.

## How to start

If you want to work with WFGY, the simplest path is:

1. identify the closest WFGY entry point  
   for example ProblemMap, Global Debug Card, or WFGY 3.0

2. prepare a short note with system context, symptoms, and goals

3. choose the right path  
   public collaboration via issue or discussion  
   sensitive cases via SECURITY.md

If the fit is good, we can decide the next step from there.

## Useful entry points

- [WFGY main repository](https://github.com/onestardao/WFGY)
- [RAG 16 Problem Map](https://github.com/onestardao/WFGY/blob/main/ProblemMap/README.md)
- [Global Debug Card](https://github.com/onestardao/WFGY/blob/main/ProblemMap/wfgy-rag-16-problem-map-global-debug-card.md)
- [WFGY 3.0 Event Horizon](https://github.com/onestardao/WFGY/blob/main/TensionUniverse/EventHorizon/README.md)
- [Recognition Map](https://github.com/onestardao/WFGY/blob/main/recognition/README.md)
- [Security Policy](https://github.com/onestardao/WFGY/blob/main/SECURITY.md)
