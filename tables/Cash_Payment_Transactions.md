# Table Cash_Payment_Transactions

Represents actual payments, which increase or decrease the balance of a payment account. Entity: Cash_Payment_Transactions

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Party_Id](#party_id)|`uniqueidentifier` |The party that is paying or receiving the money|
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` |The account towards which the payment was effected|
|[Direction](#direction)|`nvarchar(1)` Allowed: `I`, `R`|I for Payment issue, R for payment receipt|
|[Total_Amount](#total_amount)|`decimal(18, 2)` |The total amount payed. The distribution of the amount among source orders is specified with payment transacion lines|
|[Total_Amount_Currency_Id](#total_amount_currency_id)|`uniqueidentifier` |The currency of the total amount|
|[Requires_Allocation](#requires_allocation)|`bit` |1=The total amount should be allocated to payment orders; 0=Payment orders are not required|
|[Payment_Slip_No](#payment_slip_no)|`nvarchar(20)` |The number of the payment slip. Can be used to directly indicate the number without referring to Payment_Slips|
|[Payment_Slip_Id](#payment_slip_id)|`uniqueidentifier` |When not NULL specifies that this payment was part of a payment slip|
|[Notes](#notes)|`nvarchar(254)` ||
|[Payment_Transaction_Id](#payment_transaction_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` |The document data of the payment transaction|
|[Original_Payment_Transaction_Id](#original_payment_transaction_id)|`uniqueidentifier` |Original Payment Transaction|
|[Payment_Reason_Id](#payment_reason_id)|`uniqueidentifier` |The payment reason, as defined in Payment Reasons.|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` |Specifies the payment type used to pay, when using this payment account. NULL when the payment type is unknown or unspecified.|
|[Fiscal_Printer_Pos_Device_Id](#fiscal_printer_pos_device_id)|`uniqueidentifier` |For POS Sales Order payments. Specifies the POS Device from fiscal printer type on which the receipt is printed. Null when the payment transaction is not created for a POS Sale Order.|
|[Parent_Payment_Slip_Amount_Id](#parent_payment_slip_amount_id)|`uniqueidentifier` |The Payment Slip Amount, which the current payment transaction fulfills . NULL when the current document does not execute any Payment Slip Amount.|
|[Pos_Location_Id](#pos_location_id)|`uniqueidentifier` |For POS Sales Order payments. Specifies the POS Location, in which the payment is performed. Null when the payment transaction is not created for a POS Sale Order.|
|[Pos_Operator_Id](#pos_operator_id)|`uniqueidentifier` |For POS Sales Order payments. Specifies the POS Operator, who created the payment order. Null when the payment transaction is not created for a POS Sale Order.|
|[Reversal_Reason](#reversal_reason)|`nvarchar(3)` Allowed: `OPE`, `TBR`, `REF`|The reason for the reversal of the payment.|

## Columns

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Direction

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Total_Amount

| Property | Value |
| - | - |
|Type|decimal(18, 2)|

### Total_Amount_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Requires_Allocation

| Property | Value |
| - | - |
|Type|bit|

### Payment_Slip_No

| Property | Value |
| - | - |
|Type|nvarchar(20)|

### Payment_Slip_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Payment_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Original_Payment_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Reason_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Single_Execution

| Property | Value |
| - | - |
|Type|bit|

### Is_Released

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Fiscal_Printer_Pos_Device_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Payment_Slip_Amount_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pos_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pos_Operator_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Reversal_Reason

| Property | Value |
| - | - |
|Type|nvarchar(3)|


