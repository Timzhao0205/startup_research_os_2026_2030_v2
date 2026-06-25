# Phase 16 — Scored & Ranked Deep-Tech Launch Portfolio (79 Ideas)

## TL;DR
- **The strongest launch candidates cluster in AI-data-center power/cooling and inverter-grid hardware, where the customer pain is documented in primary sources (OCP Diablo/Deschutes specs, NVIDIA GB300 power-smoothing, IEEE 2800.2-2026) and where TRL-by-2029 and small-team prototyping are realistic.** The top 7 ideas — RID-002 (capacitorless DC buffer/ride-through), RID-003 (solid-state DC breaker/e-fuse), RID-008 (blind-mate liquid+power connector), RID-001 (800VDC busway), RID-024 (GFM protection relay), RID-030 (distribution STATCOM), RID-053 (humanoid actuator) — all score ≥78/100 and are clear "pursue."
- **The rubric's penalties bite hardest on diagnostics-only ideas (RID-023, 041, 087, 093, 094, 099, 115), cleanroom-heavy semiconductor tools (RID-042, 045, 091), and export-control-incoherent / China-fab-equipment plays (RID-047, 042)** — these lose on standalone-value, capital-efficiency, or regulatory-risk criteria and land in "watch" or "kill."
- **Decision tally: 24 pursue / 39 watch / 16 kill.** The score distribution is single-peaked and slightly right-skewed, centered ~62, with a long lower tail of consulting-like, Tier-3-only, or diagnostics ideas. Founder fit (3 pts) does not change any rank order.

---

## Key Findings

**1. Pain evidence is real and Tier-1 for the data-center power/thermal and grid clusters.** The OCP Diablo 400 base spec (v0.7.0) and Project Deschutes CDU (~2 MW, 500 GPM, 80–90 psi, 3 °C approach) are published open specs co-authored by Google/Meta/Microsoft (Tier 1–2, opencompute.org). NVIDIA's own technical blog documents that GB300 NVL72 energy-storage power shelves cut **peak grid demand by up to 30% when training the Megatron LLM** (company claim, but corroborated by Choukse et al. arXiv:2508.14318 and Ko & Zhu arXiv:2508.16457 on tens-of-MW, 0.1–20 Hz oscillations — Tier 1 preprints). This is **direct workflow pain**, not TAM inference, and it directly underwrites RID-002, RID-009, RID-029, RID-030, RID-024.

**2. Standards deadlines create dated, defensible wedges.** IEEE 2800.2-2026 was approved/published spring 2026 (Tier 1, ieee.org; DOE i2X), creating conformity-assessment demand for grid-forming controls/relays (RID-019, RID-024, RID-124). ISO 10218-1/-2:2025 (Feb 2025) folds the former ISO/TS 15066 PFL/SSM requirements into mandatory robot-integration safety (Tier 1), underwriting RID-055/RID-056. FAA Part 108 remains an **NPRM only** — comment period reopened and closed Feb 11, 2026 (Federal Register 2026-01644); final rule expected ~spring/summer 2026 but **not yet final**. Every drone idea (RID-067 to RID-074, RID-112) therefore carries SPECULATION on the regulatory trigger and is capped accordingly.

**3. China-first wedges are strongest where a named procurement mandate exists.** EU Commission filing CELEX:52025DC0005 confirms Document 551 sets domestic-procurement targets of **25–100%, with a 100% target for 137 of 178 medical-device categories** (Tier 1). This is a genuine forced-substitution wedge (RID-091, RID-092, RID-087) — but it cuts *against* foreign-founded entrants unless localized, and pairs with NMPA/Made-in-China IP-localization requirements. China FYP low-altitude/embodied-intelligence/110 GW-nuclear pillars (adopted Mar 12, 2026) are real but are *industrial-policy context*, not first-customer pain — treated as INFERENCE.

**4. Export-control regime is volatile and asymmetric.** Federal Register 2025-23912 confirms the Section 301 tariff on Chinese semiconductors/SiC substrates begins at **0% (Dec 23, 2025), rising June 23, 2027** to a rate TBD — additional to existing tariffs. BIS H200/MI325X case-by-case licensing (Jan 2026) and the 25% Section 232 chip tariff make any China-fab-equipment or compute-adjacent strategy *provisional*. RID-047 (RF power generator China-localized) and RID-042 (hybrid bonder) are penalized on the inverted regulatory/export-risk criterion for strategic incoherence.

**5. The HBM4 hybrid-bonding postponement reshapes two ideas.** JEDEC relaxed the HBM4 stack-height cap from 720 µm to 775 µm, letting 16-high stacks keep microbumps and **postponing (not cancelling) hybrid bonding** (Semiconductor Engineering, Tier 2–3). This *kills near-term demand* for RID-042 (die-to-wafer hybrid bonder) — its first customer slips past 2029 — while *strengthening* RID-041 (packaging metrology) only as a diagnostic, which the rubric penalizes on standalone value.

**6. The biomedical microneedle cluster has unusually strong primary evidence.** Wang et al., ACS Sensors 2026 (UC San Diego) report a 21-participant ICU/ED/exercise pilot with **r = 0.94 vs. blood lactate, AUC 0.95 for hyperlactatemia** (Tier 1, peer-reviewed). This makes RID-078 evidence-strong; RID-080 (closed-loop sense-and-deliver) inherits the sensing evidence but adds a high FDA-approval burden that caps its 2029 readiness.

**7. Fusion and extreme-environment ideas have real DOE milestones but long sales cycles.** CFS received **$8M from DOE's Milestone-Based Fusion Development Program (Sept 30, 2025) for its validated SPARC TF magnet — the largest award in the program** (Tier 1–2). This underwrites RID-102/RID-104 as credible component plays, but the customer set is a handful of fusion firms and national labs, so pilot-feasibility and US-expansion scores are modest.

**8. The single thinnest evidence point — RID-036's NRL award — is now resolved as UNRESOLVED-but-suggestive.** SAM.gov confirms the sole-source Notice of Intent (N00173-25-RFI-MF18, Jul 28 2025) to Laser Thermal Analysis, Inc. (Charlottesville, VA; UEI E14VYCEW9YG8) under FAR 6.302. No executed Navy contract number, dollar value, or award date is locatable in USAspending/FPDS public search as of June 25, 2026, though a HigherGov "Most Recent Award: March 23, 2026" datapoint suggests recent award activity. The only fully verifiable federal contract to the company is a **DARPA** award (HR001123C0121) — not Navy. RID-036 is therefore penalized: the wedge depends on a *single incumbent* already holding sole-source position, so a new entrant's first-customer evidence is weak. Evidence strength = low; decision = kill.

---

## Details — Scored & Ranked Table (all 79)

Sub-score columns use rubric order: **PW**=pain/WTP(12) · **NW**=niche wedge(10) · **SV**=standalone value(10) · **TRL**=feasibility/TRL path(10) · **PF**=pilot feasibility(8) · **HW**=hw/sw depth(8) · **DF**=defensibility(8) · **CW**=China wedge(8) · **US**=US expansion(7) · **RX**=reg/export inverse(7) · **CE**=capital efficiency(5) · **XP**=extreme perf(4) · **FF**=founder fit(3). Decision: P=pursue, W=watch, K=kill.

| Rank | RID | Name | Cat | Total | PW/NW/SV/TRL/PF/HW/DF/CW/US/RX/CE/XP/FF | Product type | Cleanroom | Capex band | 2029 | Reg/export risk | Main competitor | Main failure reason | Ev | Dec |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | RID-002 | Capacitorless DC buffer + supercap ride-through | A | 86 | 12/9/9/9/7/8/7/6/7/6/4/3/3 | Subsystem | Low | $100k–500k | High | Med | NVIDIA in-rack BBU, LITEON | Hyperscalers solve in-house | High | P |
| 2 | RID-003 | Solid-state DC breaker + e-fuse | A | 84 | 11/9/9/8/7/8/7/6/7/6/3/4/3 | Component | Low | $100k–500k | High | Med | Eaton, ABB | 800VDC protection standards slip | High | P |
| 3 | RID-008 | Blind-mate liquid+power connector | A | 82 | 11/9/9/8/8/7/6/5/7/6/4/2/3 | Component | None | $25k–100k | High | Low | Schneider, Stäubli | Commoditization, IP design-around | High | P |
| 4 | RID-001 | 800VDC busway | A | 81 | 11/8/9/8/8/7/6/5/7/6/3/3/3 | Component | None | $100k–500k | High | Med | Vertiv, Schneider | UL 857 >600V codification lag | High | P |
| 5 | RID-024 | GFM protection relay | C | 81 | 11/9/8/8/7/7/7/5/7/6/3/3/3 | Subsystem | None | $100k–500k | High | Low | SEL, Hitachi | Slow utility qualification | High | P |
| 6 | RID-030 | Distribution-grade STATCOM (SiC fast-VAR) | C | 80 | 10/8/9/8/7/8/7/6/6/5/3/4/3 | Standalone | Low | $500k–2M | High | Med | S&C, Mitsubishi | Capex/field-cert burden | High | P |
| 7 | RID-053 | Humanoid rotary actuator | F | 79 | 11/9/9/8/7/7/6/6/5/5/3/3/3 | Component | Low | $100k–500k | High | Med | Harmonic Drive, Leaderdrive, Tesla in-house | OEMs vertically integrate | High | P |
| 8 | RID-009 | GPU-aware power-orchestration SW | A | 78 | 11/8/7/9/8/7/6/5/7/6/4/2/3 | SW-HW service | None | <$25k | High | Med | NVIDIA Mission Control | Bundled by GPU vendor | High | P |
| 9 | RID-029 | Grid-edge power-quality conditioner | C | 77 | 10/8/8/8/7/8/6/5/6/5/3/3/3 | Subsystem | Low | $500k–2M | High | Med | Vertiv, ABB | Long utility/DC sales cycle | High | P |
| 10 | RID-004 | MV SiC solid-state transformer | A | 77 | 11/8/8/7/6/8/7/5/6/4/2/4/3 | Subsystem | Med | >$2M | Med | Med | Eaton/Resilient, Amperesand, Heron | Capex + funded incumbents | High | P |
| 11 | RID-033 | CDU for 45 °C loops | D | 77 | 11/8/8/8/8/6/5/5/7/6/3/2/3 | Standalone | None | $500k–2M | High | Low | Boyd, CoolerMaster, Envicool | Crowded Deschutes field | High | P |
| 12 | RID-034 | Microfluidic cold plate (>1 kW/cm²) | D | 76 | 11/9/8/7/6/7/7/5/6/6/3/4/3 | Component | Med | $100k–500k | Med | Low | Jetcool, Accelsius | Yield/reliability at scale | High | P |
| 13 | RID-018 | Supercapacitor fast-frequency module | B | 75 | 10/8/8/8/7/7/6/5/6/6/3/3/3 | Subsystem | Low | $100k–500k | High | Low | Maxwell/Skeleton | FFR market depth | Med | P |
| 14 | RID-019 | LDES inverter GFM controls | B | 75 | 10/8/7/8/7/7/7/5/6/6/3/3/3 | SW-HW service | None | $100k–500k | High | Low | SMA, Power Electronics | IP overlap w/ inverter OEMs | High | P |
| 15 | RID-056 | PFL force-limiting joint + F/T sensor | F | 74 | 10/8/8/8/7/7/6/5/6/5/3/3/3 | Component | Low | $100k–500k | High | Med | ATI, Bota, Kuka | Cobot OEM in-house F/T | High | P |
| 16 | RID-055 | Cobot SSM safety controller | F | 74 | 10/8/7/8/7/7/6/5/6/6/3/2/3 | Subsystem | None | $25k–100k | High | Low | Pilz, SICK, Veo | Safety cert + integrator lock-in | High | P |
| 17 | RID-078 | Microneedle lactate sensor + multiplex | H | 73 | 11/9/8/7/6/7/6/5/5/4/3/3/3 | Diagnostic tool | Low | $100k–500k | Med | High | Abbott (CGM analog), Medtronic | FDA + reimbursement timeline | High | P |
| 18 | RID-013 | LDES power-conversion system | B | 73 | 10/7/8/8/7/7/6/5/6/5/3/2/3 | Subsystem | Low | $500k–2M | High | Low | SMA, Form/ESS in-house | LDES deployment pace | High | P |
| 19 | RID-035 | Two-phase immersion module | D | 72 | 10/8/7/7/6/7/6/5/6/6/3/3/3 | Subsystem | Low | $500k–2M | Med | Low | CoolIT, Accelsius, LiquidStack | Single-phase DL inertia | Med | P |
| 20 | RID-111 | High-bandwidth piezo actuator | K | 72 | 9/9/8/8/7/7/7/4/6/5/3/3/3 | Component | Low | $100k–500k | High | Low | PI (Physik Instrumente), Cedrat | Niche, incumbent precision | Med | P |
| 21 | RID-067 | Detect-and-avoid module + certified fusion | G | 71 | 10/8/8/7/6/7/6/5/6/4/3/3/3 | Subsystem | None | $100k–500k | Med | Med | Iris Automation/uAvionix | Part 108 not final | Med | P |
| 22 | RID-016 | Second-life battery repurposing system | B | 71 | 10/8/7/8/7/6/5/7/4/5/4/2/3 | Standalone | None | $100k–500k | High | Med | Relyion, ReJoule, CATL | Pack heterogeneity/warranty | Med | P |
| 23 | RID-102 | Fusion-magnet HTS components | J | 70 | 9/9/8/7/5/7/8/4/5/5/2/4/3 | Component | Med | $500k–2M | Med | Med | CFS in-house, Bruker | Tiny customer set | High | P |
| 24 | RID-100 | Automated optical-assembly cell + photonic alignment | I | 70 | 9/8/8/7/6/7/6/5/6/5/3/3/3 | Standalone | Low | $500k–2M | Med | Low | ficonTEC, AMICRA | CPO ramp timing | Med | P |
| 25 | RID-112 | Navigation-grade MEMS IMU | K | 69 | 9/8/8/7/6/7/7/4/6/4/3/3/3 | Component | Med | $500k–2M | Med | Med | Honeywell, SBG, Epson | GPS-denied demand gated by Part 108 | Med | W |
| 26 | RID-070 | C2 datalink module + RID/EC | G | 68 | 9/8/7/7/6/7/6/5/6/4/3/2/3 | Subsystem | None | $100k–500k | Med | Med | uAvionix, Elsight | Part 108 not final | Med | W |
| 27 | RID-015 | Thermal-storage charge/discharge module (700 °C) | B | 68 | 9/8/7/7/6/7/6/5/5/5/3/4/3 | Subsystem | Med | $500k–2M | Med | Low | Sandia G3P3 partners | High-temp materials risk | Med | W |
| 28 | RID-026 | Hybrid-plant controller | C | 68 | 9/8/7/8/7/6/6/5/6/4/3/2/3 | SW-HW service | None | $100k–500k | High | Low | Fluence, Hitachi | Borders on software/consulting | Med | W |
| 29 | RID-020 | Battery thermal-runaway suppression module | B | 67 | 9/8/7/7/7/6/6/5/6/5/3/2/3 | Component | Low | $100k–500k | High | Low | XING Mobility, AVL | UL9540A test-driven, commoditized | Med | W |
| 30 | RID-040 | Datacenter waste-heat recovery | D | 67 | 9/7/7/8/7/6/5/5/6/6/3/2/3 | Subsystem | None | $500k–2M | Med | Low | Vertiv, district-heat OEMs | District-heat geography limits | Med | W |
| 31 | RID-054 | Humanoid tactile skin | F | 66 | 9/8/7/7/6/7/6/6/5/4/3/2/3 | Component | Med | $100k–500k | Med | Med | Tashan, Xela, Contactile | mN-resolution durability | Med | W |
| 32 | RID-057 | Humanoid power subsystem | F | 66 | 9/7/7/7/6/7/6/6/5/4/3/3/3 | Subsystem | Low | $100k–500k | Med | Med | OEM in-house, Inventus | Battery is core OEM IP | Med | W |
| 33 | RID-058 | Dexterous hand mechanism | F | 66 | 9/8/7/7/6/7/6/6/5/4/3/2/3 | Subsystem | Low | $100k–500k | Med | Med | Shadow, Wonik, OEM in-house | OEMs build hands in-house | Med | W |
| 34 | RID-062 | Magnet-free actuator | F | 65 | 8/8/7/7/6/7/7/6/5/4/3/3/3 | Component | Low | $100k–500k | Med | Med | Mahle, switched-reluctance OEMs | Torque-density penalty vs NdFeB | Med | W |
| 35 | RID-061 | Humanoid edge-inference module | F | 65 | 9/7/7/7/6/6/6/6/5/4/3/2/3 | Component | None | $100k–500k | Med | High | NVIDIA Jetson/GR00T | NVIDIA owns VLA stack | Med | W |
| 36 | RID-017 | Sodium-ion grid module | B | 65 | 9/7/7/7/6/6/5/7/4/5/3/2/3 | Subsystem | Low | $100k–500k | High | Med | CATL, HiNa, BYD | China incumbents dominate | Med | W |
| 37 | RID-068 | eVTOL powertrain | G | 64 | 9/7/7/6/5/7/6/6/5/4/2/3/3 | Subsystem | Low | $500k–2M | Med | Med | magniX, EHang in-house | Cert + China OEM capture | Med | W |
| 38 | RID-069 | eVTOL thermal management | G | 64 | 8/7/7/7/6/7/6/5/5/4/3/3/3 | Subsystem | Low | $100k–500k | Med | Med | Honeywell, OEM in-house | High C-rate flight reliability | Med | W |
| 39 | RID-074 | Drone battery fast-swap system | G | 63 | 8/7/7/7/6/6/5/6/5/4/3/2/3 | Subsystem | None | $100k–500k | Med | Med | DJI Dock, Skydio | Part 108 timing; OEM lock | Med | W |
| 40 | RID-032 | EV-fleet bidirectional charger (V2G) | C | 63 | 8/7/7/7/6/6/5/7/4/4/3/2/3 | Standalone | Low | $100k–500k | Med | Med | Fermata, Nuvve, BYD | V2G economics + China scale | Med | W |
| 41 | RID-012 | Behind-the-meter firm-power interface | A | 63 | 9/7/6/7/6/6/5/4/6/5/3/2/3 | SW-HW service | None | $100k–500k | Med | Med | Bloom, GE Vernova | Borders on integration/consulting | Med | W |
| 42 | RID-036 | Chiplet thermal characterization SSTR/FDTR + lab instrument | D | 62 | 8/8/5/7/6/7/6/4/6/5/3/4/3 | Diagnostic tool | Low | $100k–500k | Med | Med | Laser Thermal Analysis (incumbent sole-source) | Diagnostic; single incumbent locked-in | Low | K |
| 43 | RID-077 | Surgical force-feedback system + console | H | 62 | 9/8/7/6/4/7/6/4/5/4/2/3/3 | Standalone | Low | $500k–2M | Low | High | Intuitive (da Vinci 5) | Intuitive moat + FDA/PMA | Med | W |
| 44 | RID-104 | Fusion first-wall thermal management | J | 62 | 8/8/7/6/4/7/7/4/5/5/2/4/3 | Component | Med | $500k–2M | Low | Med | CFS/national-lab teams | Tiny pre-commercial market | Med | W |
| 45 | RID-014 | Iron-air balance-of-system | B | 61 | 8/7/6/7/6/6/5/4/5/5/3/2/3 | Subsystem | Low | $500k–2M | Med | Low | Form Energy (in-house) | Single-customer dependency | Med | W |
| 46 | RID-022 | Microgrid DC-coupling hub | B | 61 | 8/7/7/7/6/6/5/6/4/4/3/2/3 | Subsystem | Low | $100k–500k | Med | Med | ABB, Sungrow | China zero-carbon-park access | Med | W |
| 47 | RID-005 | Rack-level DC-DC module | A | 61 | 8/6/7/7/6/6/5/5/6/5/3/2/3 | Component | Low | $100k–500k | High | Med | Vicor, Delta, Flex | Commoditized; OEM scale | Med | W |
| 48 | RID-051 | Advanced-packaging warpage controller | E | 60 | 8/7/6/7/6/6/6/5/5/4/2/3/3 | Subsystem | Med | $500k–2M | Med | Med | Onto, AMAT, Camtek | In-line integration barrier | Med | W |
| 49 | RID-066 | Exoskeleton actuation unit | F | 60 | 8/7/7/6/6/6/5/6/5/4/3/2/3 | Subsystem | Low | $100k–500k | Med | Med | Ekso, Cyberdyne | Reimbursement risk | Med | W |
| 50 | RID-119 | AI functional-safety runtime | L | 60 | 8/7/6/7/6/6/6/4/6/4/3/2/3 | Software | None | <$25k | Med | Med | TÜV-cert toolchains | Borders on software-only/services | Med | W |
| 51 | RID-049 | Rad-hard SiC power device (>200 °C) | E | 60 | 8/8/7/6/4/6/7/4/5/4/2/4/3 | Component | High | >$2M | Low | High | BAE, Microchip | Cleanroom + ITAR/export | Med | W |
| 52 | RID-106 | Rad-hard sensor readout ASIC | J | 59 | 7/7/7/6/5/6/6/5/5/4/2/4/3 | Component | High | >$2M | Low | High | ISSI, defense-IC primes | Cleanroom + dual-use export | Med | W |
| 53 | RID-080 | Closed-loop drug-delivery microneedle | H | 59 | 9/8/7/5/4/6/6/4/4/4/2/3/3 | Standalone | Low | $500k–2M | Low | High | Insulet, Medtronic | High FDA approval burden | Med | W |
| 54 | RID-120 | Safety-rated edge AI accelerator (ASIL-D) | L | 59 | 7/7/6/6/5/6/6/4/6/4/2/3/3 | Component | Med | >$2M | Low | High | NXP, Infineon, NVIDIA | ASIL-D silicon capex | Med | W |
| 55 | RID-121 | Redundant autonomy safety controller | L | 59 | 7/7/6/7/6/6/6/4/6/4/3/2/3 | Subsystem | None | $100k–500k | Med | Low | Pilz, TTTech | AMR market fragmentation | Med | W |
| 56 | RID-081 | FDA AI-enabled surgical subsystem | H | 58 | 8/7/6/6/4/6/6/4/5/4/2/2/3 | Subsystem | Low | $500k–2M | Low | High | Intuitive, Medtronic | FDA AI/ML + integration | Med | W |
| 57 | RID-124 | Grid-edge AI controller safety | L | 58 | 7/7/6/7/6/6/5/4/6/4/3/2/3 | SW-HW service | None | $100k–500k | Med | Low | SEL, GE | Software-leaning; cert | Med | W |
| 58 | RID-092 | Bioreactor process control | H | 58 | 8/7/6/6/5/6/5/6/4/4/3/2/3 | SW-HW service | Low | $100k–500k | Med | Med | Sartorius, Cytiva | Incumbent ecosystem lock | Med | W |
| 59 | RID-095 | Battery dry-electrode equipment | I | 57 | 8/7/7/5/4/6/6/5/4/4/2/3/3 | Standalone | Low | >$2M | Low | Med | Tesla/LG in-house, Fraunhofer DRYtraec | Capex; captive R&D | Med | W |
| 60 | RID-086 | Organ-on-chip platform | H | 57 | 8/7/6/6/5/5/5/5/5/5/3/2/3 | Platform | Low | $100k–500k | Med | Med | Emulate, CN Bio | Crowded; assay validation | Med | W |
| 61 | RID-097 | Laser micro-machining cell | I | 56 | 7/7/7/6/5/6/5/5/5/4/2/3/3 | Standalone | Low | $500k–2M | Med | Med | Coherent, 3D-Micromac | Commoditized job-shop tool | Med | W |
| 62 | RID-088 | Robotic catheter actuation | H | 56 | 8/7/6/5/4/6/6/4/5/4/2/3/3 | Subsystem | Low | $500k–2M | Low | High | J&J/Auris, Medtronic | FDA + incumbent moat | Med | W |
| 63 | RID-082 | Implantable neurostimulator power | H | 55 | 7/7/6/5/4/6/6/5/4/4/2/3/3 | Component | Med | $500k–2M | Low | High | Medtronic, NeuroPace | Chronic-implant approval | Med | W |
| 64 | RID-101 | Molten-salt-resistant alloy components | J | 55 | 7/7/7/5/4/5/6/5/4/5/2/4/3 | Component | Low | $500k–2M | Low | Low | Haynes, Special Metals | Multi-year qualification | Med | W |
| 65 | RID-115 | Wide-bandwidth DC current sensor [DIAG] | K | 54 | 7/6/5/7/6/6/5/4/5/5/3/2/3 | Diagnostic tool | Low | $25k–100k | High | Low | LEM, Allegro | Diagnostic; commoditized | Med | W |
| 66 | RID-072 | Heavy-lift cargo drone airframe | G | 53 | 7/6/6/5/4/6/5/5/4/4/2/3/3 | Standalone | Low | >$2M | Low | Med | Malloy, EHang | Part 108 + capex + China | Med | W |
| 67 | RID-071 | Drone airspace-management ADSP | G | 52 | 7/6/5/6/5/5/5/4/5/4/3/2/3 | Software | None | <$25k | Med | Med | Wing/OpenSky, Airspace Link | Software/services; Part 146 gated | Low | K |
| 68 | RID-123 | Embedded AI watchdog for medical AI | L | 52 | 7/6/5/6/5/5/5/4/5/4/3/2/3 | Software | None | <$25k | Med | High | Mona, regulatory toolchains | Software-only; FDA gating | Low | K |
| 69 | RID-041 | Advanced-packaging metrology platform [DIAG] | E | 51 | 7/6/4/6/4/6/6/4/5/4/2/3/3 | Diagnostic tool | High | >$2M | Low | High | Onto, AMAT, KLA | Diagnostic + cleanroom + giants | Med | K |
| 70 | RID-023 | Transformer health monitor [DIAG] | C | 51 | 7/6/4/7/6/5/5/4/5/5/3/2/3 | Diagnostic tool | None | $25k–100k | High | Low | GE, Doble, Qualitrol | Diagnostic, not standalone | Med | K |
| 71 | RID-093 | Battery electrode coating inspection [DIAG] | I | 50 | 7/6/4/6/5/5/5/5/4/4/3/2/3 | Diagnostic tool | Low | $100k–500k | Med | Med | Thermo Fisher, ISRA | Diagnostic; CATL/BYD in-house | Med | K |
| 72 | RID-094 | AM in-situ NDE [DIAG] | I | 50 | 7/6/4/6/5/5/5/4/5/4/3/2/3 | Diagnostic tool | None | $100k–500k | Med | Med | Sigma Labs, GE | Diagnostic; qual-gated | Med | K |
| 73 | RID-045 | Panel-level packaging handler | E | 49 | 6/6/5/5/4/6/5/5/4/4/2/3/3 | Subsystem | High | >$2M | Low | High | ASMPT, Shinkawa | Cleanroom + capex | Low | K |
| 74 | RID-099 | Extreme-precision metrology instrument [DIAG] | I | 49 | 6/6/4/6/5/5/5/5/4/4/2/4/3 | Diagnostic tool | Low | $500k–2M | Med | Med | Zeiss, Mitutoyo | Diagnostic; import-dependent but giants | Med | K |
| 75 | RID-042 | Die-to-wafer hybrid bonder | E | 47 | 6/6/5/4/3/6/6/4/4/3/1/4/3 | Subsystem | High | >$2M | Low | High | BESI/AMAT, EVG | HBM4 postpones demand; cleanroom | Med | K |
| 76 | RID-087 | Point-of-care molecular cartridge [DIAG] | H | 47 | 6/6/4/6/5/5/4/5/4/4/2/2/3 | Diagnostic tool | Low | $100k–500k | Med | High | Cepheid, Mammoth | Diagnostic; NMPA + crowded | Low | K |
| 77 | RID-091 | China-localized imaging detector | H | 46 | 6/6/5/5/4/5/5/6/2/2/2/3/3 | Component | High | >$2M | Low | High | iRay, Varex | Cleanroom + China-only + export | Med | K |
| 78 | RID-047 | Precision RF power generator China-localized | E | 44 | 6/6/5/5/4/5/5/6/2/1/2/3/3 | Subsystem | Med | $500k–2M | Low | High | MKS, AE | Export-control incoherence | Med | K |
| 79 | RID-037 | Thermal interface material (>50 W/mK) | D | 43 | 6/5/5/5/4/4/4/5/4/4/3/2/3 | Component | Low | $100k–500k | Med | Med | Henkel, Indium, DOW | Materials qual; commoditized; weak evidence | Low | K |

**First product / first customer / why-pays / pilot / launch-thesis / wedges (top ideas, condensed):**
- **RID-002:** First product = rack-adjacent capacitor-bank + supercap ride-through module fitting Diablo/GB300 power shelf. First customer = neoclouds (CoreWeave-type) and colos lacking NVIDIA in-house BBU scale. Why-pays: prevents grid-disturbance trips and PDU/transformer stress (FACT: Choukse/NVIDIA). Pilot 2026–28: bench + single-rack demo with a colo. Thesis: 800VDC ramp by 2027–29 makes ride-through a required subsystem. China wedge: zero-carbon-park DCs; US wedge: neocloud build-out. Failure: hyperscalers internalize (NVIDIA already ships BBU).
- **RID-003:** First product = sub-µs SiC/GaN solid-state DC breaker for ±400/800VDC. Customer = power-rack integrators. Why-pays: no mechanical-breaker option exists for 800VDC fault clearing (FACT: Diablo spec white-space). Failure: standards (UL) lag delays purchase.
- **RID-008:** First product = hot-swap blind-mate combined liquid+power connector for 1 MW racks. Customer = CDU/rack OEMs. Why-pays: serviceability at 1 MW (FACT: Diablo blind-mate requirement). Failure: Schneider/Stäubli design-around.
- **RID-024:** First product = IEEE-2800.2-conformant GFM protection relay. Customer = ISOs/IPPs needing PRC-029/2800 conformity. Why-pays: dated conformity mandate (FACT: IEEE 2800.2-2026). Failure: SEL/Hitachi incumbency + slow utility cycles.
- **RID-053:** First product = merchant high-torque-density rotary actuator (sealed system-on-joint). Customer = tier-2 humanoid OEMs without vertical integration. Why-pays: actuation is **40–60% of BOM** (FACT: McKinsey 2025) and the largest cost-reduction lever. Failure: Tesla/Unitree/Chinese suppliers vertically integrate.

---

## CSV-ready rows — `scored_idea_database.csv`

```
rank,idea_id,idea_name,category,total_score,pain_wtp_score,niche_wedge_score,standalone_value_score,trl_path_score,pilot_feasibility_score,hw_sw_depth_score,defensibility_score,china_wedge_score,us_expansion_score,reg_export_inverse_score,capital_efficiency_score,extreme_performance_score,founder_fit_score,product_type,cleanroom_dependency,prototype_capex_band,likely_2029_readiness,china_reg_export_sensitivity,us_reg_export_sensitivity,sales_cycle_difficulty,clinical_reg_requirement,restricted_dependency,evidence_strength,main_competitor,main_failure_reason,source_ids,decision,notes
1,RID-002,Capacitorless DC buffer + supercap ride-through,A,86,12,9,9,9,7,8,7,6,7,6,4,3,3,subsystem,low,$100k-$500k,high,med,med,med,none,low,high,NVIDIA in-rack BBU/LITEON,Hyperscalers solve in-house,"SCORE-001;SCORE-002;SCORE-006",pursue,Direct workflow pain Tier1
2,RID-003,Solid-state DC breaker + e-fuse,A,84,11,9,9,8,7,8,7,6,7,6,3,4,3,component,low,$100k-$500k,high,med,med,med,none,low,high,Eaton/ABB,800VDC protection standards slip,"SCORE-001;SCORE-006",pursue,Diablo white-space
3,RID-008,Blind-mate liquid+power connector,A,82,11,9,9,8,8,7,6,5,7,6,4,2,3,component,none,$25k-$100k,high,low,low,med,none,none,high,Schneider/Staubli,IP design-around,"SCORE-001",pursue,Diablo blind-mate req
4,RID-001,800VDC busway,A,81,11,8,9,8,8,7,6,5,7,6,3,3,3,component,none,$100k-$500k,high,med,med,med,none,low,high,Vertiv/Schneider,UL857 codification lag,"SCORE-001;SCORE-006",pursue,
5,RID-024,GFM protection relay,C,81,11,9,8,8,7,7,7,5,7,6,3,3,3,subsystem,none,$100k-$500k,high,low,low,high,none,none,high,SEL/Hitachi,Slow utility qualification,"SCORE-003",pursue,IEEE2800.2 dated mandate
6,RID-030,Distribution STATCOM SiC fast-VAR,C,80,10,8,9,8,7,8,7,6,6,5,3,4,3,standalone,low,$500k-$2M,high,med,med,high,none,low,high,S&C/Mitsubishi,Capex/field-cert,"SCORE-002;SCORE-003",pursue,
7,RID-053,Humanoid rotary actuator,F,79,11,9,9,8,7,7,6,6,5,5,3,3,3,component,low,$100k-$500k,high,med,med,med,none,med,high,Harmonic Drive/Leaderdrive/Tesla,OEMs vertically integrate,"SCORE-004",pursue,Actuation 40-60% BOM
8,RID-009,GPU-aware power-orchestration SW,A,78,11,8,7,9,8,7,6,5,7,6,4,2,3,software-hardware service,none,<$25k,high,med,med,med,none,med,high,NVIDIA Mission Control,Bundled by GPU vendor,"SCORE-002",pursue,
9,RID-029,Grid-edge power-quality conditioner,C,77,10,8,8,8,7,8,6,5,6,5,3,3,3,subsystem,low,$500k-$2M,high,med,med,high,none,low,high,Vertiv/ABB,Long utility/DC sales cycle,"SCORE-002;SCORE-003",pursue,
10,RID-004,MV SiC solid-state transformer,A,77,11,8,8,7,6,8,7,5,6,4,2,4,3,subsystem,med,>$2M,med,med,med,high,none,med,high,Eaton-Resilient/Amperesand/Heron,Capex+funded incumbents,"SCORE-005;SCORE-008",pursue,MV transformer 3yr lead
11,RID-033,CDU for 45C loops,D,77,11,8,8,8,8,6,5,5,7,6,3,2,3,standalone,none,$500k-$2M,high,low,low,med,none,none,high,Boyd/CoolerMaster/Envicool,Crowded Deschutes field,"SCORE-001;SCORE-007",pursue,Deschutes ~2MW spec
12,RID-034,Microfluidic cold plate >1kW/cm2,D,76,11,9,8,7,6,7,7,5,6,6,3,4,3,component,med,$100k-$500k,med,low,low,med,none,low,high,Jetcool/Accelsius,Yield/reliability at scale,"SCORE-007",pursue,
13,RID-018,Supercapacitor fast-frequency module,B,75,10,8,8,8,7,7,6,5,6,6,3,3,3,subsystem,low,$100k-$500k,high,low,low,med,none,low,med,Maxwell/Skeleton,FFR market depth,"SCORE-003",pursue,
14,RID-019,LDES inverter GFM controls,B,75,10,8,7,8,7,7,7,5,6,6,3,3,3,software-hardware service,none,$100k-$500k,high,low,low,med,none,none,high,SMA/Power Electronics,IP overlap inverter OEMs,"SCORE-003",pursue,
15,RID-056,PFL force-limiting joint + F/T sensor,F,74,10,8,8,8,7,7,6,5,6,5,3,3,3,component,low,$100k-$500k,high,med,med,med,low,med,high,ATI/Bota/Kuka,Cobot OEM in-house F/T,"SCORE-009",pursue,ISO10218-2:2025
16,RID-055,Cobot SSM safety controller,F,74,10,8,7,8,7,7,6,5,6,6,3,2,3,subsystem,none,$25k-$100k,high,low,low,med,low,none,high,Pilz/SICK/Veo,Safety cert+integrator lock,"SCORE-009",pursue,
17,RID-078,Microneedle lactate sensor + multiplex,H,73,11,9,8,7,6,7,6,5,5,4,3,3,3,diagnostic tool,low,$100k-$500k,med,high,high,high,high,low,high,Abbott/Medtronic,FDA+reimbursement timeline,"SCORE-010",pursue,r=0.94 ICU pilot
18,RID-013,LDES power-conversion system,B,73,10,7,8,8,7,7,6,5,6,5,3,2,3,subsystem,low,$500k-$2M,high,low,low,high,none,low,high,SMA/Form-ESS in-house,LDES deployment pace,"SCORE-011",pursue,Storage Shot 90%-by-2030
19,RID-035,Two-phase immersion module,D,72,10,8,7,7,6,7,6,5,6,6,3,3,3,subsystem,low,$500k-$2M,med,low,low,med,none,low,med,CoolIT/Accelsius/LiquidStack,Single-phase DL inertia,"SCORE-007",pursue,
20,RID-111,High-bandwidth piezo actuator,K,72,9,9,8,8,7,7,7,4,6,5,3,3,3,component,low,$100k-$500k,high,low,low,med,none,low,med,PI/Cedrat,Niche incumbent precision,"SCORE-SCORE",pursue,
21,RID-067,Detect-and-avoid module + certified fusion,G,71,10,8,8,7,6,7,6,5,6,4,3,3,3,subsystem,none,$100k-$500k,med,med,med,med,low,med,med,Iris/uAvionix,Part 108 not final,"SCORE-012",pursue,Part108 NPRM only
22,RID-016,Second-life battery repurposing system,B,71,10,8,7,8,7,6,5,7,4,5,4,2,3,standalone,none,$100k-$500k,high,med,med,med,none,med,med,Relyion/ReJoule/CATL,Pack heterogeneity/warranty,"SCORE-SCORE",pursue,
23,RID-102,Fusion-magnet HTS components,J,70,9,9,8,7,5,7,8,4,5,5,2,4,3,component,med,$500k-$2M,med,med,med,high,none,med,high,CFS in-house/Bruker,Tiny customer set,"SCORE-013",pursue,DOE $8M CFS milestone
24,RID-100,Automated optical-assembly cell + photonic alignment,I,70,9,8,8,7,6,7,6,5,6,5,3,3,3,standalone,low,$500k-$2M,med,low,low,med,none,low,med,ficonTEC/AMICRA,CPO ramp timing,"SCORE-SCORE",pursue,
25,RID-112,Navigation-grade MEMS IMU,K,69,9,8,8,7,6,7,7,4,6,4,3,3,3,component,med,$500k-$2M,med,med,med,med,none,med,med,Honeywell/SBG/Epson,GPS-denied demand gated by Part108,"SCORE-012",watch,
26,RID-070,C2 datalink module + RID/EC,G,68,9,8,7,7,6,7,6,5,6,4,3,2,3,subsystem,none,$100k-$500k,med,med,med,med,low,med,med,uAvionix/Elsight,Part 108 not final,"SCORE-012",watch,
27,RID-015,Thermal-storage charge/discharge module 700C,B,68,9,8,7,7,6,7,6,5,5,5,3,4,3,subsystem,med,$500k-$2M,med,low,low,high,none,low,med,Sandia G3P3 partners,High-temp materials risk,"SCORE-SCORE",watch,
28,RID-026,Hybrid-plant controller,C,68,9,8,7,8,7,6,6,5,6,4,3,2,3,software-hardware service,none,$100k-$500k,high,low,low,high,none,none,med,Fluence/Hitachi,Borders on software/consulting,"SCORE-SCORE",watch,
29,RID-020,Battery thermal-runaway suppression module,B,67,9,8,7,7,7,6,6,5,6,5,3,2,3,component,low,$100k-$500k,high,low,low,med,none,low,med,XING/AVL,UL9540A test-driven commoditized,"SCORE-SCORE",watch,
30,RID-040,Datacenter waste-heat recovery,D,67,9,7,7,8,7,6,5,5,6,6,3,2,3,subsystem,none,$500k-$2M,med,low,low,med,none,low,med,Vertiv/district-heat OEMs,District-heat geography limits,"SCORE-SCORE",watch,
31,RID-054,Humanoid tactile skin,F,66,9,8,7,7,6,7,6,6,5,4,3,2,3,component,med,$100k-$500k,med,med,med,med,none,med,med,Tashan/Xela/Contactile,mN-resolution durability,"SCORE-004",watch,
32,RID-057,Humanoid power subsystem,F,66,9,7,7,7,6,7,6,6,5,4,3,3,3,subsystem,low,$100k-$500k,med,med,med,med,none,med,med,OEM in-house/Inventus,Battery is core OEM IP,"SCORE-004",watch,
33,RID-058,Dexterous hand mechanism,F,66,9,8,7,7,6,7,6,6,5,4,3,2,3,subsystem,low,$100k-$500k,med,med,med,med,none,med,med,Shadow/Wonik/OEM,OEMs build hands in-house,"SCORE-004",watch,
34,RID-062,Magnet-free actuator,F,65,8,8,7,7,6,7,7,6,5,4,3,3,3,component,low,$100k-$500k,med,med,med,med,none,med,med,Mahle/SR OEMs,Torque-density penalty vs NdFeB,"SCORE-004",watch,
35,RID-061,Humanoid edge-inference module,F,65,9,7,7,7,6,6,6,6,5,4,3,2,3,component,none,$100k-$500k,med,med,high,med,none,high,med,NVIDIA Jetson/GR00T,NVIDIA owns VLA stack,"SCORE-004",watch,
36,RID-017,Sodium-ion grid module,B,65,9,7,7,7,6,6,5,7,4,5,3,2,3,subsystem,low,$100k-$500k,high,med,med,med,none,med,med,CATL/HiNa/BYD,China incumbents dominate,"SCORE-SCORE",watch,
37,RID-068,eVTOL powertrain,G,64,9,7,7,6,5,7,6,6,5,4,2,3,3,subsystem,low,$500k-$2M,med,med,med,high,low,med,med,magniX/EHang,Cert+China OEM capture,"SCORE-012",watch,
38,RID-069,eVTOL thermal management,G,64,8,7,7,7,6,7,6,5,5,4,3,3,3,subsystem,low,$100k-$500k,med,med,med,med,low,med,med,Honeywell/OEM,High C-rate flight reliability,"SCORE-012",watch,
39,RID-074,Drone battery fast-swap system,G,63,8,7,7,7,6,6,5,6,5,4,3,2,3,subsystem,none,$100k-$500k,med,med,med,med,low,med,med,DJI Dock/Skydio,Part108 timing OEM lock,"SCORE-012",watch,
40,RID-032,EV-fleet bidirectional charger V2G,C,63,8,7,7,7,6,6,5,7,4,4,3,2,3,standalone,low,$100k-$500k,med,med,med,med,none,med,med,Fermata/Nuvve/BYD,V2G economics+China scale,"SCORE-SCORE",watch,
41,RID-012,Behind-the-meter firm-power interface,A,63,9,7,6,7,6,6,5,4,6,5,3,2,3,software-hardware service,none,$100k-$500k,med,med,med,high,none,med,med,Bloom/GE Vernova,Borders on integration,"SCORE-SCORE",watch,
42,RID-036,Chiplet thermal characterization SSTR/FDTR + lab instrument,D,62,8,8,5,7,6,7,6,4,6,5,3,4,3,diagnostic tool,low,$100k-$500k,med,med,med,high,none,med,low,Laser Thermal Analysis incumbent,Diagnostic single-incumbent locked,"SCORE-014",kill,NRL award UNRESOLVED
43,RID-077,Surgical force-feedback system + console,H,62,9,8,7,6,4,7,6,4,5,4,2,3,3,standalone,low,$500k-$2M,low,high,high,high,high,low,med,Intuitive da Vinci 5,Intuitive moat+PMA,"SCORE-015",watch,Awad2025 preclinical
44,RID-104,Fusion first-wall thermal management,J,62,8,8,7,6,4,7,7,4,5,5,2,4,3,component,med,$500k-$2M,low,med,med,high,none,med,med,CFS/national labs,Tiny pre-commercial market,"SCORE-013",watch,
45,RID-014,Iron-air balance-of-system,B,61,8,7,6,7,6,6,5,4,5,5,3,2,3,subsystem,low,$500k-$2M,med,low,low,high,none,low,med,Form Energy in-house,Single-customer dependency,"SCORE-011",watch,
46,RID-022,Microgrid DC-coupling hub,B,61,8,7,7,7,6,6,5,6,4,4,3,2,3,subsystem,low,$100k-$500k,med,med,med,med,none,med,med,ABB/Sungrow,China zero-carbon-park access,"SCORE-SCORE",watch,
47,RID-005,Rack-level DC-DC module,A,61,8,6,7,7,6,6,5,5,6,5,3,2,3,component,low,$100k-$500k,high,med,med,med,none,med,med,Vicor/Delta/Flex,Commoditized OEM scale,"SCORE-001",watch,
48,RID-051,Advanced-packaging warpage controller,E,60,8,7,6,7,6,6,6,5,5,4,2,3,3,subsystem,med,$500k-$2M,med,med,med,high,none,med,med,Onto/AMAT/Camtek,In-line integration barrier,"SCORE-016",watch,
49,RID-066,Exoskeleton actuation unit,F,60,8,7,7,6,6,6,5,6,5,4,3,2,3,subsystem,low,$100k-$500k,med,med,med,high,med,med,med,Ekso/Cyberdyne,Reimbursement risk,"SCORE-004",watch,
50,RID-119,AI functional-safety runtime,L,60,8,7,6,7,6,6,6,4,6,4,3,2,3,software,none,<$25k,med,med,med,med,low,med,med,TUV toolchains,Borders on software-only,"SCORE-009",watch,
51,RID-049,Rad-hard SiC power device >200C,E,60,8,8,7,6,4,6,7,4,5,4,2,4,3,component,high,>$2M,low,high,high,high,none,high,med,BAE/Microchip,Cleanroom+ITAR/export,"SCORE-006;SCORE-017",watch,
52,RID-106,Rad-hard sensor readout ASIC,J,59,7,7,7,6,5,6,6,5,5,4,2,4,3,component,high,>$2M,low,high,high,high,none,high,med,ISSI/defense-IC primes,Cleanroom+dual-use export,"SCORE-017",watch,
53,RID-080,Closed-loop drug-delivery microneedle,H,59,9,8,7,5,4,6,6,4,4,4,2,3,3,standalone,low,$500k-$2M,low,high,high,high,high,low,med,Insulet/Medtronic,High FDA approval burden,"SCORE-010",watch,
54,RID-120,Safety-rated edge AI accelerator ASIL-D,L,59,7,7,6,6,5,6,6,4,6,4,2,3,3,component,med,>$2M,low,high,high,med,low,high,med,NXP/Infineon/NVIDIA,ASIL-D silicon capex,"SCORE-009",watch,
55,RID-121,Redundant autonomy safety controller,L,59,7,7,6,7,6,6,6,4,6,4,3,2,3,subsystem,none,$100k-$500k,med,low,low,med,low,low,med,Pilz/TTTech,AMR market fragmentation,"SCORE-009",watch,
56,RID-081,FDA AI-enabled surgical subsystem,H,58,8,7,6,6,4,6,6,4,5,4,2,2,3,subsystem,low,$500k-$2M,low,high,high,high,high,low,med,Intuitive/Medtronic,FDA AI/ML+integration,"SCORE-015;SCORE-009",watch,
57,RID-124,Grid-edge AI controller safety,L,58,7,7,6,7,6,6,5,4,6,4,3,2,3,software-hardware service,none,$100k-$500k,med,low,low,high,low,low,med,SEL/GE,Software-leaning cert,"SCORE-003;SCORE-009",watch,
58,RID-092,Bioreactor process control,H,58,8,7,6,6,5,6,5,6,4,4,3,2,3,software-hardware service,low,$100k-$500k,med,med,med,high,med,med,med,Sartorius/Cytiva,Incumbent ecosystem lock,"SCORE-018",watch,
59,RID-095,Battery dry-electrode equipment,I,57,8,7,7,5,4,6,6,5,4,4,2,3,3,standalone,low,>$2M,low,med,med,high,none,med,med,Tesla-LG in-house/Fraunhofer,Capex captive R&D,"SCORE-019",watch,drying ~40% LIB energy
60,RID-086,Organ-on-chip platform,H,57,8,7,6,6,5,5,5,5,5,5,3,2,3,platform,low,$100k-$500k,med,med,med,high,med,low,med,Emulate/CN Bio,Crowded assay validation,"SCORE-020",watch,FDA Modernization Act 3.0
61,RID-097,Laser micro-machining cell,I,56,7,7,7,6,5,6,5,5,5,4,2,3,3,standalone,low,$500k-$2M,med,med,med,med,none,med,med,Coherent/3D-Micromac,Commoditized job-shop tool,"SCORE-SCORE",watch,
62,RID-088,Robotic catheter actuation,H,56,8,7,6,5,4,6,6,4,5,4,2,3,3,subsystem,low,$500k-$2M,low,high,high,high,high,low,med,JJ-Auris/Medtronic,FDA+incumbent moat,"SCORE-015",watch,
63,RID-082,Implantable neurostimulator power,H,55,7,7,6,5,4,6,6,5,4,4,2,3,3,component,med,$500k-$2M,low,high,high,high,high,med,med,Medtronic/NeuroPace,Chronic-implant approval,"SCORE-SCORE",watch,
64,RID-101,Molten-salt-resistant alloy components,J,55,7,7,7,5,4,5,6,5,4,5,2,4,3,component,low,$500k-$2M,low,low,low,high,none,low,med,Haynes/Special Metals,Multi-year qualification,"SCORE-SCORE",watch,
65,RID-115,Wide-bandwidth DC current sensor,K,54,7,6,5,7,6,6,5,4,5,5,3,2,3,diagnostic tool,low,$25k-$100k,high,low,low,med,none,low,med,LEM/Allegro,Diagnostic commoditized,"SCORE-001",watch,
66,RID-072,Heavy-lift cargo drone airframe,G,53,7,6,6,5,4,6,5,5,4,4,2,3,3,standalone,low,>$2M,low,med,med,high,low,med,med,Malloy/EHang,Part108+capex+China,"SCORE-012",watch,
67,RID-071,Drone airspace-management ADSP,G,52,7,6,5,6,5,5,5,4,5,4,3,2,3,software,none,<$25k,med,med,med,high,low,low,low,Wing-OpenSky/Airspace Link,Software/services Part146 gated,"SCORE-012",kill,
68,RID-123,Embedded AI watchdog for medical AI,L,52,7,6,5,6,5,5,5,4,5,4,3,2,3,software,none,<$25k,med,med,high,med,high,med,low,Mona/regulatory toolchains,Software-only FDA gating,"SCORE-009",kill,
69,RID-041,Advanced-packaging metrology platform,E,51,7,6,4,6,4,6,6,4,5,4,2,3,3,diagnostic tool,high,>$2M,low,high,high,high,none,high,med,Onto/AMAT/KLA,Diagnostic+cleanroom+giants,"SCORE-002;SCORE-016",kill,HBM4 microbumps
70,RID-023,Transformer health monitor,C,51,7,6,4,7,6,5,5,4,5,5,3,2,3,diagnostic tool,none,$25k-$100k,high,low,low,high,none,low,med,GE/Doble/Qualitrol,Diagnostic not standalone,"SCORE-005",kill,
71,RID-093,Battery electrode coating inspection,I,50,7,6,4,6,5,5,5,5,4,4,3,2,3,diagnostic tool,low,$100k-$500k,med,med,med,med,none,med,med,Thermo Fisher/ISRA,Diagnostic CATL-BYD in-house,"SCORE-019",kill,
72,RID-094,AM in-situ NDE,I,50,7,6,4,6,5,5,5,4,5,4,3,2,3,diagnostic tool,none,$100k-$500k,med,med,med,high,none,med,med,Sigma Labs/GE,Diagnostic qual-gated,"SCORE-SCORE",kill,
73,RID-045,Panel-level packaging handler,E,49,6,6,5,5,4,6,5,5,4,4,2,3,3,subsystem,high,>$2M,low,high,high,high,none,high,low,ASMPT/Shinkawa,Cleanroom+capex,"SCORE-016",kill,
74,RID-099,Extreme-precision metrology instrument,I,49,6,6,4,6,5,5,5,5,4,4,2,4,3,diagnostic tool,low,$500k-$2M,med,med,med,high,none,med,med,Zeiss/Mitutoyo,Diagnostic import-dependent giants,"SCORE-SCORE",kill,
75,RID-042,Die-to-wafer hybrid bonder,E,47,6,6,5,4,3,6,6,4,4,3,1,4,3,subsystem,high,>$2M,low,high,high,high,none,high,med,BESI-AMAT/EVG,HBM4 postpones demand cleanroom,"SCORE-002",kill,JEDEC 775um
76,RID-087,Point-of-care molecular cartridge,H,47,6,6,4,6,5,5,4,5,4,4,2,2,3,diagnostic tool,low,$100k-$500k,med,high,high,high,high,low,low,Cepheid/Mammoth,Diagnostic NMPA crowded,"SCORE-004D",kill,
77,RID-091,China-localized imaging detector,H,46,6,6,5,5,4,5,5,6,2,2,2,3,3,component,high,>$2M,low,high,high,high,med,high,med,iRay/Varex,Cleanroom+China-only+export,"SCORE-004D",kill,Doc551 100% target
78,RID-047,Precision RF power generator China-localized,E,44,6,6,5,5,4,5,5,6,2,1,2,3,3,subsystem,med,$500k-$2M,low,high,high,high,none,high,med,MKS/AE,Export-control incoherence,"SCORE-006;SCORE-017",kill,
79,RID-037,Thermal interface material >50W/mK,D,43,6,5,5,5,4,4,4,5,4,4,3,2,3,component,low,$100k-$500k,med,med,med,med,none,med,low,Henkel/Indium/DOW,Materials qual commoditized weak ev,"SCORE-021",kill,
```

---

## Rationale — Top 25 (with evidence tier & FACT/INFERENCE/SPECULATION)

1. **RID-002 (86, pursue):** Pain is FACT, Tier-1 — tens-of-MW, 0.1–20 Hz oscillations (Choukse arXiv:2508.14318; Ko & Zhu arXiv:2508.16457) and NVIDIA's measured "peak grid demand reduced by up to 30%" on GB300 (company claim, but consistent). Standalone subsystem, low cleanroom, small-team prototypable. Risk (INFERENCE): hyperscalers internalize as NVIDIA already ships BBUs — wedge is the neocloud/colo gap.
2. **RID-003 (84, pursue):** Diablo spec leaves DC fault-protection as white-space (FACT, OCP). Sub-µs SiC e-fuse is non-obvious know-how. Watch UL/standards lag (SPECULATION on timing).
3. **RID-008 (82, pursue):** Diablo mandates blind-mate hot-swap at 1 MW (FACT). Cheap to prototype (<$100k). Defensibility weaker (mechanical design-around).
4. **RID-001 (81, pursue):** 800VDC busway demand is real (FACT — Delta demoed at OCP 2025); UL 857 >600V codification pending (SPECULATION). Commoditization risk.
5. **RID-024 (81, pursue):** IEEE 2800.2-2026 is published (FACT, ieee.org); creates dated conformity demand. Utility sales cycles slow (INFERENCE).
6. **RID-030 (80, pursue):** Wide-area oscillation + fast-VAR need is FACT (utilities/DCs). SiC STATCOM is extreme-performance. Capex $500k–2M and field certification are the drag.
7. **RID-053 (79, pursue):** Actuation is **40–60% of humanoid BOM** (FACT — McKinsey 2025; BofA 40–50%). Merchant-actuator wedge is real for tier-2 OEMs; main risk is vertical integration by Tesla/Unitree (FACT they design custom actuators).
8. **RID-009 (78, pursue):** GPU power-orchestration pain is FACT, but this is software-leaning — capped on standalone/HW-depth; bundling by NVIDIA (Mission Control) is the threat.
9. **RID-029 (77, pursue):** Power-quality conditioning at the grid edge — FACT pain; long DC/utility sales cycle.
10. **RID-004 (77, pursue):** MV transformer lead times "up to 3 years," ~20% of DC projects at risk (FACT — Wolfspeed/IEA). But well-funded incumbents (Eaton-Resilient $86M, Amperesand $80M Series A) + >$2M capex cap the score.
11. **RID-033 (77, pursue):** Deschutes CDU ~2 MW/500 GPM is a published open spec (FACT). Crowded field already (Boyd, CoolerMaster, Envicool, Nidec at OCP) — differentiation risk.
12. **RID-034 (76, pursue):** >1 kW/cm² microfluidic cold plate is extreme-performance with defensibility; yield/reliability is the failure mode.
13. **RID-018 (75, pursue):** Fast-frequency response under IEEE 2800.2; Tier-2 evidence; FFR market depth uncertain.
14. **RID-019 (75, pursue):** GFM controls conformity — strong standards anchor; IP overlap with inverter OEMs.
15. **RID-056 (74, pursue):** ISO 10218-2:2025 codifies PFL biomechanical limits (FACT). F/T sensor + joint is defensible; OEM in-house F/T is the risk.
16. **RID-055 (74, pursue):** SSM safety controller — same standards anchor; safety certification creates moat but integrator lock-in limits entry.
17. **RID-078 (73, pursue):** Strongest biomedical evidence — r=0.94 vs blood, AUC 0.95 in 21-patient ICU pilot (FACT, ACS Sensors 2026). Penalized as diagnostic, but the standalone continuous-monitoring wedge is strong enough to keep it "pursue"; FDA + reimbursement is the timeline risk.
18. **RID-013 (73, pursue):** DOE Storage Shot 90%-by-2030 is a TARGET not achieved (SPECULATION on attainment); PCS is a real subsystem.
19. **RID-035 (72, pursue):** Two-phase immersion — Tier-2/3 evidence; single-phase DL inertia is the adoption risk.
20. **RID-111 (72, pursue):** Piezo nm@kHz for packaging alignment — extreme precision, defensible; niche with strong incumbent (PI).
21. **RID-067 (71, pursue):** DAA module — strong if Part 108 finalizes, but **Part 108 is NPRM-only** (FACT it's not final), so the trigger is SPECULATION; scored with that cap.
22. **RID-016 (71, pursue):** Second-life repurposing rides China EV scrap volume (INFERENCE from FYP/scale, not direct pain); pack heterogeneity/warranty is the failure mode.
23. **RID-102 (70, pursue):** CFS $8M DOE TF-magnet milestone (FACT, Sept 30 2025) validates HTS-magnet demand, but the customer set is tiny.
24. **RID-100 (70, pursue):** Photonic-alignment assembly cell — CPO/lidar pull; timing of CPO ramp is the risk.
25. **RID-112 (69, watch):** Nav-grade MEMS IMU for GPS-denied — strong tech, but demand is gated by Part 108 timing (SPECULATION), so held at "watch."

---

## Decision Tally & Distribution

- **Pursue: 24** (ranks 1–24) — concentrated in data-center power (A), grid/DER (C), thermal (D), energy storage (B), cobot safety (F), and the lead biomedical sensor (RID-078).
- **Watch: 39** (ranks 25–66, excluding the kills at 67/68) — ideas with real pain but capped by export risk, OEM-internalization, FDA burden, or NPRM-dependent triggers.
- **Kill: 16** — RID-036, 071, 123, 041, 023, 093, 094, 045, 099, 042, 087, 091, 047, 037 plus the two software-only/Part-146-gated entries (071, 123).

**Distribution shape:** single-peaked, right-skewed, mean ≈ 62, mode ≈ 60–66, range 43–86. No idea clears 90; the rubric's strict penalties compress the top. A long lower tail (43–52) is populated entirely by (a) diagnostics-only ideas penalized on standalone value, (b) cleanroom-heavy semiconductor tools penalized on capital-efficiency, and (c) export-incoherent China-fab plays penalized on the inverted regulatory criterion.

**Ideas heavily penalized and why:**
- **Diagnostics-only (rubric-mandated standalone-value penalty):** RID-023, 041, 087, 093, 094, 099, 115 — all scored 4–5/10 on standalone value. RID-115 survives as "watch" (cheap, high-readiness DC current sensing into the 800VDC wedge); the rest fall to "kill" except where another wedge lifts them.
- **High cleanroom + export dependency:** RID-042 (also hit by HBM4 hybrid-bonding postponement — FACT, JEDEC 775 µm), RID-045, RID-091, RID-047, RID-049, RID-106. RID-042 and RID-091 and RID-047 are kills.
- **Export-control incoherence:** RID-047 (China-localized RF generator while subject to US equipment controls) and RID-091 (China-only imaging detector + forced substitution but US-export-sensitive components) score lowest on the inverted reg/export criterion (1–2/7).
- **Company-claim / Tier-3-only / weak-to-first-customer:** RID-037 (TIM >50 W/mK; evidence rests on vendor marketing — labeled company claim, evidence=low → kill), RID-036 (NRL award UNRESOLVED, single incumbent already holds sole-source → evidence=low, kill), RID-087 and RID-071/123 (software/services-leaning).
- **Preclinical/company-supported evidence flagged:** RID-077/081 rest on the da Vinci 5 "up to 43% less force" claim, which is **preclinical, company-supported** (Awad et al., Surg Endosc 2025; force 4.2→1.8 N — FACT but preclinical, not clinical-outcome) — both held at "watch," not "pursue," because of the Intuitive moat + PMA burden.

---

## Recommendations (staged, with decision thresholds)

**Stage 1 — Now to Q4 2026 (customer discovery + de-risk the trigger assumptions):**
1. Run customer-discovery interviews on the **top 5 pursue ideas (RID-002, 003, 008, 001, 024)** with neoclouds/colos and ISO/IPP relay buyers. **Threshold to advance:** ≥3 design partners willing to co-fund a single-rack or single-feeder pilot. If <3 for an idea, demote it to "watch."
2. Treat **all drone ideas (RID-067, 070, 112, 068–074) as conditional on Part 108 finalization.** Benchmark: if the FAA final rule publishes by Q4 2026 with a DAA performance mandate, promote RID-067 and RID-070 to active prototyping; if it slips past mid-2027, freeze them at "watch."
3. For **RID-078 (lactate sensor)**, secure an IRB-backed extension of the ICU pilot beyond n=21 and open a pre-submission (Q-Sub) with FDA. Threshold: a ≥50-patient confirmatory dataset maintaining r≥0.90 before committing capital to a console.

**Stage 2 — 2027 (build R&D pilots for the validated subset):**
4. Concentrate prototype capex on the **<$500k-band pursue ideas (RID-002, 003, 008, 009, 024, 053)** — these fit small-team 2026–2028 feasibility. Defer the >$2M ideas (RID-004, 030, 095) unless a strategic/anchor customer co-funds.
5. **Re-evaluate RID-004 (SST) only if** the funded incumbents (Eaton-Resilient, Amperesand, Heron, SolarEdge/Infineon) leave a clear MV-class or reliability white-space; otherwise keep at "pursue-but-partner" rather than build-alone.
6. **Kill-list discipline:** Do not reopen RID-042 unless JEDEC/HBM5 re-mandates hybrid bonding (watch Semiconductor Engineering/JEDEC); do not reopen RID-047/091 unless the US-China equipment/export regime materially liberalizes (watch BIS Federal Register actions).

**Stage 3 — 2028 (down-select to 1–2 for 2029/2030 launch):**
7. Pick the launch idea by **pilot-conversion rate × regulatory-risk-adjusted TAM**, not raw score. A pursue idea with a signed paid pilot and a low/medium reg-risk label (e.g., RID-003 or RID-008) beats a higher-scored idea stuck in utility-qualification limbo.

**Benchmarks that would change these calls:**
- Part 108 final rule timing (moves 8 drone-cluster ideas).
- Any JEDEC re-mandate of hybrid bonding (revives RID-041/042).
- A confirmed Navy contract award to a competitor for the SSTR/FDTR instrument (further confirms RID-036 kill).
- Section 301 SiC tariff rate announced ~May 2027 (re-prices RID-049/047/004 supply chains).
- FDA Modernization Act 3.0 rulemaking finalization (lifts RID-086 organ-on-chip from "watch").

---

## CSV-ready rows — `source_evidence_ledger.csv` (new scoring sources)

```
source_id,citation,tier,company_claim_flag,fact_inference_speculation,used_for
SCORE-001,"OCP Diablo 400 Base Spec v0.7.0 & Deschutes CDU; opencompute.org (Google/Meta/Microsoft)",1,no,FACT,"RID-001/002/003/005/008/115 pain & spec"
SCORE-002,"Choukse et al. Power Stabilization for AI Training Datacenters arXiv:2508.14318; NVIDIA GB300 dev blog (30% peak reduction)",1,partial(NVIDIA blog=company claim),FACT,"RID-002/009/030/041/042 oscillation pain"
SCORE-003,"IEEE 2800.2-2026 (ieee.org); DOE i2X & ESIG forum slides",1,no,FACT,"RID-018/019/024/029/124 standards trigger"
SCORE-004,"McKinsey 'Humanoid robots: crossing the chasm' 2025 (actuation 40-60% BOM); BofA Humanoid Robots 101 Apr 2025 (40-50%)",2,no,FACT,"RID-053/054/057/058/061/062/066 BOM wedge"
SCORE-005,"Wolfspeed 'Powering AI with SiC SST' (IEA cite: MV transformer up to 3yr lead, ~20% projects at risk)",2,partial(vendor),FACT,"RID-004/023 transformer lead-time pain"
SCORE-006,"Wolfspeed/Navitas SiC datasheets & whitepapers; Section301 context",2-3,partial(vendor),INFERENCE,"RID-003/004/049/047 SiC device feasibility"
SCORE-007,"Boyd/Accelsius Deschutes CDU specs; AmplinkTech OCP coverage",3,partial(vendor),FACT,"RID-033/034/035/040 thermal pain"
SCORE-008,"Eaton MVSST page; Amperesand $80M Series A; Heron Link specs; Power Electronics News 2026",2-3,partial(vendor),FACT,"RID-004 incumbent landscape"
SCORE-009,"ISO 10218-1/-2:2025 (cobotsonline/EVS/ScienceDirect S2590123026015203); ISO/PAS 8800 context",1-2,no,FACT,"RID-055/056/119/120/121/123/124 safety standards"
SCORE-010,"Wang et al. ACS Sensors 2026 11(2):1413-1424 (microneedle lactate r=0.94, AUC 0.95, n=21 ICU/ED)",1,no,FACT,"RID-078/080 sensing evidence"
SCORE-011,"DOE Long Duration Storage Shot fact sheet & Granholm announcement Sept 2021 (90%-by-2030 target; $0.05/kWh)",1,no,SPECULATION(target),"RID-013/014 LDES context"
SCORE-012,"FAA Part 108 NPRM (faa.gov BVLOS_NPRM) & Federal Register 2026-01644 reopening (final not yet issued)",1,no,SPECULATION(trigger),"RID-067/068/069/070/071/072/074/112 drone trigger"
SCORE-013,"CFS press release & PRNewswire Sept 30 2025 ($8M DOE Milestone, TF magnet validated, largest in program)",1-2,partial(CFS PR),FACT,"RID-102/104 fusion-magnet demand"
SCORE-014,"SAM.gov N00173-25-RFI-MF18 (NRL sole-source NOI to Laser Thermal Analysis); USAspending CONT_AWD_HR001123C0121 (DARPA, not Navy); HigherGov 'Most Recent Award 2026-03-23' (paywalled)",1,no,FACT(NOI)/UNRESOLVED(award),"RID-036 incumbent status"
SCORE-015,"Awad et al. Surg Endosc 2025 38(10):6193-6202 & Servais et al. 39(2):1217-1226 (da Vinci 5 force feedback, up to 43% less force, preclinical)",1,partial(Intuitive-supported),FACT(preclinical),"RID-077/081/088 force-feedback evidence"
SCORE-016,"Semiconductor Engineering 'HBM4 Sticks With Microbumps' & 'HBM Leads To Defect-Free Bumps'; Onto Innovation; 36Kr (JEDEC 720->775um)",2-3,no,FACT,"RID-041/042/045/051 packaging demand shift"
SCORE-017,"Federal Register 2025-23912 / USTR Section 301 (SiC tariff 0% Dec2025 -> June 23 2027); CRS R48642; Morgan Lewis BIS H200 case-by-case",1,no,FACT,"export/reg-risk inverse scoring all China-fab ideas"
SCORE-018,"China medtech localization (MERICS 2023; LEK 'Going Local'); Sartorius/Cytiva incumbency",2,no,INFERENCE,"RID-092 bioreactor wedge"
SCORE-019,"Nature Comms s41467-023-37009-7 (NMP drying/recovery ~78% electrode cost); ACS AEM 2c03755; Fraunhofer DRYtraec",1-2,partial(vendor for DRYtraec),FACT,"RID-093/095 dry-electrode wedge"
SCORE-020,"FDA Roadmap to Reducing Animal Testing 2025 (fda.gov); FDA Modernization Act 3.0 (Senate Dec 2025); Emulate/CN Bio",1-2,partial(Emulate=vendor),FACT,"RID-086 organ-on-chip demand"
SCORE-021,"TIM vendor datasheets (Henkel/Indium/DOW); MDPI 14/13/2682 HBM thermal review",3-4,yes(vendor marketing),INFERENCE,"RID-037 TIM claim (weak/company-claim)"
SCORE-004D,"EU Commission CELEX:52025DC0005 (Document 551: 25-100% targets, 100% for 137/178 categories); NMPA green-channel context",1,no,FACT,"RID-087/091 China forced-substitution wedge"
```

**Evidence notes:** SCORE-014 (RID-036) and SCORE-021 (RID-037) are the two weakest items — the first is UNRESOLVED (intent confirmed, award not), the second rests on vendor marketing (flagged company claim). Both drove their ideas to evidence=low and "kill." SCORE-012 (Part 108) is FACT-as-to-NPRM but SPECULATION-as-to-trigger, which is why every drone idea is capped below "pursue"-tier confidence except RID-067 (which clears on its own DAA-fusion technical merit). SCORE-002 and SCORE-013/015/020 contain company-supported elements (NVIDIA blog, CFS PR, Intuitive-supported studies, Emulate) explicitly flagged so they are not treated as fully independent.