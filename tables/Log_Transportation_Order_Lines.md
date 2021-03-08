# Table Log_Transportation_Order_Lines

Different cargoes of a transportation order. Entity: Log_Transportation_Order_Lines

# Aggregate Hierarchy

* [Log_Transportation_Orders](Log_Transportation_Orders.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Transportation_Order_Line_Id|`Guid`|`PK`, Readonly||
|Contents_Description|`String`||Textual description of the cargo contents. `Required` |
|Line_No|`Int32`||Line number, unique within the TransportationOrder. Usually is increasing number like 10, 20, 30, ... when initially entering the TransportationOrder (in order to allow insertions with adjustment documents). `Required` `Filter(eq)` |
|Notes|`String`||Notes for this TransportationOrderLine. `Introduced in version 18.2` |
|Pallets_Count|`Int32?`||Number of palettes comprising the cargo. null when it is unknown. |
|Parent_Line_No|`Int32?`||The number of the line within the parent document, which the current line executes. null when the current line does not execute parent line. `Filter(eq)` |
|Volume_Cbm|`Int32?`||The volume of the cargo, in CBM (cubic meters). null when it is unknown. |
|Weight_Kg|`Int32?`||The weight of the cargo, in KG (kilogramms). null when it is unknown. |
