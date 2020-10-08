---
uid: Systems.Core.ObjectChanges
---
# Systems.Core.ObjectChanges

Actual tracked changes to one object. Entity: Sys_Object_Changes (Introduced in version 19.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Core.ObjectChanges.md#Id) | guid |  
| [ChangeType](Systems.Core.ObjectChanges.md#ChangeType) | [Systems.Core.ObjectChangesRepository.ChangeType](Systems.Core.ObjectChanges.md#ChangeType) | Type of change - Create, Update or Delete. [Required] 
| [EntityItemId](Systems.Core.ObjectChanges.md#EntityItemId) | guid | The id of the actual changed object, described by this change. This is different than the aggregate root, which is pointed by Root Object. [Required] [Filter(multi eq)] 
| [RepositoryName](Systems.Core.ObjectChanges.md#RepositoryName) | string | The repository of the actual changed object, described by this change. This is different than the aggregate root, which is pointed by Root Object. [Required] [Filter(multi eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ObjectChangeset](Systems.Core.ObjectChanges.md#ObjectChangeset) | [Systems.Core.ObjectChangesets](Systems.Core.ObjectChangesets.md) | The changeset containing this change. [Required] [Filter(multi eq)] [Owner] |
| [RootObject](Systems.Core.ObjectChanges.md#RootObject) | [Systems.Core.ExtensibleDataObjects](Systems.Core.ExtensibleDataObjects.md) | The root object in the aggregate of the object, which has been changed. Each change is recorded at the aggregate root level. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ChangeType

> Type of change - Create, Update or Delete. [Required]

_Type_: **[Systems.Core.ObjectChangesRepository.ChangeType](Systems.Core.ObjectChanges.md#ChangeType)**  
Allowed values for the [ChangeType](Systems.Core.ObjectChanges.md#ChangeType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Create | Create value. Stored as 'C'. <br /> _Database Value:_ 'C' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Create' |
| Update | Update value. Stored as 'U'. <br /> _Database Value:_ 'U' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Update' |
| Delete | Delete value. Stored as 'D'. <br /> _Database Value:_ 'D' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Delete' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### EntityItemId

> The id of the actual changed object, described by this change. This is different than the aggregate root, which is pointed by Root Object. [Required] [Filter(multi eq)]

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### RepositoryName

> The repository of the actual changed object, described by this change. This is different than the aggregate root, which is pointed by Root Object. [Required] [Filter(multi eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### ObjectChangeset

> The changeset containing this change. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Systems.Core.ObjectChangesets](Systems.Core.ObjectChangesets.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### RootObject

> The root object in the aggregate of the object, which has been changed. Each change is recorded at the aggregate root level. [Required] [Filter(multi eq)]

_Type_: **[Systems.Core.ExtensibleDataObjects](Systems.Core.ExtensibleDataObjects.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Core.ObjectChanges erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Core.ObjectChanges erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Core.ObjectChanges erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_ObjectChanges?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_ObjectChanges?$top=10>

