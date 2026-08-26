# SYS_ALG_BOUNDARY

Works whose algorithmic novelty remains central, but which expose substantial runtime/deployment primitives.

- [Jetson-PI](https://arxiv.org/abs/2607.12659) — onboard asynchronous VLA runtime + confidence scheduling.
- [VLASH](https://arxiv.org/abs/2512.01031) — future-state-aware asynchronous inference.
- [Reflex](https://arxiv.org/abs/2607.14695) — streaming inference and incremental cache updates.
- [FASTER](https://arxiv.org/abs/2603.19199) — reaction-latency/TTFA framing and streaming dispatch.
- [SpecVLA](https://arxiv.org/abs/2608.15636) — speculative VLA algorithm/architecture co-design.
- [FlashDrive](https://arxiv.org/abs/2608.12932) — streaming KV reuse, speculative reasoning and CUDA-graph/kernel fusion.
- [World Action Models in Real Time](https://arxiv.org/abs/2608.01880) — asynchronous WAM deployment strategies.
- [AsyncVLA](https://arxiv.org/abs/2602.13476) — remote semantic model plus onboard reactive adapter.
- [CloudEdgeVLA](https://arxiv.org/abs/2608.00569) — stale-cloud/fresh-edge correction under network delay.
- [ActFovea](https://arxiv.org/abs/2607.29169) — runtime safeguarding, observation freshness and bounded recovery.
- [CheckVLA](https://arxiv.org/abs/2607.26789) — execution-time world-model verification of action chunks.
- [Pre-VLA](https://arxiv.org/abs/2605.22446) — pre-execution verification and budget-aware resampling.
- [SV-VLA](https://arxiv.org/abs/2604.02965) — low-frequency planning plus frequent lightweight closed-loop verification.

These are not promoted to `CORE_SYS` merely because they reduce latency: the system abstraction must become the primary contribution for that promotion.

### HELP (2026) — Human-efficient fleet post-training pipeline
- **Paper:** https://arxiv.org/abs/2607.09776
- **Routes:** fleet-scale infrastructure (1), evaluation/post-training infrastructure (9)
- **Role:** two specialized operators supervise 12 robots; centralized training/inference services plus automatic rollout segmentation/data curation. Kept at SYS_ALG_BOUNDARY because the central novelty is workflow/human efficiency, not serving resource management.

### Learning while Deploying (LWD) — fleet-scale continual policy improvement
- **Paper:** https://arxiv.org/abs/2605.00416
- **Project:** https://finch.agibot.com/research/lwd
- **Routes:** 1 / 7 / 9 · **Priority:** A
- **Role:** real fleet deployment infrastructure over 16 dual-arm robots, shared replay aggregation and periodic shared-policy refresh; reaches 95% average success across eight real-world tasks. Kept at `SYS_ALG_BOUNDARY` because the central novelty is offline-to-online RL (DIVL + QAM), not serving/resource scheduling.

### Sirius-Fleet — deployment-time fleet monitoring and continual improvement
- **Paper:** https://arxiv.org/abs/2410.22689
- **Official proceedings:** https://proceedings.mlr.press/v270/liu25g.html
- **Project:** https://ut-austin-rpl.github.io/sirius-fleet/
- **Code:** https://github.com/UT-Austin-RPL/sirius-fleet
- **Routes:** 1 / 7 / 9 / 10 · **Priority:** A
- **Role:** multi-task fleet deployment with runtime anomaly monitoring, visual-world-model prediction, selective human intervention and continual policy/monitor updates. Kept at `SYS_ALG_BOUNDARY` because interactive monitoring/learning is the main novelty rather than serving admission, resource management or scheduler design.

### dWorldEval — scalable world-model policy evaluation
- **Paper:** https://arxiv.org/abs/2604.22152
- **Project:** https://dworldeval.github.io/
- **Venue:** ICML 2026 Spotlight · **Routes:** 9 / 10 · **Priority:** A+
- **Role:** action-centric discrete-diffusion world model with sparse keyframe memory and automatic progress scoring used as a scalable policy-evaluation proxy. Important evaluation-serving workload, but method-first rather than a scheduler/resource runtime.

### Hi-WM — cached rollback/branching world-state substrate
- **Paper:** https://arxiv.org/abs/2604.21741
- **Project:** https://hi-wm.github.io/
- **Routes:** 5 / 9 / 10 · **Priority:** A
- **Role:** caches intermediate world-model states and supports rollback/branching so one failure state can seed multiple corrective continuations. Strong state-reuse/fork-backtrack signal, but the primary contribution is corrective post-training rather than an independent serving system.

### ROBOGATE — deployment validation with correction-aware evidence
- **Paper:** https://arxiv.org/abs/2603.22126
- **Official status/correction:** https://www.robogate.io/paper
- **Route:** 9 · **Priority:** A-
- **Role:** physics-based deployment-validation framework using large-scale failure-boundary sampling and deployment-gate semantics. The retained scripted-controller study reports 50K+ Isaac Sim experiments across four robot embodiments and risk-model AUC 0.780 vs 0.754 for Stage 1 alone.
- **Integrity note:** the publisher's 2026-07-18 correction retracts and quarantines the learned-policy/VLA comparison and cross-simulator capability/safety interpretation because harness paths were non-equivalent and the success predicate was insufficient. Those historical VLA numbers are not current evidence. The historical code link currently returns 404 from public fetch, so current repo adoption is not claimed.

### Relax — asynchronous omni-modal post-training runtime
- **Paper:** https://arxiv.org/abs/2604.11554
- **Code:** https://github.com/redai-infra/Relax
- **Routes:** 7 / 11 · **Priority:** A+
- **Role:** omni-native, service-oriented post-training runtime with fault-isolated RL roles, TransferQueue data bus, staleness-controlled async execution, and Qwen3-Omni image/audio/video validation. It reports 1.20× over veRL on Qwen3-4B on-policy training, 1.76× fully-async over colocate on Qwen3-4B, and 2.00× on Qwen3-Omni-30B. Kept at `SYS_ALG_BOUNDARY` because the primary workload is post-training rather than online inference serving, despite substantial reusable rollout/runtime infrastructure.

### WCM — asynchronous embodied-agent runtime
- **Paper:** https://arxiv.org/abs/2607.22999
- **Venue:** RSS 2026 Workshop on Human-centric Mobile Manipulation · **Routes:** 2 / 3 / 5 / 7 · **Priority:** A
- **Role:** SLAK separates sensing, logic, action and knowledge; its asynchronous runtime lets reasoning, dialogue, state updates and physical execution proceed concurrently and revalidates current context before stale actions are committed. Real-robot evaluation reports 73.8% average success over nine HRI tasks. Kept at `SYS_ALG_BOUNDARY` because the primary novelty is embodied-agent/HRI architecture and teaching, not serving/resource scheduling.

### Decoding Task Progress from VLA Representations — deploy-time VLA observability
- **Paper:** https://arxiv.org/abs/2608.13474
- **Routes:** 3 / 8 / 9 · **Priority:** A-
- **Role:** reads task-progress from pi0.5 residual-stream activations with a lightweight linear probe and uses it as a label-free stalled-progress/OOD detector. It directly supports deployed-policy instrumentation, failure detection and runtime observability, but remains `SYS_ALG_BOUNDARY` because it does not introduce a serving scheduler, resource manager or reusable monitoring runtime substrate.

### Edge-Native Embodied Intelligence — action-aware wireless edge / Physical-AI co-design
- **Paper:** https://arxiv.org/abs/2608.17774
- **Routes:** 4 / 6 / 8 · **Priority:** A-
- **Role:** connects embodied agents, 6G networking and edge cognitive services via confidence-aware edge assistance, edge-driven adaptation, value-of-experience active embodied federated learning, goal-oriented transmission and programmable radio-resource allocation. Kept below `CORE_SYS` because current evidence is a framework + case-study co-design rather than a mature serving/runtime substrate.

### Rollplex — cross-phase GPU spatial sharing for VLM post-training
- **Paper:** https://arxiv.org/abs/2608.14498
- **Code/runtime:** https://github.com/alibaba/ROLL
- **Routes:** 6 / 8 / 11 · **Priority:** A+
- **Role:** decomposes reference/training at the response boundary and overlaps response-independent visual/prompt prefix work with rollout decode; CUDA-VMM-backed phase-aware HBM residency controls boundary/intermediate state, while TP-layout-aware physical weight sharing avoids a second full actor copy. On 32xH800 it reports 1.23x-1.30x over serial colocation and 1.57x-2.24x over disaggregation. Kept `SYS_ALG_BOUNDARY` because the workload is VLM RL post-training rather than online serving.

### PonderPounce — asynchronous episode-context MLLM + fast VLA control
- **Paper:** https://arxiv.org/abs/2608.24115
- **Project:** https://worv-ai.github.io/ponderpounce/
- **Code:** https://github.com/worv-ai/PonderPounce
- **Routes:** 3 / 5 / 7 · **Priority:** A
- **Role:** a slow pretrained MLLM keeps episode history and asynchronously refreshes a continuous cognition token; the fast VLA consumes only the newest token plus its age/freshness signal. The optimized serving path reports p50 78 ms cognition refresh and 25 ms action invocation, supporting 20 Hz action playback. Kept `SYS_ALG_BOUNDARY` because the main novelty is model/interface design, but the async refresh contract directly informs control-loop freshness, temporal state serving, and composite MLLM+VLA orchestration.

### AgenticRobotics — durable robot-policy improvement control plane
- **Paper:** https://arxiv.org/abs/2608.07555
- **Routes:** 2 / 9 · **Priority:** A
- **Role:** backend-independent outer-loop control plane with durable Bind→Analyze→Act→Measure→Score→Commit transactions, commit-keyed crash recovery, append-only evidence, artifact-bound capability quality and a recorded MCP tool surface. Hardened evidence gating reports 0.001 false promotions/run versus 0.005–0.021 for shipped baselines, while kill injection reports zero lost/duplicate effects. Kept at `SYS_ALG_BOUNDARY` because the reference implementation provides control-plane/evaluation utilities rather than a complete online serving or training scheduler.

### DreamLedger — execution-settled world-model trust/state layer
- **Paper:** https://arxiv.org/abs/2608.23863
- **Routes:** 5 / 9 / 10 · **Priority:** A
- **Role:** turns consumed world-model predictions into persistent condition×region×horizon credit records, settles them against later execution evidence, attaches dependency tickets/replay logs, and gates whether the robot should rely on imagination, shorten the horizon or observe again. Across DreamerV3, TD-MPC2, V-JEPA 2-AC and real Franka execution it reduces burned imagination by 62% and replays all 1,062 registered physical spends. Kept at `SYS_ALG_BOUNDARY` because the core novelty is deployment trust/calibration/state rather than a general multi-request resource scheduler.

### ASPIRE — trace-driven closed-loop robot skill discovery
- **Paper:** https://arxiv.org/abs/2607.00272
- **Code:** https://github.com/NVlabs/ASPIRE
- **Routes:** 2 / 7 / 9 · **Priority:** A
- **Role:** closed-loop robot execution engine exposes fine-grained multimodal traces for failure diagnosis, repair synthesis and validation, backed by a persistent skill library. Kept `SYS_ALG_BOUNDARY` because the main novelty is skill discovery/continual learning rather than serving/resource management. Official Apache-2.0 repo had 28 stars / 1 fork on this scan.

### RHO — training-time robotics harness optimization
- **Paper:** https://arxiv.org/abs/2606.16458
- **Artifact:** https://github.com/KE7/helix
- **Routes:** 2 / 9 · **Priority:** A
- **Role:** searches interpretable multi-file Repositories-as-Policies with tool-enabled coding agents and execution feedback, then freezes the deployment artifact for single-turn execution. Kept `SYS_ALG_BOUNDARY` because the main contribution is training-time harness/policy search rather than a reusable online serving runtime.

### ENPIRE — agentic physical autoresearch / fleet rollout harness
- **Paper:** https://arxiv.org/abs/2606.19980
- **Project:** https://research.nvidia.com/labs/gear/enpire/
- **Routes:** 1 / 2 / 9 · **Priority:** A+
- **Role:** reusable physical experiment/evaluation harness with automatic reset and verification, auditable rollout artifacts, and single- or multi-robot parallel physical execution. ENPIRE introduces MRU/MTU to measure robot-fleet and token utilization. Kept at SYS_ALG_BOUNDARY because its primary objective is autonomous policy self-improvement, not online inference admission or resource scheduling.
