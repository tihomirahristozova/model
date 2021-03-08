# Table Cash_Bulk_Payment_Order_Lines

Bulk payment order document line. Each line usually creates one payment order. Entity: Cash_Bulk_Payment_Order_Lines

# Aggregate Hierarchy

* [Cash_Bulk_Payment_Orders](Cash_Bulk_Payment_Orders.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Bulk_Payment_Order_Line_Id|`Guid`|`PK`, Readonly||
|Bill_To|`BillTo?`|Allowed: `C`, `L`|If filled indicates which party is billed for the total amount. Possible values: 'C' = Company (means the Party_Id), 'L' = Company location (the Location_Party_Id), null = unidentified. |
|Direction|`Direction`|Allowed: `I`, `R`|I for Payment issue, R for payment receipt. `Required` `Default("I")` `Filter(eq)` |
|Due_Date|`DateTime?`||The due date of the payment. null means there is no due date. `Filter(ge;le)` |
|Installment_Number|`Int32?`||Consequtive installment number. Used for identifying the payment when using payment plans. null means that the payment is not part of a payment plan. |
|Is_Amount_With_VAT|`Boolean`||Is_Amount_With_VAT=true if the requested amount includes VAT. `Required` `Default(true)` `Filter(eq)` |
|Notes|`String`||Notes for this BulkPaymentOrderLine. |
|Ref_Document_Date|`DateTime?`||The date of the base document. null means that it is unknown. |
|Ref_Document_No|`String`||The number of the document which is the basis for the payment. `Required` |
|Ref_Invoice_Apply_Date|`DateTime?`||The apply date of the related invoice. Not specified when the payment order isn't related to any invoice or the apply date is unknown. |
|Ref_Invoice_Document_Date|`DateTime?`||The date of the related invoice. null means that the payment order isn't related to any invoice or the date is unknown. |
|Ref_Invoice_Document_No|`String`||The number of the invoice which is related and is the basis for the payment. null means that the payment order isn't created or related to any invoice. |
