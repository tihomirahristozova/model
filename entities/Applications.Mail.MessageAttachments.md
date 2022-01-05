---
uid: Applications.Mail.MessageAttachments
---
# Applications.Mail.MessageAttachments Entity

**Namespace:** [Applications.Mail](Applications.Mail.md)  

Represents attachments to mail messages. Entity: Mail_Message_Attachments

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.Mail.Messages](Applications.Mail.Messages.md)  
Aggregate Root:  
[Applications.Mail.Boxes](Applications.Mail.Boxes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AttachmentContent](Applications.Mail.MessageAttachments.md#attachmentcontent) | byte[] __nullable__ | The actual content of the attachment. null when the content is not downloaded or is unknown for some other reason. 
| [ContentDescriptors](Applications.Mail.MessageAttachments.md#contentdescriptors) | string (4000) __nullable__ | Content flags, like "Content-Type: text/plain; charset=utf-8". 
| [ContentDownloaded](Applications.Mail.MessageAttachments.md#contentdownloaded) | boolean | True when the content is included, false when this is only an empty container. Content should be included when sending mail. `Required` `Default(false)` `Filter(eq)` 
| [Id](Applications.Mail.MessageAttachments.md#id) | guid |  
| [Name](Applications.Mail.MessageAttachments.md#name) | string (128) __nullable__ | The name of this MessageAttachment. `Filter(eq;like)` 
| [ObjectVersion](Applications.Mail.MessageAttachments.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [MailMessage](Applications.Mail.MessageAttachments.md#mailmessage) | [Messages](Applications.Mail.Messages.md) | The <see cref="Message"/> to which this MessageAttachment belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### AttachmentContent

The actual content of the attachment. null when the content is not downloaded or is unknown for some other reason.

_Type_: **byte[] __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ContentDescriptors

Content flags, like "Content-Type: text/plain; charset=utf-8".

_Type_: **string (4000) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **4000**  

### ContentDownloaded

True when the content is included, false when this is only an empty container. Content should be included when sending mail. `Required` `Default(false)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this MessageAttachment. `Filter(eq;like)`

_Type_: **string (128) __nullable__**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **128**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### MailMessage

The <see cref="Message"/> to which this MessageAttachment belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Messages](Applications.Mail.Messages.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  


## API Methods

Methods that can be invoked in public APIs.

### GetAllowedCustomPropertyValues

Gets the allowed values for the specified custom property for this entity object.              If supported the result is ordered by property value. Some property value sources does not support ordering.  
_Return Type_: **Collection Of [CustomPropertyValue](../data-types.md#general.custompropertyvalue)**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **GET**  

**Parameters**  
  * **customPropertyCode**  
    The code of the custom property  
    _Type_: string  

  * **search**  
    The search text - searches by value or description  
    _Type_: string  
     _Optional_: True  
    _Default Value_: null  

  * **exactMatch**  
    If true the search text should be equal to the property value  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **orderByDescription**  
    If true the result is ordered by Description instead of Value. Note that ordering is not always possible.  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **top**  
    The top clause - default is 10  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 10  

  * **skip**  
    The skip clause - default is 0  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 0  



## Business Rules

[!list limit=1000 erp.entity=Applications.Mail.MessageAttachments erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.Mail.MessageAttachments erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Mail_MessageAttachments?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Mail_MessageAttachments?$top=10>

