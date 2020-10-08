---
uid: Applications.Mail.Messages
---
# Applications.Mail.Messages

Represents email messages. Entity: Mail_Messages

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Body](Applications.Mail.Messages.md#body) | string (nullable) | The body of the message. 
| [CcEmailAddressList](Applications.Mail.Messages.md#ccemailaddresslist) | string (nullable) | Semicolon-separated list of Cc email addresses. [Filter(like)] 
| [CreationDateTime](Applications.Mail.Messages.md#creationdatetime) | datetime | Date and time when the message was created. [Required] [Default(Now)] [Filter(ge;le)] 
| [FromEmailAddress](Applications.Mail.Messages.md#fromemailaddress) | string | Sending email address. [Required] [Filter(like)] 
| [Id](Applications.Mail.Messages.md#id) | guid |  
| [IsEncrypted](Applications.Mail.Messages.md#isencrypted) | boolean | True when the message is stored in encrypted format. [Required] [Default(false)] [Filter(eq)] 
| [IsRead](Applications.Mail.Messages.md#isread) | boolean | True when the message was read by the user. [Required] [Default(false)] [Filter(eq)] 
| [ReceivedDateTime](Applications.Mail.Messages.md#receiveddatetime) | datetime (nullable) | Date and time when the message was received. [Filter(ge;le)] 
| [SentDateTime](Applications.Mail.Messages.md#sentdatetime) | datetime (nullable) | Date and time when the message was sent. [Filter(ge;le)] 
| [ServerMessageID](Applications.Mail.Messages.md#servermessageid) | string (nullable) | Message ID as it appears on the mail server. [Filter(eq)] 
| [Subject](Applications.Mail.Messages.md#subject) | string (nullable) | The message subject. [Filter(like)] 
| [ToEmailAddressList](Applications.Mail.Messages.md#toemailaddresslist) | string (nullable) | Semicolon-separated list of receiving email addresses. [Filter(like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [MailBoxFolder](Applications.Mail.Messages.md#mailboxfolder) | [Applications.Mail.BoxFolders](Applications.Mail.BoxFolders.md) | The [BoxFolder](Applications.Mail.BoxFolders.md) to which this Message belongs. [Required] [Filter(multi eq)] [Owner] |
| [RelatedToParty](Applications.Mail.Messages.md#relatedtoparty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | The party id of the external participating (sender/receiver) party (customer, supplier, etc.) in this mail. null means that the email is still not related to any specific party. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Attachments | [Applications.Mail.MessageAttachments](Applications.Mail.MessageAttachments.md) | List of [MessageAttachment](Applications.Mail.MessageAttachments.md) child objects, based on the [Applications.Mail.MessageAttachment.MailMessage](Applications.Mail.MessageAttachments.md#mailmessage) back reference 


## Attribute Details

### Body

> The body of the message.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### CcEmailAddressList

> Semicolon-separated list of Cc email addresses. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### CreationDateTime

> Date and time when the message was created. [Required] [Default(Now)] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### FromEmailAddress

> Sending email address. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsEncrypted

> True when the message is stored in encrypted format. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### IsRead

> True when the message was read by the user. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ReceivedDateTime

> Date and time when the message was received. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### SentDateTime

> Date and time when the message was sent. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ServerMessageID

> Message ID as it appears on the mail server. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### Subject

> The message subject. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### ToEmailAddressList

> Semicolon-separated list of receiving email addresses. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### MailBoxFolder

> The [BoxFolder](Applications.Mail.BoxFolders.md) to which this Message belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Applications.Mail.BoxFolders](Applications.Mail.BoxFolders.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### RelatedToParty

> The party id of the external participating (sender/receiver) party (customer, supplier, etc.) in this mail. null means that the email is still not related to any specific party. [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.Mail.Messages erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Mail.Messages erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Mail.Messages erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Mail_Messages?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Mail_Messages?$top=10>

