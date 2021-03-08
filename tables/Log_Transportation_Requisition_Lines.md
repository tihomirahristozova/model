# Table Log_Transportation_Requisition_Lines

One line in a client requisition for transportation. Different lines usually represent requisitions for different cargo types. Entity: Log_Transportation_Requisition_Lines

# Aggregate Hierarchy

* [Log_Transportation_Requisitions](Log_Transportation_Requisitions.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Transportation_Requisition_Line_Id|`Guid`|`PK`, Readonly||
|Contents_Description|`String`||Textual description of the cargo contents. `Required` |
|Line_No|`Int32`||Line number, unique within the TransportationRequisition. Usually is increasing number like 10, 20, 30, ... when initially entering the TransportationRequisition (in order to allow insertions with adjustment documents). `Required` `Filter(eq)` |
|Pallets_Count|`Int32?`||Number of palettes comprising the cargo. null when it is unknown. |
|Parent_Line_No|`Int32?`||The number of the line within the parent document, which the current line executes. null when the current line does not execute another line. `Filter(eq)` |
|Volume_Cbm|`Int32?`||The volume of the cargo, in CBM (cubic meters). null when it is unknown. |
|Weight_Kg|`Int32?`||The weight of the cargo, in KG (kilogramms). null when it is unknown. |
