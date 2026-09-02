# Physical AI + Multimodal Serving Radar

> SYS-first research radar for two closely related but independently organized tracks: **Physical AI Serving** and **Multimodal / Omni Efficient Serving**.

**Last updated: 2026-09-03 04:02 CST**

This repository intentionally keeps the two research areas **in one place but written separately**. They share a single verified paper dataset, while each track has its own taxonomy, core reading list, and research narrative.

Pure pruning, quantization, token reduction, or action compression does **not** enter `CORE_SYS` unless it contributes a real runtime, scheduling, resource-management, cache/state, or deployment abstraction.

## Choose a track

| Track | What it studies | Research map | Core reading |
|---|---|---|---|
| 🤖 **Physical AI Serving** | VLA/WAM runtimes, fleet serving, control-loop scheduling, edge/cloud robotics, physical-state cache, heterogeneous robot deployment, evaluation/runtime infrastructure | [`physical_ai/README.md`](physical_ai/README.md) · [`taxonomy/PHYSICAL_AI_MAP.md`](taxonomy/PHYSICAL_AI_MAP.md) | [`physical_ai/CORE_READING.md`](physical_ai/CORE_READING.md) |
| 🌐 **Multimodal / Omni Efficient Serving** | MLLM/Omni stage disaggregation, module multiplexing, any-to-any graph serving, distributed state/KV, streaming interaction, heterogeneous placement, AIGC pipelines | [`multimodal/README.md`](multimodal/README.md) · [`taxonomy/MULTIMODAL_MAP.md`](taxonomy/MULTIMODAL_MAP.md) | [`multimodal/CORE_READING.md`](multimodal/CORE_READING.md) |

The overlap is deliberate, not a classification bug. Systems such as **vLLM-Omni, M\*, Omni-Flow, Cornserve, PhyAI, and ROSA** connect the two tracks. See [`taxonomy/CROSSOVER.md`](taxonomy/CROSSOVER.md).


## Core recommendations

| Title | Year / Venue | Route | System Contribution | Open Source / Repo | Paper | Priority |
|---|---|---|---|---|---|---|
| Kairos | 2026 / arXiv | P1, P3 | Generate–execute-aware fleet serving and execution-aware scheduling | — | [paper](https://arxiv.org/abs/2605.11381) | S+ |
| ROSA | 2026 / arXiv | P1, P7 | Shared-GPU robotics foundation-model serving for robot factories | — | [paper](https://arxiv.org/abs/2607.01088) | S+ |
| PhyAI | 2026 / arXiv | P2, P6, P7, P8, P10 | Unified VLA/WAM runtime across onboard, edge and cloud rollout paths | — | [paper](https://arxiv.org/abs/2608.03682) | S+ |
| M* | 2026 / arXiv | P7, P10, M3 | Modular component-graph serving for multimodal/composite models | — | [paper](https://arxiv.org/abs/2606.12688) | S+ |
| vLLM-Omni | 2026 / arXiv | P2, P7, M1, M3 | Fully disaggregated any-to-any multimodal serving runtime | [repo](https://github.com/vllm-project/vllm-omni) | [paper](https://arxiv.org/abs/2602.02204) | S |
| HorizonServe | 2026 / arXiv | P3, P6, M2, M8 | Heterogeneous-SLO scheduling with temporal/spatial GPU sharing | — | [paper](https://arxiv.org/abs/2608.01785) | A+ |
| CaP-X | 2026 / arXiv | P9 | Open robot coding-agent evaluation/execution substrate with parallel workers and real-robot bringup | [repo](https://github.com/capgym/cap-x) | [paper](https://arxiv.org/abs/2603.22435) | A |
| StreamArena / StreamMind | 2026 / arXiv | P3, P5, P8, P9, M-streaming | Always-on multimodal runtime with independently scheduled frontend/backend workers and persistent-state reuse | [repo](https://github.com/JIA-Lab-research/StreamArena) | [paper](https://arxiv.org/abs/2608.05703) | A |
| TypeGo | 2026 / AgenticOS @ SOSP 2026 | P2, P3, P7 | OS-style task processes/PCBs, Skill Kernel physical-resource arbitration, preemption and asynchronous multi-timescale planning | — | [paper](https://arxiv.org/abs/2607.05482) | A+ |
| TimelyLLM | 2026 / ACM MobiSys 2026 | P1, P3, P8 | Segmented, timing-aware LLM serving for multiple physical agents; overlaps plan generation with physical-I/O execution | Artifact award verified; public repo not independently resolved | [paper](https://arxiv.org/abs/2412.18695) | A+ |

---

# Track A — Physical AI Serving

Physical AI serving treats **physical execution, state freshness, deadlines, robots, and world-model rollouts as first-class system concerns** rather than ordinary request/response inference.

| Route | Focus | Representative anchors |
|---|---|---|
| P1. Fleet-scale / Multi-Robot Serving | GPU pools, batching, execution-aware scheduling, fleet learning loops | Kairos, ROSA, Armory, TimelyLLM, SOP, Physical Agentic AI |
| P2. Unified Physical-AI Runtime | portable VLA/WAM execution, robot-facing serving APIs, embodied-agent harnesses | PhyAI, Embodied.cpp, vla.cpp, LeRobot, Thea, Retriever, TypeGo, Physical Agentic AI |
| P3. Real-Time / Streaming / Control Loop | reaction latency, deadlines, async execution, accelerator arbitration | CROS-RT, PAAM, TimelyLLM, TypeFly, VLASH, FASTER, Retriever, TypeGo |
| P4. Edge-Cloud / Disaggregated Physical AI | device/edge/cloud placement, network/tail-latency reliability | RoboECC, RAPID, EcoVLA, FogROS2 |
| P5. Physical-State / Temporal Cache | cache validity over vision/action/world/planner/execution state | AgenticCache, Persistent Computational State, Execution-State Capsules, DreamLedger |
| P6. Hardware-Aware / Heterogeneous Serving | GPU/XPU/NPU placement, CPU-GPU partitioning, offload | XPU Characterization, PAAM, OOM-Free Alpamayo |
| P7. Composite VLA + WAM + Planner Serving | policy + planner + world model + verifier/safety/tool graphs | M*, PhyAI, vLLM-Omni, Thea, Physical Agentic AI |
| P8. Workload Characterization / Modeling | control-time, network, cost-energy-time models | VLA-Perf, PhyAI |
| P9. Evaluation / Serving Infrastructure | model-server decoupling, real-robot EaaS, experiment control/evidence, observability, simulator reliability | DeepInsight, RoboArena, RoboChallenge, PhAIL, CaP-X, AgenticRobotics, DreamLedger, RoboFuzz, PHYFU, IcFuzz |
| P10. World-Model / WAM Rollout Serving | persistent rollout state, trust/credit state, branch scheduling, migration, rollback/fork | WorldMove, PCS, PhyAI, DreamLedger |

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

| FlashRT: Agent Harness for Guiding Agents to Deploy Real-Time Multimodal Applications | 2026 / arXiv | 2/3/6/7/10/11 | Agent-guided IR + streaming/multi-GPU deployment runtime across CUDA/ROCm | [Repo](https://github.com/Infini-AI-Lab/FlashRT) | [Paper](https://arxiv.org/abs/2607.18171) | A+ |
| Lingjing: A Simulation Testbed for Multi-Agent Embodied Tasks in Open-Ended Cities | 2026 / arXiv | 1/2/9 | Multi-engine city-scale heterogeneous-agent runtime + replayable evaluation | [Repo](https://github.com/seanlxh/Air-Lingjing) | [Paper](https://arxiv.org/abs/2608.08045) | A+ |
| Deployment Is Not Destiny: Robot Recomposition in the Field with Unseen Software, Hardware, and Compute Payloads | 2026 / arXiv | 1/2/4/6/7 | Runtime recomposition + distributed capability/compute sharing | — | [Paper](https://arxiv.org/abs/2608.11063) | A |

