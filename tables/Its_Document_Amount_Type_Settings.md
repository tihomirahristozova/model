# Table Its_Document_Amount_Type_Settings

Specifies the additional amounts, which are added to the invoiced and statistical values. Entity: Its_Document_Amount_Type_Settings

# Aggregate Hierarchy

* [Gen_Document_Amount_Types](Gen_Document_Amount_Types.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Document_Amount_Type_Setting_Id|`Guid`|`PK`, Readonly||
|Add_To_Invoiced_Value|`Boolean`||True= to add the amount to the invoiced value, false=otherwise. `Required` `Default(false)` |
|Add_To_Statistical_Value|`Boolean`||True= to add the amount to the statistical value, false=otherwise. `Required` `Default(false)` |
