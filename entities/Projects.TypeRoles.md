---
uid: Projects.TypeRoles
---
# Projects.TypeRoles Entity

Contains the roles of the participants of each project type. Entity: Prj_Type_Roles

Default Display Text Format:  
_{RoleName:T}_  
Default Search Member:  
_RoleName_  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Description](Projects.TypeRoles.md#description) | string (nullable) | Description of the participant role. 
| [Id](Projects.TypeRoles.md#id) | guid |  
| [RoleName](Projects.TypeRoles.md#rolename) | string | The name of the participant role. [Required] [Filter(multi eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ProjectType](Projects.TypeRoles.md#projecttype) | [ProjectTypes](Projects.ProjectTypes.md) | Project type. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Description

Description of the participant role.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Default Value_: **NewGuid**  

### RoleName

The name of the participant role. [Required] [Filter(multi eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### ProjectType

Project type. [Required] [Filter(multi eq)] [Owner]

_Type_: **[ProjectTypes](Projects.ProjectTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Projects.TypeRoles erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.TypeRoles erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_TypeRoles?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_TypeRoles?$top=10>

