# Applications.Mail.Boxes

Represents user mailboxes. Entity: Mail_Boxes

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Mail.Boxes.md#Id) | guid |  
| [Active](Applications.Mail.Boxes.md#Active) | boolean | True when the mail box is active for mail sinchronization, sending and receiving. [Required] [Default(true)] [Filter(eq)] 
| [EmailAddress](Applications.Mail.Boxes.md#EmailAddress) | string | The email address associated with this mail box. [Required] [Filter(eq)] 
| [IsDefault](Applications.Mail.Boxes.md#IsDefault) | boolean | True when this is the default mailbox for the user. [Required] [Default(true)] [Filter(eq)] 
| [IsEncrypted](Applications.Mail.Boxes.md#IsEncrypted) | boolean | True when the mailbox messages are stored in encrypted format. [Required] [Default(false)] [Filter(eq)] 
| [ResetOnNextSync](Applications.Mail.Boxes.md#ResetOnNextSync) | boolean | Reset is pending: true = next sync should delete and retrieve again all messages; false = no pending reset. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [SendServerAddress](Applications.Mail.Boxes.md#SendServerAddress) | string (nullable) | The address of the server to use for sending mail. The same credentials as the sync server are used. When null, the mail will be sent using the default server, which is setup at the application server. 
| [SentItemsFolderName](Applications.Mail.Boxes.md#SentItemsFolderName) | string (nullable) | The name of the SentItems folder. It is left empty, EnterpriseOne won't save the sent mail in any folder (but it is still possible that the actual mail server would nevertheless save the mail in a sent items folder, independently from EnterpriseOne). 
| [SignatureHtml](Applications.Mail.Boxes.md#SignatureHtml) | string (nullable) | Html text of the default signature, when creating new emails from this mailbox. When is null, a default generic signature is attached. 
| [SyncPassword](Applications.Mail.Boxes.md#SyncPassword) | string (nullable) | The password to supply to the server when retrieving email. null when the connection is not setup or the server does not require user name. 
| [SyncProtocol](Applications.Mail.Boxes.md#SyncProtocol) | [Applications.Mail.BoxesRepository.SyncProtocol](Applications.Mail.Boxes.md#SyncProtocol) (nullable) | Synchronization protocol, 'POP3' or 'IMAP'. null means that syncrhonization is not setup. 
| [SyncServerAddress](Applications.Mail.Boxes.md#SyncServerAddress) | string (nullable) | Incoming and outgoing mail server internet address. null when synchronization is not setup. 
| [SyncUserName](Applications.Mail.Boxes.md#SyncUserName) | string (nullable) | User name to supply to the server, when retrieving email. null when the connection is not setup or the server does not require user name. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [OwnerUser](Applications.Mail.Boxes.md#OwnerUser) | [Systems.Security.Users](Systems.Security.Users.md) | The user, who owns the mailbox. [Required] [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Folders | [Applications.Mail.BoxFolders](Applications.Mail.BoxFolders.md) | List of [BoxFolder](Applications.Mail.BoxFolders.md) child objects, based on the [Applications.Mail.BoxFolder.MailBox](Applications.Mail.BoxFolders.md#MailBox) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Active

> True when the mail box is active for mail sinchronization, sending and receiving. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### EmailAddress

> The email address associated with this mail box. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### IsDefault

> True when this is the default mailbox for the user. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### IsEncrypted

> True when the mailbox messages are stored in encrypted format. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ResetOnNextSync

> Reset is pending: true = next sync should delete and retrieve again all messages; false = no pending reset. [Required] [Default(false)] [Filter(eq)] [ReadOnly]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### SendServerAddress

> The address of the server to use for sending mail. The same credentials as the sync server are used. When null, the mail will be sent using the default server, which is setup at the application server.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### SentItemsFolderName

> The name of the SentItems folder. It is left empty, EnterpriseOne won't save the sent mail in any folder (but it is still possible that the actual mail server would nevertheless save the mail in a sent items folder, independently from EnterpriseOne).

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### SignatureHtml

> Html text of the default signature, when creating new emails from this mailbox. When is null, a default generic signature is attached.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### SyncPassword

> The password to supply to the server when retrieving email. null when the connection is not setup or the server does not require user name.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### SyncProtocol

> Synchronization protocol, 'POP3' or 'IMAP'. null means that syncrhonization is not setup.

_Type_: **[Applications.Mail.BoxesRepository.SyncProtocol](Applications.Mail.Boxes.md#SyncProtocol) (nullable)**  
Allowed values for the [SyncProtocol](Applications.Mail.Boxes.md#SyncProtocol) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Recommended | Recommended value. Stored as 'IMAP'. <br /> _Database Value:_ 'IMAP' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Recommended' |
| POP3 | POP3 value. Stored as 'POP3'. <br /> _Database Value:_ 'POP3' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'POP3' |
| MicrosoftExchange | MicrosoftExchange value. Stored as 'MEWS'. <br /> _Database Value:_ 'MEWS' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'MicrosoftExchange' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### SyncServerAddress

> Incoming and outgoing mail server internet address. null when synchronization is not setup.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### SyncUserName

> User name to supply to the server, when retrieving email. null when the connection is not setup or the server does not require user name.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### OwnerUser

> The user, who owns the mailbox. [Required] [Filter(multi eq)]

_Type_: **[Systems.Security.Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Mail.Boxes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Mail.Boxes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Mail.Boxes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Mail_Boxes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Mail_Boxes?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Mail_Boxes?$top=10>

