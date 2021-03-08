# Table Cash_Payment_Orders

Each payment order contains a receivable or payable amount. Entity: Cash_Payment_Orders

# Inheritance

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Payment_Order_Id|`Guid`|`PK`, Readonly||
|Adjustment_Number|`Int32`|Readonly||
|Adjustment_Time|`DateTime?`|Readonly||
|Adjustment_User|`String`|Readonly||
|Allow_Close_Not_Paid|`Boolean`||True to allow closing of payment orders, that are not fully paid. `Required` `Default(false)` `Filter(eq)` |
|Bill_To|`BillTo?`|Allowed: `C`, `L`|If filled indicates which party is billed for the total amount. Possible values: 'C' = Company (means the Party_Id), 'L' = Company location (the Location_Party_Id), null = unidentified. `Filter(eq)` |
|Complete_Time|`DateTime?`|Readonly||
|Creation_Time|`DateTime`|Readonly||
|Creation_User|`String`|Readonly||
|Direction|`Direction`|Allowed: `I`, `R`|I for Payment issue, R for payment receipt. `Required` `Default("I")` `Filter(eq)` |
|Document_Date|`DateTime`|||
|Document_No|`String`|||
|Notes|`String`|||
|Document_Version|`Int32`|Readonly||
|Due_Date|`DateTime?`||The due date of the payment. null means there is no due date. `Filter(eq;ge;le)` |
|Due_Start_Date|`DateTime?`||The date at which the payment becomes executable. null means the payment is executable at all times. `Filter(eq;ge;le)` `ORD` |
|Entity_Name|`String`|Readonly||
|Installment_Number|`Int32?`||Consequtive installment number. Used for identifying the payment when using payment plans. null means that the payment is not part of a payment plan. `Filter(eq)` |
|Is_Amount_With_VAT|`Boolean`||Is_Amount_With_VAT=true if the requested amount includes VAT. `Required` `Default(true)` `Filter(eq)` |
|Is_Released|`Boolean`|Readonly|True if the document is not void and its state is released or greater. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Is_Single_Execution|`Boolean`|Readonly|Specifies whether the document is a single execution of its order document. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Notes|`String`||Notes for this PaymentOrder. |
|Parent_Document_Relationship_Type|`ParentDocumentRelationshipType?`|Allowed: `S`, `N`, Readonly||
|Planning_Only|`Boolean`|Readonly||
|Read_Only|`Boolean`|Readonly||
|Ref_Document_Date|`DateTime?`||The date of the original document. null means that it is unknown. `Filter(eq)` |
|Ref_Document_No|`String`||The number of the document which has created the payment order and is the basis for the payment. `Required` `Filter(eq)` |
|Reference_Date|`DateTime?`|||
|Reference_Document_No|`String`|||
|Ref_Invoice_Apply_Date|`DateTime?`||The apply date of the related invoice. Not specified when the payment order isn't related to any invoice or the apply date is unknown. `Filter(eq;ge;le)` |
|Ref_Invoice_Document_Date|`DateTime?`||The date of the related invoice. null means that the payment order isn't related to any invoice or the date is unknown. `Filter(eq;ge;le)` |
|Ref_Invoice_Document_No|`String`||The number of the invoice which has created or is related to the payment order and is the basis for the payment. null means that the payment order isn't created or related to any invoice. `Filter(eq)` |
|Release_Time|`DateTime?`|Readonly||
|State|`DocumentState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|Void|`Boolean`|Readonly||
|Void_Reason|`String`|Readonly||
|Void_Time|`DateTime?`|Readonly||
|Void_User|`String`|Readonly||
