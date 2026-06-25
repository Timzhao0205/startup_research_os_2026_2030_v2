# Source-Audit Execution Pack — 2026-06-25

Use this pack after running `prompts/04_diligence_scoring/02_source_audit_after_scoring.md`.

Your state:
- 300-source corpus is complete. Do not rebuild it.
- Raw idea generation is complete. Do not rerun it.
- Diversity filter is complete. Do not rerun it.
- Scoring is complete, but the scoring evidence needs repair before deep dives.

Sequence:
1. Upload/refresh the files in this pack into your Claude Project.
2. Run `02b_apply_source_audit_remediation.md`.
3. Run `02c_placeholder_source_repair.md`.
4. Run `02d_policy_trigger_watchlist.md`.
5. Run `02e_targeted_rescore_affected_ideas.md`.
6. Run `02f_top25_eligibility_gate.md`.
7. Only after the gate clears, run `01a_top25_deep_dive_after_source_repair.md`.

Execution command for Claude:
`Execute the attached prompt exactly. Use Research and Web Search. Use Project files when referenced. Do not merely summarize the prompt; perform the task. Do not proceed to deep dives unless the prompt explicitly says the deep-dive gate is cleared.`

Local-file discipline:
- Treat your current scoring output as a baseline snapshot.
- Write repaired scores to `scored_idea_database_repaired_2026_06_25.csv`.
- Do not edit raw idea definitions unless a source repair changes the actual idea.
- Re-upload `source_issue_tracker.csv`, `source_evidence_ledger.csv`, and repaired scored database after each repair chat.
