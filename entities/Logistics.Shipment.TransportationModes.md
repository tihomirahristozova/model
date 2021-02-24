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
  @aggregates  
Aggregate Tree  
* [Logistics.Shipment.TransportationModes](Logistics.Shipment.TransportationModes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Logistics.Shipment.TransportationModes.md#code) | string | Unique transportation mode code. [Required] [Filter(eq;like)] [ORD] 
| [Id](Logistics.Shipment.TransportationModes.md#id) | guid |  
| [Name](Logistics.Shipment.TransportationModes.md#name) | string | Multilanguage name of the mode of transportation. [Required] [Filter(eq;like)] 
| [SystemIcon](Logistics.Shipment.TransportationModes.md#systemicon) | string | Icon, depicting the mode of transport. A=Air, W=Water, T=Train/Rail, R=Road, O=Other. [Required] [Default("O")] 


## Attribute Details

### Code

Unique transportation mode code. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Multilanguage name of the mode of transportation. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### SystemIcon

Icon, depicting the mode of transport. A=Air, W=Water, T=Train/Rail, R=Road, O=Other. [Required] [Default("O")]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
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

