# DIVERSITY FILTER & ANTI-BIAS AUDIT (PHASE 15)

**Input:** 124 raw ideas (RID-001…RID-124) from Phase 14.
**Output:** filtered set of **79 ideas** (34 hard removals + 11 merges → 45 culled). No attractiveness scoring yet (that is Phase 16). Rule followed: be harsh, remove generic, preserve diversity.

---

## 1. BIAS PROBLEMS FOUND (10 audit questions)

1. **Too biased toward PhD topic (GaN/WBG/SiC/plasma/fusion/cleanroom)?** **No.** Only ~12 of 124 touch it (RID-004, 010, 030, 031, 049, 101–107, 111), and they are framed as transferable power-electronics/extreme-environment/instrumentation skills. After filtering, the fusion/nuclear sub-cluster was the most over-built relative to founder fit (slow qual, capex-heavy) and was thinned hardest (10→4).
2. **Too many diagnostics/test/monitoring?** **Yes — the single biggest bias.** 24 DIAG-tagged ideas, and a tail of "monitor/inspection" items whose failure mode was literally "OEM owns it / built into the host / commoditized." This is exactly the monitoring-overproduction trap the founder flagged. Cut DIAG from 24 → ~9.
3. **Too many generic AI dashboards?** **Mild.** A handful of software-centric ideas (RID-025 interconnection accelerator, RID-027 VPP node, RID-063 industrial-vision QC) leaned generic-software with weak moats. Removed.
4. **Too many cleanroom-heavy?** **Moderate.** The semiconductor *process-equipment* ideas (D2W bonder, panel handler, precision valve, photonic alignment, KGD test) need a fab. Kept the lower-burden metrology and the one China-localization subsystem with the strongest chokepoint; cut the rest.
5. **Stanford-IP dependent?** **No.** None rely on Stanford IP.
6. **Too many commodity/weak-differentiation markets?** **Yes.** ~15 ideas had incumbent-owns / commoditized / vendor-bundles failure modes (RDHx, mobile-manipulator base, RID beacon, ag-spray, smoke evacuation, dispensing, weld inspection, fiber sensor, cryocooler, magnetic bearing). Removed or merged.
7. **Enough standalone products?** **Yes,** and strengthened by the cull: ~70 of 79 survivors are standalone products/subsystems (~89%).
8. **Enough China-first but US-expandable?** **Yes.** ~28 China-first survivors, ~37 with a credible US-expansion path; large overlap preserved.
9. **Enough feasible for 2026–2028 R&D piloting?** **Yes** — the cull removed the worst TRL/timeline offenders (sCO2 turbine, ATF cladding, organ-on-chip kept only as a China-biomanufacturing platform, TPS material).
10. **Enough capable of 2029/2030 launch?** **Yes** — survivors skew toward 2029-launchable; the 2030-stretch items were thinned, with a few high-conviction extreme-environment exceptions retained (fusion magnet/first-wall, molten-salt alloy).

**Net bias correction:** the universe was over-weighted toward (a) monitoring/inspection tools and (b) commodity hardware with no moat. Both were cut hard. Domain breadth, China-first/US-expandable balance, and standalone-product share were preserved or improved. Biomedical was deliberately thinned (16→10) because most bio ideas were monitoring-overproduction or incumbent-dominated; the surviving 10 still span surgical force-feedback, microneedle therapeutics, implant power, imaging-detector localization, biomanufacturing, catheter robotics, and organ-on-chip, so bio *diversity* is intact even though the absolute count drops below the Phase-14 generation floor of 15 (relaxation flagged in §6).

---

## 2. IDEAS TO REMOVE (34 hard cuts)

| RID | Name | Removal reason |
|---|---|---|
| 006 | Power-electronics reliability qual tool | DIAG; "OEM in-house" — no durable wedge (MC18 better served by RID-018/024) |
| 011 | ±400VDC isolation monitor | DIAG; built into PSU — commodity |
| 021 | CAES/LAES expander | Capex-heavy turbomachinery; weak founder fit; LDES covered by 013–015 |
| 025 | Interconnection-study accelerator | Fatal failure mode: bottleneck is regulatory, not technical |
| 027 | VPP aggregation edge node | Generic software; "software-only rivals" |
| 028 | Dynamic line-rating sensor | DIAG; slow adoption; overlaps transformer monitor (023) |
| 031 | Substation SiC retrofit module | Overlaps STATCOM (030); utility-procurement drag |
| 038 | Coolant leak-detection mesh | DIAG; built into CDU |
| 039 | Rear-door heat exchanger | Commodity; leapfrogged by full-liquid |
| 046 | China CMP endpoint sensor | DIAG; entity-list risk; RID-047 is the stronger China-subsystem play |
| 048 | Precision vacuum valve | Cleanroom; reliability risk; keep RID-047 only as China-localization subsystem |
| 050 | Chiplet KGD test | DIAG; incumbent ATE (Advantest/Teradyne) |
| 059 | Cobot safety vision scanner | DIAG; incumbent scanners; cobot safety covered by SSM controller (055) |
| 060 | Mobile-manipulator base | Crowded market, no moat |
| 063 | Industrial AI vision QC | DIAG; commoditized |
| 065 | Robot joint health monitor | DIAG; OEM owns |
| 075 | Counter-UAS detection | DIAG; mitigation-regulation dependency; drone-sensing covered by DAA (067) |
| 076 | Precision-ag spray controller | DJI dominance |
| 083 | Portable dialysis fluidics | 2030-stretch + heavy regulatory risk |
| 085 | Wearable cardiac patch | Monitoring overproduction |
| 089 | Cuff-less continuous BP module | Monitoring overproduction; accuracy/regulatory |
| 090 | Surgical smoke evacuation | Low differentiation |
| 096 | Precision dispensing robot | Incumbents (Nordson) |
| 098 | Weld-quality AI inspection | DIAG; commoditized |
| 103 | Accident-tolerant fuel cladding | NRC/NNSA timeline far beyond 2030; nuclear-materials covered by molten-salt alloy (101) |
| 105 | Cryogenic power feedthrough | Niche; covered within fusion-magnet scope (102) |
| 107 | High-temp SiC reactor instrumentation | DIAG; long qual; rad-hard covered by readout ASIC (106) |
| 108 | Aerospace thermal-protection material | Qual-heavy; weak fit |
| 109 | sCO2 power-cycle turbomachine | TRL/capex; far from founder fit |
| 113 | Fiber-optic distributed sensor | DIAG; incumbents |
| 114 | Magnetic-bearing controller | Niche; no clear beachhead |
| 116 | Soft-robotic actuator | Durability risk; overlaps actuator family with weaker angle |
| 117 | Phased-array ultrasonic NDE | DIAG; incumbents; NDE covered by AM in-situ (094) |
| 118 | Compact cryocooler | Incumbents; niche |

---

## 3. IDEAS TO MERGE (11 merges → folded into a stronger survivor)

| Merge | Into | Rationale |
|---|---|---|
| RID-007 supercap ride-through | **RID-002** capacitorless DC buffer | Same job: rack-level GPU-transient energy buffering; combine active-decoupling + supercap into one buffer family |
| RID-010 800VDC e-fuse chip | **RID-003** solid-state DC breaker | Both 800VDC fault-interruption devices |
| RID-043 microbump inspection AI | **RID-041** hybrid-bonding metrology | One advanced-packaging metrology/inspection platform |
| RID-044 backside-thinning metrology | **RID-041** hybrid-bonding metrology | Same platform, added measurement mode |
| RID-052 photonic-IC alignment | **RID-100** automated optical-assembly cell | Both sub-µm active optical alignment |
| RID-064 6-axis F/T sensor | **RID-056** PFL force-limiting joint | Force-limiting joint requires the F/T sensing; one safe-actuation product |
| RID-073 RID/EC beacon | **RID-070** C2 datalink module | Combine into one drone comms/conspicuity module |
| RID-079 multiplex microneedle | **RID-078** microneedle lactate sensor | One microneedle biosensor platform (multi-analyte option) |
| RID-084 surgical haptic console | **RID-077** surgical force-sensing instrument | One surgical force-feedback system (instrument tip + master console) |
| RID-110 national-lab sole-source instrument | **RID-036** chiplet thermal-characterization (SSTR/FDTR) | Same instrument, same buyer family (NRL/NIST FAR 6.302) |
| RID-122 sensor-fusion DAA safety module | **RID-067** detect-and-avoid sensor suite | Certified fusion is part of the DAA module |

---

## 4. IDEAS TO STRENGTHEN (top survivors — sharpen before scoring)

1. **RID-001 800VDC busway** — narrow first product to a specific blind-mate ±400VDC busbar segment for the OCP Mt Diablo / Deschutes rack; name Vertiv or Schneider as design partner; add a quantified copper-savings spec vs 54V as the wedge.
2. **RID-002 capacitorless DC buffer (+supercap)** — anchor explicitly to GB200/Vera-Rubin power-oscillation traces (Choukse arXiv:2508.14318); define the 0.1–20 Hz attenuation target as the acceptance metric.
3. **RID-003 solid-state DC breaker (+e-fuse)** — pin the white-space: OCP Diablo 400 has no mature 800VDC protection; target sub-µs trip + arc-fault as the qualification claim.
4. **RID-036 chiplet thermal characterization (+lab-instrument)** — lead with the NRL FAR 6.302 sole-source precedent (N00173-25-RFI-MF18, Laser Thermal Analysis) as the beachhead procurement; extend to NIST/Sandia/ORNL.
5. **RID-041 advanced-packaging metrology platform (+inspection +thinning)** — position against the HBM4 hybrid-bonding postponement; define the buried-void/overlay detection limit (sub-100 nm) as the differentiator vs Onto/AMAT.
6. **RID-053 humanoid rotary actuator** — quantify torque density and target a merchant "engine-supplier" niche; cite the 40–60% BOM and roller-screw cost-down ($3,000→$800) as the willingness-to-pay basis.
7. **RID-055 cobot SSM safety controller** — tie directly to ISO 10218-1/-2:2025 PFL/SSM limits (Feb 2025); target PLd/SIL2 certification as the moat.
8. **RID-067 DAA module (+fusion safety)** — anchor to FAA Part 108 DAA mandate; make the first product a certifiable small-UAS DAA sensor+fusion unit for a named BVLOS logistics operator.
9. **RID-077 surgical force-feedback system (+console)** — lead with da Vinci 5 validation (up-to-43% less tissue force, Awad et al., *Surg Endosc* 2025) as proof of willingness-to-pay; target a non-Intuitive platform OEM.
10. **RID-101 molten-salt-resistant alloy components** — anchor to China's 110 GW-by-2030 nuclear build (15th FYP) as China-first; define the 700°C salt-corrosion lifetime spec as the wedge; flag the long qualification cycle honestly.
11. **RID-013 LDES power-conversion system** — anchor to DOE Long Duration Storage Shot (90% cost cut by 2030); name Form Energy/ESS as integration partners; target the BOS cost-share as the entry.
12. **RID-091 China-localized imaging detector** — anchor to MOF/MIIT Document 551 (100% domestic for 137/178 categories) forced-substitution; name the detector subsystem and a Chinese OEM buyer.

---

## 5. FINAL FILTERED LIST (79 ideas, grouped by domain)

**A — Data-center power (8):** 001 800VDC busway · 002 capacitorless DC buffer (+supercap) · 003 solid-state DC breaker (+e-fuse) · 004 MV SiC solid-state transformer · 005 rack-level DC-DC module · 008 blind-mate liquid+power connector · 009 GPU-aware power-orchestration SW · 012 behind-the-meter firm-power interface

**B — Energy storage / LDES / BOS (9):** 013 LDES power-conversion system · 014 iron-air BOS · 015 thermal-storage charge/discharge module · 016 second-life battery repurposing system · 017 sodium-ion grid module · 018 supercapacitor fast-frequency module · 019 LDES inverter GFM controls · 020 battery thermal-runaway suppression module · 022 microgrid DC-coupling hub

**C — Grid / DER / transformer (6):** 023 transformer health monitor *(DIAG, strengthen)* · 024 GFM protection relay · 026 hybrid-plant controller · 029 grid-edge power-quality conditioner · 030 distribution-grade STATCOM · 032 EV-fleet bidirectional charger

**D — Data-center thermal / cooling (6):** 033 CDU for 45 °C loops · 034 microfluidic cold plate · 035 two-phase immersion module · 036 chiplet thermal characterization SSTR/FDTR (+lab instrument) · 037 thermal interface material · 040 datacenter waste-heat recovery

**E — Semiconductors / packaging / metrology (6):** 041 advanced-packaging metrology platform (+inspection +thinning) · 042 die-to-wafer hybrid bonder · 045 panel-level packaging handler · 047 precision RF power generator (China-localized) · 049 rad-hard SiC power device · 051 advanced-packaging warpage controller

**F — Robotics / cobots / humanoid (9):** 053 humanoid rotary actuator · 054 humanoid tactile skin · 055 cobot SSM safety controller · 056 PFL force-limiting joint (+F/T sensor) · 057 humanoid power subsystem · 058 dexterous hand mechanism · 061 humanoid edge-inference module · 062 magnet-free actuator · 066 exoskeleton actuation unit

**G — Low-altitude / drones / eVTOL (7):** 067 detect-and-avoid module (+fusion safety) · 068 eVTOL powertrain · 069 eVTOL thermal management · 070 C2 datalink module (+RID/EC) · 071 drone airspace-management ADSP · 072 heavy-lift cargo drone airframe · 074 drone battery fast-swap system

**H — Biomedical (10):** 077 surgical force-feedback system (+console) · 078 microneedle lactate sensor (+multiplex) · 080 closed-loop drug-delivery microneedle · 081 FDA AI-enabled surgical subsystem · 082 implantable neurostimulator power · 086 organ-on-chip platform · 087 point-of-care molecular cartridge *(DIAG)* · 088 robotic catheter actuation · 091 China-localized imaging detector · 092 bioreactor process control

**I — Advanced manufacturing / quality automation (6):** 093 battery electrode coating inspection *(DIAG)* · 094 AM in-situ NDE *(DIAG)* · 095 battery dry-electrode equipment · 097 laser micro-machining cell · 099 extreme-precision metrology instrument *(DIAG)* · 100 automated optical-assembly cell (+photonic alignment)

**J — Extreme-environment (4):** 101 molten-salt-resistant alloy components · 102 fusion-magnet HTS components · 104 fusion first-wall thermal management · 106 rad-hard sensor readout ASIC

**K — Sensors / actuation / control (3):** 111 high-bandwidth piezo actuator · 112 navigation-grade MEMS IMU · 115 wide-bandwidth DC current sensor *(DIAG)*

**L — High-reliability embedded AI / functional safety (5):** 119 AI functional-safety runtime · 120 safety-rated edge AI accelerator · 121 redundant autonomy safety controller · 123 embedded AI watchdog for medical AI · 124 grid-edge AI controller (safety)

---

## 6. QUOTA-COMPLIANCE TABLE (filtered set of 79)

| Quota | Phase-14 floor/ceiling | Filtered count | Status |
|---|---|---|---|
| Total ideas | 70–90 | **79** | ✅ in range |
| Standalone products (non-diagnostic) | ≥ majority | **~70 (89%)** | ✅ improved |
| Diagnostic/test/inspection/monitoring | as few as defensible | **9** (023, 036, 041, 067, 087, 093, 094, 099, 115) | ✅ cut from 24 |
| Outside semis/GaN/WBG/fusion/cleanroom | ≥40 | **~55** | ✅ |
| China-first / China-early | ≥25 | **~28** | ✅ |
| US-expansion path | ≥25 | **~37** | ✅ |
| Near-zero cleanroom | ≥25 | **~50** | ✅ |
| Weird / high-end / extreme-performance | ≥20 | **~22** (incl. extreme-performance subsystems 002/003/004/034/054/077 + 040/045/047/049/062/082/097/099/100/101/102/104/106/111/112/115) | ✅ |
| AI / robotics / automation | ≥20 | **~26** (F9 + G-autonomy + L5 + 081/093/094/100) | ✅ |
| Energy / power / grid / data-center | ≥20 | **~29** (A8+B9+C6+D6) | ✅ |
| Semiconductor / electronics / hardware | ≥20 | **~20** (E6 + 004/030/034/036/037/049/061/106/111/115/120) | ✅ (tight) |
| Biomedical / health / bio-instrumentation | ≥15 | **10** | ⚠️ **relaxed 15→10** — see note |
| PhD-topic (GaN/WBG/fusion/cleanroom) over-representation | keep low | **~11 (14%)** | ✅ not over-represented |

**Biomedical relaxation note:** the harsh filter (rule: "be harsh, remove generic") cut biomedical from 16 to 10 because the removed bio ideas (cardiac patch, cuff-less BP, smoke evacuation, portable dialysis) were monitoring-overproduction or incumbent-dominated with weak moats — precisely the founder's stated anti-pattern. The surviving 10 still cover seven distinct bio sub-areas (surgical force-feedback, microneedle therapeutics, implant power, imaging-detector localization, biomanufacturing/bioreactor, catheter robotics, organ-on-chip), so biomedical *diversity* is preserved even though the absolute count falls below the Phase-14 generation floor. If you prefer to hold the ≥15 floor, the cleanest restorations would be RID-085 (cardiac patch) and RID-089 (cuff-less BP) reframed as non-monitoring closed-loop products — but as currently scoped they are monitoring plays and were cut on purpose.

---

## 7. CSV-READY ROWS — updated `raw_idea_database.csv`

Schema note: the full 13 fields for every surviving idea persist unchanged from the Phase-14 `raw_idea_database.csv`. This update adds three columns — `status` (keep), `merged_from` (RIDs folded in), `strengthen_note` — and the survivors are the 79 listed in §5. Removed and merged-away IDs are NOT deleted from the historical DB; their `status` is set to `removed` or `merged_into:RID-xxx` and they are logged in `rejected_ideas.md` (§8).

Header: `idea_id,status,merged_from,name,domain,strengthen_note`

```
RID-001,keep,,800VDC busway,DC-power,"Narrow to blind-mate ±400VDC busbar for OCP Diablo/Deschutes; name Vertiv/Schneider; quantify Cu savings vs 54V"
RID-002,keep,RID-007,capacitorless DC buffer + supercap ride-through,DC-power,"Anchor to GB200/Vera-Rubin oscillation traces; define 0.1-20Hz attenuation acceptance metric"
RID-003,keep,RID-010,solid-state DC breaker + e-fuse,DC-power,"Pin OCP Diablo 400 protection white-space; sub-us trip + arc-fault qualification claim"
RID-004,keep,,MV SiC solid-state transformer,DC-power,"Lead with MV-transformer 3yr lead-time pain; Microchip 3.3kV modules; 1MW demo target"
RID-005,keep,,rack-level DC-DC module,DC-power,"Name Foxconn Kaohsiung-1; density spec kW/in3"
RID-008,keep,,blind-mate liquid+power connector,DC-power,"Hot-swap at 1MW; OCP-native dock"
RID-009,keep,,GPU-aware power-orchestration SW,DC-power/AI,"Tie to NERC large-load oscillation report; CoreWeave pilot"
RID-012,keep,,behind-the-meter firm-power interface,DC-power/energy,"Anchor to 2290GW LBNL queue; Bloom related-party concentration as WTP context"
RID-013,keep,,LDES power-conversion system,energy,"Anchor DOE Storage Shot 90%-by-2030; Form/ESS partner; BOS cost-share entry"
RID-014,keep,,iron-air balance-of-system,energy,"Form Energy site demo; water/thermal mgmt skid"
RID-015,keep,,thermal-storage charge/discharge module,energy/extreme,"Sandia G3P3; 700C dispatch"
RID-016,keep,,second-life battery repurposing system,energy/AI,"China EV-scrap volume; grading SW + reassembly line"
RID-017,keep,,sodium-ion grid module,energy,"China Na-ion lead; cold-climate firm; DOE Na pathway"
RID-018,keep,,supercapacitor fast-frequency module,energy,"IEEE 2800.2-2026 fast-response; HIL"
RID-019,keep,,LDES inverter GFM controls,energy,"IEEE 2800.2 conformity test; black-start"
RID-020,keep,,battery thermal-runaway suppression module,energy/bio,"UL9540A abuse test; propagation halt"
RID-022,keep,,microgrid DC-coupling hub,energy,"China zero-carbon parks (15th FYP); single-stage DC"
RID-023,keep,,transformer health monitor,grid,"DIAG; lead with 3yr replacement lead-time; failure-prediction; utility pilot"
RID-024,keep,,GFM protection relay,grid,"IEEE 2800.2-2026; fault discrimination vs legacy relays"
RID-026,keep,,hybrid-plant controller,grid/energy,"CAISO 93% hybrid; real-time co-optimization"
RID-029,keep,,grid-edge power-quality conditioner,grid,"arXiv:2508.16457 wide-area oscillation; 0.1-20Hz damping"
RID-030,keep,,distribution-grade STATCOM,grid/semi,"SiC fast-VAR for DER-heavy feeders"
RID-032,keep,,EV-fleet bidirectional charger,grid,"China EV scale; SST bidirectionality; depot pilot"
RID-033,keep,,CDU for 45C loops,thermal,"OCP Deschutes ~2MW/500GPM spec; rack-loop pilot"
RID-034,keep,,microfluidic cold plate,thermal/semi,">1kW/cm2; Kyber liquid-only; thermal rig"
RID-035,keep,,two-phase immersion module,thermal,"CoolIT/Accelsius 250kW demos; fluorochemical phase-out risk noted"
RID-036,keep,RID-110,chiplet thermal characterization SSTR/FDTR + lab instrument,thermal/semi,"Lead NRL FAR 6.302 sole-source N00173-25-RFI-MF18; extend NIST/Sandia/ORNL"
RID-037,keep,,thermal interface material,thermal/semi,">50 W/mK; HBM4 16-high; CXMT China angle"
RID-040,keep,,datacenter waste-heat recovery,thermal/extreme,"COP at low dT; district-heat reuse"
RID-041,keep,"RID-043,RID-044",advanced-packaging metrology platform,semi,"Position vs HBM4 hybrid-bonding postponement; sub-100nm void/overlay limit vs Onto/AMAT"
RID-042,keep,,die-to-wafer hybrid bonder,semi,"HBM5 hybrid bonding inevitable; sub-um placement; cleanroom burden flagged"
RID-045,keep,,panel-level packaging handler,semi/extreme,"Glass-panel warpage; large-panel flatness"
RID-047,keep,,precision RF power generator (China-localized),semi/extreme,"RF power <20% domestic in China; MKS-competitor subsystem"
RID-049,keep,,rad-hard SiC power device,semi/extreme,">200C rad-tolerant; China aerospace pillar; defense primes"
RID-051,keep,,advanced-packaging warpage controller,semi/extreme,"In-line flatness compensation for large-die"
RID-053,keep,,humanoid rotary actuator,robotics,"Quantify torque density; merchant engine-supplier niche; 40-60% BOM WTP basis"
RID-054,keep,,humanoid tactile skin,robotics,"mN resolution; China embodied-intelligence FYP"
RID-055,keep,,cobot SSM safety controller,robotics,"ISO 10218-1/2:2025 SSM/PFL; PLd/SIL2 moat"
RID-056,keep,RID-064,PFL force-limiting joint + F/T sensor,robotics,"ISO 10218-2:2025 Table A.2 biomechanical limits"
RID-057,keep,,humanoid power subsystem,robotics/energy,"Wh/kg + peak current; pack+PMIC"
RID-058,keep,,dexterous hand mechanism,robotics,"MIIT humanoid standards Feb 2026; DOF density"
RID-061,keep,,humanoid edge-inference module,robotics/semi,"GR00T/VLA maturing; TOPS/W"
RID-062,keep,,magnet-free actuator,robotics/extreme,"Hedge vs China NdFeB export controls (Apr 2024)"
RID-066,keep,,exoskeleton actuation unit,robotics/bio,"Aging-workforce FYP; reimbursement risk flagged"
RID-067,keep,RID-122,detect-and-avoid module + certified fusion,low-alt,"FAA Part 108 DAA mandate; named BVLOS logistics operator"
RID-068,keep,,eVTOL powertrain,low-alt/energy,"China low-altitude pillar; power density + redundancy"
RID-069,keep,,eVTOL thermal management,low-alt/energy,"High C-rate flight thermal"
RID-070,keep,RID-073,C2 datalink module + RID/EC,low-alt,"Part 108 C2 + RID mandate; multi-link redundancy"
RID-071,keep,,drone airspace-management ADSP,low-alt,"Part 108 creates Part 146 ADSP; deconfliction"
RID-072,keep,,heavy-lift cargo drone airframe,low-alt/extreme,"Part 108 up to 1,320 lb; payload/range"
RID-074,keep,,drone battery fast-swap system,low-alt/energy,"<60s swap; scaled BVLOS ops"
RID-077,keep,RID-084,surgical force-feedback system (instrument + console),bio,"da Vinci 5 up-to-43%-less-force (Awad 2025) as WTP proof; non-Intuitive OEM"
RID-078,keep,RID-079,microneedle lactate sensor + multiplex,bio,"ICU continuous lactate r=0.94; multi-analyte option; avoid monitoring overproduction framing"
RID-080,keep,,closed-loop drug-delivery microneedle,bio,"Sense-and-deliver feedback dosing; standalone therapeutic"
RID-081,keep,,FDA AI-enabled surgical subsystem,bio/AI,"ISO/PAS 8800 + FDA AI/ML; deterministic AI safety"
RID-082,keep,,implantable neurostimulator power,bio/extreme,"China BCI in 15th FYP; chronic wireless power"
RID-086,keep,,organ-on-chip platform,bio/extreme,"China biomanufacturing pillar; FDA Modernization Act"
RID-087,keep,,point-of-care molecular cartridge,bio,"DIAG; NMPA green channel; <30min sample-to-answer"
RID-088,keep,,robotic catheter actuation,bio/AI,"Sub-mm steering; surgical-robot momentum; incumbents flagged"
RID-091,keep,,China-localized imaging detector,bio/semi,"MOF/MIIT Document 551 100%-domestic forced substitution; name detector + Chinese OEM"
RID-092,keep,,bioreactor process control,bio/extreme,"China biomanufacturing pillar; localization vs Sartorius"
RID-093,keep,,battery electrode coating inspection,mfg,"DIAG; coating 2-5% scrap = 20-40% of mfg cost; CATL/BYD line pilot"
RID-094,keep,,AM in-situ NDE,mfg/extreme,"DIAG; aerospace AM qualification; layer-wise defect"
RID-095,keep,,battery dry-electrode equipment,mfg/energy,"Drying energy 20-40% of cost; solvent-free line"
RID-097,keep,,laser micro-machining cell,mfg/extreme,"Sub-um features; medical/semi"
RID-099,keep,,extreme-precision metrology instrument,mfg/extreme,"DIAG; sub-um metrology import-dependent in China; nm precision"
RID-100,keep,RID-052,automated optical-assembly cell + photonic alignment,mfg/extreme,"Sub-um 6-axis active alignment; CPO/lidar growth"
RID-101,keep,,molten-salt-resistant alloy components,extreme,"China 110GW-by-2030 nuclear; 700C salt-corrosion lifetime spec; long qual flagged"
RID-102,keep,,fusion-magnet HTS components,extreme,"CFS $8M TF-magnet milestone (DOE $46M program); high-field cryo"
RID-104,keep,,fusion first-wall thermal management,extreme/energy,"DOE Milestone fusion; MW/m2 flux"
RID-106,keep,,rad-hard sensor readout ASIC,semi/extreme,"China nuclear+aerospace pillars; rad-tolerant"
RID-111,keep,,high-bandwidth piezo actuator,sensors/semi,"nm at kHz; advanced-packaging alignment"
RID-112,keep,,navigation-grade MEMS IMU,sensors,"Part 108 GPS-denied nav; low drift"
RID-115,keep,,wide-bandwidth DC current sensor,sensors/semi,"DIAG; 800VDC current sensing; kA wide-bandwidth"
RID-119,keep,,AI functional-safety runtime,embedded-AI,"ISO/PAS 8800 + TR 5469 (SAE 2026-01-0036)"
RID-120,keep,,safety-rated edge AI accelerator,embedded-AI/semi,"ASIL-D edge inference; ISO 10218:2025"
RID-121,keep,,redundant autonomy safety controller,embedded-AI,"Dual-channel fail-operational for AMRs"
RID-123,keep,,embedded AI watchdog for medical AI,embedded-AI/bio,"FDA AI/ML + ISO/PAS 8800; drift detection"
RID-124,keep,,grid-edge AI controller (safety),embedded-AI/energy,"IEEE 2800.2-2026 + AI safety; deterministic grid control"
```

---

## 8. ENTRIES FOR `rejected_ideas.md`

```text
# Rejected / Merged Ideas — Phase 15 Diversity Filter (2026-06-24)

## Removed (34) — generic, commodity, monitoring-overproduction, or out-of-window
RID-006 Power-electronics reliability qual tool — DIAG; OEM in-house; no durable wedge.
RID-011 ±400VDC isolation monitor — DIAG; built into PSU; commodity.
RID-021 CAES/LAES expander — capex-heavy turbomachinery; weak founder fit.
RID-025 Interconnection-study accelerator — bottleneck is regulatory not technical (fatal).
RID-027 VPP aggregation edge node — generic software; software-only rivals.
RID-028 Dynamic line-rating sensor — DIAG; slow adoption; overlaps RID-023.
RID-031 Substation SiC retrofit module — overlaps RID-030; procurement drag.
RID-038 Coolant leak-detection mesh — DIAG; built into CDU.
RID-039 Rear-door heat exchanger — commodity; leapfrogged by full-liquid.
RID-046 China CMP endpoint sensor — DIAG; entity-list risk; RID-047 stronger.
RID-048 Precision vacuum valve — cleanroom; reliability risk.
RID-050 Chiplet KGD test — DIAG; incumbent ATE.
RID-059 Cobot safety vision scanner — DIAG; incumbent scanners.
RID-060 Mobile-manipulator base — crowded; no moat.
RID-063 Industrial AI vision QC — DIAG; commoditized.
RID-065 Robot joint health monitor — DIAG; OEM owns.
RID-075 Counter-UAS detection — DIAG; mitigation-regulation dependency.
RID-076 Precision-ag spray controller — DJI dominance.
RID-083 Portable dialysis fluidics — 2030-stretch; regulatory.
RID-085 Wearable cardiac patch — monitoring overproduction.
RID-089 Cuff-less continuous BP module — monitoring overproduction; accuracy/regulatory.
RID-090 Surgical smoke evacuation — low differentiation.
RID-096 Precision dispensing robot — incumbents (Nordson).
RID-098 Weld-quality AI inspection — DIAG; commoditized.
RID-103 Accident-tolerant fuel cladding — NRC/NNSA timeline beyond 2030.
RID-105 Cryogenic power feedthrough — niche; within RID-102 scope.
RID-107 High-temp SiC reactor instrumentation — DIAG; long qual.
RID-108 Aerospace thermal-protection material — qual-heavy; weak fit.
RID-109 sCO2 power-cycle turbomachine — TRL/capex; weak fit.
RID-113 Fiber-optic distributed sensor — DIAG; incumbents.
RID-114 Magnetic-bearing controller — niche; no beachhead.
RID-116 Soft-robotic actuator — durability; overlaps actuator family.
RID-117 Phased-array ultrasonic NDE — DIAG; incumbents.
RID-118 Compact cryocooler — incumbents; niche.

## Merged (11) — folded into a stronger survivor
RID-007 supercap ride-through — merged into RID-002 (rack-level DC buffer family).
RID-010 800VDC e-fuse chip — merged into RID-003 (DC fault-interruption).
RID-043 microbump inspection AI — merged into RID-041 (packaging metrology platform).
RID-044 backside-thinning metrology — merged into RID-041 (packaging metrology platform).
RID-052 photonic-IC alignment — merged into RID-100 (optical-assembly cell).
RID-064 6-axis F/T sensor — merged into RID-056 (force-limiting joint).
RID-073 RID/EC beacon — merged into RID-070 (drone comms module).
RID-079 multiplex microneedle — merged into RID-078 (microneedle platform).
RID-084 surgical haptic console — merged into RID-077 (surgical force-feedback system).
RID-110 national-lab sole-source instrument — merged into RID-036 (SSTR/FDTR thermal characterization).
RID-122 sensor-fusion DAA safety module — merged into RID-067 (DAA module).
```

---

## NOTES & CAVEATS
- **No attractiveness scoring performed** — that is Phase 16 (`04_diligence_scoring/01_score_filtered_ideas.md`), which will rank these 79 against the launch rubric and assign pursue/watch/kill.
- **Biomedical floor relaxed 15→10**, deliberately and with rationale (§6); flag for your review if you want the floor held.
- **Semiconductor/hardware count is tight (~20)** — acceptable but worth watching if scoring kills several power/packaging ideas.
- **Merges fold scope, not just IDs:** each survivor that absorbed a merge should have its 13 Phase-14 fields broadened to cover the merged scope before scoring (the `strengthen_note` flags this).
- **All "why now" anchors and company-claim labels carry over unchanged** from Phase 14; nothing new was researched in this filter.
- **Counts in the quota table** use the same overlapping-category convention as Phase 14 (one idea can satisfy several quotas).
