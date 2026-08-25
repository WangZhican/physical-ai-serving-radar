## Hourly scan — 2026-08-26 07:04 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0.
- **Physical AI:** independent 24h→7d fresh scan + targeted 30d checks completed across VLA/robot-policy serving, fleet/control-loop scheduling, edge/device runtime, state reuse, evaluation infrastructure and world-model rollout. Fresh hits were canonical PhyAI/XPolicyLab/Zetta/DeepInsight II or below threshold; no duplicate promotion.
- **Multimodal / Omni:** independent fresh scan covered omni serving, stage/modality disaggregation, any-to-any/composite runtime and vLLM/SGLang production ecosystems. HorizonServe/vLLM-Omni re-hit canonical; no new paper-level SYS promotion.
- **Observability / release gates:** SGLang-Omni #1593 remains open after #1595 merged; remaining work is slot-pool failure events plus comm-layer-triggered soak/CI-nightly policy. #1436 remains open, so V0.1.2 is still gated by Qwen3-TTS admission/queueing, playback continuity, batch invariance, same-GPU MPS-DP config, absolute KV budgets and `WEIGHT_SHARE=1` correctness. #946 remains open for a Prometheus-compatible Omni `/metrics` endpoint.
- **Request lifecycle:** vLLM-Omni #6403 remains open with queued-vs-running status ambiguity and ineffective cancellation of already-running video inference; #6413 remains open for aborted diffusion outputs retained in `_completed_outputs`. No fresh first-party evidence in this scan warranted upgrading #6439 beyond PR-scoped reclamation evidence.
- **Current state:** 140 works = 103 CORE_SYS / 27 SYS_ALG / 4 ALG / 6 WATCH. Private PDF state remains 133 valid; public repo contains links only.
- **Next:** #1593 failure-path/soak CI integration → #6439 reclamation final semantics → #6403 true cancellation/status → #946/#1436 production gates → vLLM-Omni release hardening → fresh 30d Multimodal SYS; parallel Physical-AI edge/fleet/state/evaluation runtime coverage.

## Hourly scan — 2026-08-26 06:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0.
- **Physical AI:** independent 24h→7d fresh scan + targeted 30d checks completed; canonical PhyAI/Kairos/Embodied.cpp/XPolicyLab/Zetta anchors re-hit, with no stronger new fleet/control-loop/edge/state/evaluation paper promoted.
- **Multimodal / Omni:** independent fresh scan re-hit canonical HorizonServe/M*/EPD-family systems; no new paper-level SYS promotion. Rollplex remains `SYS_ALG_BOUNDARY / A+`; no verified online-serving transfer of its cross-phase/HBM/weight-sharing mechanisms was found.
- **Release-state correction:** a direct first-party `git ls-remote --tags` check against `vllm-project/vllm-omni` at 06:00 CST shows tags through `v0.27.0rc1` only; **no final `v0.27.0` or `v0.27.1` tag is present**. Durable/public release claims therefore stay pinned to `v0.27.0rc1` until an actual upstream tag appears.
- **Observability update:** GitHub's first-party API confirms SGLang-Omni PR **#1595 merged on 2026-08-21 23:22 UTC** (`94b143fe88f7b98d8d7ef548fc9ac45ef1bc502e`). It adds paged-KV, transport-selection and direct-IPC stream tracing, including success/failure and same-GPU fast paths. Parent issue #1593 remains open: slot-pool failure events and comm-layer-triggered soak/CI-nightly policy are still pending.
- **Current state:** 140 works = 103 CORE_SYS / 27 SYS_ALG / 4 ALG / 6 WATCH. Private PDF state remains 133 valid; public repo contains links only.
- **Next:** verify whether SGLang-Omni #1593's comm-layer soak/failure-path policy has entered CI/nightly and whether remaining slot-pool failure events land → vLLM-Omni #6439 reclamation → #6403 true cancellation/status → #946/#1608/#1436 production gates → v0.28 hardening → fresh 30d Multimodal SYS; parallel ROLL/VeRL-Omni transfer census and Physical-AI edge/fleet/state/evaluation runtime coverage.

## Hourly scan — 2026-08-26 05:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0.
- **Physical AI:** independent 24h→7d fresh scan + targeted 30d checks completed; canonical PhyAI/Kairos/state-runtime anchors re-hit, with no stronger new fleet/control-loop/edge/evaluation paper promoted.
- **Multimodal / Omni:** Rollplex/ROLL reverse census found adjacent VeRL-Omni runtime evidence for multimodal generative RL, but no verified transfer of Rollplex cross-phase prefix overlap, phase-aware HBM residency or TP-layout-aware physical weight sharing into online serving. Rollplex remains `SYS_ALG_BOUNDARY / A+`.
- **Production lifecycle:** vLLM-Omni #6403 remains open for queued-vs-running status/cancellation; #6413 remains open for aborted diffusion orphan-output retention. The public v0.28.0 milestone remains at the latest indexed 50/129 closed (38%), due 2026-08-30.
- **Release evidence guard:** the first-party releases page fetched in this scan is stale and cannot safely confirm a final 0.27.x cut. Public/durable claims remain pinned to directly verified `v0.27.0rc1` until a fresh first-party tag/release endpoint is resolved.
- **Current state:** 140 works = 103 CORE_SYS / 27 SYS_ALG / 4 ALG / 6 WATCH. Private PDF state remains 133 valid; public repo contains links only.
- **Next:** resolve vLLM-Omni current tag/release state → SGLang-Omni #1595/#1593 tracing+soak integration → #6439 reclamation → #6403 true cancellation/status → #946/#1608/#1436 production gates → fresh 30d Multimodal SYS; parallel ROLL/VeRL-Omni transfer census and Physical-AI edge/fleet/state/evaluation runtime coverage.

## Hourly scan — 2026-08-26 00:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0.
- **Physical AI:** independent 24h→7d fresh scan plus targeted 30d checks covered VLA/robot-policy serving, fleet/control-loop scheduling, world-model rollout, state reuse, edge/device deployment and evaluation infrastructure. Fresh hits were canonical XPolicyLab/ROSA/Zetta or below-threshold work; no duplicate promotion.
- **Multimodal / Omni:** independent 24h→7d scan plus targeted 30d systems/runtime checks covered MLLM/Omni serving, stage/modality disaggregation, composite/any-to-any runtime and official vLLM/SGLang ecosystems. HorizonServe re-hit canonical; no new paper-level SYS promotion.
- **Boundary checks:** current arXiv/new results around the latest 2608.21xxx batch did not surface a new Physical-AI/Multimodal serving paper clearing the SYS-first bar; agent-learning architectures and generic LLM/MoE serving remain outside CORE_SYS without direct runtime/serving evidence for this scope.
- **Current state:** 139 works = 103 CORE_SYS / 26 SYS_ALG / 4 ALG / 6 WATCH. Private PDF state remains 132 valid; public repo contains links only.
- **Next:** ENEI reverse census → SGLang-Omni #1595/#1593 observability+soak → vLLM-Omni reclamation/cancellation/pause-resume semantics → production gates + fresh 30d Multimodal SYS; parallel Physical-AI action-freshness/fleet-SLO/state/evaluation runtime coverage.

## Hourly scan — 2026-08-25 21:04 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +1 / ALG +0 / WATCH +0 — [Edge-Native Embodied Intelligence](https://arxiv.org/abs/2608.17774).
- **Physical AI:** 24h→7d fresh scan + targeted 30d edge/runtime recovery completed. ENEI couples embodied agents, a 6G fabric and edge cognitive services through confidence-aware assistance, goal-oriented transmission, programmable radio-resource allocation and value-of-experience embodied federated learning. Kept at `SYS_ALG_BOUNDARY / A-` because it is currently a framework/case-study co-design rather than a mature serving runtime.
- **Multimodal / Omni:** independent 24h→7d scan re-hit canonical HorizonServe/Cornserve/vLLM-Omni; no paper promotion. vLLM-Omni #6403/#6413/#6083 remain open in current first-party evidence.
- **Boundary guard:** FleetSieve (arXiv:2608.19659) was audited but excluded: its `fleet` is an LLM GPU/replica serving fleet, not a robot fleet, and no multimodal workload evidence was verified.
- **Private PDF state:** ENEI official arXiv PDF archived and validated (3,297,504 B). Canonical private state: 139 works / 132 valid PDFs; public repo stores links only.
- **Next:** ENEI author/reference reverse census → SGLang-Omni #1595/#1593 observability+soak → vLLM-Omni #6439 reclamation → #6403 true cancellation/status → #6083 AR pause/sleep → production gates + fresh 30d Multimodal SYS.

## Hourly scan — 2026-08-25 18:01 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH_ONLY +1 — HODAgent (arXiv:2608.17584), retained only as a withdrawn watch.
- **Physical AI:** independent 24h→7d fresh scan plus targeted 30d runtime/harness/state/evaluation recovery completed. HODAgent is system-relevant because it defines a semi-duplex System-2 runtime with independently scheduled interaction/planning/execution/memory, asynchronous skill cancellation, persistent service state and a shared embodiment contract. Its arXiv listing was withdrawn on 2026-08-20 for mandatory company internal review, no official repo was verified, and the official PDF endpoint is unavailable; quantitative claims are therefore not treated as stable evidence.
- **Multimodal / Omni:** no paper promotion. vLLM-Omni #6413/#6403 remain open; #6083 AR pause/resume + sleep/wake remains open; public v0.28.0 milestone remains due 2026-08-30 at 50/129 closed (38%).
- **Integrity repair:** private canonical manifest had already advanced to 137 works / 103 CORE_SYS because PhyAgentOS was present while the summary state still reported 136/102; private PDF manifest had already advanced to 131 valid PDFs. Public dataset was also one record/count behind. This heartbeat reconciles public coverage with the current canonical state.
- **Current public/private paper state:** 138 works = 103 CORE_SYS / 25 SYS_ALG / 4 ALG / 6 WATCH. Private PDF state: 131 valid PDFs; legal debt Eevee/ROSGM/TILDE plus withdrawn HODAgent PDF pending official re-release.
- **Next:** HODAgent re-release/repo monitor → independently verify SGLang-Omni #1595 merge/release + #1593 soak CI/nightly integration → vLLM-Omni #6439 reclamation → #6403 true cancellation/status → #946/#1608/#1436 production gates → v0.28.0 hardening → fresh 30d Multimodal SYS; parallel Physical-AI action-freshness/fleet-SLO/state/evaluation runtime coverage.

## Hourly scan — 2026-08-25 17:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- **Physical AI:** independent 24h→7d fresh scan plus targeted 30d runtime/state/evaluation checks completed; hits were canonical or below the SYS-first threshold.
- **Multimodal / Omni:** no paper promotion. Current SGLang-Omni `main` documents a fail-closed same-GPU MPS-DP + CUDA-IPC weight-sharing contract: validated models must pass N=2 MPS boot/attach, concurrent-request output correctness and clean teardown, with sharing restricted to validated tp=pp=1 configurations. Current supported rows span MOSS TTS delay/local, Higgs TTS, Whisper, MOSS Transcribe-Diarize, Qwen3-ASR and FunASR Nano; documented shared-weight savings range roughly **1.51–17.05 GiB per follower**.
- **Important boundary:** Qwen3-TTS remains **not supported** for default-mode weight sharing; its passing byte-identity result required deterministic mode that serializes preprocessing/vocoder execution and changes throughput. Mutable streaming/preprocessing/vocoder state stays replica-private even when read-only weights are shared.
- **Lifecycle / observability watch:** vLLM-Omni #6403 and #6413 remain open; #6439 remains the reclamation path. The v0.28.0 public milestone remains due 2026-08-30 at 50/129 closed (38%). SGLang-Omni #1593 remains open and still cites #1595 for 14 paged-KV/transport/direct-IPC trace events; independent merge/release status remains unverified.
- **PDF:** no new canonical paper/PDF; private canonical state remains 136 works / 130 valid PDFs. Legal debt remains Eevee, ROSGM, TILDE.
- **Next:** verify #1595 merge/release + #1593 soak CI/nightly integration → #6439 reclamation → #6403 true cancellation/status → #946/#1608/#1436 production gates → v0.28.0 hardening → fresh 30d Multimodal SYS; parallel Physical-AI action-freshness/fleet-SLO/state/evaluation runtime coverage.

## Hourly scan — 2026-08-25 16:01 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- **Physical AI:** independent 24h→7d fresh scan plus targeted 30d runtime/state/evaluation checks completed; fresh hits were canonical or below the SYS-first threshold.
- **Multimodal / Omni:** no paper promotion, but SGLang-Omni `main` now exposes a reusable same-GPU MPS-DP deployment path with managed CUDA MPS, explicit CPU/NUMA pinning, per-replica KV sizing and optional CUDA-IPC weight sharing. In the pinned TTS profiles, saturated DP2/DP3 reaches roughly **1.4–2.1×** tuned single-replica throughput; documented shared-weight savings range from about **1.51 to 17.05 GiB per follower** depending on the ASR/TTS model.
- **State-isolation boundary:** weight sharing is opt-in and validation-gated; streaming preprocessing/vocoder/codec processes remain replica-private when they carry mutable stream state. The research map now explicitly separates shareable immutable weights from per-replica streaming state, admission/KV budgeting and host-dispatch placement.
- **Lifecycle / release watch:** vLLM-Omni #6403/#6413 remain open in current indexed first-party evidence; #6439 remains the reclamation path. The v0.28.0 public milestone remains due 2026-08-30 at 50/129 closed (38%). SGLang-Omni #1593 remains open and still cites #1595 for 14 paged-KV/transport/direct-IPC trace events; independent merge/release status is not yet verified.
- **PDF:** no new canonical paper/PDF; private canonical state remains 136 works / 130 valid PDFs. Legal debt remains Eevee, ROSGM, TILDE.
- **Next:** verify release/paper lineage and concurrent-request correctness for SGLang-Omni MPS-DP/weight sharing → #1595/#1593 observability+soak integration → #6439 reclamation → #6403 true cancellation/status → #946/#1608/#1436 production gates → v0.28.0 hardening → fresh 30d Multimodal SYS; parallel Physical-AI action-freshness/fleet-SLO/state/evaluation runtime coverage.

## Hourly scan — 2026-08-25 15:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- **Physical AI:** independent 24h→7d fresh scan plus targeted 30d runtime/state/evaluation checks completed; no new paper crossed the SYS-first threshold, and fresh hits were canonical or below-threshold.
- **Multimodal / Omni:** no new paper promotion. vLLM-Omni #6403 remains open with queued-vs-running status ambiguity and ineffective cancellation for already-running video inference; #6413 remains open with #6439 still the reclamation path. The v0.28.0 public milestone remains due 2026-08-30 at 50/129 issues closed (38%) in the latest indexed snapshot.
- **Failure-path observability:** SGLang-Omni #1593 remains open. Its first-party issue text says #1595 implements 14 paged-KV / transport-selection / direct-IPC stream trace events, but an independent merge/release signal for #1595 is still not verified; slot-pool failure events and comm-layer-triggered soak/CI policy remain open.
- **PDF:** no new canonical paper/PDF; private canonical state remains 136 works / 130 valid PDFs. Legal debt remains Eevee, ROSGM, TILDE.
- **Next:** obtain fresh post-#6458 MiniCPM-o continuous-request CI evidence → independently verify #1595 merge/release + #1593 soak CI/nightly integration → #6439 reclamation merge/final semantics → #6403 real cancellation/status → #946 metrics + #1608/#1436 production gates → v0.28.0 hardening → fresh 30d Multimodal SYS; parallel Physical-AI action-freshness/recovery/fleet-SLO/state/evaluation runtime coverage.

## Hourly scan — 2026-08-25 14:02 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- **Physical AI:** independent 24h→7d fresh scan plus targeted 30d runtime/state/evaluation checks completed; no new paper crossed the SYS-first threshold.
- **Multimodal / Omni:** no new paper promotion. The historical vLLM-Omni #6426 continuous-request OOM/audio-correctness record remains visible in current indexed evidence even after merged #6458; #6458 is therefore kept scoped to long-form Talker repetition/EOS/length remediation until fresh post-merge CI confirms memory/correctness behavior.
- **Failure-path observability:** SGLang-Omni #1593 remains open and states that #1595 implements 14 paged-KV / transport-selection / direct-IPC stream trace events. Slot-pool failure events and comm-layer-triggered soak/CI policy are still open; independent #1595 merge/release status is not yet confirmed.
- **PDF:** no new canonical paper/PDF; private canonical state remains 136 works / 130 valid PDFs. Legal debt remains Eevee, ROSGM, TILDE.
- **Next:** fresh post-#6458 MiniCPM-o continuous-request CI → verify #1595 merge/release + #1593 soak integration → #6439 reclamation → #6403 cancellation/status → #946 metrics + #1608/#1436 production gates → v0.28.0 hardening → fresh 30d Multimodal SYS; parallel Physical-AI action-freshness/recovery/fleet-SLO/state/evaluation runtime coverage.

## Hourly scan — 2026-08-25 12:59 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- **Physical AI:** independent 24h→7d fresh scan plus targeted 30d runtime/state/evaluation checks completed; fresh hits re-hit canonical PhyAI/ROSA/Embodied.cpp/XPolicyLab/Zetta or remained below the SYS-first threshold.
- **Multimodal / Omni:** vLLM-Omni #6426 is now **closed**. It links to merged PR #6458 (merged 2026-08-22), which restores MiniCPM-o 4.5 long-form Talker correctness through a request-local 16-frame repetition penalty, forced EOS restoration after `min_tokens`, and offline generation capped at `min(2048, remaining context)`. Because #6426 bundled OOM and several audio-correctness failures, continuous-request memory/correctness still needs revalidation instead of assuming every failure mode is resolved.
- **Observability:** SGLang-Omni #1593 remains open and states that #1595 implements 14 trace events for paged-KV / transport-selection / direct-IPC stream gaps. Independent merge/release status for #1595 is not yet confirmed; slot-pool failure events and CI/nightly soak policy remain follow-up work.
- **Lifecycle debt:** vLLM-Omni #6403 async-video queued-vs-running/cancellation remains open; #6413 aborted-diffusion orphan-output leak remains open with #6439 as the reclamation path.
- **PDF:** no new canonical paper/PDF; private canonical state remains 136 works / 130 valid PDFs. Legal debt remains Eevee, ROSGM, TILDE.
- **Next:** revalidate #6426 continuous-request CI after #6458 → verify #1595 merge/release + #1593 soak integration → #6439 reclamation merge → #6403 cancellation/status → #946 metrics + #1608/#1436 production gates → v0.28.0 hardening → fresh 30d Multimodal SYS; parallel Physical-AI action-freshness/recovery/fleet-SLO/state/evaluation runtime coverage.

## Hourly scan — 2026-08-25 11:58 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- **Physical AI:** independent 24h→7d fresh scan plus targeted 30d runtime/state/evaluation checks completed; fresh hits re-hit canonical PhyAI/Kairos/M* or stayed below SYS-first threshold.
- **Multimodal / Omni:** no new paper promotion. vLLM-Omni remains the main stage-based serving trunk; current docs continue to expose stage-local batching/resource placement across text/image/audio/video and robot-policy paths.
- **Failure-path observability:** SGLang-Omni #1593 remains open and documents that paged-KV transfer currently lacks trace events, transport fallback can be invisible, and direct-IPC streaming lacks consumer-side events. The issue states that #1595 implements 14 events for paged-KV/transport/stream gaps; slot-pool failure events and CI/nightly soak policy remain follow-up work. Its 8-hour two-H200 Qwen3-Omni-30B soak processed 4,764 requests / 3,510,175 slot allocations; low peak pool occupancy means this is a reference point, not proof of leak-freedom.
- **PDF:** no new canonical paper/PDF; private canonical state remains 136 works / 130 valid PDFs. Legal debt remains Eevee, ROSGM, TILDE.
- **Next:** verify #1595 merge/implementation status + #1593 soak integration → #6439 reclamation merge/final semantics → #6403 cancellation/status → #6426 continuous-request correctness → #946 metrics + #1608/#1436 production gates → v0.28.0 hardening → fresh 30d Multimodal SYS; parallel Physical-AI action-freshness/recovery/fleet-SLO/state/evaluation runtime coverage.

## Hourly scan — 2026-08-25 10:02 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- **Physical AI:** independent 24h→7d fresh scan plus targeted 30d runtime/state/evaluation checks completed; fresh hits re-hit canonical PhyAI and existing robot-policy/fleet/state/evaluation anchors, with no duplicate promotion.
- **Multimodal / Omni:** vLLM-Omni #6403 async-video cancellation/status remains open; #6413 orphan-output leak remains open with #6439 as the reclamation path; #6426 continuous-request MiniCPM-o 4.5 OOM/correctness and #6083 AR-stage pause/resume + sleep/wake remain active runtime debt.
- **Failure-path observability:** SGLang-Omni #1593 shows current comm tracing is success-path-heavy and can miss failure branches, stranded slots, retained pending transfers, selected transport and paged-KV traffic. Its reference soak ran Qwen3-Omni-30B on two H200s for 8 hours (4,764 requests / 3,510,175 slot allocations); useful as leak-testing evidence, not proof of leak-freedom. #946 remains open for Prometheus-compatible Omni `/metrics`.
- **PDF:** no new canonical paper/PDF; private canonical state remains 136 works / 130 valid PDFs. Legal debt remains Eevee, ROSGM, TILDE.
- **Next:** #1595/#1593 failure-path tracing + soak integration → #6439 reclamation merge → #6403 cancellation/status → #6426 correctness → #946 metrics + #1608/#1436 production gates → v0.28.0 hardening → fresh 30d Multimodal SYS; parallel Physical-AI action-freshness/recovery/fleet-SLO/state/evaluation runtime coverage.

## Hourly scan — 2026-08-25 06:19 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- **Physical AI:** independent 24h→7d fresh scan plus targeted 30d runtime/state/evaluation checks completed; fresh hits re-hit canonical PhyAI and existing robot-policy/fleet/state/evaluation anchors, with no duplicate promotion.
- **Multimodal / Omni:** vLLM-Omni #6403 async-video cancellation/status remains open; #6413 orphan-output leak remains open with #6439 still represented as an open reclamation path; #6426 continuous-request MiniCPM-o 4.5 OOM/correctness remains active.
- **Observability:** SGLang-Omni #946 remains open and documents the absence of a Prometheus-compatible `/metrics` endpoint for the Omni API server. `/health` covers readiness, but standard scrapeable request-volume/error-rate/latency/coordinator telemetry is still missing; tracked as production observability infrastructure debt, not a paper promotion.
- **Release watch:** vLLM-Omni `v0.28.0` remains due 2026-08-30 at the latest indexed 50/129 closed snapshot; SGLang-Omni #1608 remains open with its 2026-08-23 Qwen3-TTS current-main hardening update.
- **PDF:** no new canonical paper/PDF; private canonical state remains 136 works / 130 valid PDFs. Legal debt remains Eevee, ROSGM, TILDE.
- **Next:** #6439 reclamation merge → #6403 cancellation/status → #6426 continuous-request correctness → SGLang-Omni #946 metrics/telemetry + #1608/#1436 production gates → v0.28.0 hardening → fresh 30d Multimodal SYS; parallel Physical-AI action-freshness/recovery/fleet-SLO/state/evaluation runtime coverage.

## Hourly scan — 2026-08-25 05:02 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- **Physical AI:** independent 24h→7d fresh scan plus targeted 30d runtime/state/evaluation checks completed; fresh hits re-hit Kairos/PhyAI/PCS/M* or below-threshold work, with no duplicate promotion.
- **Multimodal / Omni:** production-runtime census keeps request lifecycle and correctness as the active frontier. vLLM-Omni #6403 remains open with queued-vs-running status ambiguity and ineffective cancellation for already-running video inference; #6413 remains open with #6439 as the reclamation path; #6426 continuous-request MiniCPM-o 4.5 OOM/correctness and #6455 CosyVoice3 streaming device/state mismatch remain active.
- **SLO / config correctness:** #5668 shows `audio_ttfp` can be reported but is not accepted/applied as a normal goodput SLO; #5728 shows some stage-overrides can be accepted and silently ignored. These are production-runtime debts, not separate paper records.
- **Release watch:** vLLM-Omni `v0.28.0` remains due 2026-08-30; latest indexed milestone snapshot is 50/129 issues closed (38%).
- **PDF:** no new canonical paper/PDF; private canonical state remains 136 works / 130 valid PDFs. Legal debt remains Eevee, ROSGM, TILDE.
- **Next:** #6439 reclamation merge → #6403 real cancellation/status → #6426/#6455 streaming/continuous correctness → #5668 audio SLO → #5728 stage-config validation → v0.28.0 + SGLang-Omni production gates → fresh 30d Multimodal SYS; parallel Physical-AI action-freshness/recovery/fleet-SLO/state/evaluation runtime coverage.

## Hourly scan — 2026-08-25 02:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- **Physical AI:** independent 24h→7d fresh scan plus targeted 30d runtime/state/evaluation checks completed; no new paper crossed the SYS-first threshold.
- **Multimodal / Omni:** production-runtime census remains active around vLLM-Omni #6426 continuous-request MiniCPM-o 4.5 OOM/correctness, #6403 async-video status/cancellation semantics, and #6455 CosyVoice3 streaming TTS device/state mismatch. These are runtime-hardening signals, not paper promotions.
- **Release watch:** vLLM-Omni milestone `v0.28.0` is due 2026-08-30; current indexed snapshot is 50/129 issues closed (38%), so release hardening is still in progress.
- **PDF:** no new canonical paper/PDF. Private canonical state remains 136 works / 130 valid PDFs; legal debt remains Eevee, ROSGM, TILDE.
- **Next:** #6439 final reclamation semantics + #6403 cancellation/status + #6426 continuous-request OOM/correctness + #6455 streaming-device/state fix → v0.28.0 hardening → SGLang-Omni production gates → fresh 30d Multimodal SYS; parallel Physical-AI action-freshness/recovery/fleet-SLO/state-substrate/evaluation-runtime coverage.

## Hourly scan — 2026-08-24 23:04 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- **Physical AI:** independent 24h→7d fresh scan plus targeted runtime/state/evaluation checks completed; no new paper crossed the SYS-first threshold.
- **Multimodal / Omni:** independent 24h→7d + targeted 30d runtime scan completed. vLLM-Omni #6413 remains open; linked fix PR #6439 is still open in current first-party indexed evidence. Async-video issue #6403 also remains open, so cancellation/status/resource-reclamation semantics are not claimed as fixed.
- **PDF:** no new canonical paper/PDF. Private canonical state remains 136 works / 130 valid PDFs; legal debt remains Eevee, ROSGM, TILDE.
- **Next:** #6439 merge/final reclamation semantics → #6403 cancellation/status fix → SGLang-Omni production gates → fresh 30d Multimodal SYS; parallel Physical-AI action-freshness/recovery/fleet-SLO/state-substrate/evaluation-runtime coverage.

## Hourly scan — 2026-08-24 22:05 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +1 / ALG/WATCH +0.
- **New SYS_ALG_BOUNDARY:** [Decoding Task Progress from VLA Representations](https://arxiv.org/abs/2608.13474) — runtime observability for deployed VLAs. A lightweight linear probe reads task progress from pi0.5 residual-stream activations and is used as a label-free stalled-progress/OOD detector. Kept below CORE_SYS because it is a monitoring/probing method rather than a serving scheduler or resource manager.
- **Physical AI coverage:** independent 24h→7d + targeted 30d scan completed; runtime-monitoring vocabulary recovered this paper while PhyAI/Kairos/RobotFleet re-hits were deduplicated.
- **Multimodal / Omni:** independent 24h→7d + targeted 30d scan completed; no new paper promotion. vLLM-Omni #6413/#6439 reclamation and #6403 async-video cancellation/status remain open runtime-lifecycle evidence.
- **Private PDF state:** official arXiv PDF archived on the private server and validated; canonical private state is now 136 works and 130 valid PDFs. Public repo contains links only.
- **Next:** vLLM-Omni reclamation/cancellation semantics → SGLang-Omni production gates → fresh 30d Multimodal SYS; parallel Physical-AI runtime observability → action freshness/recovery/fleet SLO/state-substrate work.

## Hourly scan — 2026-08-24 16:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +1 / ALG/WATCH +0.
- **New SYS_ALG_BOUNDARY:** [WCM](https://arxiv.org/abs/2607.22999) — SLAK separates sensing/logic/action/knowledge; its asynchronous runtime runs reasoning, dialogue, state updates and physical execution concurrently, with stale-context validation before committing actions. Kept below CORE_SYS because HRI/teaching architecture remains the main novelty.
- **Physical AI coverage:** independent 24h→7d + targeted 30d scan completed; WCM was recovered via asynchronous embodied-runtime vocabulary rather than serving-title keywords.
- **Multimodal / Omni:** no paper promotion. vLLM-Omni #6403 exposes incomplete async-video lifecycle semantics: queued requests can be reported `IN_PROGRESS`, while deleting an already-running task removes metadata without terminating GPU inference. Track with #6413/#6439 under cancellation/reclamation.
- **PDF state:** WCM official arXiv PDF archived on the private server; public repo keeps links only. Canonical private state is now 135 works, with legal PDF debt still Eevee/ROSGM/TILDE.
- **Next:** #6403 cancellation/status semantics + #6439 reclamation → SGLang-Omni #1436/#1608 → fresh 30d Multimodal SYS; parallel WCM/SLAK runtime lineage and Physical-AI state/fleet/evaluation coverage.

## Hourly scan — 2026-08-24 14:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- **Physical AI:** independent 24h→7d + targeted 30d scan completed; fresh VLA/robot-policy/fleet/state/evaluation hits were canonical or below threshold.
- **Multimodal / Omni:** vLLM-Omni #6439, the fix for aborted diffusion output leakage (#6413), is **open/not merged**. The PR adds orphan-output reclamation, shutdown cache cleanup, and explicit discard of late outputs for cancelled/done waiters; targeted CPU tests report 42 passing after review-driven fixes.
- **TTS runtime boundary:** vLLM-Omni #6158 remains open with no linked implementation PR, so catastrophic codec repetition/missing-EOS safeguards are not claimed as shipped.
- **SGLang-Omni:** #1608 was updated 2026-08-23; Qwen3-TTS KDA reproduction is rebased to current main, compile parity is closed, Talker `torch.compile` was removed after no reproducible end-to-end gain, CUDA Graph remains enabled, and 204 directly affected current-main tests passed.
- **PDF state:** unchanged at 128 valid / 0 invalid; legal debt remains Eevee, ROSGM, TILDE.
- **Next:** #6439 merge/final semantics → #6158 implementation → SGLang-Omni #1608/#1436 production gates → fresh 30d Multimodal SYS; parallel Physical-AI state/fleet/evaluation/heterogeneous-runtime coverage.

## Hourly scan — 2026-08-24 10:58 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- **Physical AI:** independent 24h→7d + targeted 30d serving/runtime scan completed; PhyAI/Kairos re-hits deduplicated, no new paper crossed the SYS-first threshold.
- **Multimodal / Omni:** no new paper promotion. Runtime watch: vLLM-Omni #6413 exposes aborted-diffusion output reclamation leaks; #6158 tracks catastrophic TTS codec repetition/missing-EOS safeguards; #6083 remains AR pause/resume + sleep/wake for colocated multi-stage serving.
- **PDF debt improved:** arXiv:2607.08215 official PDF retry succeeded on full97 (443,796 B, valid %PDF-); remaining legal PDF debt is Eevee/ROSGM/TILDE.
- **Next:** #6413/#6439 reclamation fix → #6158 safeguards → SGLang-Omni production gates → fresh 30d Multimodal SYS; parallel Physical-AI state/fleet/evaluation runtime coverage.

## Hourly scan — 2026-08-24 09:03 CST

- **Promotions:** CORE_SYS +1 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- **New CORE_SYS:** [On the Limitations of Non-GPU AI Accelerators for Large-Model Inference](https://arxiv.org/abs/2607.08215) — heterogeneous/non-CUDA serving field study on 16 Huawei Ascend 910 accelerators. Real MoE + multimodal deployments required 12 source-level vLLM-Ascend/plugin patches and operational safeguards, exposing eight platform-level limitation classes across operators/features, multi-axis parallelism, numerical correctness, graph compilation, advanced-feature stability, scalability, observability and ecosystem fragmentation.
- **Artifact:** [official companion repo](https://github.com/YuZhengYYDS/ascend-large-model-inference-field-study); current public adoption is low (~1 star), so priority is A rather than A+.
- **Multimodal production-runtime watch:** vLLM-Omni #6426 reports continuous-request MiniCPM-o 4.5 OOM/correctness failures; SGLang-Omni #1470 reports Whisper scheduler crashes under c8/c16/c32 concurrency. Tracked as runtime correctness/state-lifecycle evidence, not separate paper promotions.
- **Physical-AI track:** independent 24h→7d + targeted 30d scan completed; no new Physical-AI paper crossed the SYS-first threshold.
- **PDF:** official arXiv URL verified; full97 download retries hit transient TLS/network errors, so PDF remains pending rather than falsely marked downloaded.
- Next: retry PDF + pending GitHub remote sync → expand Ascend/NPU/non-CUDA multimodal-serving census → vLLM-Omni/SGLang-Omni concurrency/state-reclamation production gates → fresh 30d Multimodal SYS; parallel Physical-AI state/fleet/evaluation coverage.

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

### 2026-08-25 06:05 CST — dual-track hourly scan
- **Promotion:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0.
- **Physical AI:** independent 24h/7d + targeted 30d systems/runtime scan completed; fresh hits re-hit canonical PhyAI/existing trunk or stayed below SYS-first threshold.
- **Multimodal / Omni:** vLLM-Omni #6403, #6413/#6439, #6426 and #6455 remain active production correctness/lifecycle debt; #5668 audio-TTFP goodput-SLO and #5728 stage-config validation also remain open. v0.28.0 milestone remains due 2026-08-30 at the latest indexed 50/129 closed snapshot. SGLang-Omni #1608 remains open with the latest public update dated 2026-08-23 and current-main Qwen3-TTS hardening evidence.
- **Next:** verify #6439 merge/approval directly, then cancellation/reclamation + continuous/streaming correctness + modality SLO/config validation; continue SGLang-Omni production gates and fresh 30d Multimodal SYS census. Physical-AI continues runtime observability/action freshness, fleet SLO, state substrate and evaluation/isolation.

### 2026-08-26 01:02 CST — dual-track hourly scan
- **Promotion:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG/WATCH +0. Independent Physical-AI and Multimodal/Omni 24h→7d scans plus targeted 30d systems/runtime checks completed.
- **Physical AI:** fresh VLA/robot-policy serving, fleet/control-loop, state reuse, edge/device deployment, evaluation-infrastructure and world-model-rollout queries produced canonical or below-threshold hits; no duplicate promotion.
- **Multimodal / Omni runtime backfill:** official vLLM-Omni **v0.27.0rc1** was released 2026-08-11 with 104 merged changes from 52 contributors. Systems-relevant changes include PersonaPlex native full-duplex speech-to-speech serving, DLO DP concurrency, scheduler-managed diffusion paged-KV worker contracts/admission cleanup, batched Chat Completions, and broader MiniMax-H3 heterogeneous deployment. This is release-candidate evidence for the existing vLLM-Omni trunk, not a new paper or proof that later lifecycle issues are fixed.
- **Fresh arXiv check:** current `2608.21xxx` results did not surface a new in-scope SYS-first Physical-AI/Multimodal paper.
- **Next:** verify final vLLM-Omni v0.27.0 cut vs rc1 → SGLang-Omni tracing/soak integration → vLLM-Omni reclamation/cancellation/pause-resume → production gates → fresh 30d Multimodal SYS census; continue Physical-AI edge-native runtime, fleet SLO, state substrate and evaluation/isolation.

## 2026-08-26 03:00 CST
- **SYS_ALG_BOUNDARY +1:** Rollplex (arXiv:2608.14498), A+, Routes 6/8/11. VLM post-training runtime with cross-phase prefix/decode overlap, phase-aware HBM residency, and TP-layout-aware weight sharing.
- Physical AI fresh scan: no new SYS promotion; 24h/7d + targeted 30d coverage completed.
- Multimodal fresh scan: Rollplex was the main omission-recovery promotion; next focus is ROLL lineage plus vLLM/SGLang production-runtime hardening.
