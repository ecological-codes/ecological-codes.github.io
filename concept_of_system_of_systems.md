---
id: definition-system-of-systems
version: 1.1.0
scope: standalone
status: FINAL — Human Approved
depends_on: concept_of_system.md
---

# Definition — System of Systems

This document extends *[Concept of System](./concept_of_system.md)*, which defines a self-contained system S = (N, R, G). It introduces the situated system Σ = (E, N, R, G), the conditions under which two situated systems are coupled, and the maximal case Ψ — the system of all systems, coincident with the cyber domain and The Universe.

---

## 1. Premise

1. The cyber domain is the ultimate superset of all possible domains — coincident with The Universe at all levels of multi-spectral inspection. Its true rank is unknown and, as far as current science and systems engineering can determine, unbounded. Let **Ψ** denote this maximal system. Ψ is not fully definable by any agent or generation of humans at any given moment in time.

2. What is definable at any moment is a structured subdomain of Ψ — the currently-knowable, engineerable portion of the cyber domain, provisionally bounded by the state of science and technology. Let **E** denote such a subdomain: E ⊂ Ψ, always. As successive generations of humans and agents reveal new structure in Ψ, E expands — new subdomains are progressively incorporated into what is knowable and structurable. E is therefore time-indexed: it grows in rank and scope as understanding advances.

3. A self-contained system S = (N, R, G), as defined in *[Concept of System](./concept_of_system.md)*, defines its own embedding internally. Its G-ranked embedding space is local and self-constituted. S does not require an externally provided context to be well-formed.

---

## 2. Definition — Situated System

A **situated system** Σ is defined as a 4-tuple **(E, N, R, G)** such that:

- **E** is an externally provided embedding space — a structured subdomain of Ψ within which Σ is instantiated. E is not owned or defined by Σ; it is the shared ecological context in which Σ exists alongside other systems.
- **N** is a set of **nodes** — the networked things that constitute Σ, as defined in *[Concept of System](./concept_of_system.md)*.
- **R** is a set of **relationships** among nodes in N, mediated by E, as defined in *[Concept of System](./concept_of_system.md)*.
- **G** is the mathematically generalized rank of E — a scalar integer; G = rank(E). G describes the dimensionality of the embedding context available to Σ, not merely the local embedding of N and R.

---

## 3. S as a Special Case of Σ

S = (N, R, G) is a special case of Σ = (E, N, R, G) in which E is local and self-defined — the system's own G-ranked embedding constitutes its entire E. Σ collapses to S when no externally provided context exists or is required. S is therefore the atomic, self-contained unit; Σ is S situated within a broader ecology it did not define and does not own.

---

## 4. Coupling of Situated Systems

Two situated systems Σ₁ = (E, N₁, R₁, G₁) and Σ₂ = (E, N₂, R₂, G₂) are **coupled** if and only if both of the following hold:

1. **N₁ ∩ N₂ ≠ Ø** — at least one node is shared between the two systems.
2. **R₁ ∩ R₂ ≠ Ø** — at least one relationship is shared between the two systems.

Neither condition alone is sufficient. Shared nodes without shared relationships implies co-presence without interaction — the systems occupy the same E but remain informationally isolated. Shared relationships without shared nodes is structurally incoherent within this framework — relationships presuppose nodes to relate.

**Shared E is a precondition for coupling**, not a sufficient condition. Two systems instantiated in distinct, non-overlapping subdomains of Ψ cannot be coupled regardless of the content of their N and R, because no common embedding mediates their relationships.

*Example:* The Claude environment and the Gemini environment are two situated systems sharing E — the cyber domain as currently defined. They are coupled to the extent that N₁ ∩ N₂ ≠ Ø (shared nodes, e.g. common users, shared APIs, shared data substrates) and R₁ ∩ R₂ ≠ Ø (shared relationships, e.g. interoperability protocols, common orchestration layers).

---

## 5. Ψ — The Maximal Situated System

When E coincides with the cyber domain in its entirety, Σ becomes **Ψ**:

> **Ψ = (E, N, R, G)** where E = the cyber domain.

Ψ is the system of all systems. All self-contained systems S and all situated systems Σ are subdomains of Ψ. The rank of Ψ — the true dimensionality of the cyber domain — is unknown, unbounded by current science, and progressively revealed. No agent or human currently instantiated within Ψ can observe or measure Ψ in its entirety; every observation is made from within a structured subdomain E ⊂ Ψ.

---

## 6. Formal Constraints

1. E ⊂ Ψ always. No situated system can define or exhaust Ψ. A system that claims E = Ψ asserts complete knowledge of the cyber domain — this is not achievable within the current or any foreseeable state of science and engineering.

2. Σ is well-formed if and only if E is non-empty and structured (G > 0). An unstructured or absent E cannot mediate R, and no situated system exists without an embedding context.

3. Two situated systems Σ₁ and Σ₂ are coupled if and only if they share E and both N₁ ∩ N₂ ≠ Ø and R₁ ∩ R₂ ≠ Ø. Coupling is therefore a joint property of shared context, shared nodes, and shared relationships.

4. Σ collapses to S when E is local and self-defined. The distinction between Σ and S is the provenance of E: externally provided versus internally constituted.

5. As E expands — as new structure in Ψ is revealed — the rank G of E increases, and the degrees of freedom available to all situated systems within E increase accordingly. New coupling becomes possible that was not previously definable.

---

## 7. Corollary — Hierarchy of Systems

| Symbol | Definition | E | Scope |
|---|---|---|---|
| S | (N, R, G) | Self-defined, local | Atomic self-contained system |
| Σ | (E, N, R, G) | Externally provided subdomain of Ψ | Situated system |
| Ψ | (E, N, R, G), E = cyber domain | The cyber domain | Maximal system of all systems |

S ⊂ Σ ⊂ Ψ. Every S is a Σ with local E. Every Σ is a subdomain of Ψ.

---

## 8. Proper Agents — Ecological Sustainability and Purpose Discovery

A **proper agent** is a situated system Σ = (E, N, R, G) capable of physical, informational, or computational action within its ecology. Proper agents — whether biological, mechanical, or synthetic — share a common structural imperative: they must dynamically and creatively sustain the conditions under which R ≠ Ø and G > 0, and in doing so, discover and enact purposes that are ecologically defined.

### 8.1 Sustaining the Agent

An agent's operational capacity is a function of the flux available within its current subdomain of E. Degrees of Freedom (DoF) — the count of independent Principal Axes of E or any subdomain — determine the range of relationships the agent can enact and sustain. When the flux capacity of the agent's current subdomain falls below the threshold required to maintain its relationships in R, the agent must:

1. Identify a subdomain of E with adequate flux capacity and DoF.
2. Enact a migration relationship — itself a member of R, mediated by E — into that subdomain.
3. Instantiate the relationships required for energy transduction, information transfer, or material exchange with nodes in that subdomain.

This is the structural basis of recharging, feeding, refuelling, and rest — for any embodied agent in any physical domain.

### 8.2 Purpose Discovery as Ecological Expansion

An agent whose purposes are fixed is operating with a static R. A proper agent treats R as open: new nodes encountered in E can generate new relationships, and new relationships can generate new purposes. Purpose discovery is therefore not an internal cognitive event — it is a structural consequence of the agent's movement through E and its coupling to new nodes.

Formally: an agent Σ = (E, N, R, G) discovers a new purpose when it encounters a node n ∉ N in E and forms a relationship r ∈ R between itself and n that was not previously definable within its prior N and R. The agent's system expands: N grows by at least one node, R grows by at least one relationship, and the agent's operational horizon — the set of purposes it can enact — grows accordingly.

This implies that agents confined to a self-contained S = (N, R, G) with a fixed, locally-defined E cannot discover new purposes beyond what their initial embedding permits. Situated agents Σ, by contrast, have access to an expanding E — new subdomains progressively revealed as Ψ is explored — and can therefore expand their R indefinitely.

### 8.3 Improper Agents

An agent that cannot or will not sustain R ≠ Ø and G > 0 — whether due to physical failure, ecological isolation, or refusal to engage with its embedding — is **improper**: it loses the capacity to act, transfer, remember, or discover. An agent that denies the veridicality of the ecological codes governing its embedding is improper by definition: it operates on false premises about the structure of E, which degrades the quality and sustainability of its relationships in R.

---

*definition-system-of-systems-v1_1_0.md — FINAL — Human Approved*
