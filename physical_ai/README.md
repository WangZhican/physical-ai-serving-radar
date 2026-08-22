# Physical AI Serving

> Dedicated systems track for serving, runtime, scheduling, infrastructure, and deployment of embodied / robotic AI.

This track is intentionally written separately from the Multimodal / Omni track even though they share one repository and one metadata source.

## Scope

Physical AI serving begins where ordinary request/response inference stops. The system must reason about:

- physical execution progress and action deadlines;
- observation/state freshness;
- multi-rate perception / reasoning / action loops;
- robot-fleet multiplexing and shared accelerator pools;
- onboard / edge / cloud placement;
- VLA, WAM, planner, verifier and safety composition;
- physical-state-aware cache/state reuse;
- heterogeneous CPU/GPU/XPU/NPU deployment;
- real-robot evaluation, observability and reproducible runtime infrastructure.

## Research routes

| Route | Topic | Representative systems |
|---|---|---|
| P1 | Fleet-scale / Multi-Robot Serving | Kairos, ROSA, Armory, SOP |
| P2 | Unified Physical-AI Runtime | PhyAI, Embodied.cpp, vla.cpp, LeRobot |
| P3 | Real-Time / Streaming / Control-loop Serving | CROS-RT, PAAM, VLASH, FASTER, Reflex |
| P4 | Edge-Cloud / Disaggregated Physical AI | RoboECC, RAPID, EcoVLA, FogROS2 |
| P5 | Physical-State / Temporal Cache & State Reuse | AgenticCache, Persistent Computational State, WorldMove |
| P6 | Hardware-Aware / Heterogeneous Serving | XPU Characterization, PAAM, OOM-Free Alpamayo |
| P7 | Composite VLA + WAM + Planner Serving | M*, PhyAI, vLLM-Omni |
| P8 | Workload Characterization / Performance Modeling | VLA-Perf, PhyAI |
| P9 | Evaluation / Serving Infrastructure | DeepInsight, RoboArena, vla-eval, ros2probe |
| P10 | World-Model / WAM Rollout Serving | WorldMove, Persistent Computational State, PhyAI |

See the full map: [`../taxonomy/PHYSICAL_AI_MAP.md`](../taxonomy/PHYSICAL_AI_MAP.md).

## Recommended first reading

1. **Kairos** — serving semantics for generate–execute loops and multi-robot scheduling.
2. **ROSA** — robot-factory shared-GPU serving and productivity-oriented resource management.
3. **PhyAI** — unified VLA/WAM runtime spanning onboard, edge, cloud and rollout settings.
4. **VLA-Perf** — deployment/performance landscape and system bottleneck model.
5. **Embodied.cpp** — embodied-runtime abstraction for multi-rate, batch-1, heterogeneous execution.
6. **vla.cpp** — portable high-performance VLA runtime.
7. **Characterizing VLA Models across XPUs** — phase/hardware asymmetry and heterogeneous deployment.
8. **M*** — composite model graph serving that extends naturally into VLA/WAM pipelines.

Full list: [`CORE_READING.md`](CORE_READING.md).

## Boundary rule

A VLA paper is **not** a Physical-AI systems paper merely because it is faster. Pure pruning, quantization, action compression, or model-level approximation stays in `SYS_ALG_BOUNDARY` / `ALG_INSPIRATION` unless the main contribution changes the runtime, resource manager, serving abstraction, cache/state substrate, scheduler, or deployment architecture.

## Connection to Multimodal Serving

Physical AI inherits important mechanisms from multimodal systems—EPD disaggregation, module multiplexing, graph serving, distributed KV/state and heterogeneous placement—but adds physical-time semantics that ordinary MLLM serving does not have.

See [`../taxonomy/CROSSOVER.md`](../taxonomy/CROSSOVER.md).
