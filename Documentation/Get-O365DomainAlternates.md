---
external help file: WiscO365-help.xml
Module Name: WiscO365
online version: https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api
schema: 2.0.0
---

# Get-O365DomainAlternates

## SYNOPSIS
Gets a list of Office 365 alternate addresses in a domain

## SYNTAX

```
Get-O365DomainAlternates [[-all_addresses] <Object>] [[-domain] <Object>] [<CommonParameters>]
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

### -all_addresses
\[Optional\] If given, return all addresses on returned accounts

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -domain
Domain for which to get a list of alternate addresses (e.g.
bar.wisc.edu)

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: $Global:O365CurrentConnection.domain
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### failure: null
### success
### unique_id
### account_type: Type of account that the alternate address is applied to (e.g. Service Account|NetID)
### addresses: Hash; key is alternate addresses in the domain requested
### can_set_primary: 1 if the authenticated user may set the primary address on the account; 0 if not
### default: 1 if the address is the default address for the account (cannot be removed); 0 if not
### domain: Domain of the account that the alternate address is applied to
### primary: 1 if the address is the primary address for the account it is applied to; 0 if not
### uid: NetID or Unique ID of the account that the alternate address is applied to
## NOTES

## RELATED LINKS

[https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api](https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api)

