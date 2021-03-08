# Table Cash_Payment_Transactions

Represents actual payments, which increase or decrease the balance of a payment account. Entity: Cash_Payment_Transactions

# Inheritance

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Payment_Transaction_Id|`Guid`|`PK`, Readonly||
|Adjustment_Number|`Int32`|Readonly||
|Adjustment_Time|`DateTime?`|Readonly||
|Adjustment_User|`String`|Readonly||
|Complete_Time|`DateTime?`|Readonly||
|Creation_Time|`DateTime`|Readonly||
|Creation_User|`String`|Readonly||
|Direction|`Direction`|Allowed: `I`, `R`|I for Payment issue, R for payment receipt. `Required` `Default("R")` `Filter(eq)` |
|Document_Date|`DateTime`|||
|Document_No|`String`|||
|Notes|`String`|||
|Document_Version|`Int32`|Readonly||
|Entity_Name|`String`|Readonly||
|Is_Released|`Boolean`|Readonly|True if the document is not void and its state is released or greater. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Is_Single_Execution|`Boolean`|Readonly|Specifies whether the document is a single execution of its order document. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Notes|`String`||Notes for this PaymentTransaction. |
|Parent_Document_Relationship_Type|`ParentDocumentRelationshipType?`|Allowed: `S`, `N`, Readonly||
|Payment_Slip_No|`String`||The number of the payment slip. Can be used to directly indicate the number without referring to Payment_Slips. `Filter(eq)` |
|Planning_Only|`Boolean`|Readonly||
|Read_Only|`Boolean`|Readonly||
|Reference_Date|`DateTime?`|||
|Reference_Document_No|`String`|||
|Release_Time|`DateTime?`|Readonly||
|Requires_Allocation|`Boolean`||True=The total amount should be allocated to payment orders; false=Payment orders are not required. `Required` `Default(true)` `Filter(eq)` |
|Reversal_Reason|`ReversalReason?`|Allowed: `OPE`, `TBR`, `REF`|The reason for the reversal of the payment. `Introduced in version 20.1` |
|State|`DocumentState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|Void|`Boolean`|Readonly||
|Void_Reason|`String`|Readonly||
|Void_Time|`DateTime?`|Readonly||
|Void_User|`String`|Readonly||
