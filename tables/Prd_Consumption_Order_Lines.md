# Table Prd_Consumption_Order_Lines

Detail lines of orders for material consumption. Entity: Prd_Consumption_Order_Lines

# Aggregate Hierarchy

* [Prd_Consumption_Orders](Prd_Consumption_Orders.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Consumption_Type|`ConsumptionType`|Allowed: `S`, `A`, Readonly|Determines whether the material cost is distributed among all produced products, or only one (specified in the Work Order Item Ingredient). `Required` `Filter(eq)` `ReadOnly` |
|Line_Ord|`Int32`||Non-unique line number within the order. `Required` |
|Notes|`String`||Notes for this ConsumptionOrderLine. |
|Scheduled_Date_Time|`DateTime?`||The scheduled date, when the material is needed. `Filter(ge;le)` |
