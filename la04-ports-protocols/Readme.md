# Lab 04 – Ports and Protocols

## Objective
Understand how different network services use specific ports and how this traffic appears across the OSI model.

---

## Topology
- Two PCs connected via a switch
- Static IPs:
  - PC0: 192.168.20.1
  - PC1: 192.168.20.2

---

## Steps
1. Built a two-PC network in Packet Tracer.
2. From PC0, attempted to connect to PC1 using:
   - FTP
   - Telnet
   - SSH
3. Switched to **Simulation Mode** to capture packets.
4. Observed OSI layer encapsulation and decapsulation for each protocol.

---

## Results
- **FTP (TCP 21):** Successful connection, traffic captured. Packets encapsulated from Layer 4 (Transport) down to Layer 1 (Physical).  
- **Telnet (TCP 23):** Connection attempted but closed — no Telnet service running on PC1.  
- **SSH (TCP 22):** Unsupported on Packet Tracer PCs without extra device configuration, command returned invalid.  

---

## Screenshots
![IMG_0166](https://github.com/user-attachments/assets/07f90910-89ae-412a-b7de-4208225d9b31)
- FTP connection and packet details showing OSI layers.
- Simulation panel event list during FTP session.

---

## Notes on Simulation Limitations
- Packet Tracer simulates some protocols fully (like FTP) but not others (Telnet, SSH) unless configured on routers/switches.
- Real-world networks require services running on the destination device for these connections to succeed.

---

## Skills Learned
- Identified well-known ports for FTP, Telnet, and SSH.
- Saw how protocol traffic encapsulates at the Transport layer before moving down the OSI stack.
- Recognized simulation limitations vs. real-world behavior.
