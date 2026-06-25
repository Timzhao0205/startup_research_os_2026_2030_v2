# Customer-Pain & Niche-Wedge Scan (Phase 13): Buyer-Pull Landscape for a 2029/2030 Deep-Tech Launch

## TL;DR
- The strongest **budgeted, named-buyer, severe-pain** clusters are: (1) AI data-center power/protection (800VDC transition; Vertiv, Eaton, NVIDIA, Foxconn, CoreWeave, Oracle) where the architecture is being standardized RIGHT NOW via OCP and components ship 2026–2027; (2) advanced-packaging yield/metrology (TSMC, SK hynix, Samsung, Micron, Intel) where hybrid-bonding overlay/void defects gate HBM4+ economics; and (3) humanoid-robot actuation/force-sensing (Tesla, Figure, Unitree) where actuators are 56% of BOM (Morgan Stanley) and there is "no equivalent of an engine supplier."
- **China-first adoption is most feasible** in semiconductor-equipment localization (metrology/inspection still import-dependent at 23.2% localization in 2025, Yole), battery-manufacturing inline inspection, data-center liquid cooling, and high-end medical devices where Beijing's Document 551 mandates 100% domestic content for 137 device categories — creating a forced-substitution pain where domestic performance lags. **US validation** comes later via national labs (NRL/NIST sole-source), fusion (DOE milestone OT), and aerospace/defense AM qualification.
- **Long sales cycles that REQUIRE starting discovery in 2026**: utilities/ISOs (interconnection median request-to-COD now >4 years / ~55 months; IBR/grid-forming protection), fusion (DOE milestone phases run to ~2029), national-lab sole-source (FAR 6.302), and FDA-regulated surgical/clinical hardware. These will not convert by 2029/2030 unless seeded now.

## Key Findings

1. **Power delivery has displaced cooling as the binding data-center constraint, and the buyers are actively writing specs.** NVIDIA's Vera Rubin platform (2027) targets up to 600 kW/rack and is driving an industry-wide shift from 415/480 VAC and 54 VDC busbars to 800 VDC. OCP published its v1.0 Data Center Facilities Power Distribution whitepaper at end of Q1 2026 with 190+ contributing companies. Vertiv expects to ship 800 VDC in 2026 ahead of Rubin Ultra in 2027, and is "still finalizing centralized rectifiers, high-efficiency DC busways, and rack-level DC-DC converters." Per NVIDIA's Oct. 13, 2025 OCP Global Summit announcement, "20-plus industry partners" are aligning: "Foxconn provided details on its 40-megawatt Taiwan data center, Kaohsiung-1, being built for 800 VDC. CoreWeave, Lambda, Nebius, Oracle Cloud Infrastructure and Together AI are among other industry pioneers designing for 800-volt data centers." This is a rare moment where the pain is acute, the buyers are named, and the open spec is unfinished — meaning gaps (DC protection/breakers, solid-state transformers, connectorization) are explicit.

2. **Hybrid-bonding metrology/yield is a "3D blind spot" gating HBM and chiplet economics.** Industry sources confirm that for die-to-wafer hybrid bonding "getting yields to be acceptable is extremely difficult and expensive for a 2 layer" — and HBM4 has POSTPONED hybrid bonding, sticking with microbumps, precisely because of yield/cost. Even 1 µm particles cause defects; overlay accuracy at 200 nm pad pitch requires "better equipment." Intel (per DARPA NGMM materials) states "improvements in post bond accuracy measurement metrology are needed." Named buyers: TSMC, SK hynix, Samsung, Micron, Intel; tool incumbents Onto Innovation, Applied Materials, Lam, BESI.

3. **Humanoid actuation is the canonical "no engine supplier" niche.** Per Morgan Stanley's Tesla Optimus analysis, "actuators account for 56% of the robot's total bill-of-materials cost," and hands alone are ~17% (~$9,500 of a $50,000–60,000 unit); building Optimus Gen-2 without Chinese suppliers would push BOM from ~$46K to ~$131K. High-reduction actuators (Tesla, Figure) require dedicated strain-gauge torque sensors because gearbox friction makes current-sensing unreliable. Harmonic/strain-wave gearboxes are concentrated among Harmonic Drive, Nabtesco, and Leaderdrive; planetary roller screws have a "narrow supplier base." Tactile/force sensing for dexterous hands is a stated bottleneck.

4. **Surgical force feedback just got validated as a real, paid feature — opening adjacent niches.** Intuitive's da Vinci 5 (FDA-cleared, March 2024) is the first system with integrated force feedback; a one-year analysis published in Journal of Robotic Surgery (2025, DOI 10.1007/s11701-025-02781-9; US data Mar 29 2024–Apr 30 2025) found "Data from 444 procedures by 73 unique surgeons were analyzed," and Intuitive reports preclinical trials showed "up to 43 percent less force exerted on tissue." This confirms willingness-to-pay for haptics/force-sensing in surgical robotics, while most other platforms still lack it — a niche pain for force-sensing instrument tips and competing platforms.

5. **CGM accuracy plateau is real but the segment risks being "diagnostic/monitoring overproduction"** the founder was told to avoid. Dexcom G7 MARD ~8.2% (arm); the literature documents MARD's limitations and Abbott's ~3M-sensor recall for inaccurate low readings. Flagged as lower-priority per founder-fit guidance.

6. **China is a forced-substitution buyer across multiple deep-tech categories.** China equipment localization rose from 8% (2021) to 23.2% (2025), projected 39% by 2030, per Yole Group's "Mainland China Semiconductor Equipment Industry 2026" (chief analyst John West: "A new generation of Chinese equipment suppliers is rapidly gaining ground, transforming the competitive landscape") — but metrology, inspection, lithography, ion implant remain weak/import-dependent; RF power (~20% domestic), precision valves (VAT <10%), quartz parts (30–40%), precision ceramics (~20–30%) remain import-bound. In medical devices, MOF/MIIT Document 551 (May 2021) sets domestic-content targets of 25–100% across 178 medical-device categories, with 100% for 137 categories (per the EU Commission Staff Working Document and US trade.gov) — while domestic firms cannot yet supply ultra-high-field MRI, photon-counting CT, ECMO, or high-end clinical mass spec, producing a "glass door" pain. A July 6, 2025 MOF notice further excludes EU-origin devices on government projects above RMB 45 million (e.g., photon-counting CT "still primarily imported from Germany").

7. **Grid/utility pain is severe but slow.** ~2,290 GW active in US interconnection queues (end-2024); median request-to-COD has doubled from <2 years (2000–2007) to over 4 years for 2018–2024 projects, with the typical 2024 project spending ~55 months in queue (LBNL "Queued Up: 2025 Edition," Rand et al.); only 13% of 2000–2019 requests reached operation. Grid-forming inverters break legacy protection relays (negative-sequence/directional elements misoperate). LDES (Form Energy iron-air, 100h; Google/Xcel 300MW/30GWh) has DOE Storage Shot (90% cost cut by 2030) but utilities "don't know who would use a 100h battery" — a procurement-readiness pain.

8. **Government/lab procurement provides credible US-validation anchors with sole-source paths.** Per the CFS/DOE announcement (Sept. 30, 2025), "CFS received $8 million from the DOE's Milestone-Based Fusion Development Program, the largest amount paid to any company in the program"; CFS states the "$8 million...is about half of the $15 million we're eligible to receive" in the first of the program's three phases ($46M appropriated, first budget period). NRL issued a FAR 6.302 sole-source Notice of Intent to Laser Thermal Analysis for an SSTR/FDTR thermal-characterization system (N00173-25-RFI-MF18, Jul 28 2025) — **award value/date remain UNCONFIRMED** in USAspending/FPDS/SAM as of this scan.

## Details

### A) Customer Pain-Point Table

Legend — Procurement difficulty / China-first / US-expansion rated High/Med/Low. Confidence reflects evidence strength and FACT/INFERENCE/SPECULATION basis.

| Customer segment | Buyer title | User title | Pain point | Current workaround | Why current solution fails | Budget/WTP signal | Procurement difficulty | China-first | US expansion | Related wedge | Source IDs | Tier mix | Confidence |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Hyperscale/neocloud data centers (US) | VP Data Center Engineering | Facility electrician / power engineer | No mature DC-side protection/breakers for 800VDC at 600kW–1MW racks | Retrofitting AC gear; sidecar power racks; staged phases | AC protection doesn't transfer; HVDC arc-fault/breaker ecosystem immature | Vertiv shipping 800VDC 2026; OCP v1.0 spec; NVIDIA Rubin 600kW/rack 2027 | High | Med | High | MC01 800VDC/DC protection; CP-001/002/003 | T1(OCP/NVIDIA dev)+T3 | High (FACT) |
| Power-equipment OEMs (Vertiv, Eaton, Schneider, ABB) | Director of Product Engineering | Power systems engineer | Need rack-level DC-DC, centralized rectifiers, solid-state transformers not yet finalized | In-house dev; partnerships (ST, TI) | Components still in design; no open standard until 2026 | Vertiv "design maturity"; Eaton functional sidecar at OCP 2025 | Med | Med | High | MC01; SST | CP-002/003/004 | T2/T3 + company-claim | High (FACT) |
| AI server integrators (Foxconn, CoreWeave, Oracle, Lambda) | Head of Infrastructure | Data center ops tech | Thermal + power co-design at >100kW/rack; integration risk | Direct-to-chip liquid cooling; vendor bundles | Siloed designs slow deployment; "fungibility" gap | Foxconn 40MW Kaohsiung-1 for 800VDC; 20+ NVIDIA partners | Med | Med | High | MC04 liquid cooling; MC01 | CP-001/003/005 | T1/T3 | High (FACT) |
| Memory makers (SK hynix, Samsung, Micron) | Director of Packaging Yield | Process/metrology engineer | Hybrid-bond overlay misalignment, micro-voids, particle defects gate HBM yield | Stick with microbumps (HBM4); offline acoustic/optical inspection | 3D "blind spot"; 1µm particle = defect; D2W yields hard even at 2 layers | HBM4 postponement = capex deferral; BESI bonding ~40%/74% concentration | High | Med | Med | MC02 hybrid-bond metrology; TB | CP-006/007/008 | T1(ASME/arXiv/DARPA)+T3 | High (FACT) |
| Logic foundries (TSMC, Intel) | Director of Advanced Packaging | Bonding process engineer | Post-bond accuracy metrology insufficient for pitch scaling; warpage distortion | EMIB/CoWoS; inline interferometry | Bonding accuracy now dominant factor; warpage causes local distortion | TSMC SoIC 6µm; CoWoS capacity-constrained (context) | High | Low | Med | MC02; MC03 chiplet thermal | CP-007/008 | T1(DARPA/Intel) | High (FACT) |
| Semiconductor equipment OEMs (US: AMAT, Lam; supplier MKS) | VP Supply Chain | Subsystem integration engineer | Customer concentration + need for higher-precision subsystems | Internal dev; MKS subsystems | Top-ten = 32% of MKS FY24 net rev; AMAT+Lam ~27% (2021) | MKS 10-K: top-ten 32% (2024), none >10% | Med | Low | High | MC02 metrology; SC | CM-MKS; CP-009 | T1(SEC) | High (FACT) |
| Humanoid robot OEMs (Tesla, Figure, Apptronik) | VP Hardware Engineering | Actuator/mechatronics engineer | No merchant high-torque-density actuator; strain-gauge torque sensing unreliable/expensive | Full custom actuator dev in-house | "No engine supplier"; gearbox friction defeats current-sensing | Actuators 56% BOM (Morgan Stanley); planetary roller screw $1,350–2,700×14 | Med | Med | High | MC07 embodied-AI actuation | CP-010/011/012 | T2/T3 | High (FACT) |
| Humanoid robot OEMs (Unitree, UBTech, Fourier) | Chief Engineer | Joint-module designer | Dexterous-hand tactile sensing + harmonic-reducer supply bottleneck | QDD current-sensing; imported Harmonic Drive/Nabtesco | Hands ~17% BOM; gearbox supply precision-bound, hard to scale | Unitree $610M Shanghai IPO (Mar 2026, ~$7B target) | Low | High | Med | MC07 tactile/actuation | CP-010/012/013 | T2/T3 | Med (FACT/INF) |
| Surgical robotics (Intuitive competitors; new entrants) | Chief Medical Officer / VP R&D | Surgeon | Lack of force/haptic feedback at instrument tip on most platforms | Visual-force surrogate; surgeon training | Direct haptics "negligible" historically; novice surgeons over-apply force | da Vinci 5 force feedback FDA-cleared 2024; "up to 43% less force"; 444-procedure study | High | Low | Med | MC09 non-radiology FDA-PCCP HW; force sensing | CP-014/015 | T1(JRS/PMC/IEEE) | High (FACT) |
| CGM makers (Dexcom, Abbott, Senseonics) | VP R&D | Endocrinologist / patient | Accuracy plateau (~8% MARD); recalls on low-glucose readings | Factory calibration; Kalman/Bayesian compensation | MARD masks per-sensor error; interstitial lag | Abbott recall ~3M sensors (context) | Med | Med | Med | (founder-fit: deprioritize) | CP-016/017 | T1(PMC/IEEE) | Med (FACT) |
| China semiconductor fabs (SMIC, Hua Hong, CXMT, YMTC) | VP Equipment Procurement | Fab process/metrology engineer | Domestic metrology/inspection/litho/implant tools lag; yield risk adopting them | Stockpiled/imported tools; FDPR-exposed | Localization only 23.2% (2025); metrology weak; entity-list cutoffs | Big Fund III ¥71B+¥93B (Jan 2025); mandatory domestic-use policy | Med | High | Low | MC02 metrology; SC | CP-018/019/020 | T2/T3 | High (FACT) |
| China advanced-packaging firms (JCET, etc.) | Director of Packaging | Back-end process engineer | Back-end tool localization window; HBM/advanced-package metrology | ACM (clean), Huahai Qingke (CMP), AMEC (TSV etch) | Advanced packaging higher barrier than legacy; metrology gaps | 2025–2030 penetration window (Yole/industry) | Med | High | Low | MC02; MC03 | CP-019/020 | T2/T3 | Med (INF) |
| China battery/EV makers (CATL, BYD, gigafactories) | VP Manufacturing | Electrode/coating process engineer | Need 100% inline electrode defect detection to cut scrap | XRF, laser triangulation, camera, EIS at formation | Scrap 2–5% (~6% of cell cost); blind spots remain | Scrap reduction payback <18mo; Tesla-LG $4.3B deal (context) | Low | High | Med | LDES BOS-adjacent; EX inspection | CP-021/022/023 | T2/T3 | Med (FACT/INF) |
| China data-center operators (Sugon, Inspur + hyperscalers) | Head of Data Center Infra | Cooling/facility engineer | Liquid-cooling interoperability; mismatched standards across vendors | Direct-to-chip, immersion (Submer/Inspur 100kW+) | "Manufacturers' design standards vary widely" (Sugon CTO) | Submer-Inspur 2-phase deal (Jan 2026); >100kW/rack | Med | High | Med | MC04 liquid cooling | CP-024/025 | T3 | Med (FACT) |
| China grid/industrial-energy customers | Provincial grid planning lead | Substation protection engineer | IBR-dominated protection misoperation; SST for renewables | DCB/POTT schemes; Y-transformers for zero-seq | GFM current-limiting breaks negative-seq relays | State-directed renewables buildout (context) | High | Med | Low | MC01 GFM-protection/SST | CP-026/027 | T1(arXiv/IEEE)+T2 | Med (FACT/INF) |
| China hospitals / medtech distributors | Hospital procurement director | Radiologist / clinical-lab director | Mandated domestic devices underperform for high-field MRI, photon-counting CT, ECMO, clinical MS | Import where still allowed (>¥45M projects) | Domestic firms lack core tech; "glass door" in bids | Document 551: 100% domestic for 137 categories; July 2025 MOF EU-device exclusion >¥45M | High | High | Low | BM high-end imaging/MS | CP-028/029/030/031 | T1(EU SWD/trade.gov/MOF)+T2 | High (FACT) |
| China robotics/drone & low-altitude (EHang, AutoFlight) | VP Engineering | eVTOL powertrain engineer | High C-rate aviation batteries, propulsion, redundancy subsystems | Adapt automotive cells; imported components | eVTOL needs 2–3C discharge, ~4× auto energy/100km | EHang VT35 ~$913K; AOCs issued Mar 2025 | Med | High | Med | EX low-altitude subsystems | CP-032/033/034 | T2/T3 | Med (FACT/INF) |
| US national labs (NRL, NIST, Sandia, ORNL) | Contracting Officer | Research physicist / branch engineer | Need turnkey high-precision thermal/material characterization for WBG/UWBG | Sole-source to niche vendor (Laser Thermal) | Commercial tools don't measure thin-film κ in-line | NRL FAR 6.302 NOI N00173-25-RFI-MF18 (award UNCONFIRMED); NIST CHIPS buy | High | Low | High | MC03 chiplet thermal metrology | CP-035/036 | T1(SAM.gov) | Med (FACT; award unresolved) |
| Fusion developers (CFS, Tokamak Energy, Thea, Type One) | VP Engineering / Program Director | Magnet/HTS engineer | HTS magnet manufacturing, cryo, diagnostics, fuel-cycle subsystems | DOE milestone cost-share; ORNL partnerships | First-of-kind components; de-risking via milestones | DOE Milestone $46M Phase 1; CFS $8M TF magnet (max, of $15M eligible) | High | Low | High | EX extreme-energy subsystems | CP-037/038 | T1(DOE/CFS) | High (FACT) |
| US utilities / ISOs / RTOs | VP Transmission Planning | Interconnection/protection engineer | Interconnection studies bottleneck; IBR protection; transformer health | FERC Order 2023 reforms; manual study | Median IR-to-COD ~55 months; 77% withdrawal; relays misoperate | ~2,290 GW queue (LBNL); Order 2023 in implementation | High | Low | Med | MC01 transformer-health/GFM | CP-039/040 | T1(LBNL/IEEE) | High (FACT) |
| US LDES / extreme-energy customers | Director of Resource Planning | Storage integration engineer | No bankable >10h storage BOS; uncertain dispatch/value | Li-ion 4h; iron-air pilots (Form) | Capex-heavy; "don't know who'd use 100h battery" | DOE Storage Shot 90% by 2030; Google/Xcel 300MW/30GWh | High | Low | Med | MC05 LDES balance-of-system | CP-041/042 | T1(DOE/PNNL)+T3 | Med (FACT) |
| Aerospace/defense primes (AM parts) | Quality/Certification Director | NDE/metallurgy engineer | AM part qualification: XCT degrades on complex geometry; destructive testing costly | Witness coupons; XCT; mechanical testing | Geometry/roughness defeat NDE; process drift | SAE 38+50 standards; defense AM "mirage" cracks reported | High | Low | High | EX additive-manufacturing NDE | CP-043/044 | T1(NASA/ScienceDirect)+T3 | Med (FACT) |
| Space/defense power (SiC) | Program Manager | Power-electronics engineer | Rad-hard/high-temp SiC for PMAD; single-event burnout at high V | Rad-hard Si; up-screened COTS | SiC SEB at high operating V; qualification gaps | WBG triples voltage, -50% losses, -20% mass (NASA-cited) | High | Med | High | MC06 SiC rad-hard/high-temp | CP-045/046 | T1(NASA/arXiv) | Med (FACT/INF) |
| US clinical labs / hospitals | Lab Director / CMO | Pathologist / lab tech | High-end analytical instrument precision & throughput | Imported high-end MS; manual workflows | (Triangulation thin — see Caveats) | Henry Schein supplier ~33% (context) | Med | Med | Med | BM clinical instrumentation | CP-031 | T2/T3 | Low (INF) |

(Wedge codes MC01–MC09 map to Phase-11 clusters as supplied; TB/SC/EX/BM map to corpus prefix families.)

### B) CSV-Ready Evidence Ledger (NEW sources)

```
source_id,domain,tier,source_type,claim_supported,confidence,limitations,use_in_ideas
CP-001,opencompute.org,1,standards body whitepaper,800VDC target architecture + OCP v1.0 power distribution spec Q1 2026 with 190+ contributors,High,directional doc not final component spec,Yes
CP-002,datacenterdynamics.com,3,trade journalism,OCP working group moving power conversion external; 800VDC up to 1500VDC future,Med,journalism not primary,Triangulation
CP-003,hpcwire.com,3,trade journalism,Vertiv ships 800VDC 2026 finalizing rectifiers/busways/DC-DC; Foxconn 40MW Kaohsiung-1; CoreWeave/Oracle adopting,High,vendor statements embedded (company claim),Yes
CP-004,developer.nvidia.com,3,vendor technical blog,NVIDIA 800VDC ecosystem; Kyber 600kW/rack; Rubin 2027,Med,company claim,Triangulation
CP-005,delloro.com,2,industry analyst,OCP 2025 supplier announcements (Eaton functional sidecar; ABB DC breakers),Med,analyst,Triangulation
CP-006,semiengineering.com,3,trade journalism,HBM4 sticks with microbumps; hybrid-bonding postponed on yield/cost,High,journalism,Yes
CP-007,darpa.mil,1,government presentation,Intel: post-bond accuracy metrology improvements needed; warpage distortion,High,presentation slides,Yes
CP-008,asmedigitalcollection.asme.org,1,peer-reviewed,Hybrid-bond yield depends on overlay accuracy; 90-95% yields; 200nm pitch needs better equipment,High,academic,Yes
CP-009,sec.gov/mks.com,1,SEC 10-K,MKS top-ten customers 32% FY2024 net rev none >10%; AMAT+Lam ~27% (2021),High,issuer filing,Yes
CP-010,kraneshares.com,3,financial commentary,Actuators 40-56% BOM; "no engine supplier"; Optimus non-China BOM $46K->$131K (Morgan Stanley),High,secondary citing MS,Yes
CP-011,firgelli.com,3,vendor technical guide,High-reduction actuators need strain-gauge torque sensors; current-sensing unreliable,Med,vendor,Triangulation
CP-012,optimusk.blog,4,enthusiast blog,Optimus actuator/sensor breakdown; actuators 56% BOM (Morgan Stanley); planetary roller screw cost,Low,weak signal only,No
CP-013,eu.36kr.com,3,trade journalism,Dexterous hands + harmonic reducers core cost-reduction bottleneck,Med,translated,Triangulation
CP-014,link.springer.com,1,peer-reviewed,da Vinci 5 force feedback 1-yr analysis 444 procedures/73 surgeons (J Robotic Surg 2025 DOI 10.1007/s11701-025-02781-9); up to 43% less tissue force,High,single-vendor data,Yes
CP-015,embs.org,2,IEEE professional,da Vinci 5 first FDA-cleared integrated force feedback (Mar 2024),High,review,Yes
CP-016,ncbi.nlm.nih.gov,1,peer-reviewed,Dexcom G7 MARD 8.2% arm/9.1% abdomen,High,clinical study,Yes
CP-017,spectrum.ieee.org,2,technical journalism,Abbott recall ~3M sensors for inaccurate low readings,Med,journalism,Triangulation
CP-018,anysilicon.com,2,industry analyst (Yole),China equip localization 8%(2021)->23.2%(2025)->39%(2030) per Yole; metrology/litho weak,High,analyst,Yes
CP-019,faxiangongchang.com,2,research firm,RF power ~20% VAT valves <10% quartz 30-40% ceramics 20-30% import-dependent; metrology adoption yield risk,Med,research firm,Yes
CP-020,yolegroup.com,2,industry analyst,YMTC/SMIC domestic-WFE pilot lines; advanced node capacity bottleneck,High,analyst,Yes
CP-021,qualitymag.com,3,trade journalism,Battery multi-modal inspection (CT/UT/X-ray) imperative; Tesla-LG $4.3B,Med,journalism,Triangulation
CP-022,ncbi.nlm.nih.gov,1,peer-reviewed,LIB electrode scrap ~2% = ~6% of battery cost; need inline QC,High,academic,Yes
CP-023,cntepower.com,4,vendor,Dry-electrode metrology; scrap 3-5%->0.5%,Low,vendor claim,No
CP-024,mordorintelligence.com,3,market research,China DC cooling: vendor standard mismatch; Chemours/Navin localization,Med,market research,Triangulation
CP-025,interestingengineering.com,3,journalism,Sugon CTO: liquid-cool design standards vary widely integration hard,Med,journalism,Yes
CP-026,arxiv.org,1,preprint,GFM inverters break negative-sequence/directional protection elements,High,preprint,Yes
CP-027,pacw.org,2,industry technical,IBR protection challenges; zero-seq/POTT/differential mitigations,High,professional,Yes
CP-028,eur-lex.europa.eu,1,government (EU SWD),Document 551: 178 medical-device categories 25-100% domestic; 100% for 137,High,EU investigation primary,Yes
CP-029,trade.gov,1,US government,Document 551 (MOF/MIIT May 2021) local-content for hundreds of items incl medical,High,govt,Yes
CP-030,hoganlovells.com,2,law firm analysis,July 2025 MOF notice excludes EU devices on projects >RMB45M; photon-counting CT ~RMB45M still imported,High,cites MOF primary,Yes
CP-031,dovepress.com,1,peer-reviewed,ECMO 6/7 suppliers foreign; "glass door" for domestic high-end devices in bids,Med,journal,Yes
CP-032,sciencedirect.com,1,peer-reviewed,eVTOL technical bottlenecks: propulsion/battery/safety,Med,review,Triangulation
CP-033,businessaviation.aero,3,trade journalism,EHang VT35 ~$913K; AOCs Mar 2025; eVTOL 2-3C discharge 4x auto energy,Med,journalism,Triangulation
CP-034,gov.cn,1,government,Low-altitude economy national strategic priority; drone PV inspection >95% accuracy,Med,govt promo,Triangulation
CP-035,sam.gov,1,procurement record,NRL FAR 6.302 sole-source NOI to Laser Thermal N00173-25-RFI-MF18 (Jul 28 2025); award unconfirmed,High,NOI not award,Yes
CP-036,laserthermal.com,4,vendor,SSTR/FDTR FASTR system; NIST collaboration,Low,company claim,No
CP-037,energy.gov,1,government,DOE Milestone fusion $46M Phase 1; public-private OT structure,High,govt,Yes
CP-038,cfs.energy,2,company (corroborated),CFS $8M TF-magnet milestone (largest); eligible $15M,High,company + DOE validated,Yes
CP-039,emp.lbl.gov,1,national lab,~2290 GW active queue end-2024; median IR-to-COD ~55 months; 13% built/77% withdrawn,High,national lab,Yes
CP-040,resourcecenter.ieee-pes.org,1,IEEE technical report,IBR low-fault-current breaks traditional line protection,High,standards body,Yes
CP-041,energy.gov,1,government,DOE Storage Shot: 90% LDES cost cut by 2030; 10+hr,High,govt,Yes
CP-042,cen.acs.org,2,society journalism,Form iron-air 100h; "utilities don't know who'd use 100h battery",Med,journalism,Yes
CP-043,ntrs.nasa.gov,1,government,AM NDE qualification challenges aerospace,High,govt,Yes
CP-044,sciencedirect.com,1,peer-reviewed,XCT degrades on complex AM geometry; destructive coupon testing costly,High,academic,Yes
CP-045,nasa.gov,1,government,SiC operates >500-650C; WBG triples voltage -50% losses -20% mass,High,govt,Yes
CP-046,arxiv.org,1,preprint,SiC MOSFET single-event burnout at high voltage; rad-hard gaps,High,preprint,Yes
```

### C) Synthesis

**(i) Top 12 highest-WTP, best-access pain points (ranked):**

1. **800VDC DC-side protection & rack-level conversion** — Buyer: VP DC Engineering / Product Eng at Vertiv, Eaton, Schneider, NVIDIA. Signal: Vertiv shipping 2026; OCP v1.0 spec Q1 2026; Rubin 600kW/rack 2027; Foxconn 40MW Kaohsiung-1. Sales cycle: 12–24 months (spec windows open NOW).
2. **Hybrid-bonding overlay/void metrology** — Buyer: Director of Packaging Yield at SK hynix, Micron, TSMC, Intel. Signal: HBM4 postponement; BESI bonding concentration ~40/74%. Cycle: 18–36 months (tool qualification).
3. **Humanoid actuator + tactile/force sensing** — Buyer: VP Hardware at Tesla, Figure, Apptronik, Unitree. Signal: actuators 56% BOM (Morgan Stanley); Unitree $610M IPO. Cycle: 6–18 months (fast-moving).
4. **China high-end medical devices under domestic mandate** — Buyer: Hospital procurement director / distributor. Signal: Document 551 (100% for 137 categories); >¥45M imaging still imported. Cycle: 12–24 months but policy-forced.
5. **China semiconductor metrology/inspection localization** — Buyer: VP Equipment Procurement at SMIC/CXMT/YMTC. Signal: Big Fund III ¥164B; localization mandate; metrology weak (23.2% localization, Yole). Cycle: 12–30 months.
6. **DOE-backed fusion subsystems (HTS magnets, fuel cycle)** — Buyer: VP Engineering at CFS/Tokamak/Type One. Signal: DOE Milestone $46M; CFS $8M (of $15M eligible). Cycle: 24–48 months (milestone phases to ~2029).
7. **Surgical force-sensing instruments** — Buyer: CMO/VP R&D at Intuitive competitors. Signal: da Vinci 5 validates WTP ("up to 43% less tissue force"). Cycle: 24–60 months (FDA).
8. **Grid-forming inverter protection** — Buyer: VP Transmission Planning at utilities/ISOs. Signal: 2,290 GW queue; Order 2023. Cycle: 36–60 months.
9. **NRL/NIST sole-source thermal/material characterization** — Buyer: Contracting Officer. Signal: FAR 6.302 NOI (award unresolved). Cycle: 6–18 months once scoped.
10. **China battery inline defect inspection** — Buyer: VP Manufacturing at CATL/BYD. Signal: scrap ~6% of cost. Cycle: 6–18 months.
11. **Aerospace/defense AM NDE/qualification** — Buyer: Quality/Certification Director at primes. Signal: SAE standards expanding; defense AM cracking. Cycle: 24–48 months.
12. **SiC rad-hard/high-temp power for space/defense** — Buyer: Program Manager. Signal: WBG mass/loss savings. Cycle: 24–48 months.

**(ii) China-first-adoptable vs US-validation:**
- **China-first:** semiconductor metrology/inspection localization; battery inline inspection; data-center liquid-cooling interoperability; high-end medical devices (forced substitution); low-altitude/eVTOL subsystems; humanoid components (Unitree/UBTech). Driver: explicit localization mandates + speed + state capital.
- **US-validation (later, premium/compliance/exportable credibility):** national-lab sole-source (NRL/NIST); DOE fusion milestone; aerospace/defense AM qualification; surgical force-sensing (FDA); utility GFM protection (NERC). Driver: rigorous independent validation that confers exportable credibility.

**(iii) Long sales cycles REQUIRING discovery to start in 2026:**
- **Utilities/ISOs** (36–60 mo): interconnection + protection; must seed pilots with ISOs now to land by 2029/2030.
- **Fusion** (24–48 mo): DOE milestone phases run to ~2029; subsystem qualification must begin in 2026.
- **FDA-regulated surgical/clinical hardware** (24–60 mo): clearance pathways demand early predicate/clinical planning.
- **National-lab sole-source** (variable but relationship-driven): FAR 6.302 requires incumbency/uniqueness established early.
- **Aerospace/defense AM** (24–48 mo): qualification/standards bodies move slowly.

**(iv) "Too small or weird for incumbents, but real" niche pains:**
- Post-bond overlay metrology specifically tuned for D2W known-good-die at relaxed pad density (incumbents chase W2W).
- Strain-gauge/torque force-sensing modules for high-reduction humanoid actuators (merchant "engine-supplier" gap).
- HVDC arc-fault/solid-state breaker for 800VDC racks (between industrial ABB gear and chip-level — an orphan integration layer).
- Inline thin-film thermal-conductivity metrology for WBG/UWBG (NRL/NIST sole-source scale — too niche for big metrology OEMs).
- Force-sensing instrument tips for non-Intuitive surgical platforms.
- 100h-class LDES balance-of-system + dispatch/value modeling (incumbents wait for the market; the BOS is unglamorous).

## Recommendations

**Stage 1 (now–Q4 2026) — seed the long-cycle, high-credibility accounts in parallel with fast China loops.**
- Open customer-discovery conversations immediately with: (a) OCP Power/Open Data Center for AI working-group members (Vertiv, Eaton, Schneider, NVIDIA ecosystem) on **800VDC DC protection/conversion gaps**; (b) packaging-yield orgs at SK hynix/Micron/Intel on **hybrid-bond metrology**; (c) at least one ISO/RTO interconnection team and one utility protection group on **GFM protection**. Benchmark to change course: if ≥3 named buyers in a cluster will sign a paid pilot/LOI within 9 months, advance; if not, deprioritize.
- In China, run fast discovery with battery (CATL/BYD) inline-inspection and semiconductor metrology-localization buyers, plus medtech distributors navigating Document 551. Benchmark: a China-first design partner with budget within 6 months.

**Stage 2 (2027) — convert discovery into R&D pilots aligned to the buyers writing specs.**
- Prioritize the cluster where you have (i) a named buyer, (ii) a primary-source budget signal, and (iii) a spec window. As of this scan that is **800VDC protection/conversion** and **hybrid-bond metrology**. Trigger to escalate: design-win or paid eval from a Tier-1 named account.
- Pursue one US-credibility anchor (NRL/NIST sole-source OR DOE fusion milestone subcontract) to build exportable validation. Trigger: a FAR 6.302 NOI naming you, or a milestone-program prime partnership.

**Stage 3 (2028) — lock 2029/2030 launch beachhead.**
- Choose a beachhead with the shortest remaining cycle and clearest budget: humanoid actuation/force-sensing (fast) or China forced-substitution (policy-driven) for early revenue; layer US validation for premium expansion.

**Thresholds that change the plan:**
- If export-control regime tightens further (BIS escalations to components), China-first compute-adjacent plays get riskier — pivot toward non-compute China pains (battery, medtech, low-altitude) and US validation.
- If OCP finalizes 800VDC protection in its next whitepaper version with an incumbent solution, the DC-protection wedge narrows — re-scope to connectorization/arc-fault niche.
- If a merchant humanoid-actuator "engine supplier" emerges at scale, the actuator wedge closes — pivot to tactile/force-sensing only.

## Caveats
- **Market-size figures are context, never pain.** Data-center TWh, humanoid TAM, LDES/CGM/eVTOL market projections cited herein are explicitly NOT treated as pain signals per scan rules.
- **Company claims flagged:** Vertiv/Eaton/Flex/ST/NVIDIA product statements, vendor metrology spec pages (Onto, Laser Thermal, cntepower), and enthusiast blogs (optimusk) are labeled company-claim/weak-signal and do NOT count as independent evidence. The Morgan Stanley "56% of BOM" and "$46K→$131K" actuator figures are secondary (relayed via financial commentary), not the primary MS note.
- **Unresolved primary fact:** The NRL Laser Thermal Analysis sole-source (N00173-25-RFI-MF18) **award value and date remain unconfirmed** in USAspending/FPDS/SAM as of this scan; only the Notice of Intent is verified. Recommend a direct FPDS-NG query by PIID (likely beginning N00173-25-).
- **Thin evidence noted:** US clinical-lab/hospital high-end-instrument pain is under-sourced here (search budget exhausted before dedicated US-hospital queries); rated Low confidence and flagged for follow-up. China hospital pain, by contrast, is well-sourced via EU SWD/trade.gov/MOF.
- **Bloom Energy customer-concentration** shifted materially: a single related-party customer accounted for ~55% of Q3-2025 revenue (10-Q), higher than the prior ~43% anchor — confirming rising concentration but updating the figure.
- **Tier discipline:** Several China-market and humanoid datapoints rest on Tier 2/3 analyst/journalism sources; treated as triangulation, not primary evidence, and confidence lowered accordingly. Fact/Inference/Speculation labels are applied per row.
- **Export-control volatility** (BIS FR 2026-00789; AI OVERWATCH Act; Section 301 SiC-substrate tariff June 2027) makes any compute-adjacent China assumption provisional.