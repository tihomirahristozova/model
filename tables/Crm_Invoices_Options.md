# Table Crm_Invoices_Options

Default options for user document types for Invoices. Entity: Crm_Invoices_Options

## Owner Tables Hierarchy

* [Gen_Document_Types](Gen_Document_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Invoices_Option_Id](#invoices_option_id)|`uniqueidentifier` `PK`||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The document type for which the invoice option applies.|
|[Default_Deal_Type_Id](#default_deal_type_id)|`uniqueidentifier` |When not NULL, specifies default VAT deal type.|
|[Sign_Restriction](#sign_restriction)|`int` Allowed: `-1`, `0`, `1`|Restricts the sign of the line amounts of the invoices. -1 =allow only negative, 0=allow all, 1=allow only positive amounts|
|[Total_Amount_Sign_Restriction](#total_amount_sign_restriction)|`int` Allowed: `-1`, `0`, `1`|Restricts the sign of the total amount (amount to pay) of the invoices. -1 =allow only negative, 0=allow all, 1=allow only positive amounts|
|[VAT_Deviation_Document_Amount_Type_Id](#vat_deviation_document_amount_type_id)|`uniqueidentifier` |Document amount that contains the difference between the total amount of the invoice formed by unit prices with VAT and the amount formed by unit prices without VAT|
|[Creates_VAT_Entries](#creates_vat_entries)|`bit` |Specifies whether the invoices of the current type create entries in the VAT ledges. If is used, for instance, to determine if null VAT entry should be automatically created when the invoice is voided.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Invoices_Option_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Deal_Type_Id

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

### VAT_Deviation_Document_Amount_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Creates_VAT_Entries

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


