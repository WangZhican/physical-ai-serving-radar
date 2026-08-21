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
