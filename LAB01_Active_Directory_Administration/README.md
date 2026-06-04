\# LAB01 – Active Directory Administration



\## Enterprise Systems Support Portfolio



\## Executive Summary



This project documents the deployment and configuration of a Windows Server Active Directory Domain Services (AD DS) environment within a virtualized enterprise lab.



The project covers the complete lifecycle of building a domain environment, including Active Directory installation, domain controller promotion, Organizational Unit (OU) design, user account administration, Group Policy configuration, and validation testing.



The objective was to simulate foundational enterprise administration tasks commonly performed by Help Desk Technicians, System Administrators, and Identity \& Access Management personnel.



\---



\## Skills Demonstrated



\- Active Directory Domain Services (AD DS)

\- Windows Server Administration

\- Domain Controller Promotion

\- DNS Configuration and Validation

\- Organizational Unit (OU) Design

\- User and Group Administration

\- Group Policy Management

\- Account Lifecycle Management

\- Access Control Administration

\- Identity and Access Management (IAM)

\- Windows Troubleshooting

\- Enterprise Documentation



\---



\## Environment



\### Hardware



\- VirtualBox Virtual Machine Environment



\### Operating Systems



\- Windows Server

\- Windows Client System



\### Technologies



\- Active Directory Domain Services (AD DS)

\- DNS

\- Group Policy

\- NTFS Permissions

\- Windows Server Manager



\---



\# Project Objectives



The goals of this project were to:



1\. Install Active Directory Domain Services.

2\. Promote a server to Domain Controller.

3\. Create and organize Organizational Units.

4\. Create and manage users and security groups.

5\. Configure and validate Group Policy Objects.

6\. Verify domain functionality and authentication.

7\. Document administrative actions and validation procedures.



\---



\# Phase 1 – Active Directory Domain Services Installation



\## Objective



Install Active Directory Domain Services using Server Manager.



\### Activities Performed



\- Opened Server Manager.

\- Added Roles and Features.

\- Selected Active Directory Domain Services role.

\- Installed required dependencies and management tools.

\- Verified successful installation.



\### Evidence



Screenshots located in:



```text

01\_AD\_DS\_Install/screenshots

```



\### Skills Demonstrated



\- Server Administration

\- Windows Role Installation

\- Enterprise Infrastructure Deployment



\---



\# Phase 2 – Domain Controller Promotion



\## Objective



Promote the server to a Domain Controller and create a new forest.



\### Activities Performed



\- Created a new forest.

\- Defined root domain.

\- Completed prerequisite checks.

\- Configured DNS integration.

\- Promoted server to Domain Controller.

\- Verified successful promotion.



\### Evidence



Screenshots located in:



```text

02\_Domain\_Promotion/screenshots

```



\### Skills Demonstrated



\- Active Directory Deployment

\- DNS Integration

\- Domain Controller Configuration



\---



\# Phase 3 – Organizational Unit Structure



\## Objective



Create an enterprise-style Organizational Unit structure for managing users and computers.



\### Activities Performed



\- Created Organizational Units.

\- Created user containers.

\- Created computer containers.

\- Organized objects according to administrative requirements.

\- Validated OU structure.



\### Evidence



Screenshots located in:



```text

03\_OU\_Structure/screenshots

```



\### Skills Demonstrated



\- Active Directory Organization

\- Enterprise Directory Design

\- Identity Management Planning



\---



\# Phase 4 – User Management



\## Objective



Perform common identity administration tasks.



\### Activities Performed



\- Created users.

\- Created groups.

\- Assigned group memberships.

\- Disabled accounts.

\- Reset passwords.

\- Managed account lockouts.

\- Verified user configurations.



\### Evidence



Screenshots located in:



```text

04\_User\_Management/screenshots

```



\### Skills Demonstrated



\- Identity Lifecycle Management

\- Access Administration

\- User Account Operations



\---



\# Phase 5 – Group Policy Administration



\## Objective



Create and validate Group Policy configurations.



\### Activities Performed



\- Created Group Policy Objects.

\- Linked policies to Organizational Units.

\- Updated policy settings.

\- Verified policy application.

\- Tested user impact.



\### Evidence



Screenshots located in:



```text

05\_GPO\_Basics/screenshots

```



\### Skills Demonstrated



\- Group Policy Management

\- Security Configuration

\- Enterprise Policy Enforcement



\---



\# Phase 6 – Proof and Validation



\## Objective



Validate domain functionality and enterprise services.



\### Activities Performed



\- Verified DNS functionality.

\- Tested name resolution.

\- Validated domain authentication.

\- Confirmed domain joins.

\- Tested connectivity between systems.

\- Verified Group Policy application.



\### Evidence



Screenshots located in:



```text

99\_Proof\_and\_Validation/screenshots

```



\### Skills Demonstrated



\- Enterprise Validation Procedures

\- DNS Troubleshooting

\- Authentication Verification



\---



\# Project Results



The Active Directory environment was successfully deployed and validated.



The environment demonstrated:



\- Functional Domain Controller

\- Working DNS Services

\- Organizational Unit Structure

\- User and Group Administration

\- Group Policy Enforcement

\- Domain Authentication

\- Enterprise Validation Procedures



All testing completed successfully.



\---



\# Lessons Learned



1\. Active Directory depends heavily on proper DNS configuration.

2\. Organizational Unit planning simplifies administration.

3\. Group Policy provides centralized configuration management.

4\. Identity administration requires consistent documentation and validation.

5\. Validation testing is essential before deploying administrative changes.



\---



\# Portfolio Reflection



This project provided practical experience with the core administrative functions that support enterprise Windows environments. While Active Directory concepts can be learned from documentation, building and validating a functioning domain environment reinforced how identity, access control, DNS, and policy management work together.



The project also highlighted the importance of structured documentation and validation. Successful administration is not only about making changes but also confirming that systems behave as expected after those changes are applied.



\---



\# Project Summary (STAR Format)



\## Situation



An enterprise environment required centralized identity management, authentication, and policy administration.



\## Task



Deploy and configure a functional Active Directory environment capable of supporting users, computers, security groups, and Group Policy management.



\## Action



Installed Active Directory Domain Services, promoted a Domain Controller, configured DNS, created Organizational Units, managed users and groups, applied Group Policy, and validated domain functionality.



\## Result



A fully functional Active Directory environment was successfully deployed and validated, demonstrating core enterprise administration skills used in real-world IT support and systems administration roles.

