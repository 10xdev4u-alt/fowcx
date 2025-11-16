---
title: "Introduction to Multiple Access Techniques"
id: "unit3-topic1-intro-ma"
tags: ["#multiple_access", "#unit3", "#fdma", "#tdma", "#cdma"]
aliases: ["Multiple Access Intro"]
links: [[FOWC/00_Syllabus.md]]
---

# UNIT III: Introduction to Multiple Access Techniques

Welcome to Unit III! In this unit, we will explore one of the most critical concepts in wireless communication: **Multiple Access**. These techniques are the fundamental "rules of engagement" that allow many users to share the same finite radio spectrum simultaneously and efficiently.

---

## 1. What is Multiple Access and Why Do We Need It?

Imagine you are in a large room with a hundred other people, and everyone wants to have a conversation. If everyone talks at once, the result is chaos—no one can be understood. To solve this, you would need a set of rules, such as:
*   People in different corners of the room talk to each other (dividing by space).
*   People take turns speaking (dividing by time).
*   People speak at different pitches (high vs. low) and you only listen to the pitch of the person you're talking to (dividing by frequency).
*   People speak in different languages, and you only listen to the language you understand (dividing by code).

In wireless communication, the "room" is the radio spectrum available in a cell, and the "people" are the mobile users. The radio spectrum is a limited, shared medium. A **Multiple Access (MA)** scheme is a protocol that allows multiple mobile users to share this spectrum without interfering with one another.

Without these schemes, only one user could make a call in an entire cell at any given time, which would make cellular networks practically useless.

---

## 2. The Three Dimensions of Sharing

The radio resource can be visualized as a three-dimensional block that can be "sliced and diced" to be allocated to different users. The three fundamental dimensions for sharing are:

1.  **Frequency:** The available spectrum is divided into smaller, non-overlapping frequency bands. Each user gets their own private frequency band. This is **Frequency Division Multiple Access (FDMA)**.
2.  **Time:** All users operate on the same frequency, but they take turns using it. The time is divided into slots, and each user is allocated specific time slots. This is **Time Division Multiple Access (TDMA)**.
3.  **Code:** All users can transmit on the same frequency at the same time, but each user's signal is encoded with a unique "key" or code. The receiver, knowing the code, can "unlock" and listen to the intended signal while all other signals appear as background noise. This is **Code Division Multiple Access (CDMA)**.

```
      ^ Frequency
      |
      |   /------------------/
      |  /      Code       /|
      | /------------------/ |
      | |                  | |
      | |       TIME       | /
      | |                  |/
      | +------------------+------> Time
      |
```
*ASCII Diagram: The three dimensions (Time, Frequency, Code) for sharing the radio resource.*

---

## 3. Classification of Multiple Access Techniques

Based on these dimensions, we can classify the primary multiple access schemes.

### A. Frequency Division Multiple Access (FDMA)
*   **How it works:** The spectrum is channelized into narrow frequency bands. Each user is assigned an exclusive frequency band for the duration of the call.
*   **Analogy:** Different radio stations (e.g., 93.5 FM, 98.3 FM). Each station has its own frequency and they all broadcast at the same time without interfering.

### B. Time Division Multiple Access (TDMA)
*   **How it works:** Multiple users share the same wide frequency band, but they use it in turns. Time is divided into frames, and each frame is divided into time slots. Each user gets one time slot per frame.
*   **Analogy:** A group of people in a meeting taking turns to speak. Everyone uses the same room (frequency), but only one person speaks at a time.

### C. Code Division Multiple Access (CDMA)
*   **How it works:** All users transmit on the same wide frequency band at the same time. Each user's signal is multiplied by a unique pseudo-random code. The receiver uses the same code to recover the original signal.
*   **Analogy:** The "cocktail party effect." You are at a noisy party where many people are talking at once. However, you can focus on the voice of the person you are talking to and tune out the others, even though they are all speaking at the same time.

### D. Advanced & Hybrid Schemes
*   Modern systems like 4G (LTE) and 5G use more advanced, hybrid schemes like **Orthogonal Frequency Division Multiple Access (OFDMA)**, which is a combination of frequency and time division, but with much higher spectral efficiency. We will touch on this later.

```
      ^ Freq.
      |
FDMA  | User 3 +-------+
      | User 2 +-------+
      | User 1 +-------+
      +---------------------> Time

      ^ Freq.
      |
TDMA  | +--+  +--+  +--+
      | |U1|U2|U3|U1|U2|U3| ...
      | +--+  +--+  +--+
      +---------------------> Time

      ^ Freq.
      |
CDMA  | +------------------+
      | | U1, U2, U3 all   |
      | | use the same     |
      | | resource,        |
      | | separated by code|
      | +------------------+
      +---------------------> Time
```
*ASCII Diagram: Visual comparison of FDMA, TDMA, and CDMA.*

---

> [!check] ### Exam Focus & Key Takeaways
>
> **Potential Exam Questions:**
> 1.  "What is the need for multiple access schemes in wireless communication? Briefly describe the three main types."
> 2.  "Use an analogy to explain the difference between FDMA, TDMA, and CDMA."
>
> **Tips for Answering:**
> - Start by stating that the radio spectrum is a limited, shared resource.
> - Use clear analogies: Radio stations for FDMA, taking turns for TDMA, and the cocktail party for CDMA.
> - A diagram showing how the time-frequency block is sliced for each technique is highly effective.
>
> **Key Takeaway:** Multiple access techniques are essential for sharing the limited wireless spectrum among many users. The main methods achieve this by dividing the spectrum by **frequency (FDMA)**, **time (TDMA)**, or **code (CDMA)**.
