# T003_Account_Lockout_Troubleshooting

## Ticket Summary
- **Problem:**
    User account was locked following multiple unsuccessful login attempts.
- **Impact:**
    User was unable to authenticate to their domain account, preventing access to required systems and interrupting assigned work duties. 
- **Root Cause:**
    Account lockout policy triggered after exceedig the maximum allowed login attempts due to repeated authentication failures with an incorrect password.
- **Resolution:**
    Verified user identity.  Unlocked the user account in Active Directory and reset the password.  Suer was instructed to log in immediately and update their password upo first access. 
- **Prevention:**
    Educated the user on proper password management practices, including avoiding repeated failed attempts and using the organization-approved password manager to reduce future lockouts. 

## Ticket Closure Notes

> **Operational Note:**  
> This ticket remains in an **Open** state within osTicket due to Tier 1 role-based access restrictions.  
>  
> As a Tier 1 Support Agent, resolution actions were completed and documented via internal notes, including:
> User identity verification
> Active Directory account status validation
> Account unlock and password reset
> User confirmation of restored access  
>  
> Per standard Tier 1 workflow, ticket closure authority is reserved for Tier 2, supervisory roles, or automated SLA processes.  
>  
> Ticket resolution and closure readiness were fully documented in accordance with operational procedures.



