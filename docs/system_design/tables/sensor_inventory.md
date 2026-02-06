# Sensor Inventory and Pin Mapping Table (Phase 1)

This table maps each sensor variable to Arduino input types (analog/digital/I²C) for Phase 1. It is **requirement-level** and focuses on planning total inputs per plant.

| Plant | Sensor Type      | Quantity | Connection Type | Conceptual Pin(s) | Notes / Phase 1 Learning Objective |
|-------|-----------------|----------|----------------|-----------------|----------------------------------|
| P1    | Temperature     | 1        | Analog / I²C   | A0 / I2C        | Learn analog reading or I²C addressing |
| P1    | Humidity        | 1        | I²C            | SDA/SCL          | Learn I²C bus sharing and unique addresses |
| P1    | Light Intensity | 1        | Analog          | A1              | Understand analog light measurement |
| P1    | Soil Moisture   | 1        | Analog          | A2              | Practice soil sensor calibration |
| P1    | Watering Event  | 1        | Digital Input   | D2              | Learn event logging (manual or sensor) |
| P2    | Temperature     | 1        | Analog / I²C   | A3 / I2C        | As above |
| P2    | Humidity        | 1        | I²C            | SDA/SCL          | Shared bus, unique address |
| P2    | Light Intensity | 1        | Analog          | A4              | As above |
| P2    | Soil Moisture   | 1        | Analog          | A5              | As above |
| P2    | Watering Event  | 1        | Digital Input   | D3              | As above |
| P3    | Temperature     | 1        | Analog / I²C   | A0 / I2C        | Shared analog pins for planning |
| P3    | Humidity        | 1        | I²C            | SDA/SCL          | As above |
| P3    | Light Intensity | 1        | Analog          | A1              | As above |
| P3    | Soil Moisture   | 1        | Analog          | A2              | As above |
| P3    | Watering Event  | 1        | Digital Input   | D4              | As above |
| P4    | Temperature     | 1        | Analog / I²C   | A3 / I2C        | As above |
| P4    | Humidity        | 1        | I²C            | SDA/SCL          | As above |
| P4    | Light Intensity | 1        | Analog          | A4              | As above |
| P4    | Soil Moisture   | 1        | Analog          | A5              | As above |
| P4    | Watering Event  | 1        | Digital Input   | D5              | As above |
| P5    | Temperature     | 1        | Analog / I²C   | A0 / I2C        | As above |
| P5    | Humidity        | 1        | I²C            | SDA/SCL          | As above |
| P5    | Light Intensity | 1        | Analog          | A1              | As above |
| P5    | Soil Moisture   | 1        | Analog          | A2              | As above |
| P5    | Watering Event  | 1        | Digital Input   | D6              | As above |

---

## **Phase 1 Notes**

1. **Analog Pins**: Arduino Uno has 6 analog inputs (A0–A5). For 5 plants, some analog pins are conceptually shared in this planning table; Phase 2 will finalize actual pin assignments or use a larger board if needed.  
2. **I²C Bus**: Temperature and humidity sensors that support I²C can share the same SDA/SCL lines; each sensor must have a unique address.  
3. **Digital Inputs**: Watering events are mapped to digital pins (D2–D6) for Phase 1 planning.  
4. **Learning Objectives**: This table is designed to help you learn:  
   - Analog vs digital readings  
   - I²C bus sharing and addressing  
   - Per-plant sensor mapping  
   - How to plan for microcontroller limitations before hardware selection  

---

