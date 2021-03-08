# Table Gen_Measurement_Units

Contains all measurement units, grouped in categories. Each category has one base unit (with ratio 1/1) and unlimited number of derived units with fixed ratio to the base unit. Entity: Gen_Measurement_Units

# Aggregate Hierarchy

* [Gen_Measurement_Categories](Gen_Measurement_Categories.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Measurement_Unit_Code|`String`||When not null, contains unique measurement unit code. `Filter(eq;like)` `ORD` |
|Description|`MultilanguageString`||Full multi-language description of the measurement unit. |
|Divisor|`Decimal`||Divisor of the relative value of the measurement unit against other units (divisor when converting to base). `Required` `Default(1)` |
|Is_Default_Unit|`Boolean`||True if this measurement unit is the default measurement unit within the category. There can be only one default measurement unit within a category. `Required` `Default(false)` `Filter(eq)` |
|Multiplier|`Decimal`||Multiplier of the relative value of the measurement unit against other units (multiplier when converting to base). `Required` `Default(1)` |
|Measurement_Unit_Name|`MultilanguageString`||Name of the measurement unit. `Required` `Filter(eq;like)` `ORD` |
|System_Unit|`SystemUnit?`|Allowed: `G`, `H`, `L`, `N`, `P`, `V`, `W`, `T`|Not null only when this is one of the system measurement units. N=NetKG; G=GrossKG; V=VolumeL; H=HeightM; W=WidthM, L=LengthM, P=Piece, T=TimeH. `Filter(eq;like)` |
