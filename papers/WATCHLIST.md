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
- [Official repository](https://github.com/Tele-AI/TeleFuser) · [Project documentation](https://tele-ai.github.io/TeleFuser/) · [ABot-World multi-session PR #45](https://github.com/Tele-AI/TeleFuser/pull/45)
- **Why watch:** directly implements continuous world-model serving with actor-owned stateful stages, bounded dataflow, per-session ordering, backpressure/lifecycle cleanup, LiveKit/WebRTC transport, distributed GPU execution and unified service APIs.
- **Multi-session maturity (2026-09-13):** ABot-World now documents continuously batched retained sessions through DiT and cached VAE decode. The published benchmark exercises **2 sessions × 30 continuously batched blocks** and checks generation, session-state isolation, ordering and batching. Multi-GPU deployment uses parent-side session assignment, process/process-NCCL worker modes, bounded per-session queues and explicit `latest` drop-oldest versus `lossless` backpressure policies. This supersedes the older one-session-per-worker/#36 snapshot; public PR frontier is now #45.
- **Evidence:** first-party README reports 17.14 steady target-side compute FPS for LingBot-World v2 on 4×H100 at 832×480 against a 16 FPS playback target. Treat this as project-scoped compute throughput rather than end-to-end user latency. Repository snapshot on 2026-09-13: **26 stars / 8 forks**.
- **Route-5 cache update:** TeleFuser documents external [CacheSeek](https://github.com/Tele-AI/CacheSeek) integration for cross-request approximate latent reuse with persistent KV/distributed storage, vector DB + metadata, explicit query/lookup/resume/save contracts and uncached fallback.
- **Why not CORE_SYS yet:** no formal arXiv/venue paper or controlled multi-session throughput/SLO/long-horizon study is verified. Promotion gate: #45 landing plus reproducible goodput/latency/fairness, bounded-memory/state-isolation evidence, migration/autoscaling semantics, or a formal systems paper.

### vLLM-Omni #6872 — chunkwise VAE → transport → MP4 overlap
- [RFC #6872](https://github.com/vllm-project/vllm-omni/issues/6872), opened 2026-08-31. It proposes a bounded ordered media-chunk contract, explicit ownership/cancellation cleanup/backpressure, overlap across VAE decode → D2H/IPC transport → CPU H.264/MP4, persistent-ring transport, and a future disaggregated-VAE boundary.
- **Why watch:** this is a concrete stage-disaggregation / streaming-output systems direction rather than model optimization. The RFC's frozen 8×B300 MiniMax-H3 profile reports 1.247 s VAE plus 1.749 s transport+CPU MP4 on a 10 s request; the ~10%/~20% E2E savings are optimistic projections, not achieved speedups.
- **Implementation precursor (2026-09-03):** open [PR #7000](https://github.com/vllm-project/vllm-omni/pull/7000) isolates LTX output materialization/transport on H200: 1.284 s→9.566 ms for the synchronized postprocess/output-transport path and 28.969→27.293 s E2E, while upstream generation/VAE stages stay within 0.5%. Related open [#6996](https://github.com/vllm-project/vllm-omni/pull/6996) and [#7001](https://github.com/vllm-project/vllm-omni/pull/7001) show that stable collective landing-buffer addresses and request-to-request device-memory lifetime are part of the same media-stage systems boundary, especially on XPU.
- **Promotion gate:** implementation A/B, bounded-memory/cancellation correctness, reusable media-contract generalization beyond H3, and evidence that the disaggregated VAE interface is broadly reusable.


### TeleFuser heterogeneous backend portability — 2026-09-03
- [PR #42](https://github.com/Tele-AI/TeleFuser/pull/42) adds Wan2.2 pipelines on Ascend NPU, complementing [#43](https://github.com/Tele-AI/TeleFuser/pull/43) MindIE-SD/VAE-parallel and [#44](https://github.com/Tele-AI/TeleFuser/pull/44) MiniMax-H3/FastH3 LoRA+FP8 Adapter support.
- **Why watch:** useful Route 6/10/11 evidence that the runtime is broadening beyond CUDA-only deployment toward reusable heterogeneous world-model/video serving.
- **Promotion gate:** merged/released implementation plus reproducible end-to-end latency, throughput, memory, failure-recovery, and reusable resource/stage-management semantics beyond model-specific enablement.

### vLLM-Omni #7074 — reusable world-model realtime/session roadmap (2026-09-12)
- [RFC #7074](https://github.com/vllm-project/vllm-omni/issues/7074) generalizes the earlier LingBot-specific roadmap into a reusable engine contract: one long-lived request, stepwise execution, streaming output, optional mid-request interaction, session-owned state and `/v1/realtime/video`.
- **Why watch:** direct Route 3/5/7/10 systems evidence spanning LingBot World 2.0, MiniMax H3 World, ABot-World and Echo-WM. The roadmap reports #6844/#6463/#6294 merged by 2026-09-07 as core prerequisites, but broader multi-session and reusable cross-model coverage remains roadmap work.
- **Promotion gate:** reusable cross-model implementation plus controlled FPS/latency/state-isolation and multi-session evidence.

### vLLM-Omni #7251 — long-video full-duplex lifecycle/correctness debt (2026-09-12)
- [Issue #7251](https://github.com/vllm-project/vllm-omni/issues/7251) reports native full-duplex long-video sessions resetting audio KV, accumulating leftover frames when `stack_frames=2`, desynchronizing AV state, growing memory, producing late playback acknowledgements and over-reserving vision slots.
- **Why watch:** concrete evidence that realtime Omni/Physical-AI serving needs bounded per-session queues, temporal compaction, state ownership/backpressure and long-horizon session regression tests rather than only endpoint-health checks.
- **Closure gate:** merged fix with multi-minute duplex regression, bounded memory/queue proof, AV alignment and state-isolation coverage.

### vLLM-Omni #7181 — Unified Full-duplex Framework (2026-09-12)
- [RFC #7181](https://github.com/vllm-project/vllm-omni/issues/7181) proposes an engine-owned `DuplexOmniEngine`/`DuplexOrchestrator`, a single `DuplexModelPlugin` seam, a unified realtime API and explicit separation of turn-based vs duplex engine stacks.
- **Why watch:** this is strong reusable-runtime evidence rather than one-model glue. Planned qualification spans MiniCPM-o 4.5, PersonaPlex, AURA, Nemotron VoiceChat, Qwen3-Omni and later multi-replica duplex serving, making it directly relevant to Routes 2/3/5/7/11.
- **Promotion gate:** merged/released multi-model implementation with state-isolation, resume/barge-in/cancellation correctness plus latency/concurrency evidence.

### vLLM-Omni #7194 — AURA on unified full-duplex runtime (2026-09-12)
- [RFC #7194](https://github.com/vllm-project/vllm-omni/issues/7194) proposes moving AURA's four-stage `Qwen3-ASR → Thinker (Qwen3-VL) → Talker → Code2Wav` pipeline from its independent turn-replay path into #7181's shared engine/session control plane.
- **Why watch:** direct composite/any-to-any serving evidence: ordered mailbox, epoch barge-in, stale filtering, playback ACK, lease/resume and multi-session admission become shared runtime semantics rather than AURA-specific orchestration.
- Keep attached to the vLLM-Omni project lineage; do not create a duplicate canonical paper/project entry.

### vLLM-Omni #7055 — Qwen3-Omni automatic turns + interruption integration (2026-09-13)
- [RFC #7055](https://github.com/vllm-project/vllm-omni/issues/7055) coordinates Qwen3-Omni automatic turn detection and reliable interruption across server-side VAD, session ordering, pending speech, cancellation, stale-output filtering, playback checkpoints and prompt/history ownership.
- **Why watch:** the systems question is whether a turn-based Omni model can share #7181's engine-owned `DuplexOmni` session/control plane with model-native duplex runtimes instead of retaining a separate serving-managed/chat-fallback state machine. This is direct unified-runtime/session-state evidence for Routes 2/3/5/7/11.
- **Acceptance gate:** automatic two-turn conversation, soft interruption, hard cancellation and playback/history consistency on the selected upstream path, with bounded pending input, semantic-history preservation, cleanup/race handling and repeated-interruption regression coverage.
- Existing #6618/#6372/#6659 results remain path-scoped evidence and do not prove the final combined runtime contract. Keep attached to the vLLM-Omni project lineage rather than creating a duplicate canonical paper/project entry.


### xDiT DistVAE — distributed VAE runtime substrate
- [Official repository](https://github.com/xdit-project/DistVAE) — MIT-licensed distributed VAE adapters for Diffusers.
- **System role:** row-sharded convolution/normalization with halo/stat exchange plus whole-tile distribution; supports multiple image/video VAE families and exposes tests/benchmark tooling.
- **Why watch:** it turns VAE decode from a monolithic tail into an explicit parallelizable media stage, making it directly relevant to heterogeneous placement, world-model/video serving, and future disaggregated-VAE contracts.
- **Current adoption signal:** ~95 stars / 15 forks in the 2026-09-03 public crawl. The xDiT parent project explicitly lists DistVAE as a self-maintained package and wires xDiT tile-overlap controls through DistVAE planners, confirming real upstream engine adoption rather than an isolated utility repo.
- **Promotion gate:** production serving integration or a formal systems evaluation showing latency/memory/scaling, stage placement/scheduling semantics, and correctness across representative workloads.

### llm-d Router: multimodal stateful-routing frontier
**Class:** runtime-project WATCH · **Routes:** real-time/stateful serving, multimodal/Omni serving, stage/modality disaggregation

- [#2663](https://github.com/llm-d/llm-d-router/issues/2663): route asynchronous  follow-up requests to the pod that owns the job — a concrete sticky/stateful routing requirement for diffusion/video serving.
- [#2650](https://github.com/llm-d/llm-d-router/issues/2650): extend coordinator media support from images to audio/video.
- [#2641](https://github.com/llm-d/llm-d-router/issues/2641): add sidecar and E2E coverage for audio/video multimodal requests.
- [#2628](https://github.com/llm-d/llm-d-router/issues/2628): E/PD multimodal embedding-cache ownership bug, highlighting stage-aware placement/accounting.

**Radar judgment:** high-value infrastructure evidence from a major distributed inference router, but not a new paper. Promote only if this matures into a reusable merged subsystem, release-level capability, or formal systems evaluation.
### vLLM-Omni #7367/#7368 — composable-parallel stage-placement/config contract (2026-09-13)
- [Issue #7367](https://github.com/vllm-project/vllm-omni/issues/7367) / [PR #7368](https://github.com/vllm-project/vllm-omni/pull/7368): documented `--strategy-config` + `--stage-overrides` can reject valid heterogeneous layouts because device-count validation runs against deploy-YAML defaults before CLI stage overrides are merged.
- **Why watch:** direct Route 4/6/11 evidence that disaggregated/heterogeneous serving needs explicit configuration precedence and validation ordering. The linked fix defers the eager check and validates the effective post-CLI layout during reconciliation.
- **Closure gate:** merged fix plus regression coverage across multi-stage/multi-device strategy + stage-override combinations. Keep attached to vLLM-Omni runtime lineage; no duplicate canonical paper/project entry.

### vLLM-Omni v0.29.0rc1 — full-duplex/world-model runtime maturity (2026-09-13)
- [Release v0.29.0rc1](https://github.com/vllm-project/vllm-omni/releases/tag/v0.29.0rc1) is a 2026-09-10 pre-release at signed commit `aff7d64`, with 159 merged changes from 95 contributors.
- **Why watch:** MiniCPM-o 4.5 and PersonaPlex full-duplex serving graduate out of experimental; shared duplex engine/serving code moves into core packages with a Python `DuplexClient`; server-side VAD and stronger multi-stage config/init land; LingBot World stepwise execution (#6844) is release-listed.
- **World-model progression:** [#7074](https://github.com/vllm-project/vllm-omni/issues/7074) marks E1 stepwise AR-Diffusion merged, E2 mid-session structured interaction partial via draft #7198, and E3 session-owned incremental VAE still open under #6533.
- **Boundary:** this is release/maturity evidence for an existing project, not a new paper. Keep RC claims scoped to v0.29.0rc1 until final release and multi-session/cross-model regression evidence mature.

