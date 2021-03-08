# Table Gen_Document_Amount_Types

Represents the different types of additional amounts which are calculated for the documents. Entity: Gen_Document_Amount_Types

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Document_Amount_Type_Id|`Guid`|`PK`, Readonly||
|Add_To_Customer|`Boolean`||True means that the amount will be charged to the primary customer of the document. `Required` `Default(true)` |
|Add_To_Line|`Boolean`||True means that the resulting amount will be added to the amount of each respective line. `Required` `Default(true)` |
|Allowed_Directions|`AllowedDirections?`|Allowed: `0`, `1`, `-1`|Specifies condition for the sign of the allowed values for input percent or amount ​​that can be set in the documents. `Default(0)` |
|Amount_Input_Allowed|`Boolean`||True when the user is allowed to input fixed amount for distribution. `Required` `Default(false)` `Filter(eq)` |
|Amount_Type_Code|`String`||A code that can be used to uniquely identify the additional amount. Can also be used for sorting purposes. `Required` `Filter(multi eq)` `ORD` |
|Amount_Type_Name|`MultilanguageString`||The name of the amount type. `Required` `Filter(like)` `ORD` |
|Base_On_Lines|`Boolean`||True means that the percentages will be applied over lines plus dependant amounts; false means only dependant amounts. `Required` `Default(true)` |
|Default_Percent|`Decimal?`||Default percent for amounts for which percent input is allowed; null otherwise. |
|Description|`String`||The description of this DocumentAmountType. |
|Distribute_By|`DistributeBy`|Allowed: `AMOUNT`, `MEASUREMENT`, `PRODUCT DEFINITION`|Specifies how the amount will be distributed among the document lines. Valid values are: ('AMOUNT','MEASUREMENT','PRODUCT DEFINITION'). `Required` `Default("AMOUNT")` `Filter(eq)` |
|Is_Active|`Boolean`||True when the amount type is active for new records; false - otherwise. `Required` `Default(true)` `Filter(eq)` |
|Percent_Input_Allowed|`Boolean`||True when the user is allowed to input percent of total for distribution. `Required` `Default(true)` `Filter(eq)` |
|Round_Scale|`Int32?`||The amounts should be rounded with the specified number of digits after the decimal point. null means to use the currency default. |
|Unit_Amount_Input_Allowed|`Boolean`||Specifies whether the user is allowed to input fixed unit amount for the calculation of the amount. `Required` `Default(false)` `Filter(eq)` |
