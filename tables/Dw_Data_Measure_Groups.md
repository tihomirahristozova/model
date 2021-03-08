# Table Dw_Data_Measure_Groups

Contains the groups of measures in the general data warehouse. Entity: Dw_Data_Measure_Groups (Introduced in version 18.2)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Data_Measure_Group_Id|`Guid`|`PK`, Readonly||
|Data_Measure_Group_Code|`String`||Unique group code. `Required` `Filter(eq;like)` `ORD` |
|Data_Measure_Group_Name|`String`||Group name (multilanguage). `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this DataMeasureGroup. |
