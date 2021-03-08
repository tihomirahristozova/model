# Table Crm_Invoice_Lines

Detail records (lines) of the invoices. Entity: Crm_Invoice_Lines

# Aggregate Hierarchy

* [Crm_Invoices](Crm_Invoices.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Invoice_Line_Id|`Guid`|`PK`, Readonly||
|Business_Reason|`InvoicingBusinessReason`|Allowed: `P`, `S`|Business reason for invoicing of this product or service. S=Shipment, P=Payment. `Required` `Default("S")` |
|Delivery_Terms_Code|`DeliveryTerms?`|Allowed: `EXW`, `FCA`, `FAS`, `FOB`, `CFR`, `CIF`, `CPT`, `CIP`, `DAP`, `DAT`, `DDP`, `DPU`|Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting. |
|Intrastat_Transaction_Nature_Code|`TransactionNature?`|Allowed: `11`, `12`, `13`, `14`, `19`, `21`, `22`, `23`, `29`, `60`, `70`, `80`, `91`, `99`, `30`, `41`, `42`, `51`, `52`|Transaction nature; used for Intrastat reporting. |
|Intrastat_Transport_Mode_Code|`TransportMode?`|Allowed: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`|Transport mode; used for Intrastat reporting. |
|Line_Custom_Discount_Percent|`Decimal`||User-defined discount for the line. `Required` `Default(0)` `Filter(ge;le)` |
|Line_No|`Int32`||Consecutive line number, unique within the invoice. Usually is increasing in steps of 10, like in 10, 20, 30, etc. `Required` `Filter(eq)` |
|Line_Standard_Discount_Percent|`Decimal`||Standard discount for the line. This is automatically computed according to discount conditions. `Required` `Default(0)` |
|Notes|`String`||Notes for this InvoiceLine. |
|Parent_Line_No|`Int32?`||The number of the line within the parent document, which the current line executes. null when the current line does not execute line. `Introduced in version 18.2` |
|Product_Description|`MultilanguageString`||The description of the invoiced product. Initially copied from the name of the invoiced Product or from the generating document. `Required` |
|Sales_Order_Amount|`Decimal?`||Specifies what portion of the amount of the sales order is invoiced with this line. The amount is calculated with respect to the trade conditions (prices, discounts, etc.) from the sales order. Can be different from the total amount of the line when the trade conditions from the sales order have changed before invoicing. |
