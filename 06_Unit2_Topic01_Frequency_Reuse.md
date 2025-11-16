---
title: "Frequency Reuse"
id: "unit2-topic1-frequency-reuse"
tags: ["#cellular", "#frequency_reuse", "#capacity", "#interference", "#unit2"]
alias: ["Frequency Reuse Concept"]
links: [[FOWC/00_Syllabus.md], [FOWC/02_Unit1_Topic02_SystemExamples.md]]
---

# UNIT II: Fundamentals of Cellular Communication - Frequency Reuse

This section introduces the concept of frequency reuse, a cornerstone of modern cellular network design that enables high system capacity.

---

## 1. What is Frequency Reuse?

In wireless communication, the radio spectrum is a finite and precious resource. If every user had a unique frequency that no one else could use, we would run out of channels very quickly.

**Frequency Reuse** is a design strategy where the same set of radio frequencies are reused in different geographic areas (cells) that are sufficiently separated from one another. This separation ensures that the interference between cells using the same frequencies (co-channel cells) is kept at a tolerable level.

By reusing frequencies, the system can support a much larger number of subscribers, dramatically increasing the overall **system capacity**.

### 1.1. The Core Concept: Cells and Clusters

To implement frequency reuse, the service area is divided into a grid of hexagonal cells.

*   **Cell:** The basic geographic unit of a cellular system, served by a single base station.
*   **Cluster:** A group of adjacent cells in which each cell is assigned a unique set of frequencies. The total number of available channels is divided among the cells in a cluster. The size of a cluster is denoted by **N**.

Once the frequency allocation pattern is defined for a cluster, the entire pattern is repeated across the service area.

```
      +-------+
      |   G   |
+-------+-------+-------+
|   B   |   A   |   F   |
+-------+-------+-------+
|   C   |   G   |   E   |
+-------+-------+-------+
      |   D   |
      +-------+
```
*ASCII Diagram: A cluster of N=7 cells (A-G). Each letter represents a unique set of frequencies. This entire 7-cell pattern can be repeated.*

### 1.2. The Frequency Reuse Distance (D)

The key to successful frequency reuse is maintaining sufficient distance between cells that use the same frequencies. This distance is called the **Frequency Reuse Distance (D)**.

The relationship between the cluster size (N), the cell radius (R), and the frequency reuse distance (D) is crucial. For a hexagonal cell geometry, this relationship is given by:

$$
\frac{D}{R} = \sqrt{3N}
$$

This ratio, D/R, is called the **co-channel reuse ratio**, often denoted by **Q**.

> [!note]
> A larger cluster size (N) means a larger frequency reuse distance (D), which leads to lower interference but also fewer channels per cell, thus reducing capacity per cell. There is a fundamental trade-off between capacity and interference.

---

## 2. Determining Cluster Size (N)

The cluster size, N, cannot be any arbitrary number. For a hexagonal cell layout, N can only have values that satisfy the following equation:

$$
N = i^2 + ij + j^2
$$

where `i` and `j` are non-negative integers.

**How it works:**
To find the nearest co-channel cell (a cell using the same frequency set), you move `i` cells along one hexagonal axis, turn 60 degrees counter-clockwise, and then move `j` cells along that new axis.

**Common Cluster Sizes:**
*   If i=1, j=1 -> N = 1^2 + 1*1 + 1^2 = 3
*   If i=2, j=0 -> N = 2^2 + 2*0 + 0^2 = 4
*   If i=2, j=1 -> N = 2^2 + 2*1 + 1^2 = 7 (A very common configuration)
*   If i=3, j=0 -> N = 3^2 + 3*0 + 0^2 = 9
*   If i=2, j=2 -> N = 2^2 + 2*2 + 2^2 = 12

> [!example] Problem: Calculating Channels per Cell
> A cellular system has a total of 395 voice channels available. If a cluster size of N=7 is used, how many channels can be allocated to each cell?
>
> **Approach:**
> 1.  **Identify Total Channels (S):** S = 395
> 2.  **Identify Cluster Size (N):** N = 7
> 3.  **Calculate Channels per Cell (k):** The total channels are divided equally among the cells in the cluster.
>     k = S / N
>     k = 395 / 7 ≈ 56.4
>
> **Solution:** Since we can't have a fraction of a channel, each cell would be allocated approximately **56 channels**. The remaining channels might be reserved for control purposes.

---

## 3. Signal-to-Interference Ratio (SIR)

The performance of a cellular system is heavily dependent on the **Signal-to-Interference Ratio (SIR or S/I)**. This ratio compares the power of the desired signal from the serving base station to the combined power of interfering signals from all co-channel cells.

For a mobile receiver, the SIR can be expressed as:

$$
\frac{S}{I} = \frac{S}{\sum_{k=1}^{i_0} I_k}
$$

Where:
*   **S** is the power of the desired signal.
*   **I_k** is the interference power from the k-th co-channel cell.
*   **i_0** is the number of interfering co-channel cells (typically, the first tier of 6 co-channel cells contributes the most interference).

Assuming the path loss exponent is `n`, the SIR can be simplified in terms of the co-channel reuse ratio (Q = D/R):

$$
\frac{S}{I} = \frac{1}{i_0} \left( \frac{D}{R} \right)^n = \frac{(\sqrt{3N})^n}{i_0}
$$

> [!note]
> *   **Path Loss Exponent (n):** This value depends on the radio environment. In free space, n=2. In urban areas, it typically ranges from 3 to 4.
> *   A higher SIR means better signal quality and fewer dropped calls. To improve SIR, one can increase the cluster size (N), which increases the distance D.

---

> [!check] ### Exam Focus & Key Takeaways
>
> **Potential Exam Questions:**
> 1.  "What is frequency reuse? Explain its importance in cellular communication with the help of a diagram."
> 2.  "A cellular system with a total of 395 channels uses a 4-cell reuse pattern. Calculate the number of channels per cell and the co-channel reuse ratio Q."
> 3.  "Derive the relationship between Signal-to-Interference Ratio (SIR), cluster size (N), and the path loss exponent (n)."
>
> **Tips for Answering:**
> - Always start your definition of frequency reuse by mentioning that spectrum is a limited resource.
> - Use a hexagonal diagram to illustrate cells and clusters. Clearly label co-channel cells.
> - For calculation problems, write down the formulas first (k = S/N, Q = sqrt(3N)), then substitute the values.
> - Understand the trade-off: Increasing N improves SIR (good) but decreases capacity per cell (bad).
>
> **Key Takeaway:** Frequency reuse is the foundational concept that enables high capacity in cellular networks. It is a careful balancing act between maximizing the number of users and minimizing co-channel interference.


