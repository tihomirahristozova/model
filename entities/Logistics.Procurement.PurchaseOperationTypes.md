---
uid: Logistics.Procurement.PurchaseOperationTypes
---
# Logistics.Procurement.PurchaseOperationTypes Entity

**Namespace:** [Logistics.Procurement](Logistics.Procurement.md)  

User-defined categorization of the purchase operations. Used to group the purchase control data. Entity: Scm_Purchase_Operation_Types (Introduced in version 18.2)

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Members:  
_Code; Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Logistics.Procurement.PurchaseOperationTypes](Logistics.Procurement.PurchaseOperationTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Logistics.Procurement.PurchaseOperationTypes.md#code) | string (16) | Unique code of the purchase operation type. `Required` `Filter(multi eq;like)` 
| [Id](Logistics.Procurement.PurchaseOperationTypes.md#id) | guid |  
| [Name](Logistics.Procurement.PurchaseOperationTypes.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Name of the purchase operation type (multilanguage). `Required` `Filter(multi eq;like)` 
| [Notes](Logistics.Procurement.PurchaseOperationTypes.md#notes) | string (max) __nullable__ | Notes for this PurchaseOperationType. `Filter(eq;like)` 
| [ObjectVersion](Logistics.Procurement.PurchaseOperationTypes.md#objectversion) | int32 |  


## Attribute Details

### Code

Unique code of the purchase operation type. `Required` `Filter(multi eq;like)`

_Type_: **string (16)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **16**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Name of the purchase operation type (multilanguage). `Required` `Filter(multi eq;like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  

### Notes

Notes for this PurchaseOperationType. `Filter(eq;like)`

_Type_: **string (max) __nullable__**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  



## Business Rules

[!list limit=1000 erp.entity=Logistics.Procurement.PurchaseOperationTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Logistics.Procurement.PurchaseOperationTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Procurement_PurchaseOperationTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Procurement_PurchaseOperationTypes?$top=10>

