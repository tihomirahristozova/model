# Table Cash_Payment_Slip_Payment_Transactions_Templates

Contains options for generation of payment transactions. Each option set is assigned to specific generation route. Entity: Cash_Payment_Slip_Payment_Transactions_Templates (Introduced in version 19.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|CreateExpensePayments|`Boolean`||True if the generation creates payment transactions for Payment Slip Amounts with direction Expense. `Required` `Filter(eq)` |
|CreateIncomePayments|`Boolean`||True if the generation creates payment transactions for Payment Slip Amounts with direction Income. `Required` `Filter(eq)` |
