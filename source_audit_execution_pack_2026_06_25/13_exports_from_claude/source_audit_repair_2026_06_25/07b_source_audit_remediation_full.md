# Source-Audit Remediation — 79-Idea Deep-Tech Portfolio (Prompt 02b), as of 2026-06-25

## TL;DR
- All 11 mandatory remediations were applied: OCP/Deschutes was re-tiered from Tier 1 to Tier 2 industry-consortium/product-spec; NVIDIA "−30%," CFS "largest," and da Vinci "43%" were relabeled company-supported/preclinical; the 36Kr HBM4 citation was replaced with JEDEC JESD270-4 + Semiconductor Engineering; the "Morgan Stanley 56% actuator-BOM" attribution was deleted as a misattribution and replaced with McKinsey 40–60%; and the SCORE-010 author was corrected to Djassemi et al. and SCORE-015 Awad to 2024.
- Of 49 affected ideas, 19 clear the deep-dive eligibility gate (1 CLEARED, 18 CLEARED_WITH_WEAKNESS) — chiefly the data-center power/cooling cluster and the humanoid actuator wedge — while 30 are blocked (24 HOLD incl. 16 placeholders + 8 drone regulatory-speculation, 4 KILL, 2 NEEDS_MORE_SOURCE).
- Two findings materially change the evidence base: the SCORE-004D "EU 25–100% procurement target" is actually a non-binding EU Commission report describing CHINA's "Document 551" localization policy (policy-context-only, geography reversed), and the HBM4 720→775µm relaxation confirms hybrid bonding is postponed — locking in the RID-042 die-to-wafer hybrid-bonder kill.

## Key Findings

**Citation corrections fully verified (Tier 1 sources):**
- **SCORE-010**: First author is **Omeed Djassemi et al.**, not "Wang et al." (Joseph Wang is senior/last author). "Clinical Evaluation of Microneedle Biosensors for Continuous Lactate Monitoring in Critically Ill Patients," *ACS Sensors* 2026, 11(2):1413–1424, DOI 10.1021/acssensors.5c03699; n=21 ICU/ED/CPET, r=0.94, AUC=0.95. Peer-reviewed Tier 1. Author corrected; claim stands.
- **SCORE-015**: Awad et al. is **2024**, not 2025 — *Surg Endosc* 38(10):6193–6202, DOI 10.1007/s00464-024-11131-z. Servais et al. 39(2):1217–1226 (DOI 10.1007/s00464-024-11472-9) is correctly **2025**. Both studies are explicitly **preclinical** (tissue models) and Intuitive-supported; the "up to 43% less force" is a company-supported/preclinical claim, not a clinical-outcome RCT.

**Company/consortium relabels confirmed:**
- **NVIDIA "−30%"**: A company dev-blog claim. NVIDIA's Technical Blog "How New GB300 NVL72 Features Provide Steady Power for AI" states verbatim: "the peak power demand seen by the grid is reduced by 30% when training the Megatron LLM, and rapid fluctuations are substantially dampened" — built with PSU vendor LITEON Technology, 65 joules/GPU of energy storage, based on NVIDIA internal testing. Relabel company-supported. Independent commentary (Utility Dive quoting Georgia Tech's Santiago Grijalva calling it "a moderate big deal") corroborates relevance but not the specific figure.
- **OCP/Project Deschutes specs verified** and re-tiered Tier 2 industry-consortium/product-spec: 2 MW, 500 GPM (1890 LPM), 80 PSI (80–90 psi target), 3°C ATD — confirmed across OCP product listings (STULZ, nVent, Delta, Envicool), the OCP "Google Deschutes 5.0 CDU Specification" (effective July 1 2025), an ARPA-E presentation deck (Google/Kabbani), and vendor PRs (Boyd, Nidec). Supports product/spec claims; NOT peer-reviewed/government Tier 1.
- **CFS $8M/"largest"**: The $8M DOE Milestone-Based Fusion Development Program award is real and DOE-validated (independent national-lab review panel; Energy Secretary Chris Wright visited SPARC Sept 29 2025). But the "largest amount paid to any company in the program" superlative appears only in CFS's own PR (cfs.energy) and PRNewswire — no DOE.gov primary page asserting "largest" was found. Relabel "largest" CFS company-supported.

**Humanoid BOM — misattribution corrected:** McKinsey "Scaling the humanoid robotics supply chain into billion-dollar wins" (2025) states verbatim: "The core hardware stack of a humanoid spans five domains: actuators (40 to 60 percent of the bill of materials, or BOM)…"; the companion "Humanoid robots: Crossing the chasm" report lists "Actuation (about 40 to 60 percent of total costs)…the single largest opportunity for cost reduction" (Tier 2), corroborated by BofA "Humanoid Robots 101" (40–50%). The "56%" cited to Morgan Stanley is a **misattribution** — Morgan Stanley's "Humanoid 100" report uses 56% to describe **China's share of listed humanoid companies**, not actuator BOM. No primary Morgan Stanley report stating a "56% actuator BOM" exists; delete that attribution.

**HBM4 — 36Kr replaced; hybrid-bonding postponed:** Semiconductor Engineering ("HBM4 Sticks With Microbumps, Postponing Hybrid Bonding") states verbatim: "JEDEC revised the module height limit from 720µm to 775µm, which affords enough room to allow microbump bonding for HBM4. However, HBM5 and its successors are expected to take advantage of hybrid bonding"; analyst Ray Wang adds: "with the JEDEC standard revision at the beginning of this year, we have seen the delayed adoption of hybrid bonding technology." JEDEC's published JESD270-4 HBM4 standard (Tier 1) confirms the 775µm relaxation for 12- and 16-high stacks. Per TrendForce (citing ZDNet, March 6 2026), "industry discussions are underway to raise the limit for future HBM to roughly 825–900 μm" for HBM4E/HBM5 20-high stacks — reinforcing that hybrid bonding is postponed, not cancelled.

**Policy triggers (all remain non-final / watchlist):**
- **FAA Part 108**: NOT final as of June 25 2026. NPRM published Aug 7 2025; comment period reopened and closed Feb 11 2026 (FR 2026-01644); the Feb 1 2026 executive-order deadline was missed (DroneXL, June 18 2026, confirms the deadline "came and went months ago with no final rule"). Keep all drone RIDs at regulatory-speculation.
- **BIS FR 2026-00789**: Final rule effective Jan 15 2026, shifting advanced-computing export review for China/Macau from presumption of denial to case-by-case. Active but volatile (State Dept shipment hold, AI OVERWATCH Act H.R. 6875, Section 232 25% tariff). WATCH.
- **USTR Section 301 SiC/semiconductor**: Notice of Action (FR 2025-23912, Dec 23 2025) sets the rate at 0% now, increasing June 23 2027 "to a rate to be announced not fewer than 30 days prior to that date" (~May 24 2027). Future rate unknown. WATCH.

**Kills hold:**
- **RID-036 (NRL)**: Only a SAM.gov sole-source Notice of Intent to Laser Thermal Analysis exists; USAspending HR001123C0121 is a DARPA (ATOMIC) award, not Navy. No executed NRL/Navy contract in USAspending/FPDS. KILL STANDS.
- **RID-042 (D2W hybrid bonder)**: HBM4 microbump relaxation postpones hybrid bonding past the 2029 window; no HBM5 pull revives D2W demand. KILL STANDS.

**SCORE-004D geography reversal (subagent finding):** CELEX:52025DC0005 is "REPORT FROM THE COMMISSION pursuant to Article 5(4) of Regulation (EU) 2022/1031 … concerning measures and practices of the People's Republic of China in the public procurement market for medical devices" — COM(2025) 5 final, a **non-binding** Commission investigative report. The 25–100% targets (100% for 137 of 178 categories) belong to **China's "Document 551"** (Notice on "Guiding Audit Standards for Government Procurement of Imported Products," 2021 Edition); the EU Staff Working Document SWD(2025) 2 final recital 28 quotes it verbatim: "The target share of domestic medical devices varies between 25 % and 100 %, with a 100% target for 137 categories of medical devices." The binding EU follow-on (Implementing Regulation (EU) 2025/1197) is a Chinese-supplier exclusion measure (≥€5M tenders, ≤50% Chinese content, 5 years), not a procurement-target mandate. For RID-087/091 this remains POLICY_CONTEXT_ONLY — it describes a forced-substitution dynamic in China but provides no direct buyer/procurement/budget evidence for the specific product theses.

## Details

### Deliverable 1 — REPAIR TABLE
(issue_id | affected SCORE/RID | original problem | corrected tier | corrected wording | corrected confidence | score impact | decision impact | citations | status)

- **ISSUE-001** | SCORE-001 / RID-001;002;003;005;008;115 | OCP over-tiered as Tier 1 | Tier 2 industry-consortium/product-spec | "Per OCP Deschutes/Diablo specs and OCP-listed product pages (industry-consortium evidence), the data-center DC-power and liquid-cooling interface requirements are defined" | Medium | small (down) | pursue/watch unchanged | opencompute.org Diablo/Deschutes specs; TechPowerUp OCP launch | CLEARED_WITH_WEAKNESS
- **ISSUE-002** | SCORE-002 / RID-002;009;024;029;030 | arXiv + NVIDIA −30% over-credited | preprint (arXiv) + company-claim (NVIDIA); effective Tier 2/3 | "AI-training power oscillations are documented in preprints (Choukse arXiv:2508.14318; Ko & Zhu arXiv:2508.16457) and a NVIDIA company blog claiming up to 30% peak reduction; the grid-oscillation pain is independently corroborated by NERC" | Medium | small (down) | unchanged | arXiv:2508.14318; arXiv:2508.16457; NVIDIA dev blog; NERC 2025 large-loads report | CLEARED_WITH_WEAKNESS
- **ISSUE-003** | SCORE-004 / RID-053 | actuator BOM figure | Tier 2 | "Actuators are ~40–60% of humanoid BOM (McKinsey 2025), corroborated by BofA 40–50%" — delete "Morgan Stanley 56%" | High | none | pursue unchanged | McKinsey "Crossing the chasm"; McKinsey supply-chain companion; BofA "Humanoid Robots 101" | CLEARED
- **ISSUE-004** | SCORE-010 / RID-078;080 | author correction | Tier 1 peer-reviewed | "Djassemi et al., ACS Sensors 2026, 11(2):1413–1424" | High | none | unchanged | DOI 10.1021/acssensors.5c03699 | CLEARED
- **ISSUE-005** | SCORE-015 / RID-077;081;088 | Awad year | Tier 1 venue, preclinical | "Awad et al., Surg Endosc 2024, 38(10):6193–6202; Servais et al. 2025, 39(2):1217–1226; up to 43% less force, preclinical/Intuitive-supported" | Medium | small (down) | watch unchanged | DOI 10.1007/s00464-024-11131-z; 10.1007/s00464-024-11472-9 | CLEARED_WITH_WEAKNESS
- **ISSUE-006** | PROJECT-DESCHUTES / RID-033;008 | specs need support | Tier 2 industry-consortium/product-spec | "2 MW, 500 GPM, 80–90 psi, 3°C ATD per OCP Deschutes 5.0 spec and OCP-listed vendor pages" | High | none | pursue unchanged | OCP Deschutes spec; OCP product listings; ARPA-E Google deck | CLEARED
- **ISSUE-007** | CFS-DOE / RID-102;104 | $8M/"largest" company-supported | $8M = DOE-validated milestone (program-administered); "largest" = company-supported | "DOE Milestone program validated CFS's TF magnet and disbursed an $8M milestone payment; CFS characterizes it as the largest program award to date (company-stated)" | Medium | small (down on superlative) | pursue/watch unchanged | cfs.energy PR; PRNewswire 2025-09-30; DOE Milestone program page | CLEARED_WITH_WEAKNESS
- **ISSUE-008** | DA-VINCI-43 / RID-077;081;088 | 43% should be preclinical/company-supported | Tier 1 venue but preclinical/non-independent | "Up to 43% less force on tissue, preclinical (tissue-model), Intuitive-supported; no clinical-outcome RCT" | Medium | small (down) | watch unchanged | Awad 2024; Servais 2025; Intuitive newsroom | CLEARED_WITH_WEAKNESS
- **ISSUE-009** | HBM4-SOURCE / RID-041;042 | 36Kr (Tier 4) | Tier 1 (JEDEC) + Tier 3 (Semiconductor Engineering) | "JEDEC relaxed HBM4 height 720→775µm, keeping microbumps for 16-high and postponing hybrid bonding" | Medium | none (confirms kills) | kills stand | JEDEC JESD270-4; Semiconductor Engineering | CLEARED (source replaced)
- **ISSUE-010** | FAA-PART-108 / RID-067;068;069;070;071;072;074;112 | Part 108 not final | Tier 1 official (FR) | "Part 108 remains an NPRM; no final Federal Register rule as of 2026-06-25" | High | none | all drone RIDs regulatory-speculation | FR 2026-01644; faa.gov NPRM | HOLD (regulatory-speculation)
- **ISSUE-011** | BIS-2026-00789 / compute & China-fab RIDs | policy volatile | Tier 1 official | "Final rule effective Jan 15 2026; case-by-case review; remains volatile" | High | none | watchlist | FR 2026-00789 | WATCH
- **ISSUE-012** | USTR-SIC-2027 / SiC RIDs | future rate unannounced | Tier 1 official | "0% now, increasing June 23 2027 to a rate to be announced ~May 24 2027" | High | none | watchlist | FR 2025-23912 | WATCH
- **ISSUE-013** | NRL-RID-036 / RID-036 | executed contract unverified | Tier 1 official | "Sole-source NOI only; no executed Navy/NRL award in USAspending/FPDS; DARPA award is unrelated" | Medium | none | kill stands | SAM.gov NOI; USAspending HR001123C0121 | KILL_STANDS
- **ISSUE-014** | PLACEHOLDER-RIDS / 16 RIDs | lack direct Tier1/2 support | n/a | "No direct Tier 1/2 source located for the core claim; market/TAM cannot satisfy the gate" | Unknown→Low | none (re-score deferred) | hold | none found | HOLD
- **ISSUE-015** | RID-087-091-PAIN / RID-087;091 | policy-context-only | Tier 1 (EU report) but context-only | "EU report describes China's Document 551 localization targets; no direct buyer/procurement/budget evidence for the product theses" | Medium | none | kills stand; policy-context-only | CELEX:52025DC0005; SWD(2025)2; Reg (EU) 2025/1197 | NEEDS_MORE_SOURCE

### Deliverable 2 — CORRECTED EVIDENCE-LABEL TABLE
(item | correct label | can support | cannot support | best source (tier) | residual uncertainty)

- **OCP/Project Deschutes** | industry-consortium product-spec | product existence; spec targets (2MW/500GPM/80–90psi/3°C ATD); interface standardization | independent market demand; peer-reviewed/government fact | OCP Deschutes 5.0 spec + OCP vendor listings (Tier 2) | OCP figures are design targets/vendor-stated, not field-measured performance
- **NVIDIA −30%** | company-supported | product capability claim (GB300 power smoothing) | independent grid-impact magnitude | NVIDIA dev blog (company) | based on NVIDIA internal Megatron test; no third-party replication
- **CFS $8M/largest** | $8M = DOE-validated milestone; "largest" = company-supported | that DOE validated the TF magnet and disbursed $8M | "largest in program" as an independent fact | cfs.energy/PRNewswire (company) + DOE Milestone program (Tier 1) | DOE never published "largest" wording
- **da Vinci 43%** | company-supported / preclinical | technical feasibility; preclinical force reduction | clinical outcomes (trauma, recovery) | Awad 2024 & Servais 2025, Surg Endosc (Tier 1 venue, preclinical) | tissue-model only; Intuitive-funded; no RCT
- **HBM4 microbump/hybrid-bonding postponement** | standards-body + journalism | that JEDEC relaxed to 775µm and microbumps persist for HBM4 | that hybrid bonding is cancelled (it is postponed) | JEDEC JESD270-4 (Tier 1) + Semiconductor Engineering (Tier 3) | exact HBM4E/HBM5 hybrid-bonding timing uncertain
- **Humanoid actuator BOM** | analysis (consulting) | actuators ~40–60% of BOM | a precise "56%" point estimate | McKinsey 2025 (Tier 2) + BofA (Tier 2) | range, not a single figure; teardown-based
- **FAA Part 108** | policy-context (NPRM, not final) | that BVLOS rulemaking is advancing | that routine BVLOS is legal/final | FR 2026-01644 (Tier 1) | final rule timing/scope unknown
- **BIS 2026-00789** | government (final rule) | current export-review posture for China/Macau | future stability of the policy | FR 2026-00789 (Tier 1) | high volatility; pending legislation/litigation
- **USTR Section 301 SiC/semiconductor** | government (scheduled future action) | that a tariff path is scheduled for 2027 | the actual future rate | FR 2025-23912 (Tier 1) | rate unannounced until ~May 2027
- **NRL/Laser Thermal procurement** | procurement-NOI-not-executed | that NRL signaled sole-source intent | an executed/funded award | SAM.gov NOI (Tier 1) | no executed contract found
- **RID-087/091 customer pain** | policy-context-only | that China mandates device localization (Document 551, via EU report) | direct buyer/procurement/budget pain for these theses | CELEX:52025DC0005 (Tier 1, context) | wrong-geography risk; non-binding report

### Deliverable 3 — CORRECTED source_issue_tracker.csv rows
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
ISSUE-010,FAA-PART-108,policy_trigger,RID-067;RID-068;RID-069;RID-070;RID-071;RID-072;RID-074;RID-112,Part 108 not final,HOLD_SPECULATIVE,Keep drone RIDs regulatory-speculation,Tier1 official,high,02e,HOLD,FR 2026-01644; no final rule as of 2026-06-25
ISSUE-011,BIS-2026-00789,policy_trigger,compute/China-fab RIDs,Export-control volatile,WATCH,Track rescission/tightening,Tier1 official,high,02e,WATCH,FR 2026-00789 effective 2026-01-15; volatile
ISSUE-012,USTR-SIC-2027,policy_trigger,SiC RIDs,Future 301 rate unannounced,WATCH,Track USTR before June 23 2027,Tier1 official,high,02e,WATCH,FR 2025-23912; 0% now, increase 2027-06-23
ISSUE-013,NRL-RID-036,procurement_claim,RID-036,Executed award unverified,KILL_STANDS,Keep kill; no executed award,Tier1 official,medium,02e,KILL_STANDS,SAM.gov NOI only; USAspending DARPA award unrelated
ISSUE-014,PLACEHOLDER-RIDS,placeholder_evidence,RID-111;RID-016;RID-100;RID-015;RID-026;RID-020;RID-040;RID-017;RID-032;RID-012;RID-022;RID-097;RID-082;RID-101;RID-094;RID-099,16 RIDs lack direct Tier1/2,HOLD,No direct source found,Tier1/2,low,02e,HOLD,Remain unsupported; ineligible for deep dive
ISSUE-015,RID-087-091-PAIN,customer_pain_evidence,RID-087;RID-091,Policy-context-only,REPAIRED,Confirmed context-only; geography is China,Tier1 context,medium,02e,NEEDS_MORE_SOURCE,CELEX:52025DC0005 = EU report on China Document 551; no direct buyer evidence
```

### Deliverable 4 — CORRECTED source_evidence_ledger.csv rows
```
source_id,batch_id,date_accessed,source_title,source_url_or_citation,domain,source_tier,source_type,publication_date,geography,topic,claim_supported,evidence_note,confidence,limitations,access_level,count_toward_300,used_in_idea_ids,notes
SCORE-001,B02,2026-06-25,OCP Diablo 400 Base Spec & Deschutes CDU,opencompute.org,opencompute.org,Tier2,industry-consortium product-spec,2025,US,DC power/cooling,DC busway/breaker/connector spec & pain,Re-tiered from Tier 1,medium,Design targets not field-measured; consortium-authored,public,no,RID-001;RID-002;RID-003;RID-005;RID-008;RID-115,Was mislabeled Tier 1
SCORE-002,B02,2026-06-25,Power Stabilization for AI Training Datacenters (preprint) + NVIDIA GB300 blog,arXiv:2508.14318; arXiv:2508.16457; developer.nvidia.com,arxiv.org/nvidia.com,Tier2/3,preprint + company-claim,2025,US,AI power oscillation,Training power-swing/oscillation pain,arXiv=preprint; NVIDIA=company claim,medium,Not peer-reviewed; NVIDIA self-test,public,no,RID-002;RID-009;RID-024;RID-029;RID-030,NERC report corroborates pain
SCORE-004,B02,2026-06-25,McKinsey Humanoid robots: crossing the chasm + BofA Humanoid Robots 101,mckinsey.com; BofA Apr 2025,mckinsey.com,Tier2,analysis,2025,Global,Humanoid BOM,Actuators 40-60% of BOM,Deleted MS 56% misattribution,high,Range estimate; teardown-based,public,no,RID-053,56% was China-share of Humanoid 100
SCORE-010,B02,2026-06-25,Clinical Evaluation of Microneedle Biosensors for Continuous Lactate Monitoring,DOI 10.1021/acssensors.5c03699,pubs.acs.org,Tier1,peer-reviewed,2026,US,Continuous lactate,r=0.94 AUC=0.95 n=21,Author corrected to Djassemi et al.,high,Pilot n=21; 4h wear,paywall,no,RID-078;RID-080,Joseph Wang senior author
SCORE-013,B02,2026-06-25,DOE validation of CFS TF magnet & $8M Milestone award,cfs.energy; PRNewswire 2025-09-30,cfs.energy,Tier1/2,company-PR + govt-program,2025-09-30,US,Fusion HTS magnet,$8M DOE milestone; TF magnet validated,"largest"=company-supported,medium,No DOE primary for "largest",public,no,RID-102;RID-104,DOE Sec. Wright visit corroborates milestone
SCORE-015,B02,2026-06-25,Force-feedback da Vinci 5 studies,DOI 10.1007/s00464-024-11131-z; 10.1007/s00464-024-11472-9,link.springer.com,Tier1,peer-reviewed (preclinical),2024/2025,US,Surgical force feedback,Up to 43% less force (preclinical),Awad year fixed to 2024; relabeled preclinical/company-supported,medium,Tissue model; Intuitive-funded; no RCT,paywall,no,RID-077;RID-081;RID-088,Servais 2025 confirmed
SCORE-016,B02,2026-06-25,HBM4 Sticks With Microbumps + JEDEC JESD270-4,semiengineering.com; JEDEC JESD270-4,semiengineering.com,Tier1/3,standards + journalism,2025/2026,Global,HBM4 packaging,720->775um relaxation postpones hybrid bonding,36Kr (Tier 4) removed/replaced,medium,Future HBM4E/HBM5 timing uncertain,public,no,RID-041;RID-042;RID-045;RID-051,Confirms RID-042 kill
SCORE-004D,B02,2026-06-25,EU Commission IPI Report on China medical-device procurement,CELEX:52025DC0005; SWD(2025)2,eur-lex.europa.eu,Tier1,government report (context),2025,EU/China,Medical-device localization,Describes China Document 551 (25-100%; 100% for 137/178),Policy-context-only; geography=China,medium,Non-binding report; not direct buyer pain,public,no,RID-087;RID-091,Binding follow-on is Reg (EU) 2025/1197 (exclusion, not target)
SCORE-013-DOE,B02,2026-06-25,DOE Milestone-Based Fusion Development Program,energy.gov fusion program page,energy.gov,Tier1,government,2023-2025,US,Fusion milestone program,Program structure & milestone validation,New supporting source (program-level),medium,No line-item "largest" wording,public,no,RID-102;RID-104,Provisional new source ID
```

### Deliverable 5 — scored_idea_database_repaired_2026_06_25.csv (affected ideas only)
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
-,RID-036,Chiplet thermal characterization,62,62,0,K,K,KILL,no,No executed NRL award; NOI only,ISSUE-013
-,RID-067,Detect-and-avoid module,71,71,0,P,P,HOLD,no,Part 108 not final; regulatory-speculation,ISSUE-010
-,RID-068,eVTOL powertrain,64,64,0,W,W,HOLD,no,Part 108 not final,ISSUE-010
-,RID-069,eVTOL thermal management,64,64,0,W,W,HOLD,no,Part 108 not final,ISSUE-010
-,RID-070,C2 datalink module+RID/EC,68,68,0,W,W,HOLD,no,Part 108 not final,ISSUE-010
-,RID-071,Drone airspace-management ADSP,52,52,0,K,K,HOLD,no,Part 108 not final; kill stands,ISSUE-010
-,RID-072,Heavy-lift cargo drone airframe,53,53,0,W,W,HOLD,no,Part 108 not final,ISSUE-010
-,RID-074,Drone battery fast-swap system,63,63,0,W,W,HOLD,no,Part 108 not final,ISSUE-010
-,RID-112,Navigation-grade MEMS IMU,69,69,0,W,W,HOLD,no,Held at regulatory-speculation; broad-market potential to revisit,ISSUE-010
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
-,RID-094,AM in-situ NDE,50,50,0,K,K,HOLD,no,Placeholder + kill; no direct source,ISSUE-014
-,RID-099,Extreme-precision metrology instrument,49,49,0,W,W,HOLD,no,Placeholder,ISSUE-014
```

### Deliverable 6 — IDEAS BLOCKED FROM TOP-25 DEEP DIVE (30)
- **16 placeholders (HOLD)**: RID-111, RID-016, RID-100 (all P-scored but unsupported), RID-015, RID-026, RID-020, RID-040, RID-017, RID-032, RID-012, RID-022, RID-097, RID-082, RID-101, RID-099, RID-094 — no direct Tier 1/2 source for the core claim; TAM cannot satisfy the gate.
- **8 drone RIDs (HOLD / regulatory-speculation)**: RID-067, RID-068, RID-069, RID-070, RID-071, RID-072, RID-074, RID-112 — thesis depends on the not-yet-final FAA Part 108 rule.
- **4 kills (KILL)**: RID-036 (no executed NRL award), RID-042 (hybrid bonding postponed), RID-041 & RID-045 (advanced-packaging pull postponed).
- **2 policy-context-only (NEEDS_MORE_SOURCE)**: RID-087, RID-091 — China Document 551 is forced-substitution context, not direct buyer/procurement/budget pain.

### Deliverable 7 — IDEAS ALLOWED INTO TOP-25 DEEP DIVE (19)
- **Data-center power/cooling cluster (12, CLEARED_WITH_WEAKNESS)**: RID-001, RID-002, RID-003, RID-005, RID-008, RID-009, RID-024, RID-029, RID-030, RID-033, RID-034, RID-115 — pain remains corroborated after OCP re-tiering and NVIDIA/arXiv relabeling.
- **Humanoid actuator (1, CLEARED)**: RID-053 — McKinsey 40–60% Tier 2 with BofA corroboration.
- **Fusion (2, CLEARED_WITH_WEAKNESS)**: RID-102, RID-104 — DOE-validated $8M milestone (with "largest" relabeled).
- **Surgical force feedback (3, CLEARED_WITH_WEAKNESS)**: RID-077, RID-081, RID-088 — peer-reviewed preclinical (Tier 1 venue), with clinical-outcome weakness flagged.
- **Advanced-packaging warpage (1, CLEARED_WITH_WEAKNESS)**: RID-051 — 16-high microbump stacks heighten warpage-control relevance.

## Recommendations
1. **Send the 19 cleared ideas to the 02e re-scoring step now**, but instruct 02e to apply downward score-impact adjustments where flagged: SCORE-002 cluster (arXiv/NVIDIA relabel, small down), SCORE-015/da Vinci surgical cluster (preclinical/company-supported, small down), SCORE-013 fusion (strip "largest" puffery, small down). The humanoid actuator RID-053 needs no penalty. **Threshold to change**: if 02e's relabeling drops any data-center idea's evidence below CLEARED_WITH_WEAKNESS, re-route it to HOLD.
2. **Keep the 16 placeholders in HOLD** and run one targeted Tier 1/2 search per RID before any future deep-dive consideration. **Benchmark to flip to eligible**: ≥1 direct Tier 1/2 source supporting the *core* claim (not TAM). Prioritize the three P-scored placeholders (RID-111 piezo actuator, RID-016 second-life battery, RID-100 optical-assembly) since they carry the highest scores.
3. **Hold all drone RIDs until a final Part 108 Federal Register rule publishes.** **Trigger to revisit**: publication of the final rule (the post-Feb 2026 deadline slipped; industry expects spring/summer 2026). RID-112 (MEMS IMU) should be re-examined independently of Part 108 given broad defense/automotive markets.
4. **Maintain RID-036, RID-041, RID-042, RID-045 as kills.** **Trigger to revive RID-036**: an executed Navy/NRL award in USAspending/FPDS/SAM. **Trigger to revive RID-042**: a JEDEC/HBM roadmap change or credible HBM5 pull reviving 2029-relevant D2W hybrid-bonding demand — currently moving the opposite direction (toward 825–900µm).
5. **Treat RID-087/091 as policy-context-only with a score cap.** **Trigger to upgrade**: a direct buyer/procurement/budget document (a Chinese provincial tender, hospital procurement award, or budget line) tied to the specific product thesis — the EU IPI report alone cannot clear it.
6. **Keep BIS 2026-00789, USTR Section 301 SiC, and Part 108 on the active watchlist** with calendar triggers: USTR rate announcement ~May 24 2027; BIS volatility (monitor for the AI OVERWATCH Act and Section 232 outcomes); Part 108 final-rule publication.

## Caveats
- **No numerical re-scoring was performed** — all new_score = old_score, delta = 0, per the 02e hand-off. Only evidence labels, corrected confidence, eligibility, and score-impact *direction* were set.
- **CFS "$8M" nuance**: the milestone payment and DOE independent validation are well-supported; only the "largest in program" superlative is company-sourced. A DOE program page confirming the figure would upgrade confidence.
- **Surgical cluster judgment call**: RID-077/081/088 are admitted as CLEARED_WITH_WEAKNESS because the underlying studies are peer-reviewed (Surg Endosc), but the evidence is preclinical and Intuitive-funded; a strict reviewer could route these to HOLD pending clinical-outcome data. Flagged for 02e.
- **SCORE-004D geography reversal** is the highest-impact correction: any downstream analysis that treated this as an EU "buy-European" procurement mandate is wrong on both geography (China) and instrument type (non-binding report).
- **RID-051** is a borderline admit — it was not in the kill set and benefits from the microbump-persistence finding, but its evidence remains thin; revisit if 02e cannot tie it to a direct spec.
- Placeholder RIDs were not exhaustively searched individually within this remediation's budget; HOLD reflects absence of a located source, not proof of absence.

## Source-Audit Status Summary (49 affected ideas)
- **CLEARED**: 1 (RID-053)
- **CLEARED_WITH_WEAKNESS**: 18 (RID-001, 002, 003, 005, 008, 009, 024, 029, 030, 033, 034, 115, 102, 104, 077, 081, 088, 051)
- **HOLD**: 24 (16 placeholders + 8 drone RIDs)
- **KILL**: 4 (RID-036, 041, 042, 045)
- **NEEDS_MORE_SOURCE**: 2 (RID-087, 091)
- **Eligible for top-25 deep dive**: **19** (1 CLEARED + 18 CLEARED_WITH_WEAKNESS). Ineligible: 30.

Reminder: no deep dive was run; this remediation only repairs evidence and sets eligibility. The deep-dive gate is NOT cleared by this step — numerical re-scoring is deferred to 02e.