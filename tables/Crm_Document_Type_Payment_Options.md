# Table Crm_Document_Type_Payment_Options

Contains payment options for user documnet types for sales orders. Entity: Crm_Document_Type_Payment_Options

## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Type_Payment_Option_Id](#document_type_payment_option_id)|`uniqueidentifier` `PK`||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The document type for which the payment option applies.|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company for which the payment options are specified|
|[Deferred_Payment_Minimal_Ammount](#deferred_payment_minimal_ammount)|`decimal(14, 2)` |The minimal order total amount, which an order must have in order to use deferred payment|
|[Deferred_Payment_Minimal_Ammount_Currency_Id](#deferred_payment_minimal_ammount_currency_id)|`uniqueidentifier` |The currency of Deferred Payment Minimal Amount|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Document_Type_Payment_Option_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Deferred_Payment_Minimal_Ammount

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Deferred_Payment_Minimal_Ammount_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


