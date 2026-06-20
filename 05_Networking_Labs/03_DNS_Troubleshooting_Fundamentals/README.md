\# DNS Troubleshooting Fundamentals



\## Lab Overview



In this lab, I investigated a common enterprise support issue in which a user could access resources by IP address but could not access them by hostname. The objective was to validate DNS functionality, identify the source of hostname resolution failures, simulate a DNS outage, restore service, and document the troubleshooting process.



This lab was performed in a Windows Active Directory environment using Windows Server 2022 DNS services and a domain-joined Windows client.



\---



\## Environment



\### Domain Controller



\* Windows Server 2022

\* Active Directory Domain Services (AD DS)

\* DNS Server

\* DHCP Server

\* Domain: Lab.Local

\* IP Address: 192.168.10.10



\### Client Workstation



\* Windows Client

\* Domain Joined

\* DHCP Assigned Address



\---



\## Learning Objectives



\* Understand the role of DNS in Active Directory environments.

\* Validate hostname resolution using DNS tools.

\* Identify DNS record types used in enterprise environments.

\* Simulate DNS failures and observe their impact.

\* Restore DNS functionality and verify successful resolution.

\* Develop a structured troubleshooting methodology.



\---



\## DNS Fundamentals



DNS (Domain Name System) translates human-readable hostnames into IP addresses that devices use for communication. Without DNS, users would need to remember numerical IP addresses instead of names such as:



\* fileserver.lab.local

\* dc01.lab.local

\* intranet.company.local



During this lab, I validated DNS functionality and observed how hostname resolution failures can occur even when underlying network connectivity remains operational.



\---



\## DNS Records Investigated



During validation, I reviewed several common DNS record types:



\### A Record



Maps a hostname to an IPv4 address.



\### AAAA Record



Maps a hostname to an IPv6 address.



\### CNAME Record



Creates an alias that points one hostname to another hostname.



\### PTR Record



Supports reverse DNS lookups by mapping IP addresses back to hostnames.



\---



\## Troubleshooting Methodology



\### Reported Problem



A user reports:



> "I can access resources by IP address, but I cannot access them by hostname."



\### Investigation Process



1\. Verify network connectivity.

2\. Review IP configuration.

3\. Verify DNS server configuration.

4\. Test hostname resolution using nslookup.

5\. Validate DNS records on the DNS server.

6\. Simulate DNS failure conditions.

7\. Restore DNS functionality.

8\. Confirm successful hostname resolution.



\### Root Cause



The client was configured with an incorrect DNS server address, preventing successful hostname resolution.



\### Resolution



The client DNS settings were restored to the correct Active Directory DNS server, allowing successful hostname resolution and normal access to domain resources.



\---



\## Key Findings



One of the most important lessons from this lab was learning that DNS failures do not necessarily indicate a network outage.



When DNS was intentionally misconfigured, hostname resolution immediately failed. However, communication using known IP addresses continued to function because Layer 3 routing remained operational.



This reinforced the distinction between Application Layer services and underlying network connectivity.



\---



\## Lessons Learned



\* DNS failures do not necessarily indicate a network outage.

\* Name resolution and network connectivity are separate services.

\* Devices can often communicate by IP address even when hostname resolution fails.

\* Active Directory environments depend heavily on DNS functionality.

\* Structured troubleshooting significantly reduces time to resolution.

\* DNS validation is a foundational Tier 1 Help Desk skill.



\---



\## Why This Matters



DNS is one of the most critical services in an Active Directory environment.



A user may have full network connectivity and still be unable to access websites, printers, file shares, applications, or domain resources if DNS is not functioning properly.



Understanding how to validate DNS records, identify DNS failures, and restore service is a foundational skill for:



\* Help Desk Technicians

\* Desktop Support Specialists

\* School District IT Staff

\* Systems Administrators

\* Infrastructure Support Technicians



\---



\## Validation Checklist



\* DNS server configuration validated

\* DNS records reviewed

\* Hostname resolution tested

\* DNS failure simulated

\* DNS service restored

\* Active Directory functionality verified



\---



\## Screenshots



\*\*Pending completion of lab execution.\*\*



Screenshots will document:



\* IP configuration

\* DNS validation

\* DNS record review

\* Failure simulation

\* Service restoration

\* Final validation testing



\---



\## Professional Skills Demonstrated



\* DNS Administration

\* Active Directory Fundamentals

\* Network Troubleshooting

\* Root Cause Analysis

\* Technical Documentation

\* Incident Resolution

\* Enterprise Support Methodology

\* Windows Server Administration



