# Procedure Cash_Payment_Orders_Table_Load_Not_Paid


## Summary

| Name | Type | Description |
| - | - | --- |
|[Ref_Document_Date](#ref_document_date)|`datetime` ||
|[Ref_Document_Type_Id](#ref_document_type_id)|`uniqueidentifier` ||
|[Ref_Document_No](#ref_document_no)|`nvarchar` ||
|[Total_Amount](#total_amount)|`decimal(0, 0)` ||
|[Total_Amount_Currency_Id](#total_amount_currency_id)|`uniqueidentifier` ||
|[Covered_Order_Amount](#covered_order_amount)|`decimal(0, 0)` ||
|[Party_Id](#party_id)|`uniqueidentifier` ||
|[Due_Date](#due_date)|`datetime` ||
|[Direction](#direction)|`nvarchar` Allowed: `I`, `R`||
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` ||
|[Ref_Invoice_Document_Type_Id](#ref_invoice_document_type_id)|`uniqueidentifier` ||
|[Ref_Invoice_Document_No](#ref_invoice_document_no)|`nvarchar` ||
|[Ref_Invoice_Document_Date](#ref_invoice_document_date)|`datetime` ||
|[Installment_Number](#installment_number)|`int` ||
|[Is_Amount_With_VAT](#is_amount_with_vat)|`bit` ||
|[Location_Party_Id](#location_party_id)|`uniqueidentifier` ||
|[Bill_To](#bill_to)|`nvarchar` Allowed: `C`, `L`||
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` ||
|[State](#state)|`smallint` Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` ||
|[Document_Date](#document_date)|`date` ||
|[Due_Start_Date](#due_start_date)|`date` ||

## Columns

### Ref_Document_Date

| Property | Value |
| - | - |
|Type|datetime|

### Ref_Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ref_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Total_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Total_Amount_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Covered_Order_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Due_Date

| Property | Value |
| - | - |
|Type|datetime|

### Direction

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ref_Invoice_Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ref_Invoice_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Ref_Invoice_Document_Date

| Property | Value |
| - | - |
|Type|datetime|

### Installment_Number

| Property | Value |
| - | - |
|Type|int|

### Is_Amount_With_VAT

| Property | Value |
| - | - |
|Type|bit|

### Location_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Bill_To

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### State

| Property | Value |
| - | - |
|Type|smallint|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Date

| Property | Value |
| - | - |
|Type|date|

### Due_Start_Date

| Property | Value |
| - | - |
|Type|date|


