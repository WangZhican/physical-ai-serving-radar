# Multimodal / Omni Efficient Serving — Core Reading

This list is ordered by **systems importance and route coverage**.

| Priority | Work | Main systems role | Paper / project |
|---|---|---|---|
| S | vLLM-Omni Technical Report (2026) | Unified multi-stage omni orchestration, replica pools, session/duplex/robot loops; [open-source runtime](https://github.com/vllm-project/vllm-omni), 34p official report, no robot-fleet p99 | https://arxiv.org/abs/2610.09307 |
| A | HeteroVDiff | Galaxy S25 NPU/GPU shared-weight video diffusion pipeline, 1.35× stream throughput, SLO-qualified 5.3 vs 3.9 clips/h | https://arxiv.org/abs/2610.16244 |
| S+ | M*: A Modular, Extensible, Serving System for Multimodal Models | composite model graph / walk abstraction | https://arxiv.org/abs/2606.12688 |
| S | vLLM-Omni | fully disaggregated any-to-any multimodal serving | https://arxiv.org/abs/2602.02204 |
| S | Eevee | module multiplexing for multimodal serving | https://doi.org/10.1145/3767295.3769389 |
| S | TriInfer | hybrid disaggregated scheduling for MLLM serving | MLSys 2026 |
| S | Cornserve | distributed any-to-any multimodal serving | https://arxiv.org/abs/2603.12118 |
| S | Omni-Flow | workflow orchestration + distributed KV/state sharing | https://arxiv.org/abs/2606.31093 |
| A+ | GENSERVE | heterogeneous T2I/T2V diffusion co-serving on 8×RTX PRO 6000 Blackwell; step preemption + elastic SP + SLO scheduler; up to 44% relative SLO attainment gain, code unverified | https://arxiv.org/abs/2604.04335 |
| A+ | xDiT | hybrid SP/PipeFusion/CFG DiT inference across real multi-node GPUs; [Apache-2.0 code](https://github.com/xdit-project/xDiT) | https://arxiv.org/abs/2411.01738 |
| A | DDiT | T2V multi-stage DiT/VAE resource allocation and step scheduling; up to 1.44x p99 latency, simulated multi-server scaling | https://arxiv.org/abs/2506.13497 |
| A+ | LiveServe | interaction-aware real-time omni serving | https://arxiv.org/abs/2606.22983 |
| A+ | HeteroServe | cross-tier heterogeneous GPU serving | https://arxiv.org/abs/2603.12707 |
| A+ | SpaceServe | spatial multiplexing of complementary encoder/decoder phases | NeurIPS 2025 |
| A+ | ModServe | modality/stage-aware resource disaggregation | https://arxiv.org/abs/2502.00937 |
| A+ | EPD-Serve | flexible encode-prefill-decode serving on Ascend | https://arxiv.org/abs/2601.11590 |
| A+ | StreamWise | real-time multimodal generation serving | https://arxiv.org/abs/2603.05800 |
| A+ | HorizonServe | request scheduling + GPU sharing for omni models | https://arxiv.org/abs/2608.01785 |
| A+ | ElasticMM | elastic multimodal parallelism | https://arxiv.org/abs/2507.10069 |
| A+ | RServe / REDServe | encoding-prefill overlap | https://arxiv.org/abs/2509.24381 |
| A+ | Cornfigurator | automated deployment planning for any-to-any serving | https://arxiv.org/abs/2512.14098 |
| A+ | FlashCodec + UnifiedServe | preprocessing-aware multi-stage MLLM serving and GPU sharing | https://arxiv.org/abs/2512.17574 |
| A+ | HELIOS | production-scale multi-cloud GPU scheduling and multimodal/video pipeline infrastructure | https://www.heygen.com/research/avatar-v-infrastructure |
| A | HydraInfer | hybrid EPD scheduling | https://arxiv.org/abs/2505.12658 |
| A | OnePiece | distributed RDMA-based AIGC workflow serving | https://arxiv.org/abs/2601.20655 |
| A | TCM-Serve | modality-aware MLLM scheduling | https://arxiv.org/abs/2603.26498 |
| A | OrbitWeaver | persistent VLM execution state across edge power/thermal interruptions; two real satellites, phase-aware recovery | https://arxiv.org/abs/2610.29183 |
| A | StreamArena / StreamMind | always-on streaming multimodal runtime, persistent-state reuse, and causal evaluation | https://arxiv.org/abs/2608.05703 |

## Suggested reading order

### Serving architecture first
`vLLM-Omni → M* → Cornserve → Cornfigurator`

### Stage/resource scheduling
`ModServe → SpaceServe → Eevee → TriInfer → EPD-Serve → RServe → HorizonServe`

### State and workflow
`Omni-Flow → LiveServe → StreamWise → FlashCodec + UnifiedServe → HELIOS`

The shared machine-readable inventory remains [`../data/papers.json`](../data/papers.json).
