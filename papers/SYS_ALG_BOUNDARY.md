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
