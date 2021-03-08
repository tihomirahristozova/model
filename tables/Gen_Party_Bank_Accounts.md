# Table Gen_Party_Bank_Accounts

The bank accounts of a party. Entity: Gen_Party_Bank_Accounts

# Aggregate Hierarchy

* [Gen_Parties](Gen_Parties.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Party_Bank_Account_Id|`Guid`|`PK`, Readonly||
|Bank_Account_Code|`String`||The code of the account, usually the IBAN code. `Required` `Filter(eq;like)` |
|Bank_Address|`MultilanguageString`||The address of the bank or the bank branch office. Required (not-null) only for own accounts for printing or exporting bank payments. |
|Bank_Branch_Name|`MultilanguageString`||The name of the branch office of the bank, where the account is located. Required (not-null) only for own accounts for printing or exporting bank payments. |
|Bank_Code|`String`||The code of the bank, usually the BIC code. `Filter(eq)` |
|Bank_Name|`MultilanguageString`||The full name of the bank. `Filter(like)` |
|Is_Default|`Boolean`||True if the this is the default account for the party. Only one default per party is allowed. `Required` `Default(false)` `Filter(eq)` |
|Notes|`String`||Notes for this PartyBankAccount. |
