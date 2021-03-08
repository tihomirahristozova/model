# Table Dw_Data_Values

The actual values in the general data warehouse. Entity: Dw_Data_Values (Introduced in version 18.2)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Data_Value_Id|`Guid`|`PK`, Readonly||
|Actual_Value|`Decimal`||Accumulates actual value for the measure. `Required` `Default(0)` `Filter(eq)` |
|Date|`DateTime`||The date for which the measure is recorded. All records with dates within each period are summed. `Required` `Filter(eq;ge;le)` |
|Target_Value|`Decimal`||Accumulates target value for the measure. `Required` `Default(0)` `Filter(eq)` |
