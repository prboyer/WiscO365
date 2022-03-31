---
external help file: WiscO365-help.xml
Module Name: WiscO365
online version: https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api
schema: 2.0.0
---

# Get-O365UserInfo

## SYNOPSIS
(Deprecated) Get information about a specific account in a domain; intended for Prep Accounts

## SYNTAX

```
Get-O365UserInfo [-msoluid] <Object> [<CommonParameters>]
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

### -msoluid
Unique ID of the account for which to get details (e.g.
foo_bar)

```yaml
Type: Object
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

### failure: null
### success: Key->value pairs for directory information about account; note: Service Accounts will not include all alternate address values -- use getAccountAddresses
## NOTES

## RELATED LINKS

[https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api](https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api)

