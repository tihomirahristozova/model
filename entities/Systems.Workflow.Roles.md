---
uid: Systems.Workflow.Roles
---
# Systems.Workflow.Roles Entity

The various roles, which the users can play. Entity: Wf_Roles

Default Display Text Format:  
_{Name:T}_  
Default Search Member:  
_Name_  

Aggregate Tree:  
* [Systems.Workflow.Roles](Systems.Workflow.Roles.md)  
  * [Systems.Workflow.RoleUsers](Systems.Workflow.RoleUsers.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Workflow.Roles.md#id) | guid |  
| [Name](Systems.Workflow.Roles.md#name) | string | The name of this Role. [Required] [Filter(eq;like)] [ORD] 
| [RoleDescription](Systems.Workflow.Roles.md#roledescription) | string (nullable) | Description of the role. 
| [VisualStyle](Systems.Workflow.Roles.md#visualstyle) | string (nullable) | The default visual style for the user interface. 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Users | [RoleUsers](Systems.Workflow.RoleUsers.md) | List of [RoleUser](Systems.Workflow.RoleUsers.md) child objects, based on the [Systems.Workflow.RoleUser.Role](Systems.Workflow.RoleUsers.md#role) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this Role. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### RoleDescription

Description of the role.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### VisualStyle

The default visual style for the user interface.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Workflow.Roles erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Workflow.Roles erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Workflow_Roles?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Workflow_Roles?$top=10>

