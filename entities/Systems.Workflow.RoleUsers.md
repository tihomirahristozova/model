# Systems.Workflow.RoleUsers

The roles "played" by the security users. Entity: Wf_Role_Users

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Workflow.RoleUsers.md#Id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Role](Systems.Workflow.RoleUsers.md#Role) | [Systems.Workflow.Roles](Systems.Workflow.Roles.md) | The [Role](Systems.Workflow.RoleUsers.md#Role) to which this RoleUser belongs. [Required] [Filter(multi eq)] [Owner] |
| [User](Systems.Workflow.RoleUsers.md#User) | [Systems.Security.Users](Systems.Security.Users.md) | The user, which plays the role. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  


## Reference Details

### Role

> The [Role](Systems.Workflow.RoleUsers.md#Role) to which this RoleUser belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Systems.Workflow.Roles](Systems.Workflow.Roles.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### User

> The user, which plays the role. [Required] [Filter(multi eq)]

_Type_: **[Systems.Security.Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Workflow.RoleUsers erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Workflow.RoleUsers erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Workflow.RoleUsers erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Workflow_RoleUsers?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Workflow_RoleUsers?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Wf_Role_Users?$top=10>

