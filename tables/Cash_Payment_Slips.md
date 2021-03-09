# Table Cash_Payment_Slips

Represents mass payment document (payment slip). Entity: Cash_Payment_Slips

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` |The account towards which the payments was effected|
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` |The currency of the amounts in this document|
|[Payment_Slip_No](#payment_slip_no)|`nvarchar(20)` |When not null, contains the number of the slip, as issued by the banking institution.|
|[Payment_Slip_Id](#payment_slip_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` |When not NULL specifies the payment type for the sales order|

## Columns

### Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Slip_No

| Property | Value |
| - | - |
|Type|nvarchar(20)|

### Payment_Slip_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

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


