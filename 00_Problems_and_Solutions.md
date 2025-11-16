---
title: "Problems and Solutions"
id: "00-problems"
tags: ["#problems", "#fowc"]
aliases: ["Problem Bank"]
links: []
---

# Problems and Solutions Repository

This file will contain all the practice problems and their solutions we cover throughout the course.

---

## UNIT II: Fundamentals of Cellular Communication

### Frequency Reuse

**Problem 1:** A cellular system has a total of 395 voice channels available. If a cluster size of N=7 is used, how many channels can be allocated to each cell?

> **Approach:**
> 1.  **Identify Total Channels (S):** The total number of available voice channels is given as S = 395.
> 2.  **Identify Cluster Size (N):** The frequency reuse pattern is defined by the cluster size, given as N = 7.
> 3.  **Calculate Channels per Cell (k):** The total channels are divided equally among the cells within a single cluster. The formula is `k = S / N`.
>
> **Calculation:**
> -   k = 395 / 7
> -   k ≈ 56.4
>
> **Solution:**
> Since a cell cannot be assigned a fraction of a channel, we take the integer part of the result. Each cell would be allocated **56 channels**. The remaining channels (395 - 56*7 = 3) might be unused or reserved as control channels.

### Interference and System Capacity

**Problem 1:** A cellular system uses a cluster size of N=7. The path loss exponent (n) is 4. Assuming there are 6 first-tier interfering cells (i_0 = 6), calculate the Signal-to-Interference Ratio (SIR) in dB.

> **Approach:**
> 1.  **Identify Given Values:**
>     -   Cluster Size (N) = 7
>     -   Path Loss Exponent (n) = 4
>     -   Number of Interfering Cells (i_0) = 6
> 2.  **Apply SIR Formula:** Use the formula for SIR in terms of N, n, and i_0:
>     $$ \frac{S}{I} = \frac{(\sqrt{3N})^n}{i_0} $$
> 3.  **Convert to dB:** Convert the linear SIR value to decibels (dB) using the formula:
>     $$ SIR_{dB} = 10 \log_{10} \left( \frac{S}{I} \right) $$
>
> **Calculation:**
> -   First, calculate the linear SIR:
>     $$ \frac{S}{I} = \frac{(\sqrt{3 \times 7})^4}{6} = \frac{(\sqrt{21})^4}{6} = \frac{(21)^2}{6} = \frac{441}{6} = 73.5 $$
> -   Now, convert to dB:
>     $$ SIR_{dB} = 10 \log_{10} (73.5) $$
>     $$ SIR_{dB} \approx 10 \times 1.866 = 18.66 \text{ dB} $$
>
> **Solution:**
> The Signal-to-Interference Ratio (SIR) for this cellular system is approximately **18.66 dB**.
