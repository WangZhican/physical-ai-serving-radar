# Multimodal / Omni Efficient Serving

> Dedicated systems track for MLLM, Omni, any-to-any, multimodal generation, and heterogeneous composite-model serving.

This track is **not an appendix to Physical AI**. It is maintained as an independent research line in the same repository because many runtime, scheduling, disaggregation, state-management, and resource-allocation ideas later transfer into Physical AI.

## Scope

The track focuses on:

- encode / prefill / decode and general multi-stage disaggregation;
- modality-specific module multiplexing and spatial GPU sharing;
- any-to-any and composite-model graph serving;
- distributed KV / state / workflow orchestration;
- real-time speech/audio/video/omni interaction;
- cross-tier heterogeneous GPU placement and elastic parallelism;
- preprocessing, codec, RDMA and video/AIGC data paths;
- SLO-aware deployment planning and production-scale resource management.

## Research routes

| Route | Topic | Representative systems |
|---|---|---|
| M1 | Stage / EPD Disaggregation | TriInfer, EPD-Serve, HydraInfer, ModServe, RServe/REDServe |
| M2 | Module Multiplexing / GPU Sharing | Eevee, SpaceServe, HorizonServe, FlashCodec + UnifiedServe |
| M3 | Any-to-Any / Graph Serving | vLLM-Omni, Cornserve, M*, Cornfigurator |
| M4 | Distributed State / KV / Workflow | Omni-Flow, Cornserve, OnePiece |
| M5 | Interactive / Streaming Omni Serving | LiveServe, StreamWise, TCM-Serve, HorizonServe |
| M6 | Heterogeneous / Elastic Placement | HeteroServe, ElasticMM, TriInfer, HELIOS |
| M7 | Preprocessing / Video / AIGC Data Path | FlashCodec + UnifiedServe, OnePiece, HELIOS |
| M8 | Deployment Planning / SLO / Production Infra | Cornfigurator, HorizonServe, HELIOS |

See the full map: [`../taxonomy/MULTIMODAL_MAP.md`](../taxonomy/MULTIMODAL_MAP.md).

## Recommended first reading

1. **vLLM-Omni** — fully disaggregated stage graph for any-to-any multimodal models.
2. **M*** — modular composite-model graph / walk abstraction.
3. **Eevee** — module multiplexing inside a GPU.
4. **TriInfer** — hybrid stage disaggregation and stage-aware scheduling.
5. **Cornserve + Cornfigurator** — generic any-to-any runtime plus deployment planning.
6. **Omni-Flow** — distributed workflow + KV/state sharing.
7. **LiveServe** — interaction-aware real-time omni serving.
8. **HeteroServe** — cross-tier GPU heterogeneity.
9. **ElasticMM** — elastic multimodal parallelism.
10. **SpaceServe / ModServe** — spatial multiplexing and modality/stage-aware disaggregation precursors.

Full list: [`CORE_READING.md`](CORE_READING.md).

## What is excluded from the core

A model paper is not promoted merely because it is multimodal or efficient. The core requires a real systems contribution in runtime architecture, resource management, scheduling, communication/state movement, placement, serving SLOs, or production infrastructure.

## Connection to Physical AI

Multimodal serving provides reusable mechanisms; Physical AI adds physical execution semantics. For example:

- EPD / stage disaggregation → VLM / action-expert / WAM stage placement;
- graph serving → VLA + planner + WAM + safety composition;
- distributed KV/state → physical-state and rollout-state infrastructure;
- interactive scheduling → action deadlines and state freshness;
- heterogeneous placement → robot / edge / cloud co-execution.

See [`../taxonomy/CROSSOVER.md`](../taxonomy/CROSSOVER.md).
