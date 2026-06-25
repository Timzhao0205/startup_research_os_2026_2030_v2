<task>
Create a live policy-trigger watchlist for the scored portfolio.
</task>

<context>
The source audit identified several policy/regulatory triggers that would change scores:
1. FAA publishes the Part 108 final rule in the Federal Register.
2. AI OVERWATCH Act is enacted.
3. BIS rescinds or tightens Federal Register 2026-00789.
4. USTR announces the post-June-23-2027 Section 301 semiconductor/SiC tariff rate.
5. An executed NRL contract appears in USAspending / FPDS / SAM.gov for RID-036.
6. da Vinci force-feedback evidence is upgraded by a powered clinical-outcomes randomized controlled trial.
7. JEDEC/HBM roadmap changes revive 2029-relevant hybrid-bonding demand.
8. FDA / organ-on-chip regulatory changes materially improve RID-086 or related biomedical-platform timelines.

Use:
- source_issue_tracker.csv
- policy_trigger_watchlist.csv
- scored_idea_database_repaired_2026_06_25.csv if available
- source_evidence_ledger.csv
- source_whitelist.md
- source_quality_policy.md
</context>

<deliverable>
Produce a policy-trigger table with columns:
- trigger_id
- trigger
- current status
- official source to monitor
- affected RIDs
- score fields affected
- what changes if trigger fires
- current confidence
- refresh cadence
- exact search query to run quarterly
- status: speculative / active / enacted / resolved

Also produce CSV-ready updated rows for policy_trigger_watchlist.csv and source_issue_tracker.csv.

<rules>
Use official sources first:
- Federal Register
- FAA
- BIS
- Congress.gov
- USTR
- DOE
- USAspending
- FPDS / SAM.gov
- FDA
- ClinicalTrials.gov
- PubMed
- JEDEC / IEEE / SEMI where relevant

Do not treat proposed rules as final.
Do not treat bills as enacted.
Do not treat company claims as clinical evidence.
Do not generate startup ideas.
</rules>
