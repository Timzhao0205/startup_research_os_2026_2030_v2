<task>
Create the top-25 deep-dive eligibility gate after source-audit repair and targeted re-score.
</task>

<inputs>
Use:
- scored_idea_database_repaired_2026_06_25.csv
- source_issue_tracker.csv
- source_evidence_ledger.csv
- policy_trigger_watchlist.csv
- 07b_source_audit_remediation.md if available
- 07c_placeholder_source_repair.md if available
- 07e_targeted_rescore.md if available
</inputs>

<eligibility_rules>
Eligible for top-25 core deep dive:
- CLEARED
- CLEARED_WITH_WEAKNESS

Not eligible:
- HOLD
- NEEDS_MORE_SOURCE
- KILL
- REGULATORY_SPECULATION if the core thesis depends on the speculative trigger
- POLICY_CONTEXT_ONLY if no buyer/procurement/budget/direct customer pain is found

Special rule for drone RIDs:
Drone RIDs may enter a watchlist appendix, but cannot be treated as top-25 core opportunities if the thesis depends on FAA Part 108 finalization.

Special rule for company-supported evidence:
Company-supported evidence can support product existence or company-claimed performance, but cannot independently support broad market pain, clinical outcome, or policy fact.

Special rule for policy-context-only pain:
Policy context can support timing, but not willingness-to-pay unless linked to buyer pain, procurement, regulation, or budget.
</eligibility_rules>

<deliverable>
Produce:
1. Eligible top-25 list, ranked by repaired score.
2. Watchlist appendix for attractive but blocked ideas.
3. Excluded list with reason.
4. Count of eligible ideas.
5. If fewer than 25 are eligible, say so and do not force weak ideas into the list.
6. CSV-ready rows updating source_issue_tracker.csv and scored_idea_database_repaired_2026_06_25.csv.

<rules>
Do not deep-dive the ideas.
Do not generate new ideas.
Do not include killed ideas.
Do not include placeholder ideas unless repaired.
Be strict.
</rules>
