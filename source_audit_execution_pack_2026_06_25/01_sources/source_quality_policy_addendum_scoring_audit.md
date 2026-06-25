# Source Quality Policy Addendum — Scoring Audit Repair

This addendum applies after the Phase 16 scoring source audit.

## Hard gates

No idea enters top-25 deep dive unless its source status is one of:
- CLEARED
- CLEARED_WITH_WEAKNESS

These statuses are not eligible for top-25 deep dive:
- HOLD
- NEEDS_MORE_SOURCE
- KILL
- REGULATORY_SPECULATION if the core thesis depends on the speculative trigger
- POLICY_CONTEXT_ONLY if no buyer, procurement, budget, or direct customer pain source exists

## Evidence-label rules

1. OCP / Project Deschutes evidence:
   - Label as industry-consortium / OCP product-spec evidence.
   - Do not label as peer-reviewed, government, or fully independent Tier 1 evidence.
   - It can support product/spec claims such as 2MW, 500 GPM, 80 PSI, and 3°C ATD if directly stated by OCP or OCP-listed product pages.

2. arXiv evidence:
   - Label as preprint.
   - It can support technical hypothesis and early technical evidence.
   - It cannot be treated as peer-reviewed proof unless published elsewhere.

3. Company claims:
   - NVIDIA “up to 30%” claims, Intuitive da Vinci “43%,” and CFS “$8M/largest” claims must be explicitly labeled as company-supported unless independently verified by a primary non-company source.
   - Company claims can support product-existence and company-claimed performance, but not independent market pain, clinical outcome, or official policy fact.

4. Policy triggers:
   - Proposed rules, NPRMs, reopened comment periods, bills, and hearings are not final law.
   - FAA Part 108 remains regulatory speculation until a final Federal Register rule exists.
   - AI OVERWATCH Act remains a bill until enacted.
   - USTR Section 301 future semiconductor/SiC rate remains unknown until USTR announces the rate.
   - BIS FR 2026-00789 is active policy evidence, but must remain on watchlist because export-control policy can change quickly.

5. Placeholder RIDs:
   - Any RID with placeholder evidence is HOLD until at least one direct Tier 1/2 source supports its core claim.
   - Market-size/TAM sources cannot satisfy the source requirement by themselves.
   - Tier 3 sources can triangulate but cannot clear the placeholder gate alone.

6. Kill discipline:
   - RID-036 and RID-042 remain killed unless a specific trigger changes:
     - RID-036: executed NRL contract appears in USAspending/FPDS/SAM.gov.
     - RID-042: strong 2029-relevant direct demand for D2W hybrid bonding returns, e.g. JEDEC/HBM roadmap changes or credible HBM5 pull.
