# Table Acc_Account_Required_Properties

Defines the required properties for new vouchers, for each account. Entity: Acc_Account_Required_Properties

# Aggregate Hierarchy

* [Acc_Accounts](Acc_Accounts.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Account_Required_Property_Id|`Guid`|`PK`, Readonly||
|Key_Order|`Int32`||The key order determines in which order the values and descriptions of the properties will form the item (grouping) key and description. `Required` |
|Key_Property|`Boolean`||Key properties particiate in forming the grouping key, which is the smallest unit of calculation for account balance. Non-key properties simply serve for comment and clarification purposes. `Required` `Default(true)` `Filter(eq)` |
