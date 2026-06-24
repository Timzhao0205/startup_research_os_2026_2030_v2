# Research Log

Use this file as the chronological index of all Claude research sessions.

## Entry template

```text
## YYYY-MM-DD — [Chat Title]

Prompt file used:
Claude mode used: Research / Web Search / normal chat
Project files used:
Key outputs:
Files updated:
New sources added:
New ideas added:
Ideas rejected:
Open questions:
Next action:
```
## 2026-06-24 — Setup Audit + Batch 01 China Policy Corpus

Prompt file used: 00_setup/00_setup_audit.md; 01_source_corpus_300/01_batch_china_policy_40.md; 01_source_corpus_300/02_batch_us_policy_export_40.md (failed); 07_refresh_and_controls/02_session_export_package.md
Claude mode used: Research (advanced) for Batch 01; normal chat for setup audit and export
Project files used: all 00_admin/, all 01_sources/ policy files, the five core CSVs, rejected_ideas.md
Key outputs:
  - Setup audit: PASS overall, 3 non-blocking hygiene fixes recommended
  - Batch 01 China policy: 50 qualifying sources, Tier1+2 = 82%, gate PASS — full artifact produced
  - Batch 02 US policy: FAILED (tool-not-found error), no output
Files updated (to be applied locally by founder):
  - source_evidence_ledger.csv — append 50 rows CN-001..CN-050
  - source_corpus_batch_tracker.csv — append BATCH_01 (complete) + BATCH_02 (not_started) rows
  - research_log.md — this entry
New sources added: 50 (China policy batch)
New ideas added: 0 (correct — pre-gate)
Ideas rejected: 0
Open questions:
  - Apply the 3 setup hygiene fixes to claude_project_instructions.md before continuing?
  - Wire two-stage anti-bias enforcement into governing instructions now vs. leave reactive?
Next action: Re-run Batch 02 (US policy / export controls) in a fresh chat; then Batches 03–08.

## 2026-06-24 — Batch 02: US Policy & Export Controls

Prompt file used: prompts/01_source_corpus_300/02_batch_us_policy_export_40.md
Claude mode used: Research
Project files used: source_whitelist.md, source_quality_policy.md, source_300_requirement.md, source_evidence_ledger.csv, source_corpus_batch_tracker.csv
Key outputs:
  - 45 qualifying sources logged (US-001 to US-045), 95.6% Tier 1/2
  - Batch quality gate PASS (>=75% Tier 1/2)
  - Identified major 2025-2026 policy shifts: AI Diffusion Rule rescinded; Natcast NSTC award voided (NIST assumes ops); SBIR/STTR reauthorized through FY2031; Section 301 semiconductor tariff; H200/MI325X moved to case-by-case licensing
Files updated:
  - source_evidence_ledger.csv (append US-001..US-045)
  - source_corpus_batch_tracker.csv (append BATCH_02 row)
  - research_log.md (this entry)
New sources added: 45 (running corpus total: 95 toward 300; 73 Tier 1, 20 Tier 2, 2 Tier 3 counted)
New ideas added: 0 (gated)
Ideas rejected: 0
Open questions:
  - Verify H200/MI325X thresholds + 25% tariff directly in Federal Register (currently medium confidence)
  - Add 3 discrete standards top-up rows next pass: NIST CHIPS Metrology Program; NIST.CHIPS.1000 grand challenges; NAPMP first-NOFO Federal Register notice
  - Watch for BIS AI-diffusion replacement rule and OSTP biosecurity replacement policy
Next action: Run prompts/01_source_corpus_300/03_batch_energy_power_grid_datacenters_45.md (Batch 03, target 45 sources)

