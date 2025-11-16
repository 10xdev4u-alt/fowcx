---
title: FAT01 Answer Key - OE22708 Fundamentals of Wireless Communication
id: fat01-answers
tags: 
  - exam
  - answers
  - unit1
  - unit2
alias: 
  - FAT1 Answers
links: 
  - "[[OE-FAT01.md|FAT01 Question Paper]]"
---

# FAT01 Answer Key: OE22708 - Fundamentals of Wireless Communication

This document provides detailed answers for the FAT01 Question Paper.

## PART A (10 x 2 = 20 Marks)

### Q1. Highlight the advantages of wireless communication systems. (CO1, RBT Level 2)

Wireless communication systems offer several key advantages over wired systems:
1.  **Mobility:** Users can communicate while on the move, free from the physical constraints of cables.
2.  **Flexibility and Ease of Deployment:** Networks can be set up and reconfigured quickly without the need for extensive physical infrastructure (e.g., trenching for cables), making them ideal for temporary, remote, or difficult-to-wire locations.
3.  **Scalability:** Capacity can be increased and coverage expanded by adding more base stations or implementing advanced techniques like cell splitting.
4.  **Cost-Effectiveness:** For large coverage areas or difficult terrain, the cost of deploying a wireless network can be significantly lower than laying physical cables.

### Q2. Define a cell and cluster in cellular communications. (CO2, RBT Level 2)

*   **Cell:** A cell is the basic geographic unit of a cellular system. It represents the area of radio coverage provided by a single base station. A mobile user within a cell communicates with the network through that cell's base station.
*   **Cluster:** A cluster is a group of adjacent cells in which each cell is allocated a unique set of frequencies. The total number of available frequencies in the system is divided among the cells of a single cluster. This entire cluster pattern is then repeated across the service area to implement frequency reuse.

### Q3. Compare hard and soft handoffs. (CO2, RBT Level 2)

| Feature             | Hard Handoff                               | Soft Handoff                                     |
| :------------------ | :----------------------------------------- | :----------------------------------------------- |
| **Connection**      | "Break-Before-Make"                        | "Make-Before-Break"                              |
| **Mechanism**       | The connection to the old cell is dropped *before* a new connection is established with the new cell. | A new connection is established with the new cell *before* the old connection is dropped. |
| **Simultaneous Links** | Connected to only one base station at a time. | Connected to two or more base stations simultaneously for a brief period. |
| **Technology**      | Used in TDMA and FDMA systems (e.g., GSM). | Used in CDMA systems (e.g., IS-95, UMTS).        |
| **Reliability**     | Less reliable; has a higher chance of dropped calls during the handoff instant. | More reliable; provides seamless transition and diversity gain from multiple links. |

### Q4. Give examples of simplex, half duplex and full duplex systems. (CO1, RBT Level 4)

*   **Simplex:** Communication is strictly one-way.
    *   **Example:** Commercial radio/TV broadcasting, Pagers.
*   **Half Duplex:** Communication is two-way, but not simultaneous. Only one party can transmit at a time.
    *   **Example:** Walkie-talkies (Push-to-Talk systems).
*   **Full Duplex:** Communication is two-way and simultaneous. Both parties can transmit and receive at the same time.
    *   **Example:** Cellular telephones, standard telephone calls.

### Q5. Write the formula to determine the cluster size of a cell. (CO2, RBT Level 4)

For a hexagonal cell geometry, the cluster size, N, can only have values that satisfy the following equation:
$$ N = i^2 + ij + j^2 $$
Where `i` and `j` are non-negative integers that represent the shift parameters used to find the nearest co-channel cell.

### Q6. Define the terms FVC and RVC. (CO1, RBT Level 2)

*   **FVC (Forward Voice Channel):** The voice channel used for transmission from the **base station to the mobile station**. It carries the voice data for the user to hear.
*   **RVC (Reverse Voice Channel):** The voice channel used for transmission from the **mobile station to the base station**. It carries the voice data from the user speaking into their phone.

### Q7. Compare and contrast Cordless and Paging Systems. (CO1, RBT Level 2)

| Feature             | Cordless System                            | Paging System                              |
| :------------------ | :----------------------------------------- | :----------------------------------------- |
| **Communication**   | Two-way, full-duplex voice communication. | One-way, simplex message transmission.     |
| **Mobility**        | Localized mobility (tens of meters) around a private base unit. | Wide-area mobility (receive-only) across a public network. |
| **Network**         | Connects to the PSTN via a private, user-owned base unit. | Connects to a public network designed for broadcasting messages. |
| **Primary Use**     | To provide a wireless extension to a landline phone at home or in an office. | To deliver urgent, short messages (alerts, numbers, text) to a mobile user. |

### Q8. Why hexagonal geometry is considered for the shape of a cell? (CO2, RBT Level 4)

Hexagonal geometry is used for cellular layout for two main reasons:
1.  **Perfect Tessellation:** Hexagons can be placed adjacent to each other to cover a geographic area completely, without any gaps or overlapping regions. Circles would leave gaps, and squares, while they tessellate, are not as good a fit for radio propagation.
2.  **Approximation of a Circle:** The radiation pattern of an omnidirectional antenna is circular. A hexagon is the geometric shape that most closely approximates a circle while still offering perfect tessellation. This provides a more realistic model for coverage compared to a square.

### Q9. Brief the Components of personal communication services. (CO1, RBT Level 2)

Personal Communication Services (PCS) are built on three core conceptual components or objectives:
1.  **Personal Mobility:** The ability for a user to access their telecommunication services at any terminal based on a personal identifier (e.g., a phone number or user ID), regardless of their location or the specific device being used.
2.  **Terminal Mobility:** The ability for a terminal (e.g., a mobile phone) to access services from different locations, even while in motion. This is the classic cellular concept enabled by handoffs.
3.  **Service Portability:** The ability for a user to access the same set of services with a consistent quality of service, regardless of the network or terminal they are using (e.g., accessing voicemail from a different phone).

### Q10. Find the cluster size and co-channel reuse factor for i=2 and j=2. (CO2, RBT Level 4)

**1. Cluster Size (N):**
The formula for cluster size is:
$$ N = i^2 + ij + j^2 $$
Substituting i=2 and j=2:
$$ N = (2)^2 + (2)(2) + (2)^2 = 4 + 4 + 4 = 12 $$
The cluster size is **12**.

**2. Co-channel Reuse Factor (Q):**
The formula for the co-channel reuse factor (also called co-channel reuse ratio) is:
$$ Q = \sqrt{3N} $$
Substituting N=12:
$$ Q = \sqrt{3 \times 12} = \sqrt{36} = 6 $$
The co-channel reuse factor is **6**.

---

## PART B (3 x 10 = 30 Marks)

### Q11(a). Compare various generations of Wireless Communication Systems. (CO1, RBT Level 3)

**Introduction**
The evolution of wireless communication is marked by distinct "generations," each representing a significant technological leap in network capabilities, speed, and services offered. This comparison covers the first five generations, from 1G to 5G.

| Feature             | 1G (First Generation) | 2G (Second Generation) | 3G (Third Generation) | 4G (Fourth Generation) | 5G (Fifth Generation) |
| :------------------ | :-------------------- | :--------------------- | :-------------------- | :--------------------- | :-------------------- |
| **Time Period**     | ~1980s                | ~1990s                 | ~2000s                | ~2010s                 | ~2020s                |
| **Core Technology** | Analog (FM)           | Digital                | Digital (Wideband)    | All-IP Network         | New Radio (NR), mmWave |
| **Primary Service** | Voice Calls           | Voice, SMS, basic data | Mobile Internet       | Mobile Broadband       | IoT, AR/VR, URLLC     |
| **Multiplexing**    | FDMA                  | TDMA / CDMA            | W-CDMA / CDMA2000     | OFDMA                  | OFDMA / Flexible Numerology |
| **Data Speeds**     | ~2.4 kbps             | ~64-144 kbps (EDGE)    | ~2 Mbps (up to 21 Mbps) | ~100 Mbps - 1 Gbps     | ~1-10+ Gbps           |
| **Key Feature**     | First mobile voice    | Digital encryption, SIM card, SMS | Video calling, mobile web | HD video streaming, VoLTE | Ultra-low latency, massive connectivity |
| **Switching**       | Circuit-Switched      | Circuit (Voice) & Packet (Data) | Circuit & Packet      | All Packet-Switched    | All Packet-Switched   |

**Conclusion**
The progression from 1G to 5G shows a clear evolution from analog voice-only systems to highly complex, all-IP digital networks designed for a vast ecosystem of data-centric services. Each generation built upon the last, driven by the demand for higher speeds, greater capacity, and new applications beyond simple voice communication.

### Q11(b). Compare different kinds of wireless systems with relevant diagrams. (CO1, RBT Level 3)

**Introduction**
Wireless systems can be broadly categorized based on their architecture, mobility support, and primary application. The three primary examples are Cordless, Paging, and Cellular systems.

**Comparison Table**

| Feature             | Cordless System                            | Paging System                              | Cellular System                            |
| :------------------ | :----------------------------------------- | :----------------------------------------- | :----------------------------------------- |
| **Communication**   | Two-way, full-duplex voice.                | One-way, simplex messaging.                | Two-way, full-duplex voice and data.       |
| **Mobility**        | Localized (tens of meters) around a base unit. | Wide-area, receive-only mobility.          | Full wide-area mobility with handoffs.     |
| **Network**         | Private base unit connected to PSTN.       | Public broadcast network.                  | Public network of interconnected cells (BS) and switches (MSC). |
| **Handoff**         | Not supported.                             | Not applicable.                            | Supported (seamless call transfer).        |
| **Primary Use**     | Wireless landline extension in a home/office. | Urgent, one-way alerts and messages.       | Ubiquitous mobile voice and data communication. |

**Diagrams**

1.  **Cordless System Architecture:**
    ```
          +-------------------+
          |     PSTN (Wired)  |
          +---------+---------+
                    | (Landline)
          +---------v---------+
          |    Base Unit      | <--- Radio Link (Short Range) ---> +----------+
          +-------------------+                                    | Handset  |
                                                                   +----------+
    ```

2.  **Paging System Architecture:**
    ```
      (Message Input) --> +-----------------+
                          | Paging Terminal |
                          +--------+--------+
                                   |
                          +--------v--------+
                          | Paging Network  |
                          +--------+--------+
                                   |
          +------------------------+------------------------+
          |                        |                        |
    +-----v----+             +-----v----+             +-----v----+
    |   BS 1   |             |   BS 2   |             |   BS n   |
    +----------+             +----------+             +----------+
          \                        |                        /
           \                       |                       /
            \                      |                      /
             +---------------------v---------------------+
                               +-------+
                               | Pager |
                               +-------+
    ```

3.  **Cellular System Architecture:**
    ```
                               +----------------+
                               |      PSTN      |
                               +-------+--------+
                                       |
                               +-------v--------+
                               |      MSC       | (Mobile Switching Center)
                               +-------+--------+
                                       |
          +----------------------------+----------------------------+
          |                            |                            |
    +-----v----+                   +-----v----+                   +-----v----+
    |   BS 1   | <--- Air ---> MS  |   BS 2   |                   |   BS 3   |
    | (Cell 1) | (Mobile Station)  | (Cell 2) |                   | (Cell 3) |
    +----------+                   +----------+                   +----------+
    ```

**Conclusion**
These three systems highlight the diverse applications of wireless technology. Cordless systems offer local convenience, paging systems provide high-reliability one-way alerts, and cellular systems deliver the ultimate goal of ubiquitous, two-way mobile communication through a complex, intelligent network architecture.

### Q12(a). If a total of 33 MHz of bandwidth is allocated... compute the number of channels available per cell...

**1. Calculate Total Channels Available**
*   Total allocated bandwidth = 33 MHz.
*   The system is FDD (Frequency Division Duplex), so the bandwidth is split equally for forward and reverse links.
    *   Bandwidth for one direction (e.g., forward link) = 33 MHz / 2 = 16.5 MHz.
*   Each simplex channel requires 25 kHz.
*   Total number of simplex channels available in one direction = 16.5 MHz / 25 kHz = 16,500,000 Hz / 25,000 Hz = **660 channels**.

**2. Separate Control and Voice Channels**
*   Spectrum for control channels = 1 MHz.
*   Number of control channels = 1 MHz / 25 kHz = 1,000,000 Hz / 25,000 Hz = **40 control channels**.
*   Number of voice channels = Total channels - Control channels = 660 - 40 = **620 voice channels**.

**3. Distribute Channels per Cell for Different Reuse Patterns**

**(a) 4-Cell Reuse (N=4)**
*   **Control Channels per Cell:** 40 control channels / 4 cells = **10 control channels per cell**.
*   **Voice Channels per Cell:** 620 voice channels / 4 cells = **155 voice channels per cell**.

**(b) 7-Cell Reuse (N=7)**
*   **Control Channels per Cell:** 40 control channels / 7 cells ≈ 5.71.
    *   We can give **5 control channels** to each of the 7 cells (totaling 35). The remaining 5 channels (40-35) can be distributed one each to 5 of the 7 cells. So, 5 cells will have 6 control channels, and 2 cells will have 5.
*   **Voice Channels per Cell:** 620 voice channels / 7 cells ≈ 88.57.
    *   We can give **88 voice channels** to each cell (totaling 616). The remaining 4 channels (620-616) can be distributed one each to 4 of the 7 cells. So, 4 cells will have 89 voice channels, and 3 cells will have 88.

**(c) 12-Cell Reuse (N=12)**
*   **Control Channels per Cell:** 40 control channels / 12 cells ≈ 3.33.
    *   **3 control channels** per cell (totaling 36). The remaining 4 channels can be given one each to 4 of the 12 cells.
*   **Voice Channels per Cell:** 620 voice channels / 12 cells ≈ 51.67.
    *   **51 voice channels** per cell (totaling 612). The remaining 8 channels can be given one each to 8 of the 12 cells.

**Summary of Results**

| Reuse Pattern | Control Channels per Cell (Approx.) | Voice Channels per Cell (Approx.) |
| :------------ | :---------------------------------- | :-------------------------------- |
| **N = 4**     | 10                                  | 155                               |
| **N = 7**     | 5-6                                 | 88-89                             |
| **N = 12**    | 3-4                                 | 51-52                             |

### Q12(b). State the principle of cellular communications and explain how it can be adopted to maximize number of customers in a cellular system. Show illustrations.

**Principle of Cellular Communications**
The fundamental principle of cellular communication is to solve the problem of limited spectrum and high user demand by replacing a single, high-power transmitter with many low-power transmitters. A large geographic service area is broken down into smaller, manageable areas called **cells**. Each cell is served by its own base station. By using low-power transmitters, the same set of frequencies can be reused in different cells that are geographically separated, a concept known as **frequency reuse**.

**Maximizing Customers with Frequency Reuse**
The key to maximizing the number of customers is **frequency reuse**.

1.  **Cellular Concept:** The service area is divided into a grid of hexagonal cells.
2.  **Clusters:** These cells are grouped into clusters (e.g., a cluster of N=7 cells). Within a cluster, each cell is assigned a unique set of frequency channels.
3.  **Reuse:** The entire cluster pattern, with its specific frequency allocation, is then repeated throughout the service area. Cells that are sufficiently far apart can use the same set of frequencies without causing significant interference. This distance is called the co-channel reuse distance (D).

**Illustration**
The diagram below shows a 7-cell reuse pattern. The cluster consists of cells labeled A, B, C, D, E, F, G. Each letter represents a unique set of frequencies. This entire 7-cell pattern is then repeated. Notice that cells with the same letter (co-channel cells) are separated by a significant distance.

```
                +-------+
              /         \
      +-------+    G    +-------+
    /         \         /         \
   +     F     +-------+     F     +
   |           |       |           |
   +     G     +   A   +     G     +
   |           |       |           |
   +     A     +-------+     A     +
    \         /         \         /
      +-------+    B    +-------+
    /         \         /         \
   +     B     +-------+     B     +
   |           |       |           |
   +     C     +   D   +     C     +
   |           |       |           |
   +     D     +-------+     D     +
    \         /         \         /
      +-------+    E    +-------+
              \         /
                +-------+
```
*Figure: A repeating 7-cell cluster pattern (N=7) demonstrating frequency reuse.*

**Conclusion**
By reusing frequencies, a limited number of channels can support a vast number of simultaneous users across a large city. If a single cell with `k` channels is reused `M` times, the total system capacity becomes `M * k` channels. This principle allows cellular systems to serve millions of customers, a feat impossible with a single high-power transmitter.

### Q13(a). Illustrate using timing diagram how call to a mobile user is initiated from a landline subscriber.

This describes a **Mobile Terminated Call (MTC)**. The process involves finding the mobile user and routing the call to their current location.

**Signaling Diagram: Landline-to-Mobile Call (MTC)**
```
+-------+   +------+   +-----+   +-----+   +-----+   +-----+   +----+
| PSTN  |   | GMSC |   | HLR |   | VLR |   | MSC |   | BS  |   | MS |
+-------+   +------+   +-----+   +-----+   +-----+   +-----+   +----+
    |           |          |         |         |         |        |
1. Call Setup (MSISDN)-->|          |         |         |         |        |
    |           |          |         |         |         |        |
    |     2. Location Query (MSISDN)-->|         |         |         |
    |           |          |         |         |         |        |
    |           |   3. MSRN Request (IMSI)-->|         |         |
    |           |          |         |         |         |        |
    |           |          |   4. MSRN Response (MSRN)-->|         |
    |           |          |         |         |         |        |
    |           |<--5. MSRN---|         |         |         |
    |           |          |         |         |         |        |
    |     6. Call Setup (MSRN)---------------------->|         |
    |           |          |         |         |         |        |
    |           |          |         |         |  7. Paging Request-->|
    |           |          |         |         |         |        |
    |           |          |         |         |         |  8. Paging (PCH)-->|
    |           |          |         |         |         |        |
    |           |          |         |         |         |<--9. Paging Resp--|
    |           |          |         |         |         |        |
    |           |          |         |         |         |  10. Authentication & Setup |
    |           |          |         |         |         |        |
    |           |          |         |         |         |  11. Alerting----->|
    |           |          |         |         |         |        |
    |           |          |         |         |         |<--12. Connect-----|
    |           |          |         |         |         |        |
    |           |          |         |         |         |  13. TCH Assignment-->|
    |           |          |         |         |         |        |
    |<------------------------- 14. Conversation -------------------------->|
    |           |          |         |         |         |        |
```
**Explanation of Steps:**
1.  A landline user dials the mobile's number (MSISDN). The call is routed via the Public Switched Telephone Network (PSTN) to the mobile network's Gateway MSC (GMSC).
2.  The GMSC queries the Home Location Register (HLR) to find the mobile's current location.
3.  The HLR knows which Visitor Location Register (VLR) the mobile is currently in and requests a temporary routing number, the Mobile Station Roaming Number (MSRN), from that VLR.
4.  The VLR provides the MSRN to the HLR.
5.  The HLR forwards the MSRN to the GMSC.
6.  The GMSC uses the MSRN to route the call to the correct serving MSC.
7.  The serving MSC sends a Paging Request to all Base Stations (BS) in the mobile's last known location area.
8.  The BSs broadcast a page for the Mobile Station (MS) on the Paging Channel (PCH).
9.  The MS responds to the page, confirming its location and readiness.
10. The MSC performs authentication and sets up the call.
11. The MSC sends an Alerting message, causing the mobile phone to ring.
12. The mobile user answers, sending a Connect message back.
13. The MSC assigns a Traffic Channel (TCH) for the voice call.
14. The conversation begins.

### Q13(b). Illustrate using timing diagram how call to a mobile user is initiated from a mobile subscriber.

This describes a **Mobile Originated Call (MOC)**. The process involves the calling mobile first connecting to the network, which then routes the call to the destination (which could be another mobile or a landline).

**Signaling Diagram: Mobile-to-Mobile Call (MOC)**
```
+-----+   +----+   +-----+   +-----+   +-----+   +------+   +-------+
| MS A|   |BS A|   |MSC A|   |VLR A|   |HLR A|   | GMSC |   | Dest. |
|(Orig)|   |    |   |     |   |     |   |     |   |      |   |Network|
+-----+   +----+   +-----+   +-----+   +-----+   +------+   +-------+
   |         |        |         |         |          |           |
1. Channel Request-->|        |         |         |          |           |
   |         |        |         |         |          |           |
   |<--2. Channel Assign--|        |         |         |          |           |
   |         |        |         |         |          |           |
3. Setup (Dialed Num)-->|        |         |         |          |           |
   |         |        |         |         |          |           |
   |   4. Setup------>|        |         |          |           |
   |         |        |         |         |          |           |
   |         |  5. Authenticate & Authorize |         |          |           |
   |         |        |<------->|         |          |           |
   |         |        |         |<------->|          |           |
   |         |        |         |         |          |           |
   |         |  6. Route Call---------------------->|           |
   |         |        |         |         |          |           |
   |         |        |         |         |          |  (MTC Flow) |
   |         |        |         |         |          |<----------->|
   |         |        |         |         |          |           |
   |<--7. Alerting------|        |         |          |           |
   |         |        |         |         |          |           |
   |         |  8. Connect (Answer from Dest.)      |          |           |
   |         |<---------------------------------------------------|
   |         |        |         |         |          |           |
   |<--9. TCH Assign---|        |         |          |           |
   |         |        |         |         |          |           |
   |<-------------------- 10. Conversation ---------------------->|
   |         |        |         |         |          |           |
```
**Explanation of Steps:**
1.  The originating Mobile Station (MS A) sends a Channel Request to its Base Station (BS A).
2.  BS A allocates a signaling channel and informs MS A.
3.  MS A sends a Setup message containing the dialed number.
4.  BS A forwards the Setup message to its serving MSC (MSC A).
5.  MSC A interacts with its VLR (VLR A) and the user's HLR (HLR A) to authenticate the subscriber and authorize the call (e.g., check account balance).
6.  Once authorized, MSC A analyzes the dialed number. It sees the number belongs to another mobile user and routes the call to the appropriate Gateway MSC (GMSC) to begin the Mobile Terminated Call (MTC) process for the destination user.
7.  **The MTC process (as described in Q13a) now occurs for the destination user.** Once the destination network sends back an indication that the called phone is ringing, MSC A sends an Alerting message to the originating MS A.
8.  When the destination user answers, a Connect message is relayed back to MSC A.
9.  MSC A assigns a Traffic Channel (TCH) to MS A for the voice call.
10. The end-to-end conversation link is established.