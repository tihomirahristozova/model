# Table Inv_Store_Order_Lines

Detail lines of store orders. Each line represents one planned stock transaction line, but can be executed in parts. E.g. many transaction lines can be bound to one order line. Entity: Inv_Store_Order_Lines

# Aggregate Hierarchy

* [Inv_Store_Orders](Inv_Store_Orders.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Store_Order_Line_Id|`Guid`|`PK`, Readonly||
|For_Ordering|`Boolean`||Specifies that the quantity of the product can be less than free to use quantity, because the product will be supplied . `Required` `Default(false)` |
|Guarantee_Period_Days|`Int32?`||Guarantee period in days for the offered product. null for non-serviced products. |
|Line_No|`Int32`||Line number within the store order. `Required` `Filter(eq)` |
|Lot_Number|`String`||Obsolete. Not used. |
|Notes|`String`||Notes for this StoreOrderLine. |
|Parent_Line_Id|`Guid?`||Id of the line of the parent document, which generated the store order. null for user-entered store orders or if not applicable. `Filter(multi eq)` |
|Parent_Line_No|`Int32?`||The number of the line within the parent document, which the current line executes. null when the current line does not execute parent line. `Filter(eq)` |
|Persist_Lot|`Boolean`||If checked specifies that the lot in the line cannot be changed in the sub-documents created by the current document. `Required` `Default(false)` `Filter(eq)` |
|Transaction_Timestamp|`DateTime?`|Readonly|Exact time when the transaction for this store order line changes the cost of the product. `ReadOnly` |
