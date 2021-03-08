# Table Fleet_Vehicles

Contains vehicle definitions. Entity: Fleet_Vehicles

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Vehicle_Id|`Guid`|`PK`, Readonly||
|Active_From|`DateTime?`||The date and time, when the vehicle has been purchased or started to be managed. Null when the date and time are unknown. `Introduced in version 18.2` |
|Active_Till|`DateTime?`||The date and time, when the vehicle has been sold or has stopped being managed. Null when the date and time are unknown. `Introduced in version 18.2` |
|Authority_Maximum_Laden_Mass_Kg|`Int32?`||Maximum permissible laden mass, as determined by the registration authority. |
|Crew_Count|`Int32?`||Crew members count. For road vehicles = 1; for trailers, coaches and wagons =0; air and water vehicles may have higher counts. `Default(1)` `Filter(eq;ge;le)` |
|Engine_Identification_Number|`String`||Engine identification number. `Filter(eq;like)` |
|Engine_Power_hp|`Int32?`||Engine output power in horse power. null means that the value is unknown or not applicable for this type of engine. `Filter(eq;ge;le)` |
|Engine_Size_cc|`Int32?`||Engine size in cubic centimeters (cm3). null means that the value is unknown or not applicable for this type of engine (e.g. electric motors). `Filter(eq;ge;le)` |
|Fuel_Capacity|`Int32?`||Maximum fuel capacity of the engine or the battery in the fuel measurement unit. |
|Fuel_Compsumption|`Decimal?`||Average fuel consumption in the fuel measurement unit for 1 operational unit. |
|Fuel_Type|`String`||Fuel type of the engine or the power source of the engine (Multilanguage) - e.g. diesel, benzine, electric, etc. `Filter(eq;like)` |
|Is_Active|`Boolean`||True if the vehicle is still owned and managed by the enterprise. `Required` `Default(true)` `Introduced in version 18.2` |
|Issuing_Authority|`MultilanguageString`||The country or state issuing the registration number. null (not recommended) means that the authority is unknown or not applicable. `Filter(eq;like)` |
|Make|`MultilanguageString`||The name of the manufacturer of the vehicle. null means that the value is unknown. `Filter(eq;like)` |
|Manufacture_Year|`Int32?`||The year when the vehicle was manufactured or first registered - whichever is known. null means that the value is unknown. `Filter(eq;ge;le)` |
|Maximum_Speed_KmH|`Int32?`||Maximum speed in km/h. |
|Model|`MultilanguageString`||The model of the vehicle. `Filter(eq;like)` |
|Notes|`String`||Notes for this Vehicle. |
|Primary_Color|`MultilanguageString`||The primary color of the vehicle. null means that the value is unknown or not applicable. `Filter(eq;like)` |
|Seating_Places_Count|`Int32?`||Number of seating places, excluding driver. `Filter(eq;ge;le)` |
|Standing_Places_Count|`Int32?`||Number of standing places, if applicable. |
|Technical_Maximum_Laden_Mass_Kg|`Int32?`||Maximum technically permissible laden mass in kg. |
|Trainset_Maximum_Laden_Mass_Kg|`Int32?`||Maximum permissible laden mass of a whole trainset, including the vehicle. |
|Vehicle_Identification_Number|`String`||VIN, aka Chassis number. `Filter(eq;like)` |
|Vehicle_Mass_Kg|`Int32?`||Vehicle own mass in kg. |
|Vehicle_Registration_Number|`String`||The registration plate number. Can be numeric or alphanumeric code. It should be unique within the Issuing_Authority. `Required` `Filter(eq;like)` |
|Vehicle_Type|`MultilanguageString`||Type of vehicle - e.g. automobile, bus, etc. null means the value is unknown. `Filter(eq;like)` |
