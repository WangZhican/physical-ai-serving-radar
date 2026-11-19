# Physical AI Serving Radar — scan status

- Latest checkpoint: `PHYSICAL_AI_SERVING_20261119_0900_CURRENT_RUN7fe271fc_S20261119T010314Z`
- Updated: 2026-11-19 09:00 CST
- Overall recall: **FAIL**
- Coverage closed: **false**
- Formal promotions: **0**

| Frontier | Status |
|---|---|
| 24h direct census | NOT_COVERED; OAI exact=0, Atom incomplete |
| 168h direct census | INCOMPLETE; 10 OAI-only category mismatches |
| cs.LG cross-list | Metadata-only; 24h zero, 168h 1,567 unique |
| Main-trunk reverse-neighborhood | 46/46 queries; 276 unique; 153 outside direct census |
| First-party fallback | /new 5/5; /abs 18/20; Atom id_list 9/20 |
| Candidate inspection | 8/8 official /abs metadata verified |
| Paper/PDF manifests | Paper 417 unchanged; PDF global reconciliation pending |
| Recall regression | Robion and Route-8 PASS |
| Scheduler | Distinct 09:00 run observed; completion and 10:00 trigger unverified |

The zero-exact 24h anomaly is retained as NOT_COVERED. Search success, metadata fallback, and source parity are not treated as coverage closure.
