<task>
Deep-dive the top eligible ideas after source-audit repair.
</task>

<inputs>
Use:
- scored_idea_database_repaired_2026_06_25.csv
- source_issue_tracker.csv
- source_evidence_ledger.csv
- policy_trigger_watchlist.csv
- source_whitelist.md
- source_quality_policy.md
- source_quality_policy_addendum_scoring_audit.md
</inputs>

<eligibility_gate>
Only include ideas whose status is:
- CLEARED
- CLEARED_WITH_WEAKNESS

Exclude:
- HOLD
- NEEDS_MORE_SOURCE
- KILL
- REGULATORY_SPECULATION if the core thesis depends on the speculative trigger
- POLICY_CONTEXT_ONLY if no buyer/procurement/budget/direct customer pain exists

Drone RIDs whose core thesis depends on FAA Part 108 finalization may only appear in a watchlist appendix, not in the top-25 core list.
</eligibility_gate>

<for_each_top_idea>
Analyze:
1. Problem.
2. First product.
3. First customer and buyer.
4. Why customer pain is severe.
5. Existing solution and why it fails.
6. Product architecture.
7. Hardware stack.
8. Software stack.
9. Data requirements.
10. Control/sensing/actuation loop, if applicable.
11. Prototype plan.
12. TRL now and TRL by 2029.
13. Capex estimate.
14. China market wedge.
15. US expansion path.
16. Regulatory issues.
17. Export-control issues.
18. Supply-chain dependencies.
19. Incumbents and startups.
20. Defensibility.
21. Failure modes.
22. Kill criteria.
23. Evidence strength.
24. Remaining evidence weaknesses from source_issue_tracker.csv.
</for_each_top_idea>

<source_requirements>
Every core deep-dive idea must include:
- at least one technical source;
- at least one customer/industry/procurement/source of pain;
- at least one policy/regulatory/standards source where relevant.

Company claims must be labeled.
Preprints must be labeled.
Market reports must be triangulation only.
Policy context must not be treated as direct customer pain unless linked to procurement, regulation, or budget.
</source_requirements>

<deliverable>
Produce:
1. Top eligible idea list.
2. One-page memo for each.
3. Comparison matrix.
4. Watchlist appendix for attractive but blocked ideas.
5. Ideas excluded because of source-audit status.
6. CSV-ready evidence ledger rows for any new sources.
7. Updated source_issue_tracker rows if any issue remains open.
8. Recommendation for top 12 after deep dives.

<rules>
Do not include unsupported placeholder ideas.
Do not include killed ideas.
Do not upgrade speculative regulatory triggers.
Be strict.
</rules>
