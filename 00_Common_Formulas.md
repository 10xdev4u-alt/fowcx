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

---

## UNIT III: Multiple Access Techniques

### FDMA

1.  **Number of Channels (N):**
    -   Calculates the number of channels in an FDMA system.
    -   Formula: $$ N = \frac{B_{total} - 2B_{guard}}{B_{channel}} $$
    -   *B_total* is total bandwidth, *B_guard* is the guard band at the edges of the spectrum, *B_channel* is the bandwidth of one channel.

### TDMA

1.  **Frame Efficiency (η_frame):**
    -   Measures the percentage of data that is useful payload versus overhead.
    -   Formula: $$ \eta_{frame} = \frac{\text{Total Data Bits}}{\text{Total Frame Bits}} \times 100\% = \left(1 - \frac{\text{Total Overhead Bits}}{\text{Total Frame Bits}}\right) \times 100\% $$

### CDMA

1.  **Processing Gain (PG):**
    -   Measures the degree to which the signal is spread.
    -   Formula: $$ PG = \frac{W}{R} = \frac{\text{Chip Rate}}{\text{Data Rate}} $$
    -   *W* is the bandwidth of the spread signal, *R* is the data rate of the original signal.

---

## UNIT IV: Mobile Radio Propagation

### Path Loss Models

1.  **Free Space Path Loss (FSPL) in dB:**
    -   For distance `d` in km and frequency `f` in MHz:
    -   Formula: $$ FSPL_{dB} = 32.44 + 20 \log_{10}(d_{km}) + 20 \log_{10}(f_{MHz}) $$

2.  **Received Power in Free Space (in dBm):**
    -   Formula: $$ P_{r,dBm} = P_{t,dBm} + G_{t,dBi} + G_{r,dBi} - FSPL_{dB} $$
    -   *P_t* is transmitted power, *G_t* and *G_r* are transmit and receive antenna gains.

3.  **Log-Distance Path Loss Model:**
    -   Formula: $$ PL(d) = PL(d_0) + 10n \log_{10}\left(\frac{d}{d_0}\right) $$
    -   *PL(d)* is path loss at distance `d`, *PL(d_0)* is path loss at reference distance `d_0`, *n* is the path loss exponent.

