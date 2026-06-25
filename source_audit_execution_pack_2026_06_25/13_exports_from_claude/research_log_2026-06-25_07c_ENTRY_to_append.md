## 2026-06-25 — 07c: Placeholder Source Repair (ISSUE-014 resolution)

Prompt file used: prompts/04_diligence_scoring/02c_placeholder_source_repair.md; prompts/07_refresh_and_controls/02g_update_export_package.md (export)
Claude mode used: Research (advanced) for the 16-RID source search; normal chat for packaging and file generation
Project files used: 00_admin/claude_project_instructions.md (governing), 01_sources/source_whitelist.md, source_quality_policy.md, source_quality_policy_addendum_scoring_audit.md, 01_score_filtered_ideas.md, 01_raw_idea_generation_120.md, source_evidence_ledger.csv, source_issue_tracker.csv, scored_idea_database_repaired_2026_06_25.csv
Key outputs:
  - Resolved the umbrella ISSUE-014 (16 placeholder RIDs lacking direct Tier 1/2 support). Result: 8 CLEARED, 7 CLEARED_WITH_WEAKNESS, 1 HOLD (RID-094).
  - All three priority "pursue" RIDs cleared on direct Tier 1 evidence: RID-111 (Sci Rep 2022 nanopositioning bandwidth-resonance tradeoff + hybrid-bonding 0.2um-at-3sigma placement spec, US Patent 12438117), RID-016 (China MIIT echelon-utilization 梯次利用 specification + UL 1974 + NREL fy22osti/84527), RID-100 (Photonics 12(8):821 2025 active-alignment packaging bottleneck; corroborated arXiv 2112.14357 "packaging up to 80% of cost").
  - Final-law / final-standard drivers confirmed (finality test passed): RID-020 (UL 9540A + NFPA 855:2026 §9.7.6.6 TRPP), RID-040 (Directive (EU) 2023/1791 Art. 26.6 + German EnEfG §11(2), effective 1 Jul 2026), RID-017 (GB/T 44265-2024), RID-032 (ISO 15118-20:2022).
  - Other clears: RID-015 (Sandia/DOE G3P3 >700C, 6h storage, AIP 10.1063/5.0029216), RID-012 (IEA Energy-and-AI 2026/2025 onsite-power-from-grid-scarcity + LBNL "Queued Up 2025"), RID-082 (Front. Neurosci. 2023 implant power/longevity, 3-5yr DBS battery), RID-026 (NREL UNIFI TP-5D00-89269 + FERC Order 2023), RID-022 (IEEE 2030.10-2021 + DOE OE), RID-097 (TGV ultrashort-pulse laser micromachining, JMPT 2025), RID-101 (JOM 2018 + ORNL OSTI 1273151 molten-salt corrosion), RID-099 (Nature Electronics 2018 + NIST overlay, sub-1nm).
  - RID-094 HOLD: NIST AM-Bench / 2026 in-situ metrology roadmap is a genuine Tier 1 source, but the RID is a prior kill and collides with the project's aversion to diagnostic/testing/monitoring overproduction; no standalone procurement/standards driver found, so not force-cleared (routed back to 02c).
Files updated:
  - source_issue_tracker.csv — REPLACE the umbrella ISSUE-014 row with 16 per-RID rows ISSUE-014-111 ... ISSUE-014-099 (status CLEARED / CLEARED_WITH_WEAKNESS / HOLD; next_prompt 02e for cleared, 02c for RID-094). Tracker now 30 data rows.
  - source_evidence_ledger.csv — APPEND 15 placeholder-repair rows PH-001..PH-015 (all count_toward_300=no; one row per cleared RID; no row for HOLD RID-094). Ledger now 448 data rows; counted corpus total unchanged at 397.
  - scored_idea_database_repaired_2026_06_25.csv — UPDATE the 16 placeholder rows: evidence_status, top25_eligible (yes for the 15 cleared, no for RID-094), repair_notes, and source_issue_ids. new_score = old_score, delta = 0, decision letters unchanged (numerical re-score deferred to 02e).
  - research_log.md — this entry.
New sources added: 0 to the 300-corpus (15 placeholder-repair rows logged count_toward_300=no; counted total stays 397)
New ideas added: 0 (hard rule)
Ideas rejected: 0 new (RID-094 remains HOLD, not a new kill; prior RID-094 kill rationale stands)
Open questions:
  - 02e: re-test RID-099 against the testing/monitoring-overproduction filter (it nearly went HOLD with RID-094); discount RID-101 if the deep-dive horizon is strictly <=2030; confirm RID-026 is a hardware controller, not a software/consulting play; confirm RID-040's target geography is EU (driver is EU/Germany-bounded).
  - RID-094: revisit only if a procurement document, standard, or regulator requirement emerges that demands AM in-situ NDE as a standalone purchased capability decoupled from generic monitoring.
  - PH-010 caveat carried forward: IEA onsite-gas/battery figures are 2030 projections; LBNL "Queued Up" explicitly excludes behind-the-meter projects (supports the scarcity half of RID-012, IEA carries the BTM-solution half).
Next action: Run prompts/04_diligence_scoring/02d_policy_trigger_watchlist.md (07d) in a fresh chat to finalize policy_trigger_watchlist.csv (full 11-column schema; seed rows from 07b), then 02e (targeted re-score of all CLEARED / CLEARED_WITH_WEAKNESS RIDs) -> 02f (top-25 eligibility gate). Do not run deep dives until the 02f gate clears.
