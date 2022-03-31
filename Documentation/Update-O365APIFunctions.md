---
external help file: WiscO365-help.xml
Module Name: WiscO365
online version: https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api
schema: 2.0.0
---

# Update-O365APIFunctions

## SYNOPSIS
Updates the API functions and documentation in the module by getting the methods from the Domain Admin API Documentation.

## SYNTAX

```
Update-O365APIFunctions [-includeAlias] [<CommonParameters>]
```

## DESCRIPTION
This function updates the API functions and documentation in the module by getting the methods from the Domain Admin API Documentation.
It first calls the script $PSScriptRoot\Update\UpdateAPIFunctions.ps1, where most of the processing takes place.
This gets the latest Domain Admin API Documentation from the web using the function Get-O365DomainAdminDoc.
Each method found in the documentation is parsed. 

First, the method name is normalized.
A list of verbs is imported from "$PSScriptRoot\actionWords.csv" and the method name is matched to one of the verbs in the originalVerbs column.
If the verb is not found in the list, the verb is assumed to be the method name string until the first capital letter and is added to actionWords.csv for later use.
If the verb is found in the list and the corresponding value in the approvedVerbs column of actionWords.csv is not null, this indicates that the original verb is an unapproved PowerShell verb.
This value in the approvedVerbs column is substituted as the verb, but the original verb is still retained to be used in a function alias.
If the original verb is an unapproved verb but has no approved verb specified, this unapproved verb is used (this has the potential to cause conflicts, but this is unlikely). 
The original verb is trimmed from the original method name, with the remaining string assumed to be the noun.
A list of unallowed words is imported from "$PSScriptRoot\unallowedWords.txt". 
Any words in this list are trimmed from the noun.
This is to prevent conflicts with functions from other modules (especially Microsoft's official Office 365 module) and to keep the naming convention consistent throughout all functions in the module.
Finally, the function name is generated in the form Verb-PrefixNoun.
The prefix for all functions is O365.
If an unapproved verb existed, a name with the original verb is also generated in this form.

Next, a header is generated for the function, which includes documentation, the function name, and any aliases.
The Synopsis section is set as the method purpose from the documentation.
The Outputs section is set as the method return from the documentation.
The Link section is set to the web address for the Domain Admin API Documentation.
The function name is the name value that was normalized earlier.
If an unapproved verb was found, a normalized name with this verb is included as an alias.
If the includeAlias switch is selected, the original method name from the documentation is added as an alias.

Next, parameters are generated for the function.
The parameter description is set as the parameter description from the documentation.
If "required" in the documentation is "1", the Mandatory property is set to $True.
The exception to this is any function that contains a "domain" parameter.
Regardless of the "required" value in the documentation, a "domain" parameter's Mandatory property is always set to $False.
This allows the user to avoid entering the "domain" value, since the "domain" value is set in the connection properties.
Any "domain" parameter is set to $Global:O365CurrentConnection.domain by default, unless overridden by the user specifying a different value.
The parameter position is determined by the order in which the parameters appear in the documentation, with the first parameter's position set as "0", the second parameter's position set as "1", etc.
If the documentation contains a pre-defined set of values for the parameter, the parameter is set to validate this set of values.
These values are determined by looking for "|" in the parameter description and splitting the string on the "|".

Next, a JSON string is generated for the body of the API method call.
This includes the original method name, parameter names, and variables for the parameter value. 

The function is then formatted as an Advanced PowerShell Function, with all the previously described values included.
Each function includes a call to the helper functions Test-HelperO365Connection (checks that a connection has been set before calling the API method) and Invoke-HelperO365APIFunction (calls the API method using Invoke-RestMethod and processes the return values).
Both of these helper functions can be found at "$PSScriptRoot\HelperFunctions.ps1".
A ps1 file is generated with all the functions and stored as "%LOCALAPPDATA%\WindowsPowerShell\ModuleData\WiscO365\New APIFunctions.ps1".
Control is then returned to the original function, Update-O365APIFunctions.

If a previous API Functions file exists as "%LOCALAPPDATA%\WindowsPowerShell\ModuleData\WiscO365\APIFunctions.ps1", this is compared to the new API Functions file.
If the new API Functions file is different, the old API Functions file and Help File are moved to "%LOCALAPPDATA%\WindowsPowerShell\ModuleData\WiscO365\Old API Functions" and renamed for archiving.
If the new API Functions file is different or if a previous file didn't exist, the new API Functions file is renamed "APIFunctions.ps1". 
The module is then reloaded using the function "Import-Module WiscO365 -Force -DisableNameChecking".
Finally, a new help file is generated for the module as "%LOCALAPPDATA%\WindowsPowerShell\ModuleData\WiscO365\WiscO365 Help.html".
This is generated using the psDoc script ("$PSScriptRoot\Update\psDoc-master\src\psDoc.ps1").
This has been modified to include UW branding and extra sections as defined by the files docFooter.html, docTitle.html, extraBody.html, and extraNav.html in "$PSScriptRoot\Update\psDoc-master\src".
If the new functions file is not different, it is deleted.

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -includeAlias
Includes the original API method name as an alias.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### If no new updates: No Updates | No new API Functions were found.
### If new updates: Updates | New API Functions were found and added.
###     APIFunctions.ps1
###     WiscO365 Help.html
## NOTES

## RELATED LINKS
