# Quadcopter — SolidWorks CAD to ANSYS FEA

A complete mechanical-engineering workflow for a quadcopter frame, covering CAD modeling, assembly, static structural analysis, modal analysis, and harmonic response analysis.

## Project Workflow

**SolidWorks CAD → Complete Assembly → ANSYS Mechanical → Static Structural → Modal Analysis → Harmonic Response**

## Repository Contents

```text
quadcopter-drone-cad-fea-analysis/
├── 01_SolidWorks_CAD/
│   ├── Parts/
│   ├── Assembly/
│   ├── Drawings/
│   └── CAD_PART_INVENTORY.md
├── 02_ANSYS/
│   ├── 01_Static_Structural/
│   ├── 02_Modal/
│   ├── 03_Harmonic_Response/
│   ├── 04_Workbench_Archive/
│   └── README.md
├── 03_Report/
│   └── Complete_Engineering_Report.pdf
├── 04_Images/
│   ├── 01_CAD_Assembly/
│   ├── 02_ANSYS_Setup/
│   ├── 03_Static_Structural/
│   ├── 04_Modal/
│   └── 05_Harmonic_Response/
├── README.md
├── .gitattributes
├── .gitignore
└── LICENSE
```

## Key Results From the Supplied Report

| Analysis | Reported result |
|---|---|
| Assembly mass | 4.15 kg |
| Applied structural loading | 32 N per arm; 128 N total |
| Maximum von-Mises stress | 1.3927 MPa |
| Maximum total deformation | 0.86549 mm |
| Equivalent elastic strain | 0.00066362 mm/mm |
| Yield-based factor of safety | ≈35.9 |
| Modal frequencies | 72.582, 72.605, 72.618, 72.620, 89.963, 89.971 Hz |
| Harmonic sweep | 1–150 Hz |
| Main harmonic response region | ≈90 Hz |
| Peak harmonic stress amplitude | ≈0.0151 MPa |
| Peak harmonic deformation amplitude | ≈0.186 mm |

## ANSYS System Mapping

The supplied Workbench archive contains three analysis systems under `dp0`:

- `SYS` → **Static Structural**
- `SYS-1` → **Modal Analysis**
- `SYS-2` → **Harmonic Response**

These labels are used for repository organization; the original ANSYS archive remains unchanged.

## CAD Assemblies

Two assemblies are preserved separately because they serve different purposes:

- **Complete Drone Assembly** — the full quadcopter assembly.
- **Analysis Assembly** — the smaller assembly used for the analysis workflow.

## Engineering Drawings

The supplied 21-page drawing document is preserved at `01_SolidWorks_CAD/Drawings/Part_Dimensions_and_Assembly_Drawings.pdf`. It is the dimensional/drawing reference supplied for the CAD parts and assembly.

## Notes on Large ANSYS Files

The original `archive_DRONE.wbpz` is approximately 362 MB and contains the ANSYS Workbench project and solver data. `.wbpz` is configured for Git LFS in `.gitattributes`. Do not manually extract, rename, or delete internal Workbench files when preserving the source archive.

## Software

The supplied report identifies SolidWorks 2026 SP3.2 and ANSYS Mechanical 2026 R1 Student.
