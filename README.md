# 🧠 Personal AI Research Library & External Memory

A personal, user-curated research library for storing, analyzing, and referencing key papers in AI, frontier models, AI agents, and scientific research. Designed for fast navigation and mobile-friendly reading on GitHub.

---

## 🎯 Repository Purpose & Agent Boundaries

- **User as Curator**: Papers in this repository are intentionally selected and supplied by the user.
- **Agent as Assistant**: AI agents process and analyze **only** the papers explicitly provided by the user (generating structured notes, Vietnamese translations, and cross-paper synthesis).
- **Persistent Reading Interface**: GitHub serves as the persistent catalog and convenient mobile-friendly reading interface for long-term reference.

> 🚫 **What this repository is NOT**: This repository is not an autonomous research system, paper search engine, web crawler, or automated literature discovery pipeline. Agents do not independently search for, discover, or pull external papers.

---

## ⚡ Workflow Model

```
User selects paper ➔ PDF added to repository ➔ Agent analyzes supplied paper ➔ Analysis / translation generated ➔ Repository index updated ➔ User reads on PC or mobile
```

1. **User Selection**: User chooses a paper and adds `paper.pdf` to `papers/<paper-slug>/`.
2. **Agent Processing**: Agent analyzes the provided paper to generate `analysis.md` (and optional `translation-vi.md`).
3. **Synthesis & Indexing**: Agent updates reading paths in `topics/` (connecting papers *already* in the repository) and logs the entry in `README.md`.
4. **Reading & Reference**: User reads and reviews paper notes on PC or mobile.

---

## 📂 Repository Structure

- 📄 **[`papers/`](papers/)**: Individual papers curated by the user, containing the original PDF, detailed analysis notes, and optional Vietnamese translations.
- 🏷️ **[`topics/`](topics/)**: Thematic synthesis and reading paths connecting papers *already present* in this repository.
- 🛠️ **[`resources/`](resources/)**: Shared reference material, including domain glossaries and evaluation terms.

---

## 📚 Papers Catalog

| Paper | Topics | Status | Links |
| --- | --- | --- | --- |
| [Towards end-to-end automation of AI research](papers/towards-end-to-end-automation-of-ai-research/analysis.md) | `#R&D-Automation` `#The-AI-Scientist` `#Automated-Peer-Review` | ⭐ Must Read | 📝 [Analysis](papers/towards-end-to-end-automation-of-ai-research/analysis.md) \| 🇻🇳 [Translation](papers/towards-end-to-end-automation-of-ai-research/translation-vi.md) \| 📄 [PDF](papers/towards-end-to-end-automation-of-ai-research/paper.pdf) |
| [Can AI agents conduct open-ended AI research?](papers/can-ai-agents-conduct-open-ended-ai-research/analysis.md) | `#AI-Agents` `#R&D-Automation` `#Agentic-Evaluations` | ⭐ Must Read | 📝 [Analysis](papers/can-ai-agents-conduct-open-ended-ai-research/analysis.md) \| 🇻🇳 [Translation](papers/can-ai-agents-conduct-open-ended-ai-research/translation-vi.md) \| 📄 [PDF](papers/can-ai-agents-conduct-open-ended-ai-research/paper.pdf) |
| [From AI for Science to Agentic Science](papers/from-ai-for-science-to-agentic-science/analysis.md) | `#Agentic-Science` `#Autonomous-Discovery` `#Self-Driving-Labs` | ⭐ Must Read | 📝 [Analysis](papers/from-ai-for-science-to-agentic-science/analysis.md) \| 🇻🇳 [Translation](papers/from-ai-for-science-to-agentic-science/translation-vi.md) \| 📄 [PDF](papers/from-ai-for-science-to-agentic-science/paper.pdf) |

---

## 🏷️ Topics & Reading Paths

Syntheses and reading maps across papers currently in the repository:

- 🗺️ **[Autonomous AI Research Reading Path](topics/autonomous-ai-research.md)** — Master reading map answering: *"AI có thể tự thực hiện nghiên cứu khoa học đến mức nào?"*
- 🤖 **[AI Agents](topics/ai-agents.md)** — Agent scaffolds, harnesses, failure modes, generator-verifier gap.
- 🔬 **[AI Research & Automation](topics/ai-research-automation.md)** — Shadow evaluations, verifiable benchmarks, execution vs direction layers.
- 🧠 **[Frontier Models](topics/frontier-models.md)** — Reasoning capabilities, extra-high compute, scaling limits.

---

## 📖 Reading Roadmap

### 🗺️ Topic Reading Path: Autonomous AI Research
- **[Autonomous Scientific Research Reading Map](topics/autonomous-ai-research.md)** (01 ➔ 02 ➔ 03)
  1. 📄 **[Towards end-to-end automation of AI research](papers/towards-end-to-end-automation-of-ai-research/analysis.md)** — The AI Scientist pipeline & $15 paper generation.
  2. 📄 **[Can AI agents conduct open-ended AI research?](papers/can-ai-agents-conduct-open-ended-ai-research/analysis.md)** — Shadow evaluations & limits of open-ended AI research.
  3. 📄 **[From AI for Science to Agentic Science](papers/from-ai-for-science-to-agentic-science/analysis.md)** — Survey on autonomous discovery across Life Sciences, Chemistry, Materials & Physics.

### 🗃️ All Papers in Library
- [Towards end-to-end automation of AI research](papers/towards-end-to-end-automation-of-ai-research/analysis.md) (Nature 2026)
- [Can AI agents conduct open-ended AI research? Early evidence from two case studies](papers/can-ai-agents-conduct-open-ended-ai-research/analysis.md) (2026)
- [From AI for Science to Agentic Science: A Survey on Autonomous Scientific Discovery](papers/from-ai-for-science-to-agentic-science/analysis.md) (2025/2026)

---

## 🛠️ Resources & Shared References

- 📖 **[Glossary of AI Research Terms](resources/glossary-ai-research-terms.md)**  
  Tài liệu tra cứu thuật ngữ ML, AI Agents, Evaluation Concepts (Shadow Evaluations, Generator-Verifier Gap, Context Rot, Instruction Drift...).

---

## ⚡ Workflow for Adding New Papers

To add a new paper to your library:

1. Create a paper folder: `papers/<paper-slug>/`
2. Save the PDF inside: `papers/<paper-slug>/paper.pdf`
3. Prompt Agent:
   > *"Analyze this paper and prepare it for my AI research library."*
4. Agent generates `analysis.md` (and optional `translation-vi.md`) using standard library formatting and updates catalog links.
