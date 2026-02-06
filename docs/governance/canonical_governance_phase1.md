
# Canonical Governance Rules — Phase 1
Bonsai Bio-Cyber System Project

These rules define the scope, constraints, learning objectives, and documentation requirements for Phase 1 of the project.

---

## 1. Scope Governance
- **Observation Only:** Phase 1 is strictly focused on **monitoring and logging** environmental variables.
- **DIY-Friendly:** Only use **Arduino-compatible sensors and boards** that can be safely handled at home.
- **No Optimization:** Do not attempt to optimize watering, lighting, or data processing yet.
- **Phase-Limited Decisions:** Hardware purchases or algorithm selection for automation are **deferred to Phase 2**.

## 2. Learning Objectives Governance
- Every task must have **explicit learning objectives**, e.g.:
  - Reading analog sensors (Temperature, Light, Soil Moisture)
  - Using I²C bus for multiple sensors
  - Understanding microcontroller pin allocation
  - Data logging and traceability
  - Conceptual system integration (block diagrams, plant mapping)

## 3. Subsystem Governance
- **Subsystem boundaries must be respected:**
  1. **Environment Subsystem:** Temperature, Humidity, Light, Soil Moisture, Watering Events
  2. **Sensor Subsystem:** Analog or I²C sensors connected to the microcontroller
  3. **Microcontroller Subsystem:** Handles data acquisition and logging only
  4. **Data Logging Subsystem:** Local storage in CSV/Markdown format, strictly read/write
- **No subsystem crossing:** Phase 1 tasks should **not mix subsystems for optimization or actuation**.

## 4. Documentation Governance
- **All observations must be logged** in a clear, traceable format (Markdown + tables + diagrams).
- **Mermaid diagrams** are required for:
  - System block flow
  - Plant layout and sensor placement
  - Sensor-to-pin mapping / wiring
- **Tables and diagrams must match:** Any sensor or pin mentioned in a table **must be represented in diagrams**.
- **Notes on uncertainties** must be explicitly documented (open questions, unknown sensor addresses, analog pin sharing, etc.).

## 5. Phase 1 Safety Governance
- **No hazardous experiments** (no high voltages, chemicals, or automation that could harm plants or humans).
- Use sensors and electronics **within rated voltage/current**.
- Manual watering and plant care remain **human-controlled**.

## 6. Traceability Governance
- Every decision, observation, or test must have:
  - **Date / Timestamp**
  - **Responsible actor** (for Phase 1, typically the project owner or collaborator)
  - **Purpose / Learning objective**

## 7. Review & Iteration Governance
- Phase 1 is **iterative**:
  - Diagrams, tables, and logs can be updated as sensors or plants are added.
  - Any change must be **documented** with reason and date.
- No Phase 2 decisions (hardware upgrades, automation, optimization) are allowed in Phase 1 documentation.

---

**Implementation Notes:**
- Save this file in `docs/governance/canonical_governance.md`.
- Reference these rules in all Phase 1 documentation to enforce consistent learning-focused design.
- Add a section for **Phase 1 Notes / Open Questions** to track uncertainties.
