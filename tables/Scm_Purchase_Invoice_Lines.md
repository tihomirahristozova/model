# Table Scm_Purchase_Invoice_Lines

Contains detail lines for purchase invoice documents. Entity: Scm_Purchase_Invoice_Lines

# Aggregate Hierarchy

* [Scm_Purchase_Invoices](Scm_Purchase_Invoices.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Purchase_Invoice_Line_Id|`Guid`|`PK`, Readonly||
|Delivery_Terms_Code|`DeliveryTerms?`|Allowed: `EXW`, `FCA`, `FAS`, `FOB`, `CFR`, `CIF`, `CPT`, `CIP`, `DAP`, `DAT`, `DDP`, `DPU`|Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting. |
|Intrastat_Apply_Date|`DateTime?`||Specifies in which period for Intrastat declaration must be included the current operation. Used only when the invoice is issued in different period than the one, that the operation must be included. If not set the document date is used. |
|Intrastat_Transaction_Nature_Code|`TransactionNature?`|Allowed: `11`, `12`, `13`, `14`, `19`, `21`, `22`, `23`, `29`, `60`, `70`, `80`, `91`, `99`, `30`, `41`, `42`, `51`, `52`|Transaction nature; used for Intrastat reporting. |
|Intrastat_Transport_Mode_Code|`TransportMode?`|Allowed: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`|Transport mode; used for Intrastat reporting. |
|Line_No|`Int32`||Consecutive line number within the invoice. `Required` |
|Notes|`String`||Notes for this PurchaseInvoiceLine. |
|Product_Name|`MultilanguageString`||The name of the invoiced product, initially copied from the name in the product definition. The field can be edited by the user. `Required` |
