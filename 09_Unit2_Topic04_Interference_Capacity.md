---
title: "Interference and System Capacity"
id: "unit2-topic4-interference-capacity"
tags: ["#cellular", "#interference", "#capacity", "#co_channel", "#adjacent_channel", "#unit2"]
aliases: ["Cellular Interference", "System Capacity"]
links: [[FOWC/00_Syllabus.md], [FOWC/06_Unit2_Topic01_Frequency_Reuse.md]]
---

# UNIT II: Interference and System Capacity

This section details the various forms of interference in cellular systems and their impact on overall system capacity. It also covers techniques used to improve both coverage and capacity.

---

## 1. Introduction to Interference

**Interference** is the primary limiting factor in the performance of cellular radio systems. It occurs when unwanted signals disrupt the reception of the desired signal. In a cellular environment, interference can originate from various sources, both within and outside the system.

Interference leads to:
*   Dropped calls.
*   Blocked calls.
*   Poor voice quality.
*   Reduced data rates.

There are two main types of interference in cellular systems:

### 1.1. Co-Channel Interference (CCI)

**Co-Channel Interference (CCI)** occurs between cells that use the same set of frequencies (co-channels). As discussed in Frequency Reuse, these cells are geographically separated to minimize interference, but it cannot be entirely eliminated.

*   **Source:** Base stations or mobile stations in different cells operating on the same frequency.
*   **Impact:** Directly limits the system capacity and the quality of communication.
*   **Mitigation:** Primarily managed by increasing the frequency reuse distance (D) or, equivalently, increasing the cluster size (N). A larger N reduces CCI but also reduces the number of channels per cell.

The Signal-to-Interference Ratio (SIR) is a key metric for evaluating CCI, as previously discussed:

$$
\frac{S}{I} = \frac{(\sqrt{3N})^n}{i_0}
$$

Where:
*   **S/I** is the Signal-to-Interference Ratio.
*   **N** is the cluster size.
*   **n** is the path loss exponent.
*   **i_0** is the number of first-tier interfering cells (typically 6).

### 1.2. Adjacent Channel Interference (ACI)

**Adjacent Channel Interference (ACI)** occurs when signals from channels adjacent in frequency to the desired channel interfere with the receiver. This happens due to imperfect receiver filters that cannot completely suppress strong signals from adjacent channels.

*   **Source:** Transmitters (base stations or mobile stations) operating on frequencies close to the desired channel, typically in adjacent cells or even within the same cell.
*   **Impact:** Can cause significant degradation in signal quality, especially if the adjacent channel signal is much stronger than the desired signal.
*   **Mitigation:**
    *   **Careful Frequency Planning:** Assigning adjacent channels to cells that are far apart.
    *   **Improved Filter Design:** Using highly selective filters in receivers to better reject adjacent frequencies.
    *   **Power Control:** Reducing the transmit power of mobile stations and base stations to the minimum required level.

```
+-------------------------------------------------+
|                                                 |
|   Cell 1 (Freq F1)      Cell 2 (Freq F2)        |
|   (Desired Signal)      (Adjacent Channel)      |
|                                                 |
|   +-----+                 +-----+               |
|   | BS1 |                 | BS2 |               |
|   +-----+                 +-----+               |
|      |                       |                   |
|      | F1 (Strong)           | F2 (Strong)       |
|      v                       v                   |
|   +-------------------------------------------+  |
|   | Mobile Station (Receiving F1, but F2 leaks)|  |
|   +-------------------------------------------+  |
|                                                 |
+-------------------------------------------------+
```
*ASCII Diagram: Illustration of Adjacent Channel Interference. Mobile Station receives F1, but strong F2 from BS2 leaks into the receiver due to imperfect filtering.*

---

## 2. System Capacity

**System Capacity** in cellular networks refers to the maximum number of users or calls that a system can support simultaneously while maintaining a specified Quality of Service (QoS). Interference is the primary factor limiting capacity.

### 2.1. Factors Affecting Capacity

*   **Frequency Reuse Factor (1/N):** A smaller cluster size (N) means more frequent reuse of channels, leading to higher capacity but also higher CCI.
*   **Signal-to-Interference Ratio (SIR):** A higher SIR requirement (for better QoS) often necessitates a larger N, which reduces capacity.
*   **Number of Available Channels:** The total spectrum allocated to the system.
*   **Traffic Intensity:** The average number of call requests per unit time.
*   **Blocking Probability:** The percentage of calls that are denied due to lack of available channels.

### 2.2. Improving Coverage and Capacity in Cellular Systems

To meet the ever-increasing demand for wireless services, various techniques are employed to improve both coverage (the geographical area where service is available) and capacity (the number of users served).

#### 2.2.1. Cell Splitting

**Cell Splitting** is the process of dividing a large cell into smaller cells, each with its own base station and a reduced transmit power.

*   **Mechanism:** When traffic density increases in a particular area, existing cells are split into smaller microcells or picocells.
*   **Impact:**
    *   **Increases Capacity:** By reducing the cell radius (R), the frequency reuse distance (D) also effectively decreases, allowing for more frequent reuse of channels in a given area. This means more base stations can be deployed, increasing the total number of channels available.
    *   **Maintains SIR:** While R decreases, D also decreases proportionally, so the D/R ratio (and thus SIR) can be maintained if the cluster size N is kept constant.
    *   **Handoff Rate:** Increases the number of handoffs due to smaller cell sizes.
    *   **Cost:** Requires more base stations, increasing infrastructure cost.

```
      Original Large Cell
      +-----------------+
      |                 |
      |       BS        |
      |                 |
      +-----------------+
              |
              v
      Split into Smaller Cells
      +---+---+---+
      |BS1|BS2|BS3|
      +---+---+---+
      |BS4|BS5|BS6|
      +---+---+---+
      |BS7|BS8|BS9|
      +---+---+---+
```
*ASCII Diagram: Cell Splitting. A large cell is divided into multiple smaller cells, each with its own Base Station (BS).*

#### 2.2.2. Sectoring

**Sectoring** involves dividing a single omnidirectional cell into several directional sectors, typically 3 (120°) or 6 (60°), using directional antennas at the base station.

*   **Mechanism:** Instead of an omnidirectional antenna radiating power in all directions, directional antennas focus power into specific sectors.
*   **Impact:**
    *   **Reduces Interference:** By directing radiation, interference to co-channel cells in other directions is reduced. This improves the SIR.
    *   **Increases Capacity:** With reduced interference, the frequency reuse factor can be improved (i.e., a smaller cluster size N can be used), thereby increasing capacity.
    *   **Cost:** Less expensive than cell splitting as it uses the same base station location.
    *   **Handoff Rate:** Does not significantly increase the handoff rate within the cell, but may increase inter-sector handoffs.

```
      Omnidirectional Cell
      +-----------------+
      |       BS        |
      |       (O)       |
      +-----------------+
              |
              v
      3-Sector Cell
      +-------+-------+
      |   /|\   /|\   |
      |  / | \ / | \  |
      | /  |  X  |  \ |
      |/   |   \|   \|
      +----+----+----+
      |    BS (X)    |
      +----+----+----+
      |\   |   /|\   /|
      | \  |  / | \  / |
      |  \|/   \|/   |
      +-------+-------+
```
*ASCII Diagram: Sectoring. An omnidirectional cell is divided into three 120-degree sectors using directional antennas at the central Base Station (BS).*

#### 2.2.3. Repeaters for Range Extensions

**Repeaters** are devices that receive signals from a base station or mobile station, amplify them, and retransmit them to extend coverage into areas that would otherwise have poor signal strength (e.g., tunnels, basements, shadow regions).

*   **Mechanism:** A repeater acts as a bidirectional amplifier. It does not perform any switching or channel assignment functions.
*   **Impact:**
    *   **Extends Coverage:** Fills in coverage holes and extends the range of existing cells.
    *   **Cost-Effective:** A relatively inexpensive way to improve coverage compared to deploying a full base station.
    *   **No Capacity Increase:** Repeaters do not add new channels; they merely extend the reach of existing channels.

#### 2.2.4. Microcell Zone Concept

The **Microcell Zone Concept** is an advanced form of cell splitting where a cell is divided into several microcell zones, each with its own zone antenna. All zone antennas are connected to a single base station.

*   **Mechanism:** Instead of multiple independent base stations (as in cell splitting), a single base station controls multiple geographically distributed antennas (zones).
*   **Impact:**
    *   **Increases Capacity:** Similar to cell splitting, by effectively reducing the cell size and allowing for more frequent reuse.
    *   **Reduced Handoff Rate:** Since all zones are connected to the same base station, handoffs between zones within the microcell are handled locally by the base station, reducing the load on the MSC and the number of inter-cell handoffs.
    *   **Improved SIR:** By having antennas closer to the mobile, transmit power can be reduced, leading to lower interference.

---

> [!check] ### Exam Focus & Key Takeaways
>
> **Potential Exam Questions:**
> 1.  "Differentiate between co-channel interference and adjacent channel interference, and explain their respective mitigation techniques."
> 2.  "Explain the concept of cell splitting and how it improves system capacity. Discuss its advantages and disadvantages."
> 3.  "Describe sectoring and the microcell zone concept as methods to enhance cellular system performance, comparing their mechanisms and benefits."
> 4.  "How does interference limit the capacity of a cellular system? Discuss various techniques used to improve both coverage and capacity."
>
> **Tips for Answering:**
> - Clearly define each type of interference and its source.
> - For capacity improvement techniques, explain the mechanism, how it impacts capacity/coverage, and any trade-offs (e.g., cost, handoff rate).
> - Use diagrams to illustrate cell splitting and sectoring.
> - Remember that interference is the *limiting factor* for capacity.
>
> **Key Takeaway:** Managing interference is paramount for maximizing cellular system capacity. Techniques like cell splitting, sectoring, repeaters, and microcell zones are crucial tools for network planners to optimize coverage and capacity in response to growing user demand.
