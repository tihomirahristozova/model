---
uid: Projects.TypeRoles
---
# Projects.TypeRoles Entity

**Namespace:** [Projects](Projects.md)  

Contains the roles of the participants of each project type. Entity: Prj_Type_Roles

## Default Visualization
Default Display Text Format:  
_{RoleName:T}_  
Default Search Member:  
_RoleName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Projects.ProjectTypes](Projects.ProjectTypes.md)  
Aggregate Root:  
[Projects.ProjectTypes](Projects.ProjectTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Description](Projects.TypeRoles.md#description) | string(2147483647) (nullable) | Description of the participant role. 
| [Id](Projects.TypeRoles.md#id) | guid |  
| [RoleName](Projects.TypeRoles.md#rolename) | string(255) | The name of the participant role. `Required` `Filter(multi eq;like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ProjectType](Projects.TypeRoles.md#projecttype) | [ProjectTypes](Projects.ProjectTypes.md) | Project type. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Description

Description of the participant role.

_Type_: **string(2147483647) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Default Value_: **NewGuid**  

### RoleName

The name of the participant role. `Required` `Filter(multi eq;like)`

_Type_: **string(255)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **255**  


## Reference Details

### ProjectType

Project type. `Required` `Filter(multi eq)` `Owner`

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

