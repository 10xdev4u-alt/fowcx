---
title: "Frequency Division Multiple Access (FDMA)"
id: "unit3-topic2-fdma"
tags: ["#multiple_access", "#unit3", "#fdma"]
aliases: ["FDMA"]
links: [[FOWC/11_Unit3_Topic01_Intro_MA.md]]
---

# UNIT III: Frequency Division Multiple Access (FDMA)

FDMA is one of the simplest and most traditional multiple access techniques. It works by assigning a unique, non-overlapping frequency channel to each user for the entire duration of their connection.

---

## 1. How FDMA Works

In FDMA, the total available bandwidth of the system is divided into a series of smaller frequency bands called channels. When a user initiates a call, they are allocated one of these channels. No other user in the same cell can use that channel until the original user's call is finished.

*   **Channel Allocation:** Each user gets an exclusive, dedicated frequency channel.
*   **Separation:** Channels are separated by **guard bands**, which are small, unused portions of the spectrum between channels. These guard bands are necessary to prevent interference between adjacent channels (Adjacent Channel Interference - ACI).

**Analogy:** Think of a highway with multiple lanes. Each car (user) is assigned its own lane (frequency channel) and must stay within it. The painted lines between the lanes are the guard bands.

```
      ^ Bandwidth
      |
      | +------------------+
      | |     Channel N    |
      | +------------------+
      | |   Guard Band     |
      | +------------------+
      | |       ...        |
      | +------------------+
      | |   Guard Band     |
      | +------------------+
      | |     Channel 2    |
      | +------------------+
      | |   Guard Band     |
      | +------------------+
      | |     Channel 1    |
      | +------------------+
      +--------------------------------------> Time
```
*ASCII Diagram: FDMA divides the total bandwidth into fixed channels separated by guard bands.*

---

## 2. Key Features of FDMA

*   **Technology:** FDMA is typically used with analog systems, though it can be used with digital modulation as well.
*   **Complexity:** It is the least complex of the multiple access schemes as it does not require the complex synchronization needed for TDMA.
*   **Capacity:** The capacity is determined by the total available bandwidth and the width of each channel.
*   **Throughput:** Since the channel is dedicated, the user has continuous access, but the data rate is limited by the channel's bandwidth.

---

## 3. Advantages and Disadvantages

### 3.1. Advantages
1.  **Simplicity:** The technology is simple to implement, as timing and synchronization are not critical.
2.  **Low Overhead:** Once a channel is assigned, no extra bits are needed for synchronization or addressing, unlike in TDMA.
3.  **Continuous Transmission:** The user has continuous access to their channel, making it suitable for analog voice.

### 3.2. Disadvantages
1.  **Inefficient Spectrum Use:** The guard bands between channels represent wasted spectrum that cannot be used for transmission.
2.  **Inflexibility:** A user is assigned a fixed channel capacity, regardless of whether they are speaking or silent. This is inefficient for bursty data traffic.
3.  **Susceptible to Narrowband Interference:** If a specific frequency band is affected by interference, the user on that channel will experience poor quality for the entire duration of the call.

---

## 4. FDMA System Capacity

The number of channels that can be created in an FDMA system can be calculated with a simple formula.

> [!formula] Number of FDMA Channels (N)
> $$ N = \frac{B_{total} - 2B_{guard}}{B_{channel}} $$
> Where:
> - **N** = Number of channels
> - **B_total** = Total available bandwidth
> - **B_guard** = Guard bandwidth at the edge of the allocated spectrum
> - **B_channel** = Bandwidth of a single channel (including the guard bands on either side of it, if specified that way)
>
> A more common variation is:
> $$ N = \frac{B_{total}}{B_{channel}} $$
> Where `B_channel` includes the user bandwidth plus one guard band.

> [!example] Problem: FDMA Channel Calculation
> The AMPS cellular system allocates a total of 12.5 MHz of bandwidth for its forward channels. Each channel consists of a 30 kHz voice channel and a 10 kHz guard band. How many channels can be supported?
>
> **Approach:**
> 1.  **Identify Total Bandwidth:** B_total = 12.5 MHz = 12,500,000 Hz
> 2.  **Identify Channel Bandwidth:** The total width for one channel is the voice channel plus its guard band. B_channel = 30 kHz + 10 kHz = 40 kHz = 40,000 Hz.
> 3.  **Calculate Number of Channels (N):**
>     N = B_total / B_channel
>     N = 12,500,000 / 40,000
>
> **Solution:**
> N = 312.5. Since we cannot have a fraction of a channel, the system can support **312 channels**.

---

> [!check] ### Exam Focus & Key Takeaways
>
> **Potential Exam Questions:**
> 1.  "Explain the principle of FDMA with a neat diagram. What are its main advantages and disadvantages?"
> 2.  "A cellular system is allocated 20 MHz of total spectrum. If each channel requires 25 kHz and a guard band of 5 kHz is needed, calculate the number of channels available in the system."
>
> **Tips for Answering:**
> - Always mention guard bands as a key feature and a source of inefficiency.
> - The "highway lanes" analogy is very effective for explaining FDMA.
> - For calculation problems, be careful with units (MHz vs. kHz).
>
> **Key Takeaway:** FDMA is a simple multiple access scheme that divides the spectrum into dedicated frequency lanes for each user. Its simplicity comes at the cost of spectral inefficiency and inflexibility.
