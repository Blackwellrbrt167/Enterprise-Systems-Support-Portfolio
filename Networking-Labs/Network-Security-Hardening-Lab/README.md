\# Network Security Hardening Lab



\## Overview



This lab demonstrates foundational network hardening techniques using VLAN segmentation and Cisco switch port security. The objective was to reinforce network isolation, validate communication boundaries, and implement security controls that help protect access-layer infrastructure from unauthorized devices.



The lab simulates how organizations use segmentation and switch security features to reduce risk while maintaining required communication paths within the network.



---



\## Technologies Used



- Cisco Packet Tracer

- Cisco 2960 Switch

- VLAN Configuration

- Port Security

- Sticky MAC Addressing

- Access Port Configuration

- IPv4 Addressing

- Network Segmentation

- Network Hardening



---



- Network Segmentation Configuration



\# VLAN Creation



![VLAN 20 Creation](Screenshots/01_NetworkSecurity_VLAN20_Creation.png)



![VLAN 30 Creation](Screenshots/02_NetworkSecurity_VLAN30_Creation.png)



VLAN 20 and VLAN 30 were created to establish separate broadcast domains and provide logical segmentation between network resources.



---



\# Access Port Assignments



![Fa0/1 VLAN 20](Screenshots/03_NetworkSecurity_F0-1_VLAN20_Assignment.png)



![Fa0/2 VLAN 20](Screenshots/04_NetworkSecurity_F0-2_VLAN20_Assignment.png)



Ports Fa0/1 and Fa0/2 were assigned to VLAN 20.



![Fa0/3 VLAN 30](Screenshots/05_NetworkSecurity_F0-3_VLAN30_Assignment.png)



![Fa0/4 VLAN 30](Screenshots/06_NetworkSecurity_F0-4_VLAN30_Assignment.png)



Ports Fa0/3 and Fa0/4 were assigned to VLAN 30.



---



- Configuration Verification



\# VLAN Membership Validation



![Show VLAN Brief](Screenshots/07_NetworkSecurity_Show_VLAN_Brief.png)



The VLAN database was reviewed to verify VLAN creation and correct port membership assignments.



\# Running Configuration Review



![Running Configuration](Screenshots/08_NetworkSecurity_Show_Running_Config.png)



The running configuration was reviewed to confirm VLAN assignments and switch configuration.



\# Interface Status Verification



![Interface Status](Screenshots/09_NetworkSecurity_Show_Interface_Status.png)



Interface status output confirmed that connected ports were operational and assigned to the correct VLANs.



---



- Connectivity Validation



\# VLAN 20 Communication



![BB to RB4](Screenshots/10_NetworkSecurity_VLAN20_BB_to_RB4_Ping.png)



![RB4 to BB](Screenshots/11_NetworkSecurity_VLAN20_RB4_to_BB_Ping.png)



Devices within VLAN 20 successfully communicated, confirming proper Layer 2 connectivity.



\# VLAN 30 Communication



![NJB to ICB](Screenshots/12_NetworkSecurity_VLAN30_NJB_to_ICB_Ping.png)



![ICB to NJB](Screenshots/13_NetworkSecurity_VLAN30_ICB_to_NJB_Ping.png)



Devices within VLAN 30 successfully communicated, confirming proper VLAN membership and connectivity.



## Cross-VLAN Isolation Testing



![BB to NJB Failure](Screenshots/14_NetworkSecurity_CrossVLAN_BB_to_NJB_Fail.png)



![BB to ICB Failure](Screenshots/15_NetworkSecurity_CrossVLAN_BB_to_ICB_Fail.png)



![RB4 to NJB Failure](Screenshots/16_NetworkSecurity_CrossVLAN_RB4_to_NJB_Fail.png)



Cross-VLAN communication attempts failed as expected. These failures confirmed that segmentation was functioning correctly and that traffic was isolated between VLANs.



---



## Port Security Implementation



## Initial Configuration and Troubleshooting



![Port Security Configuration](Screenshots/17_NetworkSecurity_PortSecurity_Initial_Configuration_Error.png)



During implementation, configuration syntax and command behavior were reviewed and corrected as part of the hardening process.



## Port Security Validation



![Fa0/1 Port Security](Screenshots/18_NetworkSecurity_PortSecurity_F0-1_Verification.png)



![Fa0/2 Port Security](Screenshots/19_NetworkSecurity_PortSecurity_F0-2_Verification.png)



![Fa0/3 Port Security](Screenshots/20_NetworkSecurity_PortSecurity_F0-3_Verification.png)



![Fa0/4 Port Security](Screenshots/21_NetworkSecurity_PortSecurity_F0-4_Verification.png)



Port security was enabled on all active access ports. The configuration limited each interface to a single MAC address and enforced shutdown mode upon violation.



---



## Final Configuration Validation



![Final Running Configuration](Screenshots/22_NetworkSecurity_Running_Config_With_PortSecurity.png)



The final running configuration confirmed that VLAN segmentation and port security controls were successfully implemented across the switch.



---



## Security Benefits



The security controls implemented in this lab provide several important protections:



- Limits unauthorized device connections

- Restricts MAC address learning

- Reduces opportunities for rogue device access

- Reinforces network segmentation

- Supports defense-in-depth principles

- Reduces opportunities for lateral movement



---



- Real-World Relevance



Organizations commonly implement VLAN segmentation and port security to protect access-layer switches from unauthorized devices and reduce risk within enterprise environments.



These controls are frequently found in corporate offices, healthcare environments, government networks, educational institutions, and data centers where network access must be carefully controlled.



---



- Skills Demonstrated



- VLAN Creation and Management

- Access Port Configuration

- Network Segmentation

- Connectivity Validation

- Port Security Configuration

- Sticky MAC Addressing

- Configuration Verification

- Network Hardening

- Network Troubleshooting

- Security Validation

- Technical Documentation



---



- Supporting Documentation



- \[Implementation Guide](Documentation/Network_Security_Hardening_Implementation_Guide.md)

- Network_Security_Hardening_Implementation_Guide.docx

