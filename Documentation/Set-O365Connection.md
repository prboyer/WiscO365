---
external help file: WiscO365-help.xml
Module Name: WiscO365
online version: https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api
schema: 2.0.0
---

# Set-O365Connection

## SYNOPSIS
Sets an existing Office 365 API connection as the current connection or clears the current connection.

## SYNTAX

```
Set-O365Connection [[-id] <String>] [<CommonParameters>]
```

## DESCRIPTION
This function sets an existing Office 365 API connection as the current connection or clears the current connection.
If the ID parameter is not specified, the current connection is cleared by setting $Global:O365CurrentConnection and $Global:O365Session as $null.
Otherwise, the function first gets all existing connections using Get-O365Connections.
If the specified connection does not exist, an error is thrown and processing stops.
A new WebRequestSession object is created and stored in $Global:O365Session.
The selected connection details are then stored in $Global:O365CurrentConnection..

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -id
The unique id for the connection.
If not specified, the current connection will be cleared.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### $Global:O365Session: Session information for the API.
### $Global:O365CurrentConnection: Connection information for the selected connection.
## NOTES

## RELATED LINKS
