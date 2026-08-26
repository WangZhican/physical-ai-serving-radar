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

### 2026-08-26: Temporal programming models for multi-rate Physical AI
Retriever adds a reusable temporal computation-graph runtime branch spanning P2/P3/P5/P7/P9: stateful modules own persistent state, explicit clocks determine execution cadence, edge synchronization policies select asynchronous input histories, and durable logs enable deterministic trace replay/debugging across backends. This is a systems abstraction for composing slow VLM planning, VLA skills, memory/monitoring and high-rate control at different clocks, distinct from ad-hoc callback glue or model-only fast/slow architectures.

### 2026-08-26: Preemptible multimodal execution joins the lifecycle branch
Routes 3/6/11 now explicitly include step-wise/preemptible multimodal generation. vLLM-Omni RFC #5822 shows why monolithic diffusion execution is a serving problem: one request can occupy the engine for an entire generation, preventing fine-grained interleaving, timely cancellation and progressive output. This connects directly to async-video cancellation/status (#6403), aborted-output reclamation (#6413/#6439), and request-scoped mutable stage-state lifecycle (#6453). Per-step control alone is ecosystem/runtime evidence rather than a new paper promotion; the research opportunity is a reusable scheduler that jointly owns admission, step execution, cancellation, state/artifact lifetime and deterministic reclamation.

### 2026-08-26: Planner knowledge vs physical execution authority
Physical Agentic AI adds a fleet/runtime-governance branch spanning P1/P2/P7. A non-actuating foundation-model planner reasons over typed robot skills and workflow contracts, but a deterministic Robot Orchestrator owns actuation and re-checks capability membership, current state, state-bound values, preconditions and synchronization constraints at every dispatch. The systems distinction is important: better retrieval/grounding improves planning but does not replace runtime authorization. Future Physical-AI serving stacks should treat semantic planning and physical execution authority as separate control planes.

### P9 refinement: simulator reliability / fuzzing infrastructure
**PHYFU (ASE 2023 Distinguished Paper) → IcFuzz (ASE 2026)** is the simulator-reliability lineage. PHYFU establishes physics-law oracles plus feedback-guided fuzzing across general physics simulation engines used in robotics/learning-based control; IcFuzz specializes the line to Isaac Sim with semantic-stage guidance and multi-level mutation. Reusable simulator test generation, coverage/failure feedback, bug discovery and reproducible artifacts are treated as Physical-AI evaluation infrastructure because simulator correctness directly affects training/evaluation validity.

### 2026-08-26: ROS2 / robot-stack reliability completes the Route-9 fuzzing lineage
Route P9 now records **RoboFuzz (ESEC/FSE 2022) → PHYFU (ASE 2023) → IcFuzz (ASE 2026)** as a focused reliability line. RoboFuzz targets semantic correctness bugs in ROS2 and ROS-based robotic systems through hybrid real/sim execution and cyber-physical/specification/physical-law oracles; PHYFU generalizes consistency checking to physics simulation engines; IcFuzz specializes semantic-stage fuzzing to Isaac Sim. This branch is scoped to robotics/simulator/runtime reliability infrastructure rather than generic fuzzing papers.
