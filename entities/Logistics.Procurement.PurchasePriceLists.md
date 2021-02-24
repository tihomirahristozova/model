---
uid: Logistics.Procurement.PurchasePriceLists
---
# Logistics.Procurement.PurchasePriceLists Entity

**Namespace:** [Logistics.Procurement](Logistics.Procurement.md)  

Contains purchase price list headers. Entity: Scm_Purchase_Price_Lists

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Member:  
_Name_  

## Aggregate
  @aggregates  
Aggregate Tree  
* [Logistics.Procurement.PurchasePriceLists](Logistics.Procurement.PurchasePriceLists.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FromDate](Logistics.Procurement.PurchasePriceLists.md#fromdate) | datetime (nullable) | Starting validity of the price list. [Filter(eq;ge;le)] 
| [Id](Logistics.Procurement.PurchasePriceLists.md#id) | guid |  
| [Name](Logistics.Procurement.PurchasePriceLists.md#name) | string | The name of this PurchasePriceList. [Required] [Filter(eq;like)] [ORD] 
| [ThruDate](Logistics.Procurement.PurchasePriceLists.md#thrudate) | datetime (nullable) | Ending validity of the price list. [Filter(eq;ge;le)] 


## Attribute Details

### FromDate

Starting validity of the price list. [Filter(eq;ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this PurchasePriceList. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### ThruDate

Ending validity of the price list. [Filter(eq;ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Procurement.PurchasePriceLists erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Procurement.PurchasePriceLists erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Procurement_PurchasePriceLists?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Procurement_PurchasePriceLists?$top=10>

