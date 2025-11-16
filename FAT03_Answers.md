---
title: FAT03 Answer Key - OE22708 Fundamentals of Wireless Communication
id: fat03-answers
tags: 
  - exam
  - answers
  - unit4
  - unit5
alias: 
  - FAT3 Answers
links: 
  - "[[OE-FAT03.md|FAT03 Question Paper]]"
---

# FAT03 Answer Key: OE22708 - Fundamentals of Wireless Communication

This document provides detailed answers for the FAT03 Question Paper, covering topics from Unit IV (Mobile Radio Propagation) and Unit V (Diversity Techniques).

## PART A (10 x 2 = 20 Marks)

### Q1. Illustrate large scale fading and small scale fading. (CO4, RBT Level 4)

*   **Large-Scale Fading:** Describes the average signal strength reduction over large distances (hundreds or thousands of meters). It is caused by distance-dependent path loss and shadowing from large obstacles like buildings and hills.
*   **Small-Scale Fading:** Describes the rapid fluctuations in signal strength over very short distances (a few wavelengths) or short periods. It is caused by the constructive and destructive interference of multiple signal paths (multipath).

```
      ^ Signal Strength (dB)
      |
      |   / \
        / \
      |  /   \      /   V   \
      | /     \    /         \   /
      |/_______"__\___________"______> Distance
      |         \
      +----------\---------------------
                 Small-Scale Fading (Rapid Fluctuations)
```
*ASCII Illustration: The signal strength slowly decreases due to large-scale path loss, while fluctuating rapidly due to small-scale fading.*

### Q2. What do you mean by EIRP? (CO4, RBT Level 2)

**EIRP** stands for **Effective Isotropic Radiated Power**. It is a measure of the total power that would have to be radiated by a hypothetical isotropic antenna (one that radiates uniformly in all directions) to produce the same power density observed in the direction of the actual antenna's maximum gain.

It is calculated as:
*   **Formula (Linear):** $$ EIRP = P_t \times G_t $$
*   **Formula (dB):** $$ EIRP_{dBW} = P_{t, dBW} + G_{t, dBi} $$

Where `P_t` is the transmitter power and `G_t` is the transmit antenna gain.

### Q3. Calculate the far-field distance for a Base station antenna with largest dimension D=0.5m and frequency of operation fc=900MHz. (CO4, RBT Level 3)

The far-field, or Fraunhofer distance ($d_f$), is the distance beyond which the antenna's radiation pattern is independent of the distance.

1.  **Given:**
    *   Largest dimension of the antenna, D = 0.5 m
    *   Frequency, f = 900 MHz = $900 \times 10^6$ Hz

2.  **Calculate Wavelength (\lambda):**
    *   $\lambda = c / f$, where $c$ is the speed of light ($3 \times 10^8$ m/s).
    *   $\lambda = (3 \times 10^8 \text{ m/s}) / (900 \times 10^6 \text{ Hz}) = 1/3 \text{ m} \approx 0.333$ m.

3.  **Calculate Far-Field Distance ($d_f$):**
    *   The formula is $d_f = \frac{2D^2}{\lambda}$.
    *   $d_f = \frac{2 \times (0.5 \text{ m})^2}{0.333 \text{ m}} = \frac{2 \times 0.25}{0.333} = \frac{0.5}{0.333} \approx 1.5$ meters.

The far-field distance for this antenna is approximately **1.5 meters**.

### Q4. Describe the factors that contribute to the rapid fluctuations of the signal amplitude? (CO4, RBT Level 2)

The rapid fluctuations of signal amplitude (small-scale fading) are primarily caused by:
1.  **Multipath Propagation:** The signal arrives at the receiver via multiple paths due to reflection, diffraction, and scattering. These multiple versions interfere constructively or destructively.
2.  **Motion of the Receiver:** As the receiver moves, the lengths of the multiple paths change, causing the phase relationships to shift rapidly and leading to fast fading.
3.  **Motion of Objects:** Moving objects (like vehicles or people) in the radio path alter the multipath environment, causing the received signal to fluctuate.
4.  **Speed of the Mobile:** The rate of signal fluctuation is directly proportional to the speed of the mobile, a phenomenon related to Doppler shift.

### Q5. Outline the necessity of diversity techniques. (CO5, RBT Level 2)

Diversity techniques are necessary to **combat the effects of multipath fading**.
*   Fading can cause the received signal power to drop by 20-30 dB, leading to high bit error rates and dropped calls.
*   Instead of inefficiently increasing transmitter power to overcome the deepest fades, diversity provides the receiver with multiple independent versions of the signal.
*   Since it is highly improbable that all versions will fade simultaneously, the receiver can select or combine them to achieve a reliable, high-quality connection.

### Q6. Differentiate between macro and micro diversity. (CO5, RBT Level 4)

| Feature           | Macro-diversity                                      | Micro-diversity                                       |
| :---------------- | :--------------------------------------------------- | :---------------------------------------------------- |
| **Purpose**       | To combat large-scale fading (shadowing).            | To combat small-scale fading (multipath).             |
| **Antenna Placement** | Antennas are at different base station sites, separated by large distances (hundreds of meters to kilometers). | Antennas are at the same receiver/transmitter location, separated by small distances (a few wavelengths). |
| **Example**       | CDMA soft handoff, where a mobile communicates with two or more cells simultaneously. | Having multiple antennas on a Wi-Fi router or a cellular base station to serve a single user. |

### Q7. List the 4 categories of space diversity reception methods. (CO5, RBT Level 2)

The four main categories of space diversity reception (processing) methods are:
1.  **Selection Combining (SC)**
2.  **Switched / Feedback Diversity**
3.  **Equal Gain Combining (EGC)**
4.  **Maximal Ratio Combining (MRC)**

### Q8. Identify the demerits of frequency diversity. (CO5, RBT Level 3)

The primary demerits of frequency diversity are:
1.  **Spectral Inefficiency:** It is the main drawback. Using multiple frequency channels to transmit the same information is a wasteful use of the limited and valuable radio spectrum.
2.  **Increased Cost and Complexity:** It requires multiple transmitters and receivers, each operating on a different frequency, which increases the cost and hardware complexity of the system.

### Q9. Give an example of time diversity receiver used in cellular communication systems. (CO5, RBT Level 4)

A practical and widely used example of a time diversity receiver is one that employs **channel coding with interleaving**.
*   In GSM and LTE systems, data bits are first encoded with an error-correction code. Then, the coded bits are "shuffled" or interleaved across different time slots.
*   The receiver performs the reverse process (de-interleaving). If a deep fade causes a burst of errors in one time slot, de-interleaving spreads these errors out. The error-correction decoder can then easily fix these scattered individual errors.

### Q10. Mention the strategies used in diversity techniques. (CO5, RBT Level 2)

The strategies used in diversity techniques refer to the different domains in which multiple signal paths can be created:
1.  **Space Diversity:** Using antennas separated in space.
2.  **Frequency Diversity:** Using different carrier frequencies.
3.  **Time Diversity:** Re-transmitting at different points in time.
4.  **Polarization Diversity:** Using antennas with different polarizations (e.g., vertical and horizontal).

---

## PART B (3 x 10 = 30 Marks)

### Q11(a). Derive the equation for path loss using the free space model and analyze the assumptions and limitations of the free space propagation model. (CO4, RBT Level 3)

**Derivation of the Free Space Path Loss (FSPL) Equation**

1.  **Start with Isotropic Power Density:** Assume an isotropic transmitter radiates power `P_t` uniformly in all directions. At a distance `d`, this power is spread over the surface of a sphere with area $4\pi d^2$. The power density ($P_D$) at this distance is:
    $$ P_D = \frac{P_t}{4\pi d^2} $$

2.  **Introduce Receiver Antenna Aperture:** A receiver antenna captures power from this wave over its **effective aperture**, $A_e$. The received power, $P_r$, is:
    $$ P_r = P_D \times A_e = \frac{P_t A_e}{4\pi d^2} $$

3.  **Relate Aperture to Gain:** The effective aperture of any antenna is related to its gain, $G_r$, and the signal's wavelength, $\lambda$: 
    $$ A_e = \frac{G_r \lambda^2}{4\pi} $$

4.  **Substitute and Form Friis Equation:** Substitute the expression for $A_e$ into the received power equation. If the transmitter also has a gain $G_t$, the equation becomes:
    $$ P_r = \frac{P_t G_t}{4\pi d^2} \times \frac{G_r \lambda^2}{4\pi} = P_t G_t G_r \left( \frac{\lambda}{4\pi d} \right)^2 $$
    This is the Friis Free Space Equation.

5.  **Derive Path Loss:** Path Loss (PL) is the ratio of transmitted power to received power, assuming unity gain antennas ($G_t = G_r = 1$).
    $$ PL = \frac{P_t}{P_r} = \frac{1}{(\lambda / 4\pi d)^2} = \left( \frac{4\pi d}{\lambda} \right)^2 $$
    Since $\lambda = c/f$ (where c is speed of light, f is frequency), we can write:
    $$ PL = \left( \frac{4\pi d f}{c} \right)^2 $$
    This is the equation for path loss in linear units. In decibels (dB), this becomes:
    $$ PL_{dB} = 10 \log_{10} \left( \frac{4\pi d f}{c} \right)^2 = 20 \log_{10}(d) + 20 \log_{10}(f) + 20 \log_{10}\left( \frac{4\pi}{c} \right) $$

---

**Analysis of Assumptions and Limitations**

**Assumptions:**
1.  **Unobstructed Line-of-Sight (LOS):** The model assumes a perfect, clear, and direct path between the transmitter and receiver.
2.  **Far-Field Propagation:** It assumes the receiver is in the far-field of the transmitter, where the wave is planar.
3.  **No Environmental Effects:** The model ignores all environmental interactions, including reflection, diffraction, scattering, and absorption from buildings, terrain, or foliage.
4.  **No Atmospheric Effects:** It assumes propagation in a vacuum, ignoring attenuation from atmospheric gases or rain.

**Limitations:**
1.  **Unrealistic for Terrestrial Systems:** Most mobile communication occurs in cluttered environments (urban, suburban) where LOS is often blocked and multipath is dominant. The model is therefore highly inaccurate for predicting real-world path loss in these scenarios.
2.  **Overly Optimistic:** Because it ignores all sources of attenuation other than distance, the Free Space Model always predicts the minimum possible path loss. Actual path loss is almost always higher.
3.  **Does Not Account for Multipath Fading:** It is a large-scale model and cannot predict the rapid signal fluctuations (small-scale fading) caused by multipath interference, which are critical for system performance.

**Conclusion:** The Free Space Propagation Model is a fundamental theoretical tool for understanding the basics of signal attenuation but is too simplistic for practical cellular network planning, which requires more complex empirical or statistical models.

### Q11(b). If a transmitter produces 50 watts of power... find the received power in dBm...

**1. Express Transmit Power in dBm and dBW**
*   Given Transmit Power, $P_t = 50$ W.

**(a) Power in dBW:**
$$ P_{t,dBW} = 10 \log_{10} \left( \frac{50 \text{ W}}{1 \text{ W}} \right) = 10 \log_{10}(50) \approx 10 \times 1.699 = 16.99 \text{ dBW} \approx \bf{17 \text{ dBW}} $$

**(b) Power in dBm:**
$$ P_{t,dBm} = 10 \log_{10} \left( \frac{50 \text{ W}}{1 \text{ mW}} \right) = 10 \log_{10} (50000) \approx 10 \times 4.699 = 46.99 \text{ dBm} \approx \bf{47 \text{ dBm}}
$$ (Alternatively: $P_{dBm} = P_{dBW} + 30 = 17 + 30 = 47$ dBm)

---

**2. Find Received Power ($P_r$) at 100m**
*   Formula: $P_{r,dBm} = P_{t,dBm} + G_{t,dBi} + G_{r,dBi} - FSPL_{dB}$
*   **Given:**
    *   $P_{t,dBm} = 47$ dBm
    *   $G_t = G_r = 1$ (Unity Gain) $\implies 0$ dBi
    *   Distance, $d = 100$ m = 0.1 km
    *   Frequency, $f = 900$ MHz

*   **Calculate Free Space Path Loss (FSPL) at 100m:**
    $$ FSPL_{dB} = 32.44 + 20 \log_{10}(d_{km}) + 20 \log_{10}(f_{MHz}) $$
    $$ FSPL_{dB} = 32.44 + 20 \log_{10}(0.1) + 20 \log_{10}(900) $$
    $$ FSPL_{dB} = 32.44 + 20(-1) + 20(2.954) = 32.44 - 20 + 59.08 = 71.52 \text{ dB} $$

*   **Calculate Received Power at 100m:**
    $$ P_r(100\text{m}) = 47 + 0 + 0 - 71.52 = \bf{-24.52 \text{ dBm}} $$

---

**3. Find Received Power ($P_r$) at 10 km**
*   **Calculate FSPL at 10 km:**
    $$ FSPL_{dB} = 32.44 + 20 \log_{10}(10) + 20 \log_{10}(900) $$
    $$ FSPL_{dB} = 32.44 + 20(1) + 59.08 = 111.52 \text{ dB} $$
*   **Calculate Received Power at 10 km:**
    $$ P_r(10\text{km}) = 47 - 111.52 = \bf{-64.52 \text{ dBm}} $$

---

**4. Analyze Power at 1 km**
*   **Calculate FSPL at 1 km:**
    $$ FSPL_{dB} = 32.44 + 20 \log_{10}(1) + 20 \log_{10}(900) $$
    $$ FSPL_{dB} = 32.44 + 20(0) + 59.08 = 91.52 \text{ dB} $$
*   **Calculate Received Power at 1 km:**
    $$ P_r(1\text{km}) = 47 - 91.52 = \bf{-44.52 \text{ dBm}} $$

**Analysis:**
The received power decreases significantly with distance. At 100m, the power is -24.52 dBm. At 1km (10 times the distance), the power is -44.52 dBm, a drop of 20 dB. At 10km (100 times the distance), the power is -64.52 dBm, a drop of 40 dB from the 100m reading. This follows the free space model, where every tenfold increase in distance results in a 20 dB increase in path loss ($20 \log_{10}(10) = 20$ dB).

### Q12(a). Explain the propagation mechanisms which impact propagation in mobile radio communication system. (CO4, RBT Level 2)

**Introduction**
In a mobile radio system, the signal rarely travels in a direct line from transmitter to receiver. Instead, it interacts with the surrounding environment through three fundamental propagation mechanisms: **Reflection, Diffraction, and Scattering**. These mechanisms create multiple signal paths, collectively known as **multipath**.

**1. Reflection**
*   **Definition:** Reflection occurs when a radio wave impinges on a surface that is large and smooth relative to the signal's wavelength. The wave bounces off the surface, changing its direction.
*   **Examples:** The ground, large building walls, bodies of water.
*   **Impact:** Creates strong, discrete multipath components. A well-known model that uses this is the two-ray ground reflection model, which considers both a direct LOS path and a ground-reflected path.

```ascii
      Tx ------ Direct Path ------> Rx
      | \
      |  \                       /
      |   \                     /
      +----\------------------/--
           \                   /
            \ Reflected Path  /
             \               /
      ========(Ground/Building)========
```

**2. Diffraction**
*   **Definition:** Diffraction occurs when the radio path between the transmitter and receiver is obstructed by an object with sharp, irregular edges. The waves bend around the edges of the obstacle, propagating into its shadow region.
*   **Examples:** Bending over a hilltop, around the corner of a building.
*   **Impact:** Enables communication even when there is no direct line-of-sight (NLOS). The strength of the diffracted signal depends on the geometry of the obstacle and the signal's frequency.

```ascii
      Tx
       \
        \           /-------
         \         / Obstacle
          \       / (e.g., Hill)
           \     /
            +---+
                 \
                  \ Diffracted Path
                   \
                    --> Rx
```

**3. Scattering**
*   **Definition:** Scattering occurs when a radio wave hits an object or a surface with dimensions that are small compared to the signal's wavelength, or a surface that is rough. The incoming energy is radiated in many directions.
*   **Examples:** Foliage (trees), street signs, lampposts, rough walls.
*   **Impact:** Creates a large number of weaker, diffuse multipath components. Scattering is what often allows a signal to be received deep within buildings or in cluttered urban environments where direct and reflected paths are blocked.

```ascii
       \ | /
Tx ----- (Object) ----- Many scattered paths
       / | \
```
**Conclusion:**
In a real mobile communication system, all three mechanisms occur simultaneously. The received signal is the vector sum of all the direct, reflected, diffracted, and scattered components. This combination leads to the phenomenon of multipath fading, which is a primary challenge in wireless system design.

### Q12(b). Demonstrate small scale fading, its causes, types and give an example scenario. (CO4, RBT Level 2)

**Demonstration of Small-Scale Fading**
Small-scale fading (or multipath fading) refers to the rapid and dramatic fluctuations in the amplitude and phase of a radio signal over a very short travel distance (a few wavelengths) or a short period of time. A receiver moving just a few inches can go from a strong signal to a "dead spot" and back again.

**Causes of Small-Scale Fading**
The primary cause is **multipath propagation**.
1.  Signals from a transmitter travel to a receiver via multiple paths due to reflection, diffraction, and scattering from objects in the environment.
2.  Each path has a different length, resulting in multiple versions of the signal arriving at the receiver at slightly different times and with different phases.
3.  At the receiver's antenna, these signals combine.
    *   **Constructive Interference:** If the signals arrive in-phase, they add up, resulting in a stronger signal.
    *   **Destructive Interference:** If the signals arrive out-of-phase, they cancel each other out, resulting in a deep fade or signal drop.

**Types of Small-Scale Fading**
Small-scale fading can be classified based on its effect on the signal:
1.  **Fading based on Multipath Time Delay Spread (Frequency Effects):**
    *   **Flat Fading:** Occurs if the channel's coherence bandwidth is *larger* than the signal's bandwidth. All frequency components of the signal experience the same fading.
    *   **Frequency-Selective Fading:** Occurs if the channel's coherence bandwidth is *smaller* than the signal's bandwidth. Different frequency components of the signal experience different levels of fading, causing signal distortion. This leads to Inter-Symbol Interference (ISI).
2.  **Fading based on Doppler Spread (Time Effects):**
    *   **Fast Fading:** Occurs if the coherence time of the channel is *shorter* than the symbol period of the signal. The channel changes rapidly *within* a single symbol's duration.
    *   **Slow Fading:** Occurs if the coherence time of the channel is *longer* than the symbol period. The channel is static over one or more symbol durations.

**Example Scenario**
*   **Scenario:** You are using your mobile phone while walking down a dense city street.
*   **Demonstration:** As you walk, the voice quality of your call fluctuates, and you might hear brief moments of static or silence. If you were watching a video, it might freeze and buffer intermittently.
*   **Explanation:** Your phone is receiving signals that are reflecting off buildings, scattering off street signs, and diffracting around corners. As you move, the paths of these signals change. In one spot, the signals add up constructively, giving you clear audio. A few steps later, they cancel destructively, causing a deep fade and a momentary loss of signal, which your brain perceives as a "dead spot" or glitch in the audio.

### Q13(a). Examine diversity techniques. (CO5, RBT Level 4)

**Examination of Diversity Techniques**

**Introduction:**
Diversity is a powerful set of techniques used in wireless communication to combat the effects of multipath fading. The fundamental principle is to provide the receiver with multiple independent (uncorrelated) versions of the same transmitted signal. The statistical probability of all versions being in a deep fade at the same time is extremely low, thus ensuring a more reliable link.

**1. Space Diversity**
*   **Principle:** Uses multiple antennas separated in space, either at the transmitter, receiver, or both. For the fading to be independent, the antennas must be separated by at least a few wavelengths.
*   **Mechanism:** Each antenna receives a signal that has traveled through a slightly different multipath environment.
*   **Examination:** This is the most practical and widely used form of diversity because it is **spectrally efficient** (it does not require extra bandwidth). Its main cost is in the hardware for extra antennas and receiver chains. It is the basis for modern MIMO systems.

**2. Frequency Diversity**
*   **Principle:** Transmits the same information simultaneously on multiple frequency carriers.
*   **Mechanism:** The carriers are separated by more than the channel's coherence bandwidth, ensuring that the fading on each frequency channel is independent.
*   **Examination:** While effective, this technique is highly **spectrally inefficient** as it consumes multiple channels for a single user's information. Due to the scarcity and cost of radio spectrum, it is rarely used in modern cellular systems.

**3. Time Diversity**
*   **Principle:** Transmits the same information at different points in time.
*   **Mechanism:** The time separation between transmissions must be greater than the channel's coherence time. This ensures the channel has changed and the fading is independent for each transmission.
*   **Examination:** This technique has the drawback of introducing **latency** and reducing throughput, as data must be buffered and/or retransmitted. However, a very practical and efficient form is **channel coding with interleaving**, which shuffles coded bits over time to spread out burst errors, allowing for their correction without the high latency of full retransmissions.

**4. Polarization Diversity**
*   **Principle:** Uses two co-located antennas with orthogonal polarizations (e.g., vertical and horizontal).
*   **Mechanism:** Reflections and scattering in the environment can change the polarization of a signal. Using two polarizations allows the receiver to capture energy that might be missed by a single-polarization antenna.
*   **Examination:** The key advantage is its **compactness**, as the antennas do not need to be physically separated. This makes it ideal for base stations with limited tower space or for small mobile devices. Its diversity gain is typically less than well-implemented space diversity, but it is a very practical compromise.

**Conclusion:**
Each diversity technique offers a way to create independent signal branches to fight fading. The choice of which to use involves a critical trade-off between performance (diversity gain), spectral efficiency, cost/complexity, and latency. In modern systems, space diversity is the dominant technique.

### Q13(b). Inspect diversity combining techniques. (CO5, RBT Level 4)

**Inspection of Diversity Combining Techniques**

**Introduction:**
Once a receiver obtains multiple, independently faded signal branches through a diversity scheme (like space diversity), it must process them to create a single, more reliable output. This processing is done by combining or selection techniques, which vary in performance and complexity.

**1. Selection Combining (SC)**
*   **Mechanism:** The receiver circuitry continuously monitors the Signal-to-Noise Ratio (SNR) of all `M` diversity branches. It then selects the single branch with the highest instantaneous SNR and feeds only that signal to the demodulator. All other branches are ignored.
*   **Inspection:** This is the simplest combiner to implement. It only requires one full receiver chain, as it just switches the input to the demodulator. However, its performance is limited because it discards the signal energy present in the other `M-1` branches.

**2. Switched Diversity**
*   **Mechanism:** This is a simpler, lower-cost version of SC. The receiver stays with one antenna until its signal quality drops below a predefined threshold. Only then does it switch to another antenna and checks its quality. It continues switching until it finds an acceptable signal.
*   **Inspection:** This is the cheapest method but offers the worst performance, as it is not guaranteed to be on the *best* branch, only the first *acceptable* one it finds. It is suitable for very low-cost applications.

**3. Equal Gain Combining (EGC)**
*   **Mechanism:** The signals from all `M` branches are first co-phased (their phases are aligned). Then, they are all summed together with equal weighting (i.e., they are simply added up).
*   **Inspection:** EGC is significantly more effective than SC because it uses the energy from all branches. Its performance is very close to the optimal method (MRC). Its complexity is higher than SC because it requires circuitry to estimate and correct the phase of each signal, but it is simpler than MRC because it doesn't need to estimate signal amplitudes.

**4. Maximal Ratio Combining (MRC)**
*   **Mechanism:** MRC is the optimal linear combining technique. Like EGC, it co-phases the signals from all `M` branches. However, before summing them, it weights each signal proportionally to its individual SNR. Strong, clean signals are given high weight, and weak, noisy signals are given low weight.
*   **Inspection:** This method yields the highest possible output SNR because it intelligently combines the signals to maximize the contribution of strong branches while minimizing the noise from weak ones. It is the most complex method, as it requires a dedicated receiver chain for each antenna to estimate both the **phase** and the **amplitude (for SNR weighting)** of each signal.

**Comparison Summary**

| Technique         | Complexity | Performance (Output SNR) | Key Requirement                                   |
| :---------------- | :--------- | :----------------------- | :------------------------------------------------ |
| Switched Diversity| Very Low   | Fair                     | Signal quality threshold detection.               |
| Selection Combining| Low        | Good                     | SNR estimation on all branches.                   |
| Equal Gain Combining| Medium     | Very Good                | Phase estimation on all branches.                 |
| **MRC**           | **High**   | **Best (Optimal)**       | **Phase and Amplitude/SNR estimation on all branches.** |

**Conclusion:**
The choice of combining technique represents a classic engineering trade-off. MRC provides the best possible performance for improving link reliability, but its high complexity means that simpler methods like EGC or even SC are often used in practice where cost and power consumption are major constraints.