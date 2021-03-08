# Table Cash_Payment_Transaction_Lines

Contains the distibution of the payments' amounts among the source payment orders. Entity: Cash_Payment_Transaction_Lines

# Aggregate Hierarchy

* [Cash_Payment_Transactions](Cash_Payment_Transactions.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Payment_Transaction_Line_Id|`Guid`|`PK`, Readonly||
|Allow_Overpayment|`Boolean`||True-Allows overpayment for the payment order; false=Does not allow (default). `Required` `Default(false)` |
|Notes|`String`||Notes for this PaymentTransactionLine. |
