## 🌐 WFGY Recognition Map · RAG & Agent Ecosystem

A verified record of public citations and integrations of WFGY ProblemMap across the RAG and agent ecosystem.
> Last updated: 2026-03-01 · Manually maintained.

<details>
<summary>ℹ️ About this recognition list</summary>

>
> This page is the central record of third-party integrations, citations, mentions, and curated-list inclusions related to WFGY.  
>  
> At the current stage, most external recognition is tied to the **WFGY ProblemMap line**, especially the **RAG 16 Problem Map / 16-problem failure checklist**. That is the part most commonly adopted, cited, or adapted by other repositories, docs, and discussions.  
>  
> This does not mean that every external project on this page is using the full WFGY product series, or every WFGY module equally. In most cases, the recognized entry point is the **ProblemMap-style diagnostic framework** for RAG, LLM robustness, and reliability workflows.  
>  
> A smaller portion of entries also references **WFGY 3.0 / Singularity Demo** and related stress-test material. Since this is still a transition period, they are kept together in one list for simplicity.  
>  
> This page exists to keep recognition in one place, reduce duplication across other docs, and make future updates easier to maintain.  
>  
> If your repository, article, benchmark, documentation page, or discussion has included WFGY, you are welcome to:  
> - open a PR  
> - open an issue  
> - fork and reference this list  
> - suggest missing entries or proof links  
>  
> Contributions are welcome. If you have cited, integrated, adapted, or discussed WFGY in a public resource, feel free to add it here.  
>  
> ### 📌 Scope note  
> For accuracy and transparency:  
> - The majority of entries below are about the **WFGY ProblemMap / RAG 16 Problem Map** line  
> - Some entries mention broader **WFGY 3.0** materials  
> - This list should be read as a **recognition log**, not as a claim that all listed projects adopted the full WFGY ecosystem  

</details>

### 1. Core integrations & research

| Project | Stars | Segment | How it uses WFGY ProblemMap | Proof (PR / doc) |
| --- | --- | --- | --- | --- |
| [RAGFlow](https://github.com/infiniflow/ragflow) | [![GitHub Repo stars](https://img.shields.io/github/stars/infiniflow/ragflow?style=social)](https://github.com/infiniflow/ragflow) | Mainstream RAG engine | Adds a RAG failure modes checklist guide in its official docs, adapted from the WFGY 16-problem failure map for step-by-step RAG pipeline diagnostics. | [PR #13204](https://github.com/infiniflow/ragflow/pull/13204) |
| [LlamaIndex](https://github.com/run-llama/llama_index) | [![GitHub Repo stars](https://img.shields.io/github/stars/run-llama/llama_index?style=social)](https://github.com/run-llama/llama_index) | Mainstream RAG infra | Integrates the WFGY 16-problem RAG failure checklist into its official RAG troubleshooting docs as a structured failure mode reference. | [PR #20760](https://github.com/run-llama/llama_index/pull/20760) |
| [ToolUniverse (Harvard MIMS Lab)](https://github.com/mims-harvard/ToolUniverse) | [![GitHub Repo stars](https://img.shields.io/github/stars/mims-harvard/ToolUniverse?style=social)](https://github.com/mims-harvard/ToolUniverse) | Academic lab / tools | Provides a `WFGY_triage_llm_rag_failure` tool that wraps the 16 mode map for incident triage. | [PR #75](https://github.com/mims-harvard/ToolUniverse/pull/75) |
| [Rankify (Univ. of Innsbruck)](https://github.com/DataScienceUIBK/Rankify) | [![GitHub Repo stars](https://img.shields.io/github/stars/DataScienceUIBK/Rankify?style=social)](https://github.com/DataScienceUIBK/Rankify) | Academic lab / system | Uses the 16 failure patterns in RAG and re-ranking troubleshooting docs. | [PR #76](https://github.com/DataScienceUIBK/Rankify/pull/76) |
| [Multimodal RAG Survey (QCRI LLM Lab)](https://github.com/llm-lab-org/Multimodal-RAG-Survey) | [![GitHub Repo stars](https://img.shields.io/github/stars/llm-lab-org/Multimodal-RAG-Survey?style=social)](https://github.com/llm-lab-org/Multimodal-RAG-Survey) | Academic lab / survey | Cites WFGY as a practical diagnostic resource for multimodal RAG. | [PR #4](https://github.com/llm-lab-org/Multimodal-RAG-Survey/pull/4) |

### 2. Curated lists, benchmarks & discussions

| Project | Stars | How it uses WFGY ProblemMap |
| --- | --- | --- |
| [Awesome LLM Apps](https://github.com/Shubhamsaboo/awesome-llm-apps) | [![GitHub Repo stars](https://img.shields.io/github/stars/Shubhamsaboo/awesome-llm-apps?style=social)](https://github.com/Shubhamsaboo/awesome-llm-apps) | Includes the **RAG Failure Diagnostics Clinic** tutorial, designed by the WFGY author as a small, framework-agnostic clinic built around the WFGY 16-problem failure map for hands-on RAG debugging. |
| [Awesome Data Science – academic](https://github.com/academic/awesome-datascience) | [![GitHub Repo stars](https://img.shields.io/github/stars/academic/awesome-datascience?style=social)](https://github.com/academic/awesome-datascience) | Lists WFGY as a reference for LLM and RAG diagnostic workflows in data science infrastructure. |
| [Awesome-AITools](https://github.com/ikaijua/Awesome-AITools) | [![GitHub Repo stars](https://img.shields.io/github/stars/ikaijua/Awesome-AITools?style=social)](https://github.com/ikaijua/Awesome-AITools) | Lists WFGY ProblemMap as an open-source RAG failure-mode checklist and diagnostics toolkit for LLM pipelines (data, embeddings, retrievers, tools, evaluation). |
| [Awesome AI in Finance](https://github.com/georgezouq/awesome-ai-in-finance) | [![GitHub Repo stars](https://img.shields.io/github/stars/georgezouq/awesome-ai-in-finance?style=social)](https://github.com/georgezouq/awesome-ai-in-finance) | Lists WFGY as a tool for stress testing and validating RAG-based financial systems. |
| [Awesome GPT Super Prompting](https://github.com/CyberAlbSecOP/Awesome_GPT_Super_Prompting) | [![GitHub Repo stars](https://img.shields.io/github/stars/CyberAlbSecOP/Awesome_GPT_Super_Prompting?style=social)](https://github.com/CyberAlbSecOP/Awesome_GPT_Super_Prompting) | Includes **onestardao/WFGY** under Secure Prompting as a structured 16 failure-mode map for RAG and agent pipelines, including prompt injection patterns with practical mitigation checklists. |
| [awesome-agentic-patterns](https://github.com/nibzard/awesome-agentic-patterns) | [![GitHub Repo stars](https://img.shields.io/github/stars/nibzard/awesome-agentic-patterns?style=social)](https://github.com/nibzard/awesome-agentic-patterns) | Adds the **Reliability Problem Map Checklist for RAG and Agents** pattern in the Reliability and Eval category, based on the WFGY ProblemMap and linking back to WFGY as a reliability checklist for RAG-heavy agents. |
| [Awesome AI Books](https://github.com/zslucky/awesome-ai-books) | [![GitHub Repo stars](https://img.shields.io/github/stars/zslucky/awesome-ai-books?style=social)](https://github.com/zslucky/awesome-ai-books) | Mentions the WFGY TXT and PDF packs in the LLM reading list. |
| [Awesome AI Web Search (discussion 15)](https://github.com/felladrin/awesome-ai-web-search/discussions/15) | [![GitHub Repo stars](https://img.shields.io/github/stars/felladrin/awesome-ai-web-search?style=social)](https://github.com/felladrin/awesome-ai-web-search) | Discusses the 16 mode map as a candidate taxonomy for RAG failure modes in web search agents. |
| [Awesome AI System](https://github.com/lambda7xx/awesome-AI-system) | [![GitHub Repo stars](https://img.shields.io/github/stars/lambda7xx/awesome-AI-system?style=social)](https://github.com/lambda7xx/awesome-AI-system) | Lists WFGY under LLM robustness and debugging infrastructure. |
| [Awesome AI Tools](https://github.com/eudk/awesome-ai-tools) | [![GitHub Repo stars](https://img.shields.io/github/stars/eudk/awesome-ai-tools?style=social)](https://github.com/eudk/awesome-ai-tools) | Includes WFGY as an open-source framework for debugging LLM agents and RAG pipelines. |
| [LLM-Agent-Benchmark-List](https://github.com/zhangxjohn/LLM-Agent-Benchmark-List) | [![GitHub Repo stars](https://img.shields.io/github/stars/zhangxjohn/LLM-Agent-Benchmark-List?style=social)](https://github.com/zhangxjohn/LLM-Agent-Benchmark-List) | Lists **WFGY 3.0 · Singularity Demo (BlackHole-131)** as a long-horizon, text-only stress test for LLM agents, covering 131 S-class problems for tension-based reasoning and robustness evaluation. |
| [AI Agents for Cybersecurity](https://github.com/santosomar/AI-agents-for-cybersecurity) | [![GitHub Repo stars](https://img.shields.io/github/stars/santosomar/AI-agents-for-cybersecurity?style=social)](https://github.com/santosomar/AI-agents-for-cybersecurity) | References the 16 mode map as a debugging guide for RAG-heavy security agents. |
| [Awesome Artificial Intelligence Research](https://github.com/ThyrixYang/awesome-artificial-intelligence-research) | [![GitHub Repo stars](https://img.shields.io/github/stars/ThyrixYang/awesome-artificial-intelligence-research?style=social)](https://github.com/ThyrixYang/awesome-artificial-intelligence-research) | Links to WFGY in the NLP section as a project on LLM robustness, debugging, and reliability. |
| [Awesome-LLM-based-Evaluators](https://github.com/dependentsign/Awesome-LLM-based-Evaluators) | [![GitHub Repo stars](https://img.shields.io/github/stars/dependentsign/Awesome-LLM-based-Evaluators?style=social)](https://github.com/dependentsign/Awesome-LLM-based-Evaluators) | Lists **WFGY 3.0 · Singularity Demo** and the **WFGY ProblemMap** in its “Robustness and stress-test resources” section as a TXT-based long-horizon tension reasoning benchmark and failure map for RAG and LLM robustness evaluation. |

---

### ⭐ Star-powered Proof

The WFGY project has been starred by a diverse group of developers, maintainers, and ecosystem contributors.  
Stars are not the same as technical integrations or formal citations, but they show who cared enough to follow WFGY and keep an eye on its work.

This section highlights some early and notable “Star Gators” who starred the project in its first growth waves.

Explore the full list of notable supporters:

👉 [Star Gators · notable stargazers](./stargazers/README.md)

---

### 🤝 Contributing

If you find a public repository, benchmark, article, doc page, course page, or discussion that includes WFGY, you are welcome to help keep this list accurate.

You can contribute by:

- adding a missing entry  
- updating an outdated description  
- attaching a better proof link  
- correcting categorization  
- submitting a PR with a new citation or integration  

Forks and PRs are welcome. If your project includes WFGY in any public form, feel free to add it to this recognition list with a short description and a verifiable link.
