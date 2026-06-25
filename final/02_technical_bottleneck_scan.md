# Technical Bottleneck Scan (Phase 12): 12-Domain Technology-Pull Map of Engineering Chokepoints, 2026–2030

## TL;DR
- Across all 12 domains, the densest cluster of small-team-buildable, reduced-cleanroom, near-zero-Stanford-IP wedges sits in **grid/power-distribution components and quality/metrology subsystems** — DC protection and arc-safe connectors (OCP Diablo 400 spec, v0.5.2 dated 2025-05-30), rack-level GPU power-transient smoothing (Choukse et al., arXiv:2508.14318, Aug 20 2025), in-line/post-bond inspection (hybrid bonding, panel-level packaging), and self-calibrating sensors — **not** in the AI-power/advanced-packaging clusters the macro scan already over-weighted.
- The highest-conviction, named-buyer bottlenecks include: 800VDC DC protection/connectors (buyers: Foxconn Kaohsiung-1, CoreWeave, Oracle, the Microsoft/Meta/Google OCP working group; signal: OCP Mt. Diablo/Diablo 400 spec, 2025); GPU power-transient smoothing storage (buyer: Microsoft/OpenAI; arXiv Aug 2025); hybrid-bonding void/overlay metrology (buyers: TSMC, Intel, SK hynix; Semiengineering/IRDS 2026); humanoid actuator/tactile stacks (buyers: Tesla, Figure; McKinsey/IDTechEx 2026); and BVLOS detect-and-avoid (buyers: utility/logistics operators; FAA Part 108 NPRM, Aug 7 2025, final rule expected ~spring 2026 under the June 5 2025 executive order's 240-day deadline).
- Founder-fit annotation: the transferable WBG/plasma/cleanroom-adjacent skillset maps best onto **extreme-environment electronics, solid-state DC protection, sensor calibration, and metrology** wedges that need high-reliability hardware-software integration with only Low/Medium cleanroom burden — while energy storage, robotics, drones, and biomedical offer the broadest greenfield where the founder competes less on physics pedigree and more on systems integration.

## Key Findings

The scan covered all 12 domains independently. Several cross-cutting patterns emerged:

1. **Protection and interconnect lag power conversion.** The industry is rushing to 800VDC/MW-scale racks and MVDC grids, but **DC fault interruption has no natural current zero-crossing**, so solid-state circuit breakers, arc-safe connectors, and DC-specific protection standards are immature. This recurs in data centers (OCP Diablo 400), MVDC grids (Infineon/Siemens SSCB), and behind-the-meter power.

2. **Metrology/inspection is the binding yield constraint** wherever a new integration method scales — hybrid bonding (buried voids invisible to optical), panel-level/glass substrate (warpage, sub-2µm RDL overlay), additive manufacturing (in-situ NDE), and battery manufacturing (defect detection in solid electrolytes).

3. **Calibration drift and sensing reliability** are unsolved across MEMS gas sensors, photonic sensors, IMUs, and grid-edge sensors — a recurring "self-calibration / drift-compensation" wedge.

4. **The "no engine supplier" problem in actuation** — there is no standardized supplier for humanoid actuators, tactile sensors, harmonic drives, or planetary roller screws; every robot program does custom development (McKinsey, IDTechEx 2026).

5. **Power-quality transients are now a grid-stability threat**, not just a chip problem — per Choukse et al. (arXiv:2508.14318, Aug 20 2025) and the companion Microsoft Azure blog, utilities impose "limits on the magnitude of oscillations within critical frequency ranges (e.g., 0.1–20 Hz)," and "aggregate power consumption can oscillate by tens of megawatts within a single datacenter"; Microsoft co-developed a power-smoothing feature with NVIDIA introduced in GB200 GPUs.

## Details

### A) Table of Technical Bottlenecks / Opportunity Seeds (≈130 seeds)

Columns: Domain | Bottleneck/opportunity seed | Technical reason it exists | Customer pain | Possible first product | Prototype feasibility before 2029 | Cleanroom dependency | Key suppliers/components | Main incumbents | Source IDs | Source tier mix | Confidence

#### Domain 1 — Energy storage and battery systems

1. Energy storage | Sulfide solid-electrolyte moisture/H2S control in pilot lines | Sulfides need ultra-dry handling; minor moisture cuts ionic conductivity and releases H2S | Pilot lines stall on contamination, yield, and safety | Inline H2S/moisture sensing + dry-room contamination-control module for SE lines | Med | Low | Solid Power/SK On lines; lithium sulfide precursors | Solid Power, Toyota, Samsung SDI | TB-001; EN-* | T1 (Wiley Adv Mater 2026, IOP roadmap 2026, SEC) + T3 | High
2. Energy storage | Solid-state cathode/SE interface defects ("needle in haystack") | Interfacial voids/dendrite initiation limit cycle life to ~hundreds–1,000 cycles | Cells fail early; no scalable defect screen | In-line interface defect inspection for ASSB stacks | Med | Low | Roll coaters, sintering tools | QuantumScape, Solid Power | TB-001 | T1+T3 | Med
3. Energy storage | Na-ion solid electrolyte low-cost synthesis | Thio-borohydride routes reduce cost/temperature but unproven at scale | LFP/Li-ion cost floor hard to beat without cheap SE | Na-B-H-S electrolyte process/precursor supply | Low | Low | NaBH4 precursors | CATL, GM (Na-ion R&D) | TB-002 | T1 (PMC) | Med
4. Energy storage | Iron-air / LDES balance-of-system reliability | Multi-day chemistries have novel BOS (air handling, corrosion) not yet field-hardened | Utilities need bankable 10+ hr systems to backfill coal | Air-handling/corrosion-control subsystem or BMS for iron-air | Med | None | Form Energy supply chain | Form Energy | EN-*; TB-003 | T1 (DOE) + T3 | Med
5. Energy storage | LDES cost above DOE Storage Shot threshold (LAES/CAES) | Thermodynamic round-trip losses and capex keep LCOS high | LCOS far above target; no bankable offtake | Thermal/round-trip efficiency improvement component | Low | None | — | Highview, Hydrostor | EN-* | T1 (DOE Liftoff) + T3 | Med
6. Energy storage | Grid-battery thermal runaway propagation safety | High-density BESS packs risk cascading failures | Insurers/AHJs demand propagation control | Cell-to-cell propagation-barrier / early off-gas detector | High | Low | Off-gas sensors, intumescents | Fluence, Tesla Megapack | EN-* | T2/T3 | Med
7. Energy storage | Fast-charge degradation sensing in BMS | Li plating during fast charge is hard to detect in real time | Fleet/EV warranty risk; conservative charging | Embedded plating-detection BMS algorithm + sensor | High | None | Current/voltage sensors | major BMS vendors | TB-001 | T2/T3 | Med
8. Energy storage | Second-life battery state-of-health grading | SOH/RUL hard to certify cheaply per cell | Recyclers/repurposers lack fast grading | Rapid impedance-spectroscopy grading instrument | High | None | EIS hardware | — | TB-001 | T3 | Med
9. Energy storage | Flow-battery membrane/stack durability | Membrane fouling and crossover degrade efficiency | High maintenance for long-duration flow | Membrane health sensor or low-cost stack component | Med | Low | ion-exchange membranes | ESS Inc., Invinity | EN-* | T3 | Low

#### Domain 2 — Power electronics and high-voltage systems

10. Power electronics | MV solid-state circuit breaker gate-drive/power supply | DC faults lack zero-crossing; series JFETs need isolated, fast, self-powered gate drives | Mechanical breakers too slow; SSCBs costly/unreliable | Compact MV-insulated self-powered gate-driver module for SSCBs | Med | Low | SiC JFET (Infineon CoolSiC), magnetics | Infineon, Siemens, ABB | TB-004; SC-* | T1 (IEEE Xplore) + T2 | High
11. Power electronics | 800VDC connector arc-prevention (LMFB short pins) | DC arcing on disconnect; connectors need last-mate-first-break + latching switch | Data-center electricians face arc-flash hazard at 800V | Arc-safe 800VDC connector/latch subsystem per Diablo 400 | High | Low | connector housings | Amphenol, TE | TB-005; EN-* | T1 (OCP spec) | High
12. Power electronics | Solid-state transformer (13.8kV AC→800VDC) | Multi-stage AC/DC conversion is lossy; SST collapses stages | Hyperscalers want grid-to-rack DC efficiency | SST building block or control card | Low | Low | SiC modules (Microchip 3.3kV) | Navitas, Hitachi | TB-005; SC-* | T1 (SEC, NVIDIA) | Med
13. Power electronics | Power-device capacitor/magnetics at MW-rack density | DC-link caps and inductors limit power density/thermals | Rack power shelves consume compute U-space | High-density DC-link capacitor or planar magnetic | Med | Med | film caps, magnetics | TDK, Vishay | EN-*; SC-* | T3 | Med
14. Power electronics | Gate-driver robustness for paralleled SiC | Current sharing/oscillation in paralleled die | Module failures, derating | Active gate-driver IC with current balancing | Med | Med | SiC die | Infineon, onsemi | SC-* | T2/T3 | Med
15. Power electronics | HVDC fault-current limiting control | GFM converters can't supply large fault current | Protection coordination breaks at high IBR penetration | Fault-current-limiting control IP / cross-forming control | Med | None | converter hardware | Hitachi, GE | TB-006 | T1 (arXiv) | Med
16. Power electronics | SiC substrate supply / Section 301 tariff exposure | Tariff scheduled June 23 2027 on SiC substrates | Supply/cost risk for SiC device makers | Domestic SiC substrate process or defect-reduction tool | Low | High | SiC boules | Wolfspeed, Coherent | SC-*; US-* | T3 | Low
17. Power electronics | Cryogenic power electronics for LH2/aerospace | SiC Ron rises, becomes non-Ohmic <60K; GaN improves | No qualified cryo inverter for LH2 aircraft | Cryo-rated gate driver / GaN half-bridge module | Low | Med | GaN HEMT, SiC | — | TB-007 | T1 (ResearchGate/arXiv) | Med

#### Domain 3 — Grid modernization and DER/VPP

18. Grid | GFM inverter protective-relay miscoordination | GFM current-limiting changes fault signatures; relays misoperate | Utilities can't protect 100%-IBR feeders | GFM-aware protection relay / settings IP | Med | None | relays, PMUs | SEL, Hitachi | TB-006; TB-008 | T1 (Sandia, IEEE 2800.1) | High
19. Grid | Distribution transformer health/aging sensing | DER + EV nonlinear loads accelerate transformer aging unpredictably | Long transformer lead times make failures catastrophic | Retrofit transformer health monitor (optical/thermal) | High | None | optical/thermal sensors | GE Vernova, Hitachi | TB-009; EN-* | T1 (USPTO) + T3 | High
20. Grid | Grid-DERMS ↔ edge-DERMS interoperability | Two DERMS layers don't share state; IEC 61850 modeling gaps | VPPs can't dispatch DERs to solve grid problems | Translation/interoperability middleware appliance | High | None | IEC 61850, XMPP | AutoGrid, Schneider | TB-010 | T2/T3 | Med
21. Grid | Synchrophasor/PMU at distribution edge | Distribution lacks cheap wide-bandwidth sensing | No observability for DER-rich feeders | Low-cost distribution micro-PMU | High | Low | ADCs, GPS timing | SEL, Schweitzer | TB-008 | T2/T3 | Med
22. Grid | Interconnection study automation (EMT models) | EMT studies are slow and bespoke; ~2,290 GW remained active in US interconnection queues at end of 2024 (1,400 GW generation + 890 GW storage across ~10,300 projects), and median time from request to commercial operation has doubled from <2 years (2000–2007) to over 4 years (2018–2024), per LBNL "Queued Up: 2025 Edition" (Rand et al.) | Multi-year interconnection delays | Automated EMT model-generation/validation tool | Med | None | — | PSCAD, PowerWorld | EN-*; TB-046 | T1 (LBNL, DOE i2X) + T3 | Med
23. Grid | Grid-forming BESS plant-level controller | IEEE 2800.2-2026 conformity test/verification new | Developers must prove GFM compliance | GFM plant controller + conformity test rig | Med | None | inverters | SMA, Huawei | TB-008 | T1 (IEEE) | Med
24. Grid | GOES electrical-steel-free transformer core | Cleveland-Cliffs sole US GOES source bottleneck | Core material constrains transformer output | Amorphous/nanocrystalline core alternative | Low | Med | amorphous ribbon | Hitachi Metals | EN-*; TB-009 | T3 | Low
25. Grid | Solid-state transformer for distribution | Conventional transformers slow to make, no controllability | Want controllable, compact distribution assets | Distribution-class SST module | Low | Med | SiC modules | — | SC-*; EN-* | T3 | Low

#### Domain 4 — Data-center energy and thermal management

26. Data center | GPU power-transient smoothing (rack storage) | Synchronized training causes oscillations in the utility-critical 0.1–20 Hz band; "aggregate power consumption can oscillate by tens of megawatts within a single datacenter" (Choukse et al., arXiv:2508.14318, Aug 20 2025); GW-scale ramp rates exceed 1000 MW/s | Utilities trip; hyperscalers face interconnect limits | Rack-level supercap/battery smoothing module + controller | High | Low | supercaps, BBU/CBU | Microsoft/NVIDIA in-house (GB200 power-smoothing) | TB-011; EN-* | T1 (arXiv 2508.14318) | High
27. Data center | CDU production capacity & reliability | Cold-plate brazing/leak-test is specialized; CDU pumps need redesign for non-conductive fluids | Customers can't deploy without CDUs even with power | Leak-test or pump/valve subsystem for non-conductive fluids | High | Low | pumps, cold plates | Vertiv, Boyd, Modine | TB-012; EN-* | T2/T3 | High
28. Data center | Microfluidic in-silicon cooling (TSV/microchannel) | Channels must be fine yet not weaken silicon; extra etch steps raise cost; ARPA-E Coolerchips $3.25M support | Thermal ceiling on >1kW chips | Microchannel cold-plate bonding/inspection process | Med | High | MEMS etch, TIMs | TSMC, Microsoft/Corintis, HP | TB-013; SC-* | T1+T3 | Med
29. Data center | TIM1/1.5 for advanced packages | Thermal interface at die level limits heat extraction | Hotspots cap performance | High-conductivity TIM1.5 material | Med | Med | TIM materials | Honeywell, DuPont | SC-* | T2/T3 | Med
30. Data center | Two-phase immersion coolant chemistry/compatibility | Coolant-material compatibility (hoses, plastics) unresolved | Adoption stalls on materials/leaks | Coolant compatibility test service or additive | Med | Low | fluids | LiquidStack, 3M (exited) | TB-012 | T3 | Low
31. Data center | Heat reuse: coolant outlet temp too low | Air/liquid outlet 32–60°C below district-heat supply ~90°C; ORNL Frontier loop 32°C upgraded to 85°C via HT heat pump | Waste heat unusable without heat pumps | High-temp coolant loop or compact high-temp heat pump | Med | None | heat pumps | Fortum (Microsoft Finland), ORNL | TB-014 | T1 (Energy & Buildings 2024) + T3 | Med
32. Data center | In-rack DC protection (SSCB for 800VDC) | DC fault no zero-cross; UL 1500V breakers just emerging (ABB Infinitus, LS Electric) | Arc/fire risk; no qualified DC breaker | DC SSCB module for rack/sidecar | Med | Low | SiC, ABB Infinitus | ABB, LS Electric | TB-005; EN-* | T1 (OCP) + T3 | High
33. Data center | Leak detection for liquid-cooled racks | Conductive coolant near electronics; fast detection needed | Single leak can destroy a rack | Distributed optical/capacitive leak-detection harness | High | Low | fiber/sensors | nVent, Vertiv | TB-012 | T3 | Med

#### Domain 5 — Semiconductor manufacturing, packaging, inspection

34. Semis | Hybrid-bonding buried void/disbond detection | Voids only nm deep; invisible to optical alone | Yield loss undetectable until electrical fail | Acoustic/AFM hybrid metrology for post-bond inspection | Med | High | AFM, acoustic, IR | Onto, Bruker, Camtek | SC-*; TB-015 | T1 (Semiengineering, USPTO) | High
35. Semis | Fine-pitch overlay metrology (5–7µm bond pitch) | Overlay accuracy must scale to tens of nm across wafer | Bonding yield collapses at fine pitch | Through-stack NIR/SWIR overlay metrology | Med | High | NIR/SWIR optics | Onto, KLA | SC-*; TB-015 | T1 | High
36. Semis | Panel-level packaging warpage control | Large panels warp at assembly temps; reduces yield | CoPoS/FOPLP ramp blocked by warpage | Warpage-measurement/compensation system or DAF material | Med | High | DAF, metrology | TSMC, ASE, Amkor | TB-016; SC-* | T1 (TrendForce, Semiengineering) | High
37. Semis | Panel RDL sub-2µm photoresist | Existing resist/overlay out of margin at <2µm L/S | Glass-panel RDL can't hit resolution | New photoresist chemistry / large-panel cure tooling | Low | High | photoresist | JSR, Fraunhofer IZM | TB-016 | T1 (Semiengineering) | Med
38. Semis | Through-glass via (TGV) formation yield | LIDE/laser ablation reliability for glass substrates | Glass substrate ramp 2028–29 gated on TGV | TGV inspection or process-control module | Low | High | laser, glass | Corning, Absolics | TB-017; SC-* | T1 (IDTechEx) + T3 | Med
39. Semis | Glass substrate micro-crack detection | Glass fragile; cracks cause catastrophic failure | Yield/reliability risk at scale | In-line crack/edge-defect inspection for glass | Med | High | imaging | Intel, Samsung | TB-017 | T3 | Med
40. Semis | Chiplet known-good-die test | Pre-bond KGD test gaps raise stacked-die scrap cost | One bad die scraps whole stack | Pre-bond die test/metrology insert | Med | High | probe, test | Advantest, Teradyne | SC-* | T2/T3 | Med
41. Semis | Specialty gas/precursor purity monitoring | Trace contaminants ruin advanced nodes | Supply quality variance | Inline gas-purity sensor | Med | High | analyzers | Entegris, Linde | SC-* | T3 | Low
42. Semis | EUV defect/stochastic inspection | Stochastic defects at low-dose EUV | Yield variance | Stochastic-defect detection software/hardware | Low | High | e-beam | KLA, ASML | SC-* | T3 | Low
43. Semis | Co-packaged optics assembly/test | Fiber-chip coupling alignment at scale | CPO ramp gated on assembly | CPO alignment/test subsystem | Low | High | photonics | Broadcom, TSMC | SC-* | T3 | Low

#### Domain 6 — Robotics and industrial automation

44. Robotics | No standard humanoid actuator supplier | Every program custom-builds joint actuators (motor+gearbox+drive+sensor) | High cost, no scale, long qualification | Standardized modular joint-actuator product line | Med | Low | frameless BLDC, encoders | Harmonic Drive, Nabtesco, Tesla | TB-018; AI-* | T2 (McKinsey, IDTechEx) | High
45. Robotics | Harmonic/strain-wave gearbox supply concentration | Precision-bound, capital-intensive; few suppliers | Supply bottleneck caps humanoid volume | Lower-cost strain-wave reducer or QC metrology | Med | Low | precision gears | Harmonic Drive, Nabtesco, Leaderdrive | TB-018 | T2 | High
46. Robotics | Planetary roller screw narrow supply | High-load/precision niche, narrow supplier base | Acute supply risk for linear actuators | Roller-screw manufacturing/metrology | Low | Low | precision screws | Rollvis, GSA | TB-018 | T2 | Med
47. Robotics | Tactile sensing — no dominant design | No standardized architecture for robot-grade tactile | Hands can't do dexterous tasks | Robust tactile sensor array / skin module | Med | Med | MEMS, polymers | no incumbent | TB-018; AI-* | T2 (McKinsey) | High
48. Robotics | Compact 6-axis force/torque sensor | Multi-axis sensors need 50–100mm joint space | Limits articulated-limb integration | Miniature 6-axis F/T sensor | Med | Med | strain gauges, MEMS | ATI, Bota | TB-019 | T3 | Med
49. Robotics | Rare-earth-magnet-light actuators | China manufactures >90% of rare-earth magnets and holds ~90% of separation/refining capacity (IDTechEx "Rare Earth Magnets 2026-2036"); Tesla needs ~3.5 kg NdFeB per Optimus, and China's April 2025 export licensing on seven rare earths disrupted Optimus production (Musk, Q1 2025 call) | Magnet supply constrains Optimus | Reduced-/no-rare-earth motor design | Med | Low | ferrite, SMC | — | TB-018 | T2 (McKinsey/IDTechEx) | Med
50. Robotics | Sim-to-real transfer for manipulation | Policies trained in sim fail on real dynamics/contact | Deployment unreliable; long tuning | Sim-to-real calibration/validation toolchain | Med | None | sim platforms | NVIDIA Isaac | AI-* | T3 | Med
51. Robotics | Safety controller for collaborative/humanoid | Functional-safety certification for mobile manipulators | Can't deploy near humans without certified safety | Certified safety controller / safety-rated perception | Med | Low | safety PLCs | Pilz, SICK | TB-020 | T2/T3 | Med
52. Robotics | Robot battery energy density/thermal | Higher capacity adds weight, reduces runtime | Short runtime, downtime to charge | High-density robot battery pack + thermal mgmt | Med | Low | cells | — | TB-021; AI-* | T2 (IDTechEx) | Med
53. Robotics | Fleet orchestration determinism | Multi-robot coordination lacks real-time guarantees | Throughput/safety in mixed fleets | Deterministic fleet-orchestration middleware | High | None | — | — | AI-* | T3 | Low
54. Robotics | High-bandwidth tactile data processing | >1kHz 6-axis data overwhelms controllers | Real-time control bottleneck | Edge signal-conditioning ASIC/module for tactile | Med | Med | DSP, ADC | — | TB-019 | T3 | Med

#### Domain 7 — Low-altitude economy, drones, autonomy

55. Drones | Detect-and-avoid (DAA) certification-grade sensing | Part 108 mandates DAA; performance-based airworthiness | Operators can't fly BVLOS without certifiable DAA | Certifiable DAA sensor+algorithm module | Med | Low | radar, EO/IR | Iris, uAvionix | TB-022 | T1 (FAA Part 108 NPRM) | High
56. Drones | Resilient C2 link for BVLOS | Continuous command/control link required | Link loss aborts missions | Multi-link redundant C2 module | High | None | cellular, SATCOM | Elsight, uAvionix | TB-022 | T2/T3 | Med
57. Drones | UTM strategic deconfliction fairness/scale | FCFS deconfliction unfair/unscalable at density | Can't scale overlapping BVLOS ops | Deconfliction algorithm / USS software (Part 146) | High | None | — | ANRA, OneSky | TB-023 | T1 (FAA, NASA) | Med
58. Drones | Electronic conspicuity (low-alt traffic) | Part 108 reopened comment on conspicuity Jan 28 2026 | Mixed manned/unmanned collision risk | Low-SWaP conspicuity beacon/receiver | High | Low | ADS-B, RID | uAvionix | TB-022 | T1 (FAA) | Med
59. Drones | Propulsion/endurance for cargo BVLOS | Battery energy density caps range/payload | Limited mission radius | Hybrid powertrain or high-density pack | Med | Low | cells, fuel cells | — | TB-021 | T3 | Med
60. Drones | Counter-UAS detection in cluttered RF/urban | Lawful emitters mask threats near populated areas | Bases/airports need safe C-UAS sensing | Passive RF/acoustic C-UAS sensor for urban | Med | Low | SDR, acoustic | DIU vendors | TB-024 | T1 (DIU solicitation) | Med
61. Drones | Drone-in-a-box autonomy reliability | Remote dispatch needs maintenance/landing reliability | Downtime, manual intervention | Autonomous docking/charging/health subsystem | High | Low | — | Skydio, Percepto | TB-022 | T3 | Med
62. Drones | BVLOS airworthiness for non-US manufacturers | Part 108 excludes makers without bilateral agreements | Supply/compliance risk | Compliant US-made avionics/airframe subsystem | Med | Low | — | Skydio | TB-022 | T1 (FAA) | Med

#### Domain 8 — Biomedical devices and bio-instrumentation

63. Biomedical | Microneedle CGM lifetime/biofouling | Enzymatic electrodes drift; 14-day life; fouling | Patients want longer-wear, calibration-free | Bioresorbable/optical microneedle CGM sensor | Med | Med | microneedle arrays | Abbott, Dexcom, Senseonics | TB-025; BM-* | T1 (Science Advances, FDA) | Med
64. Biomedical | Surgical robot force feedback instruments | Lack of tactile sensation in MIS; FFB new on dV5 (2024) | Surgeons over-tension tissue without haptics | Force-sensing instrument tip / FBG force sensor | Med | Med | FBG, strain | Intuitive Surgical | TB-026; BM-* | T1 (PMC, ClinicalTrials) | High
65. Biomedical | Sensorless/vision-based surgical force estimation | Sterilizable force sensors hard; ML estimates forces | Cost/sterilization barriers to haptics | Vision-based force-estimation software module | Med | None | cameras | Intuitive, Medtronic | TB-027 | T1 (arXiv) | Med
66. Biomedical | Implantable electrode chronic stability | Foreign-body response degrades neural electrodes | Neurotech signal loss over months | Anti-fouling/flexible electrode coating | Low | High | thin-film, polymers | Neuralink, Synchron | BM-* | T3 | Low
67. Biomedical | Point-of-care microfluidic sample prep | Sample-to-answer integration hard outside lab | Decentralized testing needs robust prep | Cartridge sample-prep module | Med | Med | microfluidics | Cepheid, Abbott | BM-* | T3 | Med
68. Biomedical | Lab automation liquid-handling precision | Low-volume dispensing accuracy/traceability | Reproducibility crisis; throughput | Precision acoustic/inkjet dispensing subsystem | Med | Med | piezo, acoustic | Tecan, Hamilton | BM-* | T3 | Med
69. Biomedical | Continuous multi-analyte (beyond glucose) | Aptamer/enzyme stability for lactate/ketone/drugs | No multi-analyte wearable | Multi-analyte microneedle/wearable biosensor | Med | Med | aptamers | — | TB-025 | T3 | Low
70. Biomedical | Wearable biosensor calibration drift | Enzyme/aptamer sensitivity drifts in vivo | Frequent recalibration limits adoption | On-body self-calibration scheme | Med | Med | — | — | TB-025 | T3 | Med
71. Biomedical | Miniaturized tendon-driven surgical micro-actuators | Scaling actuation to micro-surgery | No fine micro-manipulation tools | Tendon-driven micro-actuator module | Low | Med | micro-actuators | Intuitive, Medical Microinstruments | TB-019 | T3 | Low

#### Domain 9 — Advanced manufacturing and quality automation

72. Adv mfg | In-situ NDE for laser powder-bed fusion | Post-process CT slow/costly; in-line hard during SLM | Can't catch porosity/lack-of-fusion in real time | In-process thermographic/acoustic monitoring module | Med | Low | IR camera, AE | EOS, Velo3D | TB-028; EX-* | T1 (NIST, PMC) | High
73. Adv mfg | Metrology throughput bottleneck | CT/3D scan takes hours; manual scanning labor-intensive | Inspection can't keep up with production | Automated robotic scanning + AI defect recognition | High | Low | CT, robots | Zeiss, Nikon | TB-029; EX-* | T1 (Metrology News) | High
74. Adv mfg | Ceramic AM defect/feedstock variability | No standardized feedstock characterization; high defect | Inconsistent ceramic-part quality | Feedstock characterization + in-process monitor | Med | Low | — | — | TB-030 | T1 (NIST event) | Med
75. Adv mfg | In-process eddy-current/ultrasound for DED | Conventional NDE is post-manufacturing | Defects found too late; scrap cost | In-cell ultrasound/eddy-current inspection robot | Med | Low | UT, EC probes | — | TB-031 | T1 (ScienceDirect) | Med
76. Adv mfg | Digital-thread traceability for high-assurance | Procurement now requires part-to-inspection data linkage | Buyers demand traceable quality data | Quality-data management / digital-thread appliance | High | None | software | Materialise, Siemens | TB-032 | T2 (3D Printing Industry) | Med
77. Adv mfg | Precision-machining in-line metrology | Closed-loop correction lacking on machine | Drift/tool wear cause scrap | On-machine probing + compensation system | High | None | probes | Renishaw, Zeiss | EX-* | T3 | Med
78. Adv mfg | Assembly automation for high-mix/low-volume | Fixturing/programming overhead for small batches | Can't automate variable assembly economically | Flexible vision-guided assembly cell | Med | None | vision, cobots | FANUC, Universal Robots | AI-* | T3 | Med
79. Adv mfg | Weld/joint NDE automation | Manual weld inspection slow, subjective | QA bottleneck in heavy fab | Automated weld-NDE system | High | None | UT, RT | Olympus/Evident | EX-* | T3 | Low
80. Adv mfg | AM micro-nano damage precursor detection | Surface damage precursors multi-scale, noisy | Quality monitoring not automated | Polarization-imaging + DL inspection module | Med | Low | polarization optics | — | TB-033 | T1 (PMC) | Med

#### Domain 10 — Extreme-environment systems

81. Extreme | High-temp downhole electronics (250–400°C) | Si leakage; packaging fails at high T | Geothermal/O&G sensing limited by electronics | AlGaN/GaN or SOI high-temp sensor/transistor package | Low | High | AlGaN/GaN, SOI, ceramic | Analog Devices, Honeywell | TB-034; EX-* | T1 (USPTO, ADI) | Med
82. Extreme | High-temp electronics packaging (bare die/ceramic) | Standard packages fail; hybrid ceramic costly/slow | No off-the-shelf high-T modules | High-T ceramic package / die-attach material | Low | High | ceramic, sinter-Ag | — | TB-035; EX-* | T1 (Hart Energy, ABB) | Med
83. Extreme | Rad-hard SiC for space power | Radiation effects on WBG devices | Space power systems need rad-hard SiC | Rad-hard SiC device/qualification data | Low | High | SiC | — | SC-*; EX-* | T3 | Low
84. Extreme | Cryogenic readout electronics for quantum | SiC MOSFETs unstable at deep cryo; contact issues | No reliable cryo control electronics | Cryo-CMOS/GaN readout module | Low | High | GaN, CMOS | — | TB-007 | T1 (arXiv) | Low
85. Extreme | Nuclear/molten-salt materials sensing | Corrosion/high-T in molten salt reactors | No in-situ sensing in molten salt | High-T corrosion-resistant sensor probe | Low | Med | refractory alloys | — | EX-* | T3 | Low
86. Extreme | Deep-sea high-pressure electronics housing | Pressure (>20,000 psi) + corrosion | Subsea sensing reliability | Pressure-tolerant electronics module | Med | Med | oil-filled, ceramic | Teledyne | EX-* | T3 | Low
87. Extreme | Downhole high-precision instrumentation amp | Weak signals in noisy high-T front-end | Signal-chain performance limits | High-T instrumentation-amplifier IC | Low | High | SOI | Analog Devices | TB-034 | T1 (ADI) | Low
88. Extreme | Space-grade actuator/mechanism lubrication | Vacuum/thermal cycling degrade mechanisms | Mechanism reliability in space | Dry-lubricant/space-rated actuator | Low | Med | solid lubricants | — | EX-* | T3 | Low

#### Domain 11 — Sensors, actuation, and control systems

89. Sensors | MEMS gas-sensor baseline/span drift | MOX poisoning causes baseline+sensitivity drift | Frequent manual calibration; mass-market blocked | In-sensor self-calibration / drift-compensation ASIC | High | Med | MOX, micro-hotplate | Bosch, Sensirion, Figaro | TB-036; TB-037 | T1 (Wiley Adv Sci, USPTO) | High
90. Sensors | Integrated photonic sensor packaging/coupling | PIC sensors bottlenecked by fiber-chip coupling, calibration drift | SHM/industrial PIC sensors not deployable | Photonic packaging/coupling subsystem | Low | High | PIC, fiber | — | TB-038 | T1 (MDPI Sensors 2026) | Med
91. Sensors | Autonomous gas-detector recalibration | EC/MOS sensors drift, cross-sensitive; manual cal costly | Industrial gas networks costly to maintain | ML drift-correction firmware for gas detectors | High | None | — | Honeywell, Dräger | TB-039 | T1 (PMC review) | Med
92. Sensors | MEMS IMU long-term zero/scale drift | Zero/scale-factor drift limits navigation use | Short calibration validity | Self-calibrating MEMS IMU (micro-vibrator) | Med | High | MEMS gyro | Honeywell, ST | TB-040 | T1 (PMC) | Med
93. Sensors | Current/voltage sensing for SSCB/grid | Fast, isolated, accurate current sensing for protection | SSCBs need precise fault detection | Integrated current-sensor + protection IC | Med | Med | Hall, shunt | LEM, Allegro | TB-004 | T2/T3 | Med
94. Sensors | Precision actuation (piezo/voice-coil) for micro-positioning | Sub-µm positioning with thermal stability | Metrology/semiconductor stages need precision | Compact precision-actuator module | Med | Med | piezo | PI, Aerotech | EX-* | T3 | Med
95. Sensors | Magnetic field sensing for grid/EV current | High-bandwidth isolated current measurement | Power-electronics control needs better sensing | TMR/fluxgate current sensor module | Med | Med | TMR | Allegro, TDK | SC-* | T3 | Med
96. Sensors | Chemical/biosensor reference electrode stability | Reference drift limits field deployment | Field chemical sensing unreliable | Solid-state reference electrode | Med | Med | — | — | TB-039 | T3 | Low
97. Sensors | NDIR methane sensing cross-sensitivity | H2 interference, calibration needs | Methane leak detection accuracy | Compensated NDIR methane module | High | Med | IR source/detector | Winsen, Honeywell | TB-037 | T3 | Med
98. Sensors | Embedded deterministic control for power | Real-time control loops at high switching freq | Control limits converter performance | Real-time control SoC/firmware for power | Med | Low | FPGA, MCU | TI, AMD | SC-* | T3 | Med

#### Domain 12 — High-reliability embedded AI systems

99. Embedded AI | Non-deterministic AI vs ISO 26262 determinism | ML breaks deterministic safety-case assumptions | Can't certify AI perception/control | Safety-shell / runtime-monitor architecture | Med | None | — | NVIDIA, AMD, Infineon | TB-041; TB-042 | T1 (SAE, Semiengineering) | High
100. Embedded AI | ISO/PAS 8800 / TR 5469 AI-safety lifecycle gap | New standards require empirical validation | OEMs unprepared for AI safety evidence | AI-safety V&V toolchain / OOD detector | Med | None | — | Parasoft, QA Systems | TB-042; TB-043 | T1 (ISO, Embedded Computing) | High
101. Embedded AI | Deterministic latency on edge GPU inference | GPU multi-process isolation imperfect; jitter | Real-time guarantees violated | Inference-isolation/scheduling runtime | High | None | NVIDIA MPS/MIG | NVIDIA | TB-044 | T1 (arXiv 2026) | Med
102. Embedded AI | Out-of-distribution detection at runtime | Models fail silently on distribution shift | Unsafe automation under novel inputs | Runtime OOD-detection module | Med | None | — | — | TB-042 | T1 (Semiengineering) | Med
103. Embedded AI | Functional-safety island for AI compute | Need HW separation of safety vs non-safety | Mixed-criticality integration risk | Safety-island co-processor / monitor | Med | Med | FSI | NVIDIA IGX, AMD Versal | TB-045 | T1 (NVIDIA, AMD) — company claim on specs | Med
104. Embedded AI | Silent data corruption in large-scale compute | SDC undetected in training/inference at scale | Reliability of large clusters | SDC-detection/monitoring hardware-software | Med | None | — | Meta, Google | SC-* | T1 (Semiengineering paper links) | Med
105. Embedded AI | Verification of OTA model updates | New model versions must meet safety baseline post-OTA | Update breaks certified behavior | Post-OTA verification/rollback framework | High | None | — | — | TB-041 | T2/T3 | Med
106. Embedded AI | HIL latency profiling across temp/voltage | Inference latency varies with conditions | Latency budget violations at edge cases | HIL latency-profiling rig/service | High | None | — | — | TB-041 | T2/T3 | Med
107. Embedded AI | Real-time sensor fusion determinism | Fusing camera/LiDAR/IMU in real time + fault tolerance | Safety risk from conflicting/failed sensors | Deterministic fusion middleware w/ fault handling | Med | None | — | — | AI-* | T3 | Med

### B) CSV-ready evidence ledger (new TB- sources)

```
source_id,domain,tier,source_type,claim_supported,confidence,limitations,use_in_ideas
TB-001,Energy storage,1,peer-reviewed/industry,"Sulfide solid electrolytes need ultra-dry handling; moisture cuts conductivity and releases H2S; cycle life ~hundreds-1000",High,"Some figures from secondary explainer; cross-check cell data",ideas 1-2-7-8
TB-002,Energy storage,1,peer-reviewed,"Na-B-H-S thio-borohydride electrolyte lowers cost/temperature for solid-state Na-ion",Med,"Lab-scale; not yet scaled",idea 3
TB-003,Energy storage,1,gov,"DOE 'Pathways to Commercial Liftoff: LDES' (Mar 2023): US grid may need 225-460 GW LDES by 2050 (~$330B capital); requires 45-55% cost cut and 7-15% RTE improvement by 2030; iron-air contracted by utilities to backfill coal",Med,"Some context from market reports (Tier3)",ideas 4-5
TB-004,Power electronics,1,peer-reviewed,"MV SiC SSCB needs compact isolated self-powered gate drivers; passive clamping limits",High,"Lab prototypes; reliability data thin",ideas 10-93
TB-005,Power electronics,1,standard/SEC,"OCP Diablo 400 800VDC spec (v0.5.2 dated 2025-05-30); arc-safe LMFB connectors; SST 13.8kV->800VDC (Navitas/NVIDIA 8-K May 21 2025)",High,"Roadmap items 2027; NVIDIA TCO/efficiency are company claims",ideas 11-12-32
TB-006,Grid,1,peer-reviewed,"GFM inverters limited fault current; cross-forming control proposed; relay miscoordination",Med,"arXiv preprints",ideas 15-18
TB-007,Power electronics,1,peer-reviewed,"SiC Ron rises and becomes non-Ohmic <60K; SiC MOSFETs unstable at deep cryo; GaN improves",Med,"Device-specific; not productized",ideas 17-84
TB-008,Grid,1,standard,"IEEE 2800.2-2026 published spring 2026; P2800.1 GFM in development; PRC-029; FERC accepted PJM expedited interconnection track Jun 9 2026",High,"Standards in progress",ideas 18-21-23
TB-009,Grid,1,patent/journalism,"DER+EV nonlinear loads accelerate transformer aging; optical monitoring; GOES single US source",High,"Patent + trade press",ideas 19-24
TB-010,Grid,2,industry,"Grid-DERMS and edge-DERMS poorly integrated; interoperability early-stage",Med,"Industry interview",idea 20
TB-011,Data center,1,peer-reviewed,"Choukse et al. arXiv:2508.14318 (Aug 20 2025): synchronized GPU training oscillates in utility-critical 0.1-20Hz band; tens of MW per datacenter; rack storage + GB200 power-smoothing mitigation",High,"Co-authored by Microsoft/NVIDIA/OpenAI",idea 26
TB-012,Data center,2,industry/analyst,"CDU capacity is binding constraint; cold-plate brazing/leak-test specialized; pumps need redesign",High,"Analyst + vendor; some vendor capacity claims",ideas 27-30-33
TB-013,Data center,3,journalism,"Microfluidic in-silicon cooling needs fine channels w/o weakening Si; extra etch raises cost; ARPA-E Coolerchips $3.25M",Med,"Trade press; HP/NVIDIA not demonstrated (company claim)",idea 28
TB-014,Data center,1,peer-reviewed,"DC waste-heat outlet 32-60C below district-heat ~90C; ORNL Frontier loop 32C upgraded to 85C via HT heat pump",Med,"Single case study; project-specific",idea 31
TB-015,Semis,1,journalism/patent,"Hybrid-bond voids nm-deep invisible to optical; need acoustic/AFM; overlay to tens of nm",High,"Semiengineering + USPTO",ideas 34-35
TB-016,Semis,1,journalism,"PLP warpage worsens with panel size; sub-2um RDL resist out of margin; CoPoS ramp 2028-29",High,"TrendForce/Semiengineering",ideas 36-37
TB-017,Semis,2,analyst,"Glass substrates: TGV formation (LIDE/laser), micro-crack/warpage are key hurdles; Intel EMIB+glass Jan 2026",Med,"IDTechEx + trade press",ideas 38-39
TB-018,Robotics,2,consultancy,"No standard humanoid actuator supplier; harmonic-drive/roller-screw/tactile supply concentrated; China >90% rare-earth magnets, ~3.5kg NdFeB/Optimus, Apr 2025 export licensing disrupted production",High,"McKinsey/IDTechEx; some forecasts",ideas 44-45-46-47-49
TB-019,Robotics,3,market/patent,"Compact 6-axis F/T sensors need 50-100mm; high-bandwidth tactile data overwhelms control; tendon micro-actuators",Med,"Market-research tone",ideas 48-54-71
TB-020,Robotics,2,industry,"Safety controllers/certification gap for collaborative/humanoid robots",Med,"Inferred from standards",idea 51
TB-021,Robotics,2,analyst,"Robot/drone battery energy density and thermal limit runtime",Med,"IDTechEx",ideas 52-59
TB-022,Drones,1,gov,"FAA Part 108 NPRM published Aug 7 2025 (700+ pp); 60-day comment closed Oct 6 2025 (~3,100 comments); June 5 2025 EO directs final rule within 240 days (~spring 2026); mandates DAA, RID, C2; creates Part 146 ADSP; conspicuity comment Jan 28 2026; excludes non-bilateral makers",High,"Final rule not yet published",ideas 55-56-58-61-62
TB-023,Drones,1,gov,"UTM strategic deconfliction; FCFS fairness/scaling issues; Part 146 USS framework",Med,"ConOps + research",idea 57
TB-024,Drones,1,gov,"DIU seeks C-UAS for Spring 2026 Yuma test; urban RF clutter challenge",Med,"Solicitation",idea 60
TB-025,Biomedical,1,peer-reviewed,"Microneedle/enzymatic CGM drift, 14-day life, biofouling; bioresorbable/optical alternatives",Med,"Research-stage",ideas 63-69-70
TB-026,Biomedical,1,clinical,"da Vinci 5 force feedback launched 2024; reduces tissue forces; haptics long missing in MIS",High,"Single-vendor; clinical trials ongoing",idea 64
TB-027,Biomedical,1,peer-reviewed,"Vision/ML-based surgical force estimation as sensorless alternative",Med,"arXiv",idea 65
TB-028,Adv mfg,1,gov,"In-situ NDE for SLM hard; thermography for melt-pool monitoring",High,"NIST/PMC",idea 72
TB-029,Adv mfg,1,trade,"Metrology throughput bottleneck; CT hours-long; automation needed",High,"Trade magazine",idea 73
TB-030,Adv mfg,1,gov,"Ceramic AM: no standardized feedstock characterization, inadequate in-process monitoring/NDE (NIST workshop Jun 2026)",Med,"Event description",idea 74
TB-031,Adv mfg,1,peer-reviewed,"In-process ultrasound/eddy-current for DED/WAAM",Med,"Research demo",idea 75
TB-032,Adv mfg,2,industry,"Digital-thread traceability now procurement requirement in high-assurance AM",Med,"Industry analysis",idea 76
TB-033,Adv mfg,1,peer-reviewed,"Polarization-imaging + DL detects AM micro-nano damage precursors at 99% porosity accuracy",Med,"Single study; defense lab",idea 80
TB-034,Extreme,1,patent/vendor,"AlGaN/GaN downhole electronics to 250-400C, >20000 psi; SOI to >200C; SiC ICs to 600C lab",Med,"Patent + ADI technical article",ideas 81-87
TB-035,Extreme,1,trade,"High-T packaging: bare-die ceramic hybrids costly/slow; bare die availability limited",Med,"Trade + ABB",idea 82
TB-036,Sensors,1,peer-reviewed,"MEMS gas sensors: MOX poisoning causes baseline+span drift; Allan-variance benchmarking; chemical stability strategies",High,"Review article",idea 89
TB-037,Sensors,1,patent,"In-sensor span calibration for MEMS ozone/gas; NDIR methane cross-sensitivity (H2)",High,"Patent + vendor",ideas 89-97
TB-038,Sensors,1,peer-reviewed,"Integrated photonic sensors bottlenecked by packaging, fiber-chip coupling, calibration drift",Med,"2026 review (Sensors)",idea 90
TB-039,Sensors,1,peer-reviewed,"EC/MOS gas sensors drift/cross-sensitive; ML drift-correction reduces manual calibration",Med,"Systematic review 2025",ideas 91-96
TB-040,Sensors,1,peer-reviewed,"MEMS IMU zero/scale-factor long-term drift; micro-vibrator self-calibration",Med,"Research demo",idea 92
TB-041,Embedded AI,1,SAE,"ISO 26262 assumes determinism; AI introduces non-determinism; safety-shell keeps deterministic control (SAE 2026-01-0036, Apr 14 2026)",High,"SAE paper",ideas 99-105-106
TB-042,Embedded AI,1,journalism/standard,"ISO/PAS 8800, ISO/IEC TR 5469 close AI-safety gap; OOD/robustness measures needed",High,"Semiengineering + ISO refs",ideas 99-100-102
TB-043,Embedded AI,1,journalism,"ISO 8800 shifts certification toward empirical validation vs deterministic proof",High,"Trade analysis",idea 100
TB-044,Embedded AI,1,peer-reviewed,"Edge GPU inference isolation imperfect (MPS/MIG); performance isolation needed for determinism",Med,"arXiv 2026",idea 101
TB-045,Embedded AI,1,vendor,"Functional-safety island (NVIDIA IGX Thor, AMD Versal) for HW separation of safety domains",Med,"Vendor material - company claim on specs",idea 103
TB-046,Grid,1,gov/lab,"LBNL 'Queued Up: 2025 Edition' (Rand et al.): ~2,290 GW active in US interconnection queues end-2024 (1,400 GW gen + 890 GW storage, ~10,300 projects); median request-to-COD doubled from <2 yr (2000-07) to >4 yr (2018-24)",High,"Lab study",idea 22
```

### C) Synthesis: Highest-conviction bottlenecks (ranked)

1. **800VDC DC protection & arc-safe connectors (Data center / Power electronics).** Buyers: Foxconn (Kaohsiung-1, 40 MW 800VDC), CoreWeave, Oracle, and the Microsoft/Meta/Google OCP working group. Dated signal: OCP Diablo 400 spec v0.5.2 (2025-05-30); NVIDIA 800VDC full production targeted with Kyber in 2027 (roadmap). DC faults lack zero-crossing → solid-state breakers and LMFB connectors are immature. Low cleanroom, strong founder fit.
2. **GPU power-transient smoothing storage (Data center).** Buyer: Microsoft/OpenAI. Dated signal: Choukse et al., arXiv:2508.14318 (Aug 20 2025) — synchronized training oscillates in the utility-critical 0.1–20 Hz band, tens of MW per datacenter; rack-level storage and the GB200 power-smoothing feature are named mitigations.
3. **Hybrid-bonding buried-void & fine-pitch overlay metrology (Semis).** Buyers: TSMC, Intel, SK hynix. Dated signal: 5–7µm pitch early production 2026–27 (Semiengineering, PatSnap). Voids nm-deep invisible to optical.
4. **Humanoid actuator / tactile-sensing standard stack (Robotics).** Buyers: Tesla, Figure, Unitree. Dated signal: McKinsey/IDTechEx 2026 — "no engine supplier"; tactile has "no dominant design"; rare-earth magnet supply (China >90%; ~3.5 kg NdFeB/Optimus) disrupted by China's April 2025 export licensing.
5. **MV solid-state circuit breaker gate-drive subsystem (Power electronics / Grid).** Buyer: Infineon/Siemens collaboration; data centers and MVDC. Dated signal: Infineon CoolSiC JFET SSCB, PCIM 2026.
6. **BVLOS detect-and-avoid certifiable module (Drones).** Buyers: utility/infrastructure/logistics operators. Dated signal: FAA Part 108 NPRM (Aug 7 2025); comment closed Oct 6 2025 (~3,100 comments); final rule expected ~spring 2026 under the June 5 2025 EO's 240-day deadline; conspicuity comment reopened Jan 28 2026.
7. **Distribution-transformer health/aging sensing (Grid).** Buyers: utilities (GE Vernova/Prolec). Dated signal: large substation/GSU transformer lead times "ballooned to 120 to 210 weeks" (Wood Mackenzie, April 2024), imports ~80% of US supply in 2025 with a ~30% supply deficit; Citi projects shortage through 2029.
8. **GFM-aware protection relays (Grid).** Buyers: utilities/ISOs. Dated signal: IEEE 2800.2-2026 published spring 2026; P2800.1 GFM in development; Sandia gap analysis (SAND2024-04848).
9. **In-situ NDE for metal additive manufacturing (Adv mfg).** Buyers: aerospace/defense primes. Dated signal: NIST ceramic-AM metrology workshop Jun 2026; system-level qualification shift 2026–28.
10. **MEMS gas-sensor self-calibration / drift compensation (Sensors).** Buyers: industrial-safety, consumer-electronics OEMs. Dated signal: Wiley Advanced Science 2025 review; mass-market blocked by baseline/span drift from MOX poisoning.
11. **Embedded-AI functional-safety architecture (Embedded AI).** Buyers: automotive/industrial/medical OEMs. Dated signal: ISO/PAS 8800 emergence; SAE 2026-01-0036 (Apr 14 2026).
12. **Panel-level packaging warpage & sub-2µm RDL (Semis).** Buyers: TSMC (CoPoS pilot mid-2026), ASE, Amkor. Dated signal: CoPoS pilot line completion mid-2026, ramp 2028–29.
13. **Surgical-robot force-sensing instruments (Biomedical).** Buyer: Intuitive Surgical (dV5). Dated signal: FFB launched 2024; clinical trials (e.g., NCT07247175, completion 2027).
14. **Microneedle/optical CGM with extended life (Biomedical).** Buyers: Abbott, Dexcom, Senseonics. Dated signal: ongoing; current enzymatic CGMs limited to ~14-day life with biofouling.
15. **Data-center heat-reuse high-temp loop (Data center).** Buyer: Fortum (Microsoft Finland project). Dated signal: ORNL Frontier 32°C→85°C heat-pump study (2024); Fortum plants operational 2026.

**Domains richest in small-team-buildable, reduced-cleanroom, near-zero-Stanford-IP wedges:** (1) **Grid/DER/VPP** — sensing, protection, and interoperability middleware are firmware/electronics-heavy, no cleanroom; (2) **Sensors/control** — self-calibration and drift-compensation are algorithm+packaging plays; (3) **Data-center power distribution** (non-silicon: connectors, protection, storage controllers); (4) **Advanced-manufacturing quality automation** — NDE/metrology subsystems; (5) **Embedded-AI functional safety** — toolchains/runtime monitors. Domains requiring **high cleanroom burden** (avoid for a small-team beachhead): hybrid-bonding/glass-substrate processing, microfluidic in-silicon cooling, implantable electrodes, and high-temp downhole device fabrication — though their **metrology/inspection adjacencies** remain accessible.

## Recommendations

**Stage 1 (2026 — customer discovery):** Prioritize face time with named buyers attached to the top-8 bottlenecks: OCP power working-group members (Microsoft/Meta/Google), hyperscaler electrical teams (for DC protection + transient smoothing), TSMC/Intel/SK hynix packaging-yield teams (metrology), and 2–3 utilities on transformer-health and GFM-protection pain. Benchmark to change course: if ≥3 independent buyers in a domain confirm the pain is "top-3 and unsolved," advance it.

**Stage 2 (2027 — technical scouting + pick 2–3):** Build paper prototypes for the highest-fit, reduced-cleanroom wedges — DC protection/connector subsystem, MEMS sensor self-calibration, GFM-protection or transformer-health sensing, and AM in-situ NDE. Threshold: demonstrate a bench result that beats the incumbent on one quantitative axis (e.g., fault-interrupt time, drift over 6 months, void-detection limit).

**Stage 3 (2028 — R&D pilot):** Down-select to one wedge with a signed pilot/LOI from a named buyer and a clear standards tailwind (OCP Diablo 400, IEEE 2800.x, FAA Part 108, ISO 8800). Avoid wedges whose feasibility depends on unresolved export-control assumptions (SiC-substrate Section 301 tariff scheduled June 23 2027; H200/MI325X case-by-case under BIS 2026-00789) or high cleanroom capex.

**Triggers that would change the plan:** A finalized 800VDC protection standard (IEEE/NFPA) would compress the DC-protection window — move faster. Slippage of the FAA Part 108 final rule past 2026 would push drone wedges out. A reversal of the memory-driven WSTS capex surge (Spring-2026 print: 2026 = $1.51T, +89.9%) would cool packaging-metrology demand.

## Caveats

- **Tier discipline:** Several high-interest items rest partly on Tier 3 trade press or vendor material (NVIDIA TCO/efficiency figures, Microsoft "35% more accelerators," CDU capacity claims, IDTechEx market reports, NVIDIA IGX/AMD Versal safety-island specs). These are labeled company claims or weak signals and must not be treated as independent technical validation. Market-size/CAGR figures throughout are context, not customer pain.
- **Forward-looking items flagged:** NVIDIA Kyber/Rubin 2027 production, 600 kW–1 MW racks, glass-substrate 2028–29 ramp, and the FAA Part 108 final rule are roadmap/projection items, not deployed facts as of June 2026. No finalized 800VDC-specific data-center protection standard exists yet — itself a bottleneck.
- **FACT vs INFERENCE vs SPECULATION:** Bottleneck existence and technical reasons are largely FACT (sourced to Tier 1). The mapping to "possible first product" and the "prototype feasibility" ratings are INFERENCE by the author. Forward-looking timing assertions (e.g., "ramp 2028–29") are SPECULATION carried from sources and flagged. Confidence ratings reflect evidence depth, lowered where only single sources or preprints exist.
- **Scope note:** This is a technical-landscape phase only — no startup ideas, business models, or scoring were generated, per instructions. Founder-fit annotations are light per-row/synthesis notes, applied only at the end, not as search filters.
- **Corpus integration:** Existing corpus prefixes (EN/SC/AI/BM/EX/CM/US/CN) are referenced where bottlenecks map to prior evidence; new web-discovered evidence carries provisional TB- IDs (TB-001…TB-046) for later corpus reconciliation. The deliverable contains 107 numbered seeds spanning all 12 domains (roughly 8–11 per domain); deduplication during corpus reconciliation may consolidate a few closely-related sensor/grid seeds.