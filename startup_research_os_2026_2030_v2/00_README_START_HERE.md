# Startup Research OS 2026–2030 — Local Folder Pack

This folder is designed for a Claude Project using **Markdown + CSV**, without converting files into Google Docs or Google Sheets.

## Goal

Build an evidence-controlled, 300+ source, multi-year deep-tech startup opportunity research system for a possible 2029/2030 launch.

## Operating model

```text
Local folder = durable memory
Claude Project = AI workspace
Markdown files = memos and instructions
CSV files = databases
Prompts folder = executable Claude research tasks
source_whitelist.md = preferred domain list
source_quality_policy.md = source hierarchy and enforcement rules
source_evidence_ledger.csv = truth-control layer
```

## Minimal manual copy-paste

Most prompts are stored as files. In Claude, attach the relevant prompt file and type only:

```text
Execute the attached prompt exactly. Use the Project knowledge files when referenced. Use Research and Web Search if the prompt requires them.
```

The only unavoidable manual step may be the Claude Project instruction field. To avoid a long copy-paste, paste this one-line instruction into the Project instructions field:

```text
Use the uploaded Project file `00_admin/claude_project_instructions.md` as the governing instruction set for this Project; follow it unless I explicitly override it in a chat.
```

Then upload `00_admin/claude_project_instructions.md` into Project Files.

## Setup steps

1. Unzip this folder locally.
2. Create a Claude Project named:

```text
Startup Research OS 2026–2030
```

3. Paste the one-line Project instruction above into Claude's Project instruction field.
4. Upload these files into Claude Project Files:

```text
00_admin/claude_project_instructions.md
00_admin/project_charter.md
00_admin/founder_profile.md
00_admin/scoring_rubric.md
00_admin/file_update_protocol.md
01_sources/source_whitelist.md
01_sources/source_quality_policy.md
01_sources/source_300_requirement.md
03_evidence_ledgers/source_evidence_ledger.csv
03_evidence_ledgers/source_corpus_batch_tracker.csv
04_opportunity_clusters/opportunity_clusters.csv
05_raw_idea_database/raw_idea_database.csv
06_scored_idea_database/scored_idea_database.csv
12_rejected_ideas/rejected_ideas.md
```

5. Turn on Claude **Web Search** and **Research** for deep-research chats.
6. Start with the setup audit prompt:

```text
prompts/00_setup/00_setup_audit.md
```

7. Then run the 300-source corpus prompts in order:

```text
prompts/01_source_corpus_300/01_batch_china_policy_40.md
prompts/01_source_corpus_300/02_batch_us_policy_export_40.md
prompts/01_source_corpus_300/03_batch_energy_power_grid_datacenters_45.md
prompts/01_source_corpus_300/04_batch_semiconductors_electronics_45.md
prompts/01_source_corpus_300/05_batch_ai_robotics_automation_40.md
prompts/01_source_corpus_300/06_batch_biomedical_medtech_35.md
prompts/01_source_corpus_300/07_batch_extreme_advanced_manufacturing_35.md
prompts/01_source_corpus_300/08_batch_customer_market_procurement_35.md
prompts/01_source_corpus_300/09_dedupe_and_gap_fill_audit.md
prompts/01_source_corpus_300/10_300_source_strategy_synthesis.md
```

8. Only after the 300-source corpus is complete, run opportunity scans and idea generation.

## The 300-source rule

Claude must not generate the final strategy until it has built or ingested a source corpus with at least:

```text
300 unique qualifying sources
At least 230 Tier 1 or Tier 2 sources
No more than 70 Tier 3 sources counted toward the 300
Tier 4 sources do not count toward the 300
Every source logged in source_evidence_ledger.csv
Every batch deduplicated by URL/DOI/title
```

## File refresh rule

After every major Claude session:

1. Ask Claude to create a session export package.
2. Save the Markdown memo into the appropriate folder.
3. Save or append CSV rows into the relevant CSV.
4. Re-upload updated CSV/Markdown files to Claude Project Files.
5. Begin the next phase in a new chat.

## Suggested chat sequence

```text
00 Setup Audit
01 Source Corpus Batch 1 — China Policy
02 Source Corpus Batch 2 — US Policy and Export Controls
03 Source Corpus Batch 3 — Energy / Power / Grid / Data Centers
04 Source Corpus Batch 4 — Semiconductors / Electronics / Advanced Manufacturing
05 Source Corpus Batch 5 — AI / Robotics / Automation
06 Source Corpus Batch 6 — Biomedical / Medtech / Bio-instrumentation
07 Source Corpus Batch 7 — Extreme / Advanced Manufacturing / Aerospace-adjacent
08 Source Corpus Batch 8 — Customer / Market / Procurement
09 Source Corpus Dedupe and Gap Fill
10 300-Source Strategy Synthesis
11 Macro Policy Scan
12 Technical Bottleneck Scan
13 Customer Pain Scan
14 Raw Idea Generation
15 Diversity Filter
16 Scoring
17 Source Audit
18 Top 25 Deep Dives
19 Top 12 Red Team
20 R&D Pilot Portfolio
21 Quarterly Refreshes
```
