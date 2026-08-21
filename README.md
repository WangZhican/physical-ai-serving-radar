# Physical AI Serving Radar

> SYS-first research radar for **Physical AI + Multimodal Efficient Serving**: runtimes, schedulers, resource managers, edge/cloud deployment, state/cache infrastructure, fleet serving, evaluation infrastructure, world-model serving, and transferable multimodal systems.

**Last updated: 2026-08-21 16:04 CST**

Pure pruning, quantization, token reduction, or action compression does **not** enter `CORE_SYS` unless it contributes a real runtime/resource-management/deployment abstraction.

## Research map

| Route | Focus | Representative anchors |
|---|---|---|
| 1. Fleet-scale / Multi-Robot Serving | GPU pools, batching, execution-aware scheduling, fleet-to-cloud learning loops | Kairos, ROSA, Armory, SOP |
| 2. Unified Physical-AI Runtime | portable VLA/WAM execution | PhyAI, Embodied.cpp, vla.cpp |
| 3. Real-Time / Streaming / Control Loop | deadlines, async execution, executor/GPU scheduling | CROS-RT, PAAM, ROSGM, LaME |
| 4. Edge-Cloud / Disaggregated Physical AI | placement, cloud/fog deployment, reliability | RoboECC, RAPID, EcoVLA, FogROS2 |
| 5. Physical-State / Temporal Cache | cache validity, planner/action/world state | AgenticCache, Persistent Computational State |
| 6. Hardware-Aware / Heterogeneous Serving | GPU/XPU/NPU placement and arbitration | XPU Characterization, PAAM, GCAPS |
| 7. Composite VLA + WAM + Planner Serving | multi-component graphs and shared state | M*, PhyAI, vLLM-Omni |
| 8. Workload Characterization / Modeling | control-time, transport and discovery models | VLA-Perf, PhyAI, Discovery Storm |
| 9. Evaluation / Serving Infrastructure | traces, robot EaaS, observability | DeepInsight, RoboArena, CARET, TILDE |
| 10. World-Model / WAM Rollout Serving | persistent sessions, rollout state, migration | WorldMove, Persistent Computational State |

See [`taxonomy/RESEARCH_MAP.md`](taxonomy/RESEARCH_MAP.md). Adjacent MLLM/Omni systems are tracked separately as transferable foundations.

## Core recommendations

| Title | Year/Venue | Route | System Contribution | Open Source/Repo | Paper | Priority |
|---|---|---|---|---|---|---|
| Kairos | 2026/arXiv | 1,3 | generate–execute-aware multi-robot serving | — | [paper](https://arxiv.org/abs/2605.11381) | S+ |
| ROSA | 2026/arXiv | 1,7 | robot-factory GPU pooling and productivity scheduling | — | [paper](https://arxiv.org/abs/2607.01088) | S+ |
| PhyAI | 2026/arXiv | 2,6,7,10 | unified edge/cloud/rollout execution engine | — | [paper](https://arxiv.org/abs/2608.03682) | S+ |
| M* | 2026/arXiv | 7 | modular composite-model serving graph | — | [paper](https://arxiv.org/abs/2606.12688) | S+ |
| VLA-Perf | 2026/arXiv | 4,8 | VLA deployment/performance characterization | — | [paper](https://arxiv.org/abs/2602.18397) | S |
| Embodied.cpp | 2026/arXiv | 2,6 | portable embodied inference runtime | — | [paper](https://arxiv.org/abs/2607.02501) | S |
| vla.cpp | 2026/arXiv | 2,6 | portable C++ VLA runtime | — | [paper](https://arxiv.org/abs/2606.08094) | S |
| Armory | 2026/arXiv | 1,3 | control-aware batched robot-policy serving | — | [paper](https://arxiv.org/abs/2608.00337) | A+ |
| SOP | 2026/arXiv | 1,2,7,9 | fleet/cloud actor-learner loop; online experience streaming and async policy synchronization | — | [paper](https://arxiv.org/abs/2601.03044) | A+ |
| LeRobot | 2026/ICLR | 2,3,9 | generalized remote async robot-policy inference; gRPC PolicyServer/RobotClient with action queues and overlap aggregation | [repo](https://github.com/huggingface/lerobot) | [paper](https://arxiv.org/abs/2602.22818) | A+ |
| PAAM | 2024/RTAS | 3,6 | shared GPU/TPU accelerator server | [repo](https://github.com/rtenlab/reference-system-paam) | [paper](https://arxiv.org/abs/2404.06452) | A+ |
| FogROS 2 | 2023/ICRA | 4,6 | cloud/fog ROS2 deployment substrate | [repo](https://github.com/BerkeleyAutomation/FogROS2) | [paper](https://arxiv.org/abs/2205.09778) | A+ |
| FogROS2-Config | 2024/ICRA | 4,6,8 | cloud server/config selection | — | [paper](https://arxiv.org/abs/2311.05600) | A |
| FogROS2-PLR | 2025/ICRA | 3,4 | tail-latency/reliability-aware cloud robotics | — | [paper](https://arxiv.org/abs/2410.05562) | A+ |
| DeepInsight | 2026/arXiv | 9 | cross-stack Physical-AI evaluation runtime | — | [paper](https://arxiv.org/abs/2606.17574) | A+ |
| RoboArena | 2025/CoRL Oral | 9 | distributed real-robot evaluation network | — | [paper](https://arxiv.org/abs/2506.18123) | A+ |
| ros2probe | 2026/arXiv | 8,9 | non-intrusive ROS2 observability | [repo](https://github.com/csi-dgist/ros2probe) | [paper](https://arxiv.org/abs/2606.10746) | A+ |
| HeyGen HELIOS | 2026/Tech Report | 6,7,11 | 5,000+ GPU multi-cloud QoS scheduling and declarative multimodal/video pipeline infrastructure | — | [report](https://www.heygen.com/research/avatar-v-infrastructure) | A+ |

## Browse

- [`papers/CORE_SYS.md`](papers/CORE_SYS.md)
- [`papers/SYS_ALG_BOUNDARY.md`](papers/SYS_ALG_BOUNDARY.md)
- [`papers/WATCHLIST.md`](papers/WATCHLIST.md)
- [`taxonomy/RESEARCH_MAP.md`](taxonomy/RESEARCH_MAP.md)
- [`latest/LATEST.md`](latest/LATEST.md)
- [`data/papers.json`](data/papers.json)
- [`CHANGELOG.md`](CHANGELOG.md)

PDFs are intentionally **not** mirrored here; use official paper/project/repository links.

## Radar update — 2026-08-21 16:04 CST
- **SOP** adds a missing fleet continual-learning systems line: multi-robot online experience/intervention streaming to a centralized cloud learner with asynchronous policy synchronization; AGIBOT reports 2.4× faster time-to-80% success with four robots versus one.
- **Learning while Deploying (LWD)** is tracked at `SYS_ALG_BOUNDARY`: real 16-robot deployment/replay/policy-refresh infrastructure, but its primary novelty is offline-to-online RL rather than serving/resource scheduling.
- Current public dataset: **110 verified works — 83 CORE_SYS / 18 SYS_ALG_BOUNDARY / 4 ALG_INSPIRATION / 5 WATCH_ONLY**.

