# IX-King Build Walkthrough  
Version 1.0 — July 2025  
Author: Bryce Wooster  
Alignment: Real-world fabrication, no fiction, Space Force–restricted build

---

## 🔧 PREPARATION

### Workspace Requirements:
- ISO Class 7 (or better) cleanroom  
- ESD-safe benches with grounding straps  
- Vibration-free surface for CryoCore alignment  
- Gimbal rig or 3-axis balance jig (DIY permitted with precise calibration)  
- RF-isolated test environment recommended for comms diagnostics  

### Tools Checklist:
- CNC mill or precision laser cutter  
- Soldering station with hot air reflow capability  
- M3 torque-limited driver (set to 0.9 Nm)  
- Cryogenic-safe thermal paste applicator  
- Thermal camera / IR signature scanner  
- Oscilloscope (100+ MHz, 4 channels)  
- Multimeter, LCR meter, and bench PSU (0–24V, 5A+)

---

## 🧱 STEP 1 — CHASSIS FRAME CONSTRUCTION

1. **Lay out all truss rods and node spheres.**  
   - Ensure aluminum rods are free from burrs.  
   - CF rods must be dry-polished to eliminate edge fray.

2. **Assemble central cube using titanium M3 brackets.**  
   - Begin with central node (#0) and attach 6 rods at equidistant face angles.  
   - Use torque driver to lock in brackets at each truss end.

3. **Attach outer nodes (1–6) to create orbital midplane.**  
   - Mount harmonically even around Node 0.  
   - Confirm frame balance on jig after midplane is complete.

4. **Complete outer tetrahedral nodes (7–12).**  
   - Connect rods forming 3D resonance extensions.  
   - Ensure full symmetry; check edge length tolerance ±0.5mm.

---

## ❄️ STEP 2 — CRYOCORE MOUNTING

1. **Mount CryoCore module inside Node 0.**  
   - Use vibration-damped ceramic bed with insulated rails.  
   - Ensure full mechanical isolation from conductive chassis.

2. **Apply thermal paste to both heat plates (cold + hot side).**  
   - Mount Peltier modules using adhesive-backed compression clips.  
   - Attach copper heat spreader and PCM-aluminum block to hot side.

3. **Install PT1000 sensors.**  
   - One each on cold plate, CryoCore frame, and external heat shroud.  
   - Wire to MCU analog input (shielded leads).

4. **Secure CryoCore pulse sync bifilar coil (Tesla logic).**  
   - Coil wraps must be oriented to north-south magnetic alignment during final test.

---

## 🔌 STEP 3 — POWER + HARVESTING INTEGRATION

1. **Install 12 rectenna modules (1 per node).**  
   - Place in outer nodes 1–6 and 7–12.  
   - Tune spacing from frame walls to reduce EM interference.

2. **Mount 6 thermal PCM harvest panels on node interiors.**  
   - Prefer opposing sides to maximize delta exposure per orbit cycle.

3. **Mount 6 piezoelectric discs on truss brackets.**  
   - Target rod junctions most likely to oscillate under thermal and solar strain.

4. **Route all harvesting nodes into harmonic power router.**  
   - Use STM32 MCU or equivalent with MOSFET isolation per channel.  
   - Buffer output to capacitor banks (onboard or radial node storage).

---

## 📡 STEP 4 — COMMS SYSTEM INSTALLATION

1. **Install harmonic comms pulse board in Node 0.**  
   - Ensure crystal oscillator is thermally isolated.  
   - Align pulse vector to line-of-sight with one outer node for beam bounce.

2. **(Optional)** Install fallback S-band module.  
   - Power isolated via switch logic from central MCU.  
   - Patch antenna tuned and mounted on side face, with choke ring for field confinement.

---

## 🛰️ STEP 5 — FINAL BALANCING + VERIFICATION

1. **Mount all remaining capacitor banks and telemetry lines.**  
   - Keep signal lines twisted-pair and EMI shielded.

2. **Place full system on 3-axis balance jig.**  
   - Acceptable deviation: ±0.3g on X, Y, Z from centerpoint.

3. **Conduct passive RF profile scan.**  
   - Ensure no persistent leak from fallback RF module when inactive.

4. **Run CryoCore operational test.**  
   - Validate target delta-T:  
     - Cold side: <40°C  
     - Hot side: >70°C under simulated solar load  
   - Run thermal loop: recover ≥500mW via thermoelectric recovery.

---

## 🚀 STEP 6 — ORBITAL DEPLOYMENT

1. **Stow system in folded frame mode (16"x16"x16").**  
2. **Lock all rods with magnetic or mechanical latches.**  
3. **Load into rideshare deployer (ESP32 trigger recommended).**  
4. **On orbital release, EM-spring triggers expansion.**  
5. **Tesla coil pulse sync fires; satellite harmonizes in under 2.5 seconds.**  
6. **System enters passive field orbit. No propulsion required.**

---

## 🔐 END

This walkthrough assumes use of `/build/BOM.md`, `/structure/metatron_geometry.md`, and `/core/cryocore_mount.md`. Do not deviate from harmonic geometry without recalculating all timing and field sync variables.

