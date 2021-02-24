---
uid: Systems.Workflow.RoleUsers
---
# Systems.Workflow.RoleUsers Entity

The roles "played" by the security users. Entity: Wf_Role_Users

Default Display Text Format:  
_{Role.Name:T}_  
Default Search Member:  
_Role.Name_  

[Aggregate](xref:aggregates) Parent:  
[Systems.Workflow.Roles](Systems.Workflow.Roles.md)  
[Aggregate](xref:aggregates) Root:  
[Systems.Workflow.Roles](Systems.Workflow.Roles.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Workflow.RoleUsers.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Role](Systems.Workflow.RoleUsers.md#role) | [Roles](Systems.Workflow.Roles.md) | The [Role](Systems.Workflow.RoleUsers.md#role) to which this RoleUser belongs. [Required] [Filter(multi eq)] [Owner] |
| [User](Systems.Workflow.RoleUsers.md#user) | [Users](Systems.Security.Users.md) | The user, which plays the role. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### Role

The [Role](Systems.Workflow.RoleUsers.md#role) to which this RoleUser belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Roles](Systems.Workflow.Roles.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### User

The user, which plays the role. [Required] [Filter(multi eq)]

_Type_: **[Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Systems.Workflow.RoleUsers erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Workflow.RoleUsers erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Workflow_RoleUsers?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Workflow_RoleUsers?$top=10>

