# Table Gen_Currency_Directory_Lines

Contains exchange rate for a currency against the main currency of currency directory. Entity: Gen_Currency_Directory_Lines

# Aggregate Hierarchy

* [Gen_Currency_Directories](Gen_Currency_Directories.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Currency_Directory_Line_Id|`Guid`|`PK`, Readonly||
|Rate_Divisor|`Decimal`||The divisor for conversion from From_Currency to Directory.To_Currency. `Required` `Default(1)` |
|Rate_Multiplier|`Decimal`||The multiplier for conversion from From_Currency to Directory.To_Currency. `Required` `Default(1)` |
