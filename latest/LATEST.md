# Latest Radar Update

**Scan time:** 2026-08-21 04:00 CST

## Fresh coverage
- **24h:** scanned; no new Physical-AI/Multimodal SYS work crossed the promotion threshold.
- **7d:** scanned; no additional fresh promotion.
- **30d / omission recovery:** active; Zenoh/DDS edge-cloud and intermittent-connectivity deployment evidence audited.

## This update
- Added **FogROS2-LS (ICRA 2024)** to the machine-readable public dataset, fixing a public-radar sync lag from the prior hour.
- Added **IoRT ROS 2 Applications: Evaluating Zenoh and VPN for Robotic Networking in the Edge-Cloud Continuum** (IEEE ISCC / DistInSys 2025 Best Paper) as `WATCH_ONLY`. It provides real-world latency, throughput, and fault-tolerance evidence for Zenoh in ROS 2 edge-cloud robotics, but evaluates existing middleware rather than introducing a new serving/runtime mechanism.
- The open-access version is available through Zenodo; the private PDF archive is not mirrored to this public repository.

## Current public radar state
- **97 verified works**
- **73 CORE_SYS**
- **16 SYS_ALG_BOUNDARY**
- **4 ALG_INSPIRATION**
- **4 WATCH_ONLY**

## Next frontier
Legal ROSGM/TILDE full-text resolution; then Zenoh/DDS intermittent-connectivity state continuity and timing/isolation enforcement, Armory-style fleet scheduling, policy-server batching, planner/procedural cache, persistent world-model state migration, and systems venue/group census.


## 2026-08-20 22:00 CST
Hourly scan completed: 24h/7d Physical-AI serving, fleet scheduling, Zenoh/DDS continuity, VLA policy-server and world-model runtime routes checked. No new work cleared the SYS-first promotion threshold; canonical classifications remain unchanged.


Last scanned: 2026-08-20 23:58 CST — 24h/7d fresh + targeted 30d systems scan; no new promotion; PCS/WorldMove deduplicated and revalidated.

Last scanned: 2026-08-21 00:57 CST — 24h/7d fresh + targeted 30d systems scan; no new promotion. Armory/action-chunk fleet serving deeply revalidated against arXiv, Georgia Tech RL2 project page and official code; already canonical CORE_SYS A+, so no duplicate added. Zenoh/DDS enforcement scan continued.

### 2026-08-21 02:01 CST
- Fresh 24h/7d SYS-first scan completed; no new paper promotion.
- Targeted coverage: fleet/action-chunk scheduling, policy-server protocols and batching, Physical-AI runtime, Omni serving, persistent world-model state.
- Ecosystem leads under reverse census: NVIDIA GR00T WholeBodyControl policy-server pipeline and TRI VLA Foundry gRPC deployment stack.

### 2026-08-21 03:01 CST
- **CORE_SYS +1: [LeRobot](https://arxiv.org/abs/2602.22818), ICLR 2026 Poster.** Recovered through policy-server/runtime reverse census rather than VLA-serving keywords.
- System role: end-to-end robot-learning infrastructure with generalized remote async inference via gRPC `PolicyServer`/`RobotClient`, action queues, overlapping action-chunk aggregation and configurable queue thresholds; this directly decouples robot execution from policy inference.
- Adoption: official `huggingface/lerobot` repository checked through GitHub API at **26,783 stars / 5,431 forks**.
- Fresh 24h/7d search itself produced no newer promotion; 30d/historical omission recovery remains active across policy-server protocols, planner cache and persistent world-state serving.

### 2026-08-21 04:00 CST
- No new CORE_SYS/SYS_ALG/WATCH promotion after fresh 24h/7d scans.
- Completed policy-server/runtime protocol census across OpenPI, NVIDIA Isaac-GR00T + WholeBodyControl, TRI VLA Foundry, GalaxeaVLA, and openpi-flash.
- Verified deployment-contract diversity: WebSocket action-chunk serving, ZMQ REQ/REP with ping/reset/timeout semantics, gRPC policy serving, ROS2 client/server deployment, and QUIC-first low-latency serving with combined planner+action mode.
- No audited system adds Armory-level multi-robot admission/fairness/deadline/SLO-aware scheduling, so these artifacts remain ecosystem evidence rather than new paper promotions.
- Next: multi-client policy admission/fairness/SLO search; vLLM-Omni OpenPI session semantics; planner/procedural cache; persistent world-state migration; Zenoh/DDS enforcement.

### 2026-08-21 05:02 CST
- **CORE_SYS +1: [RobotFleet](https://arxiv.org/abs/2510.10379)** — RSS 2025 Workshop on Scalable and Resilient Multi-Robot Systems.
- System role: centralized fleet orchestration over containerized robot services, with modular planner/allocator, task-status/schedule management, shared declarative world state, two-way execution feedback and replanning. It complements Armory/ROSA at the planner-to-fleet execution layer rather than GPU inference scheduling.
- Official repo: [therohangupta/robot-fleet](https://github.com/therohangupta/robot-fleet), about **30 stars / 5 forks** at this scan.
- vLLM-Omni OpenPI revalidation found a meaningful stateful serving contract: per-connection sessions, OpenPI handshake metadata (`action_horizon`, action keys, embodiment, session-id requirement), reset/session operations, and a dedicated serving bridge where batching/streaming/serialization live. This strengthens the reusable stateful robot-serving abstraction, but does not add a separate new paper promotion.
- Fresh multi-client admission/fairness/deadline/SLO search found no system beyond already-canonical Armory/ROSA with stronger fleet-serving scheduling evidence.

## 2026-08-21 06:01 CST
- Fresh 24h/7d SYS-first scan: no new promotion.
- **WATCH +1:** HELIOS: Heterogeneous Lightweight VLA Model Serving System — author/CV lists EuroSys 2027 submission; no public preprint/repo/details yet, so metadata-only watch.
- Continued planner/procedural-cache, fleet SLO/admission, and persistent world-state runtime omission recovery.

### 2026-08-21 06:57 CST
- **CORE_SYS +1:** [HeyGen HELIOS](https://www.heygen.com/research/avatar-v-infrastructure) — production-scale unified GPU infrastructure for multimodal/video AI.
- Scale/evidence: 5,000+ GPUs across 5+ clouds and 15+ cells; two-stage QoS-aware scheduling improved GPU utilization by 15% and reduced non-productive GPU time by ~20%; declarative reconciliation engine supports 200K+ concurrent tasks, >95% GPU utilization and <30s failure detection.
- Fresh 24h/7d Physical-AI serving scan produced no additional direct promotion; this item came from 30d industrial-infrastructure omission recovery.
- Name collision guard: HeyGen HELIOS is distinct from the HELIOS heterogeneous lightweight VLA-serving EuroSys 2027 submission watch item.
- Public state: 100 verified works / 75 CORE_SYS / 16 SYS_ALG / 4 ALG / 5 WATCH.

### 2026-08-21 08:04 CST
- **CORE_SYS +1:** [HydraInfer](https://arxiv.org/abs/2505.12658) — historical adjacent-multimodal SYS omission recovery: hybrid Encode-Prefill-Decode disaggregation, heterogeneous stage placement/resource reallocation, and stage-level batching.
- arXiv v2 reports up to **4x throughput** over vLLM on an 8xH800 node while meeting the 90th-percentile request SLO.
- Fresh 24h/7d Physical-AI serving scan produced no direct promotion; planner/fleet/world-state and multimodal SYS omission recovery continues.
- Public state: **101 verified works / 76 CORE_SYS / 16 SYS_ALG / 4 ALG / 5 WATCH**.
