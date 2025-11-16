---
title: Assignment 01 Answer Key - OE22708 Fundamentals of Wireless Communication
id: ass01-answers
tags: 
  - assignment
  - answers
  - unit1
  - unit2
alias: 
  - Assignment 1 Answers
links: 
  - "[[OE-Ass01.md|Assignment 01 Question Paper]]"
---

# Assignment 01 Answer Key: OE22708 - Fundamentals of Wireless Communication

This document provides detailed answers for the Assignment 01 Question Paper.

---

### Q1. Compare various generations (1G to 5G) of wireless communication systems in terms of carrier frequency, operating frequency, modulation technique, multiple access technique, bandwidth, switching type, data rate, applications, advantages and disadvantages. (CO1, RBT Level 2, 10 Marks)

**Introduction**
The evolution of wireless communication is marked by distinct "generations," each representing a significant technological leap. This comparison details the key characteristics of each generation from 1G to 5G across multiple technical and practical parameters.

**Comparison Table: 1G to 5G**

| Feature                 | 1G (First Generation) | 2G (Second Generation) | 3G (Third Generation) | 4G (Fourth Generation) | 5G (Fifth Generation) |
| :---------------------- | :-------------------- | :--------------------- | :-------------------- | :--------------------- | :-------------------- |
| **Operating Frequency** | 800-900 MHz           | 850/900/1800/1900 MHz  | ~1.8-2.5 GHz          | ~2-8 GHz              | Sub-6 GHz & mmWave (24-100 GHz) |
| **Modulation**          | Analog FM             | GMSK, QPSK             | QPSK, 16-QAM          | QPSK, 16-QAM, 64-QAM  | QPSK up to 256-QAM    |
| **Multiple Access**     | FDMA                  | TDMA, CDMA             | W-CDMA, CDMA2000      | OFDMA, SC-FDMA        | OFDMA, Flexible Numerology |
| **Bandwidth**           | 30 KHz                | 200 KHz (GSM)          | 5-20 MHz              | Up to 100 MHz         | Up to 1 GHz+          |
| **Switching Type**      | Circuit-Switched      | Circuit (Voice) & Packet (Data) | Circuit & Packet      | All Packet-Switched    | All Packet-Switched   |
| **Data Rate**           | ~2.4 kbps             | ~64-144 kbps           | ~2-42 Mbps            | ~100 Mbps - 1 Gbps    | ~1-20+ Gbps           |
| **Applications**        | Analog voice calls    | Digital voice, SMS, basic WAP | Mobile web, video calls, GPS | HD video streaming, VoLTE, gaming | IoT, AR/VR, autonomous vehicles, smart cities |
| **Advantages**          | First mobile voice    | Improved security, efficiency, SMS | Higher data rates, mobile internet | High speed, low latency, all-IP | Ultra-low latency, massive capacity, high speed |
| **Disadvantages**       | Poor security, low capacity, poor voice quality | Low data rates, inefficient for data | Higher complexity, less spectral efficiency than 4G | High infrastructure cost | mmWave has short range, high infrastructure cost |

**Conclusion**
The progression from 1G to 5G demonstrates a clear and consistent trend: a shift from analog to digital, from circuit-switched to all-packet-switched networks, and from a voice-centric model to a data-centric ecosystem. Each generation has brought exponential increases in speed, capacity, and spectral efficiency, enabling revolutionary new applications at each step.

---

### Q2. Explain in detail the different handoff strategies for mobile cellular communication systems. (CO1, RBT Level 3, 10 Marks)

**Introduction**
A handoff (or handover) is the process of transferring an active call or data session from one cell to another without service interruption. It is a critical function for maintaining user mobility. Handoff strategies are primarily categorized by how the connection transfer is executed.

**1. Hard Handoff ("Break-Before-Make")**
*   **Mechanism:** In a hard handoff, the mobile station breaks its connection with the current base station *before* establishing a new connection with the target base station. There is a very brief interruption of the communication link.
*   **Technology:** This is the characteristic handoff type for systems where users are separated by frequency or time, such as **FDMA and TDMA** (e.g., GSM). A mobile cannot be tuned to two different frequency channels simultaneously.
*   **Advantages:**
    *   **Simpler Implementation:** Only one connection needs to be managed at any given time, simplifying the mobile device and network logic.
*   **Disadvantages:**
    *   **Higher Dropped Call Probability:** The brief "break" can lead to a dropped call if the new connection is not established quickly and successfully.
    *   **Perceptible Interruption:** While very fast, the break can sometimes cause a momentary glitch in voice or data.

```ascii
      (Moving Direction) -->
+----------+
| Mobile   |
| Station  |
+----------+

   Signal from BS1 (Weakening)
  /
 /
+-----+                               +-----+
| BS1 |<-- Connection is BROKEN -->    | BS2 |
+-----+                               +-----+
                                         \
                                          \
                                    Signal from BS2 (Strengthening)
                                    <-- New connection is MADE
```

**2. Soft Handoff ("Make-Before-Break")**
*   **Mechanism:** In a soft handoff, the mobile station establishes a connection with the new base station *before* breaking its connection with the old one. For a short period, the mobile is connected to two or more base stations simultaneously.
*   **Technology:** This is the characteristic handoff type for **CDMA** systems, where all cells use the same frequency. The mobile can listen to and combine signals from multiple base stations using different spreading codes.
*   **Advantages:**
    *   **Seamless and Reliable:** Eliminates the risk of dropping a call during the handoff instant, as there is no "break" in connectivity.
    *   **Diversity Gain:** By being connected to two base stations at the cell edge (where signals are weakest), the mobile benefits from macro-diversity, improving signal quality.
*   **Disadvantages:**
    *   **Increased Complexity:** The mobile device must be capable of communicating with multiple base stations at once. The network (MSC) must also manage these multiple links and combine the signals.
    *   **Higher Resource Consumption:** During the handoff period, the mobile consumes resources (e.g., codes, channels) from two cells instead of one.

**Conclusion**
The choice of handoff strategy is fundamentally tied to the underlying multiple access technology. Hard handoff is simpler but less reliable, suitable for TDMA/FDMA. Soft handoff is more complex and resource-intensive but provides a highly reliable, seamless transition, making it a key advantage of CDMA systems.

---

### Q3. If a signal to interference ratio of 15 dB is required... what is the frequency reuse factor and cluster size... (CO1, RBT Level 3, 10 Marks)

This question is identical to Q12(a) from FAT02. The solution is as follows:

**Introduction:**
This problem requires us to determine the optimal cluster size (N) and the corresponding frequency reuse factor (1/N) for a cellular system, given a required Signal-to-Interference Ratio (SIR) and path loss exponent (n). The goal is to achieve maximum capacity, which implies using the smallest possible N that satisfies the SIR requirement.

**Given:**
*   Required SIR = 15 dB
*   Number of first-tier interfering cells, $i_0 = 6$

**Formula for SIR:**
The Signal-to-Interference Ratio (SIR) in a cellular system is given by:
$$ \frac{S}{I} = \frac{(\sqrt{3N})^n}{i_0} $$

**Step 1: Convert Required SIR from dB to Linear Scale**
$$ SIR_{linear} = 10^{\frac{SIR_{dB}}{10}} = 10^{\frac{15}{10}} = 10^{1.5} \approx 31.62 $$

**Step 2: Rearrange the SIR formula to solve for N**
$$ N = \frac{1}{3} (SIR_{linear} \times i_0)^{2/n} $$

**Step 3: Calculate N and Frequency Reuse Factor for (a) n=4**

*   **Given:** Path loss exponent, n = 4
*   **Calculation for N:**
    $$ N = \frac{1}{3} (31.62 \times 6)^{2/4} = \frac{1}{3} (189.72)^{1/2} = \frac{1}{3} \sqrt{189.72} $$
    $$ N = \frac{1}{3} \times 13.774 \approx 4.59 $$
*   **Choose Valid Cluster Size:** Cluster size N must be an integer that satisfies $N = i^2 + ij + j^2$. Valid values include 1, 3, 4, 7, 9, 12, etc. We must choose the smallest valid N that is greater than or equal to 4.59. The next valid N is **7**.
*   **Frequency Reuse Factor:** $1/N = \bf{1/7}$

**Step 4: Calculate N and Frequency Reuse Factor for (b) n=3**

*   **Given:** Path loss exponent, n = 3
*   **Calculation for N:**
    $$ N = \frac{1}{3} (31.62 \times 6)^{2/3} = \frac{1}{3} (189.72)^{0.6667} $$
    $$ N = \frac{1}{3} \times 32.96 \approx 10.98 $$
*   **Choose Valid Cluster Size:** The smallest valid N that is greater than or equal to 10.98 is **12**.
*   **Frequency Reuse Factor:** $1/N = \bf{1/12}$

**Conclusion:**
For a path loss exponent of n=4, a cluster size of N=7 is required. For a less forgiving environment with n=3, a larger cluster size of N=12 is needed to maintain the same signal quality, which consequently reduces the system's overall capacity.

---

### Q4. Explain the common techniques for improving the capacity of a cellular system. (CO2, RBT Level 3, 10 Marks)

**Introduction**
Improving the capacity of a cellular system—meaning, increasing the number of users it can support—is a primary goal for all network operators. The main techniques to achieve this involve managing interference and reusing the available spectrum more efficiently.

**1. Cell Splitting**
*   **Concept:** The process of subdividing a congested cell into smaller cells, each with its own low-power base station.
*   **Mechanism:** When traffic in a specific area grows, the large macrocell is replaced by several smaller microcells. The new microcells can have a smaller cluster size, allowing for more frequent reuse of frequency channels in the same geographic area.
*   **Impact:** Dramatically increases capacity in high-traffic areas. However, it increases the number of handoffs and the infrastructure cost (more base stations are needed).

**2. Sectoring**
*   **Concept:** Using directional antennas at the base station to divide a single omnidirectional cell into multiple sectors (typically 3 sectors of 120° or 6 sectors of 60°).
*   **Mechanism:** Instead of radiating power in all directions, each antenna focuses its energy into a specific sector. This reduces the number of interfering co-channel cells for any given user.
*   **Impact:** Improves the Signal-to-Interference Ratio (SIR). This improved SIR allows the system to be designed with a smaller cluster size (N), which means frequencies can be reused more often, thus increasing capacity. It is more cost-effective than cell splitting as it uses the same base station site.

**3. Microcell Zone Concept**
*   **Concept:** An advanced technique where a cell is divided into several "zones," each served by a low-power zone antenna connected to a central base station via fiber or coaxial cable.
*   **Mechanism:** Mobiles in a zone are served by the zone antenna. As a user moves between zones within the same cell, the handoff is managed locally by the single base station, not the MSC.
*   **Impact:** Increases capacity similar to cell splitting but significantly reduces the handoff load on the MSC, improving overall network efficiency.

**4. Advanced Multiple Access and Modulation**
*   **Concept:** Using more spectrally efficient technologies.
*   **Mechanism:** Migrating from older technologies like TDMA to more advanced ones like OFDMA (used in 4G/5G) allows for more flexible and dense packing of users into the available spectrum. Similarly, using higher-order modulation (e.g., 256-QAM vs. 16-QAM) allows more data bits to be sent per symbol, increasing data capacity.

**Conclusion**
These techniques provide network planners with a toolbox to scale system capacity in response to growing user demand. Cell splitting and sectoring are the most fundamental and widely used methods for managing interference and increasing frequency reuse.

---

### Q5. Explain i) Channel assignment strategies ii) Two major types of interference. (CO2, RBT Level 3, 10 Marks)

**i) Channel Assignment Strategies**

Channel assignment strategies dictate how radio channels are allocated to users in a cellular system.

**1. Fixed Channel Assignment (FCA)**
*   **Principle:** Each cell is permanently assigned a fixed set of channels.
*   **Operation:** When a call is initiated, the base station attempts to allocate a free channel from its pre-assigned set. If all channels are busy, the call is blocked.
*   **Pros:** Simple to implement, low signaling overhead.
*   **Cons:** Inefficient for variable traffic. A busy cell may block calls while an adjacent, lightly loaded cell has idle channels.

**2. Dynamic Channel Assignment (DCA)**
*   **Principle:** Channels are not permanently assigned to cells. They are kept in a central pool managed by the MSC.
*   **Operation:** When a call is initiated, the base station requests a channel from the MSC. The MSC allocates a channel based on real-time system conditions (e.g., traffic load, interference levels), ensuring the channel can be used without causing undue interference. When the call ends, the channel is returned to the pool.
*   **Pros:** Highly efficient in utilizing the spectrum, adapts to traffic variations, and reduces call blocking probability.
*   **Cons:** Much more complex to implement, requires significant real-time computation and signaling between the base stations and the MSC.

**ii) Two Major Types of Interference**

Interference is the primary factor limiting the performance and capacity of cellular systems.

**1. Co-Channel Interference (CCI)**
*   **Source:** Interference between cells that use the **same set of frequencies**. These are known as co-channel cells.
*   **Cause:** Arises from the principle of frequency reuse. While co-channel cells are separated geographically, their signals can still propagate into each other's territory.
*   **Mitigation:** CCI is managed by ensuring sufficient distance between co-channel cells. This is achieved by increasing the cluster size (N), which increases the co-channel reuse distance (D). Sectoring also helps reduce CCI.

**2. Adjacent Channel Interference (ACI)**
*   **Source:** Interference from signals in frequency channels that are directly **adjacent** to the desired channel.
*   **Cause:** Caused by imperfect receiver filters that cannot completely reject the energy from strong signals in neighboring frequency bands.
*   **Mitigation:** ACI is managed through:
    *   **Careful Frequency Planning:** Assigning adjacent frequency channels to cells that are geographically distant from one another.
    *   **High-Quality Filters:** Using sharp filters in receivers that can better reject adjacent channel energy.
    *   **Power Control:** Ensuring transmitters do not use excessive power that could "bleed" into adjacent channels.
