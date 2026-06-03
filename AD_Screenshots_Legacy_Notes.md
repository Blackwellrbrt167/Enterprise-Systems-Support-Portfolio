# Screenshots (Evidence)

## Objective

Validate that the Active Directory environment is fully functional end-to-end by confirming domain services, authentication, name resolution, Group Policy application, and user management behaviors from both the Domain Controller and a joined client system.

## Why This Matters

Building Active Directory is not enough. In real enterprise environments, administrators must prove that systems operate correctly after deployment. Validation confirms that users can authenticate, policies apply as expected, and the environment is production-ready. This step mirrors real help desk, systems administration, and security validation workflows.

## Validation Actions Performed

Confirmed Domain Controller operational status
Verified Active Directory Domain Services running successfully
Validated DNS resolution for the domain
Confirmed client successfully joined to the domain
Verified domain user authentication from client system
Confirmed Group Policy Objects applied to correct Organizational Units
Validated user account behavior including login, password policy, and account status

## Evidence Collected

Domain Controller ready and operational
Successful domain join confirmation from Windows client
DNS resolution using ping and nslookup for domain name
Successful domain user login on client machine
whoami output confirming domain authentication context
Group Policy application confirmation
Account status validation for enabled, disabled, and locked users

## Screenshots Included

Domain Controller operational confirmation
Client-to-domain ping success
Domain name resolution via DNS
Domain join success message
Domain user login confirmation
whoami command output showing domain authentication
Group Policy validation results

## Skills Demonstrated

Active Directory validation and troubleshooting
DNS and domain authentication verification
Client-domain integration testing
Group Policy enforcement confirmation
User authentication and access control validation
Enterprise-style post-deployment verification

## Final Outcome

The Active Directory lab environment is fully functional and validated. Domain services, DNS resolution, user authentication, organizational structure, and Group Policy enforcement operate as expected. This confirms the lab is ready for real-world help desk, systems administration, and security operations use cases.
