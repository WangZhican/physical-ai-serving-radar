# Physical AI Serving Radar — latest

**Checkpoint:** 2026-11-19 16:55 CST
**Updated:** 2026-11-19 17:10 CST
**Status:** Paired direct-source census parity restored; semantic recall and scheduler continuity remain open.

## Source coverage

- Rolling 24h: OAI 671 exact / 269 unique; Atom 269 unique. Exact set equality across cs.DC, cs.AR, cs.PF, cs.RO, and cs.LG.
- Rolling 168h: OAI 6,322 exact / 2,491 unique; Atom 2,491 unique. Exact set equality across the same categories.
- Both 24h sets are contained in their 168h sets. This closes paired source-acquisition parity for these windows, not overall semantic recall.
- cs.LG cross-list: 24h 180 unique / 138 cross-listed / 18 target-category cross-lists; 168h 1,834 / 1,449 / 158.
- Main-trunk reverse-neighborhood: 46/46 queries, 330 unique IDs, including 176 outside the direct census.

## Candidate radar

- Eight candidates were checked against official arXiv metadata.
- FlatCake is a strong cross-domain KV-storage/serving candidate; Cap-and-Track is an adaptive dispatch design with production evidence. Both remain unpromoted pending fit to the Physical-AI serving scope.
- Z-sight and Phoenix are relevant VLA/world-action-model research, but the inspected evidence does not establish serving/runtime contributions.
- No formal promotion was made.

## Research status

- SYS-first: 2,491 unique IDs, 325 high-signal, 300 unclassified.
- Robion arXiv:2609.12075 and Route-8 recall regression checks pass.
- Formal promotions: 0.
- Overall recall: FAIL; coverage_closed=false.
- Paper/PDF reconciliation and named evidence gates remain open.
- The automation remains expected-active; scheduler continuity is still under investigation.

See [the hourly scan](hourly/2026-11-19-1655.md) and [scan status](SCAN_STATUS.md).
