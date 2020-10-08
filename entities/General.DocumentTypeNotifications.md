---
uid: General.DocumentTypeNotifications
---
# General.DocumentTypeNotifications

Provides notification addresses to be notified upon occurrence of different document events. Entity: Gen_Document_Type_Notifications

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.DocumentTypeNotifications.md#Id) | guid |  
| [DocumentEvent](General.DocumentTypeNotifications.md#DocumentEvent) | string | The event which will trigger the notification. [Required] [Default("StateChanging")] [Filter(eq)] 
| [FilterXML](General.DocumentTypeNotifications.md#FilterXML) | string (nullable) | Filtering condition for the document. Only documents which match the filter will trigger the event. 
| [StateBitMask](General.DocumentTypeNotifications.md#StateBitMask) | int32 | The document states that will trigger the event. [Required] [Default(0)] 
| [StatusChangeDirection](General.DocumentTypeNotifications.md#StatusChangeDirection) | [General.DocumentTypeNotificationsRepository.StatusChangeDirection](General.DocumentTypeNotifications.md#StatusChangeDirection) | Direction of status change. Positive when the new status is greater than the previous. Applicable values: Positive '+', Negative '-', No change '0', Any change '*'. [Required] [Default("*")] 
| [ToEmailAddressList](General.DocumentTypeNotifications.md#ToEmailAddressList) | string | List of email addressess to be notified. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentType](General.DocumentTypeNotifications.md#DocumentType) | [General.DocumentTypes](General.DocumentTypes.md) | The document type for which this notification is set. [Required] [Filter(multi eq)] [Owner] |
| [UserStatus](General.DocumentTypeNotifications.md#UserStatus) | [General.DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable) | When not null, specifies that the event will be triggered only on this user status. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### DocumentEvent

> The event which will trigger the notification. [Required] [Default("StateChanging")] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **StateChanging**  

### FilterXML

> Filtering condition for the document. Only documents which match the filter will trigger the event.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### StateBitMask

> The document states that will trigger the event. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### StatusChangeDirection

> Direction of status change. Positive when the new status is greater than the previous. Applicable values: Positive '+', Negative '-', No change '0', Any change '*'. [Required] [Default("*")]

_Type_: **[General.DocumentTypeNotificationsRepository.StatusChangeDirection](General.DocumentTypeNotifications.md#StatusChangeDirection)**  
Allowed values for the [StatusChangeDirection](General.DocumentTypeNotifications.md#StatusChangeDirection) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| AnyChange | AnyChange value. Stored as '*'. <br /> _Database Value:_ '*' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'AnyChange' |
| NoChange | NoChange value. Stored as '0'. <br /> _Database Value:_ '0' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'NoChange' |
| PositiveChange | PositiveChange value. Stored as '+'. <br /> _Database Value:_ '+' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'PositiveChange' |
| NegativeChange | NegativeChange value. Stored as '-'. <br /> _Database Value:_ '-' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'NegativeChange' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **AnyChange**  

### ToEmailAddressList

> List of email addressess to be notified. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### DocumentType

> The document type for which this notification is set. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### UserStatus

> When not null, specifies that the event will be triggered only on this user status. [Filter(multi eq)]

_Type_: **[General.DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.DocumentTypeNotifications erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.DocumentTypeNotifications erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.DocumentTypeNotifications erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentTypeNotifications?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentTypeNotifications?$top=10>

