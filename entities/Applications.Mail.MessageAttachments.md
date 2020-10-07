# Applications.Mail.MessageAttachments

Represents attachments to mail messages. Entity: Mail_Message_Attachments

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Mail.MessageAttachments.md#Id) | guid |  
| [AttachmentContent](Applications.Mail.MessageAttachments.md#AttachmentContent) | byte[] (nullable) | The actual content of the attachment. null when the content is not downloaded or is unknown for some other reason. 
| [ContentDescriptors](Applications.Mail.MessageAttachments.md#ContentDescriptors) | string (nullable) | Content flags, like "Content-Type: text/plain; charset=utf-8". 
| [ContentDownloaded](Applications.Mail.MessageAttachments.md#ContentDownloaded) | boolean | True when the content is included, false when this is only an empty container. Content should be included when sending mail. [Required] [Default(false)] [Filter(eq)] 
| [Name](Applications.Mail.MessageAttachments.md#Name) | string (nullable) | The name of this MessageAttachment. [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [MailMessage](Applications.Mail.MessageAttachments.md#MailMessage) | [Applications.Mail.Messages](Applications.Mail.Messages.md) | The [Message](Applications.Mail.Messages.md) to which this MessageAttachment belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### AttachmentContent

> The actual content of the attachment. null when the content is not downloaded or is unknown for some other reason.

_Type_: **byte[] (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ContentDescriptors

> Content flags, like "Content-Type: text/plain; charset=utf-8".

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ContentDownloaded

> True when the content is included, false when this is only an empty container. Content should be included when sending mail. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Name

> The name of this MessageAttachment. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### MailMessage

> The [Message](Applications.Mail.Messages.md) to which this MessageAttachment belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Applications.Mail.Messages](Applications.Mail.Messages.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Mail.MessageAttachments erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Mail.MessageAttachments erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Mail.MessageAttachments erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Mail_MessageAttachments?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Mail_MessageAttachments?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Mail_Message_Attachments?$top=10>

