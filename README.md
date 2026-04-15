
🚀 Cisco Packet Tracer - Dynamic Routing Labs

This repository features three distinct network architectures built in Cisco Packet Tracer, demonstrating the implementation of the primary dynamic routing protocols: RIPv2, OSPF, and EIGRP.
📋 Project Overview
![Capture d'écran du projet](image.png)

The objective is to establish Full Mesh connectivity between multiple Local Area Networks (LANs) through an infrastructure of routers interconnected via serial links (using /30 subnets).
🛠️ Technologies Used

    Software: Cisco Packet Tracer

    Protocols: RIPv2, OSPF, EIGRP

    Addressing: IPv4 (VLSM - Variable Length Subnet Masking)

    Hardware: 2911 Routers, 2960 Switches, End Devices (PCs)

🏗️ The 3 Lab Architectures
1. RIPv2 Lab (Routing Information Protocol)

A distance-vector protocol, ideal for simplicity in smaller topologies.

    Version: 2 (Supports VLSM)

    Key Configuration: no auto-summary to prevent unwanted route summarization.

    Verification Command: show ip route rip

2. OSPF Lab (Open Shortest Path First)

The industry-standard link-state protocol used in large-scale enterprise networks.

    Algorithm: Dijkstra (Shortest Path First)

    Hierarchy: Implementation of Area 0 (Backbone).

    Key Configuration: Precise Wildcard masks (e.g., 0.0.0.3) for point-to-point serial links.

    Verification Command: show ip ospf neighbor

3. EIGRP Lab (Enhanced Interior Gateway Routing Protocol)

A Cisco-proprietary hybrid protocol known for ultra-fast convergence.

    AS (Autonomous System): 10

    Algorithm: DUAL (Diffusing Update Algorithm).

    Key Configuration: Use of wildcard masks for optimal subnet precision.

    Verification Command: show ip eigrp neighbors

🚀 Installation and Testing

    Download the .pkt file corresponding to the protocol you wish to study.

    Open the file in Cisco Packet Tracer.

    To test connectivity:

        Use the Ping tool between PCs at different network extremities.

        Use the traceroute command to visualize the path taken by packets.

    To inspect routing tables:

        Access the Router CLI and type show ip route.

🔍 Protocol Comparison
Protocol	Type	Administrative Distance	Convergence
RIPv2	Distance Vector	120	Slow
OSPF	Link-State	110	Fast
EIGRP	Hybrid	90	Very Fast
✍️ Author

Moad - Cybersecurity and Web Technology Student.

