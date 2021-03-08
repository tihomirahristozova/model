# Table Crm_Invoice_Order_Lines

Detail records (lines) of Invoice Orders. Entity: Crm_Invoice_Order_Lines

# Aggregate Hierarchy

* [Crm_Invoice_Orders](Crm_Invoice_Orders.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Invoice_Order_Line_Id|`Guid`|`PK`, Readonly||
|Business_Reason|`InvoicingBusinessReason`|Allowed: `P`, `S`|Business reason for invoicing of this product or service. S=Shipment, P=Payment. `Required` `Default("S")` |
|Line_Custom_Discount_Percent|`Decimal`||User-defined discount for the line. `Required` `Default(0)` |
|Line_No|`Int32`||Line number, unique within the InvoiceOrder. Usually is increasing number like 10, 20, 30, ... when initially entering the InvoiceOrder (in order to allow insertions with adjustment documents). `Required` |
|Line_Standard_Discount_Percent|`Decimal`||Standard discount for the line. This is automatically computed according to discount conditions. `Required` `Default(0)` |
|Product_Description|`MultilanguageString`||The description of Product. Initially copied from the name of the Product or from the generating document. `Required` |
