---
uid: Applications.Fleet.Vehicles
---
# Applications.Fleet.Vehicles

Contains vehicle definitions. Entity: Fleet_Vehicles

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Fleet.Vehicles.md#Id) | guid |  
| [ActiveFrom](Applications.Fleet.Vehicles.md#ActiveFrom) | datetime (nullable) | The date and time, when the vehicle has been purchased or started to be managed. Null when the date and time are unknown. (Introduced in version 18.2.100.0) 
| [ActiveTill](Applications.Fleet.Vehicles.md#ActiveTill) | datetime (nullable) | The date and time, when the vehicle has been sold or has stopped being managed. Null when the date and time are unknown. (Introduced in version 18.2.100.0) 
| [AuthorityMaximumLadenMassKg](Applications.Fleet.Vehicles.md#AuthorityMaximumLadenMassKg) | int32 (nullable) | Maximum permissible laden mass, as determined by the registration authority. 
| [CrewCount](Applications.Fleet.Vehicles.md#CrewCount) | int32 (nullable) | Crew members count. For road vehicles = 1; for trailers, coaches and wagons =0; air and water vehicles may have higher counts. [Default(1)] [Filter(eq;ge;le)] 
| [EngineIdentificationNumber](Applications.Fleet.Vehicles.md#EngineIdentificationNumber) | string (nullable) | Engine identification number. [Filter(eq;like)] 
| [EnginePowerhp](Applications.Fleet.Vehicles.md#EnginePowerhp) | int32 (nullable) | Engine output power in horse power. null means that the value is unknown or not applicable for this type of engine. [Filter(eq;ge;le)] 
| [EngineSizecc](Applications.Fleet.Vehicles.md#EngineSizecc) | int32 (nullable) | Engine size in cubic centimeters (cm3). null means that the value is unknown or not applicable for this type of engine (e.g. electric motors). [Filter(eq;ge;le)] 
| [FuelCapacity](Applications.Fleet.Vehicles.md#FuelCapacity) | int32 (nullable) | Maximum fuel capacity of the engine or the battery in the fuel measurement unit. 
| [FuelCompsumption](Applications.Fleet.Vehicles.md#FuelCompsumption) | decimal (nullable) | Average fuel consumption in the fuel measurement unit for 1 operational unit. 
| [FuelType](Applications.Fleet.Vehicles.md#FuelType) | string (nullable) | Fuel type of the engine or the power source of the engine (Multilanguage) - e.g. diesel, benzine, electric, etc. [Filter(eq;like)] 
| [IsActive](Applications.Fleet.Vehicles.md#IsActive) | boolean | True if the vehicle is still owned and managed by the enterprise. [Required] [Default(true)] (Introduced in version 18.2.100.0) 
| [IssuingAuthority](Applications.Fleet.Vehicles.md#IssuingAuthority) | [MultilanguageString](../data-types.md#MultilanguageString) (nullable) | The country or state issuing the registration number. null (not recommended) means that the authority is unknown or not applicable. [Filter(eq;like)] 
| [Make](Applications.Fleet.Vehicles.md#Make) | [MultilanguageString](../data-types.md#MultilanguageString) (nullable) | The name of the manufacturer of the vehicle. null means that the value is unknown. [Filter(eq;like)] 
| [ManufactureYear](Applications.Fleet.Vehicles.md#ManufactureYear) | int32 (nullable) | The year when the vehicle was manufactured or first registered - whichever is known. null means that the value is unknown. [Filter(eq;ge;le)] 
| [MaximumSpeedKmH](Applications.Fleet.Vehicles.md#MaximumSpeedKmH) | int32 (nullable) | Maximum speed in km/h. 
| [Model](Applications.Fleet.Vehicles.md#Model) | [MultilanguageString](../data-types.md#MultilanguageString) (nullable) | The model of the vehicle. [Filter(eq;like)] 
| [Notes](Applications.Fleet.Vehicles.md#Notes) | string (nullable) | Notes for this Vehicle. 
| [PrimaryColor](Applications.Fleet.Vehicles.md#PrimaryColor) | [MultilanguageString](../data-types.md#MultilanguageString) (nullable) | The primary color of the vehicle. null means that the value is unknown or not applicable. [Filter(eq;like)] 
| [SeatingPlacesCount](Applications.Fleet.Vehicles.md#SeatingPlacesCount) | int32 (nullable) | Number of seating places, excluding driver. [Filter(eq;ge;le)] 
| [StandingPlacesCount](Applications.Fleet.Vehicles.md#StandingPlacesCount) | int32 (nullable) | Number of standing places, if applicable. 
| [TechnicalMaximumLadenMassKg](Applications.Fleet.Vehicles.md#TechnicalMaximumLadenMassKg) | int32 (nullable) | Maximum technically permissible laden mass in kg. 
| [TrainsetMaximumLadenMassKg](Applications.Fleet.Vehicles.md#TrainsetMaximumLadenMassKg) | int32 (nullable) | Maximum permissible laden mass of a whole trainset, including the vehicle. 
| [VehicleIdentificationNumber](Applications.Fleet.Vehicles.md#VehicleIdentificationNumber) | string (nullable) | VIN, aka Chassis number. [Filter(eq;like)] 
| [VehicleMassKg](Applications.Fleet.Vehicles.md#VehicleMassKg) | int32 (nullable) | Vehicle own mass in kg. 
| [VehicleRegistrationNumber](Applications.Fleet.Vehicles.md#VehicleRegistrationNumber) | string | The registration plate number. Can be numeric or alphanumeric code. It should be unique within the Issuing_Authority. [Required] [Filter(eq;like)] 
| [VehicleType](Applications.Fleet.Vehicles.md#VehicleType) | [MultilanguageString](../data-types.md#MultilanguageString) (nullable) | Type of vehicle - e.g. automobile, bus, etc. null means the value is unknown. [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [FuelMeasurementUnit](Applications.Fleet.Vehicles.md#FuelMeasurementUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) (nullable) | The measurement unit in which the fuel is measured. E.g. liters for automobiles, Watt-hours for electrics, etc. null means unknown. [Filter(multi eq)] |
| [MaintenanceProfile](Applications.Fleet.Vehicles.md#MaintenanceProfile) | [Applications.Fleet.MaintenanceProfiles](Applications.Fleet.MaintenanceProfiles.md) (nullable) | When not null, specifies, that the vehicle should be maintained according to the specified profile. Assigning a profile creates plan assignments for the vehicle. Ultimately, the specific plan assignments are taken into consideration, when planning vehicle maintenance. The profile is only for conveniently assigning multiple plans. [Filter(multi eq)] |
| [OperationalMeasurementUnit](Applications.Fleet.Vehicles.md#OperationalMeasurementUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) (nullable) | The measurement unit in which the operation of the vehicle is measured. E.g. km for automobiles, hrs for airplanes, etc. null means that the unit is unknown. [Filter(multi eq)] |
| [OwnerParty](Applications.Fleet.Vehicles.md#OwnerParty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | Vehicle owner. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Equipment | [Applications.Fleet.VehicleEquipment](Applications.Fleet.VehicleEquipment.md) | List of [VehicleEquipment](Applications.Fleet.VehicleEquipment.md) child objects, based on the [Applications.Fleet.VehicleEquipment.Vehicle](Applications.Fleet.VehicleEquipment.md#Vehicle) back reference 
| TransportationVehicles | [Logistics.Shipment.TransportationVehicles](Logistics.Shipment.TransportationVehicles.md) | List of [TransportationVehicle](Logistics.Shipment.TransportationVehicles.md) child objects, based on the [Logistics.Shipment.TransportationVehicle.Vehicle](Logistics.Shipment.TransportationVehicles.md#Vehicle) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ActiveFrom

> The date and time, when the vehicle has been purchased or started to be managed. Null when the date and time are unknown. (Introduced in version 18.2.100.0)

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ActiveTill

> The date and time, when the vehicle has been sold or has stopped being managed. Null when the date and time are unknown. (Introduced in version 18.2.100.0)

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### AuthorityMaximumLadenMassKg

> Maximum permissible laden mass, as determined by the registration authority.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### CrewCount

> Crew members count. For road vehicles = 1; for trailers, coaches and wagons =0; air and water vehicles may have higher counts. [Default(1)] [Filter(eq;ge;le)]

_Type_: **int32 (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### EngineIdentificationNumber

> Engine identification number. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### EnginePowerhp

> Engine output power in horse power. null means that the value is unknown or not applicable for this type of engine. [Filter(eq;ge;le)]

_Type_: **int32 (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### EngineSizecc

> Engine size in cubic centimeters (cm3). null means that the value is unknown or not applicable for this type of engine (e.g. electric motors). [Filter(eq;ge;le)]

_Type_: **int32 (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### FuelCapacity

> Maximum fuel capacity of the engine or the battery in the fuel measurement unit.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### FuelCompsumption

> Average fuel consumption in the fuel measurement unit for 1 operational unit.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### FuelType

> Fuel type of the engine or the power source of the engine (Multilanguage) - e.g. diesel, benzine, electric, etc. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### IsActive

> True if the vehicle is still owned and managed by the enterprise. [Required] [Default(true)] (Introduced in version 18.2.100.0)

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### IssuingAuthority

> The country or state issuing the registration number. null (not recommended) means that the authority is unknown or not applicable. [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString) (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Make

> The name of the manufacturer of the vehicle. null means that the value is unknown. [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString) (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### ManufactureYear

> The year when the vehicle was manufactured or first registered - whichever is known. null means that the value is unknown. [Filter(eq;ge;le)]

_Type_: **int32 (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### MaximumSpeedKmH

> Maximum speed in km/h.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Model

> The model of the vehicle. [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString) (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

> Notes for this Vehicle.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PrimaryColor

> The primary color of the vehicle. null means that the value is unknown or not applicable. [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString) (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### SeatingPlacesCount

> Number of seating places, excluding driver. [Filter(eq;ge;le)]

_Type_: **int32 (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### StandingPlacesCount

> Number of standing places, if applicable.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### TechnicalMaximumLadenMassKg

> Maximum technically permissible laden mass in kg.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### TrainsetMaximumLadenMassKg

> Maximum permissible laden mass of a whole trainset, including the vehicle.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### VehicleIdentificationNumber

> VIN, aka Chassis number. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### VehicleMassKg

> Vehicle own mass in kg.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### VehicleRegistrationNumber

> The registration plate number. Can be numeric or alphanumeric code. It should be unique within the Issuing_Authority. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### VehicleType

> Type of vehicle - e.g. automobile, bus, etc. null means the value is unknown. [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString) (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### FuelMeasurementUnit

> The measurement unit in which the fuel is measured. E.g. liters for automobiles, Watt-hours for electrics, etc. null means unknown. [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### MaintenanceProfile

> When not null, specifies, that the vehicle should be maintained according to the specified profile. Assigning a profile creates plan assignments for the vehicle. Ultimately, the specific plan assignments are taken into consideration, when planning vehicle maintenance. The profile is only for conveniently assigning multiple plans. [Filter(multi eq)]

_Type_: **[Applications.Fleet.MaintenanceProfiles](Applications.Fleet.MaintenanceProfiles.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### OperationalMeasurementUnit

> The measurement unit in which the operation of the vehicle is measured. E.g. km for automobiles, hrs for airplanes, etc. null means that the unit is unknown. [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### OwnerParty

> Vehicle owner. [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Fleet.Vehicles erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Fleet.Vehicles erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Fleet.Vehicles erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_Vehicles?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_Vehicles?$top=10>

