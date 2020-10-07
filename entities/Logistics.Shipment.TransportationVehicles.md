# Logistics.Shipment.TransportationVehicles

A vehicle, which is used for transportation. One actual vehicle might be defined multiple times as transportation vehicle - for different modes of transportation or cargo types. Entity: Log_Transportation_Vehicles

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Shipment.TransportationVehicles.md#Id) | guid |  
| [Code](Logistics.Shipment.TransportationVehicles.md#Code) | string | The unique code (or call sign) of this transportation vehicle. [Required] [Filter(eq;like)] [ORD] 
| [MaxCargoWeightKg](Logistics.Shipment.TransportationVehicles.md#MaxCargoWeightKg) | int32 (nullable) | The maximum weight of the cargo (in kg), which can be transported. null when this is unknown and no limit should be enforced. 
| [MaxPalletsCount](Logistics.Shipment.TransportationVehicles.md#MaxPalletsCount) | int32 (nullable) | The maximum number of pallets, which can be transported by the vehicle. null when this is unknown and no limit should be enforced. 
| [Notes](Logistics.Shipment.TransportationVehicles.md#Notes) | string (nullable) | Notes for this TransportationVehicle. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CargoType](Logistics.Shipment.TransportationVehicles.md#CargoType) | [Logistics.Shipment.CargoTypes](Logistics.Shipment.CargoTypes.md) | The cargo type supported by this transportation vehicle. [Required] [Filter(multi eq)] |
| [EnterpriseCompany](Logistics.Shipment.TransportationVehicles.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company to which the transportation vehicle will be bound. [Required] [Filter(multi eq)] |
| [TransportationMode](Logistics.Shipment.TransportationVehicles.md#TransportationMode) | [Logistics.Shipment.TransportationModes](Logistics.Shipment.TransportationModes.md) | The mode of transportation provided by this transportation vehicle. The same base vehicle might be used for more than one mode. [Required] [Filter(multi eq)] |
| [Vehicle](Logistics.Shipment.TransportationVehicles.md#Vehicle) | [Applications.Fleet.Vehicles](Applications.Fleet.Vehicles.md) | The definition of the base vehicle. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Code

> The unique code (or call sign) of this transportation vehicle. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### MaxCargoWeightKg

> The maximum weight of the cargo (in kg), which can be transported. null when this is unknown and no limit should be enforced.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### MaxPalletsCount

> The maximum number of pallets, which can be transported by the vehicle. null when this is unknown and no limit should be enforced.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Notes

> Notes for this TransportationVehicle.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### CargoType

> The cargo type supported by this transportation vehicle. [Required] [Filter(multi eq)]

_Type_: **[Logistics.Shipment.CargoTypes](Logistics.Shipment.CargoTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### EnterpriseCompany

> The enterprise company to which the transportation vehicle will be bound. [Required] [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### TransportationMode

> The mode of transportation provided by this transportation vehicle. The same base vehicle might be used for more than one mode. [Required] [Filter(multi eq)]

_Type_: **[Logistics.Shipment.TransportationModes](Logistics.Shipment.TransportationModes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Vehicle

> The definition of the base vehicle. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Applications.Fleet.Vehicles](Applications.Fleet.Vehicles.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Shipment.TransportationVehicles erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Shipment.TransportationVehicles erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Shipment.TransportationVehicles erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Shipment_TransportationVehicles?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Shipment_TransportationVehicles?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Log_Transportation_Vehicles?$top=10>

