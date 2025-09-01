# Lab 02 – Network Topologies

## Objective
Build and test three common network topologies in Cisco Packet Tracer. Compare strengths/weaknesses, and document workarounds for Packet Tracer limitations.

---

## 1. Star Topology
**Setup**
- 1 switch, 4 PCs
- Straight-through cables PC → Switch
- IPs:  
  - PC1: 192.168.2.1  
  - PC2: 192.168.2.2  
  - PC3: 192.168.2.3  
  - PC4: 192.168.2.4  

**Test**
- Ping PC1 → PC4 successful

**Pros**
- Simple to design and expand
- Easy to troubleshoot

**Cons**
- Single point of failure (the switch)

**Screenshot**
![IMG_0162](https://github.com/user-attachments/assets/2f8f6422-ab5a-4e03-9204-48c65d77f05a)


---

## 2. Mesh Topology (Simulated)
**Setup**
- 4 switches, 4 PCs
- Each PC connects to both switches
- Switches interconnected
- IPs:  
  - PC1: 10.0.0.1  
  - PC2: 10.0.0.2  
  - PC3: 10.0.0.3  
  - PC4: 10.0.0.4  

**Test**
- Ping PC1 → PC4  
- Deleted one switch link → traffic still worked (redundancy shown)

**Pros**
- High redundancy, resilient to failures

**Cons**
- Expensive, complex cabling
- In Packet Tracer, full mesh not possible due to single NIC per PC

**Screenshot**
![IMG_0163](https://github.com/user-attachments/assets/cc3da64a-2d48-4f3b-b83a-d5c26ad359b3)


---

## 3. Hub-and-Spoke Topology (Router + Switch Hub)
**Setup**
- 1 Router, 1 Switch, 3 PCs
- Router Fa0/0 → Switch (straight-through)
- PCs → Switch (straight-through)
- Router Fa0/0: 172.16.0.1  
- PC1: 172.16.0.2 (GW 172.16.0.1)  
- PC2: 172.16.0.3 (GW 172.16.0.1)  
- PC3: 172.16.0.4 (GW 172.16.0.1)  

**Test**
- Ping PC1 → PC2 successful via router
- Required CLI:

enable
configure terminal
interface fastethernet 0/0
no shutdown
exit

**Pros**
- Centralized control
- Easy to add/remove spokes

**Cons**
- Hub (router) is single point of failure
- Higher latency for spoke-to-spoke traffic

**Screenshot**
![IMG_0164](https://github.com/user-attachments/assets/1e56c692-e03c-418a-a5fa-279b90cefb99)


---

## Skills Learned
- Identifying and building common topologies  
- Correct cable selection (straight-through vs crossover)  
- Router interface configuration (`no shutdown`)  
- Pros/cons of star, mesh, hub-and-spoke  
- Documenting Packet Tracer limitations in real-world terms  
