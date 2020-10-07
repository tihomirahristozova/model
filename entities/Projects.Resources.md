# Projects.Resources

Contains the enterprise resources, which are available for including in projects. Entity: Prj_Resources

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Projects.Resources.md#Id) | guid |  
| [Description](Projects.Resources.md#Description) | string (nullable) | The description of this Resource. 
| [Name](Projects.Resources.md#Name) | string | The name of this Resource. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Projects.Resources.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company owning the resource. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Description

> The description of this Resource.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Name

> The name of this Resource. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

> The enterprise company owning the resource. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Projects.Resources erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.Resources erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Projects.Resources erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_Resources?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_Resources?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Prj_Resources?$top=10>

