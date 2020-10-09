---
uid: Systems.External.PublicUserLists
---
# Systems.External.PublicUserLists Entity

Each list represents a unique collection of public users. Entity: Ext_Public_User_Lists

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.External.PublicUserLists.md#id) | guid |  
| [Name](Systems.External.PublicUserLists.md#name) | string | The name of this PublicUserList. [Required] [Filter(like)] 
| [Notes](Systems.External.PublicUserLists.md#notes) | string (nullable) | Notes for this PublicUserList. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Systems.External.PublicUserLists.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The enterprise company to which this list belongs. Null means that the list is available to services offered by all enterprise companies. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

> The name of this PublicUserList. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Notes

> Notes for this PublicUserList.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

> The enterprise company to which this list belongs. Null means that the list is available to services offered by all enterprise companies. [Filter(multi eq)]

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Systems.External.PublicUserLists erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.External.PublicUserLists erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.External.PublicUserLists erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_External_PublicUserLists?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_External_PublicUserLists?$top=10>

