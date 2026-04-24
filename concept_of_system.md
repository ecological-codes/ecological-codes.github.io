---
id: definition-system
version: 1.3.4
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
	- *Degrees of freedom* — coincide with dimensionality. Uncertainty in information transfer within a subdomain is a function of its degrees of freedom.
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

1. Information transfer within S is possible if and only if R ≠ Ø and |N| ≥ 1. A system with nodes but no relationships is degenerate — no transfer channel exists.

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

*definition-system-v1_3_4.md — FINAL — Human Approved*
