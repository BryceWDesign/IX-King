# CryoCore Mounting and Configuration — IX-King Core Node  
Version 1.0 — July 2025  
Author: Bryce Wooster

---

## 🧊 Purpose

The **CryoCore** is the literal and energetic heart of IX-King. It provides:

- Solid-state thermal regulation
- Microsecond-level harmonic sync logic
- Passive IR suppression for stealth
- Energy reclamation from orbital delta-T events
- Tesla 3-6-9 frequency pulse timing

This file outlines how to mount, insulate, wire, and harmonically align the CryoCore unit within Node 0 of the IX-King Metatron chassis.

---

## 🔧 Physical Mounting

### Materials:
- Vibration-damped ceramic baseplate  
- Polycarbonate rail system (non-conductive, laser-cut slots)  
- Carbon-fiber lateral dampers (edge clamping without mechanical screw-down)  
- Thermal isolation ring (Boron Nitride sheet) between CryoCore and chassis frame

### Mounting Procedure:
1. Affix baseplate to Node 0 using four titanium M2 screws (isolated).
2. Slide CryoCore unit into rail system; do not allow metal-to-metal contact with outer chassis.
3. Insert lateral CF dampers to constrain vertical and torsional movement.
4. Apply thermal paste to interface with internal copper spreader.
5. Install thermal sensors: PT1000s to cold side, hot side, and control body.

---

## 🌀 Tesla Harmonic Sync Coil (Internal)

- Wrapped as bifilar copper coil, 9 turns total  
- Orientation must be N-S relative to Earth's magnetic pole during activation  
- Pulse sequence: 3ms / 6ms / 9ms duty-cycle harmonic propagation (refer to `/field/harmonic_sync.md`)  
- Powered by capacitor bank charged from ambient harvesters  
- Output must remain <10V peak-to-peak to maintain field coherence

---

## 🌡 Thermal Behavior Targets

| Surface         | Operational Temp Range | Note                                  |
|----------------|-------------------------|----------------------------------------|
| Cold Plate      | –40°C to +40°C          | Interfaces with internal chassis heat load |
| Hot Plate       | +60°C to +120°C         | Feeds thermal differential into recovery PCM |
| CryoCore Core   | Maintain 0–20°C         | Keeps MCU + timing logic at stable performance |

Cooling cycle is dynamic, adjusted every 0.5 seconds based on orbital sun exposure, shadow entry, and ambient thermal profile.

---

## ♻ Energy Recovery Subsystem

CryoCore includes a thermoelectric loop:
- Harvests power via differential between hot and cold plates  
- Output: ~300–600 mW per full orbital day cycle  
- Routes recovered energy back into:
  - Comms burst capacitor
  - Tesla sync pulse capacitor
  - Central MCU power buffer

---

## 📡 Sync Logic Integration

The CryoCore acts as the harmonic sync governor for IX-King:
- Coordinates pulse timing for all 12 outer nodes  
- Sets phase trigger for communications, energy routing, field alignment  
- Watchdog mode will reinitialize sync pulse if drift exceeds ±1.5ms  
- Telemetry logs sync health every 30s and stores in hardened EEPROM

---

## 🛑 Deployment Cautions

- Do not allow CryoCore to make direct conductive contact with chassis
- Never apply voltage to sync coil without grounded harmonic path
- Keep all analog sensor wires shielded and twisted; route away from digital PWM lines
- If CryoCore temp exceeds 125°C, system will auto-enter cooldown mode and pause all sync operations

---

## 🔚 Output Summary

The CryoCore is fully integrated with the following systems:
- `/power/ambient_harvest_array.md`
- `/field/harmonic_sync.md`
- `/comms/pulse_modulator.md`
- `/build/walkthrough.md`

Changes to CryoCore placement, orientation, or material composition will require retuning the harmonic logic structure of the satellite.

