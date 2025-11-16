---
title: "Small Scale Multipath Propagation"
id: "unit4-topic5-small-scale-multipath"
tags: ["#propagation", "#unit4", "#multipath", "#fading", "#isi"]
alias: ["Multipath Fading"]
links: [[FOWC/22_Unit4_Topic04_PropagationMechanisms.md]]

---

# UNIT IV: Small Scale Multipath Propagation

Small Scale Multipath Propagation, often simply called **multipath fading**, refers to the rapid fluctuations in the amplitude, phase, or delay of a radio signal over a short period of time or over a small geographical travel distance. These rapid changes are caused by the constructive and destructive interference of multiple versions of the transmitted signal arriving at the receiver.

---

## 1. The Origin of Multipath

As discussed in the previous topic, radio waves interact with the environment through reflection, diffraction, and scattering. These interactions create multiple paths for the signal to travel from the transmitter (Tx) to the receiver (Rx).

```
      Tx
      | \
      |  \ Direct Path
      |   \
      |    \
      |     \
      |      \
      |       \
      |        \ Reflected Path 1
      |         \
      |          \
      |           \
      +------------+-------------------- Rx
      |            |
      |            | Reflected Path 2
      +------------+-------------------- Ground/Building
```
*ASCII Diagram: Multiple signal paths (direct, reflected) arriving at the receiver.*

Each path has a different length, meaning the signals arrive at the receiver at slightly different times and with different amplitudes and phases. When these multiple versions of the signal combine at the receiver antenna, they can either add up (constructive interference) or cancel each other out (destructive interference).

---

## 2. Effects of Small Scale Multipath

Multipath propagation has three major effects on the received signal:

### 2.1. Rapid Fluctuations in Signal Strength (Fading)
*   **Description:** The most noticeable effect. As the mobile moves, the phase relationships between the multipath components change rapidly, causing the received signal strength to fluctuate dramatically (sometimes by 20-30 dB) over distances as small as half a wavelength.
*   **Impact:** Leads to "dead spots" or "fadeouts" where the signal temporarily drops below the receiver's sensitivity, causing dropped calls or data errors.

### 2.2. Time Dispersion (Inter-Symbol Interference - ISI)
*   **Description:** Different multipath components arrive at different times, causing the transmitted signal to be "smeared" or spread out in time. If the delay spread is significant, a symbol from one transmission can overlap and interfere with a subsequent symbol.
*   **Impact:** Limits the maximum data rate that can be reliably transmitted. High data rates mean shorter symbol durations, making them more susceptible to ISI.

### 2.3. Frequency Dispersion (Doppler Spread)
*   **Description:** When the mobile is moving, the frequency of the received signal changes due to the Doppler effect. Different multipath components arrive from different directions, each experiencing a slightly different Doppler shift. This spreads the signal's energy in the frequency domain.
*   **Impact:** Causes frequency-selective fading and limits the coherence time of the channel.

---

## 3. Types of Small Scale Fading

Small scale fading is often characterized by two main statistical distributions:

### 3.1. Rayleigh Fading
*   **Conditions:** Occurs when there is no dominant line-of-sight (LOS) path between the transmitter and receiver, and the signal arrives via many reflected and scattered paths.
*   **Characteristics:** The envelope of the received signal follows a Rayleigh distribution. Common in dense urban environments or indoors where LOS is blocked.

### 3.2. Rician Fading
*   **Conditions:** Occurs when there is a strong dominant line-of-sight (LOS) path in addition to several weaker multipath components.
*   **Characteristics:** The envelope of the received signal follows a Rician distribution. Common in less obstructed environments (e.g., suburban) or when the mobile is close to the base station.

---

## 4. Coherence Bandwidth and Coherence Time

These two parameters quantify the time and frequency characteristics of the fading channel.

*   **Coherence Bandwidth ($B_c$):** A measure of the range of frequencies over which the channel can be considered "flat" (i.e., all frequency components experience similar fading). If the signal bandwidth is greater than $B_c$, the channel is **frequency-selective** (different frequencies fade differently).
*   **Coherence Time ($T_c$):** A measure of the duration over which the channel impulse response is essentially invariant. If the symbol duration is greater than $T_c$, the channel is **time-selective** (fading changes significantly during a symbol).

---

> [!check] ### Exam Focus & Key Takeaways
> 
> **Potential Exam Questions:**
> 1.  "What is small scale multipath propagation? Explain its three major effects on the received signal."
> 2.  "Differentiate between Rayleigh and Rician fading, including the conditions under which each occurs."
> 3.  "Define coherence bandwidth and coherence time, and explain their significance in wireless channel characterization."
> 
> **Tips for Answering:**
> - Emphasize that multipath is caused by reflection, diffraction, and scattering.
> - Clearly explain how constructive/destructive interference leads to fading.
> - Connect time dispersion to ISI and frequency dispersion to Doppler spread.
> 
> **Key Takeaway:** Small scale multipath propagation causes rapid signal fluctuations (fading), time dispersion (ISI), and frequency dispersion (Doppler spread). Understanding these effects is crucial for designing robust wireless systems that can mitigate their detrimental impact.
