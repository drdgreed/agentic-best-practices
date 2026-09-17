<div align="center">

# Agentic Best Practices

**Two frameworks for specifying and governing agentic AI systems —
published as general best-practice guidance.**

![docs](https://img.shields.io/badge/documents-2-1f6feb?style=for-the-badge)
![words](https://img.shields.io/badge/~27,500%20words-3fb950?style=for-the-badge)
![status](https://img.shields.io/badge/brand--neutral-8957e5?style=for-the-badge)

*David Reed, PhD*

</div>

---

## What's here

| | Document | It answers |
|---|---|---|
| 🏛️ | **[CRISP-AG](CRISP-AG.md)** — Comprehensive Risk & Implementation Standard for Practical Agentic Governance | *"What is this agent allowed to do, and who approves it?"* |
| 📐 | **[Specification-Driven Design for Agentic Systems](SDD-Method.md)** — the method | *"How do I write a specification that actually constrains what gets built?"* |

They fit together. CRISP-AG classifies agents by consequence and assigns each action an
approval position. The SDD method is how you write the specification that holds an agent
to it.

---

## The idea both are built on

> A mechanism **enforces** when it can refuse — a schema validator, a permission rule, a
> deterministic check, a failing test, a blocking hook. It **guides** when it can only
> influence — prompt text, instruction files. *Never let a guiding mechanism be the only
> thing standing between a hazard and an outcome.*

Most of what follows in both documents is a consequence of taking that seriously.

---

## Where to start

```mermaid
flowchart TD
    A([What are you trying to do?]) --> Q{ }
    Q -->|"Decide whether an agent<br/>may take an action"| C["🏛️ <b>CRISP-AG</b><br/>§4 agent classes<br/>§5.1 approval positions"]
    Q -->|"Write a spec for<br/>something you'll build"| S["📐 <b>SDD Method</b><br/>A2 enforce vs guide<br/>A3 the four layers"]
    Q -->|"Work out what the<br/>regulation actually requires"| R["📐 <b>SDD Method</b> A6<br/>the regulatory frame<br/>as a specification input"]
    Q -->|"Set up evaluation<br/>that means something"| E["📐 <b>SDD Method</b> A7<br/>golden sets · calibration<br/>judges · drift"]
    Q -->|"Stand up governance<br/>across a portfolio"| L["🏛️ <b>CRISP-AG</b> §6<br/>nine-phase lifecycle<br/>and its gates"]

    style C fill:#1f2d3d,stroke:#58a6ff,color:#c9d1d9
    style L fill:#1f2d3d,stroke:#58a6ff,color:#c9d1d9
    style S fill:#2d1f3d,stroke:#bc8cff,color:#c9d1d9
    style R fill:#2d1f3d,stroke:#bc8cff,color:#c9d1d9
    style E fill:#2d1f3d,stroke:#bc8cff,color:#c9d1d9
```

**In a hurry?** Read the SDD method's **A2** (~640 words) and CRISP-AG's **§4** (~480
words). Between them they give you the two distinctions everything else hangs on: what
can refuse versus what can only suggest, and how much damage this agent could do.

---

## What these documents are, and are not

**They are** a method and a governance framework, written to be applied. Both carry
worked examples concrete enough to argue with, and both cite their sources.

**They are not** a compliance product or legal advice. Both describe regulatory
instruments as inputs that generate requirements; what any instrument requires of *your*
system is a question for your own counsel.

**On the evidence.** Both documents are explicit about the strength of what they cite.
The empirical record on specification-driven work is young — small studies, preprints,
practitioner reports — and the text says so where it matters rather than overclaiming.
Numeric thresholds are defensible defaults with citations, meant to be replaced by
measured ones.

---

## Editions

These are brand-neutral editions. They carry the method and the framework, with every
illustration set in a neutral worked example and every requirement stated inline rather
than cited by an identifier, so each document stands on its own.

Organisation-specific material — a fully worked system specification and a platform
playbook — is not included. That material describes an operating model rather than a
method, and would not have been made general by renaming.

---

## Citing

> Reed, D. (2026). *CRISP-AG: Comprehensive Risk & Implementation Standard for Practical
> Agentic Governance*, v3.0, public edition.

> Reed, D. (2026). *Specification-Driven Design for Agentic Systems: The Method*,
> v1.0.2, public edition.

---

<div align="center">

Questions, corrections and disagreements are welcome — open an issue.

</div>
