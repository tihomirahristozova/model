---
uid: Logistics.Shipment.TransportationVehicles
---
# Logistics.Shipment.TransportationVehicles Entity

**Namespace:** [Logistics.Shipment](Logistics.Shipment.md)  

A vehicle, which is used for transportation. One actual vehicle might be defined multiple times as transportation vehicle - for different modes of transportation or cargo types. Entity: Log_Transportation_Vehicles

## Default Visualization
Default Display Text Format:  
_{Code}_  
Default Search Member:  
_Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.Fleet.Vehicles](Applications.Fleet.Vehicles.md)  
Aggregate Root:  
[Applications.Fleet.Vehicles](Applications.Fleet.Vehicles.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Logistics.Shipment.TransportationVehicles.md#code) | string | The unique code (or call sign) of this transportation vehicle. `Required` `Filter(eq;like)` `ORD` 
| [Id](Logistics.Shipment.TransportationVehicles.md#id) | guid |  
| [MaxCargoWeightKg](Logistics.Shipment.TransportationVehicles.md#maxcargoweightkg) | int32 (nullable) | The maximum weight of the cargo (in kg), which can be transported. null when this is unknown and no limit should be enforced. 
| [MaxPalletsCount](Logistics.Shipment.TransportationVehicles.md#maxpalletscount) | int32 (nullable) | The maximum number of pallets, which can be transported by the vehicle. null when this is unknown and no limit should be enforced. 
| [Notes](Logistics.Shipment.TransportationVehicles.md#notes) | string (nullable) | Notes for this TransportationVehicle. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CargoType](Logistics.Shipment.TransportationVehicles.md#cargotype) | [CargoTypes](Logistics.Shipment.CargoTypes.md) | The cargo type supported by this transportation vehicle. `Required` `Filter(multi eq)` |
| [EnterpriseCompany](Logistics.Shipment.TransportationVehicles.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company to which the transportation vehicle will be bound. `Required` `Filter(multi eq)` |
| [TransportationMode](Logistics.Shipment.TransportationVehicles.md#transportationmode) | [TransportationModes](Logistics.Shipment.TransportationModes.md) | The mode of transportation provided by this transportation vehicle. The same base vehicle might be used for more than one mode. `Required` `Filter(multi eq)` |
| [Vehicle](Logistics.Shipment.TransportationVehicles.md#vehicle) | [Vehicles](Applications.Fleet.Vehicles.md) | The definition of the base vehicle. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Code

The unique code (or call sign) of this transportation vehicle. `Required` `Filter(eq;like)` `ORD`

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### MaxCargoWeightKg

The maximum weight of the cargo (in kg), which can be transported. null when this is unknown and no limit should be enforced.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### MaxPalletsCount

The maximum number of pallets, which can be transported by the vehicle. null when this is unknown and no limit should be enforced.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Notes

Notes for this TransportationVehicle.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### CargoType

The cargo type supported by this transportation vehicle. `Required` `Filter(multi eq)`

_Type_: **[CargoTypes](Logistics.Shipment.CargoTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompany

The enterprise company to which the transportation vehicle will be bound. `Required` `Filter(multi eq)`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### TransportationMode

The mode of transportation provided by this transportation vehicle. The same base vehicle might be used for more than one mode. `Required` `Filter(multi eq)`

_Type_: **[TransportationModes](Logistics.Shipment.TransportationModes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Vehicle

The definition of the base vehicle. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Vehicles](Applications.Fleet.Vehicles.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Shipment.TransportationVehicles erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Shipment.TransportationVehicles erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Shipment_TransportationVehicles?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Shipment_TransportationVehicles?$top=10>

