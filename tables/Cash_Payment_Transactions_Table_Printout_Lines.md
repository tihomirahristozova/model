# Procedure Cash_Payment_Transactions_Table_Printout_Lines


## Summary

| Name | Type | Description |
| - | - | --- |
|[Payment_Transaction_Line_Id](#payment_transaction_line_id)|`uniqueidentifier` `PK`||
|[Payment_Transaction_Id](#payment_transaction_id)|`uniqueidentifier` ||
|[Amount](#amount)|`decimal(10, 2)` |The part of the total payed amount by the transaction, that is distributed to the specified payment order|
|[Covered_Order_Amount](#covered_order_amount)|`decimal(10, 2)` |The part of the original payment order amount, that is covered by this transaction line|
|[Payment_Order_Id](#payment_order_id)|`uniqueidentifier` |The payment order, that is covered by this transaction amount distribution (tr.line)|
|[Payment_Order_Ref_Document_Type_Id](#payment_order_ref_document_type_id)|`uniqueidentifier` |The type of the document which has created the payment order and is the basis for the payment|
|[Payment_Order_Ref_Document_Type_Name](#payment_order_ref_document_type_name)|`nvarchar` `ML`|Description of the document type|
|[Payment_Order_Ref_Document_No](#payment_order_ref_document_no)|`nvarchar` ||
|[Payment_Order_Ref_Document_Date](#payment_order_ref_document_date)|`datetime` |The date of the original document. NULL means that it is unknown|
|[Payment_Order_Due_Date](#payment_order_due_date)|`datetime` |The due date of the payment. NULL means there is no due date|
|[Payment_Order_Direction](#payment_order_direction)|`nvarchar` Allowed: `I`, `R`|I for Payment issue, R for payment receipt|
|[Payment_Order_Total_Amount](#payment_order_total_amount)|`decimal(18, 2)` |Total amount that should be payed|
|[Payment_Order_Total_Amount_Currency_Id](#payment_order_total_amount_currency_id)|`uniqueidentifier` |The currency of Total Amount.|
|[Payment_Order_Total_Amount_Currency_Name](#payment_order_total_amount_currency_name)|`nvarchar` ||
|[Payment_Order_Total_Amount_Currency_Sign](#payment_order_total_amount_currency_sign)|`nvarchar` |The international currency designator, as defined in ISO 4217. For example euro is represented as 'EUR'.|

## Columns

### Payment_Transaction_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Transaction_Id

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

### Payment_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Order_Ref_Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Order_Ref_Document_Type_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Order_Ref_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Order_Ref_Document_Date

| Property | Value |
| - | - |
|Type|datetime|

### Payment_Order_Due_Date

| Property | Value |
| - | - |
|Type|datetime|

### Payment_Order_Direction

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Order_Total_Amount

| Property | Value |
| - | - |
|Type|decimal(18, 2)|

### Payment_Order_Total_Amount_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Order_Total_Amount_Currency_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Order_Total_Amount_Currency_Sign

| Property | Value |
| - | - |
|Type|nvarchar|


