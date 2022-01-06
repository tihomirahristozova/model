---
uid: Systems.Core.ObjectChanges
---
# Systems.Core.ObjectChanges Entity

**Namespace:** [Systems.Core](Systems.Core.md)  

Actual tracked changes to one object. Entity: Sys_Object_Changes (Introduced in version 19.1)

## Default Visualization
Default Display Text Format:  
_{RepositoryName}_  
Default Search Members:  
_RepositoryName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Systems.Core.ObjectChangesets](Systems.Core.ObjectChangesets.md)  
Aggregate Root:  
[Systems.Core.ObjectChangesets](Systems.Core.ObjectChangesets.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ChangeType](Systems.Core.ObjectChanges.md#changetype) | [ChangeType](Systems.Core.ObjectChanges.md#changetype) | Type of change - Create, Update or Delete. `Required` 
| [EntityItemId](Systems.Core.ObjectChanges.md#entityitemid) | guid | The id of the actual changed object, described by this change. This is different than the aggregate root, which is pointed by Root Object. `Required` `Filter(multi eq)` 
| [Id](Systems.Core.ObjectChanges.md#id) | guid |  
| [ObjectVersion](Systems.Core.ObjectChanges.md#objectversion) | int32 |  
| [RepositoryName](Systems.Core.ObjectChanges.md#repositoryname) | string (64) | The repository of the actual changed object, described by this change. This is different than the aggregate root, which is pointed by Root Object. `Required` `Filter(multi eq;like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ObjectChangeset](Systems.Core.ObjectChanges.md#objectchangeset) | [ObjectChangesets](Systems.Core.ObjectChangesets.md) | The changeset containing this change. `Required` `Filter(multi eq)` `Owner` |
| [RootObject](Systems.Core.ObjectChanges.md#rootobject) | [ExtensibleDataObjects](Systems.Core.ExtensibleDataObjects.md) | The root object in the aggregate of the object, which has been changed. Each change is recorded at the aggregate root level. `Required` `Filter(multi eq)` |


## Attribute Details

### ChangeType

Type of change - Create, Update or Delete. `Required`

_Type_: **[ChangeType](Systems.Core.ObjectChanges.md#changetype)**  
Allowed values for the `ChangeType`(Systems.Core.ObjectChanges.md#changetype) data attribute  
_Allowed Values (Systems.Core.ObjectChangesRepository.ChangeType Enum Members)_  

| Value | Description |
| ---- | --- |
| Create | Create value. Stored as 'C'. <br /> _Database Value:_ 'C' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Create' |
| Update | Update value. Stored as 'U'. <br /> _Database Value:_ 'U' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Update' |
| Delete | Delete value. Stored as 'D'. <br /> _Database Value:_ 'D' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Delete' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### EntityItemId

The id of the actual changed object, described by this change. This is different than the aggregate root, which is pointed by Root Object. `Required` `Filter(multi eq)`

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### RepositoryName

The repository of the actual changed object, described by this change. This is different than the aggregate root, which is pointed by Root Object. `Required` `Filter(multi eq;like)`

_Type_: **string (64)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  


## Reference Details

### ObjectChangeset

The changeset containing this change. `Required` `Filter(multi eq)` `Owner`

_Type_: **[ObjectChangesets](Systems.Core.ObjectChangesets.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### RootObject

The root object in the aggregate of the object, which has been changed. Each change is recorded at the aggregate root level. `Required` `Filter(multi eq)`

_Type_: **[ExtensibleDataObjects](Systems.Core.ExtensibleDataObjects.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  


## API Methods

Methods that can be invoked in public APIs.

### GetAllowedCustomPropertyValues

Gets the allowed values for the specified custom property for this entity object.              If supported the result is ordered by property value. Some property value sources do not support ordering - in that case the result is not ordered.  
_Return Type_: **Collection Of [CustomPropertyValue](../data-types.md#general.custompropertyvalue)**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **GET**  

**Parameters**  
  * **customPropertyCode**  
    The code of the custom property  
    _Type_: string  

  * **search**  
    The search text - searches by value or description. Can contain wildcard character %.  
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

[!list limit=1000 erp.entity=Systems.Core.ObjectChanges erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Systems.Core.ObjectChanges erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_ObjectChanges?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_ObjectChanges?$top=10>

