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


Vehicle_Id


Unique vehicle id


Unique vehicle id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Vehicle_Id](Fleet_Vehicles.md#vehicle_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Vehicle_Type


Vehicle_Type


Type of vehicle - e.g. automobile, bus, etc. NULL means the value is unknown


Type of vehicle - e.g. automobile, bus, etc. NULL means the value is unknown

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Vehicle_Type](Fleet_Vehicles.md#vehicle_type)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|yes|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Make


Make


The name of the manufacturer of the vehicle. NULL means that the value is unknown


The name of the manufacturer of the vehicle. NULL means that the value is unknown

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Make](Fleet_Vehicles.md#make)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|yes|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Model


Model


The model of the vehicle


The model of the vehicle

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Model](Fleet_Vehicles.md#model)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|yes|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Vehicle_Registration_Number


Vehicle_Registration_Number


The registration plate number. Can be numeric or alphanumeric code. It should be unique within the Issuing_Authority


The registration plate number. Can be numeric or alphanumeric code. It should be unique within the Issuing_Authority

| Property | Value |
| - | - |
|Type|nvarchar(16)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Vehicle_Registration_Number](Fleet_Vehicles.md#vehicle_registration_number)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|16|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Issuing_Authority


Issuing_Authority


The country or state issuing the registration number. NULL (not recommended) means that the authority is unknown or not applicable


The country or state issuing the registration number. NULL (not recommended) means that the authority is unknown or not applicable

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Issuing_Authority](Fleet_Vehicles.md#issuing_authority)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|yes|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Primary_Color


Primary_Color


The primary color of the vehicle. NULL means that the value is unknown or not applicable


The primary color of the vehicle. NULL means that the value is unknown or not applicable

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Primary_Color](Fleet_Vehicles.md#primary_color)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|yes|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Manufacture_Year


Manufacture_Year


The year when the vehicle was manufactured or first registered - whichever is known. NULL means that the value is unknown


The year when the vehicle was manufactured or first registered - whichever is known. NULL means that the value is unknown

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Manufacture_Year](Fleet_Vehicles.md#manufacture_year)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|GreaterThanOrLessThan|None|no|no|

### Engine_Size_cc


Engine_Size_cc


Engine size in cubic centimeters (cm3). NULL means that the value is unknown or not applicable for this type of engine (e.g. electric motors)


Engine size in cubic centimeters (cm3). NULL means that the value is unknown or not applicable for this type of engine (e.g. electric motors)

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Engine_Size_cc](Fleet_Vehicles.md#engine_size_cc)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|GreaterThanOrLessThan|None|no|no|

### Engine_Power_hp


Engine_Power_hp


Engine output power in horse power. NULL means that the value is unknown or not applicable for this type of engine


Engine output power in horse power. NULL means that the value is unknown or not applicable for this type of engine

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Engine_Power_hp](Fleet_Vehicles.md#engine_power_hp)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|GreaterThanOrLessThan|None|no|no|

### Engine_Identification_Number


Engine_Identification_Number


Engine identification number


Engine identification number

| Property | Value |
| - | - |
|Type|nvarchar(20)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Engine_Identification_Number](Fleet_Vehicles.md#engine_identification_number)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|20|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Vehicle_Identification_Number


Vehicle_Identification_Number


VIN, aka Chassis number


VIN, aka Chassis number

| Property | Value |
| - | - |
|Type|nvarchar(20)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Vehicle_Identification_Number](Fleet_Vehicles.md#vehicle_identification_number)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|20|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Seating_Places_Count


Seating_Places_Count


Number of seating places, excluding driver


Number of seating places, excluding driver

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Seating_Places_Count](Fleet_Vehicles.md#seating_places_count)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|GreaterThanOrLessThan|None|no|no|

### Crew_Count


Crew_Count


Crew members count. For road vehicles = 1; for trailers, coaches and wagons =0; air and water vehicles may have higher counts


Crew members count. For road vehicles = 1; for trailers, coaches and wagons =0; air and water vehicles may have higher counts

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|1|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Crew_Count](Fleet_Vehicles.md#crew_count)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|GreaterThanOrLessThan|None|no|no|

### Standing_Places_Count


Standing_Places_Count


Number of standing places, if applicable


Number of standing places, if applicable

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Standing_Places_Count](Fleet_Vehicles.md#standing_places_count)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Vehicle_Mass_Kg


Vehicle_Mass_Kg


Vehicle own mass in kg


Vehicle own mass in kg

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Vehicle_Mass_Kg](Fleet_Vehicles.md#vehicle_mass_kg)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Technical_Maximum_Laden_Mass_Kg


Technical_Maximum_Laden_Mass_Kg


Maximum technically permissible laden mass in kg


Maximum technically permissible laden mass in kg

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Technical_Maximum_Laden_Mass_Kg](Fleet_Vehicles.md#technical_maximum_laden_mass_kg)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Authority_Maximum_Laden_Mass_Kg


Authority_Maximum_Laden_Mass_Kg


Maximum permissible laden mass, as determined by the registration authority


Maximum permissible laden mass, as determined by the registration authority

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Authority_Maximum_Laden_Mass_Kg](Fleet_Vehicles.md#authority_maximum_laden_mass_kg)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Trainset_Maximum_Laden_Mass_Kg


Trainset_Maximum_Laden_Mass_Kg


Maximum permissible laden mass of a whole trainset, including the vehicle


Maximum permissible laden mass of a whole trainset, including the vehicle

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Trainset_Maximum_Laden_Mass_Kg](Fleet_Vehicles.md#trainset_maximum_laden_mass_kg)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Fuel_Type


Fuel_Type


Fuel type of the engine or the power source of the engine (Multilanguage) - e.g. diesel, benzine, electric, etc.


Fuel type of the engine or the power source of the engine (Multilanguage) - e.g. diesel, benzine, electric, etc.

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Fuel_Type](Fleet_Vehicles.md#fuel_type)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|yes|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Fuel_Capacity


Fuel_Capacity


Maximum fuel capacity of the engine or the battery in the fuel measurement unit


Maximum fuel capacity of the engine or the battery in the fuel measurement unit

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Fuel_Capacity](Fleet_Vehicles.md#fuel_capacity)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Fuel_Compsumption


Fuel_Compsumption


Average fuel consumption in the fuel measurement unit for 1 operational unit


Average fuel consumption in the fuel measurement unit for 1 operational unit

| Property | Value |
| - | - |
|Type|decimal(7, 1)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Fuel_Compsumption](Fleet_Vehicles.md#fuel_compsumption)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Maximum_Speed_KmH


Maximum_Speed_KmH


Maximum speed in km/h


Maximum speed in km/h

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Maximum_Speed_KmH](Fleet_Vehicles.md#maximum_speed_kmh)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Owner_Party_Id


Owner_Party_Id


Vehicle owner


Vehicle owner

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Parties](Gen_Parties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Owner_Party_Id](Fleet_Vehicles.md#owner_party_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Notes](Fleet_Vehicles.md#notes)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Operational_Measurement_Unit_Id


Operational_Measurement_Unit_Id


The measurement unit in which the operation of the vehicle is measured. E.g. km for automobiles, hrs for airplanes, etc. NULL means that the unit is unknown


The measurement unit in which the operation of the vehicle is measured. E.g. km for automobiles, hrs for airplanes, etc. NULL means that the unit is unknown

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Measurement_Units](Gen_Measurement_Units.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Operational_Measurement_Unit_Id](Fleet_Vehicles.md#operational_measurement_unit_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Fuel_Measurement_Unit_Id


Fuel_Measurement_Unit_Id


The measurement unit in which the fuel is measured. E.g. liters for automobiles, Watt-hours for electrics, etc. NULL means unknown


The measurement unit in which the fuel is measured. E.g. liters for automobiles, Watt-hours for electrics, etc. NULL means unknown

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Measurement_Units](Gen_Measurement_Units.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Fuel_Measurement_Unit_Id](Fleet_Vehicles.md#fuel_measurement_unit_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Row_Version](Fleet_Vehicles.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Maintenance_Profile_Id


Maintenance_Profile_Id


When not null, specifies, that the vehicle should be maintained according to the specified profile. Assigning a profile creates plan assignments for the vehicle. Ultimately, the specific plan assignments are taken into consideration, when planning vehicle maintenance. The profile is only for conveniently assigning multiple plans.


When not null, specifies, that the vehicle should be maintained according to the specified profile. Assigning a profile creates plan assignments for the vehicle. Ultimately, the specific plan assignments are taken into consideration, when planning vehicle maintenance. The profile is only for conveniently assigning multiple plans.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Fleet_Maintenance_Profiles](Fleet_Maintenance_Profiles.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Maintenance_Profile_Id](Fleet_Vehicles.md#maintenance_profile_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Is_Active


Is_Active


True if the vehicle is still owned and managed by the enterprise.


True if the vehicle is still owned and managed by the enterprise.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|True|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Is_Active](Fleet_Vehicles.md#is_active)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Active_From


Active_From


The date and time, when the vehicle has been purchased or started to be managed. Null when the date and time are unknown.


The date and time, when the vehicle has been purchased or started to be managed. Null when the date and time are unknown.

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Active_From](Fleet_Vehicles.md#active_from)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Active_Till


Active_Till


The date and time, when the vehicle has been sold or has stopped being managed. Null when the date and time are unknown.


The date and time, when the vehicle has been sold or has stopped being managed. Null when the date and time are unknown.

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicles](Fleet_Vehicles.md).[Active_Till](Fleet_Vehicles.md#active_till)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


