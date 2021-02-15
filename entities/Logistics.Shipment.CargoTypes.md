---
uid: Logistics.Shipment.CargoTypes
---
# Logistics.Shipment.CargoTypes Entity

Represents a cargo type. Different cargo types might require different types of vehicles or modes of transportartion. Entity: Log_Cargo_Types

Default Display Text Format:  
_{Code}: {Name:T}_  
Default Search Member:  
_Code_  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Logistics.Shipment.CargoTypes.md#code) | string | The unique code of the CargoType. [Required] [Filter(eq;like)] [ORD] 
| [Id](Logistics.Shipment.CargoTypes.md#id) | guid |  
| [Name](Logistics.Shipment.CargoTypes.md#name) | string | The name of this CargoType. [Required] [Filter(eq;like)] 
| [Notes](Logistics.Shipment.CargoTypes.md#notes) | string (nullable) | Notes for this CargoType. 


## Attribute Details

### Code

The unique code of the CargoType. [Required] [Filter(eq;like)] [ORD]

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

The name of this CargoType. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

Notes for this CargoType.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Shipment.CargoTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Shipment.CargoTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Shipment_CargoTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Shipment_CargoTypes?$top=10>

