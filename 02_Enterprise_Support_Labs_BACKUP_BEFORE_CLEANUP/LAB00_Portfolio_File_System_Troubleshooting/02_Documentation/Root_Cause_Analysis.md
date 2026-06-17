\# Root Cause Analysis



\## Incident



Unable to delete an empty legacy folder during Enterprise Systems Support repository cleanup.



\## Symptoms



\* Git Bash reported "Device or resource busy"

\* PowerShell reported the directory was in use

\* PowerShell later reported access denied

\* Folder appeared empty in File Explorer and Git Bash



\## Investigation



1\. Verified folder contents using Git Bash.

2\. Verified no hidden files existed.

3\. Attempted removal using Git Bash.

4\. Attempted removal using PowerShell.

5\. Used Resource Monitor to identify active handles.

6\. Confirmed handles associated with command-line processes.

7\. Verified handles were released.

8\. Reviewed directory attributes using PowerShell.

9\. Tested native Windows directory removal methods.



\## Root Cause



The directory was temporarily locked by active command-line processes. Even after the handles were released, standard Git Bash and PowerShell removal methods were unsuccessful. The native Windows directory removal utility successfully removed the directory.



\## Resolution



Removed the directory using:



cmd /c rd /s /q "Windows-SecureBoot-BitLocker-Incident-Response"



\## Validation



\* Folder no longer existed

\* Repository structure remained intact

\* Portfolio cleanup completed successfully



\## Lessons Learned



\* Empty folders can still be locked by active processes.

\* Resource Monitor is valuable for identifying file and directory handles.

\* Different command-line tools may behave differently when interacting with the Windows file system.

\* Verification after remediation is essential.



