# Physical AI Serving Radar — latest

**Checkpoint:** 2026-11-19 21:27 CST
**Updated:** 2026-11-19T21:48:26+08:00
**Status:** Paired 24h/168h direct-source census parity holds; main-trunk reverse-neighborhood remains partial due HTTP 429; semantic recall and scheduler continuity remain open.

## Source coverage

- Rolling 24h: OAI 386 exact / 151 unique; Atom 151 unique. Five-category exact set equality.
- Rolling 168h: OAI 6144 exact / 2434 unique; Atom 2434 unique. Five-category exact set equality.
- Both 24h sets are subsets of their 168h sets. This closes paired source-acquisition parity for these exact windows, not semantic recall.
- Main-trunk: 21/46 query templates succeeded; 25 HTTP 429; 121 unique IDs, 33 outside direct census. Both official arXiv API host probes returned HTTP 429.
- SYS-first: 2434 unique IDs, 315 high-signal, 291 unclassified.

## Candidate radar

- 16 selected candidates were checked against official arXiv metadata.
- FlashRT-PAI (2610.24349) received official PDF/full-text inspection; its public repository is https://github.com/flashrt-project/FlashRT. It is a strong Physical-AI serving candidate, not yet promoted.
- HyCoInfer (2611.22086) received official PDF/full-text inspection; it is a cloud-edge GPU/FPGA LLM-serving candidate, not a demonstrated Physical-AI workload.
- No new Paper/PDF Manifest entry or formal promotion was made.

## Research status

- Robion arXiv:2609.12075 and Route-8 recall regression checks pass.
- Formal promotions: 0.
- Overall recall: FAIL; coverage_closed=false.
- Paper/PDF reconciliation and named evidence gates remain open.
- Automation remains expected-active; same-Run-ID started_at mutation and next-trigger verification remain open.

See [the hourly scan](hourly/2026-11-19-2127_CURRENT_RUN0c7c8271_S20261119T132747Z.md) and [scan status](SCAN_STATUS.md).
