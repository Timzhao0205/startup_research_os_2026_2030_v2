# Claude Settings Checklist for Source-Audit Repair

Use this before each repair chat.

## Project
- Use your existing Project: `Startup Research OS 2026–2030`
- Do not create a new Project.

## Model / mode
- Use the strongest Claude model available to you.
- Turn on Web Search.
- Turn on Research for:
  - 02b source-audit remediation
  - 02c placeholder source repair
  - 02d policy-trigger watchlist
  - 02e targeted re-score

## Files to upload or refresh before 07b
Core:
- source_whitelist.md
- source_quality_policy.md
- source_quality_policy_addendum_scoring_audit.md
- scoring_rubric.md
- founder_profile.md
- project_charter.md

Current outputs:
- 01_score_filtered_ideas(1).md or 01_score_filtered_ideas.md
- 02_diversity_filter_70_90(1).md or 02_diversity_filter_70_90.md
- 01_raw_idea_generation_120(1).md or 01_raw_idea_generation_120.md
- source_evidence_ledger.csv
- source_corpus_batch_tracker.csv

Repair files:
- source_issue_tracker.csv
- policy_trigger_watchlist.csv
- scored_idea_database_repaired_2026_06_25.csv

## Important toggles / behavior
- Do not use ordinary chat without Web Search for source repair.
- Ask Claude to produce CSV-ready rows after every repair chat.
- Start a fresh chat for each prompt:
  - 07b Source Audit Remediation
  - 07c Placeholder Source Repair
  - 07d Policy Trigger Watchlist
  - 07e Targeted Re-score
  - 07f Top-25 Eligibility Gate

## Stop condition
If Claude cannot find direct Tier 1/2 support for a placeholder RID, the RID stays HOLD. Do not let Claude substitute a weak market report or company page.
