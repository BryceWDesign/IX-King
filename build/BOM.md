# IX-King Bill of Materials (BOM)  
Version 1.0 — July 2025  
Author: Bryce Wooster  
Purpose: Public open-source construction guide for the IX-King satellite platform

---

## 🛰️ OVERVIEW

This Bill of Materials is for the full mechanical and electronic assembly of IX-King — a modular harmonic orbital system with stealth and passive energy collection. All components listed below are real-world parts or materials with verified sourcing.

This BOM excludes launch services and assumes terrestrial assembly.

---

## 🔩 STRUCTURAL COMPONENTS

| Qty | Component                       | Material                     | Source / Notes                                      |
|-----|----------------------------------|-------------------------------|-----------------------------------------------------|
| 12  | Outer Node Spheres              | Carbon fiber shell + Al core | 10 cm spheres, CNC/fabbed in two halves            |
| 1   | Central Node Housing            | Ceramic-polycarbonate shell  | For CryoCore + logic center                         |
| 36  | Truss Rods (13 cm each)         | 6061-T6 Aluminum hex or CF   | Milled to precision, ±0.5mm tolerance               |
| 60  | Truss Mount Brackets            | Titanium (M3 thread)         | 120° and 90° multi-angle universal fasteners        |
| 40  | Fasteners                       | M3 socket titanium           | Countersunk or socket-head; Loctite 9460 optional   |
| 1   | Deployment Spring Assembly      | Stainless steel flat coil    | Triggers mechanical bloom in orbit                  |

---

## 🔌 POWER & ENERGY HARVESTING (TESLA-SCYTHE SUBSYSTEM)

| Qty | Component                       | Specification                | Notes                                               |
|-----|----------------------------------|-------------------------------|-----------------------------------------------------|
| 12  | RF Rectenna Modules             | CMOS dual-band, ~400μW ea    | Commercially available or build from scratch        |
| 6   | Thermal PCM Harvest Panels      | Graphene/paraffin sandwich   | ~1.3mW per panel @ 10°C swing                       |
| 6   | Piezoelectric Discs             | Bimorph type, tuned for <1 Hz| Mounted on stress junctions                         |
| 1   | Tesla Pulse Sync Coil           | Copper bifilar coil (9 wraps)| Hand-wound; syncs energy node timing (3-6-9 logic)  |
| 1   | Harmonic Power Router           | STM32 MCU + isolated MOSFETs | Routes harvested energy to CryoCore / buffers       |

---

## ❄️ THERMAL & CRYOCORE

| Qty | Component                       | Specification                | Notes                                               |
|-----|----------------------------------|-------------------------------|-----------------------------------------------------|
| 4   | Bi-directional Peltier Modules  | TEC1-12706 or better          | 12V, 6A standard; attach to heatsinks               |
| 1   | Heat Plate (Cold Side)          | Copper + graphene composite  | Disperses excess thermal load outward               |
| 1   | Heat Plate (Hot Side)           | Aluminum PCM block           | Transfers energy to harvesting panel                |
| 2   | High-efficiency Capacitors      | >1000μF, 50V, low ESR         | Stores recovered thermal → electric conversion      |
| 3   | PT1000 Temp Sensors             | 2-wire RTD class B           | One each on CryoCore, hot face, cold face           |

---

## 📡 COMMUNICATIONS

| Qty | Component                       | Specification                | Notes                                               |
|-----|----------------------------------|-------------------------------|-----------------------------------------------------|
| 1   | Harmonic Comms Controller       | Custom logic + crystal clock | Tesla-style 3-6-9 burst timing via PWM loop         |
| 1   | Fallback RF Module (optional)   | S-band transceiver + 5V LDO  | For emergency ping or test tracking                 |
| 1   | Directional Patch Antenna       | Tuned for S-band or X-band   | Internal or extendable from center node             |

---

## 🔋 POWER DISTRIBUTION + CONTROL

| Qty | Component                       | Specification                | Notes                                               |
|-----|----------------------------------|-------------------------------|-----------------------------------------------------|
| 1   | Central MCU                     | STM32F405 or ESP32S3         | Low power, supports PWM + ADC + watchdog            |
| 1   | FPGA (Optional for upgrade)     | Lattice ICE40 / Xilinx       | For real-time harmonic corrections (μs resolution)  |
| 12  | Low-ESR Capacitor Banks         | 470μF x12, 35V                | One per node for stabilization + routing buffer     |
| 1   | PCB Core Board                  | Custom etched or CNC router  | 4-layer FR4; 10x10cm footprint                      |

---

## 🧰 TOOLS REQUIRED (BUILD)

- Vacuum-rated Loctite 9460 adhesive (or equivalent)  
- M3 socket driver w/ torque limiter  
- Thermal paste (Arctic MX-5 or equivalent)  
- Laser cutter / CNC mill for strut ends  
- Access to cleanroom (ISO class 5–7 recommended)  
- Multi-channel oscilloscope (≥100 MHz)  
- Thermal imaging for passive IR profile checks  
- CryoCore test jig (provided in future `/tools` folder)

---

## 📦 TOTAL ESTIMATED COST

| Section             | Est. Cost (USD) |
|---------------------|------------------|
| Structure & Frame   | $2,500           |
| CryoCore Subsystem  | $3,000           |
| Energy Harvesting   | $1,000           |
| Comms & Control     | $1,500           |
| Tools & Fasteners   | ~$2,000 (non-consumable) |
| **Total**           | **~$10,000–$12,000** (excluding launch)

---

This BOM is compatible with `/build/walkthrough.md` and `/structure/metatron_geometry.md`. Do not substitute materials without recalculating structural stiffness and harmonic field propagation effects.

