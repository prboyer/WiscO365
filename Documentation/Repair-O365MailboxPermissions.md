---
external help file: WiscO365-help.xml
Module Name: WiscO365
online version: https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api
schema: 2.0.0
---

# Repair-O365MailboxPermissions

## SYNOPSIS
Compares permissions assigned locally and in Office 365 to check for inconsistencies and (optionally) repairs the inconsistencies

## SYNTAX

```
Repair-O365MailboxPermissions [-msoluid] <Object> [[-notify_email] <Object>] [-repair_action] <Object>
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

### -msoluid
Unique ID of the account on which to run the permission validation and repair

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

### -notify_email
Email address to which the results should be sent. 
Note that this is the only way you will see the results of calls to this method.

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

### -repair_action
Must be one of: add, remove, use_local, use_o365, or notify. 
Option 'add' applies any permissions missing from either source. 
Option 'remove' removes any permissions missing from either source. 
Option 'use_local' will apply is stored locally to O365. 
Option 'use_o365' will apply what is in O365 to local permissions. 
Option 'notify' will send an email with inconsistent permissions to the 'notify_email' value given which is required for this option.

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### failure: If queuing the job fails, you will receive a null result.
### success: Successfully queuing the job to validate permissions will result in a response of 1.
## NOTES

## RELATED LINKS

[https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api](https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api)

