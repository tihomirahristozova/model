# Table Acc_Voucher_Correspondances

Obsolete. Not used. Entity: Acc_Voucher_Correspondances

# Aggregate Hierarchy

* [Acc_Vouchers](Acc_Vouchers.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Correspondance_Id|`Guid`|`PK`, Readonly||
|Amount_Base|`Decimal`||Obsolete. Not used. `Required` `Default(0)` |
|Credit_Amount|`Decimal`||Obsolete. Not used. `Required` `Default(0)` |
|Credit_Voucher_Line_Id|`Guid`||Obsolete. Not used. (The voucher line which contains the credited account). `Required` `Filter(multi eq)` |
|Debit_Amount|`Decimal`||Obsolete. Not used. `Required` `Default(0)` |
|Debit_Voucher_Line_Id|`Guid`||Obsolete. Not used. (The voucher line which contains the debited account). `Required` `Filter(multi eq)` |
