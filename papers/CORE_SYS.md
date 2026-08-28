# CORE_SYS

Primary contribution must be runtime, serving, resource management, scheduling, deployment, cache/state infrastructure, heterogeneous execution, profiling, or evaluation infrastructure.

## Physical-AI serving trunk
- [Kairos](https://arxiv.org/abs/2605.11381) — multi-robot generate–execute-aware serving — **S+**
- [ROSA](https://arxiv.org/abs/2607.01088) — robot-factory shared GPU serving — **S+**
- [PhyAI](https://arxiv.org/abs/2608.03682) — unified onboard/edge/cloud/rollout engine — **S+**
- [M*](https://arxiv.org/abs/2606.12688) — modular composite-model serving — **S+**
- [VLA-Perf](https://arxiv.org/abs/2602.18397) — deployment/performance map — **S**
- [Embodied.cpp](https://arxiv.org/abs/2607.02501) — portable embodied runtime — **S**
- [vla.cpp](https://arxiv.org/abs/2606.08094) — portable C++ VLA runtime — **S**
- [Characterizing VLA Models across XPUs](https://arxiv.org/abs/2604.24447) — heterogeneous phase characterization — **S**
- [Armory](https://arxiv.org/abs/2608.00337) — control-aware batched robot-policy serving — **A+**
- [Retriever](https://arxiv.org/abs/2607.17213) — temporal computation-graph runtime for multi-rate closed-loop robot programs (`Flow` / `Clock` / `Sync`, replay/debugging, multi-backend execution) — **A+** · [project](https://retriever.systems/) · [repo](https://github.com/openretriever/retriever)
- [Physical Agentic AI](https://arxiv.org/abs/2608.22657) — heterogeneous robot-crew orchestration with typed skills/workflow contracts and deterministic per-dispatch execution authorization; separates LLM planner knowledge from physical actuation authority — **A**
- [LeRobot](https://arxiv.org/abs/2602.22818) — ICLR 2026 end-to-end robot-learning infrastructure; generalized gRPC PolicyServer/RobotClient async inference with action-queue/overlap semantics — **A+** · [repo](https://github.com/huggingface/lerobot)
- [RobotFleet](https://arxiv.org/abs/2510.10379) — RSS 2025 Multi-Robot Systems Workshop; centralized fleet planner/allocator + task-status/schedule manager over containerized robot services, with shared world state and feedback-driven replanning — **A-** · [repo](https://github.com/therohangupta/robot-fleet)

## Edge / cloud / heterogeneous deployment
- [RoboECC](https://arxiv.org/abs/2603.20711) — model/hardware/network-aware edge-cloud partitioning — **A+**
- [RAPID](https://arxiv.org/abs/2603.07949) — physical-state-triggered edge/cloud offload — **A**
- [EcoVLA (device-edge)](https://arxiv.org/abs/2608.15502) — stage-level energy-aware co-inference — **A+**
- [FogROS 2](https://arxiv.org/abs/2205.09778) — cloud/fog ROS2 deployment substrate — **A+** · [repo](https://github.com/BerkeleyAutomation/FogROS2)
- [FogROS2-Config](https://arxiv.org/abs/2311.05600) — cloud server/configuration selection — **A**
- [FogROS2-PLR](https://arxiv.org/abs/2410.05562) — probabilistic latency/reliability management — **A+**

## Real-time runtime / resource management
- [PAAM](https://arxiv.org/abs/2404.06452) — shared accelerator server and priority arbitration — **A+** · [repo](https://github.com/rtenlab/reference-system-paam)
- **CROS-RT** — cross-layer ROS2 priority propagation — **A+**
- **ROSGM** — pluggable real-time GPU management for ROS2 — **A**
- **GCAPS** — driver-level GPU context preemption — **A**
- **LaME** — adaptive latency/resource management executor — **A+**

## State / cache / world sessions
- [AgenticCache](https://arxiv.org/abs/2604.24039) — planner-transition runtime cache — **A+**
- [Persistent Computational State](https://arxiv.org/abs/2607.21686) — world-session checkpoint/restore — **A**
- [WorldMove](https://arxiv.org/abs/2607.10389) — exact-state migration and admission control — **A**

## Evaluation / observability infrastructure
- [DeepInsight](https://arxiv.org/abs/2606.17574) — cross-stack Physical-AI evaluation runtime — **A+**
- [RoboArena](https://arxiv.org/abs/2506.18123) — distributed real-robot evaluation — **A+**
- [AutoEval](https://arxiv.org/abs/2503.24278) — real-robot evaluation-as-a-service — **A+**
- [RoboDojo](https://arxiv.org/abs/2607.04434) — unified sim/real remote evaluation — **A+**
- [ros2probe](https://arxiv.org/abs/2606.10746) — non-intrusive middleware observability — **A+** · [repo](https://github.com/csi-dgist/ros2probe)
- **CARET** — chain-aware ROS2 latency evaluation — **A** · [repo](https://github.com/tier4/CARET)
- **TILDE** — online message-latency/deadline tracking — **A** · [repo](https://github.com/tier4/TILDE)

This page is intentionally selective; machine-readable coverage lives in [`data/papers.json`](../data/papers.json).

- **FogROS2-LS** — ICRA 2024 — Routes 3/4 — location-independent latency-sensitive cloud/fog service selection for ROS 2; [paper](https://doi.org/10.1109/ICRA57147.2024.10610759). Priority: A+.

## Industrial multimodal infrastructure
- [HeyGen HELIOS](https://www.heygen.com/research/avatar-v-infrastructure) — 5,000+ GPU multi-cloud unified control plane, two-stage QoS-aware scheduling, resource governance, observability and declarative heterogeneous video-pipeline engine — **A+**. Transferable serving/infra anchor; not Physical-AI-specific.

- **HydraInfer** (2025, arXiv:2505.12658) — Route 6/11; hybrid EPD-disaggregated MLLM serving with heterogeneous stage placement and stage-level batching. [Paper](https://arxiv.org/abs/2505.12658) — Priority A.
- [**On the Limitations of Non-GPU AI Accelerators for Large-Model Inference**](https://arxiv.org/abs/2607.08215) — Routes 6/8/11; field study of real MoE + multimodal serving on a 16-device Huawei Ascend 910 system using CANN + vLLM-Ascend. Documents 12 source-level integration patches plus platform limits in correctness, parallelism, compilation, scalability, observability and fault handling. [Repo](https://github.com/YuZhengYYDS/ascend-large-model-inference-field-study) — **Priority A**.
## 2026-08-21 omission recovery
- [**JoyNexus**](https://arxiv.org/abs/2607.16074) — service-oriented **multi-tenant VLA** post-training/inference/evaluation substrate with tenant-scoped state, Training/Inference/Environment Services, separate global queues, group batching, fault isolation and elastic rollout scaling — **A+**, Routes 2/7/9.
- [**FlashCodec + UnifiedServe**](https://arxiv.org/abs/2512.17574) — multi-stage MLLM serving with collaborative multi-GPU/NVDEC preprocessing and logical stage disaggregation over physically shared GPU resources — **A+**, Routes 6/11.


## Cloud-native embodied simulation / evaluation infrastructure
- [**Cloud-Native Simulation Infrastructure for Embodied Intelligence**](https://arxiv.org/abs/2606.27962) — elastic resource scheduling, containerized simulation, standardized model/task/evaluation interfaces, trajectory/data governance, and failure-driven closed-loop regeneration — **A-**, Routes 7/9. Early-stage infrastructure white paper; no verified public implementation repo yet.

## Distributed VLA RL / rollout infrastructure
- [**D-VLA**](https://arxiv.org/abs/2605.13276) — Plane Decoupling, asynchronous Swimlane overlap, dual-pool VRAM management and topology-aware replication for high-concurrency distributed VLA RL — **A+**, Routes 2/6/7/9.

## Distributed VLA RL / rollout infrastructure
- [**RL-VLA3**](https://arxiv.org/abs/2602.05765) — fully asynchronous simulation/inference/training, dynamic batching, environment sharding, and 8–256 GPU scalability — **A+**, Routes 2/6/7/9. Current arXiv v2 reports up to 85.2% throughput improvement over synchronous baselines with identical sample efficiency; older workshop metrics are kept version-scoped.

### CoMuRoS — Frontiers in Robotics and AI 2026
**Routes:** 1 Fleet-scale / multi-robot; 7 Composite VLA + planner serving · **Priority:** A-

A hierarchical multi-robot runtime with centralized task management and decentralized ROS2 execution. Its system role is runtime task classification/dispatch, queue-based execution, bidirectional status/event feedback, and event-triggered replanning/task reallocation on physical heterogeneous robots. This complements GPU-policy serving systems such as Armory: CoMuRoS orchestrates the planner/execution layer rather than GPU inference resources. [Official paper](https://doi.org/10.3389/frobt.2026.1843313)

### SOP — Scalable Online Post-Training System for VLA Models
**Routes:** 1 / 2 / 7 / 9 · **Priority:** A+

[Paper](https://arxiv.org/abs/2601.03044) · [AGIBOT project page](https://finch.agibot.com/research/sop)

A fleet/cloud actor-learner substrate: multiple robots stream on-policy trajectories and human interventions to a centralized cloud learner, and asynchronously receive updated shared policies. The architecture is algorithm-agnostic and is demonstrated with HG-DAgger and RECAP. AGIBOT reports a four-robot configuration reaching 92.5% success after 3 hours versus 80.5% for one robot, and reaching 80% success in 71.7 minutes versus 173.6 minutes (2.4× faster). No official implementation repository was verified in this scan.
## RLinf embodied-learning infrastructure — 2026-08-21
- **RLinf-VLA** — RSS 2026 — Routes 2/6/7/9 — `A+`. Unified simulator/model/algorithm interfaces and collocated/disaggregated/hybrid GPU resource allocation; hybrid pipeline allocation reports 1.61×–1.88× speedup, with project-level comparison up to 2.27×. [Paper](https://arxiv.org/abs/2510.06710) · [Project](https://rlinf-vla.github.io/) · [Repo](https://github.com/RLinf/RLinf)
- **RLinf-USER** — RSS 2026 — Routes 1/2/4/6/7/9 — `A+`. Robots become first-class schedulable hardware resources alongside GPUs; adaptive cloud-edge networking/data channels, SM-aware weight synchronization, asynchronous online learning, persistent cache-aware buffering and crash recovery. [Paper](https://arxiv.org/abs/2602.07837) · [Project](https://rlinf-user.github.io/) · [Repo](https://github.com/RLinf/RLinf)


## RLinf base system — OSDI 2026
- [**RLinf: Flexible and Efficient Large-Scale Reinforcement Learning via Macro-to-Micro Flow Transformation**](https://arxiv.org/abs/2509.15965) — **A+**, Routes 2/6/7/9. M2Flow rewrites logical RL workflows into optimized execution flows; adaptive communication, context switching, elastic pipelining and profiling-guided scheduling are evaluated on reasoning and embodied RL. [OSDI 2026](https://www.usenix.org/conference/osdi26/presentation/yu-chao) · [Repo](https://github.com/RLinf/RLinf). Current OSDI/docs report up to **2.43×** embodied-RL throughput speedup; older arXiv abstract numbers are version-scoped.

## Real-time multi-robot control runtime
- [**multipanda_ros2**](https://arxiv.org/abs/2602.02269) — ICRA 2026 — **A**, Routes 2/3/9. Open-source ROS2 runtime for controlling arbitrary numbers of Franka robots from one process; sustains a 1 kHz torque-control loop, supports <=2 ms controller switching and runtime recovery, and exposes matched simulation/real interfaces for reproducible multi-robot benchmarking. [Repo](https://github.com/tenfoldpaper/multipanda_ros2) (~88 stars / 39 forks in current crawl).


### OSDAG — Online Scheduling for Efficient Multi-Robot Collaboration (2026)
- Routes: fleet-scale/multi-robot serving; composite planner/execution runtime.
- Contribution: dependency/resource DAG plus constraint-aware online ready-task scheduling across heterogeneous robots.
- Result: 5-15x faster reasoning; up to 38% makespan reduction; simulation + real dual-arm validation.
- Paper: https://arxiv.org/abs/2606.15255
- Project: http://thanhnguyencanh.github.io/LLM_DAG4MultiRobot
- Priority: A- (strong execution scheduler; not GPU-serving/resource-manager).

### OpenBot-Fleet — ICRA 2024 — A+
**Routes:** 1 Fleet-scale serving · 4 Edge-cloud Physical AI · 9 Evaluation/infrastructure. Open-source full policy-improvement loop across 72 real robots: edge sensing/compute, secure cloud experience upload, asynchronous collection, replay/policy learning, and continuous policy redeployment. Online learning reaches 82.5% success in unseen homes. [Paper](https://arxiv.org/abs/2405.07515) · [Project](https://www.openbot.org/)

### Execution-State Capsules / FlashRT — arXiv:2606.20537 — A+
Routes 3/5/6. Complete graph-bound execution-state checkpoint/restore/fork/rollback for low-latency, small-batch, on-device Physical-AI serving. Includes KV, recurrent, convolution, MTP state and metadata; sub-ms GPU restore and 3.9x to 27x TTFT speedup over cold prefill from 2k to 16k context. Paper: https://arxiv.org/abs/2606.20537 · Repo: https://github.com/flashrt-project/FlashRT

### PhAIL — arXiv:2605.29710 — A
Routes 8/9. Open real-robot VLA evaluation infrastructure with Franka FR3 rollouts, distributional time-to-success, Human-Relative Throughput, bootstrap confidence intervals, KS tests and public per-rollout artifacts/reference implementation. Paper: https://arxiv.org/abs/2605.29710 · Project: https://phail.ai/

### RoboChallenge — Large-scale Real-robot Evaluation of Embodied Policies — A+
**Routes:** P3 Real-Time / Streaming / Control Loop · P9 Evaluation / Serving Infrastructure

Public online real-robot evaluation infrastructure rather than a static benchmark: a 10-machine heterogeneous fleet (UR5, Franka, Aloha, ARX-5), low-level fully asynchronous APIs with precisely timestamped observations and explicit FIFO action-queue state, evaluation-job scheduling, public submission/results, and 7×24-oriented service design. [Paper](https://arxiv.org/abs/2510.17950) · [Project](https://robochallenge.ai/) · [Repo](https://github.com/RoboChallenge/RoboChallengeInference)


### Thea — Towards the Harness of Embodied Agents — A
**Routes:** P2 Unified Physical-AI Runtime · P5 Physical-State / State Reuse · P7 Composite VLA + WAM + Planner Serving

Provider-neutral embodied-agent harness/runtime that owns the agentic loop, context lifetimes, Tool Protocol, memory, skills, safety and post-execution evaluation. `Scene Graph as Context` provides persistent symbolic world state; `Evaluation as Exit Codes` makes physical tool outcomes observable and recoverable; an embodiment profile ports the same harness across robot bodies. Validated on Astribot S1, AgileX Cobot Magic and Unitree G1; evaluator accuracy is 93.3% on 90 real-robot checkpoints. [Paper](https://arxiv.org/abs/2608.11246) · [Project](https://eit-hai.github.io/thea/) · [Repo](https://github.com/EIT-HAI/Thea) (~45 stars in current public crawl).

### Zetta ζ / Z-Infra — A+
- **Paper:** https://arxiv.org/abs/2608.16590
- **Repo:** https://github.com/air-embodied-brain/Zetta-Embodiment
- **Routes:** 2 / 3 / 6 / 7 / 9
- **System role:** closed-loop embodied harness; action-frequency runtime governance; Z-Infra decouples agent logic from heterogeneous rollout execution resources.

### RoboLab — A+
**Route:** P9 Evaluation / Serving Infrastructure  
NVIDIA RSS 2026 evaluation runtime for task-generalist robot policies: robot/policy-agnostic task generation, server-client policy execution, automated success/failure predicates, multi-environment parallel evaluation, faithful replay and a results dashboard. The Apache-2.0 implementation is actively released. [Paper](https://arxiv.org/abs/2604.09860) · [Project](https://research.nvidia.com/labs/srl/projects/robolab/) · [Repo](https://github.com/NVlabs/RoboLab) (~447 stars / 66 forks in current crawl).

## 2026-08-23 14:00 CST

**Coverage:** 24h + 7d fresh scan; targeted 30d omission recovery.

**New CORE_SYS:** AEROS (arXiv:2604.07039) and Harnessing Embodied Agents: Runtime Governance for Policy-Constrained Execution (arXiv:2604.07833). AEROS adds a persistent-agent / installable-capability runtime abstraction; Runtime Governance externalizes admission, policy enforcement, monitoring, rollback, and human override.

**Evidence boundary:** AEROS has an Apache-2.0 runtime MVP, but its current public implementation is single-process/single-thread, mock-robot, and has no real-time guarantees; do not overstate production maturity.

## 2026-08-23 16:00 CST — ECM Contracts
- [**ECM Contracts**](https://arxiv.org/abs/2604.13097) — **A-**, Routes 2/5/7. Implements an embodied-capability registry/resolver/contract checker and pre-deployment compatibility checks over resource requirements, permission boundaries, recovery semantics and version compatibility. Current arXiv evaluation reports 56%/72% prediction of independently documented ROS integration failures across two substrates versus at most 17% for type/QoS baselines, with zero false positives on matched-good controls.
- **Maturity boundary:** prototype infrastructure rather than a production serving runtime; no official public repository was verified in this scan.

## 2026-08-25 — PhyAgentOS
- [**PhyAgentOS**](https://arxiv.org/abs/2607.16636) — **A+**, Routes 2/3/5/7/9 · [repo](https://github.com/PhyAgentOS/PhyAgentOS). Session-centered embodied operating/runtime substrate that makes scheduling, compatibility preflight, supervised execution, semantic verification, persistent state/memory, benchmarking and layered safety first-class services. `State-as-a-File` and target adapters decouple cognitive planning from heterogeneous simulation/real-robot execution.

### IcFuzz — ASE 2026 — A
**Route:** P9 Evaluation / Serving Infrastructure  
First Isaac Sim-focused reliability/fuzzing infrastructure: semantic-stage-guided valid program generation, multi-level mutations, coverage/crash feedback and adaptive mutation scheduling. Reports ~190%-205% baseline coverage, 3.7 unique crashes across three 12-hour rounds, and 11 bugs over ~4 months with 9 confirmed/fixed. [Paper](https://arxiv.org/abs/2608.06088) · [Replication package](https://doi.org/10.5281/zenodo.19244624)

### PHYFU — ASE 2023 Distinguished Paper — A
**Route:** P9 Evaluation / Serving Infrastructure  
Foundational physics-simulation-engine reliability infrastructure for robotics and learning-based control. PHYFU combines physics-law consistency oracles for forward/backward simulation, valid initial-state mutation and feedback-guided test scheduling; it reports more than 5,000 error-triggering inputs across four physics simulation engines. It is included as the direct historical anchor for the later IcFuzz lineage, not as generic legacy software testing. [Paper](https://arxiv.org/abs/2307.10818) · [Repo](https://github.com/PhyFuzz/phyfu)

### RoboFuzz — ESEC/FSE 2022 — A
**Route:** P9 Evaluation / Serving Infrastructure  
Foundational ROS2/robot-stack reliability infrastructure: data-type-aware mutation, hybrid real/sim execution, semantic correctness oracles for physical-law/specification/cyber-physical discrepancies, and semantic feedback guidance. Evaluated ROS2 internals plus Turtlesim, MoveIt2+PANDA, TurtleBot3 and PX4; reported **30 previously unknown bugs, 25 acknowledged, 6 fixed**. Included as a direct historical anchor for the modern PHYFU/IcFuzz reliability lineage, not as generic software testing. [Paper](https://2022.esec-fse.org/details/fse-2022-research-papers/86/RoboFuzz-Fuzzing-Robotic-Systems-over-Robot-Operating-System-ROS-for-Finding-Corre) · [Repo](https://github.com/sslab-gatech/robofuzz)

### CaP-X — open robot coding-agent evaluation substrate — A
**Route:** P9 Evaluation / Serving Infrastructure  
Reusable execution/evaluation infrastructure with CaP-Gym interactive environments, CaP-Bench tiers, parallel evaluation workers, auto-launched perception services with GPU allocation, regression tests and real-world Franka bringup. Official MIT repo had **758 stars / 116 forks** on this scan. Included in CORE_SYS for the reusable evaluation substrate, not for its agent-learning methods. [Paper](https://arxiv.org/abs/2603.22435) · [Repo](https://github.com/capgym/cap-x)

## 2026-08-27 — FlashRT agent-guided multimodal deployment runtime
- **FlashRT: Agent Harness for Guiding Agents to Deploy Real-Time Multimodal Applications** — arXiv:2607.18171 — **CORE_SYS / A+**, Routes 2/3/6/7/10/11. Converts a sequential reference backend into an explicit IR and uses an agent plus reusable runtime to build/validate streaming, multi-GPU deployments across CUDA and ROCm. Reports up to 70× lower latency and 3.6× higher throughput across five multimodal applications. [Paper](https://arxiv.org/abs/2607.18171) · [Repo](https://github.com/Infini-AI-Lab/FlashRT). Do not confuse with Execution-State Capsules / FlashRT (2606.20537).
## Added 2026-08-27 13:00 CST
| Title | Year/Venue | Route | System Contribution | Open Source/Repo | Paper | Priority |
|---|---|---|---|---|---|---|
| Lingjing: A Simulation Testbed for Multi-Agent Embodied Tasks in Open-Ended Cities | 2026 / arXiv | 1/2/9 | Multi-engine heterogeneous-agent digital-twin runtime, shared physical/structured state, constrained communication, replayable evaluation | [Repo](https://github.com/seanlxh/Air-Lingjing) | [Paper](https://arxiv.org/abs/2608.08045) | A+ |
| Deployment Is Not Destiny: Robot Recomposition in the Field with Unseen Software, Hardware, and Compute Payloads | 2026 / arXiv | 1/2/4/6/7 | Runtime recomposition, capability discovery/attachment, peer sharing and remote compute payload use | Author/project evidence; dedicated repo not yet verified | [Paper](https://arxiv.org/abs/2608.11063) | A |


## 2026-08-28 03:00 CST — PinSieve
| Title | Year/Venue | Route | System Contribution | Open Source/Repo | Paper | Priority |
|---|---|---|---|---|---|---|
| PinSieve: Production Selective VLM Serving and a Governed Memory Flywheel for Enterprise Content-Quality Triage | 2026 / KDD 2026 | 8/9/11 | Selective VLM cascade/routing, controlled human escalation, feedback provenance, governed refresh, staged promotion & rollback | No dedicated public repo verified | [Paper](https://arxiv.org/abs/2608.24040) · [Pinterest Labs](https://labs.pinterest.com/publications) | A+ |


## 2026-08-28 10:02 CST — always-on streaming multimodal runtime
- **StreamArena / StreamMind** — arXiv:2608.05703 — **A**, Routes 3/5/8/9/11. Independently scheduled frontend workers handle latency-critical interaction and proactive monitoring while asynchronous backend workers build persistent multimodal memory, perform historical recall, and invoke external search. Official project reports 27.5 s weighted query-to-answer latency versus 81.4 s for the same offline backbone (66.2% reduction). Official Apache-2.0 toolkit verified (~15 stars / 1 fork); full StreamMind agent implementation is still marked coming soon. Paper: https://arxiv.org/abs/2608.05703 · Repo: https://github.com/JIA-Lab-research/StreamArena


## 2026-08-28 23:58 CST — TypeGo
- [**TypeGo: An OS Runtime for Embodied Agents**](https://arxiv.org/abs/2607.05482) — **A+**, Routes P2/P3/P7, also listed at **AgenticOS @ SOSP 2026**. TypeGo turns concurrent embodied tasks into processes with PCBs, introduces a Skill Kernel that arbitrates typed physical resources, supports preemption/source-dependent resumption, and runs asynchronous S0–S3 loops from reflexes to semantic task scheduling. Speculative skill streaming overlaps planning with execution. The Unitree Go2 prototype reports 50% lower per-step delay than step-by-step planning and 73% lower TTFA than monolithic planning. No official implementation repo was verified this cycle.
