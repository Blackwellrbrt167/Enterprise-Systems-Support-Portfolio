OU structure screenshots
# 03 – Organizational Unit (OU) Structure Design

## Objective
Design and implement a logical Organizational Unit (OU) structure in Active Directory that reflects a real-world enterprise environment and supports scalable user, computer, group, and policy management.

## Why This Matters
Organizational Units are the backbone of Active Directory administration. A well-designed OU structure allows administrators to delegate control, apply Group Policy in a targeted manner, and keep users, computers, and departments logically separated. Poor OU design often leads to policy sprawl, security issues, and unnecessary administrative complexity.

## Actions Performed
Active Directory Users and Computers was opened to review the default directory layout. A top-level organizational OU was created to represent the business environment. Department-based OUs were built under this parent OU to reflect a realistic enterprise structure. Protection from accidental deletion was enabled on critical OUs to prevent administrative mistakes. Sub-OUs were created to separate users, groups, and computers where appropriate.

## OU Structure Implemented
The following hierarchy was implemented within the lab.local domain.

Lab.local  
CareAdvantage  
Clinical  
Finance  
HR  
IT  
Leadership  
Operations  
Users  
Groups  
Computers  
Sales_Marketing  
Scheduling_Dispatch  
Shared_Services  

## Screenshots Included
Screenshots document the default Active Directory structure, the creation of the CareAdvantage organizational unit, the buildout of departmental OUs, the Operations OU with its Users, Groups, and Computers sub-OUs, confirmation of the final hierarchy, and the application of accidental deletion protection.

## Validation Performed
The OU hierarchy was verified within Active Directory Users and Computers to confirm correct nesting and placement. The structure was refreshed and reviewed to ensure all OUs persisted correctly. The final layout was validated as ready for user placement, group management, and Group Policy linking.

## Skills Demonstrated
This section demonstrates enterprise Active Directory logical design, best-practice directory organization, preparation for delegated administration, and foundational planning for Group Policy management.
