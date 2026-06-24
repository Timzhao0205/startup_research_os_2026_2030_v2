<task>
Deduplicate and audit the 300+ source corpus.
</task>

<context>
I have run the 8 source-corpus batch prompts. Use `source_evidence_ledger.csv` and `source_corpus_batch_tracker.csv` from Project Files or attached files. Do not generate startup ideas yet.
</context>

<requirements>
The strategy corpus must contain at least:
- 300 unique qualifying sources;
- at least 230 Tier 1 or Tier 2 sources;
- no more than 70 Tier 3 sources counted toward the 300;
- zero Tier 4 sources counted toward the 300.
</requirements>

<dedupe_rules>
Deduplicate by URL, DOI, title, report name, preprint/final-paper overlap, and press-release mirrors. If multiple sources support the same claim, keep the highest-quality source and mark others as supporting/secondary.
</dedupe_rules>

<deliverable>
Produce:
1. Corpus count summary.
2. Tier count summary.
3. Sources excluded from the 300 count and why.
4. Duplicate groups found.
5. Evidence gaps by domain.
6. Whether the 300-source gate passes.
7. If the gate fails, generate gap-fill search prompts with exact source targets by domain.
8. Updated CSV-ready rows or corrections for `source_evidence_ledger.csv`.
9. Updated row for `source_corpus_batch_tracker.csv` if needed.

<final_gate_format>
End with exactly this checklist:
- 300-source gate: PASS/FAIL
- Tier 1/2 count: PASS/FAIL
- Tier 3 cap: PASS/FAIL
- Tier 4 excluded: PASS/FAIL
- Duplicates removed: PASS/FAIL
- Evidence ledger populated: PASS/FAIL
- Ready for strategy synthesis: YES/NO
</final_gate_format>

<rules>
Do not generate startup ideas unless Ready for strategy synthesis is YES.
</rules>
