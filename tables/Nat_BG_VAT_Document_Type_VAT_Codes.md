# Table Nat_BG_VAT_Document_Type_VAT_Codes

Contains the VAT codes, which should be used, when reporting VAT for the different document types. Entity: Nat_BG_VAT_Document_Type_VAT_Codes

## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Type_VAT_Code_Id](#document_type_vat_code_id)|`uniqueidentifier` `PK`|Unique identification of the record.|
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |Document type that generates VAT entries.|
|[VAT_Code](#vat_code)|`nvarchar(2)` Allowed: `01`, `02`, `03`, `04`, `05`, `07`, `09`, `11`, `12`, `13`, `81`, `82`, `91`, `92`, `93`, `94`|VAT code to use when creating VAT export files for the specified Document Type. Allowed values is government-regulated list of values.|
|[Cash_Reporting_VAT_Code](#cash_reporting_vat_code)|`nvarchar(2)` Allowed: `01`, `02`, `03`, `04`, `05`, `07`, `09`, `11`, `12`, `13`, `81`, `82`, `91`, `92`, `93`, `94`|VAT code, which will be used when Cash Reporting mode is used for the entry. Allowed values are the same as for VAT Code.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Document_Type_VAT_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### VAT_Code

| Property | Value |
| - | - |
|Type|nvarchar(2)|

### Cash_Reporting_VAT_Code

| Property | Value |
| - | - |
|Type|nvarchar(2)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


