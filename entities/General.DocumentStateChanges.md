---
uid: General.DocumentStateChanges
---
# General.DocumentStateChanges

History of document state changes. Entity: Gen_Document_State_Changes

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.DocumentStateChanges.md#Id) | guid |  
| [NewState](General.DocumentStateChanges.md#NewState) | [General.DocumentStateChangesRepository.NewState](General.DocumentStateChanges.md#NewState) | The new state after the change. [Required] [Filter(eq)] 
| [SystemInitiated](General.DocumentStateChanges.md#SystemInitiated) | boolean | Specifies whether the state change was caused by system process or from user action. [Required] [Default(false)] [ReadOnly] 
| [UpdateTime](General.DocumentStateChanges.md#UpdateTime) | datetime | The time when the change took effect. [Required] [Filter(ge;le)] [ORD] 
| [UpdateUser](General.DocumentStateChanges.md#UpdateUser) | string | The login name of the user, who made the status change. [Required] [Filter(eq)] 
| [Void](General.DocumentStateChanges.md#Void) | boolean | True if the document is voided with this change. [Required] [Default(false)] [Filter(eq)] (Introduced in version 19.1.100.0) 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](General.DocumentStateChanges.md#Document) | [General.Documents](General.Documents.md) | The document which has changed state. [Required] [Filter(multi eq)] [Owner] |
| [UserStatus](General.DocumentStateChanges.md#UserStatus) | [General.DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable) | The new user status after the change. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### NewState

> The new state after the change. [Required] [Filter(eq)]

_Type_: **[General.DocumentStateChangesRepository.NewState](General.DocumentStateChanges.md#NewState)**  
Allowed values for the [NewState](General.DocumentStateChanges.md#NewState) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| New | New value. Stored as 0. <br /> _Database Value:_ 0 <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'New' |
| Corrective | Corrective value. Stored as 5. <br /> _Database Value:_ 5 <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Corrective' |
| Planned | Planned value. Stored as 10. <br /> _Database Value:_ 10 <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'Planned' |
| FirmPlanned | FirmPlanned value. Stored as 20. <br /> _Database Value:_ 20 <br /> _Model Value:_ 20 <br /> _Domain API Value:_ 'FirmPlanned' |
| Released | Released value. Stored as 30. <br /> _Database Value:_ 30 <br /> _Model Value:_ 30 <br /> _Domain API Value:_ 'Released' |
| Completed | Completed value. Stored as 40. <br /> _Database Value:_ 40 <br /> _Model Value:_ 40 <br /> _Domain API Value:_ 'Completed' |
| Closed | Closed value. Stored as 50. <br /> _Database Value:_ 50 <br /> _Model Value:_ 50 <br /> _Domain API Value:_ 'Closed' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### SystemInitiated

> Specifies whether the state change was caused by system process or from user action. [Required] [Default(false)] [ReadOnly]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### UpdateTime

> The time when the change took effect. [Required] [Filter(ge;le)] [ORD]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **True**  

### UpdateUser

> The login name of the user, who made the status change. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### Void

> True if the document is voided with this change. [Required] [Default(false)] [Filter(eq)] (Introduced in version 19.1.100.0)

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  


## Reference Details

### Document

> The document which has changed state. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Documents](General.Documents.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### UserStatus

> The new user status after the change. [Filter(multi eq)]

_Type_: **[General.DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.DocumentStateChanges erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.DocumentStateChanges erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.DocumentStateChanges erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentStateChanges?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentStateChanges?$top=10>

