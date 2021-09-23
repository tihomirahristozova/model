---
uid: Logistics.Shipment.CargoTypes
---
# Logistics.Shipment.CargoTypes Entity

**Namespace:** [Logistics.Shipment](Logistics.Shipment.md)  

Represents a cargo type. Different cargo types might require different types of vehicles or modes of transportartion. Entity: Log_Cargo_Types

## Default Visualization
Default Display Text Format:  
_{Name:T} : {Code}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Logistics.Shipment.CargoTypes](Logistics.Shipment.CargoTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Logistics.Shipment.CargoTypes.md#code) | string (16) | The unique code of the CargoType. `Required` `Filter(eq;like)` `ORD` 
| [Id](Logistics.Shipment.CargoTypes.md#id) | guid |  
| [Name](Logistics.Shipment.CargoTypes.md#name) | string (256) | The name of this CargoType. `Required` `Filter(eq;like)` 
| [Notes](Logistics.Shipment.CargoTypes.md#notes) | string (max) __nullable__ | Notes for this CargoType. 


## Attribute Details

### Code

The unique code of the CargoType. `Required` `Filter(eq;like)` `ORD`

_Type_: **string (16)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **16**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this CargoType. `Required` `Filter(eq;like)`

_Type_: **string (256)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **256**  

### Notes

Notes for this CargoType.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  



## Business Rules

[!list limit=1000 erp.entity=Logistics.Shipment.CargoTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Logistics.Shipment.CargoTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Shipment_CargoTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Shipment_CargoTypes?$top=10>

