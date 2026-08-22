# Physical AI Serving — Core Reading

This list is ordered by **systems value**, not by citation count.

| Priority | Work | Main systems role | Paper / project |
|---|---|---|---|
| S+ | Kairos: A Scalable Serving System for Physical AI | generate–execute-aware multi-robot serving | https://arxiv.org/abs/2605.11381 |
| S+ | ROSA: A Robotics Foundation Model Serving System for Robot Factories | fleet GPU pooling, multi-model robot SLOs | https://arxiv.org/abs/2607.01088 |
| S+ | PhyAI | unified VLA/WAM edge-cloud-rollout runtime | https://arxiv.org/abs/2608.03682 |
| S+ | M* | composite-model graph serving, robotic/world-model crossover | https://arxiv.org/abs/2606.12688 |
| S | VLA-Perf | VLA deployment/performance modeling | https://arxiv.org/abs/2602.18397 |
| S | Embodied.cpp | portable embodied inference runtime | https://arxiv.org/abs/2607.02501 |
| S | vla.cpp | portable C++ VLA runtime | https://arxiv.org/abs/2606.08094 |
| S | Characterizing VLA Models across XPUs | heterogeneous on-robot performance characterization | https://arxiv.org/abs/2604.24447 |
| S | vLLM-Omni | general multimodal serving infrastructure extending into robot/action serving | https://arxiv.org/abs/2602.02204 |
| A+ | Armory | control-aware batched robot-policy serving | https://arxiv.org/abs/2608.00337 |
| A+ | SOP | fleet/cloud actor-learner infrastructure and async policy synchronization | https://arxiv.org/abs/2601.03044 |
| A+ | LeRobot | generalized remote async policy serving API/runtime | https://arxiv.org/abs/2602.22818 |
| A+ | PAAM | shared accelerator server for real-time robotics workloads | https://arxiv.org/abs/2404.06452 |
| A+ | FogROS 2 | cloud/fog robotics deployment substrate | https://arxiv.org/abs/2205.09778 |
| A+ | FogROS2-PLR | tail-latency/reliability-aware cloud robotics | https://arxiv.org/abs/2410.05562 |
| A+ | DeepInsight | cross-stack Physical-AI evaluation/runtime infrastructure | https://arxiv.org/abs/2606.17574 |
| A+ | RoboArena | distributed real-robot evaluation network | https://arxiv.org/abs/2506.18123 |
| A+ | RLinf-VLA / RLinf | distributed embodied/VLA RL runtime and resource allocation | https://arxiv.org/abs/2510.06710 |

## Important SYS–ALG boundary line

These works are worth reading because they expose system semantics, but their primary novelty is not a general serving system:

- **VLASH** — prediction/execution temporal misalignment and asynchronous inference.
- **FASTER** — TTFA and horizon-aware real-time action generation.
- **Reflex** — streaming state/cache maintenance and asynchronous vision/action pipeline.
- **AsyncVLA** — remote semantic model + onboard reactive execution.
- **CloudEdgeVLA** — stale-state-tolerant cloud/edge split.
- **ActionCache** — action-intermediate reuse as inspiration for physical-state-aware cache infrastructure.

See the complete inventory in [`../papers/CORE_SYS.md`](../papers/CORE_SYS.md) and [`../papers/SYS_ALG_BOUNDARY.md`](../papers/SYS_ALG_BOUNDARY.md).

### RoboChallenge — A+
Online real-robot evaluation-as-a-service with a 10-machine heterogeneous fleet, asynchronous timestamped observation/action-queue APIs, job scheduling, public submission/results and an official inference client. [Paper](https://arxiv.org/abs/2510.17950) · [Project](https://robochallenge.ai/) · [Repo](https://github.com/RoboChallenge/RoboChallengeInference)
