---
uid: Projects.TypeRoles
---
# Projects.TypeRoles

Contains the roles of the participants of each project type. Entity: Prj_Type_Roles

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Projects.TypeRoles.md#Id) | guid |  
| [Description](Projects.TypeRoles.md#Description) | string (nullable) | Description of the participant role. 
| [RoleName](Projects.TypeRoles.md#RoleName) | string | The name of the participant role. [Required] [Filter(multi eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ProjectType](Projects.TypeRoles.md#ProjectType) | [Projects.ProjectTypes](Projects.ProjectTypes.md) | Project type. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Description

> Description of the participant role.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RoleName

> The name of the participant role. [Required] [Filter(multi eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### ProjectType

> Project type. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Projects.ProjectTypes](Projects.ProjectTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Projects.TypeRoles erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.TypeRoles erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Projects.TypeRoles erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_TypeRoles?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_TypeRoles?$top=10>

