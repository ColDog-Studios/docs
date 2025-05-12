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

## Temporary User

This issue occurs when:

- The user's directory is removed from a domain-joined computer
- A virus or program edits the registry profile

### Fixes

1. Log in as an administrator
2. Open regedit.exe
3. Navigate to `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsNT\CurrentVersion\ProfileList`
4. Rename the **Key** to remove the `.bak` or `.back` from the end of its name, or remove the **Key**
5. Reboot the system

{: .warning }
> It is always recommended to backup the registry before making changes

## Unable to change Computer Name

## Unable to change Workgroup
