# WATCHLIST

Promising concepts or ecosystem artifacts that are relevant to Physical-AI serving but do not yet meet the `CORE_SYS` evidence bar.

- **Harness Engineering for Physical AI: Robot Middleware Is the Harness Layer** — systems vision around Projection / Isolation / Transfer and a ROS 2 Harness Profile; kept here until a validated implementation/evaluation exists.
- **Same Weights, Different Robot: A Deployment Safety View of VLA Policies** — useful executable-policy/deployment-contract semantics, but currently a specification/diagnostic contribution rather than a serving system.
- **The Three Dimensions of ROS 2 Middleware** — Space / Time / State taxonomy; useful query anchor for topology abstraction, temporal predictability and state continuity, but not a runtime implementation.
- **IoRT ROS 2 Applications: Evaluating Zenoh and VPN for Robotic Networking in the Edge-Cloud Continuum** — IEEE ISCC / DistInSys 2025 Best Paper; useful real-world edge-cloud latency/throughput/fault-tolerance evidence for Zenoh, but primarily evaluates existing middleware rather than introducing a new runtime mechanism.

## Active follow-ups
- FogROS2-SGC / FogROS2-LS: determine whether they contribute durable cloud-connectivity/placement abstractions beyond the existing FogROS lineage.
- NVIDIA `ros2_benchmark`: classify as a mature infrastructure artifact and determine whether a canonical paper record should be created.
- Zenoh/DDS intermittent-connectivity state continuity and timing/isolation enforcement.
- Fleet admission/fairness and action-buffer-aware scheduling beyond Armory/Kairos/ROSA.

### HELIOS: Heterogeneous Lightweight VLA Model Serving System
- EuroSys 2027 in submission; metadata-only author disclosure. No public preprint/repo/details verified yet.
