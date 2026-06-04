# T004_Shared_Drive_Permissions

## Ticket Summary
- **Problem:**
    User reports inability to access a shared network drive. 
- **Impact:**
    User cannot access or save files required to perform assigned job duties.
- **Root Cause:**
    User was not a member of the required Active Directory security group associated with the shared drive.

    > Note: Detailed permission design and inheritance configuration are handled by Tier 2 / Systme Administration. 
- **Resolution:**
    - Verified user identity per company policy 
    - Confirmed shared drive access issue 
    - Added user to the appropriate AD security group 
    - informed user that access may require logoff/logon or policy refresh
- **Prevention:**
    - Reinforce group-based access control (RBAC)
    - Ensure access requests follow documented approval workflows 
    - Escalate recurring access issues for review by tier 3 

    ---

Tier 1 responsibilities include:
- Identifying access failure symptoms  
- Verifying user identity  
- Confirming group membership status  
- Applying approved access changes **or** escalating when outside scope  

Tier 1 does **not** redesign NTFS permissions, inheritance models, or share architecture.