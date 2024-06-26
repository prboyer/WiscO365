# WiscO365
This module provides a turnkey solution for University of Wisconsin-Madison domain administrators to manage their domain''s Office 365 accounts. It integrates the Domain Admin API, converting all available methods to PowerShell functions for simple execution from the console or in scripts. Functions can be added, removed, and updated as the API is modified. Additionally, this module provides the ability to easily add, save, and manage API connection parameters for later use.

> [!IMPORTANT]
> The module needs to be run initially with administrator permissions to properly update the list of available PowerShell cmdlet from the O365 API.

To get started, enter the function Get-O365Help after importing the module.

- [WiscO365](#wisco365)
	- [Add-O365AllowedNetID](#add-o365allowednetid)
	- [Add-O365Alternate](#add-o365alternate)
	- [Add-O365AuthorizedAdmin](#add-o365authorizedadmin)
	- [Add-O365Connection](#add-o365connection)
	- [Add-O365NetIDAdminAccess](#add-o365netidadminaccess)
	- [Add-O365Resource](#add-o365resource)
	- [Add-O365ServiceAccount](#add-o365serviceaccount)
	- [Disable-O365OutlookAutomapping](#disable-o365outlookautomapping)
	- [Edit-O365Profile](#edit-o365profile)
	- [Edit-O365Resource](#edit-o365resource)
	- [Edit-O365User](#edit-o365user)
	- [Get-O365AccountAddresses](#get-o365accountaddresses)
	- [Get-O365AccountChangelog](#get-o365accountchangelog)
	- [Get-O365AccountSourcesystem](#get-o365accountsourcesystem)
	- [Get-O365AccountState](#get-o365accountstate)
	- [Get-O365AccountTransitionInfo](#get-o365accounttransitioninfo)
	- [Get-O365AdminGroups](#get-o365admingroups)
	- [Get-O365AdministeredObjects](#get-o365administeredobjects)
	- [Get-O365AllowedNetID](#get-o365allowednetid)
	- [Get-O365AuthorizedAdmins](#get-o365authorizedadmins)
	- [Get-O365AuthorizedByAdmin](#get-o365authorizedbyadmin)
	- [Get-O365BasicAuthPolicy](#get-o365basicauthpolicy)
	- [Get-O365CalendarConfiguration](#get-o365calendarconfiguration)
	- [Get-O365CalendarPermission](#get-o365calendarpermission)
	- [Get-O365CalendarProcessing](#get-o365calendarprocessing)
	- [Get-O365Connections](#get-o365connections)
	- [Get-O365ContextAllowedMethods](#get-o365contextallowedmethods)
	- [Get-O365CurrentConnection](#get-o365currentconnection)
	- [Get-O365DomainAdminDoc](#get-o365domainadmindoc)
	- [Get-O365DomainAlternates](#get-o365domainalternates)
	- [Get-O365DomainChangelog](#get-o365domainchangelog)
	- [Get-O365DomainLinkedAccounts](#get-o365domainlinkedaccounts)
	- [Get-O365DomainResources](#get-o365domainresources)
	- [Get-O365DomainSecurityLockedAccounts](#get-o365domainsecuritylockedaccounts)
	- [Get-O365DomainUsersInfo](#get-o365domainusersinfo)
	- [Get-O365Forward](#get-o365forward)
	- [Get-O365GALStatus](#get-o365galstatus)
	- [Get-O365Help](#get-o365help)
	- [Get-O365InboxRules](#get-o365inboxrules)
	- [Get-O365JunkFilters](#get-o365junkfilters)
	- [Get-O365LinkedAccounts](#get-o365linkedaccounts)
	- [Get-O365MailboxLogins](#get-o365mailboxlogins)
	- [Get-O365MailboxPermission](#get-o365mailboxpermission)
	- [Get-O365MobileDevices](#get-o365mobiledevices)
	- [Get-O365PasswordChangeHistory](#get-o365passwordchangehistory)
	- [Get-O365PrimaryAddress](#get-o365primaryaddress)
	- [Get-O365Profile](#get-o365profile)
	- [Get-O365ResourceFullAccess](#get-o365resourcefullaccess)
	- [Get-O365ResourceInfo](#get-o365resourceinfo)
	- [Get-O365UnlinkedAccounts](#get-o365unlinkedaccounts)
	- [Get-O365UserInfo](#get-o365userinfo)
	- [Get-O365UsersByDomain](#get-o365usersbydomain)
	- [Move-O365Alternate](#move-o365alternate)
	- [Remove-O365AllowedNetID](#remove-o365allowednetid)
	- [Remove-O365Alternate](#remove-o365alternate)
	- [Remove-O365AuthorizedAdmin](#remove-o365authorizedadmin)
	- [Remove-O365Connection](#remove-o365connection)
	- [Remove-O365NetIDAdminAccess](#remove-o365netidadminaccess)
	- [Remove-O365Resource](#remove-o365resource)
	- [Remove-O365ServiceAccount](#remove-o365serviceaccount)
	- [Repair-O365MailboxPermissions](#repair-o365mailboxpermissions)
	- [Request-O365NetIDAdminAccess](#request-o365netidadminaccess)
	- [Reset-O365Password](#reset-o365password)
	- [Search-O365Objects](#search-o365objects)
	- [Set-O365BasicAuthPolicy](#set-o365basicauthpolicy)
	- [Set-O365CalendarConfiguration](#set-o365calendarconfiguration)
	- [Set-O365CalendarProcessing](#set-o365calendarprocessing)
	- [Set-O365Connection](#set-o365connection)
	- [Set-O365Forward](#set-o365forward)
	- [Set-O365GALStatus](#set-o365galstatus)
	- [Set-O365MailboxPermission](#set-o365mailboxpermission)
	- [Set-O365MailboxPolicy](#set-o365mailboxpolicy)
	- [Set-O365MailPrimaryAddress](#set-o365mailprimaryaddress)
	- [Set-O365PrimaryAddress](#set-o365primaryaddress)
	- [Set-O365ResourceFullAccess](#set-o365resourcefullaccess)
	- [Set-O365StartupPreferences](#set-o365startuppreferences)
	- [Update-O365APIFunctions](#update-o365apifunctions)

<hr>

## Add-O365AllowedNetID
### Synopsis
Grants access to a NetID to administer the account; also grants delegated mailbox access
### Syntax
```
Add-O365AllowedNetID [-addr] <Object> [-netid] <Object> [<CommonParameters>]
```
### Add-O365AllowedNetID Aliases
 - addAllowedNetID

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>addr</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Primary email address of the account to which a NetID is being granted access (e.g. foo@bar.wisc.edu)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>netid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>The NetID that should be granted access to the account (e.g. bbadger)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Add-O365Alternate
### Synopsis
Adds an alternate address to an Office 365 account
### Syntax
```
Add-O365Alternate [-alternate] <Object> [[-domain] <Object>] [-msoluid] <Object> [-sponsornetid] <Object>
[<CommonParameters>]
```
### Add-O365Alternate Aliases
 - addAlternate

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>alternate</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Fully qualified new alternate email address to add (e.g. foo@bar.wisc.edu)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>domain</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>The domain of the alternate address.  Must match domain in alternate value (e.g. bar.wisc.edu)</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">$Global:O365CurrentConnection.domain</td>
		</tr>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the account to which the alternate address should be added</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>sponsornetid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>The NetID of the user requesting the alternate address be assigned (e.g. bbadger)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Add-O365AuthorizedAdmin
### Synopsis
Grants full administrative control over a Service Account or Resource to a NetID
### Syntax
```
Add-O365AuthorizedAdmin [-admin] <Object> [-msoluid] <Object> [<CommonParameters>]
```
### Add-O365AuthorizedAdmin Aliases
 - addAuthorizedAdmin

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>admin</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>NetID of the user to which access is being granted</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the Service Account or Resource for which to grant access</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Add-O365Connection
### Synopsis
Creates a new connection for the Office 365 API and sets it as the current connection.
### Syntax
```
Add-O365Connection [-id] <String> [-userName] <String> [-password] <String> [-domain] <String> [[-endpoint] <String>]
[[-save]] [<CommonParameters>]
```
### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>id</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>The unique id for the connection. This can be whatever the user prefers.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>userName</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>The user name for the connection. This is obtained from the DoIT Mail Team.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>password</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>The password for the connection. This is obtained from the DoIT Mail Team.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>domain</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>The domain for the connection. The specified credentials must have administrative access to this domain. This is also
the value that will be used by default by functions with a "domain" parameter.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>endpoint</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>The endpoint for the connection. If not specified, the default endpoint is used.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">$defaultEndpoint</td>
		</tr>
		<tr>
			<td><nobr>save</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>If specified, the connection will be saved for use in later sessions. The connection can only be used on the computer
and by the user account on which it was originally created.
If not specified, the connection can only be used during the session in which it is entered.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">False</td>
		</tr>
	</tbody>
</table>

### Outputs
- connections.csv: Connection details for saved connections.
- $id.xml: Encrypted password file for saved connection.
- $Global:O365Connections: An array of all connections, both saved and temporary.
## Add-O365NetIDAdminAccess
### Synopsis
Adds a Manifest group to administer a NetID
### Syntax
```
Add-O365NetIDAdminAccess [-group] <Object> [-netid] <Object> [<CommonParameters>]
```
### Add-O365NetIDAdminAccess Aliases
 - addNetIDAdminAccess

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>group</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Manifest group ID that is being granted administrative access over the NetID</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>netid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>NetID to which the Manifest group is being granted access</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Add-O365Resource
### Synopsis
Creates an Office 365 Resource
### Syntax
```
Add-O365Resource [[-authorized\\_admin] <Object>] [[-description] <Object>] [-displayname] <Object> [[-domain] <Object>]
[-owner] <Object> [-resourcetype] <Object> [-sponsornetid] <Object> [-uid] <Object> [<CommonParameters>]
```
### Add-O365Resource Aliases
 - addMsolResource

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>authorized\\_admin</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>(Optional) NetID (or comma-separated list of NetIDs) who will be granted full administrative control over the Resource</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>description</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Brief description only available from Admin Site</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>displayname</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Name of the resource to be displayed in most places (e.g. Foo Room)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>domain</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Domain to create the resource in (e.g. bar.wisc.edu)</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">$Global:O365CurrentConnection.domain</td>
		</tr>
		<tr>
			<td><nobr>owner</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>User who will be granted full permissions to the resource and granted some administrative permissions</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>resourcetype</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>room or equipment</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>sponsornetid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>NetID of the person who is sponsoring creation of this resource</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>uid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Left-hand side of the resource email address (e.g. foo\\_room)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Add-O365ServiceAccount
### Synopsis
Creates an Office 365 Service Account in a domain that is not capable of hosting WiscMail Plus accounts
### Syntax
```
Add-O365ServiceAccount [[-authorized\\_admin] <Object>] [[-description] <Object>] [[-domain] <Object>] [-firstname]
<Object> [[-fwd\\_addr] <Object>] [-lastname] <Object> [[-linkednetid] <Object>] [[-no\\_gapps] <Object>] [-sponsornetid]
<Object> [-uid] <Object> [[-userpassword] <Object>] [<CommonParameters>]
```
### Add-O365ServiceAccount Aliases
 - addServiceAccount

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>authorized\\_admin</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>(Optional) NetID (or comma-separated list of NetIDs) who will be granted full administrative control over the Service
Account</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>description</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Brief description only available from Admin Site</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>domain</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Domain to create the Service Account in (e.g. bar.wisc.edu)</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">$Global:O365CurrentConnection.domain</td>
		</tr>
		<tr>
			<td><nobr>firstname</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>First name for Service Account; will be concatenated with lastname to form Display Name</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>fwd\\_addr</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>(Optional) Forwarding address that will be applied at the time of creation</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>lastname</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Last name for Service Account; will be concatenated with firstname to form Display Name</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>linkednetid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>(Optional) NetID (or comma-separated list of NetIDs) who will be granted full permissions to the Service Account and
granted some administrative permissions</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>no\\_gapps</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>(Optional - Deprecated) If given, the Service Account will not be enabled for Google Apps</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>sponsornetid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>NetID of the person who is sponsoring creation of this Service Account</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>uid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Left-hand side of the Service Account email address (e.g. foo)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>userpassword</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>(Optional) Password for the Service Account; must meet the password policy criteria.  A secure random password will be
generated if none is given.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Disable-O365OutlookAutomapping
### Synopsis
Removes the automapping from Outlook for all users that currently have Full Mailbox permission
### Syntax
```
Disable-O365OutlookAutomapping [-msoluid] <Object> [<CommonParameters>]
```
### Disable-O365OutlookAutomapping Aliases
 - disableMsolOutlookAutomapping

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the Service Account from which to remove all existing automapping settings</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Edit-O365Profile
### Synopsis
Add or update profile attributes for a Service Account
### Syntax
```
Edit-O365Profile [[-company] <Object>] [[-department] <Object>] [[-facsimiletelephonenumber] <Object>] [[-homephone]
<Object>] [[-mobile] <Object>] [-msoluid] <Object> [[-physicaldeliveryofficename] <Object>] [[-postalcode] <Object>]
[[-telephonenumber] <Object>] [[-title] <Object>] [<CommonParameters>]
```
### Edit-O365Profile Aliases
 - editMsolProfile

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>company</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Company value</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>department</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Department value</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>facsimiletelephonenumber</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Business Fax value</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>homephone</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Home phone number value</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>mobile</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Mobile phone number value</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique identifier for the Service Account</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>physicaldeliveryofficename</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Business Address street value</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>postalcode</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Business Address postcal code value</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>telephonenumber</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Business phone number value</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>title</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Job Title value</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Edit-O365Resource
### Synopsis
Change the name or owner of an Office 365 Resource
### Syntax
```
Edit-O365Resource [-description] <Object> [-msoluid] <Object> [-name] <Object> [-owner] <Object> [<CommonParameters>]
```
### Edit-O365Resource Aliases
 - editMsolResource

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>description</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Brief description only available from Admin Site</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the Resource to edit (e.g. foo\\_room\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>name</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>The Display Name of the resource; required, but does not need to change</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>owner</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>User who will be granted full permissions to the resource and granted some administrative permissions; required, but
does not need to change</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Edit-O365User
### Synopsis
Change the first or last name of an Office 365 Service Account
### Syntax
```
Edit-O365User [[-description] <Object>] [[-firstname] <Object>] [[-lastname] <Object>] [-msoluid] <Object>
[<CommonParameters>]
```
### Edit-O365User Aliases
 - editMsolUser

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>description</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Brief description only available from Admin Site</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>firstname</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>First name for Service Account; will be concatenated with lastname to form Display Name; required, but does not need
to change</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>lastname</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Last name for Service Account; will be concatenated with firstname to form Display Name; required, but does not need
to change</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the Service Account to edit (e.g. foo\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365AccountAddresses
### Synopsis
Gets the full list of email addresses applied to an account
### Syntax
```
Get-O365AccountAddresses [-msoluid] <Object> [<CommonParameters>]
```
### Get-O365AccountAddresses Aliases
 - getAccountAddresses

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the account to get addresses on (e.g. foo\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: List of email addresses on an account
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365AccountChangelog
### Synopsis
Returns a list of modifications made to an account
### Syntax
```
Get-O365AccountChangelog [[-change\\_types] <Object>] [-msoluid] <Object> [<CommonParameters>]
```
### Get-O365AccountChangelog Aliases
 - getAccountChangelog

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>change\\_types</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Optional comma-separated list of change keys (e.g. create\\_account)</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the account for which to get change logs (e.g. foo\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: List of changes to an account with a change\\_type, change\\_description, and timestamp
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365AccountSourcesystem
### Synopsis
Get the system that an account is hosted on
### Syntax
```
Get-O365AccountSourcesystem [-account] <Object> [<CommonParameters>]
```
### Get-O365AccountSourcesystem Aliases
 - get_account_sourcesystem

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>account</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>A unique identifier of the account, such as unique ID or primary email address (e.g. foo\\_bar or foo@bar.wisc.edu)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null (if unknown or not-existent)
- success: wiscmail|office365|external
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365AccountState
### Synopsis
Get information about a Service Account or WiscMail Plus account in a domain you administer
### Syntax
```
Get-O365AccountState [-account] <Object> [[-to\\_return] <Object>] [<CommonParameters>]
```
### Get-O365AccountState Aliases
 - get_account_state

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>account</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>A unique identifier of the account, such as unique ID or primary email address (e.g. foo\\_bar or foo@bar.wisc.edu)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>to\\_return</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>[Optional] Data to return, comma-separated; options are: exists, sourcesystem, eligibility, primary, readiness</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success
- exists: 1 if account exists, undef if not
- msol\\_uid: Unique ID of the account (e.g. foo\\_bar)
- readiness: a hash with a wide array of data about preparedness to migrate account to Office 365
- sourcesystem: wiscmail|office365|external
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365AccountTransitionInfo
### Synopsis
Get information about when and how an account transitioned to Office 365, if available
### Syntax
```
Get-O365AccountTransitionInfo [-msoluid] <Object> [<CommonParameters>]
```
### Get-O365AccountTransitionInfo Aliases
 - getAccountTransitionInfo

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the account to get transition information about (e.g. foo\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: Transition timestamp and if the account was force transitioned
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365AdminGroups
### Synopsis
Gets a list of Manifest groups that have administrative access to a NetID
### Syntax
```
Get-O365AdminGroups [-netid] <Object> [<CommonParameters>]
```
### Get-O365AdminGroups Aliases
 - getAdminGroups

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>netid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>The NetID for which to get the list of groups with administrative access</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: List of groups with access or pending access; pending groups will show as PENDING in the response
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365AdministeredObjects
### Synopsis
Provides a list of objects that the authenticated user can administer
### Syntax
```
Get-O365AdministeredObjects [<CommonParameters>]
```
### Get-O365AdministeredObjects Aliases
 - getAdministeredObjects

### Outputs
- failure: null
- success: A list of objects and basic details about the objects
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365AllowedNetID
### Synopsis
Gets list of NetIDs that have access to administer the Service Account; these NetIDs also have full mailbox access
### Syntax
```
Get-O365AllowedNetID [-addr] <Object> [<CommonParameters>]
```
### Get-O365AllowedNetID Aliases
 - getAllowedNetID

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>addr</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Address of the Service Account for which to get allowed NetIDs (e.g. foo@bar.wisc.edu)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: A list of NetIDs that have administrative access; list may be empty if there are none
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365AuthorizedAdmins
### Synopsis
Gets list of NetIDs that have full administrative access over the Service Account or Resource
### Syntax
```
Get-O365AuthorizedAdmins [-msoluid] <Object> [<CommonParameters>]
```
### Get-O365AuthorizedAdmins Aliases
 - getAuthorizedAdmins

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the Service Account or Resource for which to get authorized administrators</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: List of NetIDs; empty list if none
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365AuthorizedByAdmin
### Synopsis
Gets list of Service Accounts and/or Resources that the NetID has administrative access over
### Syntax
```
Get-O365AuthorizedByAdmin [[-acct\\_type] <Object>] [-msoluid] <Object> [<CommonParameters>]
```
### Get-O365AuthorizedByAdmin Aliases
 - getAuthorizedByAdmin

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>acct\\_type</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>[optional] String identifying account types to return; examples: 'service', 'resource', or 'service and resource',
'all'. Defaults to 'service' if not given.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID (NetID) of the account for which to get a list of Service Accounts and/or Resources administered</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: List of Service Accounts and/or Resources; empty list if none
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365BasicAuthPolicy
### Synopsis
Get the status of Office 365 basic authentication for a Service Account
### Syntax
```
Get-O365BasicAuthPolicy [[-detail] <Object>] [-msoluid] <Object> [<CommonParameters>]
```
### Get-O365BasicAuthPolicy Aliases
 - getMsolBasicAuthPolicy

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>detail</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>[Optional] Will a complex response with additional details about the basic auth policy for this account</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the account for which to get Office 365 Basic Auth policy (e.g. foo\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: Returns the string 'Blocked' if Basic Authentication is disallowed, or the string 'Allowed' if Basic
- Authentication is allowed
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365CalendarConfiguration
### Synopsis
Get a calendar configuration details
### Syntax
```
Get-O365CalendarConfiguration [[-include\\_metadata] <Object>] [[-request\\_params] <Object>] [-resource\\_email] <Object>
[<CommonParameters>]
```
### Get-O365CalendarConfiguration Aliases
 - getCalendarConfiguration

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>include\\_metadata</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>If defined, the return value will include metadata</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>request\\_params</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Parameters to get the calendar configuration for</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>resource\\_email</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>The email address of the resource for which to get configuration details</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: A set of keys and values with the configuration settings
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365CalendarPermission
### Synopsis
Get the Calendar permissions on an Office 365 Service Account or Resource
### Syntax
```
Get-O365CalendarPermission [-msoluid] <Object> [<CommonParameters>]
```
### Get-O365CalendarPermission Aliases
 - getMsolCalendarPermission

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the account for which to get calendar permissions (e.g. foo\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: An array of permissions with the following key/values: user (string, display name of the user with
- permissions), rights (string, comma-separated list of permissions for the user); returns empty array if none
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365CalendarProcessing
### Synopsis
Details about how Exchange Online handles resource calendar events
### Syntax
```
Get-O365CalendarProcessing [[-include\\_metadata] <Object>] [[-request\\_params] <Object>] [-resource\\_email] <Object>
[<CommonParameters>]
```
### Get-O365CalendarProcessing Aliases
 - getCalendarProcessing

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>include\\_metadata</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>(Optional) Include details about the paramater, including acceptable values that it can be set to</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>request\\_params</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>[Optional] Comma-separated or array of calendar processing values for which to request about the resource; if not
provided, all available data is returned</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>resource\\_email</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Email address of the O365 resource for which to get calendar processing information (e.g. foo\\_room@bar.wisc.edu)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: Array of parameters requested (or all if none requested); each item will include key/value pairs with name,
- value, updating, and metadata (if requested)
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365Connections
### Synopsis
Gets all the existing connections for the Office 365 API, both saved and in-memory.
### Syntax
```
Get-O365Connections [<CommonParameters>]
```
### Outputs
- An array of all existing connections is returned.
## Get-O365ContextAllowedMethods
### Synopsis
Gives a list of methods available based on the provided context
### Syntax
```
Get-O365ContextAllowedMethods [[-context] <Object>] [<CommonParameters>]
```
### Get-O365ContextAllowedMethods Aliases
 - getContextAllowedMethods

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>context</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>An identifier for the object you want to get available methods on, such as foo\\_bar, or bar.wisc.edu</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: A list of methods avaialble based on the context given
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365CurrentConnection
### Synopsis
Gets the currently selected connection.
### Syntax
```
Get-O365CurrentConnection [<CommonParameters>]
```
### Outputs
- The details of the currently selection connection are returned.
## Get-O365DomainAdminDoc
### Synopsis
Gets the documentation for the Domain Admin API, which is what you are viewing right now
### Syntax
```
Get-O365DomainAdminDoc [[-domain] <Object>] [<CommonParameters>]
```
### Get-O365DomainAdminDoc Aliases
 - getDomainAdminDoc

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>domain</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Domain name (e.g. bar.wisc.edu)</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">$Global:O365CurrentConnection.domain</td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: JSON array with all Domain Admin API documentation
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365DomainAlternates
### Synopsis
Gets a list of Office 365 alternate addresses in a domain
### Syntax
```
Get-O365DomainAlternates [[-all\\_addresses] <Object>] [[-domain] <Object>] [<CommonParameters>]
```
### Get-O365DomainAlternates Aliases
 - getDomainAlternates

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>all\\_addresses</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>[Optional] If given, return all addresses on returned accounts</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>domain</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Domain for which to get a list of alternate addresses (e.g. bar.wisc.edu)</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">$Global:O365CurrentConnection.domain</td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success
- unique\\_id
- account\\_type: Type of account that the alternate address is applied to (e.g. Service Account|NetID)
- addresses: Hash; key is alternate addresses in the domain requested
- can\\_set\\_primary: 1 if the authenticated user may set the primary address on the account; 0 if not
- default: 1 if the address is the default address for the account (cannot be removed); 0 if not
- domain: Domain of the account that the alternate address is applied to
- primary: 1 if the address is the primary address for the account it is applied to; 0 if not
- uid: NetID or Unique ID of the account that the alternate address is applied to
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365DomainChangelog
### Synopsis
Returns a list of modifications made to a domain
### Syntax
```
Get-O365DomainChangelog [[-change\\_types] <Object>] [[-domain] <Object>] [<CommonParameters>]
```
### Get-O365DomainChangelog Aliases
 - getDomainChangelog

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>change\\_types</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Optional comma-separated list of change keys (e.g. edit\\_properties)</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>domain</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Domain for which to get change logs (e.g. bar.wisc.edu)</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">$Global:O365CurrentConnection.domain</td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: List of changes to a domain with a change\\_type, change\\_description, and timestamp
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365DomainLinkedAccounts
### Synopsis
Returns a list of accounts that with linked NetIDs in the domain
### Syntax
```
Get-O365DomainLinkedAccounts [[-domain] <Object>] [[-netid] <Object>] [<CommonParameters>]
```
### Get-O365DomainLinkedAccounts Aliases
 - getDomainLinkedAccounts

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>domain</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Domain for which to get linked NetIDs (e.g. bar.wisc.edu)</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">$Global:O365CurrentConnection.domain</td>
		</tr>
		<tr>
			<td><nobr>netid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>(Optional) If given, returns only accounts linked to the NetID in this domain</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: List of objects that includes account identifier and linked NetID(s)
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365DomainResources
### Synopsis
Get a list of Office 365 Resources in a domain
### Syntax
```
Get-O365DomainResources [[-domain] <Object>] [<CommonParameters>]
```
### Get-O365DomainResources Aliases
 - getO365DomainResources

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>domain</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Domain for which to get a list of Office 365 resources (e.g. bar.wisc.edu)</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">$Global:O365CurrentConnection.domain</td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success
- description: Description
- displayname: Primary identifier of the resource in the GAL and in events (e.g. Foo Room)
- mail: Email address for the resource (e.g. foo-room@bar.wisc.edu)
- msol\\_uid: Unique ID for the resource (e.g. foo-room\\_bar)
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365DomainSecurityLockedAccounts
### Synopsis
Returns a list of Service Accounts that have been security locked
### Syntax
```
Get-O365DomainSecurityLockedAccounts [[-domain] <Object>] [<CommonParameters>]
```
### Get-O365DomainSecurityLockedAccounts Aliases
 - getDomainSecurityLockedAccounts

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>domain</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Domain in which to get list of locked accounts (e.g. bar.wisc.edu)</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">$Global:O365CurrentConnection.domain</td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: List of unique IDs for locked accounts and timestamp indicating when the account was locked
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365DomainUsersInfo
### Synopsis
Get a list of all accounts in a domain and some details about each
### Syntax
```
Get-O365DomainUsersInfo [[-domain] <Object>] [<CommonParameters>]
```
### Get-O365DomainUsersInfo Aliases
 - getDomainUsersInfo

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>domain</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Domain for which to get a list accounts and information (e.g. bar.wisc.edu)</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">$Global:O365CurrentConnection.domain</td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success
- accounttype: user|role|alias|service
- description: example description
- givenname: Foo
- mailquota: 1000M
- netid: foo
- surname: Bar
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365Forward
### Synopsis
Get the forwarding address (if any) on a Service Account
### Syntax
```
Get-O365Forward [-msoluid] <Object> [<CommonParameters>]
```
### Get-O365Forward Aliases
 - getMsolForward

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the account for which to get the forward (e.g. foo\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: forward if present or an empty string if none
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365GALStatus
### Synopsis
Determine whether an account is visible in or hidden from the Office 365 Global Address List (GAL)
### Syntax
```
Get-O365GALStatus [-msoluid] <Object> [<CommonParameters>]
```
### Get-O365GALStatus Aliases
 - getO365GALStatus

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the account for which to get GAL search status (e.g. foo\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: visible|hidden
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365Help
### Synopsis
Launches the HTML help documentation for the module.
### Syntax
```
Get-O365Help [<CommonParameters>]
```
### Outputs
- WiscO365 Help.html or WiscO365 Initial Help.html
## Get-O365InboxRules
### Synopsis
Get the inbox rules (if any) on a Service Account
### Syntax
```
Get-O365InboxRules [-msoluid] <Object> [<CommonParameters>]
```
### Get-O365InboxRules Aliases
 - getMsolInboxRules

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the account for which to get inbox rules (e.g. foo\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: An array of Inbox rules with the following key/values: name (string), priority (integer), conditions (array,
- list of conditions that triggers the rule), actions (array, actions to take on message); returns empty array if none
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365JunkFilters
### Synopsis
Get the junk mail filter settings for a Service Account
### Syntax
```
Get-O365JunkFilters [-msoluid] <Object> [<CommonParameters>]
```
### Get-O365JunkFilters Aliases
 - getMsolJunkFilters

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the account for which to get junk mail filters (e.g. foo\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: enabled: 1|0, trust\\_contacts: 1|0, only\\_trust\\_lists: 1|0, trusted\\_senders: array of addresses or domains,
- blocked\\_senders: array of addresses or domains
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365LinkedAccounts
### Synopsis
Obtain a list of Service Accounts that are linked to a NetID
### Syntax
```
Get-O365LinkedAccounts [-netid] <Object> [<CommonParameters>]
```
### Get-O365LinkedAccounts Aliases
 - getLinkedAccounts

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>netid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>NetID of the account for which to obtain the list of linked Service Accounts</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: List of Service Accounts; list will be empty if none
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365MailboxLogins
### Synopsis
Get information about protocols and clients being used to access a mailbox.
### Syntax
```
Get-O365MailboxLogins [[-days] <Object>] [[-days\\_ago] <Object>] [-msoluid] <Object> [<CommonParameters>]
```
### Get-O365MailboxLogins Aliases
 - getMsolMailboxLogins

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>days</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>[Optional] Number of days of data to request</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>days\\_ago</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>[Optional] The latest day to get information about (number of days ago)</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>The unique ID of the account for which to get mailbox access information</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: A list of successful mailbox logins by owner; each item includes the IP of the client, the client user agent
- string, and a timestamp of the login
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365MailboxPermission
### Synopsis
Retrieve mailbox permissions on an Office 365 account
### Syntax
```
Get-O365MailboxPermission [-msoluid] <Object> [<CommonParameters>]
```
### Get-O365MailboxPermission Aliases
 - getMsolMailboxPermission

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the account for which to get mailbox permissions (e.g. foo\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success
- result
- fullMailbox: list of users with Full Mailbox permission
- sendAs: list of users with Send As permission
- sendOnBehalf: list of users with Send On Behalf permission
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365MobileDevices
### Synopsis
Gets a list of mobile devices that have been granted access to connect with Exchange Active Sync to an O365 account
### Syntax
```
Get-O365MobileDevices [-msoluid] <Object> [<CommonParameters>]
```
### Get-O365MobileDevices Aliases
 - getMsolMobileDevices

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the account for which to get connected mobile devices (e.g. foo\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: Returns an array of clients that have been connected to the account.  Each returned client has some
- information about it.
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365PasswordChangeHistory
### Synopsis
Provides a list of occurrences when the password has changed for a Service Account
### Syntax
```
Get-O365PasswordChangeHistory [-msoluid] <Object> [<CommonParameters>]
```
### Get-O365PasswordChangeHistory Aliases
 - getPasswordChangeHistory

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the account for which to get the password change history (e.g. foo\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: A list of changes with a timestamp and user for each
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365PrimaryAddress
### Synopsis
Gets the primary address for an account from Office 365
### Syntax
```
Get-O365PrimaryAddress [-msoluid] <Object> [<CommonParameters>]
```
### Get-O365PrimaryAddress Aliases
 - getMsolPrimaryAddress

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the account for which to get the primary address (e.g. foo\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: Primary address for the given account
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365Profile
### Synopsis
Get profile information (address, phone numbers, etc) about a Service Account
### Syntax
```
Get-O365Profile [-msoluid] <Object> [<CommonParameters>]
```
### Get-O365Profile Aliases
 - getMsolProfile

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the Service Account</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: key/value pairs with profile information
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365ResourceFullAccess
### Synopsis
Get a list of users that have full access to an Office 365 resource
### Syntax
```
Get-O365ResourceFullAccess [-msoluid] <Object> [<CommonParameters>]
```
### Get-O365ResourceFullAccess Aliases
 - getMsolResourceFullAccess

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the resource (e.g. room\\_1234\\_foo)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: List of users that have full access and the source of that access (e.g. resource owner or granted to the user)
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365ResourceInfo
### Synopsis
Get basic details about an Office 365 Resource
### Syntax
```
Get-O365ResourceInfo [-msoluid] <Object> [<CommonParameters>]
```
### Get-O365ResourceInfo Aliases
 - getMsolResourceInfo

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the resource for which to get details (e.g. room\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: Resource name, email address, description, and type
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365UnlinkedAccounts
### Synopsis
Get a list of accounts in a domain that are not linked to any NetID
### Syntax
```
Get-O365UnlinkedAccounts [[-domain] <Object>] [<CommonParameters>]
```
### Get-O365UnlinkedAccounts Aliases
 - getUnlinkedAccounts

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>domain</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Domain for which to get a list of unlinked accounts (e.g. bar.wisc.edu)</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">$Global:O365CurrentConnection.domain</td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: List of accounts in the domain that have no linked NetIDs; return value is left-hand side of email address
- (e.g. foo)
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365UserInfo
### Synopsis
(Deprecated) Get information about a specific account in a domain; intended for Prep Accounts
### Syntax
```
Get-O365UserInfo [-msoluid] <Object> [<CommonParameters>]
```
### Get-O365UserInfo Aliases
 - getUserInfo

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the account for which to get details (e.g. foo\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: Key->value pairs for directory information about account; note: Service Accounts will not include all
- alternate address values -- use getAccountAddresses
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Get-O365UsersByDomain
### Synopsis
Gets a list of accounts in a domain
### Syntax
```
Get-O365UsersByDomain [[-domain] <Object>] [<CommonParameters>]
```
### Get-O365UsersByDomain Aliases
 - getUsersByDomain

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>domain</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Domain for which to get a list of accounts (e.g. bar.wisc.edu)</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">$Global:O365CurrentConnection.domain</td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: List of accounts in the domain; return value is the left-hand side of the email address (e.g. foo)
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Move-O365Alternate
### Synopsis
Reassigns an existing alternate address on one account to another account
### Syntax
```
Move-O365Alternate [-alternate] <Object> [[-domain] <Object>] [-msoluid] <Object> [<CommonParameters>]
```
### Move-O365Alternate Aliases
 - reassignAlternate
 - Reassign-O365Alternate

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>alternate</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>The alternate address that is currently assigned to some account that should be reassigned to another account (e.g.
foo@bar.wisc.edu)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>domain</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>The domain of the alternate address.  Must match domain in alternate value (e.g. bar.wisc.edu)</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">$Global:O365CurrentConnection.domain</td>
		</tr>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the new account to which the alternate address should be added (e.g. foo\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Remove-O365AllowedNetID
### Synopsis
Revokes access from a NetID to administer the account; also removes delegated mailbox access
### Syntax
```
Remove-O365AllowedNetID [-addr] <Object> [-netid] <Object> [<CommonParameters>]
```
### Remove-O365AllowedNetID Aliases
 - removeAllowedNetID

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>addr</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Primary email address of the account from which a NetID is being revoked access (e.g. foo@bar.wisc.edu)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>netid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>The NetID that should have access revoked from the account (e.g. bbadger)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Remove-O365Alternate
### Synopsis
Removes an alternate address from an Office 365 account
### Syntax
```
Remove-O365Alternate [-alternate] <Object> [[-domain] <Object>] [<CommonParameters>]
```
### Remove-O365Alternate Aliases
 - removeAlternate

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>alternate</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Alternate email address to remove (e.g. foo@bar.wisc.edu)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>domain</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>The domain of the alternate address.  Must match domain in alternate value (e.g. bar.wisc.edu)</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">$Global:O365CurrentConnection.domain</td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Remove-O365AuthorizedAdmin
### Synopsis
Revokes administrative control over a Service Account or Resource from a NetID
### Syntax
```
Remove-O365AuthorizedAdmin [-admin] <Object> [-msoluid] <Object> [<CommonParameters>]
```
### Remove-O365AuthorizedAdmin Aliases
 - removeAuthorizedAdmin

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>admin</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>NetID of the user from which access is being revoked</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the Service Account or Resource to which access is being revoked</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Remove-O365Connection
### Synopsis
Removes an existing Office 365 API connection from memory and disk storage.
### Syntax
```
Remove-O365Connection [-id] <String> [<CommonParameters>]
```
### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>id</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>The unique id for the connection.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- Connections.csv: Connection details for saved connections (specified connection removed).
- $id.xml: Encrypted password file for saved connection (file for specified connection removed).
- $Global:O365Connections: An array of all connections, both saved and temporary (specified connection removed)..
## Remove-O365NetIDAdminAccess
### Synopsis
Revokes access from a Manifest group to administer a NetID
### Syntax
```
Remove-O365NetIDAdminAccess [-group] <Object> [-netid] <Object> [<CommonParameters>]
```
### Remove-O365NetIDAdminAccess Aliases
 - removeNetIDAdminAccess

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>group</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Manifest group ID that is being revoked administrative access over the NetID</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>netid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>NetID to which the Manifest group is being revoked access</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Remove-O365Resource
### Synopsis
Deletes an Office 365 Resource
### Syntax
```
Remove-O365Resource [-msoluid] <Object> [<CommonParameters>]
```
### Remove-O365Resource Aliases
 - deleteMsolResource
 - Delete-O365Resource

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the Resource to delete (e.g. foo\\_room\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Remove-O365ServiceAccount
### Synopsis
Deletes an Office 365 Service Account
### Syntax
```
Remove-O365ServiceAccount [-msoluid] <Object> [<CommonParameters>]
```
### Remove-O365ServiceAccount Aliases
 - Delete-O365ServiceAccount
 - deleteServiceAccount

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the Service Account to delete (e.g. foo\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Repair-O365MailboxPermissions
### Synopsis
Compares permissions assigned locally and in Office 365 to check for inconsistencies and (optionally) repairs the inconsistencies
### Syntax
```
Repair-O365MailboxPermissions [-msoluid] <Object> [[-notify\\_email] <Object>] [-repair\\_action] <Object>
[<CommonParameters>]
```
### Repair-O365MailboxPermissions Aliases
 - repairMsolMailboxPermissions

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the account on which to run the permission validation and repair</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>notify\\_email</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Email address to which the results should be sent.  Note that this is the only way you will see the results of calls
to this method.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>repair\\_action</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Must be one of: add, remove, use\\_local, use\\_o365, or notify.  Option 'add' applies any permissions missing from either
source.  Option 'remove' removes any permissions missing from either source.  Option 'use\\_local' will apply is stored
locally to O365.  Option 'use\\_o365' will apply what is in O365 to local permissions.  Option 'notify' will send an
email with inconsistent permissions to the 'notify\\_email' value given which is required for this option.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: If queuing the job fails, you will receive a null result.
- success: Successfully queuing the job to validate permissions will result in a response of 1.
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Request-O365NetIDAdminAccess
### Synopsis
Requests administrative access over a NetID for a Manifest group
### Syntax
```
Request-O365NetIDAdminAccess [-group] <Object> [-netid] <Object> [<CommonParameters>]
```
### Request-O365NetIDAdminAccess Aliases
 - requestNetIDAdminAccess

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>group</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Manifest group ID for which administrative access is being requested</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>netid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>NetID to which the Manifest group is requesting administrative access</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Reset-O365Password
### Synopsis
Change the password for an account
### Syntax
```
Reset-O365Password [-msoluid] <Object> [[-password] <Object>] [<CommonParameters>]
```
### Reset-O365Password Aliases
 - resetPassword

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the account for which the password is being changed (e.g. foo\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>password</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>[Optional] New password for the account; must meet password policy requirements.  If no password is provided, a random
password is generated and not returned.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Search-O365Objects
### Synopsis
Find a list of objects that the authenticated account can administer based on a search string
### Syntax
```
Search-O365Objects [-search\\_string] <Object> [<CommonParameters>]
```
### Search-O365Objects Aliases
 - searchObjects

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>search\\_string</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Objects matching this search\\_string will be returned, including name, email address, or unique ID</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: A list of objects and basic details about the objects that match the search\\_string
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Set-O365BasicAuthPolicy
### Synopsis
Set the status of Office 365 basic authentication for a Service Account
### Syntax
```
Set-O365BasicAuthPolicy [[-enable] <Object>] [-msoluid] <Object> [<CommonParameters>]
```
### Set-O365BasicAuthPolicy Aliases
 - setMsolBasicAuthPolicy

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>enable</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Use '1' or anything that will evaluate to true to allow basic authentication, or 0, null, or any other false value to
disallow basic auth</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the account for which to set Office 365 Basic Auth policy (e.g. foo\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Set-O365CalendarConfiguration
### Synopsis
Change a calendar configuration details
### Syntax
```
Set-O365CalendarConfiguration [-param\\_name] <Object> [-param\\_value] <Object> [-resource\\_email] <Object>
[<CommonParameters>]
```
### Set-O365CalendarConfiguration Aliases
 - setCalendarConfiguration

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>param\\_name</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>The parameter to change configuration for</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>param\\_value</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>The value that should be set for the parameter given</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>resource\\_email</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>The email address of the resource that is being modified</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Set-O365CalendarProcessing
### Synopsis
Change the calendar processing configuration for an Office 365 calendar
### Syntax
```
Set-O365CalendarProcessing [-param\\_name] <Object> [-param\\_value] <Object> [-resource\\_email] <Object>
[<CommonParameters>]
```
### Set-O365CalendarProcessing Aliases
 - setCalendarProcessing

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>param\\_name</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Value that will be set for the parameter supplied</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>param\\_value</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Case-sensitive name of the parameter to set or change; use getCalendarProcessing with include\\_metadata to get
acceptable values with parameter names</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>resource\\_email</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Email address of the resource for which to change calendar processing configuration</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Set-O365Connection
### Synopsis
Sets an existing Office 365 API connection as the current connection or clears the current connection.
### Syntax
```
Set-O365Connection [[-id] <String>] [<CommonParameters>]
```
### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>id</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>The unique id for the connection. If not specified, the current connection will be cleared.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- $Global:O365Session: Session information for the API.
- $Global:O365CurrentConnection: Connection information for the selected connection.
## Set-O365Forward
### Synopsis
Set the forwarding address on a Service Account
### Syntax
```
Set-O365Forward [[-forward] <Object>] [-msoluid] <Object> [<CommonParameters>]
```
### Set-O365Forward Aliases
 - setMsolForward

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>forward</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>[Optional] If this parameter is included, the forward will be set to the given address.  Absence of forward will
remove any existing forward on the account.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the account for which to set the forward (e.g. foo\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Set-O365GALStatus
### Synopsis
Changes the Office 365 Global Address List (GAL) searchable status for a Service Account
### Syntax
```
Set-O365GALStatus [-msoluid] <Object> [-status] <Object> [<CommonParameters>]
```
### Set-O365GALStatus Aliases
 - setO365GALStatus

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the account for GAL status is being changed (e.g. foo\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>status</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>show|hide</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Set-O365MailboxPermission
### Synopsis
Add or remove mailbox permissions on an Office 365 account; Full, Send As, or Send on Behalf
### Syntax
```
Set-O365MailboxPermission [-delegate\\_account] <Object> [-permission] <Object> [-set\\_type] <Object> [-target\\_account]
<Object> [<CommonParameters>]
```
### Set-O365MailboxPermission Aliases
 - setMsolMailboxPermission

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>delegate\\_account</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique identifier of the account that is having permissions granted or revoked</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>permission</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>full|sendas|sendonbehalf</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>set\\_type</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>add|remove</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>target\\_account</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique identifier of the account to which the delegate account is gaining or losing permissions</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: ID of the PowerShell job that was queued to change the permission
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Set-O365MailboxPolicy
### Synopsis
Update the mailbox policy for an Office 365 account; used to restrict forwarding for example
### Syntax
```
Set-O365MailboxPolicy [-msoluid] <Object> [-policy] <Object> [<CommonParameters>]
```
### Set-O365MailboxPolicy Aliases
 - setMsolMailboxPolicy

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the account (e.g. foo\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>policy</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Identifier of the policy to apply to the account (e.g. default or no\\_forward)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Set-O365MailPrimaryAddress
### Synopsis
DEPRECATED; use setMsolPrimaryAddress - Set the primary email address on a Service Account
### Syntax
```
Set-O365MailPrimaryAddress [-msoluid] <Object> [-primary\\_address] <Object> [<CommonParameters>]
```
### Set-O365MailPrimaryAddress Aliases
 - setMailPrimaryAddress

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the account for which to set the primary address (e.g. foo\\_bar)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>primary\\_address</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Email address that should be set as the primary address on the account; must be a valid email address already assigned
to the account (e.g. foo@bar.wisc.edu)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Set-O365PrimaryAddress
### Synopsis
Set the primary email address on a NetID or Service Account
### Syntax
```
Set-O365PrimaryAddress [-msoluid] <Object> [-primary\\_address] <Object> [<CommonParameters>]
```
### Set-O365PrimaryAddress Aliases
 - setMsolPrimaryAddress

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the account</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>primary\\_address</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Email address that should be set as the primary address on the account; must be a valid email address already assigned
to the account (e.g. foo@bar.wisc.edu)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Set-O365ResourceFullAccess
### Synopsis
Add or remove full access to an Office 365 resource.
### Syntax
```
Set-O365ResourceFullAccess [-delegate\\_account] <Object> [-resource\\_msoluid] <Object> [-set\\_type] <Object>
[<CommonParameters>]
```
### Set-O365ResourceFullAccess Aliases
 - setMsolResourceFullAccess

### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>delegate\\_account</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Account to receive or remove access from the resource</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>resource\\_msoluid</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Unique ID of the resource (e.g. room\\_1234\\_foo)</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>set\\_type</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Defines whether permission is being added or removed, must be add or reomve</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Outputs
- failure: null
- success: 1
### Links

 - [System.Collections.Hashtable.name](System.Collections.Hashtable.link)
## Set-O365StartupPreferences
### Synopsis
Sets the preference to determine if the startup menu will be shown when importing the module.
### Syntax
```
Set-O365StartupPreferences [[-showStartupMenu]] [<CommonParameters>]
```
### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>showStartupMenu</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Determines if the startup menu will be shown</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">False</td>
		</tr>
	</tbody>
</table>

### Outputs
- Startup.txt
## Update-O365APIFunctions
### Synopsis
Updates the API functions and documentation in the module by getting the methods from the Domain Admin API Documentation.
### Syntax
```
Update-O365APIFunctions [-includeAlias] [<CommonParameters>]
```
### Parameters
<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>includeAlias</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Includes the original API method name as an alias.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">False</td>
		</tr>
	</tbody>
</table>

### Outputs
- If no new updates: No Updates | No new API Functions were found.
- If new updates: Updates | New API Functions were found and added.
- APIFunctions.ps1
- WiscO365 Help.html
