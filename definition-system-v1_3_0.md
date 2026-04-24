---
id: definition-system
version: 1.3.0
scope: standalone
status: FINAL — Human Approved
---

# Definition — System

**Premise 1:** All ecological embeddings have geometric properties.

**Premise 2:** Flux denotes the rate of information transfer across a surface within G.

---

A **system** S is defined as a triplet **(N, R, G)** such that:

- **N** is a set of **nodes** — the networked things that constitute the system.
- **R** is a set of **relationships** among nodes — including self-relationships, where a node in N relates to itself via a reflexive relation in R.
- **G** is a set of **ecological embeddings** that defines the spatio-temporal adjacency of N and R within a hyper-dimensional space. G mediates R: the relationships in R are made persistent and meaningful by the ecological embedding G provides.

---

## Formal Constraints

1. N and R may each be empty. The empty system (N = Ø, R = Ø) is valid — it is informationally inert but not ill-formed.

1. A node n in N may hold a reflexive relationship (n, n) in R. In this case, n is simultaneously the sender and receiver of its own signal, ecologically coupled to itself via G. This is the minimal non-degenerate system: a single node with memory of itself.

1. Information transfer within S is possible if and only if R ≠ Ø and |N| ≥ 1. A system with nodes but no relationships is degenerate — no transfer channel exists.

1. Memory of S exists if and only if G is non-trivially structured — nodes in N have spatio-temporal adjacency within the ecological embedding G, and G mediates at least one relationship in R. A system with no ecological embedding, or with an unstructured one, has no memory even if N and R are non-empty.

1. The cost of forgetting within S depends on the ecology encoded in G — the individual, organizational, cultural, and environmental context in which S is embedded. Where relationships in R are non-linear and observer-constituted, forgetting may be irreversible. Where they are linear and observer-independent, forgetting is recoverable from residual components or external records.

---

## Boundary Cases

| N | R | G | Name | Status |
|---|---|---|---|---|
| Ø | Ø | — | Empty system | Valid. Informationally inert. |
| ≠ Ø | Ø | — | Degenerate system | Valid. No transfer possible. No memory. |
| {n} | {(n,n)} | Structured | Minimal system | Valid. Single node, reflexive relation, self-memory via G. |
| ≠ Ø | ≠ Ø | Unstructured | Transfer-capable, memoryless | Theoretically possible but ecologically intangible. |
| ≠ Ø | ≠ Ø | Structured | Fully realized system | Transfer and memory both available. |

---

## Corollary — Graph Representation

Any system S can be represented as a graph where nodes in N are vertices and relationships in R are edges, including self-loops. An equivalent representation is a dictionary where keys are nodes in N and values are the sets of nodes they relate to via R. G is the ecological embedding in which that graph is physically instantiated and temporally persistent — without G, the graph is an abstract structure with no memory.

---

*definition-system-v1_3_0.md — FINAL — Human Approved*
