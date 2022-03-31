---
external help file: WiscO365-help.xml
Module Name: WiscO365
online version: https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api
schema: 2.0.0
---

# Set-O365StartupPreferences

## SYNOPSIS
Sets the preference to determine if the startup menu will be shown when importing the module.

## SYNTAX

```
Set-O365StartupPreferences [-showStartupMenu] [<CommonParameters>]
```

## DESCRIPTION
If the switch "showStartupMenu" is included, the startup menu will be displayed when importing the module.
Otherwise, the menu will not be displayed.
This preference is saved in the file "%LOCALAPPDATA%\WindowsPowerShell\ModuleData\WiscO365\Preferences\Startup.txt" as either "0" (don't show) or "1" (show).
The startup menu is defined by the function Show-HelperO365StartupMenu in "$PSScriptRoot\HelperFunctions.ps1".

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -showStartupMenu
Determines if the startup menu will be shown

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Startup.txt
## NOTES

## RELATED LINKS
