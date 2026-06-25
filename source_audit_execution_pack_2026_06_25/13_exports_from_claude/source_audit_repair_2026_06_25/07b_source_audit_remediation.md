# Session Export — 07b: Source-Audit Remediation (Phase 16 repair)

**Date:** 2026-06-25
**Prompt:** `prompts/04_diligence_scoring/02b_apply_source_audit_remediation.md` (+ `prompts/07_refresh_and_controls/02g_update_export_package.md` for this export)
**Mode:** Research (advanced) for source verification; normal chat for packaging
**Hard-rule status:** Evidence remediation + deep-dive eligibility gating only — **no new ideas, no deep dives, no numerical re-scoring** (re-score is deferred to 02e per the pack sequence).

---

## 1. What this session did

Applied the 11 mandatory source-audit recommendations (ISSUE-001…ISSUE-015) to the scored 79-idea portfolio: re-tiered OCP/Deschutes from Tier 1 to Tier 2 industry-consortium/product-spec; relabeled NVIDIA "−30%," CFS "largest," and da Vinci "43%" as company-supported/preclinical; replaced the 36Kr (Tier 4) HBM4 citation with JEDEC JESD270-4 + Semiconductor Engineering; deleted the misattributed "Morgan Stanley 56% actuator BOM" and kept McKinsey 40–60%; corrected SCORE-010 author (→ Djassemi et al.) and SCORE-015 year (Awad → 2024); and set top-25 deep-dive eligibility per the addendum gate. Two findings changed the evidence base: SCORE-004D was geography-reversed (the "EU 25–100% target" is actually **China's Document 551**, described in a non-binding EU report), and the HBM4 720→775 µm height relaxation confirms hybrid bonding is **postponed**, locking the RID-042 kill. The full repair tables and evidence-label table live in the chat artifact "Source-Audit Remediation — 79-Idea Deep-Tech Portfolio (Prompt 02b)" → save as `07b_source_audit_remediation.md`.

## 2. Repair outcome (49 affected ideas)

| Evidence status | Count | Ideas |
|---|---:|---|
| CLEARED | 1 | RID-053 |
| CLEARED_WITH_WEAKNESS | 18 | RID-001,002,003,005,008,009,024,029,030,033,034,115 (data-center power/cooling); RID-102,104 (fusion); RID-077,081,088 (surgical force-feedback); RID-051 (warpage) |
| HOLD | 24 | 16 placeholders (RID-111,016,100,015,026,020,040,017,032,012,022,097,082,101,094,099) + 8 drone RIDs (RID-067,068,069,070,071,072,074,112) |
| KILL | 4 | RID-036, RID-041, RID-042, RID-045 |
| NEEDS_MORE_SOURCE | 2 | RID-087, RID-091 |
| **Eligible for top-25 deep dive** | **19** | 1 CLEARED + 18 CLEARED_WITH_WEAKNESS |
| **Blocked from deep dive** | **30** | 24 HOLD + 4 KILL + 2 NEEDS_MORE_SOURCE |

## 3. Deliverables produced (and where they go)

| Deliverable | Destination | Status |
|---|---|---|
| Repair table + evidence-label table (02b output) | chat artifact → `07b_source_audit_remediation.md` | done |
| Issue-tracker corrections (15 rows) | `03_evidence_ledgers/source_issue_tracker.csv` | replace — see §4 |
| Evidence-ledger corrections (8 edits + 1 new) | `03_evidence_ledgers/source_evidence_ledger.csv` | edit/append — see §5 |
| Repaired scored rows (49 affected) | `06_scored_idea_database/scored_idea_database_repaired_2026_06_25.csv` | new file — see §6 |
| Policy-trigger rows | `policy_trigger_watchlist.csv` | provisional only; finalize in 02d — see §7 |
| rejected_ideas.md entries | `12_rejected_ideas/rejected_ideas.md` | no new rejections — see §8 |
| Research-log entry | `02_research_log/research_log.md` | append — see §9 |

## 4. CSV-ready rows — `source_issue_tracker.csv` (REPLACE all 15 rows)

```
issue_id,item_id,item_type,affected_rids,issue_summary,current_status,required_action,required_source_tier,confidence_after_repair,next_prompt,status,notes
ISSUE-001,SCORE-001,score_evidence,RID-001;RID-002;RID-003;RID-008;RID-033,OCP/Deschutes over-tiered as Tier 1,REPAIRED,Re-tiered OCP to Tier 2 industry-consortium/product-spec,Tier2/industry-consortium,medium,02e,CLEARED_WITH_WEAKNESS,OCP Diablo/Deschutes specs + OCP vendor listings; pain corroborated
ISSUE-002,SCORE-002,score_evidence,RID-002;RID-009;RID-029;RID-030;RID-024,arXiv-bundle + NVIDIA -30% over-credited,REPAIRED,Labeled arXiv preprint + NVIDIA company-claim,Tier2/3+company-claim,medium,02e,CLEARED_WITH_WEAKNESS,arXiv:2508.14318/2508.16457 preprints; NVIDIA blog; NERC corroborates oscillation pain
ISSUE-003,SCORE-004,score_evidence,RID-053,Actuator BOM figure,REPAIRED,Deleted MS 56%; kept McKinsey 40-60%,Tier2,high,02e,CLEARED,McKinsey 40-60% + BofA 40-50%; 56% was China-company-share misattribution
ISSUE-004,SCORE-010,citation_fix,RID-078;RID-080,Author correction,REPAIRED,Corrected to Djassemi et al.,Tier1,high,02e,CLEARED,ACS Sensors 2026 11(2):1413-1424 DOI 10.1021/acssensors.5c03699
ISSUE-005,SCORE-015,citation_fix,RID-077;RID-081;RID-088,Awad year,REPAIRED,Corrected Awad to 2024,Tier1,medium,02e,CLEARED_WITH_WEAKNESS,Awad 2024 38(10):6193-6202; Servais 2025 39(2):1217-1226; preclinical
ISSUE-006,PROJECT-DESCHUTES,spec_verification,RID-033;RID-008,Deschutes specs,VERIFIED,Confirmed 2MW/500GPM/80-90psi/3C via OCP,Tier2 industry-consortium,high,02e,CLEARED,OCP Deschutes 5.0 spec + OCP vendor pages + ARPA-E deck
ISSUE-007,CFS-DOE,fusion_claim,RID-102;RID-104,CFS $8M/largest,REPAIRED,$8M=DOE-validated milestone; largest=company-supported,Tier1+company-claim,medium,02e,CLEARED_WITH_WEAKNESS,cfs.energy/PRNewswire 2025-09-30; no DOE "largest" primary
ISSUE-008,DA-VINCI-43,biomed_claim,RID-077;RID-081;RID-088,43% force reduction,REPAIRED,Relabeled company-supported/preclinical,Tier1 venue preclinical,medium,02e,CLEARED_WITH_WEAKNESS,Awad 2024 & Servais 2025; tissue-model; Intuitive-funded
ISSUE-009,HBM4-SOURCE,semiconductor_source,RID-041;RID-042,36Kr citation,REPAIRED,Replaced with JEDEC JESD270-4 + Semiconductor Engineering,Tier1/3,medium,02e,CLEARED,720->775um confirmed; hybrid bonding postponed
ISSUE-010,FAA-PART-108,policy_trigger,RID-067;RID-068;RID-069;RID-070;RID-071;RID-072;RID-074;RID-112,Part 108 not final,HOLD_SPECULATIVE,Keep drone RIDs regulatory-speculation,Tier1 official,high,02d,HOLD,FR 2026-01644; no final rule as of 2026-06-25
ISSUE-011,BIS-2026-00789,policy_trigger,compute/China-fab RIDs,Export-control volatile,WATCH,Track rescission/tightening,Tier1 official,high,02d,WATCH,FR 2026-00789 effective 2026-01-15; volatile
ISSUE-012,USTR-SIC-2027,policy_trigger,SiC RIDs,Future 301 rate unannounced,WATCH,Track USTR before June 23 2027,Tier1 official,high,02d,WATCH,FR 2025-23912; 0% now, increase 2027-06-23 to rate announced ~2027-05-24
ISSUE-013,NRL-RID-036,procurement_claim,RID-036,Executed award unverified,KILL_STANDS,Keep kill; no executed award,Tier1 official,medium,02d,KILL_STANDS,SAM.gov NOI only; USAspending HR001123C0121 is DARPA (unrelated)
ISSUE-014,PLACEHOLDER-RIDS,placeholder_evidence,RID-111;RID-016;RID-100;RID-015;RID-026;RID-020;RID-040;RID-017;RID-032;RID-012;RID-022;RID-097;RID-082;RID-101;RID-094;RID-099,16 RIDs lack direct Tier1/2,HOLD,Find >=1 direct Tier1/2 citation per RID before deep dive,Tier1/2,low,02c,HOLD,Unsupported; ineligible for deep dive; TAM cannot satisfy gate
ISSUE-015,RID-087-091-PAIN,customer_pain_evidence,RID-087;RID-091,Policy-context-only,REPAIRED,Confirmed context-only; geography is China,Tier1 context,medium,02e,NEEDS_MORE_SOURCE,CELEX:52025DC0005 = EU report on China Document 551; no direct buyer evidence
```

## 5. CSV-ready rows — `source_evidence_ledger.csv` (EDIT 8 SCORE rows + APPEND 1 new)

```
source_id,batch_id,date_accessed,source_title,source_url_or_citation,domain,source_tier,source_type,publication_date,geography,topic,claim_supported,evidence_note,confidence,limitations,access_level,count_toward_300,used_in_idea_ids,notes
SCORE-001,B02,2026-06-25,OCP Diablo 400 Base Spec & Deschutes CDU,opencompute.org,opencompute.org,Tier2,industry-consortium product-spec,2025,US,DC power/cooling,DC busway/breaker/connector spec & pain,Re-tiered from Tier 1,medium,Design targets not field-measured; consortium-authored,public,no,RID-001;RID-002;RID-003;RID-005;RID-008;RID-115,Was mislabeled Tier 1
SCORE-002,B02,2026-06-25,Power Stabilization for AI Training Datacenters (preprint) + NVIDIA GB300 blog,arXiv:2508.14318; arXiv:2508.16457; developer.nvidia.com,arxiv.org/nvidia.com,Tier2/3,preprint + company-claim,2025,US,AI power oscillation,Training power-swing/oscillation pain,arXiv=preprint; NVIDIA=company claim,medium,Not peer-reviewed; NVIDIA self-test,public,no,RID-002;RID-009;RID-024;RID-029;RID-030,NERC report corroborates pain
SCORE-004,B02,2026-06-25,McKinsey Humanoid robots: crossing the chasm + BofA Humanoid Robots 101,mckinsey.com; BofA Apr 2025,mckinsey.com,Tier2,analysis,2025,Global,Humanoid BOM,Actuators 40-60% of BOM,Deleted MS 56% misattribution,high,Range estimate; teardown-based,public,no,RID-053,56% was China-share figure in MS Humanoid 100
SCORE-010,B02,2026-06-25,Clinical Evaluation of Microneedle Biosensors for Continuous Lactate Monitoring,DOI 10.1021/acssensors.5c03699,pubs.acs.org,Tier1,peer-reviewed,2026,US,Continuous lactate,r=0.94 AUC=0.95 n=21,Author corrected to Djassemi et al.,high,Pilot n=21; 4h wear,paywall,no,RID-078;RID-080,Joseph Wang senior author
SCORE-013,B02,2026-06-25,DOE validation of CFS TF magnet & $8M Milestone award,cfs.energy; PRNewswire 2025-09-30,cfs.energy,Tier1/2,company-PR + govt-program,2025-09-30,US,Fusion HTS magnet,$8M DOE milestone; TF magnet validated,"largest"=company-supported,medium,No DOE primary for "largest",public,no,RID-102;RID-104,DOE Sec. Wright SPARC visit corroborates milestone
SCORE-015,B02,2026-06-25,Force-feedback da Vinci 5 studies,DOI 10.1007/s00464-024-11131-z; 10.1007/s00464-024-11472-9,link.springer.com,Tier1,peer-reviewed (preclinical),2024/2025,US,Surgical force feedback,Up to 43% less force (preclinical),Awad year fixed to 2024; relabeled preclinical/company-supported,medium,Tissue model; Intuitive-funded; no RCT,paywall,no,RID-077;RID-081;RID-088,Servais 2025 confirmed
SCORE-016,B02,2026-06-25,HBM4 Sticks With Microbumps + JEDEC JESD270-4,semiengineering.com; JEDEC JESD270-4,semiengineering.com,Tier1/3,standards + journalism,2025/2026,Global,HBM4 packaging,720->775um relaxation postpones hybrid bonding,36Kr (Tier 4) removed/replaced,medium,Future HBM4E/HBM5 timing uncertain,public,no,RID-041;RID-042;RID-045;RID-051,Confirms RID-042 kill
SCORE-004D,B02,2026-06-25,EU Commission IPI Report on China medical-device procurement,CELEX:52025DC0005; SWD(2025)2,eur-lex.europa.eu,Tier1,government report (context),2025,EU/China,Medical-device localization,Describes China Document 551 (25-100%; 100% for 137/178),Policy-context-only; geography=China,medium,Non-binding report; not direct buyer pain,public,no,RID-087;RID-091,Binding follow-on is Reg (EU) 2025/1197 (exclusion, not target)
SCORE-013-DOE,B02,2026-06-25,DOE Milestone-Based Fusion Development Program,energy.gov fusion program page,energy.gov,Tier1,government,2023-2025,US,Fusion milestone program,Program structure & milestone validation,New supporting source (program-level),medium,No line-item "largest" wording,public,no,RID-102;RID-104,Provisional new source ID
```

## 6. CSV-ready rows — `scored_idea_database_repaired_2026_06_25.csv` (NEW FILE; 49 affected rows)

> Local-file discipline: repaired scores go in this file; do **not** edit the original `scored_idea_database.csv`. All `new_score = old_score`, `score_delta = 0` (numerical re-score is 02e's job); only evidence labels, eligibility, and score-impact direction were set.

```
rank,idea_id,idea_name,old_score,new_score,score_delta,old_decision,new_decision,evidence_status,top25_eligible,repair_notes,source_issue_ids
-,RID-001,800VDC busway,81,81,0,P,P,CLEARED_WITH_WEAKNESS,yes,OCP re-tiered Tier2; pain holds; impact small,ISSUE-001;ISSUE-006
-,RID-002,Capacitorless DC buffer+supercap,86,86,0,P,P,CLEARED_WITH_WEAKNESS,yes,arXiv preprint+NVIDIA company-claim; pain corroborated; impact small,ISSUE-001;ISSUE-002
-,RID-003,Solid-state DC breaker+e-fuse,84,84,0,P,P,CLEARED_WITH_WEAKNESS,yes,OCP Tier2; impact small,ISSUE-001
-,RID-005,Rack-level DC-DC module,61,61,0,W,W,CLEARED_WITH_WEAKNESS,yes,OCP Diablo spec; impact small,ISSUE-001
-,RID-008,Blind-mate liquid+power connector,82,82,0,P,P,CLEARED_WITH_WEAKNESS,yes,Deschutes/Diablo spec Tier2; impact small,ISSUE-001;ISSUE-006
-,RID-009,GPU-aware power-orchestration SW,78,78,0,P,P,CLEARED_WITH_WEAKNESS,yes,arXiv preprint+NVIDIA claim; impact small,ISSUE-002
-,RID-024,GFM protection relay,81,81,0,P,P,CLEARED_WITH_WEAKNESS,yes,oscillation pain corroborated (NERC); impact small,ISSUE-002
-,RID-029,Grid-edge power-quality conditioner,77,77,0,P,P,CLEARED_WITH_WEAKNESS,yes,impact small,ISSUE-002
-,RID-030,Distribution-grade STATCOM (SiC),80,80,0,P,P,CLEARED_WITH_WEAKNESS,yes,SiC tariff = watch not kill; impact small,ISSUE-002;ISSUE-012
-,RID-033,CDU for 45C loops,77,77,0,P,P,CLEARED_WITH_WEAKNESS,yes,Deschutes specs verified Tier2; impact small,ISSUE-001;ISSUE-006
-,RID-034,Microfluidic cold plate >1kW/cm2,76,76,0,P,P,CLEARED_WITH_WEAKNESS,yes,80PSI spec enables cold plates; impact none,ISSUE-006
-,RID-115,Wide-bandwidth DC current sensor,54,54,0,W,W,CLEARED_WITH_WEAKNESS,yes,OCP DC-power spec; impact small,ISSUE-001
-,RID-053,Humanoid rotary actuator,79,79,0,P,P,CLEARED,yes,McKinsey 40-60% confirmed; 56% deleted; impact none,ISSUE-003
-,RID-102,Fusion-magnet HTS components,70,70,0,P,P,CLEARED_WITH_WEAKNESS,yes,$8M DOE-validated; "largest"=company; impact small,ISSUE-007
-,RID-104,Fusion first-wall thermal mgmt,62,62,0,W,W,CLEARED_WITH_WEAKNESS,yes,CFS milestone context; impact small,ISSUE-007
-,RID-077,Surgical force-feedback system,62,62,0,W,W,CLEARED_WITH_WEAKNESS,yes,43% preclinical/company-supported; impact small down,ISSUE-005;ISSUE-008
-,RID-081,FDA AI-enabled surgical subsystem,58,58,0,W,W,CLEARED_WITH_WEAKNESS,yes,preclinical evidence; impact small down,ISSUE-005;ISSUE-008
-,RID-088,Robotic catheter actuation,56,56,0,W,W,CLEARED_WITH_WEAKNESS,yes,preclinical force-feedback; impact small down,ISSUE-005;ISSUE-008
-,RID-051,Advanced-packaging warpage controller,60,60,0,W,W,CLEARED_WITH_WEAKNESS,yes,HBM4 microbump 16-high raises warpage relevance; impact small,ISSUE-009
-,RID-041,Advanced-packaging metrology platform,51,51,0,K,K,KILL,no,HBM4 microbump postpones adv-packaging metrology pull,ISSUE-009
-,RID-042,Die-to-wafer hybrid bonder,47,47,0,K,K,KILL,no,720->775um postpones hybrid bonding past 2029 window,ISSUE-009
-,RID-045,Panel-level packaging handler,49,49,0,K,K,KILL,no,advanced-packaging pull postponed,ISSUE-009
-,RID-036,Chiplet thermal characterization,62,62,0,K,K,KILL,no,No executed NRL award; SAM.gov NOI only,ISSUE-013
-,RID-067,Detect-and-avoid module,71,71,0,P,P,HOLD,no,Part 108 not final; regulatory-speculation,ISSUE-010
-,RID-068,eVTOL powertrain,64,64,0,W,W,HOLD,no,Part 108 not final,ISSUE-010
-,RID-069,eVTOL thermal management,64,64,0,W,W,HOLD,no,Part 108 not final,ISSUE-010
-,RID-070,C2 datalink module+RID/EC,68,68,0,W,W,HOLD,no,Part 108 not final,ISSUE-010
-,RID-071,Drone airspace-management ADSP,52,52,0,K,K,HOLD,no,Part 108 not final; kill stands,ISSUE-010
-,RID-072,Heavy-lift cargo drone airframe,53,53,0,W,W,HOLD,no,Part 108 not final,ISSUE-010
-,RID-074,Drone battery fast-swap system,63,63,0,W,W,HOLD,no,Part 108 not final,ISSUE-010
-,RID-112,Navigation-grade MEMS IMU,69,69,0,W,W,HOLD,no,Held at regulatory-speculation; broad-market potential to revisit independently of Part 108,ISSUE-010
-,RID-087,Point-of-care molecular cartridge,47,47,0,K,K,NEEDS_MORE_SOURCE,no,Policy-context-only (China Document 551); no buyer pain,ISSUE-015
-,RID-091,China-localized imaging detector,46,46,0,K,K,NEEDS_MORE_SOURCE,no,Policy-context-only; geography=China; no buyer pain,ISSUE-015
-,RID-111,High-bandwidth piezo actuator,72,72,0,P,P,HOLD,no,Placeholder; no direct Tier1/2 source,ISSUE-014
-,RID-016,Second-life battery repurposing,71,71,0,P,P,HOLD,no,Placeholder; no direct Tier1/2 source,ISSUE-014
-,RID-100,Automated optical-assembly cell,70,70,0,P,P,HOLD,no,Placeholder; no direct Tier1/2 source,ISSUE-014
-,RID-015,Thermal-storage module (700C),68,68,0,W,W,HOLD,no,Placeholder,ISSUE-014
-,RID-026,Hybrid-plant controller,68,68,0,W,W,HOLD,no,Placeholder,ISSUE-014
-,RID-020,Battery thermal-runaway suppression,67,67,0,W,W,HOLD,no,Placeholder,ISSUE-014
-,RID-040,Datacenter waste-heat recovery,67,67,0,W,W,HOLD,no,Placeholder,ISSUE-014
-,RID-017,Sodium-ion grid module,65,65,0,W,W,HOLD,no,Placeholder,ISSUE-014
-,RID-032,EV-fleet bidirectional charger,63,63,0,W,W,HOLD,no,Placeholder,ISSUE-014
-,RID-012,Behind-the-meter firm-power interface,63,63,0,W,W,HOLD,no,Placeholder,ISSUE-014
-,RID-022,Microgrid DC-coupling hub,61,61,0,W,W,HOLD,no,Placeholder,ISSUE-014
-,RID-097,Laser micro-machining cell,56,56,0,W,W,HOLD,no,Placeholder,ISSUE-014
-,RID-082,Implantable neurostimulator power,55,55,0,W,W,HOLD,no,Placeholder,ISSUE-014
-,RID-101,Molten-salt-resistant alloy,55,55,0,W,W,HOLD,no,Placeholder,ISSUE-014
-,RID-094,AM in-situ NDE,50,50,0,K,K,HOLD,no,Placeholder + prior kill; no direct source,ISSUE-014
-,RID-099,Extreme-precision metrology instrument,49,49,0,W,W,HOLD,no,Placeholder,ISSUE-014
```

## 7. `policy_trigger_watchlist.csv` — provisional rows (FINALIZE IN 02d)

The dedicated watchlist build is **prompt 02d** (`02d_policy_trigger_watchlist.md`), which expects the full 11-column schema (trigger_id, trigger, current status, official source, affected RIDs, score fields affected, what changes if fired, current confidence, refresh cadence, quarterly search query, status). The triggers carried forward from this session are seeded below — treat as provisional and complete in 02d; do not over-build here.

```
trigger_id,trigger,current_status,official_source,affected_rids,what_changes_if_fired,current_confidence,refresh_cadence,status
TRIG-01,FAA Part 108 BVLOS final rule published,not final (NPRM; comment closed 2026-02-11),Federal Register / faa.gov,RID-067;068;069;070;071;072;074;112,Drone RIDs move from regulatory-speculation toward eligible,high,quarterly,speculative
TRIG-02,BIS FR 2026-00789 rescinded or tightened,active (effective 2026-01-15),Federal Register / BIS,compute & China-fab RIDs,Re-prices export/reg-risk inverse on compute/China-fab ideas,high,quarterly,active
TRIG-03,USTR Section 301 SiC/semiconductor rate announced,rate TBD (increase 2027-06-23; announce ~2027-05-24),USTR / Federal Register,SiC RIDs (RID-030;004;049;047),Re-prices SiC supply-chain cost on affected ideas,high,quarterly,speculative
TRIG-04,Executed NRL/Navy award appears for SSTR/FDTR instrument,NOI only (no executed award),USAspending / FPDS / SAM.gov,RID-036,Could reopen RID-036 kill if a competitor award confirms demand,medium,quarterly,speculative
TRIG-05,JEDEC/HBM roadmap revives hybrid bonding (HBM5 pull),postponed (720->775um; trending 825-900um),JEDEC / IEEE / SEMI,RID-041;042;045,Could reopen RID-042/041/045 kills if D2W demand returns by 2029,medium,quarterly,speculative
TRIG-06,da Vinci force-feedback upgraded by powered clinical-outcomes RCT,preclinical only,ClinicalTrials.gov / PubMed,RID-077;081;088,Upgrades surgical force-feedback evidence above CLEARED_WITH_WEAKNESS,low,quarterly,speculative
```

## 8. `rejected_ideas.md` — no new rejections

No new ideas were rejected this session. The 4 KILLs (RID-036, RID-041, RID-042, RID-045) were already rejected in Phase 16 scoring; this session only **confirmed the kills with strengthened evidence**. Optional rationale append (only if you want the strengthened basis recorded):

```
- RID-042 (Die-to-wafer hybrid bonder): KILL confirmed 2026-06-25. JEDEC JESD270-4 relaxed HBM4 max stack height 720->775um, keeping microbumps for 16-high stacks and postponing hybrid bonding past the 2029 window (Semiconductor Engineering; JEDEC). Revive only on a JEDEC/HBM5 hybrid-bonding re-mandate.
- RID-041 (Advanced-packaging metrology) / RID-045 (Panel-level handler): KILL confirmed 2026-06-25 — advanced-packaging demand pull postponed with hybrid bonding; diagnostic/cleanroom + giants (Onto/KLA/AMAT/ASMPT).
- RID-036 (Chiplet thermal characterization SSTR/FDTR): KILL confirmed 2026-06-25. Only a SAM.gov sole-source Notice of Intent to Laser Thermal Analysis exists; USAspending HR001123C0121 is an unrelated DARPA award; no executed NRL/Navy contract located. Revive only on an executed Navy/NRL award in USAspending/FPDS/SAM.
```

## 9. Research-log entry — append to `02_research_log/research_log.md`

```text
## 2026-06-25 — 07b: Source-Audit Remediation (Phase 16 repair)

Prompt file used: prompts/04_diligence_scoring/02b_apply_source_audit_remediation.md; prompts/07_refresh_and_controls/02g_update_export_package.md (export)
Claude mode used: Research (advanced) for source verification; normal chat for packaging
Project files used: 00_admin/claude_project_instructions.md (governing), 01_sources/source_whitelist.md, source_quality_policy.md, source_quality_policy_addendum_scoring_audit.md, 01_score_filtered_ideas.md, 02_diversity_filter_70_90.md, 01_raw_idea_generation_120.md, source_evidence_ledger.csv, source_issue_tracker.csv
Key outputs:
  - Applied all 11 remediations (ISSUE-001..ISSUE-015). Eligibility result: 19 eligible for top-25 deep dive (1 CLEARED RID-053; 18 CLEARED_WITH_WEAKNESS), 30 blocked (24 HOLD = 16 placeholders + 8 drone RIDs; 4 KILL = RID-036/041/042/045; 2 NEEDS_MORE_SOURCE = RID-087/091).
  - Verified citations: SCORE-010 first author = Djassemi et al. (ACS Sensors 2026 11(2):1413-1424, DOI 10.1021/acssensors.5c03699); SCORE-015 Awad = 2024 (Surg Endosc 38(10):6193-6202); Servais 2025 confirmed.
  - Relabels: OCP/Deschutes -> Tier 2 industry-consortium/product-spec (specs 2MW/500GPM/80-90psi/3C verified via OCP Deschutes 5.0 + vendor pages); NVIDIA "-30%" -> company-supported (GB300 dev blog, LITEON, internal Megatron test); CFS "$8M" = DOE-validated milestone, "largest" -> company-supported (no DOE primary for superlative); da Vinci "43%" -> preclinical/Intuitive-supported.
  - HBM4: replaced 36Kr (Tier 4) with JEDEC JESD270-4 + Semiconductor Engineering; 720->775um confirmed -> hybrid bonding postponed -> RID-042 kill locked (trend toward 825-900um for HBM4E/HBM5).
  - Humanoid BOM: deleted misattributed "Morgan Stanley 56%" (that 56% = China share of MS Humanoid 100 universe, not actuator BOM); kept McKinsey 40-60% + BofA 40-50%.
  - SCORE-004D geography reversal: CELEX:52025DC0005 is a non-binding EU IPI report describing CHINA's Document 551 (25-100% localization; 100% for 137/178 categories); binding follow-on is Reg (EU) 2025/1197 (exclusion measure). RID-087/091 stay policy-context-only.
  - Policy triggers confirmed non-final: FAA Part 108 (FR 2026-01644, no final rule); BIS FR 2026-00789 (active/volatile); USTR Section 301 SiC (rate TBD, announce ~2027-05-24).
Files updated:
  - source_issue_tracker.csv — REPLACE 15 rows (status -> CLEARED/CLEARED_WITH_WEAKNESS/HOLD/KILL_STANDS/WATCH/NEEDS_MORE_SOURCE)
  - source_evidence_ledger.csv — EDIT 8 SCORE rows + APPEND SCORE-013-DOE (all count_toward_300=no, scoring sources)
  - scored_idea_database_repaired_2026_06_25.csv — NEW FILE, 49 affected rows (new_score=old_score; re-score deferred to 02e)
  - 07b_source_audit_remediation.md — substantive 02b output (repair + evidence-label tables, blocked/eligible lists)
  - policy_trigger_watchlist.csv — provisional 6 trigger rows (finalize in 02d)
  - research_log.md — this entry
New sources added: 0 to the 300-corpus (scoring-evidence rows only, count_toward_300=no); 1 provisional scoring source (SCORE-013-DOE)
New ideas added: 0 (hard rule)
Ideas rejected: 0 new (4 prior kills confirmed with strengthened rationale)
Open questions:
  - 02e: apply downward score adjustments where flagged (SCORE-002 cluster, surgical SCORE-015/da Vinci cluster, CFS "largest"); RID-053 needs no penalty.
  - Find a DOE.gov primary page asserting the CFS "$8M / largest" figure to upgrade ISSUE-007 confidence.
  - Strict-reviewer call: should RID-077/081/088 route to HOLD pending clinical-outcome data rather than CLEARED_WITH_WEAKNESS? Flagged for 02e.
  - RID-051 is a borderline admit (thin evidence); confirm a direct spec or downgrade in 02e.
Next action: Run prompts/04_diligence_scoring/02c_placeholder_source_repair.md (07c) in a fresh chat to attempt >=1 direct Tier 1/2 source per the 16 placeholder RIDs; prioritize the three P-scored ones (RID-111, RID-016, RID-100).
```

## 10. Files to re-upload to Claude Project before the next chat (02c)

1. `03_evidence_ledgers/source_issue_tracker.csv` — after replacing the 15 rows (§4)
2. `03_evidence_ledgers/source_evidence_ledger.csv` — after the 8 edits + 1 append (§5)
3. `06_scored_idea_database/scored_idea_database_repaired_2026_06_25.csv` — new file (§6)
4. `07b_source_audit_remediation.md` — the substantive 02b output (save from the chat artifact)
5. `02_research_log/research_log.md` — after appending §9
6. (Already in Project, no change needed: `01_raw_idea_generation_120.md`, `01_score_filtered_ideas.md`, `source_quality_policy_addendum_scoring_audit.md`, `source_whitelist.md`, `source_quality_policy.md` — all required by 02c.)

> Note: `policy_trigger_watchlist.csv` is not strictly needed for 02c (placeholder repair); it becomes the working file for 02d. Add the provisional rows (§7) whenever you create that file.

## 11. Next action

Run **`prompts/04_diligence_scoring/02c_placeholder_source_repair.md` (07c)** in a fresh chat — attempt at least one direct Tier 1/2 source for each of the 16 placeholder RIDs, prioritizing the three currently scored "pursue" (RID-111 piezo actuator, RID-016 second-life battery, RID-100 optical-assembly cell). Any placeholder that does not clear stays HOLD. Then 02d (policy-trigger watchlist) → 02e (targeted re-score) → 02f (top-25 eligibility gate). Do not run deep dives until the 02f gate clears.
