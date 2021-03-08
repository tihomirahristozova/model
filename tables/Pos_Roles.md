# Table Pos_Roles

Represents a role, which can be assigned to POS operators (like Cashier, Manager, etc.). The role indicates the operations, which are allowed to be performed by the operators. Entity: Pos_Roles (Introduced in version 19.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Pos_Role_Id|`Guid`|`PK`, Readonly||
|Can_Process_Minus_Sales|`Boolean`||Indicates whether the role is allowed to process minus (qty and/or value) sales. `Required` `Default(false)` `Filter(multi eq)` |
|Can_Void_Sales|`Boolean`||Indicates whether this role can void sales orders. `Required` `Default(false)` `Filter(multi eq)` |
|Pos_Role_Code|`String`||Unique role code. `Required` `Filter(multi eq;like)` `ORD` |
|Pos_Role_Name|`MultilanguageString`||Multi-language name of the POS role. `Required` `Filter(multi eq;like)` |
