# Table Scm_Purchase_Control_Document_Lines

The detail line of purchase control data. The purchase control is used to tally all orders and execuctions in the purchasing module. Entity: Scm_Purchase_Control_Document_Lines (Introduced in version 18.2)

# Aggregate Hierarchy

* [Scm_Purchase_Control_Documents](Scm_Purchase_Control_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Purchase_Control_Document_Line_Id|`Guid`|`PK`, Readonly||
|Confirmed_Amount_Base|`Decimal?`||The amount (in base currency) of the ordered items, confirmed by the supplier (usually with Purchase Confirmation). Null when the logged operation did not involve confirming ordered items. |
|Confirmed_Standard_Quantity_Base|`Decimal?`||The standard quantity of the ordered items, confirmed by the supplier (usually with Purchase Confirmation) in base measurement unit. Null when the logged operation did not involve confirming ordered items. |
|Invoiced_Amount_Base|`Decimal?`||The amount (in base currency) of the invoiced items (usually with Purchase Invoice). Null when the logged operation did not involve invoicing items. |
|Invoiced_Standard_Quantity_Base|`Decimal?`||The standard quantity of the invoiced items (usually with Purchase Invoice) in base measurement unit. Null when the logged operation did not involve invoicing items. |
|Line_No|`Int32`||The consecutive line number within the control document. `Required` |
|Notes|`String`||Notes for this PurchaseControlDocumentLine. |
|Ordered_Amount_Base|`Decimal?`||The amount (in base currency) of the ordered items (usually with Purchase Order). Null when the logged operation did not involve ordering items. |
|Ordered_Standard_Quantity_Base|`Decimal?`||The standard quantity of the ordered items (usually with Purchase Order) in base measurement unit. Null when the logged operation did not involve ordering items. |
|Received_Amount_Base|`Decimal?`||The amount (in base currency) of the received items (usually with Receiving Order). Null when the logged operation did not involve receiving items. |
|Received_Standard_Quantity_Base|`Decimal?`||The standard quantity of the received items (usually with Receiving Order) in base measurement unit. Null when the logged operation did not involve receiving items. |
|Requested_Amount_Base|`Decimal?`||The amount (in base currency) of the requested items (usually with Purchase Requisition). Null when the logged operation did not involve requesting items. |
|Requested_Standard_Quantity_Base|`Decimal?`||The standard quantity of the requested items (usually with Purchase Requisition) in base measurement unit. Null when the logged operation did not involve requesting items. |
