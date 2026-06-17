# LAB 02 · Software Installation Failure Investigation

## Overview

This lab simulates a real-world enterprise software deployment failure where an application installer fails to complete successfully on a Windows workstation.

The objective is to collect evidence, reproduce the failure, analyze installer logs, review Event Viewer, identify the root cause, remediate the issue, validate successful installation, and document the incident according to enterprise support standards.

---

## Skills Demonstrated

* Software Deployment Troubleshooting
* MSI Installer Analysis
* Event Viewer Investigation
* Dependency Validation
* Windows Installer Logging
* PowerShell Troubleshooting
* Root Cause Analysis
* Ticket Documentation

---

## Technologies Used

* Windows
* MSI Installer
* msiexec
* Event Viewer
* PowerShell
* Programs and Features
* Windows Installer Logs

---

## Business Scenario

An accounting software deployment fails during rollout. The installer closes without obvious errors and the application does not appear in Programs and Features.

The objective is to determine whether the failure is caused by:

* Missing prerequisites
* Permission issues
* Dependency failures
* Installer corruption
* Unsupported OS configuration

---

## Lab Objectives

* Establish baseline workstation state
* Reproduce installation failure
* Generate verbose MSI logs
* Review Event Viewer evidence
* Validate dependencies and prerequisites
* Remediate root cause
* Validate successful installation
* Document findings

---

## Screenshot Checklist

(To be completed during lab execution)

* LAB02_00_LabStart_Environment.png
* LAB02_01_FolderStructure_Created.png
* LAB02_02_ProgramsAndFeatures_Baseline.png
* LAB02_03_SystemInfo_Baseline.png
* LAB02_04_InstallerFailure_Observed.png
* LAB02_05_AppStillMissing_AfterFailure.png
* LAB02_06_MSILog_CommandExecuted.png
* LAB02_07_MSILog_FileCreated.png
* LAB02_08_MSILog_ErrorSearch.png
* LAB02_09_EventViewer_Application_MsiInstaller.png
* LAB02_10_EventViewer_ErrorDetails.png
* LAB02_11_Prerequisite_Check.png
* LAB02_12_ServiceStatus_Check.png
* LAB02_13_InstallerProperties_Context.png
* LAB02_14_Whoami_Privileges.png
* LAB02_15_Prerequisite_Installed.png
* LAB02_16_Reinstall_Attempt_AfterFix.png
* LAB02_17_AppInstalled_ProgramsAndFeatures.png
* LAB02_18_AppLaunch_Success.png
* LAB02_19_FinalValidation_PowerShell.png
* LAB02_20_TicketNotes_Final.png

---

## Evidence Collection

(To be completed after screenshots are captured)

---

## Root Cause Analysis

### Observed Symptoms

### Evidence Collected

### Root Cause

### Remediation

### Validation

---

## Ticket Documentation

### User Complaint

### Business Impact

### Troubleshooting Performed

### Root Cause
## Expanded Investigation

During troubleshooting, it was determined that the software installation issue extended beyond simple user permissions.

A dedicated Active Directory security group was created and assigned to the target user account to provide the administrative permissions required for software installation testing. However, the expected permissions were not being applied to the client workstation.

Further investigation revealed multiple infrastructure-related issues affecting communication between the client workstation and the Domain Controller, including:

* Virtual network configuration issues
* APIPA address assignment
* Static IP configuration requirements
* DNS resolution failures
* Domain Controller discovery validation
* Group Policy processing verification

These issues prevented Active Directory changes from properly reaching the client workstation and directly impacted the software installation troubleshooting process.

A full breakdown of the investigation, remediation steps, validation testing, and supporting screenshots has been documented separately in:

**05_Auxiliary_Troubleshooting**

The investigation concluded with successful restoration of domain communication, validation of Active Directory group memberships, successful Group Policy processing, and confirmation of user permissions.

### Resolution
### Related Investigation

See:

`05_Auxiliary_Troubleshooting/README.md`

for the complete Active Directory, DNS, networking, and Group Policy troubleshooting process that was required before software installation testing could continue.

### Escalation Decision

---

## Lessons Learned

(To be completed after lab execution)
