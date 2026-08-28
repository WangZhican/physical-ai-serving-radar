# Physical AI Serving — Research Map

A paper may appear in multiple routes when it plays a distinct technical role in each. This map is the **Physical AI-specific** taxonomy; Multimodal / Omni serving has its own independent map.

## P1. Fleet-scale / Multi-Robot Serving
Multi-tenant robot-policy serving, shared GPU pools, action-aware batching, admission/fairness and execution-aware scheduling, plus fleet-to-cloud actor/learner loops that continuously turn deployment experience into shared policy updates. **Anchors:** Kairos, ROSA, Armory, SOP. LWD is tracked as an algorithm-system follow-on because its main novelty is offline-to-online RL rather than serving/resource scheduling.

## P2. Unified Physical-AI Runtime
Common runtime contracts for VLA/WAM/policy execution, portable kernels, memory management, action-head plugins and robot-facing protocols. **Anchors:** PhyAI, Embodied.cpp, vla.cpp, LeRobot.

## P3. Real-Time / Streaming / Control-loop Serving
Reaction latency, deadlines, async perception/inference/execution, executor scheduling, accelerator arbitration and physical-state-aware timing. **Anchors:** LeRobot async inference, CROS-RT, PAAM, ROSGM, LaME, VLASH, FASTER, Reflex.

## P4. Edge-Cloud / Disaggregated Physical AI
Device/edge/cloud partitioning, fog/cloud provisioning, server selection, network adaptation and tail-latency reliability. The recovered systems lineage is **FogROS 2 → FogROS2-Config → FogROS2-PLR**, complementing modern VLA-specific RoboECC, RAPID and device-edge EcoVLA.

## P5. Physical-State / Temporal Cache and State Reuse
Beyond KV cache: vision features, planner transitions, action intermediates, recurrent/convolution/MTP state, world state, rollout state and session checkpoints. **Anchors:** AgenticCache, Persistent Computational State, WorldMove, Execution-State Capsules / FlashRT. **Boundary signal:** Hi-WM shows cached world-model states with rollback/branching as a reusable failure-state substrate, but remains method-first rather than a general serving runtime. ActionCache remains an algorithmic inspiration rather than a general cache system.

## P6. Hardware-Aware / Heterogeneous Serving
GPU/XPU/NPU placement, phase asymmetry, CPU–GPU partitioning, memory swapping and shared accelerator management. **Anchors:** Characterizing VLA across XPUs, PAAM, GCAPS, OOM-Free Alpamayo, Hybrid Block-Layer VLA inference.

## P7. Composite VLA + WAM + Planner Serving
Graph/walk abstractions for perception → reasoner → planner → policy → WAM → verifier/safety, including shared intermediate state and per-component SLOs. **Anchors:** M*, PhyAI, vLLM-Omni, ROSA.

## P8. Workload Characterization / Performance Modeling
Model/hardware/network landscapes, control-time rooflines, wireless discovery/transport behavior and deployment cost-energy-time modeling. **Anchors:** VLA-Perf, PhyAI, Discovery Storm.

## P9. Evaluation / Serving Infrastructure
Model-server/benchmark decoupling, real-robot evaluation-as-a-service, distributed evaluation, traces, observability, distributional real-hardware metrics and deadline/latency instrumentation. **Anchors:** DeepInsight, RoboArena, AutoEval, RoboDojo, vla-eval, ros2probe, CARET, TILDE, PhAIL. **Boundary:** dWorldEval adds scalable world-model proxy evaluation with automatic progress scoring, but remains method-first rather than a serving/resource system.

## P10. World-Model / WAM Rollout Serving
Branching/iterative rollouts, persistent sessions, checkpoint/restore, exact-state migration, rollout-state reuse, evaluation proxies and reusable rollback/branching substrates. **Anchors:** Persistent Computational State, WorldMove, PhyAI. **Boundary signals:** dWorldEval and Hi-WM.

## Important refinements

### Service-oriented multi-tenant VLA runtime
Resident shared base models + tenant-private action/training state + separate training/inference queues + environment sessions + group batching + fault isolation + elastic rollouts. **Anchor:** JoyNexus.

### Cloud-native embodied simulation as serving infrastructure
Route P9 includes cloud-native simulation platforms only when they contribute schedulable compute pools, containerized multi-task execution, standardized model/task interfaces, reproducible evaluation/data governance, and closed-loop replay/regeneration. Pure simulator or embodied-learning algorithms remain outside `CORE_SYS`.

### Distributed VLA RL as Physical-AI runtime infrastructure
P2/P6/P7/P9 include distributed VLA RL systems when the contribution is runtime/resource infrastructure across simulator interaction, inference rollout, actor training, dynamic batching, environment sharding, communication, or multi-GPU scaling. Pure RL algorithm improvements remain outside `CORE_SYS`. RLinf-VLA and D-VLA are important anchors.

### Robots as first-class resources
RLinf-USER extends the map from GPU/server resource management into physical-resource management: heterogeneous robots are discovered, scheduled and coordinated alongside GPUs, while cloud-edge data channels, weight synchronization and persistent state are managed by one runtime substrate.

### Real-time multi-robot control runtime
P2/P3/P9 explicitly include reusable real-time robot-control middleware/runtime, not only model-serving layers. `multipanda_ros2` is a representative anchor: single-process multi-arm ROS2 execution, 1 kHz control, fast controller switching, runtime recovery and matched sim/real interfaces.

## Boundary with Multimodal / Omni Serving

General MLLM/Omni systems are **not placed here merely because their mechanisms are transferable**. They live in [`MULTIMODAL_MAP.md`](MULTIMODAL_MAP.md). Cross-track works are explained in [`CROSSOVER.md`](CROSSOVER.md).

### 2026-08-27 Route-9 refinement
Evaluation infrastructure explicitly includes **robot coding-agent evaluation/execution substrate**: interactive execution environments, parallel workers, perception-service orchestration, regression harnesses and real-robot bringup. CaP-X is the anchor; skill/harness optimization remains boundary work absent a general runtime/resource plane.

### Latent freshness at the edge
A new P4/P5/P8 boundary subline tracks whether remotely maintained semantic/latent state is fresh enough for downstream physical decisions, including temporal integration-window selection and communication/encoding resource control. [Age-of-Latent (2608.09411)](https://arxiv.org/abs/2608.09411) is the current boundary anchor; it is not classified CORE_SYS without a reusable runtime implementation.
