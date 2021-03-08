# Table Acc_Financial_Statements

Contains the user-defined financial statement definitions. Entity: Acc_Financial_Statements

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Financial_Statement_Id|`Guid`|`PK`, Readonly||
|Financial_Statement_Code|`String`||Unique identifying code of the financial statement. `Required` `Filter(eq;like)` `ORD` |
|Financial_Statement_Name|`MultilanguageString`||Name of the financial statement. `Required` `Filter(eq;like)` |
