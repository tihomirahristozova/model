---
uid: Systems.Workflow.Roles
---
# Systems.Workflow.Roles Entity

**Namespace:** [Systems.Workflow](Systems.Workflow.md)  

The various roles, which the users can play. Entity: Wf_Roles

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Member:  
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



## Business Rules

[!list erp.entity=Systems.Workflow.Roles erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Workflow.Roles erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Workflow_Roles?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Workflow_Roles?$top=10>

