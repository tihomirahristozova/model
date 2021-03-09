# Table Fleet_Vehicles

Contains vehicle definitions. Entity: Fleet_Vehicles

## Summary

| Name | Type | Description |
| - | - | --- |
|[Vehicle_Id](#vehicle_id)|`uniqueidentifier` `PK`|Unique vehicle id|
|[Vehicle_Type](#vehicle_type)|`nvarchar(64)` `ML`|Type of vehicle - e.g. automobile, bus, etc. NULL means the value is unknown|
|[Make](#make)|`nvarchar(64)` `ML`|The name of the manufacturer of the vehicle. NULL means that the value is unknown|
|[Model](#model)|`nvarchar(64)` `ML`|The model of the vehicle|
|[Vehicle_Registration_Number](#vehicle_registration_number)|`nvarchar(16)` |The registration plate number. Can be numeric or alphanumeric code. It should be unique within the Issuing_Authority|
|[Issuing_Authority](#issuing_authority)|`nvarchar(64)` `ML`|The country or state issuing the registration number. NULL (not recommended) means that the authority is unknown or not applicable|
|[Primary_Color](#primary_color)|`nvarchar(64)` `ML`|The primary color of the vehicle. NULL means that the value is unknown or not applicable|
|[Manufacture_Year](#manufacture_year)|`int` |The year when the vehicle was manufactured or first registered - whichever is known. NULL means that the value is unknown|
|[Engine_Size_cc](#engine_size_cc)|`int` |Engine size in cubic centimeters (cm3). NULL means that the value is unknown or not applicable for this type of engine (e.g. electric motors)|
|[Engine_Power_hp](#engine_power_hp)|`int` |Engine output power in horse power. NULL means that the value is unknown or not applicable for this type of engine|
|[Engine_Identification_Number](#engine_identification_number)|`nvarchar(20)` |Engine identification number|
|[Vehicle_Identification_Number](#vehicle_identification_number)|`nvarchar(20)` |VIN, aka Chassis number|
|[Seating_Places_Count](#seating_places_count)|`int` |Number of seating places, excluding driver|
|[Crew_Count](#crew_count)|`int` |Crew members count. For road vehicles = 1; for trailers, coaches and wagons =0; air and water vehicles may have higher counts|
|[Standing_Places_Count](#standing_places_count)|`int` |Number of standing places, if applicable|
|[Vehicle_Mass_Kg](#vehicle_mass_kg)|`int` |Vehicle own mass in kg|
|[Technical_Maximum_Laden_Mass_Kg](#technical_maximum_laden_mass_kg)|`int` |Maximum technically permissible laden mass in kg|
|[Authority_Maximum_Laden_Mass_Kg](#authority_maximum_laden_mass_kg)|`int` |Maximum permissible laden mass, as determined by the registration authority|
|[Trainset_Maximum_Laden_Mass_Kg](#trainset_maximum_laden_mass_kg)|`int` |Maximum permissible laden mass of a whole trainset, including the vehicle|
|[Fuel_Type](#fuel_type)|`nvarchar(64)` |Fuel type of the engine or the power source of the engine (Multilanguage) - e.g. diesel, benzine, electric, etc.|
|[Fuel_Capacity](#fuel_capacity)|`int` |Maximum fuel capacity of the engine or the battery in the fuel measurement unit|
|[Fuel_Compsumption](#fuel_compsumption)|`decimal(7, 1)` |Average fuel consumption in the fuel measurement unit for 1 operational unit|
|[Maximum_Speed_KmH](#maximum_speed_kmh)|`int` |Maximum speed in km/h|
|[Owner_Party_Id](#owner_party_id)|`uniqueidentifier` |Vehicle owner|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Operational_Measurement_Unit_Id](#operational_measurement_unit_id)|`uniqueidentifier` |The measurement unit in which the operation of the vehicle is measured. E.g. km for automobiles, hrs for airplanes, etc. NULL means that the unit is unknown|
|[Fuel_Measurement_Unit_Id](#fuel_measurement_unit_id)|`uniqueidentifier` |The measurement unit in which the fuel is measured. E.g. liters for automobiles, Watt-hours for electrics, etc. NULL means unknown|
|[Row_Version](#row_version)|`timestamp` ||
|[Maintenance_Profile_Id](#maintenance_profile_id)|`uniqueidentifier` |When not null, specifies, that the vehicle should be maintained according to the specified profile. Assigning a profile creates plan assignments for the vehicle. Ultimately, the specific plan assignments are taken into consideration, when planning vehicle maintenance. The profile is only for conveniently assigning multiple plans.|
|[Is_Active](#is_active)|`bit` |True if the vehicle is still owned and managed by the enterprise.|
|[Active_From](#active_from)|`datetime` |The date and time, when the vehicle has been purchased or started to be managed. Null when the date and time are unknown.|
|[Active_Till](#active_till)|`datetime` |The date and time, when the vehicle has been sold or has stopped being managed. Null when the date and time are unknown.|

## Columns

### Vehicle_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Vehicle_Type

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Make

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Model

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Vehicle_Registration_Number

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Issuing_Authority

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Primary_Color

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Manufacture_Year

| Property | Value |
| - | - |
|Type|int|

### Engine_Size_cc

| Property | Value |
| - | - |
|Type|int|

### Engine_Power_hp

| Property | Value |
| - | - |
|Type|int|

### Engine_Identification_Number

| Property | Value |
| - | - |
|Type|nvarchar(20)|

### Vehicle_Identification_Number

| Property | Value |
| - | - |
|Type|nvarchar(20)|

### Seating_Places_Count

| Property | Value |
| - | - |
|Type|int|

### Crew_Count

| Property | Value |
| - | - |
|Type|int|

### Standing_Places_Count

| Property | Value |
| - | - |
|Type|int|

### Vehicle_Mass_Kg

| Property | Value |
| - | - |
|Type|int|

### Technical_Maximum_Laden_Mass_Kg

| Property | Value |
| - | - |
|Type|int|

### Authority_Maximum_Laden_Mass_Kg

| Property | Value |
| - | - |
|Type|int|

### Trainset_Maximum_Laden_Mass_Kg

| Property | Value |
| - | - |
|Type|int|

### Fuel_Type

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Fuel_Capacity

| Property | Value |
| - | - |
|Type|int|

### Fuel_Compsumption

| Property | Value |
| - | - |
|Type|decimal(7, 1)|

### Maximum_Speed_KmH

| Property | Value |
| - | - |
|Type|int|

### Owner_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Operational_Measurement_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Fuel_Measurement_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Maintenance_Profile_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Active_From

| Property | Value |
| - | - |
|Type|datetime|

### Active_Till

| Property | Value |
| - | - |
|Type|datetime|


