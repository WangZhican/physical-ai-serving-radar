# Scan Status

Checkpoint: PHYSICAL_AI_SERVING_20261115_1240

Status: PUBLIC_SYNC_VERIFIED / 24H_NOT_COVERED / 168H_OAI_ONLY_ATOM_INCOMPLETE / 720H_LAST_GOOD_NOT_REFRESHED / MAIN_TRUNK_2_OF_34_PLUS_0_OF_12_HTTP429 / ZERO_FORMAL_PROMOTIONS / COVERAGE_OPEN.

Rolling 24h (2026-11-14T04:11:23+00:00 to 2026-11-15T04:11:23+00:00): OAI-PMH 1 page / 0 retrieved / 0 exact; all five direct Atom category requests timed out on page 0. Official first-party fallback: /new 5/5 HTTP 200 (817 IDs), /abs 41/41 HTTP 200 but 0 exact-window, Atom id_list timed out. Latest checked version timestamp 2026-11-12T18:59:54+00:00, 57.19 hours before the window end. Keep NOT_COVERED.

Rolling 168h: OAI-PMH 7,693 retrieved / 4,745 exact / 1,975 unique; category counts cs.DC 125, cs.AR 56, cs.PF 35, cs.RO 410, cs.LG 1,485. All five Atom requests timed out on page 0; no OAI/Atom set-equality claim. SOURCE_ONLY_NOT_COVERED.

Rolling 720h was not refreshed. Preserve the last-good 11:10 result (11,226 OAI/Atom unique, five category sets equal) as historical SOURCE_ONLY_NOT_COVERED, not as a current refresh.

Main-trunk: 34 primary + 12 expansion queries attempted; 2/34 primary passed and 32 returned HTTP 429; 0/12 expansion passed and 12 returned HTTP 429. The last-good 11:10 34/34 + 12/12 result is retained but its window ended at 03:01:23 UTC, before this checkpoint's 04:11:23 UTC window. Current main-trunk status remains PARTIAL_429.

SYS-first triage: 1,975 unique / 252 high-signal / 217 unclassified. Robion arXiv:2609.12075 remains the permanent recall regression seed; official /abs HTTP 200, no current-window credit. Route-8 seed 2610.05062 remains retained, no current-window credit.

Candidate added: SlackTier (arXiv:2611.13413 v1), CORE_SYS/WATCH_ONLY/B+, routes 5/6/8. Official /abs and /pdf both HTTP 200; 15-page PDF exactly SHA-matches the existing local file. It adds deadline-aware lookup-table placement, cache allocation and NVMe/RDMA serving to SGLang. Generic LLM/agent traces only; no Physical-AI/VLA workload or author-linked implementation verified. No formal promotion.

Inventory: 387 papers; 842 valid PDF entries / 0 invalid / 3 pending; 824 unique paper IDs / 833 unique versioned PDFs / 9 duplicate copies. The three PDF blockers remain Eevee ACM 403, ROSGM IEEE 502 and TILDE IEEE 502; no non-due retry.

Public sync verified: heartbeat commit adc78dbb8e1d2a3f1ed24b5601a28c4a52d0c6f8; the 387-row public index matches all 387 private manifest IDs with no missing or extra IDs. Origin and explicit SSH refs/heads/master independently matched the heartbeat commit before this status-seal commit.

Automation: original task remains Enabled/Expected-active. Current run cd35fd72-57e0-8320-b706-235c8649be16 started 40m06s after its 12:00 CST boundary; registry next_run_time still points to the past 12:00 boundary, and the next future trigger is unverified. No schedule mutation.

KerColle, Streaming-WAM and HarnessPAI remain open evidence gates. Overall recall FAIL; coverage_closed=false; SEARCHED != COVERED.
