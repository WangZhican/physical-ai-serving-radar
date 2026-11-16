# Physical AI Serving Radar — Latest

Checkpoint: PHYSICAL_AI_SERVING_20261116_1000
Updated: 2026-11-16T11:08:07+08:00
Source window end: 2026-11-16T02:08:14Z
Overall: RECALL_OPEN / COVERAGE_OPEN

- 24h direct census: OAI transport PASS, 0 exact; Atom INCOMPLETE (cs.DC timeout, cs.AR HTTP 429, cs.PF/cs.RO/cs.LG one page / 0 exact). Official /new 5/5 HTTP 200 / 817 IDs; /abs 41/41 HTTP 200 / 0 exact; Atom id_list HTTP 429. NOT_COVERED_ZERO_EXACT.
- 168h direct census: OAI 8,202 retrieved / 4,628 exact / 1,866 unique; Atom INCOMPLETE / 578 unique. Five-category sets do not match; OAI-only delta 1,408. SOURCE_ONLY_NOT_COVERED.
- Main-trunk reverse-neighborhood: primary 9/34; expansion 0/12. 37 failed/incomplete queries, mostly HTTP 429/timeouts. PARTIAL_SOURCE_NOT_COVERED; SEARCHED != COVERED.
- SYS-first triage: 1,866 unique, 240 high-signal, 199 high-signal unclassified. Robion arXiv:2609.12075 remains the permanent recall-regression seed.
- Full-text review: Superfluid (arXiv:2611.17753v1), official 8-page PDF and author-linked Apache-2.0 implementation inspected. CORE_SYS candidate / A- / Routes 6/9, **not formally promoted**. Remaining evidence gates: docs/code durability reconciliation, session-ID restart/WAL replay test, open-loop p95/p99 and fairness, VLA/robot workload, independent reproduction.
- Full-text review: H2E (arXiv:2611.16246v1), official 11-page PDF; ALG_INSPIRATION / WATCH_ONLY / B. Policy-training/algorithmic inspiration, not a serving/runtime/scheduler result.
- Public curated index: 392 unchanged. Private canonical manifest: 402 papers; 853 valid PDFs; 3 pending; 31 full-text reviews. Private PDF Manifest is not published.
- Formal promotions this checkpoint: 0; cumulative 2. Overall recall remains FAIL; coverage is not closed.

Public sync status at scan time: PUBLIC_SYNC_PENDING. Prior remote master baseline: 934eab7dcb74a4df742c182171ba676456ae68e9.
