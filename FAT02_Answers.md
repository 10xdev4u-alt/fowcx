---
title: FAT02 Answer Key - OE22708 Fundamentals of Wireless Communication
id: fat02-answers
tags: 
  - exam
  - answers
  - unit2
  - unit3
aliases: 
  - FAT2 Answers
links: 
  - "[[OE-FAT02.md|FAT02 Question Paper]]"
---

# FAT02 Answer Key: OE22708 - Fundamentals of Wireless Communication

This document provides detailed answers for the FAT02 Question Paper, covering topics from Unit II (Fundamentals of Cellular Communication) and Unit III (Multiple Access Techniques).

## PART A (10 x 2 = 20 Marks)

### Q1. How can RAKE receivers be used to improve the reception of the required signal in CDMA-based systems? (CO3, RBT Level 4)

RAKE receivers improve signal reception in CDMA systems by exploiting multipath propagation. In a multipath environment, multiple delayed versions of the same signal arrive at the receiver. A RAKE receiver uses multiple "fingers," each tuned to a different multipath component. It then:
1.  **Identifies and separates** these distinct multipath components.
2.  **Aligns** them in time.
3.  **Combines** them coherently (e.g., using Maximal Ratio Combining).
By doing so, it effectively gathers the energy from otherwise destructive multipath components, increasing the overall Signal-to-Noise Ratio (SNR) and improving the reliability and quality of the received signal.

### Q2. What is the cluster size of the CDMA system? (CO2, RBT Level 2)

The cluster size (N) of a CDMA system is typically **N=1**. This is because CDMA systems employ **universal frequency reuse**, meaning that all cells in the network can use the same wide frequency band simultaneously. User separation is achieved through unique spreading codes, not by dividing the spectrum geographically.

### Q3. What type of handoff is done in CDMA systems? (CO3, RBT Level 2)

CDMA systems primarily use **Soft Handoff**. This is a "make-before-break" type of handoff where the mobile station establishes a connection with the new base station *before* terminating the connection with the old one. For a brief period, the mobile is simultaneously connected to two or more base stations, ensuring a seamless and highly reliable transition without any perceptible interruption to the user.

### Q4. Compare CCI and ACI. (CO2, RBT Level 4)

| Feature           | Co-Channel Interference (CCI)                      | Adjacent Channel Interference (ACI)                |
| :---------------- | :------------------------------------------------- | :------------------------------------------------- |
| **Source**        | Signals from cells using the *same* frequency.     | Signals from channels *adjacent* in frequency.     |
| **Cause**         | Imperfect frequency reuse (co-channel cells are not sufficiently separated). | Imperfect receiver filters (strong adjacent channel signals "bleed" into the desired channel). |
| **Impact**        | Limits system capacity and signal quality.         | Degrades signal quality, especially if adjacent signal is strong. |
| **Mitigation**    | Increasing frequency reuse distance (larger cluster size N), sectoring. | Careful frequency planning (assigning adjacent channels to distant cells), improved receiver filter design, power control. |

### Q5. How can a cellular provider handle different speeds of customers? (CO2, RBT Level 2)

A cellular provider can handle different speeds of customers using the **Umbrella Cell Concept**.
*   **Mechanism:** This concept involves overlaying large macrocells (the "umbrella") over smaller microcells.
*   **Application:**
    *   **Fast-moving customers** (e.g., in cars on highways) are served by the larger macrocells. This minimizes the number of handoffs they experience, reducing signaling load and potential call drops.
    *   **Slow-moving customers** (e.g., pedestrians in urban areas) are served by the smaller microcells. These microcells offer higher capacity and better signal quality in dense areas.
The Mobile Switching Center (MSC) intelligently directs handoffs based on the mobile's speed.

### Q6. Compare TDD and FDD. (CO3, RBT Level 4)

| Feature           | Time Division Duplex (TDD)                         | Frequency Division Duplex (FDD)                    |
| :---------------- | :------------------------------------------------- | :------------------------------------------------- |
| **Spectrum Use**  | Uses a *single* frequency band for both uplink (UL) and downlink (DL), separated by time slots. | Uses *two separate* frequency bands (one for UL, one for DL), allowing simultaneous transmission. |
| **Simultaneity**  | UL and DL transmissions occur at different times.   | UL and DL transmissions occur simultaneously.      |
| **Guard**         | Requires a **guard time** between UL and DL slots to prevent interference. | Requires a **guard band** between UL and DL frequency bands. |
| **Flexibility**   | More flexible for asymmetric traffic (e.g., more DL data than UL). Can dynamically adjust UL/DL ratio. | Less flexible for asymmetric traffic; UL/DL ratio is fixed by spectrum allocation. |
| **Synchronization** | Requires tight time synchronization.               | Requires tight frequency synchronization.          |
| **Application**   | Often used in Wi-Fi, some 4G/5G deployments.       | Widely used in traditional cellular systems (2G, 3G, 4G). |

### Q7. Differentiate narrow-band and wide-band systems. (CO3, RBT Level 4)

| Feature           | Narrow-band Systems                                | Wide-band Systems                                  |
| :---------------- | :------------------------------------------------- | :------------------------------------------------- |
| **Bandwidth**     | Signal bandwidth is much *less* than the channel's coherence bandwidth. | Signal bandwidth is *greater* than the channel's coherence bandwidth. |
| **Fading**        | Experience **flat fading** (all frequency components fade similarly). | Experience **frequency-selective fading** (different frequency components fade differently). |
| **ISI**           | Less susceptible to Inter-Symbol Interference (ISI). | More susceptible to ISI due to time dispersion.    |
| **Complexity**    | Generally simpler to implement.                    | More complex, often requiring equalization or OFDM to mitigate ISI. |
| **Examples**      | FDMA, TDMA (e.g., GSM).                            | CDMA, OFDM/OFDMA (e.g., 3G, 4G, 5G).               |

### Q8. What are the major drawbacks of CDMA systems? (CO3, RBT Level 2)

The major drawbacks of CDMA systems include:
1.  **Near-Far Problem and Strict Power Control:** If a mobile close to the base station transmits with the same power as a distant mobile, the near mobile's signal will overpower the distant one. This necessitates very fast, accurate, and complex **power control** mechanisms to ensure all signals arrive at the base station with roughly equal strength.
2.  **Synchronization Complexity:** Receivers must be precisely synchronized to the unique spreading code of the desired transmitter to correctly despread the signal. This adds significant complexity to the receiver design.
3.  **Self-Interference:** Even with orthogonal codes, multipath propagation can destroy the orthogonality, causing signals from different users within the same cell to interfere with each other. This limits the ultimate capacity.

### Q9. What is QoS relevant to cellular services? (CO2, RBT Level 4)

**Quality of Service (QoS)** in cellular services refers to the overall performance of a telecommunications service from the perspective of the user. It encompasses various measurable parameters that define the level of satisfaction a user experiences. Key QoS metrics relevant to cellular services include:
*   **Call Blocking Probability:** The likelihood that a new call attempt is denied due to network congestion.
*   **Call Dropping Probability:** The likelihood that an active call is prematurely terminated.
*   **Bit Error Rate (BER):** The rate at which bits are corrupted during transmission.
*   **Throughput:** The actual data rate achieved by the user.
*   **Latency/Delay:** The time taken for data to travel from source to destination.
*   **Voice Quality:** Subjective measure of clarity and intelligibility.

### Q10. Highlight the methods to increase the capacity of cellular systems. (CO2, RBT Level 4)

To increase the capacity of cellular systems, several methods are employed:
1.  **Cell Splitting:** Dividing large cells into smaller microcells or picocells, each with its own base station, to increase the number of available channels per unit area.
2.  **Sectoring:** Using directional antennas at the base station to divide a cell into multiple sectors (e.g., 3 or 6 sectors). This reduces co-channel interference and allows for more aggressive frequency reuse.
3.  **Frequency Reuse Optimization:** Using smaller cluster sizes (N) where interference conditions allow, to reuse frequencies more often.
4.  **Microcell Zone Concept:** Dividing a cell into zones, each with an antenna connected to a central base station. This reduces handoff rates and improves SIR.
5.  **Advanced Modulation and Coding:** Using higher-order modulation schemes (e.g., 64-QAM) and more efficient error-correction codes to transmit more bits per Hz.
6.  **Dynamic Channel Assignment (DCA):** Dynamically allocating channels based on real-time traffic demand, improving spectrum utilization.

## PART B (3 x 10 = 30 Marks)

### Q11(a). (i) Highlight the salient features of the CDMA-based system and write down the equations to calculate it’s efficiency. (CO3, RBT Level 2)

**Salient Features of CDMA-based Systems**

CDMA (Code Division Multiple Access) is a spread spectrum technique that allows multiple users to share the same frequency band simultaneously, separating them by unique pseudo-random codes. Its key features include:

1.  **Universal Frequency Reuse (N=1):** All cells in a CDMA system can use the same wide frequency band. This maximizes the overall system capacity by eliminating the need for complex frequency planning and inter-cell frequency allocation.
2.  **Soft Handoff:** Mobiles can communicate with multiple base stations simultaneously during a handoff, ensuring a seamless "make-before-break" transition and significantly reducing dropped calls.
3.  **Resistance to Multipath Fading:** Due to its wideband nature and the use of RAKE receivers, CDMA can effectively combine energy from multiple delayed signal paths, turning what would be destructive interference in narrowband systems into useful signal energy.
4.  **Inherent Security and Privacy:** The use of unique, pseudo-random spreading codes makes it difficult for unauthorized users to intercept or decode the signal without knowing the specific code.
5.  **Soft Capacity Limit:** Unlike FDMA/TDMA systems which have a hard limit on the number of users (channels), CDMA's capacity is interference-limited. Adding more users gradually increases the noise floor for everyone, leading to a graceful degradation of service rather than abrupt blocking.
6.  **Interference Rejection:** The processing gain of CDMA allows it to suppress narrowband interference, as the interference is spread out while the desired signal is despread.

**Equations to Calculate CDMA Efficiency (Capacity)**

The "efficiency" or capacity of a CDMA system is not as straightforward to calculate with a single, simple formula as in FDMA or TDMA, because it is interference-limited rather than channel-limited. The capacity is typically expressed as the maximum number of simultaneous users (M) that can be supported while maintaining a required Signal-to-Interference Ratio (SIR) or Energy per Bit to Noise Power Spectral Density Ratio ($E_b/N_0$).

A common approximation for the maximum number of users (M) in a single cell (or sector) for a voice system is:

$$ M \approx \frac{PG}{\left(\frac{E_b}{N_0}\right)_{req}} \times \eta_{voice} $$

Where:
*   **M:** Maximum number of simultaneous users (capacity).
*   **PG (Processing Gain):** This is a crucial factor and is defined as the ratio of the spread bandwidth (chip rate, $W$) to the data rate ($R$).
    $$ PG = \frac{W}{R} = \frac{\text{Chip Rate}}{\text{Data Rate}} $$ 
A higher processing gain means the signal is spread more, providing better interference rejection and thus supporting more users.
*   **$(E_b/N_0)_{req}$ (Required Energy per Bit to Noise Power Spectral Density Ratio):** This is the minimum $E_b/N_0$ required at the receiver to achieve a desired Bit Error Rate (BER) or voice quality. This value is typically determined by the modulation and coding scheme used.
*   **$\\eta_{voice}$ (Voice Activity Factor):** In voice communication, users are not speaking 100% of the time. The voice activity factor (typically around 0.4 or 40%) accounts for the periods of silence, allowing more users to share the channel.

**Considerations for Multi-Cell Capacity:**
For a multi-cell environment, the capacity is further reduced by inter-cell interference. The capacity per cell (M) can be approximated as:

$$ M \approx \frac{PG}{\left(\frac{E_b}{N_0}\right)_{req}} \times \frac{1}{1 + f} \times \eta_{voice} $$ 
Where `f` is the inter-cell interference factor (typically 0.5 to 0.6 for a well-designed system).

**Conclusion:**
CDMA's efficiency is fundamentally tied to its ability to manage interference. The processing gain, the required signal quality, and the voice activity factor are key parameters in determining how many users a CDMA system can efficiently support.

### Q11(b). Compare CDMA and FHMA techniques used in wireless communication systems. (CO3, RBT Level 2)

**Introduction:**
CDMA (Code Division Multiple Access) and FHMA (Frequency Hopping Multiple Access) are both spread spectrum techniques designed to allow multiple users to share a common frequency band while providing robustness against interference and enhancing security. However, they achieve this through different spreading mechanisms.

**Comparison Table:**

| Feature             | CDMA (Code Division Multiple Access)               | FHMA (Frequency Hopping Multiple Access)           |
| :------------------ | :------------------------------------------------- | :------------------------------------------------- |
| **Spreading Method**| **Direct Sequence Spread Spectrum (DSSS):** User data is multiplied by a high-rate pseudo-random "chipping sequence." | **Frequency Hopping Spread Spectrum (FHSS):** The carrier frequency rapidly changes ("hops") across a wide band according to a pseudo-random sequence. |
| **User Separation** | By unique, orthogonal **spreading codes**. All users transmit on the same wide frequency band at the same time. | By unique, pseudo-random **hopping sequences**. Users take turns on different frequencies. |
| **Bandwidth Use**   | Signal occupies the *entire* wideband channel continuously. | Signal occupies a *narrowband* channel at any given instant, but hops across a wide total band. |
| **Interference**   | Interference is averaged over the wideband. Resists narrowband interference through processing gain. | Avoids narrowband interference by hopping away from occupied frequencies. |
| **Near-Far Problem**| **Significant problem:** Requires strict and fast power control to ensure signals from all mobiles arrive at the base station with equal power. | **Less severe problem:** Does not require the same level of strict power control as CDMA. |
| **Handoff**         | **Soft Handoff:** Seamless "make-before-break" transitions as mobiles can communicate with multiple base stations simultaneously. | **Hard Handoff:** Typically "break-before-make" transitions, similar to TDMA/FDMA. |
| **Capacity**        | Generally higher capacity due to better spectrum sharing and interference averaging. "Soft" capacity limit. | Generally lower capacity than well-designed CDMA due to potential for "hits" (collisions) between hopping sequences. |
| **Complexity**      | Higher complexity due to strict power control and precise code synchronization. | Complex frequency synthesizers required for rapid hopping. |
| **Examples**        | 3G (UMTS, CDMA2000), IS-95.                        | Bluetooth, some military communication systems, early GSM (as a secondary feature). |

**Conclusion:**
Both CDMA and FHMA are effective spread spectrum techniques, but their underlying principles lead to different operational characteristics. CDMA, with its continuous wideband transmission and code-based separation, offers higher capacity and soft handoff, making it suitable for cellular systems. FHMA, with its frequency-agile nature, excels in interference avoidance and is well-suited for applications like Bluetooth where robustness and co-existence are key.

### Q12(a). If a signal-to-interference ratio of 15dB is required for satisfactory forward channel performance of a cellular system, what is the frequency reuse factor and cluster size that should be used for maximum capacity if the path loss exponent is (a) n=4, (b) n=3? Assume that there are 6 co-channel cells in the first tier and all of them are at the same distance from the mobile. Use suitable approximations. (CO2, RBT Level 4)

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
$$ SIR_{linear} = \frac{(3N)^{n/2}}{i_0} $$
$$ SIR_{linear} \times i_0 = (3N)^{n/2} $$
$$ (SIR_{linear} \times i_0)^{2/n} = 3N $$
$$ N = \frac{1}{3} (SIR_{linear} \times i_0)^{2/n} $$

**Step 3: Calculate N and Frequency Reuse Factor for (a) n=4**

*   **Given:** Path loss exponent, n = 4
*   **Calculation for N:**
    $$ N = \frac{1}{3} (31.62 \times 6)^{2/4} = \frac{1}{3} (189.72)^{1/2} = \frac{1}{3} \sqrt{189.72} $$
    $$ N = \frac{1}{3} \times 13.774 \approx 4.59 $$
*   **Choose Valid Cluster Size:** Cluster size N must be an integer that satisfies $N = i^2 + ij + j^2$. Valid values include 1, 3, 4, 7, 9, 12, etc. Since we need to satisfy the SIR requirement, we must choose the smallest valid integer N *greater than or equal to* 4.59. The smallest valid N is **7**. (For N=4, $N=i^2+ij+j^2$ with $i=2, j=0$ is valid, but $4 < 4.59$, so it won't meet the SIR requirement).
*   **Frequency Reuse Factor:** $1/N = \bf{1/7}$

**Step 4: Calculate N and Frequency Reuse Factor for (b) n=3**

*   **Given:** Path loss exponent, n = 3
*   **Calculation for N:**
    $$ N = \frac{1}{3} (31.62 \times 6)^{2/3} = \frac{1}{3} (189.72)^{0.6667} $$
    $$ N = \frac{1}{3} \times 32.96 \approx 10.98 $$
*   **Choose Valid Cluster Size:** The smallest valid integer N *greater than or equal to* 10.98 is **12**.
*   **Frequency Reuse Factor:** $1/N = \bf{1/12}$

**Summary of Results:**

| Path Loss Exponent (n) | Calculated N (approx.) | Chosen Valid N | Frequency Reuse Factor |
| :--------------------- | :--------------------- | :------------- | :--------------------- |
| **4**                  | 4.59                   | **7**          | **1/7**                |
| **3**                  | 10.98                  | **12**         | **1/12**               |

**Conclusion:**
For a path loss exponent of n=4, a cluster size of N=7 (and a frequency reuse factor of 1/7) should be used. For n=3, a larger cluster size of N=12 (and a frequency reuse factor of 1/12) is required to meet the same SIR requirement. This demonstrates that in environments with lower path loss exponents (meaning signals decay slower, leading to more interference), a larger cluster size is needed to maintain signal quality, which in turn reduces the overall system capacity (as capacity is inversely proportional to N).

### Q12(b). Analyze the differences between static and dynamic channel assignment strategies, and explain how each impacts the efficiency of radio resource utilization in wireless communication systems. (CO2, RBT Level 4)

**Introduction:**
Channel assignment strategies are crucial for managing the limited radio spectrum in cellular systems. They dictate how available channels (frequencies, time slots, codes) are allocated to active calls. The two primary strategies are Fixed Channel Assignment (FCA) and Dynamic Channel Assignment (DCA), each with distinct impacts on resource utilization.

**1. Fixed Channel Assignment (FCA)**

*   **Differences:**
    *   **Principle:** Each cell is permanently allocated a predetermined, fixed set of channels based on the frequency reuse plan. These channels do not change over time.
    *   **Allocation:** Channels are assigned to cells in a static manner, regardless of real-time traffic load.
    *   **Complexity:** Simpler to implement and manage due to its static nature.
    *   **Interference:** Co-channel interference is predictable and can be managed through careful cell planning.

*   **Impact on Efficiency of Radio Resource Utilization:**
    *   **Lower Efficiency:** FCA leads to inefficient spectrum utilization, especially under non-uniform or fluctuating traffic conditions. If a cell has low traffic, its assigned channels remain idle, even if adjacent cells are experiencing high traffic and call blocking. This wastes valuable spectrum.
    *   **Higher Blocking Probability:** Calls can be blocked in a cell even if channels are available elsewhere in the system, simply because all channels *within that specific cell* are occupied. This reduces the overall number of calls the system can handle.
    *   **Rigid:** Does not adapt well to changes in user distribution or network conditions.

**2. Dynamic Channel Assignment (DCA)**

*   **Differences:**
    *   **Principle:** Channels are not permanently assigned to cells. Instead, all available channels are kept in a central pool, and they are allocated to cells on demand.
    *   **Allocation:** Channels are assigned dynamically in real-time based on various criteria such as signal strength, interference levels, and current traffic load in the cell and its neighbors.
    *   **Complexity:** More complex to implement, requiring sophisticated algorithms and real-time processing at the Mobile Switching Center (MSC) and base stations.
    *   **Interference:** Can lead to more unpredictable interference patterns if not managed carefully, requiring robust interference management techniques.

*   **Impact on Efficiency of Radio Resource Utilization:**
    *   **Higher Efficiency:** DCA significantly improves radio resource utilization. Channels are allocated where they are most needed, allowing the system to adapt to fluctuating traffic loads. This reduces the number of idle channels and maximizes the use of the available spectrum.
    *   **Lower Blocking Probability:** Calls are less likely to be blocked because a channel can be assigned from the central pool as long as one is available anywhere in the system and its use does not cause unacceptable interference.
    *   **Flexible:** Highly adaptable to changes in network conditions, user mobility, and traffic hotspots.

**Conclusion:**
While FCA offers simplicity and predictable interference, it is spectrally inefficient and leads to higher call blocking under variable traffic. DCA, despite its higher complexity and signaling overhead, provides much greater efficiency in radio resource utilization by dynamically adapting to real-time traffic demands, thereby maximizing the overall capacity of the wireless communication system.

### Q13(a). (i) Highlight the salient features of the FDMA-based system and write down the equations to calculate the number of simultaneous users. (CO3, RBT Level 4) (ii) Consider a GSM mobile system with TDMA/FDD that uses 25MHz for the forward link and is broken with radio channels of bandwidth 200KHz. If 8 speech channels are supported on a single radio channel with no guard bands, find the number of simultaneous users accommodated. (CO3, RBT Level 4)

**(i) Salient Features of FDMA-based Systems**

FDMA (Frequency Division Multiple Access) is one of the oldest and simplest multiple access techniques. It divides the total available bandwidth into a number of non-overlapping frequency channels, and each user is assigned an exclusive channel for the duration of their communication.

**Salient Features:**
1.  **Dedicated Frequency Channels:** Each user is allocated a unique frequency band for the entire duration of their call.
2.  **Simplicity:** It is relatively simple to implement as it does not require complex time synchronization between users or base stations.
3.  **Continuous Transmission:** Once a channel is assigned, the user has continuous access to it, making it suitable for analog voice communication.
4.  **Guard Bands:** To prevent Adjacent Channel Interference (ACI), small unused frequency bands (guard bands) are placed between adjacent channels, which leads to spectral inefficiency.
5.  **"Hard" Capacity Limit:** The number of simultaneous users is strictly limited by the number of available frequency channels. Once all channels are occupied, new calls are blocked.
6.  **Low Overhead:** Minimal signaling overhead is required once a channel is assigned.

**Equation to Calculate the Number of Simultaneous Users (Channels):**

The number of channels (N) that can be supported in an FDMA system is calculated based on the total available bandwidth and the bandwidth required per channel, including guard bands.

$$ N = \frac{B_{total} - 2B_{guard\_edge}}{B_{channel}} $$

Where:
*   **N:** Total number of available channels (simultaneous users).
*   **$B_{total}$:** Total available system bandwidth.
*   **$B_{guard\_edge}$:** Guard band required at each edge of the total allocated spectrum (if applicable). Often, this term is simplified or absorbed into $B_{channel}$ definition.
*   **$B_{channel}$:** Bandwidth of a single channel, which typically includes the user's signal bandwidth plus any guard bands between adjacent channels.

A more common practical formula, where $B_{channel}$ is defined as the total bandwidth per user (including its own guard band on one side), is:
$$ N = \frac{B_{total}}{B_{channel}} $$

---

**(ii) Calculation for GSM Mobile System**

*   **Given:**
    *   Forward link bandwidth = 25 MHz
    *   Radio channel bandwidth = 200 KHz
    *   Speech channels (users) per radio channel = 8
    *   No guard bands mentioned between radio channels (implied that 200 KHz is the effective channel spacing).

*   **Step 1: Calculate the number of available radio channels.**
    The forward link bandwidth is 25 MHz, and each radio channel occupies 200 KHz.
    $$ \text{Number of Radio Channels} = \frac{\text{Forward Link Bandwidth}}{\text{Radio Channel Bandwidth}} $$
    $$ \text{Number of Radio Channels} = \frac{25 \text{ MHz}}{200 \text{ KHz}} = \frac{25000 \text{ KHz}}{200 \text{ KHz}} = 125 $$
    So, there are 125 distinct radio frequency carriers available.

*   **Step 2: Calculate the total number of simultaneous users.**
    Each radio channel (which is an FDMA channel in this TDMA/FDD system) supports 8 speech channels (users) using TDMA.
    $$ \text{Total Simultaneous Users} = \text{Number of Radio Channels} \times \text{Users per Radio Channel} $$
    $$ \text{Total Simultaneous Users} = 125 \times 8 = \bf{1000} $$

**Conclusion:**
The GSM mobile system, with the given parameters, can accommodate **1000 simultaneous users** on its forward link. This calculation highlights how a hybrid FDMA/TDMA system combines frequency division (for radio channels) and time division (for users within each radio channel) to achieve significant capacity.

### Q13(b). (i) Highlight the salient features of the TDMA-based system and write down the equations to calculate it’s efficiency. (CO3, RBT Level 4) (ii) If GSM uses a frame structure where each frame consists of 8-time slots and each time slot has 156.25 bits, data is transmitted at 270.833 kbps in the channel, then find the time duration of a bit, time duration of a slot, time duration of a frame and time between successive transmission of a user in each time slot. (CO3, RBT Level 4)

**(i) Salient Features of TDMA-based Systems**

TDMA (Time Division Multiple Access) is a digital multiple access technique that allows multiple users to share the same frequency channel by dividing the signal into different time slots. Users transmit in short, periodic bursts during their assigned time slots.

**Salient Features:**
1.  **Shared Frequency, Divided Time:** Multiple users share a single carrier frequency, but each user is allocated a unique, recurring time slot within a frame.
2.  **Digital Technology:** TDMA is inherently a digital technology, allowing for digital voice and data transmission.
3.  **Power Efficiency:** Mobile devices can transmit in bursts and then power down their transmitters during other users' time slots, saving battery life.
4.  **Flexible Data Rates:** It is relatively easy to assign multiple time slots to a single user to provide higher data rates (e.g., for data services).
5.  **Guard Times:** Small guard times are inserted between time slots to prevent overlap due to propagation delays and synchronization inaccuracies.
6.  **Synchronization Requirement:** Requires precise time synchronization between the base station and all mobile users to ensure transmissions occur within their assigned slots.
7.  **"Hard" Capacity Limit:** Like FDMA, TDMA has a hard capacity limit determined by the number of available time slots per frequency channel.

**Equations to Calculate TDMA Efficiency:**

The efficiency of a TDMA system, particularly its frame efficiency, measures the proportion of useful data bits relative to the total bits transmitted, accounting for overhead.

**Frame Efficiency ($\\eta_{frame}$):**
$$ \eta_{frame} = \frac{\text{Total Data Bits per Frame}}{\text{Total Bits per Frame}} \times 100\% $$
Or, equivalently:
$$ \eta_{frame} = \left(1 - \frac{\text{Total Overhead Bits per Frame}}{\text{Total Bits per Frame}}\right) \times 100\% $$

Where:
*   **Total Data Bits per Frame:** The sum of all useful data bits transmitted by all users within one TDMA frame.
*   **Total Bits per Frame:** The sum of all bits (data + overhead) transmitted within one TDMA frame.
*   **Total Overhead Bits per Frame:** Includes synchronization bits, guard bits, control bits, and any unused bits within the frame.

---

**(ii) Calculation for GSM Frame Structure**

*   **Given:**
    *   Each frame consists of 8 time slots.
    *   Each time slot has 156.25 bits.
    *   Data transmitted in the channel at 270.833 kbps ($270.833 \times 10^3$ bits per second).

*   **1. Time Duration of a Bit ($T_{bit}$):**
    The bit rate is the inverse of the bit duration.
    $$ T_{bit} = \frac{1}{\text{Data Rate}} = \frac{1}{270.833 \times 10^3 \text{ bps}} \approx 3.692 \times 10^{-6} \text{ seconds} = \bf{3.692 \text{ µs}} $$

*   **2. Time Duration of a Slot ($T_{slot}$):**
    Each slot contains 156.25 bits.
    $$ T_{slot} = \text{Bits per Slot} \times T_{bit} = 156.25 \times 3.692 \text{ µs} \approx \bf{577 \text{ µs}} $$

*   **3. Time Duration of a Frame ($T_{frame}$):**
    A frame consists of 8 time slots.
    $$ T_{frame} = \text{Number of Slots per Frame} \times T_{slot} = 8 \times 577 \text{ µs} = 4616 \text{ µs} = \bf{4.616 \text{ ms}} $$

*   **4. Time Between Successive Transmissions of a User in Each Time Slot:**
    In a TDMA system, a user is assigned one specific time slot within each frame. Therefore, the time between two successive transmissions for a single user is equal to the duration of one full TDMA frame.
    $$ \text{Time between successive transmissions} = T_{frame} = \bf{4.616 \text{ ms}} $$

**Conclusion:**
These calculations provide a clear understanding of the timing structure within a GSM TDMA system, illustrating how bits are organized into slots and frames to enable multiple users to share the same radio channel.
