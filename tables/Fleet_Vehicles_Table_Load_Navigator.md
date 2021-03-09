# Query Fleet_Vehicles_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Vehicle_Id](#vehicle_id)|`uniqueidentifier` `PK`||
|[Vehicle_Type](#vehicle_type)|`nvarchar` `ML`||
|[Make](#make)|`nvarchar` `ML`||
|[Model](#model)|`nvarchar` `ML`||
|[Vehicle_Registration_Number](#vehicle_registration_number)|`nvarchar` ||
|[Issuing_Authority](#issuing_authority)|`nvarchar` `ML`||
|[Primary_Color](#primary_color)|`nvarchar` `ML`||
|[Manufacture_Year](#manufacture_year)|`int` ||
|[Engine_Size_cc](#engine_size_cc)|`int` ||
|[Engine_Power_hp](#engine_power_hp)|`int` ||
|[Engine_Identification_Number](#engine_identification_number)|`nvarchar` ||
|[Vehicle_Identification_Number](#vehicle_identification_number)|`nvarchar` ||
|[Seating_Places_Count](#seating_places_count)|`int` ||
|[Crew_Count](#crew_count)|`int` ||
|[Standing_Places_Count](#standing_places_count)|`int` ||
|[Vehicle_Mass_Kg](#vehicle_mass_kg)|`int` ||
|[Technical_Maximum_Laden_Mass_Kg](#technical_maximum_laden_mass_kg)|`int` ||
|[Authority_Maximum_Laden_Mass_Kg](#authority_maximum_laden_mass_kg)|`int` ||
|[Trainset_Maximum_Laden_Mass_Kg](#trainset_maximum_laden_mass_kg)|`int` ||
|[Fuel_Type](#fuel_type)|`nvarchar` ||
|[Fuel_Capacity](#fuel_capacity)|`int` ||
|[Fuel_Compsumption](#fuel_compsumption)|`decimal(0, 0)` ||
|[Maximum_Speed_KmH](#maximum_speed_kmh)|`int` ||
|[Owner_Party_Id](#owner_party_id)|`uniqueidentifier` ||
|[Notes](#notes)|`nvarchar` ||
|[Operational_Measurement_Unit_Id](#operational_measurement_unit_id)|`uniqueidentifier` ||
|[Fuel_Measurement_Unit_Id](#fuel_measurement_unit_id)|`uniqueidentifier` ||
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
|Type|nvarchar|

### Make

| Property | Value |
| - | - |
|Type|nvarchar|

### Model

| Property | Value |
| - | - |
|Type|nvarchar|

### Vehicle_Registration_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Issuing_Authority

| Property | Value |
| - | - |
|Type|nvarchar|

### Primary_Color

| Property | Value |
| - | - |
|Type|nvarchar|

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
|Type|nvarchar|

### Vehicle_Identification_Number

| Property | Value |
| - | - |
|Type|nvarchar|

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
|Type|nvarchar|

### Fuel_Capacity

| Property | Value |
| - | - |
|Type|int|

### Fuel_Compsumption

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

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
|Type|nvarchar|

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


