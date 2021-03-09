# Table Scm_Purchase_Invoices_Options

Contains purchase invoice specific options for the different document types. Entity: Scm_Purchase_Invoices_Options

## Summary

| Name | Type | Description |
| - | - | --- |
|[Purchese_Invoices_Option_Id](#purchese_invoices_option_id)|`uniqueidentifier` `PK`||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The document type, for which the options are specified.|
|[Sign_Restriction](#sign_restriction)|`int` Allowed: `-1`, `0`, `1`|This option can restrict the sign of the Line Amounts for each detail line in purchase invoices of the specified document type.|
|[Total_Amount_Sign_Restriction](#total_amount_sign_restriction)|`int` Allowed: `-1`, `0`, `1`|This option can restrict the sign of the Total Amounts of the purchase invoices of the specified document type. The restriction is applied upon document Release.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Purchese_Invoices_Option_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sign_Restriction

| Property | Value |
| - | - |
|Type|int|

### Total_Amount_Sign_Restriction

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


