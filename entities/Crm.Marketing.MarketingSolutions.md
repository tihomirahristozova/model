---
uid: Crm.Marketing.MarketingSolutions
---
# Crm.Marketing.MarketingSolutions Entity

**Namespace:** [Crm.Marketing](Crm.Marketing.md)  

The solutions which we are offering to our clients. The solutions usually depend on the industry and the size of the client. Entity: Crm_Marketing_Solutions (Introduced in version 21.1.3.59)

## Default Visualization
Default Display Text Format:  
_{Name:T} : {Code}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Crm.Marketing.MarketingSolutions](Crm.Marketing.MarketingSolutions.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Crm.Marketing.MarketingSolutions.md#code) | string (32) | The unique code of the MarketingSolution. `Required` `Filter(eq;like)` `ORD` 
| [Id](Crm.Marketing.MarketingSolutions.md#id) | guid |  
| [Name](Crm.Marketing.MarketingSolutions.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of this MarketingSolution. `Required` `Filter(eq;like)` 
| [Notes](Crm.Marketing.MarketingSolutions.md#notes) | string (max) __nullable__ | Notes for this MarketingSolution. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CompanySizeClass](Crm.Marketing.MarketingSolutions.md#companysizeclass) | [CompanySizeClasses](Crm.Marketing.CompanySizeClasses.md) (nullable) | The company size class, for which this solution is appropriate. null if not applicable. `Filter(multi eq)` |
| [EnterpriseCompany](Crm.Marketing.MarketingSolutions.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company offering this marketing solution. `Required` `Filter(multi eq)` |
| [Industry](Crm.Marketing.MarketingSolutions.md#industry) | [Industries](Crm.Marketing.Industries.md) (nullable) | The industry, for which this solution is appropriate. null if not applicable. `Filter(multi eq)` |


## Attribute Details

### Code

The unique code of the MarketingSolution. `Required` `Filter(eq;like)` `ORD`

_Type_: **string (32)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **32**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this MarketingSolution. `Required` `Filter(eq;like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

Notes for this MarketingSolution.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  


## Reference Details

### CompanySizeClass

The company size class, for which this solution is appropriate. null if not applicable. `Filter(multi eq)`

_Type_: **[CompanySizeClasses](Crm.Marketing.CompanySizeClasses.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompany

The enterprise company offering this marketing solution. `Required` `Filter(multi eq)`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Industry

The industry, for which this solution is appropriate. null if not applicable. `Filter(multi eq)`

_Type_: **[Industries](Crm.Marketing.Industries.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Crm.Marketing.MarketingSolutions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.Marketing.MarketingSolutions erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Marketing_MarketingSolutions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Marketing_MarketingSolutions?$top=10>

