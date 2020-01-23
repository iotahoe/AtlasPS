---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: AtlasPS
online version: https://docs.iotahoe.org/AtlasPS/new-atlascontext
schema: 2.0.0
---

# New-AtlasContext

## SYNOPSIS
Creates an APache Atlas access context.

## SYNTAX

### OAuthAccount (Default)
```
New-AtlasContext [-Endpoint] <String> [-UseConnectedAccount] [-Protocol <String>]
  [<CommonParameters>]
```

### Credential
```
New-AtlasContext [-Endpoint] <String> [-Credential] <PsCredential> [-Protocol <String>]
  [<CommonParameters>]
```

### AnonymousAccount
```
New-AtlasContext [-Endpoint] <String> [-Anonymous] [-Protocol <String>] 
 [<CommonParameters>]
```

### ConnectionString
```
New-AtlasContext -ConnectionString <String> [<CommonParameters>]
```


## DESCRIPTION
The **New-AtlasContext** cmdlet creates an Apache Atlas context.
The default Authentication of a Apache Context is OAuth (Azure AD), if only input Atlas instance name.
See details of authentication of the Storage Service in https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services.

## EXAMPLES

### Example 1: Create a context by specifying a Atlas instance name and credential
```
PS C:\>New-AtlasContext -StorageAccountName "ContosoGeneral" -Credential $MyCredential
```

This command creates a context for the account named ContosoGeneral that uses the specified key.

### Example 2: Create a context by specifying a connection string
```
PS C:\>New-AtlasContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

This command creates a context based on the specified connection string for the account ContosoGeneral.

### Example 3: Create a context for an anonymous Atlas instance
```
PS C:\>New-AtlasContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

This command creates a context for anonymous use for the account named ContosoGeneral.
The command specifies HTTP as a connection protocol.

### Example 5: Get the container for the local developer Atlas instance
```
PS C:\>New-AtlasContext -Local | Get-AtlasContainer
```

This command creates a context by using the local development Atlas instance, and then passes the new context to the **Get-AtlasContainer** cmdlet by using the pipeline operator.
The command gets the Apache Atlas container for the local developer Atlas instance.

### Example 6: Get multiple containers
```
PS C:\>$Context01 = New-AtlasContext -Local 
PS C:\> $Context02 = New-AtlasContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AtlasContainer
```

The first command creates a context by using the local development Atlas instance, and then stores that context in the $Context01 variable.
The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.
The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AtlasContainer**.

### Example 7: Create a context with an endpoint
```
PS C:\>New-AtlasContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

This command creates an Apache Atlas context that has the specified storage endpoint.
The command creates the context for the account named ContosoGeneral that uses the specified key.


### Example 10: Create a context by using the OAuth Authentication
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AtlasContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

This command creates a context by using the OAuth (Azure AD) Authentication.

## PARAMETERS

### -Anonymous
Indicates that this cmdlet creates an Apache Atlas context for anonymous logon.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionString
Specifies a connection string for the Apache Atlas context.

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Endpoint
Specifies the endpoint for the Apache Atlas context.

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
Specfy the transfer protocol: Options are 'http' or 'https'.
If -Protocol is omitted, then https is assumed.

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, OAuthAccountEnvironment
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SasToken
Specifies a Shared Access Signature (SAS) token for the context.

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountKey
Specifies an Apache Atlas account key.
This cmdlet creates a context for the key that this parameter specifies.

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseConnectedAccount
Indicates that this cmdlet creates an Apache Atlas context with OAuth (Azure AD) Authentication.
The cmdlet will use OAuth Authentication by default, when other authentication not specified.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable,
-InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable,
-Verbose, -WarningAction, and -WarningVariable.
For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## OUTPUTS

### Atlas.AtlasStorageContext

## NOTES

## RELATED LINKS



