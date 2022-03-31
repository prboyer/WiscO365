---
external help file: WiscO365-help.xml
Module Name: WiscO365
online version: https://wiscmail.wisc.edu/admin/index.php?action=domain-domainadmin_api
schema: 2.0.0
---

# Add-O365Connection

## SYNOPSIS
Creates a new connection for the Office 365 API and sets it as the current connection.

## SYNTAX

```
Add-O365Connection [-id] <String> [-userName] <String> [-password] <String> [-domain] <String>
 [[-endpoint] <String>] [-save] [<CommonParameters>]
```

## DESCRIPTION
This function allows a user to add connection properties for the API, giving them the option to save the connection for later use.
The module first imports the existing connections using Get-O365Connections, then checks if that connection ID already exists.
If the ID already exists, an error is thrown and processing stops.
Next, a new PSCredential object is created to store the credentials.
All the connection information is then added $Global:O365Connections.
If the save option is selected, the connection information is also exported to Connections.csv and the PSCredential object is exported to an XML file with a title identical to the specified ID.
Both files are stored in %LOCALAPPDATA%\WindowsPowerShell\ModuleData\WiscO365\Connections.
A stored password can only be used on the computer and by the user account on which it was originally created.
Finally, this connection is set as the current connection using Set-O365Connection.

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -domain
The domain for the connection.
The specified credentials must have administrative access to this domain.
This is also the value that will be used by default by functions with a "domain" parameter.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -endpoint
The endpoint for the connection.
If not specified, the default endpoint is used.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: $defaultEndpoint
Accept pipeline input: False
Accept wildcard characters: False
```

### -id
The unique id for the connection.
This can be whatever the user prefers.

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

### -password
The password for the connection.
This is obtained from the DoIT Mail Team.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -save
If specified, the connection will be saved for use in later sessions.
The connection can only be used on the computer and by the user account on which it was originally created. 
If not specified, the connection can only be used during the session in which it is entered.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -userName
The user name for the connection.
This is obtained from the DoIT Mail Team.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### connections.csv: Connection details for saved connections.
### $id.xml: Encrypted password file for saved connection.
### $Global:O365Connections: An array of all connections, both saved and temporary.
## NOTES

## RELATED LINKS
