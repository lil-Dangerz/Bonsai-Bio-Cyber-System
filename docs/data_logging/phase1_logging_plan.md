# Phase 1 Observation & Logging Plan
Bonsai Bio-Cyber System

This document defines **what is logged, how often, where it is stored, and how it is structured** during Phase 1.

It adheres strictly to **Canonical Governance Rules**:
- Observation only
- No optimization or control
- Manual + sensor data allowed
- Human-readable, local storage

---

## 1. Purpose

The goal of Phase 1 logging is to:
- Establish **baseline environmental and biological data**
- Practice **structured observation**
- Ensure **traceability and reproducibility**
- Support learning, not automation

No data is used for control or optimization in Phase 1.

---

## 2. What Is Logged

### 2.1 Environmental Variables (Per Plant)

Each plant logs the following variables:

| Variable        | Source        | Type        | Notes |
|-----------------|---------------|-------------|------|
| Temperature     | Sensor        | Numeric     | Ambient air near plant |
| Humidity        | Sensor        | Numeric     | Ambient |
| Light Intensity | Sensor        | Numeric     | Relative or lux-based |
| Soil Moisture   | Sensor        | Numeric     | Raw or normalized |
| Watering Event  | Manual / Input| Event       | Timestamp only |

---

### 2.2 Biological Observations (Per Plant)

Logged manually:

| Observation | Type | Notes |
|------------|------|------|
| Germination status | Boolean / Text | Not sprouted / sprouted |
| Visual notes | Text | Leaf color, posture |
| Anomalies | Text | Mold, dryness, damage |

---

## 3. Logging Frequency

### 3.1 Sensor Readings

| Variable | Frequency | Rationale |
|--------|-----------|-----------|
| Temperature | 1× daily | Baseline trends |
| Humidity | 1× daily | Environment awareness |
| Light | 1× daily | Relative exposure |
| Soil Moisture | 1× daily | Water availability |
| Watering Event | On occurrence | Event-based |

> Frequency may increase later, but Phase 1 prioritizes **consistency over resolution**.

---

### 3.2 Biological Observations

| Observation | Frequency |
|------------|-----------|
| Germination | Daily |
| Visual notes | Daily |
| Anomalies | As observed |

---

## 4. Data Storage Format

### 4.1 Directory Structure

```text
data/
├── sensors/
│   ├── plant_01.csv
│   ├── plant_02.csv
│   └── ...
├── observations/
│   ├── plant_01.md
│   ├── plant_02.md
│   └── ...
└── README.md
