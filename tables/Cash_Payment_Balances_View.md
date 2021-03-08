# Table Cash_Payment_Balances_View

Represents the payment orders with their covered amounts. Entity: Cash_Payment_Balances_View

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Is_Invoiced|`Boolean`||When Is_Invoiced = true, then in the view results will be included only the Payment Orders which do have a RefInvoiceDocument. If Is_Invoiced = false, then in the view results will be included only the Payment Orders which do NOT have a RefInvoiceDocument. `Required` `Filter(multi eq)` |
