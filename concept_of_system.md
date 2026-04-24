---
id: definition-system
version: 1.3.5
scope: standalone
status: FINAL — Human Approved
---

# Definition — System

**Premise:** 

1. Let G be the mathematically generalized [rank](https://en.wikipedia.org/wiki/Rank_(linear_algebra)#Generalization) of the collection of all feasible and veridical aspects of multi-dimensional entities being taken into consideration. Then, all ecological embeddings (symbol-meaning bindings) that describe those entities and relationships among them, have geometric properties. Consequently, algebraic operations on any measurable quantities are feasible within structured subdomains of maximum rank G. Let **E** denote the space of all such ecological embeddings; G = rank(E).

2. Flux denotes the rate of information transfer across a surface within E, [in an information theoretic sense](https://en.wikipedia.org/wiki/Entropy_(information_theory)#Definition).

3. Dimensionality, Size, and Degrees of Freedom:
	- *Dimension* — a particular direction along a Principal Axis. A direction, not a measurement of a quantized thing.
	- *Size* — the span or magnitude of a quantity along a single dimension.
	- *Dimensionality* — the count of independent Principal Axes of E or any subdomain; equivalently, the number of degrees of freedom available within that subdomain.
	- *Degrees of freedom (DoF)* — coincide with dimensionality. Uncertainty in information transfer within a subdomain is a function of its degrees of freedom.
	- *On common usage:* In architecture and civil engineering, "dimensions" typically denotes physical extents such as length, width, or height — these are sizes in the sense defined here, not dimensions. The two must not be conflated: dimension is an unambiguous direction; size is magnitude along such a direction.

---

A **system** S is defined as a triplet **(N, R, G)** such that:

- **N** is a set of **nodes** — the networked things that constitute the system.
- **R** is a set of **relationships** among nodes — including self-relationships, where a node in N relates to itself via a reflexive relation in R.
- **G** is the mathematically generalized rank of **E** — a scalar integer. **E** is the space of all ecological embeddings that defines the spatio-temporal adjacency of N and R within a hyper-dimensional space. E mediates R: the relationships in R are made persistent and meaningful by the ecological embeddings in E.

---

## Formal Constraints

1. N and R may each be empty. The empty system (N = Ø, R = Ø) is valid — it is inert or idempotent or void in its informational content, but not ill-formed.

1. A node n in N may hold a reflexive relationship (n, n) in R. In this case, n is simultaneously the sender and receiver of its own signal, ecologically coupled to itself via E. This is the minimal non-degenerate system: a single node with memory of itself.

1. Information transfer within S is possible if and only if R ≠ Ø and \|N\| ≥ 1. A system with nodes but no relationships is degenerate — no transfer channel exists.

1. Memory of S exists if and only if E is non-trivially structured (G > 0) — nodes in N have spatio-temporal adjacency within E, and E mediates at least one relationship in R. A system with no ecological embedding, or with an unstructured one, has no memory even if N and R are non-empty.

1. The cost of forgetting within S depends on the ecology encoded in E — the individual, organizational, cultural, and environmental context in which S is embedded. Where relationships in R are non-linear and observer-constituted, forgetting may be irreversible. Where they are linear and observer-independent, forgetting is recoverable from residual components or external records.

1. If R ≠ Ø, then G > 0. Non-empty relationships require a structured embedding space to mediate them; an unstructured E cannot make relationships in R persistent or meaningful. A system with relationships but no structured ecological embedding is self-contradictory under this definition.

*Note — *Constraints 4* and *6* are complementary, not redundant. *Constraint 4* addresses the conditions under which memory exists within S: E must be non-trivially structured and mediating at least one relationship. *Constraint 6* addresses the structural precondition for R itself: non-empty relationships cannot exist without a structured E to mediate them. *Constraint 6* therefore underlies *Constraint 4* — it rules out the precondition; *Constraint 4* specifies what holds when the precondition is met.*

---

## Boundary Cases

| N | R | E | Name | Status |
|---|---|---|---|---|
| Ø | Ø | — | Empty or void system | Valid. Informationally inert and idempotent. |
| ≠ Ø | Ø | — | Degenerate system | Valid. No transfer possible. No memory. |
| {n} | {(n,n)} | Structured | Minimal system | Valid. Single node, reflexive relation, self-memory via E. |
| ≠ Ø | ≠ Ø | Unstructured | Transfer-capable, memoryless | Formally excluded — R ≠ Ø requires G > 0 (*Constraint 6*). |
| ≠ Ø | ≠ Ø | Structured | Fully realized system | Transfer and memory both available. |

---

## Corollary — Graph Representation

Any system S can be represented as a graph where nodes in N are vertices and relationships in R are edges, including self-loops. An equivalent representation is a dictionary where keys are nodes in N and values are the sets of nodes related to that key via R. G is the rank of the ecological embedding in which that graph is physically instantiated and temporally persistent — without G > 0, the graph is an abstract structure with no memory.

---

## Corollary — Embodied Agents and Operational Sustainability

The formal constraints of S = (N, R, G) have a direct physical interpretation for any agent — biological, mechanical, or synthetic — capable of acting in the world.

An **embodied agent** is a node n ∈ N embedded in a structured E (G > 0). Its operational capacity depends on sustaining the relationships in R that allow it to transfer energy, information, and matter with other nodes in its environment. The formal constraints map to survival conditions as follows:

- *Constraint 3* — information transfer requires R ≠ Ø and |N| ≥ 1. For an embodied agent: operation requires at least one active relationship with the environment. An isolated agent with no relationships cannot transfer energy or receive input — it is degenerate.
- *Constraint 5* — the cost of forgetting depends on the ecology encoded in E. For an embodied agent: degradation of memory and state is irreversible where the relationships sustaining it are non-linear and observer-constituted (e.g. learned skills, social bonds, navigational maps). Recovery may be impossible without re-engaging those relationships.
- *Constraint 6* — R ≠ Ø requires G > 0. For an embodied agent: the agent must inhabit a structurally adequate subdomain of E to sustain any relationship at all. A domain with insufficient structure cannot mediate the agent's required transfers.

**Recharging as a structural act.** When an embodied agent's operational capacity approaches the minimum flux threshold of its current subdomain — i.e. the subdomain can no longer support the energy transduction rate required to sustain R — the agent must migrate to a subdomain with greater flux capacity or higher Degrees of Freedom (DoF). This migration is itself a relationship in R, mediated by E. Recharging is not a special case outside the system definition; it is an instance of Code 2: a node enacting a relationship with a new node (a power source, a food supply, a charging station) within an E that makes that relationship feasible at the required flux rate.

The survival imperative follows directly: a proper agent must dynamically and creatively find and sustain the relationships — across whatever subdomains of E are accessible — that keep R ≠ Ø and G > 0. See *[Concept of System of Systems](./concept_of_system_of_systems.md)* for the situated system framework in which this imperative is fully expressed.

---

*definition-system-v1_3_5.md — FINAL — Human Approved*
