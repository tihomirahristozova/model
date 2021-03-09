# Procedure Cash_Payment_Transactions_Table_Get_Payment_Transaction_Lines_Total_Amounts


## Summary

| Name | Type | Description |
| - | - | --- |
|[Payment_Transaction_Id](#payment_transaction_id)|`uniqueidentifier` ||
|[Payment_Order_Id](#payment_order_id)|`uniqueidentifier` |The payment order, that is covered by this transaction amount distribution (tr.line)|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` ||
|[Payment_Order_Currency_Id](#payment_order_currency_id)|`uniqueidentifier` ||
|[Amount](#amount)|`decimal(10, 2)` |The part of the total payed amount by the transaction, that is distributed to the specified payment order|
|[Covered_Order_Amount](#covered_order_amount)|`decimal(10, 2)` |The part of the original payment order amount, that is covered by this transaction line|

## Columns

### Payment_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Order_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Amount

| Property | Value |
| - | - |
|Type|decimal(10, 2)|

### Covered_Order_Amount

| Property | Value |
| - | - |
|Type|decimal(10, 2)|


