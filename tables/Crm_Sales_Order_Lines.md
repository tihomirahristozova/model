# Table Crm_Sales_Order_Lines

Sales Orders detail records. Entity: Crm_Sales_Order_Lines

# Aggregate Hierarchy

* [Crm_Sales_Orders](Crm_Sales_Orders.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Sales_Order_Line_Id|`Guid`|`PK`, Readonly||
|Delivery_Terms_Code|`DeliveryTerms?`|Allowed: `EXW`, `FCA`, `FAS`, `FOB`, `CFR`, `CIF`, `CPT`, `CIP`, `DAP`, `DAT`, `DDP`, `DPU`|Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting. |
|Guarantee_Period_Days|`Int32?`||Guarantee period in days for the offered product. null for non-serviced products. |
|Historical_Data_Json|`String`||Used only for lines, which are returns. It is a JSON-formatted string, containing data from the original sale. `Introduced in version 19.1` |
|Intrastat_Transaction_Nature_Code|`TransactionNature?`|Allowed: `11`, `12`, `13`, `14`, `19`, `21`, `22`, `23`, `29`, `60`, `70`, `80`, `91`, `99`, `30`, `41`, `42`, `51`, `52`|Transaction nature; used for Intrastat reporting. |
|Intrastat_Transport_Mode_Code|`TransportMode?`|Allowed: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`|Transport mode; used for Intrastat reporting. |
|Line_Custom_Discount_Percent|`Decimal`||User-defined discount for the line. `Required` `Default(0)` `Filter(ge;le)` |
|Line_From_Date|`DateTime?`||When selling a service valid only for a period, denotes the beginning of the period. null means that it is unknown or N/A. `Introduced in version 20.1` |
|Line_No|`Int32`||Consecutive number of the line within the sales order. `Required` `Filter(eq)` `ORD` |
|Line_Standard_Discount_Percent|`Decimal`|Readonly|Standard discount for the line. This is automatically computed according to discount conditions. `Required` `Default(0)` `ReadOnly` |
|Line_To_Date|`DateTime?`||When selling a service valid only for a period, denotes the end of the period. null means that it is unknown or N/A. `Introduced in version 20.1` |
|Notes|`String`||Notes for this SalesOrderLine. |
|Parent_Line_No|`Int32?`||The number of the line within the parent document, which the current line executes. null when the current line does not execute parent line. `Filter(eq)` |
|Persist_Lot|`Boolean`||If checked specifies that the lot in the line cannot be changed in the sub-documents created by the current document. `Required` `Default(false)` `Filter(eq)` |
|Product_Description|`MultilanguageString`||The name of the sold product at the time the sale was made. `Required` `Filter(like)` |
|Required_Delivery_Date|`DateTime?`||The required (contracted) delivery date for the line. `Filter(ge;le)` |
