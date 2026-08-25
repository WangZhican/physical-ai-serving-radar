# Multimodal / Omni Efficient Serving — Research Map

This is the independent systems taxonomy for MLLM / Omni / any-to-any multimodal serving. It is maintained separately from the Physical AI map even when a system is relevant to both.

## M1. Stage / EPD Disaggregation
Split encode, prefill, decode, preprocessing, or other stages so each can be independently batched, scaled, placed, and scheduled. **Anchors:** TriInfer, EPD-Serve, HydraInfer, ModServe, RServe/REDServe.

Key questions:
- which stages should be logically vs physically disaggregated;
- how to overlap encoding/prefill/decode;
- stage-specific batching and load balancing;
- transfer overhead versus resource specialization;
- dynamic resource reallocation across stages.

## M2. Module / Replica Multiplexing / GPU Sharing
Exploit complementary compute/memory behavior between modality modules, serving stages, or complete replicas on the same GPU. **Anchors:** Eevee, SpaceServe, HorizonServe, FlashCodec + UnifiedServe; ecosystem evidence: SGLang-Omni same-GPU MPS-DP.

Key questions:
- SM/spatial partitioning and managed CUDA-MPS colocation;
- safe concurrent kernels and cross-replica correctness;
- module-level independent batching versus multi-replica admission;
- read-only shared weights versus replica-private streaming/codec state;
- per-replica KV-budget sizing and memory fragmentation;
- NUMA/CPU-dispatch placement when the GPU is under-fed by one serving replica;
- coordinating scheduling with GPU sharing rather than assuming one stage or one replica per GPU.

## M3. Any-to-Any / Graph Serving
Represent arbitrary multimodal models as component graphs rather than a fixed LLM pipeline. **Anchors:** vLLM-Omni, Cornserve, M*, Cornfigurator.

Key questions:
- generic stage/component abstractions;
- dynamic walks/branches/loops;
- independent component scaling;
- graph-aware placement and scheduling;
- model-fission versus monolithic execution.

## M4. Distributed State / KV / Workflow
Treat intermediate tensors, KV, multimodal state, and workflow control as first-class distributed serving objects. **Anchors:** Omni-Flow, Cornserve, OnePiece.

Key questions:
- cross-role and cross-stage KV reuse;
- GPU/CPU/SSD state hierarchy;
- tensor/state transfer;
- workflow orchestration and replay;
- consistency and lifetime management for shared state.

## M5. Interactive / Streaming Omni Serving
Optimize for real-time speech/audio/video/omni interaction rather than only request throughput. **Anchors:** LiveServe, StreamWise, TCM-Serve, HorizonServe.

Key questions:
- playback/speech/barge-in-aware scheduling;
- modality-aware head-of-line blocking;
- latency, smoothness, TTFT and SLO interactions;
- streaming generation pipelines;
- buffer-risk and deadline-aware prioritization.

## M6. Heterogeneous / Elastic Placement
Use different GPU tiers, devices, or elastic parallelism because stages/modalities have different resource profiles. **Anchors:** HeteroServe, ElasticMM, TriInfer, HELIOS.

Key questions:
- compute-bound versus memory-bound stage mapping;
- cross-tier GPU assignment;
- elastic multimodal parallelism;
- QoS-aware global/cell scheduling;
- cost, energy and throughput tradeoffs.

## M7. Preprocessing / Video / AIGC Data Path
Move preprocessing, codec/decode, data movement, RDMA, and video-generation workflow costs into the serving-system design rather than treating them as free. **Anchors:** FlashCodec + UnifiedServe, OnePiece, HELIOS.

Key questions:
- NVDEC/GPU collaborative decode;
- preprocessing as a first-class stage;
- RDMA-based inter-service transfer;
- asynchronous buffering;
- large-scale video/AIGC DAG execution.

## M8. Deployment Planning / SLO / Production Infrastructure
Automatically choose placement and scheduling plans that maximize SLO-qualified goodput or production efficiency. **Anchors:** Cornfigurator, HorizonServe, HELIOS.

Key questions:
- deployment-plan search;
- SLO-qualified goodput;
- production cluster/cell placement;
- elastic scale-out/scale-in;
- scheduling under heterogeneous request mixes.

## Why this track is separate

These systems solve general multimodal-serving problems even when they later benefit robots. Physical AI introduces extra semantics—physical execution progress, state freshness, action deadlines, robot resources and world-model rollouts—that deserve a different taxonomy.

See [`PHYSICAL_AI_MAP.md`](PHYSICAL_AI_MAP.md) and [`CROSSOVER.md`](CROSSOVER.md).
