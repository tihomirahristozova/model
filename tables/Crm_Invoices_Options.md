# Table Crm_Invoices_Options

Default options for user document types for Invoices. Entity: Crm_Invoices_Options

# Aggregate Hierarchy

* [Gen_Document_Types](Gen_Document_Types.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Invoices_Option_Id|`Guid`|`PK`, Readonly||
|Creates_VAT_Entries|`Boolean`||Specifies whether the invoices of the current type create entries in the VAT ledges. If is used, for instance, to determine if null VAT entry should be automatically created when the invoice is voided. `Required` `Default(true)` |
|Sign_Restriction|`SignRestriction`|Allowed: `0`, `1`, `-1`|Restricts the sign of the line amounts of the invoices. -1 =allow only negative, 0=allow all, 1=allow only positive amounts. `Required` `Default(0)` |
|Total_Amount_Sign_Restriction|`SignRestriction`|Allowed: `0`, `1`, `-1`|Restricts the sign of the total amount (amount to pay) of the invoices. -1 =allow only negative, 0=allow all, 1=allow only positive amounts. `Required` `Default(0)` |
