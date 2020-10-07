# Systems.Workflow.Roles

The various roles, which the users can play. Entity: Wf_Roles

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Workflow.Roles.md#Id) | guid |  
| [RoleDescription](Systems.Workflow.Roles.md#RoleDescription) | string (nullable) | Description of the role. 
| [Name](Systems.Workflow.Roles.md#Name) | string | The name of this Role. [Required] [Filter(eq;like)] [ORD] 
| [VisualStyle](Systems.Workflow.Roles.md#VisualStyle) | string (nullable) | The default visual style for the user interface. 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Users | [Systems.Workflow.RoleUsers](Systems.Workflow.RoleUsers.md) | List of [RoleUser](Systems.Workflow.RoleUsers.md) child objects, based on the [Systems.Workflow.RoleUser.Role](Systems.Workflow.RoleUsers.md#Role) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### RoleDescription

> Description of the role.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Name

> The name of this Role. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### VisualStyle

> The default visual style for the user interface.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Workflow.Roles erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Workflow.Roles erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Workflow.Roles erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Workflow_Roles?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Workflow_Roles?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Wf_Roles?$top=10>

