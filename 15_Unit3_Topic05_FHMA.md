---
title: "Frequency Hopping Multiple Access (FHMA)"
id: "unit3-topic5-fhma"
tags: ["#multiple_access", "#unit3", "#spread_spectrum", "#fhss", "#fhma"]
aliases: ["FHMA", "FHSS"]
links: [[FOWC/14_Unit3_Topic04_SpreadSpectrum.md]]
---

# UNIT III: Frequency Hopping Multiple Access (FHMA)

Frequency Hopping is a spread spectrum technique where the signal is broadcast over a seemingly random series of radio frequencies, hopping from frequency to frequency. When used as a multiple access method, it is called Frequency Hopping Multiple Access (FHMA).

---

## 1. How Frequency Hopping (FHSS) Works

The core principle of Frequency Hopping Spread Spectrum (FHSS) is to avoid interference by not staying on any single frequency for long.

*   **Hopping Sequence:** The total available bandwidth is divided into many possible channels. The transmitter uses a carrier frequency that changes rapidly, "hopping" from one channel to another.
*   **Pseudo-Randomness:** The sequence of frequencies is not truly random; it is a predetermined, pseudo-random sequence that is known to both the transmitter and the intended receiver.
*   **Synchronization:** The receiver must be synchronized to the same hopping pattern to be able to follow the signal and reconstruct the original message. To an unintended listener without the correct hopping sequence, the signal appears as short, random bursts of noise.

**Analogy:** Imagine you and a friend are having a secret conversation across a crowded room where people keep shouting on different megaphones (interference). You agree beforehand to switch your listening and talking "channels" (frequencies) every second in a specific pattern (e.g., Channel 7 -> Channel 23 -> Channel 5 -> ...). As long as you both follow the pattern, you can communicate, and any single shouting person can only disrupt a tiny piece of your conversation.

```
  ^ Frequency
  |
F5| - - - - - - - + - - - - - - - - - - - - - - - - - -
  |               |
F4| - - - - - - - - - - - - - - - - - + - - - - - - - -
  |                                   |
F3| - - - - - + - - - - - - - - - - - - - - - - - - - -
  |           |
F2| - - - - - - - - - - - - - - - + - - - - - - - - - -
  |                               |
F1| - + - - - - - - - - - - - - - - - - - - - - - - - -
  +-----------------------------------------------------> Time
```
*ASCII Diagram: The carrier frequency hops between different frequency channels (F1, F3, F5, F2, F4...) over time according to a pseudo-random sequence.*

---

## 2. Slow Hopping vs. Fast Hopping

FHSS systems are categorized based on the rate of hopping relative to the data rate.

### 2.1. Slow Frequency Hopping
In slow hopping, one or more data symbols are transmitted on a single frequency hop. The symbol rate is higher than the hop rate.
*   **Characteristic:** `Symbol Rate > Hop Rate`
*   **Example:** Several bits of data are sent before the frequency changes.

### 2.2. Fast Frequency Hopping
In fast hopping, the carrier frequency hops multiple times during the transmission of a single data symbol. The hop rate is higher than the symbol rate.
*   **Characteristic:** `Hop Rate > Symbol Rate`
*   **Example:** The frequency changes several times while sending just one bit of data. This provides much better resistance to interference, as a single jammed frequency can only affect a small fraction of a single data bit.

---

## 3. FHMA: Using FHSS for Multiple Access

To allow multiple users to share the same spectrum, FHMA assigns each user a different hopping sequence.

*   **Orthogonal Sequences:** Ideally, the hopping sequences for different users are designed to be "orthogonal," meaning they will not land on the same frequency channel at the same time.
*   **Collision:** In practice, it's possible for two users' sequences to randomly assign them the same frequency at the same time, causing a "hit" or collision. However, since the hopping is so rapid, the collision only affects a small amount of data, which can often be corrected by error-correction codes.

---

## 4. Advantages and Disadvantages

### 4.1. Advantages
1.  **Robustness to Interference:** FHSS is highly resistant to narrowband interference and jamming, as the signal only spends a very short time on any single frequency.
2.  **Security:** It is difficult for an eavesdropper to listen in without knowing the correct hopping sequence.
3.  **Simple Implementation:** FHSS systems do not suffer from the "near-far problem" that affects CDMA, so they do not require the same complex power control mechanisms.

### 4.2. Disadvantages
1.  **Complex Frequency Synthesizers:** Requires transmitters and receivers that can change frequencies very rapidly and accurately, which can be complex and expensive.
2.  **Lower Capacity than CDMA:** While it supports multiple users, the capacity is generally lower than a well-designed DSSS (CDMA) system because of the potential for random hits/collisions between users.
3.  **Latency:** The process of hopping and synchronizing can introduce a small amount of latency.

---

> [!check] ### Exam Focus & Key Takeaways
>
> **Potential Exam Questions:**
> 1.  "Explain the principle of Frequency Hopping Spread Spectrum (FHSS). How is it used to provide multiple access (FHMA)?"
> 2.  "Differentiate between slow and fast frequency hopping."
> 3.  "What are the primary advantages of FHSS that make it suitable for applications like Bluetooth?"
>
> **Tips for Answering:**
> - The "secret channel switching" analogy is very effective.
> - For FHMA, emphasize that each user gets a unique hopping *sequence*.
> - For advantages, focus on interference avoidance and inherent security.
>
> **Key Takeaway:** FHMA allows multiple users to share a band by assigning each one a unique, rapidly changing frequency hopping pattern. Its main strengths are its robustness against narrowband interference and its relative simplicity compared to CDMA.
