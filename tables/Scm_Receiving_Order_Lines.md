# Table Scm_Receiving_Order_Lines

Contains detail records of Receiving Orders. Each line contains the receiving of a quantity of a product. Entity: Scm_Receiving_Order_Lines

# Aggregate Hierarchy

* [Scm_Receiving_Orders](Scm_Receiving_Orders.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Receiving_Order_Line_Id|`Guid`|`PK`, Readonly||
|Finished|`Boolean`||When true, denotes that this is the last receivement for this purchase order line and further receivements are not expected. `Required` `Default(false)` |
|Line_No|`Int32`||Line number, unique within the ReceivingOrder. Usually is increasing number like 10, 20, 30, ... when initially entering the ReceivingOrder (in order to allow insertions with adjustment documents). `Required` |
|Notes|`String`||Notes for this ReceivingOrderLine. |
|Product_Description|`MultilanguageString`||The name of the received product, initially copied from the name in the product definition. The field can be edited by the user. `Required` |
