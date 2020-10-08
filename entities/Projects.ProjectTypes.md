---
uid: Projects.ProjectTypes
---
# Projects.ProjectTypes

Contains the types of projects, which can be executed by the enterprise company. Entity: Prj_Types

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Projects.ProjectTypes.md#Id) | guid |  
| [Notes](Projects.ProjectTypes.md#Notes) | string (nullable) | Notes. 
| [Name](Projects.ProjectTypes.md#Name) | string | The name of the project type. [Required] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Projects.ProjectTypes.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | When not null means that the project type is specific to the enterprise company. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Roles | [Projects.TypeRoles](Projects.TypeRoles.md) | List of [TypeRole](Projects.TypeRoles.md) child objects, based on the [Projects.TypeRole.ProjectType](Projects.TypeRoles.md#ProjectType) back reference 
| WorkElements | [Projects.TypeWorkElements](Projects.TypeWorkElements.md) | List of [TypeWorkElement](Projects.TypeWorkElements.md) child objects, based on the [Projects.TypeWorkElement.ProjectType](Projects.TypeWorkElements.md#ProjectType) back reference 
| WorkTypes | [Projects.TypeWorkTypes](Projects.TypeWorkTypes.md) | List of [TypeWorkType](Projects.TypeWorkTypes.md) child objects, based on the [Projects.TypeWorkType.ProjectType](Projects.TypeWorkTypes.md#ProjectType) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Notes

> Notes.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Name

> The name of the project type. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

> When not null means that the project type is specific to the enterprise company. [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Projects.ProjectTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.ProjectTypes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Projects.ProjectTypes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_ProjectTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_ProjectTypes?$top=10>

