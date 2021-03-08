# Table Acc_Accounts

Contains the leaf level of the chart of accounts. Entity: Acc_Accounts

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Account_Id|`Guid`|`PK`, Readonly||
|Account_Full_Number|`String`|Readonly|The full number of the account, unique among all accounts. It consists of the group number, concatenated with the account number. `Required` `Filter(like)` `ReadOnly` |
|Currency_Valuation_Method|`CurrencyValuationMethod`|Allowed: `ACB`, `DCD`, `BRD`|Method for base currency valuation of non base currency amounts. ACB = Account_Current_Balance, DCD = Document_Currency_Directory, BRD=Balance_Reference_Document. `Required` `Default("ACB")` |
|Description|`String`||The description of this Account. |
|Discontinued|`Boolean`||True means that the account won't be used any more and should not appear in combo boxes. `Required` `Default(false)` `Filter(eq)` |
|Account_Name|`MultilanguageString`||The account name. `Required` `Filter(like)` |
|Account_Number|`String`||The number of the account, unique within the account group. `Required` `Filter(like)` |
