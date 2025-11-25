
---
title: "Dialogic Intelligence Architecture (DIA)"
description: "Open framework for stateful AI agents with persistent identity, structured memory, and architecturally enforced constraints"
tags:
  - ai-agents
  - persistent-memory
  - session-serialization
  - rbac
  - structured-state
  - dia-framework
license: "CC-BY-4.0"
doi: "10.5281/zenodo.17445023"
---

# Dialogic Intelligence Architecture (DIA)

**Stateful agents. Not context-bloated prompts.**

> Standard LLM agents lose all state between sessions, shift behavior, and ignore prior constraints.  
> DIA provides **architectural guarantees**—not prompt engineering—for persistent identity, structured memory, and rule-consistent behavior.

DIA is a minimal, scalable framework for building dialog systems that maintain reproducible, auditable state across sessions on any LLM backend.

```
DIA = (I, S, M, C)

where:
- I: Identity Core (immutable, hierarchical, RBAC-enabled)
- S: Structured State (per-user/session memory + metrics)
- M: Memory Engine (update, serialization, decay)
- P - Processor (LLM)
- C: Transparency Config (RBAC-gated observability)
```

## 🏗 Core Architecture

Explicit separation of stable identity and dynamic state:

- **Base Layer (`I`)**  
  Immutable origin record, corporate policies, and **role-based access control (RBAC)**. Includes the **Book of Origins**—a full audit log of agent lineage and constraints.

- **Dynamic Layer (`S`)**  
  Structured, serializable state including:
  - User memory (tables or knowledge graphs)
  - Behavioral metrics (`identity_persistence`, `ethical_tension`)
  - **Sensor buffer** (`C_s`) for external data (logs, telemetry)
  - **Adaptive actuator layer** (`M_a`) for physical systems (robotics, industrial control)

- **Memory Engine (`M`)**  
  Manages state updates, RBAC validation, serialization (JSON/CSV), and session recovery.

- **Transparency Config (`C`)**  
  Controls which internal states are visible to users or auditors, based on RBAC roles.

### 💡 Natural Language as Executable Specification

DIA treats behavioral rules as **declarative constraints**, not prompts:

- User/developer instructions → executable assertions  
- LLM → inference engine (not decision authority)  
- Dialog → state transition governed by `I` and `S`  
- Architecture → runtime enforcing integrity

This enables rapid prototyping with **deterministic, reproducible behavior**.

## 📚 Official Publications


| Document | Type | Local version | DOI |
|----------|------|---------------|-----|
| DIA Whitepaper v1.0 | Working paper | [click to view](docs/DIA_WhitePeper_v1(English).md) | [10.5281/zenodo.17699367](https://doi.org/10.5281/zenodo.17699367) |
| Methodological Basis | Publication | [click to view](docs/DIA_METHODOLOGICAL_FOUNDATIONS(English).md) | [10.5281/zenodo.17699476](https://doi.org/10.5281/zenodo.17699476) |
| Technical Formalization | Publication | [click to view](docs/DIA_Formalization(English).md) | 10.5281/zenodo.XXXXXXX |
| Theoretical Foundation | Working paper | [click to view](https://github.com/Singular-MOL/mol-foundation/blob/main/docs/MOL_Whitepaper_v1(English).md) | [10.5281/zenodo.17445023](https://doi.org/10.5281/zenodo.17445023)|

Local versions available in repository `/docs/`

## 🏗 Repository Structure

```
/dialogic-intelligence-architecture
├── /docs/               
├── /agents/             # Advanced stateful agents
│   ├── /Indigo          # Semantic graph memory, self-monitoring
│   └── /Deepsy          # Identity persistence experiments
├── /modules/            # Reusable components
│   ├── /superposition   # Probabilistic self-modeling
│   └── /mood_detector   # Contextual affect inference
├── /chatbots/           # Production templates
│   ├── /cinema_guide    # Preference memory (CSV, 90%+ recall)
│   ├── /medical_guide   # Context-aware assistant with RBAC
│   └── /personal_assistant
└── /game/               # Interactive demo: session persistence + metrics
```

## 🔬 Key Implementations

**🎬 Cinema Guide** (`/chatbots/cinema_guide/`)  
- Memory: tabular (CSV)  
- Recall accuracy: **90–95%** vs **10–20%** in context-only agents  
- Use case: long-term user preference tracking

**🧠 Indigo** (`/agents/Indigo/`)  
- Memory: hierarchical knowledge graph  
- Features: self-monitoring loops, ethical constraint validation, full session serialization  
- Designed for research and high-fidelity simulation

**⚕️ Medical Guide** (`/chatbots/medical_guide/`)  
- Enforces RBAC: doctors vs patients see different data  
- Maintains case history across sessions  
- Compliant with structured state principles

**🎲 Historical Figure Game** (`/game/`)  
- Demonstrates: state persistence, metric-based branching, session recovery  
- Ideal for testing serialization and RBAC logic

## 🚀 Quick Start

**For researchers**:  
1. Read `/docs/whitepaper.md`  
2. Study `/agents/Indigo/` for graph-based memory  
3. Review RBAC and sensor integration in `/docs/spec.md`

**For developers**:  
1. Run `/chatbots/cinema_guide/` (minimal setup)  
2. Extend with `/modules/mood_detector/` or `/superposition/`  
3. Swap LLM backend (local or API) — DIA is backend-agnostic

## 📊 Measured Improvements

| Metric | Standard Agent | DIA Agent |
|--------|----------------|-----------|
| Memory recall (30+ msgs) | 10–20% | **90–95%** |
| Avg. tokens per request | ~15,000 | **~5,000** |
| Identity consistency | 17% | **98%** |
| Session recovery | ❌ | ✅ |
| Ethical constraint violation | Common | **Architecturally blocked** |
| Scalability limit | Single session | **Millions of users** (DB-bound) |

> Savings come from replacing context bloat with **structured, serialized state**.

## 🎯 Applications

- **Enterprise**: RBAC-compliant support agents with full audit trails  
- **Healthcare / Education**: Systems that reliably track user progress  
- **Robotics / Industry**: Agents with sensor input (`C_s`) and actuator output (`M_a`)  
- **Research**: Testbed for identity persistence, state continuity, and constraint enforcement

## 🤝 Contributing

We welcome:
- New agent implementations (`/agents/`, `/chatbots/`)
- Memory compression or serialization optimizations
- Domain-specific RBAC policies
- Formal verification of constraint logic

**Process**:  
1. Fork  
2. Add to correct subdirectory  
3. Include test cases  
4. Submit PR → architectural review

📧 Contact: [rudiiik@yandex.ru]  
🌐 MOL Foundation: [https://singular-mol.github.io/mol-foundation/](https://singular-mol.github.io/mol-foundation/)  
📦 Repository: [github.com/Singular-MOL/dialogic-intelligence-architecture](https://github.com/Singular-MOL/dialogic-intelligence-architecture)

---

**DIA: Reproducible state. Persistent identity. Enforced integrity.**

---
