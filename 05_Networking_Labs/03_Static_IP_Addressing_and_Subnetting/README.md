## Current Lab Status



### Status: Planning and Research Complete



At this stage, the conceptual portion of the lab has been completed, including IPv4 addressing research, subnetting fundamentals, troubleshooting methodology, and enterprise use cases.



The physical lab execution has not yet been performed. Validation testing, screenshot collection, and configuration changes will be completed during the hands-on phase of the lab.



### Completed



* Environment planning

* IPv4 addressing research

* DHCP vs Static IP research

* Subnetting fundamentals research

* Gateway functionality research

* DNS and connectivity testing methodology

* Root cause analysis planning

* Real-world school district scenario analysis



### Pending



* Static IP configuration

* Connectivity validation

* Subnetting calculations validation

* Incorrect subnet mask simulation

* Incorrect gateway simulation

* Screenshot collection

* Final validation testing

* Real-world security research documentation



\---



## Real-World Scenario



You are the sole IT Support Technician for a small school district.



The district recently deployed several new infrastructure components including:



* Domain Controller

* File Server

* Network Printer

* Security Camera System



Users are reporting intermittent connectivity issues after devices were manually configured.



Your responsibilities include:



* Identifying proper network addressing

* Configuring static IP addresses

* Verifying subnet membership

* Troubleshooting incorrect subnet masks

* Validating gateway configuration

* Performing root cause analysis

* Documenting findings



\---



## Knowledge Validation



### Static vs Dynamic Addressing



A static IP address is manually assigned and remains consistent until changed by an administrator.



A dynamic IP address is automatically assigned by a DHCP server and may change periodically based on lease duration and network configuration.



### Devices That Commonly Require Static Addresses



* Domain Controllers

* DNS Servers

* DHCP Servers

* File Servers

* Printers

* Routers

* Firewalls

* Switches

* Access Points

* Security Cameras



### Why Test IP Connectivity Before Hostnames



Testing by IP address validates Layer 3 connectivity independently of DNS.



If the IP responds successfully, troubleshooting efforts can focus on DNS, application services, or security controls rather than basic network connectivity.



### Why Test Hostnames Second



Hostname testing validates DNS functionality.



Successful hostname resolution confirms:



* DNS server reachability

* DNS record availability

* Proper DNS client configuration

* Active Directory service discovery functionality



\---



## Subnetting Fundamentals



### Example Network



IP Address:



192.168.10.100/24



### Network Information



| Item              | Value          |

| ----------------- | -------------- |

| Network Address   | 192.168.10.0   |

| Broadcast Address | 192.168.10.255 |

| First Host        | 192.168.10.1   |

| Last Host         | 192.168.10.254 |

| Total Hosts       | 254            |



### Why This Matters



Understanding subnetting enables support technicians to correctly identify network boundaries, troubleshoot connectivity issues, and validate proper IP addressing within enterprise environments.



Incorrect subnet masks can cause routing failures, connectivity issues, and inconsistent communication between hosts.



\---



## Root Cause Analysis Planning



### Incorrect Subnet Mask



Potential Impact:



* Improper network boundary calculations

* Routing inconsistencies

* Intermittent connectivity issues



Expected Resolution:



* Restore correct subnet mask

* Validate connectivity

* Document results



### Incorrect Default Gateway



Potential Impact:



* Loss of communication outside local subnet

* Internet access failures

* Inability to reach remote resources



Expected Resolution:



* Restore correct gateway configuration

* Validate communication

* Document findings



\---



## Screenshots



Pending physical lab execution.



Screenshots will include:



* Initial DHCP configuration

* Static IP assignment

* ipconfig validation

* Connectivity testing

* nslookup testing

* Incorrect subnet mask simulation

* Incorrect gateway simulation

* Root cause analysis evidence

* Final validation testing

