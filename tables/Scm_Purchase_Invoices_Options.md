# Table Scm_Purchase_Invoices_Options

Contains purchase invoice specific options for the different document types. Entity: Scm_Purchase_Invoices_Options

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Purchese_Invoices_Option_Id|`Guid`|`PK`, Readonly||
|Sign_Restriction|`SignRestriction`|Allowed: `0`, `1`, `-1`|This option can restrict the sign of the Line Amounts for each detail line in purchase invoices of the specified document type. `Required` `Default(0)` |
|Total_Amount_Sign_Restriction|`TotalAmountSignRestriction`|Allowed: `0`, `1`, `-1`|This option can restrict the sign of the Total Amounts of the purchase invoices of the specified document type. The restriction is applied upon document Release. `Required` `Default(0)` |
