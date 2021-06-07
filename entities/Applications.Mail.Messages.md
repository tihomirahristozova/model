---
uid: Applications.Mail.Messages
---
# Applications.Mail.Messages Entity

**Namespace:** [Applications.Mail](Applications.Mail.md)  

Represents email messages. Entity: Mail_Messages

## Default Visualization
Default Display Text Format:  
_{MailBoxFolder.FolderName:T}_  
Default Search Member:  
_MailBoxFolder.FolderName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.Mail.BoxFolders](Applications.Mail.BoxFolders.md)  
Aggregate Root:  
[Applications.Mail.Boxes](Applications.Mail.Boxes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Body](Applications.Mail.Messages.md#body) | string (max) __nullable__ | The body of the message. 
| [CcEmailAddressList](Applications.Mail.Messages.md#ccemailaddresslist) | string (2048) __nullable__ | Semicolon-separated list of Cc email addresses. `Filter(like)` 
| [CreationDateTime](Applications.Mail.Messages.md#creationdatetime) | datetime | Date and time when the message was created. `Required` `Default(Now)` `Filter(ge;le)` 
| [FromEmailAddress](Applications.Mail.Messages.md#fromemailaddress) | string (512) | Sending email address. `Required` `Filter(like)` 
| [Id](Applications.Mail.Messages.md#id) | guid |  
| [IsEncrypted](Applications.Mail.Messages.md#isencrypted) | boolean | True when the message is stored in encrypted format. `Required` `Default(false)` `Filter(eq)` 
| [IsRead](Applications.Mail.Messages.md#isread) | boolean | True when the message was read by the user. `Required` `Default(false)` `Filter(eq)` 
| [ReceivedDateTime](Applications.Mail.Messages.md#receiveddatetime) | datetime __nullable__ | Date and time when the message was received. `Filter(ge;le)` 
| [SentDateTime](Applications.Mail.Messages.md#sentdatetime) | datetime __nullable__ | Date and time when the message was sent. `Filter(ge;le)` 
| [ServerMessageID](Applications.Mail.Messages.md#servermessageid) | string (256) __nullable__ | Message ID as it appears on the mail server. `Filter(eq)` `ORD` 
| [Subject](Applications.Mail.Messages.md#subject) | string (1024) __nullable__ | The message subject. `Filter(like)` 
| [ToEmailAddressList](Applications.Mail.Messages.md#toemailaddresslist) | string (2048) __nullable__ | Semicolon-separated list of receiving email addresses. `Filter(like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [MailBoxFolder](Applications.Mail.Messages.md#mailboxfolder) | [BoxFolders](Applications.Mail.BoxFolders.md) | The `BoxFolder`(Applications.Mail.BoxFolders.md) to which this Message belongs. `Required` `Filter(multi eq)` `Owner` |
| [RelatedToParty](Applications.Mail.Messages.md#relatedtoparty) | [Parties](General.Contacts.Parties.md) (nullable) | The party id of the external participating (sender/receiver) party (customer, supplier, etc.) in this mail. null means that the email is still not related to any specific party. `Filter(multi eq)` |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Attachments | [MessageAttachments](Applications.Mail.MessageAttachments.md) | List of `MessageAttachment`(Applications.Mail.MessageAttachments.md) child objects, based on the `Applications.Mail.MessageAttachment.MailMessage`(Applications.Mail.MessageAttachments.md#mailmessage) back reference 


## Attribute Details

### Body

The body of the message.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### CcEmailAddressList

Semicolon-separated list of Cc email addresses. `Filter(like)`

_Type_: **string (2048) __nullable__**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **2048**  

### CreationDateTime

Date and time when the message was created. `Required` `Default(Now)` `Filter(ge;le)`

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### FromEmailAddress

Sending email address. `Required` `Filter(like)`

_Type_: **string (512)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **512**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsEncrypted

True when the message is stored in encrypted format. `Required` `Default(false)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### IsRead

True when the message was read by the user. `Required` `Default(false)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ReceivedDateTime

Date and time when the message was received. `Filter(ge;le)`

_Type_: **datetime __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### SentDateTime

Date and time when the message was sent. `Filter(ge;le)`

_Type_: **datetime __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ServerMessageID

Message ID as it appears on the mail server. `Filter(eq)` `ORD`

_Type_: **string (256) __nullable__**  
_Indexed_: **True**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  
_Maximum Length_: **256**  

### Subject

The message subject. `Filter(like)`

_Type_: **string (1024) __nullable__**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **1024**  

### ToEmailAddressList

Semicolon-separated list of receiving email addresses. `Filter(like)`

_Type_: **string (2048) __nullable__**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **2048**  


## Reference Details

### MailBoxFolder

The `BoxFolder`(Applications.Mail.BoxFolders.md) to which this Message belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[BoxFolders](Applications.Mail.BoxFolders.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### RelatedToParty

The party id of the external participating (sender/receiver) party (customer, supplier, etc.) in this mail. null means that the email is still not related to any specific party. `Filter(multi eq)`

_Type_: **[Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.Mail.Messages erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Mail.Messages erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Mail_Messages?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Mail_Messages?$top=10>

