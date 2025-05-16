---
title: Troubleshooting
parent: Windows
nav_order: 1
---

# Troubleshooting
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Missing Boot Files

This issue occures when:

- N/A

### Fixes

N/A

## Temporary User

This issue occurs when:

- The user's directory is removed from a domain-joined computer
- A virus or program edits the registry profile

### Fixes

1. Log in as an administrator
2. Open regedit.exe
3. Navigate to:
```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsNT\CurrentVersion\ProfileList
```
5. Rename the **Key** to remove the `.bak` or `.back` from the end of its name, or remove the **Key**
6. Reboot the system

{: .warning }
> It is always recommended to backup the registry before making changes

## Unable to change Computer Name

This issue occurs when:

- N/A - Unknown

### Fixes

1. Open an elevated PowerShell
2. Enter the prompt:
```powershell
Rename-Computer -NewName "NEW_PC_NAME"
```
3. Reboot the system

**OR**

1. Open an elevated command prompt
2. Enter the command:
```batchfile
wmic computersystem where name="%computername%" call rename name="NEW_PC_NAME"
```
3. Reboot the system

{: .note }
> Replace `NEW_PC_NAME` with the name you want to set

## Unable to change Workgroup

This issue occurs when:

- N/A - Unknown

### Fixes

1. Open an elevated PowerShell
2. Enter the prompt:
```powershell
Add-Computer -WorkGroupName "NEW_WORKGROUP"`
```
3. Reboot the system

**OR**

1. Open an elevated command prompt
2. Enter the command:
```batchfile
wmic computersystem where name="%computername%" call joindomainorworkgroup name="NEW_WORKGROUP"
```
3. Reboot the system

{: .note }
> Replace `NEW_WORKGROUP` with the workgroup name you want to set

