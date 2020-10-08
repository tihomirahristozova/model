---
uid: Crm.PriceLists
---
# Crm.PriceLists

Price Lists are used to manage multiple price records, assign to customers, etc. Entity: Crm_Price_Lists

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.PriceLists.md#Id) | guid |  
| [Description](Crm.PriceLists.md#Description) | string (nullable) | The description of this PriceList. 
| [FromDate](Crm.PriceLists.md#FromDate) | datetime (nullable) | Starting validity of the price list. [Filter(eq;ge;le)] 
| [Name](Crm.PriceLists.md#Name) | string | The name of this PriceList. [Required] [Filter(eq;like)] [ORD] 
| [ThruDate](Crm.PriceLists.md#ThruDate) | datetime (nullable) | Ending validity of the price list. [Filter(eq;ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Crm.PriceLists.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The Enterprise Company to which this PriceList applies, or null if it is for all enterprise companies. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Description

> The description of this PriceList.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### FromDate

> Starting validity of the price list. [Filter(eq;ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Name

> The name of this PriceList. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### ThruDate

> Ending validity of the price list. [Filter(eq;ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

> The Enterprise Company to which this PriceList applies, or null if it is for all enterprise companies. [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.PriceLists erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.PriceLists erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.PriceLists erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_PriceLists?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_PriceLists?$top=10>

