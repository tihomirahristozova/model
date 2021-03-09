# Table Cash_Payment_Transaction_Lines

Contains the distibution of the payments' amounts among the source payment orders. Entity: Cash_Payment_Transaction_Lines

## Owner Tables Hierarchy

* [Cash_Payment_Transactions](Cash_Payment_Transactions.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Amount](#amount)|`decimal(10, 2)` |The part of the total payed amount by the transaction, that is distributed to the specified payment order|
|[Covered_Order_Amount](#covered_order_amount)|`decimal(10, 2)` |The part of the original payment order amount, that is covered by this transaction line|
|[Payment_Order_Id](#payment_order_id)|`uniqueidentifier` |The payment order, that is covered by this transaction amount distribution (tr.line)|
|[Payment_Transaction_Line_Id](#payment_transaction_line_id)|`uniqueidentifier` `PK`||
|[Payment_Transaction_Id](#payment_transaction_id)|`uniqueidentifier` ||
|[Notes](#notes)|`nvarchar(254)` ||
|[Allow_Overpayment](#allow_overpayment)|`bit` |1-Allows overpayment for the payment order; 0=Does not allow (default)|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Amount

| Property | Value |
| - | - |
|Type|decimal(10, 2)|

### Covered_Order_Amount

| Property | Value |
| - | - |
|Type|decimal(10, 2)|

### Payment_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Transaction_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Allow_Overpayment

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


