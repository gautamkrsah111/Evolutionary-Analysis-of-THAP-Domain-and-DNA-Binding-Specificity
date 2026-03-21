# Evolutionary Analysis of THAP Domain and DNA Binding Specificity

## Overview
This repository presents a comprehensive computational study of the THAP (Thanatos-associated protein) domain across human THAP proteins and their homologs.

The THAP domain is a zinc-coordinating DNA-binding domain with conserved structural features but highly diverse DNA-binding specificities. This work investigates how sequence and structural variations influence DNA-binding interactions.

---

## Key Objectives

- Analyze conservation of THAP domain across species
- Identify structural and sequence variations
- Investigate evolutionary hotspots
- Evaluate impact on protein–DNA interactions

---

## Core Findings

- THAP domains vary significantly in length (short <50 aa, long >100 aa)
- Amino-terminal region acts as an evolutionary hotspot
- Insertions/deletions alter DNA-binding interface
- No universal correlation between protein length and domain length
- Structural fold conserved, but interaction patterns differ

---

## Methodology Summary

The study integrates:

- Sequence curation (PROSITE, NCBI)
- Multiple sequence alignment (Clustal Omega, MMseqs2)
- Motif discovery (GLAM2)
- Secondary structure prediction (JPRED, PSIPRED, SPIDER3)
- Structure prediction (ColabFold / AlphaFold2)
- Energy minimization (GROMACS)
- Protein–DNA docking (HDOCK, NPDOCK)
- Statistical analysis (Pearson correlation)

See [`docs/methodology.md`](docs/methodology.md) for full details.

---

## Repository Structure
```text
.
├── README.md
├── Data/
│   ├── DNA/
│   │   ├── DNA_Prepared_4_Alphafold/
│   │   └── DNA_Prepared_for_4_PDBs/
│   ├── Protein_Structure/
│   │   ├── Alphafold_predictions/
│   │   └── PDB_Database/
│   └── Sequences/              # THAP0–THAP11 sequence files
├── Docs/
│   ├── Methodology.md
│   └── Pipeline_diagram.*
├── Results/
│   ├── Alphafold_analysis/      # PAE, PLDDT, sequence coverage plots
│   ├── Docking/               # HDOCK and NPDOCK results
│   ├── Energy_minimization/     # Minimized protein structures
│   ├── Ramachandran_plot/      # Before/after energy minimization plots
│   ├── Secondary_structure/     # Combined JPRED results
│   └── alignments/           # mmseqs2 outputs
├── Scripts/
│   ├── Energy_Minization_Code/  # GROMACS parameter files and codes
│   └── Pymol_Visualization_scripts/
├── figures/
│   ├── Docking_Visualization/   # PNGs of docking poses
│   └── Inkscape_Edited_SVG/     # Final publication-ready figures
└── Supplementary/
    ├── Protein&Domain Lenght.xls/   # It contains the scallter plots of all the proteins
    └   ...
```



---

## Significance

This work provides:

- A systematic framework for studying DNA-binding domain evolution
- Insights into functional diversification of THAP proteins
- A computational pipeline applicable to other protein families

---

## Future Directions

- Molecular dynamics simulations of protein–DNA complexes
- Experimental validation of binding affinities
- Functional annotation of divergent THAP homologs

---

## Authors

- Hiral M. Sanghavi
- Gautam Kumar Sah   @GautamKrSah111@gmail.com

Department of Biotechnology  
Pandit Deendayal Energy University, India

---

## Data Availability

All datasets and analysis workflows are included or referenced in this repository.

---

## Citation

If you use this work, please cite the associated manuscript.
