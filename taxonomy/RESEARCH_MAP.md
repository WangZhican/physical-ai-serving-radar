# Research Map Index

This repository contains **two independent SYS-first research maps** backed by one verified metadata dataset.

## Track A — Physical AI Serving

Covers VLA/WAM runtimes, fleet-scale serving, control-loop scheduling, edge/cloud robotics, physical-state cache/state, heterogeneous robot deployment, evaluation infrastructure and world-model rollout serving.

- Overview: [`../physical_ai/README.md`](../physical_ai/README.md)
- Full taxonomy: [`PHYSICAL_AI_MAP.md`](PHYSICAL_AI_MAP.md)
- Core reading: [`../physical_ai/CORE_READING.md`](../physical_ai/CORE_READING.md)

## Track B — Multimodal / Omni Efficient Serving

Covers MLLM/Omni stage disaggregation, module multiplexing, any-to-any graph serving, distributed KV/state, interactive streaming, heterogeneous placement, preprocessing/video/AIGC pipelines and SLO-aware deployment planning.

- Overview: [`../multimodal/README.md`](../multimodal/README.md)
- Full taxonomy: [`MULTIMODAL_MAP.md`](MULTIMODAL_MAP.md)
- Core reading: [`../multimodal/CORE_READING.md`](../multimodal/CORE_READING.md)

## Cross-over

The two tracks intentionally overlap at systems such as vLLM-Omni, M*, Omni-Flow, Cornserve/Cornfigurator, Eevee/SpaceServe and heterogeneous placement systems. Those papers remain in their native track while their transfer to Physical AI is described separately:

- [`CROSSOVER.md`](CROSSOVER.md)

## Shared source of truth

Both tracks read from the same verified dataset:

- [`../data/papers.json`](../data/papers.json)

This prevents duplicate metadata and divergent paper identities while keeping the research narratives separate.


### 2026-08-23: Embodied-agent harness/runtime branch
Thea adds a reusable harness layer above robot capabilities: provider-neutral agentic loop + Tool Protocol + persistent Scene Graph state + post-execution Evaluation-as-Exit-Codes + memory/skills/safety + embodiment profile. This branch connects P2 runtime, P5 persistent physical state, and P7 composite planner/policy/safety orchestration. It is distinct from ordinary tool-use prompting because the contribution is a reusable physical execution/runtime substrate.

### 2026-08-26: Request/session lifecycle becomes a first-class Omni-serving branch
The Multimodal/Omni track now treats request-scoped mutable stage state, scheduler-owned request lifecycle, persistent session/world-model memory, transactional full-duplex session cleanup, and deterministic cancellation/failure reclamation as one systems lineage instead of unrelated model-specific fixes. vLLM-Omni RFC #6453, the diffusion scheduler state model, and SessionMemoryManager (#4480) are current ecosystem anchors. Shared-stage deduplication (#4108) cross-links this branch with resource sharing: a shared encoder/VAE only saves memory if request identity, mutable-state isolation, admission, cleanup and failure propagation remain correct when multiple orchestrators use the same stage.
