# WATCHLIST

Promising concepts or ecosystem artifacts that are relevant to Physical-AI serving but do not yet meet the `CORE_SYS` evidence bar.

- **Harness Engineering for Physical AI: Robot Middleware Is the Harness Layer** — systems vision around Projection / Isolation / Transfer and a ROS 2 Harness Profile; kept here until a validated implementation/evaluation exists.
- **Same Weights, Different Robot: A Deployment Safety View of VLA Policies** — useful executable-policy/deployment-contract semantics, but currently a specification/diagnostic contribution rather than a serving system.
- **The Three Dimensions of ROS 2 Middleware** — Space / Time / State taxonomy; useful query anchor for topology abstraction, temporal predictability and state continuity, but not a runtime implementation.
- **IoRT ROS 2 Applications: Evaluating Zenoh and VPN for Robotic Networking in the Edge-Cloud Continuum** — IEEE ISCC / DistInSys 2025 Best Paper; useful real-world edge-cloud latency/throughput/fault-tolerance evidence for Zenoh, but primarily evaluates existing middleware rather than introducing a new runtime mechanism.

## Active follow-ups
- FogROS2-SGC / FogROS2-LS: determine whether they contribute durable cloud-connectivity/placement abstractions beyond the existing FogROS lineage.
- NVIDIA `ros2_benchmark`: classify as a mature infrastructure artifact and determine whether a canonical paper record should be created.
- Zenoh/DDS intermittent-connectivity state continuity and timing/isolation enforcement.
- Fleet admission/fairness and action-buffer-aware scheduling beyond Armory/Kairos/ROSA.

### HELIOS: Heterogeneous Lightweight VLA Model Serving System
- EuroSys 2027 in submission; metadata-only author disclosure. No public preprint/repo/details verified yet.

### HODAgent: Towards On-Demand, Responsive Humanoids for Physical World Human Interaction
- [arXiv:2608.17584](https://arxiv.org/abs/2608.17584) — high-level Physical-AI harness/runtime with semi-duplex interaction, asynchronous skill lifecycle/cancellation, persistent task state, shared embodiment contract and outcome-grounded completion.
- **Why WATCH_ONLY:** the arXiv listing was withdrawn on 2026-08-20 for mandatory company internal review; no official implementation repo is verified and the official PDF endpoint is unavailable. Keep the withdrawal provenance attached and do not treat the reported quantitative results as stable published evidence until an official re-release appears.

### TeleFuser — real-time world-model / multimodal streaming runtime
- [Official repository](https://github.com/Tele-AI/TeleFuser) · [Project documentation](https://tele-ai.github.io/TeleFuser/) · [ABot-World multi-session PR #36](https://github.com/Tele-AI/TeleFuser/pull/36)
- **Why watch:** directly implements continuous world-model serving with actor-owned stateful stages, bounded dataflow, per-session ordering, backpressure/lifecycle cleanup, LiveKit/WebRTC transport, distributed GPU execution and unified service APIs. LingBot serving already exposes retained multi-session admission and chunk-boundary time slicing; the ABot path preserves KV/RNG/VAE temporal state across control blocks.
- **Evidence:** first-party README reports 17.14 steady target-side compute FPS for LingBot-World v2 on 4×H100 at 832×480 against a 16 FPS playback target. Treat this as project-scoped compute throughput rather than end-to-end user latency.
- **Route-5 cache update (2026-09-02 19:02 CST):** TeleFuser documents external [CacheSeek](https://github.com/Tele-AI/CacheSeek) integration for cross-request approximate latent reuse. The serving path combines prompt-embedding similarity, persistent KV/distributed storage, vector DB + metadata, explicit query/lookup/resume/save contracts and uncached fallback. This is distinct from request-local feature caching and makes CacheSeek a concrete state-reuse/cache-infrastructure watch item; key open questions are validity/SLOs, cache pollution, multi-tenant isolation, placement, versioning and benchmark methodology.
- **Why not CORE_SYS yet:** no formal arXiv/venue paper was verified as of 2026-09-02; current public adoption is still early. Promote only when a paper/technical report, stronger independent deployment evidence, or a clearly reusable multi-session/cache resource-management substrate matures.

### vLLM-Omni #6872 — chunkwise VAE → transport → MP4 overlap
- [RFC #6872](https://github.com/vllm-project/vllm-omni/issues/6872), opened 2026-08-31. It proposes a bounded ordered media-chunk contract, explicit ownership/cancellation cleanup/backpressure, overlap across VAE decode → D2H/IPC transport → CPU H.264/MP4, persistent-ring transport, and a future disaggregated-VAE boundary.
- **Why watch:** this is a concrete stage-disaggregation / streaming-output systems direction rather than model optimization. The RFC's frozen 8×B300 MiniMax-H3 profile reports 1.247 s VAE plus 1.749 s transport+CPU MP4 on a 10 s request; the ~10%/~20% E2E savings are optimistic projections, not achieved speedups.
- **Promotion gate:** implementation A/B, bounded-memory/cancellation correctness, reusable media-contract generalization beyond H3, and evidence that the disaggregated VAE interface is broadly reusable.
