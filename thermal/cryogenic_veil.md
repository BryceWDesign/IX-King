# Cryogenic Veil System — IX-King Satellite  
Version 1.0 — July 2025  
Author: Bryce Wooster

---

## 🎯 Purpose

Space isn’t cold — **space is hot** when you're in direct sunlight, and **thermal extremes** are the enemy of component longevity and field sync.

The Cryogenic Veil is a **passive + active hybrid cooling and shielding system** that keeps IX-King’s core subsystems under operational temperature, even during:

- Full solar arc exposure  
- Blackbody side re-radiation  
- Extended polar orbit periods  

---

## 🧊 Core Components

| Subsystem              | Function                                      |
|------------------------|-----------------------------------------------|
| Radiant Shadow Panels  | Reflect 96%+ of incoming thermal radiation     |
| CryoCore Heat Loops    | Draw excess thermal energy via phase-change fluid |
| Graphene Radiator Spines| Emit thermal energy via deep-space radiation  |
| Multilayer Insulation (MLI) | Minimize heat flux internally                |

---

## 🧠 Working Principle

1. **Solar Impact Block**  
   - Radiant Shadow Panels are angled using frame-locked geometry (see `/structure/metatron_geometry.md`)  
   - High-albedo coating (barium titanate + silica) reflects thermal load

2. **Internal Thermal Extraction**  
   - CryoCore interfaces with heat loop matrix using non-toxic liquid metal (Galinstan)  
   - Latent phase change draws excess heat during overload pulses  

3. **Radiative Cooling**  
   - Radiator fins (graphene-infused copper) emit in 8–14μm bandpass  
   - Cold space backdrop ensures ΔT gradient sustains passive heat loss

4. **Insulation Buffering**  
   - MLI wraps around node internals using 30-layer mylar with Dacron spacing  
   - Prevents conduction/cross-heating between power and sensor banks

---

## 🌡 Thermal Survival Profile

| Zone                  | Temperature Range (°C) | Maintained Value | Method                       |
|------------------------|------------------------|------------------|------------------------------|
| CryoCore interior      | –40 to +100            | ~24°C constant   | Phase change + MLI + shield |
| Sensor banks           | –20 to +70             | ~15–35°C range   | Passive radiator loop       |
| TeslaScythe array zone | –50 to +110            | ~30–40°C         | Shielded from sunface       |

---

## ⚠ Performance Envelope

- Total radiant rejection: ~320W  
- Passive heat radiation capacity: ~170W continuous  
- Peak solar exposure survival: 1360W/m² for 11 min uninterrupted  
- CryoCore thermal buffer charge time: ~16 minutes  
- Overload bleedoff time: ~8.6 minutes per buffer cycle

---

## 💡 Real-World Materials

| Component                  | Material                        | Reason                             |
|----------------------------|----------------------------------|-------------------------------------|
| Radiant Shadow Panels      | Al-Si alloy + barium titanate   | High reflectivity, low weight       |
| CryoCore Loop Tubing       | Teflon-coated Galinstan lines   | Non-toxic, no outgassing            |
| Radiator Fins              | Graphene-on-copper blades       | Lightweight, high IR emissivity     |
| Insulation Layer (MLI)     | Aluminized Mylar + Dacron mesh  | NASA-proven thermal barrier         |

---

## 🧩 Linked Systems

- `/core/cryocore_mount.md`  
- `/structure/metatron_geometry.md`  
- `/power/node_harvest_array.md`

---

## 🌀 Summary

The Cryogenic Veil isn’t a cooling system —  
It’s a **thermal survivability armor**.  
And it works 24/7, with or without power.  
IX-King does not overheat. It **equalizes**.

