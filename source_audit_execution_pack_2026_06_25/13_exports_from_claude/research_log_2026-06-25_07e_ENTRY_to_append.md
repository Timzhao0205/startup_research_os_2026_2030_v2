## 2026-06-25 — 07e: Targeted Re-Score of Affected Ideas (ISSUE-001..017 score application)

Prompt file used: prompts/04_diligence_scoring/02e_targeted_rescore_affected_ideas.md
Claude mode used: Normal chat (deterministic re-score + file packaging). No research/search performed — the evidence basis was fully gathered in 07b–07d; 02e operates only on Project files (the re-score is a computation over the audit findings, not new evidence collection).
Project files used: 00_admin/claude_project_instructions.md (governing), 00_admin/scoring_rubric.md (13-criterion / 100-pt rubric), source_quality_policy_addendum_scoring_audit.md (hard gates + evidence-label rules), final/01_score_filtered_ideas.md (original sub-scores + rationale), scored_idea_database_repaired_2026_06_25.csv (canonical 49 affected rows), source_issue_tracker.csv, policy_trigger_watchlist.csv, source_evidence_ledger.csv
Key outputs:
  - Re-scored all 49 audit-affected ideas against the rubric using the anchor new_score = published old_score + Σ(category deltas) (sub-scores are NOT re-summed; published total column is authoritative). 28 ideas lost points; total −41 points; no score rose. Arithmetic verified (new = old + delta, 0 mismatches).
  - Category aggregate of the −41: Pain/WTP −22 (OCP Tier1→Tier2 re-tiering + NVIDIA/CFS company-claim relabels), Reg/export-inverse −14 (speculative FAA Part 108 trigger across the drone cluster), TRL −2 (RID-101 molten-salt >2030), Niche-wedge −1 (RID-102), Standalone-value −1 (RID-026), China-wedge −1 (RID-040).
  - Decision changes: 1 — RID-067 (detect-and-avoid) P→W (core thesis gated by NPRM-only Part 108).
  - Evidence-status changes: 3 — RID-077 CLEARED_WITH_WEAKNESS→HOLD; RID-099 CLEARED_WITH_WEAKNESS→HOLD; RID-071 HOLD→KILL.
  - Eligibility changes: 2 — RID-077 and RID-099 (yes→no). Eligible deep-dive pool = 32 (was 33 provisional).
  - JUDGMENT CALL #1 (surgical force-feedback): standalone console RID-077 → HOLD (its displacement-of-Intuitive thesis is an implicit clinical-outcome claim that preclinical/Intuitive-funded evidence + surrogate-endpoint trial NCT07247175 cannot support, per addendum evidence-rule 3); subsystem plays RID-081/088 kept CLEARED_WITH_WEAKNESS (−1 PW each), clinical-outcome gate deferred to 02f. Reversible — flagged for override (defer all three to 02f) if preferred.
  - JUDGMENT CALL #2 (RID-099): re-tested against the diagnostic/metrology-overproduction hard filter → HOLD, consistent with RID-094 (standalone metrology instrument, no non-diagnostic function, no procurement/standards driver). Reversible — flagged for override if extreme-precision dimensional/overlay metrology is treated as distinct from generic monitoring.
  - Locked kills confirmed: RID-036 (NRL award unverifiable; TRIG-005), RID-041, RID-042 (JEDEC JESD270-4 775µm; hybrid bonding postponed >2029; TRIG-007), RID-045 — all stay KILL/ineligible. RID-094 stays HOLD. RID-087/091 stay NEEDS_MORE_SOURCE (pain policy-context-only, Doc 551).
  - RID-053 (humanoid actuator): no penalty (Morgan Stanley "56%" misattribution removed; 40–60% actuation-BOM holds on McKinsey + BofA). Stays the only CLEARED pursue in its cluster.
  - Tally among the 49 affected (new): decisions P15 / W26 / K8; evidence-status CLEARED_WITH_WEAKNESS 23 / CLEARED 9 / HOLD 10 / KILL 5 / NEEDS_MORE_SOURCE 2; eligible yes 32 / no 17. (Only the 49 affected ideas were re-scored; the other 30 portfolio ideas keep their original decisions.)
Files updated:
  - scored_idea_database_repaired_2026_06_25.csv — RE-SCORE in place: new_score / score_delta / new_decision / evidence_status / top25_eligible updated for all 49 rows; 02e rationale appended to repair_notes (prefixed " | 02e:"). 12 cols, CRLF/no-BOM, 49 data rows.
  - source_issue_tracker.csv — advance all 25 issues with next_prompt=02e to next_prompt=02f (append "RESCORED_02E"); set ISSUE-014-099 current_status/status → HOLD; record the surgical HOLD call (ISSUE-008/005), the RID-099 HOLD (ISSUE-014-099), and the drone caps + RID-071 KILL (ISSUE-010). 32 data rows, CRLF/no-BOM.
  - 07e_targeted_rescore.md — substantive 02e output covering deliverables #1–8 (before/after table; deltas by rubric category; decision changes; top-25 eligibility; CSV-ready rows; blocked list; eligible list of 32; final summary + the two open judgment calls).
  - research_log.md — this entry.
New sources added: 0 to the 300-corpus (no new evidence collected in 02e; counted total stays 397). No source_evidence_ledger.csv change.
New ideas added: 0 (hard rule)
Ideas rejected: 0 new (RID-036/041/042/045 kills stand; RID-071 hardened HOLD→KILL on a pre-existing permanent reason, not a new kill; RID-077/099/094 are HOLD, not kills)
Open questions:
  - 02f: resolve the two flagged judgment calls — (a) surgical cluster RID-077/081/088 (HOLD-the-console vs defer-all-three); (b) RID-099 metrology filter (HOLD vs defer-as-weakness).
  - 02f confirm-or-kill priority: RID-051 (weakest admit — thin evidence, borders in-line metrology; needs a direct purchased-capability spec or it should be killed).
  - 02f: confirm RID-115 is a functional current-sense component (not a standalone diagnostic instrument); confirm RID-026 is a HW/SW controller (not integration/consulting).
  - Carried watch flags: RID-040 geography (EU/Germany-bounded driver, weak China wedge); RID-101 timing (deployment largely >2030); RID-012 (IEA figures are 2030 projections, borders integration).
  - Drone cluster (RID-067/068/069/070/072/074/112) revisits only on a FINAL FAA Part 108 Federal Register rule (TRIG-001); RID-094 revisits only on a procurement/standard demanding AM in-situ NDE as a purchased capability.
Next action: Re-upload the two corrected files (scored_idea_database_repaired_2026_06_25.csv, source_issue_tracker.csv) to Project Files, then run prompts/04_diligence_scoring/02f_top25_eligibility_gate.md (02f) in a fresh chat against the 32-idea eligible pool. Do not run deep dives until the 02f gate clears.
