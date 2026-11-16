# Physical AI Serving Radar — Latest

Checkpoint: PHYSICAL_AI_SERVING_20261116_0800
Updated: 2026-11-16T08:21:10+08:00
Source window end: 2026-11-16T00:02:09Z
Overall: RECALL_OPEN / COVERAGE_OPEN

- 24h direct census: OAI transport PASS but 0 retrieved / 0 exact. Atom is INCOMPLETE: cs.DC/cs.AR/cs.PF/cs.RO returned HTTP 429; cs.LG crossed one page with 0 exact. Official fallback checked five /new pages (817 IDs) and 41 /abs version-history requests (41 HTTP 200, 0 exact); Atom id_list returned HTTP 429. NOT_COVERED_ZERO_EXACT.
- 168h direct census: OAI 7,693 retrieved / 4,197 exact / 1,703 unique. Atom is INCOMPLETE with 555 unique: cs.RO 364 exact, cs.LG 200 before timeout, cs.DC timeout, cs.AR/cs.PF HTTP 429. Category-set equality is not established; SOURCE_ONLY_NOT_COVERED.
- Main-trunk reverse-neighborhood: primary 10/34 queries passed (57 unique, 56 category pairs, 0 reverse-only); expansion 0/12. 36 queries failed or were incomplete, predominantly HTTP 429. PARTIAL_SOURCE_NOT_COVERED; preserve 0400 last-good 46/46 and 0557 partial 15/34, 0/12.
- Full-text review: Read Once, Answer Many (arXiv:2611.15130), official 17-page PDF and author-linked Apache-2.0 repository verified. Classified SYS_ALG_BOUNDARY / WATCH_ONLY: shared-context KV reuse and stream-id masking are useful, but the inspected implementation is offline, single-GPU, Triton-only, and not integrated with an online scheduler. No formal promotion.
- Next dynamic full-text candidate: MARS (arXiv:2604.26963), “Towards High Goodput and Low KV Thrashing in Agent Serving under GPU Memory Constraints.” KerColle, Streaming-WAM, and HarnessPAI remain open evidence gates.
- Public curated index: 392. Private canonical manifest: 399 papers; 850 valid PDFs; 3 pending; 28 full-text reviews. The public index remains a separately curated subset.
- Formal promotions this checkpoint: 0; cumulative 2. Overall recall remains FAIL; coverage is not closed.

Public sync status at scan time: PUBLIC_SYNC_PENDING. Remote master baseline: fee42c08d920b9a5ea90f8fdfcdc225d1eae4f01. This checkpoint is not yet published.
