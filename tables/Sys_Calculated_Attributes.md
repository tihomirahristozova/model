# Table Sys_Calculated_Attributes

User-defined read-only calculated attribute. Entity: Sys_Calculated_Attributes

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Calculated_Attribute_Id|`Guid`|`PK`, Readonly||
|Caption|`MultilanguageString`||The multi-language caption, used to display the attribute. `Required` |
|Is_Active|`Boolean`||True if the attribute is activated and added to the repository. `Required` `Default(false)` |
|Name|`String`||The unique name of the attribute within the repository. `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this CalculatedAttribute. |
|Repository_Name|`String`||The repository, for which the attribute is defined. `Required` `Filter(multi eq)` `ORD` |
|Starting_Expression_No|`Int32`||The expression, from which the calculation starts. The result of the expression gives the value of the calculated attribute. `Required` `Default(10)` |
