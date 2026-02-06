# System Design — Subsystems

This document outlines the Bonsai Bio-Cyber System subsystems as defined for Phase 1. Each subsystem includes its purpose, components (requirement-level), and learning objectives. All designs adhere to Phase 1 governance rules: observation and learning only, no optimization, no final hardware decisions.

---

## 1. Sensor Subsystem

**Purpose:** Capture environmental variables critical to bonsai seed growth and early development.

**Phase 1 Scope:**
- Temperature (air and optional soil/root)
- Humidity
- Light intensity
- Soil moisture
- Watering events (manual or sensor-based)
- Optional: CO₂ or air quality sensors

**Components (Requirement-Level):**
- Arduino-compatible sensors
- Analog or digital interface per variable
- One sensor per plant per variable (except optional shared variables)

**Learning Objectives:**
- Understand which environmental variables affect bonsai growth
- Learn about sensor types, analog vs digital/I²C connections
- Practice sensor placement and calibration for accurate readings
- Learn to document sensor data consistently

**Notes / Phase 1 Limitations:**
- Total number of sensors per plant must be planned to fit board capabilities
- No hardware purchase decisions made yet; focus on requirements and quantity

---

## 2. Data Logging Subsystem

**Purpose:** Collect and store environmental measurements and observations for analysis and Phase 1 learning.

**Phase 1 Scope:**
- Simple logging of sensor readings per plant
- Manual logging of watering events (optional automatic logging)
- Storage in CSV or Markdown files

**Components (Requirement-Level):**
- Arduino or microcontroller (requirements-level planning only)
- Local storage (SD card, USB, or PC connection)
- File naming conventions to separate plant data and variable type

**Learning Objectives:**
- Learn methods for structured data collection
- Understand data organization for reproducibility
- Explore options for sensor-to-file mapping without committing to hardware

**Notes / Phase 1 Limitations:**
- Continuous logging is optional; focus is on capturing meaningful, periodic data
- No automation of data upload or cloud storage in Phase 1

---

## 3. Power Subsystem

**Purpose:** Provide stable power for sensors and microcontroller during Phase 1 monitoring.

**Phase 1 Scope:**
- Power supply sufficient for sensors and logging microcontroller
- No advanced power management or optimization required

**Components (Requirement-Level):**
- Placeholder for Arduino-compatible power source (battery, adapter)
- Wires and connectors for sensor power

**Learning Objectives:**
- Understand basic power requirements for simple DIY sensor systems
- Learn the concept of safe power supply for multiple small electronics
- Practice documenting requirements before hardware selection

**Notes / Phase 1 Limitations:**
- No final selection of power solution; focus on estimating capacity needed
- No automation of power monitoring

---

## 4. Communication / Bus Subsystem

**Purpose:** Connect sensors to the microcontroller and organize input/output for data collection.

**Phase 1 Scope:**
- Map sensor variables to microcontroller inputs (analog/digital/I²C)
- Identify shared bus options (I²C) for multiple sensors
- Track total pin and input requirements

**Components (Requirement-Level):**
- Arduino Uno or equivalent microcontroller (requirements-level only)
- Sensor-to-pin mapping table
- Conceptual wiring diagram (for reference)

**Learning Objectives:**
- Understand digital and analog I/O requirements
- Learn bus-sharing concepts (I²C) and address limitations
- Practice planning sensor layout without making final hardware decisions

**Notes / Phase 1 Limitations:**
- Focus on requirement-level planning for 5 plants
- Wiring diagrams are conceptual; actual connections will be verified in Phase 2

---

## 5. Plant / Biological Subsystem

**Purpose:** Provide the living system that the sensors monitor — bonsai seeds and early seedlings.

**Phase 1 Scope:**
- Plant 5 bonsai seeds in separate containers
- Monitor growth and environmental conditions
- Record watering and other observable variables

**Components (Requirement-Level):**
- Bonsai seeds (species TBD)
- Pots and soil medium
- Manual logging tools for growth observations

**Learning Objectives:**
- Learn species-specific germination requirements
- Understand the impact of environmental variables on early growth
- Practice structured observation and documentation

**Notes / Phase 1 Limitations:**
- No interventions beyond basic care
- Focus on establishing baseline observations for later phases

---

## Notes

- All subsystems should be cross-referenced with **sensor inventory tables**, **phase 1 roadmap**, and **canonical governance rules**.
- Emphasis is on **observation, learning, and documentation**, not on optimization, automation, or hardware finalization.
