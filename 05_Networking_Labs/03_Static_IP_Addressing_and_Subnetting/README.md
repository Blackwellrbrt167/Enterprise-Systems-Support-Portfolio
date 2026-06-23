# Static IP Addressing and Subnetting

## Lab Overview

This lab focused on configuring static IPv4 addressing, validating network connectivity, understanding subnetting fundamentals, and troubleshooting common network configuration issues in an Active Directory environment.

The objective was to identify and remediate connectivity issues caused by incorrect subnet masks and gateway configurations while documenting the troubleshooting process and validating successful network communication.

---

## Skills Demonstrated

### Networking

- IPv4 Addressing
- Static IP Configuration
- DHCP Fundamentals
- Subnet Masks
- Default Gateways
- DNS Validation
- Hostname Resolution
- Network Connectivity Testing

### Troubleshooting

- Incorrect Subnet Mask Identification
- Incorrect Gateway Identification
- Root Cause Analysis
- Connectivity Validation
- Network Remediation

### Enterprise Support

- Technical Documentation
- Change Verification
- Incident Investigation
- Problem Resolution
- Validation Testing

---

## Environment

### Domain Controller

- Windows Server 2022
- Active Directory Domain Services (AD DS)
- DNS Server
- DHCP Server
- Domain: lab.local
- IP Address: 192.168.10.10
- Gateway: 192.168.10.1

### Client Workstation

- Windows Client
- Domain Joined
- Static IPv4 Configuration

### Static Configuration Applied

- IP Address: 192.168.10.100
- Subnet Mask: 255.255.255.0
- Gateway: 192.168.10.1
- DNS Server: 192.168.10.10

---

## Lab Findings

During testing, an intentionally incorrect subnet mask was applied to the client workstation to simulate a common enterprise support issue.

### Configuration

- IP Address: 192.168.10.100
- Incorrect Subnet Mask: 255.255.255.240

### Observed Results

- Hostname resolution failed
- DNS queries timed out
- nslookup failed
- ping lab.local failed

### Root Cause

The incorrect subnet mask caused the workstation to calculate network boundaries incorrectly, preventing normal communication with DNS services and domain resources.

---

## Screenshots

### 01 – DHCP Baseline Configuration

![DHCP Baseline](screenshots/01_IPConfig_DHCP_Baseline.png)

---

### 02 – Detailed DHCP Configuration

![DHCP Detailed Configuration](screenshots/02_IPConfig_All_Baseline.png)

---

### 03 – Static IP Configuration

![Static IP Configuration](screenshots/03_Static_IP_Configuration.png)

---

### 04 – Static IP Validation

![Static IP Validation](screenshots/04_IPConfig_Static_Assigned.png)

---

### 05 – Connectivity Test by IP Address

![Ping Domain Controller](screenshots/05_Ping_Domain_Controller_By_IP.png)

---

### 06 – DNS Resolution Validation

![NSLookup Validation](screenshots/06_NSLookup_Lab_Local.png)

---

### 07 – Hostname Connectivity Validation

![Hostname Ping](screenshots/07_Ping_Hostname.png)

---

### 08 – Incorrect Subnet Mask Configuration

![Incorrect Subnet Mask](screenshots/08_Incorrect_Subnet_Mask_Test.png)

---

### 09 – DNS Failure Caused by Incorrect Subnet Mask

![Subnet Mask Failure](screenshots/09_Incorrect_Subnet_Mask_DNS_Failure.png)

---

### 10 – Incorrect Gateway Configuration

![Incorrect Gateway](screenshots/10_Incorrect_Gateway_Test.png)

---

### 11 – Connectivity Results with Incorrect Gateway

![Gateway Failure](screenshots/11_Incorrect_Gateway_Result.png)

---

### 12 – Final Validation After Remediation

![Final Validation 1](screenshots/12_Restored_Static_IP_Validation_1.png)

![Final Validation 2](screenshots/12_Restored_Static_IP_Validation_2.png)

---

## Root Cause Analysis

| Section | Findings |
|----------|----------|
| Problem Observed | User reported loss of access to network resources |
| Investigation Performed | Reviewed IP configuration, subnet mask, gateway, DNS settings, and tested connectivity using ping and nslookup |
| Root Cause | Incorrect subnet mask and invalid gateway configuration caused network communication failures |
| Corrective Action | Restored proper subnet mask, gateway, and DNS settings |
| Validation | Verified functionality using ipconfig /all, ping 192.168.10.10, ping lab.local, and nslookup lab.local |

---

## Lessons Learned

This lab reinforced the importance of ensuring that IP addressing, subnet masks, DNS settings, and gateway configurations align with the network design.

Incorrect network settings can disrupt domain communication, prevent DNS resolution, and cause connectivity issues throughout an enterprise environment.

The lesson I learned from this lab is that a workstation must have the correct IP address, subnet mask, DNS server, and gateway configuration in order to communicate properly on a network. If any of these settings are incorrect, connectivity problems can occur, DNS resolution can fail, and access to domain resources can be disrupted.

This lab reinforced the importance of validating network configurations and using a structured troubleshooting process to identify and correct network issues.

---

## Related Research

### Security Case Study

- [PrintNightmare (CVE-2021-1675)](Research/PrintNightmare_CVE_2021_1675.md)

### Related Topics

- DNS Infrastructure Security
- Active Directory Name Resolution
- Enterprise Network Troubleshooting Methodologies
- Windows Service Hardening
- Network Segmentation
---

## Professional Skills Demonstrated

- IPv4 Addressing
- DHCP Administration
- Static IP Configuration
- DNS Troubleshooting
- Active Directory Fundamentals
- Network Connectivity Testing
- Root Cause Analysis
- Technical Documentation
- Incident Response Methodology
- Enterprise Support Operations