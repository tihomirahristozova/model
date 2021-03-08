# Table Gen_Measurement_Categories

Categories of measurement units. The units within a category are directly convertable to each other. Each category contains one base unit and unlimited number of derived units with fixed ratio to the base unit. Entity: Gen_Measurement_Categories

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Is_Default|`Boolean`||True=This category is the default category; false=otherwise. `Required` `Default(false)` `Filter(eq)` |
|Measurement_Category_Name|`MultilanguageString`||The name of this MeasurementCategory. `Required` `Filter(eq;like)` `ORD` |
