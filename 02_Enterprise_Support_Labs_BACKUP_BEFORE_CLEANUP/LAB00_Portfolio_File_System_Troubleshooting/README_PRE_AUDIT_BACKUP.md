# LAB00 – Portfolio File System Troubleshooting

## Overview

This troubleshooting case study documents a real-world file system issue encountered during a major portfolio reorganization and repository cleanup effort.

While restructuring project folders and standardizing repository naming conventions, an empty legacy folder could not be removed despite appearing empty in File Explorer, Git Bash, and PowerShell.

The objective was to identify the cause, collect evidence, validate assumptions, and remove the directory using proper troubleshooting methodology.

---

## Technologies Used

- Windows 11
- Git Bash
- PowerShell
- Windows Resource Monitor
- Windows Command Prompt
- Git

---

## Business Scenario

During portfolio cleanup, a legacy project folder remained after restructuring the Enterprise Systems Support repository.

The folder appeared empty but resisted deletion through normal methods.

Multiple command-line tools produced different error messages, requiring systematic investigation to determine the root cause.

---

## Symptoms Observed

- Git Bash reported:

```text
Device or resource busy
```

- PowerShell reported:

```text
The process cannot access the file because it is being used by another process
```

- PowerShell later reported:

```text
Access denied
```

- Folder appeared empty in File Explorer
- Folder appeared empty using command-line inspection

---

## Investigation Process

### Step 1: Verify Folder Contents

Confirmed the directory was empty using Git Bash.

**Evidence:**

- LAB00_02_Empty_Folder_Verified_GitBash.png

---

### Step 2: Attempt Standard Removal

Attempted deletion using Git Bash.

**Result:**

```text
Device or resource busy
```

**Evidence:**

- LAB00_01_Delete_Failure_GitBash_DeviceBusy.png

---

### Step 3: Attempt PowerShell Removal

Attempted deletion using PowerShell.

**Result:**

```text
The process cannot access the file because it is being used by another process
```

**Evidence:**

- LAB00_03_PowerShell_RemoveItem_AccessDenied.png

---

### Step 4: Investigate Open Handles

Used Windows Resource Monitor to determine whether a process was actively holding the directory open.

Initial investigation identified active handles associated with command-line processes.

**Evidence:**

- LAB00_04_ResourceMonitor_Handles_Found.png

---

### Step 5: Verify Handle Release

After closing associated processes, Resource Monitor confirmed that no handles remained attached to the directory.

**Evidence:**

- LAB00_05_ResourceMonitor_Handles_Cleared.png

---

### Step 6: Review Directory Attributes

Used PowerShell to inspect directory properties and attributes.

Observed:

```text
ReadOnly
Directory
Archive
```

**Evidence:**

- LAB00_06_GetItem_Attributes_ReadOnlyDirectoryArchive.png

---

### Step 7: Use Native Windows Removal Command

Executed:

```cmd
cmd /c rd /s /q "Windows-SecureBoot-BitLocker-Incident-Response"
```

The command completed successfully.

**Evidence:**

- LAB00_07_CMD_RD_Command_Success.png

---

### Step 8: Validate Resolution

Confirmed the folder no longer existed.

**Evidence:**

- LAB00_08_GetItem_PathNotFound_Verification.png
- LAB00_09_Final_Repository_Verification.png

---

## Root Cause Analysis

### Root Cause

The directory was initially held open by active command-line processes.

Even after the handles were released, standard Git Bash and PowerShell removal methods were unsuccessful.

The native Windows directory removal utility successfully removed the folder.

### Resolution

Removed the directory using:

```cmd
cmd /c rd /s /q "Windows-SecureBoot-BitLocker-Incident-Response"
```

### Validation

Verified:

- Directory no longer existed
- Repository structure remained intact
- Portfolio cleanup completed successfully

---

## Skills Demonstrated

- Windows File System Troubleshooting
- Git Bash Administration
- PowerShell Investigation
- Resource Monitor Analysis
- Root Cause Analysis
- Process Handle Investigation
- Documentation and Evidence Collection
- Validation and Remediation Testing

---

## Lessons Learned

1. Empty folders can still be locked by active processes.
2. Resource Monitor is useful for identifying directory handles.
3. Git Bash, PowerShell, and native Windows commands may behave differently.
4. Verification is just as important as remediation.
5. Evidence-based troubleshooting prevents unnecessary assumptions.

---

## Screenshot Inventory

- LAB00_01_Delete_Failure_GitBash_DeviceBusy.png
- LAB00_02_Empty_Folder_Verified_GitBash.png
- LAB00_03_PowerShell_RemoveItem_AccessDenied.png
- LAB00_04_ResourceMonitor_Handles_Found.png
- LAB00_05_ResourceMonitor_Handles_Cleared.png
- LAB00_06_GetItem_Attributes_ReadOnlyDirectoryArchive.png
- LAB00_07_CMD_RD_Command_Success.png
- LAB00_08_GetItem_PathNotFound_Verification.png
- LAB00_09_Final_Repository_Verification.png