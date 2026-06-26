# 07e Targeted Re-Score of Affected Ideas — ISSUE-001..017 Score Application (Batch 07E)

_Phase: prompts/04_diligence_scoring/02e_targeted_rescore_affected_ideas.md • Date: 2026-06-25 • Mode: deterministic re-score/packaging (no new search — evidence was gathered in 07b–07d; the re-score operates only on Project files). Anchor: new_score = published old_score + Σ(category deltas)._

## TL;DR
- **49 audit-affected ideas re-scored; 28 lost points, totalling −41 points. No score rose.** The published total column is authoritative; category sub-scores were not re-summed.
- **Eligible deep-dive pool = 32** (was 33 provisional). The net change is two ideas dropped to HOLD: **RID-077** (surgical force-feedback console) and **RID-099** (extreme-precision metrology instrument).
- **Only one decision letter moved: RID-067 (detect-and-avoid) P→W.** Three evidence-status moves: RID-077 CLEARED_WITH_WEAKNESS→HOLD, RID-099 CLEARED_WITH_WEAKNESS→HOLD, RID-071 HOLD→KILL.
- **The four locked kills hold** (RID-036, RID-041, RID-042, RID-045); RID-094 stays HOLD; RID-087/091 stay NEEDS_MORE_SOURCE/blocked.
- **Two judgment calls are flagged for override** (surgical cluster RID-077/081/088; RID-099 vs the metrology filter) — see §8.

## Key Findings
- **Data-center power cluster (the top of the portfolio) takes small, uniform haircuts, not structural hits.** OCP/Project Deschutes was re-tiered Tier 1→Tier 2 (vendor co-authorship) and NVIDIA's “up to −30%” was relabeled company-supported, so each affected RID loses 1 Pain/WTP point (flagship **RID-002 −2**: 86→84). Every one of these stays a CLEARED_WITH_WEAKNESS pursue — the pain is still corroborated by Tier-1 preprints and IEEE 2800.2. RID-024 and RID-034 take **no** cut because their sources were not re-tiered.
- **The drone / air-mobility cluster is uniformly capped under TRIG-001.** FAA Part 108 BVLOS is still NPRM-only (no final Federal Register rule as of 2026-06-25), so the regulatory-trigger thesis is speculative: −2 on the inverse Reg/export axis for the whole cluster, plus −1 Pain/WTP on the two most rule-coupled (RID-067/070). All seven go HOLD/ineligible; **RID-067 also flips P→W**; **RID-071 hardens HOLD→KILL** for an independent, permanent reason (software/services + Part 146/108 gating).
- **Judgment Call #1 — surgical force-feedback (RID-077/081/088).** Clinical-benefit evidence is preclinical (Awad) and Intuitive-funded, and NCT07247175 measures surrogate endpoints (traction force, path length), not patient outcomes. The standalone console **RID-077**, whose thesis is direct displacement of Intuitive, makes an implicit clinical-outcome claim the addendum says company/preclinical evidence cannot support → **HOLD** (−2 Pain/WTP). The two subsystem plays **RID-081/088** keep CLEARED_WITH_WEAKNESS (−1 each), with the clinical-outcome gate deferred to 02f.
- **Judgment Call #2 — RID-099 vs RID-094 consistency.** RID-099 is a standalone metrology instrument with no non-diagnostic function; held to the same diagnostic/metrology-overproduction hard filter as RID-094, it moves to **HOLD** and leaves the eligible pool (score unchanged at 49).
- **Placeholder re-tests (07c) mostly hold; four take timing/scope haircuts.** RID-101 −2 TRL (molten-salt deployment largely >2030), RID-026 −1 Standalone-value (consulting-border), RID-040 −1 China-wedge (EU/Germany-bounded driver), RID-012 −1 Pain/WTP (IEA figures are 2030 projections). The other cleared placeholders take no cut — their evidence was confirmed, not decreased.
- **Humanoid actuator RID-053 takes no penalty.** The misattributed “Morgan Stanley 56%” was removed, but the 40–60% actuation-BOM claim still stands on McKinsey + BofA; it remains the only CLEARED pursue in the cluster.
- **CFS / fusion-magnet RID-102 −1 Niche-wedge** (the “largest-in-program” line is company-supported and immaterial; the DOE $8M milestone is intact); RID-104 unchanged.
- **No new corpus sources, no new ideas, no new kills.** Counted corpus total stays **397**. Only the 49 affected ideas were re-scored; the other 30 portfolio ideas keep their original decisions.

## §1 — Before/After Score Table (all 49 affected ideas)

| RID | Idea | Old | New | Δ | Old→New decision | Evidence status | Top-25? |
|---|---|---:|---:|---:|:--:|---|:--:|
| RID-002 | Capacitorless DC buffer+supercap | 86 | 84 | -2 | P | CLEARED_WITH_WEAKNESS | yes |
| RID-003 | Solid-state DC breaker+e-fuse | 84 | 83 | -1 | P | CLEARED_WITH_WEAKNESS | yes |
| RID-008 | Blind-mate liquid+power connector | 82 | 81 | -1 | P | CLEARED_WITH_WEAKNESS | yes |
| RID-001 | 800VDC busway | 81 | 80 | -1 | P | CLEARED_WITH_WEAKNESS | yes |
| RID-024 | GFM protection relay | 81 | 81 | 0 | P | CLEARED_WITH_WEAKNESS | yes |
| RID-030 | Distribution-grade STATCOM (SiC) | 80 | 79 | -1 | P | CLEARED_WITH_WEAKNESS | yes |
| RID-053 | Humanoid rotary actuator | 79 | 79 | 0 | P | CLEARED | yes |
| RID-009 | GPU-aware power-orchestration SW | 78 | 77 | -1 | P | CLEARED_WITH_WEAKNESS | yes |
| RID-029 | Grid-edge power-quality conditioner | 77 | 76 | -1 | P | CLEARED_WITH_WEAKNESS | yes |
| RID-033 | CDU for 45C loops | 77 | 76 | -1 | P | CLEARED_WITH_WEAKNESS | yes |
| RID-034 | Microfluidic cold plate >1kW/cm2 | 76 | 76 | 0 | P | CLEARED_WITH_WEAKNESS | yes |
| RID-111 | High-bandwidth piezo actuator | 72 | 72 | 0 | P | CLEARED | yes |
| RID-067 | Detect-and-avoid module | 71 | 68 | -3 | P→W | HOLD | no |
| RID-016 | Second-life battery repurposing | 71 | 71 | 0 | P | CLEARED | yes |
| RID-102 | Fusion-magnet HTS components | 70 | 69 | -1 | P | CLEARED_WITH_WEAKNESS | yes |
| RID-100 | Automated optical-assembly cell | 70 | 70 | 0 | P | CLEARED | yes |
| RID-112 | Navigation-grade MEMS IMU | 69 | 67 | -2 | W | HOLD | no |
| RID-070 | C2 datalink module+RID/EC | 68 | 65 | -3 | W | HOLD | no |
| RID-015 | Thermal-storage module (700C) | 68 | 68 | 0 | W | CLEARED | yes |
| RID-026 | Hybrid-plant controller | 68 | 67 | -1 | W | CLEARED_WITH_WEAKNESS | yes |
| RID-020 | Battery thermal-runaway suppression | 67 | 67 | 0 | W | CLEARED_WITH_WEAKNESS | yes |
| RID-040 | Datacenter waste-heat recovery | 67 | 66 | -1 | W | CLEARED_WITH_WEAKNESS | yes |
| RID-017 | Sodium-ion grid module | 65 | 65 | 0 | W | CLEARED | yes |
| RID-068 | eVTOL powertrain | 64 | 62 | -2 | W | HOLD | no |
| RID-069 | eVTOL thermal management | 64 | 62 | -2 | W | HOLD | no |
| RID-074 | Drone battery fast-swap system | 63 | 61 | -2 | W | HOLD | no |
| RID-032 | EV-fleet bidirectional charger | 63 | 63 | 0 | W | CLEARED | yes |
| RID-012 | Behind-the-meter firm-power interface | 63 | 62 | -1 | W | CLEARED | yes |
| RID-104 | Fusion first-wall thermal mgmt | 62 | 62 | 0 | W | CLEARED_WITH_WEAKNESS | yes |
| RID-077 | Surgical force-feedback system | 62 | 60 | -2 | W | HOLD | no |
| RID-036 | Chiplet thermal characterization | 62 | 62 | 0 | K | KILL | no |
| RID-005 | Rack-level DC-DC module | 61 | 60 | -1 | W | CLEARED_WITH_WEAKNESS | yes |
| RID-022 | Microgrid DC-coupling hub | 61 | 61 | 0 | W | CLEARED_WITH_WEAKNESS | yes |
| RID-051 | Advanced-packaging warpage controller | 60 | 58 | -2 | W | CLEARED_WITH_WEAKNESS | yes |
| RID-081 | FDA AI-enabled surgical subsystem | 58 | 57 | -1 | W | CLEARED_WITH_WEAKNESS | yes |
| RID-088 | Robotic catheter actuation | 56 | 55 | -1 | W | CLEARED_WITH_WEAKNESS | yes |
| RID-097 | Laser micro-machining cell | 56 | 56 | 0 | W | CLEARED_WITH_WEAKNESS | yes |
| RID-082 | Implantable neurostimulator power | 55 | 55 | 0 | W | CLEARED | yes |
| RID-101 | Molten-salt-resistant alloy | 55 | 53 | -2 | W | CLEARED_WITH_WEAKNESS | yes |
| RID-115 | Wide-bandwidth DC current sensor | 54 | 53 | -1 | W | CLEARED_WITH_WEAKNESS | yes |
| RID-072 | Heavy-lift cargo drone airframe | 53 | 51 | -2 | W | HOLD | no |
| RID-071 | Drone airspace-management ADSP | 52 | 52 | 0 | K | KILL | no |
| RID-041 | Advanced-packaging metrology platform | 51 | 51 | 0 | K | KILL | no |
| RID-094 | AM in-situ NDE | 50 | 50 | 0 | K | HOLD | no |
| RID-045 | Panel-level packaging handler | 49 | 49 | 0 | K | KILL | no |
| RID-099 | Extreme-precision metrology instrument | 49 | 49 | 0 | W | HOLD | no |
| RID-042 | Die-to-wafer hybrid bonder | 47 | 47 | 0 | K | KILL | no |
| RID-087 | Point-of-care molecular cartridge | 47 | 46 | -1 | K | NEEDS_MORE_SOURCE | no |
| RID-091 | China-localized imaging detector | 46 | 45 | -1 | K | NEEDS_MORE_SOURCE | no |

## §2 — Score Deltas by Rubric Category

Only the 28 ideas with non-zero deltas are listed. Aggregate at the bottom.

| RID | Idea | Category(ies) reduced | Δ | Why |
|---|---|---|---:|---|
| RID-002 | Capacitorless DC buffer+supercap | Pain/WTP -2 | -2 | NVIDIA -30% relabeled company-supported (pain still corroborated by Tier-1 preprints Choukse/Ko-Zhu); OCP Diablo/Deschutes Tier1->Tier2. PW-2. |
| RID-003 | Solid-state DC breaker+e-fuse | Pain/WTP -1 | -1 | OCP Diablo white-space Tier1->Tier2. PW-1. |
| RID-008 | Blind-mate liquid+power connector | Pain/WTP -1 | -1 | OCP blind-mate requirement Tier1->Tier2. PW-1. |
| RID-001 | 800VDC busway | Pain/WTP -1 | -1 | OCP Diablo spec Tier1->Tier2; UL857>600V codification lag. PW-1. |
| RID-030 | Distribution-grade STATCOM (SiC) | Pain/WTP -1 | -1 | NVIDIA company-supported; IEEE-2800.2 (Tier1) backstop intact. PW-1. |
| RID-009 | GPU-aware power-orchestration SW | Pain/WTP -1 | -1 | NVIDIA -30% company-supported; preprint-corroborated pain. PW-1. |
| RID-029 | Grid-edge power-quality conditioner | Pain/WTP -1 | -1 | NVIDIA company-supported; IEEE-2800.2 (Tier1) backstop intact. PW-1. |
| RID-033 | CDU for 45C loops | Pain/WTP -1 | -1 | OCP Deschutes spec Tier1->Tier2; SCORE-007 thermal intact. PW-1. |
| RID-067 | Detect-and-avoid module | Pain/WTP -1, Reg/export (inverse) -2 | -3 | Core thesis gated by FAA Part 108 BVLOS (NPRM only; not final; TRIG-001 speculative). Decision P->W; HOLD pending final FR rule. PW-1,RX-2. |
| RID-102 | Fusion-magnet HTS components | Niche-wedge -1 | -1 | DOE $8M milestone intact (Tier1/2); 'largest in program' relabeled company-supported (immaterial). Tiny customer set. NW-1. |
| RID-112 | Navigation-grade MEMS IMU | Reg/export (inverse) -2 | -2 | GPS-denied IMU demand gated by Part 108 (speculative). RX-2. |
| RID-070 | C2 datalink module+RID/EC | Pain/WTP -1, Reg/export (inverse) -2 | -3 | Remote-ID/C2 demand gated by Part 108 (speculative). PW-1,RX-2. |
| RID-026 | Hybrid-plant controller | Standalone-value -1 | -1 | NREL UNIFI/FERC 2023 clears existence, but confirm true HW/SW controller vs integration/consulting at deep-dive; residual consulting-border penalty. SV-1. |
| RID-040 | Datacenter waste-heat recovery | China-wedge -1 | -1 | Driver EU/Germany-bounded (Dir 2023/1791 Art 26.6 + EnEfG, eff 1 Jul 2026); weak China-first wedge. Geography-flagged. CW-1. |
| RID-068 | eVTOL powertrain | Reg/export (inverse) -2 | -2 | eVTOL/AAM type-cert gated; regulatory trigger speculative. RX-2. |
| RID-069 | eVTOL thermal management | Reg/export (inverse) -2 | -2 | eVTOL/AAM type-cert gated; regulatory trigger speculative. RX-2. |
| RID-074 | Drone battery fast-swap system | Reg/export (inverse) -2 | -2 | Part 108 timing + OEM lock; trigger speculative. RX-2. |
| RID-012 | Behind-the-meter firm-power interface | Pain/WTP -1 | -1 | IEA onsite gas/battery figures are 2030 projections; LBNL 'Queued Up' excludes behind-the-meter; borders on integration. Eligible; flagged. PW-1. |
| RID-077 | Surgical force-feedback system | Pain/WTP -2 | -2 | JUDGMENT CALL #1: standalone console competing directly with Intuitive; displacement thesis is an implicit clinical-outcome claim that evidence cannot support (Awad preclinical + Intuitive-funded; NCT07247175 measures surrogate endpoints, not patient outcomes). Addendum evidence-rule -> HOLD pending independent patient-outcome RCT. PW-2. (Reversible; override to defer-to-02f if preferred.) |
| RID-005 | Rack-level DC-DC module | Pain/WTP -1 | -1 | OCP-adjacent Tier1->Tier2; commoditized. PW-1. |
| RID-051 | Advanced-packaging warpage controller | Pain/WTP -2 | -2 | Borderline admit: thin evidence (SCORE-016), borders on in-line metrology; no direct purchased-capability spec confirmable in re-score (no new search in 02e). Downgraded; flagged WEAKEST ADMIT for 02f confirm-or-kill. PW-2. |
| RID-081 | FDA AI-enabled surgical subsystem | Pain/WTP -1 | -1 | JUDGMENT CALL #1: clinical-outcome benefit preclinical/company-funded, BUT subsystem play with ISO-10218 (SCORE-009) functional-safety backstop. Kept CLEARED_WITH_WEAKNESS; clinical-outcome gate deferred to 02f. PW-1. |
| RID-088 | Robotic catheter actuation | Pain/WTP -1 | -1 | JUDGMENT CALL #1: robotic-catheter subsystem; preclinical/company-funded benefit. Kept CLEARED_WITH_WEAKNESS (component play); FLAG for 02f. PW-1. |
| RID-101 | Molten-salt-resistant alloy | TRL/feasibility -2 | -2 | Molten-salt customer deployment largely >2030; near-term (<=2030) first-customer demand discounted. Eligible-with-weakness; timing-flagged. TRL-2. |
| RID-115 | Wide-bandwidth DC current sensor | Pain/WTP -1 | -1 | OCP Tier1->Tier2. Diagnostic-adjacent (functional current-sense component, not standalone instrument) -> FLAG for 02f. PW-1. |
| RID-072 | Heavy-lift cargo drone airframe | Reg/export (inverse) -2 | -2 | Part 108 + capex + China; trigger speculative. RX-2. |
| RID-087 | Point-of-care molecular cartridge | Pain/WTP -1 | -1 | Customer pain remains policy-context-only (Doc 551 localization; no direct workflow-pain/buyer source); also diagnostic. PW-1; stays blocked. |
| RID-091 | China-localized imaging detector | Pain/WTP -1 | -1 | Customer pain policy-context-only (Doc 551); cleanroom-high + China-only + export-incoherent. PW-1; stays blocked. |

**Category aggregate:** Pain/WTP -22 · Reg/export (inverse) -14 · TRL/feasibility -2 · Niche-wedge -1 · Standalone-value -1 · China-wedge -1 → **total −41 points** across 28 ideas. Pain/WTP (source re-tiering + company-claim relabels) and the inverse Reg/export axis (speculative Part 108 trigger) account for almost all of it.

## §3 — Decision Changes

| RID | Idea | Old | New | Reason |
|---|---|:--:|:--:|---|
| RID-067 | Detect-and-avoid module | P | W | Core thesis gated by FAA Part 108 BVLOS, which is NPRM-only/not final (TRIG-001 speculative); demoted out of the pursue tier pending a final FR rule. |

_No other decision letter changed. The three drone RIDs already at W stay W (now HOLD/ineligible); RID-071 was already decision-K and is now status-aligned to KILL._

## §4 — Top-25 Eligibility Status

- **Eligible (CLEARED / CLEARED_WITH_WEAKNESS): 32** of the 49 affected ideas.
- **Blocked (HOLD / KILL / NEEDS_MORE_SOURCE): 17.**
- **Eligibility changes this phase: 2** — RID-077 (yes→no) and RID-099 (yes→no), both to HOLD.
- Gate rule applied (addendum): only CLEARED / CLEARED_WITH_WEAKNESS pass; HOLD, NEEDS_MORE_SOURCE, KILL, speculative-trigger-dependent, and policy-context-only (no buyer/procurement) are excluded.

## §5 — CSV-Ready Corrected Rows

Authoritative file is `scored_idea_database_repaired_2026_06_25.csv` (12 columns, CRLF/no-BOM, 49 rows; `new_score = old_score + score_delta`, verified 0 mismatches). Verbatim contents:

```csv
rank,idea_id,idea_name,old_score,new_score,score_delta,old_decision,new_decision,evidence_status,top25_eligible,repair_notes,source_issue_ids
-,RID-001,800VDC busway,81,80,-1,P,P,CLEARED_WITH_WEAKNESS,yes,OCP re-tiered Tier2; pain holds; impact small | 02e: OCP Diablo spec Tier1->Tier2; UL857>600V codification lag. PW-1.,ISSUE-001;ISSUE-006
-,RID-002,Capacitorless DC buffer+supercap,86,84,-2,P,P,CLEARED_WITH_WEAKNESS,yes,arXiv preprint+NVIDIA company-claim; pain corroborated; impact small | 02e: NVIDIA -30% relabeled company-supported (pain still corroborated by Tier-1 preprints Choukse/Ko-Zhu); OCP Diablo/Deschutes Tier1->Tier2. PW-2.,ISSUE-001;ISSUE-002
-,RID-003,Solid-state DC breaker+e-fuse,84,83,-1,P,P,CLEARED_WITH_WEAKNESS,yes,OCP Tier2; impact small | 02e: OCP Diablo white-space Tier1->Tier2. PW-1.,ISSUE-001
-,RID-005,Rack-level DC-DC module,61,60,-1,W,W,CLEARED_WITH_WEAKNESS,yes,OCP Diablo spec; impact small | 02e: OCP-adjacent Tier1->Tier2; commoditized. PW-1.,ISSUE-001
-,RID-008,Blind-mate liquid+power connector,82,81,-1,P,P,CLEARED_WITH_WEAKNESS,yes,Deschutes/Diablo spec Tier2; impact small | 02e: OCP blind-mate requirement Tier1->Tier2. PW-1.,ISSUE-001;ISSUE-006
-,RID-009,GPU-aware power-orchestration SW,78,77,-1,P,P,CLEARED_WITH_WEAKNESS,yes,arXiv preprint+NVIDIA claim; impact small | 02e: NVIDIA -30% company-supported; preprint-corroborated pain. PW-1.,ISSUE-002
-,RID-024,GFM protection relay,81,81,0,P,P,CLEARED_WITH_WEAKNESS,yes,"oscillation pain corroborated (NERC); impact small | 02e: SCORE-003 (IEEE 2800.2-2026, Tier1) confirmed; evidence not decreased -> no reduction.",ISSUE-002
-,RID-029,Grid-edge power-quality conditioner,77,76,-1,P,P,CLEARED_WITH_WEAKNESS,yes,impact small | 02e: NVIDIA company-supported; IEEE-2800.2 (Tier1) backstop intact. PW-1.,ISSUE-002
-,RID-030,Distribution-grade STATCOM (SiC),80,79,-1,P,P,CLEARED_WITH_WEAKNESS,yes,SiC tariff = watch not kill; impact small | 02e: NVIDIA company-supported; IEEE-2800.2 (Tier1) backstop intact. PW-1.,ISSUE-002;ISSUE-012
-,RID-033,CDU for 45C loops,77,76,-1,P,P,CLEARED_WITH_WEAKNESS,yes,Deschutes specs verified Tier2; impact small | 02e: OCP Deschutes spec Tier1->Tier2; SCORE-007 thermal intact. PW-1.,ISSUE-001;ISSUE-006
-,RID-034,Microfluidic cold plate >1kW/cm2,76,76,0,P,P,CLEARED_WITH_WEAKNESS,yes,80PSI spec enables cold plates; impact none | 02e: SCORE-007 thermal evidence intact (not a re-tiering target) -> no reduction.,ISSUE-006
-,RID-115,Wide-bandwidth DC current sensor,54,53,-1,W,W,CLEARED_WITH_WEAKNESS,yes,"OCP DC-power spec; impact small | 02e: OCP Tier1->Tier2. Diagnostic-adjacent (functional current-sense component, not standalone instrument) -> FLAG for 02f. PW-1.",ISSUE-001
-,RID-053,Humanoid rotary actuator,79,79,0,P,P,CLEARED,yes,"McKinsey 40-60% confirmed; 56% deleted; impact none | 02e: Morgan Stanley '56%' misattribution removed (was China-share of MS Humanoid-100, not BOM); actuation=40-60% BOM holds on McKinsey (Tier2)+BofA. No penalty.",ISSUE-003
-,RID-102,Fusion-magnet HTS components,70,69,-1,P,P,CLEARED_WITH_WEAKNESS,yes,$8M DOE-validated; 'largest'=company; impact small | 02e: DOE $8M milestone intact (Tier1/2); 'largest in program' relabeled company-supported (immaterial). Tiny customer set. NW-1.,ISSUE-007
-,RID-104,Fusion first-wall thermal mgmt,62,62,0,W,W,CLEARED_WITH_WEAKNESS,yes,CFS milestone context; impact small | 02e: CFS DOE-milestone evidence intact; 'largest' not load-bearing here; pre-commercial market already priced -> no reduction.,ISSUE-007
-,RID-077,Surgical force-feedback system,62,60,-2,W,W,HOLD,no,"43% preclinical/company-supported; impact small down | 02e: JUDGMENT CALL #1: standalone console competing directly with Intuitive; displacement thesis is an implicit clinical-outcome claim that evidence cannot support (Awad preclinical + Intuitive-funded; NCT07247175 measures surrogate endpoints, not patient outcomes). Addendum evidence-rule -> HOLD pending independent patient-outcome RCT. PW-2. (Reversible; override to defer-to-02f if preferred.)",ISSUE-005;ISSUE-008
-,RID-081,FDA AI-enabled surgical subsystem,58,57,-1,W,W,CLEARED_WITH_WEAKNESS,yes,"preclinical evidence; impact small down | 02e: JUDGMENT CALL #1: clinical-outcome benefit preclinical/company-funded, BUT subsystem play with ISO-10218 (SCORE-009) functional-safety backstop. Kept CLEARED_WITH_WEAKNESS; clinical-outcome gate deferred to 02f. PW-1.",ISSUE-005;ISSUE-008
-,RID-088,Robotic catheter actuation,56,55,-1,W,W,CLEARED_WITH_WEAKNESS,yes,preclinical force-feedback; impact small down | 02e: JUDGMENT CALL #1: robotic-catheter subsystem; preclinical/company-funded benefit. Kept CLEARED_WITH_WEAKNESS (component play); FLAG for 02f. PW-1.,ISSUE-005;ISSUE-008
-,RID-051,Advanced-packaging warpage controller,60,58,-2,W,W,CLEARED_WITH_WEAKNESS,yes,"HBM4 microbump 16-high raises warpage relevance; impact small | 02e: Borderline admit: thin evidence (SCORE-016), borders on in-line metrology; no direct purchased-capability spec confirmable in re-score (no new search in 02e). Downgraded; flagged WEAKEST ADMIT for 02f confirm-or-kill. PW-2.",ISSUE-009
-,RID-041,Advanced-packaging metrology platform,51,51,0,K,K,KILL,no,HBM4 microbump postpones adv-packaging metrology pull | 02e: Diagnostic + cleanroom + giants; HBM4 microbump continuation strengthens only the diagnostic role (penalized on standalone value). Kill stands.,ISSUE-009
-,RID-042,Die-to-wafer hybrid bonder,47,47,0,K,K,KILL,no,"720->775um postpones hybrid bonding past 2029 window | 02e: Kill LOCKED on Tier-1 JEDEC JESD270-4 (775um, 16-Hi keeps microbumps) replacing Tier-4 36Kr; hybrid bonding postponed >2029 (TRIG-007: no near-term pull). Per addendum kill discipline.",ISSUE-009
-,RID-045,Panel-level packaging handler,49,49,0,K,K,KILL,no,advanced-packaging pull postponed | 02e: Cleanroom + capex; no audit finding revives. Kill stands.,ISSUE-009
-,RID-036,Chiplet thermal characterization,62,62,0,K,K,KILL,no,"No executed NRL award; SAM.gov NOI only | 02e: NRL award not verifiable (NOI N00173-25-RFI-MF18 + DARPA prime only; TRIG-005 speculative/medium). Per addendum, kill stands unless executed contract appears in USAspending/FPDS/SAM.gov.",ISSUE-013
-,RID-067,Detect-and-avoid module,71,68,-3,P,W,HOLD,no,"Part 108 not final; regulatory-speculation | 02e: Core thesis gated by FAA Part 108 BVLOS (NPRM only; not final; TRIG-001 speculative). Decision P->W; HOLD pending final FR rule. PW-1,RX-2.",ISSUE-010
-,RID-068,eVTOL powertrain,64,62,-2,W,W,HOLD,no,Part 108 not final | 02e: eVTOL/AAM type-cert gated; regulatory trigger speculative. RX-2.,ISSUE-010
-,RID-069,eVTOL thermal management,64,62,-2,W,W,HOLD,no,Part 108 not final | 02e: eVTOL/AAM type-cert gated; regulatory trigger speculative. RX-2.,ISSUE-010
-,RID-070,C2 datalink module+RID/EC,68,65,-3,W,W,HOLD,no,"Part 108 not final | 02e: Remote-ID/C2 demand gated by Part 108 (speculative). PW-1,RX-2.",ISSUE-010
-,RID-071,Drone airspace-management ADSP,52,52,0,K,K,KILL,no,Part 108 not final; kill stands | 02e: Software/services + Part 146/108 gated; permanent kill reason independent of trigger. Status aligned HOLD->KILL (decision already K).,ISSUE-010
-,RID-072,Heavy-lift cargo drone airframe,53,51,-2,W,W,HOLD,no,Part 108 not final | 02e: Part 108 + capex + China; trigger speculative. RX-2.,ISSUE-010
-,RID-074,Drone battery fast-swap system,63,61,-2,W,W,HOLD,no,Part 108 not final | 02e: Part 108 timing + OEM lock; trigger speculative. RX-2.,ISSUE-010
-,RID-112,Navigation-grade MEMS IMU,69,67,-2,W,W,HOLD,no,Held at regulatory-speculation; broad-market potential to revisit independently of Part 108 | 02e: GPS-denied IMU demand gated by Part 108 (speculative). RX-2.,ISSUE-010
-,RID-087,Point-of-care molecular cartridge,47,46,-1,K,K,NEEDS_MORE_SOURCE,no,Policy-context-only (China Document 551); no buyer pain | 02e: Customer pain remains policy-context-only (Doc 551 localization; no direct workflow-pain/buyer source); also diagnostic. PW-1; stays blocked.,ISSUE-015
-,RID-091,China-localized imaging detector,46,45,-1,K,K,NEEDS_MORE_SOURCE,no,Policy-context-only; geography=China; no buyer pain | 02e: Customer pain policy-context-only (Doc 551); cleanroom-high + China-only + export-incoherent. PW-1; stays blocked.,ISSUE-015
-,RID-111,High-bandwidth piezo actuator,72,72,0,P,P,CLEARED,yes,07c: PH-001 nanopositioning nm/kHz tradeoff + hybrid-bonding 0.2um placement; cleared | 02e: Placeholder CLEARED on Sci Rep 2022 + US Patent 12438117 (Tier1) -> no reduction.,ISSUE-014-111
-,RID-016,Second-life battery repurposing,71,71,0,P,P,CLEARED,yes,07c: PH-002 MIIT echelon-utilization + UL 1974 + NREL; cleared | 02e: Placeholder CLEARED on MIIT echelon-utilization spec + UL1974 + NREL (Tier1/2) -> no reduction.,ISSUE-014-016
-,RID-100,Automated optical-assembly cell,70,70,0,P,P,CLEARED,yes,07c: PH-003 peer-reviewed active-alignment packaging bottleneck; cleared | 02e: Placeholder CLEARED on Photonics 12(8):821 2025 (peer-reviewed Tier1); arXiv only corroborates -> no reduction.,ISSUE-014-100
-,RID-015,Thermal-storage module (700C),68,68,0,W,W,CLEARED,yes,07c: PH-004 Sandia/DOE G3P3 >700C 6h storage; cleared | 02e: Placeholder CLEARED on Sandia/DOE G3P3 (Tier1) -> no reduction.,ISSUE-014-015
-,RID-026,Hybrid-plant controller,68,67,-1,W,W,CLEARED_WITH_WEAKNESS,yes,"07c: PH-005 NREL UNIFI + FERC Order 2023; cleared-with-weakness (borders software/consulting; verify HW at 02e) | 02e: NREL UNIFI/FERC 2023 clears existence, but confirm true HW/SW controller vs integration/consulting at deep-dive; residual consulting-border penalty. SV-1.",ISSUE-014-026
-,RID-020,Battery thermal-runaway suppression,67,67,0,W,W,CLEARED_WITH_WEAKNESS,yes,07c: PH-006 UL 9540A + NFPA 855 2026 TRPP; cleared-with-weakness (commoditized/test-driven) | 02e: Placeholder CLEARED on UL9540A + NFPA 855:2026 (Tier1) -> no reduction.,ISSUE-014-020
-,RID-040,Datacenter waste-heat recovery,67,66,-1,W,W,CLEARED_WITH_WEAKNESS,yes,"07c: PH-007 EU EED + German EnEfG final law; cleared-with-weakness (EU/Germany geography limit) | 02e: Driver EU/Germany-bounded (Dir 2023/1791 Art 26.6 + EnEfG, eff 1 Jul 2026); weak China-first wedge. Geography-flagged. CW-1.",ISSUE-014-040
-,RID-017,Sodium-ion grid module,65,65,0,W,W,CLEARED,yes,07c: PH-008 GB/T 44265-2024 + PNNL/DOE; cleared | 02e: Placeholder CLEARED on GB/T 44265-2024 (Tier1) -> no reduction. China-incumbent competition already priced.,ISSUE-014-017
-,RID-032,EV-fleet bidirectional charger,63,63,0,W,W,CLEARED,yes,07c: PH-009 ISO 15118-20 + EVS38 V2G demo; cleared | 02e: Placeholder CLEARED on ISO 15118-20:2022 (Tier1) -> no reduction.,ISSUE-014-032
-,RID-012,Behind-the-meter firm-power interface,63,62,-1,W,W,CLEARED,yes,07c: PH-010 IEA 2026/2025 onsite-power + LBNL queue scarcity; cleared | 02e: IEA onsite gas/battery figures are 2030 projections; LBNL 'Queued Up' excludes behind-the-meter; borders on integration. Eligible; flagged. PW-1.,ISSUE-014-012
-,RID-022,Microgrid DC-coupling hub,61,61,0,W,W,CLEARED_WITH_WEAKNESS,yes,07c: PH-011 IEEE 2030.10 + DOE OE; cleared-with-weakness (diffuse/narrow scope) | 02e: Placeholder CLEARED on IEEE 2030.10-2021 + DOE OE (Tier1) -> no reduction.,ISSUE-014-022
-,RID-097,Laser micro-machining cell,56,56,0,W,W,CLEARED_WITH_WEAKNESS,yes,07c: PH-012 peer-reviewed TGV laser micromachining; cleared-with-weakness (generic application) | 02e: Placeholder CLEARED on JMPT 2025 (Tier1) -> no reduction. Commoditized job-shop risk already priced.,ISSUE-014-097
-,RID-082,Implantable neurostimulator power,55,55,0,W,W,CLEARED,yes,07c: PH-013 neural-implant power/longevity review; cleared | 02e: Placeholder CLEARED on Front. Neurosci. 2023 (Tier1) -> no reduction. FDA burden already priced.,ISSUE-014-082
-,RID-101,Molten-salt-resistant alloy,55,53,-2,W,W,CLEARED_WITH_WEAKNESS,yes,07c: PH-014 JOM/ORNL molten-salt corrosion; cleared-with-weakness (timeline likely past 2030) | 02e: Molten-salt customer deployment largely >2030; near-term (<=2030) first-customer demand discounted. Eligible-with-weakness; timing-flagged. TRL-2.,ISSUE-014-101
-,RID-094,AM in-situ NDE,50,50,0,K,K,HOLD,no,"07c: NIST AM-Bench Tier1 exists but prior-kill + monitoring-overproduction; HOLD, no standalone procurement/standards driver | 02e: Diagnostic/NDE-overproduction; prior kill; no standalone procurement/standards driver. HOLD stands.",ISSUE-014-094
-,RID-099,Extreme-precision metrology instrument,49,49,0,W,W,HOLD,no,"07c: PH-015 Nature Electronics + NIST overlay (sub-1nm); cleared-with-weakness (monitoring-adjacent, re-test at 02e) | 02e: Re-tested vs diagnostic/metrology-overproduction hard filter: standalone metrology instrument with no non-diagnostic function -> HOLD (consistent with RID-094). Revive only on a procurement/standard demanding it as a purchased capability.",ISSUE-014-099
```

## §6 — Updated Blocked-From-Deep-Dive List

**17 ideas blocked.** Grouped by status.

**HOLD (10)**

| RID | Idea | Score | Reason |
|---|---|---:|---|
| RID-067 | Detect-and-avoid module | 68 | FAA Part 108 BVLOS gating (TRIG-001 NPRM-only, speculative); decision P->W |
| RID-112 | Navigation-grade MEMS IMU | 67 | GPS-denied IMU demand gated by Part 108 (speculative) |
| RID-070 | C2 datalink module+RID/EC | 65 | Remote-ID/C2 demand gated by Part 108 (speculative) |
| RID-068 | eVTOL powertrain | 62 | eVTOL/AAM type-cert gated; trigger speculative |
| RID-069 | eVTOL thermal management | 62 | eVTOL/AAM type-cert gated; trigger speculative |
| RID-074 | Drone battery fast-swap system | 61 | Part 108 timing + OEM lock; trigger speculative |
| RID-077 | Surgical force-feedback system | 60 | HOLD — standalone-displacement clinical-outcome claim unsupported (preclinical/Intuitive-funded; surrogate endpoints only) |
| RID-072 | Heavy-lift cargo drone airframe | 51 | Part 108 + capex + China; trigger speculative |
| RID-094 | AM in-situ NDE | 50 | HOLD — diagnostic/NDE-overproduction; prior kill; no standalone procurement driver |
| RID-099 | Extreme-precision metrology instrument | 49 | HOLD — trips diagnostic/metrology-overproduction hard filter; no standalone procurement/standards driver |

**KILL (5)**

| RID | Idea | Score | Reason |
|---|---|---:|---|
| RID-036 | Chiplet thermal characterization | 62 | KILL — NRL award not verifiable (TRIG-005 speculative/medium); revive only on executed FPDS/SAM.gov contract |
| RID-071 | Drone airspace-management ADSP | 52 | KILL — software/services + Part 146/108 gated; permanent reason independent of trigger |
| RID-041 | Advanced-packaging metrology platform | 51 | KILL — diagnostic + cleanroom + giants; HBM4 microbump continuation strengthens only diagnostic role |
| RID-045 | Panel-level packaging handler | 49 | KILL — cleanroom + capex; no audit finding revives |
| RID-042 | Die-to-wafer hybrid bonder | 47 | KILL — JEDEC JESD270-4 (775um) locks it; hybrid bonding postponed >2029 (TRIG-007) |

**NEEDS_MORE_SOURCE (2)**

| RID | Idea | Score | Reason |
|---|---|---:|---|
| RID-087 | Point-of-care molecular cartridge | 46 | NEEDS_MORE_SOURCE — customer pain policy-context-only (Doc 551); also diagnostic |
| RID-091 | China-localized imaging detector | 45 | NEEDS_MORE_SOURCE — customer pain policy-context-only (Doc 551); cleanroom + China-only + export-incoherent |

## §7 — Updated Deep-Dive-Eligible List

**32 ideas eligible** for the 02f top-25 gate, highest score first. “Flag” notes a weakness to resolve at the gate or in the deep dive.

| RID | Idea | Score | Decision | Evidence | Flag for 02f / deep dive |
|---|---|---:|:--:|---|---|
| RID-002 | Capacitorless DC buffer+supercap | 84 | P | CLEARED_WITH_WEAKNESS | NVIDIA −30% company-supported; OCP Tier-2 |
| RID-003 | Solid-state DC breaker+e-fuse | 83 | P | CLEARED_WITH_WEAKNESS | OCP Tier-2 |
| RID-008 | Blind-mate liquid+power connector | 81 | P | CLEARED_WITH_WEAKNESS | OCP Tier-2 |
| RID-024 | GFM protection relay | 81 | P | CLEARED_WITH_WEAKNESS | none (SCORE-003 IEEE 2800.2 confirmed) |
| RID-001 | 800VDC busway | 80 | P | CLEARED_WITH_WEAKNESS | OCP Tier-2; UL857 >600V codification lag |
| RID-030 | Distribution-grade STATCOM (SiC) | 79 | P | CLEARED_WITH_WEAKNESS | NVIDIA company-supported (IEEE-2800.2 backstop) |
| RID-053 | Humanoid rotary actuator | 79 | P | CLEARED | none material (CLEARED) |
| RID-009 | GPU-aware power-orchestration SW | 77 | P | CLEARED_WITH_WEAKNESS | NVIDIA −30% company-supported |
| RID-029 | Grid-edge power-quality conditioner | 76 | P | CLEARED_WITH_WEAKNESS | NVIDIA company-supported (IEEE-2800.2 backstop) |
| RID-033 | CDU for 45C loops | 76 | P | CLEARED_WITH_WEAKNESS | OCP Tier-2 (SCORE-007 intact) |
| RID-034 | Microfluidic cold plate >1kW/cm2 | 76 | P | CLEARED_WITH_WEAKNESS | none (SCORE-007 thermal intact) |
| RID-111 | High-bandwidth piezo actuator | 72 | P | CLEARED | none (CLEARED, Tier-1 + patent) |
| RID-016 | Second-life battery repurposing | 71 | P | CLEARED | none (CLEARED, MIIT spec + UL1974 + NREL) |
| RID-100 | Automated optical-assembly cell | 70 | P | CLEARED | none (CLEARED, peer-reviewed) |
| RID-102 | Fusion-magnet HTS components | 69 | P | CLEARED_WITH_WEAKNESS | “largest” company-supported; tiny customer set |
| RID-015 | Thermal-storage module (700C) | 68 | W | CLEARED | none (CLEARED, Sandia/DOE G3P3) |
| RID-026 | Hybrid-plant controller | 67 | W | CLEARED_WITH_WEAKNESS | confirm HW/SW controller vs integration/consulting |
| RID-020 | Battery thermal-runaway suppression | 67 | W | CLEARED_WITH_WEAKNESS | UL9540A-test-driven/commoditized — competitive, not source |
| RID-040 | Datacenter waste-heat recovery | 66 | W | CLEARED_WITH_WEAKNESS | geography — EU/Germany-bounded driver; weak China wedge |
| RID-017 | Sodium-ion grid module | 65 | W | CLEARED | China-incumbent competition already priced |
| RID-032 | EV-fleet bidirectional charger | 63 | W | CLEARED | none (CLEARED, ISO 15118-20) |
| RID-104 | Fusion first-wall thermal mgmt | 62 | W | CLEARED_WITH_WEAKNESS | pre-commercial market already priced |
| RID-012 | Behind-the-meter firm-power interface | 62 | W | CLEARED | IEA figures are 2030 projections; borders integration |
| RID-022 | Microgrid DC-coupling hub | 61 | W | CLEARED_WITH_WEAKNESS | IEEE 2030.10 narrow/diffuse scope |
| RID-005 | Rack-level DC-DC module | 60 | W | CLEARED_WITH_WEAKNESS | OCP-adjacent Tier-2; commoditized |
| RID-051 | Advanced-packaging warpage controller | 58 | W | CLEARED_WITH_WEAKNESS | WEAKEST ADMIT — thin evidence, borders in-line metrology; confirm purchased-capability spec or KILL |
| RID-081 | FDA AI-enabled surgical subsystem | 57 | W | CLEARED_WITH_WEAKNESS | clinical-outcome benefit preclinical/company-funded — confirm-or-HOLD |
| RID-097 | Laser micro-machining cell | 56 | W | CLEARED_WITH_WEAKNESS | commoditized job-shop risk already priced |
| RID-088 | Robotic catheter actuation | 55 | W | CLEARED_WITH_WEAKNESS | component play; preclinical/company-funded benefit |
| RID-082 | Implantable neurostimulator power | 55 | W | CLEARED | FDA burden already priced |
| RID-115 | Wide-bandwidth DC current sensor | 53 | W | CLEARED_WITH_WEAKNESS | OCP Tier-2; diagnostic-adjacent — confirm functional vs standalone |
| RID-101 | Molten-salt-resistant alloy | 53 | W | CLEARED_WITH_WEAKNESS | timing — molten-salt deployment largely >2030 |

## §8 — Final Source-Audit Status Summary & Open Judgment Calls

**Where the audit (07b→07e) lands.** Every audit-affected idea now carries a verified evidence label and a score consistent with it. The corpus is unchanged at **397** counted sources (07b–07e added only `count_toward_300=no` evidence/monitoring rows). The re-score removed 41 soft points but changed the portfolio's shape only at the margin: one demotion (RID-067), two new HOLDs (RID-077, RID-099), one hardened kill (RID-071). The pursue tier is intact and led by the data-center power cluster.

**Tally among the 49 affected ideas (new):** decisions P15 / W26 / K8; evidence-status CLEARED_WITH_WEAKNESS 23 / CLEARED 9 / HOLD 10 / KILL 5 / NEEDS_MORE_SOURCE 2; eligible yes 32 / no 17.

**Two open judgment calls (both reversible — flagged for Tim to override before/at 02f):**

1. **Surgical force-feedback cluster (RID-077/081/088).** This phase puts the standalone console RID-077 on HOLD and keeps the two subsystem plays (RID-081/088) eligible-with-weakness. The alternative is to defer all three to the 02f gate at CLEARED_WITH_WEAKNESS and let the gate adjudicate the clinical-outcome question uniformly. Current choice errs strict on the one idea whose thesis is direct clinical displacement.
2. **RID-099 vs the metrology-overproduction filter.** RID-099 is moved to HOLD for consistency with RID-094. If the project wants to treat extreme-precision *dimensional/overlay* metrology as distinct from generic in-process monitoring, RID-099 could instead be deferred to 02f as CLEARED_WITH_WEAKNESS. Current choice applies the hard filter uniformly.

Additionally noted for 02f: **RID-051** is the weakest admit (thin evidence, borders in-line metrology) and should be the first confirm-or-kill at the gate; **RID-115** should be confirmed as a functional current-sense component rather than a standalone diagnostic instrument.

**Files updated this phase:** `scored_idea_database_repaired_2026_06_25.csv` (49 rows re-scored), `source_issue_tracker.csv` (25 issues routed 02e→02f; RID-099 issue→HOLD; judgment-call + drone-cap notes recorded). No `source_evidence_ledger.csv` change (no new corpus sources). 

**Next action:** re-upload the corrected files to Project Files, then run `prompts/04_diligence_scoring/02f_top25_eligibility_gate.md` in a fresh chat. **Deep dives stay locked until 02f clears.**
