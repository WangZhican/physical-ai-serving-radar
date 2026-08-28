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

### 2026-08-27: Durable experiment evidence + execution-settled WAM trust state
Two boundary works refine Routes P5/P9/P10 without creating a new top-level route. **AgenticRobotics** treats robot-policy improvement rounds as durable, crash-recoverable experiment transactions with append-only evidence and artifact-bound capability quality, sharpening P9 around experiment provenance and promotion validity. **DreamLedger** treats consumed world-model predictions as persistent execution-settled credit state with dependency tickets and replayable audit logs, sharpening P5/P10 around trust/state that persists across rollout decisions. Both remain `SYS_ALG_BOUNDARY`: their systems abstractions are directly reusable, but neither is yet a general online multi-request serving/resource scheduler.

### 2026-08-27: Physical autoresearch / fleet experiment orchestration
Routes P1/P2/P9 now track reusable physical experiment orchestration when a framework provides automatic reset/verification, auditable rollout artifacts, multi-robot parallel execution and explicit utilization metrics. **ENPIRE** is the current boundary anchor: MRU/MTU make robot-fleet and agent-token utilization measurable, but its primary objective remains policy self-improvement rather than online inference scheduling/resource management.

### 2026-08-27 — Agent-guided multimodal deployment/runtime synthesis
Routes 2/3/6/7/10/11 now explicitly include systems that own an application IR, placement/parallelism plan, streaming execution, state/dependency handling, validation against reference behavior, and heterogeneous backend deployment. **FlashRT (2607.18171)** is the current anchor. Same-name collision guard: it is not Execution-State Capsules / FlashRT (2606.20537).
### Runtime recomposition & city-scale digital-twin orchestration — 2026-08-27
- **Lingjing (Routes 1/2/9):** synchronized multi-engine urban runtime, shared state and attribution-ready multi-agent replay/evaluation.
- **Deployment Is Not Destiny (Routes 1/2/4/6/7):** post-deployment recomposition of software, hardware and compute payloads, with distributed capability/compute sharing.



### Always-on streaming multimodal runtime / persistent-state serving (added 2026-08-28 10:02 CST)
Routes 3/5/8/9/11 now explicitly track systems that decouple latency-critical live interaction from asynchronous persistent-memory construction, historical recall and tool/search work. **StreamArena / StreamMind (2608.05703)** is the anchor. Promotion requires explicit runtime scheduling/state reuse or serving/evaluation infrastructure, not merely a streaming-model architecture.

### 2026-08-28 refinement: latent freshness as a Physical-AI edge resource signal
Routes P4/P5/P8 now explicitly track task-relevant latent freshness (AoL/AoI-like signals) when it drives sensor admission, temporal integration windows, encoder selection, wireless scheduling/power, and uncertainty-aware edge decisions. Algorithmic optimization alone stays `SYS_ALG_BOUNDARY`; `CORE_SYS` requires a reusable runtime/scheduler/deployment substrate.


### 2026-08-28 23:58 CST — OS-style embodied process/resource runtime
Routes P2/P3/P7 now explicitly include embodied-agent OS runtimes. **TypeGo** is the anchor: task processes/PCBs carry scheduling state, a Skill Kernel owns typed physical-resource arbitration, and preemption/resumption plus asynchronous reflex/action/decomposition/scheduling loops are first-class runtime semantics. This is a runtime/resource-management branch, not merely fast/slow planning.

### 2026-08-29 refinement: Physical-I/O-aware segmented serving lineage
Routes P1/P3/P8 now explicitly connect fleet serving to the timing slack created by physical execution. **TimelyLLM** is the serving/scheduling anchor: generation is segmented around robot execution and scheduled by segment timing needs rather than ordinary FCFS. **TypeFly** is the boundary predecessor showing stream-interpreted control programs can begin execution before full plan generation. Together with TypeGo, this forms a lineage from token/stream-aware robot runtime → Physical-I/O-aware multi-agent serving → OS-style embodied process/resource management.
