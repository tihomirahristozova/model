---
uid: General.PropertyEnterpriseCompanyFilters
---
# General.PropertyEnterpriseCompanyFilters Entity

**Namespace:** [General](General.md)  

Provides a way to apply different filtering of the property allowed values for the different enterprise companies. Entity: Gen_Property_Enterprise_Company_Filters

## Default Visualization
Default Display Text Format:  
_{Property.AllowedValuesEntityName:T} : {Property.Code}_  
Default Search Member:  
_Property.AllowedValuesEntityName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.CustomProperties](General.CustomProperties.md)  
Aggregate Root:  
[General.CustomProperties](General.CustomProperties.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FilterXml](General.PropertyEnterpriseCompanyFilters.md#filterxml) | dataaccessfilter __nullable__ | When not null, specifies a filter for the allowed values of the property for the specified enterprise company. 
| [Id](General.PropertyEnterpriseCompanyFilters.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](General.PropertyEnterpriseCompanyFilters.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company for which the current filter is specifed. `Required` `Filter(multi eq)` |
| [Property](General.PropertyEnterpriseCompanyFilters.md#property) | [CustomProperties](General.CustomProperties.md) | The `CustomProperty`(General.CustomProperties.md) to which this PropertyEnterprise<br />CompanyFilter belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### FilterXml

When not null, specifies a filter for the allowed values of the property for the specified enterprise company.

_Type_: **dataaccessfilter __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### EnterpriseCompany

The enterprise company for which the current filter is specifed. `Required` `Filter(multi eq)`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### Property

The `CustomProperty`(General.CustomProperties.md) to which this PropertyEnterpriseCompanyFilter belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[CustomProperties](General.CustomProperties.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=General.PropertyEnterpriseCompanyFilters erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.PropertyEnterpriseCompanyFilters erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_PropertyEnterpriseCompanyFilters?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_PropertyEnterpriseCompanyFilters?$top=10>

