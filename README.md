# Company-Enterprize
My Network Design for the Trading Floor Support Center's New Multi-Floor Building
Challenge: As our trading floor support center moves to a new, three-story building housing 600 staff across six departments, I was tasked with designing a secure, scalable, and future-proof network infrastructure. Here's how I envisioned this solution:

My Solution:

Utilizing Cisco Packet Tracer, I crafted a hierarchical network with redundancy at every layer, catering to the specific needs of each floor and department:

Core Layer:

Redundant Backbone: Two core routers (R1 and R2) connected to both ISPs (ISP1 and ISP2) ensure unwavering uptime through failover and load balancing.
Routing Intelligence: BGP efficiently handles communication with ISPs, while OSPF facilitates internal traffic flow across all floors, guaranteeing smooth data exchange.
Distribution Layer:

Centralized Access: Two multilayer switches (SW1 and SW2) connect to the core routers and provide access to all six departments across all floors. This simplifies switch management and network maintenance.
Inter-VLAN Routing: Inter-VLAN routing enabled on both switches using RIPv2 allows seamless communication between departments across floors while maintaining security boundaries through VLAN segregation.
Access Layer:

Departmental Reach: Six access switches (SW3-SW8) are strategically placed on each floor, one per department:
First Floor:
SW3: Dedicated to Sales & Marketing Department
SW4: Dedicated to Human Resources & Logistics Department
Second Floor:
SW5: Dedicated to Finance & Accounts Department
SW6: Dedicated to Administration & Public Relations Department
Third Floor:
SW7: Dedicated to ICT Department
SW8: Dedicated to Server Room devices
Wired & Wireless Flexibility: Each switch connects to wired workstations and a wireless access point, enabling mobility and flexibility for users throughout the building.
Secure Addressing: DHCP servers in the server room automatically assign IP addresses using 802.1x authentication for enhanced security.
Addressing and Security:

Floor-Wise Subnetting: I meticulously calculated subnet masks within subnet 172.16.1.0 to provide adequate IP addresses for each department on each floor.
Public IP Management: Four static public IP addresses (195.136.17.x/30) from ISPs are assigned to core routers for controlled internet access.
DMZ Implementation: A separate network segment with a firewall isolates internet-facing services from the internal network, bolstering overall security posture.
Additional Features:

Configuration Consistency: Basic device settings (hostnames, passwords, banners) are configured consistently across all devices for streamlined management.
Loop Prevention: Spanning Tree Protocol (STP) prevents network loops, ensuring optimal traffic flow.
Prioritization: Quality of Service (QoS) prioritizes critical traffic like VoIP and video conferencing, guaranteeing smooth performance for essential applications.
Outcome:

This multi-floor network design delivers a robust, secure, and scalable solution for our new building. Redundancy ensures availability, floor-specific segmentation optimizes network traffic, and wireless access empowers user mobility across all departments and floors. By incorporating industry-standard protocols and best practices, I'm confident this network will seamlessly support our expanding trading floor operations, now and in the future.
