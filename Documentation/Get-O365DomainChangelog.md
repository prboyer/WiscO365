---
external help file: WiscO365-help.xml
Module Name: WiscO365
online version: https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api
schema: 2.0.0
---

# Get-O365DomainChangelog

## SYNOPSIS
Returns a list of modifications made to a domain

## SYNTAX

```
Get-O365DomainChangelog [[-change_types] <Object>] [[-domain] <Object>] [<CommonParameters>]
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

### -change_types
Optional comma-separated list of change keys (e.g.
edit_properties)

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
Domain for which to get change logs (e.g.
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
### success: List of changes to a domain with a change_type, change_description, and timestamp
## NOTES

## RELATED LINKS

[https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api](https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api)
