# Physical AI Serving Radar — scan status

- Latest checkpoint: PHYSICAL_AI_SERVING_20261119_1000_CURRENT_RUN20ff2969_S20261119T015803Z
- Updated: 2026-11-19 10:00 CST
- Overall recall: **FAIL**
- Coverage closed: **false**
- Formal promotions: **0**

| Frontier | Status |
|---|---|
| 24h direct census | NOT_COVERED; OAI 141 exact / 57 unique, Atom 50 unique; 7 OAI-only IDs |
| 168h direct census | NOT_COVERED; OAI 5,759 exact / 2,270 unique, Atom 2,263 unique; 7 OAI-only IDs |
| OAI nested-window check | PASS_SUBSET; does not close pair parity |
| cs.LG cross-list | 24h 40 unique / 31 cross-listed / 9 target; 168h 1,685 / 1,337 / 141 |
| Main-trunk reverse-neighborhood | 46/46 queries; 294 unique; 163 outside direct census |
| First-party fallback | /new 5/5; /abs 19/20; Atom id_list 19/20; metadata only |
| Candidate inspection | 8/8 official /abs metadata verified |
| Paper/PDF manifests | Paper 417 unchanged; PDF 876 valid / 3 pending / 0 invalid; global reconciliation pending |
| Recall regression | Robion and Route-8 PASS |
| Scheduler | Run ID started_at mutation; next future trigger unverified |

The 24h zero-exact condition seen in the previous checkpoint is no longer present, but OAI/Atom parity remains incomplete. Search success, metadata fallback, and subset consistency are not treated as coverage closure.
