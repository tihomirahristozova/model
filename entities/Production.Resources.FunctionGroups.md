---
uid: Production.Resources.FunctionGroups
---
# Production.Resources.FunctionGroups Entity

**Namespace:** [Production.Resources](Production.Resources.md)  

Represents the hierarchy of the function groups. They group the multitude of resource functions in logical, user-defined groups. Entity: Prd_Function_Groups

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Production.Resources.FunctionGroups](Production.Resources.FunctionGroups.md)  
  * [Production.Resources.Functions](Production.Resources.Functions.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FullPath](Production.Resources.FunctionGroups.md#fullpath) | string (254) | The full path of the item. `Required` `Default("")` `Filter(eq;like)` 
| [Id](Production.Resources.FunctionGroups.md#id) | guid |  
| [Name](Production.Resources.FunctionGroups.md#name) | string (64) | The name of this FunctionGroup. `Required` `Filter(like)` 
| [ObjectVersion](Production.Resources.FunctionGroups.md#objectversion) | int32 |  
| [Parent](Production.Resources.FunctionGroups.md#parent) | string (254) | The path of the parent item. `Required` `Default("/")` `Filter(eq;like)` `ORD` 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Functions | [Functions](Production.Resources.Functions.md) | List of `Function`(Production.Resources.Functions.md) child objects, based on the `Production.Resources.Function.FunctionGroup`(Production.Resources.Functions.md#functiongroup) back reference 


## Attribute Details

### FullPath

The full path of the item. `Required` `Default("")` `Filter(eq;like)`

_Type_: **string (254)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  
_Default Value_: ****  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this FunctionGroup. `Required` `Filter(like)`

_Type_: **string (64)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### Parent

The path of the parent item. `Required` `Default("/")` `Filter(eq;like)` `ORD`

_Type_: **string (254)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **254**  
_Default Value_: **/**  


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

[!list limit=1000 erp.entity=Production.Resources.FunctionGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Production.Resources.FunctionGroups erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Resources_FunctionGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Resources_FunctionGroups?$top=10>

