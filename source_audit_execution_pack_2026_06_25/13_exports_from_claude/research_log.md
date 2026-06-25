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

## 2026-06-24 — Batch 03: Energy, Power, Grid, Data Centers & Climate Infrastructure

Prompt file used: prompts/01_source_corpus_300/03_batch_energy_power_grid_datacenters_45.md
Claude mode used: Research (advanced)
Project files used: source_whitelist.md, source_quality_policy.md, source_300_requirement.md, source_evidence_ledger.csv, source_corpus_batch_tracker.csv, research_log.md
Key outputs:
  - 50 net-new qualifying sources logged (EN-001..EN-050; 55 summarized, 5 overflow for dedupe margin)
  - Tier 1/2 ~84%, batch quality gate PASS (>=75%); Tier 3 = 16% (under 25% ceiling)
  - All 12 sub-topics covered; anchors: DOE, EIA, FERC, NERC, NREL, ORNL, PNNL, IEEE, IEA, IRENA, IAEA, UL, ASHRAE, OCP, ARPA-E
  - China energy cross-referenced to CN-025..CN-036 (not re-logged); US energy US-020/021/022, US-030/031, US-044 cross-referenced (not duplicated)
  - Key signals: IEA DC 485->950 TWh by 2030 (proj); NERC summer peak +224 GW 2026-35; OCP 800 VDC transition; DOE Earthshots/ARPA-E/VPP Liftoff; UL 9540A / IEEE 2800 standards layer
Files updated (to be applied locally by founder):
  - source_evidence_ledger.csv — append EN-001..EN-055
  - source_corpus_batch_tracker.csv — append BATCH_03 row
  - research_log.md — this entry
  - 01_sources/source_corpus_summaries/batch_03_energy_power_grid_datacenters_summary.md — new
New sources added: 50 counted (running corpus total: 145 toward 300; ~118 Tier 1, ~12 Tier 2, ~18 Tier 3 counted across all batches — confirm exact split on merge)
New ideas added: 0 (gated)
Ideas rejected: 0
Open questions:
  - Hold the 5 overflow rows (EN-051..EN-055) as count_toward_300=no, or keep all 50 + 5 as counted up to 50?
  - Top-up needed for HVDC primaries, immersion-cooling standard, and 2 NREL industrial-heat rows before any data-center power/cooling idea-gating
  - Reconcile IEA 945 vs 950 TWh 2030 figure and EIA 15 GW actual vs 18.2 GW forecast in later verification pass
Next action: Run prompts/01_source_corpus_300/04_batch_semiconductors_electronics_45.md (Batch 04, target 45 sources)

## 2026-06-24 — Batch 04: Semiconductors, Electronics, Packaging & Advanced Manufacturing

Prompt file used: prompts/01_source_corpus_300/04_batch_semiconductors_electronics_45.md
Claude mode used: Research (advanced); normal chat for ledger merge + this log update
Project files used: 00_admin/claude_project_instructions.md (governing), 01_sources/source_whitelist.md, source_quality_policy.md, source_300_requirement.md, source_evidence_ledger.csv, source_corpus_batch_tracker.csv, research_log.md
Key outputs:
  - 46 net-new qualifying sources logged (SC-001..SC-049; gap IDs SC-011/SC-018/SC-032 dropped in synthesis, no rows) + 3 company-claim rows (SC-C1 ASML, SC-C2 Wolfspeed, SC-C3 Navitas) logged as count_toward_300=no
  - Batch quality gate: MISS — Tier1+2 = 34/46 = 73.9% (below 75% gate); Tier 3 = 12/46 = 26.1% (above 25% ceiling)
  - CORRECTION: earlier in-session summary overstated this batch as 49 logged / 33 Tier 1 / 75.5% PASS; verified-on-merge figures are 46 logged / 30 Tier 1 / 4 Tier 2 / 12 Tier 3 / 73.9% (miss). Tracker and ledger reflect the corrected numbers.
  - Coverage: advanced packaging & hybrid bonding (ECTC/imec/ASME/SPIE), chiplets/UCIe, WBG power + JEDEC JC-70 reliability (GaN/SiC), near-junction & microchannel thermal, silicon photonics (imec iSiPP/UMC), HBM4 + SPHBM4 memory standards, high-NA EUV & equipment market (SEMI/WSTS/SIA), OSAT/industry structure (CSET/ITIF/TrendForce), materials chokepoints (photoresist/specialty gases), backside power delivery & CFET device scaling, NAPMP packaging policy (net-new primaries)
  - Cross-referenced, NOT re-logged: US-010/011/012/035/036/045 (CHIPS/NSTC/NAPMP), CN-010/011/012/013/046/047 (China semiconductors/OSAT)
Files updated (to be applied locally by founder):
  - source_evidence_ledger.csv — appended SC-001..SC-049 (46 counted) + SC-C1..SC-C3 (3 company, not counted); merged file now 199 data rows; 191 counted toward 300 (134 Tier 1, 33 Tier 2, 24 Tier 3)
  - source_corpus_batch_tracker.csv — append corrected BATCH_04 row (status: complete_below_quality_gate; 46/30/4/12; running total 191/300)
  - research_log.md — this entry
New sources added: 46 counted (running corpus total: 191 toward 300; whole-corpus Tier1/2 = 167/191 = ~87%, still well above the 230/300 final requirement despite this batch's per-batch miss)
New ideas added: 0 (gated)
Ideas rejected: 0
Open questions:
  - Resolve Batch 04 gate miss now via Tier-1 top-up (~3 sources -> 49 counted, ~75.5% Tier1/2, ~24.5% Tier 3): retire low-confidence vendor rows SC-047 (photoresist) and SC-048 (specialty gases); add a SEMI/SIA materials-share primary, IEDM 2024/2025 IEEE Xplore primaries (TSMC N2 GAA / CFET; imec CFET+BSPDN), and an HVDC/800 VDC distribution standards primary?
  - Or carry the marginal miss forward and clear it in the source dedupe/gap-fill audit (workflow step 3)?
  - Verify paywalled abstracts before idea-gating: SC-004 (Nature Electronics UCIe 3D SiP), SC-017 (Nature Electronics 3000 W/cm2), SC-044 (ASME hybrid-bonding review); confirm SPHBM4 (SC-026) status on formal release
  - Replace ASML/Wolfspeed/Navitas company-claim rows (SC-C1..C3) with independent technical corroboration where a top-ranked idea would otherwise lean on them
Next action: Resolve Batch 04 quality-gate miss (top-up or defer to audit), then run prompts/01_source_corpus_300/05_batch_ai_robotics_automation_low_altitude_40.md (Batch 05, target 40 sources)

## 2026-06-24 — Batch 05: AI, Robotics, Industrial Automation & Low-Altitude Economy

Prompt file used: prompts/01_source_corpus_300/05_batch_ai_robotics_automation_40.md; prompts/07_refresh_and_controls/02_session_export_package.md (export)
Claude mode used: Research (advanced) for Batch 05; normal chat for ledger merge + export
Project files used: 00_admin/claude_project_instructions.md (governing), 01_sources/source_whitelist.md, source_quality_policy.md, source_300_requirement.md, source_evidence_ledger.csv, source_corpus_batch_tracker.csv, research_log.md
Key outputs:
  - 46 net-new qualifying sources logged (AI-001..AI-046) + 1 company-claim row (AI-C1 EHang) logged count_toward_300=no
  - Batch quality gate: PASS — Tier1+2 = 44/46 = 95.7% (>=75% gate); Tier 3 = 2/46 = 4.3% (under 25% ceiling)
  - Per-row tier split 35 Tier 1 / 9 Tier 2 / 2 Tier 3; reconciles the in-session audit line (36 T1 / 8 T2) to the table-accurate 35/9 — Tier1+2 unchanged at 44, gate result unchanged
  - Coverage: AI governance (NIST AI RMF + AIRC + AI 100-1; OECD AI Principles 2024 + incident framework); benchmarks (MLPerf Inference v5.0/v5.1, MLPerf Tiny v1.3 + 2021 origin, TinyML->TinyDL survey); robot safety standards (ISO 10218-1/-2:2025, ISO/TS 15066, ISO 13482, IEC/ISO TR 5469 + TS 22440 WG, NIST SSM study); robot learning/embodied AI (RT-2 VLA, GR00T N1, foundation-model + sim2real surveys, SSM path-replanning); industrial robots (IFR World Robotics 2025 global + China + density); AI trends (Stanford HAI 2025 + 2026); China LAE + robotics policy (State Council/CMC UAV Interim Regs primary + MOJ Q&A; CAAC airspace classification + flight-service plan; NDRC LAE division; MIIT humanoid guidance via Jamestown/MERICS/CGTN); US BVLOS/UTM (FAA Part 108 NPRM; NASA UTM ConOps + flight tests); counter-UAS standardized evaluation
  - Cross-referenced, NOT re-logged: China LAE as "new quality productive force" in 2024 Government Work Report (CN-batch); US "Unleashing American Drone Dominance" EO Jun 2025 (US-batch); Made in China 2025 robotics designation (CN-batch)
Files updated (to be applied locally by founder):
  - source_evidence_ledger.csv — append AI-001..AI-046 + AI-C1 (47 rows); merged file now 246 data rows; 237 counted toward 300 (169 Tier 1, 42 Tier 2, 26 Tier 3)
  - source_corpus_batch_tracker.csv — append BATCH_05 row (status: complete; 46/35/9/2; running total 237/300)
  - research_log.md — this entry
New sources added: 46 counted (running corpus total: 237 toward 300; whole-corpus Tier1/2 = 211/237 = 89.0%)
New ideas added: 0 (gated)
Ideas rejected: 0
Open questions:
  - Upgrade AI-033 (CAAC airspace classification) from KWM secondary citation to canonical caac.gov.cn primary URL; fetch original MIIT Chinese-text humanoid-robot Guiding Opinions to replace reliance on Jamestown/MERICS/CGTN (AI-038/039/040); add standalone NIST/ASTM E54 robot test-method primaries
  - Add MLPerf Automotive v0.5 (AVCC+MLCommons, Aug 2025) and MLPerf Training rows in a follow-on top-up
  - Batch 04 gate miss (73.9% Tier1/2) still outstanding — resolve via Tier-1 top-up or clear in Step-3 dedupe/gap-fill audit
  - Treat all Chinese LAE market-size figures (RMB 1.5T 2025 / 3.5T 2035) as CAAC/state forecasts, not realized demand
Next action: Run prompts/01_source_corpus_300/06_batch_biomedical_medtech_35.md (Batch 06, target 35 sources) in a fresh chat

## 2026-06-24 — Batch 06: Biomedical, Medtech, Bio-instrumentation & Regulation

Prompt file used: prompts/01_source_corpus_300/06_batch_biomedical_medtech_35.md; prompts/07_refresh_and_controls/02_session_export_package.md (export)
Claude mode used: Research (advanced) for Batch 06; normal chat for ledger/tracker merge + export
Project files used: 00_admin/claude_project_instructions.md (governing), 01_sources/source_whitelist.md, source_quality_policy.md, source_300_requirement.md, source_evidence_ledger.csv, source_corpus_batch_tracker.csv, research_log.md
Key outputs:
  - 49 net-new qualifying sources logged (BM-001..BM-049) + 2 company-claim rows (BM-C1 Dexcom, BM-C2 Us2.ai) logged count_toward_300=no
  - Batch quality gate: PASS — Tier1+2 = 46/49 = 93.9% (>=75% gate); Tier 3 = 3/49 = 6.1% (under 25% ceiling); per-tier split 42 T1 / 4 T2 / 3 T3
  - Coverage: FDA AI-device landscape (1,451 cumulative through end-2025, 76% radiology, ~96% 510(k)); FDA PCCP final (Dec 2024) + draft all-device PCCP (Aug 2024); IMDRF SaMD (N12/N41/N81) + GMLP (N88, Jan 2025); EU MDR/IVDR transition + EUDAMED; WHO IVD prequalification; China NMPA green channel (104 devices/12 batches in 2025, Apr 2025 rules) + MERICS state-support; expedited pathways (Breakthrough 12.3% authorization rate; De Novo ~0.89% of 510(k) volume); bio-instrumentation primaries (wearable electrochemical/microneedle/regenerable sweat sensors, CGM head-to-head); surgical robotics (IDEAL framework, Science Robotics autonomy, R-TAMIS review); POC diagnostics + NIH POCTRN/RADx; lab automation workforce (1.4x chem / 3.7x serology) + ADLM staffing; reimbursement (first AI CPT 92229, Viz LVO NTAP)
  - Cross-referenced, NOT re-logged: none from CN-/US-/EN-/SC-/AI- batches; all 49 are net-new
Files updated (to be applied locally by founder):
  - source_evidence_ledger.csv — append BM-001..BM-049 + BM-C1/BM-C2; merged file now 297 data rows; 286 counted toward 300 (211 Tier 1, 46 Tier 2, 29 Tier 3)
  - source_corpus_batch_tracker.csv — append BATCH_06 row (status: complete; 49/42/4/3; running total 286/300)
  - research_log.md — this entry
  - 01_sources/source_corpus_summaries/batch_06_biomedical_medtech_summary.md — new (optional; the corpus report)
New sources added: 49 counted (running corpus total: 286 toward 300; whole-corpus Tier1/2 = 257/286 = 89.9%)
New ideas added: 0 (gated)
Ideas rejected: 0
Open questions:
  - Step-3 dedupe must resolve 5 pre-existing cross-batch duplicate URLs (CN-019/AI-039, CN-020/AI-040, CN-024/AI-037, US-016/AI-001, US-045/SC-014); collapsing nets 281 counted
  - Batch 04 gate miss (73.9% Tier1/2) still outstanding — resolve via Tier-1 top-up or clear in Step-3 audit
  - Top up Batch 06 thin spots with primaries: official NMPA/CMDE page (replace Tier 3 trackers BM-046/047); direct ISO/IEC standards citations (ISO 13485:2016, ISO 14971:2019, IEC 62304, ISO 10993 — currently synthesis-only); EMA/MDCG primary; CLSI + AAMI primaries (absent); fetch post-March-2026 FDA AI cumulative count from the FDA CSV (1,451 is the end-2025 figure)
  - Treat all paywalled abstracts (BM-025 Science Robotics, BM-035 NEJM AI) as verified-on-access before idea-gating
Next action: Run prompts/01_source_corpus_300/07_batch_extreme_advanced_manufacturing_35.md (Batch 07, target 35 sources) in a fresh chat; corpus is 286/300 — Batches 07–08 (target 35 each) should clear the 300 gate with margin before the Step-3 dedupe/synthesis.

## 2026-06-24 — Batch 07: Extreme Environments / Aerospace-adjacent / Nuclear-Fusion-Geothermal-Hydrogen / Advanced Materials

Prompt file used: prompts/01_source_corpus_300/07_batch_extreme_advanced_manufacturing_35.md; prompts/07_refresh_and_controls/02_session_export_package.md (export)
Claude mode used: Research (advanced) for Batch 07; normal chat for ledger/tracker merge + export
Project files used: 00_admin/claude_project_instructions.md (governing), 01_sources/source_whitelist.md, source_quality_policy.md, source_300_requirement.md, source_evidence_ledger.csv, source_corpus_batch_tracker.csv, research_log.md
Key outputs:
  - 44 net-new qualifying sources logged (EX-001..EX-044), all Tier 1 + 3 company-claim rows (EX-C1..EX-C3 patents) + 1 Tier-4 row (EX-T4-1 DRACO cancellation) logged count_toward_300=no
  - Batch quality gate: PASS — Tier1+2 = 44/44 = 100% (>=75% gate); Tier3 = 0% (under 25% ceiling)
  - New EX prefix introduced (no collision with CN/US/EN/SC/AI/BM); 9 duplicate/cross-ref/excluded clusters removed incl. 1 cross-ref to EN- batch (IRENA hydrogen-cost economics)
  - Coverage densest in fusion materials/components, nuclear fuels & ATF, rad-hard + high-temp electronics, advanced materials (UHTC/RHEA), hydrogen embrittlement; thin in standalone extreme-pressure metrology, supercritical-CO2 materials, non-fusion high-magnetic-field facilities
  - Whole-corpus counted total now 330 (255 Tier1 / 46 Tier2 / 29 Tier3 = 91.2% Tier1/2); 300-source floor, Tier1/2 floor, and Tier3 cap all clear on counted basis
Files updated:
  - source_evidence_ledger.csv (append EX-001..EX-044, EX-C1..EX-C3, EX-T4-1 — additive merge, 297 -> 345 rows)
  - source_corpus_batch_tracker.csv (append BATCH_07 row; 6 -> 7 rows)
  - research_log.md (this entry)
New sources added: 44 counted (running corpus total 330 toward 300)
New ideas added: 0 (gated)
Ideas rejected: 0
Open questions:
  - Run Batch 08 (customer/market/procurement, target 35) before the Batch 09 dedupe/gap-fill audit, or run the audit now since the counted floor (330) is already cleared?
  - Resolve in Batch 09: (a) Batch 04 quality-gate miss (73.9% Tier1/2); (b) collapse the 5 pre-existing cross-batch duplicate URLs (CN-019/AI-039, CN-020/AI-040, CN-024/AI-037, US-016/AI-001, US-045/SC-014) -> ~325 counted; (c) verify paywalled/abstract-only EX rows (EX-021 ACS, EX-022 Nature, EX-024 JECS); (d) confirm EX-044 Feb-2024 NIF yield is an estimate not a finalized measurement
  - Gap-fill thin EX sub-topics: standalone extreme-pressure sensors/metrology, supercritical-CO2 cycle materials, non-fusion high-magnetic-field (e.g. NHMFL), SiC/GaN as a power-device class
Next action: Run prompts/01_source_corpus_300/08_batch_customer_market_procurement_35.md (Batch 08, target 35) in a fresh chat; then prompts/01_source_corpus_300/09_dedupe_and_gap_fill_audit.md.
```

---

## Open questions (session-level)
1. **Sequencing:** proceed to Batch 08, or trigger the Batch 09 dedupe/gap-fill audit early given the counted floor is already met?
2. **Carry-forward debt for Batch 09:** Batch 04 gate miss; 5 cross-batch duplicate URLs; paywalled EX rows to verify; the NIF Feb-2024 estimate caveat.
3. **EX gap-fill targets:** the four thin sub-topics listed above (searches not run — `web_search` budget hit 18 calls).


## 8. Research log entry (ready to paste into `02_research_log/research_log.md`)

```text
## 2026-06-24 — Batch 08: Customer Pain / Procurement / Market Structure / Competitor / Public Filings

Prompt file used: prompts/01_source_corpus_300/08_batch_customer_market_procurement_35.md; prompts/07_refresh_and_controls/02_session_export_package.md (export)
Claude mode used: Research (advanced) for Batch 08; normal chat for ledger/tracker merge, cross-batch dedupe, and export
Project files used: 00_admin/claude_project_instructions.md (governing), 01_sources/source_whitelist.md, source_quality_policy.md, source_300_requirement.md, source_evidence_ledger.csv, source_corpus_batch_tracker.csv, research_log.md
Key outputs:
  - 41 counted qualifying sources logged (CM-prefix; new prefix, no collision) + 3 cross-reference rows (count=no) + 3 company-claim rows (count=no)
  - Batch quality gate: PASS — Tier1+2 = 39/41 = 95.1% (>=75% gate); Tier3 = 2/41 = 4.9% (under 25% ceiling)
  - Customer-concentration facts from SEC filings (Bloom 43%/13%/12% rising YoY; Methode 41%/10.9%; Willdan 27.4% + $1.0B backlog); procurement-vehicle map (DIU CSO/OT, FAR 6.302 sole-source, OSP-4 IDIQ Firefly $21.81M, HII OT->FAR $19M/$347M, DOE fusion milestone OTs); market-structure chokepoints (Besi 40%/74%; China SME 9.6% domestic demand 2023; US 50.4% share / China 24% demand)
  - Cross-batch dedupe caught 3 re-surfaced URLs already in corpus: CM-016=US-044, CM-017=EN-016, CM-027=AI-016 -> converted to count=no cross-references
Files updated (to be applied locally by founder):
  - source_evidence_ledger.csv — append CM-001..CM-044 + CM-C1..CM-C3 (3 of the CM rows are count=no cross-references); merged file now 392 data rows; 371 counted toward 300 (286 Tier1 / 54 Tier2 / 31 Tier3)
  - source_corpus_batch_tracker.csv — append BATCH_08 row (status complete; 41 counted; running total 371/300)
  - research_log.md — this entry
New sources added: 41 counted (running corpus total: 371 toward 300; whole-corpus Tier1/2 = 340/371 = 91.6%; Tier3 31 of 70 cap)
New ideas added: 0 (gated)
Ideas rejected: 0
Open questions:
  - Step-3 dedupe must still collapse 5 pre-existing cross-batch duplicate pairs (CN-019/AI-039, CN-020/AI-040, CN-024/AI-037, US-016/AI-001, US-045/SC-014); collapsing nets corpus to ~366 counted
  - Batch 04 quality-gate miss (73.9% Tier1/2, Tier3 over 25%) still outstanding from earlier — resolve via Tier-1 top-up or clear in Step-3 audit
  - Thin Batch 08 sub-topics for Step-3 gap-fill: explicit willingness-to-pay / price-point evidence (currently inferred from award $ values); documented vendor-dissatisfaction / switching signals (currently inferred from second-source/qualification language); a US biomedical-instrumentation 10-K with extracted customer/distributor concentration %; China customs/MOFCOM primary import-dependency line items (used Rhodium/USCC secondary instead)
  - Verify before idea-gating: SEC figures pulled via StockTitan/TradingView routes against EDGAR primaries; CSET OSAT shares (CM-035) are 2019-vintage — refresh against current TrendForce; SEMI $117.1B is a full-year ACTUAL, not the SEMI forecast figures
Next action: 300-source gate PASSES (371 counted, Tier1/2 91.6%, Tier3 under cap). Corpus collection complete — run prompts/01_source_corpus_300/09_dedupe_and_gap_fill_audit.md (Step-3) in a fresh chat to collapse the 5 cross-batch dupe pairs, resolve the Batch 04 gate miss, and gap-fill the four thin sub-topics, then proceed to 10_300_source_strategy_synthesis.md.
```

---

## Open questions & next action (summary)

**Open questions**
1. Collapse the 5 pre-existing cross-batch duplicate pairs in Step-3 (nets corpus to ~366 counted).
2. Resolve the outstanding Batch 04 quality-gate miss (Tier-1 top-up or clear in Step-3).
3. Gap-fill the four thin Batch 08 sub-topics (willingness-to-pay; vendor-switching; US medtech concentration %; China customs primaries).
4. Verify aggregator-sourced SEC figures against EDGAR; refresh the 2019-vintage CSET OSAT shares; keep SEMI actuals vs forecasts distinct.

**Next action:** The 300-source gate is **PASS**. Collection is complete — proceed to **Step-3** (`09_dedupe_and_gap_fill_audit.md`) in a fresh chat, then **strategy synthesis** (`10_300_source_strategy_synthesis.md`).


### Research log entry (paste into `02_research_log/research_log.md`)

```text
## 2026-06-24 — Batch 09: Step-3 Dedupe & Gap-Fill Audit (+ gap-fill collection)

Prompt file used: prompts/01_source_corpus_300/09_dedupe_and_gap_fill_audit.md; prompts/07_refresh_and_controls/02_session_export_package.md (export)
Claude mode used: direct file audit (pandas on uploaded ledger/tracker) for dedupe; Research (advanced) for gap-fill collection
Project files used: 00_admin/claude_project_instructions.md (governing), 01_sources/source_300_requirement.md, source_evidence_ledger.csv, source_corpus_batch_tracker.csv, research_log.md
Key outputs:
  - PHASE 1 dedupe: collapsed the 5 pre-existing cross-batch exact-URL dup pairs (CN-019/AI-039, CN-020/AI-040, CN-024/AI-037, US-016/AI-001, US-045/SC-014); full URL/DOI/title sweep found no other dups; post-collapse = 366 counted; gate PASS
  - PHASE 2 gap-fill: +31 counted Tier-1/2 sources across SC (+11), EX (+12), CM (+8); CM-053 logged count=no (dup filing)
  - SC batch lifted 73.3% -> 78.6% Tier1/2 (clears 75% per-batch gate); EX 100%; CM 95.9%
  - FINAL CORPUS: 424 ledger rows; 397 counted (313 T1 / 54 T2 / 30 T3 / 0 T4 = 92.4% Tier1/2; Tier3 30 of 70); 27 not counted
  - GATE PASS on all six criteria; Ready for strategy synthesis = YES
Files updated:
  - source_evidence_ledger.csv (5 demotions + 32 appended rows -> 424 rows / 397 counted)
  - source_corpus_batch_tracker.csv (BATCH_04/07/08 revised; BATCH_04 status -> complete; BATCH_09 corpus row = 397)
  - research_log.md (this entry)
  - session_2026-06-24_batch09_dedupe_and_gapfill.md (this memo)
New sources added: 31 counted (gap-fill); corpus 366 -> 397
New ideas added: 0 (gated)
Ideas rejected: 0
Open questions:
  - Backfill 38 legacy blank `limitations` fields (BM x28, CN x10)?
  - CM-051: pull a specific gsaAdvantage line-item unit price next pass
  - Legacy tracker-vs-ledger tier drift (~7 rows); ledger parse authoritative
  - Verify-on-access: paywalled journal rows + IR/aggregator SEC route (CM-048) vs EDGAR
Next action: Gate PASSES. Re-upload the two updated CSVs to Project Files, then run prompts/01_source_corpus_300/10_300_source_strategy_synthesis.md in a fresh chat.
```

## 2026-06-25 — 07b: Source-Audit Remediation (Phase 16 repair)

Prompt file used: prompts/04_diligence_scoring/02b_apply_source_audit_remediation.md; prompts/07_refresh_and_controls/02g_update_export_package.md (export)
Claude mode used: Research (advanced) for source verification; normal chat for packaging and file generation
Project files used: 00_admin/claude_project_instructions.md (governing), 01_sources/source_whitelist.md, source_quality_policy.md, source_quality_policy_addendum_scoring_audit.md, 01_score_filtered_ideas.md, 02_diversity_filter_70_90.md, 01_raw_idea_generation_120.md, source_evidence_ledger.csv, source_issue_tracker.csv
Key outputs:
  - Applied all 11 remediations (ISSUE-001..ISSUE-015). Eligibility: 19 eligible for top-25 deep dive (1 CLEARED = RID-053; 18 CLEARED_WITH_WEAKNESS), 30 blocked (24 HOLD = 16 placeholders + 8 drone RIDs; 4 KILL = RID-036/041/042/045; 2 NEEDS_MORE_SOURCE = RID-087/091).
  - Citation fixes verified: SCORE-010 first author = Djassemi et al. (ACS Sensors 2026 11(2):1413-1424, DOI 10.1021/acssensors.5c03699; Wang is senior author); SCORE-015 Awad = 2024 (Surg Endosc 38(10):6193-6202), Servais 2025 confirmed (39(2):1217-1226).
  - Relabels: OCP/Deschutes -> Tier 2 industry-consortium/product-spec (specs 2MW/500GPM/80-90psi/3C verified via OCP Deschutes 5.0 + vendor pages + ARPA-E deck); NVIDIA "-30%" -> company-supported (GB300 dev blog, LITEON, internal Megatron test); CFS "$8M" = DOE-validated milestone, "largest" -> company-supported (no DOE primary); da Vinci "43%" -> preclinical/Intuitive-supported.
  - HBM4: replaced 36Kr (Tier 4) with JEDEC JESD270-4 + Semiconductor Engineering; 720->775um confirmed -> hybrid bonding postponed -> RID-042 kill locked (industry trending to 825-900um for HBM4E/HBM5).
  - Humanoid BOM: deleted misattributed "Morgan Stanley 56%" (the 56% = China share of MS Humanoid 100 universe, not actuator BOM); kept McKinsey 40-60% + BofA 40-50%.
  - SCORE-004D geography reversal: CELEX:52025DC0005 is a non-binding EU IPI report describing CHINA's Document 551 (25-100% localization; 100% for 137/178 categories); binding follow-on is Reg (EU) 2025/1197 (supplier-exclusion measure). RID-087/091 stay policy-context-only.
  - Policy triggers confirmed non-final: FAA Part 108 (FR 2026-01644; no final rule as of 2026-06-25); BIS FR 2026-00789 (active/volatile); USTR Section 301 SiC (rate TBD, announce ~2027-05-24).
Files updated:
  - source_issue_tracker.csv — REPLACE 15 rows (status -> CLEARED / CLEARED_WITH_WEAKNESS / HOLD / KILL_STANDS / WATCH / NEEDS_MORE_SOURCE; next_prompt routed to 02c/02d/02e)
  - source_evidence_ledger.csv — APPEND 9 scoring-evidence rows SCORE-001/002/004/010/013/015/016/004D + new SCORE-013-DOE (all count_toward_300=no; corpus counted total unchanged at 397). Ledger now 433 data rows.
  - scored_idea_database_repaired_2026_06_25.csv — NEW FILE, 49 affected rows (new_score=old_score, delta=0; numerical re-score deferred to 02e)
  - 07b_source_audit_remediation.md — substantive 02b output (repair + evidence-label tables, blocked/eligible lists)
  - policy_trigger_watchlist.csv — 6 provisional trigger rows seeded (finalize in 02d)
  - research_log.md — this entry
New sources added: 0 to the 300-corpus (9 scoring-evidence rows logged count_toward_300=no); 1 provisional new scoring source located (SCORE-013-DOE)
New ideas added: 0 (hard rule)
Ideas rejected: 0 new (4 prior Phase-16 kills confirmed with strengthened rationale: RID-036/041/042/045)
Open questions:
  - 02e: apply downward score adjustments where flagged (SCORE-002 cluster; surgical SCORE-015/da Vinci cluster; CFS "largest"); RID-053 needs no penalty.
  - Find a DOE.gov primary page asserting the CFS "$8M / largest" figure to upgrade ISSUE-007 confidence.
  - Strict-reviewer call: route RID-077/081/088 to HOLD pending clinical-outcome data rather than CLEARED_WITH_WEAKNESS? Flagged for 02e.
  - RID-051 is a borderline admit (thin evidence); confirm a direct spec or downgrade in 02e.
Next action: Run prompts/04_diligence_scoring/02c_placeholder_source_repair.md (07c) in a fresh chat to attempt >=1 direct Tier 1/2 source per the 16 placeholder RIDs; prioritize the three currently scored "pursue" (RID-111, RID-016, RID-100). Then 02d (policy-trigger watchlist) -> 02e (targeted re-score) -> 02f (top-25 eligibility gate). Do not run deep dives until the 02f gate clears.

## 2026-06-25 — 07c: Placeholder Source Repair (ISSUE-014 resolution)

Prompt file used: prompts/04_diligence_scoring/02c_placeholder_source_repair.md; prompts/07_refresh_and_controls/02g_update_export_package.md (export)
Claude mode used: Research (advanced) for the 16-RID source search; normal chat for packaging and file generation
Project files used: 00_admin/claude_project_instructions.md (governing), 01_sources/source_whitelist.md, source_quality_policy.md, source_quality_policy_addendum_scoring_audit.md, 01_score_filtered_ideas.md, 01_raw_idea_generation_120.md, source_evidence_ledger.csv, source_issue_tracker.csv, scored_idea_database_repaired_2026_06_25.csv
Key outputs:
  - Resolved the umbrella ISSUE-014 (16 placeholder RIDs lacking direct Tier 1/2 support). Result: 8 CLEARED, 7 CLEARED_WITH_WEAKNESS, 1 HOLD (RID-094).
  - All three priority "pursue" RIDs cleared on direct Tier 1 evidence: RID-111 (Sci Rep 2022 nanopositioning bandwidth-resonance tradeoff + hybrid-bonding 0.2um-at-3sigma placement spec, US Patent 12438117), RID-016 (China MIIT echelon-utilization 梯次利用 specification + UL 1974 + NREL fy22osti/84527), RID-100 (Photonics 12(8):821 2025 active-alignment packaging bottleneck; corroborated arXiv 2112.14357 "packaging up to 80% of cost").
  - Final-law / final-standard drivers confirmed (finality test passed): RID-020 (UL 9540A + NFPA 855:2026 §9.7.6.6 TRPP), RID-040 (Directive (EU) 2023/1791 Art. 26.6 + German EnEfG §11(2), effective 1 Jul 2026), RID-017 (GB/T 44265-2024), RID-032 (ISO 15118-20:2022).
  - Other clears: RID-015 (Sandia/DOE G3P3 >700C, 6h storage, AIP 10.1063/5.0029216), RID-012 (IEA Energy-and-AI 2026/2025 onsite-power-from-grid-scarcity + LBNL "Queued Up 2025"), RID-082 (Front. Neurosci. 2023 implant power/longevity, 3-5yr DBS battery), RID-026 (NREL UNIFI TP-5D00-89269 + FERC Order 2023), RID-022 (IEEE 2030.10-2021 + DOE OE), RID-097 (TGV ultrashort-pulse laser micromachining, JMPT 2025), RID-101 (JOM 2018 + ORNL OSTI 1273151 molten-salt corrosion), RID-099 (Nature Electronics 2018 + NIST overlay, sub-1nm).
  - RID-094 HOLD: NIST AM-Bench / 2026 in-situ metrology roadmap is a genuine Tier 1 source, but the RID is a prior kill and collides with the project's aversion to diagnostic/testing/monitoring overproduction; no standalone procurement/standards driver found, so not force-cleared (routed back to 02c).
Files updated:
  - source_issue_tracker.csv — REPLACE the umbrella ISSUE-014 row with 16 per-RID rows ISSUE-014-111 ... ISSUE-014-099 (status CLEARED / CLEARED_WITH_WEAKNESS / HOLD; next_prompt 02e for cleared, 02c for RID-094). Tracker now 30 data rows.
  - source_evidence_ledger.csv — APPEND 15 placeholder-repair rows PH-001..PH-015 (all count_toward_300=no; one row per cleared RID; no row for HOLD RID-094). Ledger now 448 data rows; counted corpus total unchanged at 397.
  - scored_idea_database_repaired_2026_06_25.csv — UPDATE the 16 placeholder rows: evidence_status, top25_eligible (yes for the 15 cleared, no for RID-094), repair_notes, and source_issue_ids. new_score = old_score, delta = 0, decision letters unchanged (numerical re-score deferred to 02e).
  - research_log.md — this entry.
New sources added: 0 to the 300-corpus (15 placeholder-repair rows logged count_toward_300=no; counted total stays 397)
New ideas added: 0 (hard rule)
Ideas rejected: 0 new (RID-094 remains HOLD, not a new kill; prior RID-094 kill rationale stands)
Open questions:
  - 02e: re-test RID-099 against the testing/monitoring-overproduction filter (it nearly went HOLD with RID-094); discount RID-101 if the deep-dive horizon is strictly <=2030; confirm RID-026 is a hardware controller, not a software/consulting play; confirm RID-040's target geography is EU (driver is EU/Germany-bounded).
  - RID-094: revisit only if a procurement document, standard, or regulator requirement emerges that demands AM in-situ NDE as a standalone purchased capability decoupled from generic monitoring.
  - PH-010 caveat carried forward: IEA onsite-gas/battery figures are 2030 projections; LBNL "Queued Up" explicitly excludes behind-the-meter projects (supports the scarcity half of RID-012, IEA carries the BTM-solution half).
Next action: Run prompts/04_diligence_scoring/02d_policy_trigger_watchlist.md (07d) in a fresh chat to finalize policy_trigger_watchlist.csv (full 11-column schema; seed rows from 07b), then 02e (targeted re-score of all CLEARED / CLEARED_WITH_WEAKNESS RIDs) -> 02f (top-25 eligibility gate). Do not run deep dives until the 02f gate clears.

## 2026-06-25 — 07d: Policy-Trigger Watchlist Finalization (ISSUE-010/011/012/013 close-out)

Prompt file used: prompts/04_diligence_scoring/02d_policy_trigger_watchlist.md; prompts/07_refresh_and_controls/02g_update_export_package.md (export)
Claude mode used: Research (advanced) for the 8-trigger current-status verification; normal chat for packaging and file generation
Project files used: 00_admin/claude_project_instructions.md (governing), 01_sources/source_whitelist.md, source_quality_policy.md, source_quality_policy_addendum_scoring_audit.md, source_issue_tracker.csv, policy_trigger_watchlist.csv, scored_idea_database_repaired_2026_06_25.csv, source_evidence_ledger.csv
Key outputs:
  - Finalized policy_trigger_watchlist.csv to the full 11-column schema; 7 provisional 07b rows verified + 1 new row added (TRIG-008 FDA/organ-on-chip -> RID-086). Watchlist now 8 trigger rows.
  - Verified all 8 triggers against official primary sources as of 2026-06-25; NONE has fired:
    - TRIG-001 FAA Part 108 BVLOS: NOT final (FR 2026-01644 reopen closed 2026-02-11; EO 2026-02-01 deadline passed unmet) -> speculative / high
    - TRIG-002 AI OVERWATCH Act: NOT enacted (H.R.6875 HFAC 42-2-1 2026-01-21; S.4456 2026-05-04; WH opposition) -> speculative / high
    - TRIG-003 BIS FR 2026-00789: in force & UNCHANGED (no rescind/tighten) -> active / high
    - TRIG-004 USTR Sec.301 SiC: rate unannounced (0% now; rises 2027-06-23; announce ~2027-05-24; FR 2025-23912) -> speculative / high
    - TRIG-005 NRL RID-036 award: NOT verifiable (NOI N00173-25-RFI-MF18 only; DARPA HR001123C0121 only verifiable prime; HigherGov "2026-03-23" paywalled) -> speculative / medium
    - TRIG-006 da Vinci powered RCT: NOT met (NCT07247175 randomized but endpoints = traction force & path length, not patient outcomes; NCT06879912 observational) -> speculative / high
    - TRIG-007 HBM D2W hybrid bonding: NO near-term pull; postponement reinforced (JESD270-4 775um; HBM4E ~825-900um press; HBM5 hybrid bonding ~2029-2030) -> speculative / high
    - TRIG-008 FDA OoC: advancing not binding (draft NAM guidance FR 2026-05390 2026-03-18, comments closed 2026-05-18; S.355 Senate UC 2025-12-16; H.R.2821 House E&C) -> active / high
  - Controlled-status note: TRIG-003 mapped to "active" (policy in force & monitored) rather than "enacted" to avoid implying the watched event (a rescission/tightening) has fired; the underlying rule IS enacted/effective. Documented for audit.
  - No re-score performed (deferred to 02e). No new corpus-300 sources. No new ideas. No new kills (RID-036/041/042 kills stand).
Files updated:
  - policy_trigger_watchlist.csv — REWRITE to 8 finalized rows (TRIG-001..008), 11-col schema, verified current_status / current_confidence / status as of 2026-06-25.
  - source_issue_tracker.csv — UPDATE the four 02d-routed rows (ISSUE-010/011/012/013) to WATCHLISTED (TRIG-001/003/004/005), next_prompt 02d; APPEND ISSUE-016 (AI-OVERWATCH -> TRIG-002) and ISSUE-017 (FDA-OOC -> TRIG-008, RID-086), both status WATCH. Tracker now 32 data rows.
  - source_evidence_ledger.csv — APPEND 8 policy-trigger monitoring rows PT-001..PT-008 (all count_toward_300=no). Ledger now 456 data rows; counted corpus total UNCHANGED at 397.
  - research_log.md — this entry (this consolidated file also merges the previously-pending 07b and 07c entries).
New sources added: 0 to the 300-corpus (8 policy-trigger rows logged count_toward_300=no; counted total stays 397)
New ideas added: 0 (hard rule)
Ideas rejected: 0 new (RID-036/041/042 kills stand; no trigger fired to revive them)
Open questions:
  - 02e: re-score all CLEARED / CLEARED_WITH_WEAKNESS RIDs (drone RIDs stay capped/HOLD under TRIG-001; compute/China-fab RIDs keep export-risk cap under TRIG-003/002).
  - RID-086: elevated watch under TRIG-008 — revisit decision only on a FINAL FDA NAM guidance or enacted Mod Act 3.0 (not draft/committee).
  - TRIG-005: re-poll USAspending/FPDS for an N00173-series PIID (UEI E14VYCEW9YG8); treat absence as inconclusive pending DoD ingest lag.
  - TRIG-007: NVIDIA Rubin/Feynman requirements or Samsung 16-Hi HBM4 yield ramp could pull hybrid bonding earlier — monitor.
Next action: Re-upload the four updated files to Project Files, then run prompts/04_diligence_scoring/02e_targeted_rescore_affected_ideas.md (02e) in a fresh chat (targeted re-score of all CLEARED / CLEARED_WITH_WEAKNESS RIDs) -> 02f (top-25 eligibility gate). Do not run deep dives until the 02f gate clears.
