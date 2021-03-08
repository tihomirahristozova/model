---
uid: Applications.Mail.Boxes
---
# Applications.Mail.Boxes Entity

**Namespace:** [Applications.Mail](Applications.Mail.md)  

Represents user mailboxes. Entity: Mail_Boxes

## Default Visualization
Default Display Text Format:  
_{SentItemsFolderName:T}_  
Default Search Member:  
_SentItemsFolderName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Applications.Mail.Boxes](Applications.Mail.Boxes.md)  
  * [Applications.Mail.BoxFolders](Applications.Mail.BoxFolders.md)  
    * [Applications.Mail.Messages](Applications.Mail.Messages.md)  
      * [Applications.Mail.MessageAttachments](Applications.Mail.MessageAttachments.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Active](Applications.Mail.Boxes.md#active) | boolean | True when the mail box is active for mail sinchronization, sending and receiving. `Required` `Default(true)` `Filter(eq)` 
| [EmailAddress](Applications.Mail.Boxes.md#emailaddress) | string | The email address associated with this mail box. `Required` `Filter(eq)` 
| [Id](Applications.Mail.Boxes.md#id) | guid |  
| [IsDefault](Applications.Mail.Boxes.md#isdefault) | boolean | True when this is the default mailbox for the user. `Required` `Default(true)` `Filter(eq)` 
| [IsEncrypted](Applications.Mail.Boxes.md#isencrypted) | boolean | True when the mailbox messages are stored in encrypted format. `Required` `Default(false)` `Filter(eq)` 
| [ResetOnNextSync](Applications.Mail.Boxes.md#resetonnextsync) | boolean | Reset is pending: true = next sync should delete and retrieve again all messages; false = no pending reset. `Required` `Default(false)` `Filter(eq)` `ReadOnly` 
| [SendServerAddress](Applications.Mail.Boxes.md#sendserveraddress) | string (nullable) | The address of the server to use for sending mail. The same credentials as the sync server are used. When null, the mail will be sent using the default server, which is setup at the application server. 
| [SentItemsFolderName](Applications.Mail.Boxes.md#sentitemsfoldername) | string (nullable) | The name of the SentItems folder. It is left empty, EnterpriseOne won't save the sent mail in any folder (but it is still possible that the actual mail server would nevertheless save the mail in a sent items folder, independently from EnterpriseOne). 
| [SignatureHtml](Applications.Mail.Boxes.md#signaturehtml) | string (nullable) | Html text of the default signature, when creating new emails from this mailbox. When is null, a default generic signature is attached. 
| [SyncPassword](Applications.Mail.Boxes.md#syncpassword) | string (nullable) | The password to supply to the server when retrieving email. null when the connection is not setup or the server does not require user name. 
| [SyncProtocol](Applications.Mail.Boxes.md#syncprotocol) | [SyncProtocol](Applications.Mail.Boxes.md#syncprotocol) (nullable) | Synchronization protocol, 'POP3' or 'IMAP'. null means that syncrhonization is not setup. 
| [SyncServerAddress](Applications.Mail.Boxes.md#syncserveraddress) | string (nullable) | Incoming and outgoing mail server internet address. null when synchronization is not setup. 
| [SyncUserName](Applications.Mail.Boxes.md#syncusername) | string (nullable) | User name to supply to the server, when retrieving email. null when the connection is not setup or the server does not require user name. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [OwnerUser](Applications.Mail.Boxes.md#owneruser) | [Users](Systems.Security.Users.md) | The user, who owns the mailbox. `Required` `Filter(multi eq)` |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Folders | [BoxFolders](Applications.Mail.BoxFolders.md) | List of `BoxFolder`(Applications.Mail.BoxFolders.md) child objects, based on the `Applications.Mail.BoxFolder.MailBox`(Applications.Mail.BoxFolders.md#mailbox) back reference 


## Attribute Details

### Active

True when the mail box is active for mail sinchronization, sending and receiving. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### EmailAddress

The email address associated with this mail box. `Required` `Filter(eq)`

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsDefault

True when this is the default mailbox for the user. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### IsEncrypted

True when the mailbox messages are stored in encrypted format. `Required` `Default(false)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ResetOnNextSync

Reset is pending: true = next sync should delete and retrieve again all messages; false = no pending reset. `Required` `Default(false)` `Filter(eq)` `ReadOnly`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### SendServerAddress

The address of the server to use for sending mail. The same credentials as the sync server are used. When null, the mail will be sent using the default server, which is setup at the application server.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### SentItemsFolderName

The name of the SentItems folder. It is left empty, EnterpriseOne won't save the sent mail in any folder (but it is still possible that the actual mail server would nevertheless save the mail in a sent items folder, independently from EnterpriseOne).

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### SignatureHtml

Html text of the default signature, when creating new emails from this mailbox. When is null, a default generic signature is attached.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### SyncPassword

The password to supply to the server when retrieving email. null when the connection is not setup or the server does not require user name.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### SyncProtocol

Synchronization protocol, 'POP3' or 'IMAP'. null means that syncrhonization is not setup.

_Type_: **[SyncProtocol](Applications.Mail.Boxes.md#syncprotocol) (nullable)**  
Allowed values for the `SyncProtocol`(Applications.Mail.Boxes.md#syncprotocol) data attribute  
_Allowed Values (Applications.Mail.BoxesRepository.SyncProtocol Enum Members)_  

| Value | Description |
| ---- | --- |
| Recommended | Recommended value. Stored as 'IMAP'. <br /> _Database Value:_ 'IMAP' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Recommended' |
| POP3 | POP3 value. Stored as 'POP3'. <br /> _Database Value:_ 'POP3' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'POP3' |
| MicrosoftExchange | MicrosoftExchange value. Stored as 'MEWS'. <br /> _Database Value:_ 'MEWS' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'MicrosoftExchange' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### SyncServerAddress

Incoming and outgoing mail server internet address. null when synchronization is not setup.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### SyncUserName

User name to supply to the server, when retrieving email. null when the connection is not setup or the server does not require user name.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### OwnerUser

The user, who owns the mailbox. `Required` `Filter(multi eq)`

_Type_: **[Users](Systems.Security.Users.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.Mail.Boxes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Mail.Boxes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Mail_Boxes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Mail_Boxes?$top=10>

