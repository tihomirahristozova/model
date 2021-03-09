# Table Cash_Invoice_Reconciliation_Lines


## Owner Tables Hierarchy

* [Cash_Invoice_Reconciliations](Cash_Invoice_Reconciliations.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Invoice_Reconciliation_Line_Id](#invoice_reconciliation_line_id)|`uniqueidentifier` `PK`||
|[Invoice_Reconciliation_Id](#invoice_reconciliation_id)|`uniqueidentifier` ||
|[Invoice_Document_Id](#invoice_document_id)|`uniqueidentifier` |Obsolete. Not used.|
|[Payment_Transaction_Document_Id](#payment_transaction_document_id)|`uniqueidentifier` |Obsolete. Not used.|
|[Covered_Invoice_Amount](#covered_invoice_amount)|`decimal(14, 2)` |Amount from the invoice that is covered by the payment. The amount is in the currency of the invoice.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Invoice_Reconciliation_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Invoice_Reconciliation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Invoice_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Transaction_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Covered_Invoice_Amount

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


