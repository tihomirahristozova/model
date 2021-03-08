# Table Scm_Purchase_Order_Lines

Contains detail lines of purchase orders. Entity: Scm_Purchase_Order_Lines

# Aggregate Hierarchy

* [Scm_Purchase_Orders](Scm_Purchase_Orders.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Purchase_Order_Line_Id|`Guid`|`PK`, Readonly||
|Line_No|`Int32`||Line number, unique within the PurchaseOrder. Usually is increasing number like 10, 20, 30, ... when initially entering the PurchaseOrder (in order to allow insertions with adjustment documents). `Required` |
|Notes|`String`||Notes for this PurchaseOrderLine. |
|Parent_Line_No|`Int32?`||The number of the line within the parent document, which the current line executes. null when the current line does not execute line. `Filter(eq)` `Introduced in version 18.2` |
|Planned_Delivery_Date|`DateTime`||The planned delivery date for this line. `Required` `Filter(ge;le)` |
|Product_Description|`MultilanguageString`||The name of the ordered product, initially copied from the name in the product definition. The field can be edited by the user. `Required` `Filter(like)` |
