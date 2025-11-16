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

---

## UNIT III: Multiple Access Techniques

### FDMA

**Problem 1:** The AMPS cellular system allocates a total of 12.5 MHz of bandwidth for its forward channels. Each channel consists of a 30 kHz voice channel and a 10 kHz guard band. How many channels can be supported?

> **Approach:**
> 1.  **Identify Total Bandwidth:** B_total = 12.5 MHz = 12,500,000 Hz.
> 2.  **Identify Full Channel Bandwidth:** The total width for one channel includes the voice channel plus its associated guard band. B_channel = 30 kHz + 10 kHz = 40 kHz = 40,000 Hz.
> 3.  **Calculate Number of Channels (N):** Use the formula N = B_total / B_channel.
>
> **Calculation:**
> -   N = 12,500,000 / 40,000
> -   N = 312.5
>
> **Solution:**
> Since we cannot have a fraction of a channel, the system can support a maximum of **312 channels**.

### TDMA

**Problem 1:** A GSM system uses a frame structure where each time slot carries a total of 156.25 bits, but only 114 of these are actual data bits. The rest are overhead. Calculate the frame efficiency.

> **Approach:**
> 1.  **Identify Total Bits:** The total number of bits in a time slot is N_total = 156.25.
> 2.  **Identify Data Bits:** The number of useful data bits is N_data = 114.
> 3.  **Calculate Efficiency:** The efficiency is the ratio of data bits to total bits. The efficiency of a single slot is representative of the entire frame.
>     $$ \eta = \frac{N_{data}}{N_{total}} \times 100\% $$
>
> **Calculation:**
> -   η = (114 / 156.25) * 100%
> -   η = 0.7296 * 100%
>
> **Solution:**
> The frame efficiency is **72.96%**. This means that approximately 27% of the transmitted information is overhead.
