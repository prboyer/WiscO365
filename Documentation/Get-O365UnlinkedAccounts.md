---
external help file: WiscO365-help.xml
Module Name: WiscO365
online version: https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api
schema: 2.0.0
---

# Get-O365UnlinkedAccounts

## SYNOPSIS
Get a list of accounts in a domain that are not linked to any NetID

## SYNTAX

```
Get-O365UnlinkedAccounts [[-domain] <Object>] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -domain
Domain for which to get a list of unlinked accounts (e.g.
bar.wisc.edu)

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: $Global:O365CurrentConnection.domain
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### failure: null
### success: List of accounts in the domain that have no linked NetIDs; return value is left-hand side of email address (e.g. foo)
## NOTES

## RELATED LINKS

[https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api](https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api)

