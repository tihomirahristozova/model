---
uid: Crm.PriceLists
---
# Crm.PriceLists Entity

**Namespace:** [Crm](Crm.md)  

Price Lists are used to manage multiple price records, assign to customers, etc. Entity: Crm_Price_Lists

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Crm.PriceLists](Crm.PriceLists.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Description](Crm.PriceLists.md#description) | string (max) __nullable__ | The description of this PriceList. 
| [FromDate](Crm.PriceLists.md#fromdate) | datetime __nullable__ | Starting validity of the price list. `Filter(eq;ge;le)` 
| [Id](Crm.PriceLists.md#id) | guid |  
| [Name](Crm.PriceLists.md#name) | string (50) | The name of this PriceList. `Required` `Filter(eq;like)` `ORD` 
| [RowVersion](Crm.PriceLists.md#rowversion) | byte[] |  
| [ThruDate](Crm.PriceLists.md#thrudate) | datetime __nullable__ | Ending validity of the price list. `Filter(eq;ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Crm.PriceLists.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The Enterprise Company to which this PriceList applies, or null if it is for all enterprise companies. `Filter(multi eq)` |


## Attribute Details

### Description

The description of this PriceList.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### FromDate

Starting validity of the price list. `Filter(eq;ge;le)`

_Type_: **datetime __nullable__**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this PriceList. `Required` `Filter(eq;like)` `ORD`

_Type_: **string (50)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **50**  

### RowVersion

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ThruDate

Ending validity of the price list. `Filter(eq;ge;le)`

_Type_: **datetime __nullable__**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

The Enterprise Company to which this PriceList applies, or null if it is for all enterprise companies. `Filter(multi eq)`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Crm.PriceLists erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.PriceLists erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_PriceLists?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_PriceLists?$top=10>

