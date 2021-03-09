# Procedure Scm_Purchase_Invoices_Table_Printout


## Summary

| Name | Type | Description |
| - | - | --- |
|[Purchase_Invoice_Id](#purchase_invoice_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Supplier_Id](#supplier_id)|`uniqueidentifier` |The supplier of the purchase, who is issuing the document.|
|[Supplier_Id_Text](#supplier_id_text)|`nvarchar` ||
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` |The currency of the unit prices and amounts in the document.|
|[Currency_Name](#currency_name)|`nvarchar` ||
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` |The payment type to be used. NULL is allowed only temporary and should be specified if payment order is to be generated|
|[Payment_Type_Name](#payment_type_name)|`nvarchar` ||
|[Purchase_Order_Id](#purchase_order_id)|`uniqueidentifier` |The purchase order that was sent to the supplier and is the base for the invoice. NULL means there is no linked PO and 3 way check won't be performed|
|[Receiving_Order_Id](#receiving_order_id)|`uniqueidentifier` ||
|[Deal_Type_Id](#deal_type_id)|`uniqueidentifier` |Deal type for this purchase invoice. If deal type in entered then VAT entry is created for this deal type.|
|[Apply_Date](#apply_date)|`date` |Specifies the date on which to create the VAT ledger entry for this purchase invoice. Usually, this date is equal to the document date, except when the document is received too late to be applied on its original document date.|
|[Cost_Center_Id](#cost_center_id)|`uniqueidentifier` |Cost center for which the amount from this document will be accounted.|
|[Sale_Deal_Type_Id](#sale_deal_type_id)|`uniqueidentifier` |Sale deal type for this purchase invoice. If sale deal type in entered then Sales VAT entry is created for this deal type.|
|[VAT_Notes](#vat_notes)|`nvarchar` |Description of the operation that will be entered in the VAT ledgers.|
|[Payment_Due_Date](#payment_due_date)|`datetime` |Due date for paying the invoice. NULL means to use the default |
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` |When not NULL, specifies the default payment account for the payment order|

## Columns

### Purchase_Invoice_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Supplier_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Supplier_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Currency_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Type_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Purchase_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Receiving_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Deal_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Apply_Date

| Property | Value |
| - | - |
|Type|date|

### Cost_Center_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sale_Deal_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### VAT_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Due_Date

| Property | Value |
| - | - |
|Type|datetime|

### Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


