Domain promotion screenshots
# 02 – Active Directory Domain Controller Promotion

## Objective
Promote a Windows Server 2022 system to a Domain Controller by creating a new Active Directory forest and domain.

## Why This Matters
Domain promotion transforms a standard Windows Server into the authoritative identity source for an organization. This enables centralized authentication, authorization, DNS integration, and Group Policy enforcement across all domain-joined systems.

Without this step, Active Directory cannot function.

## Actions Performed

Launched **Server Manager**

Selected **Promote this server to a domain controller**

Chose **Add a new forest**

Created a new domain: `lab.local`

Verified and accepted NetBIOS name configuration

Configured Domain Controller options (DNS, GC)

Set Directory Services Restore Mode (DSRM) password

Reviewed paths for NTDS database, logs, and SYSVOL

Passed all prerequisite checks

Completed domain controller promotion

Allowed automatic reboot to finalize promotion

## Screenshots Included

AD DS post-installation notification

New forest creation (`lab.local`)

Domain Controller options

DNS delegation warning (non-blocking)

NetBIOS name confirmation

Prerequisite check passed

Installation progress

Successful promotion and reboot confirmation

## Validation Performed

Confirmed server rebooted successfully

Verified domain controller role installed

Confirmed availability of Active Directory tools:
  
  Active Directory Users and Computers (ADUC)
  
  Active Directory Domains and Trusts
  
  Group Policy Management

Confirmed `lab.local` domain appears in ADUC

## Skills Demonstrated
Active Directory forest and domain creation

Domain Controller promotion process

DNS integration with Active Directory

Windows Server role configuration

Understanding of enterprise identity infrastructure
