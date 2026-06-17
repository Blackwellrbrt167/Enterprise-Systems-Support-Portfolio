# Auxiliary Investigation – Active Directory and Network Remediation

## Executive Summary

While troubleshooting a software installation failure, it was determined that the issue extended beyond user permissions and required investigation of Active Directory communication between the client workstation and Domain Controller.

The investigation began after a dedicated security group was created to grant software installation permissions to the target user account. Despite successful group creation and membership assignment, the permissions were not being applied to the client workstation.

Further investigation revealed multiple infrastructure issues affecting communication between the workstation and the Domain Controller, including:

* Virtual network configuration issues
* APIPA address assignment
* Static IP configuration requirements
* DNS resolution failures
* Domain Controller discovery validation
* Group Policy processing verification

This investigation documents the troubleshooting methodology used to identify, remediate, and validate the underlying infrastructure issues before software installation testing could continue.

## Supporting Evidence

* LAB02_10_AD_Security_Group_Created.png
* LAB02_11_Group_Membership_Not_Applying.png
* LAB02_13_VM_Network_Configuration_Review.png
* LAB02_14_Domain_Controller_Static_IP_Validated.png
* LAB02_15_Client_Static_IP_Configured.png
* LAB02_16_Client_Network_Configuration_Validated.png
* LAB02_17_Client_APIPA_Address_Discovered.png
* LAB02_18_Local_Admin_Access_Recovery.png
* LAB02_19_Ping_Domain_Controller_Success.png
* LAB02_20_Domain_Controller_Discovered.png
* LAB02_21_DNS_Resolution_Restored.png
* LAB02_22_Interface_Metric_Optimization.png
* LAB02_23_GPUpdate_Force_Success.png
* LAB02_24_AD_Group_Membership_Validated.png
* LAB02_25_Group_Policy_Processing_Validated.png
* LAB02_26_Domain_User_Validation.png

## Outcome

Network communication was restored, DNS functionality was validated, Group Policy processing was confirmed, Active Directory group membership was successfully applied, and the user account was validated.

These corrections allowed software installation troubleshooting to continue and provided a documented example of enterprise Active Directory, DNS, networking, and Group Policy troubleshooting.
