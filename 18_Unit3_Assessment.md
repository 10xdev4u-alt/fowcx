---
title: "Unit III Assessment: Multiple Access Techniques"
id: "unit3-assessment"
tags: ["#assessment", "#unit3", "#quiz", "#exam_prep"]
aliases: ["Unit 3 Questions", "Multiple Access Quiz"]
links: [[FOWC/11_Unit3_Topic01_Intro_MA.md], [FOWC/12_Unit3_Topic02_FDMA.md], [FOWC/13_Unit3_Topic03_TDMA.md], [FOWC/14_Unit3_Topic04_SpreadSpectrum.md], [FOWC/15_Unit3_Topic05_FHMA.md], [FOWC/16_Unit3_Topic06_CDMA.md], [FOWC/17_Unit3_Topic07_OFDM.md]]
---

# UNIT III Assessment: Multiple Access Techniques

This assessment covers the key concepts from Unit III, including FDMA, TDMA, Spread Spectrum, FHMA, CDMA, and OFDM.

---

## 1. Quiz Questions (Multiple Choice/Short Answer)

1.  Which multiple access technique separates users by assigning them unique frequency channels?
2.  The "near-far problem" is a critical issue in which multiple access scheme?
    a) FDMA
    b) TDMA
    c) CDMA
    d) OFDM
3.  What is the primary purpose of a "guard time" in a TDMA system?
4.  Which spread spectrum technique involves rapidly changing the carrier frequency according to a pseudo-random sequence?
5.  The ratio of the chip rate to the data rate in a DSSS system is known as the __________.
6.  Which technology uses orthogonal sub-carriers to achieve high spectral efficiency and combat multipath interference?
7.  In the "cocktail party" analogy, the different languages being spoken correspond to the use of different __________ in a CDMA system.
8.  Which 2G cellular standard is a classic example of a TDMA-based system?
9.  What is the main disadvantage of using guard bands in an FDMA system?
10. The multiple access scheme used in 4G LTE and 5G NR, which allocates subsets of sub-carriers to different users, is called __________.

---

## 2. Reasoning Questions

1.  Compare and contrast FDMA and TDMA, explaining one key advantage and one key disadvantage of each relative to the other.
2.  Explain why spread spectrum techniques are inherently more secure than narrowband techniques like FDMA or TDMA.
3.  A CDMA system requires strict power control, while an FDMA system does not. Explain the fundamental reason for this difference.
4.  Why is OFDM particularly effective at combating multipath interference, a major problem for high-speed single-carrier systems?
5.  Differentiate between slow and fast frequency hopping (FHSS). Which one offers better protection against a narrowband jammer and why?
6.  If you increase the length of the spreading code (i.e., more chips per data bit) in a DSSS/CDMA system, how does this affect the Processing Gain and the system's resistance to interference?
7.  A TDMA system and an FDMA system are both designed to support 10 users. Describe how the radio resource is allocated to the 10th user in each system.
8.  Explain the purpose of a Cyclic Prefix (CP) in OFDM and how it helps maintain orthogonality in a multipath environment.
9.  Why is CDMA capacity considered "soft," while FDMA/TDMA capacity is considered "hard"?
10. A Bluetooth headset (which uses FHSS) is operating near a Wi-Fi router (which can use DSSS or OFDM). Explain why the Bluetooth audio might occasionally stutter but is unlikely to fail completely.

---

## 3. Real-World Happening Questions

1.  Early analog TV broadcasts assigned a different 6 MHz frequency channel to each station in a city. Which multiple access principle does this resemble and why?
2.  You are designing a low-cost, low-power sensor network where each sensor only needs to send a tiny amount of data once every hour. Would you choose a complex scheme like CDMA or a simpler scheme like TDMA? Justify your choice.
3.  Military communication systems often need to be "anti-jam." Which spread spectrum technique would be more suitable for this requirement and why?
4.  A 3G phone (using CDMA) and a 2G phone (using TDMA/GSM) are operating in the same area. Why can they both operate without interfering with each other, even if their frequency bands partially overlap?
5.  Modern Wi-Fi (Wi-Fi 6) uses OFDMA. How does this allow a single Wi-Fi router to communicate more efficiently with multiple devices (like a smartphone, a laptop, and a smart TV) simultaneously, compared to older Wi-Fi standards?
6.  If you look at a spectrum analyzer showing a busy CDMA channel, you would just see a wide, flat, noise-like signal. However, if you looked at a busy FDMA channel, you would see distinct spikes. Explain this difference.
7.  To increase the number of users in a GSM (TDMA) system, a network operator implements "half-rate" voice codecs. Conceptually, how does this double the user capacity on a single frequency carrier?
8.  GPS signals are transmitted from satellites at extremely low power levels, arriving at the Earth's surface far weaker than background noise. Yet, a GPS receiver can still lock onto them. What technology makes this possible and how?
9.  Why is it that in a TDMA system like GSM, your phone's battery life is generally better than it would be in a comparable FDMA system where you have a channel dedicated to you continuously?
10. A city deploys a new 5G network using OFDMA. A user streaming a 4K video gets a large number of sub-carriers, while a nearby IoT water meter gets only a few sub-carriers. Explain how OFDMA makes this efficient allocation possible.

---

## 4. Rapid Fire Questions with Answers

1.  **Q:** Does FDMA require network-wide time synchronization?
    **A:** No.
2.  **Q:** What is the multiple access version of OFDM?
    **A:** OFDMA.
3.  **Q:** What is the primary solution to the near-far problem in CDMA?
    **A:** Strict power control.
4.  **Q:** Does FHSS use a chipping sequence?
    **A:** No, it uses a hopping sequence. DSSS uses a chipping sequence.
5.  **Q:** What is the main purpose of a guard band in FDMA?
    **A:** To prevent adjacent channel interference.
6.  **Q:** Is a higher Processing Gain in CDMA better or worse for interference rejection?
    **A:** Better.
7.  **Q:** Which technique is more robust against frequency-selective fading: single-carrier or OFDM?
    **A:** OFDM.
8.  **Q:** What does the "T" in TDMA stand for?
    **A:** Time.
9.  **Q:** Can users in a CDMA system transmit at the same time on the same frequency?
    **A:** Yes.
10. **Q:** What part of an OFDM symbol is copied to create the Cyclic Prefix?
    **A:** The end of the symbol.

---

## 5. Answers

### 5.1. Quiz Questions - Answers

1.  **Answer:** FDMA (Frequency Division Multiple Access).
    -   **Concept:** FDMA is a multiple access protocol that allocates a unique, non-overlapping frequency band to each user.
    -   **Reasoning:** The defining characteristic of FDMA is the division of the available spectrum into distinct channels, separating users by frequency.

2.  **Answer:** c) CDMA.
    -   **Concept:** The near-far problem occurs when a receiver picks up a strong signal from a nearby transmitter that drowns out a weaker signal from a farther transmitter.
    -   **Reasoning:** In CDMA, all users transmit on the same frequency. Without power control, a user close to the base station would completely overpower users who are farther away, making it impossible to decode their signals. This is not an issue in FDMA/TDMA where users are already separated by frequency or time.

3.  **Answer:** To prevent the time slots of different users from overlapping.
    -   **Concept:** Guard times are unused periods inserted between TDMA time slots to account for timing uncertainties and signal propagation delays.
    -   **Reasoning:** Since signals from different users arrive at the base station at slightly different times, the guard time provides a buffer, ensuring that one user's transmission doesn't bleed into the beginning of the next user's time slot.

4.  **Answer:** FHSS (Frequency Hopping Spread Spectrum).
    -   **Concept:** FHSS is a spread spectrum method where the signal's carrier frequency hops from one channel to another in a predetermined but pseudo-random pattern.
    -   **Reasoning:** This rapid hopping is the defining mechanism of FHSS, used to avoid interference and provide security.

5.  **Answer:** Processing Gain (PG).
    -   **Concept:** Processing Gain is a fundamental parameter in DSSS systems that quantifies the degree to which the signal is spread.
    -   **Reasoning:** It is calculated as the ratio of the spreading bandwidth (chip rate) to the data bandwidth (data rate) and directly relates to the system's ability to suppress interference.

6.  **Answer:** OFDM (Orthogonal Frequency Division Multiplexing).
    -   **Concept:** OFDM is a digital modulation scheme that uses a large number of closely-spaced, mathematically orthogonal sub-carriers to transmit data in parallel.
    -   **Reasoning:** This orthogonality allows the sub-carriers to overlap without interfering, leading to high spectral efficiency. The use of many slow sub-streams makes it robust against multipath fading.

7.  **Answer:** Codes (or spreading codes).
    -   **Concept:** The "cocktail party" analogy explains how CDMA separates users who are all speaking (transmitting) at the same time.
    -   **Reasoning:** In the analogy, different languages allow a listener to focus on one conversation. In CDMA, these "languages" are the unique spreading codes assigned to each user, which allow the receiver to isolate and decode only the intended signal.

8.  **Answer:** GSM (Global System for Mobile Communications).
    -   **Concept:** Real-world cellular standards are built upon specific multiple access techniques.
    -   **Reasoning:** The GSM standard, the most widely deployed 2G technology, is fundamentally based on a TDMA structure, where 8 users share a single frequency carrier in different time slots. (It is technically a hybrid FDMA/TDMA system).

9.  **Answer:** They represent wasted spectrum that cannot be used for data transmission.
    -   **Concept:** Guard bands are unused frequency gaps between FDMA channels.
    -   **Reasoning:** While necessary to prevent adjacent channel interference, guard bands are spectrally inefficient because no information can be transmitted within them, reducing the total number of users the system can support for a given bandwidth.

10. **Answer:** OFDMA (Orthogonal Frequency Division Multiple Access).
    -   **Concept:** OFDMA is the multi-user version of OFDM.
    -   **Reasoning:** It extends the OFDM technique by allocating different subsets of the orthogonal sub-carriers to different users in both the time and frequency domains, providing a highly flexible and efficient multiple access scheme for 4G and 5G.

### 5.2. Reasoning Questions - Answers

1.  **Answer:** FDMA's advantage is simplicity, but it's inefficient. TDMA is more efficient but requires synchronization.
    -   **Concept:** The trade-off between system complexity and spectral efficiency in basic multiple access schemes.
    -   **Reasoning:** **FDMA**'s advantage is its simplicity, as it requires no complex timing across the network. Its disadvantage is its inefficiency, as it wastes spectrum on guard bands and dedicates a channel even when the user is silent. **TDMA**'s advantage is its efficiency, as multiple users share one carrier and the transmitter can be turned off between slots to save power. Its disadvantage is the added complexity of requiring precise time synchronization for all users.

2.  **Answer:** The signal is spread to look like low-power noise and requires a secret code to be decoded.
    -   **Concept:** The security-through-obscurity principle of spread spectrum.
    -   **Reasoning:** A spread spectrum signal's power is distributed over a very wide bandwidth, making its power level at any single frequency very low, often below the background noise floor. This makes it difficult for an eavesdropper to even detect. Furthermore, without the correct pseudo-random code (the "key"), the signal cannot be "despread" and remains indistinguishable from noise.

3.  **Answer:** In CDMA all users are on the same frequency, so power is the only way to manage interference. In FDMA, users are already separated by different frequencies.
    -   **Concept:** The mechanism used to separate users in different multiple access schemes.
    -   **Reasoning:** In **CDMA**, all users share the same frequency. The receiver separates signals based on their codes. If a nearby user's signal arrives with much higher power, it will drown out the farther user's signal, making it impossible for the receiver to decode it. Power control ensures all signals arrive at the receiver with equal power. In **FDMA**, users are in different, non-overlapping frequency bands, so they are separated by filters. The power of one user doesn't directly affect another.

4.  **Answer:** OFDM divides one fast data stream into many slow sub-streams, making the symbol duration long relative to the multipath delay.
    -   **Concept:** The "divide and conquer" strategy of OFDM to combat Inter-Symbol Interference (ISI).
    -   **Reasoning:** High-speed single-carrier systems have very short symbol durations. Multipath delay can cause a symbol to smear into the next one (ISI). OFDM breaks the high-speed stream into thousands of slow sub-streams. Each sub-stream has a very long symbol duration. The multipath delay is now only a small fraction of this long symbol duration, making its effect negligible and easy to mitigate with a cyclic prefix.

5.  **Answer:** Fast hopping provides better protection because it hops multiple times per data bit.
    -   **Concept:** The relationship between hop rate and symbol rate in FHSS.
    -   **Reasoning:** In **slow hopping**, multiple bits are sent per hop. If a jammer is on that frequency, all those bits are lost. In **fast hopping**, the frequency changes multiple times during the transmission of a single bit. If a jammer is on one of the hop frequencies, it only corrupts a small fraction of the bit. The receiver can use majority logic or error correction to recover the original bit, providing much better protection.

6.  **Answer:** It increases the Processing Gain, which improves interference resistance.
    -   **Concept:** The relationship between code length, Processing Gain, and interference suppression in DSSS.
    -   **Reasoning:** Processing Gain (PG) is the ratio of the chip rate to the data rate. Using a longer spreading code for each bit means the chip rate increases for a fixed data rate, thus increasing the PG. A higher PG means the signal is spread more widely. During despreading, this provides more "leverage" to suppress interfering signals, improving the system's overall interference resistance.

7.  **Answer:** In FDMA, the 10th user gets a dedicated frequency channel. In TDMA, the 10th user gets a dedicated time slot on a shared frequency.
    -   **Concept:** The fundamental resource allocation unit in FDMA vs. TDMA.
    -   **Reasoning:** In the **FDMA** system, the total bandwidth is divided into at least 10 channels, and the 10th user is assigned one of these frequency channels for their exclusive use. In the **TDMA** system, a single frequency channel is divided into frames containing at least 10 time slots, and the 10th user is assigned one of these recurring time slots.

8.  **Answer:** The CP is a copy of the end of the symbol placed at the beginning, which acts as a guard interval to absorb multipath delay.
    -   **Concept:** The use of a guard interval to mitigate ISI and maintain orthogonality in OFDM.
    -   **Reasoning:** Multipath causes delayed versions of a symbol to arrive at the receiver. The Cyclic Prefix provides a guard time for these delayed signals to arrive and settle before the main part of the symbol is processed. By discarding the CP at the receiver, the system ensures that the processing window for the FFT (Fast Fourier Transform) contains a signal free from the previous symbol's interference, thus preserving the crucial orthogonality between sub-carriers.

9.  **Answer:** CDMA capacity is interference-limited ("soft"), while FDMA/TDMA capacity is channel-limited ("hard").
    -   **Concept:** The difference between interference-limited and channel-limited system capacity.
    -   **Reasoning:** In **FDMA/TDMA**, there is a fixed number of channels or time slots. When they are all in use, the 11th user is blocked. This is a "hard" limit. In **CDMA**, all users are on the same frequency. Each new user adds a little more noise to the system for everyone else. There is no fixed limit; the system can continue adding users, but the quality (SIR) for all users will gradually degrade. This graceful degradation is called "soft" capacity.

10. **Answer:** The FHSS of Bluetooth is designed to avoid interference by hopping away from frequencies that are in use.
    -   **Concept:** The interference avoidance mechanism of Frequency Hopping Spread Spectrum.
    -   **Reasoning:** The Wi-Fi signal will occupy a fixed band of frequencies. The Bluetooth device, using FHSS, is constantly hopping across many frequencies. When its hopping sequence lands on a frequency being used by the Wi-Fi router, a "hit" occurs, and that small piece of audio data is lost, causing a stutter. However, on the very next hop (typically 1600 times per second), it moves to a clear frequency, and the audio resumes.

### 5.3. Real-World Happening Questions - Answers

1.  **Answer:** This resembles FDMA.
    -   **Concept:** Relating real-world spectrum allocation to multiple access principles.
    -   **Reasoning:** In this system, the total broadcast spectrum is divided into distinct, non-overlapping 6 MHz frequency channels. Each TV station is assigned one channel for its exclusive use. This is a perfect macroscopic example of FDMA, where users (TV stations) are separated by frequency.

2.  **Answer:** A simpler scheme like TDMA would be a better choice.
    -   **Concept:** Matching the complexity of a multiple access scheme to the application's requirements.
    -   **Reasoning:** The sensors have very low data rate requirements ("tiny amount of data") and are mostly inactive. A simple TDMA scheme where each sensor is assigned a specific time slot (e.g., Sensor 1 transmits at 1:00:01, Sensor 2 at 1:00:02) is very power-efficient and simple to implement. The complexity and power control requirements of CDMA would be overkill and inefficient for this type of "bursty," low-rate application.

3.  **Answer:** Both work, but FHSS is often considered more robust against simple jammers.
    -   **Concept:** The anti-jamming properties of different spread spectrum techniques.
    -   **Reasoning:** **FHSS** avoids the jammer by hopping to a different frequency. If a jammer targets a specific frequency, the FHSS system is only affected for the brief moment it hops onto that frequency. **DSSS** resists the jammer by spreading the jamming energy during the despreading process (using its Processing Gain). While both are effective, FHSS's avoidance strategy is conceptually simpler and can be more robust against powerful narrowband jammers that could otherwise overcome the processing gain of a DSSS system.

4.  **Answer:** They use different multiple access schemes that appear as noise to each other.
    -   **Concept:** The ability of different, well-designed communication systems to coexist.
    -   **Reasoning:** The 2G TDMA signal is confined to a relatively narrow frequency channel. The 3G CDMA signal is a wideband, low-power signal spread across a much larger frequency range. To the CDMA receiver, the TDMA signal looks like a narrowband interferer that can be suppressed by the despreading process. To the TDMA receiver, the CDMA signal looks like a slight increase in the background noise floor, which is generally not strong enough to cause significant interference.

5.  **Answer:** OFDMA allows the router to divide its channel into smaller sub-groups of sub-carriers and assign them to different devices simultaneously.
    -   **Concept:** The multi-user capability of OFDMA for efficient small-packet transmission.
    -   **Reasoning:** Older Wi-Fi used OFDM, where the entire channel was dedicated to one user at a time. If the user was just sending a small packet, the rest of the channel's capacity in that moment was wasted. With OFDMA, the router can break the channel into smaller Resource Units (RUs) and serve multiple devices at the same time: a large RU for the video stream, a medium RU for the laptop, and a small RU for the smart TV's status update, all in the same transmission window. This is vastly more efficient.

6.  **Answer:** A CDMA signal is intentionally spread to be noise-like, while FDMA signals are concentrated in narrow frequency spikes.
    -   **Concept:** The spectral appearance of different multiple access signals.
    -   **Reasoning:** A **CDMA** signal's power is spread thinly across a very wide bandwidth. The sum of many such signals still looks like a flat, wideband noise signal. An **FDMA** system allocates specific, narrow frequency bands to each user. On a spectrum analyzer, each active user's signal will appear as a distinct power "spike" at its assigned frequency.

7.  **Answer:** It allows two users to share a single time slot, one using the first half and the other using the second half.
    -   **Concept:** Increasing TDMA capacity by modifying the voice encoding and slot structure.
    -   **Reasoning:** A standard "full-rate" codec uses an entire time slot to transmit the voice data for one user. A "half-rate" codec compresses the voice more, requiring only half the number of bits. This allows the system to redefine a single time slot into two smaller, sub-slots. By assigning one sub-slot to User A and the second to User B, the system can now support two users in the same time slot that previously supported only one, effectively doubling the capacity.

8.  **Answer:** DSSS (Direct Sequence Spread Spectrum), the technology behind CDMA.
    -   **Concept:** The ability of a DSSS receiver to pull a signal out from below the noise floor.
    -   **Reasoning:** The GPS signal is spread using a unique, publicly known code (the C/A code). The GPS receiver knows this code. When the receiver multiplies the extremely weak incoming signal by the same code, the despreading process collapses the signal's energy back into a narrow band, raising its power far above the noise floor. This is possible due to the high Processing Gain of the system.

9.  **Answer:** In TDMA, the phone's transmitter is only active during its assigned time slot and can be powered down for the rest of the frame.
    -   **Concept:** The power-saving benefits of a non-continuous transmission scheme.
    -   **Reasoning:** In a TDMA system like GSM with 8 time slots, the phone only transmits 1/8th of the time. For the other 7/8ths of the time, the power-hungry transmitter circuitry can be turned off, significantly conserving battery life. In a pure FDMA system, the transmitter would have to be on continuously for the entire duration of the call.

10. **Answer:** OFDMA allows for flexible resource allocation based on user need.
    -   **Concept:** The dynamic and granular resource allocation capability of OFDMA.
    -   **Reasoning:** OFDMA allows the base station to act as a master scheduler. It sees that the video stream requires high bandwidth and allocates a large number of sub-carriers to that user. It also sees that the IoT meter only needs to send a tiny data packet and allocates just a few sub-carriers to it for a very short duration. This ability to assign resources (sub-carriers and time slots) with fine granularity based on real-time demand is what makes OFDMA so efficient.
