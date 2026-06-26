# 02f — Top-25 Deep-Dive Eligibility Gate (RE-RUN after ISSUE-018)

_Phase 02f, second pass. Date: 2026-06-25. This re-run folds in the ISSUE-018 source-audit confirmation pass, which assigned evidence labels to the 8 previously-unaudited PURSUE ideas. Gate only — no scores changed (labels carry each idea's original score), no ideas generated. Supersedes the first 02f run._

## What changed since the first 02f run

The ISSUE-018 confirmation pass labelled the 8 unaudited PURSUE ideas: **5 cleared, 3 went to HOLD.**

| RID | Idea | ISSUE-018 label | Result |
|---|---|---|---|
| RID-004 | MV SiC solid-state transformer | CWW | → enters top-25 |
| RID-019 | LDES inverter GFM controls | CWW | → enters top-25 |
| RID-055 | Cobot SSM safety controller | CLEARED | → enters top-25 |
| RID-056 | PFL force-limiting joint + F/T sensor | CWW | → enters top-25 |
| RID-078 | Microneedle lactate sensor + multiplex | CLEARED | → enters top-25 |
| RID-018 | Supercapacitor fast-frequency module | HOLD | → watchlist (HOLD) |
| RID-013 | LDES power-conversion system | HOLD | → watchlist (HOLD) |
| RID-035 | Two-phase immersion module | HOLD | → watchlist (HOLD) |

**Net effect on the gate:**
- Eligible pool **32 → 37** (+5 newly cleared: RID-004, RID-019, RID-055, RID-056, RID-078).
- All 5 newcomers land **inside** the top-25 (ranks 9–16), so **5 audited ideas are displaced** below the cut: RID-032, RID-012, RID-104, RID-022, RID-005 (now ranks 26–30).
- Top-25 cut **rises from score 60 (RID-005) to score 65 (RID-017)** — a stronger core list.
- Watchlist **9 → 12** (+RID-018, RID-013, RID-035, all HOLD). Excluded unchanged at 8.
- Reconciliation: **37 eligible + 12 watchlist + 8 excluded = 57** (49 audited + 8 confirmation-pass).

---

## 1. Eligible top-25 (ranked by repaired score)

Tiebreak: score desc → original score desc → idea_id. **NEW** = newly cleared via ISSUE-018.

| # | RID | Idea | Score | Evidence | Dec | New? | Flag for deep dive |
|--:|---|---|--:|---|:--:|:--:|---|
| 1 | RID-002 | Capacitorless DC buffer+supercap | 84 | CWW | P |  | NVIDIA −30% company-supported; OCP Tier-2 |
| 2 | RID-003 | Solid-state DC breaker+e-fuse | 83 | CWW | P |  | OCP Tier-2 |
| 3 | RID-008 | Blind-mate liquid+power connector | 81 | CWW | P |  | OCP Tier-2 |
| 4 | RID-024 | GFM protection relay | 81 | CWW | P |  | none — SCORE-003 IEEE 2800.2 confirmed |
| 5 | RID-001 | 800VDC busway | 80 | CWW | P |  | OCP Tier-2; UL857 >600V codification lag |
| 6 | RID-030 | Distribution-grade STATCOM (SiC) | 79 | CWW | P |  | NVIDIA company-supported (IEEE 2800.2 backstop) |
| 7 | RID-053 | Humanoid rotary actuator | 79 | CLEARED | P |  | none material (CLEARED) |
| 8 | RID-009 | GPU-aware power-orchestration SW | 77 | CWW | P |  | NVIDIA −30% company-supported |
| 9 | RID-004 | MV SiC solid-state transformer | 77 | CWW | P | **NEW** | NEW — pre-commercial; near-term purchasable-subsystem pull + efficiency figures company/Tier-3 |
| 10 | RID-029 | Grid-edge power-quality conditioner | 76 | CWW | P |  | NVIDIA company-supported (IEEE 2800.2 backstop) |
| 11 | RID-033 | CDU for 45C loops | 76 | CWW | P |  | OCP Tier-2 (SCORE-007 intact) |
| 12 | RID-034 | Microfluidic cold plate >1kW/cm2 | 76 | CWW | P |  | none (SCORE-007 thermal intact) |
| 13 | RID-019 | LDES inverter GFM controls | 75 | CWW | P | **NEW** | NEW — GFM conformity driver is IBR-wide, not LDES-specific |
| 14 | RID-055 | Cobot SSM safety controller | 74 | CLEARED | P | **NEW** | NEW — clean: ISO 10218:2025 mandates SSM; confirm buyers procure a discrete controller vs integrated |
| 15 | RID-056 | PFL force-limiting joint + F/T sensor | 74 | CWW | P | **NEW** | NEW — ISO/TS 15066 biomechanical limits flagged "preliminary"; subsystem is a market inference |
| 16 | RID-078 | Microneedle lactate sensor + multiplex | 73 | CLEARED | P | **NEW** | NEW — clean sensing demo; clinical-outcome/long-wear/WTP + dense microneedle IP are separate risks |
| 17 | RID-111 | High-bandwidth piezo actuator | 72 | CLEARED | P |  | none (CLEARED — Tier-1 + patent) |
| 18 | RID-016 | Second-life battery repurposing | 71 | CLEARED | P |  | none (CLEARED — MIIT spec + UL1974 + NREL) |
| 19 | RID-100 | Automated optical-assembly cell | 70 | CLEARED | P |  | none (CLEARED — peer-reviewed) |
| 20 | RID-102 | Fusion-magnet HTS components | 69 | CWW | P |  | "largest" company-supported; tiny customer set |
| 21 | RID-015 | Thermal-storage module (700C) | 68 | CLEARED | W |  | none (CLEARED — Sandia/DOE G3P3) |
| 22 | RID-026 | Hybrid-plant controller | 67 | CWW | W |  | confirm HW/SW controller vs integration/consulting |
| 23 | RID-020 | Battery thermal-runaway suppression | 67 | CWW | W |  | UL9540A-test-driven/commoditized — competitive risk, not source |
| 24 | RID-040 | Datacenter waste-heat recovery | 66 | CWW | W |  | EU/Germany-bounded driver; weak China wedge |
| 25 | RID-017 | Sodium-ion grid module | 65 | CLEARED | W |  | China-incumbent competition already priced |

The data-center-power and grid/inverter clusters still lead (ranks 1–13 all ≥75). The five ISSUE-018 entrants slot into the upper-middle: **RID-004** (#9, MV SiC SST), **RID-019** (#13, LDES GFM controls), and the cobot-safety pair **RID-055/056** (#14–15) plus the **RID-078** microneedle sensor (#16).

### Eligible but below the top-25 cut (ranks 26–37)

Still eligible (CLEARED/CWW); admit only if the top-25 is exhausted. The 5 newly-displaced audited ideas sit at the top of this band.

| # | RID | Idea | Score | Flag |
|--:|---|---|--:|---|
| 26 | RID-032 | EV-fleet bidirectional charger | 63 | none (CLEARED — ISO 15118-20) |
| 27 | RID-012 | Behind-the-meter firm-power interface | 62 | IEA figures are 2030 projections; borders integration |
| 28 | RID-104 | Fusion first-wall thermal mgmt | 62 | pre-commercial market already priced |
| 29 | RID-022 | Microgrid DC-coupling hub | 61 | IEEE 2030.10 narrow/diffuse scope |
| 30 | RID-005 | Rack-level DC-DC module | 60 | OCP-adjacent Tier-2; commoditized |
| 31 | RID-051 | Advanced-packaging warpage controller | 58 | WEAKEST ADMIT — thin evidence, borders in-line metrology; first confirm-or-kill |
| 32 | RID-081 | FDA AI-enabled surgical subsystem | 57 | clinical-outcome gate resolved: ISO-10218/FDA basis only |
| 33 | RID-097 | Laser micro-machining cell | 56 | commoditized job-shop risk already priced |
| 34 | RID-088 | Robotic catheter actuation | 55 | component play; no clinical-outcome claim |
| 35 | RID-082 | Implantable neurostimulator power | 55 | FDA burden already priced |
| 36 | RID-101 | Molten-salt-resistant alloy | 53 | molten-salt deployment largely >2030 |
| 37 | RID-115 | Wide-bandwidth DC current sensor | 53 | diagnostic-adjacent — confirm functional vs standalone |

> The four 07e-flagged borderline items (RID-051 #31, RID-081 #32, RID-088 #34, RID-115 #37) remain **below the cut** — their gate conditions (from ISSUE-019) still ride into any future deep dive but do not touch the core 25.

---

## 2. Watchlist appendix — attractive but blocked (HOLD)

| RID | Idea | Score | Blocked — unlock condition |
|---|---|--:|---|
| RID-018 | Supercapacitor fast-frequency module | 75 | NEW (ISSUE-018) — peer-reviewed tens-of-MW 0.1–20 Hz AI-training oscillation measurement + a supercapacitor-specific deployment (today: preprints + NVIDIA electrolytic-cap figures only) |
| RID-013 | LDES power-conversion system | 73 | NEW (ISSUE-018) — Tier-1/2 source establishing a distinct PCS subsystem market for non-Li LDES (today: DOE pull is technology-inclusive/system-level) |
| RID-035 | Two-phase immersion module | 72 | NEW (ISSUE-018) — hyperscaler two-phase immersion procurement at scale + a confirmed non-PFAS two-phase fluid pathway (today: lab-stage, displaced by direct-to-chip + Novec phase-out) |
| RID-067 | Detect-and-avoid module | 68 | FAA Part 108 BVLOS final rule (TRIG-001) |
| RID-112 | Navigation-grade MEMS IMU | 67 | FAA Part 108 BVLOS final rule (TRIG-001) |
| RID-070 | C2 datalink module+RID/EC | 65 | FAA Part 108 BVLOS final rule (TRIG-001) |
| RID-068 | eVTOL powertrain | 62 | FAA Part 108 BVLOS final rule (TRIG-001) |
| RID-069 | eVTOL thermal management | 62 | FAA Part 108 BVLOS final rule (TRIG-001) |
| RID-074 | Drone battery fast-swap system | 61 | FAA Part 108 BVLOS final rule (TRIG-001) |
| RID-077 | Surgical force-feedback system | 60 | independent (non-Intuitive) patient-outcome RCT |
| RID-072 | Heavy-lift cargo drone airframe | 51 | FAA Part 108 BVLOS final rule (TRIG-001) |
| RID-099 | Extreme-precision metrology instrument | 49 | procurement/standard demanding extreme-precision metrology as a purchased standalone capability |

- **Drone / air-mobility cluster (7):** capped under TRIG-001 (FAA Part 108 BVLOS still NPRM-only). Watchlist-only; revisit on a FINAL rule.
- **RID-077 (surgical console):** independent patient-outcome RCT.
- **RID-099 (extreme-precision metrology):** standalone procurement/standards driver (diagnostic-overproduction filter).
- **NEW from ISSUE-018 — RID-018, RID-013, RID-035:** see unlock conditions above. RID-035 (two-phase immersion) and RID-018 (supercapacitor module) were the two the confirmation pass confirmed as *materially weaker than their PURSUE rating implied* — two-phase immersion is displaced by direct-to-chip and PFAS/Novec phase-out; the supercapacitor AI-oscillation rationale rests on preprints + NVIDIA's (electrolytic-capacitor) figures.
- **Cross-reference — RID-094** (AM in-situ NDE): decision = KILL but evidence HOLD (revivable); listed under Excluded to match `rejected_ideas.md`.

---

## 3. Excluded (decision = KILL)

Unchanged by this re-run.

| RID | Idea | Score | Evidence | Reason / revival condition |
|---|---|--:|---|---|
| RID-036 | Chiplet thermal characterization | 62 | KILL | NRL/Navy contract not verifiable (NOI + DARPA prime only; TRIG-005). Revive on an executed USAspending/FPDS/SAM.gov contract. |
| RID-071 | Drone airspace-management ADSP | 52 | KILL | Software/services structurally gated by FAA Part 146/108 (hardened HOLD→KILL in 02e). |
| RID-041 | Advanced-packaging metrology platform | 51 | KILL | Diagnostic/metrology-only, cleanroom-heavy, incumbents own the socket. |
| RID-094 | AM in-situ NDE | 50 | HOLD (revivable) | Diagnostic/in-situ-NDE overproduction. evidence_status=HOLD → REVIVABLE on a procurement/standard for AM in-situ NDE as a purchased capability. |
| RID-045 | Panel-level packaging handler | 49 | KILL | Cleanroom + >$2M capex vs entrenched OEMs; no first-customer wedge. |
| RID-042 | Die-to-wafer hybrid bonder | 47 | KILL | HBM4 stays on microbumps (JEDEC JESD270-4); D2W pull moves past 2029 (TRIG-007). |
| RID-087 | Point-of-care molecular cartridge | 46 | NEEDS_MORE_SOURCE | Pain is policy-context-only (Doc 551); no independent buyer/workflow source; diagnostic, NMPA-gated. |
| RID-091 | China-localized imaging detector | 45 | NEEDS_MORE_SOURCE | Pain policy-context-only (Doc 551); cleanroom-high, China-only, export-incoherent. |

---

## 4. Count of eligible ideas

**37 eligible** (CLEARED 11, CLEARED_WITH_WEAKNESS 26). Top-25 presented; ranks 26–37 in reserve. Watchlist 12; excluded 8.

## 5. Fewer than 25 eligible?

**No — 37.** The list is not padded; the cut is now at score 65, so the deep-dive phase will examine a uniformly stronger core (every top-25 idea scores ≥65, vs ≥60 before).

---

## 6. CSV-ready updates

**`02f_rerun_scored_db_resolved_rows.csv`** — these 8 rows **replace** the 8 `pending_confirmation` rows added by the first 02f run in `scored_idea_database_repaired_2026_06_25.csv` (LF, no BOM). They now carry the resolved `evidence_status` (5 cleared / 3 HOLD), `top25_eligible` (yes/no), `new_decision` (P for cleared, W for HOLD), and the ISSUE-018 justification in `repair_notes`.

**`02f_rerun_issue_tracker_update.csv`** — replacement row for **ISSUE-018** in `source_issue_tracker.csv` (CRLF, no BOM): status `RESOLVED` (5 CLEARED/CWW → eligible; 3 HOLD → watchlist). ISSUE-019 (the RID-051/081/088/115 borderline conditions) is unchanged and still rides into the deep dive.

No change to `source_evidence_ledger.csv`: the ISSUE-018 pass was label-only and the corpus stays at 397 counted sources (the confirmation sources are evidence/standards rows, `count_toward_300=no`). If you want, I can also generate ledger rows for the specific Tier-1/2 sources the pass surfaced (ISO 10218:2025, IEEE 2800.2-2026, ORNL MV-SST, the microneedle papers, etc.) so they're traceable in the ledger.

---

## Gate decision

**02f CLEARS.** The eligible top-25 is final for this pass (37 eligible, cut at score 65). Both open judgment calls from 02e are now fully closed: the surgical cluster (judgment call #1, via ISSUE-019) and the 8 unaudited PURSUE ideas (judgment call #2, via ISSUE-018). **Deep dives are now unlocked.**

**Next action:** re-upload the corrected `scored_idea_database_repaired_2026_06_25.csv` (8 rows replaced) and `source_issue_tracker.csv` (ISSUE-018 resolved), then run `prompts/05_deep_dives_red_team/01a_top25_deep_dive_after_source_repair.md` in a fresh chat. Carry the per-idea flags above (esp. RID-051 first confirm-or-kill, and the ISO-10218/FDA-basis condition on RID-081/088) into the deep dives.