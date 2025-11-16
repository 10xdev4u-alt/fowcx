--- 
title: "Code Division Multiple Access (CDMA)"
id: "unit3-topic6-cdma"
tags: ["#multiple_access", "#unit3", "#spread_spectrum", "#dsss", "#cdma"]
aliases: ["CDMA", "DSSS"]
links: [[FOWC/14_Unit3_Topic04_SpreadSpectrum.md]]
---

# UNIT III: Code Division Multiple Access (CDMA)

CDMA is a powerful multiple access technique based on Direct Sequence Spread Spectrum (DSSS). Unlike FDMA (which gives users their own frequency) or TDMA (which gives users their own time slot), CDMA allows all users to transmit on the **same frequency at the same time**. It separates users by assigning each one a unique "spreading code."

---

## 1. How CDMA Works (via DSSS)

The core principle of CDMA is to spread a user's narrowband data signal across a very wide bandwidth using a special code.

1.  **Spreading:** Each bit of the user's data (e.g., a '1' or '-1') is multiplied by a high-rate pseudo-random code, also known as a **chipping sequence**. This code consists of many "chips" (e.g., `+1, -1, -1, +1, +1, ...`).
2.  **Transmission:** This multiplication process "spreads" the low-rate data signal into a wideband signal that looks like noise. This wideband signal is then transmitted.
3.  **Reception & Despreading:** The receiver, which knows the exact same spreading code, multiplies the incoming wideband signal by that code. This has two effects:
    *   The intended user's signal is "despread" back to its original narrowband form, concentrating its power.
    *   All other users' signals (which used different codes) are *not* despread. They remain as low-power, wideband noise and are effectively ignored.

**Analogy:** The "cocktail party" or "multiple languages" analogy is perfect. Imagine a room where many pairs of people are talking. Each pair is speaking a different language (the code). You can tune your brain to listen to only the language you understand (your code) and ignore all the other conversations, even though they are all happening at the same time in the same room.

```
User 1 Data: [  1  ]
User 1 Code: [1,-1,1,-1]
Transmitted: [1,-1,1,-1]  (User 1 Data * User 1 Code)

User 2 Data: [ -1  ]
User 2 Code: [1, 1,-1,-1]
Transmitted: [-1,-1,1, 1]  (User 2 Data * User 2 Code)

Receiver (for User 1):
Receives Sum: [0,-2,2, 0] = [1,-1,1,-1] + [-1,-1,1, 1]
Multiplies by User 1 Code [1,-1,1,-1]:
  (0*1) + (-2*-1) + (2*1) + (0*-1) = 0 + 2 + 2 + 0 = 4
Result is a large positive number -> Decodes as a '1'.

Receiver (for User 2):
Multiplies by User 2 Code [1,1,-1,-1]:
  (0*1) + (-2*1) + (2*-1) + (0*-1) = 0 - 2 - 2 + 0 = -4
Result is a large negative number -> Decodes as a '-1'.
```
*Simplified example of CDMA encoding and decoding.*

---

## 2. Key Concepts in CDMA

### 2.1. Spreading Codes
The codes used in CDMA must have good properties.
*   **Walsh Codes:** In many systems (like IS-95), Walsh codes are used to separate users within the same cell. They are perfectly **orthogonal**, meaning that when you multiply and sum them as in the example above, the result for a non-matching code is exactly zero (in a perfectly synchronized system).
*   **Pseudo-Noise (PN) Codes:** These codes are used to separate different cells from each other. They are not perfectly orthogonal but have very low cross-correlation, meaning they appear as random noise to each other.

### 2.2. Processing Gain (PG)
Processing gain is a measure of how much the signal is spread. It is the ratio of the bandwidth of the spread signal (chip rate) to the bandwidth of the data signal (data rate).

> [!formula] Processing Gain (PG)
> $$ PG = \frac{W}{R} = \frac{\text{Chip Rate}}{\text{Data Rate}} $$
> A higher processing gain means the signal is spread more widely, providing better resistance to interference. It is a key factor in determining CDMA system capacity.

### 2.3. The Near-Far Problem
A major challenge in CDMA is the **near-far problem**. If a user close to the base station transmits at the same power as a user far away, the signal from the nearby user will be received much more strongly, drowning out the weaker signal from the distant user.
*   **Solution:** CDMA systems require very strict and fast **power control**. The base station constantly tells all mobiles to adjust their transmit power so that all signals arrive at the base station with roughly equal strength.

---

## 3. Advantages and Disadvantages

### 3.1. Advantages
1.  **High Capacity:** CDMA allows for a "soft" capacity limit. Adding more users increases the overall noise floor for everyone, gradually degrading performance rather than causing hard blocking. Universal frequency reuse (N=1) is possible, maximizing capacity.
2.  **Inherent Security:** The use of codes makes the signal difficult to intercept or decode without the correct key.
3.  **Robustness:** Excellent resistance to multipath fading and narrowband interference.
4.  **Soft Handoff:** Since adjacent cells use the same frequency, a mobile can connect to a new cell before disconnecting from the old one ("make-before-break"), leading to highly reliable handoffs.

### 3.2. Disadvantages
1.  **Strict Power Control Requirement:** The near-far problem necessitates complex, fast, and accurate power control mechanisms, which adds significant system complexity.
2.  **Synchronization:** The receiver must be perfectly synchronized with the transmitter's code to despread the signal correctly.
3.  **Self-Interference:** Even with orthogonal codes, multipath can delay signals, destroying the orthogonality and causing users within the same cell to interfere with each other.

---

> [!check] ### Exam Focus & Key Takeaways
>
> **Potential Exam Questions:**
> 1.  "Explain the principle of CDMA. How are users separated if they all transmit at the same time and frequency?"
> 2.  "What is the near-far problem in CDMA and how is it mitigated?"
> 3.  "Define Processing Gain and explain its significance in a CDMA system."
>
> **Tips for Answering:**
> - The "multiple languages at a party" analogy is the best way to explain the core concept.
> - For user separation, emphasize the role of unique, orthogonal spreading codes.
> - Power control is the critical solution to the near-far problem—always mention it.
>
> **Key Takeaway:** CDMA is a powerful spread spectrum technique that achieves high capacity and robustness by allowing all users to share the same spectrum, separating them with unique codes. Its biggest operational challenge is the need for strict power control.
