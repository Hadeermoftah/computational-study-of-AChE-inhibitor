# Computational Study of an Acetylcholinesterase Inhibitor

This repository documents the molecular docking and molecular dynamics workflow used to study compound **6F** in complex with acetylcholinesterase.

## Project Overview

The workflow includes:

- Protein preparation using the AChE structure **PDB 4EY7**
- Ligand preparation and molecular docking
- Selection of the docked 6F pose
- Ligand parameterization using CGenFF/CHARMM-compatible parameters
- Molecular dynamics system preparation in GROMACS
- Energy minimization
- NVT equilibration
- NPT equilibration
- Production molecular dynamics
- Planned trajectory analysis including RMSD, RMSF, radius of gyration, and hydrogen-bond analysis

## Software

- MOE — protein/ligand preparation and docking
- GROMACS 2023.3 — molecular dynamics
- CHARMM36 force field
- CGenFF-derived ligand parameters
- TIP3P water model
- Python — structure validation and analysis

## Repository Structure

```text
MD_6F/
├── inputs/
│   ├── ligand/
│   └── protein/
├── structures/
├── topology/
├── md_setup/
│   └── legacy/
├── scripts/
├── analysis/
├── results/
├── docs/
└── README.md
```
## Molecular Dynamics Setup
The protein-ligand complex was prepared using the CHARMM36 force field with TIP3P water.
The simulation workflow consists of:
1. Energy minimization
2. NVT equilibration
3. NPT equilibration
4. Production MD
The current production setup uses:
- Time step: **2 fs**
- Number of steps: **10,000,000**
- Total production time: **20 ns**
- Temperature: **300 K**
- Pressure: **1 bar**
- Electrostatics: **Particle Mesh Ewald (PME)**
- Bond constraints: **LINCS, hydrogen bonds constrained**
Large trajectory, checkpoint, energy, and run-input files are intentionally excluded from the repository using `.gitignore`.
## Ligand Topology
Compound 6F was parameterized using CHARMM/CGenFF-compatible parameters.
The ligand topology includes a chlorine lone-pair virtual site (`LP1`) defined through a GROMACS `virtual_sites3` construction.
Relevant files are located in:
```text
topology/
```
and the parameterization workflow scripts are stored in:
```text
scripts/
```
## Analysis
After completion of the production trajectory, the following analyses will be performed:
- Protein backbone RMSD
- Ligand RMSD
- RMSF
- Radius of gyration
- Protein-ligand hydrogen bonds
- Binding-site interaction stability
- Representative structural snapshots
Final figures and summarized results will be added to:
```text
results/
```
## Notes
Raw MOE project files, large GROMACS trajectory files, checkpoints, temporary outputs, force-field distributions, and local backup files are not tracked in Git.
This repository is intended to provide a reproducible record of the computational workflow and the key input files required to understand the simulation setup.
