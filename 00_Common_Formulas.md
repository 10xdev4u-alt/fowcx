---
title: "Common Formulas"
id: "00-formulas"
tags: ["#formulas", "#fowc"]
aliases: ["Formula Sheet"]
links: []
---

# Common Formulas Repository

This file will contain all the important formulas we cover throughout the course.

---

## UNIT II: Fundamentals of Cellular Communication

### Frequency Reuse

1.  **Co-channel Reuse Ratio (Q):**
    -   Relates the distance to the nearest co-channel cell (D) to the cell radius (R).
    -   Formula: $$ Q = \frac{D}{R} = \sqrt{3N} $$
    -   *N* is the cluster size.

2.  **Cluster Size (N):**
    -   Defines the number of cells in a reuse pattern.
    -   Formula: $$ N = i^2 + ij + j^2 $$
    -   *i* and *j* are non-negative integers.

3.  **Signal-to-Interference Ratio (SIR):**
    -   Measures the quality of the signal by comparing the desired signal power (S) to the interference power (I) from co-channel cells.
    -   General Formula: $$ \frac{S}{I} = \frac{S}{\sum_{k=1}^{i_0} I_k} $$
    -   Practical Formula: $$ \frac{S}{I} = \frac{(\sqrt{3N})^n}{i_0} $$
    *n* is the path loss exponent, and *i_0* is the number of first-tier interfering cells (usually 6).

### Interference and System Capacity

1.  **Signal-to-Interference Ratio (SIR) for Co-Channel Interference:**
    -   Formula: $ \frac{S}{I} = \frac{(\sqrt{3N})^n}{i_0} $
    -   *N* is the cluster size.
    -   *n* is the path loss exponent (typically 2 to 4).
    -   *i_0* is the number of first-tier interfering cells (usually 6).

