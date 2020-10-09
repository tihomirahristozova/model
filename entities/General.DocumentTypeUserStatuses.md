---
uid: General.DocumentTypeUserStatuses
---
# General.DocumentTypeUserStatuses

User-defined document statuses. Entity: Gen_Document_Type_User_Statuses

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Active](General.DocumentTypeUserStatuses.md#active) | boolean | Is the user status active for applying to documents. [Required] [Default(true)] [Filter(eq)] 
| [DisplayOrder](General.DocumentTypeUserStatuses.md#displayorder) | int32 | Consecutive display order of the status, with regard to other statuses within the same document type. [Required] [Filter(ge;le)] 
| [Id](General.DocumentTypeUserStatuses.md#id) | guid |  
| [Instructions](General.DocumentTypeUserStatuses.md#instructions) | string (nullable) | Instructions what should be done when this user status is active (Rich Text). 
| [IsExitStatus](General.DocumentTypeUserStatuses.md#isexitstatus) | boolean | True when the status allows going to the next system status, false otherwise. For example for system status Firm Planned, only user status Approved might allow going to Released. [Required] [Default(true)] [Filter(eq)] 
| [State](General.DocumentTypeUserStatuses.md#state) | [DocumentState](General.DocumentTypeUserStatuses.md#state) | The system state to which this user status is bound. [Required] [Filter(eq)] 
| [UserStatusName](General.DocumentTypeUserStatuses.md#userstatusname) | string | Multi-language name of the user status. [Required] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentType](General.DocumentTypeUserStatuses.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The document type, to which this user status is bound. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Active

> Is the user status active for applying to documents. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### DisplayOrder

> Consecutive display order of the status, with regard to other statuses within the same document type. [Required] [Filter(ge;le)]

_Type_: **int32**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.DocumentType.UserStatuses.Select( c => c.DisplayOrder).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.DocumentType.UserStatuses.Select( c => c.DisplayOrder).DefaultIfEmpty( 0).Max( ) + 10)`
### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Instructions

> Instructions what should be done when this user status is active (Rich Text).

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### IsExitStatus

> True when the status allows going to the next system status, false otherwise. For example for system status Firm Planned, only user status Approved might allow going to Released. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### State

> The system state to which this user status is bound. [Required] [Filter(eq)]

_Type_: **[DocumentState](General.DocumentTypeUserStatuses.md#state)**  
Enumeration of document system states  
_Allowed Values (General.DocumentState Enum Members)_  

| Value | Description |
| ---- | --- |
| New | New document, just created. Can be edited. (Stored as 0). <br /> _Database Value:_ 0 <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'New' |
| Adjustment | Document which adjusts other released documents. (Stored as 5). <br /> _Database Value:_ 5 <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Adjustment' |
| Planned | Planned by the system for future releasing. (Stored as 10). <br /> _Database Value:_ 10 <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'Planned' |
| FirmPlanned | Planned by operator for future releasing. (Stored as 20). <br /> _Database Value:_ 20 <br /> _Model Value:_ 20 <br /> _Domain API Value:_ 'FirmPlanned' |
| Released | Released document. Changes can be applied only through adjustment documents. (Stored as 30). <br /> _Database Value:_ 30 <br /> _Model Value:_ 30 <br /> _Domain API Value:_ 'Released' |
| Completed | Work has completed. (Stored as 40). <br /> _Database Value:_ 40 <br /> _Model Value:_ 40 <br /> _Domain API Value:_ 'Completed' |
| Closed | The document is audited and closed. Adjustments are not allowed, but reopening is allowed. (Stored as 50). <br /> _Database Value:_ 50 <br /> _Model Value:_ 50 <br /> _Domain API Value:_ 'Closed' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### UserStatusName

> Multi-language name of the user status. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### DocumentType

> The document type, to which this user status is bound. [Required] [Filter(multi eq)] [Owner]

_Type_: **[DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.DocumentTypeUserStatuses erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.DocumentTypeUserStatuses erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.DocumentTypeUserStatuses erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentTypeUserStatuses?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentTypeUserStatuses?$top=10>

