\# Network Security Hardening Lab



\## Overview



This lab demonstrates foundational network hardening techniques using VLAN segmentation and Cisco switch port security. The objective was to reinforce network isolation, validate communication boundaries, and implement security controls that help protect access-layer infrastructure from unauthorized devices.



The lab simulates how organizations use segmentation and switch security features to reduce risk while maintaining required communication paths within the network.



\---



\## Technologies Used



\- Cisco Packet Tracer

\- Cisco 2960 Switch

\- VLAN Configuration

\- Port Security

\- Sticky MAC Addressing

\- Access Port Configuration

\- IPv4 Addressing

\- Network Segmentation

\- Network Hardening



\---



\## Network Segmentation Configuration



\### VLAN Creation



!\[VLAN 20 Creation](Screenshots/01\_NetworkSecurity\_VLAN20\_Creation.png)



!\[VLAN 30 Creation](Screenshots/02\_NetworkSecurity\_VLAN30\_Creation.png)



VLAN 20 and VLAN 30 were created to establish separate broadcast domains and provide logical segmentation between network resources.



\---



\### Access Port Assignments



!\[Fa0/1 VLAN 20](Screenshots/03\_NetworkSecurity\_F0-1\_VLAN20\_Assignment.png)



!\[Fa0/2 VLAN 20](Screenshots/04\_NetworkSecurity\_F0-2\_VLAN20\_Assignment.png)



Ports Fa0/1 and Fa0/2 were assigned to VLAN 20.



!\[Fa0/3 VLAN 30](Screenshots/05\_NetworkSecurity\_F0-3\_VLAN30\_Assignment.png)



!\[Fa0/4 VLAN 30](Screenshots/06\_NetworkSecurity\_F0-4\_VLAN30\_Assignment.png)



Ports Fa0/3 and Fa0/4 were assigned to VLAN 30.



\---



\## Configuration Verification



\### VLAN Membership Validation



!\[Show VLAN Brief](Screenshots/07\_NetworkSecurity\_Show\_VLAN\_Brief.png)



The VLAN database was reviewed to verify VLAN creation and correct port membership assignments.



\### Running Configuration Review



!\[Running Configuration](Screenshots/08\_NetworkSecurity\_Show\_Running\_Config.png)



The running configuration was reviewed to confirm VLAN assignments and switch configuration.



\### Interface Status Verification



!\[Interface Status](Screenshots/09\_NetworkSecurity\_Show\_Interface\_Status.png)



Interface status output confirmed that connected ports were operational and assigned to the correct VLANs.



\---



\## Connectivity Validation



\### VLAN 20 Communication



!\[BB to RB4](Screenshots/10\_NetworkSecurity\_VLAN20\_BB\_to\_RB4\_Ping.png)



!\[RB4 to BB](Screenshots/11\_NetworkSecurity\_VLAN20\_RB4\_to\_BB\_Ping.png)



Devices within VLAN 20 successfully communicated, confirming proper Layer 2 connectivity.



\### VLAN 30 Communication



!\[NJB to ICB](Screenshots/12\_NetworkSecurity\_VLAN30\_NJB\_to\_ICB\_Ping.png)



!\[ICB to NJB](Screenshots/13\_NetworkSecurity\_VLAN30\_ICB\_to\_NJB\_Ping.png)



Devices within VLAN 30 successfully communicated, confirming proper VLAN membership and connectivity.



\### Cross-VLAN Isolation Testing



!\[BB to NJB Failure](Screenshots/14\_NetworkSecurity\_CrossVLAN\_BB\_to\_NJB\_Fail.png)



!\[BB to ICB Failure](Screenshots/15\_NetworkSecurity\_CrossVLAN\_BB\_to\_ICB\_Fail.png)



!\[RB4 to NJB Failure](Screenshots/16\_NetworkSecurity\_CrossVLAN\_RB4\_to\_NJB\_Fail.png)



Cross-VLAN communication attempts failed as expected. These failures confirmed that segmentation was functioning correctly and that traffic was isolated between VLANs.



\---



\## Port Security Implementation



\### Initial Configuration and Troubleshooting



!\[Port Security Configuration](Screenshots/17\_NetworkSecurity\_PortSecurity\_Initial\_Configuration\_Error.png)



During implementation, configuration syntax and command behavior were reviewed and corrected as part of the hardening process.



\### Port Security Validation



!\[Fa0/1 Port Security](Screenshots/18\_NetworkSecurity\_PortSecurity\_F0-1\_Verification.png)



!\[Fa0/2 Port Security](Screenshots/19\_NetworkSecurity\_PortSecurity\_F0-2\_Verification.png)



!\[Fa0/3 Port Security](Screenshots/20\_NetworkSecurity\_PortSecurity\_F0-3\_Verification.png)



!\[Fa0/4 Port Security](Screenshots/21\_NetworkSecurity\_PortSecurity\_F0-4\_Verification.png)



Port security was enabled on all active access ports. The configuration limited each interface to a single MAC address and enforced shutdown mode upon violation.



\---



\## Final Configuration Validation



!\[Final Running Configuration](Screenshots/22\_NetworkSecurity\_Running\_Config\_With\_PortSecurity.png)



The final running configuration confirmed that VLAN segmentation and port security controls were successfully implemented across the switch.



\---



\## Security Benefits



The security controls implemented in this lab provide several important protections:



\- Limits unauthorized device connections

\- Restricts MAC address learning

\- Reduces opportunities for rogue device access

\- Reinforces network segmentation

\- Supports defense-in-depth principles

\- Reduces opportunities for lateral movement



\---



\## Real-World Relevance



Organizations commonly implement VLAN segmentation and port security to protect access-layer switches from unauthorized devices and reduce risk within enterprise environments.



These controls are frequently found in corporate offices, healthcare environments, government networks, educational institutions, and data centers where network access must be carefully controlled.



\---



\## Skills Demonstrated



\- VLAN Creation and Management

\- Access Port Configuration

\- Network Segmentation

\- Connectivity Validation

\- Port Security Configuration

\- Sticky MAC Addressing

\- Configuration Verification

\- Network Hardening

\- Network Troubleshooting

\- Security Validation

\- Technical Documentation



\---



\## Supporting Documentation



\- \[Implementation Guide](Documentation/Network\_Security\_Hardening\_Implementation\_Guide.md)

\- Network\_Security\_Hardening\_Implementation\_Guide.docx

