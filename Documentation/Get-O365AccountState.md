---
external help file: WiscO365-help.xml
Module Name: WiscO365
online version: https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api
schema: 2.0.0
---

# Get-O365AccountState

## SYNOPSIS
Get information about a Service Account or WiscMail Plus account in a domain you administer

## SYNTAX

```
Get-O365AccountState [-account] <Object> [[-to_return] <Object>] [<CommonParameters>]
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

### -account
A unique identifier of the account, such as unique ID or primary email address (e.g.
foo_bar or foo@bar.wisc.edu)

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

### -to_return
\[Optional\] Data to return, comma-separated; options are: exists, sourcesystem, eligibility, primary, readiness

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### failure: null
### success
### exists: 1 if account exists, undef if not
### msol_uid: Unique ID of the account (e.g. foo_bar)
### readiness: a hash with a wide array of data about preparedness to migrate account to Office 365
### sourcesystem: wiscmail|office365|external
## NOTES

## RELATED LINKS

[https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api](https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api)

