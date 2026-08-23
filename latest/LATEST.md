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
