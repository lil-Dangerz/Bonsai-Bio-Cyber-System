# Phase 1 — Open Questions & Uncertainties
Bonsai Bio-Cyber System

This document captures **known unknowns** identified during Phase 1 planning.
These items are intentionally unresolved and will inform Phase 2 decisions.

---

## 1. Hardware & Board Selection

- Should Phase 2 continue with **Arduino Uno**, or migrate to:
  - Arduino Mega (more analog inputs)
  - Multiple microcontrollers
  - Hybrid setup (microcontroller + higher-level system)
- How many total analog inputs are required if all sensors are per-plant?
- Is I²C address space sufficient for all planned sensors?

**Reason deferred:** Phase 1 governance prohibits final hardware decisions.

---

## 2. Sensor Model Selection

- Which specific sensor models best balance:
  - Accuracy
  - Stability
  - DIY availability
- Are capacitive soil moisture sensors preferable to resistive ones?
- Do temperature + humidity combo sensors reduce complexity or introduce coupling risk?

**Reason deferred:** Requires hardware testing and budget considerations.

---

## 3. Pin Pressure & Expansion

- Will analog pin sharing be sufficient long-term?
- Is an analog multiplexer required?
- Should sensor density be reduced by grouping plants into micro-environments?

**Reason deferred:** Depends on observed Phase 1 data variability.

---

## 4. Logging Frequency & Data Volume

- Is daily sampling sufficient to capture meaningful trends?
- Would higher-frequency sampling reveal useful dynamics?
- What is the tradeoff between resolution and data manageability?

**Reason deferred:** Requires baseline data to evaluate.

---

## 5. Biological Variability

- How much variability exists between plants under similar conditions?
- Are environmental differences or biological differences dominant?
- Does per-plant sensing justify its complexity?

**Reason deferred:** Requires Phase 1 observations.

---

## 6. Data Interpretation Boundaries

- At what point does observation become implicit control?
- How should thresholds be defined without triggering automation?
- How to distinguish curiosity-driven exploration from optimization?

**Reason deferred:** Governance-driven; requires explicit Phase 2 framing.

---

## 7. Phase Transition Criteria

- What constitutes “sufficient” Phase 1 data?
- How many days or weeks of logging are required?
- What signals readiness for Phase 2 automation planning?

**Reason deferred:** Must be decided after initial growth observations.

---

## Notes

- This document is **append-only** during Phase 1.
- Items may be clarified but not resolved.
- Resolutions belong explicitly to Phase 2.

---

## References

- Canonical Governance Rules: `docs/governance/canonical_governance.md`
- Phase 1 Logging Plan: `docs/data_logging/phase1_logging_plan.md`
- Subsystems: `docs/system_design/subsystems.md`
