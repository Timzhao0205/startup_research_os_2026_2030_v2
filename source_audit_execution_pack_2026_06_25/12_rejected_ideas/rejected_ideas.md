# Rejected Ideas

Use this file to preserve negative learning. Do not delete rejected ideas; record why they were rejected so they are not regenerated repeatedly.

_Last updated: 2026-06-25, after prompt 02e (targeted re-score of audit-affected ideas), packaged by 02e/02g. Authoritative current decisions for audit-affected ideas come from `06_scored_idea_database/scored_idea_database_repaired_2026_06_25.csv`. Kills not touched by the source audit are carried from `final/01_score_filtered_ideas.md` and were not re-audited._

**Current kill count: 13** — Section A (audit-adjudicated): 8; Section B (carried from original scoring): 5. Ideas on HOLD are listed separately at the bottom and are NOT rejected.

## Template

```text
## [Idea ID] — [Idea Name]

Date rejected:
Reason:
Primary risk:
Evidence source IDs:
What would need to change to reconsider:
Notes:
```

---

## Section A — Audit-adjudicated kills (authoritative, 2026-06-25)

These eight ideas carry decision = KILL in the repaired scored database after the 07b–07e source audit and 02e re-score.

### RID-036 — Chiplet thermal characterization

Date rejected: 2026-06-25 (original scoring; kill confirmed/locked in 02e)
Reason: NRL award not verifiable (NOI N00173-25-RFI-MF18 + DARPA prime only; TRIG-005 speculative/medium). Per addendum, kill stands unless executed contract appears in USAspending/FPDS/SAM.gov.
Primary risk: Wedge depends on a single incumbent (Laser Thermal Analysis) already holding sole-source position; diagnostic instrument; first-customer evidence weak.
Evidence source IDs: SCORE-014; tracked under ISSUE-013
What would need to change to reconsider: An executed Navy/other contract for the SSTR/FDTR instrument visible in USAspending/FPDS/SAM.gov (PIID N00173-series, UEI E14VYCEW9YG8). Absence is treated as inconclusive pending DoD ingest lag (TRIG-005).
Notes: score 62/100; evidence status KILL; decision K.

### RID-071 — Drone airspace-management ADSP

Date rejected: 2026-06-25 (original scoring; kill hardened from HOLD in 02e)
Reason: Software/services + Part 146/108 gated; permanent kill reason independent of trigger. Status aligned HOLD->KILL (decision already K).
Primary risk: Software/services play gated by FAA Part 146/108; permanent reason independent of the (speculative) Part 108 trigger.
Evidence source IDs: SCORE-012; tracked under ISSUE-010
What would need to change to reconsider: Nothing audit-driven — this is a structural software/services + regulatory-gating kill. (Status hardened HOLD->KILL in 02e; decision was already K.)
Notes: score 52/100; evidence status KILL; decision K.

### RID-041 — Advanced-packaging metrology platform

Date rejected: 2026-06-25 (original scoring; kill confirmed/locked in 02e)
Reason: Diagnostic + cleanroom + giants; HBM4 microbump continuation strengthens only the diagnostic role (penalized on standalone value). Kill stands.
Primary risk: Diagnostic/metrology-only (rubric standalone-value penalty), cleanroom-heavy, and incumbents (Onto/AMAT/KLA) own the socket.
Evidence source IDs: SCORE-002;SCORE-016; tracked under ISSUE-009
What would need to change to reconsider: A purchased-capability spec or procurement that demands it as a standalone tool rather than an in-line monitoring add-on.
Notes: score 51/100; evidence status KILL; decision K.

### RID-094 — AM in-situ NDE

Date rejected: 2026-06-25 (original scoring; kill confirmed/locked in 02e)
Reason: Diagnostic/NDE-overproduction; prior kill; no standalone procurement/standards driver. HOLD stands.
Primary risk: Diagnostic / in-situ-NDE monitoring-overproduction; AM qualification-gated; incumbents (Sigma Labs/GE) in-house.
Evidence source IDs: NIST AM-Bench (07c re-test, ISSUE-014-094); tracked under ISSUE-014-094
What would need to change to reconsider: A procurement or standard that demands AM in-situ NDE as a *purchased standalone capability*. Evidence status is HOLD (revivable on that driver), decision K.
Notes: score 50/100; evidence status HOLD; decision K.

### RID-045 — Panel-level packaging handler

Date rejected: 2026-06-25 (original scoring; kill confirmed/locked in 02e)
Reason: Cleanroom + capex; no audit finding revives. Kill stands.
Primary risk: Cleanroom + >$2M capex subsystem against entrenched OEMs (ASMPT/Shinkawa); no first-customer wedge.
Evidence source IDs: SCORE-016; tracked under ISSUE-009
What would need to change to reconsider: A specific panel-level-packaging line need with an addressable, non-cleanroom entry point. No audit finding revives it.
Notes: score 49/100; evidence status KILL; decision K.

### RID-042 — Die-to-wafer hybrid bonder

Date rejected: 2026-06-25 (original scoring; kill confirmed/locked in 02e)
Reason: Kill LOCKED on Tier-1 JEDEC JESD270-4 (775um, 16-Hi keeps microbumps) replacing Tier-4 36Kr; hybrid bonding postponed >2029 (TRIG-007: no near-term pull). Per addendum kill discipline.
Primary risk: Demand-timing + cleanroom capex: HBM4 stays on microbumps, so the die-to-wafer hybrid-bonding pull moves past the 2029 window.
Evidence source IDs: SCORE-002; + JEDEC JESD270-4 (07b); tracked under ISSUE-009
What would need to change to reconsider: JEDEC/HBM5 (or a Samsung/SK 16-Hi yield ramp) re-mandating hybrid bonding inside the build window. Watch JEDEC + Semiconductor Engineering (TRIG-007).
Notes: score 47/100; evidence status KILL; decision K.

### RID-087 — Point-of-care molecular cartridge

Date rejected: 2026-06-25 (original scoring; kill confirmed/locked in 02e)
Reason: Customer pain remains policy-context-only (Doc 551 localization; no direct workflow-pain/buyer source); also diagnostic. PW-1; stays blocked.
Primary risk: Customer pain is policy-context-only (China Document 551 localization) with no independent buyer/workflow-pain source; also diagnostic; NMPA-gated, crowded (Cepheid/Mammoth).
Evidence source IDs: SCORE-004D; tracked under ISSUE-015
What would need to change to reconsider: A direct, independent workflow-pain or buyer source (not policy context). Evidence status NEEDS_MORE_SOURCE.
Notes: score 46/100; evidence status NEEDS_MORE_SOURCE; decision K.

### RID-091 — China-localized imaging detector

Date rejected: 2026-06-25 (original scoring; kill confirmed/locked in 02e)
Reason: Customer pain policy-context-only (Doc 551); cleanroom-high + China-only + export-incoherent. PW-1; stays blocked.
Primary risk: Customer pain policy-context-only (Doc 551, 100% localization target); cleanroom-high, China-only, export-incoherent.
Evidence source IDs: SCORE-004D; tracked under ISSUE-015
What would need to change to reconsider: An independent buyer/workflow-pain source plus a coherent export posture. Evidence status NEEDS_MORE_SOURCE.
Notes: score 45/100; evidence status NEEDS_MORE_SOURCE; decision K.

---

## Section B — Kills carried from original scoring (not re-audited)

These ideas were killed in `final/01_score_filtered_ideas.md` and fall outside the 49 audit-affected ideas, so 02e did not re-score them. Rationale is preserved from the original scoring.

### RID-023 — Transformer health monitor

Date rejected: 2026-06-25 (original 01 scoring)
Reason: Diagnostic tool, not standalone; incumbents GE/Doble/Qualitrol.
Primary risk: Rubric standalone-value penalty; monitoring add-on rather than a bought capability.
Evidence source IDs: SCORE-005
What would need to change to reconsider: A standalone procurement/standard that demands it as purchased equipment.
Notes: score 51/100; decision K; not re-audited in 07b–07e.

### RID-093 — Battery electrode coating inspection

Date rejected: 2026-06-25 (original 01 scoring)
Reason: Diagnostic tool; CATL/BYD do this in-house.
Primary risk: Captive in-house demand at the only large buyers; diagnostic-overproduction.
Evidence source IDs: SCORE-019
What would need to change to reconsider: An independent merchant-market buyer outside the captive cell makers.
Notes: score 50/100; decision K; not re-audited in 07b–07e.

### RID-123 — Embedded AI watchdog for medical AI

Date rejected: 2026-06-25 (original 01 scoring)
Reason: Software-only; FDA-gated; regulatory-toolchain competition (Mona et al.).
Primary risk: Software-only with no hardware moat; FDA gating; thin defensibility.
Evidence source IDs: SCORE-009
What would need to change to reconsider: A hardware/standards anchor or a regulatory mandate creating a procured-capability need.
Notes: score 52/100; decision K; not re-audited in 07b–07e.

### RID-047 — Precision RF power generator (China-localized)

Date rejected: 2026-06-25 (original 01 scoring)
Reason: Export-control incoherence; cleanroom-adjacent; incumbents MKS/AE.
Primary risk: China-localization thesis is export-control-incoherent for a US-expandable venture.
Evidence source IDs: SCORE-006;SCORE-017
What would need to change to reconsider: A material liberalization of the US-China equipment/export regime (watch BIS Federal Register).
Notes: score 44/100; decision K; not re-audited in 07b–07e.

### RID-037 — Thermal interface material (>50 W/mK)

Date rejected: 2026-06-25 (original 01 scoring)
Reason: Materials-qualification-gated, commoditized; supporting evidence was vendor-marketing (company claim), evidence=low.
Primary risk: Commoditized materials play with weak, non-independent (vendor) evidence and long qual cycles.
Evidence source IDs: SCORE-021
What would need to change to reconsider: Independent (non-vendor) performance validation plus a defensible, non-commoditized application wedge.
Notes: score 43/100; decision K; not re-audited in 07b–07e.

---

## On HOLD — NOT rejected (do not regenerate as new; do not treat as killed)

These carry decision = WATCH with evidence status HOLD. They are parked pending a specific unlock, not rejected:

- **RID-077 — Surgical force-feedback system**: standalone-displacement clinical-outcome claim unsupported by preclinical/Intuitive-funded evidence (surrogate endpoints only). Revisit at/after the 02f gate.
- **RID-099 — Extreme-precision metrology instrument**: trips the diagnostic/metrology-overproduction hard filter; no standalone procurement/standards driver. Revisit at/after the 02f gate.
- **Drone / air-mobility cluster (RID-067, RID-068, RID-069, RID-070, RID-072, RID-074, RID-112)**: all on HOLD under the speculative FAA Part 108 BVLOS trigger (TRIG-001); revisit only on a FINAL Part 108 Federal Register rule.

_RID-094 appears in Section A because its decision is KILL, but its evidence status is HOLD — it is the one kill that revives on a procurement/standard demanding AM in-situ NDE as a purchased capability._
