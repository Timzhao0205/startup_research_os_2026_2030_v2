<task>
Re-score only the ideas affected by the source-audit remediation.
</task>

<inputs>
Use:
- updated source_issue_tracker.csv
- updated source_evidence_ledger.csv
- scored_idea_database_repaired_2026_06_25.csv if available
- 01_score_filtered_ideas(1).md or 01_score_filtered_ideas.md
- 07b_source_audit_remediation.md if available
- 07c_placeholder_source_repair.md if available
- policy_trigger_watchlist.csv
</inputs>

<affected_groups>
Re-score only:
1. RIDs affected by SCORE-001 and SCORE-002 re-tiering.
2. RIDs affected by NVIDIA company-claim relabeling.
3. RIDs affected by CFS company-supported relabeling.
4. RIDs affected by da Vinci preclinical/company-supported relabeling.
5. RIDs affected by HBM4 citation replacement and hybrid-bonding timing.
6. RID-053 humanoid actuator after replacing 56%/Morgan Stanley with McKinsey 40–60%.
7. All drone RIDs whose regulatory trigger remains speculative.
8. The 16 placeholder RIDs after source repair.
9. RID-036 and RID-042, confirming whether kill status stands.
10. RID-087 and RID-091, confirming whether customer pain remains policy-context-only.
</affected_groups>

<scoring_rules>
Use the original 100-point scoring rubric.
Do not re-score unaffected ideas.
Reduce score if evidence quality decreased.
Reduce score if customer pain is only policy-context.
Reduce score if the core regulatory trigger remains speculative.
Reduce score if source support is company-claim only.
Reduce score if source support is preprint-only.
Keep kills if the audit says the kill stands and no new direct evidence changes it.
</scoring_rules>

<deliverable>
Produce:
1. Before/after score table.
2. Score deltas by rubric category.
3. Decision changes.
4. Top-25 eligibility status.
5. CSV-ready corrected scored_idea_database_repaired_2026_06_25.csv rows.
6. Updated blocked-from-deep-dive list.
7. Updated deep-dive-eligible list.
8. Final source-audit status summary.

<status_options>
Use only these:
- CLEARED
- CLEARED_WITH_WEAKNESS
- HOLD
- KILL
- NEEDS_MORE_SOURCE
</status_options>

<rules>
Do not generate new ideas.
Do not deep-dive ideas.
Do not re-score unaffected ideas.
Be strict.
</rules>
