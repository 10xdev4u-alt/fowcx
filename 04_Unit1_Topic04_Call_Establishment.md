---
title: "Call Establishment in Cellular Systems"
id: "unit1-topic4-call-establishment"
tags: ["#cellular", "#callflow", "#moc", "#mtc", "#unit1"]
aliases: ["Cellular Call Flow"]
links: [[FOWC/00_Syllabus.md], [FOWC/02_Unit1_Topic02_SystemExamples.md]]
---

# UNIT I: Call Establishment in Cellular Systems

This section details the fundamental processes involved in establishing a call within a cellular communication network. Understanding these procedures is crucial for comprehending the operational dynamics of mobile telephony. Call establishment can be broadly categorized into two main types: Mobile Originated Call (MOC) and Mobile Terminated Call (MTC).

---

## 1. Introduction to Call Establishment

Call establishment refers to the sequence of signaling and resource allocation procedures that enable a communication link between two parties in a cellular network. This complex process involves interaction between the Mobile Station (MS), Base Station (BS), Mobile Switching Center (MSC), and various databases such as the Home Location Register (HLR) and Visitor Location Register (VLR).

---

## 2. Mobile Originated Call (MOC)

A Mobile Originated Call (MOC) occurs when a mobile subscriber initiates a call to another subscriber, who may be on the same cellular network, another mobile network, or a fixed-line (PSTN) network.

### 2.1. MOC Process Flow

The typical steps for an MOC are as follows:

1.  **Call Initiation:** The mobile user dials the destination number and presses the "send" button. The MS sends a **Channel Request** message to the nearest BS over the Random Access Channel (RACH).
2.  **Channel Assignment:** The BS receives the request and allocates a dedicated signaling channel (SDCCH) to the MS. The BS then forwards the **Setup** message (containing the dialed number) to the MSC.
3.  **Authentication and Authorization:** The MSC receives the Setup message. It then communicates with the VLR (Visitor Location Register) and HLR (Home Location Register) to authenticate the mobile subscriber and check their service subscriptions (e.g., sufficient balance, valid plan).
4.  **Call Routing:** If authentication is successful, the MSC analyzes the dialed number to determine the call's destination.
    *   If the destination is within the same MSC area, the MSC directly routes the call.
    *   If the destination is in another MSC area, another mobile network, or the PSTN, the MSC routes the call through the appropriate gateway (e.g., Gateway MSC for inter-network calls, PSTN gateway for fixed-line calls).
5.  **Alerting:** Once the destination is reached, the network sends an **Alerting** message back to the originating MS, indicating that the destination phone is ringing. Simultaneously, the destination phone begins to ring.
6.  **Traffic Channel Assignment:** When the destination party answers, the MSC assigns a dedicated traffic channel (TCH) for voice or data communication between the MS and the BS.
7.  **Conversation:** The communication link is established, and the conversation begins.
8.  **Call Release:** When either party hangs up, a **Release** message is sent through the network, and the assigned channels are deallocated.

### 2.2. MOC Signaling Diagram

```
+-----+     +-----+     +-----+     +-----+     +-----+
| MS  |     | BS  |     | MSC |     | VLR |     | HLR |
+-----+     +-----+     +-----+     +-----+     +-----+
   |           |           |           |           |
   |--Channel Request (RACH)-->|           |           |           |
   |           |           |           |           |
   |<--SDCCH Assignment----|           |           |           |
   |           |           |           |           |
   |--Setup (Dialed Number)-->|           |           |           |
   |           |           |           |           |
   |           |-----------Setup (Dialed Number)-->|           |
   |           |           |           |           |
   |           |           |<--Authentication Req----|           |
   |           |           |           |           |
   |           |           |----------Authentication Req-->|
   |           |           |           |           |
   |           |           |<--Authentication Resp---|           |
   |           |           |           |           |
   |           |           |-----------Authentication Resp-->|
   |           |           |           |           |
   |           |           |--Call Routing (to Destination)-->| (PSTN/Other MS)
   |           |           |           |           |
   |<--Alerting (Ringing)----|           |           |           |
   |           |           |           |           |
   |--Connect (Answer)------>|           |           |           |
   |           |           |           |           |
   |           |-----------Connect (Answer)-->|           |
   |           |           |           |           |
   |<--TCH Assignment------|           |           |           |
   |           |           |           |           |
   |<--------------------Conversation--------------------->|
   |           |           |           |           |
   |--Release (Hang Up)---->|           |           |           |
   |           |           |           |           |
   |<--Release Complete----|           |           |           |
   |           |           |           |           |
```
*ASCII Diagram: Mobile Originated Call (MOC) Flow.*

---

## 3. Mobile Terminated Call (MTC)

A Mobile Terminated Call (MTC) occurs when a call is placed to a mobile subscriber from another subscriber (mobile or fixed-line).

### 3.1. MTC Process Flow

The typical steps for an MTC are as follows:

1.  **Call Initiation:** A calling party (fixed-line or mobile) dials the mobile subscriber's number. The call is routed to the Gateway MSC (GMSC) of the mobile subscriber's home network.
2.  **Location Query:** The GMSC queries the HLR (Home Location Register) of the called mobile subscriber to determine their current location (i.e., which VLR they are currently registered with).
3.  **Routing Information Request:** The HLR, knowing the VLR where the MS is registered, requests a **Mobile Station Roaming Number (MSRN)** from that VLR. The MSRN is a temporary number used to route the call to the serving MSC.
4.  **Call Routing to Serving MSC:** The HLR provides the MSRN to the GMSC. The GMSC then routes the call to the serving MSC (the MSC associated with the VLR that provided the MSRN).
5.  **Paging:** The serving MSC initiates a **Paging** process. It sends a Paging Request message to all BSs within the location area where the MS was last registered. The BSs broadcast this message over the Paging Channel (PCH).
6.  **Paging Response:** The MS, upon receiving its unique identifier (IMSI/TMSI) in the Paging Request, responds to the serving BS over the RACH. This response confirms the MS's presence in the cell.
7.  **Channel Assignment:** The serving MSC assigns a dedicated signaling channel (SDCCH) to the MS.
8.  **Alerting:** The MSC sends an **Alerting** message to the MS, causing the mobile phone to ring.
9.  **Traffic Channel Assignment:** When the mobile subscriber answers, the MSC assigns a dedicated traffic channel (TCH) for communication.
10. **Conversation:** The communication link is established, and the conversation begins.
11. **Call Release:** When either party hangs up, a **Release** message is sent through the network, and the assigned channels are deallocated.

### 3.2. MTC Signaling Diagram

```
+-----+     +-----+     +-----+     +-----+     +-----+     +-----+
|Calling|     | GMSC|     | HLR |     | VLR |     | MSC |     | MS  |
| Party |     |     |     |     |     |     |     |     |     |     |
+-----+     +-----+     +-----+     +-----+     +-----+     +-----+
   |           |           |           |           |           |
   |--Call Setup (MSISDN)-->|           |           |           |           |
   |           |           |           |           |           |
   |           |--Location Query (MSISDN)-->|           |           |           |
   |           |           |           |           |           |
   |           |           |<--VLR Address (IMSI)----|           |           |
   |           |           |           |           |           |
   |           |           |--MSRN Request (IMSI)-->|           |           |
   |           |           |           |           |           |
   |           |           |<--MSRN Response (MSRN)--|           |           |
   |           |           |           |           |           |
   |           |<--MSRN (MSRN)-----------|           |           |           |
   |           |           |           |           |           |
   |           |--Call Setup (MSRN)------------------>|           |           |
   |           |           |           |           |           |
   |           |           |           |           |--Paging Request (PCH)-->|
   |           |           |           |           |           |
   |           |           |           |           |<--Paging Response (RACH)--|
   |           |           |           |           |           |
   |           |           |           |           |--SDCCH Assignment-->|
   |           |           |           |           |           |
   |           |           |           |           |--Alerting (Ringing)-->|
   |           |           |           |           |           |
   |           |           |           |           |<--Connect (Answer)----|
   |           |           |           |           |           |
   |           |           |           |           |--TCH Assignment-->|
   |           |           |           |           |           |
   |<--------------------------------Conversation--------------------------------->|
   |           |           |           |           |           |
   |--Release---------------------------------------------------------------->|
   |           |           |           |           |           |
```
*ASCII Diagram: Mobile Terminated Call (MTC) Flow.*

---

## 4. Key Network Elements Involved

*   **Mobile Station (MS):** The user's mobile phone, responsible for initiating and receiving calls.
*   **Base Station (BS):** Manages radio communication within a cell, handling signaling and traffic channels.
*   **Mobile Switching Center (MSC):** The central switching node that connects calls within the mobile network and to external networks (PSTN). It also manages mobility and call setup.
*   **Home Location Register (HLR):** A permanent database storing subscriber information (e.g., services, authentication keys) and the current VLR address of the mobile subscriber.
*   **Visitor Location Register (VLR):** A temporary database storing information about mobile subscribers currently roaming within its associated MSC's service area.

---

> [!check] ### Exam Focus & Key Takeaways
>
> **Potential Exam Questions:**
> 1.  "Describe the step-by-step process of a Mobile Originated Call (MOC) in a cellular network, illustrating with a signaling diagram."
> 2.  "Explain the procedure for a Mobile Terminated Call (MTC), detailing the roles of HLR and VLR in location management."
> 3.  "Identify and explain the functions of the primary network elements involved in cellular call establishment."
>
> **Tips for Answering:**
> - Clearly distinguish between MOC and MTC.
> - For process descriptions, use numbered lists for clarity.
> - Diagrams are highly recommended for illustrating signaling flows; ensure labels are clear.
> - Emphasize the interaction between different network entities (MS, BS, MSC, HLR, VLR).

This concludes the detailed explanation of call establishment procedures in cellular systems.
