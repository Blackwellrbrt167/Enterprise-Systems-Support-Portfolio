\# Inter-VLAN Routing Lab (Router-on-a-Stick)



\## Overview



This lab demonstrates Inter-VLAN Routing using the Router-on-a-Stick (ROAS) method in Cisco Packet Tracer. The objective was to create multiple VLANs, verify traffic isolation, and then enable communication between VLANs through Layer 3 routing.



The lab simulates how organizations segment networks for security and performance while still allowing controlled communication between departments.



\---



\## Technologies Used



\- Cisco Packet Tracer

\- Cisco 2960 Switch

\- Cisco 1941 Router

\- VLAN Configuration

\- 802.1Q Trunking

\- Router-on-a-Stick (ROAS)

\- IPv4 Addressing

\- Inter-VLAN Routing



\---



\## Lab Objectives



\- Create VLAN 20 and VLAN 30

\- Assign switch ports to VLANs

\- Configure a trunk link between the switch and router

\- Configure router subinterfaces using 802.1Q encapsulation

\- Verify VLAN isolation before routing

\- Verify successful communication after routing configuration



\---



\## Network Topology



The lab consisted of:



\- 1 Cisco Router

\- 1 Cisco Switch

\- 4 End User Workstations

\- VLAN 20

\- VLAN 30



Traffic from both VLANs was carried across a single trunk connection to the router where subinterfaces performed Layer 3 routing between the networks.



\---



\## IP Addressing



\### VLAN 20



| Device | IP Address |

|----------|------------|

| PC0 | 172.16.1.2 |

| PC1 | 172.16.1.3 |

| Gateway | 172.16.1.1 |



\### VLAN 30



| Device | IP Address |

|----------|------------|

| PC2 | 172.16.2.4 |

| PC3 | 172.16.2.5 |

| Gateway | 172.16.2.1 |



\---



\## Configuration Summary



\### Switch Configuration



\- Created VLAN 20 and VLAN 30

\- Assigned access ports to the appropriate VLANs

\- Configured a trunk port to transport traffic from multiple VLANs over a single link



\### Router Configuration



\- Created subinterface G0/0.20

\- Created subinterface G0/0.30

\- Applied 802.1Q encapsulation

\- Configured VLAN gateways

\- Enabled routing between VLANs



\---



\## Validation Testing



\### Before Routing



Testing confirmed VLAN segmentation was functioning correctly.



Successful Communication:



\- VLAN 20 to VLAN 20

\- VLAN 30 to VLAN 30



Failed Communication:



\- VLAN 20 to VLAN 30

\- VLAN 30 to VLAN 20



These failures were expected because devices in separate VLANs cannot communicate without Layer 3 routing.



\### After Routing



After configuring Router-on-a-Stick, devices in VLAN 20 and VLAN 30 successfully communicated across VLAN boundaries.



Testing verified:



\- PC0 → PC2

\- PC0 → PC3

\- PC1 → PC2

\- PC1 → PC3

\- PC2 → PC0

\- PC2 → PC1

\- PC3 → PC0

\- PC3 → PC1



All tests completed successfully.



\---



\## Real-World Relevance



Organizations commonly use VLANs to separate departments, users, and security zones while maintaining centralized network infrastructure.



Inter-VLAN Routing allows those isolated segments to communicate when business operations require it. This design improves security, reduces unnecessary broadcast traffic, and provides better network management.



\---



\## Skills Demonstrated



\- VLAN Creation and Management

\- Cisco Switch Configuration

\- 802.1Q Trunking

\- Router-on-a-Stick Configuration

\- IPv4 Addressing

\- Layer 2 Segmentation

\- Layer 3 Routing

\- Connectivity Validation

\- Network Troubleshooting

\- Network Documentation



\---



\## Documentation



Additional implementation details, screenshots, research questions, and technical analysis are included in:



```text

Documentation/

└── InterVLAN\_Routing\_Lab\_Rebuild\_Guide\_with Screen prints.docx

```

