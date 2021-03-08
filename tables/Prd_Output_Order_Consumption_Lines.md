# Table Prd_Output_Order_Consumption_Lines

The internal production consumption of materials. Used only for control purposes - for comparison with the active consumption orders. Warehouse and accounting are still updated only by Consumption Orders. Entity: Prd_Output_Order_Consumption_Lines

# Aggregate Hierarchy

* [Prd_Output_Orders](Prd_Output_Orders.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Output_Order_Consumption_Line_Id|`Guid`|`PK`, Readonly||
|Line_No|`Int32`||Line number, unique within the OutputOrder. Usually is increasing number like 10, 20, 30, ... when initially entering the OutputOrder (in order to allow insertions with adjustment documents). `Required` |
|Notes|`String`||Notes for this OutputOrderConsumptionLine. |
