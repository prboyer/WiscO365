---
external help file: WiscO365-help.xml
Module Name: WiscO365
online version: https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api
schema: 2.0.0
---

# Add-O365ServiceAccount

## SYNOPSIS
Creates an Office 365 Service Account in a domain that is not capable of hosting WiscMail Plus accounts

## SYNTAX

```
Add-O365ServiceAccount [[-authorized_admin] <Object>] [[-description] <Object>] [[-domain] <Object>]
 [-firstname] <Object> [[-fwd_addr] <Object>] [-lastname] <Object> [[-linkednetid] <Object>]
 [[-no_gapps] <Object>] [-sponsornetid] <Object> [-uid] <Object> [[-userpassword] <Object>]
 [<CommonParameters>]
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

### -authorized_admin
(Optional) NetID (or comma-separated list of NetIDs) who will be granted full administrative control over the Service Account

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

### -description
Brief description only available from Admin Site

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

### -domain
Domain to create the Service Account in (e.g.
bar.wisc.edu)

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: $Global:O365CurrentConnection.domain
Accept pipeline input: False
Accept wildcard characters: False
```

### -firstname
First name for Service Account; will be concatenated with lastname to form Display Name

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -fwd_addr
(Optional) Forwarding address that will be applied at the time of creation

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -lastname
Last name for Service Account; will be concatenated with firstname to form Display Name

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -linkednetid
(Optional) NetID (or comma-separated list of NetIDs) who will be granted full permissions to the Service Account and granted some administrative permissions

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -no_gapps
(Optional - Deprecated) If given, the Service Account will not be enabled for Google Apps

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -sponsornetid
NetID of the person who is sponsoring creation of this Service Account

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -uid
Left-hand side of the Service Account email address (e.g.
foo)

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -userpassword
(Optional) Password for the Service Account; must meet the password policy criteria. 
A secure random password will be generated if none is given.

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### failure: null
### success: 1
## NOTES

## RELATED LINKS

[https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api](https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api)

