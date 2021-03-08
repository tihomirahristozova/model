# Table Log_Carriers

Represents a carrier agreement. One actual carrier can have different agreements over time or with different enterprise companies. Entity: Log_Carriers

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Carrier_Id|`Guid`|`PK`, Readonly||
|Agreement_End_Date|`DateTime?`||The ending date of the agreement with this carrier. null for agreements which are still active. `Filter(eq;ge;le)` |
|Agreement_Start_Date|`DateTime`||The start date of the agreement with this carrier. `Required` `Default(Today)` `Filter(eq;ge;le)` |
|Code|`String`||Unique carrier code (or call sign). The code is unique within all enterprise companies. `Required` `Filter(eq;like)` `ORD` |
|Is_Active|`Boolean`||Specifies whether the carrier agreement is active. `Required` `Default(true)` `Filter(eq)` |
|Notes|`String`||Notes for this Carrier. |
