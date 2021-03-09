# Table Cash_Payment_Slip_Lines

Mass payment line, which is distribution of an amount among payment orders. Each record generates one payment transaction line. Entity: Cash_Payment_Slip_Lines

## Owner Tables Hierarchy

* [Cash_Payment_Slip_Amounts](Cash_Payment_Slip_Amounts.md)
* [Cash_Payment_Slips](Cash_Payment_Slips.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Amount](#amount)|`decimal(10, 2)` |The part of the total amount in the payment slip amount, that is distributed to the specified payment order|
|[Covered_Order_Amount](#covered_order_amount)|`decimal(10, 2)` |The part of the original payment order amount, that is covered by this payment slip line|
|[Payment_Order_Id](#payment_order_id)|`uniqueidentifier` |The payment order, that is covered by this payment slip line|
|[Payment_Slip_Line_Id](#payment_slip_line_id)|`uniqueidentifier` `PK`||
|[Payment_Slip_Amount_Id](#payment_slip_amount_id)|`uniqueidentifier` Readonly||
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

### Payment_Slip_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Slip_Amount_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


