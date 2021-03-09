# Table Scm_Purchase_Invoices

Contains purchase invoice headers. Entity: Scm_Purchase_Invoices

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Purchase_Invoice_Id](#purchase_invoice_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Supplier_Id](#supplier_id)|`uniqueidentifier` |The supplier of the purchase, who is issuing the document.|
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` |The currency of the unit prices and amounts in the document.|
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` |The payment type to be used. NULL is allowed only temporary and should be specified if payment order is to be generated|
|[Purchase_Order_Id](#purchase_order_id)|`uniqueidentifier` |The purchase order that was sent to the supplier and is the base for the invoice. NULL means there is no linked PO and 3 way check won't be performed|
|[Receiving_Order_Id](#receiving_order_id)|`uniqueidentifier` |The receiving order for the goods that were invoiced. The id is used for 2 or 3 way quantity check. NULL means that there is no linked RO and the 2 or 3 way check will not include the RO|
|[Credit_Note_Original_Purchase_Invoice_Id](#credit_note_original_purchase_invoice_id)|`uniqueidentifier` |The original invoice, which is debited/credited with this note|
|[Credit_Note_Reason](#credit_note_reason)|`nvarchar(254)` |Reason for the debit/credit note|
|[Deal_Type_Id](#deal_type_id)|`uniqueidentifier` |Deal type for this purchase invoice. If deal type in entered then VAT entry is created for this deal type.|
|[Cost_Center_Id](#cost_center_id)|`uniqueidentifier` |Cost center for which the amount from this document will be accounted.|
|[Apply_Date](#apply_date)|`date` |Specifies the date on which to create the VAT ledger entry for this purchase invoice. Usually, this date is equal to the document date, except when the document is received too late to be applied on its original document date.|
|[Sale_Deal_Type_Id](#sale_deal_type_id)|`uniqueidentifier` |Sale deal type for this purchase invoice. If sale deal type in entered then Sales VAT entry is created for this deal type.|
|[VAT_Notes](#vat_notes)|`nvarchar(254)` |Description of the operation that will be entered in the VAT ledgers.|
|[Payment_Due_Date](#payment_due_date)|`datetime` |Due date for paying the invoice. NULL means to use the default |
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` |When not NULL, specifies the default payment account for the payment order|
|[Purchase_Price_List_Id](#purchase_price_list_id)|`uniqueidentifier` |The price list, which, when non-NULL, is used to automatically load unit prices of the products, when entering the invoice manually.|
|[Delivery_Terms_Code](#delivery_terms_code)|`nvarchar(3)` Allowed: `EXW`, `FCA`, `FAS`, `FOB`, `CFR`, `CIF`, `CPT`, `CIP`, `DAP`, `DAT`, `DDP`, `DPU`|Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting|
|[Intrastat_Transaction_Nature_Code](#intrastat_transaction_nature_code)|`nvarchar(2)` Allowed: `11`, `12`, `13`, `14`, `19`, `21`, `22`, `23`, `29`, `60`, `70`, `80`, `91`, `99`, `30`, `41`, `42`, `51`, `52`|Transaction nature; used for Intrastat reporting|
|[Intrastat_Transport_Mode_Code](#intrastat_transport_mode_code)|`nvarchar(1)` Allowed: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`|Transport mode; used for Intrastat reporting|
|[Intrastat_Transport_Country_Id](#intrastat_transport_country_id)|`uniqueidentifier` |Country of origin of the transport company; used for Intrastat reporting|
|[Intrastat_Destination_Region_Id](#intrastat_destination_region_id)|`uniqueidentifier` |Region, which is the final destination of the goods. Used for Intrastat reporting. When this is non-NULL, it applies to the whole document.|
|[VAT_Cash_Reporting_Mode](#vat_cash_reporting_mode)|`bit` |When True, indicates, that this invoice uses the special 'Cash reporting mode' when creating VAT ledger entries.|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||

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

### Document_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Receiving_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Credit_Note_Original_Purchase_Invoice_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Credit_Note_Reason

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Deal_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Cost_Center_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Apply_Date

| Property | Value |
| - | - |
|Type|date|

### Sale_Deal_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### VAT_Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Payment_Due_Date

| Property | Value |
| - | - |
|Type|datetime|

### Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Price_List_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Delivery_Terms_Code

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Intrastat_Transaction_Nature_Code

| Property | Value |
| - | - |
|Type|nvarchar(2)|

### Intrastat_Transport_Mode_Code

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Intrastat_Transport_Country_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Intrastat_Destination_Region_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### VAT_Cash_Reporting_Mode

| Property | Value |
| - | - |
|Type|bit|

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


