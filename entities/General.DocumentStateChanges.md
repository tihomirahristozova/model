---
uid: General.DocumentStateChanges
---
# General.DocumentStateChanges Entity

**Namespace:** [General](General.md)  

History of document state changes. Entity: Gen_Document_State_Changes

## Default Visualization
Default Display Text Format:  
_{Document.DocumentType.Code}:{Document.DocumentNo} - {Document.DocumentType.TypeName:T}_  
Default Search Member:  
_Document.DocumentType.Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Documents](General.Documents.md)  
Aggregate Root:  
[General.Documents](General.Documents.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.DocumentStateChanges.md#id) | guid |  
| [NewState](General.DocumentStateChanges.md#newstate) | [NewState](General.DocumentStateChanges.md#newstate) | The new state after the change. [Required] [Filter(eq)] 
| [SystemInitiated](General.DocumentStateChanges.md#systeminitiated) | boolean | Specifies whether the state change was caused by system process or from user action. [Required] [Default(false)] [ReadOnly] 
| [UpdateTime](General.DocumentStateChanges.md#updatetime) | datetime | The time when the change took effect. [Required] [Filter(ge;le)] [ORD] 
| [UpdateUser](General.DocumentStateChanges.md#updateuser) | string | The login name of the user, who made the status change. [Required] [Filter(eq)] 
| [Void](General.DocumentStateChanges.md#void) | boolean | True if the document is voided with this change. [Required] [Default(false)] [Filter(eq)] [Introduced in version 19.1] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](General.DocumentStateChanges.md#document) | [Documents](General.Documents.md) | The document which has changed state. [Required] [Filter(multi eq)] [Owner] |
| [UserStatus](General.DocumentStateChanges.md#userstatus) | [DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable) | The new user status after the change. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### NewState

The new state after the change. [Required] [Filter(eq)]

_Type_: **[NewState](General.DocumentStateChanges.md#newstate)**  
Allowed values for the [NewState](General.DocumentStateChanges.md#newstate) data attribute  
_Allowed Values (General.DocumentStateChangesRepository.NewState Enum Members)_  

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

Specifies whether the state change was caused by system process or from user action. [Required] [Default(false)] [ReadOnly]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### UpdateTime

The time when the change took effect. [Required] [Filter(ge;le)] [ORD]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **True**  

### UpdateUser

The login name of the user, who made the status change. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### Void

True if the document is voided with this change. [Required] [Default(false)] [Filter(eq)] [Introduced in version 19.1]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  


## Reference Details

### Document

The document which has changed state. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Documents](General.Documents.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### UserStatus

The new user status after the change. [Filter(multi eq)]

_Type_: **[DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.DocumentStateChanges erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.DocumentStateChanges erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentStateChanges?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentStateChanges?$top=10>

