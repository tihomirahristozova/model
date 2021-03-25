---
uid: Logistics.Shipment.TransportationModes
---
# Logistics.Shipment.TransportationModes Entity

**Namespace:** [Logistics.Shipment](Logistics.Shipment.md)  

Represents a mode of transportation, like water, air, road, etc. Entity: Log_Transportation_Modes

## Default Visualization
Default Display Text Format:  
_{Code}: {Name:T}_  
Default Search Member:  
_Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Logistics.Shipment.TransportationModes](Logistics.Shipment.TransportationModes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Logistics.Shipment.TransportationModes.md#code) | string (8) | Unique transportation mode code. `Required` `Filter(eq;like)` `ORD` 
| [Id](Logistics.Shipment.TransportationModes.md#id) | guid |  
| [Name](Logistics.Shipment.TransportationModes.md#name) | string (254) | Multilanguage name of the mode of transportation. `Required` `Filter(eq;like)` 
| [SystemIcon](Logistics.Shipment.TransportationModes.md#systemicon) | string (1) | Icon, depicting the mode of transport. A=Air, W=Water, T=Train/Rail, R=Road, O=Other. `Required` `Default("O")` 


## Attribute Details

### Code

Unique transportation mode code. `Required` `Filter(eq;like)` `ORD`

_Type_: **string (8)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **8**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Multilanguage name of the mode of transportation. `Required` `Filter(eq;like)`

_Type_: **string (254)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### SystemIcon

Icon, depicting the mode of transport. A=Air, W=Water, T=Train/Rail, R=Road, O=Other. `Required` `Default("O")`

_Type_: **string (1)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **1**  
_Default Value_: **O**  



## Business Rules

[!list erp.entity=Logistics.Shipment.TransportationModes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Shipment.TransportationModes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Shipment_TransportationModes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Shipment_TransportationModes?$top=10>

