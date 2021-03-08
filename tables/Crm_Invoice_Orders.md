# Table Crm_Invoice_Orders

Invoice Orders can be created by different modules and order the creation of Invoices. Entity: Crm_Invoice_Orders

# Inheritance

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Invoice_Order_Id|`Guid`|`PK`, Readonly||
|Adjustment_Number|`Int32`|Readonly||
|Adjustment_Time|`DateTime?`|Readonly||
|Adjustment_User|`String`|Readonly||
|Apply_Date|`DateTime?`||Apply date to be passed to the invoice. When not null specifies that the VAT entry should be applied for a different period than that specified by the document date. |
|Complete_Time|`DateTime?`|Readonly||
|Creation_Time|`DateTime`|Readonly||
|Creation_User|`String`|Readonly||
|Credit_Note_Description|`String`||Descriptions/reason for the credit note. |
|Delivery_Date|`DateTime?`||Date, when the delivery was effected. When null = document date. |
|Document_Date|`DateTime`|||
|Document_No|`String`|||
|Notes|`String`|||
|Document_Version|`Int32`|Readonly||
|Entity_Name|`String`|Readonly||
|Is_Released|`Boolean`|Readonly|True if the document is not void and its state is released or greater. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Is_Single_Execution|`Boolean`|Readonly|Specifies whether the document is a single execution of its order document. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Notes|`String`||Notes for this InvoiceOrder. |
|Parent_Document_Relationship_Type|`ParentDocumentRelationshipType?`|Allowed: `S`, `N`, Readonly||
|Payment_Due_Date|`DateTime?`||When not null specifies due date for the payment. |
|Payment_Due_Start_Date|`DateTime?`||The date when the payment becomes due for documents with one installment. |
|Payment_Type_Description|`String`||Description of the payment type. Initially copied from the name of the Payment Type. `Required` |
|Planning_Only|`Boolean`|Readonly||
|Read_Only|`Boolean`|Readonly||
|Reference_Date|`DateTime?`|||
|Reference_Document_No|`String`|||
|Release_Time|`DateTime?`|Readonly||
|State|`DocumentState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|Void|`Boolean`|Readonly||
|Void_Reason|`String`|Readonly||
|Void_Time|`DateTime?`|Readonly||
|Void_User|`String`|Readonly||
