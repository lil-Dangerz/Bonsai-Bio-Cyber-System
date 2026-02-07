# System Design — Subsystems (Phase 1)

This document defines the **Phase 1 subsystems** of the Bonsai Bio-Cyber System.
Each subsystem includes its **purpose**, **Phase 1 scope**, **requirement-level components**, and **explicit learning objectives**.

All content adheres to **Canonical Governance Rules**:
- Observation and learning only
- No optimization
- No final hardware decisions
- Requirement-level planning only

---

## 1. Environment Subsystem

**Purpose:**  
Represent the physical and biological conditions affecting bonsai growth that are observable and measurable.

**Phase 1 Scope:**
- Temperature (ambient air)
- Humidity (ambient)
- Light intensity
- Soil moisture
- Watering events (manual observation)

**Components (Conceptual):**
- Physical growing environment
- Pots, soil, ambient air, light source
- Human interaction (watering, inspection)

**Learning Objectives:**
- Understand which environmental variables influence early bonsai growth
- Learn to translate biological conditions into measurable signals
- Develop intuition for environmental variability across multiple plants

**Phase 1 Limitations:**
- No environmental control or optimization
- No automated intervention
- Observation only

---

## 2. Plant / Biological Subsystem

**Purpose:**  
Provide the living biological system being observed and measured.

**Phase 1 Scope:**
- Germination and early growth of 5 bonsai plants
- Manual care (watering, positioning)
- Visual and qualitative observations

**Components (Requirement-Level):**
- Bonsai seeds (species TBD)
- Individual pots and soil medium
- Manual observation notes

**Learning Objectives:**
- Learn species-specific germination characteristics
- Understand early plant response to environmental conditions
- Practice structured biological observation and documentation

**Phase 1 Limitations:**
- No pruning, shaping, or growth manipulation
- No experimental stress induction
- Baseline growth only

---

## 3. Sensor Subsystem

**Purpose:**  
Convert environmental variables into measurable electrical signals.

**Phase 1 Scope:**
- Temperature sensors (analog or I²C)
- Humidity sensors (I²C)
- Light sensors (analog)
- Soil moisture sensors (analog)
- Watering event inputs (digital/manual)

**Components (Requirement-Level):**
- Arduino-compatible sensors
- Analog, digital, and I²C interfaces
- One sensor per plant per variable (except shared buses)

**Learning Objectives:**
- Understand analog vs digital vs I²C sensors
- Learn sensor placement and calibration principles
- Practice multi-sensor system planning
- Learn limitations imposed by sensor quantity and interfaces

**Phase 1 Limitations:**
- No sensor model selection finalization
- No performance optimization
- No redundancy or fault tolerance design

---

## 4. Communication / Bus Subsystem

**Purpose:**  
Define how sensor data is transmitted to the microcontroller.

**Phase 1 Scope:**
- Analog input mapping
- Digital input mapping
- I²C bus sharing and addressing
- Conceptual pin allocation planning

**Components (Requirement-Level):**
- Analog input channels
- Digital input channels
- I²C bus (SDA/SCL)
- Sensor-to-pin mapping table
- Conceptual wiring diagram (Mermaid)

**Learning Objectives:**
- Understand microcontroller I/O constraints
- Learn I²C bus sharing concepts
- Practice planning under pin-count limitations
- Understand why architectural planning precedes hardware selection

**Phase 1 Limitations:**
- Pin assignments are conceptual
- Wiring diagrams are non-binding
- Final board selection deferred to Phase 2

---

## 5. Microcontroller Subsystem

**Purpose:**  
Central node for data acquisition and coordination.

**Phase 1 Scope:**
- Read sensor inputs
- Perform minimal signal handling
- Forward data to logging subsystem

**Components (Requirement-Level):**
- Arduino or compatible microcontroller
- GPIO, analog inputs, I²C interface

**Learning Objectives:**
- Understand microcontroller role in cyber-physical systems
- Learn sensor polling concepts
- Learn how subsystems integrate logically

**Phase 1 Limitations:**
- No control logic
- No actuation
- No optimization or scheduling complexity

---

## 6. Data Logging Subsystem

**Purpose:**  
Persist observational data for analysis and learning.

**Phase 1 Scope:**
- Log sensor readings per plant
- Log watering events
- Use local, human-readable storage

**Components (Requirement-Level):**
- CSV or Markdown files
- Timestamping
- Plant and sensor identifiers
- Directory-based organization

**Learning Objectives:**
- Learn structured data collection
- Understand traceability and reproducibility
- Practice separating raw data from interpretation

**Phase 1 Limitations:**
- No cloud storage
- No automated data pipelines
- No analytics or visualization requirements

---

## 7. Power Subsystem

**Purpose:**  
Provide safe and sufficient power to sensors and microcontroller.

**Phase 1 Scope:**
- Powering sensors and microcontroller only
- Stable, low-risk operation

**Components (Requirement-Level):**
- Low-voltage power source (USB, adapter, or battery)
- Wiring and connectors

**Learning Objectives:**
- Understand basic power requirements
- Learn why power planning matters even in small systems
- Practice documenting power assumptions without committing to solutions

**Phase 1 Limitations:**
- No power optimization
- No battery management systems
- No monitoring or redundancy

---

## 8. Subsystem Integration Notes

- Subsystems are **modular and loosely coupled**
- No subsystem may control another in Phase 1
- All interactions are **observational and unidirectional**
- Diagrams and tables define conceptual relationships only

**Primary Phase 1 Learning Objective:**
Develop a complete mental model of a bio-cyber system **before** introducing automation, optimization, or control.

---

## References

- Canonical Governance Rules: `docs/governance/canonical_governance.md`
- Sensor Tables & Diagrams: `docs/system_design/diagrams/sensor_mapping_and_diagrams.md`
- Phase 1 Roadmap: `docs/roadmap/phased_plan.md`
