---
title: "Unit V Assessment: Diversity Techniques"
id: "unit5-assessment"
tags: ["#assessment", "#unit5", "#quiz", "#exam_prep"]
aliases: ["Unit 5 Questions", "Diversity Quiz"]
links: [[FOWC/25_Unit5_Topic01_Intro_Diversity.md], [FOWC/26_Unit5_Topic02_SpaceDiversity_Combining.md], [FOWC/27_Unit5_Topic03_Other_Diversity_Types.md]]
---

# UNIT V Assessment: Diversity Techniques

This assessment covers the key concepts from Unit V, including the principles of diversity, space diversity, combining methods (SC, MRC, EGC), and other diversity types like polarization, frequency, and time diversity.

---

## 1. Quiz Questions (Multiple Choice/Short Answer)

1.  What is the fundamental purpose of using diversity techniques in wireless communication?
2.  Which diversity combining technique is considered optimal as it provides the highest possible output SNR?
    a) Selection Combining (SC)
    b) Equal Gain Combining (EGC)
    c) Switched Diversity
    d) Maximal Ratio Combining (MRC)
3.  Which form of diversity is the most spectrally inefficient because it requires sending the same information on multiple carriers?
4.  For space diversity to be effective, the separation between antennas should be at least a few __________.
5.  Which combining technique is the simplest to implement as it only requires one receiver chain and selects the single best signal branch?
6.  Time diversity techniques rely on the time separation between transmissions being greater than the channel's __________.
7.  Which diversity technique uses two co-located antennas with orthogonal orientations (e.g., vertical and horizontal)?
8.  In Maximal Ratio Combining (MRC), each signal branch is weighted according to its ________ before being summed.
9.  The process of shuffling coded data bits before transmission to spread out burst errors is a practical application of which diversity type?
10. Which low-cost diversity method involves staying with one antenna until the signal quality drops below a certain threshold before switching to another?

---

## 2. Reasoning Questions

1.  Explain the core principle of diversity. Why is it highly improbable for all diversity branches to experience a deep fade simultaneously?
2.  Compare and contrast Maximal Ratio Combining (MRC) and Equal Gain Combining (EGC). Why is MRC considered optimal, and what is the practical advantage of using EGC?
3.  A wireless system designer has to choose between space diversity and frequency diversity. Explain why space diversity is almost always preferred in modern cellular systems.
4.  Describe how a Selection Combining (SC) receiver with two antennas works. What is its main advantage and its main limitation?
5.  Explain how channel coding combined with interleaving acts as a form of time diversity.
6.  Why is antenna separation a critical factor for the effectiveness of space diversity? What happens if the antennas are too close together?
7.  A mobile phone needs to implement diversity but has very limited physical space. Which two diversity techniques would be most suitable for this compact application and why?
8.  Explain the trade-off between performance and complexity across the four main space diversity processing techniques (Switched, SC, EGC, MRC).
9.  If a wireless channel is characterized by very slow fading (long coherence time), how does this impact the effectiveness of time diversity?
10. A receiver uses Maximal Ratio Combining (MRC). What two pieces of information must it estimate for each diversity branch to perform the combining process correctly?

---

## 3. Real-World Happening Questions

1.  High-end Wi-Fi routers often have multiple visible antennas. What type of diversity does this primarily enable, and what is the benefit to the user?
2.  Some early paging systems would transmit the same page message from multiple towers on different frequencies. What form of diversity is this, and why was it used?
3.  You are streaming a video on your 4G phone. The data is encoded and interleaved before being sent over the air. A car passes by, causing a brief, deep fade that corrupts some of the received data. Why does your video likely not freeze or show errors?
4.  A base station is being installed on a tower with limited space for mounting antennas. The engineer decides to use a single antenna housing that contains both vertically and horizontally polarized elements. What is this technique called, and why is it a good compromise?
5.  In a 2-antenna MRC system, the signal from Antenna 1 has an SNR of 15 dB, and the signal from Antenna 2 has an SNR of 5 dB. Which signal will be given more weight in the combining process, and why is this approach better than just adding them equally?
6.  Some low-cost wireless microphones use switched diversity. You might see two small antennas on the receiver. Explain what the receiver is doing with these two antennas as the performer moves around the stage.
7.  To save money, a company decides to implement frequency diversity by buying two separate, cheap, low-bandwidth radio links instead of one expensive, high-reliability link. Under what channel conditions would this strategy be effective?
8.  MIMO (Multiple Input Multiple Output) in modern 4G/5G systems is an advanced form of space diversity. Why does having multiple antennas at *both* the transmitter and receiver provide even greater benefits than just having them at the receiver?
9.  A deep-space probe communicates with Earth over a very stable, line-of-sight path with no multipath. Would implementing diversity techniques on the probe provide any significant benefit? Why or why not?
10. A car's AM/FM radio often has its antenna embedded in the rear window as a grid of wires. Some cars use two such antennas in different windows. What is the name for this technique, and how does it help prevent audio from fading as the car drives through a city?

---

## 4. Rapid Fire Questions with Answers

1.  **Q:** What is the primary goal of diversity?
    **A:** To combat fading.
2.  **Q:** Which combining method is the most complex?
    **A:** Maximal Ratio Combining (MRC).
3.  **Q:** What type of diversity is spectrally inefficient?
    **A:** Frequency diversity.
4.  **Q:** What does SC stand for in the context of diversity?
    **A:** Selection Combining.
5.  **Q:** Does polarization diversity require antenna separation?
    **A:** No.
6.  **Q:** What must be estimated for each branch in EGC?
    **A:** The phase of the signal.
7.  **Q:** What is the simplest form of diversity combining?
    **A:** Switched or Selection Diversity.
8.  **Q:** Time diversity introduces what performance trade-off?
    **A:** Latency.
9.  **Q:** What is the optimal diversity combining technique?
    **A:** Maximal Ratio Combining (MRC).
10. **Q:** What physical property of a radio wave is used in polarization diversity?
    **A:** The orientation of its electric field.

---

## 5. Answers

### 5.1. Quiz Questions - Answers

1.  **Answer:** To combat the effects of multipath fading.
    -   **Concept:** Diversity is a fading mitigation technique.
    -   **Reasoning:** By providing the receiver with multiple, independently fading versions of the same signal, diversity dramatically reduces the probability that the signal will be lost in a deep fade, thus improving link reliability.

2.  **Answer:** d) Maximal Ratio Combining (MRC).
    -   **Concept:** MRC is the optimal linear diversity combining method.
    -   **Reasoning:** MRC maximizes the output SNR by coherently combining all signal branches, with each branch weighted by its individual SNR. This ensures that stronger signals contribute more and weaker signals contribute less, achieving the best possible performance.

3.  **Answer:** Frequency diversity.
    -   **Concept:** Frequency diversity involves sending the same information over multiple frequency channels.
    -   **Reasoning:** This approach is spectrally inefficient because it consumes more bandwidth than necessary to transmit the actual information, making it a poor use of a scarce resource.

4.  **Answer:** Wavelengths.
    -   **Concept:** The principle of antenna separation in space diversity.
    -   **Reasoning:** For the fading on different antennas to be independent (uncorrelated), the antennas must be separated by a distance of at least a few wavelengths of the carrier frequency. This ensures they are not in the same fade simultaneously.

5.  **Answer:** Selection Combining (SC).
    -   **Concept:** SC is a simple diversity processing technique.
    -   **Reasoning:** SC works by monitoring all signal branches and simply selecting the one with the highest SNR. Since it only processes one branch at a time, it requires only a single receiver chain, making it the simplest to implement after switched diversity.

6.  **Answer:** Coherence time.
    -   **Concept:** Time diversity relies on changes in the channel state over time.
    -   **Reasoning:** The coherence time is the duration for which the channel is considered stable. To ensure that retransmissions experience independent fading conditions, the time separation between them must be greater than the channel's coherence time.

7.  **Answer:** Polarization diversity.
    -   **Concept:** Polarization diversity uses antennas with different polarizations.
    -   **Reasoning:** This technique exploits the fact that reflections and scattering can change a signal's polarization. By using two co-located antennas with orthogonal polarizations (e.g., vertical and horizontal), the system can capture signal energy that might be missed by a single-polarization antenna.

8.  **Answer:** Signal-to-Noise Ratio (SNR).
    -   **Concept:** The weighting mechanism of Maximal Ratio Combining.
    -   **Reasoning:** MRC achieves its optimal performance by weighting each branch proportionally to its signal quality. Stronger, cleaner signals (higher SNR) are given more weight, while weaker, noisier signals are given less weight in the final sum.

9.  **Answer:** Time diversity.
    -   **Concept:** Interleaving is a practical implementation of time diversity.
    -   **Reasoning:** By shuffling the order of coded bits before transmission, a deep fade that corrupts a burst of consecutive bits is transformed into a series of scattered, single-bit errors after de-interleaving. These scattered errors are much easier for the error-correction decoder to fix.

10. **Answer:** Switched (or Feedback) Diversity.
    -   **Concept:** Switched diversity is a low-cost alternative to Selection Combining.
    -   **Reasoning:** Instead of constantly monitoring all branches to find the best one, switched diversity uses a simpler logic: stay with the current antenna until the quality drops below a threshold, then switch. This is easier and cheaper to implement.

### 5.2. Reasoning Questions - Answers

1.  **Answer:** Diversity provides multiple independent versions of a signal, and the probability of all versions failing simultaneously is very low.
    -   **Concept:** The statistical advantage of using multiple independent paths.
    -   **Reasoning:** Fading on different diversity branches (e.g., separated by space, time, or frequency) is largely uncorrelated. If the probability of one branch being in a deep fade is `p`, the probability of two independent branches being in a deep fade at the same time is `p^2`. For `p=0.01` (1%), the joint probability is `0.0001` (0.01%). This multiplicative effect makes simultaneous deep fades on all branches extremely unlikely.

2.  **Answer:** MRC is optimal because it weights signals by their SNR, while EGC's advantage is its lower complexity as it only needs to estimate phase.
    -   **Concept:** The trade-off between performance and complexity in coherent combining techniques.
    -   **Reasoning:** **MRC** is optimal because it maximizes the output SNR by giving more weight to cleaner signals and less weight to noisier ones. This requires estimating both the phase and amplitude of each signal. **EGC**'s advantage is its simplicity compared to MRC. It still provides excellent performance by co-phasing the signals but avoids the complexity of estimating signal amplitudes for weighting, making it easier to implement.

3.  **Answer:** Space diversity is spectrally efficient and highly effective, whereas frequency diversity is spectrally wasteful.
    -   **Concept:** The resource cost of different diversity schemes.
    -   **Reasoning:** **Space diversity** achieves its gain by using multiple antennas, which is a one-time hardware cost. It does not consume any additional radio spectrum. **Frequency diversity**, on the other hand, requires transmitting the same information on multiple frequency channels, directly consuming more of the scarce and valuable radio spectrum. In modern systems where spectral efficiency is paramount, this makes space diversity the far superior choice.

4.  **Answer:** SC monitors two antennas and selects the one with the higher SNR. Its advantage is simplicity, but its limitation is that it discards the energy from the other antenna.
    -   **Concept:** The operation and trade-offs of Selection Combining.
    -   **Reasoning:** An SC receiver with two antennas constantly measures the SNR of both. It feeds the signal from the stronger branch to the demodulator and completely ignores the signal from the weaker branch. The main **advantage** is its simplicity, as it only requires one full receiver chain. The main **limitation** is that it fails to use the potentially valuable signal energy arriving at the second antenna, thus providing less diversity gain than combining methods.

5.  **Answer:** Interleaving spreads burst errors over time, allowing the channel decoder to correct them.
    -   **Concept:** Using channel coding and interleaving to create time diversity without simple retransmission.
    -   **Reasoning:** A deep fade often causes a burst of consecutive bit errors. Error-correction codes are good at fixing random, scattered errors but poor at fixing long bursts. **Interleaving** shuffles the data bits before transmission. After reception and de-interleaving, the burst of errors is spread out into single-bit errors separated by correct bits. The error-correction decoder can then easily identify and correct these individual errors, effectively using the information from different points in time (the correct bits) to fix the faded bits.

6.  **Answer:** The antennas must be separated enough for the fading to be uncorrelated. If they are too close, they will experience the same fades, and no diversity gain is achieved.
    -   **Concept:** The requirement for independent fading in diversity systems.
    -   **Reasoning:** The core principle of diversity relies on the low probability of all branches fading simultaneously. If the antennas are too close together (typically less than half a wavelength), they are in the same local multipath environment. This means their signals will be highly correlated; when one fades, the other will also fade. In this case, there is no diversity gain because there is no "backup" strong signal to switch to.

7.  **Answer:** Polarization diversity and space diversity (with small separation).
    -   **Concept:** Applying diversity techniques within the physical constraints of a mobile device.
    -   **Reasoning:** **Polarization diversity** is ideal because it uses two co-located antennas with different polarizations (e.g., vertical and horizontal), requiring no extra physical separation. **Space diversity** can also be used if the antennas are placed at points of the device with sufficient separation and different orientation (e.g., top and bottom of the phone) to achieve a degree of pattern and spatial diversity, even if the separation is not multiple wavelengths.

8.  **Answer:** Performance increases with complexity: Switched < SC < EGC < MRC.
    -   **Concept:** The engineering trade-off between system performance and implementation cost/complexity.
    -   **Reasoning:** **Switched** is simplest (just a threshold check). **SC** is slightly more complex (needs to compare all branches). **EGC** is more complex still (needs to co-phase all signals). **MRC** is most complex (needs to co-phase *and* estimate SNR for weighting). This increase in complexity directly corresponds to an increase in performance, as more information from the diversity branches is utilized at each step.

9.  **Answer:** It would be ineffective because the channel state does not change between retransmissions.
    -   **Concept:** The requirement for a time-varying channel for time diversity to work.
    -   **Reasoning:** Time diversity relies on the channel changing between transmissions so that if the first transmission is in a deep fade, the second one is likely not. If the channel is fading very slowly (long coherence time), the channel state will be the same for both the original transmission and the retransmission. Both will be caught in the same deep fade, and no diversity gain will be achieved.

10. **Answer:** It must estimate the phase and the amplitude (or SNR) of the signal on each branch.
    -   **Concept:** The channel estimation requirements for Maximal Ratio Combining.
    -   **Reasoning:** To perform MRC, the receiver must do two things for each of the M signals: 1) Estimate the **phase** of the signal so it can be rotated and added coherently (in-phase) with the others. 2) Estimate the **amplitude** or SNR of the signal so it can be used as the weighting factor, ensuring that stronger signals contribute more to the final sum.

### 5.3. Real-World Happening Questions - Answers

1.  **Answer:** Space diversity. The benefit is a more reliable and stable Wi-Fi connection with fewer dropouts.
    -   **Concept:** The practical application of space diversity in consumer electronics.
    -   **Reasoning:** The multiple antennas on the router create multiple independent signal paths to your device. The router's chipset uses diversity combining techniques (like SC or MRC) to mitigate the effects of multipath fading caused by reflections in the office. This results in a more stable link, higher average data rates, and a reduction in "dead spots."

2.  **Answer:** This is a combination of space diversity and frequency diversity.
    -   **Concept:** Applying multiple diversity techniques for maximum reliability.
    -   **Reasoning:** Using multiple towers provides **space diversity**, as the path from each tower to the pager is different and will fade independently. Transmitting on different frequencies provides **frequency diversity**, protecting against interference or fading on a single frequency. This combined approach was used to make critical paging alerts extremely reliable.

3.  **Answer:** Due to time diversity implemented via interleaving and channel coding.
    -   **Concept:** The practical effect of time diversity on data streaming.
    -   **Reasoning:** The brief fade caused by the car corrupts a burst of data. However, because the data was interleaved (shuffled) before transmission, the receiver de-interleaves it, spreading the burst of errors into single, scattered errors. The forward error correction (FEC) code is then easily able to correct these individual errors, and the video player's buffer ensures that the corrected data is available, resulting in no noticeable freeze or glitch.

4.  **Answer:** This is called polarization diversity, and it's a good compromise because it provides diversity gain without requiring physical antenna separation.
    -   **Concept:** The use of polarization diversity to overcome physical space constraints.
    -   **Reasoning:** By using two antennas with orthogonal polarizations (vertical and horizontal) in the same physical housing, the system can get two largely uncorrelated fading paths. This provides valuable diversity gain to combat fading, which is crucial for reliability, without the need to mount two separate, bulky antenna enclosures on the crowded tower.

5.  **Answer:** The signal from Antenna 1 (15 dB SNR) will be given more weight. This is better because it prioritizes the cleaner signal.
    -   **Concept:** The weighting principle of Maximal Ratio Combining.
    -   **Reasoning:** MRC weights each branch by its SNR. A 15 dB SNR signal is significantly cleaner (less noisy) than a 5 dB SNR signal. By giving the 15 dB signal more weight, MRC maximizes the quality of the final combined signal. Simply adding them equally (like in EGC) would allow the much noisier signal from Antenna 2 to degrade the high-quality signal from Antenna 1.

6.  **Answer:** The receiver is using switched diversity. It stays on one antenna until the signal gets weak (e.g., due to the performer's body blocking the path), then it quickly switches to the other antenna to find a better signal.
    -   **Concept:** The practical operation of switched diversity.
    -   **Reasoning:** As the performer moves, the multipath environment changes constantly. The receiver uses one antenna as its primary. If the performer turns and the signal from that antenna becomes weak or fades, the receiver's logic detects the drop in quality and instantly switches to the second antenna, which is likely receiving a stronger signal due to its different location, thus preventing an audio dropout.

7.  **Answer:** This would be effective if the two links operate on frequencies separated by more than the channel's coherence bandwidth.
    -   **Concept:** The conditions required for frequency diversity to be effective.
    -   **Reasoning:** For frequency diversity to work, the fading on the two channels must be independent. This occurs if their frequency separation is greater than the coherence bandwidth of the channel. If the frequencies are too close, they will be affected by the same fading events, and both links will fail simultaneously, providing no diversity benefit.

8.  **Answer:** It enables spatial multiplexing, allowing multiple data streams to be sent simultaneously, which dramatically increases data rates.
    -   **Concept:** The extension of space diversity to spatial multiplexing in MIMO systems.
    -   **Reasoning:** With antennas at the receiver only (SIMO), you can achieve diversity gain (reliability). With antennas at both ends (MIMO), you can go a step further. The system can treat the multiple paths not just as redundant copies but as separate "pipes" to send different data streams at the same time over the same frequency, a technique called spatial multiplexing. This is a primary reason for the massive speed increases in 4G and 5G.

9.  **Answer:** No, it would provide almost no benefit.
    -   **Concept:** Diversity techniques are designed to combat fading caused by multipath.
    -   **Reasoning:** The communication path for a deep-space probe is a stable, line-of-sight channel with no multipath. There are no reflections, diffractions, or scattering to create multiple, independently fading paths. Since there is no fading to combat, implementing diversity would add complexity, weight, and power consumption for no performance gain.

10. **Answer:** This is space diversity. It helps prevent fading by ensuring that if one antenna is in a "dead spot," the other is likely receiving a clear signal.
    -   **Concept:** The application of space diversity in a consumer context like a car radio.
    -   **Reasoning:** As the car moves through a city, multipath fading causes the signal strength of a given radio station to fluctuate rapidly. By having two antennas in different locations (e.g., front and rear windows), the car's radio can implement diversity (likely selection combining). When the signal on one antenna fades, the radio can instantly switch to the other antenna, which is in a different physical location and likely receiving a stronger signal, thus providing continuous, uninterrupted audio.
