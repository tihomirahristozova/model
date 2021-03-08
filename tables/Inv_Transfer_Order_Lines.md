# Table Inv_Transfer_Order_Lines

Details of Transfer Orders. Each line contains order for the movement of one product. Entity: Inv_Transfer_Order_Lines

# Aggregate Hierarchy

* [Inv_Transfer_Orders](Inv_Transfer_Orders.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Transfer_Order_Line_Id|`Guid`|`PK`, Readonly||
|Due_Date_In|`DateTime`||The date, when the goods are expected to be received in the destination warehouse. Initially copied from the transfer header. `Required` `Filter(ge;le)` |
|Due_Date_Out|`DateTime`||When this line of the transfer is scheduled to issue the goods from the source warehouse. Initially copied from the transfer header. `Required` `Filter(ge;le)` |
|Line_Ord|`Int32`||Line ordinal position within the transaction. Duplicates are allowed, but not advised. `Required` |
|Notes|`String`||Notes for this TransferOrderLine. |
