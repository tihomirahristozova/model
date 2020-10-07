# Systems.External.PublicUserLists

Each list represents a unique collection of public users. Entity: Ext_Public_User_Lists

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.External.PublicUserLists.md#Id) | guid |  
| [Notes](Systems.External.PublicUserLists.md#Notes) | string (nullable) | Notes for this PublicUserList. 
| [Name](Systems.External.PublicUserLists.md#Name) | string | The name of this PublicUserList. [Required] [Filter(like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Systems.External.PublicUserLists.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The enterprise company to which this list belongs. Null means that the list is available to services offered by all enterprise companies. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Notes

> Notes for this PublicUserList.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Name

> The name of this PublicUserList. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

> The enterprise company to which this list belongs. Null means that the list is available to services offered by all enterprise companies. [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



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

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Ext_Public_User_Lists?$top=10>

