# 300-Source Strategy Requirement

## Core requirement

Before final strategy synthesis or top opportunity ranking, Claude must build or ingest a source corpus with at least:

```text
300 unique qualifying sources
At least 230 Tier 1 or Tier 2 sources
No more than 70 approved Tier 3 sources counted toward the 300
Tier 4 sources excluded from the 300 count
Every counted source logged in source_evidence_ledger.csv
```

## Source-batch plan

| Batch | Topic | Minimum qualifying sources |
|---|---:|---:|
| 1 | China policy, industrial strategy, standards, regulation | 40 |
| 2 | US policy, funding, export controls, standards, regulation | 40 |
| 3 | Energy, power, grid, data centers, climate infrastructure | 45 |
| 4 | Semiconductors, electronics, packaging, advanced manufacturing | 45 |
| 5 | AI, robotics, industrial automation, low-altitude economy | 40 |
| 6 | Biomedical, medtech, bio-instrumentation, regulation | 35 |
| 7 | Extreme environments, aerospace-adjacent, nuclear/fusion/geothermal/hydrogen, advanced materials | 35 |
| 8 | Customer pain, procurement, market structure, competitor and public-filing evidence | 35 |
| **Total target** |  | **315** |

The target is 315 so that after deduplication the remaining corpus should still exceed 300.

## What counts as “go through” a source

A source counts only when Claude provides:

- source title;
- URL/DOI/citation;
- publication date or access date;
- source tier;
- source type;
- geography;
- topic;
- 1–3 claims supported;
- 2–4 sentence summary or evidence note;
- limitations;
- confidence rating.

## Deduplication rules

Deduplicate by:

1. exact URL;
2. DOI;
3. same report mirrored on multiple domains;
4. same press release republished by newswires;
5. same paper preprint and final version, unless both contain materially different information.

## Gaps after dedupe

If the deduped corpus has fewer than 300 qualifying sources, Claude must generate a gap-fill source plan and continue source collection before strategy synthesis.

## Strategy gating rule

Claude must not produce final top opportunities or final recommendations until the source corpus audit says:

```text
300-source gate: PASS
Tier 1/2 count: PASS
Tier 3 cap: PASS
Tier 4 excluded: PASS
Duplicates removed: PASS
Evidence ledger populated: PASS
```
