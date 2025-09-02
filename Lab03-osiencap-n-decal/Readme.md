# Lab 03 – OSI Encapsulation and Decapsulation

## Objective
Visualize how data moves through the OSI model by using Packet Tracer’s Simulation mode during a ping test.

---

## Topology
- 2 PCs connected to a switch with straight-through cables
- IPs:
  - PC0: 192.168.10.1
  - PC1: 192.168.10.2

---

## Steps
1. Built topology in Packet Tracer.
2. Assigned static IPs to both PCs.
3. Switched to **Simulation Mode**.
4. From PC0, ran:
ping 192.168.10.2
5. Captured packets as they moved through the network.
6. Opened **PDU Details → OSI Model tab** to see each encapsulation step.

---

## Encapsulation Example (PC0 sending)
- **Application Layer (L7):** Ping request created (ICMP echo).
- **Transport Layer (L4):** Data segmented.
- **Network Layer (L3):** IP header added (src: 192.168.10.1, dst: 192.168.10.2).
- **Data Link Layer (L2):** Ethernet frame header with MAC addresses.
- **Physical Layer (L1):** Frame converted into bits/electrical signals.

---

## Decapsulation Example (PC1 receiving)
- **L1:** Bits arrive on NIC.
- **L2:** Frame reassembled, MAC checked.
- **L3:** IP header verified (192.168.10.2 is destination).
- **L4:** ICMP segment processed.
- **L7:** Application delivers ping reply to user.

---

## Results
- Packets successfully sent and received.
- Event list showed the full journey (PC0 → Switch0 → PC1).
- PDU details confirmed headers were added/removed at each layer.

---

## Screenshot
![IMG_0165](https://github.com/user-attachments/assets/bb052119-f086-4f6e-a5da-0030897f5642)
_Encapsulation and decapsulation shown step-by-step._

---

## Skills Learned
- Used Simulation mode to analyze packets.
- Observed encapsulation (headers added at each layer).
- Observed decapsulation (headers removed at each layer).
- Linked theory of OSI to a real packet exchange.
