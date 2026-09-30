# Quadcopter Drone — SolidWorks CAD & ANSYS FEA

A complete mechanical engineering project covering **3D CAD design, assembly development, mass-property evaluation, finite-element analysis, modal analysis, and harmonic response analysis** of a quadcopter frame.

The project follows a complete CAD-to-CAE workflow:

**SolidWorks Part Design → Assembly → Mass Properties → ANSYS Setup → Static Structural → Modal → Harmonic Response**

---

## 📌 Project Overview

This project presents the mechanical design and structural/vibration analysis of a quadcopter developed in SolidWorks and analyzed using ANSYS Mechanical.

Individual mechanical components were modeled in SolidWorks and assembled into a complete quadcopter containing the structural frame, arms, motors, propellers, covers, stands, controller unit, and fastening hardware.

The completed CAD assembly was then used as the basis for finite-element analysis in ANSYS Mechanical.

The analysis consists of:

- Static Structural Analysis
- Modal Analysis
- Harmonic Response Analysis

The objective is to evaluate:

- Structural deformation
- Equivalent von-Mises stress
- Equivalent elastic strain
- Factor of safety against yielding
- Natural frequencies
- Mode shapes
- Frequency-dependent dynamic response
- Resonance-sensitive regions

---

## 🛠️ Software Used

| Software | Version / Platform |
|---|---|
| SolidWorks | Design 2026 SP3.2 |
| ANSYS Mechanical | 2026 R1 Student |
| Git / GitHub | Version-controlled project repository |
| Git LFS | Large ANSYS Workbench archive |

---

## 🔧 Project Specifications

| Parameter | Value |
|---|---:|
| Assembly mass | **4.15 kg** |
| Structural load | **32 N × 4 arms = 128 N** |
| Mesh size | **10 mm** |
| Material basis | **PETG-based** |
| Young's modulus | **2.1 GPa** |
| Poisson's ratio | **0.35** |
| Tensile yield strength | **50 MPa** |
| Static maximum stress | **1.3927 MPa** |
| Static maximum deformation | **0.86549 mm** |
| Modal frequency range | **72.582–89.971 Hz** |
| Harmonic sweep | **1–150 Hz** |
| Critical harmonic region | **≈90 Hz** |

The reported assembly mass of 4.15 kg is the SolidWorks model value used for the project analysis. The report notes that one or more components have overridden mass properties, so this should be interpreted as the model value rather than an independently measured physical mass. :contentReference[oaicite:1]{index=1}

---

# 📂 Repository Structure

```text
quadcopter-drone-cad-fea-analysis/
│
├── 01_SolidWorks_CAD/
│   ├── Parts/
│   │   ├── 01_Structural/
│   │   ├── 02_Covers_Mounting/
│   │   ├── 03_Propulsion/
│   │   └── 04_Fasteners/
│   │
│   ├── Assembly/
│   │   ├── 01_Complete_Drone_Assembly/
│   │   └── 02_Analysis_Assembly/
│   │
│   ├── Drawings/
│   └── CAD_PART_INVENTORY.md
│
├── 02_ANSYS/
│   ├── 01_Static_Structural/
│   ├── 02_Modal/
│   ├── 03_Harmonic_Response/
│   └── 04_Workbench_Archive/
│       └── archive_DRONE.wbpz
│
├── 03_Report/
│   └── Complete_Engineering_Report.pdf
│
├── 04_Images/
│   ├── 01_CAD_Assembly/
│   ├── 02_ANSYS_Setup/
│   ├── 03_Static_Structural/
│   ├── 04_Modal/
│   └── 05_Harmonic_Response/
│
├── .gitattributes
├── .gitignore
├── LICENSE
└── README.md