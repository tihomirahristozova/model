# Table Prd_Work_Order_Item_Ingredients

The materials consumed in the production order operations. Entity: Prd_Work_Order_Item_Ingredients

# Aggregate Hierarchy

* [Prd_Work_Orders](Prd_Work_Orders.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Distribute_By|`DistributeBy?`|Allowed: `SP`, `MC`, `SC`|Distribution method in case the materials from the line are distributed amongst all work order items. Should be NOT null iif Work_Order_Item_Id is null. MC=Measurement, SP=Standard_Price. |
|Line_Ord|`Int32`||The order of the line within the item. `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this WorkOrderItemIngredient. |
