# File Update Protocol

## After every Claude session

Ask Claude to generate a session export package with:

1. Markdown memo.
2. CSV-ready rows for relevant CSV files.
3. Evidence ledger rows.
4. Rejected idea entries, if relevant.
5. Research log entry.
6. Open questions and next actions.

## Manual local update

1. Save Markdown memo into the correct folder.
2. Append CSV rows into the correct CSV.
3. Save the files locally.
4. Re-upload changed files to Claude Project Files.
5. Start the next phase in a new chat.

## Files to refresh most often in Claude Project Files

- `03_evidence_ledgers/source_evidence_ledger.csv`
- `03_evidence_ledgers/source_corpus_batch_tracker.csv`
- `04_opportunity_clusters/opportunity_clusters.csv`
- `05_raw_idea_database/raw_idea_database.csv`
- `06_scored_idea_database/scored_idea_database.csv`
- `12_rejected_ideas/rejected_ideas.md`
- latest top deep-dive memos
- latest red-team memos
- latest R&D pilot plans

## Snapshot principle

Treat uploaded Markdown, TXT, CSV, and XLSX files as snapshots unless the Claude UI clearly indicates live Drive syncing.
