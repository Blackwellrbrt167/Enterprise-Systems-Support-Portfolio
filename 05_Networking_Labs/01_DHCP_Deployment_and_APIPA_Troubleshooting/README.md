# Lab 01 – DHCP Deployment and APIPA Troubleshooting

## Scenario

A workstation in the Lab.Local Active Directory environment experienced network connectivity issues and originally received an APIPA address. The goal of this lab was to investigate the issue, deploy DHCP on the Domain Controller, configure a DHCP scope, and validate dynamic IP address assignment.

## Skills Demonstrated

- Windows Server 2022 DHCP role installation
- DHCP scope creation
- DHCP lease validation
- DNS option configuration
- APIPA troubleshooting
- Static-to-DHCP client migration
- `ipconfig`, `ipconfig /release`, and `ipconfig /renew`
- Client/server network validation
- Root cause analysis

## Lab Summary

The client workstation was initially configured with a static IP address after an earlier APIPA issue. During troubleshooting, I confirmed that DHCP was not being provided by the Domain Controller. I installed and configured the DHCP Server role, created a DHCP scope for the 192.168.10.0/24 network, configured DNS options, and validated that the client received a DHCP lease from the Domain Controller.

## Network Configuration

| Device | Role | IP Address |
|---|---|---|
| Server 2022 | Domain Controller / DNS / DHCP | 192.168.10.10 |
| Windows Client | Domain-Joined Workstation | 192.168.10.100 |
| DHCP Scope | Workstation Address Pool | 192.168.10.100 - 192.168.10.200 |

## Screenshots

| Screenshot | Description |
|---|---|
| 01_IPConfig_Current_Configuration.png | Initial client IP configuration |
| 02_IPConfig_All_Details.png | Detailed adapter configuration |
| 03_IPConfig_Release_Address.png | Released IP configuration |
| 04_IPConfig_Renew_Address.png | Renewed DHCP lease |
| 05_Connectivity_Ping_Tests.png | Connectivity validation |
| 06_Network_Adapter_Disabled.png | Simulated adapter/network issue |
| 07_APIPA_Address_Assigned.png | APIPA address after DHCP failure |
| 08_DHCP_Scope_Created.png | DHCP scope created |
| 09_DHCP_Address_Pool.png | DHCP address pool configured |
| 10_DHCP_Scope_Options.png | DNS and domain options configured |
| 11_DHCP_Address_Lease.png | Client lease issued by DHCP server |

## Root Cause Analysis

The original issue was caused by the lack of a DHCP service on the Active Directory lab network. The workstation could not automatically receive a valid IP address and fell back to APIPA addressing. A temporary static IP address restored connectivity, but the underlying issue required DHCP deployment.

## Resolution

The DHCP Server role was installed and authorized on the Domain Controller. A scope was created for the 192.168.10.0/24 network, with available addresses from 192.168.10.100 through 192.168.10.200. DNS options were configured so clients would use the Domain Controller for name resolution.

## Validation

After switching the client adapter from static addressing to automatic addressing, the workstation successfully received 192.168.10.100 from DHCP server 192.168.10.10. The DHCP console confirmed the active lease for WindowClient.Lab.Local.

## Lessons Learned

- APIPA usually indicates that a client cannot reach a DHCP server.
- Static IP addressing can be useful as a temporary troubleshooting workaround.
- DHCP must be authorized and scoped before clients can receive leases.
- DNS and DHCP are closely connected in Active Directory environments.
- DHCP lease tables help verify that clients are receiving addresses correctly.
