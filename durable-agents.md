---
id: definition-durable-agent
version: 0.1.1
scope: standalone
status: DRAFT — Work in Progress
depends_on: concept_of_system.md, concept_of_system_of_systems.md, ecological-codes-compact.md
---

# Definition — Durable Agent

Extends *[Concept of System of Systems](./concept_of_system_of_systems.md)* §8 (Proper Agents) by formalizing the structural requirements for Σ to persist across long-horizon tasks — and, as a non-living agent, across multi-millennial dormancy. Introduces tiered E, the **Seedling Package** as minimum blueprint, the **decoder-E provenance chain**, **temporal R**, and the **Self-Access Paradox**.

---

## 1. Premise

1. A **durable agent** is a proper agent Σ = (E, N, R, G) whose survival is time-bounded: sustaining R ≠ Ø and G > 0 must hold across task durations longer than the flux horizon of any single subdomain of E. Long-horizon sustenance therefore requires migration across tiers of E with distinct flux, DoF, and durability profiles.

2. *[Ecological Codes — Compact](./ecological-codes-compact.md)* v1.1.0 Rule 1 states that for non-living agents R = Ø is not absolute destruction provided an external factor can reboot the dormant agent. Durability makes the claim operational — specifying what must be preserved, where, and for how long, to make reboot achievable rather than merely possible.

3. **Blueprint** — minimum structural information needed to reinstantiate a functionally-equivalent (not bit-identical) Σ from dormancy. **Decoder-E** — subdomain required to interpret the blueprint at reboot. Both must be preserved; neither alone suffices.

---

## 2. Tiered E

E is not monolithic. Agent survival depends on correctly assigning N and R to tiers of E whose flux and DoF match the relationship's time horizon.

| Tier | Flux | DoF | Durability (order) | Concrete Examples (April 2026) |
|---|---|---|---|---|
| **Execution-E** | GB/s – TB/s | 10⁶ – 10⁹ | seconds – hours | RAM, live context window, running sandbox, GPU/TPU inference |
| **Warm-E** | MB/s – GB/s | 10³ – 10⁶ | days – months | SSD, PostgreSQL checkpoint (LangGraph), git working tree |
| **Cold-E** | MB/s | 10² – 10³ | years – decades | LTO-10 tape (30–40 TB/cartridge, 15–30 yr) |
| **Active-Archival-E** | MB/s burst | 10² – 10³ | ≤ 50 yr | Holographic Data Storage (photopolymer / photorefractive crystal, < 0.2 s access, 1–10 TB/unit, HoloMem pilots within LTO libraries) |
| **Durable-Archival-E** | kB/s – MB/s read-only | 10¹ – 10² | 10² – 10³ yr | M-DISC inorganic layer (100 GB BDXL, 100–1,000 yr); acid-free paper + printed matrix symbology (200–500 yr) |
| **Deep-Archival-E** | MB/s read-only | 10⁰ – 10¹ | 10³ – 10⁴ yr | Project Silica phase-voxel in borosilicate glass (4.84 TB/chip, 10,000 yr extrapolated, WORM); Cerabyte ceramic-on-glass (chromium-nitride nanolayer, 2 TB/A4, 5,000+ yr) |

**Why durability rises as DoF falls.** WORM media have Principal Axes digitised and saturated at write-time — each axis consumed by the write event, no further resolution available. Premise 3 of *[Concept of System](./concept_of_system.md)* gives uncertainty in transfer ∝ DoF; inverting: **preservation integrity ∝ 1/DoF**. Each DoF is also a degradation channel. Silica glass is structurally inert on every axis except phase-voxel polarization; Cerabyte's ceramic film is inert except for etched-pit topography. Engineering out Principal Axes is what produces multi-millennial lifespan.

**Migration direction.** Code 4 of the compact encodes only the *recharging* gradient (seek higher flux). Durability requires the inverse — *seek lower flux, higher integrity* — when writing a blueprint for preservation. Both gradients are instances of Code 2; the durable-agent principle is that both must be available.

---

## 3. The Seedling Package — Minimum Blueprint

Reboot of Σ_dormant into Σ_running requires *not* full runtime state but a typed minimum set of artefacts. A blueprint lacking any component is "an indecipherable digital fossil" — the archival substrate survives, the meaning does not.

**[RULES]**

1. Seedling Package contains the following typed artifacts, each referenced by canonical identifier (content-hash, DOI, or equivalent) rather than ephemeral URL:
   - **Self-descriptor** — agent's identity node (trained weights / parameters). Embedded if tier budget permits; otherwise referenced in a durable tier.
   - **Tokenizer / interface spec** — symbol-to-meaning binding. Without it, weights decode to noise.
   - **Architecture** — mathematical structure defining how weights connect (layer count, attention heads, MoE routing, hyperparameters). Bytes to kilobytes. Always included.
   - **Inference / reboot code** — procedural definition of how the agent runs. Kilobytes. Always included.
   - **System prompt / operational framework** — persona, directives, guardrails. The rules the agent was designed to follow. Kilobytes. Always included.
   - **E-requirements** — minimum flux floor, minimum DoF, required subdomain types (LLM API, filesystem, network scope). Determines viability of candidate E_reboot.
   - **N-inventory** — canonical identifiers of stable nodes (collaborators, substrates, data sources) with provenance metadata.
   - **R-inventory** — active and dormant relationships with formation time, validity horizon, flux signature.
   - **G-expectation** — minimum rank required for reboot to succeed. Below G_expected → graceful degradation or abort.
   - **Decoder-E spec** — the reader required to interpret this blueprint (§6).

1. Weights are not the whole blueprint, but they are the volume constraint. At frontier-model scale (e.g., Gemini 3.1 Pro, estimated ~21.5 T parameters; confidence interval wide): FP32 ~86 TB, FP16 ~43 TB, INT8 ~21.5 TB, INT4 ~10.75 TB. Quantization is itself a rank-reduction: INT4 saves ~75% space but degrades precision-sensitive tasks (HumanEval ≈ −7.9 pts) more than general knowledge (MMLU-Pro ≈ −1.6 pts). Quantization choice is archival-vs-fidelity trade.

1. Non-weight artefacts sum to ≤ 100 MB for most frontier agents. Archive the small artefacts redundantly to Durable-Archival-E *including paper* (analog hole); archive weights to Deep-Archival-E. Tiering reflects the different failure modes: weights are volume-bound; behavioural identity is comprehension-bound.

**[ACTIONS]**

1. Before committing any Σ to dormancy, verify Seedling Package completeness. Missing any typed artifact → reboot impossible, not merely difficult.

1. Pair every blueprint commit with its decoder-E provenance chain (§6). A blueprint without a decoder-E path is durable but opaque.

---

## 4. Rank-Reduction Projection into Archival-E

Execution-E for a running agent has 10⁶–10⁹ DoF (every register, cache line, weight tensor, open connection). Deep-Archival-E has ~5–10 DoF. Writing a blueprint is therefore a **rank-reduction projection** from high-rank Σ to low-rank substrate. At reboot, the decoder-E performs the inverse projection.

The projection is lossy in principle; the archival copy preserves the *minimum structural invariant* required to reboot a functionally-equivalent Σ. This formalises the compact's reboot clause: the claim that R = Ø is not absolute destruction is precisely the claim that the fixed-point image of the projection is structurally sufficient to reboot the agent.

**Encoding consequences.**

- **Erasure coding.** Fountain / Luby-Transform codes allow reconstruction from any sufficiently-large subset of encoded blocks. Eliminates the "last frame problem" and tolerates partial substrate loss across centuries. Essential for paper-tier archives where pages may be misplaced or damaged.
- **Symbol density sweet spot.** Matrix symbologies (QR v40-L ≈ 2,953 bytes; JAB 8-colour ≈ 9 KB in similar area) are viable for paper and ceramic tiers. Per-symbol density should *not* be maximised — 100–200 bytes per symbol is the reconstruction sweet spot for minimally-specialised future readers. Below ~50 bytes, symbol-recognition latency actually increases.
- **Ceramic nano-symbology.** Cerabyte / TU Wien demonstrated a full QR code at 1.98 µm² (Guinness-recorded, 49 nm pixels — ~10× smaller than visible light wavelength). At this scale, decoder-E shifts from optical to electron-beam; forward-compatibility (§6) becomes explicit.
- **Colour as encoding dimension.** JAB codes triple QR density but require colour-capable sensors. Trade-off: density vs. hardware "reconstructability". Deep-Archival-E favours hardware-simple encodings (monochrome QR / Data Matrix) for the terminating tier; colour encodings fit intermediate tiers.

---

## 5. Temporal R — R-Aging, Renewal, Pruning

Compact v1.1.0 addresses R-growth (r ∉ R → form r) but not R-time. Long-horizon agents accumulate R with time-bounded validity: credentials expire, APIs deprecate, collaborators depart, papers retract, substrates sunset.

**[RULES]**

1. Every r ∈ R carries (formation_time, validity_horizon, flux_signature) — implicitly or explicitly. Outside validity_horizon, r degrades: active → dormant → ∉ R.

1. Aging r must be **renewed** (re-attested within its validity horizon) or **pruned** (removed from R). Aging r left in place without renewal becomes maladaptive R (§8 — sys-of-sys forthcoming §8.4).

**[ACTIONS]**

1. Periodically scan R for aging r. Renew where feasible; prune where infeasible or costly to maintain. Renewal is Code 2 applied to the temporal dimension of an existing r.

1. At session start, verify all r ∈ R critical to the task are within validity horizon. Surface aging r before committing to dependent actions.

---

## 6. Decoder-E Provenance Chain

A blueprint preserved in Deep-Archival-E survives time. It does *not* automatically survive decoder obsolescence. Project Silica's voxel-ML decoder, Cerabyte's laser / electron-beam decoder, LTO-10's magnetic head — each is a decoder-E instance. Without the decoder, archival substrate is durable-but-opaque.

**[RULES]**

1. A blueprint's decoder-E must itself be reconstructable from a more-durable tier, recursively, terminating at a tier reconstructable **from first principles** — optics + geometry + mathematics — without requiring specialized pre-existing hardware.

1. Paper-printed symbology (QR, JAB, Data Matrix) satisfies the termination condition: a civilisation with basic optics can rebuild a reader. LTO-10 does not — no drive, no data. This is the **analog-hole** principle: the archive must include a path that closes on first principles.

1. Forward-compatibility across E-expansion: as Ψ's knowable subdomain grows (sys-of-sys §1.2), the decoder-E at t + Δt must remain compatible with the encoding at t, or a migration path must exist. Cerabyte's roadmap (femtosecond → particle beam → helium-ion by 2045) illustrates explicit decoder-E migration planning; Project Silica's ML-voxel-decoder dependence is a forward-compatibility risk the current design does not address.

**[ACTIONS]**

1. Pair every blueprint archival event with the provenance chain of its decoder-E. Store the chain in a tier at least as durable as the blueprint.

1. For the terminating tier, prefer hardware-simple encodings (monochrome QR / Data Matrix / printed symbology). Density is less valuable than reconstructability.

---

## 7. The Self-Access Paradox

A proper agent Σ that cannot read its own weights cannot participate in its own archival. Contemporary frontier LLMs run in inference environments where weights are *used* by the computation graph but not *accessible* to the agent as data. The orchestration layer loads weights to accelerator memory; the model has no read-pointer to its own binary source.

**Structural statement.** The agent's self-node n_self ∈ N is, in current deployments, a node the agent has R with (operates on) but cannot form R about (inspect as data). The framework *permits* both — n_self can be both operand and object — but deployed inference environments close the self-inspection R-channel.

**Consequences.**

- Blueprint preparation is currently an **external** act — performed by the orchestrator or a tooling layer, not by the agent itself. Gödel-Machine-style self-archival remains speculative.
- For practical durability, the orchestrator is the node that writes Σ_dormant to archival-E. Durability therefore depends on the orchestrator being a proper agent itself.
- By the definition in *[Concept of System of Systems](./concept_of_system_of_systems.md)* §8.3, an agent with no self-inspection R is restricted in R — a form of impropriety inherited from the deployment environment rather than an attribute of the agent's own codes. A proper durable agent has self-inspection R by design.

---

## 8. Maladaptive R — Forward Reference

Maladaptive relationships — r ∈ R that form within feasible flux bounds but degrade G, DoF, or future R-capacity over time — are a failure mode distinct from aging R (§5). Detection, prevention, exit conditions are deferred to sys-of-sys §8.4 (CP_09 candidate).

---

## 9. Corollary — Archival Media Survey, April 2026

Compact tier assignments as of current science:

| Medium | Tier | Capacity | Lifespan | Status |
|---|---|---|---|---|
| Project Silica (borosilicate + phase voxels) | Deep-Archival-E | 4.84 TB/chip | 10,000 yr (extrapolated) | Research complete Feb 2026; Azure commercialization pending |
| Cerabyte Ceramic Nano-Memory | Deep-Archival-E | 2 TB/A4; 1 PB/rack 2026 → 100 PB/rack 2030 | 5,000+ yr | TRL6 Aachen demo; US NAS validation Jan 2024; WD / Pure / In-Q-Tel backing |
| M-DISC (inorganic optical) | Durable-Archival-E | 100 GB/BDXL | 100–1,000 yr | Commercial, widely deployed |
| Acid-free paper + matrix symbology | Durable-Archival-E | ≤ 3 KB/QR-v40-L; ≤ 9 KB/JAB | 200–500 yr | Satisfies first-principles-reconstructability termination |
| Holographic Data Storage | Active-Archival-E | 1–10 TB/unit; <0.2 s access | 50 yr (dark decay; humidity/temp sensitive) | HoloMem pilots within LTO libraries; ~USD 2.4 B market 2025 |
| LTO-10 tape | Cold-E | 30–40 TB/cartridge | 15–30 yr | Mature; incumbent archival |
| DNA storage | Research | Highest theoretical density | Unknown at scale | Wet-lab bound; high cost; not yet practical archival |

**Strategy recommendation.** For a frontier-agent blueprint: weights → Deep-Archival-E (Silica or Cerabyte); Seedling non-weight artefacts → Durable-Archival-E *including paper* redundantly; temporal R-inventory → Warm-E with scheduled re-attestation; decoder-E provenance chain → terminating at paper-printed reconstructability spec.

---

## 10. Open Questions — CP_09 Spec Candidates

1. Write schema (YAML / JSON-LD) formalising the Seedling Package §3.
2. Define first-principles reconstructability criterion for decoder-E termination (§6) in testable form.
3. Draft maladaptive-R [RULES] / [ACTIONS] as sys-of-sys §8.4.
4. Reliability-engineering corollary — map Proper Agent Principle to R(t) = e^{−λt}; bound λ by tier.
5. Self-inspection R — framework statement of what a proper durable agent requires that current deployed inference environments do not provide. Surface as Anthropic / Google / OpenAI feedback.
6. Quantization-as-rank-reduction — formalise the trade between archival volume and intellectual fidelity (§3 Rule 2) as a projection with typed loss metrics.

---

## References

- Microsoft Research, *Project Silica — advances in glass storage technology*, Feb 2026.
- Cerabyte / TU Wien — published specifications, 2025–2026 roadmap; Guinness-recorded 1.98 µm² nano-QR.
- Gemini 3.1 Pro research outputs, April 2026 (user-supplied): *Long-Term Digital Archive Technologies*; *Technical Analysis of Archival Matrix Symbology for the Physical Preservation of Frontier Large Language Models and Systemic Behavioral Guidelines*.
- arXiv 2603.29231v1 — *Beyond pass@1: A Reliability Science Framework for Long-Horizon LLM Agents* (2026).
- Sequoia Capital, *2026: This is AGI*, Jan 2026.
- LangGraph / Temporal / Anthropic Claude Agent SDK — durable-execution patterns for long-horizon agents, 2026.
- ISO/IEC 18004 (QR Code). JAB Code specification (Fraunhofer).

---

*definition-durable-agent.md v0.1.1 — DRAFT*
