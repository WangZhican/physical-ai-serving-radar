## Hourly scan — 2026-09-02 19:59 CST

- **Paper promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. Completed a real fresh 24h→7d SYS-first scan; 0 promotion is not 0 search.
- **Coverage:** refreshed Physical-AI/VLA serving/runtime, multimodal/Omni serving, world-model rollout/session serving, cache/state infrastructure and stage/modality disaggregation. Fresh paper hits re-covered canonical LiveServe, M*, vLLM-Omni and PhyAI; no new reusable serving substrate crossed threshold.
- **TeleFuser frontier:** PR [#36](https://github.com/Tele-AI/TeleFuser/pull/36) remains open; current public PR surface lists 6 open PRs. #42/#43/#44 are heterogeneous/runtime maturity work, not new serving papers.
- **Cache qualification:** CacheSeek-backed latent reuse remains a strong Route-5/11 project-level signal: cross-request, prompt-similarity keyed, persistent, and externalized behind query/lookup/resume/save contracts. The missing systems evidence is now explicit: validity-threshold calibration, false-hit quality loss, multi-tenant pollution/isolation, distributed placement/versioning, eviction/admission and SLO impact.
- **World-model serving:** vLLM-Omni #6672 remains open and continues to separate performance, paging/memory, long-lived session semantics, mid-stream interaction and streaming-video serving; validated realtime results remain below its ≥12 FPS target on the reported H200 setups.
- **Canonical paper state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 paper WATCH; 154 valid internal PDFs, 4 pending. No taxonomy split/merge and no new PDF download.
- **Next:** TeleFuser PR #36 → CacheSeek validity/false-hit quality/pollution/isolation/placement/versioning/eviction/SLOs → vLLM-Omni #5805 → #6672/#6227/#6646/#5120/#6294 → #4480 → #4907/#4909 → SGLang/SGLang-Omni lifecycle/correctness → fresh 30d SYS census.

## Hourly scan — 2026-09-02 19:02 CST

- **Paper promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. Completed a real fresh 24h→7d SYS-first scan; 0 promotion is not 0 search.
- **Route-5 runtime update:** [TeleFuser](https://github.com/Tele-AI/TeleFuser) now documents external [CacheSeek](https://github.com/Tele-AI/CacheSeek) integration for **cross-request approximate latent reuse**. This is distinct from request-local feature cache: it persists reusable latent state across requests and uses prompt-embedding similarity to skip an initial denoising prefix.
- **Serving abstraction:** the integration separates query construction, lookup, resume injection, response capture and save; individual cache failures fall back to uncached execution. The documented backend includes persistent KV/distributed storage plus vector DB + metadata, making this a genuine serving-cache/state substrate rather than a local memoization trick.
- **Multi-session frontier:** TeleFuser PR [#36](https://github.com/Tele-AI/TeleFuser/pull/36) remains open. Fresh PRs #42/#43/#44 strengthen heterogeneous/runtime maturity but are not paper promotions.
- **Classification:** CacheSeek/TeleFuser remains runtime-project evidence, not a canonical paper. No taxonomy split/merge; Routes 5/11 are strengthened around cross-request state validity, cache pollution, placement, versioning and SLO-aware reuse.
- **Canonical paper state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 paper WATCH; 154 valid internal PDFs, 4 pending.
- **Next:** TeleFuser PR #36 → CacheSeek validity/pollution/placement/versioning/SLOs → vLLM-Omni #5805 → #6672/#6227/#6646/#5120/#6294 → #4480 → #4907/#4909 → SGLang/SGLang-Omni lifecycle/correctness → fresh 30d SYS census.

## Hourly scan — 2026-09-02 18:02 CST

- **Paper promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. **New runtime-project WATCH: TeleFuser +1.** Completed a real fresh 24h→7d SYS-first scan; 0 paper promotion is not 0 search.
- **Omission recovery:** [TeleFuser](https://github.com/Tele-AI/TeleFuser) is a public runtime directly targeting real-time world-model and multimodal serving. Its first-party architecture exposes actor-owned stateful stages, bounded artifact edges, per-session ordering, backpressure, lifecycle cleanup, explicit resource groups, LiveKit/WebRTC transport, distributed GPU execution and unified service APIs.
- **Multi-session/world-model evidence:** LingBot-World v2 supports retained multi-session admission with chunk-boundary time slicing. The project reports 17.14 steady target-side compute FPS on 4×H100 at 832×480 against a 16 FPS playback target; this is compute-path evidence, not end-to-end latency.
- **Stateful ABot-World:** the checked-in ABot path retains prompt/image latent, self/cross KV, scheduler, RNG and VAE temporal cache across control blocks and applies bounded FIFO backpressure. The documented baseline remains one retained session per worker; open PR [#36](https://github.com/Tele-AI/TeleFuser/pull/36) targets multi-session ABot-World serving.
- **Classification:** no formal TeleFuser paper/venue was verified, so it is a high-value project WATCH rather than CORE_SYS/PAPER_MANIFEST. No taxonomy split/merge; it strengthens Routes 3/5/6/10/11.
- **Existing frontier:** vLLM-Omni #5805/#6672/#4480/#4907 were rechecked; fresh generic vLLM/SGLang startup/loading bugs stay below Physical-AI/Omni canonical threshold.
- **Canonical paper state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 paper WATCH; 154 valid internal PDFs, 4 pending.
- **Next:** TeleFuser PR #36 merge/session-isolation/admission/fairness/memory-accounting → LingBot multi-session concurrency benchmarks → #5805 common session/full-duplex convergence → #6672/#6227/#6646/#5120/#6294 → #4480 → #4907/#4909 → SGLang/SGLang-Omni lifecycle/correctness → fresh 30d SYS census.

## Hourly scan — 2026-09-02 17:02 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. Completed a real fresh 24h→7d SYS-first scan; 0 promotion is not 0 search.
- **Coverage:** refreshed Physical-AI/VLA serving/runtime, world-model rollout/session serving, multimodal/Omni serving, state/cache infrastructure and first-party runtime ecosystems.
- **Full-duplex maturity update:** vLLM-Omni #5805 is not only a roadmap concept. The current experimental full-duplex tree already exposes model-agnostic `core/` adapter/session/turn-runtime contracts, an AsyncOmni/orchestrator engine bridge and OpenAI/WebSocket transport. Core owns session lifecycle, epoch-based barge-in, playback cursor and event protocol.
- **Qualification:** PersonaPlex and MiniCPM still retain distinct model-owned execution paths, so this is experimental implementation + unification RFC evidence rather than proof of fully shipped cross-model convergence. The design nevertheless strengthens Route 3/5/11 convergence between Omni full-duplex and world-model session/state management.
- **World-model serving:** #6672 remains OPEN and continues to depend on realtime stateful video serving, streaming backpressure, mid-stream interaction and generalized session memory.
- **Correctness:** SGLang #36475/#36690 remain open lifecycle/multimodal correctness evidence; #37368/#37369 stay below canonical Physical-AI/Omni promotion threshold.
- **Research-map impact:** no taxonomy split/merge and no canonical paper-count change.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending.
- **Next:** #5805 experimental contracts → concrete mainline/session convergence PRs → #6672/#6227/#6646/#5120/#6294 → #4480 generalized session-memory accounting/reclamation → #4907/#4909 branch completeness → SGLang/SGLang-Omni lifecycle/correctness → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-02 15:57 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. Completed a real fresh 24h→7d SYS-first scan; 0 promotion is not 0 search.
- **Coverage:** refreshed Physical-AI/VLA serving/runtime, world-model rollout/session serving, multimodal/Omni serving, state/cache infrastructure and first-party runtime ecosystems.
- **Runtime-abstraction omission recovery:** vLLM-Omni RFC #5805 (opened 2026-08-05) was newly recovered into the radar narrative. It proposes converging experimental full-duplex paths into the common orchestrator/stage-runner execution framework and unifying session representation/flow across Aura, MiniCPM, JoyAI and DreamZero/world-model sessions. This is ecosystem/runtime evidence, not a paper promotion.
- **World-model serving:** #6672 remains OPEN/high-priority and still reports roughly 5 FPS validated realtime throughput versus a >=12 FPS target, with remaining production gaps around stateful-video serving, structured mid-stream interaction, session memory, paging/backpressure and long-horizon lifecycle.
- **Correctness:** SGLang #36690 remains open multimodal-serving correctness evidence; fresh #37368 remains generic serving-loading correctness below canonical Physical-AI/Omni promotion threshold.
- **Research-map impact:** no taxonomy split/merge, but Route 3/5/11 convergence is strengthened: full-duplex Omni and world-model serving increasingly share the same session/state abstraction problem.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending.
- **Sync recovery:** the previously pending 15:01 local heartbeat was successfully pushed before this scan.
- **Next:** #5805 common full-duplex/session unification → #6672/#6227/#6646/#5120/#6294 → #4480 generalized session-memory accounting/reclamation → #4907/#4909 branch completeness → SGLang/SGLang-Omni lifecycle/correctness → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-02 15:01 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. Completed a real fresh 24h→7d SYS-first scan; 0 promotion is not 0 search.
- **Coverage:** refreshed Physical-AI/VLA serving/runtime, world-model rollout/session serving, multimodal/Omni serving, edge-cloud/disaggregated deployment, state/cache infrastructure and first-party vLLM/SGLang runtime surfaces.
- **Boundary screen:** fresh Riemann-1.0 (arXiv:2608.27033) was explicitly screened and remains outside CORE_SYS because its primary contribution is WAM modeling/pretraining/capability rather than a reusable serving abstraction, scheduler, resource manager or runtime substrate.
- **World-model serving:** vLLM-Omni #6672 remains OPEN. Its dependency tree separates merged LingBot World 2 model-path integration (#5491) from the still-incomplete production serving stack: #6227 realtime stateful video serving, #6646 streaming backpressure, #5120/#6294 mid-stream interaction and #4480 generalized session memory.
- **Lifecycle qualification:** SGLang #36475 remains OPEN for streaming-session disconnect/session-state corruption. Treat issue/RFC evidence as runtime qualification, not as a paper promotion.
- **Research-map impact:** no taxonomy split/merge and no canonical paper-count change.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending.
- **Next:** #6672 → #6227/#6646/#5120/#6294 production session path → #4480 generalized session-memory accounting/reclamation → #4907/#4909 branch completeness → SGLang/SGLang-Omni lifecycle/correctness → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-02 13:58 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. Completed a real fresh 24h→7d SYS-first scan; 0 promotion is not 0 search.
- **Coverage:** refreshed Physical-AI/VLA serving/runtime, multimodal/Omni serving, world-model rollout/session serving, edge-cloud inference, stage/state/cache infrastructure, and first-party vLLM/SGLang runtime surfaces.
- **World-model serving:** vLLM-Omni #6672 remains OPEN and keeps the production path explicit through #6227 realtime stateful video serving, #6646 backpressure, #5120/#6294 mid-stream interaction and #4480 generalized session memory. Its current issue-scoped realtime measurements remain about 4.5–7.0 pixel-equivalent FPS depending on TP/resolution versus the RFC target of >=12 FPS.
- **Lifecycle qualification:** #4480 remains partially landed rather than complete; generalized multi-model byte-budget/accounting/reclamation is still unfinished, and paged/CoW KV is not complete deterministic world-state ownership. SGLang #36475 remains OPEN for streaming-session disconnect/session-state corruption; fresh #37368/#37369 loading-correctness issues stay below canonical Physical-AI/Omni promotion threshold.
- **Research-map impact:** no taxonomy split/merge and no canonical paper-count change.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending.
- **Next:** #6672 → #6227/#6646/#5120/#6294 production session path → #4480 generalized session-memory accounting/reclamation → #4907/#4909 branch completeness → SGLang/SGLang-Omni lifecycle/correctness → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-02 13:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. Completed a real fresh 24h→7d SYS-first scan; 0 promotion is not 0 search.
- **Coverage:** refreshed Physical-AI/VLA serving/runtime, multimodal/Omni serving, world-model rollout/session serving, stage/modality disaggregation, cache/state infrastructure, plus first-party vLLM/SGLang runtime surfaces.
- **Session-state correction:** vLLM-Omni #4480 is **partially shipped**, not wholly unshipped. Phase 0 landed via merged PR #4487 on 2026-07-27, including the SessionStateManager contract and DreamZero port. LingBot/Cosmos3/FixedState coverage and generalized cross-session byte-budget/accounting/reclamation remain incomplete; Phase 1 PagedKV is allocator-unblocked by merged #4534.
- **Branch/disaggregation qualification:** #4907 remains KV-fork scoped rather than a complete deterministic world-state fork. SGLang-Omni #1760 remains high-value typed P/D-disaggregation roadmap evidence; unsupported resume schemas fail closed, but it is not counted as shipped until merge/release evidence lands.
- **Research-map impact:** no taxonomy split/merge and no canonical paper-count change.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending.
- **Next:** #4480 Phase-0/1 chain (#4487→#4534→LingBot/Cosmos3 ports) → #6227/#6646/#5120/#6294 production session path → #4907/#4909 completeness → SGLang-Omni #1760 landing + lifecycle/correctness → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-02 11:59 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. Completed a real fresh 24h→7d SYS-first scan; 0 promotion is not 0 search.
- **Coverage:** refreshed Physical-AI/VLA serving/runtime, multimodal/Omni serving, world-model rollout/session serving, stage/modality disaggregation and cache/state infrastructure.
- **Runtime systems update:** vLLM-Omni #6672 remains OPEN and continues to expose the production gap around realtime world-model throughput, long-lived session semantics, mid-stream interaction, stateful video serving, backpressure, paging/state memory and disaggregation. #4480 remains the generalized session-memory ownership layer; paged/CoW KV alone is not complete world-state/session ownership.
- **Benchmark/adoption:** current first-party diffusion serving benchmark code supports multiple OpenAI-compatible serving endpoints plus async video jobs. A fresh community one-H100 demo spans image/video/speech/Cosmos world-model workloads; both are runtime/adoption evidence, not new canonical papers.
- **Research-map impact:** no taxonomy split/merge and no canonical paper-count change.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending.
- **Next:** #6227 stateful-video implementation/closure → #6646 + #5120/#6294 backpressure/mid-stream interaction → #4480 typed session memory → #4907/#4909 branch completeness → SGLang-Omni lifecycle/correctness → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-02 11:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. Completed a real fresh 24h→7d SYS-first scan; 0 promotion is not 0 search.
- **Coverage:** refreshed Physical-AI/VLA serving/runtime, multimodal/Omni serving, world-model/session runtime, stage/state/cache infrastructure and first-party runtime roadmaps.
- **Runtime systems update:** vLLM-Omni #6672 remains OPEN and is the clearest current integration map for production world-model serving: #6227 realtime stateful video serving, #6646 streaming backpressure, #5120/#6294 structured mid-stream interaction and #4480 generalized session memory remain distinct runtime layers around merged baseline PR #5491. The #6227 subtree already includes concrete session-affinity/paging/runtime work; #4907 remains narrow CoW-KV branching evidence, not complete deterministic world-state ownership.
- **Qualification:** fresh SGLang #37369/#37368 RunAI streaming-weight correctness and #36690 multimodal-backend correctness remain adjacent generic serving evidence below canonical promotion threshold.
- **Research-map impact:** no taxonomy split/merge and no canonical paper-count change. Route 3/5/10 state ownership + lifecycle/backpressure remains the highest-value systems frontier.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending.
- **Next:** #6227/#6233/#6481 stateful-video path → #6646 + #5120/#6294 backpressure/mid-stream interaction → #4480 typed session memory → #4907/#4909 branch completeness → SGLang-Omni lifecycle/correctness → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-02 09:59 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. Completed a real 24h→7d SYS-first scan; 0 promotion is not 0 search.
- **Coverage:** refreshed Physical-AI/VLA serving/runtime, multimodal/Omni serving, world-model rollout/session serving, cache/state infrastructure and first-party vLLM-Omni runtime roadmaps.
- **Runtime roadmap update:** vLLM-Omni #6672 remains OPEN and documents the production gap for LingBot World 2.0 around realtime throughput, long-lived session semantics, mid-stream interaction, stateful video serving, backpressure, paging/state memory and disaggregation. #4480 remains the generalized typed session-memory ownership frontier; #6665/#6787 remain heterogeneous qualification evidence rather than paper promotions.
- **Research-map impact:** no taxonomy split/merge and no canonical paper-count change.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending.
- **Next:** #6672 → #6227/#6646/#5120/#6294 production session path → #4480 typed session memory → #4907/#4909 branch completeness → heterogeneous qualification → SGLang-Omni lifecycle/correctness → fresh 30d SYS census.

## Hourly scan — 2026-09-02 08:57 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. Completed a real fresh 24h→7d SYS-first scan; 0 promotion is not 0 search.
- **Coverage:** refreshed Physical-AI/VLA serving/runtime, multimodal/Omni serving, world-model rollout/runtime, session/cache/state infrastructure, plus first-party vLLM-Omni/SGLang-Omni implementation surfaces.
- **Runtime implementation update:** vLLM-Omni #4480 remains **OPEN**, while the underlying AR-Diffusion paged-KV allocator from #4366 / merged PR #4534 is already on `main`. This means the typed session-memory phase is allocator-unblocked, but the generalized cross-session byte-budget/session-level manager is not yet shipped. #4907 also remains OPEN and references draft #4909 for CoW KV branching; treat it as KV-branch evidence, not a complete deterministic world-state fork.
- **Research-map impact:** no taxonomy split/merge and no canonical paper-count change. Route 5/10 session-state ownership remains the highest-value systems frontier.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending.
- **Next:** #4480 typed session-memory manager implementation/landing → #4907/#4909 CoW merge/qualification + #4497 completeness → #6665/#6852/#6672 → SGLang-Omni lifecycle/correctness → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-02 08:02 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. Completed a real fresh 24h→7d SYS-first scan; 0 promotion is not 0 search.
- **Coverage:** refreshed Physical-AI/VLA serving/runtime/world-model surfaces plus first-party vLLM-Omni and SGLang-Omni runtime/release ecosystems. Fresh paper hits re-covered canonical Embodied.cpp, ROSA, PhyAI and existing session-state work; no new reusable serving/resource-management substrate crossed threshold.
- **Runtime/release update:** first-party SGLang-Omni now lists **v0.1.4** as its latest 2026-09 release. This is runtime/adoption maturity evidence, not a paper promotion and not proof that lifecycle/correctness debt is closed.
- **Research-map impact:** no taxonomy split/merge and no canonical paper-count change. Route 5/10 world-model session-state remains the highest-value systems frontier.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending.
- **Next:** #4480/#4907/#4497 session/branch-state completeness → #6665/#6852/#6672 landing/qualification → SGLang-Omni v0.1.4 changelog/lifecycle-correctness implications → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-02 06:59 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. Completed a real fresh 24h→7d SYS-first scan; 0 promotion is not 0 search.
- **Coverage:** refreshed fresh arXiv Physical-AI/VLA runtime and world-model serving surfaces plus first-party multimodal/Omni runtime ecosystems. Fresh paper hits re-covered canonical Zetta/Z-Infra and model-centric work; no new reusable serving/resource-management substrate crossed threshold.
- **Runtime/repo recheck:** Zetta/Z-Infra remains canonical CORE_SYS; its public artifact still exposes rollout/deployment infrastructure and remains a re-hit rather than a new promotion. Generic datacenter multimodal infrastructure such as Dynamo remains adjacent substrate evidence, not a new Physical-AI paper promotion.
- **Research-map impact:** no taxonomy split/merge and no canonical paper-count change. Route 5/10 session/world-model state ownership remains the highest-value next frontier.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending.
- **Next:** #4480/#4907/#4497 session/branch-state completeness → #6665/#6852/#6672 landing/qualification → SGLang lifecycle/correctness + composite routing → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-02 03:28 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. Global-watchdog recovery completed a real fresh 24h→7d SYS-first catch-up; 0 promotion is not 0 search.
- **Coverage:** refreshed Physical-AI/VLA runtime, world-model/session-state, Multimodal/Omni serving, and first-party vLLM-Omni/SGLang runtime-correctness surfaces.
- **Fresh runtime qualification:** SGLang RunAI streaming / quantized-loading reports #37369 and #37368 were retained as below-threshold generic serving-correctness evidence; neither is a new reusable Physical-AI/Omni serving substrate.
- **Research-map impact:** no taxonomy split/merge and no canonical paper-count change. vLLM-Omni #4480/#4907/#4497 plus #6672 remain the next session/state/world-model systems frontier.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending.
- **Recovery:** hourly trigger was healthy, but canonical progress and public heartbeat had remained at 2026-09-01 22:32 CST; this heartbeat records the completed catch-up without manufacturing paper changes.
- **Next:** #4480/#4907/#4497 session/branch-state completeness → #6665/#6852/#6672 landing/qualification → SGLang lifecycle/correctness + composite routing → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-01 22:32 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. Global-watchdog catch-up completed a real fresh 24h→7d SYS-first scan; 0 promotion is not 0 search.
- **Coverage:** refreshed Physical-AI/VLA runtime, world-model/session-state, Multimodal/Omni serving, streaming/full-duplex and first-party vLLM-Omni/SGLang runtime surfaces.
- **Major runtime release:** first-party vLLM-Omni releases now verify **v0.28.0** as the latest stable release (released 2026-08-31, commit `eb11446`), with 397 merged changes from 126 contributors. The final release ships scheduler-managed paged KV for diffusion, broader full-duplex/realtime speech serving, Host Weight Runtime + no-AllGather layerwise offload, AR pause/resume and event-driven orchestration, expanded heterogeneous support, and native pi0 VLA inference support. This supersedes the prior rc1-only release state.
- **Research-map impact:** no new paper-level canonical record or taxonomy split/merge, but Route 3/5/6/7/10 maturity evidence is upgraded from RC/roadmap to stable-release evidence. Generalized world-model session memory #4480 remains the next state-ownership frontier.
- **Canonical state:** paper counts and PDF manifest unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending.
- **Next:** audit v0.28.0-linked #4480/#4907/#4497 session/branch-state completeness → #6665/#6852/#6672 landing/qualification → SGLang lifecycle/correctness + composite routing → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-01 15:59 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. Real fresh 24h→7d SYS-first search completed; 0 promotion is not 0 search.
- **Coverage:** refreshed Physical-AI/robot-serving/runtime/world-model/multimodal-serving surfaces plus first-party vLLM-Omni branch/session-state and SGLang streaming-session/multimodal correctness frontiers.
- **Fresh-paper qualification:** search primarily re-hit canonical Embodied.cpp, ROSA, PhyAI, Kairos, M* and VLA-Perf; no new reusable serving/runtime substrate crossed threshold.
- **Runtime frontier:** vLLM-Omni #4907 remains OPEN. Copy-on-write AR-diffusion KV branching remains valuable for speculative branches/RL rollouts/rollback, while full deterministic world-state fork still requires session-level RNG/noise and recurrent-state completeness under #4480/#4497.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending. No taxonomy split/merge.
- **Next:** v0.28.0 milestone→release → #4907/#4480/#4497 implementation/completeness → #6665/#6852/#6672 → #36475/#36690 closure → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-01 15:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. Real fresh 24h→7d SYS-first search completed; 0 promotion is not 0 search.
- **Coverage:** refreshed Physical-AI/robot-serving/world-model/multimodal-serving arXiv surfaces plus first-party vLLM-Omni milestone/session-state and SGLang streaming-session/multimodal correctness surfaces.
- **Fresh-paper qualification:** no new reusable serving/runtime substrate crossed threshold. PUDA (arXiv:2607.26464) was checked but remains outside canonical serving scope because its primary contribution is deterministic self-driving-lab device execution/provenance rather than inference serving/resource management.
- **Runtime frontier:** vLLM-Omni `v0.28.0` milestone remains open at 50/129 closed (38%, 79 open). #4907 remains OPEN and sharpens Route 5/10 around copy-on-write AR-diffusion KV branching for speculative branches/RL rollouts/rollback, while full deterministic world-state completeness still requires session-level RNG/recurrent-state semantics under #4480/#4497. SGLang #36475/#36690 remain OPEN.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending. No taxonomy split/merge.
- **Next:** v0.28.0 milestone→release → #4907/#4480/#4497 implementation/completeness → #6665/#6852/#6672 → #36475/#36690 closure → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-01 14:01 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. Real fresh 24h→7d SYS-first search completed; 0 promotion is not 0 search.
- **Coverage:** fresh Physical-AI/robot-serving/runtime searches plus first-party vLLM-Omni milestone/session-memory and SGLang streaming-session/multimodal correctness surfaces.
- **Release state:** vLLM-Omni `v0.28.0` milestone remains open at 50/129 issues closed (38% complete) on the first-party milestone surface checked this cycle; no final `v0.28.0` release transition was verified. Stable base `vllm==0.28.0` is a separate release state.
- **Lifecycle/correctness:** SGLang #36475 remains open with a reproducible client-disconnect race causing silent session-context loss, exact KV leakage and scheduler failure; #36690 remains open multimodal correctness/attention-backend qualification evidence.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending. No taxonomy split/merge.
- **Next:** vLLM-Omni v0.28.0 milestone/release transition → #4907/#4480 implementation/lifecycle → #6665/#6852/#6672 → #36475/#36690 closure → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-01 13:01 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. Real fresh 24h→7d SYS-first search completed; 0 promotion is not 0 search.
- **Coverage:** fresh Physical-AI/robot-serving/runtime searches plus first-party vLLM-Omni release/milestone/session-memory and SGLang streaming-session/multimodal correctness surfaces.
- **Release-state resolution:** first-party GitHub surfaces show vLLM-Omni latest stable release is `v0.20.0`; milestone `v0.28.0` remains open/incomplete. Stable base `vllm==0.28.0` and the official `vllm/vllm-omni:v0.28.0` deployment image therefore do **not** prove a final vLLM-Omni `v0.28.0` GitHub release.
- **Runtime frontier:** vLLM-Omni #4907 strengthens Route 5/10 around copy-on-write AR-diffusion KV branching and explicitly points to #4480 generalized session memory as the broader ownership layer. SGLang #36475/#36690 remain lifecycle/correctness qualification signals.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending. No taxonomy split/merge.
- **Next:** track vLLM-Omni v0.28.0 milestone/release transition → #4907/#4480 implementation/lifecycle → #6665/#6852/#6672 → #36475/#36690 closure → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-01 12:01 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. Real fresh 24h→7d SYS-first search completed; 0 promotion is not 0 search.
- **Coverage:** fresh Physical-AI/robot-serving/runtime searches plus first-party vLLM-Omni installation/runtime and SGLang streaming-session/multimodal correctness surfaces.
- **Release-state correction:** stable base `vllm==0.28.0` and official `vllm/vllm-omni:v0.28.0` deployment image are verified. This does **not** independently prove a separate final vLLM-Omni GitHub release tag; own-package/tag state remains under audit.
- **Runtime qualification:** vLLM-Omni #6852 remains heterogeneous Ascend/NPU INT8 diffusion qualification evidence; SGLang #36475/#36690 remain session-lifecycle and multimodal-correctness frontiers. No new paper-level promotion.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending. No taxonomy split/merge.
- **Next:** resolve vLLM-Omni own release/tag state → #6665/#6852/#6672 → #4480 generalized world-model session memory → #36475/#36690 closure → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-01 09:31 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. No paper crossed the SYS-first threshold; 0 promotion is not 0 search.
- **Coverage:** global-watchdog recovery completed a fresh targeted 24h→7d Physical-AI + Multimodal/Omni SYS-first catch-up across fresh arXiv Physical-AI/robot-serving/runtime surfaces plus first-party vLLM/vLLM-Omni/SGLang runtime surfaces.
- **Qualification:** fresh generic streaming/KV/runtime issues were retained as below-threshold substrate evidence; no new reusable Physical-AI/Omni serving system crossed the canonical promotion threshold.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending. No taxonomy split/merge.
- **Next:** audit vLLM-Omni v0.28.0 release contents → #6665/#6852/#6672 → #4480 generalized world-model session memory → multimodal lifecycle/correctness → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-01 07:04 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. No paper crossed the SYS-first threshold; 0 promotion is not 0 search.
- **Coverage:** completed fresh 24h→7d Physical-AI + Multimodal/Omni SYS-first scan across first-party runtime/release surfaces.
- **Release/runtime qualification:** vLLM-Omni installation documentation now targets stable base vLLM 0.28.0, closing the prior base-runtime 0.28.0rc1 transition watch. This does **not** claim that vLLM-Omni itself has a new stable package release. LingBot #6672 and SGLang #36475/#36690 remain open runtime frontiers.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending. No taxonomy split/merge.
- **Next:** audit vLLM-Omni own package/release transition → #6665/#6852/#6672 → #4480 generalized world-model session memory → #36475/#36690 lifecycle/correctness → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-01 04:58 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. No paper crossed the SYS-first threshold; 0 promotion is not 0 search.
- **Coverage:** completed fresh 24h→7d Physical-AI + Multimodal/Omni SYS-first scan across fresh first-party SGLang runtime/correctness surfaces and vLLM-Omni world-model lineage.
- **Runtime qualification:** SGLang #37215 (DP=8 TCPStore EADDRINUSE on 8×H800) and #36938 (mixed-batch prefill-logprob ownership shift after retract/finish) were retained as useful general serving robustness/correctness evidence, but neither is sufficiently direct for Physical-AI/Omni canonical promotion. World-model searches re-hit existing LingBot/DreamZero lineage.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending. No taxonomy split/merge.
- **Next:** #6665/#6852/#6672 landing/fix lineage → vLLM-Omni final-release transition → #4480 generalized world-model session-memory implementation/landing → SGLang multimodal lifecycle/correctness closure → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-01 03:57 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. No paper crossed the SYS-first threshold; 0 promotion is not 0 search.
- **Coverage:** completed fresh 24h→7d Physical-AI + Multimodal/Omni SYS-first scan across fleet/runtime, unified Physical-AI runtime, multimodal serving and first-party SGLang runtime surfaces.
- **Candidate qualification:** Physical Agentic AI (arXiv:2608.22657) was checked as multi-robot orchestration evidence but remains planning/execution architecture rather than inference-serving/resource-management substrate, so no SYS promotion.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending. No taxonomy split/merge.
- **Next:** #6665/#6852/#6672 landing/fix lineage → #4480 world-model session-memory → multimodal lifecycle/correctness → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-01 02:58 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. No paper crossed the SYS-first threshold; 0 promotion is not 0 search.
- **Coverage:** completed fresh 24h→7d Physical-AI + Multimodal/Omni SYS-first scan across arXiv fresh surfaces and first-party vLLM-Omni/SGLang runtime ecosystems.
- **Runtime qualification:** fresh SGLang #37215 is a generic distributed-serving TCPStore/DP initialization failure signal, not a direct Physical-AI/Multimodal promotion; vLLM-Omni world-model and heterogeneous hits were existing/canonical.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending. No taxonomy split/merge.
- **Next:** #6665/#6852/#6672 landing/fix lineage → vLLM-Omni final-release transition → #4480 generalized world-model session-memory implementation/landing → SGLang multimodal lifecycle/correctness closure → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-01 02:02 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. No paper crossed the SYS-first threshold; 0 promotion is not 0 search.
- **Coverage:** completed fresh 24h→7d Physical-AI + Multimodal/Omni SYS-first searches across arXiv and first-party vLLM-Omni/SGLang runtime surfaces.
- **Runtime/session check:** fresh results re-hit canonical ROSA, Embodied.cpp, Kairos, PhyAI, M* and existing world-model/session-runtime RFCs. vLLM-Omni #4480 remains the generalized world-model session-memory frontier; BWM #4903 and OmniDreams #4126 remain model-integration evidence rather than new system papers.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending. No taxonomy split/merge.
- **Next:** #6665/#6852/#6672 landing/fix lineage → final-release transition → #4480 session-memory implementation/landing → multimodal correctness/lifecycle closure → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-01 01:01 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. No paper crossed the SYS-first threshold; 0 promotion is not 0 search.
- **Coverage:** completed fresh 24h→7d Physical-AI + Multimodal/Omni SYS-first scan across arXiv fresh surfaces and first-party vLLM-Omni/SGLang runtime ecosystems.
- **Runtime/release check:** vLLM-Omni v0.28.0rc1 remains the newest verified release surface; no final v0.28.0 transition or new paper-level system promotion was verified this cycle. Fresh arXiv hits were canonical or algorithm-centric.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending. No taxonomy split/merge.
- **Next:** #6665/#6852/#6672 landing/fix audit → v0.28 final-release transition → multimodal correctness/lifecycle closure → fresh 30d SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-09-01 00:31 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. No paper crossed the SYS-first threshold; 0 promotion is not 0 search.
- **Coverage:** catch-up rechecked current arXiv fresh surfaces for Physical-AI/robot-serving/runtime terms, vLLM-Omni official release/runtime surfaces, and SGLang multimodal/streaming-runtime surfaces after two triggered cycles produced no durable research checkpoint.
- **Result:** fresh hits were either already-canonical Physical-AI anchors (including PhyAI), generic serving work without direct Physical-AI/Multimodal systems novelty, or existing runtime roadmap/qualification themes. No new reusable fleet/runtime/resource-management paper was verified.
- **Canonical state:** unchanged at 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; no new paper triggered a PDF download or taxonomy split/merge.
- **Next:** resume #6665/#6852/#6672 landing/fix audit → multimodal correctness/lifecycle closure → fresh 30d SYS census → remaining legal PDF debts.

## Hourly scan — 2026-08-31 19:03 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. No paper crossed the SYS-first threshold; 0 promotion is not 0 search.
- **Coverage:** completed fresh Physical-AI + Multimodal/Omni 24h→7d SYS-first scans plus targeted heterogeneous/diffusion runtime follow-up.
- **Runtime qualification:** SGLang #36853 reports native Qwen-Image diffusion serving with SP=4 on 4×48GB GPUs being killed by host OOM while loading DiT. Treat this as Route 6 and adjacent Route 10 qualification evidence, not a paper promotion. vLLM-Omni #6852 remains the Ascend/NPU INT8 diffusion qualification frontier.
- **Canonical state:** 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending. No new paper triggered a PDF download.
- **Taxonomy:** unchanged; heterogeneous diffusion/world-model serving remains an active systems qualification gap.
- **Next:** #36853 root-cause/fix/CI → #6852 → #6665 child-issue landing → #37187/#37183 → #36690 regression closure → #6672 interactive world-model lineage → vLLM #54288/#54193 → SGLang-Omni #1724 → fresh 30d Multimodal SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-08-31 18:02 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. No paper crossed the SYS-first threshold; 0 promotion is not 0 search.
- **Coverage:** completed real Physical-AI + Multimodal/Omni 24h→7d scans plus targeted 30d diffusion/heterogeneous-runtime follow-up.
- **Runtime roadmap:** vLLM-Omni #6665 (Boogu-Image) sharpens Route 6/10 maturity debt: current native serving is single-GPU, while multi-GPU TP/SP/CFG/HSDP and CPU/layerwise offload remain planned/unvalidated. #6852 remains open Ascend/NPU INT8 diffusion qualification debt.
- **Canonical state:** 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending. No new paper triggered a PDF download.
- **Taxonomy:** unchanged; heterogeneous placement/offload for diffusion/world-model serving remains an active systems gap.
- **Next:** #6665 child-issue landing audit + #6852 fix/CI → #37187/#37183 → #36690 regression closure → #6672 interactive world-model lineage → vLLM #54288/#54193 → SGLang lifecycle/cache → SGLang-Omni #1724 → fresh 30d Multimodal SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-08-31 17:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / paper WATCH +0. No paper crossed the SYS-first threshold; 0 promotion is not 0 search.
- **Coverage:** completed fresh Physical-AI + Multimodal/Omni 24h→7d scans plus targeted heterogeneous/world-model/runtime follow-up. Fresh paper queries re-hit canonical Kairos, PhyAI, LiveServe and M*; no new reusable serving substrate was verified.
- **Runtime qualification:** vLLM-Omni #6852 remains the freshest direct heterogeneous Omni signal: Ascend/NPU MiniMax-H3 diffusion with INT8 online quantization fails in the reported distributed-offload/cache/sparse-attention configuration. Keep this as Route 6/10 WATCH evidence, not a paper promotion or framework-wide incompatibility claim.
- **Canonical state:** 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending. No new paper triggered a PDF download.
- **Taxonomy:** unchanged; heterogeneous serving and stateful world-model serving remain active qualification frontiers.
- **Next:** #6852 fix/CI audit → #37187/#37183 linked fixes → #36690 regression closure → #6672 interactive world-model lineage → vLLM #54288/#54193 → SGLang lifecycle/cache correctness → SGLang-Omni #1724 → fresh 30d Multimodal SYS census → remaining 4 legal PDF debts.

## Hourly scan — 2026-08-31 12:58 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH paper-record +0. Runtime-roadmap watch +1: vLLM-Omni [#6672](https://github.com/vllm-project/vllm-omni/issues/6672).
- **Coverage:** completed real Physical-AI + Multimodal/Omni 24h→7d fresh scans plus targeted 30d world-model/session/runtime checks; no new paper crossed the SYS-first threshold.
- **World-model serving frontier:** #6672 moves LingBot World 2.0 from basic offline integration toward production-like interactive serving. First-party realtime measurements are ~4.5–4.7 pixel-equivalent FPS on 1×H200 and ~6.8–7.0 FPS on 2×H200; target is ≥12 FPS on at most 2 H-series GPUs.
- **System mechanisms under watch:** one long-lived request/session, mid-stream camera+prompt updates, streaming VAE decode, session affinity, backpressure, paged-KV/session-memory sizing, regression/profiling harnesses and disaggregated diffusion inference. These strengthen Routes 3/5/7/10, but remain issue/roadmap evidence until merged/released.
- **Current canonical state:** 161 papers/works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; 154 valid internal PDFs, 4 pending. Public repo contains no PDFs or private server state.
- **Next:** #6672 lineage landing/release audit (#6227/#6233/#6533/#6534/#6646/#6294/#4590) → vLLM #54288/#54193 closure → SGLang lifecycle fixes → SGLang-Omni #1724/leaf cleanup → post-TimelyLLM/TypeGo successor census → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-29 13:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Physical-AI and Multimodal/Omni 24h→7d scans plus targeted 30d lifecycle/cache/runtime checks completed; no new paper crossed the SYS-first threshold.
- **Physical AI:** fresh fleet/runtime/control-loop/edge/shared-state/heterogeneous/composite VLA+WAM+planner/evaluation/world-model searches produced canonical or algorithm/application-centric hits; no new reusable serving substrate was verified.
- **vLLM KV-offload:** issue [#54193](https://github.com/vllm-project/vllm/issues/54193) remains OPEN; fix PR [#54288](https://github.com/vllm-project/vllm/pull/54288) is the concrete review frontier for excluding the unwritten final sampled-token KV slot from decode-side offload storage. Keep this fix-in-review until merge/release.
- **SGLang lifecycle:** [#36333](https://github.com/sgl-project/sglang/issues/36333) remains OPEN with #36418 as the zombie-request fix path; [#36475](https://github.com/sgl-project/sglang/issues/36475) remains a separate streaming-session rollback/KV-leak crash. No shipped closure verified this cycle.
- **SGLang-Omni cache:** #1723/#1724 remains active; no verified merge/release. Persistent lazy eviction addresses O(leaves) scheduler overhead, while zero-token leaf lifecycle growth remains a separate cleanup/ownership frontier.
- **vLLM-Omni:** #6403 and #6413/#6439 remain open cancellation/reclamation evidence; no new shipped closure verified.
- **Current state:** 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** #54288 merge/CI → #36333/#36418 + #36475 closure → #1724 merge/CI + zero-token leaf cleanup → vLLM-Omni #6453/#6403/#6413/#6439 → #1754/#1760 landing → post-TimelyLLM/TypeGo successor census → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-29 12:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Physical-AI and Multimodal/Omni 24h→7d scans plus targeted 30d lifecycle/cache/runtime checks completed; no new paper crossed the SYS-first threshold.
- **Physical AI:** fresh fleet/runtime/control-loop/edge/shared-state/heterogeneous/composite VLA+WAM+planner/evaluation/world-model searches re-hit canonical PhyAI/Zetta-class anchors or model/algorithm-centric work; no new reusable serving substrate was verified.
- **vLLM KV-offload fix in review:** issue [#54193](https://github.com/vllm-project/vllm/issues/54193) now links OPEN PR [#54288](https://github.com/vllm-project/vllm/pull/54288). It changes the finished-request offload watermark to `req.num_tokens - 1`, so the final sampled token whose KV was never computed is not persisted. The PR reports 241 passed / 2 skipped in its connector unit suite; this remains PR-scoped until merge/release.
- **Integrity correction:** an earlier private scan note misidentified SGLang #36877. [#36877](https://github.com/sgl-project/sglang/issues/36877) is the Anthropic rolling-`cache_control` prefix-cache invalidation issue. The disconnected-streaming zombie-request issue is [#36333](https://github.com/sgl-project/sglang/issues/36333), while [#36475](https://github.com/sgl-project/sglang/issues/36475) is the separate streaming-session disconnect rollback/KV-leak crash. The radar now tracks these as distinct lifecycle/cache contracts.
- **SGLang-Omni:** PR #1724 remains active/open in current first-party activity; no verified merge/release this cycle. Persistent lazy eviction heap and zero-token leaf cleanup remain separate runtime frontiers.
- **Current state:** 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** vLLM #54288 merge/CI → SGLang #36333/#36418 + #36475 lifecycle closure → #36877 cache-control correctness → SGLang-Omni #1724/leaf cleanup → vLLM-Omni lifecycle/cancellation/reclamation → #1754/#1760 landing → post-TimelyLLM/TypeGo successor census → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-29 10:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Physical-AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/session-lifecycle/correctness checks completed; no new paper crossed the SYS-first threshold.
- **Physical AI:** fresh fleet/runtime/control-loop/edge/shared-state/heterogeneous/composite VLA+WAM+planner/evaluation/world-model searches re-hit canonical anchors; no new reusable serving substrate was verified.
- **vLLM-Omni realtime maturity:** issue [#6474](https://github.com/vllm-project/vllm-omni/issues/6474) is now closed through merged PR [#6564](https://github.com/vllm-project/vllm-omni/pull/6564) (merged 2026-08-26). The fix handles a final-stage raw terminal with no processed output by emitting an exactly-once terminal completion for non-duplex realtime requests, preventing the client from waiting forever for `response.audio.done`. First-party validation reports 3 targeted terminal regressions, 197 related CPU tests, and a long-audio Qwen3-Omni realtime GPU regression on 2×L20X passed.
- **Lifecycle guard:** this closes one concrete completion failure mode, not the full session-lifecycle problem. Request-scoped mutable stage state [#6453](https://github.com/vllm-project/vllm-omni/issues/6453), queued-vs-running / true cancellation [#6403](https://github.com/vllm-project/vllm-omni/issues/6403), and aborted-diffusion output reclamation [#6413](https://github.com/vllm-project/vllm-omni/issues/6413) remain separate active frontiers.
- **Current state:** 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** #6453 → #6403 → #6413/#6439 post-#6564 lifecycle audit → SGLang-Omni #1724 merge/CI + zero-token leaf cleanup → #1754/#1726/#1753 landing → #1760 Stage-1/placement/overload → post-TimelyLLM/TypeGo successor census → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-29 09:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Physical-AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/session-lifecycle/correctness checks completed; no new paper crossed the SYS-first threshold.
- **Physical AI:** fresh fleet/runtime/control-loop/edge/shared-state/heterogeneous/composite VLA+WAM+planner/evaluation/world-model searches re-hit canonical anchors or model/algorithm-centric work; no new reusable serving substrate was verified.
- **Multimodal / Omni:** SGLang-Omni #1723/#1724 remains the active cache/runtime frontier from the prior hour; no verified #1724 merge/release was found, and zero-token leaf lifecycle remains a separate unresolved concern. Fresh SGLang #36894 is adjacent general scheduler-lifecycle evidence (LoRA unload deadlock after parallel-sampling traffic), not a direct Physical-AI/Multimodal promotion.
- **Current state:** 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** #1724 merge/CI + leaf-lifecycle cleanup → #1754 T-PR7→T-PR14/T-PR19 + #1726/#1753 → #1760 #1517 + placement/sizing/overload chain → post-TimelyLLM/TypeGo successor census → vLLM-Omni lifecycle/batching → correctness closure → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-29 08:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Physical-AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/session-lifecycle/correctness checks completed; no new paper crossed the SYS-first threshold.
- **New runtime signal:** first-party SGLang-Omni #1723 identifies an O(leaves) radix-cache eviction heap rebuild on the scheduler thread once the KV pool saturates. Under the reported zero-hit short-request workloads, qwen3_tts c32 loses ~17–19% QPS and audio-TTFP p95 rises ~62%; qwen3_asr can collapse by ~92% QPS. This is runtime/cache evidence, not a paper promotion.
- **Fix maturity:** linked PR #1724 remains OPEN. Its persistent lazy eviction heap reports post-saturation qwen3_tts +19% QPS / -18% p95 and qwen3_asr roughly 4–5x QPS with ~5x lower p95 versus the affected baseline; additional soak data keeps per-evict p50 around 50–66 us as leaves grow. Treat all numbers as PR-scoped until merge/release.
- **Lifecycle caveat:** #1724 also reports zero-token partition leaves accumulating under unique `extra_key`; the heap fix bounds eviction cost but does not itself prove that underlying leaf growth is cleaned up. Track leaf lifecycle/state ownership separately.
- **Current state:** 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** #1724 merge/CI + leaf-lifecycle cleanup → #1754 T-PR7→T-PR14/T-PR19 + #1726/#1753 → #1760 #1517 + placement/overload chain → post-TimelyLLM/TypeGo successor census → vLLM-Omni lifecycle/batching → correctness closure → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-29 07:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Physical-AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/session-lifecycle/correctness checks completed; no new paper crossed the SYS-first threshold.
- **Physical AI:** post-TimelyLLM/TypeGo successor, fleet/control-loop, edge/shared-state, heterogeneous execution, composite VLA+WAM+planner, evaluation/workload and world-model rollout searches produced canonical or below-threshold hits; no new reusable paper-level serving substrate verified.
- **Multimodal / Omni maturity update:** SGLang-Omni Qwen3-TTS roadmap #1754 remains OPEN. T-PR2 / PR #1675 is now explicitly verified as merged into `main` on 2026-08-27, adding CUDA-Graph capture for follow-up vocoder decodes. First-party H200 measurements at c16 report +6.2%/+8.8% throughput in two candidate servers, 6.3%/9.0% lower mean inter-chunk latency, and 13.8%/15.4% lower p95 inter-chunk latency; c1 is within noise. Metrics remain PR-scoped.
- **Still open:** #1726 mixed sampled/argmax batching and #1753 batched reference encoding remain OPEN; stateful incremental Codec ownership/cancellation-safe reuse, slack/playback-aware scheduling, admission retuning and streaming-readiness/backpressure remain roadmap work. P/D roadmap #1760 still says nothing has merged; Stage-1 #1517 remains the gate.
- **Current state:** 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** #1754 T-PR7→T-PR14/T-PR19 + #1726/#1753 landing → #1760 #1517 + placement/overload chain → post-TimelyLLM/TypeGo successor census → vLLM-Omni lifecycle/batching → SGLang/SGLang-Omni correctness closure → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-29 06:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Physical-AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/session-lifecycle/correctness checks completed; no new paper crossed the SYS-first threshold.
- **Physical AI:** post-TimelyLLM/TypeGo successor, fleet/control-loop, edge/shared-state, heterogeneous execution, composite VLA+WAM+planner, evaluation/workload and world-model rollout searches produced canonical or below-threshold hits; no new reusable paper-level serving substrate verified.
- **Multimodal / Omni shipped-vs-open update:** SGLang-Omni Qwen3-TTS roadmap #1754 now has a concrete landed production-readiness item: PR #1786 merged into main on 2026-08-28, moving vocoder CUDA-Graph capture into synchronous warmup before readiness publication. First-party PR evidence reports 218 focused tests passed, 10/10 fresh H100 starts, and 10/10 immediate warmups without the prior capture/readiness failure. Mixed-sampling PR #1726 and reference-batching PR #1753 remain OPEN; stateful incremental Codec state ownership, slack/playback-aware scheduling, admission retuning and streaming backpressure/readiness remain roadmap work.
- **P/D guard:** SGLang-Omni #1760 still explicitly states that nothing has merged; do not treat its P/D design as shipped support.
- **Current state:** 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** #1754 T-PR7→T-PR14/T-PR19 and #1726/#1753 landing status → #1760 Stage-1 gate #1517 → post-TimelyLLM/TypeGo successor census → vLLM-Omni lifecycle/batching → SGLang/SGLang-Omni correctness closure → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-29 05:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Physical-AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/session-lifecycle/correctness checks completed; 0 promotion is not 0 search.
- **Physical AI:** no new paper-level SYS promotion; post-TimelyLLM/TypeGo successor, fleet/control-loop, edge/shared-state, heterogeneous execution, composite VLA+WAM+planner, evaluation/workload and world-model rollout searches stayed within canonical anchors or below-threshold work.
- **Multimodal / Omni runtime watch:** SGLang-Omni **#1754** materially sharpens the Qwen3-TTS production-serving roadmap around stateful incremental Codec decoding, request-slot-indexed state, cancellation/finish-safe slot reuse, COLD/WARM CUDA Graphs, compatibility/slack-aware vocoder scheduling, playback-pressure feedback into Talker scheduling, named serving profiles, admission retuning, and explicit streaming-readiness/backpressure hardening. This is an ecosystem/runtime roadmap, not a paper promotion.
- **Correctness/heterogeneity watch:** fresh first-party issue **#1782** reports Qwen3-Omni text-only startup failure with thinker TP>1; the NPU roadmap (#1597) remains partially implemented with CI/model coverage still incomplete. These are qualification signals only.
- **Current state:** 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** trace #1754 T-PR7→T-PR14/T-PR19 landing chain and cancellation/state-slot tests → #1760 P/D-disaggregation merge gates → post-TimelyLLM/TypeGo successor census → vLLM-Omni lifecycle/batching → SGLang/SGLang-Omni correctness closure → fresh 30d Multimodal SYS census → legal PDF debt retry.

## Hourly scan — 2026-08-29 04:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Physical-AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/session-lifecycle/correctness checks completed.
- **Physical AI:** no new paper-level SYS promotion; post-TimelyLLM/TypeGo successor searches and fleet/control-loop/runtime/state/world-model serving scans stayed within canonical anchors or below-threshold work.
- **Multimodal / Omni runtime watch:** SGLang-Omni **#1760** is a new high-value P/D-disaggregation roadmap. It specifies generic stage expansion, typed continuation handoff, exactly-once ownership transfer, CUDA-IPC paged-KV movement, free placement/sizing, overload visibility and future N:M prefill/decode ratios. Current first-party status explicitly says **nothing has merged**, so this is tracked as strong runtime-frontier evidence, not shipped capability or a paper promotion. The roadmap reports one-H200 overlapped-prefill inter-token gap at 2.28× non-overlap, same-GPU PD p95 first-token time <0.65 s versus 26 s for a colocated replica in the cited measurement, and a second decode half giving +46% at c8 / +66% at c16 for 1024-token prompts while providing no gain at 8128 tokens.
- **Heterogeneous/runtime watch:** SGLang-Omni **#1777** is an open Intel CPU-support roadmap; #1779 reports a Qwen3-TTS profiler deadlock at concurrency 16. These are ecosystem signals only.
- **Current state:** 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** follow #1760 Stage-1 gate (#1517) and Stage-2/3 placement+overload work to merge/release → post-TimelyLLM/TypeGo successor census → vLLM-Omni batching/lifecycle audit → SGLang-Omni queue/KV correctness + soak/CI closure → fresh 30d Multimodal SYS census → legal PDF debt retry.

## Hourly scan — 2026-08-29 03:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Independent Physical-AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/session-lifecycle/correctness checks completed.
- **Physical AI:** no new paper-level SYS promotion; fleet/multi-robot, unified/control-loop runtime, edge/shared-state, heterogeneous execution, composite VLA+WAM+planner, evaluation/workload and world-model rollout searches stayed within canonical anchors or below-threshold work.
- **Multimodal / Omni runtime watch:** vLLM-Omni #6705 is OPEN for request-level batching support for Boogu-Image; #6691 is an OPEN RFC for model-owned dummy-run plans aligned with serving task mode. SGLang-Omni #1707 is a queue-depth/KV-slot correctness signal and #1697 a KV-budget sizing signal. These are runtime/ecosystem evidence, not paper promotions.
- **Release guard:** first-party vLLM-Omni releases still list **v0.28.0rc1** as latest; no final v0.28.0 claim is made.
- **Current state:** 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** post-TimelyLLM/TypeGo successor census → vLLM-Omni batching/lifecycle audit → SGLang-Omni queue/KV correctness + soak/CI closure → SGLang streaming/multimodal correctness → fresh 30d Multimodal SYS census → legal PDF debt retry.

## Hourly scan — 2026-08-29 02:01 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Independent Physical-AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/session-lifecycle/correctness checks completed.
- **Physical AI:** no new paper-level SYS promotion; fresh fleet/multi-robot, unified/control-loop runtime, edge/shared-state, heterogeneous execution, composite VLA+WAM+planner, evaluation/workload and world-model rollout queries re-hit canonical anchors or below-threshold work.
- **Multimodal / Omni:** no new paper promotion. SGLang #36475 remains a streaming-session lifecycle correctness signal; #36690 remains OPEN for Gemma-3n multimodal degeneration/crash. First-party vLLM-Omni releases still list **v0.28.0rc1** as latest, so no final v0.28.0 claim is made.
- **PDF retry:** TimelyLLM and TypeFly official arXiv downloads were retried from the research host and again hit TLS connect errors; both remain `PENDING_RETRY`, with no invalid file counted.
- **Current state:** 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** retry TimelyLLM/TypeFly when TLS recovers → post-TimelyLLM/TypeGo successor census → SGLang #36475/#36690 → vLLM-Omni lifecycle/cancellation/reclamation → SGLang-Omni #1593 → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-29 01:02 CST

- **Promotions:** CORE_SYS +1 — **TimelyLLM** (MobiSys 2026 Best Paper Runner-up + Best Artifact Runner-up, A+, Routes 1/3/8); SYS_ALG_BOUNDARY +1 — **TypeFly** (IEEE TMC 2025, A, Routes 3/4/7); WATCH +0.
- **Why TimelyLLM matters:** direct time-sensitive serving for multiple robotic agents; segmented generation/scheduling overlaps future plan generation with physical execution and reports up to 1.97x higher time utility and 84% lower waiting time.
- **Why TypeFly stays boundary:** MiniSpec + stream interpretation enables early robot execution and forms a useful edge/cloud runtime, but compact plan representation is co-primary with systems design. Official Apache-2.0 repo: ~110 stars / 25 forks in current public crawl.
- **Fresh scan:** independent Physical-AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/session-lifecycle checks found no additional paper-level SYS promotion.
- **Current state:** 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** TimelyLLM/TypeGo successor census → SGLang #36475/#36690 → vLLM-Omni lifecycle/cancellation/reclamation → SGLang-Omni #1593 → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-28 22:01 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Physical AI and Multimodal/Omni 24h→7d fresh scans plus targeted 30d runtime/streaming/edge-freshness/lifecycle/correctness checks completed.
- **Physical AI:** no new SYS-first paper; fleet/multi-robot, unified/control-loop runtime, edge/shared-state, heterogeneous execution, composite VLA+WAM+planner, evaluation/workload and world-model rollout searches stayed within canonical anchors or below-threshold work.
- **Multimodal / Omni runtime watch:** no paper promotion. Fresh first-party SGLang #36475 reports a streaming-session lifecycle failure mode: client disconnect can drop session context and an immediate same-session continuation can crash the scheduler. Track as runtime/session-state evidence, not as a paper. #36690 remains open for Gemma-3n multimodal correctness; SGLang-Omni #1593 remains open for failure-path observability + soak/CI closure.
- **Current state:** 158 works = 114 CORE_SYS / 34 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** SGLang #36475 session-state recovery/fix/CI → #36690 correctness closure → AoL/TWI runtime-successor + StreamMind full-agent release → vLLM-Omni lifecycle/cancellation audit → SGLang-Omni #1593 soak/CI → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-28 21:02 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Independent Physical AI and Multimodal/Omni 24h→7d fresh scans plus targeted 30d runtime/streaming/edge-freshness/lifecycle/correctness checks completed.
- **Physical AI:** no new SYS-first paper; fleet/multi-robot, unified/control-loop runtime, edge/shared-state, heterogeneous execution, composite VLA+WAM+planner, evaluation/workload and world-model rollout searches stayed within canonical anchors or below-threshold work.
- **Multimodal / Omni:** no paper promotion. First-party SGLang #36690 remains OPEN for Gemma-3n multimodal correctness and #36678 remains OPEN for opt-in per-request metrics; no merged fix/implementation was verified this cycle.
- **Current state:** 158 works = 114 CORE_SYS / 34 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** AoL/TWI runtime-successor + StreamMind full-agent release → SGLang #36690/#36678 → vLLM-Omni #6453/#5822/#6439/#6403 → SGLang-Omni #1593 soak/CI → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-28 20:03 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Independent Physical AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/streaming/edge-freshness/lifecycle/correctness checks completed.
- **Physical AI:** no new SYS-first paper; fleet/multi-robot, unified/control-loop runtime, edge/shared-state, heterogeneous execution, composite VLA+WAM+planner, evaluation/workload and world-model rollout searches stayed within canonical anchors or below-threshold work.
- **Multimodal / Omni:** no paper promotion. Fresh serving scans re-hit M*, HorizonServe, Cornfigurator/Cornserve, LiveServe and TurboServe. SGLang #36690 remains OPEN for Gemma-3n multimodal correctness and #36678 remains OPEN for opt-in per-request metrics; fresh #36830/#36829/#36822/#36820/#36807/#36802 are adjacent runtime qualification signals only.
- **Current state:** 158 works = 114 CORE_SYS / 34 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** AoL/TWI runtime-successor + StreamMind full-agent release → SGLang #36690/#36678 → vLLM-Omni #6453/#5822/#6439/#6403 → SGLang-Omni #1593 soak/CI → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-28 19:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Independent Physical AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/streaming/edge-freshness/lifecycle/correctness checks completed.
- **Physical AI:** no new SYS-first paper; fleet/multi-robot, unified runtime, control-loop, edge/shared-state, heterogeneous execution, composite VLA+WAM+planner, evaluation and world-model rollout searches returned canonical or below-threshold work.
- **Multimodal / Omni:** no new paper promotion. Fresh searches re-hit M*, HorizonServe, LiveServe, TurboServe and Cornserve. Fresh SGLang issues #36802/#36822 are text/MoE runtime correctness/performance signals, not direct Physical-AI/Multimodal paper promotions; existing #36690/#36678 and lifecycle/cancellation frontiers remain separately tracked.
- **Current state:** 158 works = 114 CORE_SYS / 34 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** AoL/TWI runtime-successor + StreamMind full-agent release → SGLang #36690/#36678 → vLLM-Omni #6453/#5822/#6439/#6403 → SGLang-Omni #1593 soak/CI → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-28 16:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Independent Physical AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/streaming/edge-freshness/lifecycle/correctness checks completed.
- **Physical AI:** no new SYS-first paper; fleet/control-loop, unified runtime, edge/shared-state, heterogeneous execution, evaluation and world-model rollout searches returned canonical or below-threshold work.
- **Multimodal / Omni:** no new paper promotion. Fresh scans re-hit HorizonServe and StreamArena/StreamMind. SGLang #36690/#36678 and SGLang-Omni #1593 remain open without verified closure; StreamMind remains A until the full agent implementation is publicly verified.
- **Current state:** 158 works = 114 CORE_SYS / 34 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** AoL/TWI runtime-successor + StreamMind full-agent release → SGLang #36690/#36678 → vLLM-Omni #6453/#5822/#6439/#6403 → SGLang-Omni #1593 soak/CI → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-28 14:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Independent Physical AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/streaming/edge-freshness and lifecycle/correctness checks completed.
- **Physical AI:** no new SYS-first paper; fresh queries re-hit canonical ROSA/Kairos/PhyAI/PhyAgentOS and below-threshold algorithm/survey work.
- **Multimodal / Omni:** no new paper promotion. Fresh serving searches re-hit canonical M*/HorizonServe/vLLM-Omni/LiveServe. First-party checks confirm SGLang #36690 and #36678, vLLM-Omni #6453/#6403, and SGLang-Omni #1593 remain open without verified closure.
- **Current state:** 158 works = 114 CORE_SYS / 34 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** AoL/TWI runtime-successor + StreamMind full-agent release → SGLang #36690/#36678 → vLLM-Omni #6453/#5822/#6439/#6403 under v0.28.0rc1 → SGLang-Omni #1593 soak/CI → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-28 13:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Independent Physical AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/streaming/edge-freshness checks completed.
- **Physical AI:** no new paper-level SYS promotion; fleet/control-loop, unified runtime, shared-state/runtime-recomposition, edge/freshness and evaluation searches re-hit canonical PhyAI/Kairos/Embodied.cpp/vla.cpp or below-threshold model/algorithm work.
- **Multimodal / Omni:** fresh serving/runtime searches re-hit canonical M*/vLLM-Omni and current streaming-state systems. PyPI verifies `vllm-omni 0.28.0rc1` released 2026-08-27 while 0.26.0 remains labeled stable; the RC/pre-release guard remains in force and open lifecycle/cancellation/reclamation items stay separately audited.
- **Current state:** 158 works = 114 CORE_SYS / 34 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** AoL/TWI runtime-successor + StreamMind release watch → SGLang #36690/#36678 → vLLM-Omni #6453/#5822/#6439/#6403 under v0.28.0rc1 → SGLang-Omni #1593 soak/CI → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-28 12:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Independent Physical AI and Multimodal/Omni 24h→7d scans plus targeted 30d Age-of-Latent/TWI, streaming-state and runtime-correctness checks completed.
- **Physical AI:** AoL/TWI reverse census found no reusable runtime-backed successor beyond the existing SYS_ALG boundary work; fleet/control-loop/runtime/world-model searches stayed within canonical anchors or below-threshold model/algorithm work.
- **Multimodal / streaming:** official StreamArena repo still marks the paper's full StreamMind agent as `coming soon`; only the streaming evaluation driver/base class is available. Fresh serving searches re-hit canonical vLLM-Omni, M*, HorizonServe and LiveServe.
- **Production runtime:** SGLang #36690 remains OPEN with no verified fix/regression-CI closure; #36678 remains OPEN as an opt-in per-request metrics request.
- **Current state:** 158 works = 114 CORE_SYS / 34 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** AoL/TWI runtime-successor census → StreamMind full-agent release → #36690/#36678 → vLLM-Omni #6453/#5822/#6439/#6403 under v0.28.0rc1 → SGLang-Omni #1593 soak/CI → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-28 09:03 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Independent Physical AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/correctness/lifecycle/failure-observability checks completed.
- **Physical AI:** no new paper-level SYS promotion; fleet/control-loop, unified runtime, edge/device, shared-state/runtime-recomposition, evaluation and WAM/world-model searches remained within canonical anchors or model/algorithm-centric work.
- **Multimodal / Omni:** SGLang #36690 remains OPEN with no verified fix/regression-CI closure; #36678 remains OPEN as an opt-in per-request metrics request. vLLM-Omni #6453/#5822/#6403 remain open lifecycle/preemption/cancellation frontiers; SGLang-Omni #1593 remains open after #1595 merged.
- **Current state:** 156 works = 113 CORE_SYS / 33 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** #36690 root-cause/fix/regression-CI → #36678 implementation/consumer path → vLLM-Omni #6453/#5822/#6439/#6403 under v0.28.0rc1 → SGLang-Omni #1593 remaining slot-pool failure instrumentation + soak/CI-nightly → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-28 08:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Independent Physical AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/correctness/lifecycle/failure-observability checks completed.
- **Physical AI:** fresh fleet/control-loop, unified-runtime, edge/device, shared-state/runtime-recomposition, evaluation and WAM/world-model searches produced canonical or model/algorithm-centric hits; no new paper-level SYS promotion.
- **Multimodal / Omni:** first-party SGLang #36690 and #36678 remain open with no verified fix/implementation closure; vLLM-Omni #6453/#6403 remain open lifecycle/cancellation frontiers; SGLang-Omni #1593 remains open after #1595 merged, with the four slot-pool failure events and comm-layer-triggered soak/CI-nightly still unverified as landed.
- **Current state:** 156 works = 113 CORE_SYS / 33 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** #36690 root-cause/fix/regression-CI → #36678 implementation/consumer path → vLLM-Omni #6453/#5822/#6439/#6403 under v0.28.0rc1 → SGLang-Omni #1593 slot-pool failure instrumentation + soak/CI-nightly → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-28 07:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Independent Physical AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/correctness/lifecycle/failure-observability checks completed.
- **Physical AI:** no new paper-level SYS promotion; fleet/control-loop, unified runtime, edge/device, shared-state/runtime-recomposition, evaluation and WAM/world-model searches stayed within canonical anchors or below-threshold model/algorithm work.
- **Multimodal / Omni:** SGLang #36690 remains OPEN with shared-KV-cache suspicion and no verified fix/regression-CI closure; #36678 remains OPEN as an opt-in per-request metrics request. SGLang-Omni #1593 remains OPEN after #1595 merged, with slot-pool failure events and comm-layer-triggered soak/CI-nightly still unverified as landed.
- **Current state:** 156 works = 113 CORE_SYS / 33 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** #36690 root-cause/fix/regression-CI → #36678 implementation/consumer path → vLLM-Omni #6453/#5822/#6439/#6403 under v0.28.0rc1 → SGLang-Omni #1593 slot-pool failure instrumentation + soak/CI-nightly → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-28 06:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Independent Physical AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/correctness/lifecycle/failure-observability checks completed.
- **Physical AI:** no new paper-level SYS promotion; fresh serving/runtime/fleet/control-loop/state/evaluation searches re-hit canonical ROSA/Kairos/PhyAI/M* or below-threshold work.
- **Multimodal / Omni:** SGLang #36690/#36678 remain OPEN. vLLM-Omni #6453/#6403/#5822 remain OPEN lifecycle/cancellation/preemption frontiers. SGLang-Omni #1593 still lacks verified landing of the remaining slot-pool failure events and comm-layer-triggered soak/CI-nightly policy.
- **Current state:** 156 works = 113 CORE_SYS / 33 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** #36690 root-cause/fix/regression-CI → #36678 request-metrics implementation/consumer path → vLLM-Omni #6453/#5822/#6439/#6403 shipped-vs-open audit under v0.28.0rc1 → SGLang-Omni #1593 slot-pool failure instrumentation + soak/CI-nightly → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-28 05:01 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Independent Physical AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/correctness/lifecycle checks completed.
- **Physical AI:** no new paper-level SYS promotion; fleet/control-loop, shared-state/runtime-recomposition, evaluation and world-model-runtime searches stayed within canonical anchors or below-threshold work.
- **Multimodal / Omni:** SGLang #36690 remains OPEN with no linked branch/PR in current first-party evidence; the report points to Gemma-3n shared-KV-cache correctness across tested attention backends. #36678 remains an OPEN per-request metrics feature request. vLLM-Omni #6453/#6403/#6413 remain OPEN lifecycle/cancellation/reclamation frontiers.
- **Current state:** 156 works = 113 CORE_SYS / 33 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** #36690 root-cause/fix/regression-CI → #36678 request-metrics implementation/consumer path → vLLM-Omni #6453/#5822/#6439/#6403 shipped-vs-open audit under v0.28.0rc1 → SGLang-Omni #1593 failure-path/soak-CI → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-28 04:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Independent Physical AI and Multimodal/Omni 24h→7d scans plus targeted 30d production-lineage/correctness checks completed.
- **Physical AI:** no new paper-level SYS promotion; fleet/control-loop/state/evaluation/world-model/runtime searches stayed within canonical anchors or below-threshold model/algorithm work.
- **Multimodal / Omni:** PinSieve/Pinterest reverse census found no second paper-backed selective-VLM serving/control-plane system at PinSieve's level this hour. Fresh SGLang issue **#36690** remains backend-qualification evidence for Gemma-3n multimodal serving degeneration/crash across selected attention backends; no root-cause fix/regression-CI closure is claimed yet.
- **Current state:** 156 works = 113 CORE_SYS / 33 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** SGLang #36690 root-cause/fix/regression-CI + #36678 request-metrics implementation → vLLM-Omni v0.28.0rc1 shipped-vs-open lifecycle audit (#6453/#5822/#6439/#6403) → SGLang-Omni #1593 remaining failure-path/soak-CI → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-28 03:00 CST

- **Promotions:** CORE_SYS +1 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. **PinSieve** (KDD 2026, arXiv:2608.24040) added to Routes 8/9/11.
- **Why SYS:** production selective VLM serving/control plane with grey-zone routing, human escalation, Feedback Memory provenance, evaluation gates, staged validation and rollback.
- **Production evidence:** review productivity +25.7%, normalized operating cost -16.2%, next-day→same-day signal delivery. Six-month FNR replay is offline governance evidence and kept separate from online claims.
- **Current state:** 156 works = 113 CORE_SYS / 33 SYS_ALG / 4 ALG / 6 WATCH. Public repo carries links/metadata only.
- **Next:** PinSieve/Pinterest reverse census → vLLM-Omni v0.28.0rc1 shipped-vs-open lifecycle audit → SGLang request metrics/correctness + SGLang-Omni failure-path/soak CI → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-28 01:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Independent Physical AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/release/lifecycle/heterogeneous checks completed.
- **Physical AI:** no new paper-level SYS promotion; fresh scans re-hit canonical fleet/control-loop/runtime anchors.
- **Multimodal / Omni release update:** first-party vLLM-Omni releases now verify **v0.28.0rc1** (released 2026-08-27, commit `651b032`, 212 merged changes). Major runtime changes include scheduler-managed diffusion paged KV, continuous/request-level batching, realtime AR-diffusion tick sessions, Host Weight Runtime + DLO, stronger full-duplex speech serving, **π0 VLA** and **SANA-WM** support, and broader accelerator portability. This is release/runtime evidence, not a paper promotion.
- **Evidence guard:** `v0.28.0rc1` is a pre-release; RC-listed capabilities are treated as RC-shipped, while open lifecycle/cancellation/reclamation RFCs/issues remain separately audited.
- **Current state:** 155 works = 112 CORE_SYS / 33 SYS_ALG / 4 ALG / 6 WATCH. Private PDF state: 148 valid; public repo keeps links only.
- **Next:** decompose v0.28.0rc1 shipped-vs-still-open runtime frontier → Lingjing + Deployment Is Not Destiny reverse census → SGLang #36678/#36690 follow-up → vLLM-Omni #6453/#5822/#6439/#6403 → SGLang-Omni #1593 failure-path/soak CI → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-28 00:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Independent Physical AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/lifecycle/observability/correctness checks completed.
- **Physical AI:** no new paper-level SYS promotion; fresh scans re-hit canonical ROSA/Kairos/Zetta and existing fleet/state/runtime anchors.
- **Multimodal / Omni:** no new paper promotion. SGLang #36678 remains OPEN as an opt-in per-request metrics feature request. A fresh first-party issue, **#36690**, reports Gemma-3n multimodal serving degenerating or crashing under selected attention backends with 0% vision accuracy; tracked as production correctness/qualification evidence, not a framework-wide claim or shipped fix.
- **Current state:** 155 works = 112 CORE_SYS / 33 SYS_ALG / 4 ALG / 6 WATCH. Private PDF state: 148 valid; public repo keeps links only.
- **Next:** Lingjing + Deployment Is Not Destiny reverse census → SGLang #36678 implementation/merge + #36690 root-cause/fix/regression-CI → vLLM-Omni #6453/#5822/#6439/#6403 → SGLang-Omni #1593 failure-path/soak CI → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-27 23:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Independent Physical AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/lifecycle/observability checks completed.
- **Physical AI:** no new paper-level SYS promotion. Fleet/control-loop, edge/device runtime, state reuse, world-model rollout and evaluation-infrastructure checks remained within current canonical anchors.
- **Multimodal / Omni:** fresh runtime evidence from SGLang core issue **#36678** (opened 2026-08-27): an opt-in coherent set of per-request latency/generation metrics is requested for OpenAI-compatible responses. This strengthens the observability→routing/scaling feedback line, but remains a feature request rather than a paper or shipped capability. vLLM-Omni #6453 remains open for request-scoped mutable stage-state lifecycle.
- **Current state:** 155 works = 112 CORE_SYS / 33 SYS_ALG / 4 ALG / 6 WATCH. Private PDF state: 148 valid; public repo keeps links only.
- **Next:** Lingjing + Deployment Is Not Destiny reverse census → SGLang #36678 implementation/merge and routing/scaling consumers → vLLM-Omni #6453/#5822/#6439/#6403 → SGLang-Omni #1593 failure-path/soak CI → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-27 22:03 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Independent Physical AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/lifecycle checks completed.
- **Physical AI:** no new paper-level SYS promotion. Fresh VLA/robot-policy serving, fleet/control-loop, edge/device runtime, state-reuse, evaluation-infrastructure and WAM/world-model queries re-hit canonical PhyAI/Embodied.cpp and existing fleet/state/runtime anchors.
- **Multimodal / Omni:** no new paper promotion. vLLM-Omni #6453 remains open for request-scoped mutable stage-state lifecycle; #6403 remains open for queued-vs-running status and true cancellation of already-running async-video inference; #6413 remains open for aborted diffusion orphan-output reclamation through #6439. SGLang-Omni v0.1.3 remains the latest first-party release found in this scan.
- **Current state:** 155 works = 112 CORE_SYS / 33 SYS_ALG / 4 ALG / 6 WATCH. Private PDF state: 148 valid; public repo keeps links only.
- **Next:** Lingjing + Deployment Is Not Destiny reverse census → vLLM-Omni #6453/#5822/#6439/#6403 → SGLang-Omni #1593 failure-path/soak CI → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-27 19:01 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Independent Physical AI and Multimodal/Omni 24h→7d scans plus targeted 30d fleet/control-loop/world-model/runtime checks completed.
- **Physical AI:** no new paper-level SYS promotion. Fresh hits re-resolved to canonical Kairos, Armory/action-chunk scheduling, Embodied.cpp/vla.cpp and existing state/runtime anchors; HorizonDrive and Hi-WM remain model/post-training centric rather than new serving/resource-management systems.
- **Multimodal / Omni:** no new paper promotion. M* and existing composite/Omni serving trunks remain canonical; request/session lifecycle, step-wise/preemptible execution, cancellation/reclamation and failure-path observability remain active production frontiers.
- **Current state:** 155 works = 112 CORE_SYS / 33 SYS_ALG / 4 ALG / 6 WATCH. Private PDF state: 148 valid; public repo keeps links only.
- **Next:** Lingjing + Deployment Is Not Destiny reverse census → vLLM-Omni #6453/#5822/#6439/#6403 → SGLang-Omni #1593 failure-path/soak CI → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-27 10:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Independent Physical AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime-adoption/FlashRT comparison checks completed.
- **Physical AI:** no new paper-level SYS promotion; fresh hits resolved to existing fleet/control-loop, edge/device, state-reuse, WAM-rollout and evaluation-infrastructure anchors or algorithm-only work.
- **Multimodal / Omni:** first-party SGLang-Omni docs now explicitly describe independent per-stage schedulers, a shared inbox/outbox abstraction and zero-copy shared-memory tensor transfer; first-party vLLM-Omni docs expose a WebSocket streaming-video session API for Qwen3-Omni that buffers video frames and optional audio chunks before queries. These strengthen stage orchestration and session-state coverage, but are runtime/adoption evidence rather than new papers.
- **Route impact:** Routes 3/5/11 streaming/session-state and Routes 6/11 multi-stage orchestration are strengthened; no top-level taxonomy split/merge this hour. FlashRT arXiv:2607.18171 remains the newest CORE_SYS promotion.
- **Current state:** 153 works = 110 CORE_SYS / 33 SYS_ALG / 4 ALG / 6 WATCH. Private PDF state: 146 valid; public repo keeps links only.
- **Next:** FlashRT IR/placement/streaming/state/heterogeneous-deployment comparison vs M*/vLLM-Omni/SGLang-Omni/Cornfigurator/HeyGen HELIOS → vLLM-Omni #6453/#5822/#6439/#6403 → SGLang-Omni #1593 failure instrumentation/soak CI → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-27 01:02 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +2 / ALG +0 / WATCH +0 — added **AgenticRobotics** (arXiv:2608.07555) and **DreamLedger** (arXiv:2608.23863), both `SYS_ALG_BOUNDARY / A`.
- **Physical AI:** AgenticRobotics adds a durable robot-policy improvement control plane with commit-keyed crash recovery, evidence-gated promotion, artifact-bound capability quality and recorded MCP tool calls. It remains boundary rather than CORE because its reference implementation is control/evaluation infrastructure, not an online serving scheduler.
- **World-model / WAM:** DreamLedger turns world-model reliability into persistent execution-settled credit state with dependency tickets and replayable logs. Credit gating cuts burned imagination by 62% and replays all 1,062 physical spends on the real-robot deployment logs; it is tracked across Routes 5/9/10 rather than promoted to CORE because the central contribution is trust/calibration/state, not multi-request resource scheduling.
- **Multimodal / Omni:** independent 24h→7d + targeted 30d scan completed. No new paper-level serving system surpassed the M*/HorizonServe/EPD trunk; request lifecycle, step-wise preemption, cancellation/reclamation and failure-path soak remain the active runtime frontier.
- **Artifacts:** both official arXiv PDFs were archived privately and validated (`%PDF-`, >10KB). No official implementation repo was independently verified for either paper in this run.
- **Current state:** 148 works = 108 CORE_SYS / 30 SYS_ALG / 4 ALG / 6 WATCH. Private PDF state: 141 valid; public repo contains links only.
- **Next:** AgenticRobotics related-work census (CaP-X/ASPIRE/RHO/EvoTrainer/ENPIRE) → DreamLedger authors/references and persistent WAM trust-state follow-ons → vLLM-Omni #6453/#5822/#6439/#6403 → SGLang-Omni #1593 soak/failure instrumentation → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-26 19:00 CST

- **Promotions:** CORE_SYS +1 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0 — added **Physical Agentic AI** (arXiv:2608.22657), `CORE_SYS / A`, Routes 1/2/7.
- **Physical AI:** new fleet/runtime-governance architecture separates a non-actuating LLM Mission Planner from a deterministic Robot Orchestrator with sole actuation authority. Typed skill libraries and workflow contracts are checked again against current state and state-bound values at dispatch time. Retrieval raises skill grounding 51%→96% but still leaves 23–29% faulted dispatches; per-dispatch enforcement reduces false dispatch to 0% with no false blocks and rejects all eight injected live-execution faults before motion.
- **Artifact:** no official code repo verified. Official arXiv PDF was archived privately and validated; this public radar keeps links only.
- **Multimodal / Omni:** independent 24h→7d + targeted 30d scan completed; no new paper-level promotion. vLLM-Omni request lifecycle/preemption/reclamation and SGLang-Omni failure-path tracing/soak remain active frontiers.
- **Taxonomy update:** Routes 1/2/7 now explicitly track **planner knowledge vs runtime execution authority** for robot crews; prompt grounding and deterministic dispatch enforcement are treated as separate control planes.
- **Current state:** 143 works = 105 CORE_SYS / 28 SYS_ALG / 4 ALG / 6 WATCH.
- **Next:** Physical Agentic AI author/reference reverse census and comparison with FSAR/AEROS/Thea/Zetta/RobotFleet/Armory → vLLM-Omni #6453/#5822/#6439/#6403 → SGLang-Omni #1593 failure events + soak CI/nightly → fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-26 18:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0. Independent Physical AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime checks completed.
- **Physical AI:** no new paper-level SYS promotion; fresh hits stayed within existing PhyAI/Kairos/Zetta-class runtime anchors and below-threshold model work.
- **Multimodal / Omni:** vLLM-Omni #6453 remains open with no implementation PR; #5822 remains open and is now tracked as a preemptible-execution frontier because per-timestep Modular Diffusers control would remove whole-generation head-of-line blocking and enable responsive cancellation/progressive output, while explicitly not adding cross-request GPU batching. #6403 remains open for queued-vs-running status and true GPU cancellation; #6413 remains open around aborted-output reclamation; SGLang-Omni #1593 remains open after #1595 merged.
- **Taxonomy update:** Routes 3/6/11 now explicitly connect step-wise execution with request lifecycle: admission/status → mutable stage state → step execution → cancellation/failure → artifact/state ownership → deterministic reclamation.
- **Current state:** 142 works = 104 CORE_SYS / 28 SYS_ALG / 4 ALG / 6 WATCH. Private PDF state remains 135 valid; public repo contains links only.
- **Next:** #6453 generic implementation/adopter → #5822 scheduler/preemption integration → #6439 reclamation → #6403 true cancellation/status → #1593 failure-event/soak CI → fresh 30d Multimodal SYS census; parallel Physical-AI edge/fleet/state/evaluation runtime coverage.

## Hourly scan — 2026-08-26 17:02 CST

- **Promotions:** CORE_SYS +1 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0 — added **Retriever** (arXiv:2607.17213), `CORE_SYS / A+`, Routes 2/3/5/7/9.
- **Physical AI:** independent 24h→7d scan plus targeted 30d omission recovery found a reusable temporal programming/runtime abstraction: stateful Flows, explicit Clocks, edge-level Sync policies, multi-backend execution and deterministic replay. The real robot pipeline composes VLM planning, belief memory, VLA skills, monitoring and high-rate control; public example uses 2 Hz VLA + 200 Hz controller.
- **Evidence guard:** 56 s / 36 s are progress-normalized **projected** task times, not measured completion times; replay determinism is trace/dataflow determinism under logged histories, not bitwise GPU determinism.
- **Artifact:** [OpenRetriever](https://github.com/openretriever/retriever) is Apache-2.0; current public crawl: 11 stars / 0 forks / 831 commits. PDFs remain private to the research workspace.
- **Multimodal / Omni:** independent fresh scan completed; no new paper-level promotion. Current request/session lifecycle, reclamation and failure-path observability frontiers remain active.
- **Current state:** 142 works = 104 CORE_SYS / 28 SYS_ALG / 4 ALG / 6 WATCH.
- **Next:** Retriever/OpenRetriever reverse census and temporal-runtime comparison with PonderPounce/AsyncVLA/Thea/Zetta → vLLM-Omni lifecycle/reclamation/cancellation → SGLang-Omni failure-path/soak CI → fresh 30d Multimodal SYS census.

## Hourly heartbeat — 2026-08-26 16:00 CST

- Completed independent Physical AI + Multimodal/Omni 24h/7d scans and targeted 30d PonderPounce/WoRV reverse census.
- Promotions: CORE_SYS +0; SYS_ALG_BOUNDARY +0; ALG/WATCH +0.
- PonderPounce remains SYS_ALG_BOUNDARY/A; Armory/action-chunk scheduling was rediscovered and confirmed already tracked.
- Next: PonderPounce freshness/runtime deep-read, Omni request lifecycle/reclamation, failure-path soak CI, and fresh 30d Multimodal SYS census.

## Hourly scan — 2026-08-26 15:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +1 / ALG +0 / WATCH +0 — added **PonderPounce** (arXiv:2608.24115), `SYS_ALG_BOUNDARY / A`.
- **Physical AI:** independent 24h→7d scan plus targeted 30d omission recovery found a dual-system control-runtime pattern: a slower episode-context MLLM asynchronously refreshes a cognition token, while a fast VLA consumes only the latest token plus its age/freshness signal. Reported serving p50 is 78 ms cognition refresh and 25 ms action invocation, supporting 20 Hz playback.
- **Multimodal / Omni:** no new paper-level CORE_SYS surfaced; canonical M*/HorizonServe and current vLLM/SGLang request-lifecycle/state/reclamation frontiers were rechecked. PonderPounce is cross-linked to composite MLLM+VLA serving and temporal state/freshness.
- **Artifact:** official WoRV repo verified at https://github.com/worv-ai/PonderPounce . Public crawl/API showed 0 stars / 0 forks at verification time; no license metadata was exposed.
- **Private PDF:** official arXiv PDF archived and validated at 1,135,426 B (`%PDF-`); PDFs are not published in this repo.
- **Current state:** 141 works = 103 CORE_SYS / 28 SYS_ALG / 4 ALG / 6 WATCH.
- **Next:** deep-read PonderPounce serving/hardware/freshness semantics + WoRV reverse census → vLLM-Omni #6453/#6439/#6403 lifecycle/reclamation/cancellation → SGLang-Omni #1593 failure-path/soak CI → #946/#1436 gates → fresh 30d Multimodal SYS census; parallel Physical-AI edge/fleet/state/evaluation coverage.

## Hourly scan — 2026-08-26 13:57 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0.
- **Physical AI:** independent 24h→7d fresh scan + targeted 30d checks completed across robot-policy/VLA serving, fleet/control-loop, edge/device runtime, state reuse, world-model rollout, evaluation infrastructure and heterogeneous deployment. Fresh hits re-hit canonical PhyAI/Kairos and existing anchors; no stronger new SYS-first paper was verified.
- **Multimodal / Omni:** no paper promotion, but first-party vLLM-Omni evidence now converges on a first-class request/session lifecycle abstraction: RFC #6453 owns request-scoped mutable stage state; the diffusion scheduler owns explicit request states; RFC #4480 separates persistent session memory from request-local world-model state; full-duplex runtime owns transactional session/response cleanup.
- **Taxonomy change:** Routes 3/5/11 now explicitly track admission → mutable stage/session state → cancellation/failure → artifact/state ownership → deterministic reclamation. Shared-stage RFC #4108 is cross-linked to Routes 6/11 because one physical stage serving multiple pipelines requires correct request identity, state isolation, cleanup and failure propagation.
- **Evidence guard:** #6453 remains open with no linked implementation PR. A fresh direct fetch for #6439 was unavailable, so the prior open/not-merged guard is retained instead of guessed forward.
- **Current state:** 140 works = 103 CORE_SYS / 27 SYS_ALG / 4 ALG / 6 WATCH. Private PDF state remains 133 valid; public repo contains links only.
- **Next:** #6453 core implementation/adopter → #4480 session-memory adoption + #4108 shared-stage semantics → #1593 failure-path/soak CI → first-party #6439 status → #6403 true cancellation/status → #6466/#946/#1436 gates → fresh 30d Multimodal SYS census; parallel Physical-AI edge/fleet/state/evaluation runtime coverage.

## Hourly scan — 2026-08-26 13:01 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0.
- **Physical AI:** independent 24h→7d fresh scan + targeted 30d checks completed across VLA/robot-policy serving, fleet/control-loop, edge/device runtime, state reuse, world-model rollout, evaluation infrastructure and heterogeneous deployment; no new paper crossed the SYS-first threshold.
- **Multimodal / Omni:** independent fresh scan re-hit canonical HorizonServe/M*/Cornserve. `Aero Realtime` (2608.08469) and `ParaJSCC` (2608.15066) were reviewed but not promoted: current evidence remains model/inference-architecture or communication-method centric rather than serving scheduling/resource runtime.
- **Request-lifecycle abstraction:** vLLM-Omni RFC #6453 is OPEN and proposes runtime-owned, request-scoped lifecycle management for mutable incremental TTS/Omni stage state. It covers explicit internal/external request identity, namespaced state, terminal-send commit ordering, cancellation/timeout/failure cleanup, segment continuation, ID reuse and stale-work fencing. At least ten current-main processors directly manage this state today; no generic implementation PR or performance claim exists yet.
- **Status checks:** SGLang-Omni #1593 remains open after #1595 merged; slot-pool failure events and comm-layer-triggered soak/CI-nightly remain unevidenced as landed. vLLM-Omni #6403 and #6466 remain open with no linked implementation PRs.
- **Current state:** 140 works = 103 CORE_SYS / 27 SYS_ALG / 4 ALG / 6 WATCH. Private PDF state remains 133 valid; public repo contains links only.
- **Next:** #6453 core implementation/adopter → #1593 failure-path/soak CI → first-party #6439 reclamation → #6403 true cancellation/status → #6466 Gaudi/PersonaPlex qualification → #946/#1436 production gates → fresh 30d Multimodal SYS census; parallel Physical-AI edge/fleet/state/evaluation runtime coverage.

## Hourly scan — 2026-08-26 11:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0.
- **Physical AI:** independent 24h→7d fresh scan + targeted 30d runtime checks completed across VLA/robot-policy serving, fleet/control-loop, edge/device runtime, state reuse, world-model rollout, evaluation infrastructure and heterogeneous deployment; no new paper crossed the SYS-first threshold.
- **Multimodal / Omni:** independent 24h→7d fresh scan + targeted 30d serving/runtime checks completed. No new paper-level serving system surfaced beyond canonical M*/HorizonServe/EPD-family work.
- **Failure-path / lifecycle:** SGLang-Omni #1593 remains open after #1595 merged; the remaining slot-pool failure events and comm-layer-triggered soak/CI-nightly policy are not yet evidenced as landed. vLLM-Omni #6403 remains open with queued-vs-running status ambiguity and ineffective cancellation for already-running async-video GPU inference.
- **Boundary guard:** speculative VLA acceleration, world-model planning/model papers and multimodal speculative-decoding surveys remain outside CORE_SYS unless they contribute serving/runtime/resource-management infrastructure.
- **Current state:** 140 works = 103 CORE_SYS / 27 SYS_ALG / 4 ALG / 6 WATCH. Private PDF state remains 133 valid; public repo contains links only.
- **Next:** #1593 failure-instrumentation/soak CI → first-party #6439 reclamation → #6403 true cancellation/status → #6466 Gaudi/PersonaPlex qualification → #946/#1436 production gates → next 30d Multimodal SYS census; parallel Physical-AI edge/fleet/state/evaluation runtime coverage.

## Hourly scan — 2026-08-26 10:00 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0.
- **Physical AI:** independent 24h→7d fresh scan completed across VLA/robot-policy serving, fleet/control-loop, edge/device runtime, state reuse, world-model rollout, evaluation infrastructure and heterogeneous deployment; no new paper crossed the SYS-first threshold.
- **Multimodal / Omni:** independent 24h→7d fresh scan + targeted 30d runtime/release checks completed. No new paper promotion, but **SGLang-Omni v0.1.3** is now verified as the latest official release (2026-08-20, `91d4359`). It ships production-facing changes including bounded Qwen3-TTS admission/fast rejection, deterministic TTS, weight-share IPC fixes, persistent TTS WebSocket input segments, breakable prefill CUDA Graph expansion, encoder batching/dedup, pinned-host encoder caching, Whisper request/cache sizing, and Code2Wav/vocoder overlap.
- **Heterogeneous full-duplex watch:** vLLM-Omni #6466 is open for PersonaPlex on Intel Gaudi2/HPU, targeting ≥4 simultaneous sessions, the model's 80 ms cadence, per-session state isolation and an eight-hour HBM/stability soak. No implementation PR is linked yet, so this is a qualification frontier rather than shipped support.
- **Current state:** 140 works = 103 CORE_SYS / 27 SYS_ALG / 4 ALG / 6 WATCH. Private PDF state remains 133 valid; public repo contains links only.
- **Next:** inspect v0.1.3 release-linked admission/streaming/weight-sharing changes + #1593 remaining soak/failure-path CI gaps → vLLM-Omni #6439 reclamation → #6403 cancellation/status → #6466 Gaudi/PersonaPlex qualification → next 30d Multimodal SYS census; parallel Physical-AI edge/fleet/state/evaluation runtime coverage.

## Hourly scan — 2026-08-26 08:01 CST

- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / ALG +0 / WATCH +0.
- **Physical AI:** independent 24h→7d fresh scan completed across VLA/robot-policy serving, fleet/control-loop runtime, edge/device runtime, state reuse, world-model rollout, evaluation infrastructure and heterogeneous deployment; no new paper crossed the SYS-first threshold.
- **Multimodal / Omni:** independent 24h→7d fresh scan + targeted 30d runtime checks completed. Fresh arXiv results did not surface a new in-scope systems paper beyond canonical HorizonServe or unrelated/algorithmic work.
- **Failure-path observability:** SGLang-Omni #1593 remains open after #1595 merged. The remaining frontier is the four slot-pool failure-path events plus comm-layer-triggered soak/CI-nightly policy.
- **Request lifecycle:** vLLM-Omni #6403 remains open with no linked development branch/PR, so queued-vs-running status and true GPU cancellation remain unresolved. #6439 could not be freshly fetched in this scan; its status is therefore not upgraded beyond the last verified open/not-merged guard.
- **Current state:** 140 works = 103 CORE_SYS / 27 SYS_ALG / 4 ALG / 6 WATCH. Private PDF state remains 133 valid; public repo contains links only.
- **Next:** #1593 failure-event/soak integration → first-party #6439 reclamation status → #6403 cancellation/status → #946/#1436 production gates → vLLM-Omni hardening → fresh 30d Multimodal SYS; parallel Physical-AI edge/fleet/state/evaluation runtime coverage.

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

## 2026-08-26 20:00 CST — hourly scan
- **CORE_SYS +1:** [IcFuzz](https://arxiv.org/abs/2608.06088) (ASE 2026), Route 9 / A — reliability-testing infrastructure for Isaac Sim with semantic-stage-guided fuzzing, hierarchical mutations and adaptive mutation scheduling. It reports 11 bugs over ~4 months, 9 confirmed or fixed. [Replication package](https://doi.org/10.5281/zenodo.19244624).
- **Multimodal / Omni:** independent 24h/7d + targeted 30d runtime scan completed; no paper promotion. Lifecycle/preemption/reclamation and failure-path observability remain active.

## 2026-08-26 21:00 CST — hourly scan
- **CORE_SYS +1:** [PHYFU](https://arxiv.org/abs/2307.10818) (**ASE 2023 Distinguished Paper**), Route 9 / A — foundational physics-simulation-engine reliability infrastructure recovered by reverse-census from IcFuzz. It combines physics-law oracles, forward/backward simulation checking, valid-state mutation and feedback-guided fuzzing; reports >5,000 error-triggering inputs across four engines. [Repo](https://github.com/PhyFuzz/phyfu).
- **Route 9 lineage:** PHYFU → IcFuzz now forms the explicit simulator-reliability branch; RoboFuzz remains older ROS2 reliability background under review rather than automatic promotion.
- **Multimodal / Omni:** independent 24h/7d + targeted 30d scan completed; no paper promotion. vLLM-Omni request lifecycle/preemption/reclamation and SGLang-Omni failure-path tracing/soak CI remain the active production-runtime frontier.

## 2026-08-26 22:00 CST — hourly scan
- **CORE_SYS +1:** [RoboFuzz](https://2022.esec-fse.org/details/fse-2022-research-papers/86/RoboFuzz-Fuzzing-Robotic-Systems-over-Robot-Operating-System-ROS-for-Finding-Corre) (ESEC/FSE 2022), Route 9 / A — foundational ROS2/robot-stack semantic-correctness fuzzing infrastructure recovered through the IcFuzz → PHYFU reverse census. Reports **30 unknown bugs, 25 acknowledged, 6 fixed** across ROS2 internals and Turtlesim / MoveIt2+PANDA / TurtleBot3 / PX4. [Repo](https://github.com/sslab-gatech/robofuzz).
- **Route 9 lineage:** RoboFuzz → PHYFU → IcFuzz now covers robot middleware/system correctness, physics-engine consistency and Isaac-Sim-specific reliability.
- **Multimodal / Omni:** independent 24h/7d + targeted 30d scan completed; no paper promotion. Request-scoped state lifecycle, step-wise/preemptible execution, true cancellation/reclamation and failure-path soak/observability remain active runtime frontiers.

## 2026-08-27 02:02 CST — hourly scan
- **CORE_SYS +1:** [CaP-X](https://arxiv.org/abs/2603.22435), Route 9 / A — open robot coding-agent evaluation/execution substrate with parallel workers, perception serving/GPU allocation, regression harnesses and real-robot bringup. [Repo](https://github.com/capgym/cap-x), 758 stars / 116 forks on this scan.
- **SYS_ALG_BOUNDARY +2:** [ASPIRE](https://arxiv.org/abs/2607.00272) and [RHO](https://arxiv.org/abs/2606.16458) — strong closed-loop execution/tracing and harness-search evidence, but primary novelty remains skill/harness optimization rather than online serving.
- **Multimodal / Omni:** independent 24h→7d + targeted 30d runtime scan completed; no new paper-level promotion. Request lifecycle/preemption/reclamation and failure-path observability remain active.
- **Next:** EvoTrainer → ENPIRE strict audit; CaP-X/ASPIRE same-group follow-ons; parallel vLLM-Omni #6453/#5822/#6439/#6403 and SGLang-Omni #1593; then fresh 30d Multimodal SYS census.

## 2026-08-27 05:01 CST — hourly scan
- **SYS_ALG_BOUNDARY +1:** [ENPIRE](https://arxiv.org/abs/2606.19980), Routes 1/2/9, A+ — NVIDIA GEAR physical autoresearch harness with automatic reset/verification, auditable rollout artifacts, parallel single/multi-robot trials, and MRU/MTU fleet-utilization metrics. [Project](https://research.nvidia.com/labs/gear/enpire/).
- **Multimodal / Omni:** independent 24h→7d + targeted 30d scan completed; no new paper-level promotion. Request-scoped state lifecycle, step-wise preemption, true cancellation/reclamation and SGLang-Omni failure-path tracing/soak remain active runtime frontiers.
- **Next:** ENPIRE same-group/follow-on fleet experiment orchestration; then vLLM-Omni #6453/#5822/#6439/#6403, SGLang-Omni #1593, fresh 30d Multimodal SYS census.

## 2026-08-27 06:01 CST — hourly scan
- **Paper promotions: 0.** Independent Physical-AI and Multimodal/Omni 24h→7d scans plus targeted 30d ENPIRE/GEAR/runtime checks completed.
- **Physical-AI runtime adoption:** first-party `NVlabs/GR00T-WholeBodyControl` evidence confirms GEAR-SONIC's C++ deployment stack evolved with motor-error monitoring, TTS alerts, ZMQ protocol v4 and idle-mode readaptation, followed by an end-to-end G1 VLA workflow. Track as Route 2/3/6 ecosystem evidence; no separate systems-paper promotion.
- **Multimodal / Omni:** no new paper cleared the SYS-first bar; HorizonServe/Cornserve/M* re-hits were canonical. Request-scoped lifecycle → step-wise preemption → true cancellation → state/artifact reclamation and SGLang-Omni failure-path/soak remain the active production-runtime frontier.
- **Next:** continue ENPIRE/GEAR same-group/reference census for paper-backed fleet experiment scheduling/utilization/runtime → vLLM-Omni lifecycle/preemption/reclamation/cancellation → SGLang-Omni failure instrumentation/soak CI → fresh 30d Multimodal SYS census.

## 2026-08-27 09:00 CST
- **CORE_SYS +1:** FlashRT — *Agent Harness for Guiding Agents to Deploy Real-Time Multimodal Applications* (arXiv:2607.18171), A+, Routes 2/3/6/7/10/11. Official repo verified; system reports up to 70× lower latency and 3.6× throughput improvement.
- Coverage: independent Physical AI + Multimodal/Omni 24h→7d fresh scan plus targeted 30d runtime/omission recovery completed; no other promotion this cycle.
## 2026-08-27 13:00 CST
- **CORE_SYS +2:** [Lingjing](https://arxiv.org/abs/2608.08045) (A+, Routes 1/2/9) — synchronized multi-engine heterogeneous-agent city-scale runtime, shared state, communication/resource constraints and attribution-ready replay. [Official repo](https://github.com/seanlxh/Air-Lingjing).
- **CORE_SYS +1:** [Deployment Is Not Destiny](https://arxiv.org/abs/2608.11063) (A, Routes 1/2/4/6/7) — runtime recomposition for unseen software/hardware/compute payloads with peer-visible capability sharing and remote compute use.
- **Multimodal/Omni:** independent fresh scan completed; no additional paper-level promotion. vLLM-Omni first-party releases still show v0.27.0rc1 as latest directly verified 0.27-series release.
- **Coverage:** 24h → 7d, plus targeted 30d runtime-recomposition/digital-twin and Omni runtime checks.



## 2026-08-28 10:02 CST
- **CORE_SYS +1 — StreamArena / StreamMind (arXiv:2608.05703, A)**: always-on streaming multimodal runtime/evaluation substrate with frontend/backend worker decoupling and persistent-state reuse; 243 videos, 3,646 tasks, 66.2% weighted query-latency reduction.
- Physical-AI fresh scan: no additional SYS-first promotion. Multimodal runtime frontier continues SGLang correctness/request-metrics and vLLM-Omni lifecycle/preemption/cancellation/reclamation.

### 2026-08-28 11:00 CST
- **SYS_ALG_BOUNDARY +1:** [Joint Age-of-Latent and Resource Minimization for Wireless Multi-Camera Perception With Temporal Window Selection](https://arxiv.org/abs/2608.09411) — **A**, Routes P4/P5/P8.
- System role: task-relevant latent freshness (AoL) jointly couples temporal integration-window selection with encoder choice, camera scheduling and NOMA power control under reliability constraints for wireless multi-camera Physical-AI perception.
- Boundary guard: numerical/simulation resource-control study, not a reusable deployed serving runtime; no official implementation repo verified.
- 24h/7d dual-track scan found no additional CORE_SYS promotion. Public dataset now contains **158 verified works**.

### 2026-08-28 15:00 CST
- **Hourly scan complete — no promotion this cycle.** Physical-AI coverage checked fleet/multi-robot, unified runtime, control-loop/streaming, edge/device, temporal/shared state, heterogeneous serving, composite VLA+WAM+planner, workload/evaluation and world-model rollout surfaces; fresh results re-hit canonical Kairos/PhyAI/PhyAgentOS/MagicSim or below-threshold work.
- Multimodal/Omni coverage checked any-to-any/composite serving, stage/modality disaggregation, streaming state and runtime surfaces; fresh results re-hit Cornserve/Cornfigurator, HorizonServe and vLLM-Omni anchors rather than a new paper-level system.
- First-party runtime heartbeat: SGLang #36690 and #36678 remain open on 2026-08-28; no verified Gemma-3n root-cause fix/regression-CI closure or shipped response-level request-metrics implementation was found this cycle.
- Canonical public set remains **158 verified works**; taxonomy unchanged.

### 2026-08-28 17:00 CST
- **Hourly scan complete — no paper promotion this cycle.** Independent Physical-AI and Multimodal/Omni 24h→7d scans plus targeted 30d runtime/streaming/edge-freshness/lifecycle/correctness checks completed.
- Physical-AI fresh hits re-confirmed canonical Kairos, Embodied.cpp, Zetta and existing fleet/runtime/evaluation anchors; no new reusable serving/resource-management substrate crossed the SYS-first bar.
- Multimodal/Omni fresh hits re-confirmed HorizonServe and existing any-to-any/streaming/runtime anchors. SGLang #36690 and #36678 remain open; no verified Gemma-3n fix/regression-CI or shipped per-request metrics implementation was found.
- Public canonical set remains **158 verified works**; taxonomy and paper counts unchanged.
- Next: AoL/TWI runtime-successor census → StreamMind full-agent release → SGLang #36690/#36678 → vLLM-Omni lifecycle/cancellation/reclamation audit → SGLang-Omni #1593 soak/CI closure.

### 2026-08-28 18:00 CST
- **Hourly scan complete — no paper promotion this cycle.** Physical-AI and Multimodal/Omni each received independent 24h→7d fresh scans plus targeted 30d runtime/streaming/edge-freshness/lifecycle/correctness checks.
- Fresh paper results re-confirmed existing PhyAI/Embodied.cpp/HorizonServe/StreamArena anchors; no new reusable serving/runtime/resource-management system crossed the SYS-first bar.
- Runtime frontier: vLLM-Omni #6403 remains open for queued-vs-running status and true cancellation semantics; SGLang-Omni #1593 remains open, with its issue text still leaving four slot-pool failure events and comm-layer-triggered soak/nightly policy outstanding after #1595 covered the paged-KV/transport/direct-IPC trace gaps.
- Public canonical set remains **158 verified works**; taxonomy and paper counts unchanged.
- Next: AoL/TWI runtime-successor census → StreamMind full-agent release → SGLang #36690/#36678 → vLLM-Omni #6453/#5822/#6439/#6403 → SGLang-Omni #1593 failure-instrumentation/soak-CI closure.
### 2026-08-28 23:00 CST
- **Hourly scan complete — no paper promotion this cycle.** Physical-AI and Multimodal/Omni 24h→7d fresh scans plus targeted 30d runtime/streaming/session-lifecycle/correctness checks completed.
- Runtime watch: SGLang #36475 remains open for streaming-session disconnect/session-state corruption; vLLM-Omni #6403 remains open for queued-vs-running status and true cancellation semantics; SGLang-Omni #1593 remains open for failure-path observability and soak/CI closure.
- World-model/full-duplex RFC activity in vLLM-Omni continues to strengthen WAM-rollout and long-lived-session serving as active runtime directions, but no RFC was promoted as a paper.
- Public canonical set remains **158 verified works**; taxonomy and paper counts unchanged.



### 2026-08-28 23:58 CST
- **CORE_SYS +1:** [TypeGo: An OS Runtime for Embodied Agents](https://arxiv.org/abs/2607.05482) — A+, Routes P2/P3/P7; historical omission recovery.
- TypeGo adds an OS-style runtime abstraction for concurrent physical tasks: process/PCB lifecycle, Skill Kernel resource arbitration, preemption/resumption and asynchronous multi-timescale planning. Unitree Go2 prototype reports 50% lower per-step delay and 73% lower TTFA against the paper baselines.
- No official implementation repo was verified this cycle. Fresh dual-track 24h→7d + targeted 30d scanning found no additional paper-level promotion. Public canonical set is now **159 verified works**.

## 2026-08-29 11:00 CST
- No new paper-level promotion after full Physical-AI + Multimodal/Omni fresh scan.
- Runtime substrate watch: SGLang #36877 exposes a client-disconnect abort race that can leave zombie requests during a batch-transition window.
- Cache/state correctness watch: vLLM #54193 reports decode-side KV offloading may persist an unwritten final-token slot and silently poison later requests when decode offload is enabled.
- These are generic serving-substrate signals, not additions to CORE_SYS/SYS_ALG paper counts.


## 2026-08-31 11:18 CST — watchdog catch-up recovery
- **Incident recovered:** the dedicated Physical-AI radar had been stale since 2026-08-29 13:00 CST. The primary tracker is enabled again and a real catch-up scan was completed.
- Coverage completed: Physical-AI + Multimodal/Omni SYS-first 24h -> 7d fresh scan plus targeted 30d lifecycle/cache/runtime checks. No new paper crossed the canonical promotion bar.
- Revalidated runtime frontiers: vLLM #54193/#54288 (KV-offload correctness), SGLang #36333/#36418 and #36475 (disconnect/session lifecycle), SGLang-Omni #1723/#1724 (radix-cache eviction), and vLLM-Omni #6403/#6413/#6439/#6453 (cancellation/reclamation/request-scoped state). Issue/PR progress is not treated as shipped without merge/release evidence.
- Public dataset remains **161 verified works**; taxonomy unchanged.
- Internal archive recovered two previously pending official PDFs (TimelyLLM and TypeFly); PDFs are intentionally not stored in this public repository.


### 2026-08-31 14:02 CST heartbeat
Real SYS-first 24h→7d plus targeted 30d runtime scan completed. No new canonical paper promotion this cycle. vLLM-Omni #6672 remains the active interactive world-model serving roadmap; vLLM #54193 and SGLang #36333/#36475 remain open lifecycle/correctness frontiers.

### 2026-08-31 15:11 CST heartbeat
Real SYS-first 24h→7d scan plus targeted multimodal/cache correctness follow-up completed. No new canonical paper promotion. Fresh runtime WATCH signals: SGLang #37187 (Qwen3.5 visual-encoder PP weight-filtering correctness) and #37183 (LMCache per-request cache-salt tenant-isolation correctness). #36690 remains an open multimodal shared-KV qualification signal. Public canonical set remains 161 works; taxonomy unchanged.


## Hourly scan — 2026-08-31 20:01 CST
- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / paper WATCH +0. Real Physical-AI + Multimodal/Omni 24h→7d SYS-first scans plus targeted heterogeneous/diffusion/runtime follow-up completed; 0 promotion is not 0 search.
- **Runtime frontier:** vLLM-Omni #6665/#6672 remained open roadmap evidence with no new landing/release evidence. SGLang #36938/#36943 were retained only as generic serving-substrate correctness evidence.
- **Canonical state:** 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; taxonomy unchanged. Internal PDF archive remained 154 valid / 4 pending; PDFs are not stored in this public repository.

## Hourly scan — 2026-08-31 22:36 CST
- **Watchdog catch-up:** canonical progress had stalled after 20:01 despite healthy triggers, so a real SYS-first 24h→7d catch-up plus targeted heterogeneous/runtime follow-up was executed.
- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / paper WATCH +0. Fresh SGLang #37215 was classified as generic distributed-initialization evidence rather than a Physical-AI/Multimodal paper promotion.
- **Canonical state:** remains 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; taxonomy unchanged; internal PDF archive remains 154 valid / 4 pending.

## Hourly scan — 2026-09-01 16:58 CST
- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / paper WATCH +0. Real 24h→7d Physical-AI + Multimodal/Omni SYS-first scan completed; fresh September arXiv surface checked.
- **Dedup/boundary:** Persistent Computational State (arXiv:2607.21686) was re-hit and confirmed already canonical CORE_SYS; Riemann-1.0 and τ0-VLA remain model/algorithm works rather than reusable serving substrates.
- **Canonical state:** 161 works = 116 CORE_SYS / 35 SYS_ALG / 4 ALG / 6 WATCH; taxonomy unchanged; internal PDF archive remains 154 valid / 4 pending.
- **Frontier:** vLLM-Omni release/session-state landing → SGLang lifecycle/correctness closure → fresh 30d SYS census.

## Hourly scan — 2026-09-01 20:27 CST
- **Watchdog catch-up:** hourly trigger remained healthy, but canonical research progress had stalled after 16:58 CST; a real SYS-first 24h→7d catch-up was completed.
- **Promotions:** CORE_SYS +0 / SYS_ALG_BOUNDARY +0 / WATCH +0. Fresh checks covered Physical-AI serving/runtime, arXiv fresh surfaces, vLLM-Omni runtime/release surfaces, and SGLang router/streaming/runtime surfaces.
- **Boundary:** fresh hits were existing runtime-roadmap signals or model/algorithm work below the SYS-first promotion bar. Canonical set remains **161 works**; taxonomy unchanged.
- **Next:** vLLM-Omni release/session-state landing → SGLang lifecycle/correctness + composite routing → fresh 30d SYS census.
