---
uid: Applications.Fleet.VehicleSetVehicles
---
# Applications.Fleet.VehicleSetVehicles Entity

**Namespace:** [Applications.Fleet](Applications.Fleet.md)  

Contains lists of vehicles in the vehicle sets. Entity: Fleet_Vehicle_Set_Vehicles

## Default Visualization
Default Display Text Format:  
_{VehicleSet.Name:T}_  
Default Search Member:  
_VehicleSet.Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.Fleet.VehicleSets](Applications.Fleet.VehicleSets.md)  
Aggregate Root:  
[General.EnterpriseCompanies](General.EnterpriseCompanies.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Fleet.VehicleSetVehicles.md#id) | guid |  
| [Notes](Applications.Fleet.VehicleSetVehicles.md#notes) | string (254) __nullable__ | Notes for this VehicleSetVehicle. `Filter(like)` 
| [OrdinalPos](Applications.Fleet.VehicleSetVehicles.md#ordinalpos) | int32 __nullable__ | Ordinal position of the vehicle within the vehicle set. Position 0 has special meaning - this is the leading vehicle. `Filter(ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Vehicle](Applications.Fleet.VehicleSetVehicles.md#vehicle) | [Vehicles](Applications.Fleet.Vehicles.md) | The Vehicle which is part of the vehicle set. `Required` `Filter(multi eq)` |
| [VehicleSet](Applications.Fleet.VehicleSetVehicles.md#vehicleset) | [VehicleSets](Applications.Fleet.VehicleSets.md) | The `VehicleSet`(Applications.Fleet.VehicleSetVehicles.md#vehicleset) to which this VehicleSetVehicle belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this VehicleSetVehicle. `Filter(like)`

_Type_: **string (254) __nullable__**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### OrdinalPos

Ordinal position of the vehicle within the vehicle set. Position 0 has special meaning - this is the leading vehicle. `Filter(ge;le)`

_Type_: **int32 __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### Vehicle

The Vehicle which is part of the vehicle set. `Required` `Filter(multi eq)`

_Type_: **[Vehicles](Applications.Fleet.Vehicles.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### VehicleSet

The `VehicleSet`(Applications.Fleet.VehicleSetVehicles.md#vehicleset) to which this VehicleSetVehicle belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[VehicleSets](Applications.Fleet.VehicleSets.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list erp.entity=Applications.Fleet.VehicleSetVehicles erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Fleet.VehicleSetVehicles erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_VehicleSetVehicles?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_VehicleSetVehicles?$top=10>

