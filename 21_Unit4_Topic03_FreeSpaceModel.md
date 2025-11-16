---
title: "Free Space Propagation Model"
id: "unit4-topic3-free-space-model"
tags: ["#propagation", "#unit4", "#path_loss", "#free_space"]
aliases: ["FSPL"]
links: [[FOWC/20_Unit4_Topic02_LargeScalePathLoss.md]]

---

# UNIT IV: Free Space Propagation Model

The Free Space Propagation Model is the simplest and most fundamental model for predicting path loss in a wireless communication system. It describes the ideal scenario where there are no obstacles between the transmitter and receiver, and the signal travels in a direct line-of-sight (LOS) path.

---

## 1. The Ideal Scenario

*   **Assumptions:**
    *   **Line-of-Sight (LOS):** A clear, unobstructed path exists between the transmitting and receiving antennas.
    *   **No Obstacles:** No reflections, diffractions, or scattering from objects in the environment.
    *   **Isotropic Antennas:** Often assumed for simplicity, meaning antennas radiate equally in all directions (though antenna gain can be incorporated).
    *   **Vacuum:** Propagation occurs in a vacuum or free space, without atmospheric absorption.

While these conditions are rarely met in real-world terrestrial communication, the Free Space Model provides a theoretical lower bound for path loss and is a building block for more complex models. It is highly applicable for satellite communication or microwave line-of-sight links.

---

## 2. Free Space Path Loss (FSPL) Formula

The Free Space Path Loss (FSPL) quantifies the signal power loss due to the spreading of the electromagnetic wave as it travels through free space.

> [!formula] Free Space Path Loss (FSPL)
> **In linear units:**
> $$ FSPL = \left(\frac{4\pi d f}{c}\right)^2 $$
> 
> **In decibels (dB):**
> $$ FSPL_{dB} = 20 \log_{10}(d) + 20 \log_{10}(f) + 20 \log_{10}\left(\frac{4\pi}{c}\right) $$
> 
> A more practical form for FSPL in dB, when `d` is in kilometers (km) and `f` is in Megahertz (MHz):
> $$ FSPL_{dB} = 32.44 + 20 \log_{10}(d_{km}) + 20 \log_{10}(f_{MHz}) $$
> 
> Where:
> -   **d** = Distance between transmitter and receiver (in meters for the first two formulas, km for the practical one).
> -   **f** = Frequency of the signal (in Hz for the first two formulas, MHz for the practical one).
> -   **c** = Speed of light (approximately $3 \times 10^8$ m/s).
> -   **32.44** = A constant derived from $20 \log_{10}(4\pi/c)$ when units are km and MHz.

### 2.1. Incorporating Antenna Gains

The received power ($P_r$) can be calculated from the transmitted power ($P_t$) and the path loss, also considering the gains of the transmitting ($G_t$) and receiving ($G_r$) antennas.

> [!formula] Received Power in Free Space
> $$ P_r = P_t G_t G_r \left(\frac{\lambda}{4\pi d}\right)^2 $$
> Where:
> -   **$P_r$** = Received power.
> -   **$P_t$** = Transmitted power.
> -   **$G_t$** = Gain of the transmitting antenna.
> -   **$G_r$** = Gain of the receiving antenna.
> -   **$\lambda$** = Wavelength of the signal ($c/f$). 
> 
> In dB:
> $$ P_{r,dBm} = P_{t,dBm} + G_{t,dBi} + G_{r,dBi} - FSPL_{dB} $$

---

## 3. Example Problem: FSPL Calculation

> [!example] Problem: Free Space Path Loss
> Calculate the Free Space Path Loss (FSPL) for a signal transmitted at 2 GHz over a distance of 10 km.
> 
> **Approach:**
> 1.  **Identify Given Values:**
>     -   Frequency (f) = 2 GHz = 2000 MHz
>     -   Distance (d) = 10 km
> 2.  **Choose Formula:** Use the practical FSPL formula for d in km and f in MHz.
>     $$ FSPL_{dB} = 32.44 + 20 \log_{10}(d_{km}) + 20 \log_{10}(f_{MHz}) $$
> 
> **Calculation:**
> -   $FSPL_{dB} = 32.44 + 20 \log_{10}(10) + 20 \log_{10}(2000)$
> -   $FSPL_{dB} = 32.44 + (20 \times 1) + (20 \times 3.301)$
> -   $FSPL_{dB} = 32.44 + 20 + 66.02$
> -   $FSPL_{dB} = 118.46 \text{ dB}$
> 
> **Solution:**
> The Free Space Path Loss for this scenario is approximately **118.46 dB**.

---

## 4. Limitations of the Free Space Model

While useful, the Free Space Model has significant limitations for terrestrial wireless communication:

*   **No Obstacles:** It assumes no obstructions, which is unrealistic in most real-world environments (urban, suburban, even rural with trees).
*   **No Multipath:** It doesn't account for reflections, diffractions, or scattering, which are major contributors to signal variations and fading.
*   **Overly Optimistic:** It generally predicts lower path loss than what is observed in practice, as it represents the theoretical minimum.

Despite these limitations, it serves as a baseline for understanding the fundamental relationship between distance, frequency, and signal loss.

---

> [!check] ### Exam Focus & Key Takeaways
> 
> **Potential Exam Questions:**
> 1.  "Derive the Free Space Path Loss formula and explain its assumptions."
> 2.  "Calculate the FSPL for a given frequency and distance. What are the limitations of this model for terrestrial communication?"
> 3.  "How do antenna gains affect the received power in a free space environment?"
> 
> **Tips for Answering:**
> - Clearly state the ideal assumptions of the model.
> - Remember the practical formula for FSPL in dB (with km and MHz).
> - Always mention the limitations, especially the lack of accounting for obstacles and multipath.
> 
> **Key Takeaway:** The Free Space Propagation Model provides a theoretical minimum for path loss in an ideal line-of-sight environment. It's crucial for understanding fundamental signal attenuation but is overly optimistic for most real-world terrestrial wireless systems.
