# Table Log_Logistic_Units

Composition of products established for transport and/or storage which needs to be managed through the supply chain. Entity: Log_Logistic_Units (Introduced in version 21.1.0.77)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Logistic_Unit_Id|`Guid`|`PK`, Readonly||
|Expected_Weight|`Decimal?`||Expected weight in KG. Used for planning purposes. null means unknown. `Filter(eq;ge;le)` |
|Measured_Weight|`Decimal?`||Actual measured weight of the unit in KG. null means unknown. `Filter(eq;ge;le)` |
|Notes|`String`||Notes for this LogisticUnit. `Filter(like)` |
|Serial_Code|`String`||Unique serial code of the logistic unit. If GS1 coding is used, this is the SSCC. `Required` `Filter(multi eq;like)` `ORD` |
