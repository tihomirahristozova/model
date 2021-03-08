# Table Dw_Data_Measures

Contains the data measures of the General data warehouse. Entity: Dw_Data_Measures (Introduced in version 18.2)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Data_Measure_Id|`Guid`|`PK`, Readonly||
|Data_Measure_Code|`String`||Unique measure code. `Required` `Filter(eq;like)` `ORD` |
|Green_Zone_Spread_Percent|`Decimal`||The plus or minus percent, by which the goal can be missed, but still considered achieved. `Required` `Default(0.2)` `Filter(eq)` |
|Horizontal_Trend_Spread_Percent|`Decimal`||The change in percents, which is considered neutral. Higher positive/negative changes are considered positive/negative trends. `Required` `Default(0.01)` `Filter(eq)` |
|Data_Measure_Name|`String`||The name of the measure (multilanguage). `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this DataMeasure. |
|Period|`Period`|Allowed: `D`, `M`, `Q`, `Y`|The period for which the data is collected. D=Day, M=Month, Q=Quarter, Y=Year. `Required` `Default("Q")` `Filter(eq)` |
