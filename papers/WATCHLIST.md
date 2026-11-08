**2026-11-08 15:01 CST — first-party PDF/repository review; WATCH_ONLY, NOT formally promoted (PHYSICAL_AI_SERVING_20261108_1501):**
- [FastAFD](https://arxiv.org/abs/2611.07149) — CORE_SYS candidate for hardware-aware MoE serving/disaggregation. The paper reports up to 1.17× over tuned vLLM wide EP on Qwen3 and 1.16× on Qwen3.5; the author-linked [MIT repository](https://github.com/hao-ai-lab/FastAFD) contains benchmark and correctness scripts plus CPU tests. The README's 1.35–1.45× uses a colocated baseline and is not the same comparison. Independent reproduction and VLM/Omni transfer remain open.
- [Phantom](https://arxiv.org/abs/2611.06019) — SYS_ALG_BOUNDARY candidate for diffusion temporal reuse and accelerator co-design. The official 13-page PDF reports 4.0× average speedup and 5.5× energy savings while preserving generation quality, with about 22% area overhead. No author-linked repository or online serving runtime was verified.

---

**2026-11-08 11:22 CST — official PDF/full-text review; SYS_ALG_BOUNDARY / WATCH_ONLY, NOT formally promoted (PHYSICAL_AI_SERVING_20261108_1122):**
- [MCUFlowNet](https://arxiv.org/abs/2611.08147) — PACE-NAS separates peak-SRAM design from latency search for MCU optical flow. The official 5-page PDF reports 18% lower peak SRAM and 93.2 ms versus 164.3 ms for retrained EdgeFlowNet (1.76×), with EPE 6.50 versus 6.40; simulated obstacle-avoidance success is 51.5% versus 41.8% at 2 m/s. The paper-linked [GitLab project](https://gitlab.kuleuven.be/emedia-research-lab/esat-stadius/mcuflownet/mcuflownet) main HEAD is verified, but the web UI was inaccessible and LICENSE/CI/tests/reproduction remain unverified. This is edge model architecture optimization, not a serving runtime or serving-SLO contribution.

---

**2026-11-07 17:45 CST — Official PDF/full-text review; ALG_INSPIRATION, WATCH_ONLY, NOT formally promoted (PHYSICAL_AI_SERVING_20261107_1744):**
- [Spatial-UMI-Dream](https://arxiv.org/abs/2611.07229) — 5B spatial WAM pretrained on 605 hours of RGB-D UMI data; two-stage world-only and joint world-action learning; RoboTwin-UMI 20-task benchmark and six real-world tasks. Policy-success results do not establish serving throughput/latency; no inference-serving runtime, scheduling/cache, p99 or fleet-SLO evidence was verified.

---

**2026-11-07 14:35 CST — Official PDF and implementation evidence; WATCH_ONLY, NOT formally promoted (PHYSICAL_AI_SERVING_20261107_1323):**
- [VisionSIM](https://arxiv.org/abs/2611.08368) — multi-modal physical-sensor simulator and synchronized indoor dataset (RGB/event/SPAD/iToF/dToF/thermal). All current evaluations are open-loop; closed-loop and eventually real-time simulation are future directions. PDF GitHub URLs are dependencies, not a verified VisionSIM project repository.
- [H-TRIP](https://arxiv.org/abs/2611.08139) — exact incremental multi-robot distance index; 2.21–8.59× query speedup in 16-robot simulation. [Matching C++20/AVX2 repository](https://github.com/ozaslan/htrip) exists, but root LICENSE is missing and paper-to-repository linkage is not fully verified.
- [Kinematic Hypothesis Context](https://arxiv.org/abs/2611.07411) — embodiment-conditioned policy-uplink video codec; 23.9% bitrate reduction and 23.2% fewer bits than DCVC-RT. Code is stated to be released upon formal publication; no public implementation or end-to-end serving SLO is currently verified.
- [Fast and Reliable Open-Vocabulary Object Search](https://arxiv.org/abs/2611.07493) — robot-memory retrieval and visual verification, about 10× fewer detector calls; real robot; live CLIP+SAM3 is about 2 s end-to-end, while optional LLM+SAM3 is about 10 s. No serving p99/code is verified.
- [Embodied RAG++](https://arxiv.org/abs/2611.07517) — embodied retrieval and per-product-model capability cache; 14–25 s preprocessing and 15–20 s query-plus-generation; 0.90/1.00 pair accuracy on 20 simulated scenes, with physical-robot validation still future work.
- [Time-Indexed Skill Success Models](https://arxiv.org/abs/2611.07964) — latency-aware skill launch-time planning with a real UR5e delay study; ALG_INSPIRATION only, not a serving runtime.
- [SCALE](https://arxiv.org/abs/2611.08390) was already registered; its official PDF is now locally validated. It remains a communication scheduler, not model inference serving.

**2026-11-06 02:45 CST — PDF validation update for PHYSICAL_AI_SERVING_20261106_0234:** TokenScale v2 (14 pages), HYPIC v3 (16 pages) and EKKA v1 (16 pages) official PDFs are now locally downloaded and PyMuPDF full-text validated. This closes their PDF evidence gate only; independent artifact reproduction and formal classification/promotion remain open.

**2026-11-06 02:34 CST — Evidence-only, NOT formally promoted (PHYSICAL_AI_SERVING_20261106_0234):**
- [TokenScale](https://arxiv.org/abs/2512.03416) — SoCC '26 PD-disaggregated autoscaling with token velocity and convertible decoders; 1.3–6.4× performance/cost improvement on production traces. **CORE_SYS candidate**; single-turn only, session affinity/multi-turn left for future work, no public code repo identified.
- [HYPIC](https://arxiv.org/abs/2607.01299) — ATC 2026 position-independent caching for hybrid attention; 3.25× TTFT reduction and 1.66× QPS at the same 1s SLO. **CORE_SYS candidate**; 14k-line SGLang implementation and Apache-2.0 repo, independent reproduction pending.
- [EKKA](https://arxiv.org/abs/2606.04594) — ICML 2026 automated diagnosis of silent errors in LLM inference; 80% pass@1, 88% pass@5 and four new bugs confirmed by developers. **CORE_SYS reliability candidate**; public repo exists but license is unresolved and engine forks are older.
- [SafeStart](https://arxiv.org/abs/2611.06147) — safety-preserving expert reduction for MoE serving; keeps at least 85% of the reported decode speedup while reducing the refusal regression. **SYS_ALG_BOUNDARY candidate**, not a serving control plane.
- [ServerBench](https://arxiv.org/abs/2611.06841) — open Apache-2.0 benchmark for agent-designed LLM serving systems; 22/33 verified, 13 above the strongest baseline. **CORE_SYS candidate**; independent artifact and production SLO validation remain open.
- [Ripple](https://arxiv.org/abs/2611.01067) — deadline-aware CPU/GPU sharing for embodied inference; one DGX Spark study meets a 2% CPU deadline-miss target and VLM deadlines. **CORE_SYS candidate**; multi-platform/fleet evidence remains open.
- [vExpert](https://arxiv.org/abs/2611.06057) — virtualized expert storage for distributed MoE inference; 55% better load balance and 1.2× E2E speedup on an 8-node H100 profile. **CORE_SYS candidate**; DeepSeek V3/R1-specific, independent reproduction pending.
- [NanoKV](https://arxiv.org/abs/2611.06377) — generation-aware KV compression for autoregressive video; up to 26.09× effective compression and 35.9% lower peak memory. **SYS_ALG_BOUNDARY candidate**; license scope differs across original code and backbone integrations.

**2026-11-02 09:12 CST — Evidence-only, WATCH_ONLY, NOT formally promoted:** [Apriel Voice 27B Preview](https://arxiv.org/abs/2610.40738) ([official model card](https://huggingface.co/ServiceNow-AI/Apriel-Voice-27B-preview)) reports ~2× output-token throughput for a custom optimized vLLM image on 4× H100 80GB. The paper's 1.91s τ-Voice latency is full-stack response latency including synthesis, not model-serving latency. Workload/baseline, author-linked serving code and independent reproduction remain unverified.

**2026-10-25 16:03 CST — Evidence-only, NOT formally promoted:** [Denoising Surface](https://arxiv.org/abs/2610.00499) (dLLM serving cost predictor and SJF scheduling, up to 1.92× lower chatbot latency); [MaskAhead](https://arxiv.org/abs/2610.06996) (dLLM mask-guided KV eviction, 9.5× cache reduction, batch-32 1.23× E2E; [Apache-2.0 code](https://github.com/brain-lab-research/MaskAhead) verified). Neither demonstrates direct multimodal/robotics serving.

**2026-10-25 15:01 CST — Evidence-only, NOT formally promoted:** [MHR-Router](https://arxiv.org/abs/2610.13278), retrieval-enhanced multimodal expert routing; five-page official PDF verified, but no measured serving latency, resource cost, throughput or p99.

**2026-10-25 14:08 CST — Evidence-only, NOT formally promoted:** [PACE](https://arxiv.org/abs/2606.00537), phase-aware action-chunk execution horizon; 50 RoboTwin2.0 tasks average success 57.8→64.2%, real-robot evaluation. No serving resource/SLO/p99 benchmark.

**2026-10-25 13:02 CST — Evidence-only, NOT formally promoted:** [RoboChrono](https://arxiv.org/abs/2609.36605), streaming robot task-understanding benchmark with 39 scenarios/34,713 instances; [official Apache-2.0 repo](https://github.com/mfan-res/ROBOCHRONO). No serving-runtime performance benchmark or p99 evidence.

**2026-10-25 12:06 CST — Evidence-only, NOT formally promoted:** [VLA Benchmark Bugs](https://arxiv.org/abs/2609.37771) audits 22 benchmark bugs and 4 design limitations; [Colosseum V2](https://arxiv.org/abs/2605.27759) GPU-parallel robot generalization evaluation. Official PDFs checked, no serving-specific system or independent author-code gate closed.

**2026-10-25 10:59 CST — Evidence-only, NOT formally promoted:** [FlashNav](https://arxiv.org/abs/2606.15846) GPU simulation/training infrastructure (9-page official PDF checked), not online Physical AI serving.

## 2026-10-24 21:02 CST — adjacent GPU/LLM memory candidates (NOT formal Physical-AI promotions)
- [UlaCache](https://arxiv.org/abs/2610.29820): GPU/CPU unified sparse-KV logical addressing, H200/B300 LLM throughput evidence; multimodal/VLA integration unverified.
- [Gandalf](https://arxiv.org/abs/2610.30791): SSD lifetime-aware LLM KV offload, trace-based lifetime gain; no robot/multimodal workload.
- [SnakeCharmer](https://arxiv.org/abs/2610.30990): generic GPU hardware prefetch control, A100 GPU-model evaluation, not a real VLA serving system.

# WATCHLIST

Promising concepts or ecosystem artifacts that are relevant to Physical-AI serving but do not yet meet the `CORE_SYS` evidence bar.

- **Harness Engineering for Physical AI: Robot Middleware Is the Harness Layer** — systems vision around Projection / Isolation / Transfer and a ROS 2 Harness Profile; kept here until a validated implementation/evaluation exists.
- **Same Weights, Different Robot: A Deployment Safety View of VLA Policies** — useful executable-policy/deployment-contract semantics, but currently a specification/diagnostic contribution rather than a serving system.
- **The Three Dimensions of ROS 2 Middleware** — Space / Time / State taxonomy; useful query anchor for topology abstraction, temporal predictability and state continuity, but not a runtime implementation.
- **IoRT ROS 2 Applications: Evaluating Zenoh and VPN for Robotic Networking in the Edge-Cloud Continuum** — IEEE ISCC / DistInSys 2025 Best Paper; useful real-world edge-cloud latency/throughput/fault-tolerance evidence for Zenoh, but primarily evaluates existing middleware rather than introducing a new runtime mechanism.

## Active follow-ups

### RoboBugBench — ROS 2 behavioral repair-oracle benchmark (2026-10-18)
- [Official arXiv:2610.16369](https://arxiv.org/abs/2610.16369): 33 execution-validated ROS 2 navigation defects with a physics-simulation behavioral oracle and adversarial audit. Adjacent **Route 9 evaluation infrastructure**, not VLA/WAM serving or a formally classified CORE_SYS paper.
- Track code/corpus availability, reproducible ROS 2 harness and oracle correctness. Official PDF retained privately on the research server.

### Wave Forcing / WaveRT — first-party streaming video runtime (2026-10-18, PROJECT WATCH)
- [Project](https://sjtu-deng-lab.github.io/WaveForcing/) · [Official source](https://github.com/SJTU-DENG-Lab/WaveForcing). No public arXiv/paper as of this checkpoint; this is **not** a formal paper promotion.
- Wave Parallelism converts the mixed-noise diffusion dependency graph into a block-causal DAG, enabling asynchronous GPU-stage wavefront execution, one-way layer-wise KV publication, copy-engine remote writes, paged KV and a measured-time streaming VAE pipeline. Built on SGLang Diffusion backend.
- First-party 8×H200 study reports 117.7 end-to-end FPS on 1.3B / 1596 output frames (7.9× matched single-GPU). 125.7 FPS is *steady p50*, not E2E. Public 5-step preview gives 84.2 E2E FPS with a different 5+2 topology; 14B result uses random weights and is not generation-quality evidence.
- **Route 3/5/6/10; HIGH priority** as adjacent multimodal/world-model runtime. Track paper/checkpoint release, multi-request SLO, independently reproduced quality/latency, and VLA/WAM applicability.

- **Microsoft Physical AI Toolchain GPU offload** — [official repo](https://github.com/microsoft/physical-ai-toolchain) / [Microsoft Research announcement](https://www.microsoft.com/en-us/research/blog/offloaded-inference-for-real-world-physical-ai-robotics/). As of 2026-09-23 it ships remote-GPU inference containerization/deployment, RPC and Kubernetes-based orchestration across robot/edge/cloud. High-value runtime-project WATCH; next gate is scheduler/admission/failure semantics and controlled multi-robot goodput/SLO evidence.
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

### MOSS-VL specialized SGLang-Omni realtime backend
- [OpenMOSS/MOSS-VL](https://github.com/OpenMOSS/MOSS-VL) · [MOSS-VL Technical Report](https://arxiv.org/abs/2608.15045)
- **Fresh runtime signal (2026-09-18):** the first-party MOSS-VL repository now bundles a specialized SGLang-Omni realtime backend for concurrent video streams, advertising dynamic multi-session scheduling and data-parallel replicas with the MOSS-VL-Realtime-SGLANG checkpoint.
- **Why watch:** this directly exercises long-lived streaming visual state, concurrent sessions and replica-level scaling, relevant to Routes 3/5/6/9. The technical report itself is primarily model/co-design work and predates this serving backend, so this remains a runtime-project watch rather than a canonical paper promotion. Track scheduler policy, state isolation/backpressure, multi-stream goodput/tail latency, replica placement/failure semantics and upstream generalization beyond MOSS-VL.

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

### SGLang-Omni #1909 — model-agnostic full-duplex runtime roadmap (2026-09-13)
- [Roadmap #1909](https://github.com/sgl-project/sglang-omni/issues/1909) targets a model-agnostic, session-centric runtime for native full-duplex models. Phase 1 covers session-owned Unit lifecycle/state/ordering/backpressure/cleanup, persistent AR KV through SGLang streaming sessions, and a shared realtime WebSocket API.
- **Systems scope:** later phases explicitly add duplex evaluation/CI and session SLOs (queue/compute/transfer latency, content latency, inter-Unit gaps, jitter, deadline misses, concurrency and memory), plus session batching, duplex-specific scheduling/stage placement, CPU-overhead reduction and CUDA-graph/kernel optimization.
- **Why watch:** together with vLLM-Omni #7181, this is strong cross-framework evidence that Omni serving is converging on reusable long-lived session/control-plane abstractions rather than per-model glue. Relevant Routes: 2/3/5/7/8/9/11.
- **Promotion gate:** merged/released session lifecycle + persistent-KV bridge + realtime API, multi-model integration, state-isolation/cancellation/backpressure correctness, and controlled concurrency/latency/jitter/memory evaluation. Track Phase-1 #2035/#2069/#2070 first.
