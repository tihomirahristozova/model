# Table Exc_Measuring_Transactions

Transaction of product input or output, measured with specialized measuring device for excise purposes. Entity: Exc_Measuring_Transactions (Introduced in version 21.1.1.9)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Measuring_Transaction_Id|`Guid`|`PK`, Readonly||
|Alcohol_Degree|`Int32?`||For alcoholic products, contains the percentage of pure alcohol. null when the transaction is not for alcoholic products. `Filter(multi eq;ge;le)` |
|Alcohol_Density|`Int32?`||For alcoholic products, contains the average density for the whole transaction. The measurement unit is dependent on the applicable legislation. null for non-alcoholic products. `Filter(multi eq;ge;le)` |
|Alcohol_Temperature|`Int32?`||For alcoholic products, contains the temperature of the fluid, when Alcohol Degree was calculated. The measurement unit is dependent on the national regulation (usually Celsius). null for non-alcoholic products. `Filter(multi eq;ge;le)` |
|Direction|`Direction`|Allowed: `I`, `O`|The direction of the transaction - IN/OUT. `Required` |
|End_Time_Utc|`DateTime`||Ending time of the transaction (in UTC time). `Required` `Filter(eq;ge;le)` |
|Measuring_Device_Code|`String`||The code of the measuring device, used to measure the transaction. `Required` `Filter(multi eq;like)` `ORD` |
|Notes|`String`||Notes for this MeasuringTransaction. |
|Start_Time_Utc|`DateTime`||Starting time of the transaction (in UTC time). `Required` `Filter(eq;ge;le)` |
|Transaction_Number|`String`||Transaction number, unique for the measuring device. `Required` `Filter(multi eq;like)` |
