# Table Acc_Voucher_Lines

Contains one debit or credit posting within an accounting voucher. Entity: Acc_Voucher_Lines

# Aggregate Hierarchy

* [Acc_Vouchers](Acc_Vouchers.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Voucher_Line_Id|`Guid`|`PK`, Readonly||
|Correspondance_No|`Int32`||The number of the correspondance group within the accounting voucher. For each correspondance group, the debits are equal to the credits. `Required` `Default(0)` |
|Correspondant_Amount|`Decimal?`|Readonly|The amount (in the currency of the correspondant line) to which the amount in this line is corresponding. This field has value only when the current line is corresponding to only one line (e.g. null means that the current line is corresponding to many lines). `ReadOnly` |
|Item_Key|`String`||The item (grouping) key for the account in the line. Account_Id + Item_Key - the smallest unit of calculation for account balance. `Filter(eq;like)` |
|Line_No|`Int32`||Consecutive number of the line within the voucher. `Required` |
|Rate_Divisor|`Decimal`||The divisor for conversion from Debit/Credit to base currency. `Required` `Default(1)` |
|Rate_Multiplier|`Decimal`||The multiplier for conversion from Debit/Credit to base currency. `Required` `Default(1)` |
