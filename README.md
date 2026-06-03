
# Enterprise-System-Support-And-Troubleshooting

# Help Desk & Systems Support Lab Portfolio
Overview

This repository documents hands-on labs that simulate real-world Help Desk and IT Support environments. The focus is on practical, job-ready skills rather than theoretical knowledge, with clear documentation, screenshots, and validation steps that reflect how work is performed in production support roles.

The lab environment combines identity management, infrastructure administration, and service desk operations to demonstrate how enterprise IT systems function together.

# Section 01 – Active Directory Labs
Overview

This section demonstrates foundational Active Directory administration skills aligned with real-world Help Desk and IT Support responsibilities. The environment simulates a small enterprise domain where user accounts, organizational units, group policies, and authentication workflows are managed using Microsoft Active Directory.

The goal of this lab is to show practical experience with identity management, domain services, and policy enforcement as they are used in day-to-day support operations.

All actions are documented with screenshots, structured walkthroughs, and validation steps.

Lab Objectives

The objectives of this lab are to:

Establish a functional Active Directory domain environment
Install and configure Active Directory Domain Services
Promote a Windows Server to a Domain Controller
Design a logical Organizational Unit (OU) structure
Manage users, groups, and group membership
Apply and scope Group Policy Objects (GPOs)
Validate domain authentication and policy enforcement

Environment Overview

The lab environment consists of:

A Windows Server configured as a Domain Controller
A Windows client joined to the domain
DNS configured for domain name resolution
Organizational Units structured by business function
User and group objects managed through Active Directory Users and Computers
Group Policy applied at the OU level

This setup mirrors common Help Desk and Tier 1–2 support environments.

# Active Directory Lab Walkthrough Sections

01 – Active Directory Domain Services Installation
Installation of the AD DS role and required management tools.

02 – Domain Promotion
Promotion of the server to a Domain Controller and creation of a new forest and domain.

03 – Organizational Unit Structure
Design and implementation of a business-aligned OU hierarchy.

04 – User Management
Creation, modification, disabling, and validation of domain user accounts and group membership.

05 – Group Policy Basics
Creation and linking of a Group Policy Object scoped to a specific OU with enforced settings.

99 – Proof and Validation
Verification of domain join, DNS resolution, authentication, and applied policies.

# Skills Demonstrated (Active Directory)

Active Directory administration
Windows Server management
User and group lifecycle management
Organizational Unit design
Group Policy creation and scoping
DNS and domain authentication validation
Help Desk–level troubleshooting and verification

# Section 02 – osTicket Help Desk Labs
Overview

This section focuses on IT service desk operations using the osTicket ticketing system. The lab simulates a real Help Desk environment where tickets are created, assigned, worked, escalated, and resolved using structured workflows.

The goal of this lab is to demonstrate hands-on experience with ticketing systems, role-based access control, and operational support processes used by Help Desk and IT Support teams.

# Lab Objectives

The objectives of this lab are to:

Deploy an Ubuntu Server for Help Desk operations
Install and configure a LAMP stack (Linux, Apache, MariaDB, PHP)
Install and secure the osTicket application
Configure Help Desk system settings and departments
Create agent roles with scoped permissions
Simulate real-world support ticket scenarios
Validate ticket lifecycle handling and system functionality

# osTicket Lab Walkthrough Sections

00 – Project Overview
Purpose and scope of the osTicket Help Desk lab.

01 – VM Setup
Creation and configuration of the Ubuntu Server virtual machine.

02 – OS Installation
Installation and baseline configuration of the Ubuntu operating system.

03 – LAMP Stack
Installation and validation of Apache, PHP, and MariaDB services.

04 – osTicket Installation
Deployment and configuration of the osTicket application.

05 – Help Desk Configuration
System settings, departments, roles, and agent permissions.

06 – Ticket Scenarios
Simulated Help Desk tickets representing common IT support requests.

07 – Validation and Testing
Verification of ticket flow, permissions, and system behavior.

99 – Proof and Evidence
Screenshots and validation artifacts demonstrating successful configuration.

# Skills Demonstrated (osTicket)

Help Desk ticketing system administration
Linux server management
Web application deployment
Role-based access control
Ticket lifecycle management
Operational troubleshooting and validation
Documentation and evidence collection

# How These Labs Work Together

Active Directory provides the identity and authentication foundation used in enterprise environments.
osTicket represents the operational layer where users submit requests and IT staff manage support workflows.

Together, these labs demonstrate how infrastructure and service operations function as a unified system in real-world IT environments.

Intended Audience

# This portfolio is intended for:

Help Desk and IT Support roles
Entry-level Systems Administration roles
Students learning enterprise IT environments
Recruiters and hiring managers reviewing hands-on experience

# Next Steps

This portfolio will continue to expand with additional labs covering:

Ticketing system integration with Active Directory
Password reset and account lockout workflows
Group-based access control scenarios
Advanced Help Desk ticket escalation
Incident response and troubleshooting simulations

