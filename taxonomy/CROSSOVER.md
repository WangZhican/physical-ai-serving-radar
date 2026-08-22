# Cross-over: Multimodal Serving → Physical AI Serving

The repository keeps Physical AI and Multimodal / Omni serving **separate in presentation** but connected in research lineage.

## The core relationship

Multimodal serving contributes reusable system mechanisms:

- stage / EPD disaggregation;
- module multiplexing and GPU sharing;
- any-to-any graph serving;
- distributed KV / intermediate-state management;
- heterogeneous placement;
- streaming / interactive scheduling;
- SLO-aware deployment planning.

Physical AI reuses these mechanisms but adds new first-class semantics:

- physical execution progress;
- action deadlines and reaction latency;
- observation / state freshness;
- robot/fleet resources;
- multi-rate control loops;
- planner / VLA / WAM / safety composition;
- physical-state-aware cache validity;
- rollout and world-state persistence.

## Important bridge systems

| System | Multimodal role | Physical-AI connection |
|---|---|---|
| **vLLM-Omni** | fully disaggregated any-to-any stage graph | action / robot-policy serving and reusable VLA stage infrastructure |
| **M*** | composite-model graph / walk serving | action generators, world-model predictors and robotic planning |
| **Omni-Flow** | distributed workflow + KV/state sharing | blueprint for shared policy/world/planner state infrastructure |
| **Cornserve** | model fission + independently scalable components | blueprint for VLA/WAM/planner component disaggregation |
| **Cornfigurator** | automatic placement / serving-plan search | potential robot/edge/cloud placement planner |
| **Eevee / SpaceServe** | module/spatial multiplexing | suggests VLM/action-expert co-location and complementary resource sharing |
| **TriInfer / EPD-Serve / HydraInfer** | stage-specific disaggregation | suggests VLM / action expert / WAM multi-rate stage placement |
| **LiveServe** | interaction-aware scheduling | analogous to action-deadline / state-freshness-aware scheduling |
| **HeteroServe / ElasticMM** | heterogeneous / elastic resource placement | maps naturally to robot / edge / cloud heterogeneous execution |
| **FlashCodec + UnifiedServe** | preprocessing-aware logical disaggregation with physical sharing | relevant to vision/video-heavy robot observation pipelines |

## A useful progression

```text
MLLM stage serving
  ↓
modality/module disaggregation
  ↓
any-to-any composite graph serving
  ↓
distributed state + heterogeneous placement
  ↓
Physical AI: graph + state + physical-time semantics
  ↓
fleet-scale VLA/WAM/planner/safety serving
```

The point of the shared repository is to preserve this technical lineage **without collapsing the two research fields into one taxonomy**.
