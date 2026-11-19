# Physical AI Serving Radar — latest

**Checkpoint:** PHYSICAL_AI_SERVING_20261119_1000_CURRENT_RUN20ff2969_S20261119T015803Z
**Updated:** 2026-11-19 10:00 CST (evidence reconciled 10:23 CST)
**Status:** SYS-first discovery advanced; direct paired coverage and scheduler continuity remain open.

## Source coverage

- Rolling 24h: NOT_COVERED. OAI returned 141 exact / 57 unique; Atom returned 50 unique. Seven unique OAI-only IDs remain.
- Rolling 168h: NOT_COVERED. OAI returned 5759 exact / 2270 unique; Atom returned 2263 unique. The same seven OAI-only IDs remain.
- The 24h OAI ID set is contained in the 168h set. This subset check does not close paired-source parity.
- Main-trunk reverse-neighborhood: 46/46 queries, 294 unique IDs, including 163 outside the direct census.
- cs.LG cross-list and first-party /new, /abs, Atom id_list routes were inspected; metadata discovery is not exact-window coverage.

## Candidate radar

- CommitKV (arXiv:2608.07855) is a high-priority multimodal KV-cache candidate; full-text and serving-path verification remain pending.
- MoMoVL (arXiv:2611.23695) is an on-device modality-aware MoE compression candidate; full-text review remains pending.
- Eight new candidate abstracts were checked against official arXiv metadata. No formal promotion was made.
- Robion arXiv:2609.12075 and Route-8 recall regression checks pass.

## Research status

- SYS-first: 2270 unique IDs, 281 high-signal, 253 unclassified.
- Formal promotions: 0.
- Overall recall: FAIL; coverage_closed=false.
- Paper/PDF reconciliation and named evidence gates remain open.
- Automation remains expected-active; scheduler Run ID timestamp mutation and the next future trigger remain unresolved.

See [the hourly scan](hourly/2026-11-19-1000_CURRENT_RUN20ff2969_S20261119T015803Z.md) and [scan status](SCAN_STATUS.md).
