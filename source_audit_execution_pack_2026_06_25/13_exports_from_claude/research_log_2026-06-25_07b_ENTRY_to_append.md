## 2026-06-25 — 07b: Source-Audit Remediation (Phase 16 repair)

Prompt file used: prompts/04_diligence_scoring/02b_apply_source_audit_remediation.md; prompts/07_refresh_and_controls/02g_update_export_package.md (export)
Claude mode used: Research (advanced) for source verification; normal chat for packaging and file generation
Project files used: 00_admin/claude_project_instructions.md (governing), 01_sources/source_whitelist.md, source_quality_policy.md, source_quality_policy_addendum_scoring_audit.md, 01_score_filtered_ideas.md, 02_diversity_filter_70_90.md, 01_raw_idea_generation_120.md, source_evidence_ledger.csv, source_issue_tracker.csv
Key outputs:
  - Applied all 11 remediations (ISSUE-001..ISSUE-015). Eligibility: 19 eligible for top-25 deep dive (1 CLEARED = RID-053; 18 CLEARED_WITH_WEAKNESS), 30 blocked (24 HOLD = 16 placeholders + 8 drone RIDs; 4 KILL = RID-036/041/042/045; 2 NEEDS_MORE_SOURCE = RID-087/091).
  - Citation fixes verified: SCORE-010 first author = Djassemi et al. (ACS Sensors 2026 11(2):1413-1424, DOI 10.1021/acssensors.5c03699; Wang is senior author); SCORE-015 Awad = 2024 (Surg Endosc 38(10):6193-6202), Servais 2025 confirmed (39(2):1217-1226).
  - Relabels: OCP/Deschutes -> Tier 2 industry-consortium/product-spec (specs 2MW/500GPM/80-90psi/3C verified via OCP Deschutes 5.0 + vendor pages + ARPA-E deck); NVIDIA "-30%" -> company-supported (GB300 dev blog, LITEON, internal Megatron test); CFS "$8M" = DOE-validated milestone, "largest" -> company-supported (no DOE primary); da Vinci "43%" -> preclinical/Intuitive-supported.
  - HBM4: replaced 36Kr (Tier 4) with JEDEC JESD270-4 + Semiconductor Engineering; 720->775um confirmed -> hybrid bonding postponed -> RID-042 kill locked (industry trending to 825-900um for HBM4E/HBM5).
  - Humanoid BOM: deleted misattributed "Morgan Stanley 56%" (the 56% = China share of MS Humanoid 100 universe, not actuator BOM); kept McKinsey 40-60% + BofA 40-50%.
  - SCORE-004D geography reversal: CELEX:52025DC0005 is a non-binding EU IPI report describing CHINA's Document 551 (25-100% localization; 100% for 137/178 categories); binding follow-on is Reg (EU) 2025/1197 (supplier-exclusion measure). RID-087/091 stay policy-context-only.
  - Policy triggers confirmed non-final: FAA Part 108 (FR 2026-01644; no final rule as of 2026-06-25); BIS FR 2026-00789 (active/volatile); USTR Section 301 SiC (rate TBD, announce ~2027-05-24).
Files updated:
  - source_issue_tracker.csv — REPLACE 15 rows (status -> CLEARED / CLEARED_WITH_WEAKNESS / HOLD / KILL_STANDS / WATCH / NEEDS_MORE_SOURCE; next_prompt routed to 02c/02d/02e)
  - source_evidence_ledger.csv — APPEND 9 scoring-evidence rows SCORE-001/002/004/010/013/015/016/004D + new SCORE-013-DOE (all count_toward_300=no; corpus counted total unchanged at 397). Ledger now 433 data rows.
  - scored_idea_database_repaired_2026_06_25.csv — NEW FILE, 49 affected rows (new_score=old_score, delta=0; numerical re-score deferred to 02e)
  - 07b_source_audit_remediation.md — substantive 02b output (repair + evidence-label tables, blocked/eligible lists)
  - policy_trigger_watchlist.csv — 6 provisional trigger rows seeded (finalize in 02d)
  - research_log.md — this entry
New sources added: 0 to the 300-corpus (9 scoring-evidence rows logged count_toward_300=no); 1 provisional new scoring source located (SCORE-013-DOE)
New ideas added: 0 (hard rule)
Ideas rejected: 0 new (4 prior Phase-16 kills confirmed with strengthened rationale: RID-036/041/042/045)
Open questions:
  - 02e: apply downward score adjustments where flagged (SCORE-002 cluster; surgical SCORE-015/da Vinci cluster; CFS "largest"); RID-053 needs no penalty.
  - Find a DOE.gov primary page asserting the CFS "$8M / largest" figure to upgrade ISSUE-007 confidence.
  - Strict-reviewer call: route RID-077/081/088 to HOLD pending clinical-outcome data rather than CLEARED_WITH_WEAKNESS? Flagged for 02e.
  - RID-051 is a borderline admit (thin evidence); confirm a direct spec or downgrade in 02e.
Next action: Run prompts/04_diligence_scoring/02c_placeholder_source_repair.md (07c) in a fresh chat to attempt >=1 direct Tier 1/2 source per the 16 placeholder RIDs; prioritize the three currently scored "pursue" (RID-111, RID-016, RID-100). Then 02d (policy-trigger watchlist) -> 02e (targeted re-score) -> 02f (top-25 eligibility gate). Do not run deep dives until the 02f gate clears.
