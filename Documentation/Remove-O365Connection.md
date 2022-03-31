---
external help file: WiscO365-help.xml
Module Name: WiscO365
online version: https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api
schema: 2.0.0
---

# Remove-O365Connection

## SYNOPSIS
Removes an existing Office 365 API connection from memory and disk storage.

## SYNTAX

```
Remove-O365Connection [-id] <String> [<CommonParameters>]
```

## DESCRIPTION
The function removes an existing Office 365 API connection from memory and disk storage.
First, the function gets all existing connections using Get-O365Connections.
If the specified connection ID doesn't exist, an error is thrown and processing stops.
The specified connection is removed from $Global:O365Connections.
If the connection was saved, it is also removed from Connections.csv and its corresponding password file is deleted.
If the specified connection was set as the current connection, the current connection is cleared using Set-O365Connection.

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -id
The unique id for the connection.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Connections.csv: Connection details for saved connections (specified connection removed).
### $id.xml: Encrypted password file for saved connection (file for specified connection removed).
### $Global:O365Connections: An array of all connections, both saved and temporary (specified connection removed)..
## NOTES

## RELATED LINKS
