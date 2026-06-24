<task>
Perform a macro policy and timing scan for startup opportunities that could be launched in 2029/2030.
</task>


<source_requirements>
Use Project files `01_sources/source_whitelist.md`, `01_sources/source_quality_policy.md`, and `01_sources/source_300_requirement.md`.
Prioritize Tier 1 and Tier 2 sources. Tier 3 may be used for market timing and triangulation. Tier 4 may be logged as weak signals but must not count toward the 300-source requirement.
Use domain-targeted `site:` queries where practical.
Do not cite company marketing as independent evidence; label it as company claim.
Do not treat market growth as customer pain.
For every major claim, cite sources and distinguish fact, inference, and speculation.
</source_requirements>


<gate>
Use the completed 300-source corpus if available. If the 300-source gate has not passed, say so and perform only a provisional scan.
</gate>

<research_questions>
1. What China policy priorities from 2026–2030 create startup opportunities?
2. What US policy priorities from 2026–2030 create startup opportunities?
3. What China/US tensions create opportunities or risks?
4. Which sectors have policy tailwinds but also export-control or regulatory risks?
5. Which sectors are likely to mature technically by 2029/2030?
6. Which sectors are overhyped or crowded?
</research_questions>

<domains>
Energy, grid, power electronics, data centers, semiconductors, advanced packaging, industrial automation, robotics, low-altitude economy, AI infrastructure, biomedical devices, biotech tools, advanced manufacturing, aerospace-adjacent systems, climate adaptation, sensors, high-reliability control systems, extreme-environment systems.
</domains>

<deliverable>
Produce a table with 15–25 macro opportunity clusters.

Columns:
- Cluster
- Why it matters for 2029/2030
- China policy/timing signal
- US policy/timing signal
- Technical maturity signal
- Supply-chain signal
- Export-control/regulatory risk
- High-end niche customer examples
- Source IDs
- Source tier mix
- Confidence

Also produce CSV-ready rows for `opportunity_clusters.csv` and `source_evidence_ledger.csv`.
</deliverable>
