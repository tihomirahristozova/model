---
uid: Systems.Workflow.Roles
---
# Systems.Workflow.Roles Entity

**Namespace:** [Systems.Workflow](Systems.Workflow.md)  

The various roles, which the users can play. Entity: Wf_Roles

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Systems.Workflow.Roles](Systems.Workflow.Roles.md)  
  * [Systems.Workflow.RoleUsers](Systems.Workflow.RoleUsers.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Workflow.Roles.md#id) | guid |  
| [Name](Systems.Workflow.Roles.md#name) | string (254) | The name of this Role. `Required` `Filter(eq;like)` `ORD` 
| [ObjectVersion](Systems.Workflow.Roles.md#objectversion) | int32 |  
| [RoleDescription](Systems.Workflow.Roles.md#roledescription) | string (max) __nullable__ | Description of the role. 
| [VisualStyle](Systems.Workflow.Roles.md#visualstyle) | string (64) __nullable__ | The default visual style for the user interface. 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Users | [RoleUsers](Systems.Workflow.RoleUsers.md) | List of `RoleUser`(Systems.Workflow.RoleUsers.md) child objects, based on the `Systems.Workflow.RoleUser.Role`(Systems.Workflow.RoleUsers.md#role) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this Role. `Required` `Filter(eq;like)` `ORD`

_Type_: **string (254)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **254**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### RoleDescription

Description of the role.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### VisualStyle

The default visual style for the user interface.

_Type_: **string (64) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  


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

[!list limit=1000 erp.entity=Systems.Workflow.Roles erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Systems.Workflow.Roles erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Workflow_Roles?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Workflow_Roles?$top=10>

