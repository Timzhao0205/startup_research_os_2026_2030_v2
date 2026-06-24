<task>
Build source corpus batch: AI, robotics, industrial automation, low-altitude economy.
</task>

<context>
This is one batch in a staged 300+ source deep-tech startup strategy corpus. Do not generate startup ideas yet. Your job is to find, screen, summarize, and log high-quality sources.
</context>


<source_requirements>
Use Project files `01_sources/source_whitelist.md`, `01_sources/source_quality_policy.md`, and `01_sources/source_300_requirement.md`.
Prioritize Tier 1 and Tier 2 sources. Tier 3 may be used for market timing and triangulation. Tier 4 may be logged as weak signals but must not count toward the 300-source requirement.
Use domain-targeted `site:` queries where practical.
Do not cite company marketing as independent evidence; label it as company claim.
Do not treat market growth as customer pain.
For every major claim, cite sources and distinguish fact, inference, and speculation.
</source_requirements>


<batch_target>
Batch ID: BATCH_05_AI_ROBOTICS_AUTOMATION
Topic: AI, robotics, industrial automation, low-altitude economy
Minimum qualifying sources for this batch: 40
</batch_target>

<focus>

Focus on IEEE, ACM, arXiv/OpenReview as early signal, NeurIPS/ICML/ICLR, CVPR, ICRA/IROS/RSS, NIST AI RMF, OECD AI, Stanford HAI, MLCommons, official Chinese low-altitude/robotics policy, industrial automation sources.

Topics: embodied AI, industrial robots, robot learning, safety certification, edge AI, high-reliability embedded AI, factory automation, low-altitude economy infrastructure, drones, inspection/autonomy if tied to standalone functionality, real-time control, simulation-to-real.

</focus>

<quality_gate>
A source counts only if it is Tier 1, Tier 2, or approved Tier 3, is unique, and directly supports at least one useful claim. Tier 4 may be logged separately but does not count toward the target.
At least 75% of counted sources in this batch should be Tier 1 or Tier 2 unless impossible; if impossible, explain why.
</quality_gate>

<method>
1. Create a source-gated search plan using whitelist domains and `site:` queries.
2. Search and collect candidate sources.
3. Exclude weak, duplicate, SEO, scraper, or marketing-only pages.
4. Summarize each qualifying source.
5. Create CSV-ready rows for `source_evidence_ledger.csv`.
6. Create one CSV-ready row for `source_corpus_batch_tracker.csv`.
</method>

<deliverable>
Produce:
1. Source-gated search plan.
2. Qualifying source table with at least 40 sources.
3. Excluded source table, if applicable.
4. CSV-ready rows for `source_evidence_ledger.csv` using this exact column order:
source_id,batch_id,date_accessed,source_title,source_url_or_citation,domain,source_tier,source_type,publication_date,geography,topic,claim_supported,evidence_note,confidence,limitations,access_level,count_toward_300,used_in_idea_ids,notes
5. CSV-ready row for `source_corpus_batch_tracker.csv` using this exact column order:
batch_id,batch_name,target_qualifying_sources,qualifying_sources_logged,tier1_count,tier2_count,tier3_count,tier4_count_not_counted,duplicate_count_removed,status,date_completed,notes
6. Batch source-quality audit.
</deliverable>

<rules>
- Do not generate startup ideas.
- Do not count Tier 4 sources toward the target.
- Do not count sources you cannot summarize substantively.
- Do not count duplicated reports or mirrored press releases twice.
- Use citations in the memo portion.
</rules>
