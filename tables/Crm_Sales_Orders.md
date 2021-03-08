# Table Crm_Sales_Orders

Sales order document headers. Entity: Crm_Sales_Orders

# Inheritance

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Sales_Order_Id|`Guid`|`PK`, Readonly||
|Adjustment_Number|`Int32`|Readonly||
|Adjustment_Time|`DateTime?`|Readonly||
|Adjustment_User|`String`|Readonly||
|Complete_Time|`DateTime?`|Readonly||
|Creation_Time|`DateTime`|Readonly||
|Creation_User|`String`|Readonly||
|Credit_Limit_Override|`Boolean`||Allows the sales order to be released even in the case of violations of credit limit or presence of overdue receivables. `Required` `Default(false)` `Filter(eq)` |
|Customer_Purchase_Order_Date|`DateTime?`||Issue date of the referent customer purchase order. `Filter(ge;le)` |
|Customer_Purchase_Order_No|`String`||Reference number of the customer's purchase order. `Filter(eq;like)` |
|Delivery_Terms_Code|`DeliveryTerms?`|Allowed: `EXW`, `FCA`, `FAS`, `FOB`, `CFR`, `CIF`, `CPT`, `CIP`, `DAP`, `DAT`, `DDP`, `DPU`|Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting. |
|Document_Date|`DateTime`|||
|Document_No|`String`|||
|Notes|`String`|||
|Document_Version|`Int32`|Readonly||
|Entity_Name|`String`|Readonly||
|Fiscal_Sales_Number|`String`|Readonly|Unique number of the sale, assigned for fiscal reporting purposes. The format is according to the applicable legislation. null means that there is no requirement for fiscal sales number for this document or it is unknown. `Filter(multi eq;like)` `ReadOnly` `Introduced in version 19.1` |
|From_Date|`DateTime?`||When selling a service valid only for a period, denotes the beginning of the period. null means that it is unknown or N/A. `Introduced in version 20.1` |
|Intrastat_Transaction_Nature_Code|`TransactionNature?`|Allowed: `11`, `12`, `13`, `14`, `19`, `21`, `22`, `23`, `29`, `60`, `70`, `80`, `91`, `99`, `30`, `41`, `42`, `51`, `52`|Transaction nature; used for Intrastat reporting. |
|Intrastat_Transport_Mode_Code|`TransportMode?`|Allowed: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`|Transport mode; used for Intrastat reporting. |
|Is_Released|`Boolean`|Readonly|True if the document is not void and its state is released or greater. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Is_Single_Execution|`Boolean`|Readonly|Specifies whether the document is a single execution of its order document. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|IsValid|`Boolean`|Readonly|True when the order is valid (e.g. released and not void). Used for internal processing. `Required` `Default(false)` `ReadOnly` |
|Notes|`String`||Notes for this SalesOrder. |
|Parent_Document_Relationship_Type|`ParentDocumentRelationshipType?`|Allowed: `S`, `N`, Readonly||
|Payment_Due_Date|`DateTime?`||The last term for the payment of the sales order. `Filter(ge;le)` |
|Payment_Due_Start_Date|`DateTime?`||The date when the payment becomes due for documents with one installment. null when the document is with multiple installments. |
|Planning_Only|`Boolean`|Readonly||
|Read_Only|`Boolean`|Readonly||
|Reference_Date|`DateTime?`|||
|Reference_Document_No|`String`|||
|Release_Time|`DateTime?`|Readonly||
|Required_Delivery_Date|`DateTime?`||The required delivery date for all lines in the sales order. Initially calculated, based on either the Ship To Customer or Customer delivery term. `Filter(ge;le)` |
|State|`DocumentState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|To_Date|`DateTime?`||When selling a service valid only for a period, denotes the end of the period. null means that it is unknown or N/A. `Introduced in version 20.1` |
|Void|`Boolean`|Readonly||
|Void_Reason|`String`|Readonly||
|Void_Time|`DateTime?`|Readonly||
|Void_User|`String`|Readonly||
