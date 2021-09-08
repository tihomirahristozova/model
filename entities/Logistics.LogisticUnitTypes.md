---
uid: Logistics.LogisticUnitTypes
---
# Logistics.LogisticUnitTypes Entity

**Namespace:** [Logistics](Logistics.md)  

Types of logistic units, like EU-PALLET, 40x40 pallet, ISO container, etc. Entity: Log_Logistic_Unit_Types (Introduced in version 21.1.0.77)

## Default Visualization
Default Display Text Format:  
_{Name:T} #{Code}_  
Default Search Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Logistics.LogisticUnitTypes](Logistics.LogisticUnitTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Logistics.LogisticUnitTypes.md#code) | string (16) | Unique code of the logistic unit type. Used for display and selection purposes. Can contain only EN letters and numbers. `Required` `Filter(multi eq;like)` 
| [Id](Logistics.LogisticUnitTypes.md#id) | guid |  
| [Name](Logistics.LogisticUnitTypes.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Multi-language name of the logistic unit type. `Required` `Filter(eq;like)` 
| [Notes](Logistics.LogisticUnitTypes.md#notes) | string (max) __nullable__ | Notes for this LogisticUnitType. `Filter(like)` 


## Attribute Details

### Code

Unique code of the logistic unit type. Used for display and selection purposes. Can contain only EN letters and numbers. `Required` `Filter(multi eq;like)`

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

Multi-language name of the logistic unit type. `Required` `Filter(eq;like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

Notes for this LogisticUnitType. `Filter(like)`

_Type_: **string (max) __nullable__**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  



## Business Rules

[!list limit=1000 erp.entity=Logistics.LogisticUnitTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Logistics.LogisticUnitTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_LogisticUnitTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_LogisticUnitTypes?$top=10>

