# Methodology

## Overview
This study performs a comprehensive computational analysis of the THAP domain across human THAP proteins and their homologs. The workflow integrates sequence curation, motif discovery, structural prediction, and protein–DNA interaction analysis.

---

## 1. Sequence Curation

### 1.1 THAP Protein Identification
- Source: PROSITE database (PS50950)
- Query: "THAP domain"
- Retrieved: 45 experimentally validated THAP domain-containing proteins

### 1.2 Dataset Refinement
- Removed:
  - Non-homolog THAP proteins (e.g., CDC14, Lin15B, DmTNP)
- Classified into:
  - Human THAP proteins (hTHAP0–hTHAP11)
  - Other THAP proteins

---

## 2. Homolog Retrieval

- Source: NCBI Protein Database
- Strategy:
  - Search using each hTHAP protein (e.g., THAP1)
  - Select **longest isoform per organism**
- Exclusion Criteria:
  - Partial sequences
  - Hypothetical/uncharacterized proteins
  - Redundant entries

---

## 3. THAP Domain Identification

- Tools:
  - Clustal Omega
  - MMseqs2
- Method:
  - Multiple sequence alignment (MSA)
  - Manual boundary identification using:
    - **C2CH motif (N-terminal)**
    - **AVPTIF motif (C-terminal)**

---

## 4. Motif Discovery & Conservation Analysis

- Tool: GLAM2
- Approach:
  - Gapped motif detection across homologs
  - Validation using MSA

### Key Features Analyzed:
- C2CH zinc-coordinating motif
- Conserved residues:
  - Cys, His, Pro, Trp, Phe
- Novel conserved residues identified

---

## 5. Secondary Structure Prediction

- Tools:
  - JPRED
  - PSIPRED
  - SPIDER3

### Objective:
- Identify consensus β–α–β fold
- Detect structural variations in:
  - Loop regions (L1–L4)
  - Insertions/deletions

---

## 6. Structural Modeling

- Tool: ColabFold (AlphaFold2)

### Parameters:
- num_relax = 1
- MSA: MMseqs2 (UniRef + environmental DB)
- Pairing mode: unpaired_paired

### Output:
- Top-ranked relaxed model (PDB)

---

## 7. Energy Minimization

- Tool: GROMACS 2023.3

### Setup:
- Force field: CHARMM27
- Water model: TIP3P
- Box: Triclinic
- Neutralization: Counter ions

### Minimization:
- Algorithm: Steepest Descent
- Steps: 50,000
- Convergence: <1000 kJ/mol/nm

---

## 8. DNA Structure Preparation

- Tool: BIOVIA Discovery Studio

### Input:
- Known DNA binding sequences:
  - THAP1: AGTACGGGCAA
  - THAP5: GTGTAACTAAC
  - THAP11: ACTATGATACCCA

---

## 9. Protein–DNA Docking

- Tools:
  - HDOCK
  - NPDOCK

### Strategy:
- Blind docking (no predefined binding site)
- Comparison between:
  - Native hTHAP proteins
  - Long-domain homologs
  - Short-domain homologs

---

## 10. Structural & Interaction Analysis

### Evaluations:
- Atomic interaction mapping
- Secondary structure involvement
- Loop participation (especially L4)

---

## 11. Statistical Analysis

- Tool: GraphPad Prism

### Analysis:
- Pearson correlation:
  - THAP domain length vs total protein length

---

## Key Insight Pipeline

This workflow enables:
- Detection of evolutionary hotspots
- Structural divergence analysis
- Functional impact on DNA binding

The amino-terminal region of the THAP domain was identified as a key evolutionary hotspot influencing DNA-binding interactions.

---
