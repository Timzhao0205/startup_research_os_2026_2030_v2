<task>
Repair the 16 unsupported placeholder RIDs before deep dives.
</task>

<context>
The source audit says these RIDs are unsupported and require at least one direct Tier 1/2 citation before any deep dive:

RID-111
RID-016
RID-100
RID-015
RID-026
RID-020
RID-040
RID-017
RID-032
RID-012
RID-022
RID-097
RID-082
RID-101
RID-094
RID-099

Use these Project files:
- 01_score_filtered_ideas(1).md or 01_score_filtered_ideas.md
- 01_raw_idea_generation_120(1).md or 01_raw_idea_generation_120.md
- source_evidence_ledger.csv
- source_issue_tracker.csv
- source_whitelist.md
- source_quality_policy.md
- source_quality_policy_addendum_scoring_audit.md
</context>

<source_requirements>
For each RID:
1. Identify the core claim that needs support.
2. Search for at least one direct Tier 1/2 source that supports the customer pain, technical bottleneck, regulatory driver, procurement driver, or standards trigger.
3. Prefer official government, standards, national lab, peer-reviewed, industry association, procurement, public filing, or regulator sources.
4. Do not use company marketing as the sole support.
5. Do not use market-size/TAM as pain evidence.
6. If no direct Tier 1/2 source is found, mark the RID as HOLD.
</source_requirements>

<deliverable>
Produce a table with columns:
- RID
- idea name
- original claim needing support
- best Tier 1/2 source found
- source tier
- source type
- exact claim supported
- confidence
- whether the source directly supports the idea
- status: CLEARED / CLEARED_WITH_WEAKNESS / HOLD
- whether it may enter top-25 deep dive
- CSV-ready source_evidence_ledger rows
- CSV-ready source_issue_tracker rows

<rules>
Use Research and Web Search.
Use source_whitelist.md and source_quality_policy.md.
Do not invent citations.
Do not use weak source substitution.
If evidence is insufficient, keep the idea on HOLD.
Do not generate new startup ideas.
Do not deep-dive the ideas.
</rules>
