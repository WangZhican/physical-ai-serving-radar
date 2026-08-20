# Research Map

The radar uses ten primary Physical-AI systems routes. A paper may appear in multiple routes when it plays a distinct technical role in each.

## 1. Fleet-scale / Multi-Robot Serving
Multi-tenant robot-policy serving, shared GPU pools, action-aware batching, admission/fairness and execution-aware scheduling. **Anchors:** Kairos, ROSA, Armory.

## 2. Unified Physical-AI Runtime
Common runtime contracts for VLA/WAM/policy execution, portable kernels, memory management, action-head plugins and robot-facing protocols. **Anchors:** PhyAI, Embodied.cpp, vla.cpp.

## 3. Real-Time / Streaming / Control-loop Serving
Reaction latency, deadlines, async perception/inference/execution, executor scheduling, accelerator arbitration and physical-state-aware timing. **Anchors:** CROS-RT, PAAM, ROSGM, LaME, F1Tenth mixed-criticality scheduling.

## 4. Edge-Cloud / Disaggregated Physical AI
Device/edge/cloud partitioning, fog/cloud provisioning, server selection, network adaptation and tail-latency reliability. The recovered systems lineage is **FogROS 2 → FogROS2-Config → FogROS2-PLR**, complementing modern VLA-specific RoboECC, RAPID and EcoVLA.

## 5. Physical-State / Temporal Cache and State Reuse
Beyond KV cache: vision features, planner transitions, action intermediates, world state, rollout state and session checkpoints. **Anchors:** AgenticCache, Persistent Computational State, WorldMove.

## 6. Hardware-Aware / Heterogeneous Serving
GPU/XPU/NPU placement, phase asymmetry, CPU–GPU partitioning, memory swapping and shared accelerator management. **Anchors:** Characterizing VLA across XPUs, PAAM, GCAPS, OOM-Free Alpamayo.

## 7. Composite VLA + WAM + Planner Serving
Graph/walk abstractions for perception → reasoner → planner → policy → WAM → verifier/safety, including shared intermediate state and per-component SLOs. **Anchors:** M*, PhyAI, vLLM-Omni.

## 8. Workload Characterization / Performance Modeling
Model/hardware/network landscapes, control-time rooflines, wireless discovery/transport behavior and deployment cost-energy-time modeling. **Anchors:** VLA-Perf, PhyAI, Discovery Storm.

## 9. Evaluation / Serving Infrastructure
Model-server/benchmark decoupling, real-robot evaluation-as-a-service, distributed evaluation, traces, observability and deadline/latency instrumentation. **Anchors:** DeepInsight, RoboArena, AutoEval, RoboDojo, ros2probe, CARET, TILDE.

## 10. World-Model / WAM Rollout Serving
Branching/iterative rollouts, persistent sessions, checkpoint/restore, exact-state migration, rollout-state reuse and VLA/WAM co-scheduling. **Anchors:** Persistent Computational State, WorldMove, PhyAI.

## Adjacent Multimodal / MLLM / Omni Systems
vLLM-Omni, M*, Eevee, TriInfer, Cornserve/Cornfigurator, Omni-Flow, LiveServe, HeteroServe, StreamWise, HorizonServe, SpaceServe, ModServe, OnePiece, TCM-Serve and related systems are retained when their graph/stage/disaggregation/cache abstractions transfer directly to Physical AI.
