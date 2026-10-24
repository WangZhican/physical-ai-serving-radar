# Physical AI + Multimodal Serving Radar

> SYS-first research radar for two closely related but independently organized tracks: **Physical AI Serving** and **Multimodal / Omni Efficient Serving**.

**Last updated: 2026-10-25 05:10 CST**

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
| GPU-resident Execution | 2026 / arXiv | P2, P3, P6, P9 | Host-free GPU sensor I/O + persistent CUDA Graph execution; 1080p camera jitter 4.83→0.66ms, not VLA serving | Holoscan SDK exists; dedicated implementation unverified | [paper](https://arxiv.org/abs/2610.13809) | A |
| HeteroVDiff | 2026 / arXiv | P6, P8 (multimodal) | Galaxy S25 NPU/GPU video diffusion shared-weight pipeline; 1.35× stream throughput, SLO-qualified | Dedicated code unverified | [paper](https://arxiv.org/abs/2610.16244) | A |
| Isaac-Net | 2026 / arXiv | P1, P9 | GPU 5G network-in-loop robot fleet simulation; 1,048,576 robots, training/evaluation only | [BSD-3 code](https://github.com/ZzZTripleZzZ/isaac-net) | [paper](https://arxiv.org/abs/2610.02370) | A- |
| Kairos | 2026 / arXiv | P1, P3 | Generate–execute-aware fleet serving and execution-aware scheduling | — | [paper](https://arxiv.org/abs/2605.11381) | S+ |
| ROSA | 2026 / arXiv | P1, P7 | Shared-GPU robotics foundation-model serving for robot factories | — | [paper](https://arxiv.org/abs/2607.01088) | S+ |
| Robion | 2026 / arXiv | P1, P2, P3, P4, P6, P8 | SLO-aware multi-robot/multi-model VLA serving; intra-GPU VLM/ADiT overlap, dynamic SM partitioning, co-location, placement and traffic assignment | — | [paper](https://arxiv.org/abs/2609.12075) | S+ |
| Industrial ReMEmbR | 2026 / arXiv | P1, P4, P5, P9 | Fleet-shared edge/on-prem vision-token memory and on-demand decoder; 100-robot GPU saving is modeled | Industrial extension repo not verified; [upstream ReMEmbR](https://github.com/NVIDIA-AI-IOT/remembr) | [paper](https://arxiv.org/abs/2610.28624) | A+ |
| FATS / Fleet Experience | 2026 / arXiv | P1, P2, P4, P9 | Real 96-robot fault-tolerant fleet execution, shared cloud inference and streaming experience; not a serving SLO study | Dedicated release not verified | [paper](https://arxiv.org/abs/2610.25736) | A |
| rMuscle | 2026 / arXiv | P3, P5, P6, P8 | Two-stage cross-execution VLA inference cache; 1.20–1.42x end-to-end vs FlashRT on RTX 4090/Jetson Thor | Dedicated code unverified | [paper](https://arxiv.org/abs/2609.19104) | A |
| OrbitWeaver | 2026 / arXiv | M4, M6; P5, P6, P9 transfer | Phase-aware VLM checkpoint/recovery on edge hardware; 72h two-satellite deployment, up to 4.07x paper-reported speedup | Dedicated code unverified | [paper](https://arxiv.org/abs/2610.29183) | A |
| HarnessPAI | 2026 / arXiv | P2, P3, P7, P9 | Executable Physical-AI harness with offline code evolution and reusable skills; no online high-level LLM per rollout; not a multi-tenant serving/SLO result | [MIT repo](https://github.com/Darwin-Agent/HarnessPAI) | [paper](https://arxiv.org/abs/2609.29166) | A |
| CARE | 2026 / arXiv | P3, P4, P7 | Adaptive local/cloud executor handoff and shared memory; 28.8–82.6% lower median time-between-action, decision-layer only | Dedicated code unverified | [paper](https://arxiv.org/abs/2610.30587) | A- |
| FastHarness | 2026 / arXiv | P2, P3, P7 | Memory-guided reviewer scheduling over VLA action chunks; 57.2% fewer tokens and 85.5→52.0 min episodes, simulation only | [MIT repo](https://github.com/FastHarness/fast-harness) | [paper](https://arxiv.org/abs/2610.31427) | A- |
| CusADi2 | 2026 / arXiv | P3, P6, P9 | GPU robot kinematics/Jacobians/Hessians DAG scheduling on RTX 4080; 67 robots, <40us common-platform evaluation, 50Hz Franka planner; not VLA serving | [MIT repo](https://github.com/johnviljoen/cusadi2) | [paper](https://arxiv.org/abs/2610.25476) | A- |
| xDiT | 2024 / arXiv | M/DiT P6/P7/P10 transfer | Hybrid SP/PipeFusion/CFG distributed DiT inference, real L40 Ethernet and A100 NVLink GPU clusters | [Apache-2.0 repo](https://github.com/xdit-project/xDiT) | [paper](https://arxiv.org/abs/2411.01738) | A+ |
| DDiT | 2025 / arXiv | M/DiT P3/P6/P7/P8 transfer | T2V T5/DiT/VAE stage-aware GPU resource allocation and step scheduling; up to 1.44x p99 latency; 8-server emulated scaling | Code unverified | [paper](https://arxiv.org/abs/2506.13497) | A |
| RETNAS | 2026 / RTNS | P3, P6, P9 (transfer) | HRT-certified mixed-deadline DAG DNN inference scheduling on heterogeneous accelerators; simulated, no robot deployment | [simulator](https://github.com/BlancoFrancescoGiulio/retnas) | [paper](https://arxiv.org/abs/2610.29503) | A- |
| PhyAI | 2026 / arXiv | P2, P6, P7, P8, P10 | Unified VLA/WAM runtime across onboard, edge and cloud rollout paths | — | [paper](https://arxiv.org/abs/2608.03682) | S+ |
| M* | 2026 / arXiv | P7, P10, M3 | Modular component-graph serving for multimodal/composite models | — | [paper](https://arxiv.org/abs/2606.12688) | S+ |
| vLLM-Omni | 2026 / arXiv | P2, P7, M1, M3 | Fully disaggregated any-to-any multimodal serving runtime | [repo](https://github.com/vllm-project/vllm-omni) | [paper](https://arxiv.org/abs/2602.02204) | S |
| GENSERVE | 2026 / arXiv | M-diffusion, P3/P6/P7/P8 transfer | 8×RTX PRO 6000 Blackwell T2I/T2V co-serving: step preemption, elastic SP/dynamic batching, SLO-aware scheduling; up to 44% relative SLO-attainment gain | Dedicated code unverified | [paper](https://arxiv.org/abs/2604.04335) | A+ |
| HorizonServe | 2026 / arXiv | P3, P6, M2, M8 | Heterogeneous-SLO scheduling with temporal/spatial GPU sharing | — | [paper](https://arxiv.org/abs/2608.01785) | A+ |
| CaP-X | 2026 / arXiv | P9 | Open robot coding-agent evaluation/execution substrate with parallel workers and real-robot bringup | [repo](https://github.com/capgym/cap-x) | [paper](https://arxiv.org/abs/2603.22435) | A |
| StreamArena / StreamMind | 2026 / arXiv | P3, P5, P8, P9, M-streaming | Always-on multimodal runtime with independently scheduled frontend/backend workers and persistent-state reuse | [repo](https://github.com/JIA-Lab-research/StreamArena) | [paper](https://arxiv.org/abs/2608.05703) | A |
| TypeGo | 2026 / AgenticOS @ SOSP 2026 | P2, P3, P7 | OS-style task processes/PCBs, Skill Kernel physical-resource arbitration, preemption and asynchronous multi-timescale planning | — | [paper](https://arxiv.org/abs/2607.05482) | A+ |
| TimelyLLM | 2026 / ACM MobiSys 2026 | P1, P3, P8 | Segmented, timing-aware LLM serving for multiple physical agents; overlaps plan generation with physical-I/O execution | Artifact award verified; public repo not independently resolved | [paper](https://arxiv.org/abs/2412.18695) | A+ |
| OmniEvaluator | 2026 / arXiv | P9, M-eval | Composable omni-modal evaluation/serving substrate with shared inference servers, provenance artifacts and dashboard | [repo](https://github.com/naver-ai/omni-evaluator) | [paper](https://arxiv.org/abs/2609.01315) | A+ |

---

# Track A — Physical AI Serving

Physical AI serving treats **physical execution, state freshness, deadlines, robots, and world-model rollouts as first-class system concerns** rather than ordinary request/response inference.

| Route | Focus | Representative anchors |
|---|---|---|
| P1. Fleet-scale / Multi-Robot Serving | GPU pools, batching, execution-aware scheduling, fleet learning loops | Kairos, ROSA, Robion, Armory, TimelyLLM, SOP, Physical Agentic AI |
| P2. Unified Physical-AI Runtime | portable VLA/WAM execution, robot-facing serving APIs, embodied-agent harnesses | PhyAI, Robion, Embodied.cpp, vla.cpp, LeRobot, Thea, Retriever, TypeGo, Physical Agentic AI |
| P3. Real-Time / Streaming / Control Loop | reaction latency, deadlines, async execution, accelerator arbitration | Robion, CROS-RT, PAAM, TimelyLLM, TypeFly, VLASH, FASTER, Retriever, TypeGo |
| P4. Edge-Cloud / Disaggregated Physical AI | device/edge/cloud placement, network/tail-latency reliability | Robion, RoboECC, RAPID, EcoVLA, FogROS2 |
| P5. Physical-State / Temporal Cache | cache validity over vision/action/world/planner/execution state | AgenticCache, Persistent Computational State, Execution-State Capsules, DreamLedger |
| P6. Hardware-Aware / Heterogeneous Serving | GPU/XPU/NPU placement, CPU-GPU partitioning, offload | Robion, XPU Characterization, PAAM, OOM-Free Alpamayo |
| P7. Composite VLA + WAM + Planner Serving | policy + planner + world model + verifier/safety/tool graphs | M*, PhyAI, vLLM-Omni, Thea, Physical Agentic AI |
| P8. Workload Characterization / Modeling | control-time, network, cost-energy-time models | VLA-Perf, Robion, PhyAI |
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

