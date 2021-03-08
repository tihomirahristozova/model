# Table Inv_Transaction_Lines

Details records of Transactions. Each detail contains the movement for one product. Entity: Inv_Transaction_Lines

# Aggregate Hierarchy

* [Inv_Transactions](Inv_Transactions.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Transaction_Line_Id|`Guid`|`PK`, Readonly||
|Allow_Over_Execution|`Boolean`||When true, specifies, that we explicitly allow over-execution. Over-execution is when the quantity in all execution lines exceed the quantity in the parent store order line. `Required` `Default(false)` |
|Finished|`Boolean`||True if this transaction entry completes the operation. false if there might be more entries. `Default(false)` `Filter(eq)` |
|Guarantee_Period_Days|`Int32?`||Guarantee period in days for the offered product. null for non-serviced products. |
|Line_No|`Int32`||Line number, unique within the store transaction. `Required` |
|Notes|`String`||Notes for this StoreTransactionLine. |
|Parent_Line_Id|`Guid?`||Used, when transaction lines are generated directly from other entities (different from Store Order). Denotes the Id of the parent document line, which generated the transaction line. `Filter(multi eq)` |
|Parent_Line_No|`Int32?`||The number of the line within the parent document, which the current line executes. null when the current line does not execute line. |
|Temp_Order_No|`String`||Obsolete. Not used. `Filter(eq)` |
|Transaction_Timestamp|`DateTime?`||Exact time when the transaction changes the cost of the product. `Filter(ge;le)` `ORD` |
