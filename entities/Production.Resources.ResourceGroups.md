---
uid: Production.Resources.ResourceGroups
---
# Production.Resources.ResourceGroups Entity

**Namespace:** [Production.Resources](Production.Resources.md)  

Groups of resource types. Entity: Prd_Resource_Groups

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Production.Resources.ResourceGroups](Production.Resources.ResourceGroups.md)  
  * [Production.Resources.Resources](Production.Resources.Resources.md)  
    * [Production.Resources.ResourceFunctions](Production.Resources.ResourceFunctions.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FullPath](Production.Resources.ResourceGroups.md#fullpath) | string (254) | The full path to the operation group. The full path starts with, ends with and is delimited by the "/" (forward slash) character. `Required` `Default("")` `Filter(like)` 
| [Id](Production.Resources.ResourceGroups.md#id) | guid |  
| [Name](Production.Resources.ResourceGroups.md#name) | string (64) | Name of resource group. `Required` `Filter(like)` 
| [ObjectVersion](Production.Resources.ResourceGroups.md#objectversion) | int32 |  
| [Parent](Production.Resources.ResourceGroups.md#parent) | string (254) | Dot-separated list of parent groups. It also contains leading and trailing dot. `Required` `Default("/")` `Filter(like)` `ORD` 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Resources | [Resources](Production.Resources.Resources.md) | List of `Resource`(Production.Resources.Resources.md) child objects, based on the `Production.Resources.Resource.ResourceGroup`(Production.Resources.Resources.md#resourcegroup) back reference 


## Attribute Details

### FullPath

The full path to the operation group. The full path starts with, ends with and is delimited by the "/" (forward slash) character. `Required` `Default("")` `Filter(like)`

_Type_: **string (254)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  
_Default Value_: ****  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Name of resource group. `Required` `Filter(like)`

_Type_: **string (64)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### Parent

Dot-separated list of parent groups. It also contains leading and trailing dot. `Required` `Default("/")` `Filter(like)` `ORD`

_Type_: **string (254)**  
_Indexed_: **True**  
_Supported Filters_: **Like**  
_Supports Order By_: **True**  
_Maximum Length_: **254**  
_Default Value_: **/**  


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

[!list limit=1000 erp.entity=Production.Resources.ResourceGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Production.Resources.ResourceGroups erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Resources_ResourceGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Resources_ResourceGroups?$top=10>

