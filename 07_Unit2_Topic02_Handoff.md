---
title: "Handoff"
id: "unit2-topic2-handoff"
tags: ["#cellular", "#handoff", "#handover", "#mobility", "#unit2"]
aliases: ["Handover"]
links: [[FOWC/00_Syllabus.md], [FOWC/06_Unit2_Topic01_Frequency_Reuse.md]]
---

# UNIT II: Handoff (Handover)

This section explains the handoff (or handover) process, a critical function for maintaining connectivity in mobile cellular networks.

---

## 1. What is Handoff and Why is it Necessary?

**Handoff** (also known as **Handover**) is the process of transferring an active call or data session from one cell's base station to another without disconnecting the session.

**Why is it necessary?**
Imagine you're on a call while driving. As you move, the signal from the base station you started with gets weaker, and the signal from the base station you are moving towards gets stronger. If the call wasn't transferred to the new, stronger base station, the signal would eventually become too weak, and your call would drop. Handoff prevents this by seamlessly switching the connection.

### 1.1. The Handoff Scenario

The handoff procedure is initiated when the signal strength from the current base station drops below a certain threshold, and the signal from an adjacent base station is strong enough to take over the call.

*   **Mobile Station (MS):** Continuously measures the signal strength of its current base station and neighboring base stations.
*   **Base Station (BS):** Relays the signal strength measurements from the MS to the Mobile Switching Center (MSC).
*   **Mobile Switching Center (MSC):** The brain of the operation. The MSC analyzes the measurements and decides when and to which base station the handoff should occur.

```
      (Moving Direction) -->
+----------+
| Mobile   |
| Station  |
+----------+

   Signal from BS1 (Weakening)
  /
 /
+-----+                               +-----+
| BS1 |<-- Old Connection (via MSC) -->| BS2 |
+-----+                               +-----+
                                         \
                                          \
                                    Signal from BS2 (Strengthening)
                                    New Connection (via MSC)
```
*ASCII Diagram: As the Mobile Station moves away from Base Station 1 (BS1) and towards Base Station 2 (BS2), the MSC orchestrates a handoff.*

---

## 2. The Handoff Process

The handoff decision is not just based on absolute signal strength. To prevent unnecessary and frequent handoffs (the "ping-pong" effect) when a user is hovering at a cell boundary, a **hysteresis** mechanism is used.

1.  **Initiation:** As the MS moves, the received signal strength from the current BS decreases. The MS is constantly scanning for "beacon" signals from neighboring cells.
2.  **Measurement:** The signal strength from a neighboring cell, say BS2, begins to exceed the signal strength from the current cell, BS1.
3.  **Handoff Threshold:** A handoff is only considered when the signal from BS2 is stronger than the signal from BS1 by a specific margin, known as the **hysteresis level (Δ)**. This ensures the new signal is consistently stronger. The handoff is initiated when the current signal drops below a minimum usable level (the **handoff threshold**).
4.  **Resource Allocation:** The MSC identifies the need for a handoff and checks if the target base station (BS2) has an available voice channel.
5.  **Handoff Execution:** If a channel is available, the MSC instructs the MS to switch to the new channel (frequency, time slot, etc.) corresponding to BS2. The call is then rerouted through BS2.
6.  **Channel Release:** Once the handoff is complete, the MSC releases the channel that was being used on the original base station (BS1), making it available for another user.

> [!tip] Handoff Signal Strength Diagram
> A graph illustrating the handoff process would show the signal strength from BS1 decreasing over time while the signal from BS2 increases. A handoff is triggered when the signal from BS1 drops below a predefined threshold and the signal from BS2 is stronger by a hysteresis margin (Δ). This prevents premature or unnecessary handoffs.

> [!note]
> The time required to complete the handoff is critical. It must be short enough to be imperceptible to the user. A long handoff duration can lead to dropped calls. This is known as **handoff latency**.

---

## 3. Types of Handoff

Handoffs can be categorized based on how the connection transfer is made.

### 3.1. Hard Handoff ("Break-Before-Make")

In a **hard handoff**, the connection to the old base station is broken *before* the connection to the new base station is established.

*   **Characteristics:**
    *   There is a very brief interruption in the connection.
    *   It's like switching from one radio station to another; there's a momentary silence.
    *   This is the typical handoff mechanism used in **TDMA** and **FDMA** systems (like 2G GSM).
*   **Advantage:** Simpler to implement.
*   **Disadvantage:** Can cause a noticeable disruption or even a dropped call if the "break" period is too long.

### 3.2. Soft Handoff ("Make-Before-Break")

In a **soft handoff**, the mobile station establishes a connection with the new base station *before* breaking the connection with the old one. For a short period, the MS is connected to two (or more) base stations simultaneously.

*   **Characteristics:**
    *   The MS is in a "soft handoff zone" at the edge of the cell.
    *   The MSC combines the signals from both base stations to improve quality.
    *   This is the characteristic handoff mechanism used in **CDMA** systems (like 3G).
*   **Advantage:** Smoother and more reliable transition, reducing the probability of dropped calls.
*   **Disadvantage:** More complex, as it requires the MS to be able to communicate with multiple base stations at once and consumes more network resources during the handoff period.

---

## 4. Practical Handoff Considerations

### Prioritizing Handoffs

Dropped calls are more frustrating for users than blocked new calls. Therefore, cellular systems are often designed to prioritize handoff requests over new call initiation requests.

One common strategy is **guard channels**, where a fraction of the total available channels in a cell is reserved exclusively for handoff requests. This ensures that a channel is likely to be available for a user moving into the cell, even if it means a new call initiated within that cell might be blocked.

### The Umbrella Cell Concept

In dense urban areas, you might have large macrocells providing wide coverage and smaller microcells covering specific high-traffic spots (e.g., a street corner). A fast-moving user (in a car) passing through these microcells would trigger too many handoffs.

The **umbrella cell** approach solves this.
*   **High-speed users** are served by the large macrocell (the "umbrella").
*   **Low-speed (pedestrian) users** are served by the smaller microcells underneath.
*   The MSC directs handoffs for fast users to the umbrella cell to minimize the handoff rate, while slow users benefit from the high capacity of the microcells.

---

> [!check] ### Exam Focus & Key Takeaways
>
> **Potential Exam Questions:**
> 1.  "What is a handoff in a cellular system? Explain why it is essential for mobility management."
> 2.  "Differentiate between a hard handoff and a soft handoff, stating which multiple access technologies they are commonly associated with."
> 3.  "Describe the steps involved in a handoff process, explaining the role of the MSC and the importance of a hysteresis margin."
> 4.  "Explain the 'guard channel' concept and why handoff requests are often prioritized over new call requests."
>
> **Tips for Answering:**
> - Start with a clear, one-sentence definition of handoff.
> - Use the "break-before-make" (hard) vs. "make-before-break" (soft) analogy to clearly distinguish the two types.
> - When describing the process, mention the signal strength threshold and the hysteresis to show a deeper understanding.
> - For prioritization questions, focus on user experience: a dropped call is more annoying than a blocked call.
>
> **Key Takeaway:** Handoff is the dynamic process that ensures call continuity in a cellular network. The choice of handoff strategy (hard vs. soft) and the management of handoff requests are critical design decisions that impact network performance and user satisfaction.


