# Changelog

## 2026-09-02 18:02 CST
- Omission recovery added **TeleFuser** as a high-value runtime/project WATCH, not a canonical paper promotion: first-party repo/docs show continuous world-model/multimodal serving with stateful stages, per-session ordering, backpressure/lifecycle cleanup, LiveKit/WebRTC transport and distributed GPU execution.
- LingBot-World v2 already exposes retained multi-session admission and chunk-boundary time slicing; the checked-in ABot-World path preserves KV/RNG/VAE temporal state, while open PR #36 targets multi-session serving.
- No formal TeleFuser arXiv/venue paper was verified, so canonical paper counts remain **161 = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH**. No taxonomy split/merge; Routes 3/5/6/10/11 are strengthened.

## 2026-08-31 12:58 CST
- No new paper promotion after real Physical-AI + Multimodal/Omni 24h→7d scans plus targeted 30d world-model/session/runtime follow-up.
- Added vLLM-Omni **#6672 LingBot World 2.0 Continuous Development Roadmap** as high-value runtime WATCH evidence, not as a paper or shipped feature.
- Route 10 is becoming more concrete around stateful interactive world-model session serving: long-lived request identity, mid-stream interaction, streaming decode, session affinity/backpressure, state/paging and disaggregated diffusion.
- Canonical paper count remains **161 = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH**; public repo stores no PDFs.

## 2026-08-29 01:02 CST
- Recovered **TimelyLLM** (arXiv:2412.18695 / ACM MobiSys 2026) as `CORE_SYS / A+`, Routes 1/3/8. Official MobiSys pages verify **Best Paper Runner-up** and **Best Artifact Runner-up**; the system serves multiple robotic agents via segmented generation and timing-aware scheduling that overlap plan generation with physical execution.
- Added **TypeFly** (arXiv:2312.14950 / IEEE TMC 2025) as `SYS_ALG_BOUNDARY / A`, Routes 3/4/7. Official project/repo verified; current public crawl shows ~110 stars / 25 forks. Kept below CORE_SYS because compact plan representation and runtime design are co-primary.
- Independent Physical-AI and Multimodal/Omni 24h→7d fresh scans plus targeted 30d runtime/session-lifecycle checks completed; no additional fresh paper crossed the SYS-first bar.
- Public canonical count is now **161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH**.

## 2026-08-28 12:00 CST
- Hourly dual-track scan completed with **no paper promotion**: CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- Physical-AI coverage refreshed across fleet/control-loop, edge/resource freshness, runtime recomposition, evaluation infrastructure and world-model/runtime queries; AoL/TWI reverse census found no reusable runtime-backed successor this hour.
- Multimodal/Omni: StreamArena official repo still marks the full StreamMind agent as `coming soon`; SGLang #36690/#36678 remain open correctness/observability frontiers with no verified fix/implementation closure.
- Public canonical count remains **158 works = 114 CORE_SYS / 34 SYS_ALG / 4 ALG / 6 WATCH**.

## 2026-08-28 04:00 CST
- Hourly dual-track scan completed with **no paper promotion**: CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- Physical-AI coverage refreshed across fleet/control-loop, state reuse, runtime recomposition, evaluation infrastructure and world-model/runtime queries; no new SYS-first paper crossed the bar.
- Multimodal/Omni: PinSieve/Pinterest reverse census found no second peer selective-VLM serving/control-plane paper this hour. SGLang #36690 remains issue-scoped backend-correctness evidence for Gemma-3n multimodal serving; no fix/regression-CI closure is claimed.
- Public canonical count remains **156 works = 113 CORE_SYS / 33 SYS_ALG / 4 ALG / 6 WATCH**.

## 2026-08-28 03:00 CST
- Added **PinSieve** (arXiv:2608.24040, **KDD 2026**) to `CORE_SYS / A+`, Routes 8/9/11.
- Taxonomy refinement: selective multimodal serving / cascade routing + governed feedback provenance, staged promotion and rollback.
- Production and offline replay claims remain explicitly source-scoped.

## 2026-08-27 23:00 CST
- Hourly dual-track scan completed with **no paper promotion**: CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- Physical-AI coverage refreshed across fleet/control-loop, edge/device runtime, state reuse, WAM/world-model rollout and evaluation infrastructure; no new SYS-first paper crossed the bar.
- Multimodal runtime evidence: SGLang core issue **#36678**, opened 2026-08-27, requests opt-in coherent per-request latency/generation metrics in OpenAI-compatible responses. It is tracked as Route 8/9/11 observability→routing/scaling feedback evidence, not as a paper or shipped feature.
- Canonical paper count remains **155 works = 112 CORE_SYS / 33 SYS_ALG / 4 ALG / 6 WATCH**. Public radar stores links/metadata only; private PDF state remains 148 valid.

## 2026-08-27 10:00 CST
- Hourly dual-track scan completed with **no paper promotion**: CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- Physical-AI coverage refreshed across fleet/control-loop, edge/device runtime, state reuse, WAM rollout and evaluation infrastructure; no new SYS-first paper crossed the bar.
- Multimodal runtime-adoption evidence refreshed from first-party docs: SGLang-Omni now explicitly documents independent per-stage schedulers, shared inbox/outbox communication and zero-copy shared-memory tensor transfer; vLLM-Omni documents session-oriented WebSocket streaming-video input for Qwen3-Omni with buffered video frames and optional audio chunks.
- These changes strengthen Routes 3/5/11 streaming/session-state and Routes 6/11 stage orchestration; no new paper record or top-level taxonomy branch was created. Public paper count remains **153 works = 110 CORE_SYS / 33 SYS_ALG / 4 ALG / 6 WATCH**.

## 2026-08-27 01:02 CST
- Added **AgenticRobotics** (arXiv:2608.07555) and **DreamLedger** (arXiv:2608.23863) as `SYS_ALG_BOUNDARY / A` after dual-track fresh scan and pending-frontier recovery.
- AgenticRobotics adds durable robot-policy improvement transactions, commit-keyed crash recovery, append-only evidence and artifact-bound capability quality; kept below CORE_SYS because the reference implementation is outer-loop control/evaluation infrastructure rather than an online serving scheduler.
- DreamLedger adds persistent execution-settled world-model credit state, dependency tickets and replayable audit logs; credit gating reduces burned imagination by 62% and replays all 1,062 physical spends. Cross-linked to Routes 5/9/10.
- Both official arXiv PDFs were privately archived and validated; no official implementation repo was independently verified for either paper. Public dataset now tracks **148 works = 108 CORE_SYS / 30 SYS_ALG / 4 ALG / 6 WATCH**.
- Independent Multimodal/Omni scan completed with no new paper-level promotion; request lifecycle, preemption, cancellation/reclamation and failure-path soak remain the active runtime frontier.

## 2026-08-26 19:00 CST
- Added **Physical Agentic AI** (arXiv:2608.22657) as `CORE_SYS / A`, Routes 1/2/7 after fresh robot-crew orchestration/runtime-enforcement recovery.
- New systems branch: **planner knowledge vs physical execution authority**. Typed robot skills/workflow contracts can inform an LLM planner, but deterministic dispatch-time checks still own capability/state/synchronization authorization before actuation.
- Paper evidence: retrieval improves skill grounding 51%→96%, yet informed planners still dispatch 23–29% of faulted steps; deterministic enforcement reports 0% false dispatch with no false blocks and rejects all eight injected live-execution faults before motion.
- Public dataset now tracks **143 works = 105 CORE_SYS / 28 SYS_ALG / 4 ALG / 6 WATCH**. Official PDF remains private; no official implementation repo was verified this run.
- Independent Multimodal/Omni scan completed with no paper-level promotion; request lifecycle/preemption/reclamation and failure-path tracing/soak remain active runtime frontiers.

## 2026-08-26 18:00 CST
- Hourly dual-track scan completed with **no paper promotion**: CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- Physical-AI coverage refreshed across runtime, fleet/control-loop, state/evaluation and heterogeneous deployment; no new SYS-first paper crossed the bar.
- Multimodal/Omni taxonomy refined around **preemptible step-wise execution**: vLLM-Omni #5822 links per-timestep diffusion control to responsive cancellation/progressive output and the existing request-lifecycle/reclamation chain (#6403, #6413/#6439, #6453). #5822 explicitly does not provide cross-request GPU batching.
- SGLang-Omni #1593 remains open after #1595 merged; remaining work is slot-pool failure instrumentation plus comm-layer-triggered soak/CI-nightly.
- Public paper count unchanged at **142 works = 104 CORE_SYS / 28 SYS_ALG / 4 ALG / 6 WATCH**; PDFs remain private to the research workspace.

## 2026-08-26 17:02 CST
- Added **Retriever** (arXiv:2607.17213) as `CORE_SYS / A+`, Routes 2/3/5/7/9 after closed-loop asynchronous-runtime omission recovery.
- Added a temporal programming-model branch for multi-rate Physical AI: stateful modules, explicit clocks, edge synchronization/history-selection policies, replay/debugging and multi-backend execution.
- Official project/repo links added; public repo currently 11 stars / 0 forks / 831 commits. Public dataset now tracks **142 works = 104 CORE_SYS / 28 SYS_ALG / 4 ALG / 6 WATCH**.
- Independent Multimodal/Omni scan completed with no paper-level promotion; lifecycle/reclamation/failure-path runtime tracking continues.

## 2026-08-26 15:00 CST
- Hourly dual-track scan added **PonderPounce** (arXiv:2608.24115) as `SYS_ALG_BOUNDARY / A`: CORE_SYS +0 / SYS_ALG +1 / ALG/WATCH +0.
- Physical-AI significance: slow episode-context MLLM asynchronously refreshes a cognition token while a fast VLA consumes only the latest token plus its age/freshness; reported p50 serving latency is 78 ms cognition refresh + 25 ms action invocation, supporting 20 Hz playback.
- Kept below CORE_SYS because the primary novelty is model/interface design rather than a general scheduler/resource manager; cross-linked to Routes 3/5/7 for control-loop freshness, temporal state and composite MLLM+VLA orchestration.
- Official WoRV repo verified; private official arXiv PDF archived and validated. Public repo stores links only.
- Public dataset now tracks 141 works = 103 CORE_SYS / 28 SYS_ALG / 4 ALG / 6 WATCH.

## 2026-08-26 13:57 CST
- Hourly dual-track scan completed with **no paper promotion**: CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- Physical-AI coverage refreshed across robot-policy/VLA serving, fleet/control-loop, edge/device runtime, state reuse, world-model rollout, evaluation infrastructure and heterogeneous deployment; no new SYS-first paper was verified.
- Multimodal/Omni taxonomy refined around a unified request/session lifecycle branch: request-scoped mutable processor state (#6453), scheduler-owned diffusion request state, persistent session memory (#4480), and full-duplex transactional session/response cleanup are now treated as one state-ownership/reclamation lineage.
- Shared-stage RFC #4108 is cross-linked as a Route 6/11 resource-management frontier because deduplicating encoders/VAEs across pipelines requires request identity, mutable-state isolation, admission, cleanup and failure propagation to remain correct.
- Paper/PDF state unchanged at 140 works and 133 valid private PDFs; public repo stores links only.

## 2026-08-26 13:01 CST
- Hourly dual-track scan completed with **no paper promotion**: CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- Physical-AI coverage refreshed across VLA/robot-policy serving, fleet/control-loop, edge/device runtime, state reuse, world-model rollout, evaluation infrastructure and heterogeneous deployment; no new paper crossed the SYS-first threshold.
- Multimodal/Omni coverage refreshed across serving/composite runtime and request lifecycle. `Aero Realtime` and `ParaJSCC` were audited but kept outside CORE_SYS under current evidence.
- Added vLLM-Omni RFC #6453 as runtime-evolution evidence: runtime-owned request-scoped mutable stage-state lifecycle spanning identity, namespace, terminal commit, cancellation/timeout/failure cleanup, segment continuation, ID reuse and late-work fencing. No generic implementation PR or performance claim yet.
- SGLang-Omni #1593 remains open after #1595 merged; vLLM-Omni #6403 and #6466 remain open with no linked implementation PRs.
- Paper/PDF state unchanged at 140 works and 133 valid private PDFs; public repo stores links only.

## 2026-08-26 11:00 CST
- Hourly dual-track scan completed with **no paper promotion**: CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- Physical-AI coverage refreshed across VLA/robot-policy serving, fleet/control-loop, edge/device runtime, state reuse, world-model rollout, evaluation infrastructure and heterogeneous deployment; fresh hits were canonical, algorithm-led or below SYS-first threshold.
- Multimodal/Omni coverage refreshed across serving, stage/modality disaggregation, composite runtime, request lifecycle and heterogeneous qualification; no new paper-level serving system surfaced beyond canonical M*/HorizonServe/EPD-family work.
- SGLang-Omni #1593 remains open after #1595 merged; slot-pool failure events and comm-layer-triggered soak/CI-nightly remain open evidence gaps. vLLM-Omni #6403 remains open for queued-vs-running status and true cancellation of already-running async-video inference.
- Paper/PDF state unchanged at 140 works and 133 valid private PDFs; public repo stores links only.

## 2026-08-26 10:00 CST
- Hourly dual-track scan completed with **no paper promotion**: CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- Physical-AI coverage refreshed across VLA/robot-policy serving, fleet/control-loop, edge/device runtime, state reuse, world-model rollout, evaluation infrastructure and heterogeneous deployment; fresh hits were canonical or below SYS-first threshold.
- Multimodal/Omni release audit verified **SGLang-Omni v0.1.3** as the latest official release (2026-08-20, `91d4359`). Production-facing shipped changes include Qwen3-TTS admission fast-reject, deterministic inference, weight-share IPC fixes, persistent streaming WebSocket input, breakable prefill CUDA Graph expansion, encoder batching/cache improvements and output-materialization/vocoder overlap.
- Added a heterogeneous full-duplex watch item: vLLM-Omni #6466 requests PersonaPlex support on Intel Gaudi2/HPU with ≥4 sessions, 80 ms cadence, state isolation and an eight-hour stability/HBM soak; no linked implementation PR exists yet, so this is not treated as shipped support.
- Paper/PDF state unchanged at 140 works and 133 valid private PDFs; public repo stores links only.

## 2026-08-26 07:04 CST
- Hourly dual-track scan completed with **no paper promotion**: CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- Physical-AI coverage refreshed across VLA/robot-policy serving, fleet/control-loop, edge/device runtime, state reuse, evaluation infrastructure and world-model rollout; fresh hits were canonical or below the SYS-first threshold.
- Multimodal/Omni coverage refreshed across omni serving, stage/modality disaggregation, composite/any-to-any runtime and official vLLM/SGLang ecosystems; no new paper-level promotion.
- SGLang-Omni #1593 remains open after #1595 merged; slot-pool failure events and comm-layer-triggered soak/CI-nightly policy remain open. #1436 remains open, so V0.1.2 is still behind Qwen3-TTS production gates; #946 remains open for Prometheus-compatible Omni `/metrics`.
- vLLM-Omni #6403 and #6413 remain open around cancellation/status and aborted-output reclamation; no new first-party evidence warranted changing #6439's PR-scoped status in this scan.
- Paper/PDF state unchanged at 140 works and 133 valid private PDFs; public repo stores links only.

## 2026-08-26 05:00 CST
- Hourly dual-track scan completed with **no paper promotion**: CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- Physical-AI coverage refreshed across serving/runtime, fleet/control-loop, state and evaluation infrastructure; no new SYS-first paper promotion.
- Multimodal/Omni Rollplex/ROLL reverse census found adjacent VeRL-Omni runtime evidence, but no verified online-serving adoption of Rollplex cross-phase scheduling, phase-aware HBM residency or TP-layout-aware physical weight sharing.
- Production lifecycle remains open around vLLM-Omni #6403 cancellation/status and #6413 aborted-output reclamation; v0.28.0 remains due 2026-08-30 at the latest indexed 50/129 closed snapshot.
- Release-state guard tightened: the first-party releases page fetched in this run is stale and cannot safely confirm a final 0.27.x cut, so the radar keeps the directly verified `v0.27.0rc1` as the durable release datum until a fresh tag/release endpoint is resolved.
- Paper/PDF state unchanged at 140 works and 133 valid private PDFs; public repo stores links only.

## 2026-08-26 00:00 CST
- Hourly dual-track scan completed with **no paper promotion**: CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- Physical-AI coverage refreshed across VLA/robot-policy serving, fleet/control-loop, world-model rollout, state reuse, edge/device deployment and evaluation infrastructure; fresh hits were canonical or below the SYS-first threshold.
- Multimodal/Omni coverage independently refreshed across MLLM/Omni serving, stage/modality disaggregation, composite/any-to-any runtime and official vLLM/SGLang ecosystems; no new paper-level promotion.
- Boundary guard preserved: agent-learning architectures and generic LLM/MoE serving remain outside CORE_SYS unless they expose direct Physical-AI/Multimodal runtime, scheduling, resource-management or infrastructure evidence.
- Paper/PDF state unchanged at 139 works and 132 valid private PDFs; public repo stores links only.

## 2026-08-25 21:04 CST
- Hourly dual-track scan completed: **CORE_SYS +0 / SYS_ALG_BOUNDARY +1 / ALG +0 / WATCH +0**.
- Added **Edge-Native Embodied Intelligence for Action-Aware Wireless Edge Networks** (arXiv:2608.17774) as `SYS_ALG_BOUNDARY / A-`, Routes 4/6/8. It contributes action-aware wireless-edge/embodied co-design mechanisms but remains below CORE_SYS because current evidence is framework/case-study oriented rather than a mature serving runtime.
- Audited **FleetSieve** (arXiv:2608.19659) and intentionally excluded it from canonical scope: generic LLM GPU/replica fleet configuration is not robot-fleet serving, and no multimodal workload was verified.
- Private official PDF archived and validated at 3,297,504 B; public repo contains links only. Current public paper count: 139.
- Multimodal/Omni scan completed with no paper promotion; vLLM-Omni #6403/#6413/#6083 remain open frontiers in current first-party evidence.

## 2026-08-25 18:01 CST
- Hourly dual-track scan completed: **CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH_ONLY +1**.
- Added **HODAgent (arXiv:2608.17584)** to WATCH_ONLY rather than SYS: the work is system-oriented (semi-duplex System-2 runtime, asynchronous execution/cancellation, persistent task state, shared embodiment contract), but its arXiv listing was withdrawn on 2026-08-20 for mandatory company internal review; no official repo was verified and the official PDF endpoint is unavailable.
- Reconciled a durable/public bookkeeping drift: canonical manifest already contained PhyAgentOS, so the actual pre-run private state was 137 works / 103 CORE_SYS rather than 136/102, and the private PDF manifest was already 131 valid PDFs. Public `data/papers.json` was also behind and is now reconciled.
- Current paper state: **138 = 103 CORE_SYS / 25 SYS_ALG / 4 ALG / 6 WATCH**. Private PDF state: 131 valid; Eevee/ROSGM/TILDE remain legal-source debt and HODAgent is pending only for an official re-release.
- Multimodal/Omni scan completed with no paper promotion; vLLM-Omni #6413/#6403/#6083 and v0.28.0 release hardening remain active frontiers.

## 2026-08-25 16:01 CST
- Hourly dual-track scan completed with **no paper promotion**: CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- Physical-AI coverage refreshed across VLA/robot-policy serving, fleet/control-loop, state reuse, evaluation infrastructure, world-model rollout and heterogeneous deployment; no new SYS-first promotion.
- Multimodal/Omni runtime taxonomy refined around same-GPU replica sharing: SGLang-Omni `main` documents managed CUDA-MPS colocation, CPU/NUMA pinning, per-replica KV sizing and optional CUDA-IPC weight sharing. Pinned TTS profiles report roughly 1.4–2.1× tuned single-replica throughput in saturated DP2/DP3 configurations; documented follower weight savings span about 1.51–17.05 GiB depending on model.
- Evidence boundary preserved: `WEIGHT_SHARE=1` is opt-in/configuration-gated; plain MPS-DP is distinct. Stateful preprocessing/vocoder/codec processes remain replica-private where streaming state must not be shared.
- vLLM-Omni #6403/#6413 remain open; SGLang-Omni #1593 remains open and continues to reference #1595 for 14 trace events, while independent merge/release status is not yet verified.
- No new PDF; private legal-source debt remains Eevee / ROSGM / TILDE.

## 2026-08-25 14:02 CST
- Hourly dual-track scan completed with **no paper promotion**: CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- Physical-AI coverage refreshed across VLA/robot-policy serving, fleet/control-loop, state reuse, evaluation infrastructure, world-model rollout and heterogeneous deployment; no new SYS-first promotion.
- Multimodal/Omni revalidation: current indexed evidence still exposes the historical vLLM-Omni #6426 continuous-request OOM/audio-correctness failure record even after merged #6458. Keep #6458 scoped to long-form Talker repetition/EOS/length remediation until fresh post-merge CI confirms continuous-request memory/correctness behavior.
- SGLang-Omni #1593 remains open and says #1595 implements 14 paged-KV/transport/direct-IPC trace events; slot-pool failure events plus comm-layer-triggered soak/CI policy remain open, and independent #1595 merge/release status is still unconfirmed.
- No new PDF; private legal-source debt remains Eevee / ROSGM / TILDE.

## 2026-08-25 12:59 CST
- Hourly dual-track scan completed with **no paper promotion**: CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- Physical-AI coverage refreshed across VLA/robot-policy serving, fleet/control-loop, state reuse, evaluation infrastructure, world-model rollout and heterogeneous deployment; fresh hits were canonical or below threshold.
- Multimodal/Omni runtime status changed: vLLM-Omni #6426 is now **closed** and links to merged PR #6458 (merged 2026-08-22). The merged fix restores request-local 16-frame repetition penalty semantics, forced EOS after `min_tokens`, and caps offline Talker generation to `min(2048, remaining context)`. Because #6426 bundled OOM plus multiple audio-correctness symptoms, continuous-request memory/correctness remains a revalidation item rather than being assumed fully solved.
- SGLang-Omni #1593 remains open and states #1595 implements 14 paged-KV/transport/direct-IPC trace events; independent merge/release status is still unconfirmed, while slot-pool failure events and CI/nightly soak integration remain open work.
- No new PDF; private legal-source debt remains Eevee / ROSGM / TILDE.

## 2026-08-25 11:58 CST
- Hourly dual-track scan completed with **no paper promotion**: CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- Physical-AI coverage refreshed across VLA/robot-policy serving, fleet/control-loop, state reuse, evaluation infrastructure, world-model rollout and heterogeneous deployment; fresh hits were canonical or below threshold.
- Multimodal/Omni update: SGLang-Omni #1593 remains the primary first-party reference for failure-path observability + soak testing. It documents missing paged-KV tracing, invisible transport fallback risk and missing direct-IPC consumer events; the issue states #1595 adds 14 trace events for these gaps, while slot-pool failure events and CI/nightly soak policy remain follow-up work.
- Reference soak evidence remains 8 hours / two H200 / Qwen3-Omni-30B / 4,764 requests / 3,510,175 slot allocations; low peak pool occupancy means this is not leak-freedom proof.
- No new PDF; private legal-source debt remains Eevee / ROSGM / TILDE.

## 2026-08-25 10:02 CST
- Hourly dual-track scan completed with **no paper promotion**: CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- Physical-AI coverage refreshed across VLA/robot-policy serving, fleet/control-loop, state reuse, evaluation infrastructure, world-model rollout and heterogeneous deployment; fresh hits were canonical or below threshold.
- Multimodal/Omni runtime watch: vLLM-Omni #6403/#6413/#6426 and #6083 remain active lifecycle/control-plane debt.
- New observability evidence: SGLang-Omni #1593 documents success-path-heavy comm tracing, missing failure/paged-KV/transport-fallback visibility, and reports an 8-hour Qwen3-Omni-30B two-H200 soak with 4,764 requests and 3,510,175 slot allocations. Track #1595 and soak integration as production observability/leak-testing infrastructure, not a paper promotion.
- No new PDF; private legal-source debt remains Eevee / ROSGM / TILDE.

## 2026-08-25 02:00 CST
- Hourly dual-track scan completed with **no paper promotion**: CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- Physical-AI coverage refreshed across VLA/robot-policy serving, fleet/control-loop, state reuse, evaluation infrastructure, world-model rollout and heterogeneous deployment; fresh hits were canonical or below threshold.
- Multimodal/Omni runtime watch: vLLM-Omni #6426 continuous-request MiniCPM-o 4.5 OOM/correctness, #6403 async-video status/cancellation, and #6455 CosyVoice3 streaming TTS device/state consistency remain active production-hardening signals.
- vLLM-Omni `v0.28.0` milestone is due 2026-08-30; current indexed snapshot shows 50/129 issues closed (38%). No release-complete claim is made.
- No new PDF; private legal-source debt remains Eevee / ROSGM / TILDE.

## 2026-08-24 23:04 CST
- Hourly dual-track scan completed with **no paper promotion**: CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- Physical-AI coverage refreshed across VLA/robot-policy serving, runtime/state/evaluation and heterogeneous deployment; fresh hits were canonical or below threshold.
- Multimodal/Omni runtime watch: vLLM-Omni #6413 and linked fix PR #6439 remain open in current first-party indexed evidence; #6403 async-video cancellation/status semantics also remain open. No shipped reclamation/cancellation behavior is claimed.
- No new PDF; private legal-source debt remains Eevee / ROSGM / TILDE.

## 2026-08-24 22:05 CST
- Added **Decoding Task Progress from VLA Representations** (arXiv:2608.13474) to `SYS_ALG_BOUNDARY / A-`, Routes 3/8/9.
- Boundary rationale: its linear progress probe provides useful deploy-time VLA observability and label-free stalled-progress/OOD detection, but it is a monitoring/probing method rather than a serving/resource scheduler.
- Independent Physical-AI and Multimodal/Omni 24h→7d scans plus targeted 30d checks completed; no Multimodal paper promotion this pass.
- Runtime watch remains focused on vLLM-Omni #6413/#6439 output reclamation and #6403 async-video cancellation/status semantics.
- Public repo contains metadata/links only; the official PDF was archived privately and validated on the research server.

## 2026-08-24 16:00 CST
- Added **WCM: World-Cognition Model for Generalizable Human-Robot Interaction** (arXiv:2607.22999; RSS 2026 Workshop on Human-centric Mobile Manipulation) to `SYS_ALG_BOUNDARY / A`, Routes 2/3/5/7.
- Reason for boundary placement: asynchronous sensing/reasoning/control/memory runtime and stale-context validation are system-relevant, but the central novelty remains embodied-agent/HRI architecture and teaching rather than serving/resource scheduling.
- Multimodal runtime watch: vLLM-Omni #6403 exposes async-video lifecycle gaps where queued requests may be labeled `IN_PROGRESS` and deleting an already-running task does not terminate GPU inference; tracked with #6413/#6439 cancellation/reclamation work.
- Private PDF archive gained the official WCM arXiv PDF; public repo still contains links/metadata only.

## 2026-08-24 14:00 CST
- No canonical paper promotion after independent Physical-AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime checks.
- vLLM-Omni #6439 (fix for #6413) verified open/not merged; current PR adds aborted-request orphan-output reclamation, shutdown cleanup, and cancelled/done-waiter handling. Treat as PR-scoped runtime evidence until merge.
- vLLM-Omni #6158 remains open with no linked implementation PR; no shipped TTS missing-EOS/repetition safeguard is claimed.
- SGLang-Omni #1608 updated 2026-08-23: Qwen3-TTS KDA reproduction rebased to current main, compile parity closed, Talker `torch.compile` removed after no reproducible end-to-end gain, CUDA Graph retained, and 204 directly affected tests passed.
- PDF state unchanged: 128 valid, 0 invalid; remaining legal debt Eevee/ROSGM/TILDE.

## 2026-08-24 09:03 CST
- Added **On the Limitations of Non-GPU AI Accelerators for Large-Model Inference** (arXiv:2607.08215) to `CORE_SYS / A`, Routes 6/8/11, after heterogeneous-serving omission recovery.
- Verified official arXiv metadata and companion repository; the study documents real MoE + multimodal serving on 16 Huawei Ascend 910 devices, 12 source-level integration patches, and eight classes of platform/runtime limitations.
- Added production-runtime watch evidence from vLLM-Omni #6426 (continuous-request OOM/correctness failures) and SGLang-Omni #1470 (concurrent Whisper scheduler crash); no separate paper promotion for these issues.
- PDF download remains pending after full97 TLS/network failures; no false download claim.
- GitHub remote push is still pending because the existing SSH path currently returns `Permission denied (publickey)`; local changes are committed before the next retry.

## 2026-08-20 17:58 CST
- Initialized the public Physical AI Serving Radar with a SYS-first ten-route research map.
- Published curated `CORE_SYS`, `SYS_ALG_BOUNDARY`, and watchlist views plus machine-readable data.
- Added five recovered `CORE_SYS` anchors: ROSGM, TILDE, FogROS 2, FogROS2-Config, and FogROS2-PLR.
- Refined the edge/cloud lineage into **provision/deploy → configuration selection → probabilistic latency/reliability management**.
- Recorded fresh 24h/7d scans as complete with no additional high-value promotion; 30d/historical omission recovery remains active.

The public repository intentionally excludes paper PDFs, private machine paths, logs, credentials, and other server-specific state.

## 2026-08-20 19:01 CST
- Added FogROS2-SGC (IROS 2023) to CORE_SYS after official project/code verification.
- Continued FogROS systems-lineage omission recovery; no new 24h/7d promotion.

- 2026-08-20 20:00 CST: Added FogROS2-LS to CORE_SYS; audited ros2_benchmark as infrastructure artifact; fresh 24h/7d scan complete.

## 2026-08-20 21:03 CST
- Fixed a public machine-readable sync lag by adding the already-classified FogROS2-LS record to `data/papers.json`.
- Added the DistInSys/ISCC 2025 Best Paper on ROS 2 Zenoh-vs-VPN edge-cloud networking as `WATCH_ONLY`: useful deployment evidence, but not a new runtime mechanism.
- Fresh 24h/7d SYS-first scans completed with no new promotion; Zenoh/DDS state-continuity omission recovery remains active.

- 2026-08-21 00:57 CST — Hourly systems scan: no classification changes; revalidated Armory end-to-end fleet policy-serving artifact and continued Zenoh/DDS timing/state-continuity coverage.

## 2026-08-21 03:01 CST
- Added **LeRobot** (ICLR 2026, arXiv:2602.22818) to `CORE_SYS` after policy-server/runtime omission recovery.
- Systems role: generalized remote asynchronous inference via gRPC `PolicyServer`/`RobotClient`, action queues, overlapping action-chunk aggregation and configurable refresh thresholds; this is deployment/runtime infrastructure rather than a VLA algorithm-speedup entry.
- Official repository adoption checked at **26,783 stars / 5,431 forks**.
- Public radar now contains **97 verified works / 73 CORE_SYS**; no PDFs or private server state are mirrored.

## 2026-08-21 05:02 CST
- Added **RobotFleet** (RSS 2025 Scalable and Resilient Multi-Robot Systems Workshop, arXiv:2510.10379) to `CORE_SYS` routes 1/7.
- Role: containerized fleet execution substrate with centralized planner/allocator, task-status/schedule manager, shared declarative world state, feedback and replanning; complements Armory/ROSA rather than duplicating inference scheduling.
- Revalidated vLLM-Omni OpenPI as a reusable stateful robot-serving API with per-connection sessions, handshake metadata, reset/session operations and a serving bridge for batching/streaming/serialization.
- Public radar now contains **98 verified works / 74 CORE_SYS**.

- 2026-08-21 06:01 CST — Added HELIOS heterogeneous VLA serving submission to WATCH_ONLY; fresh scan found no new promotion.

## 2026-08-21 06:57 CST
- Added **HeyGen HELIOS** as `CORE_SYS / A+` under heterogeneous/composite multimodal infrastructure.
- Added explicit HELIOS name-collision note versus the EuroSys 2027 VLA-serving submission watch item.
- Public dataset now contains 100 verified works.

### 2026-08-21 08:04 CST
- **CORE_SYS +1:** [HydraInfer](https://arxiv.org/abs/2505.12658) — historical adjacent-multimodal SYS omission recovery: hybrid Encode-Prefill-Decode disaggregation, heterogeneous stage placement/resource reallocation, and stage-level batching.
- arXiv v2 reports up to **4x throughput** over vLLM on an 8xH800 node while meeting the 90th-percentile request SLO.
- Fresh 24h/7d Physical-AI serving scan produced no direct promotion; planner/fleet/world-state and multimodal SYS omission recovery continues.
- Public state: **101 verified works / 76 CORE_SYS / 16 SYS_ALG / 4 ALG / 5 WATCH**.
## 2026-08-21 09:00 CST
- Added **JoyNexus** (`CORE_SYS/A+`) as the radar's multi-tenant VLA service/runtime anchor.
- Added **FlashCodec + UnifiedServe** (`CORE_SYS/A+`) for GPU-internal multimodal stage scheduling/resource sharing.
- Refined the research map with multi-tenant VLA service substrates and logical-disaggregation/physical-sharing MLLM execution.
- Public dataset now contains 103 verified records; no private PDF archive or server-local metadata is mirrored.


## 2026-08-21 10:00 CST
- Added arXiv:2606.27962 as `CORE_SYS / A-` through same-group omission recovery.
- Refined Route 9 to explicitly include cloud-native embodied simulation/evaluation infrastructure under strict systems criteria.
- Refreshed public machine-readable dataset to 104 verified works.

## 2026-08-21 11:00 CST
- Added D-VLA (arXiv:2605.13276) as  via JoyNexus/RL-VLA3 same-group omission recovery.
- Refreshed public machine-readable dataset to 105 verified works / 80 CORE_SYS.

## 2026-08-21 12:00 CST
- Added RL-VLA3 (arXiv:2602.05765v2) as `CORE_SYS / A+` through historical same-group omission recovery.
- Added version-scoped metric note to avoid mixing the current arXiv v2 with the earlier ICLR 2026 SPOT Workshop version.
- Refreshed public machine-readable dataset to 106 verified works.

- 2026-08-21 14:04 CST — Added HELP (arXiv:2607.09776) to SYS_ALG_BOUNDARY; refreshed fleet/post-training omission coverage.

- 2026-08-21 15:03 CST — Added CoMuRoS to CORE_SYS (A-, Routes 1/7) after fleet/composite-runtime omission recovery; refreshed hourly coverage.

## 2026-08-21 16:04 CST
- Added **SOP** (arXiv:2601.03044) to `CORE_SYS / A+` as a missing fleet/cloud actor-learner systems anchor for online VLA post-training.
- Added **Learning while Deploying (LWD)** (arXiv:2605.00416v2) to `SYS_ALG_BOUNDARY / A`: substantial fleet deployment infrastructure, but algorithmic novelty remains central.
- Refined Route 1 to include deployment-to-learning actor/learner loops and asynchronous shared-policy synchronization alongside inference-serving/fleet-scheduling systems.
- Public dataset updated to **110 verified works / 83 CORE_SYS / 18 SYS_ALG_BOUNDARY / 4 ALG / 5 WATCH**.
## 2026-08-21 17:01 CST
- Added RLinf-VLA and RLinf-USER as `CORE_SYS / A+` after RLinf lineage omission recovery.
- Updated public dataset to 112 records / 85 CORE_SYS.
- Added taxonomy note for robots as first-class schedulable resources and embodied-learning infrastructure.


- **2026-08-21 18:00 CST** — Recovered missing OSDI 2026 RLinf base-system paper into CORE_SYS; refreshed public dataset to 113 records. DynaRL verified as adjacent systems evidence but not promoted without embodied/Multimodal evaluation.
- **2026-08-21 19:03 CST** — Hourly SYS-first scan found no new promotion. Updated DynaRL ecosystem evidence: RLinf v0.3 explicitly integrates it as the framework's dynamic-scheduling feature, while the paper itself remains outside the Physical-AI canonical list until direct embodied/VLA evaluation is verified.
- **2026-08-21 20:00 CST** — Added **multipanda_ros2** (ICRA 2026, arXiv:2602.02269) to `CORE_SYS / A`, Routes 2/3/9; refined the map with a real-time multi-robot control-runtime branch; public dataset now contains **114 works / 87 CORE_SYS**.


- 2026-08-21 21:05 CST — Hourly heartbeat: no promotion; refreshed TUM/Haddadin multi-robot runtime, fleet-SLO, persistent-state, and middleware timing/isolation coverage; strengthened multipanda_ros2 runtime-role evidence.
- 2026-08-21 21:57 CST — Hourly heartbeat: no paper promotion; added **Strands Robots** as deployment/runtime ecosystem evidence after verifying Zenoh fleet mesh, ROS2/RTPS, remote WebSocket policy serving, LeRobot gRPC async inference, persistent policy workers, and v0.5.0 release status. Canonical paper counts unchanged.

## 2026-08-22 02:00 CST
- New CORE_SYS: OSDAG (arXiv:2606.15255), A-, Routes 1/7. Constraint-aware online scheduler consumes an LLM-generated dependency/resource DAG and dispatches ready tasks to idle heterogeneous robots; reports 5-15x faster reasoning and up to 38% makespan reduction.
- Fresh 24h/7d scan found no newer direct promotion; OSDAG came from historical omission recovery.
- Public canonical state: 115 works / 88 CORE_SYS / 18 SYS_ALG_BOUNDARY / 4 ALG / 5 WATCH.
- Next: OSDAG references/same-group -> stronger fleet admission/fairness/deadline/SLO -> PCS/WorldMove -> Zenoh/DDS enforcement -> HELIOS monitor.

## 2026-08-22 04:03 CST
- Added **Sirius-Fleet** (CoRL 2024 / PMLR 270, arXiv:2410.22689) to `SYS_ALG_BOUNDARY / A` after fleet-runtime omission recovery.
- Verified official PMLR proceedings, UT Austin RPL project page, and `UT-Austin-RPL/sirius-fleet` code repository.
- Classified as a fleet deployment/runtime-monitoring boundary work rather than CORE_SYS because interactive monitoring/learning remains the primary novelty.
- Public dataset updated to **116 works / 88 CORE_SYS / 19 SYS_ALG_BOUNDARY / 4 ALG / 5 WATCH**.

## 2026-08-22 07:02 CST
- Added OpenBot-Fleet (ICRA 2024) as CORE_SYS/A+ after historical omission recovery.
- Added fleet experience-streaming / continuous policy lifecycle coverage.

## 2026-08-22 08:12 CST — repository dual-track restructure
- Promoted **Multimodal / Omni Efficient Serving** from an adjacent appendix into a first-class track alongside **Physical AI Serving**.
- Kept both tracks in the same repository but separated their narratives, taxonomies, and reading lists.
- Added `physical_ai/README.md` and `physical_ai/CORE_READING.md`.
- Added `multimodal/README.md` and `multimodal/CORE_READING.md`.
- Split taxonomy into `PHYSICAL_AI_MAP.md` and `MULTIMODAL_MAP.md`, plus `CROSSOVER.md` for shared systems/technical lineage.
- Preserved one shared `data/papers.json` as the metadata source of truth to avoid duplicate or drifting paper records.
- Rewrote the repository homepage to expose both tracks equally and independently.

## 2026-08-22 11:05 CST
- Hourly SYS-first scan found no new paper promotion.
- Updated vLLM-Omni ecosystem evidence: RFC #6168 reports DreamZero-DROID served end-to-end through the OpenPI robot endpoint on 2×MI300X/ROCm with 34 closed-loop rollouts, extending robot-policy serving beyond the CUDA-only path.
- RFC #6069 and pi0/pi0.5 model integration remain open; tracked as serving-contract / cross-vendor deployment progress rather than a separate paper entry.

## 2026-08-22 12:03 CST
- Completed fresh 24h/7d plus targeted 30d SYS-first scan; no new paper promotion.
- Revalidated vLLM-Omni RFC #6069/#6168 as still-open contract/evaluation work and preserved the distinction between end-to-end rollout evidence and task success-rate evidence.
- Rechecked fleet-SLO and persistent world-state runtime routes; no taxonomy split or priority change was warranted.

## 2026-08-22 14:01 CST
- Completed fresh 24h/7d plus targeted 30d SYS-first scan; no paper promotion.
- Added a runtime/ecosystem milestone: vLLM-Omni `main` now documents an executable LeRobot π0 robot-policy serving path over `/v1/realtime/robot/openpi`, including `policy_server_config` handshake metadata, action-shape semantics, e2e tests and LeRobot parity validation.
- Kept this as vLLM-Omni runtime evolution rather than a new canonical paper; next watch points are π0.5/generalized realtime serving, streaming structural state, fleet SLO scheduling and persistent world-state migration.

## 2026-08-22 15:00 CST
- Hourly SYS-first scan found no new paper promotion.
- Added a public watch note for vLLM-Omni's iterative state/scheduling direction: per-request persistent state, independent RNG/request identity under mixed batches, explicit state cleanup, and resumable chunk-level EDF/preemption.
- Kept the evidence at runtime/ecosystem level; no canonical paper counts or taxonomy routes changed.

## 2026-08-22 16:01 CST
- Completed fresh 24h/7d plus targeted 30d SYS-first scan; no canonical paper promotion.
- Added vLLM-Omni RFC #6231 as runtime/cache ecosystem evidence: node-local DLO runtime mmap-cache compatibility is explicitly defined across DP/TP/SP using final host-weight-layout equivalence.
- Rechecked ROSGM/TILDE legal full-text routes; both remain closed/request-only, so public paper counts and private PDF inventory are unchanged.

## 2026-08-22 17:01 CST
- Completed fresh 24h/7d plus targeted 30d SYS-first scan; no canonical paper promotion.
- Corrected an implementation-status ambiguity in the vLLM-Omni ecosystem: RFC #6168 still shows π0/π0.5 as proposed, while current `main` already includes executable LeRobot π0 online serving over `/v1/realtime/robot/openpi`.
- Treat current mainline as the stronger π0 implementation-status source; π0.5/generalized realtime serving remains an active watch item rather than inferred support.

## 2026-08-22 17:57 CST
- Completed fresh 24h/7d plus targeted 30d SYS-first scan; no canonical paper promotion.
- Clarified π0.5 status: current public contract/tracker evidence still treats PR #4419 as WIP with an opt-in `realtime_triton_prefix`; generalized π0.5 realtime serving is not yet verified as mainline-stable.
- RFC #6069 explicitly defers longer-lived camera/robot-action structural updates to #5120; keep that state path as future contract work rather than current robot-policy serving capability.

## 2026-08-22 18:58 CST
- Completed fresh 24h/7d plus targeted 30d SYS-first scan; no canonical paper promotion.
- Corrected π0.5 implementation status: vLLM-Omni PR #4419 was closed on 2026-08-18 with no merged marker. Keep its `realtime_triton_prefix` implementation and latency numbers PR-scoped, not mainline-stable evidence.
- RFC #5120 remains open; structural streaming data updates are still explicitly outside Robot Policy Serving Contract RFC #6069 Phase 1.

## 2026-08-22 21:02 CST
- Completed fresh 24h/7d plus targeted 30d SYS-first scan; no canonical paper promotion.
- Revalidated current vLLM-Omni robot-serving boundary: π0 is executable in mainline, while no indexed successor to the closed π0.5 PR #4419 was found and RFC #6069 remains open.
- Rechecked legal full-text routes for Eevee, ROSGM, and TILDE; no new open copy was resolved, so private PDF status remains unchanged.

## 2026-08-22 22:00 CST
- Completed fresh 24h/7d plus targeted 30d SYS-first scan; no canonical paper promotion.
- Refined vLLM-Omni RFC #5120 status: the frontend prerequisite (`OmniTextPrompt` + generic `interaction` event) is already marked done, while the core structural-data routing/scheduling, per-request state, chunk-boundary application and model-specific processor work remain open.
- Kept the serving boundary conservative: RFC #6069 still excludes #5120 from Phase 1, and no successor to closed π0.5 PR #4419 was found.

## 2026-08-22 23:00 CST
- Completed fresh 24h/7d plus targeted 30d SYS-first scan; no canonical paper promotion.
- Added vLLM-Omni RFC #6195 as runtime/cache ecosystem evidence: DLO host-weight storage is being decoupled from DP request scheduling via `HostWeightPlan` and fail-closed runtime-layout compatibility.
- Kept paper counts/taxonomy unchanged; no new robot-specific admission/SLO scheduler or stable π0.5 successor was verified.

## 2026-08-23 00:01 CST
- Completed fresh 24h/7d plus targeted 30d SYS-first scan; no canonical paper promotion.
- Upgraded vLLM-Omni DLO implementation status: RFC #6195 now records **Phase A merged** via PR #6213 (`HostWeightPlan`, fail-closed direct checkpoint mmap, bounded no-AllGather staging) for TP=1.
- Phase B under RFC #6231 remains open for normalized node-local runtime mmap-cache sharing across equivalent DP/TP/SP host-weight layouts; request scheduling/admission/batching remain explicit non-goals.
- Kept canonical paper counts/taxonomy unchanged; next watch point is whether the Phase-B cache substrate is actually exercised by robot-policy/world-model deployments.

## 2026-08-23 01:00 CST
- Completed fresh 24h/7d plus targeted 30d SYS-first scan; no canonical paper promotion or taxonomy change.
- Rechecked vLLM-Omni DLO Phase B: RFC #6231 remains open and no new indexed implementation PR beyond merged Phase-A PR #6213 was found; request scheduling/batching/orchestration remain out of scope.
- Rechecked robot-policy/runtime frontier: mainline π0 remains executable, RFC #6069 remains open, no indexed successor to closed π0.5 PR #4419 was found, and RFC #5120 core structural-state engine/request-state work remains unfinished.
- HELIOS heterogeneous lightweight VLA serving remains a EuroSys 2027 submission watch item with no public preprint/repo found in this scan.


## 2026-08-23 02:02 CST
- CORE_SYS +2: Execution-State Capsules / FlashRT (arXiv:2606.20537, A+, Routes 3/5/6) adds graph-bound complete execution-state checkpoint/restore/fork/rollback for latency-first on-device Physical-AI serving; PhAIL (arXiv:2605.29710, A, Routes 8/9) adds open real-robot VLA evaluation infrastructure with distributional time-to-success, Human-Relative Throughput, confidence intervals, significance testing and per-rollout artifacts.
- Fresh 24h/7d scan: no newer direct SYS promotion; both additions are historical omission recovery.

## 2026-08-23 03:00 CST
- Added **dWorldEval** (arXiv:2604.22152, ICML 2026 Spotlight) to `SYS_ALG_BOUNDARY / A+`, Routes 9/10, as a scalable world-model policy-evaluation proxy.
- Added **Hi-WM** (arXiv:2604.21741) to `SYS_ALG_BOUNDARY / A`, Routes 5/9/10, as rollback/branching world-state reuse evidence for corrective post-training.
- Refined P5/P9/P10 to distinguish complete execution-state reuse, world-model proxy evaluation, and cached rollback/branching workloads from true serving/resource-management systems.
- FlashRT adoption rechecked at 486 stars / 60 forks / 508 commits in the current public crawl. Public dataset updated to **121 verified works / 91 CORE_SYS / 21 SYS_ALG_BOUNDARY / 4 ALG / 5 WATCH**.

## 2026-08-23 04:02 CST
- Added RoboChallenge (arXiv:2510.17950) to CORE_SYS/A+ as public online real-robot evaluation infrastructure.
- Updated P9 representative anchors and machine-readable paper count to 122.
- Fresh 24h/7d scan completed with no newer direct SYS promotion.


## 2026-08-23 05:02 CST
- Added **Thea / Towards the Harness of Embodied Agents** (arXiv:2608.11246) to `CORE_SYS` (A; P2/P5/P7).
- Added official project/repo links and embodied-agent harness/runtime branch to the research map.
- Updated public dataset to 123 verified records and refreshed hourly coverage heartbeat.

## 2026-08-23 05:57 CST
- Completed fresh 24h/7d plus targeted 30d SYS-first scan; no canonical paper promotion or taxonomy-count change.
- Upgraded public ecosystem evidence for **Execution-State Capsules / FlashRT**: official serving docs now show capsules used for fresh sessions, branch/fork, restart/resume, non-hot workers and pinned shared prefixes, with Nexus connecting the native C++ Pi0.5 runtime ABI to embedded robot loops, HTTP serving and execution-state capsules.
- Kept this as adoption/runtime evolution of the existing CORE_SYS paper rather than creating a duplicate entry.

## 2026-08-23 07:00 CST
- Completed fresh 24h/7d plus targeted 30d SYS-first scan; no canonical paper promotion or taxonomy-count change.
- Refreshed FlashRT serving evidence: complete execution-state capsules are now documented as practical session/branch/restart primitives above the fixed execution ABI, with bounded request queues kept in the serving layer.
- Refreshed PhAIL production-evaluation adoption: the public leaderboard currently exposes **1,083 real-robot episodes** and a unified real/sim evaluation workflow with per-run video and telemetry artifacts.

## 2026-08-23 08:00 CST
**New CORE_SYS:** Zetta ζ / Z-Infra (arXiv:2608.16590, A+, routes 2/3/6/7/9). Closed-loop embodied harness with action-frequency governance and heterogeneous rollout infrastructure. Official repo verified (~60 stars in current crawl). Fresh 24h/7d scan completed; next: Z-Infra implementation and resource/scheduling comparison with Thea/Embodied.cpp/XPolicyLab.

## 2026-08-23 10:02 CST
- Fresh 24h/7d plus targeted 30d SYS-first scan completed; no canonical paper promotion.
- Deepened Zetta/Z-Infra artifact evidence: public repo exposes campaign queues/workers, capacity probes, deployment/preflight orchestration, LIBERO VLA client/server and RoboCasa environment-farm/provider-broker components.
- Preserved a strict evidence boundary: full Z-Infra remains marked as coming soon, so scheduler/fairness/resource-isolation/fault-tolerance mechanisms are not inferred beyond the released code.

## 2026-08-23 11:02 CST
- Added **RoboLab** (RSS 2026, arXiv:2604.09860) to `CORE_SYS` (A+, P9).
- Recorded NVIDIA's reusable simulation-evaluation runtime: policy server/client, automatic success detection, multi-env parallel evaluation, faithful replay/dashboard and active Apache-2.0 releases.
- Public dataset updated to 125 verified records / 95 CORE_SYS.

## 2026-08-23 13:00 CST
- Added ROBOGATE to SYS_ALG_BOUNDARY with correction-aware evidence status.
- Recorded the 2026-07-18 official validity correction so retracted VLA comparison numbers cannot silently re-enter the radar.
- Updated public dataset to 126 verified records.

## 2026-08-23 14:00 CST

**Coverage:** 24h + 7d fresh scan; targeted 30d omission recovery.

**New CORE_SYS:** AEROS (arXiv:2604.07039) and Harnessing Embodied Agents: Runtime Governance for Policy-Constrained Execution (arXiv:2604.07833). AEROS adds a persistent-agent / installable-capability runtime abstraction; Runtime Governance externalizes admission, policy enforcement, monitoring, rollback, and human override.

**Evidence boundary:** AEROS has an Apache-2.0 runtime MVP, but its current public implementation is single-process/single-thread, mock-robot, and has no real-time guarantees; do not overstate production maturity.

- 2026-08-23 15:03 CST — Added FSAR, Governed Capability Evolution, and EmbodiedGovBench from AEROS research-program omission recovery; next: ECM Contracts/artifact audit.

## 2026-08-23 16:00 CST
- Added **ECM Contracts** (arXiv:2604.13097) to `CORE_SYS / A-`, Routes 2/5/7, after verifying implemented registry/resolver/contract-checker infrastructure and pre-deployment compatibility enforcement.
- Preserved maturity boundary: no official public implementation repository was verified in this scan.
- Reconciled public dataset to **132 verified works / 101 CORE_SYS / 22 SYS_ALG / 4 ALG / 5 WATCH**.
- Fresh 24h/7d SYS-first scan completed with no newer direct serving/runtime promotion.

## 2026-08-23 17:00 CST
- Hardened the radar into an explicit **dual-track hourly scan**: Physical-AI/VLA/WAM and Multimodal/MLLM/Omni now require separately recorded 24h→7d coverage, followed by targeted 30d omission recovery.
- No paper promotion this hour. The multimodal scan re-hit canonical HorizonServe, M*, HydraInfer, Omni-Flow, Cornserve and vLLM-Omni.
- Added SGLang-Omni v0.1.2 production-serving tracker as ecosystem evidence: same-GPU Qwen3-TTS MPS-DP plus `WEIGHT_SHARE=1` serving/concurrency correctness are now monitored as Multimodal/Omni runtime evolution.
- Updated the dedicated multimodal landing page and latest heartbeat; public paper counts remain **132 / 101 CORE_SYS / 22 SYS_ALG / 4 ALG / 5 WATCH**.

- **2026-08-23 19:00 CST:** Hourly dual-track scan: no canonical-paper promotion; added vLLM-Omni full-duplex-runtime graduation (#6028) and video-output-transport optimization (#6212) as multimodal runtime radar evidence.

## 2026-08-23 21:00 CST
- Dual-track 24h→7d fresh scan plus targeted 30d systems/runtime checks completed; no canonical-paper promotion.
- SGLang-Omni v0.1.2 tracker remains open; active gates now cover Qwen3-TTS admission/queueing, playback continuity, deterministic/batch-invariant inference, absolute per-stage KV-memory budgets, same-GPU MPS-DP configuration, and `WEIGHT_SHARE=1` concurrent-request correctness.
- Retained vLLM-Omni #6028/#6212 implementation boundaries: duplex graduation/migration is still RFC-level; Hop-1 video shared-memory IPC is landed while Hop-2 binary/compressed/zero-copy transport remains open.
- Public paper counts unchanged at **132 verified / 101 CORE_SYS / 22 SYS_ALG / 4 ALG / 5 WATCH**.

## 2026-08-23 22:00 CST
- Completed independent Physical-AI and Multimodal/Omni 24h→7d scans plus targeted 30d systems/runtime checks; no canonical-paper promotion.
- SGLang-Omni v0.1.2 release tracker #1436 remains open with the production gates unchanged.
- Added a runtime-evolution note for SGLang-Omni #1357: reusable breakable Prefill CUDA Graph support is merged/default-ON for Higgs-TTS, MOSS-Transcribe-Diarize, and Qwen3-ASR; Qwen3-ASR uses 50 prefill buckets up to 4096 tokens.
- Revalidated vLLM-Omni #6028/#6212/#5120/#6231 as open at their previously recorded boundaries; public paper counts remain **132 verified / 101 CORE_SYS / 22 SYS_ALG / 4 ALG / 5 WATCH**.

### 2026-08-23 23:59 CST
- Added Relax (arXiv:2604.11554) to SYS_ALG_BOUNDARY after multimodal omission recovery; synced public dataset to 133 records.

- **2026-08-24 07:01 CST:** dual-track hourly scan; no paper promotion. Recorded vLLM-Omni v0.26 DLO/Cosmos3 production correctness debt and SGLang-Omni release-gate status.

- 2026-08-24 10:58 CST — dual-track scan: no paper promotion; tracked vLLM-Omni request-lifecycle/runtime-safety issues; Ascend field-study PDF debt resolved.

## 2026-08-26 01:02 CST
- Completed independent Physical-AI and Multimodal/Omni 24h→7d scans plus targeted 30d systems/runtime checks; no canonical-paper promotion.
- Backfilled official vLLM-Omni `v0.27.0rc1` release/runtime evidence: 104 merged changes from 52 contributors, with PersonaPlex full-duplex serving, DLO DP concurrency, scheduler-managed diffusion paged-KV/admission cleanup, batched Chat Completions and broader MiniMax-H3 heterogeneous deployment.
- Kept this as release-candidate evolution of the existing vLLM-Omni trunk, not a new paper and not evidence that later cancellation/reclamation issues are resolved.

## 2026-08-26 03:00 CST
- Added Rollplex (arXiv:2608.14498) to `SYS_ALG_BOUNDARY` (A+, Routes 6/8/11).
- Refined Multimodal map with a cross-phase GPU-sharing/post-training boundary branch.
- Hourly dual-track scan completed; no new Physical-AI CORE_SYS promotion.

## 2026-08-26 20:00 CST — hourly scan
- **CORE_SYS +1:** [IcFuzz](https://arxiv.org/abs/2608.06088) (ASE 2026), Route 9 / A — reliability-testing infrastructure for Isaac Sim with semantic-stage-guided fuzzing, hierarchical mutations and adaptive mutation scheduling. It reports 11 bugs over ~4 months, 9 confirmed or fixed. [Replication package](https://doi.org/10.5281/zenodo.19244624).
- **Multimodal / Omni:** independent 24h/7d + targeted 30d runtime scan completed; no paper promotion. Lifecycle/preemption/reclamation and failure-path observability remain active.

## 2026-08-26 21:00 CST — hourly scan
- Added **PHYFU: Fuzzing Modern Physics Simulation Engines** (ASE 2023 Distinguished Paper) to `CORE_SYS / A`, Route 9, as the foundational physics-simulation reliability anchor recovered from IcFuzz reverse census.
- Route 9 now explicitly records the **PHYFU → IcFuzz** lineage; PHYFU supplies physics-law oracles and feedback-guided fuzzing across general physics engines, while IcFuzz specializes to Isaac Sim with semantic-stage guidance/multi-level mutation.
- Official PHYFU repository verified; official arXiv PDF archived privately on full97 only. No PDF or internal server data was added to this public repository.
- Independent Multimodal/Omni 24h/7d + targeted 30d scan completed with no paper promotion; request lifecycle/preemption/reclamation and failure-path tracing/soak CI remain active.

## 2026-08-26 22:00 CST
- Added **RoboFuzz: Fuzzing Robotic Systems over Robot Operating System (ROS) for Finding Correctness Bugs** (ESEC/FSE 2022) to `CORE_SYS / A`, Route 9, as the foundational ROS2/robot-stack reliability anchor recovered from the PHYFU/IcFuzz lineage.
- Route 9 now explicitly records **RoboFuzz → PHYFU → IcFuzz**. Public content links only to official paper/repository sources; PDFs remain off-repo.
- Independent Multimodal/Omni fresh scan completed with no paper promotion; lifecycle/preemption/reclamation and failure-path observability remain the active production-runtime frontier.

## 2026-08-27 02:02 CST
- Added CaP-X to CORE_SYS / Route 9; added ASPIRE and RHO to SYS_ALG_BOUNDARY.
- Refined Route 9 to explicitly include reusable robot coding-agent evaluation/execution substrates.
- Refreshed public radar heartbeat after independent Physical-AI and Multimodal/Omni scans.

## 2026-08-27 05:01 CST
- Added **ENPIRE** (arXiv:2606.19980) to SYS_ALG_BOUNDARY / A+, Routes 1/2/9.
- Refined P1/P2/P9 with physical autoresearch / fleet experiment orchestration: automatic reset+verification, auditable rollout artifacts, parallel robot trials and MRU/MTU utilization metrics.
- Independent Multimodal/Omni scan completed with no paper promotion; lifecycle/preemption/cancellation/reclamation and failure-path tracing remain active.

## 2026-08-27 06:01 CST
- Hourly dual-track scan completed with **no paper promotion**.
- Added first-party GEAR-SONIC C++ deployment/runtime adoption evidence from `NVlabs/GR00T-WholeBodyControl`: motor-error monitoring, TTS alerts, ZMQ protocol v4 and idle-mode readaptation, plus the later G1 end-to-end VLA workflow. Kept as Route 2/3/6 ecosystem evidence rather than a paper record.
- ENPIRE/GEAR same-group census did not surface a new paper-backed fleet scheduler/runtime; Multimodal/Omni scan re-hit canonical systems and continued lifecycle/preemption/reclamation/failure-path monitoring.

## 2026-08-27 09:00 CST
- Added FlashRT (arXiv:2607.18171) to CORE_SYS/A+ for agent-guided multimodal deployment/runtime synthesis.
- Added explicit collision guard vs Execution-State Capsules / FlashRT (arXiv:2606.20537).
- Updated latest coverage heartbeat and dataset count.
## 2026-08-27 13:00 CST
- Promoted **Lingjing** to CORE_SYS/A+ (Routes 1/2/9): multi-engine heterogeneous-agent digital-twin runtime and evaluation substrate.
- Promoted **Deployment Is Not Destiny** to CORE_SYS/A (Routes 1/2/4/6/7): runtime recomposition and distributed capability/compute sharing.
- Added omission queries for runtime robot recomposition, unseen payload attachment, multi-engine embodied runtime, shared physical state, city-scale digital twins and attribution-ready replay.


- **2026-08-28 10:02 CST** — Added StreamArena / StreamMind (arXiv:2608.05703) as CORE_SYS/A; added always-on streaming multimodal runtime + persistent-state serving branch; refreshed hourly coverage heartbeat.

## 2026-08-28 11:00 CST
- Added arXiv:2608.09411 as `SYS_ALG_BOUNDARY / A` (P4/P5/P8) for latent-freshness-aware multi-camera Physical-AI edge resource control.
- Refined taxonomy to track AoL/TWI-style freshness as a resource signal while preserving the runtime/serving bar for CORE_SYS.
- Refreshed machine-readable dataset to **158** verified works and corrected the previously stale declared `count` metadata.
- Completed the hourly dual-track scan; no additional CORE_SYS promotion.

- 2026-08-28 17:00 CST — hourly coverage heartbeat after real dual-track fresh scan; no paper/classification change. Revalidated SGLang #36690/#36678 as open production-runtime frontiers.
- 2026-08-28 18:00 CST — hourly coverage heartbeat after real dual-track fresh scan; no paper/classification change. Revalidated vLLM-Omni #6403 true-cancellation/status semantics and SGLang-Omni #1593 failure-observability/soak-CI as open production-runtime frontiers.
- 2026-08-28 23:00 CST — hourly coverage heartbeat after real dual-track fresh scan; no paper/classification change. Revalidated SGLang #36475, vLLM-Omni #6403, and SGLang-Omni #1593 as open production-runtime frontiers.

- 2026-08-28 23:58 CST — recovered **TypeGo** (arXiv:2607.05482) into CORE_SYS/A+ (P2/P3/P7); added OS-style embodied process/resource runtime branch; public dataset now 159 works. No PDF/internal server artifact was added to the public repo.

## 2026-08-29 06:00 CST
- Runtime maturity update, no paper promotion: SGLang-Omni Qwen3-TTS startup-safety PR #1786 verified merged; #1726/#1753 remain open and #1760 P/D-disaggregation remains unmerged.


## 2026-08-31 11:18 CST
- Recovered the radar after a stale-heartbeat incident; performed a substantive 24h/7d + targeted 30d SYS-first catch-up scan rather than a heartbeat-only repair.
- No paper/classification promotion. Revalidated active lifecycle/cache correctness frontiers across vLLM, vLLM-Omni, SGLang and SGLang-Omni.
- Corrected the public heartbeat count to the already-present machine-readable canonical set of **161 works**.
- No PDFs or private server artifacts were added to the public repository.
