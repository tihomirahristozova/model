---
uid: Crm.PriceTypes
---
# Crm.PriceTypes Entity

**Namespace:** [Crm](Crm.md)  

Price types. Entity: Crm_Price_Types

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Crm.PriceTypes](Crm.PriceTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Crm.PriceTypes.md#code) | string (16) | Short identification code of the price type. `Required` `Filter(eq)` `ORD` 
| [Id](Crm.PriceTypes.md#id) | guid |  
| [Name](Crm.PriceTypes.md#name) | string (254) | Full name of the price type. `Required` `Filter(eq;like)` 
| [Notes](Crm.PriceTypes.md#notes) | string (max) __nullable__ | Notes for this PriceType. 
| [OrdinalPos](Crm.PriceTypes.md#ordinalpos) | int32 | Priority position of the price type, with respect to the other price types. `Required` `ORD` 


## Attribute Details

### Code

Short identification code of the price type. `Required` `Filter(eq)` `ORD`

_Type_: **string (16)**  
_Indexed_: **True**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  
_Maximum Length_: **16**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Full name of the price type. `Required` `Filter(eq;like)`

_Type_: **string (254)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Notes

Notes for this PriceType.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### OrdinalPos

Priority position of the price type, with respect to the other price types. `Required` `ORD`

_Type_: **int32**  
_Indexed_: **True**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Crm.PriceTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.PriceTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_PriceTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_PriceTypes?$top=10>

