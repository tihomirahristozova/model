---
uid: Logistics.Shipment.TransportationModes
---
# Logistics.Shipment.TransportationModes

Represents a mode of transportation, like water, air, road, etc. Entity: Log_Transportation_Modes

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Shipment.TransportationModes.md#Id) | guid |  
| [SystemIcon](Logistics.Shipment.TransportationModes.md#SystemIcon) | string | Icon, depicting the mode of transport. A=Air, W=Water, T=Train/Rail, R=Road, O=Other. [Required] [Default("O")] 
| [Code](Logistics.Shipment.TransportationModes.md#Code) | string | Unique transportation mode code. [Required] [Filter(eq;like)] [ORD] 
| [Name](Logistics.Shipment.TransportationModes.md#Name) | string | Multilanguage name of the mode of transportation. [Required] [Filter(eq;like)] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### SystemIcon

> Icon, depicting the mode of transport. A=Air, W=Water, T=Train/Rail, R=Road, O=Other. [Required] [Default("O")]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **O**  

### Code

> Unique transportation mode code. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Name

> Multilanguage name of the mode of transportation. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Shipment.TransportationModes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Shipment.TransportationModes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Shipment.TransportationModes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Shipment_TransportationModes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Shipment_TransportationModes?$top=10>

