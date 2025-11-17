---
title: "Time Division Multiple Access (TDMA)"
id: "unit3-topic3-tdma"
tags: ["#multiple_access", "#unit3", "#tdma"]
aliases: ["TDMA"]
links: [[FOWC/11_Unit3_Topic01_Intro_MA.md]]
---

# UNIT III: Time Division Multiple Access (TDMA)

TDMA is a digital multiple access technique that allows multiple users to share the same frequency channel by dividing the signal into different time slots. Instead of giving each user their own frequency, TDMA gives each user their own turn on a shared frequency.

---

## 1. How TDMA Works

In a TDMA system, the radio spectrum is divided into frequency channels (like in FDMA), but each frequency channel is further divided in the time domain. Time is structured into **frames**, and each frame is divided into a fixed number of **time slots**.

*   **Channel Allocation:** Each user is assigned one or more time slots within a repeating frame on a specific frequency.
*   **Transmission:** Users transmit their data in short bursts only during their assigned time slots. For the rest of the frame, the user's transmitter is idle.
*   **Separation:** To prevent time slots from overlapping due to signal propagation delays, small **guard times** are inserted between each time slot.

**Analogy:** Imagine a single-lane road (frequency channel) where traffic is managed by a traffic light. Cars (users) are grouped together, and each group is allowed to pass for a short period (time slot) before the light turns red and the next group gets its turn.

```
<----------------- One TDMA Frame ----------------->
+------+------+------+------+------+------+------+------+
| TS 1 | TS 2 | TS 3 |  ..  | TS N | TS 1 | TS 2 | TS 3 | ... (Next Frame)
+------+------+------+------+------+------+------+------+
  ^      ^      ^             ^
User 1 User 2 User 3         User N
(All on the same frequency)
```
*ASCII Diagram: A TDMA frame is divided into N time slots, with each slot assigned to a different user.*

---

## 2. Structure of a TDMA Frame

A TDMA time slot is not just raw data. It contains overhead bits that are crucial for the system's operation. A typical TDMA slot (like in GSM) includes:

*   **Synchronization Bits:** A known bit pattern that helps the receiver lock onto the start of the slot and synchronize its timing.
*   **Data:** The actual voice or data payload.
*   **Header/Control Information:** Information about the user, the type of data, etc.
*   **Guard Time:** An empty period at the end of the slot to prevent overlap with the next slot.

```
+----------------+----------------+----------------+------------+
| Sync & Control |      Data      | Sync & Control | Guard Time |
+----------------+----------------+----------------+------------+
<---------------------- One Time Slot ------------------------->
```

---

## 3. Advantages and Disadvantages

### 3.1. Advantages
1.  **Spectrum Efficiency:** Allows multiple users to share a single frequency carrier, which is more efficient than dedicating a carrier to one user (as in pure FDMA).
2.  **Flexibility:** It's easy to allocate multiple time slots to a single user to provide higher data rates.
3.  **Power Efficiency:** Since the transmitter is only active during its assigned time slot, it can be turned off for the rest of the frame, saving battery life in mobile devices.
4.  **Less Stringent Filtering:** Compared to FDMA, the requirements for channel filtering are less strict because adjacent channels are not as close in the frequency domain.

### 3.2. Disadvantages
1.  **Synchronization Requirement:** TDMA requires precise synchronization between the base station and all mobile users to ensure transmissions occur exactly within their time slots. This adds complexity.
2.  **Overhead:** A significant portion of each time slot is used for synchronization and control bits, which reduces the overall data throughput. This is known as the overhead of the system.
3.  **Multipath Susceptibility:** The high-speed data bursts within a time slot can be more susceptible to frequency-selective fading caused by multipath propagation.

---

## 4. TDMA System Capacity & Efficiency

The efficiency of a TDMA system is a measure of how much of the transmitted data is useful payload versus overhead.

> [!formula] TDMA Frame Efficiency (η_frame)
> $$ \eta_{frame} = \frac{N_d}{N_f} \times 100\% = \left(1 - \frac{N_{oh}}{N_f}\right) \times 100\% $$
> Where:
> - **η_frame** = Frame Efficiency
> - **N_d** = Number of data bits per frame
> - **N_f** = Total number of bits per frame
> - **N_oh** = Number of overhead bits per frame (N_oh = N_f - N_d)

> [!example] Problem: TDMA Efficiency Calculation
> A GSM system uses a frame structure where each frame consists of 8 time slots. Each time slot carries a total of 156.25 bits, but only 114 of these are actual data bits. The rest are overhead. Calculate the frame efficiency.
>
> **Approach:**
> 1.  **Identify Total Bits per Slot:** N_slot_total = 156.25 bits
> 2.  **Identify Data Bits per Slot:** N_slot_data = 114 bits
> 3.  **Calculate Overhead Bits per Slot:** N_slot_oh = 156.25 - 114 = 42.25 bits
> 4.  **Calculate Efficiency:** The efficiency of a slot is the same as the efficiency of the frame.
>     η = (N_slot_data / N_slot_total) * 100%
>
> **Solution:**
> η = (114 / 156.25) * 100% = 0.7296 * 100% = **72.96%**.
> This means that about 27% of all transmitted data in GSM is overhead required for the system to function.

---

> [!check] ### Exam Focus & Key Takeaways
>
> **Potential Exam Questions:**
> 1.  "Compare and contrast FDMA and TDMA, highlighting at least two advantages and two disadvantages of each."
> 2.  "Draw the structure of a generic TDMA frame and explain the purpose of each component, including guard times."
> 3.  "A TDMA system has a frame rate of 100 frames/second. Each frame has 20 time slots, and each time slot contains 100 data bits and 20 overhead bits. Calculate the system's raw data rate and its efficiency."
>
> **Tips for Answering:**
> - The "taking turns" analogy is key for TDMA.
> - Emphasize that TDMA's main challenge is synchronization.
> - When comparing with FDMA, focus on spectrum sharing (frequency vs. time) and complexity (simple vs. sync-heavy).
>
> **Key Takeaway:** TDMA enables multiple users to share a single frequency by giving each user a recurring time slot. This digital technique improves efficiency over FDMA but introduces the complexity of network-wide time synchronization.
