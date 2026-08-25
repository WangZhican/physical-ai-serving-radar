# Physical AI + Multimodal Serving Radar

> SYS-first research radar for two closely related but independently organized tracks: **Physical AI Serving** and **Multimodal / Omni Efficient Serving**.

**Last updated: 2026-08-25 18:01 CST**

This repository intentionally keeps the two research areas **in one place but written separately**. They share a single verified paper dataset, while each track has its own taxonomy, core reading list, and research narrative.

Pure pruning, quantization, token reduction, or action compression does **not** enter `CORE_SYS` unless it contributes a real runtime, scheduling, resource-management, cache/state, or deployment abstraction.

## Choose a track

| Track | What it studies | Research map | Core reading |
|---|---|---|---|
| 🤖 **Physical AI Serving** | VLA/WAM runtimes, fleet serving, control-loop scheduling, edge/cloud robotics, physical-state cache, heterogeneous robot deployment, evaluation/runtime infrastructure | [`physical_ai/README.md`](physical_ai/README.md) · [`taxonomy/PHYSICAL_AI_MAP.md`](taxonomy/PHYSICAL_AI_MAP.md) | [`physical_ai/CORE_READING.md`](physical_ai/CORE_READING.md) |
| 🌐 **Multimodal / Omni Efficient Serving** | MLLM/Omni stage disaggregation, module multiplexing, any-to-any graph serving, distributed state/KV, streaming interaction, heterogeneous placement, AIGC pipelines | [`multimodal/README.md`](multimodal/README.md) · [`taxonomy/MULTIMODAL_MAP.md`](taxonomy/MULTIMODAL_MAP.md) | [`multimodal/CORE_READING.md`](multimodal/CORE_READING.md) |

The overlap is deliberate, not a classification bug. Systems such as **vLLM-Omni, M\*, Omni-Flow, Cornserve, PhyAI, and ROSA** connect the two tracks. See [`taxonomy/CROSSOVER.md`](taxonomy/CROSSOVER.md).

---

# Track A — Physical AI Serving

Physical AI serving treats **physical execution, state freshness, deadlines, robots, and world-model rollouts as first-class system concerns** rather than ordinary request/response inference.

| Route | Focus | Representative anchors |
|---|---|---|
| P1. Fleet-scale / Multi-Robot Serving | GPU pools, batching, execution-aware scheduling, fleet learning loops | Kairos, ROSA, Armory, SOP |
| P2. Unified Physical-AI Runtime | portable VLA/WAM execution, robot-facing serving APIs, embodied-agent harnesses | PhyAI, Embodied.cpp, vla.cpp, LeRobot, Thea |
| P3. Real-Time / Streaming / Control Loop | reaction latency, deadlines, async execution, accelerator arbitration | CROS-RT, PAAM, VLASH, FASTER |
| P4. Edge-Cloud / Disaggregated Physical AI | device/edge/cloud placement, network/tail-latency reliability | RoboECC, RAPID, EcoVLA, FogROS2 |
| P5. Physical-State / Temporal Cache | cache validity over vision/action/world/planner/execution state | AgenticCache, Persistent Computational State, Execution-State Capsules |
| P6. Hardware-Aware / Heterogeneous Serving | GPU/XPU/NPU placement, CPU-GPU partitioning, offload | XPU Characterization, PAAM, OOM-Free Alpamayo |
| P7. Composite VLA + WAM + Planner Serving | policy + planner + world model + verifier/safety/tool graphs | M*, PhyAI, vLLM-Omni, Thea |
| P8. Workload Characterization / Modeling | control-time, network, cost-energy-time models | VLA-Perf, PhyAI |
| P9. Evaluation / Serving Infrastructure | model-server decoupling, real-robot EaaS, distributional metrics, observability | DeepInsight, RoboArena, RoboChallenge, PhAIL |
| P10. World-Model / WAM Rollout Serving | persistent rollout state, branch scheduling, migration, rollback/fork | WorldMove, PCS, PhyAI |

**Start here:** [`physical_ai/README.md`](physical_ai/README.md)

---

# Track B — Multimodal / Omni Efficient Serving

This track studies **system support for heterogeneous multimodal model pipelines**, independently of robotics. Its main objects are stages, modules, modality-specific resources, composite model graphs, distributed state, and SLO-aware scheduling.

| Route | Focus | Representative anchors |
|---|---|---|
| M1. Stage / EPD Disaggregation | encode-prefill-decode decomposition, overlap and independent scaling | TriInfer, EPD-Serve, HydraInfer, ModServe, RServe |
| M2. Module Multiplexing / GPU Sharing | complementary modules/stages sharing one GPU safely and efficiently | Eevee, SpaceServe, HorizonServe, UnifiedServe |
| M3. Any-to-Any / Graph Serving | arbitrary multimodal model graphs and component walks | vLLM-Omni, Cornserve, M*, Cornfigurator |
| M4. Distributed State / KV / Workflow | cross-stage KV/state movement, tiered storage, workflow orchestration | Omni-Flow, Cornserve, OnePiece |
| M5. Interactive / Streaming Omni Serving | playback, speech, barge-in, real-time generation and latency SLOs | LiveServe, StreamWise, TCM-Serve |
| M6. Heterogeneous / Elastic Placement | cross-tier GPUs, elastic parallelism, stage-aware placement | HeteroServe, ElasticMM, TriInfer, HELIOS |
| M7. Preprocessing / Video / AIGC Data Path | codec/decode, RDMA, video-generation pipelines, data movement | FlashCodec + UnifiedServe, OnePiece, HELIOS |
| M8. Deployment Planning / SLO / Production Infra | placement search, goodput, production-scale scheduling | Cornfigurator, HorizonServe, HELIOS |

**Start here:** [`multimodal/README.md`](multimodal/README.md)

---

## Shared data, separate views

- [`data/papers.json`](data/papers.json) — single verified metadata source of truth
- [`papers/CORE_SYS.md`](papers/CORE_SYS.md) — complete cross-track CORE_SYS inventory
- [`papers/SYS_ALG_BOUNDARY.md`](papers/SYS_ALG_BOUNDARY.md) — system/algorithm boundary work
- [`papers/WATCHLIST.md`](papers/WATCHLIST.md) — emerging or not-yet-mature system directions
- [`latest/LATEST.md`](latest/LATEST.md) — chronological radar updates
- [`taxonomy/RESEARCH_MAP.md`](taxonomy/RESEARCH_MAP.md) — top-level taxonomy index
- [`taxonomy/CROSSOVER.md`](taxonomy/CROSSOVER.md) — where the two tracks converge
- [`CHANGELOG.md`](CHANGELOG.md)

PDFs are intentionally **not** mirrored here; the repository links to official paper/project/repository sources.
