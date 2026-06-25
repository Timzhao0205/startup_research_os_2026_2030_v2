<task>
Apply the source-audit remediation recommendations to the scored 79-idea portfolio.
</task>

<context>
The scoring output has already been generated. Do not regenerate the raw idea database. Do not run top-25 deep dives yet.

Use these Project files:
- 01_score_filtered_ideas(1).md or 01_score_filtered_ideas.md
- 02_diversity_filter_70_90(1).md or 02_diversity_filter_70_90.md
- source_evidence_ledger.csv
- source_issue_tracker.csv
- source_whitelist.md
- source_quality_policy.md
- source_quality_policy_addendum_scoring_audit.md

The source audit produced these mandatory recommendations:
1. Re-tier SCORE-001 to Tier 2 and SCORE-002 to Tier 2/Tier 3 where appropriate. Strip the Tier 1 label from OCP and arXiv-bundle evidence.
2. Re-label NVIDIA “−30%,” CFS “largest-in-program,” and da Vinci “43%” as company-supported / preclinical / non-independent evidence unless stronger primary sources are found.
3. Replace the 36Kr HBM4 citation.
4. Reconcile humanoid actuator BOM evidence to McKinsey 40–60% and delete the unverified “56%/Morgan Stanley” attribution unless the original Morgan Stanley source is found.
5. Fix citation metadata: SCORE-010 author should be “Djassemi et al.” and SCORE-015 Awad year must be verified/corrected.
6. Verify the Project Deschutes 2MW / 500 GPM / 80–90 psi / 3C numbers using published OCP or product-spec evidence.
7. Obtain a DOE primary source for the CFS $8M and “largest” claim; if no DOE source is found, label it as CFS company-supported only.
8. Keep RID-036 and RID-042 kills unless direct evidence changes them.
9. Keep all drone RIDs at regulatory-speculation because FAA Part 108 is not final.
10. Keep RID-087 and RID-091 customer pain as policy-context-only unless direct buyer/procurement/budget evidence is found.
11. Treat RID-111, RID-016, RID-100, RID-015, RID-026, RID-020, RID-040, RID-017, RID-032, RID-012, RID-022, RID-097, RID-082, RID-101, RID-094, and RID-099 as unsupported until each has at least one direct Tier 1/2 source.
</context>

<source_rules>
Use source_whitelist.md, source_quality_policy.md, and source_quality_policy_addendum_scoring_audit.md.
Use Research and Web Search.
Prefer official, standards, peer-reviewed, national-lab, industry-association, public-filing, procurement, or high-quality technical sources.
Company pages may be used only as company claims.
Trade journalism may be used only as Tier 3 triangulation unless source_quality_policy.md says otherwise.
Do not cite weak sources if higher-quality sources exist.
Do not invent citations.
</source_rules>

<deliverable>
Produce:
1. A repair table with columns:
   - issue_id
   - affected SCORE/RID
   - original problem
   - corrected source tier
   - corrected claim wording
   - corrected confidence
   - score impact: none / small / medium / large
   - decision impact: pursue / watch / kill / hold
   - citations
   - status: CLEARED / CLEARED_WITH_WEAKNESS / HOLD / KILL / NEEDS_MORE_SOURCE

2. A corrected evidence-label table for:
   - OCP / Project Deschutes
   - NVIDIA -30%
   - CFS $8M/largest
   - da Vinci 43%
   - HBM4 microbump/hybrid-bonding postponement
   - humanoid actuator BOM cost
   - FAA Part 108
   - BIS 2026-00789
   - USTR Section 301 SiC/semiconductor tariff trigger
   - NRL/Laser Thermal procurement
   - RID-087/RID-091 policy-context-only customer pain

3. Corrected rows for source_issue_tracker.csv.

4. Corrected rows for source_evidence_ledger.csv.

5. Corrected rows for scored_idea_database_repaired_2026_06_25.csv only for affected ideas.

6. A list of ideas blocked from top-25 deep dive.

7. A list of ideas allowed into top-25 deep dive.

<rules>
Do not generate new startup ideas.
Do not deep-dive any idea.
Do not rewrite the entire scoring table unless necessary.
Be strict.
If evidence is company-supported only, say so and reduce confidence.
If evidence is policy-context-only, say so and cap score contribution.
If evidence is preprint-only, label it as preprint and reduce certainty.
</rules>
