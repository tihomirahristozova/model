# Table Log_Transportation_Modes

Represents a mode of transportation, like water, air, road, etc. Entity: Log_Transportation_Modes

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Transportation_Mode_Id|`Guid`|`PK`, Readonly||
|Transportation_Mode_Code|`String`||Unique transportation mode code. `Required` `Filter(eq;like)` `ORD` |
|Transportation_Mode_Name|`String`||Multilanguage name of the mode of transportation. `Required` `Filter(eq;like)` |
|System_Icon|`String`||Icon, depicting the mode of transport. A=Air, W=Water, T=Train/Rail, R=Road, O=Other. `Required` `Default("O")` |
