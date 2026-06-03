GPO basics screenshots
# 05 – Group Policy Basics

## Objective
Create and apply a basic Group Policy Object (GPO) within Active Directory to demonstrate centralized policy management and enforcement at the Organizational Unit level.

## Why This Matters
Group Policy is one of the most powerful features of Active Directory. It allows administrators to centrally control security settings, user experience, and system behavior across domain-joined computers. Proper use of Group Policy ensures consistency, reduces manual configuration, and strengthens organizational security posture.

## Actions Performed
Group Policy Management Console was opened to manage domain policies. A new Group Policy Object was created to display a logon message for users within the Operations Organizational Unit. Policy settings were configured to define the logon message text and title. The GPO was linked directly to the Operations OU to ensure scoped application. Policy inheritance and linkage were reviewed to confirm correct targeting.

## Group Policy Configuration Implemented
A logon message policy was configured under user settings to display a standardized notice at user sign-in. The policy was scoped to the Operations OU to prevent unintended application across the entire domain. This approach reflects real-world policy targeting practices used in enterprise environments.

## Screenshots Included
Screenshots document the creation of the Group Policy Object, configuration of the logon message settings, linkage of the GPO to the Operations OU, and confirmation of the policy structure within Group Policy Management.

## Validation Performed
Policy linkage was confirmed within Group Policy Management Console. The policy was reviewed for correct scope and configuration. Domain-joined user authentication was tested to verify that the logon message appeared as expected upon sign-in.

## Skills Demonstrated
This section demonstrates Group Policy Object creation, OU-based policy scoping, centralized configuration management, and validation of policy enforcement in an Active Directory environment.
