---
uid: Logistics.Procurement.PurchasePriceLists
---
# Logistics.Procurement.PurchasePriceLists

Contains purchase price list headers. Entity: Scm_Purchase_Price_Lists

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Procurement.PurchasePriceLists.md#Id) | guid |  
| [FromDate](Logistics.Procurement.PurchasePriceLists.md#FromDate) | datetime (nullable) | Starting validity of the price list. [Filter(eq;ge;le)] 
| [Name](Logistics.Procurement.PurchasePriceLists.md#Name) | string | The name of this PurchasePriceList. [Required] [Filter(eq;like)] [ORD] 
| [ThruDate](Logistics.Procurement.PurchasePriceLists.md#ThruDate) | datetime (nullable) | Ending validity of the price list. [Filter(eq;ge;le)] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### FromDate

> Starting validity of the price list. [Filter(eq;ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Name

> The name of this PurchasePriceList. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### ThruDate

> Ending validity of the price list. [Filter(eq;ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Procurement.PurchasePriceLists erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Procurement.PurchasePriceLists erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Procurement.PurchasePriceLists erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Procurement_PurchasePriceLists?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Procurement_PurchasePriceLists?$top=10>

