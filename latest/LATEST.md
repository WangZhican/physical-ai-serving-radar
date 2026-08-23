## Hourly scan — 2026-08-23 23:59 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +1 / ALG/WATCH +0.
- **New:** [Relax](https://arxiv.org/abs/2604.11554) — service-oriented asynchronous omni-modal post-training runtime with fault-isolated services, TransferQueue data bus, staleness-controlled async execution and Qwen3-Omni validation. Kept at SYS_ALG_BOUNDARY because its primary workload is post-training rather than online serving.
- **Open source:** [redai-infra/Relax](https://github.com/redai-infra/Relax), Apache-2.0; public crawl ~550 stars.
- **Physical-AI track:** independent 24h→7d + targeted 30d scan completed; no new paper crossed SYS-first threshold.
- **Multimodal track:** independent scan covered omni serving/runtime, vLLM-Omni/SGLang-Omni and 30d MLLM systems; Relax was recovered through the post-training-runtime omission route.
- Next: Relax/VeRL-Omni runtime census → SGLang-Omni v0.1.2 production gates → vLLM-Omni duplex/zero-copy/runtime-cache → fresh 30d Multimodal SYS; parallel Physical-AI runtime/state/fleet/evaluation coverage.

## Hourly scan — 2026-08-23 22:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0; Physical-AI and Multimodal/Omni were independently scanned over fresh 24h→7d plus targeted 30d systems/runtime queries.
- **SGLang-Omni production serving:** v0.1.2 tracker #1436 remains open; the release cut is still gated by Qwen3-TTS admission/queueing (#1449), playback continuity (#1450), deterministic/batch invariance (#1475), absolute per-stage KV budgets (#1452), MPS-DP configuration/docs, and `WEIGHT_SHARE=1` concurrent correctness.
- **Reusable Omni runtime primitive:** SGLang-Omni #1357 now records merged/default-ON breakable Prefill CUDA Graph support for Higgs-TTS, MOSS-Transcribe-Diarize and Qwen3-ASR; Qwen3-ASR uses 50 prefill buckets up to 4096 tokens. This is framework/runtime evolution, not a paper promotion.
- **vLLM-Omni:** #6028 full-duplex graduation, #6212 Hop-2 video transport, #5120 structural updates and #6231 runtime-cache compatibility remain open at the verified boundaries.
- **Physical-AI:** fresh robot-policy/fleet/state/evaluation scans produced no new paper above the SYS-first threshold.
- Next: SGLang-Omni release cut + Prefill CUDA Graph expansion/production impact → vLLM-Omni duplex/video-transport implementation → check SGLang shared-KV/MPS generalization to Omni → fresh 30d Multimodal SYS census; Physical-AI continues runtime/evaluation/state/fleet omission recovery.

## Hourly scan — 2026-08-23 21:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0; Physical-AI and Multimodal/Omni were independently scanned over fresh 24h→7d plus targeted 30d systems/runtime queries.
- **SGLang-Omni production serving:** v0.1.2 tracker #1436 remains open. Active gates include Qwen3-TTS admission/queueing past c32 (#1449), playback continuity (#1450), deterministic/batch-invariant inference (#1475), absolute per-stage KV-memory budgets (#1452), same-GPU MPS-DP configuration, and `WEIGHT_SHARE=1` concurrent-request correctness. The Qwen3-TTS MPS-DP track reports +55% peak throughput and better p95 latency/RTF at c32; this is runtime/release evidence, not a paper promotion.
- **vLLM-Omni:** RFC #6028 remains open with no linked migration PR in current indexed evidence; RFC #6212 remains open with Hop-1 POSIX shared-memory video IPC already landed and Hop-2 binary/compressed/zero-copy output transport still on the roadmap.
- **Adjacent substrate:** SGLang #35648 proposes same-GPU native-DP replicas with managed CUDA MPS, daemon-owned shared weights and a global HBM KV pool; its first draft is not multimodal, so it is not promoted into the Multimodal core.
- **Physical-AI:** fresh robot-policy/fleet/state/evaluation scans produced no new paper above the SYS-first threshold.
- Next: SGLang-Omni v0.1.2 release gates → vLLM-Omni duplex/video-transport implementation → test whether SGLang shared-KV/MPS generalizes to Omni → fresh 30d multimodal systems census; Physical-AI continues runtime/evaluation/state/fleet omission recovery.

## Hourly scan — 2026-08-23 18:03 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0; both Physical-AI and Multimodal/Omni tracks were independently scanned over fresh 24h→7d plus targeted 30d systems/runtime queries.
- **Multimodal runtime update:** vLLM-Omni RFC #5822 proposes generic per-timestep execution for Modular Diffusers, removing whole-generation head-of-line blocking and enabling inter-request step interleaving, responsive cancellation and progressive output across roughly 15 modular diffusion families. The RFC explicitly does **not** add cross-request GPU batching, so this is tracked as runtime evolution rather than a paper promotion.
- **Configuration/runtime hygiene:** vLLM-Omni tracker #6232 is moving request-varying model behavior away from process-global environment switches into typed/request-scoped configuration.
- **Physical-AI:** fresh scans re-hit PhyAI and existing runtime anchors; no new paper crossed the SYS-first bar.
- Next: verify #5822 implementation/merge and interaction with batching/preemption → SGLang-Omni v0.1.2 same-GPU MPS-DP/WEIGHT_SHARE release gate → fresh 30d multimodal systems census; Physical-AI continues runtime/evaluation/state/fleet omission recovery.

## Hourly scan — 2026-08-23 17:00 CST

- **Dual-track coverage is now explicit.** Physical-AI/VLA/WAM and Multimodal/MLLM/Omni were scanned independently over 24h→7d, followed by targeted 30d omission checks; neither track is inferred from the other.
- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0. Physical-AI hits were canonical or below threshold.
- **Multimodal/Omni scan:** re-hit canonical HorizonServe, M*, HydraInfer, Omni-Flow, Cornserve and vLLM-Omni; no additional 2026-08 paper crossed the SYS-first bar.
- **Runtime ecosystem update:** first-party SGLang-Omni issue #1436 (opened 2026-08-10) tracks production-serving v0.1.2, including same-GPU Qwen3-TTS MPS-DP and `WEIGHT_SHARE=1` request/concurrency correctness. Tracked as runtime evolution, not a paper promotion.
- Next multimodal frontier: SGLang-Omni production-serving release gate → same-GPU stage sharing / weight-sharing correctness → vLLM-Omni multimodal batching/state evolution → fresh 30d MLLM/Omni systems census.

## Hourly scan — 2026-08-23 12:00 CST

- Fresh 24h/7d + targeted 30d scan completed; no new paper crossed the SYS-first promotion threshold.
- Coverage: robot-policy serving/runtime, world-model rollout, evaluation infrastructure, deployment-gate/runtime-safety systems.
- Watch lead: SimTooReal exposes cross-engine verification, runtime safety gating and staged fleet rollback, but no paper-grade primary evidence/open artifact was verified yet; not promoted.

## Hourly scan — 2026-08-23 10:02 CST

- Fresh 24h/7d plus targeted 30d SYS-first scan completed; **no new canonical paper promotion**.
- Zetta/Z-Infra deep artifact audit: first-party repo now exposes immutable campaign manifests/queues, shared-queue workers, capacity probes, deployment/preflight orchestration, LIBERO VLA client/server and RoboCasa environment-farm/provider-broker components. This materially strengthens the existing Zetta CORE_SYS entry as a real rollout-infrastructure control plane.
- Evidence boundary preserved: the same README still marks the full Z-Infra open-source release as coming soon, so no unpublished global scheduler/fairness/resource-isolation/fault-tolerance mechanism is inferred from partial code release.
- Fresh re-hits (PhyAI, HorizonServe, vLLM-Omni, M*, Embodied.cpp) were deduplicated; algorithm-only work was not promoted.

## Hourly scan — 2026-08-23 09:00 CST

- Fresh 24h/7d plus targeted 30d scan completed; no new canonical paper promotion.
- Zetta/Z-Infra follow-up: the official repository now exposes substantial campaign, shared-queue worker, capacity-probe, deployment, VLA-server and environment-farm infrastructure, while its README still labels Z-Infra as coming soon. We therefore track this as a **partial infrastructure artifact release**, not a completed Z-Infra release.
- Re-hits (Zetta, Embodied.cpp, Kairos serving, PhyAI, M*) were deduplicated; algorithm-only Efficient VLA work was not promoted into CORE_SYS.

# Latest scan

**Updated:** 2026-08-23 07:00 CST

- **CORE_SYS +1:** OpenBot-Fleet (ICRA 2024), recovered via fleet data/runtime omission audit.
- Fresh 24h/7d scan: no newer direct SYS promotion.
- Coverage: fleet experience streaming, cloud policy lifecycle, edge-cloud robotics, admission/fairness/deadline/SLO.
- Next: OpenBot-Fleet references/Intel lineage, then Armory-external fleet SLO and world-state runtime.


### 2026-08-22 08:00 CST
Fresh 24h/7d + targeted fleet-data/runtime scan completed. No new SYS-first promotion; reviewed distributed fleet policy merging and cloud-assisted fleet/VLA runtime references. Continuing paper-backed fleet experience-streaming and SLO-scheduling census.

### 2026-08-22 09:02 CST
Fresh 24h/7d + targeted 30d fleet/cloud/runtime scan completed. No new paper cleared the SYS-first promotion bar. Ecosystem watch: Intel OpenVINO Physical AI is now tracked as a strong production robot-policy runtime lead (unified deployment API, sync/async control loop, heterogeneous CPU/GPU/NPU execution, real-time action chunking); paper/technical-report evidence is being reverse-censused before any canonical promotion.

### 2026-08-22 10:00 CST
Fresh 24h/7d + targeted 30d policy-serving/runtime scan completed; no new paper promotion. Ecosystem watch: vLLM-Omni RFC #6069 proposes a shared Robot Policy Serving Contract for VLA models (request/action schema, metadata, validation and reusable serving examples), building on realtime OpenPI serving and active pi0/pi0.5 integrations. XPolicyLab was revalidated and deduplicated; OpenVINO Physical AI remains a strong runtime lead pending paper-backed systems evidence.

### 2026-08-22 11:05 CST
Fresh 24h/7d + targeted robot-policy runtime scan completed; no new SYS-first paper promotion. vLLM-Omni RFC #6168 adds an important deployment milestone: DreamZero-DROID has now been served end-to-end through the OpenPI robot endpoint on 2×MI300X/ROCm with 34 closed-loop rollouts. RFC #6069 and the pi0/pi0.5 tracker remain open, so this is tracked as cross-vendor serving/evaluation ecosystem progress rather than a new paper entry.

### 2026-08-22 12:03 CST
Fresh 24h/7d + targeted 30d scans completed; no new SYS-first paper promotion. vLLM-Omni RFC #6069 remains an open shared robot-policy serving contract and #6168 remains an open ROCm evaluation tracker. Current public evidence still supports DreamZero-DROID end-to-end serving on 2×MI300X/ROCm, while pi0/pi0.5 and broader evaluator coverage remain follow-up work. Persistent world-state and fleet-SLO queries were also rechecked; no stronger new paper displaced the current canonical anchors.


### 2026-08-22 13:01 CST — hourly scan
Fresh 24h/7d plus targeted 30d SYS-first scan completed. No new paper promotion this hour. Revalidated the still-open vLLM-Omni Robot Policy Serving Contract RFC and deduplicated canonical XPolicyLab/PhyAI hits. Next focus: cross-model robot-policy contract stabilization, fleet admission/deadline/action-freshness SLOs, persistent world-state migration, and middleware timing isolation.

### 2026-08-22 14:01 CST — hourly scan
Fresh 24h/7d plus targeted 30d SYS-first scan completed; no new paper promotion. **Runtime milestone:** vLLM-Omni `main` now includes a concrete LeRobot π0 online-serving recipe over `/v1/realtime/robot/openpi`, with `policy_server_config` handshake metadata, action-horizon/action-dimension semantics, OpenPI WebSocket e2e tests, and LeRobot reference-parity validation. This is tracked as an implementation step toward the open Robot Policy Serving Contract RFC #6069, not as a separate paper. Next: π0.5/generalized realtime backend + streaming structural state, then fleet SLO and world-state runtime.

### 2026-08-22 15:00 CST — hourly scan
Fresh 24h/7d plus targeted 30d SYS-first scan completed; no new paper promotion. Revalidated RFC #6069 as still open and added a stateful-serving watch point from vLLM-Omni's iterative diffusion runtime: explicit per-request state, independent RNG/request identity under mixed batching, cleanup on completion/cancellation/failure, and resumable chunk-level EDF/preemption. These are transferable primitives for future VLA/WAM stateful serving, not a separate robot-policy paper. Next: π0.5/generalized robot serving, structural-state adoption by robot/world-model paths, fleet SLO scheduling, persistent world-state migration, and middleware timing isolation.

### 2026-08-22 16:01 CST — hourly scan
Fresh 24h/7d plus targeted 30d SYS-first scan completed; no new paper promotion. vLLM-Omni RFC #6069/#6168 remain open. New runtime signal: RFC #6231 makes DLO node-local runtime-cache sharing an explicit DP/TP/SP compatibility contract based on final host-weight-layout equivalence. This is tracked as runtime/cache ecosystem evidence rather than a separate paper. Legal full-text retries for ROSGM and TILDE still resolve only to closed/request-only routes, so no PDF status was falsely upgraded. Next: check whether runtime-cache/state primitives enter robot-policy/world-model paths, then π0.5/generalized serving and fleet SLO scheduling.

### 2026-08-22 17:01 CST — hourly scan
Fresh 24h/7d plus targeted 30d SYS-first scan completed; no paper promotion. **Implementation-status correction:** vLLM-Omni RFC #6168 is a dated tracker snapshot and still lists π0/π0.5 as proposed, while current `main` already contains an executable LeRobot π0 online-serving recipe over `/v1/realtime/robot/openpi`. We now treat mainline as stronger current evidence for π0 support; π0.5/generalized realtime serving remains unresolved in this scan. Next: resolve π0.5/#4419 and structural streaming-state #5120, then continue fleet SLO and persistent-state runtime coverage.

### 2026-08-22 17:57 CST — hourly scan
Fresh 24h/7d plus targeted 30d SYS-first scan completed; no new paper promotion. Current evidence still supports π0 as executable mainline robot-policy serving, while π0.5 remains WIP in the shared-contract RFC through PR #4419 and its opt-in `realtime_triton_prefix`; generalized π0.5 realtime serving is not yet verified as mainline-stable. RFC #6069 explicitly defers longer-lived camera/robot-action structural updates to #5120, so that state path is still future contract work. Next: resolve #4419/#5120 first-party status, then fleet SLO, world-state migration, and middleware timing isolation.

### 2026-08-22 18:58 CST — hourly scan
Fresh 24h/7d plus targeted 30d SYS-first scan completed; no new canonical paper promotion. **Implementation-status correction:** vLLM-Omni π0.5 PR #4419 was closed on 2026-08-18 and shows no merged marker, so its specialized `realtime_triton_prefix` backend and PR benchmarks must remain PR-scoped rather than mainline claims. RFC #5120 remains open; generic structural updates for streaming camera/robot/world-model inputs are still future contract work relative to Robot Policy Serving Contract RFC #6069 Phase 1. Next: find any successor π0.5 implementation and #5120 implementation PRs, then fleet SLO/state-runtime/middleware enforcement.

### 2026-08-22 19:58 CST — hourly scan
Fresh 24h/7d plus targeted 30d SYS-first scan completed; no new canonical paper promotion. First-party recheck found no indexed successor/replacement to the closed π0.5 PR #4419; current `main` still has executable LeRobot π0 serving, while #4136 and Robot Policy Serving Contract RFC #6069 remain open. RFC #5120 structural streaming state also remains separate from Phase 1 robot-policy serving, with no verified stable robot/world-model integration in this scan. Continued fleet-SLO, persistent-state, and Zenoh/DDS enforcement searches returned canonical, ecosystem-only, or non-SYS hits. Next: successor π0.5/#5120 implementation linkage, Armory-external fleet SLO, state migration, middleware enforcement, and legal PDF retries.

### 2026-08-22 21:02 CST — hourly scan
Fresh 24h/7d plus targeted 30d SYS-first scan completed; no new canonical paper promotion. vLLM-Omni evidence remains bounded: executable LeRobot π0 serving is in current main, issue #4136 and Robot Policy Serving Contract RFC #6069 remain open, and no indexed successor to the closed π0.5 PR #4419 was found. RFC #6069 still excludes RFC #5120 structural streaming updates from Phase 1. Legal full-text retries for Eevee, ROSGM, and TILDE resolved no new open copy. Next: π0.5/#5120 linkage, Armory-external fleet SLO scheduling, PCS/WorldMove migration, Zenoh/DDS enforcement, and pending-PDF retries.

### 2026-08-22 22:00 CST — hourly scan
Fresh 24h/7d plus targeted 30d SYS-first scan completed; no new canonical paper promotion. **RFC #5120 status refined:** it remains open, but its prerequisite frontend generalization is already marked done (`prompt_update` → typed `OmniTextPrompt`, generic `interaction` event). The core systems work is still open: structural payload/schema/timing/update-mode routing through the engine/orchestrator, per-request structural state, chunk-boundary application and model-specific `StructuralDataProcessor`. Robot Policy Serving RFC #6069 still excludes #5120 from Phase 1, and no successor to closed π0.5 PR #4419 was found. Next: track #5120 engine/state implementation and robot/world-model linkage, then π0.5 successor, fleet SLO, state migration, middleware enforcement and pending PDFs.

### 2026-08-22 23:00 CST — hourly scan
Fresh 24h/7d plus targeted 30d SYS-first scan completed; no new canonical paper promotion. New first-party runtime signal: vLLM-Omni RFC #6195 proposes decoupling DLO host-weight storage from DP request scheduling via a loader-owned `HostWeightPlan` with automatic, fail-closed checkpoint-mmap/runtime-cache selection based on runtime-layout compatibility. This is tracked as deployment/cache ecosystem evidence for large VLA/WAM stacks, not as a separate Physical-AI paper or a new request scheduler. Current robot-serving boundary is unchanged: executable LeRobot π0 is in mainline, no indexed successor to closed π0.5 PR #4419 was found, and RFC #5120 core structural-data engine/state path remains unfinished and outside RFC #6069 Phase 1.

### 2026-08-23 00:01 CST — hourly scan
Fresh 24h/7d plus targeted 30d SYS-first scan completed; no new canonical paper promotion. **Implementation-status upgrade:** vLLM-Omni RFC #6195 now explicitly records Phase A merged via PR #6213: loader-owned `HostWeightPlan`, fail-closed direct checkpoint mmap and bounded no-AllGather staging are in mainline for TP=1. TP>1 remains functional through the normal TP-aware loader but does not receive the shared-mmap host-memory benefit. Phase B under RFC #6231—normalized node-local runtime mmap-cache sharing by final host-weight-layout identity across DP/TP/SP—remains open and explicitly excludes request admission/batching/orchestration. Next: follow Phase-B implementation and whether this cache substrate is exercised by robot-policy/world-model serving, then structural state (#5120), π0.5 successor, fleet SLO and world-state runtime.

### 2026-08-23 01:00 CST — hourly scan
Fresh 24h/7d plus targeted 30d SYS-first scan completed; no new canonical paper promotion. **Phase-B status unchanged:** RFC #6231 remains open and no new indexed implementation PR beyond the already-merged Phase-A PR #6213 was found in this pass. Mainline π0 serving remains executable, while RFC #6069 is still open, no successor to closed π0.5 PR #4419 was found, and RFC #5120 core structural-state engine/request-state work remains unfinished. HELIOS heterogeneous lightweight VLA serving is still only an author-CV EuroSys 2027 submission signal with no public preprint/repo found. Next: Phase-B implementation linkage → structural state → π0.5 successor → fleet SLO → world-state migration → middleware enforcement.


## 2026-08-23 02:02 CST
- CORE_SYS +2: Execution-State Capsules / FlashRT (arXiv:2606.20537, A+, Routes 3/5/6) adds graph-bound complete execution-state checkpoint/restore/fork/rollback for latency-first on-device Physical-AI serving; PhAIL (arXiv:2605.29710, A, Routes 8/9) adds open real-robot VLA evaluation infrastructure with distributional time-to-success, Human-Relative Throughput, confidence intervals, significance testing and per-rollout artifacts.
- Fresh 24h/7d scan: no newer direct SYS promotion; both additions are historical omission recovery.

## 2026-08-23 03:00 CST
- `SYS_ALG_BOUNDARY +2`: **dWorldEval** (arXiv:2604.22152, ICML 2026 Spotlight, Routes 9/10) adds scalable world-model proxy evaluation with action-centric discrete diffusion, sparse keyframe memory and automatic progress scoring; **Hi-WM** (arXiv:2604.21741, Routes 5/9/10) adds cached intermediate world-state rollback/branching for reusable corrective continuations.
- Both remain below CORE_SYS because their primary novelty is evaluation/post-training methodology rather than serving resource management or scheduling. Official project pages and arXiv PDFs verified.
- Fresh 24h/7d scan produced no newer direct SYS promotion. FlashRT adoption recheck: 486 stars / 60 forks / 508 commits in the current public crawl.

## 2026-08-23 04:02 CST
- **CORE_SYS +1:** RoboChallenge (arXiv:2510.17950), recovered through the real-robot evaluation-infrastructure audit.
- System role: 10-machine heterogeneous online robot fleet, fully asynchronous timestamped observation/action-queue APIs, explicit evaluation-job scheduling, public submission/result flow, 7×24-oriented robot service.
- Official `RoboChallenge/RoboChallengeInference` artifact verified (~149 stars in current public crawl). Fresh 24h/7d SYS-first scan found no newer direct promotion.
- Next: RoboChallenge/RoboArena/AutoEval/PhAIL/RoboDojo admission/resource-isolation comparison, then execution-state/world-state runtime and fleet SLO scheduling.


## 2026-08-23 05:02 CST
- **CORE_SYS +1:** [Thea / Towards the Harness of Embodied Agents](https://arxiv.org/abs/2608.11246), Routes P2/P5/P7, priority A. Provider-neutral embodied-agent harness with persistent scene-graph context, Tool Protocol, post-execution evaluation/exit codes, memory/skills/safety and embodiment portability. Official [project](https://eit-hai.github.io/thea/) and [Apache-2.0 repo](https://github.com/EIT-HAI/Thea) verified (~45 stars).
- Fresh 24h/7d SYS-first scan found no newer direct promotion; this addition came from 30d harness/orchestration omission recovery.
- Coverage frontier: Thea/EIT-HAI harness follow-ons → RoboChallenge evaluation admission/fairness → FlashRT/PCS/WorldMove fork/rollback/migration → vLLM-Omni stateful robot serving → fleet SLO → Zenoh/DDS enforcement.

## 2026-08-23 05:57 CST — hourly scan
- Fresh 24h/7d + targeted 30d SYS-first scan completed; **no new canonical paper promotion**.
- **FlashRT / Execution-State Capsules adoption update:** first-party serving docs now operationalize capsules for fresh sessions, branch/fork, restart/resume, non-hot workers and pinned shared prefixes. FlashRT Nexus also ties the native C++ Pi0.5 runtime ABI to embedded robot loops, HTTP serving and execution-state capsules.
- Interpretation: complete execution-state checkpoint/restore/fork/rollback is increasingly a production serving abstraction, not just a paper primitive. This is an ecosystem/adoption update to the existing CORE_SYS entry, not a duplicate paper.
- Next: FlashRT follow-ons/adoption → RoboChallenge/Thea resource-enforcement and evaluation scheduling → PCS/WorldMove state migration → vLLM-Omni stateful robot serving → fleet SLO → Zenoh/DDS enforcement.

## 2026-08-23 07:00 CST — hourly scan
- Fresh 24h/7d + targeted 30d SYS-first scan completed; **no new canonical paper promotion**.
- FlashRT: production docs now treat execution-state capsule restore/fork as a serving-layer primitive for fresh sessions, branches, restart/resume, non-hot workers and pinned prefixes; bounded request queues are also documented above the fixed execution ABI.
- PhAIL: the live public leaderboard now exposes **1,083 real-robot episodes** and a unified real/sim evaluation service with randomized/blinded runs plus per-run video/telemetry artifacts. This strengthens the existing PhAIL CORE_SYS entry as production evaluation infrastructure; it is not a new paper.
- Next: complete-state serving follow-ons → PhAIL/RoboChallenge/AutoEval/RoboArena scheduling/resource-isolation comparison → PCS/WorldMove/Hi-WM state migration/fork/rollback → vLLM-Omni stateful robot serving → fleet SLO → Zenoh/DDS enforcement.

## 2026-08-23 08:00 CST
**New CORE_SYS:** Zetta ζ / Z-Infra (arXiv:2608.16590, A+, routes 2/3/6/7/9). Closed-loop embodied harness with action-frequency governance and heterogeneous rollout infrastructure. Official repo verified (~60 stars in current crawl). Fresh 24h/7d scan completed; next: Z-Infra implementation and resource/scheduling comparison with Thea/Embodied.cpp/XPolicyLab.

## 2026-08-23 11:02 CST — hourly scan
- **New CORE_SYS:** RoboLab (RSS 2026, arXiv:2604.09860), Route P9 / A+.
- Fresh 24h/7d SYS-first scans found no newer direct promotion; RoboLab was recovered through NVIDIA evaluation-infrastructure omission auditing.
- Official repo is Apache-2.0 and actively maintained; current public crawl shows ~447 stars / 66 forks and v0.3.0 released 2026-08-07.
- Next: RoboLab/Isaac Lab-Arena ecosystem → real/sim evaluation admission, scheduling and resource isolation → stateful Physical-AI serving and fleet SLO.

## 2026-08-23 13:00 CST
- SYS_ALG_BOUNDARY +1: ROBOGATE (arXiv:2603.22126), Route 9, A-. Deployment-validation/failure-boundary framework.
- Evidence guard: the official 2026-07-18 correction retracts/quarantines the learned-policy VLA comparison and cross-simulator capability/safety interpretation. Retained scripted-controller failure-boundary results remain usable; historical VLA leaderboard numbers are not current evidence.
- Fresh 24h/7d scan completed; promotion came from deployment-gate/runtime-safety omission recovery.

## 2026-08-23 14:00 CST

**Coverage:** 24h + 7d fresh scan; targeted 30d omission recovery.

**New CORE_SYS:** AEROS (arXiv:2604.07039) and Harnessing Embodied Agents: Runtime Governance for Policy-Constrained Execution (arXiv:2604.07833). AEROS adds a persistent-agent / installable-capability runtime abstraction; Runtime Governance externalizes admission, policy enforcement, monitoring, rollback, and human override.

**Evidence boundary:** AEROS has an Apache-2.0 runtime MVP, but its current public implementation is single-process/single-thread, mock-robot, and has no real-time guarantees; do not overstate production maturity.


### 2026-08-23 15:03 CST
AEROS-program reverse census promoted three systems/infrastructure works: **Federated Single-Agent Robotics** (fleet runtime federation), **Governed Capability Evolution** (shadow/gated deployment + rollback), and **EmbodiedGovBench** (governance/recovery evaluation harness). Fresh 24h/7d scan completed; next audit targets ECM Contracts and implementation artifacts.

### 2026-08-23 16:00 CST
Fresh 24h/7d SYS-first scan completed; no newer direct Physical-AI/Multimodal serving paper crossed the promotion bar. **CORE_SYS +1: ECM Contracts** (arXiv:2604.13097, A-, Routes 2/5/7), recovered from the saved AEROS-cluster frontier. It implements registry/resolver/contract-checker infrastructure for installable embodied capabilities and pre-deployment checks for resource, permission, recovery and version conflicts. No official public repo was verified in this scan, so maturity remains A-. Public dataset is now **132 verified works / 101 CORE_SYS / 22 SYS_ALG / 4 ALG / 5 WATCH**.


### 2026-08-23 19:00 CST — dual-track hourly scan
- **Physical AI:** fresh robot-policy/runtime scan completed; no new paper promotion. vLLM-Omni Robot Policy Serving Contract #6069 remains an active serving-boundary evolution.
- **Multimodal / Omni:** no new paper promotion, but two high-value runtime developments were verified: vLLM-Omni #6028 proposes graduating the model-neutral full-duplex engine/control-plane + serving stack after reuse by MiniCPM-o 4.5 and PersonaPlex; #6212 targets repo-wide video tensor/output transport to address very large video payloads, IPC overflow/drop risks, serialization copies, and network overhead.
- **Classification:** both are ecosystem/runtime evidence, not new canonical papers.
- **Next:** verify implementation/merge status for #6028/#6212, then SGLang-Omni v0.1.2 MPS-DP/weight-sharing and the next 30-day multimodal SYS census.


### 2026-08-23 20:04 CST — hourly scan
- **Physical AI:** fresh robot-policy/runtime scan completed; no new paper cleared SYS-first promotion threshold.
- **Multimodal / Omni:** fresh 24h/7d + targeted 30d runtime scan completed. vLLM-Omni #6028 remains open; its generic full-duplex control plane (sessions/leases/fences/messages) is already reused by MiniCPM-o 4.5 and PersonaPlex, but the proposed graduation/move has no linked PR yet. vLLM-Omni #6212 remains open; Hop-1 large-video IPC is already POSIX shared-memory based, while binary/compressed remote output and zero-copy colocated transport remain roadmap items.
- **Adjacent substrate watch:** SGLang #35648 proposes same-GPU replicas with managed CUDA MPS, shared weights and a global KV pool; its first draft explicitly excludes multimodal models, so it is tracked as a possible future Omni substrate rather than promoted as a multimodal system.
- **Promotion:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.

### 2026-08-24 07:01 CST — hourly scan
- **Promotion:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- **Physical AI:** independent 24h/7d + targeted 30d systems/runtime scan completed; no new paper cleared the SYS-first threshold.
- **Multimodal / Omni:** vLLM-Omni main/docs are now aligned with vLLM 0.26.0. Production audit found open Cosmos3-Super DLO request-batch-forward correctness debt (#5953) and a v0.26.0 guardrail packaging/startup issue (#5936). SGLang-Omni public releases still show 0.1.0 while production/concurrency hardening continues.
- **Next:** vLLM-Omni v0.26 DLO correctness fixes + SGLang-Omni production gates + fresh 30d Multimodal SYS census; continue Physical-AI state/fleet/evaluation runtime scan.
