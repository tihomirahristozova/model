# Table Prd_Output_Order_Lines

Detail records of output orders. Entity: Prd_Output_Order_Lines

# Aggregate Hierarchy

* [Prd_Output_Orders](Prd_Output_Orders.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|End_Time|`DateTime`||Date and time when the operation has ended. `Required` `Default(Now)` `Filter(ge;le)` |
|Finished|`Boolean`||True if this output entry completes the operation. false if there might be more entries. `Required` `Default(false)` `Filter(eq)` |
|Line_Ord|`Int32`||Line number within the order. `Required` |
|Notes|`String`||Notes for this OutputOrderLine. |
|Start_Time|`DateTime`||Date and time when the operation has began. `Required` `Default(Now)` `Filter(ge;le)` |
|Transaction_Timestamp|`DateTime?`|Readonly|Sets the timestamp of the receipt store operations for this output order line. Used in completing output orders. `ReadOnly` |
