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
## 2026-08-21 omission recovery
- [**JoyNexus**](https://arxiv.org/abs/2607.16074) — service-oriented **multi-tenant VLA** post-training/inference/evaluation substrate with tenant-scoped state, Training/Inference/Environment Services, separate global queues, group batching, fault isolation and elastic rollout scaling — **A+**, Routes 2/7/9.
- [**FlashCodec + UnifiedServe**](https://arxiv.org/abs/2512.17574) — multi-stage MLLM serving with collaborative multi-GPU/NVDEC preprocessing and logical stage disaggregation over physically shared GPU resources — **A+**, Routes 6/11.


## Cloud-native embodied simulation / evaluation infrastructure
- [**Cloud-Native Simulation Infrastructure for Embodied Intelligence**](https://arxiv.org/abs/2606.27962) — elastic resource scheduling, containerized simulation, standardized model/task/evaluation interfaces, trajectory/data governance, and failure-driven closed-loop regeneration — **A-**, Routes 7/9. Early-stage infrastructure white paper; no verified public implementation repo yet.
