# Table Cash_Payment_Accounts

Payment accounts are cash, bank and other accounts, which are used in payments. Payment accounts are frequently used as analytical dimensions (properties) for general ledger accounts. Entity: Cash_Payment_Accounts

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Payment_Account_Id|`Guid`|`PK`, Readonly||
|Payment_Account_Code|`String`||The unique code of the PaymentAccount. `Required` `Filter(eq;like)` `ORD` |
|Is_Active|`Boolean`||Indicates wheather the payment account is currently used (active). `Required` `Default(true)` `Filter(eq)` |
|Payment_Account_Name|`MultilanguageString`||The name of this PaymentAccount. `Required` `Filter(like)` |
