# Lab 01 - Basic LAN Setup

## Objective
Create a simple local area network (LAN) in Cisco Packet Tracer to connect two PCs and verify connectivity.

## Topology
- 2 PCs connected via copper crossover cable
- Static IP addressing

## Steps
1. Add two PCs in Packet Tracer workspace
2. Connect PC → PC using a copper crossover cable (FastEthernet0)
3. Configure IP addresses:
   - PC1: 192.168.1.1 / 255.255.255.0
   - PC2: 192.168.1.2 / 255.255.255.0
4. Test connectivity:
   - From PC1, open Command Prompt → `ping 192.168.1.2`
   - From PC2, `ping 192.168.1.1`

## Expected Result
Both PCs should successfully ping each other, confirming the LAN is operational.

## Skills Learned
- Cable selection (crossover vs straight-through)
- Static IP configuration
- Basic connectivity testing with `ping`

## Screenshot
_Add a screenshot of your Packet Tracer topology and ping results here._![IMG_0161](https://github.com/user-attachments/assets/38b788e9-41cb-4f9b-8a98-de4c5da0271c)
