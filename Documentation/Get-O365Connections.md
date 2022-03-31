---
external help file: WiscO365-help.xml
Module Name: WiscO365
online version: https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api
schema: 2.0.0
---

# Get-O365Connections

## SYNOPSIS
Gets all the existing connections for the Office 365 API, both saved and in-memory.

## SYNTAX

```
Get-O365Connections
```

## DESCRIPTION
This function gets all the existing connections for the Office 365 API, both saved and in-memory.
It first checks that %LOCALAPPDATA%\WindowsPowerShell\ModuleData\WiscO365\Connections\Connections.csv exists.
If the file doesn't exist, it is created with the proper headers.
Connections.csv and any password files are imported and added to $GlobalO365Connections with any temporary, in-memory connections.

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

## INPUTS

## OUTPUTS

### An array of all existing connections is returned.
## NOTES

## RELATED LINKS
