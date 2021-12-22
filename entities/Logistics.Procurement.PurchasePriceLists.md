---
uid: Logistics.Procurement.PurchasePriceLists
---
# Logistics.Procurement.PurchasePriceLists Entity

**Namespace:** [Logistics.Procurement](Logistics.Procurement.md)  

Contains purchase price list headers. Entity: Scm_Purchase_Price_Lists

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Logistics.Procurement.PurchasePriceLists](Logistics.Procurement.PurchasePriceLists.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FromDate](Logistics.Procurement.PurchasePriceLists.md#fromdate) | datetime __nullable__ | Starting validity of the price list. `Filter(eq;ge;le)` 
| [Id](Logistics.Procurement.PurchasePriceLists.md#id) | guid |  
| [Name](Logistics.Procurement.PurchasePriceLists.md#name) | string (50) | The name of this PurchasePriceList. `Required` `Filter(eq;like)` `ORD` 
| [ObjectVersion](Logistics.Procurement.PurchasePriceLists.md#objectversion) | int32 |  
| [ThruDate](Logistics.Procurement.PurchasePriceLists.md#thrudate) | datetime __nullable__ | Ending validity of the price list. `Filter(eq;ge;le)` 


## Attribute Details

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

The name of this PurchasePriceList. `Required` `Filter(eq;like)` `ORD`

_Type_: **string (50)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **50**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### ThruDate

Ending validity of the price list. `Filter(eq;ge;le)`

_Type_: **datetime __nullable__**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  



## Business Rules

[!list limit=1000 erp.entity=Logistics.Procurement.PurchasePriceLists erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Logistics.Procurement.PurchasePriceLists erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Procurement_PurchasePriceLists?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Procurement_PurchasePriceLists?$top=10>

