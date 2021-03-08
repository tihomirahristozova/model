# Table Sys_Default_Values

Contains user-specified default values for columns in data entry forms. Entity: Sys_Default_Values

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Default_Value_Id|`Guid`|`PK`, Readonly||
|Column_Name|`String`||The column for which the default is specified. `Required` `Filter(eq)` |
|Condition_Form_Name|`String`||If not null specifies that the default should be applied only if Form_Name equals the specified value. `Filter(eq)` `ORD` |
|Condition_User_Login|`String`||If not null specifies that the default should be applied only if User_Login equals this value. `Filter(eq)` |
|Condition_User_Machine|`String`||If not null specifies that the default should be applied only if User_Machine equals this value. `Filter(eq)` |
|Default_Value|`String`||The default value for Column_Name. Should be applied only if the other conditions are met. null specifies null default. |
|Panel_Name|`String`||When not null, specifies the panel for which the default value applies. `Filter(eq;like)` |
|Table_Name|`String`||The table, containing the column for which the default value is specified. `Filter(eq)` |
