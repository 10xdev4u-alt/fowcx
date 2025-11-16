---
title: Assignment 03 Answer Key - OE22708 Fundamentals of Wireless Communication
id: ass03-answers
tags: 
  - assignment
  - answers
  - unit4
  - unit5
alias: 
  - Assignment 3 Answers
links: 
  - "[[OE-Ass03.md|Assignment 03 Question Paper]]"
---

# Assignment 03 Answer Key: OE22708 - Fundamentals of Wireless Communication

This document provides detailed answers for the Assignment 03 Question Paper.

---

### Q1. Determine the far-field distance for a base station antenna with largest dimension D=0.5m, when the frequency of operation is fc=900MHz, 1800MHz and comment on the result. (CO4, RBT Level 3, 5 Marks)

**Introduction**
The far-field (or Fraunhofer) distance, $d_f$, is the minimum distance from an antenna where the radiation pattern becomes independent of distance. It is calculated using the formula $d_f = \frac{2D^2}{\lambda}$, where D is the largest dimension of the antenna and $\lambda$ is the wavelength.

**Given:**
*   Largest dimension of the antenna, D = 0.5 m
*   Frequencies, $f_1 = 900$ MHz and $f_2 = 1800$ MHz

**Step 1: Calculation for f = 900 MHz**
*   **Wavelength ($\\lambda_1$):** $\\lambda_1 = c / f_1 = (3 \times 10^8 \text{ m/s}) / (900 \times 10^6 \text{ Hz}) = 0.333$ m.
*   **Far-Field Distance ($d_{f1}$):**
    $$ d_{f1} = \frac{2 \times (0.5 \text{ m})^2}{0.333 \text{ m}} = \frac{0.5}{0.333} = \bf{1.5 \text{ meters}} $$

**Step 2: Calculation for f = 1800 MHz**
*   **Wavelength ($\\lambda_2$):** $\\lambda_2 = c / f_2 = (3 \times 10^8 \text{ m/s}) / (1800 \times 10^6 \text{ Hz}) = 0.167$ m.
*   **Far-Field Distance ($d_{f2}$):**
    $$ d_{f2} = \frac{2 \times (0.5 \text{ m})^2}{0.167 \text{ m}} = \frac{0.5}{0.167} = \bf{3.0 \text{ meters}} $$

**Comment on the Result:**
The far-field distance is inversely proportional to the wavelength ($\\lambda$). As the frequency of operation increases (from 900 MHz to 1800 MHz), the wavelength decreases. Consequently, the far-field distance increases (from 1.5m to 3.0m). This means that for higher frequency signals, one must be further away from the antenna to be in the far-field region where reliable measurements can be made.

---

### Q2. An isotropic radiator is supplied with a 110W power, and the transmitter gain is 5dB. Calculate EIRP and the power density at a distance of 9km from the transmitter using FRIIS transmission formular. (CO4, RBT Level 3, 5 Marks)

**Introduction**
This problem requires calculating the Effective Isotropic Radiated Power (EIRP) and then using it to find the power density at a specified distance.

**Given:**
*   Transmitter Power ($P_t$) = 110 W
*   Transmitter Gain ($G_t$) = 5 dB
*   Distance (d) = 9 km = 9000 m

**Step 1: Convert Transmitter Gain from dB to a linear value.**
$$ G_{t,linear} = 10^{(G_{t,dB}/10)} = 10^{(5/10)} = 10^{0.5} \approx 3.162 $$

**Step 2: Calculate EIRP.**
EIRP is the product of the transmitter power and the antenna gain.
$$ EIRP = P_t \times G_{t,linear} $$
$$ EIRP = 110 \text{ W} \times 3.162 = \bf{347.82 \text{ W}} $$

**Step 3: Calculate Power Density ($P_D$).**
Power density is the EIRP spread over the surface area of a sphere with radius `d`.
$$ P_D = \frac{EIRP}{4\pi d^2} $$
$$ P_D = \frac{347.82 \text{ W}}{4\pi (9000 \text{ m})^2} = \frac{347.82}{4\pi (81 \times 10^6)} \approx \frac{347.82}{1.018 \times 10^9} $$
$$ P_D \approx 3.417 \times 10^{-7} \text{ W/m}^2 = \bf{0.3417 \text{ µW/m}^2} $$

**Conclusion:**
The EIRP is 347.82 W, and the power density at 9 km is approximately 0.3417 µW/m².

---

### Q3(a). If a transmitter produces 50 watts of power... find the received power in dBm... (CO4, RBT Level 4, 10 Marks)

This question is identical to Q11(b) from FAT03. The solution is as follows:

**1. Express Transmit Power in dBm and dBW**
*   $P_t = 50$ W.
*   $P_{t,dBW} = 10 \log_{10}(50) \approx \bf{17 \text{ dBW}}$
*   $P_{t,dBm} = 10 \log_{10}(50000) \approx \bf{47 \text{ dBm}}$

**2. Find Received Power ($P_r$) at 100m**
*   **Given:** $P_{t,dBm} = 47$ dBm, $G_t = G_r = 0$ dBi, $d = 0.1$ km, $f = 900$ MHz.
*   **FSPL(100m):** $32.44 + 20\log_{10}(0.1) + 20\log_{10}(900) = 32.44 - 20 + 59.08 = 71.52$ dB.
*   **$P_r(100\text{m}):** $47 - 71.52 = \bf{-24.52 \text{ dBm}}$.

**3. Find Received Power ($P_r$) at 10 km**
*   **FSPL(10km):** $32.44 + 20\log_{10}(10) + 20\log_{10}(900) = 32.44 + 20 + 59.08 = 111.52$ dB.
*   **$P_r(10\text{km}):** $47 - 111.52 = \bf{-64.52 \text{ dBm}}$.

**4. Calculate Received Power at 1 km using Pr(10km)**
The free space path loss increases by 20 dB for every tenfold increase in distance. Conversely, it decreases by 20 dB for every tenfold decrease in distance. The distance from 10 km to 1 km is a tenfold decrease.
$$ P_r(1\text{km}) = P_r(10\text{km}) + 20 \log_{10}\left(\frac{10\text{km}}{1\text{km}}\right) $$
$$ P_r(1\text{km}) = -64.52 \text{ dBm} + 20 \log_{10}(10) = -64.52 + 20 = \bf{-44.52 \text{ dBm}} $$

---

### Q4. If the transmitter power is 1W and carrier frequency is 2.4 GHz... Determine the received power in dBm in the free space of a signal, the path loss in dB. (CO4, RBT Level 4, 5 Marks)

**Introduction**
This problem requires calculating the free space path loss (FSPL) and the received power using the Friis transmission equation.

**Given:**
*   Transmitter Power ($P_t$) = 1 W
*   Carrier Frequency (f) = 2.4 GHz = 2400 MHz
*   Distance (d) = 1 mile = 1.6 km
*   Antenna Gains ($G_t = G_r$) = 1.6 (linear)

**Step 1: Convert Power and Gain to dB units.**
*   $P_{t,dBm} = 10 \log_{10}(1000 \text{ mW}) = \bf{30 \text{ dBm}}$
*   $G_{t,dBi} = G_{r,dBi} = 10 \log_{10}(1.6) \approx \bf{2.04 \text{ dBi}}$

**Step 2: Calculate the Free Space Path Loss (FSPL).**
$$ FSPL_{dB} = 32.44 + 20 \log_{10}(d_{km}) + 20 \log_{10}(f_{MHz}) $$
$$ FSPL_{dB} = 32.44 + 20 \log_{10}(1.6) + 20 \log_{10}(2400) $$
$$ FSPL_{dB} = 32.44 + 20(0.204) + 20(3.38) = 32.44 + 4.08 + 67.6 = \bf{104.12 \text{ dB}} $$

**Step 3: Determine the Received Power in dBm.**
$$ P_{r,dBm} = P_{t,dBm} + G_{t,dBi} + G_{r,dBi} - FSPL_{dB} $$
$$ P_{r,dBm} = 30 + 2.04 + 2.04 - 104.12 = 34.08 - 104.12 = \bf{-70.04 \text{ dBm}} $$

**Conclusion:**
The path loss is **104.12 dB**, and the received power is **-70.04 dBm**.

---

### Q5. Compare diversity techniques. (CO5, RBT Level 4, 10 Marks)

This question is identical to Q13(a) from FAT03. The solution is as follows:

**Introduction:**
Diversity is a powerful set of techniques used in wireless communication to combat the effects of multipath fading. The fundamental principle is to provide the receiver with multiple independent (uncorrelated) versions of the same transmitted signal.

**Comparison of Diversity Techniques**

| Technique             | Principle                               | Mechanism                                                              | Pros                               | Cons                               |
| :-------------------- | :-------------------------------------- | :--------------------------------------------------------------------- | :--------------------------------- | :--------------------------------- |
| **Space Diversity**   | Use multiple antennas separated in space. | Each antenna receives a signal from a different multipath environment. | Spectrally efficient, widely used. | Requires physical space, extra hardware. |
| **Frequency Diversity**| Transmit on multiple frequencies.       | Frequencies are separated by more than the coherence bandwidth.        | Effective against fading.          | **Spectrally inefficient**, costly. |
| **Time Diversity**    | Transmit at different times.            | Time separation is greater than the channel's coherence time.          | Effective, enables error correction. | Introduces latency, reduces throughput. |
| **Polarization Diversity**| Use antennas with orthogonal polarizations. | Captures signal energy from different polarizations after scattering. | Compact (no separation needed).    | Diversity gain is typically less than space diversity. |

**Conclusion:**
Each diversity technique offers a way to create independent signal branches to fight fading. The choice of which to use involves a critical trade-off between performance, spectral efficiency, cost, and latency. In modern systems, space diversity (in the form of MIMO) is the dominant technique.

---

### Q6. Compare diversity combining techniques. (CO5, RBT Level 4, 10 Marks)

This question is identical to Q13(b) from FAT03. The solution is as follows:

**Introduction:**
Once a receiver obtains multiple signal branches, it must process them to create a single, more reliable output. This is done by combining techniques, which vary in performance and complexity.

**Comparison of Diversity Combining Techniques**

| Technique         | Mechanism                                                              | Complexity | Performance (Output SNR) |
| :---------------- | :--------------------------------------------------------------------- | :--------- | :----------------------- |
| **Switched**      | Stays with one antenna until quality drops below a threshold, then switches. | Very Low   | Fair                     |
| **Selection (SC)**| Monitors all branches and always selects the one with the best SNR.     | Low        | Good                     |
| **Equal Gain (EGC)**| Co-phases all signals and sums them with equal weight.                 | Medium     | Very Good                |
| **Maximal Ratio (MRC)**| Co-phases all signals and sums them, weighted by their individual SNR. | **High**   | **Best (Optimal)**       |

**Conclusion:**
The choice of combining technique represents a classic engineering trade-off. MRC provides the best possible performance for improving link reliability, but its high complexity means that simpler methods like EGC or SC are often used in practice where cost and power consumption are major constraints.

---

### Q7. How do RAKE receiver work as time diversity in CDMA receivers. (CO5, RBT Level 4, 5 Marks)

**Introduction**
A RAKE receiver is a specialized receiver used in CDMA systems to combat multipath fading. It works by resolving and combining individual multipath components, which is a form of diversity.

**Mechanism:**
1.  **Multipath as Time-Delayed Signals:** In a multipath environment, the transmitted signal arrives at the receiver via multiple paths, each with a different propagation delay. This means the receiver sees multiple time-delayed versions of the same signal.
2.  **RAKE Receiver Structure:** A RAKE receiver consists of multiple "fingers." Each finger is a correlator that can be synchronized to a specific time delay.
3.  **Resolving Multipath:** The receiver's searcher circuitry identifies the strongest multipath components and assigns a finger to each one. Each finger then despreads its assigned multipath component.
4.  **Combining:** The outputs of all the fingers are then co-phased and combined (typically using Maximal Ratio Combining).

**RAKE as Time Diversity:**
The RAKE receiver provides diversity by treating the time-delayed multipath components as independently faded versions of the same signal.
*   A standard receiver would see these delayed signals as self-interference.
*   The RAKE receiver, however, turns this problem into a solution. By collecting the energy from signals that arrive at **different times**, it is essentially performing **time diversity**.
*   It is highly unlikely that all multipath components will fade simultaneously. By combining them, the RAKE receiver ensures that even if one path is in a deep fade, the energy from other paths (arriving at different times) is still captured, resulting in a robust and reliable final signal.

```ascii
Received Signal
      |
      +-----> Finger 1 (Correlator for Path 1, delay t1) --->|
      |                                                      |
      +-----> Finger 2 (Correlator for Path 2, delay t2) --->| Combiner
      |                                                      | (MRC) --> Output
      +-----> Finger 3 (Correlator for Path 3, delay t3) --->|
      .
      .
```

**Conclusion:**
The RAKE receiver cleverly exploits the time-of-arrival differences inherent in a multipath channel. By resolving and combining these time-delayed signals, it effectively implements a form of time diversity, making CDMA systems exceptionally robust against small-scale fading.
