---
title: Assignment 02 Answer Key - OE22708 Fundamentals of Wireless Communication
id: ass02-answers
tags: 
  - assignment
  - answers
  - unit3
alias: 
  - Assignment 2 Answers
links: 
  - "[[OE-Ass02.md|Assignment 02 Question Paper]]"
---

# Assignment 02 Answer Key: OE22708 - Fundamentals of Wireless Communication

This document provides detailed answers for the Assignment 02 Question Paper.

---

### Q1(a). Consider the Global System for Mobile, which is a TDMA/FDD system that uses 25 MHz for the forward link, which is broken into radio channels of 200 kHz. If 8 speech channels are supported on a single radio channel, and if no guard band is assumed, find the number of simultaneous users that can be accommodated in GSM. (CO3, RBT Level 3, 10 Marks)

**Introduction**
This problem requires calculating the total user capacity of a GSM system based on its frequency allocation (FDMA component) and time-slot allocation (TDMA component).

**Given:**
*   Total Forward Link Bandwidth ($B_{total}$) = 25 MHz
*   Radio Channel Bandwidth ($B_{channel}$) = 200 KHz
*   Users (speech channels) per Radio Channel = 8

**Step 1: Calculate the number of available radio channels.**
The system uses FDMA to create distinct radio channels from the total available spectrum.
$$ \text{Number of Radio Channels} = \frac{B_{total}}{B_{channel}} $$
$$ \text{Number of Radio Channels} = \frac{25 \text{ MHz}}{200 \text{ KHz}} = \frac{25000 \text{ KHz}}{200 \text{ KHz}} = 125 $$
There are 125 distinct radio frequency carriers available.

**Step 2: Calculate the total number of simultaneous users.**
Each of the 125 radio channels is further subdivided in time using TDMA to support 8 users.
$$ \text{Total Simultaneous Users} = \text{Number of Radio Channels} \times \text{Users per Radio Channel} $$
$$ \text{Total Simultaneous Users} = 125 \times 8 = \bf{1000} $$

**Conclusion:**
The GSM system described can accommodate **1000 simultaneous users**.

---

### Q1(b). If Bt is 12.5MHz, Bguard is 10 kHz, and Bc is 30 kHz, find the number of channels available in an FDMA system. (CO3, RBT Level 3, 10 Marks)

**Introduction**
This problem requires calculating the number of channels in an FDMA system, accounting for the channel bandwidth and the guard band between channels.

**Given:**
*   Total Bandwidth ($B_t$) = 12.5 MHz
*   Guard Band ($B_{guard}$) = 10 KHz
*   Channel Bandwidth ($B_c$) = 30 KHz

**Step 1: Determine the total bandwidth occupied by one channel.**
In an FDMA system, the total bandwidth for one channel includes the carrier bandwidth plus the guard band required to prevent interference with the next channel.
$$ B_{channel\_total} = B_c + B_{guard} $$
$$ B_{channel\_total} = 30 \text{ KHz} + 10 \text{ KHz} = 40 \text{ KHz} $$

**Step 2: Calculate the number of available channels.**
The total number of channels is the total system bandwidth divided by the total bandwidth occupied by a single channel.
$$ \text{Number of Channels} = \frac{B_t}{B_{channel\_total}} $$
$$ \text{Number of Channels} = \frac{12.5 \text{ MHz}}{40 \text{ KHz}} = \frac{12500 \text{ KHz}}{40 \text{ KHz}} = 312.5 $$

**Step 3: Finalize the number of channels.**
Since a system cannot have half a channel, we take the integer part of the result.
$$ \text{Number of Channels} = \bf{312} $$

**Conclusion:**
The FDMA system can support **312 channels**.

---

### Q2. If GSM uses a frame structure where each frame consists of 8 time slots, and each time slot contains 156.25 bits, and data is transmitted at 270.833 kbps in the channel, find (a) the time duration of a bit, (b) the time duration of a slot, (c) the time duration of a frame, and (d) how long must a user occupying a single time slot must wait between two simultaneous transmissions. (CO3, RBT Level 3, 10 Marks)

This question is identical to Q13(b) from FAT02. The solution is as follows:

**Given:**
*   Slots per Frame = 8
*   Bits per Slot = 156.25
*   Channel Bit Rate = 270.833 kbps ($270,833$ bits per second)

**(a) Time Duration of a Bit ($T_{bit}$):**
The bit duration is the inverse of the bit rate.
$$ T_{bit} = \frac{1}{\text{Data Rate}} = \frac{1}{270,833 \text{ bps}} \approx 3.692 \times 10^{-6} \text{ seconds} = \bf{3.692 \text{ µs}} $$

**(b) Time Duration of a Slot ($T_{slot}$):**
The slot duration is the number of bits in a slot multiplied by the bit duration.
$$ T_{slot} = \text{Bits per Slot} \times T_{bit} = 156.25 \times 3.692 \text{ µs} \approx \bf{577 \text{ µs}} $$

**(c) Time Duration of a Frame ($T_{frame}$):**
The frame duration is the number of slots in a frame multiplied by the slot duration.
$$ T_{frame} = \text{Slots per Frame} \times T_{slot} = 8 \times 577 \text{ µs} = 4616 \text{ µs} = \bf{4.616 \text{ ms}} $$

**(d) Wait Time Between Transmissions:**
A user occupying a single time slot transmits once per frame. Therefore, the wait time between two consecutive transmissions for that user is exactly one frame duration.
$$ \text{Wait Time} = T_{frame} = \bf{4.616 \text{ ms}} $$

---

### Q3. If a normal GSM time slot consists of 6 trailing bits, 8.25 guard bits, 26 training bits, and 2 traffic bursts of 58 bits of data, find the frame efficiency. (CO3, RBT Level 3, 10 Marks)

**Introduction**
Frame efficiency in a TDMA system measures the percentage of transmitted bits that carry useful user data, as opposed to overhead bits required for control and synchronization.

**Given (per time slot):**
*   Trailing Bits = 6
*   Guard Bits = 8.25
*   Training Bits = 26
*   Traffic Data = 2 bursts of 58 bits = $2 \times 58 = 116$ bits

**Step 1: Calculate the total number of bits per time slot.**
The total bits are the sum of all data and overhead bits.
$$ \text{Total Bits} = (\text{Traffic Bits}) + (\text{Trailing Bits}) + (\text{Guard Bits}) + (\text{Training Bits}) $$
$$ \text{Total Bits} = 116 + 6 + 8.25 + 26 = \bf{156.25 \text{ bits}} $$
This matches the standard GSM slot size given in the previous question.

**Step 2: Identify the number of useful data bits.**
The useful data bits are the traffic bits.
$$ \text{Useful Bits} = 116 \text{ bits} $$

**Step 3: Calculate the frame efficiency ($\eta_{frame}$).**
Efficiency is the ratio of useful bits to total bits.
$$ \eta_{frame} = \frac{\text{Useful Bits}}{\text{Total Bits}} \times 100\% $$
$$ \eta_{frame} = \frac{116}{156.25} \times 100\% = \bf{74.24\%} $$

**Conclusion:**
The frame efficiency of a normal GSM time slot is **74.24%**. This means that roughly 25.76% of the transmission is dedicated to overhead required for the system to function correctly.

---

### Q4. Find the inter-modulation (IM) frequencies generated if a base station transmits two carrier frequencies at 1930 MHz and 1932 MHz that are amplified by a saturated clipping amplifier. If the mobile radio band is allocated from 1920 MHz to 1940 MHz, designate the IM frequencies that lie inside and outside the band. (CO3, RBT Level 3, 10 Marks)

**Introduction**
When multiple signals pass through a non-linear device, such as a saturated amplifier, they mix and create new, unwanted frequency components called Inter-Modulation (IM) products. The most problematic are the third-order products, as they are closest in frequency to the desired signals.

**Given:**
*   Carrier Frequency 1 ($f_1$) = 1930 MHz
*   Carrier Frequency 2 ($f_2$) = 1932 MHz
*   Mobile Radio Band = 1920 MHz to 1940 MHz

**Step 1: Calculate the third-order IM products.**
The formulas for the two main third-order IM products are:
*   Lower Product: $f_{IM3,lower} = 2f_1 - f_2$
*   Upper Product: $f_{IM3,upper} = 2f_2 - f_1$

**Calculation:**
$$ f_{IM3,lower} = 2 \times 1930 - 1932 = 3860 - 1932 = \bf{1928 \text{ MHz}} $$
$$ f_{IM3,upper} = 2 \times 1932 - 1930 = 3864 - 1930 = \bf{1934 \text{ MHz}} $$

**Step 2: Designate the IM frequencies relative to the band.**
We compare the calculated IM frequencies to the allocated band (1920-1940 MHz).

*   **1928 MHz:** This frequency is greater than 1920 MHz and less than 1940 MHz. Therefore, it lies **inside** the band.
*   **1934 MHz:** This frequency is greater than 1920 MHz and less than 1940 MHz. Therefore, it lies **inside** the band.

**Conclusion:**
Both of the significant third-order inter-modulation products, **1928 MHz** and **1934 MHz**, fall inside the allocated mobile radio band. This is a serious problem, as they will cause interference to other users operating on or near these frequencies.

---

### Q5. Compare FDMA, TDMA and CDMA – Features, Merits, Demerits, Applications. (CO3, RBT Level 4, 10 Marks)

**Introduction**
FDMA, TDMA, and CDMA are the three fundamental multiple access techniques used to allow multiple users to share a limited radio spectrum. They achieve this by dividing the spectrum by frequency, time, or code, respectively.

**Comparison Table**

| Feature             | FDMA (Frequency Division MA) | TDMA (Time Division MA) | CDMA (Code Division MA) |
| :------------------ | :--------------------------- | :---------------------- | :---------------------- |
| **Separation**      | By Frequency                 | By Time                 | By Code                 |
| **Transmission**    | Continuous                   | Bursty (in time slots)  | Continuous              |
| **Bandwidth**       | Narrowband channel per user  | Wider channel shared by users | Wideband channel shared by all users |
| **Synchronization** | Not required               | Strict time synchronization required | Strict code and power control required |
| **Near-Far Problem**| Not an issue                 | Not a major issue       | **Significant issue**, requires strict power control |
| **Handoff**         | Hard Handoff                 | Hard Handoff            | Soft Handoff            |
| **Capacity**        | Low, limited by channels     | Medium, limited by slots | High, "soft" capacity limited by interference |
| **Merits**          | Simple, low overhead         | Power efficient (bursty TX), flexible data rates | High capacity, soft handoff, resists multipath |
| **Demerits**        | Inefficient (guard bands), rigid capacity | Requires synchronization, guard times | Complex power control, self-interference |
| **Applications**    | Analog 1G systems, satellite TV | 2G systems (GSM), DECT phones | 3G systems (UMTS, CDMA2000), GPS |

**Conclusion**
The choice of multiple access technique has a profound impact on a system's design, capacity, and complexity. While FDMA is the simplest, CDMA offers the highest capacity and most robust performance in mobile environments, though at the cost of significant complexity. TDMA represents a practical middle ground, widely used in 2G systems. Modern systems like 4G and 5G use even more advanced hybrid techniques like OFDMA.