# SYS_ALG_BOUNDARY
- [Progress Probes P2](https://arxiv.org/abs/2610.31613) — **A-**, lightweight pi0.5 activation-linear runtime failure monitor, 0.026ms on RTX A6000; not a shared GPU serving scheduler, code unverified.
- [CovNav](https://arxiv.org/abs/2610.27677) — **A-**, calibrated fast/slow on-device navigation reasoning; Table II adaptive 0.72s vs slow-only 3.40s, slow activation 12.4%, RTX4090D and TurtleBot4/RTX3080 evaluation; no multi-tenant GPU-serving/p99 evidence, official code unverified.
- [PACT-VLA](https://arxiv.org/abs/2610.28019) — **A-**, pre-commit observation verification for speculative asynchronous action chunks; batched frozen-policy scoring overlapped with inference, no added control-step delay reported on evaluated hardware; success +15.0pp Kinetix/+5.2pp LIBERO, not multi-tenant serving p99; code unverified.
- [ActionGround](https://arxiv.org/abs/2609.33256) — **A-**, frozen VLA phase/dynamics correction runtime layer (<1ms author-reported overhead per control step), task success/stability focus, no multi-tenant serving/p99; source code unverified.
- [FlashForward](https://arxiv.org/abs/2609.32540) — **A**, stage-matched in-flight KV and sparse clean anchors for autoregressive video diffusion; up to 4 GPUs, 1.16–1.69× vs HiAR, 1.42–2.92× vs Self-Forcing; [author project](https://yikai-wang.github.io/FlashForward) verified, code unverified; not multi-session p99.
- [SemARC: Efficient Multimodal Inference through Adaptive Acquisition and Sequential Fusion](https://arxiv.org/abs/2610.07466) — **A**, modality-selective runtime controller, 61.4% lower GFLOPs, 44.0% GPU/CPU and 47.2% Android INT8 mean latency reduction; no multi-tenant scheduling.
- [Frequency-Step Cache](https://arxiv.org/abs/2610.15922) — **A**, exact-anchor vs drift-controlled repair separation for AR video diffusion; 2.36× SkyReels-V2 speedup, not WAM serving p99.
- [EmbodiTTA](https://arxiv.org/abs/2505.00986) — **A-**, on-demand edge adaptation on Jetson Orin Nano, 6.7× faster for 10k frames vs MECTA, 47.2% energy reduction vs EATA-C; [official code](https://github.com/TheMaXiao/EmbodiTTA) verified, not VLA multi-tenant serving.
- [Fast Plans, Faithful Actions](https://arxiv.org/abs/2609.30833) — **A**, block-AR waypoint planning 57→8 VLM passes, 8.7× lower real-robot planning latency, not end-to-end serving.
- [SimpleMemVLA](https://arxiv.org/abs/2609.05533) — **A**, video-history shared-prefix prefill during robot action execution, 1.02→0.68s decision latency, not multi-session cache isolation.
- [TurboVLA](https://arxiv.org/abs/2607.27205) — **A**, 0.2B/0.9GiB/31.2ms RTX4090, optimized CUDA Graph 7.42ms model inference; [official code](https://github.com/H-EmbodVis/TurboVLA) verified, not serving p99.
- [Staircase Policy: Streaming Inference for World-Action Models with Large Action Chunks](https://arxiv.org/abs/2609.36471) — **A**, staggered subchunk inference; 292.7 executed actions/s, first action 123.6→73.3ms; no verified code, not serving p99.
- [RAVEL: Asynchronous Rolling Inference for Flow-Based VLA Models](https://arxiv.org/abs/2609.34170) — **A**, async VLM and rolling action denoising; 178.52→92.97ms example response latency; no verified code.
- [WAMachine: Efficient World Action Model Inference with Adaptive Intermediate States](https://arxiv.org/abs/2609.34608) — **A**, replan/denoise/layer state adaptation; 1.47–3.05× observation-to-action latency improvement; linked GitHub repo currently HTTP404.
- [RoboHarness: Memory-Driven Orchestration of Heterogeneous Robot Policies for Long-Horizon Planning](https://arxiv.org/abs/2607.18060) — **A-**, policy routing and Memory Bridge; 135 real-robot trials, but reasoning/planning API 4.6s/call and 67.4s additional per trial; no verified author code or serving p99.
- [Urgent Actions Go First: Urgency-Aware Denoising for Real-Time VLA Control](https://arxiv.org/abs/2609.37772) — **A**, urgent action early release and background tail denoising; up to 1.89× *average action-availability latency* gain, not end-to-end throughput; no verified author code.
- [Communication-Aware Robot Execution for Cloud Inference under Spatially Heterogeneous Connectivity](https://arxiv.org/abs/2606.31497) — **A-**, cloud request-response window and motion-aware request placement under variable wireless connectivity. Simulated indoor network/emulated cloud; no production serving/p99 or verified code.
- [SpectralCache: Accelerating Diffusion-Based World Models via Spectral Feature Caching](https://arxiv.org/abs/2610.02660) — **A**, training-free spectral subspace reuse in diffusion world models; HunyuanWorld-Voyager-13B 5.22× author-reported generation speedup (1054s→202s, two Pro 6000 GPUs). No multi-tenant serving/p99 or verified code.
- [RESCUE: Counterfactual Evaluation of VLA Runtime Monitors](https://arxiv.org/abs/2610.13516) — **A-**, 128,340 counterfactual branches to assess intervention timing/cost; not a released production runtime or p99 system. Reusable code not independently verified.
- [FreeBar: Barrier-Constrained Guidance For Real-time Asynchronous VLA Execution](https://arxiv.org/abs/2610.14997) — **A-**, closed-form training-free action-chunk boundary alignment, 10–15% author-reported average success improvement; [Apache-2.0 code](https://github.com/NamelessCrew/FreeBar) verified. Model-level async plugin, not multi-tenant serving.
- [WAM-Cache: Staleness-Bounded KV Reuse](https://arxiv.org/abs/2610.11401) — **A**, action-attention plus latent-surprise refresh, 32–42% video-DiT prefill FLOP reduction; native-token CUDA prefill 1.23×, no p99/multi-session ownership. [Project](https://dingkai0302.github.io/wam-cache/).
- [REMM: Revisable Embodied Memory](https://arxiv.org/abs/2610.12710) — **A-**, evidence-linked task-state invalidation and recovery scheduling around frozen G0.5; 51 physical trials incl operator assistance, progress metrics not unassisted success or serving p99. [Project](https://revanthsenthil.github.io/remm/).
- [StreamingWAM: Chunk-Wise Staircase Flow Matching](https://arxiv.org/abs/2610.15585) — **A-**, 20p official PDF, RTX5090 Franka real-robot 15Hz control, 57.3ms steady-state replan vs 61.5ms π0.5; model-level streaming, no multi-tenant p99.
- [TacitVLA: Reasoning Without Reasoning Latency](https://arxiv.org/abs/2610.17540) — **A-**, 26p official PDF, one-H100 model-level latency up to 3.4× lower than explicit reasoning; action expert masks reasoning dependency, no production scheduler.
- [When to Ask for Help: Slow-Module Scheduling](https://arxiv.org/abs/2610.21160) — **A-**, 41p official study: VoI-based dual-system VLA invocation economics, RTX4090 52ms slow/55ms fast, 14 closed-loop arms and negative intervention result; no released production scheduler or fleet p99.
- [Into the LidarVerse](https://arxiv.org/abs/2610.19201) — **A-**, 31p official world-model report: rolling temporal KV and world-aligned spatial cache, four-step causal model, author reports 11 FPS on H100; model-level reuse, no general serving or p99 proof.
- [ActTune](https://arxiv.org/abs/2610.08444) — **A-**, VLA per-action precision plus asynchronous GPU frequency/power-cap adaptation, resident quantized weight bank; author reports up to 2.02× inference speedup and 76.8% less GPU energy per successful LIBERO task (BF16 baseline), latency-increase budget <=10%; dedicated controller code and fleet p99 unverified.

Works whose algorithmic novelty remains central, but which expose substantial runtime/deployment primitives.

- [LateMatch](https://arxiv.org/abs/2610.25358) — **A-**, CoRL 2026 cacheable late-interaction visual localization; paper-reported 2.2x desktop-GPU full-pipeline speedup (Aachen K=50). [Official MIT repository](https://github.com/UTAustin-SwarmLab/LateMatch) currently contains only LICENSE/.gitignore, no implementation; no real edge-device p99.
- [UniW(A)M](https://arxiv.org/abs/2610.18697) — **B+**, unified WM/WAM MoE and per-action-chunk PAIR interface selection with cache rebuild on switches; real-robot experiments. ~63ms router-only timing excludes full-loop components, no multi-tenant serving or p99, author code unconfirmed.

- [PICES](https://arxiv.org/abs/2610.19656) — **A-**, adaptive VLA action-chunk/horizon selection; up to 2.3x cumulative policy inference time on Jetson Orin/Thor (paper-reported), real-robot evaluation. [Official Apache-2.0 adapters](https://github.com/JHLee2314/PICES_VLA), not a standalone server/evaluator; no p99.
- [TIDE](https://arxiv.org/abs/2610.29264) — **A-**, real-robot asynchronous inference/recording server + online learner + checkpoint handoff; 8x H100 training (0.4s/optimizer step is not inference latency). Provenance-conditioned adaptation rather than multi-tenant serving/p99.

- [Xiaomi-Robotics-0](https://arxiv.org/abs/2602.12684) — **A-**, RTX 4090 80ms VLA inference, 30Hz aligned input timeline and asynchronous action-chunk execution on real bimanual robots; model/deployment boundary, not reusable multi-tenant serving or p99. Dedicated author code not independently verified.
- [Agile-VLA](https://arxiv.org/abs/2603.22899) — **B+**, edge robot asynchronous perception 10Hz / control 50Hz, physical 6-DoF industrial manipulation; task-specific action primitives, not generic GPU VLA serving/p99. Code unconfirmed.

- [FrameBlend](https://arxiv.org/abs/2610.29229) — **A-**, query-aware selective video KV recomputation across idle prefill and query-time processing; 14.1–58.7% total latency reduction on RVS-Ego for ReKV/LiveVLM (paper-reported). Algorithmic cache boundary, not multi-tenant GPU serving/p99; 15-page official PDF verified, code unconfirmed.

- [Rolling-WAM](https://arxiv.org/abs/2609.30247) — rolling/staggered WAM denoising across replanning cycles; 4.5x steady-state replanning speedup. Strong real-time control/runtime boundary evidence, but primary novelty remains model formulation rather than reusable serving substrate.
- [RealtimeWAM](https://arxiv.org/abs/2610.06617) — TACD + CEWP block-wise video-KV wavefront overlap for asynchronous one-step WAM inference; WAM-specific acceleration rather than reusable serving substrate.
- [SlackDrive](https://arxiv.org/abs/2609.28064) — pre-inference compute allocator that turns completed-forward latency into online compute-state/slack and chooses the highest-utility budget predicted to meet the next control-step latency envelope; +21.7% latency-constrained EPDMS on NAVSIM v2. Runtime-adaptive inference, not multi-tenant serving.
- [Watch, Recall, Act / ARMS](https://arxiv.org/abs/2609.28429) — always-on π0.5 streaming policy with asynchronously updated live-perception, embodied-state and agent-causal self-history contexts plus concurrent dual-arm action; strong state/lifecycle inspiration, but primary contribution remains policy/dataset integration rather than reusable serving infrastructure.
- [The World Model Hardware Accelerator (WMHA)](https://arxiv.org/abs/2609.16244) — latency-first diffusion/world-model accelerator with VLIW static scheduling, FP8/BF16 weight-stationary compute and online-softmax attention; Routes 6/10. Hardware-aware WAM inference evidence, not CORE_SYS serving/runtime.
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

## Edge latent-freshness / semantic-perception resource control
- [**Joint Age-of-Latent and Resource Minimization for Wireless Multi-Camera Perception With Temporal Window Selection**](https://arxiv.org/abs/2608.09411) — **A**, Routes P4/P5/P8. Defines AoL as freshness of decoded task-relevant latent state and jointly optimizes task-level temporal integration window with slot-level encoder selection, camera scheduling and NOMA power allocation. Kept outside CORE_SYS because current evidence is numerical/simulation-based rather than a reusable runtime.

## 2026-08-29 — TypeFly lineage predecessor
- [**TypeFly: Low-Latency Drone Planning With Large Language Models**](https://arxiv.org/abs/2312.14950) — **IEEE TMC 2025**, **A**, Routes P3/P4/P7. TypeFly/ChatFly combines the MiniSpec compact robot-planning language with stream interpretation so a drone can start executing before full LLM generation completes; local vision/skill execution gives it a practical edge/cloud runtime. [Project](https://typefly.github.io/) · [Repo](https://github.com/typefly/TypeFly) (~110 stars / 25 forks in current public crawl). Kept at `SYS_ALG_BOUNDARY` because compact plan representation and runtime execution are co-primary rather than a general serving scheduler/resource manager.


### JoyAI-VL-Interaction — always-on real-time vision-language interaction stack
- **Paper:** https://arxiv.org/abs/2606.14777
- **Project:** https://joyai-vl-video-future-academy-jd.github.io/JoyAI-VL-Interaction/
- **Code:** https://github.com/jd-opensource/JoyAI-VL-Interaction
- **Routes:** 3 / 5 / 7 / 11 · **Priority:** A+
- **Role:** complete open deployment stack around an interaction model: continuous video, long-horizon state, pluggable ASR/TTS/memory/UI, a real-time loop plus asynchronous background-model/agent delegation, served on standard vLLM infrastructure. The official repo currently surfaces ~1.8k stars / 182 forks. Kept at `SYS_ALG_BOUNDARY` because the main research novelty is model/training design, not serving scheduling or resource management.

## 2026-09-24 18:00 CST — asynchronous Physical-AI model/runtime boundary
- [**LiMA**](https://arxiv.org/abs/2609.28431) — **SYS_ALG_BOUNDARY / A**, Routes 3/7/10. Slow long-horizon intent generation runs asynchronously from fast dense motion refinement; reports 45.8% lower inference latency than Cosmos-Policy. Kept boundary because novelty is generative control/model coupling rather than a reusable serving substrate.
- [**InternW0**](https://arxiv.org/abs/2609.27656) — **SYS_ALG_BOUNDARY / A+**, Routes 3/5/7/10. Asynchronous multi-frequency video/action world model that reuses and observation-conditionally edits layerwise KV context instead of regenerating the future for every action update. Strong state-reuse/continuous-control evidence, but not a general serving runtime.

## 2026-09-24 21:00 CST — fixed-state episodic VLA memory
- [**MemBodied**](https://arxiv.org/abs/2609.28256) — **SYS_ALG_BOUNDARY / A**, Routes 3/5. Fixed-size associative state persists interactions across policy calls while an episode anchor preserves initial-scene context. The paper reports **91.9% lower inference latency than NativeMEM** while keeping memory/access cost independent of episode length. Strong Physical-AI temporal-state/cache inspiration, but the mechanism is a VLA model architecture rather than a reusable serving runtime. [Code](https://github.com/declare-lab/MemBodied).

## 2026-09-24 21:00 CST — fixed-state episodic VLA memory
- [**MemBodied**](https://arxiv.org/abs/2609.28256) — **SYS_ALG_BOUNDARY / A**, Routes 3/5. Fixed-size associative state persists interactions across policy calls while an episode anchor preserves initial-scene context. The paper reports **91.9% lower inference latency than NativeMEM** while keeping memory/access cost independent of episode length. Strong Physical-AI temporal-state/cache inspiration, but the mechanism is a VLA model architecture rather than a reusable serving runtime. [Code](https://github.com/declare-lab/MemBodied).
