# CORE_SYS
- [XAIR](https://arxiv.org/abs/2610.27971) — **B+**, reusable execution-time action-intent validation runtime (P2/P3/P9); [Apache-2.0 author artifact/CI](https://github.com/ProSoDiAC/LD1-execution-gap-xair) verified; paper reports 0 stale effects/1,100 and 0/180 OpenPLC; independent reproduction not run, no wired PLC I/O or VLA serving p99.
- [EdgePace](https://arxiv.org/abs/2610.37307) — **A**, bandwidth-aware edge runtime for foreground camera/robot tracking deadlines and LLM output freshness on OnePlus 13/three Jetsons; 24.1–96.1% fewer deadline misses, 64.9–98.5% LLM throughput retained vs unmanaged; dedicated code unverified, no multi-tenant VLA p99.
- [SAKURA](https://arxiv.org/abs/2610.29733) — **A-**, cloud-edge DiT reusable attention-state transfer, bandwidth-adaptive cache-shard compression and pipelined on-device execution; paper-reported 1.82× vs CacheGen and 3.27× vs local, 3.06× storage reduction; adjacent multimodal serving, not a Physical-AI deployment; code unverified.
- [WorldOracle](https://arxiv.org/abs/2610.18826) — **A-**, paired real-robot action-execution benchmark for action-conditioned world models, reproducible evaluation harness; [official code/tests](https://github.com/WorldOracle-benchmark/WorldOracle) verified; no serving p99.
- [AstroBench](https://arxiv.org/abs/2610.31064) — **B+**, Isaac Sim free-floating robotic manipulation benchmark with 9 tasks/29 task-target combinations; [official code/tests](https://github.com/AstroUpLab/AstroBench) verified; not a serving benchmark.
- [TARSphere](https://arxiv.org/abs/2610.30043) — **A-**, 360-episode robot-oriented simulation/runtime and evaluation harness; [official code](https://github.com/xuyicheng-zju/TARSphere) verified; no serving p99.
- [Physical AI for Intralogistics](https://arxiv.org/abs/2610.28432) — **A-**, industrial digital-twin/real-robot benchmark with Jetson Xavier 54ms/5-8Hz, 0.892GB and 38.6% GPU; benchmark release unverified, no multi-tenant serving p99.
- [StreamAhead](https://arxiv.org/abs/2610.25551) — **A+**, adaptive streaming video L1/L2/L3 representation scheduling, shared segment state, CPU-GPU pipeline and query-priority/recovery; 30FPS P95 TTFT<0.5s and 57FPS P95 TTFT<2s on single RTX 6000 Ada; code unverified, not robot-fleet p99.
- [LocoManiLab](https://arxiv.org/abs/2610.30876) — **A-**, 234 humanoid tasks, 12 policies, cross-controller and sim-to-real evaluation testbed; [official project](https://locomanilab.github.io/), no verified executable source or GPU serving p99.
- [UniCache](https://arxiv.org/abs/2609.32831) — **A**, unified multimodal task/type-aware KV cache compression and shared-budget scheduling; up to 1.78× throughput and 5× KV compression for understanding/editing; [Apache-2.0 code](https://github.com/Superone77/UniCache) verified, no multi-tenant p99.
- [Cache-Aware Conv3D Lowering](https://arxiv.org/abs/2609.31938) — **A**, cache-preserving Conv3D-to-Conv2D runtime lowering on Jetson AGX Orin world-model decoder, ~7× VAE decode and >2× full-generation acceleration; no verified code or p99.
- [OmniTide](https://arxiv.org/abs/2609.34653) — **S**, OmniPick/OmniPage logical retention + physical KV compaction for on-device omni streaming; up to 2.40× lower loop latency and 26.7% less physical KV span; no verified official code, not multi-tenant p99.
- [LENS: FPGA Scene Memory for Robots](https://arxiv.org/abs/2610.25068) — **A**, AMD KR260 INT16 localization and 3DGS scene-memory rendering, board-measured 25.42ms localization and 1.9–5.7× perf/W vs Jetson Orin NX; no verified code or VLA serving p99.
- [RT-SAFE](https://arxiv.org/abs/2610.09294) — **A**, time-advancing urban embodied-agent safety benchmark; 12.3× more collisions in real-time than static evaluation despite comparable task success; [official code](https://github.com/XTRose29/RT-SAFE) verified, simulation not serving p99.
- [Multimodal Remote Inference](https://arxiv.org/abs/2508.07555) — **A-**, AoI-aware multi-sensor remote feature scheduling, SMDP and switching/index policies; robot-state/hand-pose trace/numerical evaluation, no deployed p99 or verified code.
- [OxyGen: Unified KV Cache Management for VLA Inference under Multi-Task Parallelism](https://arxiv.org/abs/2603.14371) — **S**, cross-task KV reuse + frame-budgeted continuous batching, RTX4090 >200 tokens/s language + 70Hz action; Jetson Thor humanoid validation; [Apache-2.0 source](https://github.com/air-embodied-brain/OxyGen) verified. Up to 3.7× author-reported speedup vs isolated execution, not cloud p99.
- [WAMJET: A Harness for World Action Model Acceleration](https://arxiv.org/abs/2610.03797) — **A**, 6 WAMs/3 coding agents/2 GPU architectures, reusable bottleneck profiling, acceleration and validation; [BSD-3 code](https://github.com/liulixinkerry/WAMJET) verified. Up to 9.95× author-reported lossless speedup vs upstream, not online serving p99.
- [MAGMA-Bench: Evaluating Long-Horizon Embodied Agents](https://arxiv.org/abs/2610.13534) — **A-**, reusable multi-robot dynamic-task/failure/interrupt evaluation and skill-level interface; [BSD-2 code/tests](https://github.com/MAGMA-rob/magma-bench) verified. Benchmark, not online GPU serving.
- [BT-Agent: Deploying Onboard Robot Agents with Behavior Trees](https://arxiv.org/abs/2610.13862) — **A-**, Jetson Thor + 9B fully onboard runtime with reactive behavior-tree skill supervisor and local interrupt guards; 161-task benchmark, 10.9× text-vs-simulation evaluation throughput. No fleet-serving/p99 inference claim.
- [Embodied Skill Bench](https://arxiv.org/abs/2610.16238) — **A-**, reproducible 250-skill closed-loop evaluation substrate (success/actions/tokens/wall-clock); [public source/tests](https://github.com/HanZhi306/EmbodiedSkill-Bench) verified. Agent-directed reuse reports 14.1% token and 11.9% wall-clock reduction in tested setting; not GPU throughput.
- [vLLM-Omni Technical Report](https://arxiv.org/abs/2610.09307) — **S**, 34p official report: unified omni multi-stage orchestrator, specialized stage engines/replica pools, connector payload transfer, session-aware streaming/duplex/world-model/robot workloads; [open-source runtime](https://github.com/vllm-project/vllm-omni). Distinct from arXiv:2602.02204; no demonstrated robot-fleet p99.
- [GPU-resident Execution](https://arxiv.org/abs/2610.13809) — **A**, NVIDIA Holoscan GPU-driven I/O + persistent CUDA Graph sensor runtime; real 1080p 60Hz camera jitter 4.83→0.66ms (7.3×), software jitter 1.70→0.01ms; 15p official PDF. Dedicated code not independently verified; not VLA fleet p99.
- [HeteroVDiff](https://arxiv.org/abs/2610.16244) — **A**, Galaxy S25 NPU/GPU shared-INT8-weight video diffusion pipeline; 49-frame 1.35× stream throughput (677 vs 917s/clip), 5.3 vs 3.9 videos/hour within deadline; dedicated code unverified, not robot serving.
- [Isaac-Net](https://arxiv.org/abs/2610.02370) — **A-**, GPU-batched 5G network-in-the-loop multi-robot evaluation; Isaac Lab 1,048,576 robots at 1.24 steps/s vs 1.50 without network, [BSD-3 repo](https://github.com/ZzZTripleZzZ/isaac-net); training/evaluation infrastructure, not production serving.
- [CARE](https://arxiv.org/abs/2610.30587) — **A-**, critic-guided cloud/local embodied execution authority transfer with shared handoff memory; median time-between-action −28.8–82.6% paper-reported; decision-layer only, no network/control p99 or verified code.
- [FastHarness](https://arxiv.org/abs/2610.31427) — **A-**, reusable memory-guided VLA reviewer scheduler and recovery harness; 57.2% fewer reviewer tokens, episode time 85.5→52.0 min on **four simulated tasks**; [MIT code](https://github.com/FastHarness/fast-harness), no real robot/p99 SLO.
- [Beyond LLM Serving](https://arxiv.org/abs/2610.05062) — ASPLOS 2027 system-level VLA workload characterization across four VLA families and RTX 4090 / Jetson Thor / Jetson AGX Orin; stage/roofline/DVFS profiling plus 43,200 closed-loop episodes expose batch-1 control-deadline and SLO-aware accuracy-speed-energy tradeoffs.
- [EAServe](https://arxiv.org/abs/2609.31551) — encode-aware disaggregated multimodal serving: load-adaptive micro-batching, partial local-prefill offload, dynamic SM partitioning, and joint resource/configuration search; up to 4.3x vs Dynamo and 1.7x vs vLLM SLO-goodput.

Primary contribution must be runtime, serving, resource management, scheduling, deployment, cache/state infrastructure, heterogeneous execution, profiling, or evaluation infrastructure.

## Multimodal / diffusion co-serving
- [HADIS](https://arxiv.org/abs/2509.00642) — **A**, EuroSys 2027 *conditionally accepted* (author artifact): text-to-image diffusion hybrid router/discriminator cascade, online MILP joint model-pair/threshold/GPU allocation; paper-reported 16-GPU traces, up to 35% quality improvement and 2.7–45× fewer SLO violations; [MIT code artifact v0.3.0-ae](https://github.com/qizhengyang98/HADIS) public, not independently reproduced; no robot/VLA control-loop p99.
- [GENSERVE](https://arxiv.org/abs/2604.04335) — **A+**; real 8×RTX PRO 6000 Blackwell T2I/T2V shared-GPU serving with diffusion-step video preemption, elastic sequence parallelism, dynamic batching and SLO-aware scheduling. Up to **44% relative** SLO-attainment improvement reported. Synthetic arrivals using real prompts; dedicated code unverified; not robot-control p99.

- [CusADi2](https://arxiv.org/abs/2610.25476) — **A-**, reusable DAG/warp-scheduled GPU robot kinematics/Jacobians/Hessians library; RTX 4080, 67 robots, <40us common platforms at B=256, 50Hz Franka planner demo; [MIT code](https://github.com/johnviljoen/cusadi2). Not VLA model serving or p99 fleet SLO.
- [DDiT](https://arxiv.org/abs/2506.13497) — **A**, T2V T5/DiT/VAE stage-aware GPU resource allocation, adaptive parallelism and step-granular scheduling; up to 1.44x p99 / 1.43x mean latency paper-reported; includes emulated 8-server scaling, author code unverified.
- [xDiT](https://arxiv.org/abs/2411.01738) — **A+**, reusable hybrid SP/PipeFusion/CFG parallel DiT inference across real L40 Ethernet and A100 NVLink GPU clusters; [Apache-2.0 code](https://github.com/xdit-project/xDiT) (2743 stars at 13h). Not VLA serving.
## Physical-AI serving trunk
- [KerColle](https://arxiv.org/abs/2609.22335) — PACT '26 (DOI [10.1145/3838684.3846872](https://doi.org/10.1145/3838684.3846872)); online GPU CTA/SM-resource-aware VLM/action-head co-scheduling across VLA requests; up to **28% simulated** throughput gain (**20.5% average**) on RTX 4090/5090-configured Accel-Sim/NVBit traces; **A-**, no author-linked implementation or real-GPU/robot p99 verified.
- [GGraph](https://arxiv.org/abs/2610.28953) — reusable GPU-resident graph/ROS2 robot runtime for real deployment and batched multi-robot learning; ms graph updates, ~10x training wall-time benefit reported; **A-**, dedicated author repo not independently resolved; not VLA serving p99.
- [HarnessPAI](https://arxiv.org/abs/2609.29166) — model-/embodiment-agnostic executable Physical-AI runtime: compiled task programs avoid online high-level LLM calls, across-rollout code evolution and reusable skill memory; **A** · [MIT code](https://github.com/Darwin-Agent/HarnessPAI) · no multi-tenant serving or p99 SLO verified.
- [FATS / Learning from Fleet Experience](https://arxiv.org/abs/2610.25736) — **96 real robots**, SwarmLink shared cloud-inference/trajectory data plane and HotSwarm fault-tolerant control plane; 9,834 episodes, 1.3% fleet-time incident downtime. **A** · fleet learning–serving co-system; no verified dedicated code or serving tail-latency SLO.
- [Industrial ReMEmbR](https://arxiv.org/abs/2610.28624) — fleet-shared spatiotemporal memory; Jetson edge vision encoding + cached vision-token reuse + on-prem on-demand decoder and GPU-indexed retrieval; 100-robot savings are **modeled**, not deployment measured — **A+** · industrial extension code unverified
- [Kairos](https://arxiv.org/abs/2605.11381) — multi-robot generate–execute-aware serving — **S+**
- [ROSA](https://arxiv.org/abs/2607.01088) — robot-factory shared GPU serving — **S+**
- [Robion](https://arxiv.org/abs/2609.12075) — SLO-aware multi-robot/multi-model VLA serving on multi-GPU edge servers; intra-GPU VLM/ADiT overlap, SM partitioning, co-location, placement and traffic assignment — **S+**
- [PhyAI](https://arxiv.org/abs/2608.03682) — unified onboard/edge/cloud/rollout engine — **S+**
- [M*](https://arxiv.org/abs/2606.12688) — modular composite-model serving — **S+**
- [VLA-Perf](https://arxiv.org/abs/2602.18397) — deployment/performance map — **S**
- [Embodied.cpp](https://arxiv.org/abs/2607.02501) — portable embodied runtime — **S**
- [vla.cpp](https://arxiv.org/abs/2606.08094) — portable C++ VLA runtime — **S**
- [Characterizing VLA Models across XPUs](https://arxiv.org/abs/2604.24447) — heterogeneous phase characterization — **S**
- [FluxVLA Engine](https://arxiv.org/abs/2609.17210) — configuration-driven VLA/WAM engineering and deployment platform; standardized interfaces, RTC, optimized inference and remote GPU serving — **A**
- [Goal-Oriented Communications for Physical AI](https://arxiv.org/abs/2609.15895) — closed-loop 5G/edge Physical-AI testbed with semantic transport, LM inference, digital-twin validation and robot control — **A**
- [HoliBench](https://arxiv.org/abs/2609.12412) — open cross-platform foundation-model deployment/evaluation toolkit for heterogeneous CPS/IoT devices and multi-model pipelines — **A**
- [Armory](https://arxiv.org/abs/2608.00337) — control-aware batched robot-policy serving — **A+**
- [Retriever](https://arxiv.org/abs/2607.17213) — temporal computation-graph runtime for multi-rate closed-loop robot programs (`Flow` / `Clock` / `Sync`, replay/debugging, multi-backend execution) — **A+** · [project](https://retriever.systems/) · [repo](https://github.com/openretriever/retriever)
- [Physical Agentic AI](https://arxiv.org/abs/2608.22657) — heterogeneous robot-crew orchestration with typed skills/workflow contracts and deterministic per-dispatch execution authorization; separates LLM planner knowledge from physical actuation authority — **A**
- [LeRobot](https://arxiv.org/abs/2602.22818) — ICLR 2026 end-to-end robot-learning infrastructure; generalized gRPC PolicyServer/RobotClient async inference with action-queue/overlap semantics — **A+** · [repo](https://github.com/huggingface/lerobot)
- [RobotFleet](https://arxiv.org/abs/2510.10379) — RSS 2025 Multi-Robot Systems Workshop; centralized fleet planner/allocator + task-status/schedule manager over containerized robot services, with shared world state and feedback-driven replanning — **A-** · [repo](https://github.com/therohangupta/robot-fleet)

## Edge / cloud / heterogeneous deployment
- [Offload or Overload](https://arxiv.org/abs/2603.18284) — measurement study of mobile-manipulation inference across onboard, edge, and cloud GPUs; quantifies latency/accuracy, battery, bandwidth, fleet batching/multiplexing, and GPU/network contention, motivating QoS-aware offload and fleet serving — **A+** · [Microsoft Research](https://www.microsoft.com/en-us/research/publication/offload-or-overload-a-platform-measurement-study-of-mobile-robotic-manipulation-workloads/)
- [GLASS](https://arxiv.org/abs/2609.28179) — reusable device-side CUDA linear-algebra/geometry infrastructure for edge robotics; architecture-tuned thread/warp/block/backend placement, compile-time dispatch, independent numerical validation, and up to 1.5× embedded-system runtime improvement — **A** · [repo](https://github.com/A2R-Lab/GLASS)
- [RoboECC](https://arxiv.org/abs/2603.20711) — model/hardware/network-aware edge-cloud partitioning — **A+**
- [RAPID](https://arxiv.org/abs/2603.07949) — physical-state-triggered edge/cloud offload — **A**
- [EcoVLA (device-edge)](https://arxiv.org/abs/2608.15502) — stage-level energy-aware co-inference — **A+**
- [FogROS 2](https://arxiv.org/abs/2205.09778) — cloud/fog ROS2 deployment substrate — **A+** · [repo](https://github.com/BerkeleyAutomation/FogROS2)
- [FogROS2-Config](https://arxiv.org/abs/2311.05600) — cloud server/configuration selection — **A**
- [FogROS2-PLR](https://arxiv.org/abs/2410.05562) — probabilistic latency/reliability management — **A+**

## Real-time runtime / resource management
- [RETNAS / HRT+SRT Scheduling](https://arxiv.org/abs/2610.29503) — policy-agnostic certified mixed-deadline DNN DAG scheduling and heterogeneous accelerator placement with deterministic HRT fallback; 81.41% **simulated** SRT deadline hit rate at high load. **A-** · P3/P6/P9; [official simulator](https://github.com/BlancoFrancescoGiulio/retnas), no real-robot/hardware SLO.
- [PAAM](https://arxiv.org/abs/2404.06452) — shared accelerator server and priority arbitration — **A+** · [repo](https://github.com/rtenlab/reference-system-paam)
- **CROS-RT** — cross-layer ROS2 priority propagation — **A+**
- **ROSGM** — pluggable real-time GPU management for ROS2 — **A**
- **GCAPS** — driver-level GPU context preemption — **A**
- **LaME** — adaptive latency/resource management executor — **A+**

## State / cache / world sessions
- [rMuscle](https://arxiv.org/abs/2609.19104) — dual-stage cross-execution VLA inference cache (Context/Action), RTX 4090 + Jetson Thor end-to-end 1.20–1.42x over FlashRT; 92 tasks incl. two real-robot tasks. **A** · Routes 3/5/6/8; dedicated code and serving p99 SLO unverified.
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
- [OrbitWeaver](https://arxiv.org/abs/2610.29183) — phase-aware checkpointing and dependency-aware VLM recovery under edge-device shutdowns; 72h on two satellites, up to 4.07x end-to-end / 3.56x fewer SSD writes **(paper reported)**. **A** · multimodal M4/M6, transferable P5/P6/P9; dedicated code and serving p99 unverified.
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

## 2026-08-29 01:02 CST — TimelyLLM
- [**TimelyLLM: Time-sensitive LLM Serving System for Physical-I/O Limited Agents**](https://arxiv.org/abs/2412.18695) — **ACM MobiSys 2026 Best Paper Runner-up + Best Artifact Runner-up**, **A+**, Routes P1/P3/P8. TimelyLLM serves multiple robotic agents using segmented generation and timing-aware scheduling that overlap future plan generation with current physical execution instead of FCFS batching. The paper reports up to **1.97× higher time utility** and **84% lower overall waiting time**. Recovered as a historical omission during the TypeFly→TimelyLLM→TypeGo lineage census.

## 2026-09-03 11:00 CST — OmniEvaluator
| Title | Year/Venue | Route | System Contribution | Open Source/Repo | Paper | Priority |
|---|---|---|---|---|---|---|
| OmniEvaluator: A Composable Evaluation System for Reproducible Omni-Modal Foundation Model Evaluation | 2026 / arXiv | 9/11 | Unified inference↔evaluation schema, provenance-rich artifacts/dashboard, federated shared inference servers and continuous-batching reuse | [Repo](https://github.com/naver-ai/omni-evaluator) | [Paper](https://arxiv.org/abs/2609.01315) | A+ |

The paper reports **1.3×–2.8× wall-time speedup** for federated evaluation under the same GPU allocation. CORE_SYS because the contribution is reusable evaluation/serving infrastructure rather than an omni-model algorithm.


## 2026-09-24 18:00 CST — continuous-vision pipeline
- [**MVP: A Motion-Predictive Speculative Vision Pipeline with Non-Blocking Drift Correction**](https://arxiv.org/abs/2609.27706) — **MICRO 2026 / CORE_SYS A+**, Routes 3/6/8. Motion-domain speculative perception plus a lightweight ISP extension and non-blocking periodic drift-correction scheduling. Reports up to **66.8% tail-latency reduction** and **46% energy savings** for object detection.
