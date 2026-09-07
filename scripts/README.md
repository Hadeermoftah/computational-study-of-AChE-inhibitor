# Utility Scripts

This directory contains third-party utility scripts used during ligand topology preparation. These scripts were not authored by the repository owner.

## cgenff_charmm2gmx.py

Utility for converting CHARMM/CGenFF ligand parameters to GROMACS-compatible files.

- Original author: E. Prabhu Raman (2014)
- Modified by Justin Lemkul (2018) to add lone-pair support
- Modified by Conrard Tetsassi (2019) for NetworkX 2.3 compatibility
- License: GNU Affero General Public License v3 or later

The original copyright and license information is retained in the script header.

## cgenff_charmm2gmx_py3_nx3.py

A later compatibility version of the CGenFF-to-GROMACS conversion utility.

- Original author: E. Prabhu Raman (2014)
- Modified by Justin Lemkul (2018)
- Modified by Conrard Tetsassi (2019)
- Modified by Naeem Mahmood Ashraf (2025) for Python 3.10+ and NetworkX 3.x compatibility
- License information is retained in the script header.

## sort_mol2_bonds.pl

Utility for reordering MOL2 bond listings.

- Author: Justin Lemkul
- License: GPL-3.0

The original authorship and licensing information is retained in the script header.

## Use in This Project

These utilities were used as supporting tools during preparation of the CGenFF-derived, CHARMM-compatible topology for compound 6F. Their inclusion here is for workflow documentation and reproducibility and does not imply authorship by the repository owner.
