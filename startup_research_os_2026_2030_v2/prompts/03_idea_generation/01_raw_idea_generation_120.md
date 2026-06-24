<task>
Generate a raw universe of at least 120 startup ideas based on the completed 300-source corpus, macro scan, technical bottleneck scan, and customer-pain scan.
</task>

<input_files>
Use:
- source_evidence_ledger.csv
- opportunity_clusters.csv
- technical bottleneck scan output if provided
- customer-pain scan output if provided
- source_whitelist.md
- source_quality_policy.md
- source_300_requirement.md
</input_files>

<gate_requirement>
If the 300-source gate has not passed, clearly label the idea generation as provisional. Prefer not to generate final-ranked ideas until the gate passes.
</gate_requirement>

<constraints>
- Do not score yet.
- Do not over-index on my PhD topic.
- Do not rely on Stanford IP.
- At least 80 ideas must be standalone products/platforms/components/subsystems, not diagnostics or test tools.
- No more than 25 ideas may be mainly diagnostics, test, inspection, monitoring, or characterization.
- At least 40 ideas must be outside semiconductors, GaN, WBG, fusion, and cleanroom devices.
- At least 25 ideas should be China-first or China-early.
- At least 25 ideas should have a credible US expansion path.
- At least 25 should have near-zero cleanroom dependency.
- At least 20 should be weird, high-end, niche, extreme-performance opportunities.
- At least 15 should be biomedical/health/bio-instrumentation.
- At least 20 should be AI/robotics/industrial automation.
- At least 20 should be energy/power/grid/data-center/industrial-energy.
- At least 20 should be semiconductor/electronics/hardware-subsystem.
</constraints>

<idea_definition>
Each idea must include:
- specific first product;
- specific first customer;
- specific customer pain;
- standalone functionality;
- hardware/software integration;
- extreme-performance angle;
- China wedge;
- US wedge;
- 2026–2028 R&D pilot path;
- 2029/2030 launch thesis;
- why now;
- likely failure reason;
- source IDs.
</idea_definition>

<deliverable>
Produce a table of at least 120 raw ideas.
Also produce CSV-ready rows for `raw_idea_database.csv`.
</deliverable>
