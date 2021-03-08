# Table Nat_BG_VAT_Document_Type_VAT_Codes

Contains the VAT codes, which should be used, when reporting VAT for the different document types. Entity: Nat_BG_VAT_Document_Type_VAT_Codes

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Document_Type_VAT_Code_Id|`Guid`|`PK`, Readonly||
|Cash_Reporting_VAT_Code|`CashReportingVATCode?`|Allowed: `01`, `02`, `03`, `04`, `05`, `07`, `09`, `11`, `12`, `13`, `81`, `82`, `91`, `92`, `93`, `94`|VAT code, which will be used when Cash Reporting mode is used for the entry. Allowed values are the same as for VAT Code. |
|VAT_Code|`VATCode?`|Allowed: `01`, `02`, `03`, `04`, `05`, `07`, `09`, `11`, `12`, `13`, `81`, `82`, `91`, `92`, `93`, `94`|VAT code to use when creating VAT export files for the specified Document Type. Allowed values is government-regulated list of values. |
